
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

Quaternionic oriented cohomology theory is the analog of [[complex oriented cohomology theory]] as [[complex vector bundles]] are replaced by [[quaternionic vector bundles]]:

## Definition

+-- {: .num_defn #QuaternionicOrientedCohomologyTheory}
###### Definition
**(quaternionic oriented cohomology theory)**

A _quaternionic orientation_ $p_1^E$ (a generalized [[first Pontrjagin class]]) in a [[multiplicative cohomology theory|multiplicative]] [[Whitehead generalized cohomology theory]] $E$ is an [[extension]] of the 4-suspended [[ring unit]] in the [[cohomology ring]] $E_\bullet \,\simeq\, E^4\big( H\mathbb{P}^1\big)$ from the [[quaternionic projective space]] $\mathbb{H}P^1$ (the [[4-sphere]]) to $H\mathbb{P}^\infty$:

\[
  \label{QuaternionicOrientationByExtension}
  \array{
    \mathbb{H}P^1 &\overset{\Sigma^4 1}{\longrightarrow}&
    \Omega^{\infty - 4} E
    \\
    \big\downarrow & \nearrow_{ \mathrlap{p_1^E} }
    \\
    H \mathbb{P}^\infty
  }
\]

=--



+-- {: .num_remark #ComplexOrientationByExtensionsAndTheirObstructions}
###### Remark
**(quaternionic $E$-orientation by [[extensions]] and their [[obstructions]])**


In terms of [[Brown representability theorem|classifying maps]], Def. \ref{QuaternionicOrientedCohomologyTheory} means that a quaternionic orientation $p_1^E$ in $E$-cohomology theory is equivalently an [[extension]] (in the [[classical homotopy category]]) of the map $\Sigma^4 1 \,\colon\, \mathbb{H}P^1 \longrightarrow \Omega^{\infty -4} E$ (which classifies the suspended [[ring unit]] in the [[cohomology ring]]) along the canonical inclusion of [[quaternionic projective spaces]] 

\[
  \label{QuaternionicOrientationAsExtension}
  \array{
     \mathbb{H}P^1
     &
     \overset{
       \Sigma^4 1_E
     }{
       \longrightarrow
     }
     &
     \Omega^{\infty - 4} E
     \\
     \big\downarrow
     &
     \nearrow \mathrlap{ {}_{p_1^E} }
     \\
     \mathbb{H}P^\infty
     \,.
  }
\]

Notice that the [[quaternionic projective spaces]] form a [[cotower]]

$$
  \ast 
  \,=\,
  \mathbb{H}P^0
  \hookrightarrow
  \mathbb{H}P^1
  \hookrightarrow
  \mathbb{H}P^2
  \hookrightarrow
  \mathbb{H}P^3
  \hookrightarrow
  \cdots
  \hookrightarrow
  \mathbb{H}P^\infty
  \,=\,
  \underset{\longrightarrow}{\lim}
  \mathbb{H}P^\bullet
$$

where each inclusion stage is (by [this Prop.](complex+projective+space#CellComplexStructureOnComplexProjectiveSpace), see at _[[cell structure of projective spaces]]_) the coprojection of a [[pushout]] [of topological spaces](Top#UniversalConstructions) (or rather: of [[pointed topological spaces]]) of the form

$$
  \array{
    D^{4n+4}
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{H}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(po)}}}&
    \big\uparrow
    \\
    S^{4n+3}
    &\underset{h^{4n+3}_{\mathbb{H}}}{\longrightarrow}&
    \mathbb{H}P^n
  }
$$

(where $h^{4n+3}_{\mathbb{H}}$ is the [[quaternionic Hopf fibration]] in dimension $4n+3$) hence of a [[homotopy pushout]] of [[classical model structure on topological spaces|underlying homotopy types]] (rather: [[classical model structure on pointed topological spaces|of pointed homotopy types]]) of this form:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{H}P^{n+1}
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    \\
    S^{4n+3}
    &\underset{h^{4n+3}_{\mathbb{H}}}{\longrightarrow}&
    \mathbb{H}P^n
  }
$$

Therefore, a quaternionic orientation by extension (eq:QuaternionicOrientationByExtension) is equivalently the homotopy colimiting map of a sequence

$$
  \big(
    \Sigma^4 1 
      \,=\, 
    p_1^{E,0}
    ,\,
    p_1^{E,1}
    ,\,
    p_1^{E,2}
    ,\,
    \cdots
  \big)
$$

of finite-stage extensions

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \mathbb{H}P^{n+1}
    &
    \overset{ p_1^{E,n+1} }{\longrightarrow}
    &
    \Omega^{\infty - 4} E
    \\
    \big\uparrow
    &\mathclap{^{_{(hpo)}}}&
    \big\uparrow
    & 
    \nearrow \mathrlap{ {}_{p_1^{E,n}} }
    \\
    S^{4n+3}
    &\underset{h^{4n+3}_{\mathbb{H}}}{\longrightarrow}&
    \mathbb{H}P^n
    \,.
  }
$$

Moreover, by the defining [[universal property]] of the [[homotopy pushout]], the extension $p_1^{E,n+1}$ of $p_1^{E,n}$ is equivalently a choice of [[homotopy]] which trivializes the pullback of $p_1^{E,n}$ to the [[n-sphere|4n+3-sphere]]:

$$
  \array{
    \ast
    &
    \overset{}{\longrightarrow}
    &
    \Omega^{\infty - 4} E
    \\
    \big\uparrow
    &
    {}_{  p_1^{E,n+1}  }
    \seArrow
    &
    \big\uparrow \mathrlap{ ^{_{ p_1^{E,n} }} }
    \\
    S^{4n+3}
    &\underset{ h^{4n+3}_{\mathbb{H}} }{\longrightarrow}&
    \mathbb{H}P^n
    \,.
  }
$$

This means, first of all, that the non-triviality of the pullback class

$$
  \big( 
    h^{4n+3}_{\mathbb{C}}
  \big)^\ast 
  ( p_1^{E,n} )
  \;\in\;
  \widetilde E^4
  \big(
    S^{4n+3}
  \big)
  \;\simeq\;
  E_{4n - 1}
$$

is the [[obstruction]] to the existence of the extension/orientation at this stage. 

It follows that if these obstructions all vanish, then a quaternionic $E$-orientation does exist.  A sufficient condition for this is, evidently, that the [[reduced cohomology|reduced]] $E$-cohomology of all $(4n-1)$-dimensional spheres vanishes.

=--

Hence:

+-- {: .num_prop #QuaternionicOrientationExistsIf4nMinus1DegreesAreTrivial}
###### Proposition

If $E$ is a [[multiplicative cohomology theory|multiplicative]]
[[Whitehead generalized cohomology theory]] whose [[graded-commutative ring|graded]] [[cohomology ring]] $E_\bullet$ is trivial in degrees $4 n - 1 $, then $E$ admits a quaternionic orientation (Def. \ref{QuaternionicOrientedCohomologyTheory}).

=--

## Examples
 {#Examples}

* [[ordinary cohomology]] has coefficient ring concentrated in degree 0, and hence satisfies the sufficient condition of Prop. \ref{QuaternionicOrientationExistsIf4nMinus1DegreesAreTrivial} to admit quaternionic orientation;

* [[KO-theory]] (orthogonal [[topological K-theory]]) has coefficient ring 

  $$
    KO_n
    \,\simeq\,
    \left\{
    \array{
      \mathbb{Z} &\vert& n = 0 \,mod\, 8
      \\
      \mathbb{Z}_2 &\vert& n = 1 \,mod\, 8
      \\
      \mathbb{Z}_3 &\vert& n = 2 \,mod\, 8
      \\
      0 &\vert& n = 3 \,mod\, 8
      \\
      \mathbb{Z} &\vert& n = 4 \,mod\, 8
      \\
      0 &\vert& n = 5 \,mod\, 8
      \\
      0 &\vert& n = 6 \,mod\, 8
      \\
      0 &\vert& n = 7 \,mod\, 8
    } 
    \right.
    \,,
  $$

  and hence satisfies the sufficient condition of Prop. \ref{QuaternionicOrientationExistsIf4nMinus1DegreesAreTrivial} to admit quaternionic orientation;


  (see also [Laughton 08, Example 2.2.7](#Laughton08))

* Among quaternionic oriented cohomology theories, [[quaternionic cobordism]] is universal in the fashion analogous to the [[universal complex orientation on MU]] ([Laughton 08, Example 2.2.9](#Laughton08))

## Related concepts

* [[MSp]]

## References

* {#Baker92} [[Andrew Baker]], _Some chromatic phenomena in the homotopy of $MSp$_, in: N. Ray, G. Walker (eds.), _Adams Memorial Symposium on Algebraic Topology, Vol. 2_ editors, Cambridge University Press (1992), 263–80 ([pdf](http://www.maths.gla.ac.uk/~ajb/dvi-ps/bpmsp.pdf), [[BakerMSp.pdf:file]])

* {#Laughton08} [[Craig Laughton]], Example 2.2.5 in: _Quasitoric manifolds and cobordism theory_, Manchester 2008 ([pdf](http://www.ma.man.ac.uk/~nige/craiglphd.pdf), [[LaughtonQuasitoric.pdf:file]])

* [[Ivan Panin]], [[Charles Walter]], _Quaternionic Grassmannians and Pontryagin classes in algebraic geometry_, 2010 ([hal:00531725](https://hal.archives-ouvertes.fr/hal-00531725), [pdf](https://www.math.uni-bielefeld.de/LAG/man/405.pdf))

* [[Ivan Panin]], [[Charles Walter]], _Quaternionic Grassmannians and Borel classes in algebraic geometry_ ([arXiv:1011.0649](https://arxiv.org/abs/1011.0649))

* [[Ivan Panin]], [[Charles Walter]], _On the algebraic cobordism spectra $MSL$ and $MSp$_ ([arXiv:1011.0651](https://arxiv.org/abs/1011.0651))


* [[Ivan Panin]], _[Oriented theories and symplectic cobordism](https://www.esaga.uni-due.de/marc.levine/SpecialSemester/Panin/)_, Seminar 

[[!redirects quaternionic oriented cohomology theories]]

[[!redirects quaternionic oriented cohomology]]

