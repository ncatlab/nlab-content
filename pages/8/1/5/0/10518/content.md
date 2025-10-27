
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Wess-Zumino-Witten theory
+--{: .hide}
[[!include infinity-Wess-Zumino-Witten theory - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea
 {#Idea}

Where a _[[WZW model]]_ is a [[sigma model]] [[quantum field theory]] whose [[target space]] is a [[group]] $G$, a _parameterization_ of such a model is a sigma-model (subject usually to some constraints) whose target space now is the total space of a $G$-[[principal bundle]] such that the [[action functional]] when restricted to fields that take values only in any one [[fiber]], reduces to the given un-parameterized model.

Parameterized WZW models have been argued to provide a more geometric and more complete description of the [[current algebra]]-sector of [[heterotic string]] backgrounds than the traditional construction in terms of worldsheet fermions  ([Gates-Siegel 88](#GatesSiegel88), [Gates-Ketov-Kozenko-Solovev 91](#GKKS91), [Distler-Sharpe 10, section 7](#DistlerSharpe10)). In particular the [[Green-Schwarz anomaly]] of the heterotic string finds a natural interpretation as the [[obstruction]] to parameterizing the given WZW term over the given principal bundle:


A ([[schreiber:∞-Wess-Zumino-Witten theory|higher]]) [[WZW model]] is an $n$-dimensional [[sigma-model]] [[field theory]] whose [[target space]] is a [[group]] $G$ and whose [[interaction]]-part of the [[action functional]] is the [[higher holonomy]] of a [[circle n-bundle with connection]] 

$$
  \mathbf{L}_{WZW}
  \;\colon\;
  G \longrightarrow 
  \mathbf{B}^n U(1)_{conn}
$$

(whose [[curvature]] is given by the global [[Maurer-Cartan form]] on $G$).


If one has a $G$-[[principal bundle]] 

$$
  \array{
    G &\hookrightarrow& X
    \\
    && \downarrow
    \\
    && B
  }
$$

over some base space $B$, then a [[lift of the structure group]] to the [[Heisenberg n-group]] $Heis_G(\mathbf{L}_{WZW})$ of $\mathbf{L}_{WZW}$ regarded as a [[prequantum n-bundle]], is the structure necessary and sufficient for the [[fiber]]-wise copies of $G$ and $\mathbf{L}_{WZW}$ glue fiberwise to a single [[circle n-bundle with connection]] 

$$
  \mathbf{L}_{WZW}^X \;\colon\; X \longrightarrow \mathbf{B}^n U(1)_{conn}
$$

on the total space $X$ of this bundle. This hence yields what one may think of as a coherent collection of [[WZW models]] _parameterized_ over base space $B$.

For the case that $G$ is a [[compact Lie group|compact]] [[semisimple Lie group]] and $\mathbf{L}_{WZW}$ its canonical WZW term (the [[circle n-bundle with connection|2-connection]] on the [[string 2-group]]), then 

$$
  Heis_G(\mathbf{L}_{WZW})\simeq String(G)
$$

and hence the [[obstruction]] to the existence of a parameterization is precisely a [[string structure]], recovering the traditional statement of the [[Green-Schwarz anomaly]] (see [cwzw](#cwzw) for details of this claim).




## Examples

### The heterotic string

The [[heterotic string]] [[worldsheet]] [[theory (physics)|theory]] is a [[sigma model]] on [[spacetime]] $X$ combined with a chiral $G$-[[WZW model]] for $G = Spin \times E_8 \times E_8$ or similar and with the [[WZW term]] being the difference between the differentially twisted [[looping]] of the [[universal Chern-Simons circle 3-bundle|universal Chern-Simons 3-connection]] of $Spin$ with that of $E_8 \times E_8$. 

By ([Fiorenza-Rogers-Schreiber 13, section 2.6.1](#FiorenzaRogersSchreiber13)) we find in this case that the [[Heisenberg 2-group]] is the [[string 2-group]]

$$
  Heis(\mathbf{L}_{WZW^{het}})
  \simeq
  String(G)
  \,.
$$

It follows thus from the above discussion that a consistent heterotic [[sigma model]] requires that the underlying $G$-[[principal bundle]] on [[spacetime]] admits a [[string structure]]. This is the famous [[Green-Schwarz anomaly]] cancellation condition, re-expressed as a consistency condition for parameterized WZW models.

On the level of [[action functionals]] in [[codimension]] 0 this observation is due to ([Distler-Sharpe 10, section 7](#DistlerSharpe10)).


### The Green-Schwarz super $p$-branes on curved super spacetime

By [Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13) the super-[[branes]] of [[string theory]]/[[M-theory]] on [[super Minkowski spacetime]] $\mathbb{R}^{d-1,1;N}$ classified by the [[brane scan]]/[[schreiber:The brane bouquet|the brane bouqet]] are [[schreiber:∞-Wess-Zumino-Witten theory]] [[sigma-model]]

$$
  \mathbf{L}_{WZW^{brane}}
  \;\colon\;
  \mathbb{R}^{d-1,1;N} \longrightarrow \mathbf{B}^{p+1}(\mathbb{R}/\Gamma)_{conn}
  \,,
$$

where $\Gamma$ is the group of [[periods]] of the defining [[super L-∞ algebra]] [[L-∞ algebra cohomology|L-∞ cocycle]]

$$
  \mathbf{B} sIso_N(d-1,1) \longrightarrow \mathbf{B}^{p+2}(\mathbb{R}/\Gamma)
  \,.
$$

A necessary structure globalizing this to a curved super-spacetime $X$ is a [[G-structure]] on $X$ for $G = \mathbf{QuantMorph}(\mathbf{L}_{WZW^{brane}}^{inf})$ the restriction of the WZW term to the [[infinitesimal disk]].

Given this then the [[Green-Schwarz action functional]] refines to a [[local prequantum field theory]] datum $\mathbf{L}_{WZW^{brane}}$ globally defined on $X$.

(For [[branes]] on which other branes may end, such as the [[D-branes]] and the [[M5-brane]], here [[super Minkowski spacetime]] is replaced by a [[extended Minkowski super spacetime]], as discussed in ([Fiorenza-Sati-Schreiber 13](#FiorenzaSatiSchreiber13))).

More details are in ([cwzw](#cwzw)).

## Related concepts

* [[gauged WZW model]]

* [[definite globalization of WZW term]]

* [[higher Cartan geometry]]

## References

Parameterized WZW models as [[sigma models]] for the [[heterotic string]] originate in

* {#GatesSiegel88} [[Jim Gates]], [[Warren Siegel]], _Leftons, Rightons, Nonlinear $\sigma$-Models, and Superstrings_, Phys.Lett. B206 (1988) 631 ([spire](https://inspirehep.net/record/251286/))

* [[Jim Gates]], _Strings, superstrings, and two-dimensional lagrangian field theory_, pp. 140-184 in Z. Haba, J. Sobczyk (eds.) _Functional integration, geometry, and strings_, proceedings of the XXV Winter School of Theoretical Physics, Karpacz, Poland (Feb. 1989), , Birkh&#228;user, 1989.

* {#GKKS91} [[Jim Gates]], S. Ketov, S. Kozenko, O. Solovev, _Lagrangian chiral coset construction of heterotic string theories in $(1,0)$ superspace_, Nucl.Phys. B362 (1991) 199-231 ([spire](http://inspirehep.net/record/314337/?ln=en))

Discussion relating this to equivariant [[elliptic genera]] is in section 7 of

* {#DistlerSharpe10} [[Jacques Distler]], [[Eric Sharpe]], _Heterotic compactifications with principal bundles for general groups and general levels_, Adv. Theor. Math. Phys. 14:335-398, 2010 ([arXiv:hep-th/0701244](http://arxiv.org/abs/hep-th/0701244))
  
Review of this includes

* [[Eric Sharpe]], _Recent developments in heterotic compactifications_, in [[Eric Sharpe]], [[Arthur Greenspoon]], _[Advances in String Theory: The First Sowers Workshop in Theoretical Physics](http://www.ams.org/bookstore-getitem/item=AMSIP-44)_, AMS 2008 ([pdf slides (39-49)](http://www.phys.vt.edu/sowers/talks/sharpe-sowers.pdf))

The corresponding [[elliptic genera]] had been considered in 

* [[Matthew Ando]], _The sigma orientation for analytic circle-equivariant elliptic cohomology_, Geom. Topol. 7 (2003) 91-153 ([arXiv:math/0201092](http://arxiv.org/abs/math/0201092))

and with more emphasis on [[equivariant elliptic cohomology]] in 

* [[Matthew Ando]], _Equivariant elliptic cohomology and the Fibered WZW models of Distler and Sharpe_, [talk 2007](http://www.math.ucsb.edu/~drm/GTPseminar/2007-fall.php) ([lecture notes pdf](https://web.archive.org/web/20150326114418/https://www.math.ucsb.edu/~drm/GTPseminar/notes/20071026-ando/20071026-malmendier.pdf))

The discussion of the relevant [[Heisenberg n-group]] theory is in 

* {#FiorenzaRogersSchreiber13} [[Domenico Fiorenza]], [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, 2013 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))

with more details in 

* {#cwzw} [[Urs Schreiber]], _[[schreiber:Obstruction theory for parameterized higher WZW terms]]_

* [[Urs Schreiber]], section "definite forms" in _[[schreiber:differential cohomology in a cohesive topos]]_
  

General [[schreiber:∞-Wess-Zumino-Witten theory]] is set up in section 6 of

* {#FiorenzaSatiSchreiber13} [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The brane bouquet|Super Lie n-algebra extensions, higher WZW models and super p-branes with tensor multiplet fields]]_, 2013 ([arXiv:1308.5264](http://arxiv.org/abs/1308.5264))
  

[[!redirects parameterized WZW models]]
[[!redirects parameterized Wess-Zumino-Witten model]]
[[!redirects parameterized Wess-Zumino-Witten models]]

[[!redirects parametrized WZW model]]
[[!redirects parametrized WZW models]]
[[!redirects parametrized Wess-Zumino-Witten model]]

[[!redirects parametrized Wess-Zumino-Witten models]]


[[!redirects fibered WZW model]]
[[!redirects fibered WZW models]]
[[!redirects fibered Wess-Zumino-Witten model]]
[[!redirects fibered Wess-Zumino-Witten models]]

[[!redirects parameterized WZW term]]
[[!redirects parameterized WZW terms]]

[[!redirects definite parameterization of WZW term]]
[[!redirects definite parameterization of WZW terms]]
[[!redirects definite parameterization of higher WZW term]]
[[!redirects definite parameterization of higher WZW terms]]

[[!redirects definite parameterizations of higher WZW terms]]
