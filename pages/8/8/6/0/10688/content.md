
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

## Related concepts

* the [[Freudenthal suspension theorem]] may be obtained from the EHP spectral sequence;

## References

Original articles include

* I. M. James, _Reduced product spaces_, Ann. of Math. (2) 62 (1955), 170-197.

* {#James57} I. M. James, _On the Suspension Sequence_, Annals of Mathematics Second Series, Vol. 65, No. 1 (Jan., 1957), pp. 74-107 ([jstor](http://www.jstor.org/stable/1969666))

* {#Toda62} [[Hiroshi Toda]], _Composition methods in homotopy groups of spheres_, Princeton University Press (1962)

* {#Mahowald85} [[Mark Mahowald]], _Lin's theorem and the EHP sequence_. Conference on algebraic
topology in honor of Peter Hilton, Contemp. Math. 37 (1985), 115&#8211;119. Amer.
Math. Soc., Providence, RI.

* [[Marcel Bökstedt]], Anne Marie Svane, _A generalization of the stable EHP spectral sequence_ ([arXiv:1208.3938](http://arxiv.org/abs/1208.3938))

Relation to the [[Goodwillie spectral sequence]] is discussed in

* {#Behrens10} [[Mark Behrens]], _The Goodwillie tower and the EHP sequence_ ([arXiv:1009.1125](http://arxiv.org/abs/1009.1125))

Review includes 

* [[Mark Mahowald]], [[Doug Ravenel]], section 7 of _Towards  a Global Understanding of the Homotopy Groups of Spheres_ ([pdf](http://www.math.rochester.edu/people/faculty/doug/mypapers/global.pdf))

* [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_

* [[eom]], _[EHP spectral sequence](https://www.encyclopediaofmath.org/index.php/EHP_spectral_sequence)_
 
* Wikipedia, _[EHP spectral sequence](http://en.wikipedia.org/wiki/EHP_spectral_sequence)_



