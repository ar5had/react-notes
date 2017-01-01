# react-notes
Simple react notes.

## Table of Contents
- Ref
- Components


## Refs
Refs can be used modify child out of typical dataflow in react. It can be used to call child component method from parent.

``` js
var Hello = React.createClass({
    componentDidMount: function(){
        React.findDOMNode(this.refs['theInput']).focus();
    },
    render: function() {
        return (
          <div>
            <input type="text" ref='theInput'/>
            <input type="button" onClick={ this.submitForm } value="Submit!" />
          </div>
        );
    },
    submitForm: function() {
      console.log( this.refs['theInput'] );
    }
});

React.render(<Hello />, document.getElementById('container'));

```

Earlier, refs can be passed name but now refs must be passed callback.

## Components

### Stateless Components

Lifecycle methods are just like normal class methods and cannot be used in a stateless component.
