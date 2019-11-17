# WebAPI testing guidance and good practice 

WebAPI testing ensures the application delivers expected behavior and handle unexpected behavior too. It allows you to test very early when there is no GUI and helps to identify and fix issues in development lifecycle which would otherwise be expensive to fix when identified during UI testing. The advantage is that a lot of logic can be validated without being dependent upon the UI.

WebAPI testing can be carried out on internal and external APIs. As internal APIs are designed to be consumed by the application/developers/support team, it is very unlikely to be exposed to end users and less vulnerable. Hence performing lightweight usability testing and robust functional testing would be ideal. Security and Performance testing on internal APIs depends on the endpoint’s requirement. External APIs are designed for external partners/third party developers; these need robust testing on all scenarios (functional, security, performance, scalability and usability) using representative test data and data volume. 

For reference and training purpose a number of WebAPI test scenarios are list here. Note: not all of them apply to every endpoint you test, use this as guidance to define your project's test scenario.  

## Functional
- Happy case: 200 status code and the expected response returned
- Http methods (CRUD) are idempotent methods
- 400 status and the user-friendly error message returned for invalid inputs in the payload.
- 401 status code returned for an unauthorized user request
- 403 status and the user-friendly error message returned for forbidden action (Non-admin user accessing admin feature)
- 404 returned for invalid URI request
- 405 method not allowed when different verbs are used. (GET instead of POST and vice versa)
- 409 status for a duplicate request (POST only)
- Check other 4xx & 5xx errors to reflect client side and server side error scenarios
- Check all header content and their inputs

## Usability
- A user-friendly error message is displayed when URI is wrong
- A user-friendly error message is displayed when payload syntax is wrong
- A user-friendly error message is displayed when a mandatory parameter has no input/missing.
- A user-friendly error message is displayed when the payload is wrong
- User guide updated with the API usage and variables details.
- API version check

## Performance
- Response time for one user request is acceptable
- Response time for production like data request is acceptable
- The HTTP compression mechanism is applied to ensure the best network performance. For e.g: Content Encoding in the header may be gzipped/compress/deflate
- API response is stable & reliable when handle bulk operations/large data volume
- Pagination is available to reduce unnecessary computations at the server where necessary

## Security
- Verify that every HTTP response contains a content type header specifying a safe character set (e.g., UTF-8, ISO 8859-1).
- Identify and validate user authentication (HTTP authentication header)
- Verify that the HTTP headers or any part of the HTTP response do not expose detailed version information of system components.
- Verify that all API responses contain X-Content-Type-Options: nosniff and Content-Disposition: attachment; filename="api.json" (or other appropriate filename for the content type).
- Verify that a content security policy (CSPv2) is in place that helps mitigate common DOM, XSS, JSON, and JavaScript injection vulnerabilities.
- Verify that the X-XSS-Protection: 1; mode=block header is in place to enable browser reflected XSS filters.

# Types of bugs WebAPI tests uncovers
- Incorrect response code (for e.g: 500 when 400 is expected, 400 when 405 is expected, so on)
- Fail to handle error conditions gracefully (for e.g: 500 for all error cases, when it is just 400/404)
- Unused flags
- Missing functionality (for e.g: in-complete/wrong response content)
- Reliability issues; connection issues and getting a response from API
- Security issues
- Performance issue
- Unhelpful error/warning
- Incorrect handling of valid argument values
- Unstructured response data (json/xml)

## Useful references for beginners 

https://www.guru99.com/testing-rest-api-manually.html  
https://app.pluralsight.com/library/courses/postman-fundamentals/table-of-contents  
https://www.kennethlange.com/posts/The-Ultimate-Checklist-for-REST-APIs.html  
https://github.com/shieldfy/API-Security-Checklist  
https://app.pluralsight.com/library/courses/five-essential-tools-building-rest-api/table-of-contents
