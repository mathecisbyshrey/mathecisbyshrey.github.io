---
title: "Story of Primes"
weight: 100
draft: false
showAuthor: true
mathjax: true
date: 2026-03-10
---

### What are Prime Numbers?

Most of us would answer: a prime number is a number divisible only by \(1\) and itself. True — but there is much more hidden inside prime numbers than this simple definition suggests.

Have we ever wondered whether prime numbers can be written as a sum of two squares?

Which prime numbers can be written in the form

$$
x^2+y^2
$$

A quick exploration of small primes reveals that numbers such as \(2\), \(5\), and \(13\) can indeed be expressed in this form, whereas \(3\), \(7\), and \(11\) cannot.

This naturally leads to a deeper question:

Is there a general rule?

Indeed, there is.

A prime number \(p\) can be expressed as

$$
x^2+y^2
$$

if and only if

$$
p=2
\quad\text{or}\quad
p\equiv1\pmod4
$$

This elegant criterion invites an even broader question:

For a fixed integer \(n\), which prime numbers can be written in the form

$$
x^2+n y^2
$$

This leads us to a beautiful and classical result in number theory known as **Fermat’s Christmas Theorem**.

---

### Fermat’s Christmas Theorem

## Statement

An odd prime number \(p\) can be written in the form

$$
p=a^2+b^2
$$

for some integers \(a,b\), if and only if

$$
p\equiv1\pmod4
$$

Thus, primes of the form

$$
4k+1
$$

are exactly the primes that can be represented as the sum of two squares.

---

# Why is it called the “Christmas Theorem”?

The theorem was first stated by
\[
\text{Pierre de Fermat}
\]
in a letter written in \(1640\), where he mentioned that he had discovered the proof on Christmas Day.

Because of this historical anecdote, the result became known as **Fermat’s Christmas Theorem**.

---

## Proof

Consider the set of complex numbers of the form

$$
a+bi
$$

where \(a\) and \(b\) are integers.

These numbers are called **Gaussian integers**.

For any Gaussian integer

$$
z=a+ib
$$

define its norm by

$$
N(z)=a^2+b^2
$$

An important property of the norm is:

$$
N(z_1z_2)=N(z_1)N(z_2)
$$

Thus, the norm of a product equals the product of the norms.

Now suppose \(p\) is a prime number satisfying

$$
p\equiv1\pmod4
$$

From elementary number theory, we know that for such primes there exists an integer \(x\) such that

$$
x^2\equiv-1\pmod p
$$

Equivalently,

$$
x^2+1\equiv0\pmod p
$$

Hence \(p\) divides \(x^2+1\).

Now observe that

$$
x^2+1=(x+i)(x-i)
$$

inside the Gaussian integers.

Thus \(p\) divides the product

$$
(x+i)(x-i)
$$

In the Gaussian integers, a prime satisfying

$$
p\equiv1\pmod4
$$

is no longer prime.

Therefore \(p\) must factorize as

$$
p=(a+bi)(a-bi)
$$

for some integers \(a,b\).

Now take norms on both sides:

$$
N(p)=N(a+bi)N(a-bi)
$$

But

$$
N(p)=p^2
$$

and

$$
N(a+bi)=a^2+b^2
$$

Similarly,

$$
N(a-bi)=a^2+b^2
$$

Therefore,

$$
p^2=(a^2+b^2)^2
$$

Taking square roots gives

$$
p=a^2+b^2
$$

Hence every prime number \(p\) satisfying

$$
p\equiv1\pmod4
$$

can be written as the sum of two squares.

\[
\boxed{\text{Q.E.D.}}
\]
