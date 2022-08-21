# Reading CRUD

## Status Codes Based On REST Methods

1. In your own words, describe what each group of status code represents:

* 100’s = “These are informational status codes, they usually tell the client that the header part of the request has been received and the server will try to comply with a transmission demand of the client. Like using a different protocol or telling the client that its request will fail before they start sending the body.”

* 200’s = “These are the success codes. They tell the client that its request was accepted. In case of asynchronous processing of a request (202), this does not mean the request was successfully processed only that it met all validation requirements at the time of sending.”

* 300’s = “These are redirection codes. They tell the client that the resource they are requesting is not available at the expected location anymore. This can have multiple reasons, be temporary or permanent, but the client has to issue a request to the new location.”

* 400’s = “These are the client error codes. They are all about invalid requests a client sent to a server. There are several causes to this, timeouts, wrong URI, missing authentication, etc. A client is sending incorrect input and should confirm the input parameters are correct before retrying the request.”

* 500’s = 500s = “These are the server error codes. Often they indicate problems with overwhelmed servers or unreachable servers behind proxies, but sometimes they can be directly related to client requests that trigger error exceptions on the server. These errors can be temporary or permanent. Usually its best for the client to retry the same request.”

1. What is a status code 202?
“Accepted - If the update is done asynchronous, this code can be used. It should include an URL to access the updated resource or an URL to check if the update has been succeeded. It can also include an estimation of how long the update will take”

2. What is a status code 308?
“308 Permanent Redirect - This is the right code if the resource will now be available at a new URL and the client should directly access it via the new URL in the future. The current endpoint cant control the clients behavior after the request and a subsequent redirect if the resource URL changes again have to be issued from the new URL.

3. What code would you use if an update didn’t return data to a client?
“204 No Content- A proper code for updates that do not return data to the client, for example when just saving a currently edited document.”

4. What code would you use if a resource used to exist but no longer does?
“308 Permanent Redirect - This tells the client to use another URL to access the resource and not use the current URL anymore. Its helpful when we have multiple endpoints for one resource, but do not want to implement reading from all of them.”

5. What is the ‘Forbidden’ status code?
“403 Forbidden - The client has authorized or does not need to authorize itself, but still has no permissions to access the resource.”

## Build A REST API With Node.js, Express, & MongoDB - Quick - First 20 minutes

1. Why do we need to pull our MongoDB database string out of our server and put it into our .env?
Our MongoDB string contains a password to the site that if not added to the env, would be out for anybody to look up on Github.

2. What is middleware?
“Middleware is software that lies between an operating system and the applications running on it. Essentially functioning as hidden translation layer, middleware enables communication and data management for distributed applications.”

3. What does app.use(express.json()) do?
It adds middleware to the app.

4. What does the /:id mean in a route?
It is a number that uniquely identifies the route.

5. What is the difference between PUT and PATCH?
Put updates an entire resource while patch updates parts of it.

6. How do you make a default value in a schema?
“Default values are applied when the document skeleton is constructed. This means that if you create a new document (new MyModel) or if you find an existing document (MyModel.findById), both will have defaults provided that a certain key is missing.”

7. What does a 500 error status code mean?
“500 means Internal Server Error, which can be anything from a missing header field the backend accessed without checking its existence to an unreachable third party service the backend wanted to call.?

8. What is the difference between a status 200 and a status 201?
200 means “200 OK - Most of the read actions will be answered with a 200 OK status.” and 201 means “201 Created - The most fitting for Create operations. This code should signal backend-side resource creation and come along with a Location header that defines the most specific URL for that newly created resource. Its also a good idea to include appropriate representation of the resource or at least one or more URLs to that resource in the response body.”

## Things I want to know more about

This is reading on CRUD and it's Status Codes Based On REST Methods. What error codes you can set up and what they mean. This sections is also building a REST API With Node.js, Express, & MongoDB.

## Bookmark and Review

[Status Codes Based On REST Methods. by moesif](https://www.moesif.com/blog/technical/api-design/Which-HTTP-Status-Code-To-Use-For-Every-CRUD-App/),
[RegExr. by gskinner](https://regexr.com/),
[Build A REST API With Node.js, Express, & MongoDB - Quick . by Web Dev Simplified](https://www.youtube.com/channel/UCFbNIlppjAuEX4znoulh0Cw),
