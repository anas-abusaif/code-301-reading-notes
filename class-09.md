# API Design Best Practices
## 1.What does REST stand for?
Representational State Transfe
## 2.REST APIs are designed around a ____.
resources
## 3.What is an identifer of a resource? Give an example.
a URI that uniquely identifies that resource.

https://adventure-works.com/orders/1
## 4.What are the most common HTTP verbs?
GET, POST, PUT, PATCH, and DELETE.
## 5.What should the URIs be based on?
nouns
## 6.Give an example of a good URI.
https://www.facebook.com/
## 7.What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
web APIs that expose a large number of small resources, defenetly a bad thing
## 8.What status code does a successful GET request return?
 a response message with the body containing the value 100.
 ## 9.What status code does an unsuccessful GET request return?
 an error message
 ## 10.What status code does a successful POST request return?
  URI to the client.
  ## 11.What status code does a successful DELETE request return?
  removes the resource at the specified URI.