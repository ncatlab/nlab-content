
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea 

A partial combinatory algebra is a generalization of a model of the [[untyped lambda calculus]] allowing for application to be only partially defined.  It is often expressed as an algebraic abstraction of [[combinatory logic]].

## Definition 

The following definitions are taken from [Hofstra](#Hofstra). 

A _partial applicative structure_ is a set equipped with a partial binary operation 

$$m \colon A \times A \to A$$ 

An [[function application|application]] of $m$ is indicated by juxtaposition: $a b$ denotes $m(a, b)$ if (and only if) $m(a, b)$ is defined, i.e., if $(a, b)$ belongs to the [[domain]] of $m$. _Homomorphisms_ between partial applicative structures $A, B$ are defined to be total functions $f \colon A \to B$ such that $f(a b) = f(a)f(b)$, meaning the right side is defined whenever the left side is. In other words, in the locally posetal [[bicategory]] of sets and [[relation|relations]], we have a 2-cell 

$$\array{
A \times A & \stackrel{f \times f}{\to} & B \times B \\
m \downarrow & \leq & \downarrow m \\
A & \underset{f}{\to} & B
}$$ 

By convention, unbracketed juxtapositions are associated to the left, so that for example $x y z$ means $(x y)z$. 

If $A$ is a partial applicative structure and $\mathbf{Magma}(A)$ is the free [[magma]] on the underlying set of $A$, then we have an evident partial function 

$$\alpha \colon \mathbf{Magma}(A) \to A$$ 

which evaluates binary words in $A$ as elements in $A$, whenever possible, using the partial applicative structure and induction on the structure of the word. 

+-- {: .num_defn}
###### Definition 
A partial applicative structure $A$ is a _partial combinatory algebra_ (a **PCA**) if there are elements $k, s \in A$ such that

* For all $a, b \in A$, $k a$ and $k a b$ are defined and $k a b = a$. 
* For all $a, b \in A$, $s a$ and $s a b$ are defined and for all $c$, $(a c)(b c)$ is defined if and only if $s a b c$ is defined, and $s a b c = (a c)(b c)$. 

A _homomorphism_ of PCA's is a homomorphism of the underlying partial applicative structures. 

A _total_ combinatory algebra is a PCA $A$ whose application $m \colon A \times A \to A$ is a total function. 
=-- 

Note that appropriate elements $k$, $s$ are not considered part of the structure (to be preserved under homomorphism) -- here one is interested only in the property that such elements exist. Indeed, they need not be uniquely determined within the PCA. 

## Functional completeness 

The definition of PCA given above is traditional but somewhat opaque at first glance. The real point of the definition is that a PCA is the same thing as a partial applicative structure $A$ that enjoys a _functional completeness_ property, in the following sense. 

Let $X$ be a countably infinite set of "variables", and let $A[X]$ denote the [[magma]] freely generated from the disjoint sum $A + X$. Each term $t$, i.e., each element $t \in A[X]$, has finitely many $x_i \in X$ occurring inside it; these are called the _free variables_ of $t$, and we write $FV(t)$ for the set of free variables. If $FV(t) \subseteq \{x_0, x_1, \ldots, x_n\}$, then we can think of $t$ as giving a partially defined function in $n+1$ variables. That is, we may consider $t$ as a term of $\mathbf{Magma}(A + \{x_0, \ldots, x_n\})$, and (partially) define the [[substitution]] $t[a_0/x_0, \ldots, a_n/x_n]$ where $a_0, \ldots, a_n$ are elements of $A$, by evaluating at $t$ of the composite 

$$\mathbf{Magma}(A + \{x_0, \ldots, x_n\}) \stackrel{\mathbf{Magma}(\phi)}{\to} \mathbf{Magma}(A) \stackrel{\alpha}{\to} A$$ 

where $\phi(x_i) = a_i$ and is elsewhere the identity. 

Then, we say $A$ is _functionally complete_ if every term $t \in A[X]$, viewed as a partial operation on $A$, is represented by some element in $A$. To be precise: for each term $t$ with $FV(t) \subseteq \{x_0, \ldots, x_n\}$, there exists an element $a \in A$ such that 

* For all $a_0, \ldots, a_{n-1} \in A$, $a a_0 \ldots a_{n-1}$ is defined; 

* For all $a_0, \ldots, a_n \in A$, $t[a_0/x_0, \ldots, a_n/x_n]$ is defined precisely when $a a_0 \ldots a_n$ is defined, and these two elements are equal. 

For example, if $k$, $s$ are elements which realize $A$ as a PCA, then $k$ represents the term $t = x_0$ viewed as belonging to $\mathbf{Magma}(A + \{x_0, x_1\})$, and $s$ represents the term $(x_0 x_2)(x_1 x_2)$ viewed as belonging to $\mathbf{Magma}(A + \{x_0, x_1, x_2)\}$. 

+-- {: .num_theorem} 
###### Theorem 
A partial combinatory algebra is functionally complete. 
=-- 

+-- {: .proof}
###### Proof 
The idea is to simulate $\lambda$-abstraction $\lambda x. t$, where $x \in X$ is a variable and $t$ is a term, by induction on $t$. Indeed, given elements $k, s$ that realize $A$ as a PCA, put 

$$\array{
\lambda x. x & \coloneqq & s k k & \\
\lambda x. t & \coloneqq & k t & if  x \notin FV(t) \\
\lambda x. t t' & \coloneqq & s(\lambda x. t)(\lambda x. t')
}$$ 

One then proves equality of partial functions $(\lambda x. t)(a) = t[a/x]$, by induction on $t$. 
=-- 

[Hofstra](#Hofstra) _defines_ a PCA to be a functionally complete partial applicative structure. This is an unbiased definition, in the sense that it does not privilege certain elements $k$, $s$ (or, for that matter, any other system of combinators that provide functional completeness). 

### Examples of combinators
 {#ExamplesOfCombinators}

1. Let us check that $s k k$ indeed represents the identity function $I$. This is trivial: we have, for any $a \in A$, equalities between defined terms 
$$s k k a = (k a)(k a) = a.$$

1. Consider the second projection function, corresponding to $x_1 \in \mathbf{Magma}(A + \{x_0, x_1\})$. Thinking in terms of $\lambda$-terms, this is represented by $\lambda x. \lambda y. y = \lambda x. s k k = k(s k k)$, or $k I$. In other words, we calculate 
$$k I a b = ((k I) a) b = I b = b.$$ 

1. Following the proof of functional completeness, we have 
$$\lambda x. x x = s(\lambda x. x)(\lambda x. x) = s I I$$ 

1. {#FinallyClassicalConstruction} Finally, consider the classical construction of the [[fixed-point combinator]], $Y = \lambda y. (\lambda x. y(x x))(\lambda x. y(x x))$. We have firstly 
$$\lambda x. y(x x) = s(\lambda x. y)(\lambda x. x x) = s(k y)(s I I)$$ 
which means 
$$\array{
Y & = & \lambda y. (s I I)(s(k y)(s I I)) \\
 & = & s(\lambda y. s I I)\big(\lambda y. s(k y)(s I I)\big) \\ 
 & = & s(k (s I I)) \big(s(\lambda y. s(k y))(\lambda y. s I I)\big) \\ 
 & = & s(k (s I I)) \big(s(s(k s)k)(k (s I I))\big)
}$$


## Examples of PCAs

1. (Kleene's first algebra.) Suppose given a coding of all [[partial recursive functions]] of the form  $\mathbb{N}^k \to \mathbb{N}$ 
(ranging over $k = 0, 1, 2, \ldots$) by elements of $\mathbb{N}$, and a coding of elements of $\mathbb{N}^k$ over all $k$ by elements of $\mathbb{N}$. Define a partial applicative structure  
$$\mathbb{N} \times \mathbb{N} \to \mathbb{N}$$ 
where $p q = \{p\}([q])$ whenever the right side is defined, where $\{p\}$ is the $p^{th}$ partial recursive function and $[q]$ is the $q^{th}$ tuple. It may be checked that $k$ and $s$, defined extensionally in the obvious way, are partial recursive functions, so we get in this way a PCA. 

1. Suppose we have a [[cartesian closed category]] generated by an object $X$ such that $X \times X$ and $X^X$ are retracts of $X$. Then elements $1 \to X$ form a PCA, in fact a total combinatory algebra, where the applicative structure is 
$$X \times X \stackrel{r \times 1_X}{\to} X^X \times X \stackrel{eval}{\to} X$$ 
for some chosen retraction $r$. In other words, models of the untyped [[lambda calculus]] give PCA's. 

1. [[Kleene's second algebra]]. 

## Realizability toposes 

From any PCA, a corresponding "[[realizability]] [[tripos]]" can be constructed, from which, in turn, a corresponding "realizability topos" can be constructed, as outlined in the article on [[tripos|triposes]]. 

A preliminary technical task is to encode pairing and unpairing functions by elements of $A$. By this we mean functions $p \colon A \times A \to A$, $l \colon A \to A$, $r \colon A \to A$ such that for all $(a, a') \in A \times A$, we have $(a, a') = (l(p(a, a')), r(p(a, a')))$. One way of doing this is to put 

* $p = \lambda x. \lambda y. \lambda z. z x y$

* $l = \lambda p. p(\lambda x. \lambda y. x)$ 

* $r = \lambda p. p(\lambda x. \lambda y. y)$ 

whereupon we may calculate 

$$\array{
p a a' & = & \lambda z. z a a' \\
l(p a a') & = & (\lambda z. z a a')(\lambda x. \lambda y. x) \\
 & = & (\lambda x. \lambda y. x) a a' \\
 & = & (\lambda y. a) a' = a
}$$ 

$$\array{
r(p a a') & = & (\lambda z. z a a')(\lambda x. \lambda y. y) \\
 & = & (\lambda x. \lambda y. y) a a' \\
 & = & (\lambda y. y) a' = a'
}$$ 

That out of the way, let $P(A)$ be the power set of $A$ and let $X$ be a set. 
Put a preorder structure on $P(A)^X$ as follows: given $f, g \in P(A)^X$, let $Hom(f, g)$ be the set of $a$ in $A$ such that for all $x$ in $X$ and $a'$ in $f(x)$, $a a'$ is defined (that is, $a$ is applicable to $a'$), and $a a'$ is an element of $g(x)$. We can turn this into a preorder by taking $f \leq g$ just in case $Hom(f, g)$ is inhabited. 

+-- {: .num_theorem} 
###### Theorem 
The preorder $P(A)^X$ has finite products, finite coproducts, and is cartesian closed. In other words, the preorder $P(A)^X$ is a [[Heyting prealgebra]]. 
=-- 

+-- {: .proof} 
###### Proof 
An initial object is given by the constant function taking each $x$ to the empty subset $\emptyset \subseteq A$, and a terminal object is given by the constant function taking each $x$ to the full subset $A \subseteq A$. 

Take $f, g \colon X \to P(A)$. For binary products, define 

$$(f \wedge g)(x) = \{p a a' | a \in f(x) \wedge a' \in g(x)\}$$ 

Notice that $l$ realizes $f \wedge g \leq f$ (since $l (p a a') = a$), and similarly $r$ realizes $f \wedge g \leq g$. Furthermore, suppose given $h \colon X \to P(A)$, and that $t \in A$ realizes $h \leq f$ and $u \in A$ realizes $h \leq g$. Then 

$$v = \lambda b. p (t b)(u b)$$ 

realizes $h \leq f \wedge g$. Thus $f \wedge g$ is a product in the preorder. 

For binary coproducts, define 

$$(f \vee g)(x) = \{p l a | a \in f(x)\} \cup \{p r a' | a' \in g(x)\}$$ 

Then $p l$ realizes $f \leq f \vee g$ and $p r$ realizes $g \leq f \vee g$. Furthermore, suppose $t$ realizes $f \leq h$ and $u$ realizes $g \leq h$. Then 

$$v = \lambda b. l(b)(p(t(r b))(u(r b)))$$ 

realizes $f \vee g \leq h$. Indeed, we have 

$$\array{
v(p l a) & = & l(p l a)(p(t(r(p l a)))(u(r(p l a)))) \\ 
 & = & l(p(t a)(u a)) \\
 & = & t a
}$$ 

and similarly $v(p r a') = u a'$. In either case, we see $v(b)$ lives in $h(x)$ for any $b \in (f \vee g)(x)$. 

For cartesian closure, define 

$$(f \Rightarrow g)(x) = \{a' | \forall a \in f(x) a' a \downarrow \wedge a' a \in g(x)\}$$ 

where $a' a \downarrow$ is standard shorthand for "$a' a$ is defined". Then for any $f$ and $g$, the combinator $\lambda b. l(b)r(b)$ realizes $(f \Rightarrow g) \wedge f \leq g$, and the combinator $\lambda b. \lambda a. p a b$ realizes $g \leq f \Rightarrow (f \wedge g)$. 
=-- 

For any function $f \colon X \to Y$, it is immediate that 

$$P(A)^f \colon P(A)^Y \to P(A)^X$$ 

is a functor preorder map that preserves Heyting prealgebra structure.

Furthermore, in the case of a projection map $f \colon Z \times Y \to Y$, there will be left and right adjoints to $P(A)^f \colon P(A)^Y \to P(A)^{Z \times Y} (\cong (P(A)^Z)^Y)$, as induced by the union and intersection maps from $P(A)^Z$ to $P(A)$.

## Related concepts

* [[combinatory logic]]
* [[realizability]]
* [[Turing category]]
* [[assembly]]

[[!include computable mathematics -- table]]

## References 

* {#Hofstra} Pieter J.W. Hofstra, _Partial Combinatory Algebras and Realizability Toposes_, 
([web](https://web.archive.org/web/20210517194958fw_/https://mysite.science.uottawa.ca/phofstra/preprints.html)) [[Kananaskis.pdf:file]] 

Lecture notes include

* {#Bauer05} [[Andrej Bauer]], section 2 of _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))




[[!redirects combinatory algebra]]

[[!redirects partial combinatory algebra]]
[[!redirects partial combinatory algebras]]


[[!redirects Kleene's first algebra]]
[[!redirects Kleene's first partial combinatory algebra]]


[[!redirects realizability tripos]]

[[!redirects PCA]]
[[!redirects PCAs]]
