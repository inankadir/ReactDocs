# ReactDocs
## React DOCS

### Create React App
Create React App is a comfortable environment for learning React, and is the best way to start building a new single-page application in React.

ıt sets up your development environment so that you can use the latest JavaScript features, provides a nice developer experience, and optimizes your app for production.You'll need to have Node >= 14.0.0 and npm >= 5.6 on your machine.To create a project, run:

**npx create-react-app my-app**
**cd my-app**
**npm strart**

## Quick Start
### Creating and nesting components
React apps are made out of components. A component is a piece of the UI(user interface) that has its own logic and appearance. A component can be as small as a button, or as large as an entire page.

React components are JavaScript functions that return markup:

```
function MyButton() {
 return (
  <button>I'm a button</button>
 );
}
```
Now that you've declared MyButton, you can nest it into another component:

```
export default function MyApp() {
 return (
  <div>
    <h1>Welcome to my app</h1>
    <MyButton />
  </div>
 );
}
```
Notice that <MyButton /> starts with a capital letter.That's how you know it's a React component.React component names must always start with a capital letter, while HTML tags must be lowercase.

How a look at the result:
## App.js
```
function MyButton() {
 return (
  <button>
   I'm a button
  </button>
 );
}

export default function MyApp() {
 return (
  <div>
   <h1>Welcome to My app<h1/>
    <MyButton />
  </div>
 );
}
```

