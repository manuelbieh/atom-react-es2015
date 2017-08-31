# Atom React ES2015+ Snippets

Some very opinionated (=[how I like it](https://www.manuelbieh.de)) React ES2015+ snippets for Atom. I try to follow community best practices and update the snippets regularly to always keep the snippets up-to-date with the recent development of React.

## React Component Class `rc`→<kbd>tab</kbd>

Hint: Use `rpc` instead to create a [PureComponent](https://facebook.github.io/react/docs/react-api.html#react.purecomponent).

```
import React from 'react';
import PropTypes from 'prop-types';

export default class ${1:MyComponent} extends Component {

    static propTypes = {
        ${2}
    };

    constructor(props) {
        super(props);
        this.state = {};
    }

    render() {
        return (
            ${3:<div></div>}
        );
    }

}
```

## Redux connected React Component Class `rcrc`→<kbd>tab</kbd>

```
import React from 'react';
import PropTypes from 'prop-types';
import { connect } from 'react-redux';

class ${1:MyComponent} extends React.Component {

    static propTypes = {
        ${2}
    };

    state = {};

    render() {
        return (
            ${3:<div></div>}
        );
    }

}

export default connect(
    (state, ownProps) => ({ ...ownProps, }),
    (dispatch) => ({ dispatch }),
)(${1});
```

## React Component Class with Child Context `rcc`→<kbd>tab</kbd>

```
import React from 'react';
import PropTypes from 'prop-types';

export default class ${1:MyComponent} extends Component {

    static propTypes = {
        ${2}
    };

    static childContextTypes = {
        ${3}
    };

    constructor(props) {
        super(props);
        this.state = {};
    }

    getChildContext() {
        return {
            ${4}
        };
    }

    render() {
        return (
            ${5:<div></div>}
        );
    }

}
```

## React Functional Component `rfn`→<kbd>tab</kbd>

```
import React from 'react';
import PropTypes from 'prop-types';

export default function ${1}(props) {
    return (
        ${2:<div>MyComponent</div>}
    );
}

${1}.propTypes = {
    ${3}
};
```

## React Functional Component with Context `rfnc`→<kbd>tab</kbd>

```
import React from 'react';
import PropTypes from 'prop-types';

export default function ${1}(props, context) {
    return (
        ${2:<div>MyComponent</div>}
    );
}

${1}.propTypes = {
    ${3}
};

${1}.contextTypes = {
    ${4}
};
```

## Lifecycle Methods

There is a shortcut for each of React's lifecycle methods. Just use the first letters of the method's words. `componentDidMount` = `cdm`, `componentWillReceiveProps` = `cwrp`, etc. Since `componentWillUpdate` and `componentWillUnmount` share the same letters/abbreviation you need to use `cwun` for the latter.

## PropTypes

PropType shortcuts begin with `pt` (or `rpt` if you need `React.PropTypes…`) and end with a lowercase (if optional) or uppercase (if required) letter (or letters) indicating their type (a = array, o = object, oo = oneOf, etc.). Here is a full list:

| Shortcut | PropType |
|--------|--------|
| `(r)pts` | `(React.)PropTypes.string` |
| `(r)ptS` | `(React.)PropTypes.string.isRequired` |
| `(r)ptn` | `(React.)PropTypes.number` |
| `(r)ptN` | `(React.)PropTypes.number.isRequired` |
| `(r)pto` | `(React.)PropTypes.object` |
| `(r)ptO` | `(React.)PropTypes.object.isRequired` |
| `(r)pta` | `(React.)PropTypes.string` |
| `(r)ptA` | `(React.)PropTypes.string.isRequired` |
| `(r)ptany` | `(React.)PropTypes.string` |
| `(r)ptAny` | `(React.)PropTypes.string.isRequired` |
| `(r)ptb` | `(React.)PropTypes.bool` |
| `(r)ptB` | `(React.)PropTypes.bool.isRequired` |
| `(r)ptf` | `(React.)PropTypes.func` |
| `(r)ptF` | `(React.)PropTypes.func.isRequired` |
| `(r)ptsh` | `(React.)PropTypes.shape({${1}})` |
| `(r)ptSh` | `(React.)PropTypes.shape({${1}}).isRequired` |
| `(r)ptoo` | `(React.)PropTypes.oneOf([${1}])` |
| `(r)ptOo` | `(React.)PropTypes.oneOf([${1}]).isRequired` |
| `(r)ptoot` | `(React.)PropTypes.oneOfType([${1}])` |
| `(r)ptOot` | `(React.)PropTypes.oneOfType([${1}]).isRequired` |
| `(r)ptao` | `(React.)PropTypes.arrayOf(${1})` |
| `(r)ptAo` | `(React.)PropTypes.arrayOf(${1}).isRequired` |
| `(r)ptio` | `(React.)PropTypes.instanceOf(${1})` |
| `(r)ptIo` | `(React.)PropTypes.instanceOf(${1}).isRequired` |
| `(r)pte` | `(React.)PropTypes.element` |
| `(r)ptE` | `(React.)PropTypes.element.isRequired` |
| `(r)ptnode` | `(React.)PropTypes.node` |
| `(r)ptNode` | `(React.)PropTypes.node.isRequired` |
