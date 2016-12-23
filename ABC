e-business 
Request Format

Authentication is done via http headers.
Http content-type need to be form data or multipart form data(suggest the request body may be JSON, with the Content-Type header set to application/json.)
Response Format

Output format as json(application/content-type is json)
all response should return right http status code
when 2xx it is ok
when 3xx it says you need to go a step further for request
when 4xx it is the client's error for the sake of bad request(always the params is illegal or auth error)
when 5xx it is sorry for the server's wrong, report it
#### error format
content type: application/json
status code: xxx
body: { error: error_type, message: error_message }
reference materials
