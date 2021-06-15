## Django Custom User

- There are two modern ways to create a custom user model in Django: `AbstractUser` and `AbstractBaseUser`. In both cases we can subclass them to extend existing functionality however AbstractBaseUser requires much more work. 

*- **Note**: that we did not run migrate to configure our database. It's important to wait until after we've created our new custom user model before doing so.*

### Custom User Model

- Creating our initial custom user model requires four steps:

   1. update `settings.py`.
        - In `settings.py` we'll add the accounts app and use the `AUTH_USER_MODEL` config to tell Django to use our new custom user model in place of the built-in User model. 
        - Within `INSTALLED_APPS` add accounts at the bottom. Then at the bottom of the entire file, add the `AUTH_USER_MODEL` config.

   2. create a new `CustomUser` model.

   3. create new `UserCreation` and `UserChangeForm`.

   4. update the admin.
   

## DjangoX

- **DjangoX**, which is an open-source Django starter framework that includes a custom user model, "email/password" by default instead of "username/email/password", social authentication, and more.

- DjangoX can be installed via Pip, Pipenv, or Docker depending upon your setup. To start, clone the repo to your local computer and change into the proper directory.

```
    $ git clone https://github.com/wsvincent/djangox.git
    $ cd djangox
```

- pip

```
    $ python3 -m venv djangox
    $ source djangox/bin/activate
    (djangox) $ pip install -r requirements.txt
    (djangox) $ python manage.py migrate
    (djangox) $ python manage.py createsuperuser
    (djangox) $ python manage.py runserver
    # Load the site at http://127.0.0.1:8000
```