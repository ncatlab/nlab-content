
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In the context of [[classical mechanics]], a _classical anomaly_ is a  [[central extension]] of a [[Noether current]] algebra (e.g. [Toppan 01](#Toppan01)).

## Definition

In terms of [[symplectic geometry]] this means the following ([Arnold 78, appendix 5.A](#Arnold78)). Given a [[Lie group]] $G$ acting by [[symplectomorphisms]] on a [[phase space]] [[symplectic manifold]] $(X,\omega)$, this [[symmetry]] has a _classical anomaly_ if it does not lift to a genuine $G$-[[Hamiltonian action]], but only to a [[projective representation|projective]] $G$-[[Hamiltonian action]], hence to a [[Hamiltonian action]] of a [[central extension]] $\widehat G$ of $G$. Specifically, the _classical anomaly_ of the original symplectic $G$-action is the 2-[[cocycle]] which classifies this extension.

If the original $G$-action is by [[flows]] of  [[Hamiltonian vector fields]] (just not with explicitly chosen [[Hamiltonians]]), then there is a  universal classical anomaly given by the [[pullback]] of the [[quantomorphism group]] [[extension]] 

$$
  \array{
     \widehat G &\longrightarrow& QuantMorph(X,\omega)
     \\
     \downarrow &(pb)& \downarrow
     \\
    G &\stackrel{}{\longrightarrow}& HamSympl(X,\omega) 
  }
  \,.
$$

This $\widehat G$ is the [[Heisenberg group]] of the given $G$-action (See also [Fiorenza-Rogers-Schreiber 13](#FiorenzaRogersSchreiber13) for discussion in [[higher prequantum geometry]]).

Notice that on the infinitesimal level of [[Lie algebras]], using that the Lie algebra of the [[quantomorphism group]] is the [[Poisson Lie algebra]] $\mathfrak{pois}(X,\omega)$, this means that an infinitesimal action of a Lie algebra $\mathfrak{g}$ via [[Hamiltonian vector fields]] on $X$ has a classical anomaly if it lifts to an action with consistently chosen [[Hamiltonians]] -- also called a [[moment map]] -- only after passing to a central [[Lie algebra extension]]

$$
  \array{
     \widehat \mathfrak{g} &\longrightarrow& \mathfrak{pois}(X,\omega)
     \\
     \downarrow && \downarrow
     \\
     \mathfrak{g} &\stackrel{}{\longrightarrow}& \Gamma(T X)_{\omega}
  }
  \,.
$$


## Examples

### Mass-anomaly of Galilean action on non-relativistic mechanics
 {#GalileoAnomaly}

The canonical [[Galileo group]]-[[action]] on the [[phase space]] of non-relativistic [[classical mechanics]] has a classical anomaly, given by a [[group cohomology|group 2-cocycle]] proportional to the [[mass]] of the system, the _[[Galileo 2-cocycle]]_ (e.g. [Chen-Shaw-Yen 85](#ChenShawYen85), [Azc&#225;rraga-Izquierdo 95](#AzcarragaIzquierdo95) [Marle 14](#Marle14)).

## Related concepts

* [[quantum anomaly]]

* [[fiber bundles in physics]]

[[!include geometric quantization extensions - table]]

## References

A textbook discussion of the concept is (without the terminology yet) is in appendix 5.A of 

* [[Vladimir Arnol'd]], _[[Mathematical methods of classical mechanics]]_, Graduate texts in Mathematics 60 (1978)
 {#Arnold78}

A discussion under the term "classical [[central charge]]" is in 

* J. D. Brown, [[Marc Henneaux]], _Central charges in the canonical realization of asymptotic symmetries: An example from three-dimensional gravity_, Commun. Math. Phys. 104 (1986) 207. ([web](http://dx.doi.org/10.1007/BF01211590))

For a list of some examples and further pointers to the (historical) literature, see

* {#Toppan01} Francesco Toppan, _On anomalies in classical mechanical systems_, Journal of Nonlinear Mathematical Physics Volume 8, Number 3 (2001), 518&#8211;533  ([[ToppanClassicalAnomaly.pdf:file]])
 

See also

* [[Glenn Barnich]], C&#233;dric Troessaert, _Comments on holographic current algebras and asymptotically flat four dimensional spacetimes at null infinity_ ([arXiv:1309.0794](http://arxiv.org/abs/1309.0794))

Discussion in terms of [[Heisenberg group]] [[group extensions|extensions]] and generalization to [[higher symplectic geometry]] is in 

* {#FiorenzaRogersSchreiber13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_ ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  
Discussion in the context of formalization of [[classical field theory]] in [[cohesive homotopy theory]] is in 

* [[Urs Schreiber]], section 2.14 of _[[schreiber:Classical field theory via Cohesive homotopy types]]_ ([pdf](https://dl.dropboxusercontent.com/u/12630719/classicalinhigher.pdf))

The example of the [[Galileo 2-cocycle]] is discussed for instance in 

* {#ChenShawYen85} Chen, Shaw, Yen, _An example of a 2-cocycle_, [pdf](http://psroc.phys.ntu.edu.tw/cjp/v23/4.pdf)

* {#Marle14} Charles-Michel Marle, _The manifold of Motions and the total mass of a mechanical system_, 2014 ([pdf](http://charles-michel.marle.pagesperso-orange.fr/diaporamas/ManifoldMotionsMass.pdf))

and in the broader context of [[WZW model]] terms in 

* {#AzcarragaIzquierdo95} [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 8.3 of _Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics_ , Cambridge monographs of mathematical physics, (1995)

following 

* [[José de Azcárraga]], _Wess-Zumino terms, extended algebras and anomalies in classical physics_, Contemp.Math. 132 (1992) 75-98 ([spire](https://inspirehep.net/record/320052?ln=de))


[[!redirects classical anomalies]]

[[!redirects Galileo 2-cocycle]]