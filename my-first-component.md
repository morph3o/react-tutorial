# My First Component

Now that we have the app up and running, we will start getting our hands dirty with the code. First we will delete some files in order to simplify the project structure. Let's remove the files:

* src/App.css
* src/App.test.js
* src/index.css
* src/logo.svg
* public/favicon.ico
* manifest.json

If we save that, we will see some errors in the browser and in the terminal. To fix those we need to remove the imports and the code within the render method in _App.js_. The file should look like the following:

```
import React, { Component } from 'react';

class App extends Component {
  render() {
    return (
      <div className="App">
        <div className="App-header">
          <img src={logo} className="App-logo" alt="logo" />
          <h2>Welcome to React</h2>
        </div>
        <p className="App-intro">
          To get started, edit <code>src/App.js</code> and save to reload.
        </p>
      </div>
    );
  }
}

export default App;
```

The other file that we will clean is _index.html _leaving it like the following



