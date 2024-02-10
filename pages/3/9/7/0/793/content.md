+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Duality in string theory
+-- {: .hide}
[[!include duality in string theory -- contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
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

A $d$-dimensional [[sigma-model]] is a [[quantum field theory]] that is induced from certain [[differential geometry|differential geometric]] and [[differential cohomology|differential cohomological]] data, to be thought of as encoding the background geometry on which quantum objects of dimension $d$ propagate.

The operation of **T-duality** is a map that interchanges pairs of such geometric data for 2-dimensional [[conformal field theory]] [[sigma-model]]s, such that the induced QFTs are equivalent. 

More specifically the space of [[differential geometry|differential geometric]] data consisting of

* a smooth [[manifold]] $X$ 

* equipped with the structure of a $k$-torus [[bundle]] $X \simeq Y \times T^k$; -- the total space of this bundle modelling [[spacetime]];

* and equipped with a [[Riemannian metric]] $g$ -- modelling the field of [[gravity]];

* and a $U(1)$-[[gerbe]] with connection $G$; -- modelling the [[Kalb-Ramond field]];

* possibly a cocycle in [[differential K-theory]] modelling the [[RR-field]];


admits a certain operation that, roughly, inverts the Riemannian circumference of the torus fibers and mixes the metric with the gerbe data, such that the induced 2-dimensional [[sigma-model]] QFTs for these backgrounds are equivalent. This is the operation called **T-duality**.

This was noticed originally in the study of [[conformal field theory|conformal field theories]] in the context of [[string theory]]: the conformal field theory [[sigma-model]]s with target space $X$ turn out to be equivalent as [[quantum field theory|quantum field theories]] for T-dual backgrounds $(X,g,G)$ and $(X',g',G')$ (at least to the approximate degree to which these are realized as full CFTs in the first place).

Further generalisations let $X$ be a nontrivial torus bundle, but the T-dual is then generically a bundle of [[noncommutative torus|non-commutative tori]]. (cite Mathai, Rosenberg and Hannabus)

## Path integral heuristics deriving T-duality {#PathIntegral}

We indicate how one can see T-duality from formal manipulations
of the [[path integral]] for the [[string theory|string]] [[sigma-model]]. We look at the simplest situation, where the torus bundle in question is a trivial circle bundle over a [[Cartesian space]] carrying the metric induced from the standard flat metric on $\mathbb{R}^n$ and where there are no other nontrivial background fields. In fact, for the purpose of the following computation we can entirely ignore the base of this bundle and consider target space to be nothing but a circle. Since the [[sigma-model]] for this is on the worldsheet just the theory of a single free field with values in $S^1$, this is often also called the "free boson on the circle".

This means that the only geometric datum determining the background geometry is the circumference $2 \pi R$ of the fiber of the circle bundle. The statement of T-duality in this situation is that the 2-dimensional [[sigma-model]] on this background yields the same 2-dimensional [[CFT]] as that for this kind of background with circumference of the circle being $2 \pi 1/R$.

### A first rough look

A quick way to get an indication for this is to consider the center-of-mass energy of the string in such a circle-bundle background. In the simplified setup we mentioned before, a string on a circle of radius $R$ has 
quantized momentum $p = \frac{\ell \in \mathbb{Z}}{R}$. In a state in which the string winds around the circle $m$ times and has $\ell$ quanta of kinetic momentum for propagation around the circle,  its energy is

$$
  E_0 = \sqrt{p^2 + M^2} = \sqrt{(\ell/R)^2 + (R m)^2 }
  \,,
$$

This energy is clearly invariant under exchanging

$$
  (R, (\ell, m)) \mapsto (\frac{1}{R}, (m,\ell))
  \,.
$$

This is of course far from being a proof that the corresponding two [[QFT]]s are equivalent, but it does already capture a good deal of the essence of what T-duality does and why it works.

In slightly more detail, but still at a very rough level, if we denote by

$$
  X : \Sigma \to S^1_R
$$

the $\sigma$-model field on the worldsheet $\Sigma = \mathbb{R}^2$ with values in target space $S^1_R$ then T-duality with respect to this circle may be thought of as exchanging worldsheet momentum $\partial_t X$ with worldsheet winding $\partial_\sigma X$.

This then also means that for the open string it exchanges von Neumann boundary conditions $\partial_\sigma X|_{\sigma = 0} = 0$ with Dirichlet boundary conditions $\partial_t X|_{\sigma = 0} = 0$. The first boundary condition is that describing an open string whose endpoints are free to propagate in worldsheet time, whereas the second boundary condition describes a situation where the endpoint of the string is fixed at some point in target space. In terms of the language of geometric target space data, a sigma-model with such a constraint is said to describe a [[D-brane]] in target space: the locus where the endpoints of the string are fixed. This is a first indication that the T-duality operation on geometric background also involves the [[RR-field]].


### The path integral

We follow [[Kentaro Hori]]'s [[path integral]] discussion of T-duality. Here the strategy is to consider a path integral over a certain space of auxiliary fields and show or argue that by "algebraically integrating out" some of these in two different ways, the path integral is equivalent to that over two different [[action functional]]s, which describe two T-dual geometric backgrounds.

Let the boundary components of the worldsheet $\Sigma$ be labeled by
$\partial \Sigma_{(1)}$.

We consider the following fields on the worldsheet:


* $\tilde X : \Sigma \to \mathbb{R}/(2\pi/R)\mathbb{Z} = S^1_{1/R}$ -- a circle-valued function; this is the standard $\sigma$-model field describing propagation of the string on the circle;

* $X_{i} : \partial \Sigma_{(i)} \to S^1_R$ -- the boundary values of this field;


* $b \in \Omega^1(\Sigma, \mathbb{R})$ -- a 1-form; this is the auxiliary field that will not contribute to the dynamics but serves to make the T-duality manifest.


Consider then the following [[action functional]] on this collection of fields given by the assignment

$$
  S'_E(\tilde X,b) = \frac{1}{2 \pi}
  \int_\Sigma
  \left(
     \frac{1}{2} b \wedge \star b  - b \wedge d \tilde X
  \right)
  -
  \frac{i}{2 \pi} \sum_{i = 1}^s
  \int_{\partial \Sigma_{(i)}}
  (\tilde X -a_i) d X_i
  \,,
$$ 

where the $(a_i)$ are a collection of real numbers.

We now want to formally perform the [[path integral]] over the fields in two different orders, which should give the same quantum field theories but in terms of different effective action functionals.

If we do first the path integral over the field $b$ then by the general formal rule of "algebraically integrating out a non-dynamical field" which says that we can evaluate this path integral that formally looks like a Gaussian integral by the usual formulas for Gaussian integrals, we obtain the action functional


$$
  \tilde S_E =
  \frac{1}{4 \pi} 
  \int_\Sigma d \tilde X \wedge \star d \tilde X
  +
  \frac{i}{2\pi}
  \int_{\partial \Sigma_{(i)}}
  (\tilde X - a_i)
  d X_i
$$

then doing the integral over the boundary values $X_i$ yields

$$
  \tilde X|_{\partial \Sigma_i} = a_i
$$

This is the action functional for a $\sigma$-model on $S^1_{1/R}$ with a D-brane at $\tilde X = a_i$.

Now we evaluate the original path integral in a different way, this way first integrating over components of $\tilde X$. To do so, we imagine that we may re-encode the field $\tilde X$ in terms of its de Rham differential

$$
  d \tilde X = d f + \frac{2\pi}{R}\sum_A \eta_A \omega_A
$$

where $\eta_A$ are integers and

$$
  \{\omega_A\} \subset 
   H^1(\Sigma, \mathbb{Z})
   \simeq
   \mathbb{Z}^{\oplus 2g + s - 1}
 \,.
$$

Then formally performing the path integral over $f$ yields $d b = 0$ and $b|_{\partial \Sigma} = d X_i$. It follows that $b = d X$ for some other field $X : \Sigma \to S^1_R$. 

So we get the action

$$
  S_E = \frac{1}{4\pi} \int_\Sigma d X \wedge \star d X
  +
  \frac{i}{2 \pi}
   \sum_{i = 1}^s
   \int_{\partial \Sigma_i}
   a_i d X
$$

in terms of the field $X$.  This is the $\sigma$-model for string propagation on  $S^1_R$. with D-brane wrapped on  $S^1_R$ that carries on its worldvolume a [[gauge field]] given by a constant connection 1-form $a_i$.



## Topological T-duality 

It turns out to be possible and useful to discuss just the _topological_ aspects of T-duality, meaning all the aspects that depend on the $X$ as a [[topological space]], on the topological class of the [[gerbe]] and of its 3-form curvature, but not on the [[Riemannian metric]] and not on the precise connection on the gerbe (there may be several inequivalent ones for a given curvature)!

This sub-phenomenon is discussed in more detail at [[topological T-duality]].


## Geometric T-duality 

### In terms of generalized differential cohomology
 {#InDiffCohomology}

[[gauge field|Gauge field]]s are [[cocycle]]s in [[differential cohomology]]. The [[Kalb-Ramond field]] is given by degree-3 [[ordinary differential cohomology]], the differential refinement on degree-3 [[integral cohomology]]. The [[RR-field]] is given by [[differential K-theory]]. 

Induced by the morphisms $\mathbf{c}(n)$ in the [[fiber sequence]]s

$$
  \mathbf{B}U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n) 
  \stackrel{\mathbf{c}_n}{\to} \mathbf{B}^2 U(1)
$$

is induced a notion of [[twisted cohomology]] which makes the Kalb-Ramond field act as a twist for [[twisted K-theory]].

In these terms, the setup of T-duality is a [[correspondence]] of [[Kalb-Ramond field]]s over [[spacetime]] [[torus]]-bundles $P \to X$ and $\hat P \to X$ that induces an integral transform

$$
  K_{diff}^{\bullet + \tau}(P)
  \to 
  K_{diff}^{\bullet + \tau -1}(\hat P)
$$

of twisted differential K-theory classes.

This is an [[isomorphism]] -- the action of the T-duality isomorphism on the Kalb-Ramond field and the RR-field.

See ([KahleValentino](#KahleValentino)).

### In generalized complex geometry {#TdualityIngcg}

Another approach to the study of T-duality takes a somewhat complementary point of view and ignores the [[Eilenberg-MacLane spectrum|integral cohomology]] class in $H^3(X,\mathbb{Z})$ of the [[gerbe]] but does consider the [[Riemannian metric]].

In this context T-duality is described as an isomorphism of [[standard Courant algebroid]]s. This picture emerged in the study of [[generalized complex geometry]].

## Examples of T-dual pairs

### In Mirror symmetry

One special case of T-duality is [[mirror symmetry]].

* [[Andrew Strominger]], [[Shing-Tung Yau]], [[Eric Zaslow]], _Mirror Symmetry is T-Duality_, Nucl. Phys. B 479:243-259,1996 (DOI 10.1016/0550-3213(96)00434-8) [hep-th/9606040](http://arxiv.org/abs/hep-th/9606040)

### In Langlands duality

In some cases the passage to the [[Langlands dual group]] in the [[geometric Langlands correspondence]] can be understood as T-duality. ([Daenzer-vanErp](#DaenzerErp))


## Related concepts

[[duality in physics]], [[duality in string theory]]

* **T-duality**

  * [[topological T-duality]]

    * [[spherical T-duality]]

  * [[Poisson-Lie T-duality]]

  * [[differential T-duality]]

  * [[T-duality 2-group]]

* [[T-fold]], [[double field theory]]

* [[duality in string theory]]

  * [[U-duality]], [[S-duality]]

  * [[AdS/CFT correspondence]]

The geometry of the fiber product of two torus fiber bundles with a [[circle 2-bundle]] on it is sometimes referred to as _[[Bn-geometry]]_.

## References

The observation of T-duality is attributed to 

* [[Thomas Buscher]], _A symmetry of the string background field equations,
Phys. Lett. B 194 (1987) 59 (<a href="https://doi.org/10.1016/0370-2693(87)90769-6">doi:10.1016/0370-2693(87)90769-6</a>)

* [[Thomas Buscher]], _Path integral derivation of quantum duality in nonlinear sigma models_, Phys. Lett. B 201 (1988) 466 (<a href="https://doi.org/10.1016/0370-2693(88)90602-8">doi:10.1016/0370-2693(88)90602-8</a>)

Precursors include (according to [Schwarz 96, first paragraph](#Schwarz96)):

* Keiji Kikkawa, Masami Yamasaki, _Casimir effects in superstring theories_, Physics Letters B Volume 149, Issues 4–5, 20 December 1984, Pages 357-360 (<a href="https://doi.org/10.1016/0370-2693(84)90423-4">doi:10.1016/0370-2693(84)90423-4</a>)

Discussion for the [[superstring]] is in

* M. Abou-Zeid, [[Chris Hull]], [[Ulf Lindström]], [[Martin Roček]], _T-Duality in $(2,1)$ Superspace_ ([arXiv:1901.00662](https://arxiv.org/abs/1901.00662))

Review:

* Amit Giveona, Massimo Porrati, Eliezer Rabinovicia, _Target space duality in string theory_, Physics Reports Volume 244, Issues 2–3, August 1994, Pages 77-202 (<a href="https://doi.org/10.1016/0370-1573(94)90070-1">doi:10.1016/0370-1573(94)90070-1</a>)

* E. Alvarez, [[Luis Alvarez-Gaume]], Y. Lozano, _An Introduction to T-Duality in String Theory_, Nucl.Phys.Proc.Suppl.41:1-20,1995 ([arXiv:hep-th/9410237](https://arxiv.org/abs/hep-th/9410237))

* [[Jonathan Rosenberg]], *Topology, $C^*$-algebras, and string duality*, Regional Conference Series in Mathematics **111**, Amer. Math. Soc. (2009)  &lbrack;[doi:10.1090/cbms/111](https://doi.org/10.1090/cbms/111), [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:05632075&type=pdf&format=complete)&rbrack;

  > (focus on [[topological T-duality]])


* {#West12} [[Peter West]], section 17.1 of _[[Introduction to Strings and Branes]]_, Cambridge University Press 2012

* [[Mathai Varghese]], _T-duality: A basic introduction_, 10th Geometry and Physics Conference _Quantum Geometry_, Anogia 2012 ([[Mathai12.pdf:file]])

* Jnanadeva Maharana, _The Worldsheet Perspective of T-duality Symmetry in String Theory_ ([arXiv:1302.1719](http://arxiv.org/abs/1302.1719))

* Mark Bugden, _A Tour of T-duality: Geometric and Topological Aspects of T-dualities_, ([arXiv:1904.03583](https://arxiv.org/abs/1904.03583))



Discussion at strong coupling ("[[F-theory]]") includes

* {#Schwarz96} [[John Schwarz]], _M Theory Extensions of T Duality_ ([arXiv:hep-th/9601077](https://arxiv.org/abs/hep-th/9601077))

* {#Russo97} [[Jorge Russo]], _T-duality in M-theory and supermembranes_, Phys.Lett. B400 (1997) 37-42 ([arXiv:hep-th/9701188](https://arxiv.org/abs/hep-th/9701188))


Dscussion in [[higher differential geometry]]:

* {#Alfonsi19} [[Luigi Alfonsi]], _Global Double Field Theory is Higher Kaluza-Klein Theory_, Fortsch. d. Phys. 2020 ([arXiv:1912.07089](https://arxiv.org/abs/1912.07089), [doi:10.1002/prop.202000010](https://doi.org/10.1002/prop.202000010))

  (relating [[Kaluza-Klein compactification]] on [[principal ∞-bundles]] to [[double field theory]], [[T-folds]], [[non-abelian T-duality]], [[type II geometry]], [[exceptional geometry]], ...)

* [[Luigi Alfonsi]], _The puzzle of global Double Field Theory: open problems and the case for a Higher Kaluza-Klein perspective_ ([arXiv:2007.04969](https://arxiv.org/abs/2007.04969))



Discussion of geometric T-duality in terms of some form of [[differential cohomology]]:

as an operation on [[twisted K-theory|twisted]] [[differential K-theory]]:

* {#KahleValentino} [[Alexander Kahle]], [[Alessandro Valentino]], _[[T-Duality and Differential K-Theory]]_ 

using [[adjusted Weil algebra|adjusted]] [[principal 2-connections]]:

* [[Hyungrok Kim]], [[Christian Saemann]], *Non-Geometric T-Duality as Higher Groupoid Bundles with Connections* *lbrack;[arXiv:2204.01783](https://arxiv.org/abs/2204.01783)&rbrack;

* [[Hyungrok Kim]], [[Christian Saemann]], *T-duality as Correspondences of Categorified Principal Bundles with Adjusted Connections* &lbrack;[arXiv:2303.16162](https://arxiv.org/abs/2303.16162)&rbrack;

* [[Konrad Waldorf]], *Geometric T-duality: Buscher rules in general topology* &lbrack;[arXiv:2207.11799](https://arxiv.org/abs/2207.11799)&rbrack;
 

More physically oriented discussion of this is in 

* [[Katrin Becker]], Aaron Bergman, _Geometric Aspects of D-branes and T-duality_ ([arXiv:0908.2249](http://arxiv.org/abs/0908.2249))

Geometric T-duality is identified as an [[isomorphism]] of [[standard Courant algebroid]]s ([[generalized complex geometry]]) in section 4 of

* [[Gil Cavalcanti]], [[Marco Gualtieri]], _Generalized complex geometry and T-duality_ ([arXiv:1106.1747](http://arxiv.org/abs/1106.1747))

Discussion of the [[sigma-model]] description of T-duality in this context includes

* [[Ulf Lindstöm]], [[Martin Rocek]], Itai Ryb, [[Rikard von Unge]], [[Maxim Zabzine]], _T-duality and Generalized K&#228;hler Geometry_, JHEP 0802:056,2008 ([arXiv:0707.1696](http://arxiv.org/abs/0707.1696))

* Jonas Persson, _T-duality and Generalized Complex Geometry_ ([arXiv:hep-th/0612034](http://arxiv.org/abs/hep-th/0612034))

Further references are

* Willie Carl Merrell, _Application of superspace techniques to effective actions, complex geometry and T-duality in String theory_ ([pdf](http://www.lib.umd.edu/drum/bitstream/1903/6865/1/umi-umd-4355.pdf))

* Peggy Kao, _T-duality and Poisson-Lie T-duality in generalized geometry_ ([pdf](http://tpsrv.anu.edu.au/Members/bouwknegt/Kao.pdf))

Discussion of the infinitesimal T-duality geometry, replacing [[gerbes]] on [[torus]]-[[fiber bundles]] with the corresponding [[dg-manifolds]] is in 

* [[Ernesto Lupercio]], Camilo Rengifo, [[Bernardo Uribe]], _T-duality and exceptional generalized geometry through symmetries of dg-manifolds_ ([arXiv:1208.6048](http://arxiv.org/abs/1208.6048))

For references on [[topological T-duality]] see there.

A relation to [[Langlands dual groups]]:

* {#DaenzerErp} [[Calder Daenzer]], [[Erik Van Erp]], *T-Duality for Langlands Dual Groups*, Advances in Theoretical and Mathematical Physics **18** 6 (2014) 1267–1285 &lbrack;[arXiv:1211.0763](http://arxiv.org/abs/1211.0763), [doi:10.4310/ATMP.2014.v18.n6.a2](https://dx.doi.org/10.4310/ATMP.2014.v18.n6.a2)&rbrack;
 
For [[RR-fields]]:

* {#Hori99} [[Kentaro Hori]], _D-branes, T-duality and Index theory_, Adv. Theor. Math. Phys. 3 (1999) 281 ([arXiv:hep-th/9902102](https://arxiv.org/abs/hep-th/9902102))


Discussion of T-duality that takes into account the [[super p-brane]] charges (i.e. the fermionic components of the [[RR-fields]]) on [[super spacetime]], hence also of [[Green-Schwarz action functionals]], includes the following:

* [[Mirjam Cvetic]], H. Lu, [[Christopher Pope]], [[Kellogg Stelle]], _T-Duality in the Green-Schwarz Formalism, and the Massless/Massive IIA Duality Map_, Nucl.Phys.B573:149-176,2000 ([arXiv:hep-th/9907202](https://arxiv.org/abs/hep-th/9907202))

* Bogdan Kulik, Radu Roiban, _T-duality of the Green-Schwarz superstring_, JHEP 0209 (2002) 007 ([arXiv:hep-th/0012010](https://arxiv.org/abs/hep-th/0012010))


* {#BandosJulia03} [[Igor Bandos]], [[Bernard Julia]], _Superfield T-duality rules_, JHEP 0308 (2003) 032 ([arXiv:hep-th/0303075](https://arxiv.org/abs/hep-th/0303075))

  reviewed in _Superfield T-duality rules in ten dimensions with one isometry_ ([arXiv:hep-th/0312299](https://arxiv.org/abs/hep-th/0312299))

Lift of T-duality from [[string theory]] to a [[SL(2,Z)]]-[[U-duality]] acting on the [[M2-brane]]-[[Green-Schwarz action functional|sigma-model]]:

* [[Maria P. Garcia del Moral]], I. Martin, [[Alvaro Restuccia]], *Nonperturbative $SL(2,\mathbb{Z})$ $(p,q)$-strings manifestly realized on the quantum M2* &lbrack;[arXiv:0802.0573](https://arxiv.org/abs/0802.0573)&rbrack;

* [[Maria P. Garcia del Moral]], J. M. Pena, [[Alvaro Restuccia]], *Aspects of the T-duality construction for the Supermembrane theory*, J. Phys.: Conf. Ser. **720** (2016) 012025 &lbrack;[arXiv:1504.06907](https://arxiv.org/abs/1504.06907), [doi:10.1088/1742-6596/720/1/012025](https://doi.org/10.1088/1742-6596/720/1/012025)&rbrack;




[[!redirects Buscher rule]]
[[!redirects Buscher rules]]
