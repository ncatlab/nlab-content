
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea 

A 'Fermat theory' is a [[Lawvere theory]] that extends the usual theory of [[commutative rings]] by permitting [[differentiation]].  

The term _Fermat theory_ has been introduced in ([Dubuc-Kock 84](#DubucKock84)) but as the name suggests, it has its roots in an old observation of [[Fermat]].  Namely: if $f \;\colon\; \mathbb{R} \longrightarrow \mathbb{R}$ is a [[polynomial]] function, then

$$f (x+y) = f(x) + y \tilde{f}(x,y) $$

for a unique polynomial function $\tilde{f} \colon \mathbb{R}^2 \to \mathbb{R}$.  Clearly

$$ \tilde{f}(x,y) = \frac{f(x+y) - f(x)}{y} $$

for $y \ne 0$, but the interesting thing is that

$$\tilde{f}(x,0) = f'(x)$$

So, the function $\tilde{f}$ knows about the [[derivative]] of $f$!  (This can be done for polynomials over any [[commutative ring]], although Fermat wasn\'t working in that generality.)

Later [[Jacques Hadamard]] generalized this observation from a polynomial function $f$ to a [[continuously differentiable function]] $f$, where now $\tilde{f}$ is unique if required to be [[continuous map|continuous]].  This is the statement of the _[[Hadamard lemma]]_. (For a merely [[differentiable function]] $f$, require $\tilde{f}$ to be continuous in $y$ alone.)  The function $\tilde{f}$ is thus called a [[Hadamard quotient]].  If $\tilde{f}$ is to be the same class of function as $f$, then we need [[smooth functions]], and that will be our motivating context from now on.

If we take $\tilde{f}(x,0) = f'(x)$ as a _definition_ of the derivative, we can derive many of the basic rules for derivatives from the formula

$$f(x+y) = f(x) + y \tilde{f}(x,y) $$

using just algebra --- no [[limit of a sequence|limits]]!  As an exercise, the reader should check these rules:

$$(f + g)' = f' + g'$$

$$(f g)' = f' g + f g' $$

$$(f \circ g)' = (f' \circ g) g' $$

These ideas continue to work if $f$ is a smooth function from $\mathbb{R}^n$ to $\mathbb{R}$; focussing on one variable and treating the others as [[parameter]]s, we have [[partial derivative|partial differentiation]].


## Definition

The above observations suggest defining the following kind of [[Lawvere theory]].  A **Fermat theory** is an extension of the [[algebraic theory]] of [[commutative rings]], such that for any $(n+1)$-ary operation $f$ there is a unique $(n+2)$-ary operation $\tilde{f}$ such that

$$ f(x + y, \vec{z}) =
f(x, \vec{z}) + y \tilde{f}(x,y,\vec{z})$$

where $\vec{z}$ is a list of $n$ variables which act as parameters.  (Here we are abusing language by writing the operations $f$ and $\tilde{f}$ as if they were functions, to avoid unintuitive commutative diagrams.)


## Examples 

### $C^\infty$-rings

There is a [[Lawvere theory]] called **the theory of $C^\infty$-rings**, whose $n$-ary operations are the [[smooth maps]] $f: \mathbb{R}^n \to \mathbb{R}$, 

$$
  T(n) \coloneqq C^\infty(\mathbb{R}^n, \mathbb{R})
  \,,
$$

with composition of operations defined in the obvious way.  An algebra of this Lawvere theory is called a **[[generalized smooth algebra|C^∞-ring]]**. 


The theory of $C^\infty$-rings is a Fermat theory.  For any [[smooth manifold]] $M$, the algebra of smooth real-valued functions $C^\infty(M)$ is a $C^\infty$ ring.  More generally, if $M$ is any [[diffeological space]], [[Chen space]] or [[Frolicher space]], we can define $C^\infty(M)$, and this will be a $C^\infty$-ring. 

In formulas, and even more generally: for any generalized [[space]] given by a [[presheaf]] $X$ on [[CartSp]], the corresponding $C^\infty$-ring is the copresheaf

$$
  C^\infty(X) : \mathbb{R}^n \mapsto [CartSp^{op},Set](X,Y(\mathbb{R}^n))
$$

that sends each object $\mathbb{R}^n \in CartSp$ to the [[hom-set]] in the [[functor category]] $[CartSp^{op},Set]$ from $X$ to the presheaf [[representable functor|represented]] by $\mathbb{R}^n$ under the [[Yoneda embedding]]. By the canonical right [[exact functor|exactness]] of the [[hom-functor]], this preserves [[limit]]s and hence in particular [[product]]s in [[CartSp]].


## Partial derivatives {#PartialDerivative}

Let $T$ be a Fermat theory and let $f$ be an $(n+1)$-ary operation, then we may define an operation $\partial_1 f$

by

$$\partial_1(x, \vec{z})  = \tilde{f}(x,0,\vec{z})$$

This acts like the [[partial derivative]] of $f$ with respect to its first argument. With a bit of more work we get a list of $n$-ary operations $\partial_i f$.   So, if $T(n)$ denotes the set of $n$-ary operations in the algebraic theory $T$, we get maps

$$\partial_i : T(n) \to T(n) $$

for $1 \le i \le n$.  

Now $T(n)$ is automatically an algebra of $T$ (this is true for any Lawvere theory: it is the free algebra on $n$ generators), whence $T(n)$ is a commutative ring.  One can check that each map

$$\partial_i : T(n) \to T(n) $$

is a [[derivation]] of this ring --- this is really just the [[chain rule]].


## Modules and derivations {#ModulesDerivations}

Let $T$ be a Fermat theory, and let $A$ be a $T$-algebra. A [[module]] $N$ over $A$ is simply a module for the underlying [[ring]] of $A$. 

But the notion of [[derivation]] $\delta : A \to N$ of such modules depends on the $T$-structure:

To motivate the concept, let first $A$ be an ordinary [[ring]] and $N$ an ordinary [[module]]. Then the three axioms of an ordinary derivation $\delta : A \to N$

1. $\delta(a + b  ) = \delta(a) + \delta(b)$

2. $\delta(\lambda a) = \lambda \delta(a)$

3. $\delta(a \cdot b) = a \delta(a) + b \delta(b)$

are equivalent to the condition that for any polynomial $p \in \mathbb{R}[x_1, \cdots, x_n]$ and ring elements $a_i$ we have

$$
  \delta\left(
    p(a_1, \cdots, a_n)
  \right)
  =
  \sum_{i= 1 }^{n}
  \frac{\partial p}{\partial x_i}
  \left(
    a_1, \cdots, a_n
  \right)
  \delta(a_i)
  \,.
$$

(It is immediate that the first three axioms imply this one. To see the converse, apply the latter to  the polynomials $p_1(x,y) = x + y$, $p_2(x) = \lambda a$ and $p_3(x,y) = x y$.)


The definition of derivations for general $T$-algebras now follows the last expression, using the notion of [partial derivatives](#PartialDerivative) from above:

+-- {: .num_defn}
###### Definition

For $T$ a Fermat theory, $A$ a $T$-algebra and $N$ an $A$-module, a **derivation**  $\delta : A \to N$ is a map such that for each $f \in T(n)$ and elements $(a_i \in A)$ we have

$$
  \delta\left(
    f(a_1, \cdots, a_n)
  \right)
  =
  \sum_{i= 1 }^{n}
  \frac{\partial f}{\partial x_i}
  \left(
    a_1, \cdots, a_n
  \right)
  \delta(a_i)
  \,.
$$

=--


Notice that in particular such a derivation of a $T$-algebra $A$ is a derivation of the underlying ring. (This follows again by using the above three polynomials and remembering that by definition $T(n)$ at least contains all polynomials.)


### K&#228;hler differentials {#K&#228;hlerDiffs}

The sets $T(n)$ for $n \in \mathbb{N}$ canonically have the structures of [[module]]s over $T(n)$. 



+-- {: .num_theorem}
###### Theorem


The map

$$
  d := 
\langle \partial_1, \dots, \partial_n \rangle : T(n) \to \prod_{i = 1}^{n}  T(n) $$

obtained from the partial derivatives is the universal 
$T$-derivation of $T(n,1)$.

=--


This means that if $N$ is a module of $T(n)$ and $\delta : T(n) \to N$ is a derivation in the above sense, then $\delta$ factors uniquely through the map $\langle \partial_1, \dots, \partial_n \rangle$.   
 
The point of this theorem is that it gives us a version of [[Kähler differentials]] for $T(n)$. 

We may think of an element  $(f_i) \in \prod_{i = 1}^{n}  T(n)$ as the [[Kähler differential]] 1-form $f_1 d x^1 + f_2 d x^2 + \cdots + f_n d x^n$ and of the derivation $d := \langle \partial_1, \dots, \partial_n \rangle$ as the operation

$$
  d  : f \mapsto \sum_i \frac{\partial f_i}{ \partial x^i} d x^i
  \,.
$$

Indeed, when the Fermat theory is that of [[generalized smooth algebra|C-infinity rings]], then this notion of K&#228;hler differentials does coincide with the ordinary notion of smooth [[differential form|1-form]]. The same is not true, in general, if one instead forms ring-theoretic K&#228;hler differentials. 

## Related concepts

* [[model structure on differential graded-commutative superalgebras]]


## References

The original reference is

* {#DubucKock84} [[Eduardo Dubuc]], [[Anders Kock]], _On 1-form classifiers_, Comm. Alg. __12__  (1984),  no. 11-12, 1471--1531 ([pdf](http://home.imf.au.dk/kock/DK84.pdf))
 

Parts of the above material are a summary of the following talk:

* {#Kock09} [[Anders Kock]], _K&#228;hler differentials for Fermat theories_, talk at  _Fields Workshop on Smooth Structures in Logic, Category Theory and Physics_, May 1, 2009, University of Ottawa.  ([abstract](http://aix1.uottawa.ca/~scpsg/Fields09/smooth.abstracts.html))
  

For more, see:

* [[Alex Hoffnung]], _Smooth Structure in Ottawa II_  ([blog entry](http://golem.ph.utexas.edu/category/2009/05/smooth_structures_in_ottawa_ii.html#c030745))

and the comments on this blog entry.

Refinement to [[supergeometry]] and extension to a notion of _super Fermat theory_ is discussed in

* [[David Carchedi]], [[Dmitry Roytenberg]], _On theories of superalgebras of differentiable functions_, ([arxiv:1211.6134](http://arxiv.org/abs/1211.6134))

Something similar appears in def. 1.1, 1.2 of 

* [[David Yetter]], _Models for synthetic supergeometry_, Cahiers, 29, 2 (1988) ([NUMDAM](http://www.numdam.org/item?id=CTGDC_1988__29_2_87_0))

For more on this see at _[[synthetic differential supergeometry]]_.


Discussion of relationship to [[Cartesian differential categories]] is here:

* [[Jean-Simon Lemay]], _Cartesian Fermat Categories, a new class of Cartesian Differential Categories_, Topos Institute Seminar, June 2025 (work with Carlos Pascual Miralles). [Slides](https://topos.institute/events/topos-colloquium/slides/2025-06-12.pdf), [Video](https://www.youtube.com/watch?v=G_EmgaM9i64).



[[!redirects Fermat theory]]
[[!redirects Fermat theories]]
[[!redirects fermat theory]]
