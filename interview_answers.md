# Interview Answers
Be prepared to demonstrate your understanding of this week's concepts by answering questions on the following topics. These will not be counted as a part of your sprint score but will be helpful for preparing you for your endorsement interview, and enhancing overall understanding.

1. What problem does the context API help solve?
    Context API prevents prop drilling with less boilerplate than redux. However, context API is not as efficient as redux for larger scale apps with high-frequency state updates as there will be much more re-renders leading to performance issues. But for lower-frequency/smaller apps context API is a great option for state management.

2. In your own words, describe `actions`, `reducers` and the `store` and their role in Redux. What does each piece do? Why is the store known as a 'single source of truth' in a redux application?
    the store houses application/global state for the app and in a redux app the state in store can be connected with any component directly rather than having to prop drill down the component tree. 
    reducer functions allow updates to the store's state and these updates are triggered by action creators that are dispatched to the reducer function with an action object. When this action object is passed to the reducer function a switch is used to check for the action type and then executes a state update based on the information associated with that action type. This update in state is then passed to our component through the use of connect and our component re-renders.

3. What does `redux-thunk` allow us to do? How does it change our `action-creators`?
    'redux-thunk' checks if our action creator is dispatching an action object or a function. If an inner function is being dispatched thunk takes over and allows the function to dispatch regular synchronous action objects once the asynchronous operations have completed and promises returned.

4. What is your favorite state management system you've learned and this sprint? Please explain why!
    Between useReducer, Redux, and Context API I like Redux and Context API the most. useReducer doesn't really seem that useful in my opinion because you still have to prop drill so might as well use useState and not have to also build out reducer and actions. I like Redux because everything is compartmentalized - components,actions, reducer - and you don't have to prop drill (which I don't mind for a couple components but I can see why after two prop drills redux might be better for state management). I like useContext because you don't have to spend as much time setting up state management as you do when using redux.
