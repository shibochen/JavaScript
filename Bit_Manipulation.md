# Bit Manipulation (位运算)

`Bit Manipulation`: It manipulates integers on bit levels.

## 原码， 反码，补码
①正数的反码和补码都与原码相同。 <br>
②而负数的反码为对该数的原码除符号位外各位取反。 <br>
③负数的补码为对该数的原码除符号位外各位取反，然后在最后一位加1

下面是书上原文：

①原码表示法规定：用符号位和数值表示带符号数，正数的符号位用“0”表示，负数的符号位用“1”表示，数值部分用二进制形式表示。 <br>
②反码表示法规定：正数的反码与原码相同，负数的反码为对该数的原码除符号位外各位取反。 <br>
③补码表示法规定：正数的补码与原码相同，负数的补码为对该数的原码除符号位外各位取反，然后在最后一位加1. <br> 
④正零和负零的补码相同，[+0]补=[-0]补=0000 0000B。


## Bitwise Operators(位运算符号)


## Reference
- [原码， 反码，补码](https://blog.csdn.net/shenhaiwen/article/details/79001039)
- [Java位运算原理及使用讲解](https://blog.csdn.net/goskalrie/article/details/52796360)
- [MDN web docs: Bitwise operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators)
