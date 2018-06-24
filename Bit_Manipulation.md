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
![capture](https://user-images.githubusercontent.com/38870192/41815560-ba5d6bfc-773c-11e8-9793-74ae14d2bf4c.PNG)

左移： 比如 1 -- 0001  每一位都是乘 2， 右移： 每移一位都是除以2
     
无符号右移>>> :不管正负标志位为0还是1，将该数的二进制码整体右移，左边部分总以0填充，右边部分舍弃。

## 常考技巧
1. 判断是否为2的倍数：  n & （n - 1） == 0
2. 判断奇偶数： n & 1 （返回 1 表示奇数， 0 表示偶数）

## 面试题型分析
1. XOR
2. 移位
3. 数据量过小/过大： 过小（Bit（方向））， 过大（Bit Map/ Bit Set）

## Reference
- [原码， 反码，补码](https://blog.csdn.net/shenhaiwen/article/details/79001039)
- [Java位运算原理及使用讲解](https://blog.csdn.net/goskalrie/article/details/52796360)
- [MDN web docs: Bitwise operators](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Operators/Bitwise_Operators)
