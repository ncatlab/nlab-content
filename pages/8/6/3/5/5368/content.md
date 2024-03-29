
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

This entry discusses [[model category]] structures on categories of [[algebras over an operad]] in the [[category of chain complexes]] (unbounded).

This is a special case of the general discussion at [[model structure on algebras over an operad]], but the category of (unbounded) chain complexes warrents some special attention.

For the operad of ordinary (commutative) algebras see also [[model structure on dg-algebras]].

## Definition
 {#Definition}

Let $k$ be a commutative ring. 
Write $Ch_\bullet(k)$ for the [[category of chain complexes|category of unbounded chain complexes]] of $k$-[[module]]s.

+-- {: .num_defn #SigmaSplitOperad}
###### Definition

An [[operad]] $P$ over $Ch_\bullet(k)$ is called **$\Sigma$-split** if (...)

A quasi-isomorphism between such operads $P_1 \to P_2$ is said to be compatible with $\Sigma$-splitting if (...)

=--

+-- {: .num_prop}
###### Proposition

If $k$ contains the ring of [[rational number]]s, $\mathbb{Q} \hookrightarrow k$, then every $Ch_\bullet(k)$-operad is $\Sigma$-split and every quasi-isomorphism of operads is compatible with $\Sigma$-splitting.


The [[associative operad]] $Assoc_k$ is $\Sigma$-split for all $k$.


=--

This is ([Hinich, example 4.2.5](#Hinich)).

+-- {: .num_theorem #ModelStructure}
###### Theorem

Let $P$ be a $\Sigma$-split operad, def. \ref{SigmaSplitOperad}, in $Ch_\bullet(k)$. Then the category $Alg_{Ch_\bullet(k)}(P)$ of [[algebras over an operad|algebras over the operad]] admits a [[model category]] structure whose 

* weak equivalences are the underlying [[quasi-isomorphisms]] 

* whose fibrations are the degreewise surjections 

in $Ch_\bullet(k)$.

The [[free-forgetful adjunction]]

$$
  Alg_{Ch_\bullet(k)}(P)
  \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  Ch_\bullet(k)
$$

is therefore a [[Quillen adjunction]] (see at _[[transferred model structure]]_).

=--

This appears as ([Hinich, theorem 4.1.1](#Hinich)).

## Properties

### Invariance under equivalence and rectification

+-- {: .num_theorem #ResolutionInvariance}
###### Theorem

If $P_1 \to P_2$ is a [[quasi-isomorphism]] of $\Sigma$-split operads compatible with splittings, then there is an induced [[Quillen equivalence]]

$$
  Alg(P_1) \stackrel{\overset{}{\leftarrow}}{\underset{}{\rightarrow}}
  Alg(P_2)
$$

between the corresponding model structures on their algebras, as above.

=--

This is ([Hinich, theorem 4.7.4](#Hinich)).

+-- {: .num_remark}
###### Remark

Theorem \ref{ResolutionInvariance} in particular provides 
rectification results for [[homotopy algebras]]: if
$P$ is some operad and $\tilde P \stackrel{\simeq}{\to} P$ a 
[[cofibrant resolution]] in the suitable [[model structure on operads]], then the theorem says that $P$-[[homotopy algebras]] have the same homotopy theory as the plain $P$-algebras.

Famous examples include the [[Quillen equivalence]] between the [[model structure on dg-Lie algebras]] and the [[model structure for L-infinity algebras]].

=--



### Simplicial enrichment {#SimplicialEnrichment}

We discuss how the [above model structure](#ModelStructure) on $Alg_{Ch_\bullet(k)}(P)$ is _almost_ enhanced to a [[simplicial model category]] structure.

First we recall the standard definition of polynomial [[differential forms on simplices]]:

+-- {: .num_defn}
###### Definition

For $n \in \mathbb{N}$ let $\Omega_{poly}^\bullet(\Delta^n)$ be the commutative [[dg-algebra]] of **[[polynomial]] [[differential form]]s** on the $n$-[[simplex]]:

as a graded algebra it is 

$$
  \Omega_{poly}^{\bullet}(\Delta^n)
  :=
  k[t_0, \cdots, t_n, d t_0, \cdots, d t_n]/(\sum t_i -1, \sum d t_i)
$$

with the differential the usual de Rham differential under the embedding $\Omega^\bullet_{poly}(\Delta^n) \hookrightarrow \Omega^\bullet(\Delta^n)$.

For $f : [k] \to [l]$ a [[morphism]] in the [[simplex category]] let

$$
  \Omega^\bullet_{poly}(f) : \Omega^\bullet_{poly}(\Delta^l) \to \Omega^\bullet_{poly}(\Delta^k)
$$

be the morphism of dg-algebras given on generators by 

$$
  \Omega^\bullet_{poly}(f) : t_i \mapsto \sum_{f(j) = i} t_j
  \,.
$$

This yields a [[simplicial object|simplicial]] commutative dg-algebra

$$
  \Omega^\bullet_{poly}(\Delta^{(-)}) : \Delta^{op} \to cdgAlg_k
$$

or equivalently a [[cosimplicial object]] in the [[opposite category]] $cdgAlg_k^{op}$.

By the general definition of [[differential forms on presheaves]] this extends by left [[Kan extension]] to a functor

$$
  \Omega^\bullet_{poly} : sSet \to cdgAlg_k^{op}
$$

given by

$$
  \Omega^\bullet_{poly}(S) = \int^{[k]\in \Delta} S_k \cdot \Omega^\bullet_{poly}(\Delta^k)
  \,, 
$$

where on the right be have the [[coend]] over the [[copowering]] of $cdgAlg_k^{op}$ over [[Set]].

=--

+-- {: .num_defn #SimplicialHomObjects}
###### Definition

For $P$ a dg-operad as above, define [[sSet]]-[[hom-object]]s between objects $A,B \in Alg(P)$ by

$$
  Alg_P(A,B) := ([n] \mapsto Hom_{Alg_P}(A, B \otimes \Omega^\bullet_{poly}(\Delta^n))
  \in sSet
  \,.
$$
 
=--

+-- {: .num_prop}
###### Proposition

These simplicial hom-objects satisfy the dual of the [[pushout-product axiom]] (see [[enriched model category]]).

=--

This is ([Hinich, lemma 4.8.4](#Hinich)).



+-- {: .num_prop }
###### Proposition

For $S$ a degreewise finite simplicial set, we have a [[natural isomorphism]]

$$
  Hom_{Alg_P}(A, B \otimes \Omega^\bullet_{poly}(S))
  \simeq
  Hom_{sSet}(S, Alg_P(A,B))
  \,.
$$

=--

This is ([Hinich, lemma 4.8.3](#Hinich)).

+-- {: .num_prop }
###### Proposition

The [[homotopy category]] of $Alg_P$ is given by

$$
  Ho(Alg_P)(A,B) \simeq \pi_0 Alg_P(Q A,B)
  \,,
$$

where $Q A$ is a cofibrant [[resolution]] of $A$.

=--

This appears as ([Hinich, section 4.8.10](#Hinich)).

## Examples

* [[model structure for L-∞ algebras]]


## Related concepts

* [[model structure on dg-operads]]

* **model structure on dg-algebras over an operad**

  * [[model structure on dg-algebras]]

  * [[model structure on dg-categories]]

## References

The model structure on dg-algebras over an operad is discussed in

* [[Vladimir Hinich]],  _Homological algebra of homotopy algebras_ Communications in algebra, 25(10). 3291-3323 (1997)([arXiv:q-alg/9702015](http://arxiv.org/abs/q-alg/9702015), _Erratum_ ([arXiv:math/0309453](http://arxiv.org/abs/math/0309453)))
{#Hinich}


based on results in

* A.K. Bousfield, V.K.A.M. Gugenheim, _On PL de Rham theory and rational homotopy type_ , Memoirs AMS, t.8, 179(1976)