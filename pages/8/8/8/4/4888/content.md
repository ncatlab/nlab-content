

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

An **associated $\infty$-bundle** $E \to X$ is a [[fiber bundle]] in an [[(∞,1)-topos]] $\mathbf{H}$ with typical fiber $F \in \mathbf{H}$ that is classified by a [[cocycle]] $X \to \mathbf{B}Aut(F)$ with coefficients in the [[delooping]] of the [[automorphism ∞-group]] of $F$.  We say this is _associated to_ the corresponding  $Aut(F)$-[[principal ∞-bundle]]. 

## Definition

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. 

+-- {: .un_def}
###### Definition

For $F,X \in \mathbf{H}$ [[pointed object]]s, an **$\infty$-fiber bundle** on $X$ with fiber $F$ is a [[fiber sequence]]

$$
  F \to E \to X
$$

which is locally trivial (...).

=--

+-- {: .un_remark}
###### Remark

By the [Properties](#Properties) discussed below we have that such $\infty$-fiber bundles are classified by morphism $X \to \mathbf{B}Auf(F)$. These also classify $Aut(F)$-[[principal ∞-bundle]]s. We may say that $E$ is **associated** to this corresponding principal $\infty$-bundle.

=--

## Properties {#Properties}

+-- {: .un_prop}
###### Theorem

$\infty$-Fiber bundles $F \to E \to X$ are classified by morphisms $X \to \mathbf{B} Aut(F)$.

=--

+-- {: .proof}
###### Proof


This is shown in ([Wendt](#Wendt)), section 5.5, using [[model category]]-theoretic presentations (see [[models for ∞-stack (∞,1)-toposes]]) 


=--


+-- {: .un_remark}
###### Remark


This generalizes to associated $\infty$-bundles the statement (discussed at [[principal ∞-bundle]]) that $G$-principal $\infty$-bundles $P \to X$ are precisely the [[homotopy fiber]]s of [[cocycle]] morphism $X \to \mathbf{B}G$.

Notice that the $(\infty,1)$-topos theoretic argument as [[principal ∞-bundle]] uses crucially that in the [[(∞,1)-topos]] $\mathbf{H}$ we have $(\infty,1)$-[[universal colimits]]. In [Wendt](#Wendt)) precisely the analogous [[homotopy colimit]]-properties produce the above result. Using these the result follows in analogy to [May](#May).

=--

+-- {: .un_prop}
###### Proposition

The universal $F$-$\infty$-bundle $\mathbf{E} F \to \mathbf{B}Aut(F)$ is presented by the [[bar construction]]

$$
  F \to B(*, Aut(F), F) \to B(*, Aut(F), *)
  \,.
$$


=--

Compare [[universal principal ∞-bundle]].


## Related concepts

* [[principal bundle]] / [[torsor]] / [[associated bundle]]

* [[principal 2-bundle]] / [[gerbe]] / [[bundle gerbe]]

* [[principal 3-bundle]] / [[bundle 2-gerbe]]

* [[principal ∞-bundle]] / **associated $\infty$-bundle


## References

Early work on associated $\infty$-bundles takes place in the $(\infty,1)$-topos [[∞Grpd]] $\simeq$ [[Top]]. In

* [[Jim Stasheff]], _A classification theorem for fiber spaces_ , Topology 2 (1963) 239-246

a classification of [[fibration]]s of [[CW-complex]]es with given CW-complex fiber in terms of maps into a classifying CW-complex is given.

A generalization of this is in

* [[Peter May]], _Classifying Spaces and Fibrations_ Mem. Amer. Math. Soc. 155 (1975)
{#May}

Consideration of associated $\infty$-bundles / [[fiber sequence]]s in general [[(∞,1)-topos]]es is more recent. 

Associated $\infty$-bundles in terms of the presentation of the $(\infty,1)$-topos by the [[model structure on simplicial presheaves]] are discussed in

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ ([arXiv](http://arxiv.org/abs/1009.2930))
{#Wendt}

Related discussion on the behaviour of [[fiber sequence]]s under left [[Bousfield localization of model categories]] is in

* [[Matthias Wendt]], _Classifying spaces and fibrations of simplicial sheaves_ ([pdf](http://home.mathematik.uni-freiburg.de/arithmetische-geometrie/preprints/wendt-flocal.pdf))


[[!redirects associated ∞-bundle]]