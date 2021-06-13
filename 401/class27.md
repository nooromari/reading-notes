# Django Models

- Django web applications access and manage data through Python objects referred to as models.

- Models define the structure of stored data, including the field types and possibly also their maximum size, default values, selection list options, help text for documentation, label text for forms, etc. 

- The definition of the model is independent of the underlying database  you just write your model structure and other code, and Django handles all the dirty work of communicating with the database for you.

![](https://djangobook.com/wp-content/uploads/Django_ORM_600.png)

## Designing the LocalLibrary models

When designing your models it makes sense to have separate models for every "object" (a group of related information). In this case, the obvious objects are books, book instances, and authors.

Once we've decided on our models and field, we need to think about the relationships. Django allows you to define relationships that are one to one (OneToOneField), one to many (ForeignKey) and many to many (ManyToManyField).

With that in mind, the UML association diagram below shows the models we'll define in this case (as boxes).

![](https://developer.mozilla.org/en-US/docs/Learn/Server-side/Django/Models/local_library_model_uml.svg)

The diagram also shows the relationships between the models, including their multiplicities. The multiplicities are the numbers on the diagram showing the numbers (maximum and minimum) of each model that may be present in the relationship. 


## Model primer

Models are usually defined in an application's `models.py` file. They are implemented as subclasses of `django.db.models`.Model, and can include fields, methods and metadata. 
