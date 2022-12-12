# How HTTP requisition works

An HTTP request is a message that is sent from a client (such as a web browser) to a server to request information or resources. HTTP is the protocol (or set of rules) that is used to communicate over the internet, and an HTTP request is a specific type of message that is sent using this protocol.

When a client wants to make an HTTP request, it sends a message to the server that includes the following information:

*   The HTTP method, which specifies the type of request that is being made (such as GET, POST, PUT, DELETE, etc.)
    
*   The URL, which specifies the location of the resource that the client wants to access
    
*   The HTTP version, which specifies the version of the HTTP protocol that is being used
    
*   Header fields, which provide additional information about the request (such as the user agent, the content type, the accepted languages, etc.)
    
*   A message body, which may contain data or other information that the client wants to send to the server (this is optional, and not all HTTP requests have a message body)
    

When the server receives an HTTP request, it processes the request and sends back a response. The response includes the following information:

*   The HTTP version, which specifies the version of the HTTP protocol that is being used
    
*   A status code, which indicates the result of the request (such as 200 for success, 404 for not found, 500 for internal server error, etc.)
    
*   Header fields, which provide additional information about the response (such as the content type, the content length, the date, etc.)
    
*   A message body, which may contain data or other information that the server wants to send back to the client (this is optional, and not all HTTP responses have a message body)
    

In summary, an HTTP request is a message that is sent from a client to a server to request information or resources, and an HTTP response is the message that the server sends back in response. HTTP requests and responses follow a specific format and protocol, and they are an essential part of how the web works.