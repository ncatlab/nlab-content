
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
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

Recall that _geometric_ [[T-duality]] is an operation acting on tuples roughly consisting of

* a [[smooth manifold]] $X$ with the structure of a torus-[[principal bundle]] $T^n \to X \to X/T^n$ -- modelling [[spacetime]]

* equipped with a [[circle n-bundle with connection|circle 2-bundle with connection]] -- modelling the [[Kalb-Ramond field]]

* and in [[twisted K-theory]] refined to elements in [[differential K-theory|differential twisted K-theory]] -- modelling the [[RR-field]]
  
* and notably equipped with a (pseudo)[[Riemannian metric]] -- modelling the field of [[gravity]].

The idea of **topological T-duality** (due to [Bouwknegt-Evslin-Mathai 04](#BouwknegtEvslinMathai04), [Bouwknegt-Hannabus-Mathai 04](#BouwknegtHannabusMathai04)) is to disregard the [[Riemannian metric]] and the connection and study the remaining "topological" structure.

While the idea of [[T-duality]] originates in [[string theory]], topological T-duality has become a field of study in pure mathematics in its own right. 

In the language of [[bi-brane]]s a topological T-duality transformation is a bi-brane of a special kind between the two gerbes involved. The induced [[integral transform]] (on sheaves of sections of, or K-classes of) (twisted) vector bundles is essentially the [[Fourier-Mukai transformation]]. More on the bi-brane interpretation of (topological and non-topological) T-duality is in ([Sarkissian-Schweigert 08](#SarkissianSchweigert08)).


## Definition

Two tuples $(X_i \to B, G_i)_{i = 1,2}$ consisting of a $T^n$-bundle $X_i$ over a manifold $B$ and a line [[bundle gerbe]] $G_i \to X_i$ over $X$ are **topological T-duals** if there exists an isomorphism $u$ of the two [[bundle gerbes]] pulled back to the [[fiber product]] [[correspondence]] space $X_1 \times_B X_2$:

$$
  \array{
    && pr_1^* G_1 && \stackrel{u}{\leftarrow}
    && pr_2^* G_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    G_1 &&&& X_1 \times_B X_2 &&&& G_2
    \\
    & \searrow && \swarrow && \searrow && \swarrow
    \\
    && X_1 &&&& X_2
    \\
    &&& \searrow && \swarrow
    \\
    &&&& B
  }
$$

of a certain prescribed [[integral transform]]-form ([Bunke-Rumpf-Schick 08, p. 9](#BunkeRumpfSchick08))).

## Related concepts

* [[T-duality]]

  * **topological T-duality**

  * [[differential T-duality]]

  * [[T-duality 2-group]]

* [[spherical T-duality]]

## References

### General

The concept of topological T-duality was introduced on the level of [[differential form]]-data in

* {#BouwknegtEvslinMathai04} [[Peter Bouwknegt]], [[Jarah Evslin]], [[Varghese Mathai]], _T-Duality: Topology Change from H-flux_, Commun. Math. Phys. 249:383-415, 2004 &lbrack;[hep-th/0306062](http://arxiv.org/abs/hep-th/0306062), [doi:10.1007/s00220-004-1115-6](https://doi.org/10.1007/s00220-004-1115-6)&rbrack; 

* {#BouwknegtHannabusMathai04} [[Peter Bouwknegt]], [[Keith Hannabus]], [[Varghese Mathai]], _T-duality for principal torus bundles_, JHEP 0403 (2004) 018 ([hep-th/0312284](http://arxiv.org/abs/hep-th/0312284)) 

In these papers the $U(1)$-[[gerbe]] ([[circle 2-bundle with connection]]) does not appear, but an integral [[differential 3-form]], representing its [[Dixmier-Douady class]] does. Note that if the [[Eilenberg-MacLane spectrum|integral]] [[cohomology group]] $H^3(X,\mathbb{Z})$ of $X$ has [[torsion]] in dimension three, not all gerbes will arise in this way.  

The formalization with the above topological/[[homotopy theory|homotopy theoretic]] data originates in 

* {#BunkeSchick04} [[Ulrich Bunke]], [[Thomas Schick]], _On the topology of T-duality_, Rev. Math. Phys. **17** (2005) 77-112 &lbrack;[arXiv:math/0405132](https://arxiv.org/abs/math/0405132), [doi:10.1142/S0129055X05002315](https://doi.org/10.1142/S0129055X05002315)&rbrack;

* {#BunkeRumpfSchick08} {#BunkeRumpfSchick08} [[Ulrich Bunke|U. Bunke]], P. Rumpf, [[Thomas Schick]], _The topology of $T$-duality for $T^n$-bundles_,  Rev. Math. Phys. **18** 1103 (2006) &lbrack;[arXiv:math.GT/0501487](http://arxiv.org/abs/math.GT/0501487), [doi:10.1142/S0129055X06002875](https://doi.org/10.1142/S0129055X06002875)&rbrack;

* [[Ulrich Bunke]], [[Markus Spitzweck]], [[Thomas Schick]], _Periodic twisted cohomology and T-duality_, Ast&#233;risque No. 337 (2011), vi+134 pp. ISBN: 978-2-85629-307-2

A refined version of this using [[smooth stacks]] is due to

* [[Ulrich Bunke]], [[Thomas Nikolaus]]: *T-Duality via Gerby Geometry and Reductions*,  Reviews in Mathematical Physics **27** 05 1550013 (2015)  &lbrack;[arXiv:1305.6050](http://arxiv.org/abs/1305.6050), [doi:10.1142/S0129055X15500130](https://doi.org/10.1142/S0129055X15500130)&rbrack;

* {#Nikolaus14} [[Thomas Nikolaus]], _[[T-Duality in K-theory and Elliptic Cohomology]]_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))

There is also [[C*-algebra|C*-algebraic]] version of toplogical T-duality, .e. in [[noncommutative topology]], which sees also topological T-duals in [[non-commutative geometry]]:

* [[Varghese Mathai]], [[Jonathan Rosenberg]], _T-Duality for Torus Bundles with H-Fluxes via Noncommutative Topology_ ([arXiv:hep-th/0401168](http://arxiv.org/abs/hep-th/0401168))

The equivalence of the [[C*-algebra|C*-algebraic]] to the Bunke-Schick version, when the latter exists, is discussed in

* Ansgar Schneider, _Die lokale Struktur von T-Dualitn&#228;tstripeln_ ([arXiv:0712.0260](https://arxiv.org/abs/0712.0260))

Introduction and review:

* [[Jonathan Rosenberg]], *Topology, $C^*$-algebras, and string duality*, Regional Conference Series in Mathematics **111**, Amer. Math. Soc. (2009)  &lbrack;[doi:10.1090/cbms/111](https://doi.org/10.1090/cbms/111), [ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:05632075&type=pdf&format=complete)&rbrack;

* §1 in [Waldorf 2022](#Waldorf22) 


Another discussion that instead of [[noncommutative geometry]] uses [[topological groupoids]] is in 

* Calder Daenzer, _A groupoid approach to noncommutative T-duality_ ([arXiv:0704.2592](http://arxiv.org/abs/0704.2592))

Comments in relation to [[T-folds]]:

* [[Peter Bouwknegt]], [[Ashwin S. Pande]], *Topological T-duality and T-folds*, Advances in Theoretical and Mathematical Physics **13** 5 (2009) &lbrack;[arXiv:0810.4374](https://arxiv.org/abs/0810.4374), [doi:10.4310/ATMP.2009.v13.n5.a6](https://dx.doi.org/10.4310/ATMP.2009.v13.n5.a6)&rbrack;


The [[bi-brane]] perspective on T-duality is amplified in

* {#SarkissianSchweigert08} Gor Sarkissian, [[Christoph Schweigert]], _Some remarks on defects and duality_ ([arXiv:0810.3159](http://arxiv.org
/abs/0810.3159))

Discussion for non-free torus actions (physically: [[KK-monopoles]]) is in

* {#Pande06} [[Ashwin S. Pande]], _Topological T-duality and Kaluza-Klein Monopoles_, Adv. Theor. Math. Phys. **12** (2007) 185-215 &lbrack;[arXiv:math-ph/0612034](https://arxiv.org/abs/math-ph/0612034), [doi:10.4310/ATMP.2008.v12.n1.a3](https://dx.doi.org/10.4310/ATMP.2008.v12.n1.a3)&rbrack;

Discussion in [[rational homotopy theory]]/[[dg-geometry]] is in

* [[Ernesto Lupercio]], Camilo Rengifo, [[Bernardo Uribe]], _T-duality and exceptional generalized geometry through symmetries of dg-manifolds_ ([arXiv:1208.6048](https://arxiv.org/abs/1208.6048))

and a derivation of the rules of topological T-duality from analysis of the [[super p-brane]] super-cocycles in super rational homotopy theory (with a [[doubled supergeometry]]) is given in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: *[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]*, Adv. Theor. Math. Phys **22** 5 (2018) &lbrack;[arXiv:1611.06536](https://arxiv.org/abs/1611.06536), [doi:10.4310/ATMP.2018.v22.n5.a3](https://dx.doi.org/10.4310/ATMP.2018.v22.n5.a3)&rbrack;

reviewed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:T-duality in rational homotopy theory via strong homomotopy Lie algebras]]_, [Geometry, Topology and Mathematical Physics Journal, Volume 1 (2018)](http://geo-top.org/GTMP/index.php/volume-1-2018/)  ([arXiv:1712.00758](https://arxiv.org/abs/1712.00758))

* {#Fiorenza18} [[Domenico Fiorenza]], _T-duality in rational homotopy theory_, talk at _[38th Srni Winter School on Geometry and Physics](http://conference.math.muni.cz/srni/files/archiv/2018/)_, 2018 ([[FiorenzaSrni2018.pdf:file]])

and further expanded on on

* [[Hisham Sati]], [[Urs Schreiber]], p. 7 of: *[[schreiber:Cyclification of Orbifolds]]* &lbrack;[arXiv:2212.13836](https://arxiv.org/abs/2212.13836)&rbrack;

See also:

* [[Domenico Fiorenza]], Mattia Coloma, [[Eugenio Landi]]: _A very short note on the (rational) graded Hori map_, Communications in Algebra **50** 5 (2022) &lbrack;[arXiv:2003.13066](https://arxiv.org/abs/2003.13066), [doi:10.1080/00927872.2021.2005076](https://doi.org/10.1080/00927872.2021.2005076)&rbrack;


Comprehensive discussion in [[higher differential geometry]]:

* {#Alfonsi19} [[Luigi Alfonsi]], _Global Double Field Theory is Higher Kaluza-Klein Theory_, Fortsch. d. Phys. 2020 ([arXiv:1912.07089](https://arxiv.org/abs/1912.07089), [doi:10.1002/prop.202000010](https://doi.org/10.1002/prop.202000010))

  (relating [[Kaluza-Klein compactification]] on [[principal ∞-bundles]] to [[double field theory]], [[T-folds]], [[non-abelian T-duality]], [[type II geometry]], [[exceptional geometry]], ...)

* [[Luigi Alfonsi]], _The puzzle of global Double Field Theory: open problems and the case for a Higher Kaluza-Klein perspective_ ([arXiv:2007.04969](https://arxiv.org/abs/2007.04969))

See also:

* Ashwin S. Pande: *On Higher Topological T-duality Functors* &lbrack;[arXiv:2402.12039](https://arxiv.org/abs/2402.12039)&rbrack;



### Equivariant refinement

Discussion in the [[equivariant cohomology|equivariant]] generality, ie. as an equivalence of [[twisted equivariant K-theory]] groups:

* [[Tom Dove]], [[Thomas Schick]], *Equivariant Topological T-Duality* &lbrack;[arXiv:2310.06064](https://arxiv.org/abs/2310.06064)&rbrack;


### Geometric refinement
 {#ReferencesGeometricRefinement}

On possible geometric refinement of topological T-duality via some form of [[differential cohomology]]:

via [[differential K-theory]] classes:

* {#KahleValentino} [[Alexander Kahle]], [[Alessandro Valentino]], _[[T-Duality and Differential K-Theory]]_, Communications in Contemporary Mathematics, **16** 02 (2014) &lbrack;[arXiv:0912.2516](http://arxiv.org/abs/0912.2516), [doi:10.1142/S0219199713500144](https://doi.org/10.1142/S0219199713500144)&rbrack;
 
using [[adjusted Weil algebra|adjusted]] [[principal 2-connections]]:

* [[Hyungrok Kim]], [[Christian Saemann]], *Non-Geometric T-Duality as Higher Groupoid Bundles with Connections* &lbrack;[arXiv:2204.01783](https://arxiv.org/abs/2204.01783)&rbrack;

* {#Waldorf22} [[Konrad Waldorf]]: *Geometric T-duality: Buscher rules in general topology*,  Ann. Henri Poincaré **25** (2024) 1285–1358 &lbrack;[arXiv:2207.11799](https://arxiv.org/abs/2207.11799), [doi:10.1007/s00023-023-01295-0](https://doi.org/10.1007/s00023-023-01295-0)&rbrack;

* [[Hyungrok Kim]], [[Christian Saemann]], *T-duality as Correspondences of Categorified Principal Bundles with Adjusted Connections* &lbrack;[arXiv:2303.16162](https://arxiv.org/abs/2303.16162)&rbrack;



