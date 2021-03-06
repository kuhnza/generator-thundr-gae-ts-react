# <%= project %>

This project was generated using the [React Thundr GAE generator][generator-react-thundr-gae]. 

## Prerequisites

Before you can run this app up you'll need to check you have the following tools:

* Java 7*
* Maven 3
* Node >= 6.9.1

> *Yes you read that right: **Java 7**. App Engine doesn't support Java 8 yet so I suggest you head
> over to David Cai's excellent guide to [Install multiple JDKs on Mac][install-multiple-jdk-on-mac].
> This project includes a `.java-version` dot file which will tell jEnv to use JDK 7 when running 
> which will hopefully make your life a lot easier.

## Getting Started

To develop the application you'll need to run two processes. 1) The GAE dev server which runs your 
server-side code and 2) the Webpack dev server which offers nice things like live updating and
hot module reloading. 

1. **Start the App Engine dev server**

  `mvn appengine:devserver`

  You can check the server is running by opening [localhost:8080](http://localhost:8080). 
  
  > Note: the static resources served up here will not be updated unless you run `npm run build` or
  > `mvn install` as the Webpack dev server operates entirely in memory.

2. **In a separate terminal window/tab start the Webpack dev server**

  `npm start`

  The Webpack dev server starts on port 3000. Open [localhost:3000](http://localhost:3000) in your
  browser and you should be good to go.

## Deploying

When you're ready to deploy your application you can:

1. **Package your app for deployment**

  `mvn package`

2. **Deploy to App Engine**

  `mvn appengine:update -P<Environment Name>`

  Where environment name matches a profile in your `pom.xml`.

[install-multiple-jdk-on-mac]: http://davidcai.github.io/blog/posts/install-multiple-jdk-on-mac/
[generator-react-thundr-gae]: https://github.com/kuhnza/generator-react-thundr-gae
