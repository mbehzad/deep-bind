# deep-bind [![NPM version](https://img.shields.io/npm/v/deep-bind.svg)](https://www.npmjs.com/package/deep-bind) [![Build Status](https://img.shields.io/travis/jonschlinkert/deep-bind.svg)](https://travis-ci.org/jonschlinkert/deep-bind)

> Bind a context to all functions in an object, including deeply nested functions.

## Install

Install with [npm](https://www.npmjs.com/):

```sh
$ npm install deep-bind --save
```

## Usage

```js
var deepBind = require('deep-bind');
```

**Example**

Bind a context to an object of template helpers before passing them to an engine:

```js
var ctx = {
  app: {views: {}},
  context: {a: 'b'}
};

// pass the following to the template engine
var helpers = deepBind({
  foo: function() {
    return this.context;
  },
  bar: function() {},
  baz: function() {}
}, ctx);
```

## API

### [deepBind](index.js#L14)

Bind a `thisArg` to all the functions on the target

**Params**

* `target` **{Object|Array}**: Object or Array with functions as values that will be bound.
* `thisArg` **{Object}**: Object to bind to the functions
* `returns` **{Object|Array}**: Object or Array with bound functions.

## Related projects

## Contributing

Pull requests and stars are always welcome. For bugs and feature requests, [please create an issue](https://github.com/jonschlinkert/deep-bind/issues/new).

## Building docs

Generate readme and API documentation with [verb](https://github.com/verbose/verb):

```sh
$ npm install verb && npm run docs
```

Or, if [verb](https://github.com/verbose/verb) is installed globally:

```sh
$ verb
```

## Running tests

Install dev dependencies:

```sh
$ npm install -d && npm test
```

## Author

**Jon Schlinkert**

* [github/jonschlinkert](https://github.com/jonschlinkert)
* [twitter/jonschlinkert](http://twitter.com/jonschlinkert)

## License

Copyright © 2016 [Jon Schlinkert](https://github.com/jonschlinkert)
Released under the [MIT license](https://github.com/jonschlinkert/deep-bind/blob/master/LICENSE).

***

_This file was generated by [verb](https://github.com/verbose/verb), v0.9.0, on February 24, 2016._