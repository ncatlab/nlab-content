
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Higher topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _$(\infty,1)$-sheaf_ or _$(\infty,1)$-stack_ is the higher analog of an [[(∞,1)-sheaf]] / [[∞-stack]].

For $\mathcal{C}$ an [[(∞,1)-category]] equipped with the structure of an [[(∞,1)-site]], an $(\infty,2)$-sheaf on $\mathcal{C}$ is an [[(∞,1)-functor]]

$$
  X : \mathcal{C}^{op} \to Cat_{(\infty,1)}
$$

to [[(∞,1)Cat]], that satisfies [[descent]]: hence which is a [[local object]] with respect to the [[covering]] [[sieve]] inclusions in $Func(\mathcal{C}^{op}, Cat_{(\infty,1)})$.

The [[(∞,2)-category]] of $(\infty,2)$-sheaves

$$
  Sh_{(\infty,2)}(\mathcal{C})
$$

is an [[(∞,2)-topos]], the [[homotopy theory]]-generalization of a [[2-topos]] of [[2-sheaves]].

## Examples

### Codomain fibration / canonical $(\infty,2)$-sheaf
 {#CodomainFibration}

Let $\mathcal{X}$ be an [[(∞,1)-topos]], regarded as a ([[large site|large]]) [[(∞,1)-site]] equipped with the [[canonical topology]]. Then an [[(∞,1)-functor]]

$$
  A : \mathcal{X}^{op} \to CAT_{(\infty,1)}
$$

is an $(\infty,2)$-sheaf precisely if it preserves [[(∞,1)-limits]] (takes [[(∞,1)-colimits]] in $\mathcal{X}$ to [[(∞,1)-limits]] in [[(∞,1)Cat]]).

+-- {: .num_prop }
###### Propositon

For $\mathcal{X}$ an $(\infty,1)$-topos, the functor

$$
  Cod : \mathcal{X}^{op} \to CAT_{(\infty,1)}
$$

$$
  Cod : A \mapsto \mathcal{X}_{/A}
$$

is a ([[universe enlargement|large]]) $(\infty,2)$-sheaf on $\mathcal{X}$ , regarded as a [[(∞,1)-site]] equipped with the [[canonical topology]]. Here $\mathcal{X}_{/A}$ is the [[slice (∞,1)-topos]] over $A$.

=--

This is a special case of ([Lurie, lemma 6.1.3.7](#Lurie)). 

+-- {: .num_remark }
###### Remark

The functor $Cod$ [[(∞,1)-Grothendieck construction|classifies]] the [[codomain fibration]]. Its fiberwise [[stabilization]] to the [[tangent (∞,1)-category]] is the $(\infty,2)$-sheaf of [[quasicoherent sheaves]] on $\mathcal{X}$.

=--



## Related concepts

* [[sheaf]]

* [[2-sheaf]], [[(2,1)-sheaf]]

* [[(∞,1)-sheaf]] / [[∞-stack]]

* **$(\infty,2)$-sheaf**

* [[(∞,n)-sheaf]]

## References

 

* {#Lurie} [[Jacob Lurie]], section 6.1.3 of _[[Higher Topos Theory]]_
 
Discussion of a local [[model structure on simplicial presheaves]] $[S^op, sSet_{Joyal}]_{loc}$ with respect to the [[Joyal model structure]] $sSet_{Joyal}$ for [[quasicategories]] is in

* {#Meadows15} Nicholas Meadows, _The Local Joyal Model Structure_ ([arXiv:1507.08723](http://arxiv.org/abs/1507.08723))


[[!redirects (∞,2)-sheaf]]
[[!redirects (∞,2)-sheaves]]
[[!redirects (infinity,2)-sheaves]]
