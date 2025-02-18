# Props and State

## Introducing Props and State Notes

Every components needs to have data (2 ways)
    - **Props:** referes to the data that you pass in from the rest of the app a component, so the component can use that data to display itself
    - **State:** is data that is internal to a component

### Props

- accessed using this.props within the render() function
- initialization data passed from parent components to child components
- props are READ-ONLY, should not be changed by child components

### State

- every react component is a state machine and can have state - private data internal to the component
- don't make a React component a stateful component unless it is required to

### How they play together

1. React components are composed one WITHIN another
2. Most React components focus on HOW to render data
3. Components recieve state via PROPS and render the display accordingly
4. Choose few components to have STATE
5. Components should ideally be at the TOP of the heirarchy
6. Higher level components calculate state and pass this information using props
---

## Props & State Notes

### State:
- Data private or internal to a component
- Component renders rich output based on state
- Components can call functions to update state
- Causing the component to re-render itself

Rules Regarding State:
 
1. State should only be modified by called **setState()**
2. The view is re-rendered only when setState() is called
3. State updates might be ASYNCHRONOUS
4. USe a function which passes in the previous state and the last value props value as arguments
5. State should never be modified directly otherwise compnenet re-rendering will not occur

1. State updates are MERGED to get the new state
2. Only properties which are updated actually change

### What should be stored in a state?
- Values which change with user or server events
    - data pulled from database and used to render component, is held in the state
- Values which cause the UI to re-render
- Anything else should be removed or moved to props

### Props and State similarities
- Both are ways to associate data with components
- both are JS objects
- both trigger a render update on components
- both are deterministic: for a certain combination of props and state the output should always be the same

### Differences
**Props:**
1. Parts of components' config
2. Passed from higher-level components to child components
3. Are immutable within a component once they are recieved from above
4. A component cannt change its props but puts together props for its children

**State:**
1. Part of components' internal state
2. Defined within a component, can take initial values from props
3. Are mutated within a component in response to user events
4. Every component can change its own private state, not the state of its children

### Working with Props
- Props are immutable: The props passed to a component cannot be updated or changed
- 