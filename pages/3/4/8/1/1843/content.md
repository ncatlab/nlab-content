
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
    \textstyle{\prod}_{f} 
    \exp(i \textstyle{\int}_f \Sigma^* B_{\rho(f)})
    \textstyle{\prod}_{e \subset f}
    \exp(i \textstyle{\int}_{e} \Sigma^* A_{\rho(f) \rho(e)})
    \textstyle{\prod}_{v \subset e \subset f}
    \exp(i \lambda_{\rho(f) \rho(e) \rho(v)})
    \,.
  $$

  That this is well defined requires that

  $$
    \lambda_{i j k} - \lambda_{i j l} +
    \lambda_{i k l} - \lambda_{j k l}
    = 0 \;mod \, 2\pi
    \,,
  $$

  which says that $(B_i, A_{i j}, \lambda_{i j k})$ is indeed a degree 3 [[Deligne cohomology|Deligne cocycle]].

## Over D-branes

The restriction of the Kalb-Ramond field in the 10-dimensional [[spacetime]] to a [[D-brane]] is a twist (as in [[twisted cohomology]]) of the [[gauge field]] on the D-brane: its 3-class is [[magnetic charge]] for the [[electromagnetic field]]/[[Yang-Mills field]] on the D-brane. See also [[Freed-Witten anomaly cancellation]] or the discussion in ([Moore](#Moore)).


## Related concepts

* [[discrete torsion]]

* [[h1-meson]], [[b1-meson]]

* [[WZW model]], [[basic bundle gerbe]]

[[!include table of branes]]


## References {#References}

The name goes back to:

* {#KalbRamond} M. Kalb, [[Pierre Ramond]], *Classical direct interstring action*, Phys. Rev. D. **9** (1974) 2273-2284 &lbrack;[doi:10.1103/PhysRevD.9.2273](https://doi.org/10.1103/PhysRevD.9.2273)&rbrack;
 
The interpretation as a 4d [[axion]]:

* {#SvrcekWitten06} Peter Svrcek, [[Edward Witten]], _Axions In String Theory_, JHEP 0606:051 (2006) &lbrack;[arXiv:hep-th/0605206](http://arxiv.org/abs/hep-th/0605206)&rbrack;

Phenomenology:

* P. C. Malta, J. P. S. Melo, C. A. D. Zarro: *Experimental signatures of Kalb-Ramond-like particles* &lbrack;[arXiv:2501.09836](https://arxiv.org/abs/2501.09836)&rbrack;


The interpretation of the B-field as a 3-[[cocycle]] in [[Deligne cohomology]] is due to

* [[Krzysztof Gawędzki]], *Topological Actions in two-dimensional Quantum Field Theories*, in: _Nonperturbative quantum field theory_, Nato Science Series B **185**, Springer (1986) &lbrack;[spire:257658](http://inspirehep.net/record/257658), [doi:10.1007/978-1-4613-0729-7_5](https://doi.org/10.1007/978-1-4613-0729-7_5), [[Gawedzki-TopologicalActions.pdf:file]]&rbrack;

picked up in

* {#FreedWitten99} [[Daniel Freed]], [[Edward Witten]], _Anomalies in String Theory with D-Branes_, Asian J. Math. **3** 4 (1999) 819-852 &lbrack;[arXiv:hep-th/9907189](http://arxiv.org/abs/hep-th/9907189), [InSpire:504509](https://inspirehep.net/literature/504509)&rbrack;

The equivalent formulation in terms of [[connections on bundle gerbes]] originates with

* {#GawędzkiReis02} [[Krzysztof Gawędzki]], [[Nuno Reis]], *WZW branes and gerbes*, Rev. Math. Phys. **14** (2002) 1281-1334 &lbrack;[arXiv:hep-th/0205233](https://arxiv.org/abs/hep-th/0205233), [doi:10.1142/S0129055X02001557](https://doi.org/10.1142/S0129055X02001557)&rbrack;

* {#CareyJohnsonMurray02} [[Alan Carey]], Stuart Johnson, [[Michael Murray]], _Holonomy on D-Branes_, Journal of Geometry and Physics **52** 2 (2004) 186-216 &lbrack;[arXiv:hep-th/0204199](http://arxiv.org/abs/hep-th/0204199), [doi:10.1016/j.geomphys.2004.02.008](https://doi.org/10.1016/j.geomphys.2004.02.008)&rbrack;


See also:

* {#BonoraRuffinoSavelli08} [[Loriano Bonora]], [[Fabio Ferrari Ruffino]], [[Raffaele Savelli]], *Classifying A-field and B-field configurations in the presence of D-branes*, JHEP 0812:078 (2008) &lbrack;[arXiv:0810.4291](https://arxiv.org/abs/0810.4291), [doi:10.1088/1126-6708/2008/12/078](https://doi.org/10.1088/1126-6708/2008/12/078)&rbrack;

* [[Fabio Ferrari Ruffino]], *Classifying A-field and B-field configurations in the presence of D-branes - Part II: Stacks of D-branes*, Nuclear Physics, Section B **858** (2012) 377-404 &lbrack;[arXiv:1104.2798](https://arxiv.org/abs/1104.2798), [doi:10.1016/j.nuclphysb.2012.01.013](https://doi.org/10.1016/j.nuclphysb.2012.01.013)&rbrack;


A more refined discussion of the [[differential cohomology]] of the Kalb-Ramond field and the [[RR-fields]] that it interacts with:

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_, Surveys in Differential Geometry **7** (2002) 129-194 &lbrack;  [arXiv:hep-th/0011220](http://arxiv.org/abs/hep-th/0011220), [doi:10.4310/SDG.2002.v7.n1.a6](https://dx.doi.org/10.4310/SDG.2002.v7.n1.a6), [spire:537392](https://inspirehep.net/literature/537392)&rbrack;

In fact, in full generality the Kalb-Ramond field on an [[orientifold]] background is not a plain bundle gerbe, but a _[[Jandl gerbe]]_, a connection on a nonabelian $AUT(U(1))$-[[principal 2-bundles]] for the [[automorphism 2-group]] $AUT(U)(1))$ of $U(1)$:

for the bosonic string this is discussed in 

* {#SSW05} [[Urs Schreiber]], [[Christoph Schweigert]], [[Konrad Waldorf]], _Unoriented WZW models and Holonomy of Bundle Gerbes_, Communications in Mathematical Physics **274** 1 (2007) 31-64 &lbrack;[arXiv:hep-th/0512283](http://arxiv.org/abs/hep-th/0512283), [doi:10.1007/s00220-007-0271-x](https://doi.org/10.1007/s00220-007-0271-x)&rbrack;

and for the refinement to the [[superstring]] in

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Precis_, in: [[Hisham Sati]], [[Urs Schreiber]] (eds.), _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics **83**, AMS (2011) &lbrack;[arXiv:0906.0795](http://arxiv.org/abs/0906.0795)&rbrack;

* {#DistlerFreedMooreII} [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Spin structures and superstrings_, Surveys in Differential Geometry, Volume 15 (2010) ([arXiv:1007.4581](http://arxiv.org/abs/1007.4581), [doi:10.4310/SDG.2010.v15.n1.a4](http://dx.doi.org/10.4310/SDG.2010.v15.n1.a4))

See at _[[orientifold]]_ for more on this; also at *[[discrete torsion]]*.

The role of the KR field in [[twisted K-theory]] (see *[[K-theory classification of D-brane charge]]*) is discussed a bit also in 

* {#Moore} [[Greg Moore]], _K-theory from a physical perspective_ &lbrack;[arXiv:hep-th/0304018](http://arxiv.org/abs/hep-th/0304018)&rbrack;

In relation to [[first-order formulation of gravity|Einstein-Cartan theory]]:

* Richa Kapoor, _A review of Einstein Cartan Theory to describe superstrings with intrinsic torsion_ ([arXiv:2009.07211](https://arxiv.org/abs/2009.07211))

* Tanmoy Paul, _Antisymmetric tensor fields in modified gravity: a summary_ ([arXiv:2009.07732](https://arxiv.org/abs/2009.07732))

In the context of [[cosmology]] with the Kalb-Ramond field as a [[dark matter]]-candidate (cf, *[[axion]]* and *[[fuzzy dark matter]]*):

* Christian Capanelli, Leah Jenks, Edward W. Kolb, Evan McDonough, *Cosmological Implications of Kalb-Ramond-Like-Particles* &lbrack;[arXiv:2309.02485](https://arxiv.org/abs/2309.02485)&rbrack;

See also:

* [[Peter D. Jarvis]], [[Jean Thierry-Mieg]], *Antisymmetric tensor fields: actions, symmetries and first order Duffin-Kemmer-Petiau formulations* &lbrack;[arXiv:2311.01675](https://arxiv.org/abs/2311.01675)&rbrack;

* [[Jean Thierry-Mieg]], [[Peter D. Jarvis]], *Conformal invariance of antisymmetric tensor field theories in any even dimension* &lbrack;[arXiv:2311.01701](https://arxiv.org/abs/2311.01701)&rbrack;




[[!redirects Kalb-Ramond fields]]  

[[!redirects Kalb--Ramond field]]
[[!redirects Kalb–Ramond field]]
[[!redirects B-field]]
[[!redirects B-fields]]


[[!redirects B2-field]]


