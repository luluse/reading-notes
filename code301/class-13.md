# Update/Delete

### On the client side: defining how to send the data

- The `<form>` element defines how the data will be sent.
- action and method -let you configure the request to be sent when a user hits a submit button.
- we use a relative URL — the data is sent to a different URL on the same origin: `<form action="/somewhere_else">`

### The method attribute

The method attribute defines how data is sent.

1. The GET method is used by the browser to ask the server to send back a given resource:
     - Since the GET method has been used, you'll see the URL www.foo.com/?say=Hi&to=Mom appear in the browser address bar when you submit the form.
     - The HTTP request looks like this:
    ```
    GET /?say=Hi&to=Mom HTTP/2.0
    Host: foo.com
    ```
    - **with a GET request the user will see the data in their URL** 


2. The POST method is the method the browser uses to talk to the server when asking for a response that takes into account the data provided in the body of the HTTP request:
      - the data is appended to the body of the HTTP request.
      - you get no data appended to the URL, and the HTTP request looks like so, with the data included in the request body instead:
      ```
      POST / HTTP/2.0
      Host: foo.com
      Content-Type: application/x-www-form-urlencoded
      Content-Length: 13

      say=Hi&to=Mom
      ```

      - **with a POST request, the user won't see their data in the URL, it is important when you're sending a password or other sensitive data**

### Security issues

Each time you send data to a server, you need to consider security. HTML forms are by far the most common server attack vectors

> All data that comes to your server must be checked and sanitized. Always. No exception.

- Escape potentially dangerous characters
- Limit the incoming amount of data to allow only what's necessary
- Sandbox uploaded files. Store them on a different server.

## [Forms in HTML 5](https://htmlreference.io/forms/)

- action- Defines which URL the form's information is sent to when submitted:

    - "/contact"- You can use a relative URL.
    - "https://htmlreference.io/contact"- You can use an absolute URL.

- method- Defines the HTTP method used when submitting the form.

    - "post"- The form information is sent to the server as part of the request body.

    - "get"- The form information is sent to the server as part URL parameters: /contact?first_name=Alex&last_name=Smith.

- name- The form's name when sent to the server. Useful when multiple forms are present on the same web page.

    - "sign_up_form"- The name value must be unique within the context of the whole web page.
    - It can only contain alphanumeric characters a-z A-Z 0-9 and some special characters like - _… but no space.



