---
title: "Problem on Inequalities and Number Theory"
weight: 100
draft: false
showAuthor: true
mathjax: true
date: 2026-02-27
---

### Introduction
The following problem appeared in the IOQM 2023 paper.
Let $\alpha,\beta$ be positive integers such that
$$
\frac{16}{37}<\frac{\alpha}{\beta}<\frac{7}{6}
$$
Find the smallest possible value of $\beta$.
There is a brute force solution for this, where we either cross-multiply by $\beta$ to get
$$
\frac{16}{37}\beta<\alpha<\frac{7}{6}\beta
$$
and then take cases by increasing the value of $\beta$ from $1,2,3,\dots$ till we get a possible integral value of $\alpha$ satisfying the above inequality.
Rather than resorting to computational brute force, we can employ elementary number theory to derive an optimal solution.

### Analysis of the Problem from a Number Theory Perspective
We cross-multiply by $\beta$:
$$
\frac{16\beta}{37}<\alpha<\frac{7\beta}{6}
$$
Now eliminate fractions:
$$
16^2\beta<37\cdot16\alpha<7\cdot37\beta
$$
$$
256\beta<592\alpha<259\beta
$$
Hence,
$$
592\alpha=256\beta+k
$$
where
$$
1\le k\le 3\beta-1
$$
Since
$$
\gcd(592,256)=16
$$
we obtain
$$
16(37\alpha-16\beta)=k
$$
Let
$$
k=16p
$$
Then
$$
37\alpha-16\beta=p
$$
where
$$
1\le p\le \frac{3\beta-1}{16}
$$
Now since
$$
\gcd(37,16)=1
$$
Bezout's theorem guarantees integers $x,y$ such that
$$
37x-16y=1
$$
Using Euclidean algorithm:
$$
37=16\cdot2+5
$$
$$
16=5\cdot3+1
$$
Thus,
$$
1=16-5\cdot3
$$
$$
=16-(37-16\cdot2)\cdot3
$$
$$
=16-37\cdot3+16\cdot6
$$
$$
=16\cdot7-37\cdot3
$$
Hence,
$$
37(-3)+16(7)=1
$$
Now suppose $x,y$ is another solution. Then
$$
37x+16y=1
$$
Subtracting the known solution:
$$
37(x+3)=16(7-y)
$$
Since
$$
\gcd(37,16)=1
$$
we get
$$
x+3=16a
$$
and
$$
7-y=37a
$$
for some
$$
a\in\mathbb Z
$$
Hence the general solution becomes
$$
x=16a-3
$$
$$
y=7-37a
$$
Therefore,
$$
37(16a-3)+16(7-37a)=1
$$
Multiplying by $p$:
$$
37(16a-3)p+16(7-37a)p=p
$$
Now let $x,y$ satisfy
$$
37x+16y=p
$$
Then
$$
37\left[x-(16a-3)p\right]
16\left[(7-37a)p-y\right]
$$
Again using coprimality:
$$
x-(16a-3)p=16b
$$
$$
(7-37a)p-y=37b
$$
Thus,
$$
x=16(ap+b)-3p
$$
$$
y=7p-37(ap+b)
$$
Now compare with
$$
37\alpha-16\beta=p
$$
Hence,
$$
\alpha=16(ap+b)-3p
$$
$$
\beta=37(ap+b)-7p
$$
where
$$
1\le p\le \frac{3\beta-1}{16}
$$
Take
$$
a=0
$$
Then
$$
\beta=37b-7p
$$
Substitute into the inequality:
$$
p\le \frac{3(37b-7p)-1}{16}
$$
$$
16p\le111b-21p-1
$$
$$
37p\le111b-1
$$
$$
p\le3b-\frac1{37}
$$
Thus,
$$
p\le3b-1
$$
Therefore,
$$
\beta=37b-7p
\ge37b-7(3b-1)
$$
$$
=16b+7
$$
Minimum occurs at
$$
b=1
$$
Hence,
$$
\beta_{\min}=16(1)+7=23
$$
Now verify positivity of $\alpha$:
$$
\alpha=16(1)-3(2)=16-6=10>0
$$
Therefore the smallest possible value is
$$
\boxed{23}
$$
