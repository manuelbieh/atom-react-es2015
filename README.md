# Atom React ES2015+ Snippets

Some very opinionated (=[how I like it](https://www.manuelbieh.de)) React ES2015+ snippets for Atom. I try to follow community best practices and update the snippets regularly to always keep the snippets up-to-date with the recent development of React.

## React Component Class `rc`→<kbd>tab</kbd>

Hint: Use `rpc` instead to create a [PureComponent](https://facebook.github.io/react/docs/react-api.html#react.purecomponent).

```
import * as React from 'react';

export default class ${1:MyComponent} extends React.Component {
    state = {};

    render() {
        return (
            ${2:<div />}
        );
    }
}
```

## Redux connected React Component `rcrc`→<kbd>tab</kbd>

```
import * React from 'react';
import { connect } from 'react-redux';

class ${1:MyComponent} extends React.Component {
    state = {};

    render() {
        return (
            ${2:<div />}
        );
    }
}

const mapStateToProps = (state) => ({});
const mapDispatchToProps = {};

export default connect(mapStateToProps, mapDispatchToProps)(${1});
```

## Stateless Functional Component `sfc`→<kbd>tab</kbd>

```
import * as React from 'react';

const ${1} = (props) => {
    return (
        ${2:<div />}
    );
}

export default {$1};
```

## Lifecycle Methods

There is a shortcut for each of React's officially supported non-deprecated (as of 16.4) lifecycle methods. Just use the first letters of the method's words. Here's a list: 

| Shortcut | Lifecycle Method |
|---|---|
| `cwm` | `componentWillMount() {}` |
| `cdm` | `componentDidMount() {}` |
| `scu` | `shouldComponentUpdate() {}` |
| `cdu` | `componentDidUpdate() {}` |
| `cwu` | `componentWillUnmount() {}` |
| `gdsfp` | `static getDerivedStateFromProps() {}` |
| `gsbu` | `getSnapshotBeforeUpdate() {}` |

