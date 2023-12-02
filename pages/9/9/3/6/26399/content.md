
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Measure and probability theory
+-- {: .hide}
[[!include measure theory - contents]]
=--
#### Categorical algebra
+-- {: .hide}
[[!include categorical algebra -- contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

The _convex powerset of distributions monad_ is a [[monad]] (or family of monads) that encompasses both [[nondeterministic computation|non-determinism]] (via [[power sets]]) and [[probability]] (via [[probability distributions]]). 


## Definition

The finitary version of the monad is defined as follows. First recall that for any [[finite set]] $n$, the set of [[probability distributions]] $\Delta(n)\subseteq [0,1]^n$,

$$\Delta(n)=\{(r_1,\dots,r_n)\in[0,1]^n | \textstyle \sum_{i=1}^n r_i=1\}$$ 

is the [[topological simplex|topological $n$-simplex]]. A subset $S\subseteq \Delta(n)$ is _[[convex set|convex]]_ if it is closed under [[convex combinations]], i.e. if $\vec r\in S$ and $\vec s\in S$ then $(a\vec r+(1-a) \vec s)\in S$ for any $a\in[0,1]$. 

Any finite set of points $\{\vec r_1\dots \vec r_k\}\subseteq \Delta(n)$ _generate_ a convex set (the [[convex hull]]):

$$[\vec r_1\dots \vec r_k] = \{
a_1\vec r_1 + \dots +a_k\vec r_k | 
(a_1,\dots, a_k)\in [0,1]^k \& \textstyle \sum_{j=1}^k a_j=1
\}$$

(Recall that the convex hull is not uniquely determined by such a set of points, since some points in the generating set maybe convex combinations of others.)

Let $C(n)$ be the set of finitely generated convex subsets of $\Delta(n)$. 

* $C(n)$ has the structure of a [[semilattice]], with $S\oplus T$ the [[union]] of $S$ and $T$ closed under convex combinations. 

* It also has the structure of a [[convex space]], with 
$[\vec r_1\dots \vec r_k]+_p [\vec s_1\dots \vec s_l]$ defined to be

$$ 
\array{[p\vec r_1+(1-p)\vec s_1,&\dots,&p\vec r_k+(1-p)\vec s_1,\\
\dots,&\dots,&\dots,\\
p\vec r_1+(1-p)\vec s_l,&\dots,&p\vec r_k+(1-p)\vec s_l].}$$

We thus build a monad structure for $C(n)$: 

* The [[unit of a monad|unit]], $\eta_n:n\to C(n)$, picks out the singleton sets containing the basis vectors: $\eta_n(1) = \{(1,0,\dots,0)\}$, $\eta_n(2) = \{(0,1,\dots,0)\}$, and so on.

* The bind, or [[Kleisli extension]], takes a function 
$f:m\to C(n)$ to a function $f^*:C(m)\to C(n)$, given by using the convex and semilattice structures:

$$
f^*([\vec r_1\dots \vec r_k]) = 
(r_{1,1}f(1)+\dots+r_{1,m}f(m))
\oplus \dots\oplus
(r_{k,1}f(1)+\dots+r_{k,m}f(m)).
$$

## Presentation

The finitary convex powerset of distributions monad is presented by an [[equational theory]]. This has the theory of [[convex spaces]] ($+_r$) together with the theory of [[semilattices]] ($\oplus$) and the axiom

$$ x +_r (y \oplus z) = (x +_r y) \oplus (x +_r z) $$

for all $r\in (0,1)$. 

(It may be tempting to think that this is a [[distributive law]] of monads, but it is not, because two sets of distributions are equated if they have the same convex hull. For instance, $x\oplus y = x \oplus y \oplus (x+_0.5 y)$, for:

$$ x \oplus y = 
(x \oplus y) +_0.5 (x \oplus y)
= 
(x +_0.5 x)\oplus (x +_0.5 y) \oplus (y +_0.5 x) \oplus (y +_0.5 y)
=
x \oplus y \oplus (x +_0.5 y) \ .)$$

## References

Convex powersets of distributions have been considered by various authors over the last few decades. A recent survey is:

* Matteo Mio, Valeria Vignudelli, *Monads and Quantitative Equational Theories for Nondeterminism and Probability*,in:  *CONCUR 2020*, LIPIcs **171** (2020) 28:1-28:18, &lbrack;[doi:10.4230/LIPIcs.CONCUR.2020.28](https://doi.org/10.4230/LIPIcs.CONCUR.2020.28), [hal:03028173](https://hal.science/hal-03028173), [arXiv:2005.07509](https://arxiv.org/abs/2005.07509)&rbrack;

[[!redirects convex powerset of distributions monads]]
