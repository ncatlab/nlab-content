


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

Since the crucial extra [[structures]] carried by an [[orbifold]] are

1. geometric structure (e.g. [[topology|topological]], [[algebraic geometry|algebro-geometric]], [[differential geometry|differential-geometric]], [[supergeometry|super-geometric]], etc.)

1. [[singularities]]

the [[cohomology]] of orbifolds should be such as to provide [[invariants]] which are sensitive not just to the underlying plain [[homotopy type]] of an orbifold (its [[shape modality|shape]]) but also to this extra structure. This means that _orbifold cohomology_ should, respectively, unify

1. geometric cohomology (e.g. [[sheaf cohomology|sheaf]] [[hypercohomology]], [[differential cohomology]], etc.)

1. [[equivariant cohomology]] in its fine form of [[Bredon cohomology]]
 
in the sense that [[differential cohomology|geometric cohomology]] is recovered away from the orbifold [[singularities]] and [[equivariant cohomology]] is recovered right at the [[singularities]], while globally orbifold cohomology provides a unification of these two aspects.

Since any concept of [[cohomology]] (as discussed there) is effectively equivalent to the choice of ambient [[(∞,1)-topos]], the question of defining orbifold cohomology is closely related to the question of how exactly to define the [[(∞,1)-category]] of orbifolds (usually a [[(2,1)-category]]) in the first place. This question is notoriously more subtle than the simple intuitive idea of orbifolds might suggest, as witnessed by the convoluted history of the concept (see e.g. [Lerman 08, Introduction](orbifold#Lerman08)).

\linebreak

### Deficiency of orbifolds as geometric groupoids

A proposal popular among [[Lie theory|Lie theorists]] ([Moerdijk-Pronk 97](orbifold#MoerdijkPronk97)) is to regard an orbifold with local charts $U_i \in G_i Actions$ ([[actions]] of some [[group]] on some local model [[space]]) as the [[geometric stack]] obtained by gluing the corresponding [[homotopy quotients]]/[[quotient stacks]] $U_i \!\sslash \!G_i$. If $\mathbf{H}$ is the ambient [[cohesive (∞,1)-topos]] in which this takes place (for instance $\mathbf{H} = $ [[Smooth∞Groupoids]], [[SuperFormalSmooth∞Groupoids]], etc.) and if $G \in Grp \overset{Disc}{\hookrightarrow} Grp(\mathbf{H})$ is a [[discrete group]] in which all the [[isotropy groups]] of the orbifold are contained, this gives an object 

$$
  \left(
  \array{
    \mathcal{X}
    \\
    \downarrow^{\mathrlap{faith}}
    \\
    \mathbf{B}G
  }
  \phantom{{}^{faith}}
  \right)
  \;\in\;
  \left( 
    \mathbf{H}_{/\mathbf{B}G}
  \right)_{\leq 0}
  \hookrightarrow
  \mathbf{H}_{/\mathbf{B}G}
$$

in the [[slice (∞,1)-topos]] over the [[delooping]] $\mathbf{B}G = \ast \sslash G$ of $G$, which is still a [[0-truncated object]], reflecting that as a [[functor]] of [[groupoids]] the morphism $\mathcal{X} \to \mathbf{B}G$ is a [[faithful functor]].

Accordingly, if this is -- or were -- the correct formalization of the nature of [[orbifolds]] $\mathcal{X}$, then the corresponding orbifold cohomology has [[coefficients]] given by objects $\mathcal{A} \in \mathbf{H}_{/\mathbf{B}G}$ and cohomology sets being the [[connected components]] of the [[(∞,1)-categorical hom-spaces]]

$$
  H_{\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \;\coloneqq\;
  \pi_0 \mathbf{H}_{/\mathbf{B}G}\big( \mathcal{X}, \mathcal{A}\big)
  \,.
$$

This concept of orbifold cohomology does fully reflect the geometric nature of orbifolds. It also reflects _some_ equivariance aspect. For example if $\mathcal{X} = \ast \sslash G$ is the one-point orbifold with singularity given by a finite group $G$, and if $V \in G Representations$ is a [[linear representation]], with $K(V,n)\sslash G \in \infty Groupoids_{/\mathbf{B}G} \overset{Disc}{\hookrightarrow} \mathbf{H}_{/\mathbf{B}G}$ its [[Eilenberg-MacLane space]], then 

$$
  H_{\mathbf{B}G}\big( 
    \mathbf{B}G, K(V,n)\sslash G
  \big)
  \;\simeq\;
  H^n_{grp}(G,V)
$$

is the [[group cohomology]] of $G$ with [[coefficients]] in $V$.

However, this definition does _not_ reflect [[Bredon cohomology|Bredon]]-[[equivariant cohomology]] around the orbifold singularities. Instead, it really given (geometric/stacky refinement) of _[[cohomology with local coefficients]]_.


$\,$

### Lift of orbifolds to singular-cohesive homotopy theory

Hence the proposal of [Moerdijk-Pronk 97](orbifold#MoerdijkPronk97), that an [[orbifold]] should be regarded as a certain [[geometric stack]], is missing something. It was briefly suggested in [Schwede 17, Introduction](#Schwede17), [Schwede 18, p. ix-x](#Schwede18) that the missing aspect is provided by [[global equivariant homotopy theory]], but details seem to have been left open. 

Here we discuss how to define the required orbifold cohomology in detail and in general. We combine the [[differential cohesion]] for the geometric aspect with the cohesion of [[global equivariant homotopy theory]] that was observed and highlighted in [Rezk 14](#Rezk14).

The following may serve as intuition for the issue with the nature of orbifolds:

Envision the picture of an orbifold singularity and hold a mathemagical magnifying glass over the singular point. Under this magnification you can see resolved the singular point as a fuzzy fattened point, to be called $\mathbb{B}G$.

Removing the magnifying glass, what one sees with the bare eye depends on how one squints:

* The physicist says that what he sees is a singular point, but a point after all. This is the plain [[quotient]]  $\ast = \ast / G$. 

* The Lie geometer says that what she sees is a point transforming under the $G$-[[action]] that fixes it, hence the [[homotopy quotient]] [[groupoid]] $\mathbf{B}G =\ast \sslash G$.

These are two [[adjoint modality|opposite extreme aspects]] of the orbifold singularity $\mathbb{B}G$, but the orbifold singularity itself is more than both of these aspects. The real nature of an orbifold singularity is in fact a point, not a big [[classifying space]] $\mathbf{B} G$ (recall that already $\mathbf{B}\mathbb{Z}_2 = \mathbb{R}P^\infty$), but it is a point that also remembers the group [[action]], for that characterizes how the singularity is being singular:

$$
   \array{
       && 
       { \text{orbifold singularity} \atop {\mathbb{B}G} }
      \\
      & {}^{\mathllap{\boxed{\lt}}}\swarrow 
      & 
       {{\phantom{A}} \atop {  \text{opposite extreme} \atop \text{aspects of orbifold singularity} }} & \searrow^{\mathrlap{ \boxed{\subset} }}
     \\
     { \text{plain quotient} \atop {\ast = \ast/G} }
     &&
     &&
     { \text{homotopy quotient} \atop { \mathbf{B}G = \ast \sslash G } }
   }
$$

This "unity of opposites" may be captured by the [[modalities]] on the [[singular-cohesive (infinity,1)-topos|singular-cohesive $\infty$-topos]]  of [[singular-smooth infinity-groupoid|singular-smooth $\infty$-groupoids]]. Its intrinsic [[cohomology]] accomodates a good notion of orbifold cohomology ([SaSc 2020](#SatiSchreiber20)).


## Related concepts

* [[orbifold]]

* [[Gromov-Witten theory]]

* [[orbifold K-theory]], [[equivariant K-theory]]

* [[twisted ad-equivariant Tate K-theory]]

* [[equivariant elliptic cohomology]]

History

According to [Abramovich 05, p. 42](#Abramovich05):

> On December 7, 1995 [[Maxim Kontsevich]] delivered a history-making lecture at Orsay, titled _String Cohomology_. This is what is now know, after [Chen-Ruan 00](#ChenRuan00), as _orbifold cohomology_, Kontsevich's lecture notes described the orbifold and  [[quantum cohomology]] of a global quotient [[orbifold]]. Twisted sectors, the age grading, and a version of orbifold stable maps for global quotients are all there.

The same lecture also introduced _[[motivic integration]]_.

## References


[[!include traditional orbifold cohomology -- references]]



### Proper orbifold cohomology
 
Discussion of orbifold cohomology in the context of [[Bredon cohomology]]:

* {#PronkScull07} [[Dorette Pronk]], [[Laura Scull]], _Translation Groupoids and Orbifold Bredon Cohomology_, Canad. J. Math. 62(2010), 614-645 ([arXiv:0705.3249](https://arxiv.org/abs/0705.3249), [doi:10.4153/CJM-2010-024-1](https://doi.org/10.4153/CJM-2010-024-1))

The suggestion to regard orbifold cohomology in [[global equivariant homotopy theory]]:

* {#Schwede17} [[Stefan Schwede]], Introduction of: _Orbispaces, orthogonal spaces, and the universal compact Lie group_, Mathematische Zeitschrift 294 (2020), 71-107 ([arXiv:1711.06019](https://arxiv.org/abs/1711.06019))

* {#Schwede18} [[Stefan Schwede]], p. ix-x of: _[[Global homotopy theory]]_, New Mathematical Monographs, 34 Cambridge University Press, 2018 ([arXiv:1802.09382](https://arxiv.org/abs/1802.09382))

Spelling out this suggestion of [Schwede 17, Intro](#Schwede17), [Schwede 1, p. ix-x8](#Schwede18):

* {#Juran20} [[Branko Juran]], _Orbifolds, Orbispaces and Global Homotopy Theory_ ([arXiv:2006.12374](https://arxiv.org/abs/2006.12374))

Based on results of or related to:

* {#HenriquesGepner07} [[André Henriques]], [[David Gepner]], _Homotopy Theory of Orbispaces_ ([arXiv:math/0701916](http://arxiv.org/abs/math/0701916))

The observation of the [[cohesion of global- over G-equivariant homotopy theory]] is due to:

* {#Rezk14} [[Charles Rezk]], _[[Global Homotopy Theory and Cohesion]]_, 2014

A formulation of orbifold cohomology in the [[singular-cohesive (infinity,1)-topos|singular-cohesive $\infty$-topos]] of [[singular-smooth infinity-groupoids|singular-smooth $\infty$-groupoids]] is then discussed in:

* {#SatiSchreiber20} [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))






[[!redirects orbifold cohomologies]]

[[!redirects orbifold cohomology group]]
[[!redirects orbifold cohomology groups]]

[[!redirects orbispace cohomology]]
[[!redirects orbispace cohomologies]]

[[!redirects orbispace cohomology group]]
[[!redirects orbispace cohomology groups]]

