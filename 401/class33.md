## JSON Web Tokens

**JSON Web Token (JWT)** is an open standard (RFC 7519) that defines a compact and self-contained way for securely transmitting information between parties as a JSON object. This information can be verified and trusted because it is digitally signed. JWTs can be signed using a secret (with the HMAC algorithm) or a public/private key pair using RSA or ECDSA.

- **Authorization**: This is the most common scenario for using JWT. Once the user is logged in, each subsequent request will include the JWT, allowing the user to access routes, services, and resources that are permitted with that token. Single Sign On is a feature that widely uses JWT nowadays, because of its small overhead and its ability to be easily used across different domains.


- JSON Web Tokens consist of three parts separated by dots (.), which are:

    1. **Header**

    The header typically consists of two parts: the type of the token, which is JWT, and the signing algorithm being used, such as HMAC SHA256 or RSA.

    2. **Payload**
    
    The payload contains the claims. Claims are statements about an entity (typically, the user) and additional data. There are three types of claims:

        - Registered claims: These are a set of predefined claims which are not mandatory but recommended, to provide a set of useful, interoperable claims.

        > Notice that the claim names are only three characters long as JWT is meant to be compact.

        - Public claims: These can be defined at will by those using JWTs. But to avoid collisions they should be defined in the IANA JSON Web Token Registry or be defined as a URI that contains a collision resistant namespace.

        - Private claims: These are the custom claims created to share information between parties that agree on using them and are neither registered or public claims.

    > Do note that for signed tokens this information, though protected against tampering, is readable by anyone. Do not put secret information in the payload or header elements of a JWT unless it is encrypted.

    3. **Signature**
    To create the signature part you have to take the encoded header, the encoded payload, a secret, the algorithm specified in the header, and sign that.

    The signature is used to verify the message wasn't changed along the way, and, in the case of tokens signed with a private key, it can also verify that the sender of the JWT is who it says it is.

![](https://miro.medium.com/max/6216/1*u3a-5xZDeudKrFGcxHzLew.png)


## DRF JWT Authentication

The JWT is acquired by exchanging an username + password for an access token and an refresh token.

- The **access token** is usually short-lived (expires in 5 min or so, can be customized though).

- The **refresh token** lives a little bit longer (expires in 24 hours, also customizable). It is comparable to an authentication session. After it expires, you need a full login with username + password again.

![](https://miro.medium.com/max/630/1*IqAodJn46th31XLkU5Qf1w.jpeg)

### Setup
- For setup we should install `djangorestframework_simplejwt` library.

- settings.py
```
REST_FRAMEWORK = {
    'DEFAULT_AUTHENTICATION_CLASSES': [
        'rest_framework_simplejwt.authentication.JWTAuthentication',
    ],
}
```

- urls.py
```
from django.urls import path
from rest_framework_simplejwt import views as jwt_views

urlpatterns = [
    # Your URLs...
    path('api/token/', jwt_views.TokenObtainPairView.as_view(), name='token_obtain_pair'),
    path('api/token/refresh/', jwt_views.TokenRefreshView.as_view(), name='token_refresh'),
]
```

### Example

- views.py

```
from rest_framework.views import APIView
from rest_framework.response import Response
from rest_framework.permissions import IsAuthenticated


class HelloView(APIView):
    permission_classes = (IsAuthenticated,)

    def get(self, request):
        content = {'message': 'Hello, World!'}
        return Response(content)
```

- urls.py

```from django.urls import path
from myapi.core import views

urlpatterns = [
    path('hello/', views.HelloView.as_view(), name='hello'),
```