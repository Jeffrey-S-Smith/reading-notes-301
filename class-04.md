# Reading Overview

## React Docs - Forms

1. What is a ‘Controlled Component’?

    In a controlled component, the data or input form element is handled by the React component itself making it the “single source of truth”, whereas it would otherwise be rendered by the DOM in normal HTML
    “In HTML, form elements such as ``` html <input>, <textarea>, and <select> ``` typically maintain their own state and update it based on user input. In React, mutable state is typically kept in the state property of components, and only updated with setState().
    We can combine the two by making the React state be the “single source of truth”. Then the React component that renders a form also controls what happens in that form on subsequent user input. An input form element whose value is controlled by React in this way is called a “controlled component”.”

2. Should we wait to store the users responses from the form into state when they submit the form OR should we update the state with their responses as soon as they enter them? Why.

    “Since the value attribute is set on our form element, the displayed value will always be this.state.value, making the React state the source of truth. Since handleChange runs on every keystroke to update the React state, the displayed value will update as the user types.” In case there is an event handler it is important to update as soon as they enter them.
  
3. How do we target what the user is entering if we have an event handler on an input field?

    We can use handleChange to re-render state on every keystroke the user inputs.

## The Conditional (Ternary) Operator Explained

1. Why would we use a ternary operator?
    It is useful in for shortening the amount of code that needs to be written for conditional statements.

2. Rewrite the following statement using a ternary statement:

```js
  if(x===y){
    console.log(true);
  } else {
    console.log(false);
  }

 x===y ? console.log(true) : console.log(false);
```

## Things I want to know more about
Then it was talking about Higher function. from handling them with normal HTML. In React, we have controlled components, which means they update the state of a component every single time the user enters something into an input field.
## Bookmark and Review

[React Docs - Forms. React Doc](https://reactjs.org/docs/forms.html),
[The Conditional (Ternary) Operator Explained. by Brandon Morelli](https://codeburst.io/javascript-the-conditional-ternary-operator-explained-cac7218beeff),
[React Bootstrap - Forms. React Bootstrap doc](https://react-bootstrap.github.io/forms/overview/),
[React Docs - conditional rendering. React Doc](https://reactjs.org/docs/conditional-rendering.html),
