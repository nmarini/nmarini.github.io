---
layout: post
title:      "Thinking About Thunk"
date:       2019-11-11 23:11:00 +0000
permalink:  thinking_about_thunk
---


To understand Thunk, you first must understand three important principles of Redux.  

(1.) Redux has a global state object which represents your applications entire state.  And Redux is often referred to as* the single source of truth* for that reason.  The store is set up through reducers that define the initial state, along with the logic that allows the state to be modified. 

(2.) Reducers are considered *pure functions*; therefore, should return a copy of state instead of mutating the original state.   

(3.) In order to modify the state, an action needs to be *dispatched* to a reducer.  An action is an object that has a key of *type*.  The reducer knows how to modify the state based off of the value of *type*. And action creators are functions that return an action.

Given what we know of Redux, there are certain circumstances that may break our application.  For example, may not be able to make an API request in our action creator because it would return the object before completing the request.  And since our reducers are suppose to be *pure functions* they are not able to make requests to APIs.  

Thunk allows Redux to make asynchronous requests within our action creators without breaking our application.  Thunk is middleware that allows Redux's action creators to return functions.  Thunk looks at every action creator, and if it is a function then Thunk calls it.  Thunk functions also get passed the dispatch function and the getState function as arguments.  This allows Thunk functions to have the ability dispatch multiple actions within a function and to have access to the state.  

Setup Thunk: 

`npm install --save redux-thunk`

```
import { createStore, applyMiddleware } from 'redux';
import thunk from 'redux-thunk';
import rootReducerExample from './reducers/example';

const store = createStore(
  rootReducerExample,
  applyMiddleware(thunk)
);
```

Now all of your action creators will be able to dispatch multiple actions and make asynchronous requests.



