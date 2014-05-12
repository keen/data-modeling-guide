# HTTP Request / Response Data Models

Here's the data model used by [Pingpong](https://github.com/keenlabs/pingpong.git). Pingpong
makes requests to configured URLs and records request and response information in a single event.

A quick synopsis by section:

+ Environment – Information about where the check is being sent from. Useful if you're testing latency from different parts of the world.
+ Request - Information about the request including how long it took and when it started
+ Check - Metadata about the check itself including its name, url, and any custom properies used for slicing and dicing
+ Response - Information about the response including status, response headers and optionally the [response body](https://github.com/keenlabs/pingpong#save-a-urls-json-response-body) if it was JSON

``` json
{
  "check": {
    "url": "http://api.keen.io/3.0?api_key=<your-api-key>",
    "frequency": 15,
    "method": "GET",
    "name": "APIVersionCheck",
    "custom": {
      "resource": "version",
      "vhost": "api",
      "lb": true,
      "ssl": false
    }
  },
  "environment": {
    "rack_env": "production",
    "region": "heroku-eu-west-1",
    "hostname": "aba7347f-2409-44a4-b254-72664b753465",
    "location": "Ireland"
  },
  "request": {
    "duration": 0.343374814,
    "sent_at": "2014-05-12 18:54:01 UTC"
  },
  "response": {
    "content_length": 42,
    "status": 200,
    "content_type": "application/json",
    "successful": true,
    "http_version": "1.1",
    "timed_out": false,
    "server": "nginx/1.6.0",
    "http_reason": "OK",
    "http_status": 200,
    "date": "Mon, 12 May 2014 18:54:02 GMT"
  },
  "keen": {
    "timestamp": "2014-05-12T18:54:02.805Z",
    "created_at": "2014-05-12T18:54:02.805Z",
    "id": "537118ca00111c34131d36cb"
  }
}
```
