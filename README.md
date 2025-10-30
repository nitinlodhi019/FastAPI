# (Pydantic Model)[https://github.com/nitinlodhi019/Pydantic]

# API

An API stands for Application Programming Interface.

**In simple words:**

API is a way for two software applications to talk to each other and share data or services.

<img width="1000" height="470" alt="image" src="https://github.com/user-attachments/assets/a08eb0fd-173b-44a0-8ff7-83d95e8de5ff" />


# FastAPI
FastAPI is a modern, fast (high-performance) Python web framework used for building APIs and backend applications.

It is built on top of **Starlette** (for the web parts) and **Pydantic** (for data validation).

# Path Parameters(Required)
In FastAPI, path parameters are used to define dynamic segments within a URL path, allowing an API endpoint to handle requests for specific resources identified by values in the URL.

## Path()
In FastAPI, Path() is a special dependency function used within path operation functions to define and validate path parameters. While FastAPI can automatically infer path parameters from type hints in your function signatures, Path() provides additional functionality for defining extra validation rules, metadata, and default values for those parameters.

## Declaration:
Path parameters are declared in the path string of a route decorator using curly braces {}. The name inside the braces corresponds to a parameter in the associated path operation function.
```bash
from fastapi import FastAPI

app = FastAPI()

@app.get("/items/{item_id}")
async def read_item(item_id: int):
    return {"item_id": item_id}
```

# HTTP status codes
HTTP status codes are three-digit numbers returned by a web server in response to a client's request. These codes, part of the Hypertext Transfer Protocol (HTTP), communicate the outcome of the request, indicating whether it was successful, redirected, or resulted in an error. 

<img width="999" height="393" alt="image" src="https://github.com/user-attachments/assets/b5da839a-c502-4351-bd6d-19f91982f9e4" />

## HTTP status codes
* **2xx Successful responses:** Indicate that the request was successfully received, understood, and accepted. Examples include:
    * **200 OK:** The request has succeeded.
    * **201 Created:*** The request has been fulfilled and resulted in a new resource being created.
    * **204 No Content:** The server successfully processed the request, but is not returning any content.
      
* **3xx Redirection messages:** Indicate that further action needs to be taken by the user agent to fulfill the request. Examples include:
    * **301 Moved Permanently:** The requested resource has been permanently moved to a new URL.
    * **302 Found:** The requested resource has been temporarily moved to a different location.
    * **304 Not Modified:** Indicates that the client's cached version of the resource is still valid.
      
* **4xx Client error responses:** Indicate that the client's request contains an error or cannot be fulfilled. Examples include:
    * **400 Bad Request:** The server cannot process the request due to a client error (e.g., malformed syntax). 
    * **401 Unauthorized:** The client must authenticate to get the requested response. 
    * **403 Forbidden:** The client does not have access rights to the content.
    * **404 Not Found:** The server cannot find the requested resource.
      
* **5xx Server error responses:** Indicate that the server failed to fulfill a request due to an error on the server's part. Examples include:
    * **500 Internal Server Error:** A generic error message, given when an unexpected condition was encountered and no more specific message is suitable.
    * **502 Bad Gateway:** The server, while acting as a gateway or proxy, received an invalid response from an upstream server.
    * **503 Service Unavailable:** The server is currently unable to handle the request due to temporary overload or scheduled maintenance.

# HTTPException
In FastAPI, HTTPException is a special type of exception used to signal HTTP-specific errors to the client. When an HTTPException is raised within a path operation function or a dependency, FastAPI automatically catches it and generates an appropriate HTTP response. This response includes the specified HTTP status code and a JSON payload containing the error details.

# Query Parameters(Optional)
In FastAPI, query parameters are key-value pairs that are included in the URL after a question mark (?) and separated by ampersands (&). They are used to pass **optional** data to an endpoint, typically for filtering, sorting, or paginating results.

## Query()
In FastAPI, Query() is a special dependency function used to declare and validate query parameters in your API endpoints. It allows you to define more specific behaviors and validations for your query parameters than simply type-hinting them.
