
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Supergeometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _super-translation group_  is a [[supergroup]] generalization of the [[translation group]], hence of the additive [[Lie group]] $\mathbb{R}^n$. Its underlying [[supermanifold]] is a [[super-Euclidean space]] or [[super-Minkowski spacetime]].

## Definition

Given a [[super Poincaré Lie algebra]] extension $\mathfrak{siso}_N(d-1,1)$ of a [[orthogonal Lie algebra]] $\mathfrak{so}(d-1,1)$ for some [[spin representation]] $N$, then the corresponding _super-translation Lie algebra_ is the [[quotient]]

$$
  \mathbb{R}^{d-1,1\vert N}
  \coloneqq
  \mathfrak{siso}_N(d-1,1)/\mathfrak{o}(d-1,1)
$$

See at _[[super Minkowski spacetime]]_.

The underlying [[super vector space]] of this is

$$
  \mathbb{R}^d \oplus \Pi S
  \,,
$$

where $S$ is the vector space underlying the given [[spin representation]].

The [[super Lie algebra]] structure is mildly non-abelian with the only non-trivial bracket being that between two [[spinors]] and given by the bilinear pairing (the [[charge conjugation matrix]]) between two spinors:

$$
  [\psi, \phi] = \langle \psi, \Gamma^a \phi \rangle t_a
  \,,
$$

where $\{t_a\}$ is a [[basis]] for the translation generators in $\mathbb{R}^d$.

## Properties

### As a central extension of the superpoint

The super-translation Lie algebra is a super-[[Lie algebra extension]] of the abelian [[super Lie algebra]] which is just the [[superpoint]] $\mathbb{R}^{0;N}$ by the $d$ super [[Lie algebra cocycles]] 

$$
  (\phi, \psi) \mapsto \langle \phi, \Gamma^a \psi\rangle t_a
  \,,
$$

for $a \in \{1, 2, \cdots, d\}$, where $\{t_a\}$ are the [[basis]] elements of $\mathbb{R}^d$.


This simple but maybe noteworthy fact has been highlighted in the context of the [[brane scan]] in ([CAIP 99, section 2.1](#CAIP99)).

This mechanism plays a role in [[string theory]] when realizing $\mathbb{R}^{11;N=1}$ as a central extension of $\mathbb{R}^{10;N=(1,1)}$, for this formalizes aspects of the idea that [[type IIA string theory]] with a [[D0-brane]] condensate is [[11-dimensional supergravity]]/[[M-theory]] ([FSS 13](#FSS13)).


## Examples

### In dimension 1

The additive group structure on $\mathbb{R}^{1|1}$ is given on [[generalized element]]s in (i.e. in the logic internal to) the [[topos]] of [[sheaf|sheaves]] on the category [[SCartSp]] of [[cartesian space|cartesian]] superspaces by

$$
  \mathbb{R}^{1|1} \times \mathbb{R}^{1|1} \to 
  \mathbb{R}^{1|1}
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

Recall how the notation works here: by the [[Yoneda embedding]] we have a [[full and faithful functor]]

> [[SDiff]] $\hookrightarrow$ $Fun(SDiff^{op}, Set)$

and we also have the theorem, discussed at [[supermanifold]]s, that maps from some $S \in SDiff$ into $\mathbb{R}^{p|q}$ is given by a tuple of $p$ even section $t_i$ and $q$ odd sections $\theta_j$. The above notation specifies the map of supermanifolds by displaying what map of sets of maps from some test object $S$ it corresponds to under the [[Yoneda embedding]].

Now,  or each $S \in $ [[SDiff]] there is a [[group]] structure on the [[hom-set]] $SDiff(S, \mathbb{R}^{1|1}) \simeq C^\infty(S)^{ev} \times C^\infty(X)^{odd}$ given by precisely the above formula for this given $S$

$$
  \mathbb{R}^{1|1}(S) \times \mathbb{R}^{1|1}(S) \to 
  \mathbb{R}^{1|1}(S)
$$

$$
  (t_1, \theta_1), (t_2, \theta_2)
  \mapsto
  (t_1 + t_2 + \theta_1 \theta_2, \theta_1 + \theta_2)
  \,.
$$

where $(t_i, \theta_i) \in C^\infty(S)^{ev} \times C^\infty(S)^{odd}$ etc and where the addition and product on the right takes place in the function [[super algebra]] $C^\infty(S)$.

Since the formula looks the same for all $S$, one often just writes it without mentioning $S$ as above.

## Related concepts

* [[translation Lie algebra]]

* [[super Minkowski spacetime]]

* [[super Poincaré group]]

* [[super Poincaré Lie algebra]]

## References

* [[Veeravalli Varadarajan]], section 7 of _Supersymmetry for mathematicians: An introduction_


Discussion in the context of the [[brane scan]] is in section 2.1 of 

* {#CAIP99} C. Chryssomalakos, [[José de Azcárraga]], J.M. Izquierdo, J.C. P&#233;rez Bueno, _The geometry of branes and extended superspaces_, Nucl.Phys.B567:293-330, 2000 ([arXiv:hep-th/9904137](http://arxiv.org/abs/hep-th/9904137))
 

and more generally in the context of [[schreiber:The brane bouquet]] in

* {#FSS13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_
 

[[!redirects super-translation groups]]

[[!redirects super-Heisenberg group]]
[[!redirects super-Heisenberg groups]]

[[!redirects super translation Lie algebra]]
[[!redirects super translation Lie algebras]]

[[!redirects translation super-Lie algebra]]
[[!redirects translation super-Lie algebras]]

[[!redirects super-translation super-Lie algebra]]
[[!redirects super-translation super-Lie algebras]]


[[!redirects super translation algebra]]
[[!redirects super translation algebras]]
[[!redirects super-translation algebra]]
[[!redirects super-translation algebras]]
[[!redirects super translation Lie algebra]]
[[!redirects super translation Lie algebras]]
[[!redirects super-translation Lie algebra]]
[[!redirects super-translation Lie algebras]]

[[!redirects super translation group]]
[[!redirects super translation groups]]

[[!redirects translation supergroup]]
[[!redirects translation supergroups]]
