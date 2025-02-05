# Props and State Notes

- Every components needs to have data (2 ways)
    - **Props:** referes to the data that you pass in from the rest of the app a component, so the component can use that data to display itself
    - **State:** is data that is internal to a component

### Props

- accessed using this.props within the render() function
- initialization data passed from parent components to child components
- props are READ-ONLY, should not be changed by child components

### State

- every react component is a state machine and can have state - private data internal to the component
- don't make a React component a stateful component unless it is required to

1. React components are composed one WITHIN another
2. Most React components focus on HOW to render data
3. Components recieve state via PROPS and render the display accordingly
4. Choose few components to have STATE
5. Components should ideally be at the TOP of the heirarchy
6. Higher level components calculate state and pass this information using props