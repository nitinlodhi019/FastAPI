# API

An API stands for Application Programming Interface.

**In simple words:**

API is a way for two software applications to talk to each other and share data or services.

<img width="1000" height="470" alt="image" src="https://github.com/user-attachments/assets/a08eb0fd-173b-44a0-8ff7-83d95e8de5ff" />


# FastAPI

FastAPI is a modern, fast (high-performance) Python web framework used for building APIs and backend applications.

It is built on top of **Starlette** (for the web parts) and **Pydantic** (for data validation).

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
