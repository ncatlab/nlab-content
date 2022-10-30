
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $C$ a [[small category]], and $PSh(C)$ its [[presheaf topos]], we have (by the discussion at _[Profunctor -- In terms of colimit preserving functors on presheaf categories](profunctor#FuncsOnPresheaves)_) that a cocontinuous,
 i.e., [[colimit]]-preserving, [[functor]] $PSh(C) \to Set$ is equivalently itself a [[copresheaf]] on $C$:

$$
  [PSh(C), Set]_{coc} \simeq CoPSh(C)
  \,.
$$

If we replace in this statement presheaves with [[sheaves]], we obtain the notion of _cosheaf_ on $C$:

$$
  [Sh(C), Set]_{coc} \simeq CoSh(C)
  \,.
$$

## Definition

+-- {: .num_defn #cosheaf}
###### Definition

Let $C$ be a [[site]]. A **cosheaf** on $C$ is a [[copresheaf]]

$$
  F : C \to Set
$$

such that it takes [[cover]]s to [[colimit]]s: for each covering family $\{U_i \to U\}$ in $C$ we have

$$
  F(U) \simeq \lim_{\to}
  \left(
     \coprod_{i j} F(U_i \times_{U} U_j)
     \stackrel{\to}{\to}
     \coprod_i F(U_i)
  \right)
$$


Write $CoSh(C) \subset CoPSh(C)$ for the full [[subcategory]] of cosheaves.

=--

## Proposition

+-- {: .num_prop}
###### Proposition

There is a [[natural transformation|natural]] [[equivalence of categories]]

$$
  CoSh(C) \simeq Func_{coc}(Sh(C), Set)
  \,,
$$

where on the left we have the category of cosheaves from def. \ref{cosheaf} and on the right we have the category of [[colimit]]-preserving functors on the [[sheaf topos]] of $C$.

Equivalently: a copresheaf is a cosheaf precisely if its [[Yoneda extension]] $PSh(C) \to Set$ factors through the [[sheafification]] functor $PSh(C) \to Sh(C)$.

=--

This is ([Bunge-Funk 06, prop. 1.4.3](BungeFunk)).


## Examples

### In AQFT and higher AQFT

Cosheaves of [[algebras]], or notions similar to this, appear in [[AQFT]] as [[local nets of observables]]. Similar structures in [[higher category theory]] are _[[factorization algebras]]_, _[[factorization homology]]_, and _[[topological chiral homology]]_. Notably the definition of _[[factorization algebra]]_ typically explicitly involves the notion of cosheaf.

## Related concepts

* [[presheaf]] /  [[sheaf]] / **cosheaf**

* [[2-sheaf]] / [[stack]]

* [[(∞,1)-sheaf]] / [[∞-stack]] 

* [[Lawvere distribution]]


## References

* G. E. Bredon, _Sheaf Theory_ , Springer Heidelberg 1997. (chap. V-VI)

* [[Marta Bunge]] and [[Jonathon Funk]], _Singular coverings of toposes_ , Lecture Notes in Mathematics vol. 1890 Springer Heidelberg (2006). (sec. 1.4)

* [[Jonathon Funk]], _The Display Locale of a Cosheaf_ , Cah. Top. G&#233;om. Diff. Cat. **36** (1995) pp.53-93.

* Justin M. Curry, _Abstract existence of cosheafification_ ([pdf](https://services.math.duke.edu/~curry/papers/abstract_cosheafification.pdf))

* Andrei V. Prasolov, _Cosheafification_ ([arXiv:1605.01555](https://arxiv.org/abs/1605.01555))

[[!redirects cosheaves]]
