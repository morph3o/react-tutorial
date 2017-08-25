# React Components

There are several ways to create a component in React, however there are 4 ways that you can find in most cases.

* ES5 createClass
* ES6 class
* ES5 stateless function
* ES6 stateless function

## ES5 createClass

This is likely the most used way to create components since React was released.

```js
var HelloWorld = React.createClass({
    render: function() {
        return (
            <h1>Hello World</h1>
        );
    }
});
```

Here we use vanilla JavaScript and JSX, this is the original way to create components since React was created. JSX is a language similar to HTML which is used in React. Don't worry about it now, we will have a section about it later.

## ES6 class

Using the ES6 syntax to create the same component above, it will look like the following:

```
class HelloWorld extends React.Component {
    render() {
        return <h1>Hello World</h1>
    }
}
```



