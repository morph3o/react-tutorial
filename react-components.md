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

```js
class HelloWorld extends React.Component {
    render() {
        return <h1>Hello World</h1>
    }
}
```

As you can see by using the ES6 syntax we can save some LoCs and improving the readability of the code.

## ES5 stateless function

Using the ES5 syntax and the functional style, our component will look like the following:

```js
var HelloWorld = function(props) {
    return (
        <h1>Hello World!</h1>
    );
};
```

Our component will be a simple function which receives the props as a parameter.

## ES6 stateless function

Using ES6 syntax our component will look like the following:

```js
const HelloWorld = (props) => {
    return (
        <h1>Hello World!</h1>
    );
};
```

Here we use the **const** \(introduced in ES6\) thus our component doesn't get accidently reassinged.

## Class vs Stateless Functional

As you you can see from the different ways a component can be created, they can be of two types Class and Stateless Functional. Each type has pros and cons and which one we should use will depends on the scenario. Despite the fact the suitability of the style depend on the scenario, using functional stateless components are more benefitial.

Benefits of using functional components:

* We don't need to use the class definition for creating a component, therefore we save time of creating one.
* By writing a function we avoid the use of **this** and all the confusion it has. To read more about **this **you can refer this link \([https://github.com/getify/You-Dont-Know-JS/blob/master/this %26 object prototypes/ch1.md\](https://github.com/getify/You-Dont-Know-JS/blob/master/this %26 object prototypes/ch1.md\)\)
* Using functional style brings the best practices of functional programming styles has such as inmutability, pure functions, etc.
* Writting functional components requires less LoCs rather than class style therefore we reduce the \_noise \_in the code.
* As a result of the last benfit, we also have a more understandable code.
* As the component will be a pure function, it will be easy to test as it doesn't handle any internal state and therefore it will always behave as expected.

These are benefits of using functional stateless React component, however this doesn't mean that we must use this style everywhere in our project. As it is stated before, it will depend on the scenario we are decide which style is bette. Now we will list a couple of scenario where we should use class component or functional stateless components.

| Class Component | Functional Stateless Component |
| :--- | :--- |
| When we need to handle the internal state of the componentas using this style is the only we can do so. | Everywhere else |
| When we need to use Refs |  |
| When we need to implement the different lifecycle methods such as componentWillMount or the others |  |

Normally it is recommended to start writting the components using the functional style and then when the component is evolving and depending on the use it has, we can transform it into a class component.

## Presentation vs Container

Another way to differentiate components in React is between presentation components and container components. The former are the components which purpose is only to receive information and show it. The don't contain any function or method inside, therefore they are built using functional style. The latter are more complex components which usually render other components. Other characteristics of container components are they pass data and actions to child components, knows about Redux, and they are normally stateful.

