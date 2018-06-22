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


Reference:
1. [The Modern JavaScript Tutorial] (https://javascript.info/)
2. [JavaScript Standards Reference Guide] (http://javascript.ruanyifeng.com/)
3. [MDN web docs: Regular Expressions] (https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions)
