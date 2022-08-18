# Reading Putting it all together

## React Docs - Thinking in React

1. What is the single responsibility principle and how does it apply to components?
    The single-responsibility principle (SRP) is a computer-programming principle that states that every module, class or function in a computer program should have responsibility over a single part of that program's functionality, and it should encapsulate that part. All of that module, class or function's services should be narrowly aligned with that responsibility.

2. What does it mean to build a ‘static’ version of your application?
    It means that there is no state used and components are built to reuse other components to pass data using props. Basically don’t use state because it changes data over time and static means no movement so it doesn’t change.

3. Once you have a static application, what do you need to add?
    Inverse data flow needs to be added. Basically the ability for the data to flow the other way from bottom to top.

4. What are the three questions you can ask to determine if something is state?
    * Is it passed in from a parent via props? If so, it probably isn’t state.
    * Does it remain unchanged over time? If so, it probably isn’t state.
    * Can you compute it based on any other state or props in your component? If so, it isn’t state.

5. How can you identify where state needs to live?

  “Identify every component that renders something based on that state.
   Find a common owner component (a single component above all the components that need the state in the hierarchy).
   Either the common owner or another component higher up in the hierarchy should own the state.
   If you can’t find a component where it makes sense to own the state, create a new component solely for holding the state and add it somewhere in the hierarchy above the common owner component.”

## Higher-Order Functions

1. What is a “higher-order function”?
    “Functions that operate on other functions, either by taking them as arguments or by returning them, are called higher-order functions. Higher-order functions allow us to abstract over actions, not just values.”

2. Explore the greaterThan function as defined in the reading. In your own words, what is  line 2 of this function doing?
    It is a function comparing variables and seeing which one is greater than the other. The function checked if 11 was greater than 10 and returned true.

3. Explain how either map or reduce operates, with regards to higher-order functions.

    “The map method transforms an array by applying a function to all of its elements and building a new array from the returned values.” So the map method would produce a higher order function because it operates on a function and returns another function.
    “Another common thing to do with arrays is to compute a single value from them. Our recurring example, summing a collection of numbers, is an instance of this. Another example is finding the script with the most characters.
    The higher-order operation that represents this pattern is called reduce (sometimes also called fold). It builds a value by repeatedly taking a single element from the array and combining it with the current value.” Same idea as with map methods with regards to higher order functions, a different array is returned making it a high-order function.

## Things I want to know more about
It is about React and static version of your application and about higher-order function, greaterThan function and map or reduce operates, with regards to higher-order functions.
## Bookmark and Review

[React Docs - Thinking in React. React Doc](https://reactjs.org/docs/thinking-in-react.html),
[Higher-Order Functions. by eloquentjavascript](https://eloquentjavascript.net/05_higher_order.html#h_xxCc98lOBK),
