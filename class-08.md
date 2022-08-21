# Reading APIs

## API Design Best Practices

1. What does REST stand for?
Representational State Transfer

2. REST APIs are designed around a ____.
REST APIs are designed around resources, which are any kind of object, data, or service that can be accessed by the client.

3. What is an identifier of a resource? Give an example.
It is a URI(uniform resource identifier) that uniquely identifies that resource.
An example would be a URL. 

4. What are the most common HTTP verbs?
GET, POST, PUT, PATCH, DELETE

5. What should the URIs be based on?
When possible, resource URIs should be based on nouns (the resource) and not verbs (the operations on the resource).

6. Give an example of a good URI.
A good URI is simple. “collection/item/collection” for example.

7. What does it mean to have a ‘chatty’ web API? Is this a good or a bad thing?
It is a web API that exposes a large number of small resources. The more web requests the bigger the load on the server so the slower it becomes.

8. What status code does a successful GET request return?
It will return 200(ok) if successful.

9. What status code does an unsuccessful GET request return?
It will return 404(not found) if unsuccessful

10. What status code does a successful POST request return?
f it creates a new resource it will return 201(created). It can also return 200(ok) if it just does some processing

11. What status code does a successful DELETE request return?

It will return 204(no content)

## Things I want to know more about
This section is about the best practices design of API's .

## Bookmark and Review

[API Design Best Practices. by Microsoft](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design),
[RegExr. by gskinner](https://regexr.com/),
[Regex Tutorial. by Jonny Fox](https://medium.com/factory-mind/regex-tutorial-a-simple-cheatsheet-by-examples-649dc1c3f285),
[Regex 101. by Regex](https://regex101.com/),
