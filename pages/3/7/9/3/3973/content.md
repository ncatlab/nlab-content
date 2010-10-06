

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--

* [[vector space]]

* [[2-vector space]]

* **$n$-vctor space**

***

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A notion of _$n$-vector space_ is a [[categorification]] of the notion of [[vector space]].

There are various different notions of $n$-vector spaces. 

One notion is: an $n$-vector space is a [[chain complex]] of [[vector space]]s in degrees 0 to $n$. For $n=2$ this is a [[Baez-Crans 2-vector space]]. This is useful for lots of things, but tends to be too restrictive in other contexts.

Another is, recursively: an $(n-1)$-algebra object (or its $(n-1)$-category of modules) in the $n$-category of $(n-1)$-bimodules. For higher $n$ this is mentioned towards the end of [[Topological Quantum Field Theories from Compact Lie Groups]].

For $n=2$ this subsumes various definitions of [[2-vector space]] that are in the literature, such as notably the notion of [[Kapranov-Voevodsky 2-vector space]].

## Definition

### Iterated module definition {#IteratedModules}

Assume that a notion of [[n-category]] is chosen for each $n$ (for instance [[(n,1)-category]]), that a notion of [[symmetric monoidal category|symmetric monoidal]] $n$-category is fixed (for instance [[symmetric monoidal (∞,1)-category]]) and that a notion of (weak) commutative [[monoid]] objects and [[module]] and [[bimodule]] object in a symmetric monoidal $n$-category is fixed (for instance the notion of [[algebra in an (∞,1)-category]]).

Then we have the following recursive (rough) definition:

fix a ground [[field]] $k$.

* a 0-vector space over $k$ is an elemment of $k$. The [[0-category]] of 0-vector spaces is the set

  $$
    0 Vect_k = k
    \,.
  $$

* The category $1 Vect_k$ is just [[Vect]].

* For $n \gt 1$, the [[n-category]] $n Vect$ of **$n$-vector spaces** over $k$ is the $n$-category with objects algebra objects in $(n-1)Vect$ and morphisms bimodule objects in $(n-1)Vect$.

Here we think of an algebra object $A \in (n-1)Vect$ as a basis for the $n$-vector space which is the $(n-1)$-category $A Mod$.

With this defintion we have that $2 Vect$ is the [[2-category]] of $k$-[[algebra]]s, [[bimodule]]s and bimodule homomorphisms.

More generally, let $k$ here be a [[ring spectrum]]. Set


* $(\infty,0)Vect_k := k$ -- a [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]];

* $(\infty,1)Vect_k := k Mod$ the [[(∞,1)-category]] of modules over that ring spectrum;

* $(\infty,1)Vect_k := k Mod$ the [[symmetric monoidal (∞,1)-category]] of modules over that ring spectrum;

* $(\infty,n)Vect_k := (\infty,n-1) Mod$ the [[symmetric monoidal (∞,n)-category]] of modules over $(\infty,n-1)Mod$.

## $n$-Representations

...