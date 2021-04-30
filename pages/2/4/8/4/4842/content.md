
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Knot theory
+-- {: .hide}
[[!include knot theory - contents]]
=--
=--
=--



# Vassiliev knot invariants
* table of contents
{: toc}

## Idea ##

The space of [[knots]] in the [[Euclidean space]] $\mathbb{R}^3$ (or in the [[3-sphere]] $S^3$) is an [[open subset|open]] [[submanifold]] of the [[smooth loop space]].  [[knot invariant|Knot invariants]] are [[locally constant functions]] on this manifold.  The [[complement]] of the space of knots is called the [[discriminant]] and consists of all [[singular knots]].

If we consider those singular knots with only a finite number of double points, we can build a [[cubical complex]] from this data.  The vertices in the complex are labelled by the isotopy classes of knots, and more generally the $n$-cubes by the isotopy classes of singular knots with $n$ double points (and a few other technical pieces of information).  The boundary operator resolves a double crossing either upwards or downwards according to the orientation at the crossing.

A **Vassiliev invariant** is simply a cubical morphism from this complex to an abelian group that vanishes above a certain degree.

## Definition ##

One does not need the language of cubical complexes to _define_ Vassiliev invariants.  Rather, there is a general method whereby a [[knot invariant]] can be extended to all [[singular knots]] with only finitely many double points (and no other singularities) using the [[Vassiliev skein relations]].


+-- {: .num_defn #vinv}
###### Definition

A **Vassiliev invariant** of degree (or order) $\le n$ is a knot invariant whose extension to singular knots (with double points) vanishes on all singular knots with more than $n$ double points.

=--

As is standard, it is of degree $n$ if it is of degree $\le n$ but not $\le n - 1$.  Vassiliev invariants are also called **finite type invariants**.


+-- {: .num_remark}
###### Remark


The degree of Vassiliev invariants defines a filtration on the space of knots (and more particularly, on the [[algebra of knots]]).  Two knots are $n$-equivalent if all the Vassiliev invariants of degree $\le n$ agree on them.  In particular, a knot that is $n$-equivalent to the unknot is said to be $n$-trivial.

=--

## Properties

### Relation to Chord diagrams and weight systems

A function which is constant on nonsingular knots may be extended to a Vassiliev invariant of degree 0 by applying the [[Vassiliev skein relations]], and conversely, any Vassiliev invariant of degree 0 must be constant on nonsingular knots.  Likewise, any Vassiliev invariant of degree 1 must be constant on nonsingular knots.


Any [[singular knot]] $f : S^1 \to \mathbb{R}^3$ with $n$ distinct double points $x_1,\dots,x_n \in \mathbb{R}^3$ gives rise to a [[chord diagram]] of order $n$, consisting of the circle $S^1$ with a chord connecting each pair of points $f^{-1}(x_1), \dots, f^{-1}(x_n)$.

The importance of this construction for singular knots comes from the fact that any finite type invariant determines a function on chord diagrams:

+-- {: .un_theorem}
######Theorem 

Let $v$ be a Vassiliev invariant of degree $\le n$.  Then the value of $v$ on a singular knot with $n$ distinct double points depends only on the [[chord diagram]] of the singular knot, and not on the knot itself.

=-- 

Conversely, one can ask which functions on chord diagrams come from finite type invariants.  The answer is that Vassiliev invariants (of degree $\le n$) can essentially be identified with _[[weight systems]]_ (of order $n$), which are functions on chord diagrams (of order $n$) satisfying two properties called the "[[1T relation]]" (or "framing independence") and the "[[4T relation]]": see Theorem 1 of [Bar-Natan 95](#BarNatan95) (or Theorem 6.2.13 of [Lando & Zvonkin](#LandoZvonkin)):




+-- {: .num_prop #WeightSystemsAreAssociatedGradedOfVassilievInvariants}
###### Proposition
**([[weight systems are associated graded of Vassiliev invariants]])**

For [[ground field]] $k = \mathbb{R}, \mathbb{C}$ the [[real numbers]] or [[complex numbers]], there is for each [[natural number]] $n \in \mathbb{N}$ a canonical [[linear isomorphism]]

$$
  \mathcal{V}_n/\mathcal{V}_{n-1}
  \underoverset{\simeq}{\phantom{AAAA}}{\longrightarrow}
  \big( 
    \mathcal{A}_n^u
  \big)^\ast
$$

from 

1. the [[quotient vector space]] of order-$n$ [[Vassiliev invariants]] of [[knots]] by those of order $n-1$ 

1. to the space of [[unframed weight systems]] of order $n$.

In other words, in [[characteristic zero]], the [[graded vector space]] of [[unframed weight systems]] is the [[associated graded vector space]] of the [[filtered vector space]] of [[Vassiliev invariants]].

=--

([Bar-Natan 95, Theorem 1](#BarNatan95), following [Kontsevich 93](#Kontsevich93))


### Relation to homology of loop spaces of configuration spaces of points
  {#RelationToHomologOfLoopSpacesOfConfigurationSpaces}

We discuss the relation between Vassiliev invariants and the [[Euler characteristic]] of the [[ordinary homology]] of [[loop spaces]] of [[configuration spaces of points]]:

For $n, q \in \mathbb{N}$ and $q \geq 1$, write 

1. $\underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{q+2} \big)$ for the [[configuration space of points|configuration space of n ordered points]] in [[Euclidean space]] $\mathbb{R}^{q+2}$;

1. $\Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{q+2} \big)$ for the corresponding [[based loop space]] (for any choice of base point);

1. $H_\bullet\Big(\Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{q+2} \big), \mathbb{C} \Big)$ for the [[ordinary homology]] of this loop space, with [[coefficients]] in the [[complex numbers]];

1. $\chi H_\bullet\Big(\Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{q+2} \big), \mathbb{C} \Big)$ for the [[Euler characteristic]]-series of the homology 


Write also

1. $V^n_k$ for the [[complex vector space]] of [[Vassiliev invariants]] of order $k$ for [[pure braids]] with $n$ strands;;

1. $A^n_k$ for the [[complex vector space]] spanned by the horizontal [[chord diagrams]] with $n$ vertical strands modulo the "horizontal 4T relation"

such that there is an [[linear isomorphism]]

$$
  V^n_k/V^n_{k-1}
  \simeq
  (A^n_k)^\ast
$$

between the [[quotient vector space]] of [[Vassiliev invariants]] and the [[dual vector space]] of [[chord diagrams]].

Then:

The [[Euler characteristic]]-series (...) of the homology of the loop spaces of configuration spaces 

$$
  \chi H_\bullet\Big(\Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{q+2} \big), \mathbb{C} \Big)
  \;=\;
  \Big[
  \big(
    1 - t^q
  \big)
  \cdot 
  \big(
    1 - 2 t^q
  \big)
  \cdots
  \big(
    1 - (n-1) t^q
  \big)
  \Big]^{-1}
$$

and is related to the complex [[dimensions]] of spaces of Vassiliev invariants according to 

\[
  \label{HomotopyOfOmegaConfR3IsBraidVassiliev}
  \chi 
  H_\bullet
  \Big(
    \Omega \underset{{}^{\{1,\cdots, n\}}}{Conf}\big( \mathbb{R}^{3} \big), \mathbb{C} 
  \Big)
  \;=\;
  \underset{k \in \mathbb{N}}{\sum}
  dim_{\mathbb{C}}\big( A^n_k \big) 
  t^k
\]

([Cohen-Gitler 01, Prop. 9.1](#CohenGitler01), based on [Cohen 76](#Cohen76) and [Kohno 94](#Kohno94))

\linebreak

Alternatively, we have the combination of the following two facts, via [[weight systems]]:


+-- {: .num_prop #WeightSystemsAreCohomologyOfLoopSpaceOfConfigurationSpace}
###### Proposition
**([[weight systems are cohomology of loop space of configuration space]])**

For [[ground field]] $k = \mathbb{R}$ the [[real numbers]], 
there is a canonical [[injection]] of the [[real vector space]] $\mathcal{W}$ of [[framed weight systems]] (eq:SpaceOfWeightSystemsAsLinearDual) into the [[real cohomology]] of the [[based loop spaces]] of the ordered [[configuration spaces of points]] in 3-[[dimension|dimensional]] [[Euclidean space]]:

$$
  \mathcal{W}
  \;\overset{\;\;\;\;}{\hookrightarrow}\;
  H^\bullet
  \Big(
    \Omega 
    \underset{{}^{\{1,\cdots,n\}}}{Conf}
    \big(
      \mathbb{R}^3 
    \big)
  \Big)
$$

=--

This is stated as [Kohno 02, Theorem 4.2](#Kohno02).

+-- {: .num_prop #WeightSystemsAreAssociatedGradedOfVassilievInvariants}
###### Proposition
**([[weight systems are associated graded of Vassiliev invariants]])**

For [[ground field]] $k = \mathbb{R}, \mathbb{C}$ the [[real numbers]] or [[complex numbers]], there is for each [[natural number]] $n \in \mathbb{N}$ a canonical [[linear isomorphism]]

$$
  \mathcal{V}_n/\mathcal{V}_{n-1}
  \underoverset{\simeq}{\phantom{AAAA}}{\longrightarrow}
  \big( 
    \mathcal{A}_n^u
  \big)^\ast
$$

from 

1. the [[quotient vector space]] of order-$n$ [[Vassiliev invariants]] of [[knots]] by those of order $n-1$ 

1. to the space of [[unframed weight systems]] of order $n$.

In other words, in [[characteristic zero]], the [[graded vector space]] of [[unframed weight systems]] is the [[associated graded vector space]] of the [[filtered vector space]] of [[Vassiliev invariants]].

=--

([Bar-Natan 95, Theorem 1](#BarNatan95), following [Kontsevich 93](#Kontsevich93))




## Examples

1. The $n$th coefficient of the [[Conway polynomial]] is a Vassiliev invariant of order $\le n$.

(...)

## Related concepts ## 

[[!include chord diagrams and weight systems -- table]]


* [[Kontsevich integral]]

* [[universal Vassiliev invariant]]

* [[knot theory]]

* [[Jones polynomial]]

* [[singularity]] 



## References 

### General

The original articles are

* [[Viktor Vassiliev]], _Complements of discriminants of smooth maps: topology and applications_, Amer. Math. Soc. 1992 ([ams:mmono-98](https://bookstore.ams.org/mmono-98))

* {#Kontsevich93} [[Maxim Kontsevich]], _Vassiliev's knot invariants_, Advances in Soviet Mathematics, Volume 16, Part 2, 1993 ([pdf](http://pagesperso.ihes.fr/~maxim/TEXTS/VassilievKnot.pdf), [[KontsevichVassilievInvariants93.pdf:file]])

* {#BarNatan95} [[Dror Bar-Natan]], _On the Vassiliev knot invariants_, Topology Volume 34, Issue 2, April 1995, Pages 423-472 (<a href="https://doi.org/10.1016/0040-9383(95)93237-2">doi:10.1016/0040-9383(95)93237-2</a>, [pdf](https://www.math.toronto.edu/drorbn/papers/OnVassiliev/OnVassiliev.pdf))

Lecture notes:

* {#BarNatanStoimenow97} [[Dror Bar-Natan]], Alexander Stoimenow, _The Fundamental Theorem of Vassiliev Invariants_ ([arXiv:q-alg/9702009](https://arxiv.org/abs/q-alg/9702009))

Textbook accounts:

* {#ChmutovDuzhinMostovoy11} [[Sergei Chmutov]], [[Sergei Duzhin]], [[Jacob Mostovoy]], _Introduction to Vassiliev knot invariants_, Cambridge University Press, 2012 ([arxiv:1103.5628](http://arxiv.org/abs/1103.5628), [doi:10.1017/CBO9781139107846](https://doi.org/10.1017/CBO9781139107846))

* [[David Jackson]], [[Iain Moffat]], _An Introduction to Quantum and Vassiliev Knot Invariants_, Springer 2019 ([doi:10.1007/978-3-030-05213-3](https://link.springer.com/book/10.1007/978-3-030-05213-3))

* {#Lescop20} [[Christine Lescop]], _Invariants of links and 3-manifolds from graph configurations_ ([arXiv:2001.09929](https://arxiv.org/abs/2001.09929))


Further review:




* [[Simon Willerton]], _On the Vassiliev invariants for knots and for pure braids_, 1997 ([hdl:1842/11581](http://hdl.handle.net/1842/11581), [ethos.663801](https://ethos.bl.uk/OrderDetails.do?uin=uk.bl.ethos.663801), [[WillertonVasdilievInvariants1997.pdf:file]])


* [[Dror Bar-Natan]], _Finite Type Invariants_, in:  J.-P. Francoise, G.L. Naber and Tsou S.T. (eds.) Encyclopedia of Mathematical Physics, Oxford: Elsevier, 2006, volume 2 page 340
([arXiv:math/0408182](https://arxiv.org/abs/math/0408182))



* {#LandoZvonkin} Sergei K. Lando and Alexander K. Zvonkin, Chapter 6 of: _Graphs on Surfaces and Their Applications_, Springer, 2004.



More literature is listed at

* [[Dror Bar-Natan]], [[Sergei Duzhin]], _[Bibliography of Vassiliev Invariants](http://www.pdmi.ras.ru/~duzhin/VasBib/Long)_

See also

* Mathworld, _[Vassiliev invariant](http://mathworld.wolfram.com/VassilievInvariant.html)_

Concrete computations:

* [[Jan Kneissler]], _On spaces of connected graphs I: Properties of Ladders_, Proc. Internat. Conf. "Knots in Hellas '98", Series on Knots and Everything, vol. 24 (2000), 252-273 ([arXiv:math/0301018](https://arxiv.org/abs/math/0301018))

* [[Jan Kneissler]], _On spaces of connected graphs II: Relations in the algebra Lambda_, Jour. of Knot Theory and its Ramif. vol. 10, no. 5 (2001), 667-674 ([arXiv:math/0301019](https://arxiv.org/abs/math/0301019))

* [[Jan Kneissler]], _On spaces of connected graphs III: The Ladder Filtration_, Jour. of Knot Theory and its Ramif. vol. 10, no. 5 (2001), 675-686 ([arXiv:math/0301020](https://arxiv.org/abs/math/0301020))

* [[Pierre Vogel]], _Algebraic structures on modules of diagrams_, Journal of Pure and Applied Algebra Volume 215, Issue 6, June 2011, Pages 1292-1339 ([pdf](https://webusers.imj-prg.fr/~pierre.vogel/diagrams.pdf))

### Relation to Jones polynomial:

Relation to the [[Jones polynomial]]:

* Joan S. Birman; Xiao-Song Lin, _Knot polynomials and Vassiliev's invariants_,  Inventiones mathematicae (1993) Volume: 111, Issue: 2, page 225-270 ([https://dml:144077](https://eudml.org/doc/144077))

Relation to other polynomial [[knot invariants]]:

* Myeong-Ju Jeong, Chan-Young Park, _Polynomial invariants and Vassiliev invariants_, Geom. Topol. Monogr. 4 (2002) 89-101 ([arxiv:math/0211045](https://arxiv.org/abs/math/0211045))

### Relation to homology of loop spaces of configuration spaces

Relation to the [[Euler characteristic]] of the [[ordinary homology]] of [[loop spaces]] of [[configuration spaces of points]]


* {#CohenGitler01} [[Fred Cohen]], [[Samuel Gitler]], _Loop spaces of configuration spaces, braid-like groups, and knots_, In: Jaume Aguadé, Carles Broto, [[Carles Casacuberta]]  (eds.) _Cohomological Methods in Homotopy Theory_. Progress in Mathematics, vol 196. Birkhäuser, Basel 2001 ([doi:10.1007/978-3-0348-8312-2_7](https://doi.org/10.1007/978-3-0348-8312-2_7))

based on 

* {#Kohno94} [[Toshitake Kohno]], _Vassiliev invariants and de Rham complex on the space of knots_, 
In: Yoshiaki Maeda, Hideki Omori and [[Alan Weinstein]] (eds.), _Symplectic Geometry and Quantization_, Contemporary Mathematics 179 (1994): 123-123 ([doi:10.1090/conm/179](http://dx.doi.org/10.1090/conm/179))

* {#Cohen76} [[Fred Cohen]], _The homology of $\mathcal{C}_{n+1}$-Spaces, $n \geq 0$. In: The Homology of Iterated Loop Spaces. Lecture Notes in Mathematics, vol 533. Springer, Berlin, Heidelberg  1976 ([doi:10.1007/BFb0080467](https://doi.org/10.1007/BFb0080467))

See also

* {#Kohno02} [[Toshitake Kohno]], _Loop spaces of configuration spaces and finite type invariants_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arXiv:math/0211056](https://arxiv.org/abs/math/0211056))


### As Chern-Simons amplitudes

Discussion of higher order Vassiliev invariants as [[Chern-Simons theory]]-[[correlators]], hence as [[configuration space of points|configuration space]]-[[integrals]] of [[wedge products]] of [[Chern-Simons propagators]] assigned to [[edges]] of [[Feynman diagrams]] in the [[graph complex]]:

* [Kontsevich 93, Section 5](#Kontsevich93)

* Daniel Altschuler, Laurent Freidel, _Vassiliev knot invariants and Chern-Simons perturbation theory to all orders_, Commun. Math. Phys. 187 (1997) 261-287 ([arxiv:q-alg/9603010](https://arxiv.org/abs/q-alg/9603010))


* [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Configuration spaces and Vassiliev classes in any dimension_, Algebr. Geom. Topol. 2 (2002) 949-1000 ([arXiv:math/9910139](https://arxiv.org/abs/math/9910139))

* [[Alberto Cattaneo]], Paolo Cotta-Ramusino, Riccardo Longoni, _Algebraic structures on graph cohomology_, Journal of Knot Theory and Its Ramifications, Vol. 14, No. 5 (2005) 627-640 ([arXiv:math/0307218](https://arxiv.org/abs/math/0307218))

Reviewed in:

* {#Volic13} [[Ismar Volić]], Section 4 of: _Configuration space integrals and the topology of knot and link spaces_, [Morfismos, Vol 17, no 2, 2013](https://fdocuments.co/amp/document/morfismos-vol-17-no-2-2013.html) ([arxiv:1310.7224](https://arxiv.org/abs/1310.7224))

See also

* J. de-la-Cruz-Moreno, H. García-Compeán, E. López, _Vassiliev Invariants for Flows Via Chern-Simons Perturbation Theory_ ([arXiv:2004.13893](https://arxiv.org/abs/2004.13893))



### As observables on fuzzy spheres

Relation of [[Dp-D(p+2)-brane bound states]] ([hence](Dp-Dp+2-brane+bound+states#ReferencesRelationToMonopoles)
[[Yang-Mills monopoles]]) to [[Vassiliev braid invariants]] via [[chord diagrams]] computing [[radii]] of [[fuzzy spheres]]:

* [[Sanyaje Ramgoolam]], [[Bill Spence]], S. Thomas, Section 3.2 of: _Resolving brane collapse with $1/N$ corrections in non-Abelian DBI_, Nucl. Phys. B703 (2004) 236-276 ([arxiv:hep-th/0405256](https://arxiv.org/abs/hep-th/0405256))

* [[Simon McNamara]], [[Constantinos Papageorgakis]], [[Sanyaje Ramgoolam]], [[Bill Spence]], Appendix A of: _Finite $N$ effects on the collapse of fuzzy spheres_, JHEP 0605:060, 2006 ([arxiv:hep-th/0512145](https://arxiv.org/abs/hep-th/0512145))

* [[Simon McNamara]], Section 4 of: _Twistor Inspired Methods in Perturbative FieldTheory and Fuzzy Funnels_, 2006 ([spire:1351861](http://inspirehep.net/record/1351861), [pdf](https://strings.ph.qmul.ac.uk/sites/default/files/Mcnamaraphd.pdf), [[McNamara06.pdf:file]])

* [[Constantinos Papageorgakis]], p. 161-162 of: _On matrix D-brane dynamics and fuzzy spheres_, 2006 ([[Papageorgakis06.pdf:file]])



### Vassiliev invariants of braids


Vassiliev invariants of [[braid group|braids]] via [[horizontal chord diagrams]]:

* {#BarNatan96} [[Dror Bar-Natan]], _Vassiliev and Quantum Invariants of Braids_, Geom. Topol. Monogr. 4 (2002) 143-160 ([arxiv:q-alg/9607001](https://arxiv.org/abs/q-alg/9607001))

* Louis Funar, _Vassiliev invariants I: Braid groups and rational homotopy theory_ ([arXiv:q-alg/9510008](https://arxiv.org/abs/q-alg/9510008))







category: geometry, topology

[[!redirects Vassiliev knot invariant]]
[[!redirects Vassiliev knot invariants]]


[[!redirects Vassiliev invariants]]

[[!redirects Vassiliev finite type invariants]]
[[!redirects Vassiliev finite type invariant]]
[[!redirects Vassiliev finite-type invariants]]
[[!redirects Vassiliev finite-type invariant]]
[[!redirects finite type invariants]]
[[!redirects finite type invariant]]
[[!redirects finite-type invariants]]
[[!redirects finite-type invariant]]

[[!redirects Vassiliev link invariant]]
[[!redirects Vassiliev link invariants]]

[[!redirects Vassiliev invariants of braids]]

[[!redirects Vassiliev braid invariant]]
[[!redirects Vassiliev braid invariants]]

