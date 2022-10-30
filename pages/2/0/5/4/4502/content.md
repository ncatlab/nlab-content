
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Topos theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $G$ a model for an [[∞-group]], there is often a model for the [[universal principal ∞-bundle]] $\mathbf{E}G$ that itself carries a group structure such that the canonical inclusion $G \to \mathbf{E}G$ is a homomorphism of group objects. This extra groupal structure is important for various constructions.

## For ordinary groups

For $G$ an ordinary bare [[group], the [[action groupoid]] $\mathbf{E}G = G//G$ of the right multiplcation action of $G$ on itself 

$$
  G//G
  =
  \left(
  G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}}
  G
  \right)
$$

is [[contractible]]. We may think of this as the groupoid $INN(G) \subset AUT(G)$ of [[inner automorphism]]s inside the [[automorphism 2-group]] of $G$. But it is also simply isomorphic to the [[codiscrete groupoid]] on the set underlying $G$. In this latter form the 2-group structure on $\mathbf{E}G$ is manifest, which corresponds to the 
[[crossed module]] $(G \stackrel{Id}{\to} G)$ .

Als manifest is then that this fits with the one-object [[delooping]] groupoid $\mathbf{B}G$ of $G$ into a sequence

$$
  G \to \mathbf{E}G \to \mathbf{B}G
  \,,
$$

where the first morphism is a homomorphism of [[strict 2-group]]s. 

Regarded as a sequence of morphisms in the model [[Kan complex|KanCplx]] of the [[(∞,1)-topos]] [[∞-Grpd]] this _is_ already a model for the universal $G$-bundle.

If $G$ here is refined to a [[Lie group]] or [[topological group]] then this is a sequence of [[∞-Lie groupoid]]s or [[topological ∞-groupoid]]s, respectively, and also then, this _is_ already a model for the universal $G$-principal bundle, as discussed at <a href="http://ncatlab.org/nlab/show/Lie+infinity-groupoid#UniversalLieGroupPrincipalBundle">?LieGrpd -- the universal G-principal bundle</a>.

By applying the [[geometric realization]] functor

$$
  |-| : \infty Grpd \stackrel{\simeq}{\to} Top
$$

we obtain a sequence of topological spaces

$$
  G \to \mathcal{E}G \to \mathcal{B}G
  \,,
$$

where $\mathcal{E}G$ carries the structure of a [[topological group]] and the morphism $G \to \mathcal{E}G$ is a topological group homomorphism. For bare groups $G$ and under mild assumptions also for general topological groups $G$, this groupal topological model for the universal $G$-bundle obtained from the realization of the groupoid $G//G$ was consider in [Segal68](#Segal).


## For strict 2-groups

For $G \in $ [[∞Grpd]] a [[strict 2-group]] a groupal model for $\mathbf{E}G$ was given in [RobertsSchr07](#RobertsSchreiber) generalizing the $INN(G) \subset AUT(G)$ construction mentioned above. This yields a weak 3-group structure on $\mathbf{E}G$ (A [[Gray-group]]).

In [Roberts07](#RobertsUniversal) it is observed that there is also an analog of $codisc(G)$ and that this yields a strict group structure on $\mathbf{E}G$. In fact, this strictly groupal model of $\mathbf{E}G$ turns out to be isomorphic to the standard model for the universal [[simplicial principal bundle]] traditionally denoted $W G$. And this statement generalizes...


## For $\infty$-Groups

Every [[∞-group]] may be modeled by a [[simplicial group]] $G$. There is a standard [[Kan complex]] model for the universal $G$-[[simplicial principal bundle]] $\mathbf{E}G \to \mathbf{B}G$ denoted $W G \to \bar W G$. 

This standard model $W G$ does happen to have the structure of a [[simplicial group]] itself, and this structure is compatible with that of $G$ in that the canonical inclusion $G \to W G$ is a homomorphisms of simplicial groups.

This sounds like a statement that must be well known, but itwas maybe not in the literature. The simplicial group structure is spelled out explicitly in [Roberts07](#RobertsUniversal)


## For $\infty$-groups in an arbitrary $(\infty,1)$-topos

Since the $W$ construction discussed above is functorial, this generalizes to prresheaves of simplicial groups and hence gives models for group objects and groupal universal [[principal ∞-bundle]]s in  [[(∞,1)-topos]]es modeled by the [[model structure on simplicial presheaves]].

(...)

## References

The observation that for $G$ an ordinary [[group]], its [[action groupoid]] sequence $G \to G//G \to \mathbf{B}G$ -- which is the [[strict 2-group]] coming from the [[crossed module]] $(G \stackrel{Id}{\to} G)$ - maps under the [[nerve]] to the universal $G$-bundle appeared in

* G. B. Segal, _Classifying spaces and spectral sequences_ , Publ. Math. IHES
No. 34 (1968) pp. 105&#8211;112 {#Segal}

A weak 3-group structure on $G \to \mathbf{E}G$ for $G$ a [[strict 2-group]] is descibed in

* [[David Roberts]], [[Urs Schreiber]], _The inner automorphism 3-group of a strict 2-group_ , Journal of Homotopy and Related Structures, vol. 3(1) ([arXiv:0708.1741](http://arxiv.org/abs/0708.1741))
  {#RobertsSchreiber}

The [[simplicial group]] structure on $G \to \mathbf{E}G$ for $G$ a general [[simplicial group]] is stated explicitly in

* [[David Roberts]], _[[DRobertsUniversalSimpBunds.pdf:file]]_  
  {#RobertsUniversal}

A general abstract construction of this simplicial group strufture is discussed in

* [[David Roberts]], [[Danny Stevenson]], _notes in preparation_

[[!redirects groupal model for universal principal ∞-bundles]]
[[!redirects groupal models for universal principal ∞-bundles]]

[[!redirects groupal models for universal principal infinity-bundles]]
