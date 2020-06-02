# Redux
## Predictable state container for JS apps
## 3 Principles
1. single source of truth
2. State is read only
3. Changes are made with pure functions
## Concepts
### Actions
1. Actions must have a **type** property
2. **type** should be string **constants**
3. Action creators are exactly that—functions that create actions.
4. bound action creator that automatically dispatches `const boundAddTodo = text => dispatch(addTodo(text))` and call them directly to create and dispatch action in one `boundAddTodo(text)`
### Reducer
1. reducer is a pure function (prevState, action) => nextState
2. **never** do inside a reducer
   1. mutate its argument
   2. perform side effects like API calls and routing transitions
   3. call non-pure functions
3. **Given the same arguments, it should calculate the next state and return it. No surprises. No side effects. No API calls. No mutations. Just a calculation.**
4. we don't mutate state and we always return previous state by default
```function todoApp(state = initialState, action) {
  switch (action.type) {
    case SET_VISIBILITY_FILTER:
      return Object.assign({}, state, {
        visibilityFilter: action.filter
      })
    default:
      return state
  }
}
```
5. All combineReducers() does is generate a function that calls your reducers **with the slices of state selected according to their keys**
6. And like other reducers, combineReducers() does not create a new object if all of the reducers provided to it do not change state. 
7. 