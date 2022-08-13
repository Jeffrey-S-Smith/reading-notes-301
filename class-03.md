# Reading Passing Functions as Props

## React Docs - lists and keys

1. What does .map() return?
  An array of modified items.
2. If I want to loop through an array and display each value in JSX, how do I do that in React?
  You would use the JS map() function which returns a ``` html <li> ``` element for each item and then assign the resulting array of elements to listItems

3. Each list item needs a unique ____.
    key

4. What is the purpose of a key?
   “Keys help React identify which items have changed, are added, or are removed.”

## The Spread Operator

1. What is the spread operator?
    The spread operator is a useful syntax for quickly manipulating arrays

2. List 4 things that the spread operator can do.
    Copying an array
    Concatenating arrays
    Using math functions
    Using an array as arguments

3. Give an example of using the spread operator to combine two arrays.
    const myArray = [‘dog’, ‘cat’, ‘snake’,]
    const yourArray = [‘tiger’, ‘bear’, ‘monkey’]
    const ourArray = […myArray…yourArray]
    console.log(…ourArray) //dog cat snake tiger bear monkey

4. Give an example of using the spread operator to add a new item to an array.
    const nfcWestTeams = [‘seahawks’, ‘chiefs’, ‘cardinals’]
    const anotherTeam = [‘niners’…nfcWestTeams]
    console.log(anotherTeam) // seahawks rams cardinals niners

5. Give an example of using the spread operator to combine two objects into one.
    const objectOne = {hello: "🤪"}
    const objectTwo = {world: "🐻"}
    const objectThree = {...objectOne, ...objectTwo, laugh: "😂"}
    console.log(objectThree) // Object { hello: "🤪", world: "🐻", laugh: "😂" }
    const objectFour = {...objectOne, ...objectTwo, laugh: () => {console.log("😂".repeat(5))}}
    objectFour.laugh() // 😂😂😂😂😂

## How to Pass Functions Between Components

1. In the video, what is the first step that the developer does to pass functions between  components?
    Creates the callback function in the parent component.

2. In your own words, what does the increment function do?
    It takes a variable and increments (changes) its value, and also returns this value. The increment can be a positive or negative number.

3. How can you pass a method from a parent component into a child component?
    * A parent component defines a function
    * The function is passed as a prop to a child component
    * The child component then invokes the prop
    * The parent function is then called, usually changing something
    * Then the parent component is re-rendered along with its children

4. How does the child component invoke a method that was passed to it from a parent component?
    1. Wrap the Child component in a forwardRef .
    2. Use the useImperativeHandle hook in the child to add a function to the Child .
    3. Call the Child's function from the Parent using the ref, e.g. childRef. current. childFunction() .

## Things I want to know more about
    This reading was about Passing Functions as Props and how to Pass Functions Between Components.
## Bookmark and Review

[React Docs - lists and keys. React Doc](https://reactjs.org/docs/lists-and-keys.html),
[The Spread Operator. by Dr. Derek Austin](https://medium.com/coding-at-dawn/how-to-use-the-spread-operator-in-javascript-b9e4a8b06fab),
[How to Pass Functions Between Components. by Steve Griffith - Prof3ssorSt3v3](https://www.youtube.com/watch?v=c05OL7XbwXU),
[React Tutorial through ‘Declaring a Winner’. React Doc](https://reactjs.org/docs/handling-events.html),
[React Docs - Lifting State Up. React Doc](https://reactjs.org/docs/lifting-state-up.html),
