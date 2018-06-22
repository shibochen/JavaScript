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

## Character classes

A character class is a special notation that matches any symbol from the set.
character classes inside square brackets `[...]`

有两个字符在字符类中有特殊含义
1. 脱字符（^）
2. 连字符（-）

## Escaping, special characters

`escaping a character`: to use a special character as a regular one, prepend it with a backslash.

## Quantifiers +, *, ? and {n}
Quantity {n}
模式的精确匹配次数，使用大括号（{}）表示。{n}表示恰好重复n次，{n,}表示至少重复n次，{n,m}表示重复不少于n次，不多于m次

量词符（Quantifiers） +, *, ?
-? 问号表示某个模式出现0次或1次，等同于{0, 1}。
-* 星号表示某个模式出现0次或多次，等同于{0,}。
-+ 加号表示某个模式出现1次或多次，等同于{1,}。

Reference:
- [The Modern JavaScript Tutorial](https://javascript.info/).
- [JavaScript Standards Reference Guide](http://javascript.ruanyifeng.com/).
- [MDN web docs: Regular Expressions](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Guide/Regular_Expressions).
