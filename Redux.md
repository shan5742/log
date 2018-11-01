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

I started by creating some dummy data inside the `initState` array. From there I created a function to get the data from the Redux _store_ and inject it into the `Home` component of the app.

### Mapping State and Actions to Props

Using Redux we can create actions and dispatch them to do various things all by creating simple functions.

example from Redux docs:

```js
function visibilityFilter(state = 'SHOW_ALL', action) {
  switch (action.type) {
    case 'SET_VISIBILITY_FILTER':
      return action.filter
    default:
      return state
  }
}
​
function todos(state = [], action) {
  switch (action.type) {
    case 'ADD_TODO':
      return [
        ...state,
        {
          text: action.text,
          completed: false
        }
      ]
    case 'COMPLETE_TODO':
      return state.map((todo, index) => {
        if (index === action.index) {
          return Object.assign({}, todo, {
            completed: true
          })
        }
        return todo
      })
    default:
      return state
  }
}
​
import { combineReducers, createStore } from 'redux'
const reducer = combineReducers({ visibilityFilter, todos })
const store = createStore(reducer)
```

### Action Creators

Action creators are simply functions, when we call them they create an action for us, the reason for using them is basically it makes our code more re-usable. It saves us re-typing out actions, we can simply just call a function.

Previously we would write our actions inside of components like this:

```js
const mapDispatchToProps = dispatch => {
  return {
    deletePost: id => {
      dispatch({ type: "DELETE_POST", id: id });
    }
  };
};
```

Instead an action creator can be made and stored in an `actions` folder in our app and then we can simply call the function in any component. The action creator is very similar to the above - naturally:

```js
export const deletePost = id => {
  return {
    type: "DELETE_POST",
    id
  };
};
```
