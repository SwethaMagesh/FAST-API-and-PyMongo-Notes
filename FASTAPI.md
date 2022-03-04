# FAST API
- Open source
- Like Flask for fast backend servers
- Best for REST APIs to send to clients in json format
- Comparable to Node js in speed
- Uses uvicorn or hypercorn services
-  `@app.get('/route/{param}')` for setting endpoints
- Functions defined to return for each route
- Add type check for param in functions => Eg:`def get_root(param:int):`
- Try using virtual env ( like pipenv)
    - `pipenv shell`
    - `pipenv install`
    (instead of pip install)

## Uvicorn
- works as server
- `uvicorn main:app --reload` to run main.py and app FASTAPI object
- --reload only for developemnt

## API Operations 
- Post, get, put, delete
- Options, head, patch, trace
- **PATH OPERATION DECORATOR**
    - @app.get('route') = `this tells python fastapi that the function below is for handling requests to that path/route/endpoint
- **PATH OPERATION FUNCTION**
    - def function below the decorator

##


## Python Types Intro
- [Sources](https://fastapi.tiangolo.com/python-types/)
- Helps declate types of variable
- eg: `def get_full_name(first_name: str, last_name: str)`
- Examples are ***int, float, bool, bytes, str***
- Module in python called **typing** for *generic* like list, dict, set, tuple
    - `from typing import List`
    - `def fun(items: List[str]):`
    - here str is called *type parameter*
- **Union** for multiple types alternatives 
- **Optional** if it can be null too
- **Classes** can be declared as types too
- **Pydantic library** for data validation
    ```
    class User(BaseModel):
        id:int
        time:Optional(datetime) = None
        friends: List[int] = []
    
    user = User(data)
    ```




## Benefits 
- Validation is much easier and mostly done by self
- Doc of Apis and testing is very easy. Good communication with frontend team
    - `localhost:8000/docs` or `localhost:8000/redoc`
- Compact code with less errors
- JSON conversion simple at end


## Explore more
- FAST API documentation
- Uvicorn vs hypercorn
- Async functions vs normal functions for returning to json
    - [Concurrency and Async/Await](https://fastapi.tiangolo.com/async/#in-a-hurry)
- PIPENV vs other virtual env, how to deactivate etc., why pipfile
- Enum class and Typing Optional, BaseModel in pydantic etc.
- Forms in FastAPI
- Decorations like @ and their uses in python
```
That @something syntax in Python is called a "decorator". 
You put it on top of a function. Like a pretty decorative hat.
A "decorator" takes the function below and does something with it.
```
- API best practices (hitesh if possible)

## Videos
- [Jerin Jose Tutorial](https://www.youtube.com/playlist?list=PL4iRawDSyRvWybsXRTommb3acUigWPEsj)
- [Crash course - Hitesh](https://www.youtube.com/watch?v=TQfIUS52QHA&list=PLQ7ByHR1RaCNLxS-y-7gXJsrWJjgtGXlb&index=3)
