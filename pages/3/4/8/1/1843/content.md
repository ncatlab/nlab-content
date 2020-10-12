
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The **Kalb-Ramond field**  or **B-field** is the [[higher U(1)-gauge field]] that generalizes the [[electromagnetic field]] from point [[particles]] to [[string theory|strings]].

Its dual incarnation in [[KK-compactifications]] of [[heterotic string theory]] to 4d is a candidate for the hypothetical [[axion]] field ([Svrcek-Witten 06, p. 15](#SvrcekWitten06)).

Recall that the [[electromagnetic field]] is modeled as a [[cocycle]] in degree 2 [[ordinary differential cohomology]] and that this mathematical model is fixed by the fact that charged particles that trace out 1-dimensional trajectories couple to the electromagnetic field by an [[action functional]] that sends each trajectory to the holonomy of a $U(1)$-[[connection on a bundle|connection]] on it.

When replacing particles with 1-dimensional trajectories by [[string theory|strings]] with 2-dimensional trajectories, one accordingly expects that they may couple to a higher degree background field given by a degree 3 [[ordinary differential cohomology]] cocycle.

In [[string theory]] this situation arises and the corresponding background field appears, where it is called the _Kalb-Ramond field_  .

Often it is also simply called the **$B$-field** , after the standard symbol used for the 2-forms $(B_i \in \Omega^2(U_i))$ on patches $U_i$ of a [[cover]] of spacetime when the differential cocycle is expressed in a [[Cech cohomology]] realization of [[Deligne cohomology]].


This is the analog of the local 1-forms $(A_i \in \Omega^1(U_i))$ in a Cech cocycle presentation of a [[line bundle]] with [[connection on a bundle|connection]] encoding the [[electromagnetic field]].

The [[field strength]] of the Kalb-Ramond field is a [[differential forms|3-form]] $H \in \Omega$. On each patch $U_i$ it is given by

$$
  H|_{U_i} = d B_i
  \,.
$$


And just as a degree 2 [[Deligne cohomology|Deligne cocycle]] is equivalently encoded in a $U(1)$-[[principal bundle]] [[connection on a bundle|with connection]], the degree 3 differential cocycle is equivalently encoded in

* a degree 3 [[Deligne cohomology|Deligne cocycle]];

* a $\mathbf{B}U(1)$-[[principal 2-bundle]] with connection;

* a $U(1)$-[[bundle gerbe]] with connection. 

The study of [[bundle gerbe]]s was largely motivated and driven by the desire to understand the Kalb-Ramond field.

The next higher degree analog of the electromagnetic field is the [[supergravity C-field]].

## Mathematical model from (formal) physical input 

The derivation of the fact that the Kalb-Ramond field that is locally given by a 2-form is globally really a degree 3 cocycle in the [[Deligne cohomology]] model for [[ordinary differential cohomology]] proceeds in in entire analogy with the corresponding discussion of the [[electromagnetic field]]:

* **classical background** The [[field strength]] 3-form $H \in \Omega^3(X)$ is required to be closed, $d H_3 = 0$.

* **quantum coupling** The gauge interaction with the quantum string is required to yield a well-defined surface holonomy in $U(1)$ from locally integrating the 2-forms $B_i \in \Omega^2(U_2)$ with $d B_i = H|_{U_i}$ over its 2-dimensional trajectory.


  $$
    hol(\Sigma)
    =
    \prod_{f} \exp(i \int_f \Sigma^* B_{\rho(f)})
    \prod_{e \subset f}
    \exp(i \int_{e} \Sigma^* A_{\rho(f) \rho(e)})
    \prod_{v \subset e \subset f}
    \exp(i \lambda_{\rho(f) \rho(e) \rho(v)})
    \,.
  $$

  That this is well defined requires that

  $$
    \lambda_{i j k} - \lambda_{i j l} +
    \lambda_{i k l} - \lambda_{j k l}
    = 0 \;mod \, 2\pi
  $$

  which says that $(B_i, A_{i j}, \lambda_{i j k})$ is indeed a degree 3 [[Deligne cohomology|Deligne cocycle]].

## Over D-branes

The restriction of the Kalb-Ramond field in the 10-dimensional [[spacetime]] to a [[D-brane]] is a twist (as in [[twisted cohomology]]) of the [[gauge field]] on the D-brane: its 3-class is [[magnetic charge]] for the [[electromagnetic field]]/[[Yang-Mills field]] on the D-brane. See also [[Freed-Witten anomaly cancellation]] or the discussion in ([Moore](#Moore)).


## Related concepts

* [[discrete torsion]]

* [[h1-meson]], [[b1-meson]]

[[!include table of branes]]

## References {#References}

The name goes back to the article

* {#KalbRamond} M. Kalb and [[Pierre Ramond]], _Classical direct interstring action, Phys. Rev. D. 9 (1974), 2273&#8211;2284_
 

The interpretation as a 4d [[axion]] is discussed in

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051,2006 ([arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206))

The earliest reference where the gauge term in the standard string [[action functional]] is identified with the surface holonomy of a 3-cocycle in [[Deligne cohomology]] seems to be

* [[Krzysztof Gawedzki]], _Topological Actions in two-dimensional Quantum Field Theories_, in: ’t Hooft G., Jaffe A., Mack G., Mitter P.K., Stora R. (eds.) Cargese 1987 proceedings, _Nonperturbative quantum field theory_ (1986) ([spire:257658](http://inspirehep.net/record/257658), [doi:10.1007/978-1-4613-0729-7_5](https://doi.org/10.1007/978-1-4613-0729-7_5))

The later article

* [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_, Asian J. Math. 3:819, 1999 ([arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189))

argues that the string $B$-field is a cocycle in [[Čech cohomology]]--[[Deligne cohomology|Deligne]] cohomology using [[quantum anomaly]]-cancellation arguments.

This is expanded on in 

* {#CareyJohnsonMurray02} [[Alan Carey]], Stuart Johnson, [[Michael Murray]], _Holonomy on D-Branes_, Journal of Geometry and Physics Volume 52, Issue 2, October 2004, Pages 186-216 ([arXiv:hep-th/0204199](http://arxiv.org/abs/hep-th/0204199), [doi:10.1016/j.geomphys.2004.02.008](https://doi.org/10.1016/j.geomphys.2004.02.008))

A more refined discussion of the [[differential cohomology]] of the Kalb-Ramond field and the fields that it interacts with is in

* [[Dan Freed]], _Dirac Charge Quantization and Generalized Differential Cohomology_ ([arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220))

In fact, in full generality the Kalb-Ramond field on an [[orientifold]] background is not a plain gerbe, but a _Jandl gerbe_ , a connection on a nonabelian $AUT(U(1))$-[[principal 2-bundle]]s for the [[automorphism 2-group]] $AUT(U)(1))$ of $U(1)$:

for the bosonic string this is discussed in 

* [[Urs Schreiber]], [[Christoph Schweigert]], [[Konrad Waldorf]], _Unoriented WZW Models and Holonomy of Bundle Gerbes_ ([arXiv:hep-th/0512283](http://arxiv.org/abs/hep-th/0512283))

and for the refinement to the [[superstring]] in

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Precis_ in [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics volume 83 AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795))

* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_, Surveys in Differential Geometry, Volume 15 (2010) ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581), [doi:10.4310/SDG.2010.v15.n1.a4](http://dx.doi.org/10.4310/SDG.2010.v15.n1.a4))
See at _[[orientifold]]_ for more on this.

The role of the KR field in [[twisted K-theory]] is discussed a bit also in 

* {#Moore} [[Greg Moore]], _K-theory from a physical perspective_ ([arXiv:hep-th/0304018](http://arxiv.org/abs/hep-th/0304018))

In relation to Einstein-Cartan theory:

* Richa Kapoor, _A review of Einstein Cartan Theory to describe superstrings with intrinsic torsion_ ([arXiv:2009.07211](https://arxiv.org/abs/2009.07211))

* Tanmoy Paul, _Antisymmetric tensor fields in modified gravity: a summary_ ([arXiv:2009.07732](https://arxiv.org/abs/2009.07732))


  

[[!redirects Kalb--Ramond field]]
[[!redirects Kalb–Ramond field]]
[[!redirects B-field]]
[[!redirects B-fields]]


[[!redirects B2-field]]
