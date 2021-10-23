

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--

=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A notion of _$n$-module_ ($n$-vector space) is a [[categorification]] of the notion of [[module]] ([[vector space]]).

There are various different notions of $n$-vector spaces. 

One notion is: an $n$-vector space is a [[chain complex]] of [[vector space]]s in degrees 0 to $n$. For $n=2$ this is a [[Baez-Crans 2-vector space]]. This is useful for lots of things, but tends to be too restrictive in other contexts.

Another is, recursively: an $(n-1)$-algebra object (or its $(n-1)$-category of modules) in the $n$-category of $(n-1)$-bimodules. For higher $n$ this is envisioned in ([FHLT, section 7](#FHLT)), details are in spring. It includes the previous concept as a special case.

For $n=2$ this subsumes various other definitions of [[2-vector space]] that are in the literature, such as notably the notion of [[Kapranov-Voevodsky 2-vector space]].

We sketch the iterative definition of $n$-vector spaces. More details are below.

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

With this definition we have that $2 Vect$ is the [[2-category]] of $k$-[[algebra]]s, [[bimodule]]s and bimodule homomorphisms.

More generally, let $k$ here be a [[ring spectrum]]. Set


* $(\infty,0)Vect_k := k$ -- a [[symmetric monoidal (infinity,1)-category|symmetric monoidal]] [[∞-groupoid]];

* $(\infty,1)Vect_k := k Mod$ the [[symmetric monoidal (∞,1)-category]] of modules over that ring spectrum;

* $(\infty,n)Vect_k := (\infty,n-1) Mod$ the [[symmetric monoidal (∞,n)-category]] of modules over $(\infty,n-1)Mod$.


## Definition
 {#Definition}

Following the [above idea](IteratedModules) we have the following definition.

+-- {: .num_defn #nVectViaALgObjects}
###### Definition

Fix a [[ring]] $k$ (usually taken to be a [[field]] if one speaks of "vector spaces" instead of just [[module]]s, but this is not actually essential for the construction). This may be an [[ring spectrum|∞-ring]].

For $n \in \mathbb{N}$, define an [[symmetric monoidal (∞,n)-category]] $n Vect_k$ of **$(\infty,n)$-vector spaces** as follows (the bi-counting follows the pattern of [[(n,r)-categories]]).

An **$(\infty,0)$-vector space** is an element of $k$. If $k$ is an ordinary ring, then the [[0-category]] $0 Vect$ is the underlying set of $k$, regarded as a [[symmetric monoidal category]] using the product structure on $k$. If $k$ is more generally an [[ring spectrum|∞-ring]], then the "stabilized [[(∞,0)-category]]" (= [[spectrum]]) of $(\infty,0)$-vector spaces is $k$ itself: $(\infty,0)Vect_k \simeq k$.

An **[[(∞,1)-vector space]]** is an [[module spectrum|∞-module]] over $k$. The [[(∞,1)-category]] of $(\infty,1)$-vector spaces is 

$$
  (\infty,1)Vect_k := k Mod
  \,,
$$

the $(\infty,1)$-category of $k$-[[module spectra]].

For $k$ a field ordinary [[vector space]]s over $k$ are a [[full sub-(∞,1)-category]] of this: $1Vect_k \hookrightarrow (\infty,1)Vect_k$ . 

For $n \geq 2$, an **$(\infty,n)$-vector space** is an [[algebra in an (infinity,1)-category|algebra object in the symmetric monoidal (∞,1)-category]] $(\infty,n-1)Vect$. A [[morphism]] is a [[bimodule object]]. [[k-morphism|Higher morphisms]] are defined recursively.

=--

For $\infty$ replaced by $n$ this appears as ([Schreiber, appendix A](#Schreiber)) and then with allusion to more sophisticated [[higher category theory|higher categorical]] tools in ([FHLT, def. 7.1](#FHLT)). 

Notice that FHLT say "$(n-1)$-algebra" instead of "$n$-vector space", but only for the reason (p. 29) that

> The discrepancy between $m$ (the algebra level) and $n$ [the algebra level] -- for which we apologize -- is caused by the fact that the term "$n$-vector space" has been used for a much more restrictive notion than our $(n-1)$-algebras.

## Examples

### $(\infty,1)$-vector spaces

See [[(∞,1)-vector space]] for more.

### 2-Modules

+-- {: .num_remark}
###### Remark

The symmetric monoidal 3-category $Alg_k^b = 2 Mod_k$ of [[2-modules]] over $k$ is:

* [[objects]] are [[associative algebras]] over $k$;

* [[morphisms]] are [[bimodules]] of associative algebras; [[composition]] is the [[tensor product]] of bimodules;

* [[2-morphisms]] are bimodule homomorphisms.

We think of this equivalently as its essential image in $Vect_k Mod$, where

* an algebra $A$ is a placeholder for its [[module category]] $Mod_A$;

* an $A$-$B$ [[bimodule]] $N$ is a placeholder for the [[functor]]

  $$
    Mod_A \stackrel{(-) \otimes_A N }{\to} Mod_B
  $$

* a bimodule homomorphism is a placeholder for a [[natural transformation]] of two such functors.

If we think of an algebra $A$ in terms of its [[delooping]] [[Vect]]-[[enriched category]] $B A$, then we have an [[equivalence of categories]]

$$
  Mod_A \simeq Vect Cat(B A, Vect)
  \,.
$$

Comparing this for the formula

$$
  V \simeq Set(S,k)
$$

for a $k$-vector space $V$ with [[basis]] $S$, we see that we may 

* think of the algebra objects appearing in the above as being _bases_ for a higher vector space;

* think of the bimodules as being higher [[matrix|matrices]].

=--



### 3-Modules

A _3-vector space_ according to def. \ref{nVectViaALgObjects} is

* a $k$-algebra $A$;

* equipped with an $A$-$A\otimes A$-[[bimodule]] defining the 2-multiplication, and a left $A$-[[module]] defining the unit.

Equivalently this is a [[sesquiunital sesquialgebra]].

Classes of examples come from the following construction:

* Every _commutative_ [[associative algebra]] $A$ becomes a 3-vector space.

* Every [[Hopf algebra]] canonically becomes a 3-vector space (amplified in [FHLT, p. 27](#FHLT)).

  More generally: every [[hopfish algebra]].

### 4-Modules

Next, an algebra object internal to $2 Alg_k^b = 3Mod_3$, is an algebra equipped with three compatible algebra structures, a [[trialgebra]].

Its [[category of modules]] is a [[monoidal category]] equipped with two compatible product structures a [[Hopf category]].

The 2-category of 2-modules of that is a [[monoidal 2-category]].

For a review see ([Baez-Lauda 09, p. 98](BaezLauda)).


## $n$-Representations

See [[infinity-representation]].

## Related concepts


* [[vector space]], 

* [[(∞,1)-module]], [[(∞,1)-module bundle]], [[(∞,1)-category of (∞,1)-modules]]

* [[2-ring]], [[2-module]]

* [[2-vector space]]

  * _[[TwoVect]]_ is a Mathematica software package for computer algebra with 2-vector spaces

* **$n$-vector space**, [[n-vector bundle]], 

[[!include structure on algebras and their module categories - table]]

## References

The notion of $n$-vector spaces is (defined for $n = 2$ and sketched recursively for greater $n$) in 

appendix A of

* {#Schreiber} [[Urs Schreiber]], _AQFT from $n$-functorial QFT_  Communications in Mathematical Physics, Volume 291, Issue 2, pp.357-401 (2008) ([pdf](http://ncatlab.org/schreiber/files/AQFTfromFQFT.pdf))
 
section 7 of 

* {#FHLT} [[Dan Freed]], [[Mike Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2009)

Full details are in 

* {#Haugseng14} [[Rune Haugseng]], _The higher Morita category of $E_n$-algebras_ ([arXiv:1412.8459](http://arxiv.org/abs/1412.8459))

Review of work on 4-modules (implicitly) as [[trialgebras]]/[[Hopf monoidal categories]] is around p. 98 of 

* {#BaezLauda} [[John Baez]], [[Aaron Lauda]], _A prehistory of $n$-categorical physics_, in _Deep beauty_, 13-128, Cambridge Univ. Press, Cambridge, 2011 ([arXiv:0908.2469](http://arxiv.org/abs/0908.2469))


 

[[!redirects n-vector spaces]]
[[!redirects n-vector spaces]]

[[!redirects nMod]]

[[!redirects (∞,n)-vector space]]
[[!redirects (infinity,n)-vector space]]
[[!redirects (∞,n)-vector spaces]]
[[!redirects (infinity,n)-vector spaces]]

[[!redirects (infinity,n)-modules]]
[[!redirects (∞,n)-module]]
[[!redirects (∞,n)-modules]]

[[!redirects (infinity,2)-module]]
[[!redirects (infinity,2)-modules]]
[[!redirects (∞,2)-module]]
[[!redirects (∞,2)-modules]]

[[!redirects (∞, n)-vector space]]
[[!redirects (infinity, n)-vector space]]
[[!redirects (∞, n)-vector spaces]]
[[!redirects (infinity, n)-vector spaces]]

[[!redirects (infinity, n)-modules]]
[[!redirects (∞, n)-module]]
[[!redirects (∞, n)-modules]]

[[!redirects (infinity, 2)-module]]
[[!redirects (infinity, 2)-modules]]
[[!redirects (∞, 2)-module]]
[[!redirects (∞, 2)-modules]]


[[!redirects 3-vector space]]
[[!redirects 3-vector spaces]]

[[!redirects 3-module]]
[[!redirects 3-modules]]

[[!redirects 4-module]]
[[!redirects 4-modules]]
[[!redirects 4-vector space]]
[[!redirects 4-vector spaces]]

[[!redirects 2-algebra]]
[[!redirects 2-algebras]]

[[!redirects 3-algebra]]
[[!redirects 3-algebras]]

[[!redirects n-algebra]]
[[!redirects n-algebras]]


[[!redirects n-module]]
[[!redirects n-modules]]


[[!redirects (infinity,n)-vector space]]
[[!redirects (infinity, n)-vector space]]
[[!redirects n-vector space]]