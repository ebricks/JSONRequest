JSONRequest
==================

JSONRequest is a tiny Swift library to do GET and POST JSON requests. Requests automatically include the following headers:

```
Content-Type: application/json
Accept: application/json
```

Response is automatically parsed as JSON and returned in a JSON object (array, dictionary, number, string...)

##Usage

### GET some JSON
```
JSONRequest.get(URL, params: ["hello": "world"]) { (JSON, request, response, error) -> Void in
    println(JSON)
    println(request)
    println(response)
    println(error)
}
```

### POST some JSON
```
let payload = ["somekey": "somevalue", "anotherkey": "another value"]
JSONRequestManager.post("http://httpbin.org/post", payload: payload) { (JSON, request, response, error) -> Void in
    println(JSON)
    println(request)
    println(response)
    println(error)
}
```
