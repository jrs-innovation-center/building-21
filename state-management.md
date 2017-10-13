Redux a State Management System

[https://dev.to/ross/reduxjs-in-30-seconds-5hj](https://dev.to/ross/reduxjs-in-30-seconds-5hj)

First, this app does not need state management, you could manage your state within react itself, by passing down data and passing actions up. This can get a bit confusing, but it is completely possible to build this app without Redux, we are using redux, to help you get familiar with its concepts.

The first thing we need to do is create a store.

Create `store.js`

``` js
import { createStore, applyMiddleware, combineReducers } from 'redux'
import thunk from 'redux-thunk'
import { game, player, dealer } from './reducers'

const store = createStore(
  combineReducers(
    game, player, dealer
  ),
  applyMiddleware(thunk)
)

export default store
```
