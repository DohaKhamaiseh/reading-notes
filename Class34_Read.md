## What are the key principles to follow when organizing and configuring Django settings for a project, according to the “Django Settings Best Practices” reading?

- Keep settings in environment variables.
  
- Write default values for production configuration (excluding secret keys and tokens).
  
- Don’t hardcode sensitive settings, and don’t put them in VCS.
  
- Split settings into groups: Django, third-party, project.
  
- Follow naming conventions for custom (project) settings.


## How does the White Noise library contribute to the efficient serving of static files in a Django application, and what are the steps to integrate it into a project?

### How?
It allows us to serve static files directly from our web server rather than relying on Django itself to handle static file serving. This can significantly improve the performance and scalability of our application.

### What?

1. Install WhiteNoise : ```pip install whitenoise```
   
2. Update Django settings : 
```
 MIDDLEWARE = [
    # ...
    'django.middleware.security.SecurityMiddleware',
    'whitenoise.middleware.WhiteNoiseMiddleware',
    # ...
] 

```

3. Collect static files: ```python manage.py collectstatic```


## What is the purpose of Cross-Origin Resource Sharing (CORS) in web applications, and how can it be implemented and configured in a Django project to control access to resources?


### What?
The purpose of CORS is to enable controlled access to resources from different domains, while still maintaining the security of the same-origin policy. 

It allows web servers to respond to cross-origin requests with appropriate permissions and headers, determining whether the requesting domain should be allowed to access the requested resources.

### How?

1. Install the Django CORS headers package : ```pip install django-cors-headers```

2. Update Django settings : 

```
INSTALLED_APPS = [
    # ...
    'corsheaders',
    # ...
]

MIDDLEWARE = [
    'corsheaders.middleware.CorsMiddleware',
    # ...
]


CORS_ORIGIN_ALLOW_ALL = False  # Set to True to allow all origins
CORS_ORIGIN_WHITELIST = [
    'http://example.com',  # Add your whitelisted domains here
    'https://example.com',
]

CORS_ALLOW_METHODS = [
    'GET',
    'POST',
    'PUT',
    'PATCH',
    'DELETE',
    'OPTIONS',
]

```

3. Save and restart the Django server


