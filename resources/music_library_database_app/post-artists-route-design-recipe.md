# POST /artists Route Design Recipe

## 1. Design the Route Signature

You'll need to include:
  * the HTTP method: POST
  * the path: /artists
  * any query parameters (passed in the URL): none
  * or body parameters (passed in the request body): 
        name=Wild nothing
        genre=Indie



## 2. Design the Response

The route might return different responses, depending on the result.

For example, a route for a specific blog post (by its ID) might return `200 OK` if the post exists, but `404 Not Found` if the post is not found in the database.

Your response might return plain text, JSON, or HTML code. 

_Replace the below with your own design. Think of all the different possible responses your route will return._

```

# Request:
POST /artists

# Expected response (200 OK)
No content

```

## 3. Write Examples

_Replace these with your own design._

```
# Request:

POST /artists

# Expected response:

Response for 200 OK ('')
```

```
# Request:

GET /artists

# Expected response:

Response for 200 OK: Pixies, ABBA, Taylor Swift, Nina Simone, Wild nothing

```

## 4. Encode as Tests Examples


## 5. Implement the Route

Write the route and web server code to implement the route behaviour.