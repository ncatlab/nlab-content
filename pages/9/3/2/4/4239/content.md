
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
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

The notion of _Calabi-Yau category_ is a [[horizontal categorification]] of that of [[Frobenius algebra]] -- a _Frobenius [[algebroid]]_ . Their name derives from the fact that the definition of Calabi-Yau categories have been originally studied as an abstract version of the [[derived category]] of [[coherent sheaves]] on a [[Calabi-Yau manifold]].

## Definition

### 1-categorical

A **Calabi-Yau category** is a [[Vect]]-[[enriched category]] $C$ equipped for each object $c \in C$ with a [[trace]]-like map

$$
  Tr_C : C(c,c) \to k
$$

to the ground field, such that for all objects $d \in C$ the induced pairing

$$
  \langle -,-\rangle_{c,d} :
  C(c,d) \otimes C(d,c) \to k  
$$

given by 

$$
  \langle f,g \rangle = Tr(g \circ f)
$$

is symmetric and non-degenerate.

A Calabi-Yau category with a single object is the same (or rather: is equivalently the [[pointed object|pointed]] [[monoid]]  [[delooping]]) of a [[Frobenius algebra]].


### $(\infty,1)$-categorical

A **Calabi-Yau $A_\infty$-category** of _dimension_ $d \in \mathbb{N}$ is an [[A-∞ category]] $C$ equipped with, for each pair $a,b$ of [[object]]s, a morphism of [[chain complex]]es

$$
  \langle -,-\rangle_{a,b}
  : 
  C(a,b) \otimes C(b,a)
  \to
  k[d]
$$

such that

1. this is non-degenerate and is symmetric in that

   $$
    \langle - , - \rangle_{a,b} =  \langle - , - \rangle_{b,a} \circ \sigma_{a,b}
   $$ 

   for $\sigma_{a,b} : C(a,b)\otimes C(b,a) \to C(b,a) \otimes C(a,b)$
   the symmetry [[isomorphism]] of the [[symmetric monoidal category]]
   of [[chain complex]]es;

1. this is cyclically invariant in that for all elements $(\alpha_i)$
   is the respective hom-complexes we have

   $$
     \langle
       m_{n-1}(\alpha_0 \otimes \cdots \otimes \alpha_{n-2}),
       \alpha_{n-1} 
     \rangle
     =
     (-1)^{(n+1)+ |\alpha_0| \sum_{i = 1}^{n-1}|\alpha_i|}
     \langle
       m_{n-1}(\alpha_1 \otimes \cdots \otimes \alpha_{n-2}),
       \alpha_0
     \rangle
     \,.
   $$




## Examples

### From Calabi-Yau varieties
 {#FromCYVarieties}


* Let $X$ be a smooth projective [[Calabi-Yau variety]] of dimension $d$.
  Write $D^b(X)$ for the bounded [[derived category]] of 
  that of [[coherent sheaves]] on $X$. 

  Then $D^b(X)$ is a CY $A_\infty$-category in a naive way:

  * the non-binary composition maps are all trivial;

  * the pairing is given by [[Serre duality]] (one needs also a choice of trivialization of the canonical bundle of $X$)

This is however not the morally correct CY $A_\infty$-structure associated with a Calabi-Yau. A correct choice is, for example, the [[Dolbeault cohomology|Dolbeault]] [[enhanced triangulated category|dg-enhancement]] of the derived category

([Costello 04, 7.2](#Costello04), [Costello 05, 2.2](#Costello05))

### From symplectic manifolds

The [[Fukaya category]] associated with a [[symplectic manifold]] $X$. But see [this MO discussion](http://mathoverflow.net/questions/13114/are-fukaya-categories-calabi-yau-categories) for more.

### From string topology

[[string topology]]: for $X$ a [[compact space|compact]] [[simply connected]] [[orientation|oriented]] [[manifold]], its cohomology $H^{\bullet}(X)$ is naturally a Calabi-Yau $A_\infty$-category with a single object. The $A_\infty$ structure comes from the [[homological perturbation lemma]]. One could also use the dg algebra of cochains $C^\bullet(X)$.

## Properties

### Classification of 2d TQFT

Calabi-Yau $A_\infty$-categories classify [[TCFT]]s. This remarkable result is what actually one should expect. Indeed, TCFTs originally arose as an abstract version of the [[CFT]]s constructed from [[sigma-model]]s whose targets are [[Calabi-Yau spaces]].

[[!include 2d TQFT -- table]]


## Related concepts

* [[Calabi-Yau object]]

## References

* {#Costello04} [[Kevin Costello]], _Topological conformal field theories and Calabi-Yau categories_ ([arXiv:math/0412149](http://arxiv.org/abs/math/0412149))

* {#Costello05} [[Kevin Costello]], _The Gromov-Witten potential associated to a TCFT_ ([arXiv:0509264](http://arxiv.org/abs/math/0509264))

* [[Maxim Kontsevich]], [[Yan Soibelman]]. _Notes on A-infinity algebras, A-infinity categories and non-commutative geometry_ &lt;http://arxiv.org/abs/math/0606241>

* Lee Cho, _Notes on Kontsevich-Soibelman's theorem about cyclic A-infinity algebras_ ([arXiv:1002.3653](http://arxiv.org/abs/1002.3653))

* {#Lurie09} [[Jacob Lurie]], section 4.2 of _[[On the Classification of Topological Field Theories]]_ ([arXiv:0905.0465](http://arxiv.org/abs/0905.0465))


[[!redirects Calabi-Yau category]]
[[!redirects Calabi-Yau categories]]
[[!redirects Calabi?Yau category]]
[[!redirects Calabi?Yau categories]]
[[!redirects Calabi--Yau category]]
[[!redirects Calabi--Yau categories]]

[[!redirects CY category]]
[[!redirects CY categories]]
[[!redirects CY-category]]
[[!redirects CY-categories]]

[[!redirects Calabi-Yau A-infinity category]]
[[!redirects Calabi-Yau A-infinity categories]]
[[!redirects Calabi-Yau A-infinity-category]]
[[!redirects Calabi-Yau A-infinity-categories]]
[[!redirects Calabi-Yau A-∞ category]]
[[!redirects Calabi-Yau A-∞ categories]]
[[!redirects Calabi-Yau A-∞-category]]
[[!redirects Calabi-Yau A-∞-categories]]