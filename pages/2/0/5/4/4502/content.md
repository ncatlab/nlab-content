
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

For an ordinary group $G$ the fact that $\mathbf{E}G$ naturally has a group structure was observed and used by Segal in 

* G. Segal, ...

The structure is manifest in the context [[∞Grpd]]: there $\mathbf{E}G$ is modeled by the [[groupoid]] $G//G$

$$
  G \times G \stackrel{\overset{\cdot}{\to}}{\underset{p_1}{\to}}
  G
  \,.
$$

We may think of this as the groupoid $INN(G) \subset AUT(G)$ of [[inner automorphism]]s inside the [[automorphism 2-group]] of $G$. But it is also simply isomorphic to the [[codiscrete groupoid]] on the set underlying $G$. In this latter form the group structure on $\mathbf{E}G$ is manifest, as is the fact that the canonical inclusion

$$
  G \to \mathbf{E}G
$$

is a homomorphism of [[strict 2-group]]s.

## For strict 2-groups

For $G \in $ [[∞Grpd]] a [[strict 2-group]] a groupal model for $\mathbf{E}G$ was given in [SchrRob](http://arxiv.org/abs/0708.1741) generalizing the $INN(G) \subset AUT(G)$ construction mentioned above. This yields a weak 3-group structure on $\mathbf{E}G$ (A [[Gray-group]]).

In [Roberts07](#RobertsUniversal) it is observed that there is also an analog of $codisc(G)$ and that this yields a strict group structure on $\mathbf{E}G$. In fact, this strictly groupal model of $\mathbf{E}G$ turns out to be isomorphic to the standard model for the universal [[simplicial principal bundle]] traditionally denoted $W G$. And this statement generalizes...


## For $\infty$-Groups

Every [[∞-group]] may be modeled by a [[simplicial group]] $G$. There is a standard [[Kan complex]] model for the universal $G$-[[simplicial principal bundle]] $\mathbf{E}G \to \mathbf{B}G$ denoted $W G \to \bar W G$. 

This standard model $W G$ does happen to have the structure of a [[simplicial group]] itself, and this structure is compatible with that of $G$ in that the canonical inclusion $G \to W G$ is a homomorphisms of simplicial groups.

This sounds like a statement that must be well known, but itwas maybe not in the literature. The simplicial group structure is spelled out explicitly in

* [[David Roberts]], _[Universal simplicial bundles and inner automorphissm n-groups](#RobertsUniversal)_

and an abstract construction of the group structure is in

* [[David Roberts]], [[Danny Stevenson]], _notes_

## For $\infty$-groups in an arbitrary $(\infty,1)$-topos

Since the $W$ construction discussed above is functorial, this generalizes to prresheaves of simplicial groups and hence gives models for group objects and groupal universal [[principal ∞-bundle]]s in  [[(∞,1)-topos]]es modeled by the [[model structure on simplicial presheaves]].

(...)

## References

* [[David Roberts]], _[[DRobertsUniversalSimpBunds.pdf:file]]_  
  {#RobertsUniversal}

[[!redirects groupal model for universal principal ∞-bundles]]
[[!redirects groupal models for universal principal ∞-bundles]]

[[!redirects groupal models for universal principal infinity-bundles]]
