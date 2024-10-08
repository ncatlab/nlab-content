
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category Theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition


A **cyclic set** is a [[presheaf]] on the _[[cyclic category]]_ (which is often called [[Connes' cyclic category]] though it is cocyclic, with the usual contravariant confusion), which is intermediate between a [[symmetric set]] and a [[simplicial set]]. With [[Set]] replaced by a general [[category]] one speaks of a _[[cyclic object]]_.

The concept of cyclic sets/objects is used in the description of the cyclic structure on [[Hochschild homology]]/[[Hochschild cohomology]] and hence for the discussion on [[cyclic homology]]/[[cyclic cohomology]].


Cyclic sets and more generally [[cyclic objects]] can be described in terms of standard generators: 

A $\mathbf{Z}$-cyclic object (synonym: [[paracyclic object]])in a [[category]] $C$ is a [[simplicial object]] $F_\bullet$ in $C$ together with a sequence of [[isomorphisms]] $t_n : F_n \rightarrow F_n$, $n\geq 1$, such that
$$\array{
\partial_i t_n = t_{n-1} \partial_{i-1},\,\, i \gt 0, &
\sigma_i t_n = t_{n+1} \sigma_{i-1},\,\, i \gt0, \\
\partial_0 t_n = \partial_n, & \sigma_0 t_n = t_{n+1}^2 \sigma_n,
}$$
where $\partial_i$ are boundaries, $\sigma_i$ are degeneracies. A $\mathbf Z$-cocyclic ([[paracocyclic object|paracocyclic]]) object in $C$ is a $\mathbf{Z}$-cyclic object in $C^{\mathrm{op}}$.
$\mathbf Z$-(co)cyclic object is (co)cyclic if,
in addition, $t_n^{n+1} = 1$

## Properties

### As a classifying topos

The [[category]] of cyclic sets, being a [[presheaf category]] is a [[topos]], and hence is the [[classifying topos]] for some [[geometric theory]]. This turns out to be the theory of [[abstract circles]] ([Moerdijk 96](#Moerdijk96)). 
A further analysis can be found in ([Caramello Wentzlaff 14](#CaramelloWentzlaff14)).
Accordingly there is an [[infinity-action]] of the [[circle group]] on the [[geometric realization]] of a cyclic set (see also [Drinfeld 03](#Drinfeld03)).

### Model category structure and $S^1$-equivariant homotopy theory
 {#ModelCategoryStructure}

There is a [[model category]]-structure on the category of
cyclic sets, which makes it a presentation for
$S^1$-[[equivariant homotopy theory]] ([Spalinski 95](#Spalinski95), [Blumberg 04](#Blumberg04)).

## Related concepts

* [[cyclic category]]

* [[cyclic cohomology]]

* [[cyclic space]], [[cyclotomic spectrum]]

* [[skew-simplicial set]], [[symmetric set]], [[simplicial set]]



## References

The original definition:

* {#Connes83} [[Alain Connes]], _Cohomologie cyclique et foncteurs $Ext^n$_, C.R.A.S. **296** (1983), S&#233;rie I, 953-958 [MR777584](https://mathscinet.ams.org/mathscinet-getitem?mr=777584) [Zbl0534.18009](https://zbmath.org/?q=an:0534.18009) ([pdf](https://alainconnes.org/wp-content/uploads/n83.pdf), [[Connes_CohomologieCyclique.pdf:file]]).

* [[Pierre Cartier]], Section 1.6 of: *Homologie cyclique : rapport sur des travaux récents de Connes, Karoubi, Loday, Quillen...*, Séminaire Bourbaki: volume 1983/84, exposés 615-632, Astérisque, no. 121-122 (1985), Exposé no. 621 ([numdam:SB_1983-1984__26__123_0](http://www.numdam.org/item/?id=SB_1983-1984__26__123_0))

Textbook account (in the generality of [[cyclic spaces]]):

* [[Jean-Louis Loday]], *Cyclic Spaces and $S^1$-Equivariant Homology* ([doi:10.1007/978-3-662-21739-9_7](https://link.springer.com/chapter/10.1007/978-3-662-21739-9_7))

  Chapter 7 in: *Cyclic Homology*, Grundlehren **301**, Springer 1992 ([doi:10.1007/978-3-662-21739-9](https://link.springer.com/book/10.1007/978-3-662-21739-9))

* {#Loday11} [[Jean-Louis Loday]], Section 3 of: _Free loop space and homology_, Chapter 4 in: Janko Latchev, Alexandru Oancea (eds.): *Free Loop Spaces in Geometry and Topology*, IRMA Lectures in Mathematics and Theoretical Physics **24**, EMS 2015 ([arXiv:1110.0405](https://arxiv.org/abs/1110.0405), [ISBN:978-3-03719-153-8](https://bookstore.ams.org/emsilmtp-24))

Exposition:

* {#Malkiewich15} [[Cary Malkiewich]]: *A visual introduction to cyclic sets and cyclotomic spectra*, talk at *Young Topologists Meeting* Lausanne, Switzerland (2015) &lbrack;[pdf](https://people.math.binghamton.edu/malkiewich/ytm_2015.pdf), [[Malkiewich-Cyclic.pdf:file]]&rbrack;



Discussion of the relation to [[simplicial sets]]:

* [[Alain Connes]], Caterina Consani, _Cyclic structures and the topos of simplicial sets_, [1309.0394](http://arxiv.org/abs/1309.0394)

* [[Julie Bergner|Julia E. Bergner]], Walker H. Stern, _Cyclic Segal Spaces_, arXiv:2409.11945 (2024). ([abstract](https://arxiv.org/abs/2409.11945))

The identification of the category of cyclic sets as the [[classifying topos]] for [[abstract circles]] is due to 

* {#Moerdijk96} [[Ieke Moerdijk]], _Cyclic sets as a classifying topos_, 1996 ([[MoerdijkCyclic.pdf:file]])

* {#CaramelloWentzlaff14} Olivia Caramello, Nicholas Wentzlaff, _Cyclic theories_, 2014 ([arXiv:1406.5479](http://arxiv.org/abs/1406.5479))

The resulting circle-action on the ([[geometric realization]] of) cyclic sets is also discussed in 

* {#Drinfeld03} [[Vladimir Drinfeld]], _On the notion of geometric realization_ ([arXiv:0304064](http://arxiv.org/abs/math/0304064))

The [[homotopy theory]] of cyclic sets and its relation to $S^1$-[[equivariant homotopy theory]] is discussed in 

* {#Spalinski95} J. Spalinski, _Strong homotopy theory of cyclic sets_, J. of Pure and Appl. Alg. 99 (1995), 35&#8211;52.

* {#Blumberg04} [[Andrew Blumberg]], _A discrete model of $S^1$-homotopy theory_ ([arXiv:math/0411183](http://arxiv.org/abs/math/0411183))

An old query is archived in $n$Forum [here](http://nforum.mathforge.org/discussion/5822/cyclic-set/?Focus=46240#Comment_46240).

There are fairly recent slides by Spalinski on the subject [here](http://www.mimuw.edu.pl/~cat09/slides/Spalinski.pdf), which also discuss relationships with [[dihedral sets]] and [[quaternionic set]]s, as studied by [[Loday]].


[[!redirects cyclic sets]]