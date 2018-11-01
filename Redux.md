# Redux

Redux is a way of managing the **state** of your whole application, essentially you are storing the whole state in **one place** and from there various components can access it and add to it.

I have decided to use Redux with my [react-router repo](https://github.com/shan5742/react-router).

To start with I simply installed two packages via npm:

```
npm install redux react-redux
```

from there I imported these into my app and created a store and passed in the reducer as follows:

```js
const store = createStore(rootReducer);

ReactDOM.render(
  <Provider store={store}>
    <App />
  </Provider>,
  document.getElementById("root")
);
```

```js
const initState = {
  posts: []
};

const rootReducer = (state = initState, action) => {
  return state;
};

export default rootReducer;
```

I started by creating some dummy data inside the `initState` array. From there I created a funtion to get the data from the Redux _store_ and inject it into the `Home` component of the app.
