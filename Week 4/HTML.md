# HTML 

## Status Code

* 100 - 199 = Informational
* 200 - 299 = Success
* 300 - 399 Redirection
* 400 - 499 Client Side Error
* 500 - 599 Server Side Error

## [HTTP Headers](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

- [Request headers](https://developer.mozilla.org/en-US/docs/Glossary/Request_header) contain more information about the resource to be fetched, or about the client requesting the resource.
- [Response headers](https://developer.mozilla.org/en-US/docs/Glossary/Response_header) hold additional information about the response, like its location or about the server providing it.
- [Representation headers](https://developer.mozilla.org/en-US/docs/Glossary/Representation_header) contain information about the body of the resource, like its [MIME type](https://developer.mozilla.org/en-US/docs/Web/HTTP/Basics_of_HTTP/MIME_types), or encoding/compression applied.
- [Payload headers](https://developer.mozilla.org/en-US/docs/Glossary/Payload_header) contain representation-independent information about payload data, including content length and the encoding used for transport.

HTTP is stateless - servers does not remember the previous requests



## XML vs JSON

[URI, URL, URN](https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers)

* URI - Uniform Resource Identifier
* URL - Uniform Resource Locator
* URN - Uniform Resource Name

![url,url,urn](C:\Users\Amit\Desktop\Notes\Week 4\Images\URI-URL-URN@2x.png)

## [Servlet Life Cycle](https://www.tutorialspoint.com/servlets/servlets-life-cycle.htm)

* `init()` - method to initialize 
* `service()` - method to process client request
* `destroy()` - terminates servlet
* Collected by garbage collector in JVM

## [HTML Methods](https://www.w3schools.com/tags/ref_httpmethods.asp)

* GET
  * Request data from specified resource
* POST
  * Send data to server to create/update a resource
* PUT
  * is used to send data to a server to create/update a resource
* HEAD
  * almost identical to GET, but without the response body
* DELETE
  * deletes the specified resource
* PATCH
  * Apply partial modifications to a resource
* OPTIONS
  * describe the communication options for the target resource 



## Servlet Hierarchy

* Servlet Interface
* Generic Servlet - Abstract class
* Http Servlet - Abstract Class
* Servlet (user created) - Concrete Class