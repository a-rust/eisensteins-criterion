# Project Description
This is a command line tool that generates random polynomials in $\mathbb{Z}[x]$ and determines if they are irreducible over $\mathbb{Q}$ via [Eisenstein's criterion](https://en.wikipedia.org/wiki/Eisenstein's_criterion).

# Overview of Theorem
Consider the polynomial $p(x) = a_0 + a_1(x) + a_2(x^2) + ... + a_n(x^n)$, where $a_i \in \mathbb{Z}$.

Eisenstein's criterion states that $p(x)$ is irreducible over $\mathbb{Q}$ if there exists a prime number $p\in \mathbb{Z}$ such that:
1. $p$ divides each $a_i$ for $0 \leq i < n$,
2. $p$ does not divide $a_n$
3. $p^2$ does not divide $a_0$

> Note: Eisenstein's criterion can be applied directly to $p(x)$, or [indirectly](https://en.wikipedia.org/wiki/Eisenstein's_criterion#Direct_(without_transformation)) to a transformation of $p(x)$. Both cases prove irreducibility of $p(x)$. This project focuses only on applying Eisenstein's criterion to $p(x)$ directly.

# How to run the program yourself
~~~
git clone https://github.com/a-rust/eisensteins-criterion.git
cd eisensteins-criterion
cargo run
~~~

# Parameters
The following parameters can be set when running the program:
* Degree $n$ of $p(x)$ (defaults to a random $2\leq n\leq 10$ if no value specified)
* Upper bound on the randomly chosen coefficients of $p(x)$ (defaults to $100$ if no value specified)
