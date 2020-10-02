
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohesive $\infty$-Toposes
+--{: .hide}
[[!include cohesive infinity-toposes - contents]]
=--
#### Super-Geometry
+--{: .hide}
[[!include supergeometry - contents]]
=--
=--
=--

> this entry is under construction

#Contents#
* table of contents
{:toc}

## Idea

The notion of _smooth super $\infty$-groupoid_ or _smooth super [[geometric homotopy type]]_ is the combination of of _[[super ∞-groupoid]]_ and _[[smooth ∞-groupoid]]_. The [[cohesive (∞,1)-topos]] of smooth super-$\infty$-groupoids is a context that realizes [[higher geometry|higher]] [[supergeometry]].

Smooth super $\infty$-groupoids include
[[supermanifolds]], [[super Lie groups]] and their [[deloopings]] etc. Under [[Lie differentiation]] these map to [[super L-∞ algebras]].


## Definition

We consider one of at least two possible definitions, that differ (only) slightly in some fine technical detail. The other is at _[[super smooth infinity-groupoid]]_.

We take a _smooth super $\infty$-groupoid_ to be a [[smooth ∞-groupoid]] but not over the [[base topos]] [[∞Grpd]] of bare [[∞-groupoid]]s, but over the [[base topos]] [[Super∞Grpd]] of [[super ∞-groupoids]].


+-- {: .num_defn #SuperCartesianSpaces}
###### Definition

Write $sCartSp$ for the [[full subcategory]] of that of [[supermanifolds]] on the [[super Cartesian spaces]] $\{\mathbb{R}^{p|q}\}_{p,q \in \mathbb{N}}$. Regard this as a [[site]] by taking the [[coverage]] the product coverage of the [[good open cover]] coverage of [[CartSp]] and the trivial coverage on [[superpoints]].

=--

+-- {: .num_remark}
###### Remark

So a [[covering]] family of $\mathbb{R}^{p|q}$ is of the form 

$$
  \{
    U_i \times \mathbb{R}^{0|q} \longrightarrow \mathbb{R}^{p|q}
  \}_{i}
$$

for 

$$
  \{
    U_i  \longrightarrow \mathbb{R}^{p}
  \}_{i}
$$

a differentiably [[good open cover]] of $\mathbb{R}^{p}$.


=--


+-- {: .num_defn #SmoothSuperInfinityGroupoids}
###### Definition

Let

$$
  SmoothSuper\infty Grpd := Sh_{(\infty,1)}(sCartSp, Super \infty Grpd)
$$

be the [[(∞,1)-topos]] of [[(∞,1)-sheaves]] over the site $sCartSp$, def. \ref{SuperCartesianSpaces}.

=--

+-- {: .num_prop}
###### Proposition

The [[(∞,1)-topos]] $Smooth \infty Grpd$ of def. \ref{SmoothSuperInfinityGroupoids} is  a [[cohesive (∞,1)-topos]] over [[∞Grpd]].

=--

This and the stronger statement that it is in fact it is actually cohesive over [[Super∞Grpd]] is discussed [below](CohesionOverBaseToposes), see cor. \ref{SystemOfCohesion}.



## Properties

### Cohesion over smooth $\infty$-groupoids and over super $\infty$-groupoids
 {#CohesionOverBaseToposes}


+-- {: .num_prop}
###### Proposition

$Smooth Super \infty Grpd$ is a [[cohesive (∞,1)-topos]]
over [[Super∞Grpd]].

$$
  Smooth Super \infty Grpd
   \stackrel{\overset{\Pi_{Super}}{\longrightarrow}}{\stackrel{\overset{Disc_{Super}}{\leftarrow}}{\stackrel{\overset{\Gamma_{Super}}{\longrightarrow}}{\underset{coDisc_{super}}{\leftarrow}}}}
  Super \infty Grpd
 \,.
$$

=--

+-- {: .proof}
###### Proof

By definition of the [[coverage]] on $sCartSp$ in def. \ref{SuperCartesianSpaces}, the proof of the cohesion of [[Smooth∞Grpd]] = $Sh_\infty(CartSp)$ goes through verbatim _for each fixed [[superpoint]]_ and that gives precisely the claim.

=--

+-- {: .num_prop}
###### Proposition

[[Super∞Grpd]] is [[infinitesimal cohesion|infinitesimally cohesive]] over [[∞Grpd]].

=--

By the discussion at [[Super∞Grpd]].

+-- {: .num_cor #SystemOfCohesion}
###### Corollary

$SmoothSuper\infty Grpd$ is cohesive and in 

In fact we have a [[commutative diagram]] of [[cohesive (∞,1)-topos]]

$$
  \array{
     Smooth Super \infty Grpd 
   &\stackrel{\overset{\Pi_{Super}}{\longrightarrow}}{\stackrel{\overset{Disc_{Super}}{\leftarrow}}{\stackrel{\overset{\Gamma_{Super}}{\longrightarrow}}{\underset{coDisc_{super}}{\leftarrow}}}}
   &
   Super \infty Grpd
     \\
     \downarrow \uparrow && \downarrow \uparrow
     \\
     Smooth \infty Grpd 
    &
   \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
    & \infty Grpd
  }
$$

where the right vertical adjoints exhibit [[infinitesimal cohesion]].

=--

## Structures 

We discuss realizations of the general abstract
<a href="http://nlab.mathforge.org/nlab/show/cohesive+%28infinity%2C1%29-topos#Structures">structures in a cohesive (∞,1)-topos</a> realized in $Smooth Super \infty Grpd$.

### Exponentiated super $L_\infty$-algebras

A [[super L-∞ algebra]] $\mathfrak{g}$ is an [[L-∞ algebra]] internal to 
$Sh(SuperPoint)$.

The [[Lie integration]] of $\mathfrak{g}$ is ...

## Applications

* [[D'Auria-Fre formulation of supergravity]]

* [[schreiber:The brane bouquet]] of [[Green-Schwarz action functionals]] for super $p$-[[brane]] [[sigma-models]].

## Related concepts

* [[cohesive (∞,1)-topos]]

  * [[discrete ∞-groupoid]]

  * [[Euclidean-topological ∞-groupoid]]

  * [[smooth ∞-groupoid]]

  * [[synthetic differential ∞-groupoid]]

  * [[super ∞-groupoid]]

  * **smooth super ∞-groupoid**

    * [[Super Gerbes]]

  * [[super formal smooth infinity-groupoid]]

  * [[synthetic differential super ∞-groupoid]]




## References


For general references see the references at _[[super ∞-groupoid]]_ .

Discussion of smooth super $\infty$-groupoids:

* [[Urs Schreiber]], section 4.5 of: _[[schreiber:differential cohomology in a cohesive topos]]_

* [[Hisham Sati]], [[Urs Schreiber]], Section 3.1.3 of: _[[schreiber:Proper Orbifold Cohomology]]_ ([arXiv:2008.01101](https://arxiv.org/abs/2008.01101))

* [[Urs Schreiber]], _[[schreiber:Introduction to Higher Supergeometry]]_, lecture at _[[Higher Structures in M-Theory 2018]]_, [Durham Symposium](http://www.maths.dur.ac.uk/lms/)

  published in parts as: _Higher Structures in M-Theory_ (with [[nLab:Branislav Jurčo]], [[nLab:Christian Saemann]], [[nLab:Martin Wolf]]), Fortschritte der Physik (2019) ([arXiv:1903.02807](https://arxiv.org/abs/1903.02807), [doi:10.1002/prop.201910001]( https://doi.org/10.1002/prop.201910001))


[[!redirects super smooth ∞-groupoid]]
[[!redirects super smooth infintiy-groupoid]]


[[!redirects smooth super ∞-groupoid]]

[[!redirects smooth super infinity-groupoids]]
[[!redirects smooth super ∞-groupoids]]

[[!redirects SuperSmooth∞Grpd]]
[[!redirects SmoothSuper∞Grpd]]

[[!redirects smooth super homotopy type]]
[[!redirects smooth super homotopy types]]

[[!redirects smooth super ∞-group]]
[[!redirects smooth super ∞-groups]]

[[!redirects smooth super-n-group]]
[[!redirects smooth super-n-groups]]

[[!redirects smooth super infinity-group]]
[[!redirects smooth super infinity-groups]]


[[!redirects smooth super space]]
[[!redirects smooth super spaces]]


