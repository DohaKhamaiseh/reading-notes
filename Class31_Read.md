## What are the key components of a Docker container, and how do they help streamline the development and deployment of applications?

### Components :



1. **Docker Image:** A Docker image is a lightweight, standalone, and executable software package that includes everything needed to run an application, including the code, runtime, libraries, tools, and system dependencies. Images are built based on a Dockerfile, which defines the instructions for creating the image.

2. **Docker Container:** A Docker container is an instance of a Docker image. It is a runtime environment that encapsulates the application and its dependencies in an isolated and portable manner. Containers are isolated from each other and from the host system, providing a consistent and predictable runtime environment. 

3. **Docker Registry:** A Docker registry is a central repository that stores Docker images. It allows US to share, distribute, and manage our images. 

## Describe the primary steps involved in building a library website using Django, including essential components like models, views, and templates.

1. Setting Up the Django Project:

    1. Install Django.
  
    2. Create a Django Project.
     
    3. Set Up Database.
     
2. Designing the Data Models:

    1. Define Models
   
    2.  Migrations.
  
    3. Apply Migrations.
  
3. Creating Views:

   1. Define Views.

   2. URL Mapping.
     
4. Building Templates:

   1. Create Templates.
     
   2. Template Inheritance.
     
5. Handling Forms:

   1. Create Forms.
     
   2. Form Processing.
  
6. Implementing User Authentication and Authorization:

   1. User Registration.
     
   2. Login and Logout.
     
   3. Authorization.
   
## Can you explain the primary differences between Django and Django REST framework?

- Django REST Framework works alongside the Django web framework to create web APIs. We cannot build a web API with only Django Rest Framework. It always must be added to a project after Django itself has been installed and configured.

- Django creates websites containing webpages, while Django REST Framework creates web APIs which are a collection of URL endpoints containing available HTTP verbs that return JSON.