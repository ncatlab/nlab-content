
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of [[motives]] in algebraic geometry can be adapted to derived [[noncommutative geometry]]. The idea and the first version has been developed by [[Maxim Kontsevich]]. There is a remarkable observation that the [[category of Chow motives]] (after localizing at the [[Lefschetz motive]]) can be embedded into the category of Kontsevich's noncommutative motives. More recently this direction has been systematically studied by Cisinski and Tabuada. 

A second approach is due to [[Bertrand Toën]], [[Michel Vaquié]], [[Gabriele Vezzosi]].  They construct a [[motivic stable homotopy theory]] for [[noncommutative geometry|noncommutative spaces]] (in the sense of [[Kontsevich]]).

There is another approach by [[Arne Ostvaer]].

In [[noncommutative geometry]] &#224; la [[Alain Connes]], Connes and [[Matilde Marcolli]] have also introduced some motivic ideas. Marcolli also has a  recent collaboration with Tabuada on the algebraic side, see her [[Matilde Marcolli|webpage]].

## Definition 
 {#Definition}

### As the universal additive/localizing invariant
 {#AsUniversalAditiveInvariant}

The definition in ([Blumberg-Gepner-Tabuada 10](#BlumbergGepnerTabuada10)) is the following.



Write $Cat_\infty^{stab}$ for the [[(∞,1)-category]] of [[stable (∞,1)-categories]]. 

+-- {: .num_defn }
###### Definition

Say that 

* a [[Morita equivalence]] is a map in $Cat_\infty^{stab}$ which becomes an [[equivalence of (∞,1)-categories]] under [[idempotent complete (∞,1)-category|idempotent completion]];

* a sequence in $Cat_\infty^{stab}$ is (split-)exact if it is so in the standard sense under idempotent completion;

* a functor $Cat_\infty^{stab} \to \mathcal{D}$ to a stable [[presentable (∞,1)-category]] is an **additive invariant** or **localizing invariant** if it

  1. inverts Morita equivalences;

  1. preserves [[filtered (∞,1)-colimits]];

  1. sends split exact sequences or exact sequences, respectively, to (split) [[homotopy cofiber sequences]]. 

=--

+-- {: .num_defn #BGTCharacterization}
###### Definition


The $(\infty,1)$-category $Mot_{add}$ or $Mot_{loc}$, respectively, of **noncommutative motives** is the [[universal construction|universal]] additive/localizing invariant

$$
  \mathcal{U}_{add} \colon Cat_\infty^{stab} \to Mot_{add}
$$

$$
  \mathcal{U}_{loc} \colon Cat_\infty^{stab} \to Mot_{loc}
  \,.
$$


=--

([Blumberg-Gepner-Tabuada 10, theorem 1.1, section 8](#BlumbergGepnerTabuada10))

+-- {: .num_remark }
###### Remark

The localization property here (be additive, invert Morita, preserve split sequences) is of the same form as that which defines the localization of [[C*-algebras]] to [[KK-theory]] in [[noncommutative stable homotopy theory]]. See at _[KK-theory -- Universal characterization](KK-theory#UniversalCharacterization)_. See also ([Blumberg-Gepner-Tabuada 10, paragraph 1.5](#BlumbergGepnerTabuada10)).


=--

## Properties

### Relation to algebraic K-theory
 {#RelationToAlgebraicKTheory}

+-- {: .num_defn }
###### Theorem

For $\mathcal{A}, \mathcal{B} \in Cat_\infty^{stab}$ with $\mathcal{B}$ smooth and proper, hence a [[compact object in an (infinity,1)-category|compact object]], then the hom-[[spectrum]] in $Mot_{loc}$ between $\mathcal{A}$ and $\mathcal{B}$ is given by the [[non-connective algebraic K-theory]] $\mathbb{K}$ of the tensor product in that there is a [[natural equivalence]]

$$
  Hom_{Mot_{loc}}(\mathcal{U}_{loc}(\mathcal{B}), \mathcal{U}_{loc}(\mathcal{K}))
  \simeq
  \mathbb{K}(\mathcal{B}^{op}\widehat \otimes \mathcal{A})
  \,.
$$

=--

([Blumberg-Gepner-Tabuada 10](#BlumbergGepnerTabuada10), theorem 9.36)

### Relation to correspondences equipped with cocycles
 {#RelationToCorrespondences}

By ([Blumberg-Gepner-Tabuada 10, theorem 9.36](#BlumbergGepnerTabuada10)), the morphisms of noncommutative motives from $\mathcal{A}$ to $\mathcal{B}$ for $\mathcal{B}$ suitably dualizable/compact are given by 

$$
  Maps(\mathcal{U}_{loc}(\mathcal{B}), \mathcal{U}_{loc}(\mathcal{A}))
  \simeq
   \mathbb{K}(\mathcal{B}^{op}\otimes\mathcal{A})
  \,,
$$

hence by the [[non-connective algebraic K-theory]] of the [[Deligne tensor product]] of the two categories. 

Thinking of these as categories of [[quasicoherent sheaves]] on some spaces (by definition in [[noncommutative algebraic geometry]]), this are $\mathbb{K}$-cocycles on the product correspondence space.

(...)

### Relation to Chow motives

The relation between ordinary [[Chow motives]] and noncommutative Chow motives is recalled as theorem 4.6 in ([Tabuada 11](#Tabuada11)). For more see [Tabuada 11 ChowNCG](#Tabuada11Chow)

### Relation to KK-theory

Noncommutative motives receive a universal functor from [[KK-theory]]

$$
  KK \longrightarrow NCC_{dg}
$$

which is given by sending a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] over (the [[unitalization]] of) its underlying [[associative algebra]] ([Mahanta 13](#Mahanta13)).

## Applications

* [[Tabuada]] has used noncommutative motives to compute the [[cyclic homology]] of [[twisted projective homogeneous varieties]].  Also, he showed that the noncommutative motive of such a variety is trivial if and only if the [[Brauer class|Brauer classes]] of the associated [[central simple algebras]] are trivial.  See ([Tabuada 13](#Tabuada13Twisted)).

* Bernardara and Tabuada have used noncommutative motives to compute the rational [[Chow groups]] of certain complete [[intersections]] of [[curves]].  See ([Bernardara-Tabuada 13](#BerTab13)).

## Related concepts

* [[bivariant cohomology]], [[bivariant algebraic K-theory]]

* [[motivic symplectic category]]

* [[motive]]

  * [[pure motive]]

    * [[Chow motive]], [[numerical motive]]

  * [[mixed motive]]

* [[motivic cohomology]]

[[!include noncommutative motives - table]]


## References
 {#References}

A survey is in 

* [[Goncalo Tabuada]], _A guided tour through the garden of noncommutative motives_, ([arxiv1108.3787](http://arxiv.org/abs/1108.3787));
 {#Tabuada11} 

Discussion of [[Maxim Kontsevich]]'s definition of 
noncommutative motives include

* [[Maxim Kontsevich]], _Noncommutative motives_, talk at the conference on Pierre Deligne's 61st birthday (2005) (<a href="http://www.ihes.fr/~maxim/TEXTS/ncmotives+(Skoda+notes).pdf">pdf</a> of part of the talk, notes by [[Zoran Skoda]])

* [[Maxim Kontsevich]], _Geometry and Arithmetic - Non-commutative motives_, talk at  Institute for Advanced Study October 20, 2005 ([video](http://video.ias.edu/Geometry-and-Arithmetic-Kontsevich))

The following article has the treatment of $A_\infty$-categories representing smooth, proper, separated etc. noncommutative varieties, notions which are used in Kontsevich's approach to motives in the above talks. 

* [[Ludmil Katzarkov]], [[Maxim Kontsevich]], [[Tony Pantev]], _Hodge theoretic aspects of mirror symmetry_, in [[Ron Donagi]] and [[Katrin Wendland]] (eds.) _From Hodge theory to integrability  and TQFT: $tt^\ast$-geometry_, Proceedings of Symposia in Pure Mathematics vol. 78 (2008), 87-174 ([arXiv:0806.0107](http://arxiv.org/abs/0806.0107))

An abstract characterization of noncommutative motives in [[dg-category]] theory and higher [[algebraic K-theory]] is in 

* [[Denis-Charles Cisinski]], [[Gonçalo Tabuada]], _Non connective K-theory via universal invariants_. Compositio
Mathematica 147 (2011), 1281&#8211;1320 ([arXiv:0903.3717](http://arxiv.org/abs/0903.3717))

* [[Denis-Charles Cisinski]], [[Gonçalo Tabuada]], _Symmetric monoidal structure on Non-commutative motives_, ([arxiv/1001.0228](http://arxiv.org/abs/1001.0228))

* [[Gonçalo Tabuada]], _K-theory via universal invariants_, Duke Math. J. 145 (2008), no.1, 121&#8211;206.

and a further lift of this to [[(∞,1)-category theory]] is in

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _A universal characterization of higher algebraic K-theory_,  Geometry and Topology 17 (2013) 733&#8211;838 ([arXiv:1001.2282](http://arxiv.org/abs/1001.2282))
 {#BlumbergGepnerTabuada10}

* [[Andrew Blumberg]], [[David Gepner]], [[Gonçalo Tabuada]], _Uniqueness of the multiplicative cyclotomic trace_,  Advances in Mathematics ([arXiv:1103.3923](http://arxiv.org/abs/1103.3923))

See also

* [[Goncalo Tabuada]],

  _Bivariant cyclic cohomology and Connes' bilinear pairings in Non-commutative motives_, [arxiv/1005.2336](http://arxiv.org/abs/1005.2336); 

  _Products, multiplicative Chern characters, and finite coefficients via Non-commutative motives_, [arxiv/1101.0731](http://arxiv.org/abs/1101.0731);  

* [[Goncalo Tabuada]], _Chow motives versus non-commutative motives_ ([arxiv/1103.0200](http://arxiv.org/abs/1103.0200)
 {#Tabuada11Chow})

* [[Goncalo Tabuada]],  _Galois descent of additive invariants_, [arxiv/1301.1928](http://arxiv.org/abs/1301.1928)

* [[Matilde Marcolli]], [[Goncalo Tabuada]], _Kontsevich's noncommutative numerical motives_, [arxiv/1108.3785](http://arxiv.org/abs/1108.3785); _Noncommutative motives, numerical equivalence, and semi-simplicity_, [arxiv/1105.2950](http://arxiv.org/abs/1105.2950); _Noncommutative numerical motives, Tannakian structures, and motivic Galois groups_, [arxiv/1110.2438](http://arxiv.org/abs/1110.2438)

* Ivo Dell'Ambrogio, [[Gonçalo Tabuada]], _Tensor triangular geometry of non-commutative motives_, [arxiv/1104.2761](http://arxiv.org/abs/1104.2761) 

For the approach of [[Bertrand Toën]]-[[Michel Vaquié]]-[[Gabriele Vezzosi]], see

* [[Michel Vaquié]], _A new approach on non commutative motives_, lecture at [JAMI 2011](http://www.mathematics.jhu.edu/new/jami2011/noncommgeo.htm).  [video](http://streams1.nts.jhu.edu/mathematics/jami2011/), [notes](http://streams1.nts.jhu.edu/mathematics/jami2011/jami2011pdf/Vaquie.pdf)

and the Ph.D. thesis of [[Marco Robalo]], under the supervision of [[Bertrand Toën]]:

* [[Marco Robalo]], _Noncommutative Motives I: A Universal Characterization of the Motivic Stable Homotopy Theory of Schemes_, June 2012 ([arxiv:1206.3645](http://arxiv.org/abs/1206.3645))

* [[Marco Robalo]], _Noncommutative Motives II: K-Theory and Noncommutative Motives_, June 2013, ([arxiv:1306.3795](http://arxiv.org/abs/1306.3795))

Also the lectures notes:

* [[Marco Robalo]], _Noncommutative motives and K-theory_, talk at [Higher Categories and Topological Quantum Field Theories,
Vienna, 2013](http://www.mat.univie.ac.at/~favero/Workshops/Higher.html), [notes](http://www.mat.univie.ac.at/~favero/Workshops/here/NotesRobalo.pdf)

Another survey article is

* S. Mahanta, Noncommutative geometry in the framework of differential graded categories, [arXiv:0805.1628](http://arxiv.org/abs/0805.1628).

Discussion of how the [[triangulated categories of sheaves|derived category]] of a [[scheme]] determines its commutative and [[noncommutative motive|noncommutative]] [[Chow motive]] is in 

* [[Adeel Khan]], _On derived categories and noncommutative motives of varieties_, [arXiv](http://arxiv.org/abs/1401.7222).

In

*  [[Snigdhayan Mahanta]], _Higher nonunital Quillen $K'$-theory, KK-dualities, and applications to topological T-duality_, ([pdf](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KQ.pdf), [talk notes](http://wwwmath.uni-muenster.de/u/snigdhayan.mahanta/papers/KKTD.pdf))
 {#Mahanta13}

it is shown that there is a universal functor $KK \longrightarrow NCC_{dg}$ from [[KK-theory]] to the category of [[noncommutative motives]], which is the category of [[dg-categories]] and dg-[[profunctors]] up to homotopy between them. This is given by sending a [[C*-algebra]] to the [[dg-category]] of [[perfect complexes]] of (the unitalization of) its underlying [[associative algebra]].

* [[Goncalo Tabuada]], _Additive invariants of toric and twisted projective homogeneous varieties via noncommutative motives_, ([arXiv](http://arxiv.org/abs/1310.4063)).
 {#Tabuada13Twisted}

* [[Marcello Bernardara]], [[Goncalo Tabuada]].  _Chow groups of intersections of quadrics via homological projective duality and (Jacobians of) noncommutative motives._  ([arXiv](http://arxiv.org/abs/1310.6020))
 {#BerTab13}

category: algebraic geometry, noncommutative geometry

[[!redirects noncommutative motif]]
[[!redirects noncommutative motive]]
[[!redirects noncommutative motives]]

[[!redirects noncommutative Chow motive]]
[[!redirects noncommutative Chow motives]]

[[!redirects (infinity,1)-category of non-commutative motives]]
[[!redirects (∞,1)-category of non-commutative motives]]

[[!redirects (infinity,1)-category of noncommutative motives]]
[[!redirects (∞,1)-category of noncommutative motives]]


[[!redirects (infinity,1)-categories of non-commutative motives]]
[[!redirects (∞,1)-categories of non-commutative motives]]

[[!redirects (infinity,1)-categories of noncommutative motives]]
[[!redirects (∞,1)-categories of noncommutative motives]]

[[!redirects non-commutative motive]]
[[!redirects non-commutative motives]]