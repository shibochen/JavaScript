# Bit Manipulation

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


## Java Bitwise Operators

| operator | Name | Description|
| :---: | :---: | :---: |
| & | AND | Sets each bit to 1 if both bits are 1 |
| \| | OR | Sets each bit to 1 if one of two bits is 1 |
| ^ | XOR | Sets each bit to 1 if only one of two bits is 1 |
| ~ | NOT | Inverts all the bits |
| << | signed left shift | Shifts left by pushing zeros in from the right and let the leftmost bits fall off |
| >> | signed right shift | Shifts right by pushing copies of the leftmost bit in from the left, and let the right most bits fall off |
| <<< | unsigned left shift | Shifts left by pushing zeroes in from the right, and let the leftmost bits fall off |
| >>> | unsigned right shift | Shifts right by pushing zeroes in from the left, and let the rightmost bits fall off |

## Examples
![bm_examples](https://user-images.githubusercontent.com/38870192/39669857-fbd78eca-50c5-11e8-84f8-9859f482f958.PNG)

## Reference
[原码， 反码，补码]{https://blog.csdn.net/shenhaiwen/article/details/79001039}
[Java位运算原理及使用讲解]{https://blog.csdn.net/goskalrie/article/details/52796360}
