# Proposal

## Purpose:

The purpose for this project is to give a starter template whether your are writting a component in react smart or dumb, or even initializing a new application.

The template provided by *react-cli* aims to be highly configurable and easily adjustable. We believe in **build on top of things** kind of applications.

## Vision:

Initially this will start out as a cli based configuration which will then move on to a GUI similar to what @vue does right now. A web application dashboard which will have options to create files and much more.. (much more part is still being thought on)

## Getting Started:

```
$ npm install -g @withvoid/react-cli
```
Then you can use it as

```
$ @withvoid/react-cli <react-cli-command-here>
$ rc <react-cli-command-here> // or use the shorthand cli command
```

Or if you don't want to have it as a global dependency but just want to use it at run time

```
$ npx @withvoid/react-cli <react-cli-command-here>
```

### @withvoid/react-cli init-webpack
This command will quickly scaffold a react application build on top of webpack/babel and will have support for the follow

- Es6/Es7 syntax
- CSS/SCSS support
- Font files support
- Images support
- React support *this goes without saying*
- Hot Module Replacement
- Code splitting
- Configuration for a NodeJS based application
- Configuration for a Java Spring Boot application
- *python, go etc* support coming soon

The main thing that I want to *empasize* here is that react-cli will aim to provide a boiler plate so simple with so thorough documentation that you can always **build on top of it** A webpack configuration so easy that anyone can work with it and add or remove from it, as it suites the developer.

```sh
$ @withvoid/react-cli init-webpack
$ rc init-webpack
```

### @withvoid/react-cli init-prepack
*same as what* **@withvoid/react-cli init-webpack** but with prepack

### @withvoid/react-cli generate sc
The *command* will generate a new smart component (State component) from the ./dir you run this command in.

```
import React from 'react';
import PropTypes from 'prop-types';
class SmartComponent extends React.Component {
   constructor(props) {
     super(props);
     this.state = {
        foo: true;
     };
   }
   static getDerivedStateFromProps(props, state) {
     // code here..
   }
   static getSnapshotBeforeUpdate(prevProps, prevState) {
     // code here..
   }
   componentDidMount() {
     // code here..
   }
   componentWillUnmount() {
     // code here..
   }
   render() {
     return (
       <div>
         {this.state.foo && <p>truthy</p>}
         <p>{props.name} is awesome</p>
       </div>
     );
   }
}
SmartComponent.propTypes = {
  name: PropTypes.string,
};
SmartComponent.getDefaultProps = {
  name: 'React-CLI'
};
export default SmartComponent;
```

### @withvoid/react-cli generate dc
The *command* will generate a new dumb component (Stateless component) from the ./dir you run this command in.

>Now although we can support both of these syntax the latest ES7 as well, but since react documentation suggests that we write it as simple old javascript so that `babel` doesn't have to add a pollyfill for the ES7 syntax we will support this syntax for now

```
import React from 'react';
import PropTypes from 'prop-types';
function DumbComponent(props) {
   return (
     <div>
       <p>{props.name} is awesome</p>
     </div>
   );
}
DumbComponent.propTypes = {
  name: PropTypes.string,
};
DumbComponent.getDefaultProps = {
  name: 'React-CLI'
};
export default DumbComponent;
```

### @withvoid/react-cli generate router

This will init a react-router with 3 sample routes in your application

**Note:** *If your code is in src/ folder, this command will assume that there is a App.js file inside that src folder and add those 3 routes in your application*

>Again the purpose of this CLI is to make your code as easy as possible.