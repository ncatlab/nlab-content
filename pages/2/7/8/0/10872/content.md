
#Contents#
* table of contents
{:toc}

## Idea

In [[quantum field theory]] a _conformal anomaly_ is a [[quantum anomaly]] that breaks [[conformal invariance]].


## Examples

### Weyl anomaly of relativistic string

Discussion of the conformal anomaly (Weyl anomaly) of the [[relativistic string]] as an anomalous action functional is in ([Freed 86, 2.](#Freed86)).
The following summary of this is taken from [this MO answer](http://mathoverflow.net/a/99667/381) by Pavel Safranov.


Let $\Sigma$ be a compact surface (worldsheet) and $M$ a Riemannian manifold (spacetime). The string partition function looks like
$$Z_{string}=\int_{g\in Met(\Sigma)}dg\int_{\sigma\in Map(\Sigma,M)}d\sigma\exp(iS(g,\sigma)).$$
Here $Met(\Sigma)$ is the space of Riemannian metrics on $\Sigma$ and $S(g,\sigma)$ is the standard $\sigma$-model action $S(g,\sigma)=\int_{\Sigma} dvol_\Sigma \langle d\sigma,d\sigma\rangle$. In particular, $S$ is quadratic in $\sigma$, so the second integral $Z_{matter}$ does not pose any difficulty and one can write it in terms of the determinant of the Laplace operator on $\Sigma$. Note that the determinant of the Laplace operator is a section of the determinant line bundle $L_{det}\rightarrow Met(\Sigma)$. The measure $dg$ is a 'section' of the bundle of top forms $L_g\rightarrow Met(\Sigma)$. Both line bundles carry natural connections.

However, the space $Met(\Sigma)$ is enormous: for example, it has a free action by the group of rescalings $Weyl(\Sigma)$ ($g\mapsto \phi g$ for $\phi\in Weyl(\Sigma)$ a positive function). It also carries an action of the diffeomorphism group. The quotient $\mathcal{M}$ of $Met(\Sigma)$ by the action of both groups is finite-dimensional, it is the moduli space of conformal (or complex) structures, so you would like to rewrite $Z_{string}$ as an integral over $\mathcal{M}$.

Everything in sight is diffeomorphism-invariant, so the only question is how does the integrand change under $Weyl(\Sigma)$. To descend the integral from $Met(\Sigma)$ to $Met(\Sigma)/Weyl(\Sigma)$ you need to trivialize the bundle $L_{det}\otimes L_g$ along the orbits of $Weyl(\Sigma)$. This is where the critical dimension comes in: the curvature of the natural connection on $L_{det}\otimes L_g$ (local anomaly) vanishes precisely when $d=26$. After that one also needs to check that the connection is actually flat along the orbits, so that you can indeed trivialize it.

### QCD trace anomaly

In [[quantum chromodynamics]]: See at _[[QCD trace anomaly]]_.

## Related concepts

* [[gravitational anomaly]]

* [[Liouville cocycle]]

## References

### General

* {#Freed86} [[Daniel Freed]], _Determinants, torsion, and strings_,  Comm. Math. Phys. Volume 107, Number 3 (1986), 483-513. ([Euclid](http://projecteuclid.org/euclid.cmp/1104116145))
  

* Nicolas Boulanger, _Algebraic Classification of Weyl Anomalies in Arbitrary Dimensions_, Phys. Rev. Lett.98:261302, 2007 ([arXiv:0706.0340](https://arxiv.org/abs/0706.0340))

* Markus B. Fröb, Jochen Zahn: *The Weyl anomaly in interacting quantum field theory on curved spacetimes* &lbrack;[arXiv:2504.17854](https://arxiv.org/abs/2504.17854)&rbrack;


See also:

* Wikipedia, _[Conformal anomaly](http://en.wikipedia.org/wiki/Conformal_anomaly)_

### Via AdS/CFT

Discussion via [[AdS/CFT]]:

* Mans Henningson, Kostas Skenderis, _The Holographic Weyl anomaly_, JHEP 9807 (1998) 023 ([arXiv:hep-th/9806087](https://arxiv.org/abs/hep-th/9806087))

* Mozhgan Mir, _On Holographic Weyl Anomaly_, JHEP 1310:084, 2013 ([arXiv:1307.5514](https://arxiv.org/abs/1307.5514))

For more see at _[[QCD trace anomaly]]_ the references [there](QCD+trace+anomaly#ReferencesHolographicQCD).


[[!redirects conformal anomalies]]

[[!redirects Weyl anomaly]]
[[!redirects Weyl anomalies]]