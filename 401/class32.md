# Permissions


- Together with authentication and throttling, permissions determine whether a request should be granted or denied access.

- Permission checks are always run at the very start of the view, before any other code is allowed to proceed. Permission checks will typically use the authentication information in the `request.user` and `request.auth` properties to determine if the incoming request should be permitted.

- Permissions are used to grant or deny access for different classes of users to different parts of the API.

- The simplest style of permission would be to allow access to any authenticated user, and deny access to any unauthenticated user. This corresponds to the `IsAuthenticated` class in REST framework.

- A slightly less strict style of permission would be to allow full access to authenticated users, but allow read-only access to unauthenticated users. This corresponds to the `IsAuthenticatedOrReadOnly` class in REST framework.

- Permissions in REST framework are always defined as a list of permission classes. Before running the main body of the view each permission in the list is checked. If any permission check fails an exceptions. `PermissionDenied` or exceptions.`NotAuthenticated` exception will be raised, and the main body of the view will not run.

-The default permission policy may be set globally, using the DEFAULT_PERMISSION_CLASSES setting. For example.

```
REST_FRAMEWORK = {
    'DEFAULT_PERMISSION_CLASSES': [
        'rest_framework.permissions.IsAuthenticated',
    ]
}
```


- If not specified, this setting defaults to allowing unrestricted access:

```
'DEFAULT_PERMISSION_CLASSES': [
   'rest_framework.permissions.AllowAny',
]
```

### API Reference

1. AllowAny: allow unrestricted access, regardless of if the request was authenticated or unauthenticated.

2. IsAuthenticated: deny permission to any unauthenticated user, and allow permission otherwise.

3. IsAdminUser: deny permission to any user, unless user.is_staff is True in which case permission will be allowed.

4. IsAuthenticatedOrReadOnly: authenticated users to perform any request. Requests for unauthorised users will only be permitted if the request method is one of the "safe" methods; GET, HEAD or OPTIONS.

