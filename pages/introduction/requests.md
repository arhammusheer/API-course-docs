# Types of HTTP Requests

HTTP requests are ways to distinguish different types of requests like getting data, editing client data in the database or creating new entries.

## GET

This is the default type of request your browser sends when you load a webpage.

A GET request is intended to receive data from the server. A get request support parameters in your query.

An example GET request with params looks like `https://jsonplaceholder.typicode.com/comments?postId=1&id=2`

The part after the `?` are the params and are seperated with the `&` operator.

The get request responds with the headers and the body which you'll learn how to create in further part of the guide.

## HEAD

This request is used to request HTTP headers from the server. The format of this request is similar to a GET request but only the headers are returned and not the body.

## POST

This request is used when the user wants to create new changes on the server, for example - Logging in as user. When the user presses the submit button, your HTML form sends the request in the POST method.

You need to send a body as a part of your request which is usually handled automatically by your HTML forms or you can create your own.

## PUT

The intended use is to overwrite existing data on the server. This method follows similar requirements as a POST request.

## DELETE

The intended use of this request is self explanatory. It is used to delete a resource on the server.

## How to use curl to create different types of request through command line

Here are some examples on how you can generate different requests to test your endpoints.

GET
```shell
curl <URL>
or
curl http://jsonplaceholder.typicode.com/users
```

POST
```shell
curl -X POST -d <Your Data> <URL>
or
curl -X POST  --header "Content-Type: application/json" -d "{\"name\":\"john smith\"}" http://jsonplaceholder.typicode.com/posts
```


## Others

You're recommended to use an API client to test your client. Some of the good ones are [Postman](http://postman.com), [Insomnia](http://insomnia.rest) and [Firecamp](http://firecamp.io)

The current info has been sources from https://developer.mozilla.org/en-US/docs/Web/HTTP/Methods

If you want to look at additional methods or learn about each or them through their proper intended documentation, visit the link above.