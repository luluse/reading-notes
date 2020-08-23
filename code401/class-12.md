# OAuth

> OAuth serves as a way to give users the ability to grant application access to services, without giving the application their password.

## How does OAuth work?

- an application such as an Express Web Server asks the user if it’s ok to login as them at some remote service, and then begins the process of authentication and access.

### Access Code

- `response_type=code` indicates that your server wants to receive an authorization code
- `client_id=<your client id>` tells the authorization server which app the user is granting access to
- `redirect_uri=<your redirect uri>` tells the auth server which server endpoint to redirect to
- `scope=<list of scopes>` tells the auth server what you want the user to give access to
- `state=<anything you want>` a place where you can store info to pass to your server if you want

### Access Token

- `grant_type=authorization_code`
- `code=<the code your received`
- `redirect_uri=REDIRECT_URI` must be same as the redirect URI your client provided
- `client_id=<your client id>` tells the authorization server which application is making the requests
- `client_secret=<your client secret>` authenticates that the application making the request is the application registered with the `client_id`
- Once you get an access token, you can use it to make API calls to the service on behalf of that user

## [OAuth2 simplified](https://aaronparecki.com/oauth-2-simplified/)

### Roles

- The Third-Party Application: "Client"
The client is the application that is attempting to get access to the user's account. It needs to get permission from the user before it can do so.

- The API: "Resource Server"
The resource server is the API server used to access the user's information.

- The Authorization Server
This is the server that presents the interface where the user approves or denies the request. In smaller implementations, this may be the same server as the API server, but larger scale deployments will often build this as a separate component.

- The User: "Resource Owner"
The resource owner is the person who is giving access to some portion of their account.

### Create an app
- register a redirect URI to be used for redirecting users to for web server, browser-based, or mobile apps.
- Any HTTP redirect URIs must be served via HTTPS


### Authorization

- first step of OAuth 2 is to get authorization from the user. For browser-based or mobile apps, this is usually accomplished by displaying an interface provided by the service to the user.

- OAuth 2 provides several "grant types" for different use cases. The grant types defined are:

  - Authorization Code for apps running on a web server, browser-based and mobile apps
  - Password for logging in with a username and password (only for first-party apps)
  - Client credentials for application access without a user present
  - Implicit was previously recommended for clients without a secret, but has been superseded by using the Authorization Code grant with PKCE.

> Make sure you always send requests over HTTPS and never ignore invalid certificates


## Resources

[Build a Node API with OAuth](https://developer.okta.com/blog/2018/08/21/build-secure-rest-api-with-node)