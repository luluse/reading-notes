# Access Control (ACL)

- selective restriction of resources
- UNIX files have read, write, and execute permissions assigned to owners, groups, and everyone else.
- Websites have limited access to pages based on the credentials of a user.
- APIs restrict access to internal and external developers differently.

- In our RESTful APIs, it is important to limit access to clients based on credentials.
- Limiting what actions a user can preform on a given resource is called Access Control

### Application Flow and Access Control

- Allow admin users to create categories, content, manage user accounts, and run reports
- Allow editor users to create, edit and delete existing content, but not see or manage user accounts
- Allow guest users to access (read) content
- Allow user users (logged in users) to access (read) content and apply a thumbs-up/down to content, but not change the actual content

Each of these constraints will have to be handled on both the backend and the front end of your application stack.

Back End (API Layer)
- Manage the login cycle with the front-end application
- Maintain the User’s database
- Maintain roles for each user
- Authenticate users (basic and bearer)
- Create, manage, and apply Role Based Access Controls
- Maintain and reference their capabilities, based on their role
- Restrict access to features (like routes) based on capabilities
  - Express Middleware could be used to restrict access to routes
  - Mongoose Middleware/Hooks could be use to restrict access to business logic

Front End (Client Layer)
- Initiate the login process
- Store login tokens as cookies
- Manage login state, capabilities
- Control physical & visual access (hide/show/alter) to components based on RBAC rules
- Alter behaviors based on RBAC rules

### Role Based access control (RBAC)

[Article](https://www.csoonline.com/article/3060780/5-steps-to-simple-role-based-access-control.html)

RBAC is the idea of assigning system access to users based on their role in an organization. It's important to remember that not every employee needs a starring role.

