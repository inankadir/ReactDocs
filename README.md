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

The export default keywords specify the main component in the file.If you're not familiar with some piece of JavaScript syntax,MDN and javascript.info have great references.

## Writing markup with JSX

The markup syntax you've seen above is called JSX.It is optional, but most React projects use JSX for its convenience.All of the tools we recommend for local development support JSX out the box.
JSX is stricter than HTML. You have to close tags like <br />. Your component also can't return multiple JSX tags.You have to wrap them into a shared parent, like a <div>...</div> or an empty <>...</> wrapper:
```
function AboutPage() {
 return(
  <>
   <h1>About</h1>
   <p>Hello there.<br />How do you do?</p>
  </>
 );
}
```
If you have a lot of HTML to port JSX, you can use an online converter.

## Adding styles

In React,you specify a CSS class with className.It works the same way as the HTML class attribute:

<img className="avatar" />

Then you write the CSS rulesfor it in a separate Css file:

/* In your CSS */
.avatar {
 border-radius: 50%;
 }

 React does not prescribe how you add CSS files.In the simplest case, you'll add a <link> tag to your HTML. If you use a build tool or a dramework,consult its documentation to learn how to adda CSS file to your project.

 ## Displaying data

JSX lets you put markup into JavaScript. Curly braces let you "escape back" into JavaScript so that you can embed some variable from your code and display it to the user. For example, this will display user.name:

return (
 <h1>
  {user.name}
 </h1>
);

You can also "escape into JavaScript" from JSX attributes, but you have to use curly braces instead of quotes.For example, className="avatar" passes the "avatar" string as the CSS class, but src={user.imageUrl} reads the JavaScript user.imageUrl variable value, and then passes that value as the src attribute:

return (
 <img 
   className="avatar"
   src={user.imageUrl}
  />
 );

 You can put more complex expressions inside the JSX curly braces too, for example, string concatenation:
```
const user = {
 name: 'Hedy Lamar',
 imageUrl: 'https://i.imgur.com/yXOvdOSs.jpg',
 imageSize: 90,
};
export default function Profile() {
 return (
  <>
   <h1>{user.name}</h1>
   <img
     className="avatar"
     src={user.imageUrl}
     alt={'Photo of} + user.name}
     style={{
      width:  user.imageSize,
      height: user.imageSize
      }}
     />
    </>
   );
 }
```

In the above example, style={{}} is not a special syntax, but a ruegular{} object inside the style={ } JSX curly braces. You can use yhe style attribute when your styles depend on JavaScript variables.

## Conditional rendering

In React, there is no special syntax for writing coditions.Instead, you'll use same techniques as you use when writing regular JavaScript code.For Example, you can use an if statement to conditionally include JSX:

```
let content;
if (isLoggedIn) {
 content = <AdminPanel />;
} else {
 content = <LoginForm />;
}
return (
 <div>
  {content}
 </div>
);
```

If you prefer more compact code, you can use the conditional ? operator. Unlike if, it works inside JSX:
```
<div>
 {isLoggedIn ? (
  <AdminPanel />
) : (
  <LoginForm />
)}
</div>
```
When you don't need the else branch, you can also use a shorter logical && syntax:
```
<div>
 {isLoggedIn && <AdminPanel />}
</div>
```
All of these approaches also work for conditionally specifying attributes. If you're unfamiliarwith some of this JavaScript syntax, you can start by always using if...else.

## Rendering lists







  
