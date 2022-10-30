

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A notion of _$n$-vector space_ is a [[categorification]] of the notion of [[vector space]].

There are various different notions of $n$-vector spaces. 

One notion is: an $n$-vector space is a [[chain complex]] of [[vector space]]s in degrees 0 to $n$. For $n=2$ this is a [[Baez-Crans 2-vector space]]. This is useful for lots of things, but tends to be too restrictive in other contexts.

Another is, recursively: an $(n-1)$-algebra object (or its $(n-1)$-category of modules) in the $n$-category of $(n-1)$-bimodules. For higher $n$ this is in ([FHLT, section 7](FHLT)). It includes the previous concept as a special case.

For $n=2$ this subsumes various other definitions of [[2-vector space]] that are in the literature, such as notably the notion of [[Kapranov-Voevodsky 2-vector space]].


### Iterated module construction
 {#IteratedModules}

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


## Definition
 {#Definition}

Following the [above idea](IteratedModules) we have the following definition.

+-- {: .num_defn #nVectViaALgObjects}
###### Definition

Fix a [[field]] $k$. For $n \in \mathbb{N}$, define an [[symmetric monoidal (∞,n)-category]] $n Vect_k$ of **$n$-vector spaces** as follows.

A 0-vector space is an element of $k$. The [[0-category]] $0 Vect$ is the underlying set of $k$, regarded as a [[symmetric monoidal category]] using the product structure on $k$.

A 1-vector space is an ordinary [[vector space]] over $k$. A morphism is a [[linear function]]. Set $1 Vect := $ [[Vect]], the ordinary category of [[vector space]]s over $k$.

For $n \geq 2$, an $n$-vector space is an [[algebra in an (infinity,1)-category|algebra object in the symmetric monoidal (∞,1)-category]] $(n-1)Vect$. A [[morphism]] is a [[bimodule object]]. [[k-morphism|Higher morphisms]] are defined recursively.

=--

This appears as ([Schreiber, appendix A](#Schreiber)) and then with allusion to more sophisticated [[higher category theory|higher categorical]] tools in ([FHLT, def. 7.1](#FHLT)). 

Notice that FHLT say "$(n-1)$-algebra" instead of "$n$-vector space", but only for the reason (p. 29) that

> The discrepancy between $m$ (the algebra level) and $n$ [the algebra level] -- for which we apologize -- is caused by the fact that the term "$n$-vector space" has been used for a much more restrictive notion than our $(n-1)$-algebras.

## Examples

### 2-Vector spaces

+-- {: .num_remark}
###### Remark

The symmetric monoidal 3-category $2 Vect_k$ is that of 

* [[object]]s are [[associative algebra]]s over $k$;

* [[morphism]]s are [[bimodule]]s of associative algebras; [[composition]] is the [[tensor product]] of bimodules;

* [[2-morphism]]s are bimodule homomorphisms.

We think of this equivalently as its essential image in $Vect_k Mod$, where

* an algebra $A$ is a placeholder for its [[module category]] $Mod_A$;

* an $A$-$B$ [[bimodule]] $N$ is a placeholder for the [[functor]]

  $$
    Mod_A \stackrel{(-) \otimes_A N }{\to} N_B
  $$

* a bimodule homomorphism is a placeholder for a [[natural transformation]] of two such functors.

If we think of an algebra $A$ in terms of its [[delooping]] [[Vect]]-[[enriched category]] $B A$, then we have an [[equivalence of categories]]

$$
  Mod_A \simeq Vect Cat(B A, Vect)
  \,.
$$

Compring this for the formula

$$
  V \simeq Set(S,k)
$$

for a $k$-vector space $V$ with [[basis]] $S$, we see that we may 

* think of the algebra objects appearing in the above as being _bases_ for a higher vector space;

* think of the bimodules as being higher [[matrix|matrices]].

=--



### 3-Vector spaces

A _3-vector space_ according to def. \ref{nVectViaALgObjects} is

* a $k$-algebra $A$;

* equipped with an $A$-$A\otimes A$-[[bimodule]] defining the 2-multiplication, and a left $A$-[[module]] defining the unit.

Classes of examples come from the following construction:

* Every _commutative_ [[associative algebra]] $A$ becomes a 3-vector space.

* Every [[Hopf algebra]] canonically becomes a 3-vector space.

See ([FHLT, p. 27](#FHLT)).

## $n$-Representations

See [[infinity-representation]].

## Related concepts

* [[vector space]]

* [[2-vector space]]

* **$n$-vector space**, [[n-vector bundle]]

## References

The notion of $n$-vector spaces is (defined for $n = 2$ and sketched recursively for greater $n$) in 

appendix A of

* [[Urs Schreiber]], _AQFT from $n$-functorial QFT_  Communications in Mathematical Physics, Volume 291, Issue 2, pp.357-401 (2008) ([pdf](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf))
 {#Schreiber}

section 7 of 

* [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2009)
 {#FHLT}

[[!redirects n-vector spaces]]