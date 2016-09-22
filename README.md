# Atom React ES2015 Snippets

Some very opinionated (= how <a href="https://www.github.com/manuelbieh">I</a> like it) React ES2015/2016/2017/Stage-0 snippets for Atom

## React Component Class `rc`→<kbd>tab</kbd>
```
import React, { PropTypes, Component } from 'react';

export default class ${1:MyComponent} extends Component {

    static propTypes = {
    };

    constructor(props) {
        super(props);
        this.state = {};
    }

    render() {
        return (
            ${2:<div></div>}
        );
    }

}
```

## React Functional Component `rfn`→<kbd>tab</kbd>
```
import React, { PropTypes } from 'react';

export default function ${1}(props) {
    return (
        ${2:<div>MyComponent</div>}
    );
}

${1}.propTypes = {
};
```

## Lifecycle Methods

There is a shortcut for each of React's lifecycle methods. Just use the first letters of the method's words. `componentDidMount` = `cdm`, `componentWillReceiveProps` = `cwrp`, etc. Since `componentWillUpdate` and `componentWillUnmount` share the same letters/abbreviation you need to use `cwun` for the latter.

## PropTypes

PropType shortcuts begin with `pt` and end with a lowercase (if optional) or uppercase (if required) letter (or letters) indicating their type (a = array, o = object, oo = oneOf, etc.). Here is a full list:

| Shortcut | PropType |
|--------|--------|
| `pts` | `PropTypes.string` |
| `ptS` | `PropTypes.string.isRequired` |
| `ptn` | `PropTypes.number` |
| `ptN` | `PropTypes.number.isRequired` |
| `pto` | `PropTypes.object` |
| `ptO` | `PropTypes.object.isRequired` |
| `pta` | `PropTypes.string` |
| `ptA` | `PropTypes.string.isRequired` |
| `ptany` | `PropTypes.string` |
| `ptAny` | `PropTypes.string.isRequired` |
| `ptb` | `PropTypes.bool` |
| `ptB` | `PropTypes.bool.isRequired` |
| `pte` | `PropTypes.element` |
| `ptE` | `PropTypes.element.isRequired` |
| `ptf` | `PropTypes.func` |
| `ptF` | `PropTypes.func.isRequired` |
| `ptsh` | `PropTypes.shape({${1}})` |
| `ptSh` | `PropTypes.shape({${1}}).isRequired` |
| `ptoo` | `PropTypes.oneOf({${1}})` |
| `ptOo` | `PropTypes.oneOf({${1}}).isRequired` |
| `ptoot` | `PropTypes.oneOfType({${1}})` |
| `ptOot` | `PropTypes.oneOfType({${1}}).isRequired` |
| `ptnode` | `PropTypes.node` |
| `ptNode` | `PropTypes.node.isRequired` |
