
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Limits and colimits
+-- {: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Given a [[set]] $S$ and a collection $\{K_s \stackrel{\iota_s}{\hookrightarrow} X_s\}_{s \in S}$ of [[morphisms]] in some [[category]] (typically [[monomorphisms]]), then the _restricted product_ $\underset{s\in S}{\prod}^\prime X_s$ is vaguely the like the actual [[product]] $\underset{s\in S}{\prod} X_s$ of all the $X_s$, but subject to the restriction that for each [[element]] $(x_s)_{s \in S}$ all but a [[finite number]] of components $x_s$ are in the [[image]] of $\iota_s$.

## Definition

Assume that the ambient [[category]] $\mathcal{C}$ has ordinary [[products]]. Write $\mathcal{P}_{fin} S$ for the [[poset]] of [[finite set|finite]] [[subsets]] of $S$ and consider the [[functor]]
 
$$
  X^K \colon \mathcal{P}_{fin}\longrightarrow \mathcal{C}
$$

which is given on a [[finite set|finite]] [[subset]] $U \subset S$ by the [[products]]

$$ 
  U \mapsto X^K_U \coloneqq \left(\underset{u \in U}{\prod} X_u\right) 
   \times 
  \left(
     \underset{s \in S-U}{\prod} K_s
  \right)
$$

and which sends an inclusion $U_1 \hookrightarrow U_2$ of subsets to the evident [[morphism]] between these products whose components $f_s$ are the [[identity]] for $s \in S-(U_2-U_1)$ and are $\iota_s$ for $s \in U_2-U_1$.

Then the restricted product is the ([[filtered colimit|filtered]]) [[colimit]] over this functor

$$
  \underset{s\in S}{\prod}^\prime X_s
  \coloneqq
  \underset{\underset{U \in \mathcal{P}_{fin}S}{\longrightarrow}}{\lim}
  X^K_U
  \,.
$$


## Examples

* A [[weak direct product]] is a restricted product whose trivial subobjects are specified [[global elements]], hence where each $K_s = \ast$ are [[terminal objects]].

* The [[ring of adeles]] of a [[global field]] $k$ is the restricted product of the [[formal completions]] $k_v$ at all its [[places]] $v$, with the restriction being that only finitely many components have [[norm]] greater than unity.

  Equivalently this is the restricted product for the inclusions $\iota_v \colon \mathcal{O}_v \hookrightarrow k_v$ of the [[ring of integers]] of $k_v$ into $k_v$.

* Under the [[function field analogy]] the above example is a special case of the following more general example: for $\Sigma$ an [[arithmetic curve]] then the restricted product of all the algebras of functions on all its punctured [[formal disks]], with the restrictions being along the inclusions of the functions on the un-punctured formal disks, appears in the description of [[Cech cohomology|Cech cocycles]] with respect to [[covers]] of the curve by the complement of any finite points and the formal disks around these points (e.g [Frenkel 05, section 3.2](#Frenkel05)). This is discussed in detail at _[moduli stack of bundles -- over curves](moduli+space+of+bundles#OverCurvesAndTheLanglandsCorrespondence)_. 




## References

* Wikipedia _[Restricted product](http://en.wikipedia.org/wiki/Restricted_product)_

* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_, in _Frontiers in number theory, physics, and geometry II_, Springer Berlin Heidelberg, 2007. 387-533. ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))

* [MO/96137/categorical-description-of-the-restricted-product-adeles](http://mathoverflow.net/questions/96137/categorical-description-of-the-restricted-product-adeles)

[[!redirects restricted product]]
[[!redirects restricted products]]
[[!redirects restricted direct product]]
[[!redirects restricted direct products]]