tags: #react #react-context #react-hooks

React has a built-in way of performing global state management with the Hooks API's Context method.

“Context provides a way to pass data through the component tree without having to pass props down manually at every level.” → React Docs

It was introduced to address the issue of prop drilling. Using Context, a HOC's context can be accessed by a child component without mapping props in intermediate components.

```js
import React from 'react';

const AppContext = React.createContext({ colour: 'blue', lang: 'en' });

const App = () => 
    <AppContext.Provider value={{ colour: 'blue', lang: 'fr' }}>
        <Menu />
    </AppContext.Provider>;

function Menu() {
    return <MenuItem />
}

const MenuItem = () =>
    <AppContext.Consumer>
        { value =>
            <div>
                <p>Theme colour: {value.colour}</p>
                <p>Locale: {value.lang}</p>
            </div>
        }
    </AppContext.Consumer>

export default App;
```

You can pass down a callback function with the context that allows Consumers to change the state of the Context Provider