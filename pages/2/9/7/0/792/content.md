
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

The concept was introduced on the level of differential form data in

* {#BouwknegtEvslinMathai04} [[Peter Bouwknegt]], [[Jarah Evslin]], [[Varghese Mathai]], _T-Duality: Topology Change from H-flux_, Commun. Math. Phys. 249:383-415, 2004 ([hep-th/0306062](http://arxiv.org/abs/hep-th/0306062)) 

* {#BouwknegtHannabusMathai04} [[Peter Bouwknegt]], [[Keith Hannabus]], [[Varghese Mathai]], _T-duality for principal torus bundles_, JHEP 0403 (2004) 018 ([hep-th/0312284](http://arxiv.org/abs/hep-th/0312284)) 

In these papers the $U(1)$-[[gerbe]] ([[circle 2-bundle with connection]]) does not appear, but an integral [[differential 3-form]], representing its [[Dixmier-Douady class]] does. Note that if the [[Eilenberg-MacLane spectrum|integral]] [[cohomology group]] $H^3(X,\mathbb{Z})$ of $X$ has [[torsion]] in dimension three, not all gerbes will arise in this way.  The formalization with the above data originates in 

* {#BunkeSchick04} [[Ulrich Bunke]], [[Thomas Schick]], _On the topology of T-duality_, Rev. Math. Phys. **17** (2005) 77-112 &lbrack;[arXiv:math/0405132](https://arxiv.org/abs/math/0405132), [doi:10.1142/S0129055X05002315](https://doi.org/10.1142/S0129055X05002315)&rbrack;

* {#BunkeRumpfSchick08} {#BunkeRumpfSchick08} [[Ulrich Bunke|U. Bunke]], P. Rumpf, [[Thomas Schick]], _The topology of $T$-duality for $T^n$-bundles_,  Rev. Math. Phys. **18** 1103 (2006) &lbrack;[arXiv:math.GT/0501487](http://arxiv.org/abs/math.GT/0501487)&rbrack;

* [[Ulrich Bunke]], [[Markus Spitzweck]], [[Thomas Schick]], _Periodic twisted cohomology and T-duality_, Ast&#233;risque No. 337 (2011), vi+134 pp. ISBN: 978-2-85629-307-2

A refined version of this using [[smooth stacks]] is due to

* [[Ulrich Bunke]], [[Thomas Nikolaus]], _T-Duality via Gerby Geometry and Reductions_ ([arXiv:1305.6050](http://arxiv.org/abs/1305.6050))

* {#Nikolaus14} [[Thomas Nikolaus]], _[[T-Duality in K-theory and Elliptic Cohomology]]_, talk at _String Geometry Network Meeting_, Feb 2014, ESI Vienna ([website](http://www.ingvet.kau.se/juerfuch/conf/esi14/esi14_34.html))

There is also [[C*-algebra|C*-algebraic]] version of toplogical T-duality, .e. in [[noncommutative topology]], which sees also topological T-duals in [[non-commutative geometry]]:

* [[Varghese Mathai]], [[Jonathan Rosenberg]], _T-Duality for Torus Bundles with H-Fluxes via Noncommutative Topology_ ([arXiv:hep-th/0401168](http://arxiv.org/abs/hep-th/0401168))

The equivalence of the [[C*-algebra|C*-algebraic]] to the Bunke-Schick version, when the latter exists, is discussed in

* Ansgar Schneider, _Die lokale Struktur von T-Dualitn&#228;tstripeln_ ([arXiv:0712.0260](https://arxiv.org/abs/0712.0260))

Jonathan Rosenberg has also written a little introductory book for mathematicians:

* [[Jonathan Rosenberg]], _Topology, $C^*$-algebras, and string duality_ ([ZMATH](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:05632075&type=pdf&format=complete))

Another discussion that instead of [[noncommutative geometry]] uses [[topological groupoids]] is in 

* Calder Daenzer, _A groupoid approach to noncommutative T-duality_ ([arXiv:0704.2592](http://arxiv.org/abs/0704.2592))

The [[bi-brane]] perspective on T-duality is amplified in

* {#SarkissianSchweigert08} Gor Sarkissian, [[Christoph Schweigert]], _Some remarks on defects and duality_ ([arXiv:0810.3159](http://arxiv.org
/abs/0810.3159))

Discussion for non-free torus actions (physically: [[KK-monopoles]]) is in

* {#Pande06} Ashwin S. Pande, _Topological T-duality and Kaluza-Klein Monopoles_, Adv. Theor. Math. Phys., 12, (2007), pp 185-215 ([arXiv:math-ph/0612034](https://arxiv.org/abs/math-ph/0612034))

Discussion in [[rational homotopy theory]]/[[dg-geometry]] is in

* [[Ernesto Lupercio]], Camilo Rengifo, [[Bernardo Uribe]], _T-duality and exceptional generalized geometry through symmetries of dg-manifolds_ ([arXiv:1208.6048](https://arxiv.org/abs/1208.6048))

and a derivation of the rules of topological T-duality from analysis of the [[super p-brane]] super-cocycles in super rational homotopy theory (with a [[doubled supergeometry]]) is given in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]_, [ATMP Volume 22 (2018) Number 5](http://www.intlpress.com/site/pub/pages/journals/items/atmp/content/vols/0022/0005/) ([arXiv:1611.06536](https://arxiv.org/abs/1611.06536), [doi:10.4310/ATMP.2018.v22.n5.a3](https://dx.doi.org/10.4310/ATMP.2018.v22.n5.a3))

reviewed in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:T-duality in rational homotopy theory via strong homomotopy Lie algebras]]_, [Geometry, Topology and Mathematical Physics Journal, Volume 1 (2018)](http://geo-top.org/GTMP/index.php/volume-1-2018/)  ([arXiv:1712.00758](https://arxiv.org/abs/1712.00758))

* {#Fiorenza18} [[Domenico Fiorenza]], _T-duality in rational homotopy theory_, talk at _[38th Srni Winter School on Geometry and Physics](http://conference.math.muni.cz/srni/files/archiv/2018/)_, 2018 ([[FiorenzaSrni2018.pdf:file]])

See also

* [[Domenico Fiorenza]], Mattia Coloma, Eugenio Landi, _A very short note on the (rational) graded Hori map_ ([arXiv:2003.13066](https://arxiv.org/abs/2003.13066))


Comprehensive discussion in [[higher differential geometry]]:

* {#Alfonsi19} [[Luigi Alfonsi]], _Global Double Field Theory is Higher Kaluza-Klein Theory_, Fortsch. d. Phys. 2020 ([arXiv:1912.07089](https://arxiv.org/abs/1912.07089), [doi:10.1002/prop.202000010](https://doi.org/10.1002/prop.202000010))

  (relating [[Kaluza-Klein compactification]] on [[principal ∞-bundles]] to [[double field theory]], [[T-folds]], [[non-abelian T-duality]], [[type II geometry]], [[exceptional geometry]], ...)

* [[Luigi Alfonsi]], _The puzzle of global Double Field Theory: open problems and the case for a Higher Kaluza-Klein perspective_ ([arXiv:2007.04969](https://arxiv.org/abs/2007.04969))



The refinement of topological T-duality to [[differential cohomology]], hence to an operation on the [[differential K-theory]] classes that model the [[RR-field]] is in

* {#KahleValentino} [[Alexander Kahle]], [[Alessandro Valentino]], _[[T-Duality and Differential K-Theory]]_, Communications in Contemporary Mathematics, Volume 16, Issue 02, April 2014 ([arXiv:0912.2516](http://arxiv.org/abs/0912.2516))
 



