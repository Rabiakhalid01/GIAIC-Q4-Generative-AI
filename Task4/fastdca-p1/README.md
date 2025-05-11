 API Parameters
This step focuses on the different ways to receive and validate parameters in your FastAPI application. We'll cover path parameters, query parameters, and request bodies with enhanced validation using FastAPI's built-in functionality.

Types of Parameters in FastAPI
FastAPI provides several ways to declare and validate parameters:

1.Path Parameters: Parts of the URL path that are variable (e.g., /items/{item_id})
2.Query Parameters: Parameters appended to the URL after a ? (e.g., /items?skip=0&limit=10)
3.Request Body: Data sent in the body of the request (usually in JSON format)
4.Headers: Custom HTTP headers sent with the request
5.Cookies: Data sent in the Cookie header
6.Form Data: Fields submitted in a form
7.File Uploads: Files uploaded in a form


Key Points to Remember
1.Use Path() for validating path parameters
2.Use Query() for validating query parameters
3.Both Path() and Query() support various validation options:
 i. ge, gt, le, lt for numerical constraints
 ii. min_length, max_length for string length
 iii. regex or pattern for pattern matching
 iv. enum for restricting to a set of values
FastAPI will automatically validate all parameters according to your specifications
When validation fails, FastAPI returns a 422 Unprocessable Entity status code with detailed error information