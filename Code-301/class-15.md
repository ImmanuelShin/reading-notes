# Class 15

## Authentication

### OAuth

Authentication is import to maintain security. That's where authentication comes in. The bad actors who would otherwise have access to everything now need to work hard to steal things.

OAuth is an open-standard authorization protocol that describes how unrelated servers and services can safely allow authenticated access to their assets without actually sharing the actual logon credential.  
A simple example of OAuth would be when you log onto a website and it offers some amount of opportunities to log in using another website's/service's login. You'd choose a different service, like google or facebook, and gain permission to access the website.

It works like this:

- The first website connects to the second website on behalf of the user, using OAuth, providing the user’s verified identity.
- The second site generates a one-time token and a one-time secret unique to the transaction and parties involved.
- The first site gives this token and secret to the initiating user’s client software.
- The client’s software presents the request token and secret to their authorization provider (which may or may not be the second site).
- If not already authenticated to the authorization provider, the client may be asked to authenticate. After authentication, the client is asked to approve the authorization transaction to the second website.
- The user approves (or their software silently approves) a particular transaction type at the first website.
- The user is given an approved access token (notice it’s no longer a request token).
- The user gives the approved access token to the first website.
- The first website gives the access token to the second website as proof of authentication on behalf of the user.
- The second website lets the first website access their site on behalf of the user.
- The user sees a successfully completed transaction occurring.
- OAuth is not the first authentication/authorization system to work this way on behalf of the end-user. In fact, many authentication systems, notably Kerberos, work similarly. What is special about OAuth is its ability to work across the web and its wide adoption. It succeeded with adoption rates where previous attempts failed (for various reasons).

[source](https://www.csoonline.com/article/562635/what-is-oauth-how-the-open-authorization-framework-works.html)

OpenID is an alternative security technology that is conceptually at a higher level than OAuth. Where OAuth works with machines to log in humans, OpenID is more for humans to log in humans.  
The idea was that OpenID would serve as a central point of sign in, rather than allowing multiple different service sign-ins. It fell out of favor because OpenID was essentially a less popular Facebook, but it has found its niche in being an authentication layer for OAuth.

### Authorization/Authentication Flows

| Authorization  | Authentication  |
|---|---|
| Determines what users can and cannot access  |  Determines whether users are who they claim to be |
| Verifies whether access is allowed through policies and rules  | Challenges the user to validate credentials (for example, through passwords, answers to security questions, or facial recognition)  |
| Usually done after successful authentication | Usually done before authorization  |
| Generally, transmits info through an Access Token  | Generally, transmits info through an ID Token |
| Generally governed by the OAuth 2.0 framework  | Generally governed by the OpenID Connect (OIDC) protocol	  |
| Example: After an employee successfully authenticates, the system determines what information the employees are allowed to access  |  Example: Employees in a company are required to authenticate through the network before accessing their company email |

#### Authorization Code Flow

- User selects Login within application.
- Auth0's SDK redirects user to Auth0 Authorization Server (/authorize endpoint).
- Auth0 Authorization Server redirects user to login and authorization prompt.
- User authenticates using one of the configured login options, and may see a consent prompt listing the permissions Auth0 will give to the application.
- Auth0 Authorization Server redirects user back to application with single-use authorization code.
- Auth0's SDK sends authorization code, application's client ID, and application's credentials, such as client secret or Private Key JWT, to Auth0 Authorization Server (/oauth/token endpoint).
- Auth0 Authorization Server verifies authorization code, application's client ID, and application's credentials.
- Auth0 Authorization Server responds with an ID token and access token (and optionally, a refresh token).
- Application can use the access token to call an API t

#### Authorization Code Flow with Proof Key for Code Exchange (PKCE)

- The user clicks Login within the application.
- Auth0's SDK creates a cryptographically-random code_verifier and from this generates a code_challenge.
- Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) along with the code_challenge.
- Your Auth0 Authorization Server redirects the user to the login and authorization prompt.
- The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the application.
- Your Auth0 Authorization Server stores the code_challenge and redirects the user back to the application with an authorization code, which is good for one use.
- Auth0's SDK sends this code and the code_verifier (created in step 2) to the Auth0 Authorization Server (/oauth/token endpoint).
- Your Auth0 Authorization Server verifies the code_challenge and code_verifier.
- Your Auth0 Authorization Server responds with an ID token and access token (and optionally, a refresh token).
- Your application can use the access token to call an API to access information about the user.
- The API responds with requested data.

#### Implicit Flow with Form Post

- The user clicks Login in the app.
- Auth0's SDK redirects the user to the Auth0 Authorization Server (/authorize endpoint) passing along a response_type parameter of id_token that indicates the type of requested credential. It also passes along a response_mode parameter of form_post to ensure security.
- Your Auth0 Authorization Server redirects the user to the login and authorization prompt.
- The user authenticates using one of the configured login options and may see a consent page listing the permissions Auth0 will give to the app.
- Your Auth0 Authorization Server redirects the user back to the app with an ID Token.

#### Client Credentials Flow

- Application sends application's credentials to the Auth0 Authorization Server. To learn more about client authentication methods.
- Auth0 Authorization Server validates application's credentials.
- Auth0 Authorization Server responds with an access token.
- Application can use the access token to call an API on behalf of itself.
- API responds with requested data.

#### Device Authorization Flow

##### Device Flow

- The user starts the app on the device.

- The device app requests authorization from the Auth0 Authorization Server using its Client ID (/oauth/device/code endpoint).

- The Auth0 Authorization Server responds with a device_code, user_code, verification_uri, verification_uri_complete expires_in (lifetime in seconds for device_code and user_code), and polling interval.

- The device app asks the user to activate using their computer or smartphone. The app may accomplish this by:

  - asking the user to visit the verification_uri and enter the user_code after displaying these values on-screen

  - asking the user to interact with either a QR Code or shortened URL with embedded user code generated from the verification_uri_complete

  - directly navigating to the verification page with embedded user code using verification_uri_complete, if running natively on a browser-based device

- The device app begins polling your Auth0 Authorization Server for an Access Token (/oauth/token endpoint) using the time period specified by interval and counting from receipt of the last polling request's response. The device app continues polling until either the user completes the browser flow path or the user code expires.

- When the user successfully completes the browser flow path, your Auth0 Authorization Server responds with an Access Token (and optionally, a Refresh Token). The device app should now forget its device_code because it will expire.

- Your device app can use the Access Token to call an API to access information about the user.

- The API responds with requested data.

##### Browser Flow

- The user visits the verification_uri on their computer, enters the user_code and confirms that the device that is being activated is displaying the user_code. If the user visits the verification_uri_complete by any other mechanism (such as by scanning a QR code), only the device confirmation will be needed.

- Your Auth0 Authorization Server redirects the user to the login and consent prompt, if needed.

- The user authenticates using one of the configured login options and may see a consent page asking to authorize the device app.

- Your device app is authorized to access the API.

#### Resource Owner Password Flow

- The user clicks Login within the application and enters their credentials.

- Your application forwards the user's credentials to your Auth0 Authorization Server (/oauth/token endpoint).

- Your Auth0 Authorization Server validates the credentials.

- Your Auth0 Authorization Server responds with an Access Token (and optionally, a Refresh Token).

- Your application can use the Access Token to call an API to access information about the user.

- The API responds with requested data.

[source](https://auth0.com/docs/get-started/authentication-and-authorization-flow#client-credentials-flow)

## Things I want to know more about
