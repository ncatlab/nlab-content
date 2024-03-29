
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _EHP spectral sequence_ (we follow [Mahowald 85](#Mahowald85)) is the [[spectral sequence]] for computation of [[homotopy groups of spheres]] induced from the [[filtration]] of the underlying homotopy type $\Omega^\infty \Sigma^\infty S^0 = \Omega^\infty \mathbb{S}$  of the [[sphere spectrum]]  by [[suspensions]] (German: _E_inh&#228;ngung):

$$
  \Omega^n S^n \stackrel{E}{\longrightarrow} \Omega^{n+1} S^{n+1}
  \,.
$$

More concretely, ([James 57](#James57)) constructed maps

$$
  \Omega S^n \stackrel{H}{\longrightarrow} \Omega S^{2n-1}
$$

(for _H_opf as in [[Hopf invariant]]) and showed that  [[p-localization|2-locally]] these fit with $E$ into [[homotopy fiber sequences]] 

$$
  \Omega^{n+2} S^{2n+1} 
    \stackrel{P}{\longrightarrow}
  \Omega^n S^n 
    \stackrel{E}{\longrightarrow} 
  \Omega^{n+1} S^{n+1}
    \stackrel{H}{\longrightarrow}
  \Omega^{n+1}S^{2n+1}
  \,.
$$

(Here $P$ is by definition the [[homotopy fiber]] of $E$, the notation refers to _[[Whitehead product]]_.)

This "EHP-[[long homotopy fiber sequence]]" gives rise to the corresponding [[long exact sequence of homotopy groups]] and so to an [[exact couple]] of the form

$$
  \array{
     \underset{s,t}{\oplus} \pi_{s+t}(\Omega^{s+1}S^{s+1})
     && \stackrel{i}{\longrightarrow} &&
     \pi_{s+t}(\Omega^{s+1}S^{s+1})
     \\
     & \nwarrow && \swarrow
     \\
     &&
     \underset{s,t}{\oplus} 
     \pi_{t+s}(\Omega^{s+1}S^{2s+1})
  }
  \,.
$$

The corresponding [[spectral sequence]] is the EHP spectral sequence proper. It converges, 2-locally, to the [[stable homotopy groups of spheres]], with $E_1$-page given by

$$
  E^{k,n}_1 = \pi_{k+n}(S^{2n-1}) \;\Rightarrow\; \pi_\bullet^{\mathbb{S}}
  \,.
$$

For more general [[prime numbers]] than just 2, ([Toda 62](#Toda62)) found analogous fibrations, which hence give EHP spectral sequences for general $p$.


The EHP spectral sequence is often used used in the context of the [[Adams-Novikov spectral sequence]] for [[p-localization]] at some prime $p$.

## Constructions of $H$

For James' fiber sequence, the essential property required of $H$ is to realize the isomorphism
$$ (the\:map\:H)^{cohomology\:pullback} : H^{2n}(\Omega\mathbb{S}^{2n+1})\overset{\sim}{\to} H^{2n}(\Omega \mathbb{S}^{n+1}) .$$
The remaining corollaries then follow using the fact cohomology pullback is a ring homomorphism, and the $mod 2$ [[Leray-Serre spectral sequence]].

### Via the James model

Using the James model of $\Omega\Sigma X$ as a quotient space of $colim_n X^n $, a candidate $H$ is constructed by recursion:
$$ H([x_0 , \dots, x_{n+1}]) = H([x_0,\dots,x_n]) \# ([x_0 \wedge x_{n+1} , \dots , x_n\wedge x_{n+1}]) $$
where $\#$ denotes concatenation and $\wedge$ [[smash product]].  One checks that the ordering of product terms $ x_i\wedge x_j $ w.r.t. $x_k\wedge x_l$ depends only on the relative orders of $i,j,k,l$, so that $H$ is well-defined on the quotient space $\Omega\Sigma X \to \Omega \Sigma(X\wedge X)$.

In particular, the restriction to $J_2 X$ factors through $ X\wedge X \to \Omega\Sigma X\wedge X$ as the cofiber of the inclusion $X \to J_2 X$.  In the case $X\simeq \mathbb{S}^n$, the desired cohomology isomorphism is immediate.

### Via pushout/pullback comparisons

Starting with the three-legged cospan $ X \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}} * $, construct the cube of all pushouts
$$
 \array{
   X    &    &              & \to &       &     &    * \\
    & \searrow &             &   &     & \swarrow \\
            &       &   *   & \to &   \Sigma X \\
  \downarrow & & \downarrow &     & \downarrow & & \downarrow \\
            &    & \Sigma X & \to & \Sigma X \vee \Sigma X \\
         & \nearrow  & &     &   &       \nwarrow \\
   *       &      &         & \to &       &      & \Sigma X 
 } 
$$
Construct pullbacks in some pair of parallel squares, and compare them by naturality
$$
 \array{
   \Omega\Sigma X &   &           & \to &           &           & * \\
        & \searrow &           &     &           & \swarrow \\
        &   & \Omega((\Omega\Sigma X)\star(\Omega\Sigma X)) & \to & \Sigma X \\
   \downarrow   &    & \downarrow &     & \downarrow &        & \downarrow \\
             &       & \Sigma X   & \to & \Sigma X \vee \Sigma X \\
             & \nearrow &         &     &               & \nwarrow \\
       *     &          &         & \to &            &          & \Sigma X 
 } 
$$
where $\star$ is [[join|reduced join]]. On the other hand, the natural transformations $ \Sigma\Omega \to 1$ give natural maps, e.g. 
$$\Omega( ev \circ \tau \circ ev ) : \Omega((\Omega\Sigma X) \star (\Omega\Sigma X)) \to \Omega( X \star X) .$$
The composite
$$ \Omega \Sigma X \to \Omega((\Omega\Sigma X)\star(\Omega\Sigma X)) \to \Omega(X\star X) $$
is a candidate $H$.

## Related concepts

* the [[Freudenthal suspension theorem]] may be obtained from the EHP spectral sequence;

* the [[Goodwillie spectral sequence]] of the identity functor at the point also computes homotopy groups of spheres, the interplay of the two is discussed in ([Behrens 10](#Behrens10))

## References

Original articles include

* [[Ioan Mackenzie James]], _Reduced product spaces_, Ann. of Math. (2) 62 (1955), 170-197.

* {#James57} [[Ioan Mackenzie James]], _On the Suspension Sequence_, Annals of Mathematics Second Series, Vol. 65, No. 1 (Jan., 1957), pp. 74-107 ([jstor](http://www.jstor.org/stable/1969666))

* {#Toda62} [[Hiroshi Toda]], _Composition methods in homotopy groups of spheres_, Princeton University Press (1962)

* {#Mahowald85} [[Mark Mahowald]], _Lin's theorem and the EHP sequence_. Conference on algebraic topology in honor of [[Peter Hilton]], Contemp. Math. 37 (1985), 115&#8211;119. Amer. Math. Soc., Providence, RI.

* [[Marcel Bökstedt]], [[Anne Marie Svane]], _A generalization of the stable EHP spectral sequence_ ([arXiv:1208.3938](http://arxiv.org/abs/1208.3938))

Relation to the [[Goodwillie spectral sequence]] is discussed in

* {#Behrens10} [[Mark Behrens]], _The Goodwillie tower and the EHP sequence_ ([arXiv:1009.1125](http://arxiv.org/abs/1009.1125))

An algebraic version of the EHP spectral sequence for the [[Lambda-algebra]] and used for computation of the second page of the [[classical Adams spectral sequence]] (the _[[Curtis algorithm]]_), is discussed in 

* {#Kochmann96} [[Stanley Kochman]], around prop. 5.2.6  of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996


Review:

* [[Michael Hopkins]] (notes by [[Akhil Mathew]]), Lectures 6,7 in: _Spectra and stable homotopy theory_, 2012 ([pdf](http://math.uchicago.edu/~amathew/256y.pdf), [[HopkinsMathewStableHomotopyTheory.pdf:file]])


* [[Mark Mahowald]], [[Doug Ravenel]], section 7 of _Towards  a Global Understanding of the Homotopy Groups of Spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf))

* [[Doug Ravenel]], chapter 1, section 5 of _[[Complex cobordism and stable homotopy groups of spheres]]_

* [[eom]], _[EHP spectral sequence](https://www.encyclopediaofmath.org/index.php/EHP_spectral_sequence)_

See also:
 
* Wikipedia, _[EHP spectral sequence](http://en.wikipedia.org/wiki/EHP_spectral_sequence)_


