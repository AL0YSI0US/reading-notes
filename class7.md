# Code 301 Reading Notes

## Class 07

[<== Previous Lesson](class6.md) [Next Lesson ==>](class8.md)

[<== Home](README.md) 🏠


## Api Design best practices 

> One of the primary motivations behind REST is that it should be  possible to navigate the entire set of resources without requiring prior knowledge of the URI scheme. 
> Each HTTP GET request should return the information necessary to find the resources related directly to the requested object through hyperlinks included in the response, 
> and it should also be provided with information that describes the operations available on each of these resources. This principle is known as HATEOAS, or Hypertext as the Engine of 
> Application State. The system is effectively a finite state machine, and the response to each request contains the information necessary to move from one state to another; no other  
> information should be necessary.

**Define operations in terms of HTTP methods**

The HTTP protocol defines a number of methods that assign semantic meaning to a request. 

> The common HTTP methods used by most RESTful web APIs are:

> The effect of a specific request should depend on whether the resource is a collection or an individual item.

+ **GET** retrieves a representation of the resource at the specified URI. The body of the response message contains the details of the requested resource.
+ **POST** creates a new resource at the specified URI. The body of the request message provides the details of the new resource. Note that POST can also be used to trigger operations that don't actually create resources.
+ **PUT** either creates or replaces the resource at the specified URI. The body of the request message specifies the resource to be created or updated.
+ **PATCH** performs a partial update of a resource. The request body specifies the set of changes to apply to the resource.
+ **DELETE** removes the resource at the specified URI.

### GET methods
A successful GET method typically returns HTTP status code 200 (OK). If the resource cannot be found, the method should return 404 (Not Found).

### POST methods
If a POST method creates a new resource, it returns HTTP status code 201 (Created). The URI of the new resource is included in the Location header of the response. The response body contains a representation of the resource.

If the method does some processing but does not create a new resource, the method can return HTTP status code 200 and include the result of the operation in the response body. Alternatively, if there is no result to return, the method can return HTTP status code 204 (No Content) with no response body.

If the client puts invalid data into the request, the server should return HTTP status code 400 (Bad Request). The response body can contain additional information about the error or a link to a URI that provides more details.

### PUT methods
If a PUT method creates a new resource, it returns HTTP status code 201 (Created), as with a POST method. If the method updates an existing resource, it returns either 200 (OK) or 204 (No Content). In some cases, it might not be possible to update an existing resource. In that case, consider returning HTTP status code 409 (Conflict).

### PATCH methods
With a PATCH request, the client sends a set of updates to an existing resource, in the form of a patch document. The server processes the patch document to perform the update. The patch document doesn't describe the whole resource, only a set of changes to apply.

### DELETE methods
If the delete operation is successful, the web server should respond with HTTP status code 204, indicating that the process has been successfully handled, but that the response body contains no further information. If the resource doesn't exist, the web server can return HTTP 404 (Not Found).

### Asynchronous operations
Sometimes a POST, PUT, PATCH, or DELETE operation might require processing that takes a while to complete. If you wait for completion before sending a response to the client, it may cause unacceptable latency. If so, consider making the operation asynchronous. Return HTTP status code 202 (Accepted) to indicate the request was accepted for processing but is not completed.

In 2008, Leonard Richardson proposed the following maturity model for web APIs:

- Level 0: Define one URI, and all operations are POST requests to this URI.
- Level 1: Create separate URIs for individual resources.
- Level 2: Use HTTP methods to define operations on resources.
- Level 3: Use hypermedia : HATEOAS 

>  Tip

Avoid requiring resource URIs more complex than collection/item/collection.

## Character classes 

| **syntax**| **description** |
|:----:|:--- |
|.	| any character except newline |
|\w\d\s	| word, digit, whitespace |
|\W\D\S	| not word, digit, whitespace |
|[abc]	| any of a, b, or c |
|[^abc] |	not a, b, or c |
|[a-g]	| character between a & g |
|**Anchors**||
|^abc$	| start / end of the string |
|\b\B	| word, not-word boundary |
|**Escaped characters**||
|\.\*\\	| escaped special characters |
|\t\n\r |	tab, linefeed, carriage return |
|**Groups & Lookaround** ||
|(abc)	| capture group |
|\1	| backreference to group #1 |
|(?:abc)	| non-capturing group |
|(?=abc)	| positive lookahead |
|(?!abc)	| negative lookahead |
|**Quantifiers & Alternation** ||
|a*a+a?	| 0 or more, 1 or more, 0 or 1 |
|a{5}a{2,}	| exactly five, two or more |
|a{1,3}	| between one & three |
|a+?a{2,}?	| match as few as possible |
|ab|cd | match ab or cd |



### Reading
+ [API Design Best Practices](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)

### Bookmark/Skim
+ [Documentation for SuperAgent](https://visionmedia.github.io/superagent/)

+ [RegExr](https://regexr.com/) - Pay particular attention to the [cheatsheet]()
+ [Regex Tutorial](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285)
+ [Regex 101](https://regex101.com/)

[<== Home](README.md) 🏠
