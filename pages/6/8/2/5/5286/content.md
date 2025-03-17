
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For the actual relation to [[BV-complexes]] see at _[[relation between BV and BD]]_.

## Definition

+-- {: .num_defn}
###### Definition


A **Batalin-Vilkovisky algebra** or **BV-algebra** for short is

* a [[Gerstenhaber algebra]] $(A, \cdot, [-,-])$

* equipped with a unary [[linear operator]] $\Delta : A \to A$ of the same degree as the bracket

* such that

  1. $\Delta$ is a [[derivation]] for $[-,-]$;

  1. $[-,-]$ is the failure of $\Delta$ being a derivation for $\cdot$:

     $$
        [-,-] = \Delta \circ (-\cdot -) - (\Delta(-) \cdot - ) - (- \cdot \Delta(-))
      \,.
     $$

=--

+-- {: .num_defn}
###### Definition

A **$(n+1)$-BV algebra** is a similar structure with a BV-operator being of degree $n$ if $n$ is odd, and of degree $n/2$ if it is even.

=--

See ([Cohen-Voronov, def. 5.3.1, theorem 2.1.3](#CohenVoronov)) for details.



## Properties

+-- {: .num_theorem}
###### Theorem

The [[operad]] for BV-algebras is the [[homology]] of the [[framed little 2-disk operad]].

=--

This is due to ([Getzler](#Getzler))


+-- {: .num_theorem}
###### Theorem

The [[homology]] of an [[algebra over an operad]] over the [[framed little n-disk operad]] has a natural structure of an $(n+1)$-BV-algebra.

=--

This appears as ([CohenVoronov, theorem 5.3.3](#CohenVoronov)). The full [[homology]] of the [[framed little n-disk operad]] is described by ([Salvatore & Wahl, theorem 5.4](#SalvatoreWahl)).

## Examples

* On a [[smooth manifold]] $X$ with a [[volume form]] $\omega$ the operation of contraction with the volume form gives an [[isomorphism]] between [[differential form]]s and [[multivector field]]s. Under this isomorphism the de Rham differential on forms becomes a BV-operator on [[multivector field]]s. See there for more details.

Multivector fields may be identified with [[Hochschild cohomology]] in good cases (the [[Hochschild-Kostant-Rosenberg theorem]]). So the next example is a generalization of the previous one:

* {#ExampleHochschildCohomology} under good conditions, [[Hochschild cohomology]] (see there for details) carries a BV-algebra structure (eg. [Felix, Thomas & Vigué-Poirrier 2004](#FelixThomasVigue-Poirrier04); [Menichi 2009](#Menichi09); [Tradler 2008](#Tradler08))

## Related concepts

* [[Batalin-Vilkovisky module]]

* [[Poisson n-algebra]]

* [[homotopy BV-algebra]]

  * [[dg-BV-algebra]]

* [[BD-algebra]]

## References

The identification of BV-algebras as algebras over the homology of the framed little disk operad is due to

* [[Ezra Getzler]], _Batalin-Vilkovisky algebras and two-dimensional topological field theories_ , Comm. Math. Phys. 159 (1994), no. 2, 265&#8211;285. ([arXiv](http://arxiv.org/abs/hep-th/9212043))
{#Getzler}

The generalization to higher dimensional framed little disks is discussed in

* {#CohenVoronov} [[Ralph Cohen]], [[Alexander Voronov]], _Notes on string topology_ ([arXiv:math/0503625](http://arxiv.org/abs/math/0503625))


* {#SalvatoreWahl} [[Paolo Salvatore]], [[Nathalie Wahl]]:  _Framed discs operads and Batalin-Vilkovisky algebras_, The Quarterly Journal of Mathematics **54** 2 (2003) 213–231 &lbrack;[pdf](http://www.math.ku.dk/~wahl/SalvatoreWahl.pdf), [doi:10.1093/qmath/hag012](https://doi.org/10.1093/qmath/hag012)&rbrack;


There are examples coming from Lagrangian intersection theory:

* Vladimir Baranovsky, Victor Ginzburg, _Gerstenhaber-Batalin-Vilkoviski structures on coisotropic intersections_, [arxiv/0907.0037](http://arxiv.org/abs/0907.0037)


The BV-algebra structure on [[multivector fields]] on an [[oriented]] [[smooth manifold]] is discussed for instance in:

* {#CattaneoFiorenzaLongoni} [[Alberto Cattaneo]], [[Domenico Fiorenza]], Riccardo Longoni, Section 2 of: _On the Hochschild-Kostant-Rosenberg map for graded manifolds_, Int. Math. Res. Not. 2005, no. 62, 3899-3918 ([arXiv:math/0503380](http://arxiv.org/abs/math/0503380))


and 

* [[Claude Roger]], p. 6 of: *Gerstenhaber and Batalin-Vilkovisky algebras*, Archivum mathematicum, Volume 45 (2009), No. 4 ([pdf](http://www.emis.de/journals/AM/09-4/roger.pdf))


The BV-algebra structure on  [[Hochschild cohomology]]:

* {#FelixThomasVigue-Poirrier04} [[Yves Félix]], [[Jean-Claude Thomas]], [[Micheline Vigué-Poirrier]]: *The Hochschild cohomology of a closed manifold* Publ. Math. IH&#201;S Sci. **99** (2004) 235-252 &lbrack;[numdam:PMIHES_2004__99__235_0/](http://www.numdam.org/item/PMIHES_2004__99__235_0)&rbrack;


* {#Menichi09} [[Luc Menichi]], *Batalin-Vilkovisky algebra structures on Hochschild cohomology*, Bulletin de la Société Mathématique de France, **137** 2 (2009) 277-295
&lbrack;[arXiv:0711.1946](https://arxiv.org/abs/0711.1946), [numdam:BSMF_2009__137_2_277_0/](http://www.numdam.org/item/BSMF_2009__137_2_277_0/), [pdf](http://math.univ-angers.fr/perso/lmenichi/BV_Hochschild.pdf)&rbrack;

* {#Tradler08} [[Thomas Tradler]], *The BV Algebra on Hochschild Cohomology Induced by Infinity Inner Products*, Annales de l'institut Fourier **58** 7 (2008) 2351-2379 &lbrack;[arXiv:math/0210150](http://arxiv.org/abs/math/0210150)&rbrack;


There is a prominent class of examples coming from [[Lie-Rinehart algebras]]:

* [[Johannes Huebschmann]], _Lie-Rinehart algebras, Gerstenhaber algebras and Batalin-Vilkovisky algebras_, Annales de l'institut Fourier __48__:2 (1998) 425-440 [eudml](https://eudml.org/doc/75288)

[[!redirects BV-algebras]]

[[!redirects Batalin-Vilkovisky algebra]]
[[!redirects Batalin-Vilkovisky algebras]]