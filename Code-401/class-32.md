# Class 32

## DRF
- **Purpose:** DRF permissions, with authentication and throttling, control API access.
- **Components:**
  - **Global Permissions:** Determine access at the view level.
  - **Object Level Permissions:** Decide if a user can act on a specific object.

### Permission Determination
- Permissions are a list of classes checked before the main view code.
- Object-level permissions run when `.get_object()` is called.

### Limitations
- Object-level permissions aren't applied to each instance in a queryset for list views.
- Custom handling needed for object-level permissions during object creation.

### Setting Permission Policy
- Set globally with `DEFAULT_PERMISSION_CLASSES` or per-view using `permission_classes`.

### Provided Permission Classes
1. **AllowAny:** Unrestricted access.
2. **IsAuthenticated:** Denies access to unauthenticated users.
3. **IsAdminUser:** Allows only users with `is_staff` set to True.
4. **IsAuthenticatedOrReadOnly:** Allows any request for authenticated users; read-only for others.
5. **DjangoModelPermissions:** Tied to Django's model permissions.
6. **DjangoObjectPermissions:** Tied to Django's object permissions.

### Custom Permissions
- Inherit from `BasePermission` and implement `has_permission` and/or `has_object_permission`.
- Raise `PermissionDenied` on failure.

### Example
```python
class BlocklistPermission(BasePermission):
    def has_permission(self, request, view):
        # Check if the request's IP is blocked
        blocked = Blocklist.objects.filter(ip_addr=request.META['REMOTE_ADDR']).exists()
        return not blocked

class IsOwnerOrReadOnly(BasePermission):
    def has_object_permission(self, request, view, obj):
        return request.method in SAFE_METHODS or obj.owner == request.user
```

## SQL

### SELECT
The SELECT statement in SQL is used to retrieve data from one or more tables in a database. It allows users to specify the columns they want to retrieve and apply conditions to filter the data.

### Example
To retrieve all columns from the 'employees' table, you can use the following SQL query:

```sql
SELECT *
FROM employees;
```

## DRF Again

### Generic Views

Django Rest Framework (DRF) Generic Views serve as a shortcut for common view development patterns. They abstract common idioms and patterns, enabling quick development of API views without redundancy. These views are class-based and allow for the composition of reusable behavior.

### Basic Configuration
When using generic views, you typically override the view and set class attributes. For example:

```python
from django.contrib.auth.models import User
from myapp.serializers import UserSerializer
from rest_framework import generics
from rest_framework.permissions import IsAdminUser

class UserList(generics.ListCreateAPIView):
    queryset = User.objects.all()
    serializer_class = UserSerializer
    permission_classes = [IsAdminUser]
```

## Things I want to know more about