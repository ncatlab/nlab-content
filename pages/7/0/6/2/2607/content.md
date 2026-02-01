
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Quantum systems
+--{: .hide}
[[!include quantum systems -- contents]]
=--
#### Linear algebra
+-- {: .hide}
[[!include higher linear algebra - contents]]
=--
#### Operator algebra
+-- {: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

\tableofcontents

## Idea

What is historically called the *matrix mechanics* formulation of [[quantum mechanics]] originates with [Heisenberg 1925](#Heisenberg1925) and is therefore also known as the *[[Heisenberg picture of quantum mechanics]]*. Here [[algebras]] of [[linear operators]] (naively: "[[matrices]]")  represent [[quantum observables]], and their non-trivial [[commutators]] reflect the *[[uncertainty principle]]* due to [Heisenberg 1927](#Heisenberg1927).

The complementary perspective is that of "[[wave mechanics]]", due to [Schrödinger 1926](quantum+mechanics#Schrödinger1926), now also called the *[[Schrödinger picture of quantum mechanics]]*.



## Over exotic ground rigs

To some extent, [[classical mechanics]] may be understood as a matrix mechanics akin to the situation in quantum mechanics, but with the *[[ground ring|ground]] [[rig]]* $R$ taken not to be that of the [[complex number]] $R \equiv \mathbb{C}$, but the [[tropical semiring]] $R \equiv \mathbb{R}_{min} \coloneqq \mathbb{R} \cup \{+\infty\}$, where the addition is $min$ and the multiplication is $+$.  

Similarly, [[statistical mechanics]], or rather *thermal statics*, may be understood as matrix mechanics over a [[rig]] $\mathbb{R}^T$ that depends on a [[temperature]] parameter $T$. As $T \to 0$, the rig $\mathbb{R}^T$ reduces to $\mathbb{R}_{min}$ and thermal statics reduces to classical statics, just as quantum dynamics reduces to classical dynamics as [[Planck's constant]] approaches zero.



## References

### General

The origin of the "matrix mechanics" formulation of [[quantum mechanics]] is:

* {#Heisenberg1925} [[Werner Heisenberg]]: *Über quantentheoretische Umdeutung kinematischer und mechanischer Beziehungen*, Zeitschrift für Physik **33** (1925) 879–893 &lbrack;[doi:10.1007/BF01328377]( https://doi.org/10.1007/BF01328377), [Engl. pdf](http://users.mat.unimi.it/users/galgani/arch/heis25ajp.pdf)&rbrack;

which however did not use the term "[[matrix]]" (which was not widely known then). The actual [[matrices]] in matrix mechanics were identified in:

* [[Max Born]], [[Pascual Jordan]]: *Zur Quantenmechanik*, Zeitschrift für Physik **34** (1925) 858–888 &lbrack;[doi:10.1007/BF01328531](https://doi.org/10.1007/BF01328531)&rbrack;

* [[Max Born]], [[Werner Heisenberg]], [[Pascual Jordan]]: *Zur Quantenmechanik. II.*, Z. Physik **35** (1926) 557–615 &lbrack;[doi:10.1007/BF01379806](https://doi.org/10.1007/BF01379806)&rbrack;

Original derivation of the [[uncertainty principle]] from non-trivial [[commutators]] of these "matrices":

* {#Heisenberg1927} [[Werner Heisenberg]]: *Über den anschaulichen Inhalt der quantentheoretischen Kinematik und Mechanik*, Zeitschrift f&uuml;r Physik **43** (1927) 172–198 &lbrack;[doi:10.1007/BF01397280](https://doi.org/10.1007/BF01397280), [pdf](https://people.isy.liu.se/jalar/kurser/QF/references/Heisenberg1927.pdf)&rbrack;
  > (where it is announced as equation (1) and established as equation (6))

with English translation (or something close) in 

* *The actual content of quantum theoretical kinematics and mechanics*, NASA Technical Memorandum [NAS 1.15:77379](https://ntrs.nasa.gov/citations/19840008978) (1983) &lbrack;[pdf](https://ntrs.nasa.gov/api/citations/19840008978/downloads/19840008978.pdf), [[Heisenberg-ActualContent.pdf:file]]&rbrack;

Historical review:

* Marco Giliberti, Luisa Lovisetti: *Matrix Mechanics*, chapter in: Old *Quantum Theory and Early Quantum Mechanics*, Springer (2024) 397–429 &lbrack;[doi:10.1007/978-3-031-57934-9_11](https://doi.org/10.1007/978-3-031-57934-9_11)&rbrack;

See also: 

* Wikipedia: *[Matrix mechanics](https://en.wikipedia.org/wiki/Matrix_mechanics)*



### Over other ground rigs

Discussion of classical/statistical mechanics as matrix mechanics over [[tropical semiring|tropical]] ground [[rigs]]:

* [Quantization and Cohomology: Week 12](http://golem.ph.utexas.edu/category/2007/01/quantization_and_cohomology_we_11.html)

* [Quantization and Cohomology: Week 13](http://golem.ph.utexas.edu/category/2007/02/quantization_and_cohomology_we_12.html#c007500)

* [superposition in classical mechanics](http://golem.ph.utexas.edu/category/2006/12/talks_at_higher_categories_and.html#c006955) 

* [Baez-Corfield discussion](http://math.ucr.edu/home/baez/qg-spring2004/discussion.html#idempotent)
* [discussion continued - homotopy theory as groupoid valued mechanics](http://golem.ph.utexas.edu/category/2007/06/cohomology_and_quantization_we.html#c022847)

* [Geometric Representation Theory (Lecture 12)](http://golem.ph.utexas.edu/category/2007/11/geometric_representation_theor_11.html)


[[!redirects matrix mechanics]]
