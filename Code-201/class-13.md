# Class 13

## Local Storage

Sometimes we will find the need to store data in local storage in order to have long lasting webpage interactions.  
Local storage, in comparison to cookies, is written to the user's disk and, in comparison to session storage, survives when the page is closed.  
Local storage allows the user to interact with their own unique changes to their webpage over multiple sessions. Any data that are sensitive or small and/or needed to be seen server side, use cookies. Any information that should be lost upon session end, say like remaining logged in to a website while you are using it. Local storage can probably used for everything else.

Local storage has a limitation of only storing strings. This means any arrays or other objects can't exactly be stored, at least not directly. One way around this is to change the objects into strings using JSON.stringify() and then translating them back into objects using JSON.parse().

That being said, local storage can also prove to be a massive privacy and security issue. Use with responsibility and caution.

Short notes.

## Things I want to know more about
