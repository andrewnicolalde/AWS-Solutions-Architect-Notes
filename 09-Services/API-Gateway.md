# What is API Gateway?

AWS API Gateway is a service in AWS which allows developers to define and
control APIs. Supported APIs include HTTP REST-ful APIs and WebSockets.

API Gateway gives developers tools to secure APIs (including ratelimiting and )

## How does it work?

Creating an API in API gateway involves:

* Defining an API
* Define resources and nested resources (URL paths)
* Set security parameters
* Chose a target (EC2, Lambda, DynamoDB)
* Set request and response trasnformations

## More Info

* API Gateway supports API caching
  * Caches responses from endpoints for a specified TTL, resulting in faster response times and lower resource consumption on resources.

## A word on Cross Origin Resource Sharing

[**Same Origin Policy**](https://en.wikipedia.org/wiki/Same-origin_policy) - a browser-enforced security policy which enables scripts present in a web page to access data in another web page, but only if both web pages have the same *origin*

* Purpose - to [prevent certain CSRF attacks.](https://security.stackexchange.com/a/72569) 

**Origin** - A combination of *scheme*, *hostname* and *port number*.

### Note

More information on API gateway will be in the serverless section of the course.

## Exam Tips

If you see a question regarding an error message stating "Origin policy cannot be read at remote resource", you need to enable CORS in API Gateway.