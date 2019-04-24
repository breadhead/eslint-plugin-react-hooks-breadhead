# eslint-plugin-react-hooks-breadhead

## What is this

This is a fork of [eslint-plugin-react-hooks](https://github.com/facebook/react/tree/master/packages/eslint-plugin-react-hooks) which allows omitting  `dispatch` in dependencies array in hooks

## Example


```js

function Foo(props) {
  const dispatch = useThunk();
  useEffect(() => {
    console.log(dispatch);
  }, []); // <-- should not error
}

```

```js

function Foo(props) {
  const test = {}
  useEffect(() => {
    console.log(test);
  }, []); // <-- should error
}

```


## Installation

```

yarn add eslint-plugin-react-hooks-breadhead --dev

```


## Usage

```js

{
  "plugins": [
      "react-hooks-breadhead"
  ],
  "rules": {
    "react-hooks-breadhead/exhaustive-deps": "error"
  }
}

```
