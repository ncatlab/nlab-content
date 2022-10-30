
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Integration theory
+-- {: .hide}
[[!include integration theory - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Here we discuss the [[integration]] of a [[differential form]] (possibly twisted in some way) on a [[topological manifold]] (possibly with additional structure) over an appropriately structured [[submanifold]] (or [[formal linear combination]] thereof).


## Description
 {#Description}

See at _[[differential form]]_ for basic definitions.


### Integration of top-dimension pseudoforms (pseudoforms to measures)

Let $X$ be an $n$-dimensional [[topological manifold]], and let $\omega$ be a [[continuous map|continuous]] $n$-pseudoform on $X$.  Suppose that $X$ is [[paracompact space|paracompact]] and [[Hausdorff space|Hausdorff]], so that we may find a [[locally finite cover]] of $X$ with a subordinate [[partition of unity]] and a continuous coordinate chart on each patch.  (When $X$ is [[differentiable manifold|differentiable]], or even [[smooth manifold|smooth]], then these may also be chosen to be differentiable or smooth, which may be convenient but is not necessary.)  Then $\omega$ defines a [[measure space|measure]] on $X$ as follows:

*  On each coordinate patch $U$, fix the orientation given by the coordinates to turn $\omega$ into an untwisted $n$-form $\hat{\omega}$; then write $\hat{\omega}$ in coordinates as
   $$ \hat{\omega} = \omega_U \wedge \mathrm{d}x^1 \wedge \cdots \wedge \mathrm{d}x^n .$$
   In this situation, it is convenient also to write
   $$ \omega = \omega_U \mathrm{d}x^1 \cdots \mathrm{d}x^n ;$$
   in other words, we interpret $\mathrm{d}x^1 \cdots \mathrm{d}x^n$ as the absolute value of $\mathrm{d}x^1 \wedge \cdots \wedge \mathrm{d}x^n$.

*  The coordinates on $U$ define a [[diffeomorphism]] between $U$ and an open subset of $\mathbf{R}^n$ that we\'ll also call $U$; so use the latter formula to interpret
   \[ \label{absvalposs} \int_U \omega = \int_U \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n ,\]
   where the right-hand side is now interpreted in the usual way as as integral with respect to [[Lebesgue measure]].

*  Using the partition of unity, write
   $$ \omega = \sum_U w_U \omega_U ,$$
   where $w_U$ is a weight function defined on $U$ and $\omega_U$ is the [[restriction]] of $\omega$ to $U$.
   Then we have
   $$ \int_X \omega = \sum_U \int_U w_U(x^1,\ldots,x^n) \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n ,$$
   or more generally,
   $$ \int_E \omega = \sum_U \int_U \chi_E(x^1,\ldots,x^n) w_U(x^1,\ldots,x^n) \omega_U(x^1,\ldots,x^n)\, \mathrm{d}x^1 \cdots \mathrm{d}x^n $$
   for $E$ a measurable subset of $X$ and $\chi_E$ the [[characteristic function]] of $E$.

_A priori_, this definition depends not only on the particular coordinate patches chosen but also on the partition of unity chosen to go with them.  Furthermore, the defintion could be done just as easily (perhaps even more easily) for something other than an $n$-pseudoform.  But the (perhaps surprising) fact that justifies it all is this:

+-- {: .num_theorem #IntegrationTheorem}
###### Theorem
When $\omega$ is an $n$-pseudoform, the definition of $\int_E \omega$ is independent of the coordinates and partition chosen.  Furthermore, the map from $n$-pseudoforms to measures is linear.
=--

Note that, if $\omega$ were an $n$-form instead of a pseudoform, then the definition would depend on the orientation of the coordinates chosen.  We could fix that by using the absolute value ${|\omega_U|}$ in place of $\omega_U$ in (eq:absvalposs) and the following equations, but then the map from forms to measures would not be linear.


### Measures to pseudoforms

It may also be enlightening to consider how to go back from a measure to an $n$-pseudoform.  If $\omega$ is an [[absolutely continuous measure|absolutely continuous]] [[Radon measure]] on $X$, then it defines an $n$-pseudoform (which we may also call $\omega$) as follows:

*  Given a point $a$, choose one of the two local orientations at $a$.
*  Given $n$ linearly independent vectors $(v_1,\ldots,v_n)$ at $a$, develop them into a coordinate system on a neighbourhood $U$ of $a$.
*  For sufficiently large natural number $k$, the coordinate cube $C_k$ of points with coordinates in $[0,1/k]^n$ exists (lies within $U$).
*  Let $L$ be $\lim_{k \to \infty} k^n \omega(C_k)$.
*  If the coordinate system on $U$ is positively oriented at $a$, then let $\omega(v_1,\ldots,v_n)$ be $L$; if the coordinate system on $U$ is negatively oriented at $a$, then let $\omega(v_1,\ldots,v_n)$ be $-L$.
*  Extend the definition to $n$ arbitrary vectors by continuity (which necessarily maps a linearly dependent tuple of vectors to zero).

Again, this definition is independent of the coordinate system chosen (as long as it extends the given vectors); or if that\'s not true, then we messed up and need to add further restrictions to the absolutely continuous Radon measure $\omega$.  The definition is *not* independent of the orientation chosen, of course; thus we get a pseudoform rather than an untwisted form.  You might try to ignore the orientation and take $\omega(v_1,\ldots,v_n)$ to be $L$ always, but that does not define an exterior form, as is most easily seen if two vectors are switched (which does not change $L$).  Instead, this would define an [[absolute differential form]] (which is equivalent to a pseudoform when, as here, the degree equals the dimension).


### Integration of more general forms

One can integrate forms other than $n$-pseudoforms, of course, but only over certain structures within the manifold $X$.  Specifically, if $R$ is a $p$-dimensional [[submanifold]] of $X$ (that is a $p$-dimensional manifold $U$ equipped with a map $R\colon U \to X$), then we would like to integrate $p$-forms or $p$-pseudoforms (defined on $X$) over $R$.  Here is how we do this:

*  We may integrate a $p$-form $\eta$ over $R$ if $R$ is _oriented_, that is if $U$ is oriented.  We pull back $\eta$ from $X$ to $U$, then use the orientation on $U$ to turn $\eta$ into a $p$-pseudoform, which we can then integrate on the $p$-dimensional manifold $U$.

*  We may integrate a $p$-pseudoform $\eta$ over $R$ if $R$ is _pseudooriented_, that is if it is equipped with a map that, for each point $a$ on $U$, takes a local orientation of $X$ at $R(a)$ to a local orientation of $U$ at $a$, continuously in $a$ and taking opposite orientations to opposite orientations.  Then locally, we turn $\eta$ into a $p$-form on $X$ using a local orientation on $X$, pull that back to $U$, and use the corresponding local orientation on $U$ to turn that back into a $p$-pseudoform, which we can then integrate on $U$.

Thus, while integration of $n$-pseudoforms is the most basic, integration of general $p$-forms is actually a bit simpler than integration of general $p$-pseudoforms.  Integration of other twisted or vector-valued forms can also be done, again given appropriate structure on $R$.

Note that, if $X$ is thought of a submanifold of itself, then it has a natural pseudoorientation that takes each local orientation to itself, and so we recover the original definition of integration of $n$-pseudoforms on $X$.  Also, if $X$ is an oriented manifold, then it may be viewed as an oriented submanifold of itself, giving a definition of integration of $n$-forms on $X$.

To integrate on *unoriented* submanifolds of arbitrary dimension, use [[absolute differential forms]].


### Integration on more general domains

One often sees the definition of integration given for *parametrised* submanifolds, that is submanifolds where $U$ is an open subset of $\mathbf{R}^p$.  This amounts to a combination of the concepts above, with the two uses of $U$ (as a coordinate patch in $X$ or as the source of a submanifold of $X$) identified.  The theorem that the integral of an $n$-pseudoform on $X$ is independent of the coordinates chosen now becomes a theorem that the integral of a parametrised submanifold is independent of the parametrisation (up to some details about orientation), which in the end returns the result that one can integrate forms over arbitrary submanifolds (given an orientation or pseudoorientation as above).

We can also integrate on a [[formal linear combination]] of submanifolds, which is handy since these are the [[chains]] of [[de Rham homology]].  This is straightforward:
$$ \int_{\sum_i \alpha_i U_i} \omega \coloneqq \sum_i \alpha_i \int_{U_i} \omega .$$

## In cohesive homotopy-type theory
 {#InCohesiveHomotopyTypeTheory}

We discuss here a general abstract formulation of differential forms, their integration and the [[Stokes theorem]] in the axiomatics of [[cohesive homotopy type theory]] (following [Bunke-Nikolaus-V&#246;lkl 13, theorem 3.2](#BunkeNikolausVoelkl13)).

### General definition

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] and write $T \mathbf{H}$ for its [[tangent cohesive (∞,1)-topos]].

Assume that there is an [[interval object]] 

$$
  \ast \cup \ast \stackrel{(i_0, i_1)}{\longrightarrow}  \Delta^1
$$ 

"exhibiting the cohesion" (see at _[[continuum]]_) in that there is a (chosen) [[equivalence]] between the [[shape modality]] $\Pi$ and the [[localization of an (∞,1)-category|localization]] $L_{\Delta^1}$ at the the [[projection]] maps out of [[Cartesian products]] with this line $\Delta^1\times (-) \to (-)$

$$
  \Pi \simeq L_{\Delta^1}
  \,.
$$ 

This is the case for instance for the "standard [[continuum]]", the [[real line]] in $\mathbf{H} = $ [[Smooth∞Grpd]].

It follows in particular that there is a chosen [[equivalence of (∞,1)-categories]] 

$$
  \flat(\mathbf{H})\simeq L_{\Delta^1}\mathbf{H}
$$

between the [[flat modality|flat]] [[modal types|modal homotopy-types]] and the $\Delta^1$-homotopy invariant homotopy-types.

Given a [[stable homotopy type]] $\hat E \in Stab(\mathbf{H})\hookrightarrow T \mathbf{H}$ [[cohesion]] provides two objects 

$$
  \Pi_{dR} \Omega \hat E \,,\;\;  \flat_{dR}\Sigma \hat E
  \;\;
  \in Stab(\mathbf{H})
$$

which may be interpreted as [[de Rham complexes]] with [[coefficients]] in $\Pi(\flat_{dR} \Sigma \hat E)$, the first one restricted to negative degree, the second to non-negative degree. Moreover, there is a canonical map

$$
  \array{
    \Pi_{dR}\Omega \hat E && \stackrel{\mathbf{d}}{\longrightarrow} && \flat_{dR}\Sigma \hat E
    \\
    & {}_{\mathllap{\iota}}\searrow && \nearrow_{\mathrlap{\theta_{\hat E}}}
    \\
    && 
    \hat E
  }
$$

which interprets as the [[de Rham differential]] $\mathbf{d}$. See at _[[differential cohomology diagram]]_ for details. 

Throughout in the following we leave the "inclusion" $\iota$ of "differential forms regarded as $\hat E$-connections on trivial $E$-bundles" implicit.

+-- {: .num_defn #CohesiveIntegrationOfDifferentialForms}
###### Definition

Integration of differential forms is the map

$$
  \int_{\Delta^1} \;\colon\;  [\Delta^1, \flat_{dR}\Sigma \hat E] \longrightarrow \Pi_{dR}\Omega \hat E
$$

which is induced via the [[homotopy cofiber]] property of $\flat_{dR}\Omega \hat E$ from the [[counit of a comonad|counit]] naturality square of the [[flat modality]] on $[(\ast \coprod \ast \stackrel{(i_0, i_1)}{\to} \Delta ^1 ), -]$, using that this square exhibits a [[null homotopy]] due to the $\Delta^1$-homotopy invariance of $\flat \hat E$.

=--

+-- {: .num_prop}
###### Proposition

The [[Stokes theorem]] holds:

$$
  \int_0^1 \circ \mathbf{d} \simeq i_1^\ast - i_0^\ast
  \,.
$$

=--

([Bunke-Nikolaus-V&#246;lkl 13, theorem 3.2](#BunkeNikolausVoelkl13)

### Recovering traditional integration of differential forms


+-- {: .num_prop}
###### Proposition

In $\mathbf{H} = $ [[Smooth∞Grpd]] let $\hat E \in Stab(\mathbf{H})$ be given, under the [[stable Dold-Kan correspondence]], by the traditional truncated [[de Rham complex]] $\hat E \coloneqq \Omega^{\bullet \geq n }$.

Then on this object the general cohesive integration map of def. \ref{CohesiveIntegrationOfDifferentialForms} reduces on the $-n$th [[homotopy group]] to the tradition [[fiber integration]] of differential forms as [above](#Description):

$$
  \int_{(\Delta^1 \times X)/X} 
  \;\colon\;
  \Omega(\Delta^1 \times X)_{cl}^n
  \longrightarrow
  \Omega^{n-1}(X)/im(\mathbf{d})
  \,.
$$

=--

([Bunke-Nikolaus-V&#246;lkl 13, lemma 4.2 (7)](#BunkeNikolausVoelkl13)


## Properties

* _[[Stokes theorem]]_


## Related concepts

* [[Lie integration]]

* [[cohomological integration]]

* [[iterated integral]], [[parallel transport]], [[holonomy]]

## References

An exposition with an eye towards applications in [[physics]] is section 3 of 

* [[Theodore Frankel]], _[[The Geometry of Physics - An Introduction]]_

Discussion in the abstract context of [[cohesion]] and [[differential cohomology]] is in 

* {#BunkeNikolausVoelkl13} [[Ulrich Bunke]], [[Thomas Nikolaus]], [[Michael Völkl]], _Differential cohomology theories as sheaves of spectra_ ([arXiv:1311.3188](http://arxiv.org/abs/1311.3188))