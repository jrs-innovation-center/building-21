
Creating a react component!

What is a react component?

A react component is part of the ui, which can contain other react components and it is responsible for presenting content and receiving user generated events.

The component can be defined using a function or a class.

``` js
function MyComponent (props) {
  return <h1>Hello World</h1>
}
```

``` js
class MyComponent extends React.Component {
  render() {
    return <h1>Hello World</h1>
  }
}
```

> If you need access to lifecycle methods, then you will want to create a class, otherwise, it is much simplier to create a function.

In this step, we will be setting up our `React` application. In order to set it up, we need to add some code to the `index.js` file.

``` js
import React from 'react'
import ReactDOM from 'react-dom'

ReactDOM.render(
  <h1>Hello React!</h1>,
  document.getElementById('app')
)
```

Once you have added this code, to your index.js file, you should be able to refresh the browser and see `Hello React!`.

## Building a React Component

Now, that we have react running, we need to write our own react component.

Create a new file called `app.js`

And type the following code in that file:

``` js
import React from 'react'

const App = props => {
  return (
    <h1>Hello React App Component</h1>
  )
}

export default App
```

And now to invoke that component, we need to modify our `index.js` file:

``` js
import React from 'react'
import ReactDOM from 'react-dom'

import App from './app'

ReactDOM.render(
  <App />,
  document.getElementById('app')
)

```

So we added a new import statement to bring in our component definition, and the we invoke the component
by adding it to the `render` method.

You will notice that all react components are capitalized. This is a React Component convention and must be followed or react will not know it is a component.


---

[Index](#)
