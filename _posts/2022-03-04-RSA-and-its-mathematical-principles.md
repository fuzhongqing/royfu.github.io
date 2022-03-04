---
title:  "RSA及其的数学原理"
tags: "RSA"
---

## 基本概念

### 素数

质数（Prime number），又称素数，指在大于1的自然数中，除了1和该数自身外，无法被其他自然数整除的数（也可定义为只有1与该数本身两个正因数的数）。前1000个素数:

>2, 3, 5, 7, 11, 13, 17, 19, 23, 29, 31, 37, 41, 43, 47, 53, 59, 61, 67, 71, 73, 79, 83, 89, 97, 101, 103, 107, 109, 113, 127, 131, 137, 139, 149, 151, 157, 163, 167, 173, 179, 181, 191, 193, 197, 199, 211, 223, 227, 229, 233, 239, 241, 251, 257, 263, 269, 271, 277, 281, 283, 293, 307, 311, 313, 317, 331, 337, 347, 349, 353, 359, 367, 373, 379, 383, 389, 397, 401, 409, 419, 421, 431, 433, 439, 443, 449, 457, 461, 463, 467, 479, 487, 491, 499, 503, 509, 521, 523, 541, 547, 557, 563, 569, 571, 577, 587, 593, 599, 601, 607, 613, 617, 619, 631, 641, 643, 647, 653, 659, 661, 673, 677, 683, 691, 701, 709, 719, 727, 733, 739, 743, 751, 757, 761, 769, 773, 787, 797, 809, 811, 821, 823, 827, 829, 839, 853, 857, 859, 863, 877, 881, 883, 887, 907, 911, 919, 929, 937, 941, 947, 953, 967, 971, 977, 983, 991, 997, ...

### 最大公约数

能够整除多个整数的最大正整数。而多个整数不能都为零。例如8和12的最大公因数为4。

$$gcd(8, 12)=4$$


### 互质

互质（英文：Coprime，符号：⊥，又称互素）。在数论中，如果两个或两个以上的整数的最大公约数是1，则称它们为互质。

$$gcd(a, b)=1 \Leftrightarrow a \perp b$$

### 同余

两个整数$$a$$，$$b$$，若它们除以正整数$$m$$所得的余数相等，则称$$a$$，$$b$$对于$$m$$同余,记作

$$ a\equiv b (\mod m) $$

读作a同余于b模m，或读作a与b关于模m同余。

比如$$ 26 \equiv 14 (\mod 12)$$。

### 欧拉函数

在数论中，对正整数n，欧拉函数 $\phi(n)$ 是小于等于n的正整数中与n互质的数的数目。

例如$$\phi(8) = 4$$，因为1,3,5,7均和8互质。

- 如果 $$p$$ 是一个素数，则  $$\phi(p)=p-1$$ 。
- 若$$m \perp n$$ ，则$$\phi(mn)=\phi(m)\phi(n)$$ （积性）。

### 欧几里得算法 (辗转相除法)

两个整数的最大公约数等于其中较小的数和两数余数的最大公约数。

$$gcd(a, b)=gcd(b,a \mod b),  a > b > 0 $$

例如:

$$ gcd(34, 10) = gcd(10, 34\mod10) = gcd(10, 4) = gcd(4, 2) = gcd(2, 0) $$

所以 34 和 10 的最大公约数是2。

### 扩展欧几里得算法

给定二个整数$$a$$、$$b$$，必存在整数$$x$$、$$y$$使得$$ax + by = gcd(a,b)$$。

### 欧拉定理


有整数$$a$$, $$p$$，且 $$a \perp p$$，那么 $$a^{\phi(p)} \equiv 1(\mod p)$$。

