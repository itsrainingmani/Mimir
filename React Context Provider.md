tags: #react #react-context
links: [[React Context Hook]]

A React Context consists of two parts: A Provider & a Consumer. Data flows from the top to the bottom. Once a Provider with values has been set, any number of components can `useContext` to Consume the Context.

There is a question of how to modify the data in the context from a consuming component. This can be achieved by creating a handler and adding it to the context that is being provided.