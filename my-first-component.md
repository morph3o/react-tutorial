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
      
    );
  }
}

export default App;
```

The other file that we will clean is \_index.html \_ leaving it like the following:

```
<html lang="en">
  <head>
    <title>React App</title>
  </head>
  <body>
    <noscript>
      You need to enable JavaScript to run this app.
    </noscript>
    <div id="root"></div>
  </body>
</html>
```

**NOTE**: After making these changes you should see an error, that's because the render method should return something. We will fix it later.

Before keep working with the code let's explain briefly the structure of the project.

