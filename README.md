# Django Rest Api Postman
## by Chau The Khanh 


### Technology
- Python 3.7
- Django 2.1.15
- Django Rest Framework 3.11.0
- django-cors-headers 3.2.1


### 1.Install Django REST framework
```bash
pip install djangorestframework
pip install django-cors-headers
```

### 2.Setup new Django project
- Let’s create a new Django project with command:
```bash
django-admin startproject DjangoRestApi
```

### 3.Setup new Django app for CRUD Rest Api
- Run following commands to create new Django app tutorials:
```bash
cd DjangoRestApi
python manage.py startapp tutorials
```

### 4.Migrate Data Model to the database
- Run the Python script:
```bash
cd DjangoRestApi
python manage.py makemigrations tutorials
```
- The console will show:
```bash
Migrations for 'tutorials':
  tutorials\migrations\0001_initial.py
    - Create model Tutorial
```
- To apply the generated migration above, run the following Python script:
```bash
cd DjangoRestApi
python manage.py migrate tutorials
```
```bash
Operations to perform:
Apply all migrations: tutorials
Running migrations:
  Applying tutorials.0001_initial... OK
```

### 5.Test the CRUD with APIs
- Run our Django Project with command:
```bash
python manage.py runserver 8080
```
It starts development server at `http://127.0.0.1:8080/` or `http://localhost:8080/.`
Using Postman, we’re gonna test all the Apis above.
- 1. `POST` `/tutorials Api`: Create a new Tutorial
- 2. `GET` `/tutorials Api`: Retrieve all Tutorials
- 3. `GET` `/tutorials/`:id Api: Retrieve a single Tutorial by id
- 4. `PUT` `/tutorials/`:id Api: Update a Tutorial
- 5. `GET` `/tutorials?title=res`: Find all Tutorials which title contains ‘res’
- 6. `GET` `/tutorials/published Api`: Find all published Tutorials
- 7. Delete a Tutorial using `DELETE` `/tutorials/`:id Api
- 8. Delete all Tutorials using `DELETE` `/tutorials` Api