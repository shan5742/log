# September 18th - 21st

For the most part I have been preparing for an upcoming interview.

My preparation plan right now is fairly simple.

- Research the company, so that I have things to talk about during the interview and demonstrate my interest and desire to work there.

- This research will also enable me to ask good questions at the end (always have questions).
  Have a lot of questions - if the interview goes the way I think there will be a good bit of back and forth, so a lot of my questions may come up, so I plan to have a bunch of backups.

- Go through the code from my test, I need to be able to explain clearly everything I did and why. Alternatively I will be asked technical questions based on what I have done for the test, again the aim of these will be to see if I understand what I have done or have copied & pasted answers from the internet.

- Have a well thought out answer to Why did you choose React other than because React is bleeping awesome. I was permitted to use anything I wanted for my technical test and I choose react, I'm sure I will be asked why.

### Why Use React?

1. **Re-usable components** - very valuable when scaling.
2. **Virtual DOM** - Increases performance
3. **Friendly** - React has some great tools available when developing such as React Dev Tools in Chrome and easy to understand warnings when compiling.
4. **React Native** - using React means all the skills learnt are transferable for creating mobile applications.
5. **Fast Learning Curve** - React is very a simple and lightweight library that only deals with the view layer.
6. **Compatible** - React can be used in conjunction with other libraries and frameworks.

### Handling API

For my technical test I had to deal with an API, which will probably result in this coming up at interview, so I figure I will brush up on API in general and explain the method I used to GET data.

##### What is a RESTful API

REST determines what the API looks like. It stands for “Representational State Transfer”. It is a set of rules that developers follow when they create their API. One of these rules states that you should be able to get a piece of data (called a resource) when you link to a specific URL.

Each URL is called a request while the data sent back to you is called a response.

A request is made up of four things:

- The endpoint
- The method
- The headers
- The data (or body)

###### Endpoint

The endpoint is simply the URL to access the API, it can include variables and params to get certain bits of data.

###### Method

The method is the type of request you send to the server. You can choose from these five types below:

- GET
- POST
- PUT
- PATCH
- DELETE

These methods provide meaning for the request you’re making. They are used to perform four possible actions: **Create**, **Read**, **Update** and **Delete** (CRUD).

**GET**
This request is used to get a resource from a server. If you perform a `GET` request, the server looks for the data you requested and sends it back to you. In other words, a `GET` request performs a `READ` operation. This is the default request method.

**POST**
This request is used to create a new resource on a server. If you perform a `POST` request, the server creates a new entry in the database and tells you whether the creation is successful. In other words, a `POST` request performs an `CREATE` operation.

**PUT & PATCH**
These two requests are used to update a resource on a server. If you perform a `PUT` or `PATCH` request, the server updates an entry in the database and tells you whether the update is successful. In other words, a `PUT` or `PATCH` request performs an `UPDATE` operation.

**DELETE**
This request is used to delete a resource from a server. If you perform a `DELETE` request, the server deletes an entry in the database and tells you whether the deletion is successful. In other words, a `DELETE` request performs a `DELETE` operation.

###### Headers

Headers are used to provide information to both the client and server. It can be used for many purposes, such as authentication and providing information about the body content.

HTTP Headers are property-value pairs that are separated by a colon. The example below shows a header that tells the server to expect JSON content.

###### The Date (or body)

The data (sometimes called “body” or “message”) contains information you want to be sent to the server. This option is only used with POST, PUT, PATCH or DELETE requests.
