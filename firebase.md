# Firebase

Firebase is a google service that offers cloud solutions for databases, authentication and more. I have utilised firebase in my full stack project management app, you can find the code [here](https://github.com/shan5742/project-manager).

### Signing Up

I already had a Google account, so I simply went to the firebase website and signed up for the free tier, which is fine for what I am using it for.

### Dummy Data

I then created a database for users and projects for my app, I started by doing this from the firebase console, just to get a feel for how the service works.

### Connecting Up

From there I connected firebase to my app by installing some dependencies and creating a config file in my project, from there I pasted in the credentials, which enabled me to make modifications to the db directly from the front end.

### Cloud Funtions

Firebase allows us to produce functions server side for things that we do not want the front end to handle. These functions are just in javascript and are handled by firebase when invoked, an example of a cloud function can be seen below:

```js
exports.helloWorld = functions.https.onRequest((request, response) => {
  response.send("Hello Asam!");
});
```
