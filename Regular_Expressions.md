# Regular Expression

Regular expression is a powerful way of searching and replacing inside a string.

A regular expression consists of a pattern and optional flags: g, i, m, u, y.

## create a regular expression

One: regular expression literal, which consist of a patten enclosed between slashes, as follow

```
var regExp = /pattern/;  //no flags
var regExp = /pattern/gmi; //with flags g, m and i
```
Two: calling the constructor function of the `RegExp` object, as follows:
```
var regExp = new RegExp("pattern", "flags")
```
## Methods of RegExp and String
![capture](https://user-images.githubusercontent.com/38870192/41758407-6917d156-75b6-11e8-8c57-dd1bf764b38a.PNG)

Reference:
- [The Modern JavaScript Tutorial](https://javascript.info/).
- [JavaScript Standards Reference Guide](http://javascript.ruanyifeng.com/).
- [MDN web docs: Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).
