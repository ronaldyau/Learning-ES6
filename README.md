# Learning-ES6

## let and const

### _let_ - how it is different from _var_
* Defines variables scoped at the block level
* Global let variables are not properties on the global object. They live in the scope of an invisible block that notionally encloses all JS code.
* Loops of the form for (let x...) create a fresh binding for x in each iteration.
* Redeclaring a variable with let is a SyntaxError.
* Trying to use a let variable before its declaration is reached results in an error

```javascript
if (true) {
  let foo = "bar";
}
foo; // will give an error because it is out of scope
```
[Fiddle](http://www.es6fiddle.net/igy3htmr/)

[let in more details](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Statements/let)

### The const declaration

* can't declare it without giving it a value
```javascript
const pi = 3.14159265359;
pi = 420; // SyntaxError
```
[Fiddle](http://www.es6fiddle.net/igy53z83/)


## Arrow function a.k.a Fat Arrow Function =>

`let add = function(x, y) {
  return x + y;
};`

`let add = (x, y) => x + y;`

[Arrow function in more details](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Functions/Arrow_functions)


# Transpilers
Babel
`npm install babel -g`

`babel source.js --out-file output.js`

Adding source maps

`babel source.js --out-file output.js --source-maps`

Transpiling a directory

`babel libfolder --out-dir buildfolder`

Concatenate folder or mulitple files

`babel libfolder --out-file concat.js`

Used withing grunt, gulp, or webpack

# References
[ES6 In Depth](https://hacks.mozilla.org/category/es6-in-depth/)

[ES6 Features](https://github.com/lukehoban/es6features)

# Tools

## Compilers
* [Babel](http://babeljs.io/)
* [Traceur](https://github.com/google/traceur-compiler)
* [TypeScript](http://www.typescriptlang.org/)

## Play with ES6
[Traceur Transcoding Demo](https://google.github.io/traceur-compiler/demo/repl.html)

[ES6 Fiddle](http://www.es6fiddle.net/)

