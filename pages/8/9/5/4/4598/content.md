
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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


The _Pontryagin classes_ are [[characteristic class]]es on the [[classifying space]] [[BO(n)|$B O(n)$]] of the [[orthogonal group]]
and, by pullback, on the base of any bundle with structural group the
[[orthogonal group]]. The latter is where they were originally defined.

The analogs for the [[unitary group]] are the [[Chern class]]es.

## Definition

The universal Pontryagin [[characteristic classes]] $P_k$ on the [[classifying space]] [[BO(n)|$B O(n)$]] are, up to a sign, the pullbacks of the [[Chern classes]] $c_{2k}$ along the [[complexification]] inclusion into the [[classifying space]] [[BU(n)|$B U(n)$]] 

$$
  B O(n) \to B U(n)
  \,.
$$

## Properties

### As generating universal characteristic classes

The torsion-free quotient of the [[cohomology ring]] $H^\bullet(B SO(2n+1), \mathbb{Z})$
is the [[polynomial ring]] on  all Pontryagin classes
$\{P_i\}_{i = 1}^n$. The torsion is generated by [[Bockstein homomorphism | Bockstein]] images of $H^\bullet(BSO(2n+1);\mathbb{F}_2)$, which is generated by the [[Stiefel-Whitney classes]].

The torsion-free quotient of the [[cohomology ring]] $H^\bullet(B SO(2n), \mathbb{Z})$
is the [[quotient]] of the [[polynomial ring]] on  Pontryagin classes
$P_i$ and the [[Euler class]] $\chi$ by the relation $\chi^2 = P_n$; again the torsion is generated by Bocksteins of monomials in the Stiefel&ndash;Whitney classes.

### Further relation to Chern classes
 {#FurtherRelationToChernClasses}

Under the other canonical map

$$
  j \;\colon\; B U(n) \to BO(2n)
$$

one has 

$$
  j^\ast(P_k) = \sum_{a + b = 2 k} (-1)^{a+k} c_a c_b
$$

and

$$
  j^\ast(\chi) = c_n
  \,.
$$

### Splitting principle and Chern roots
 {#SplittingPrincipleAndChernRoots}

Under the inclusion

$$
  i \;\colon\; U(1)^n \hookrightarrow U(n) \to O(2n)
$$

of the [[maximal torus]] one has that 

$$
  (B i)^\ast(P_k) = \sigma_k(x_1, \cdots, x_n)^2
$$

and

$$
  (B i)^\ast(\chi) = \sigma_n(x_1, \cdots, x_n)
$$

where the $x_i \in H^\bullet(B U(1)^n, \mathbb{Z})$ are the "[[Chern roots]]". 

See at _[Chern class - Properties -- Splitting principle and Chern roots](Chern%20class#SplittingPrinciple)_ and at _[splitting principle - Examples - Real vector bundles](splitting+principle#RealVectorBundles)_ for more.




[[!include Chern- and Pontrjagin forms -- section]]






## Trivializations and structures

The [[twisted differential c-structures]] corresponding to Pontryagin class include

* [[twisted differential string structure]] for the first fractional Pontryagin class $\frac{p_1}{2} : B Spin \to B^3 U(1)$;

* [[twisted differential fivebrane structure]] for the second fractional Pontryagin class $\frac{1}{6}p_2 : B String \to B^7 U(1)$.

## Related concepts

* [[Pontrjagin character]]

* [[p1-structure]], [[string structure]], [[fivebrane structure]]

* [[shifted C-field flux quantization]]

* [[Stiefel-Whitney class]], [[Wu class]], [[one-loop anomaly polynomial I8]]

* [[Chern class]]

* [[Stiefel-Whitney class]]

* [[Chern character]]

* [[orthogonal calculus]]

* [[quaternionic oriented cohomology theory]]

## References

### General

The original definition is in

* [[Л. С. Понтрягин]], _Характеристические циклы многообразий_, ДАН, XXXV, № 2 (1942), 35–39.
English translation: _Characteristic Cycles of Manifolds_.  L. S. Pontryagin Selected Works.  Volume 1.  Selected Research Papers.  Edited by R. V. Gamkrelidze.  CRC Press, 1986.  283–287.  [doi](https://doi.org/10.1201/9780367813758).

* [[Л. С. Понтрягин]], _Характеристические циклы дифференцируемых многообразий_, Матем. сб., 21(63):2 (1947), 233–284.  [MathNet.Ru PDF](http://mi.mathnet.ru/msb6237 ).
English translation by A. A. Brown: [[Lev Pontrjagin]], _Characteristic cycles on differentiable manifolds_, Mat. Sbornik N. S. 21(63) (1947), 233-284; A.M.S. Translation 32 (1950).  [PDF](https://www.maths.ed.ac.uk/~v1ranick/papers/pont4.pdf).
English translation by P. S. V. Naidu:
_Characteristic Cycles of Differentiable Manifolds_.  L. S. Pontryagin Selected Works.  Volume 1.  Selected Research Papers.  Edited by R. V. Gamkrelidze.  CRC Press, 1986.  375–433.  [doi](https://doi.org/10.1201/9780367813758).

Early accounts:

* {#Hirzebruch56} [[Friedrich Hirzebruch]], Chapter 1, Section 4 of: _Neue topologische Methoden in der Algebraischen Geometrie_, Ergebnisse der Mathematik und Ihrer Grenzgebiete. 1. Folge, Springer 1956 ([doi:10.1007/978-3-662-41083-7](https://www.springer.com/de/book/9783662406052))


Classical textbook references are


* {#KobayashiNomizu63} [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], Section  XII.4 in: _Foundations of Differential Geometry, Volume 1_, Wiley 1963 ([web](https://www.zuj.edu.jo/download/foundations-of-differential-geometry-vol-1-kobayashi-nomizu-pdf/), [ISBN:9780471157335](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+Volume+1-p-9780471157335), [Wikipedia](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry))


* [[John Milnor]], [[Jim Stasheff]], _Characteristic classes_, Princeton Univ. Press 1974 ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76), [doi:10.1515/9781400881826](https://doi.org/10.1515/9781400881826), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnstas.pdf))

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

With an eye towards [[mathematical physics]]:

* [[Mikio Nakahara]], Section 11.4.1 of: *[[Geometry, Topology and Physics]]*, IOP 2003 ([doi:10.1201/9781315275826](https://doi.org/10.1201/9781315275826), <a href="http://alpha.sinp.msu.ru/~panov/LibBooks/GRAV/(Graduate_Student_Series_in_Physics)Mikio_Nakahara-Geometry,_Topology_and_Physics,_Second_Edition_(Graduate_Student_Series_in_Physics)-Institute_of_Physics_Publishing(2003).pdf">pdf</a>)


* {#RudolphSchmidt} [[Gerd Rudolph]], [[Matthias Schmidt]], around Def. 4.2.19 in: _Differential Geometry and Mathematical Physics: Part II. Fibre Bundles, Topology and Gauge Fields_, Theoretical and Mathematical Physics series, Springer 2017 ([doi:10.1007/978-94-024-0959-8](https://link.springer.com/book/10.1007/978-94-024-0959-8))


See also

* Paul Bressler, _The first Pontryagin class_, [math.AT/0509563](http://arxiv.org/abs/math/0509563)

* Ivan Panin, Charles Walter, _Quaternionic Grassmannians and Pontryagin classes in algebraic geometry_, [arxiv/1011.0649](http://arxiv.org/abs/1011.0649)

A brief introduction is in chapter 23, section 7 

* [[Peter May]], _A concise course in algebraic topology_ ([pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

### Relation to gravitational instantons

First Pontrjagin class as counting [[gravitational instanton number]]:

* {#EguchiFreund67} [[Tohru Eguchi]], [[Peter Freund]], _Quantum Gravity and World Topology_, Phys. Rev. Lett. 37, 1251 (1967) ([doi:10.1103/PhysRevLett.37.1251](https://doi.org/10.1103/PhysRevLett.37.1251))

* {#BelavinBurlankov76} [[Alexander Belavin]], D. Burlankov, _The renormalisable theory of gravitation and the Einstein equations_, Physics Letters A Volume 58, Issue 1, 26 July 1976, Pages 7-8 (<a href="https://doi.org/10.1016/0375-9601(76)90530-2">doi:10.1016/0375-9601(76)90530-2</a>)

* Serdar Nergiz, Cihan Saclioglum, equation (27) in: _A Quasiperiodic Gibbons--Hawking Metric and Spacetime Foam_, Phys. Rev. D 53, 2240 (1996) ([arXiv:hep-th/9505141](https://arxiv.org/abs/hep-th/9505141))


[[!redirects Pontryagin classes]]

[[!redirects Pontrjagin class]]
[[!redirects Pontrjagin classes]]

[[!redirects first Pontryagin class]]
[[!redirects second Pontryagin class]]
[[!redirects first Pontrjagin class]]
[[!redirects second Pontrjagin class]]


[[!redirects first fractional Pontryagin class]]
[[!redirects first fractional Pontrjagin class]]


[[!redirects second fractional Pontryagin class]]
[[!redirects second fractional Pontrjagin class]]



[[!redirects fractional first Pontryagin class]]
[[!redirects fractional second Pontryagin class]]

