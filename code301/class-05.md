# Heroku Deployment

Node.js is an open source, cross-platform runtime environment, which allows you to build server-side and networking applications. 

Heroku is a cloud platform as a service. It allows you to deploy your web server.

### Prepare the app
- heroku login 
- git clone *url*
- cd *directory*

### Deploy the app
- heroku create
- git push heroku master
- heroku ps:scale web=1
- heroku open (to open app in browser)

### view logs
- heroku logs --tail (nformation about your running app)
- Press Control+C to stop streaming the logs.

[Deploy Your Blog to Heroku](https://howtonode.org/deploy-blog-to-heroku