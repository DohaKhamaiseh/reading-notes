## What are the key components and purpose of Django Rest Framework (DRF) permissions, and how do they help in securing an API?


1. **Authentication:** DRF includes various authentication classes that handle the process of authenticating incoming requests. Authentication ensures that the user making the request is who they claim to be.


<br>

2. **Permissions:** DRF provides a range of permission classes that determine whether a user is allowed to perform a certain action on a particular resource. Permissions can be applied at the view level or the object level. View-level permissions control access to entire views or sets of views, while object-level permissions allow you to specify permissions on individual objects within a view.

     - Example view-level permissions: IsAuthenticated, AllowAny, IsAdminUser, etc.
    
      - Example object-level permissions: IsOwner, IsAuthenticatedOrReadOnly, etc.


<br>


3. **Filtering:** DRF includes filtering capabilities that allow us to control which data is exposed through your API. Filtering allows us to restrict the data returned based on query parameters.

<br>
   
   
## In SQL, what is the purpose of the SELECT statement, and how would you use it to retrieve all columns from a table called ‘employees’?

<br>

### Purpose:

In SQL, the SELECT statement is used to retrieve data from one or more database tables.

<br>

### Example:

```SELECT * FROM employees;```

<br>


## Can you explain the role of DRF Generic Views and provide examples of their usage in building a RESTful API?

<br>

### Role:

The role of DRF Generic Views is to handle common HTTP methods and provide default behavior for various operations. 

<br>

### Examples:

```


from rest_framework  import generics 
from .models import Word
from .serializers import WordSerializer

class WordDetail(generics.RetrieveUpdateDestroyAPIView):
    queryset = Word.objects.all()
    serializer_class = WordSerializer
```

