*This repository is a mirror of the [component](http://component.io) module [timoxley/to-array](http://github.com/timoxley/to-array). It has been modified to work with NPM+Browserify. You can install it using the command `npm install npmcomponent/timoxley-to-array`. Please do not open issues or send pull requests against this repo. If you have issues with this repo, report it to [npmcomponent](https://github.com/airportyh/npmcomponent).*
# to-array

  Try convert an object into an Array

## Installation

    $ component install timoxley/to-array

## Examples

```js
// Array-likes
var divs = document.getElementsByTagName('div') // `NodeList` of `HTMLDivElement`
toArray(divs) // => Array of `HTMLDivElement`

(function() {
  toArray(arguments) // => [1, 2]
})(1, 2)

// Primitives
toArray('hello') // => ['hello']
toArray(12345) // => [12345]
toArray(/regex/) // => [/regex/]
toArray(null) // => [null]
toArray({}) // => [{}]
toArray(window) // => [window]
toArray(new Date) // => [Wed Nov 07 2012 04:40:26 GMT+1000 (EST)]

// Special case
toArray(undefined) // => []

```

## API

### toArray(collection): Array
  Array-like structures like `arguments`, `NodeList`
  or `HTMLCollection`, will be converted into `Array`s.

  `Date`, `String`, `Regex`, `null`, `Object`, and `Function` will
  convert into an `Array`, with a single element being whatever was
  passed to `toArray`.

  `undefined` will return an empty `Array`

## Alternatives

[wilmoore/to-array.js](https://github.com/wilmoore/to-array.js): slightly different semantics.

## Contributors

* 21	Tim Oxley               75.0%
* 4	Jonny Strömberg        14.3%
* 2	Forbes Lindesay         7.1%
* 1	Dominic Barnes          3.6%

## License

  MIT
