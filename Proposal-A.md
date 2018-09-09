# Proposal A - React-GUI

## Introduction

> This is the simple introduction how **React-GUI** will help the community in building robust webapps in less time.

### Scope

The proposal covers most of the pre-requisites that we'll need to before we build this library
Things you'll need:

- React
- Redux
- RollUp

### Goals
- A gui to make components to reduce writing recundant code
- All build configuraton will be configurable 
- There will be no abstractions likely other libraries creat-react-app -all generated files will be available in structured app

#### Features

- GUI will run on localhost
- React Components Interface :
    - There will be toggle to check whether to make it stateful or stateless
    - Checkboxes will be added to include lifyCycles method optioanlly
      - An example how resultant component will look like:

```jsx
class ReactGuiComponent extends Component {
  state={}

  componentWillMount() {
    // write implementation
  }

  componentDidMount() {
    // write implementation
  }

  static getDerivedStateFromProps(nextProps, prevState) {
    // write implementation
  }
 
  componentDidMount() {
    // write implementation
  }

  render() {
    return(
       "Welcome to React GUI"
    )
  }

}

export default ReactGuiComponent
```
    - Named and default export configurable

- Redux Interface
    - Actions and reducer will be created with a little configuration in GUI
    - Which components are to be connected with `connect()`, can be configured through GUI

## Parent - Child relationship visualisation:

- User can make Parent-Child relation with drgaggable option
- A visualisation library like `React-dnd`, `d3` can be integrated
    - This all can be implemented for reducers and  components.

> The goal is to make apps more concise and user will only focus on logic implmentation. Our target is to make clean code and readable. There's a big misconeption in the community when begginers decide to build a webapp from scratch. All code will be generated with comments so user everyone can leverage. Our ultimate goal is to provide a basic boilerplate so user can just pick the app name and start coding.


