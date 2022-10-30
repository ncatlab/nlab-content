
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### AQFT
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Vertex operator algebras (or "vertex algebras", for short) are [[algebras]] with a product-operation parameterized by points in the [[complex plane]]. 

Vertex operator algebras equipped with an [[action]] of the [[Virasoro algebra]] encode the local ([[genus of a surface|genus-0]] behaviour) of [[2-dimensional conformal field theories]]. Here one may think of the [[complex plane]] as the [[Riemann sphere]] and of the $z$-parameterized product operation in the vertex algebras as being the [[n-point function|3-point function]] of the [[2d CFT]] with field insertions at the points 0, $z$ and $\infty$. In fact one vertex operator algebra enodes (only) one chiral/holomorphic half of such a genus-0 2d CFT; a full genus-0 2d CFT is given by the combination of two vertex operator algebras called a _[[full field algebra]]_.

The traditional definition of _vertex operator algebra_ (VOA) is long and tends to be somewhat unenlightening. But due to ([Huang 91](#Huang)) it is now known that vertex operator algebras have equivalenlty an [[FQFT]]-type characterization which manifestly captures this relation to [[n-point functions]] in the [[2d CFT]]:

There is a [[monoidal category]] or [[operad]] whose [[morphism|morphisms]] are conformal spheres with $n$-punctures marked as incoming and one puncture marked as outgoing (each puncture equipped with a conformally parametrized annular neighborhood). Composition of such spheres is by gluing along punctures. This can be regarded as a category $2Cob_{conf}^0$ of 2-dimensional genus-0 conformal [[cobordism|cobordisms]].

As shown by theorems by [[Yi-Zhi Huang]] and [[Liang Kong]], a vertex operator algebra is precisely a _[[holomorphic representation]]_ of this category, or [[algebra over an operad]] for this [[operad]] i.e. an genus-0 [[conformal field theory|conformal]] [[FQFT]], hence a [[monoidal functor]]

$$
  V : 2Cob_{conf}^0 \to Vect
$$

such that its component $V_1$ is a holomorphic function on the moduli space of conformal punctured spheres.

## Standard definition

(under construction) A __vertex algebra__ consists of the following data:

* nonnegatively graded complex vector space $V = \oplus_{n =0}^\infty V_n$
* vacuum vector $|0\rangle\in V_0$
* a shift operator $T: V\to V$ 
* operation $Y = Y(-,z) : V\to End V [ [z,z^{-1}] ]$ 



This data satisfy three axioms: 

(vacuum)

(translation axiom)

(locality)

In practice, the most important case is when the shift $T$ is related to a conformal vector "the energy momentum tensor" $\omega$ whose Fourier components are related to the generators $L_i$ of the [[Virasoro Lie algebra]] $Vir$. In that case we talk about a __conformal vertex algebra__.

There is a notion of a module over a vertex algebra. A conformal vertex algebra $A$ is said to be __rational__ if every $A$-module is completely reducible. Then it follows that there are only finitely many nonisomorphic simple $A$-modules.  

## Properties
 {#Properties}

### Category of vertex operator algebras
 {#CategoryOfVOAs}

Vertex operator algebras naturally form a [[category]] (see section 2.4 of ([FrenkenHuangLepowsky](#FrenkenHuangLepowsky)). This is naturally a [[monoidal category]] with respect to [[tensor product]] of VOAs (section 2.5).

This is [[equivalence of categories|equivalent]] to 

* the category of algebras over the holomorphic punctured sphere operad ([Huang](#HuangCFT)); 

* the category of vertex operator coalgebras ([Hubbard](#Hubbard)).

### Modular category of modules over a VOA
 {#ModularTensorCategories}

The [[category]] of [[modules]]/[[representations]] over a given vertex operator algebra is a [[modular tensor category]], ([Huang](#Huang))

### Goddard-Thorn theorem

* [[Goddard-Thorn theorem]]

### Relation to $A_\infty$-algebras and RG fixed points
 {#RelationToAInfinityAlgebras}

A [[functor]] from the category of  [[BRST complex|BRST]]-VOAs to that of [[A-infinity algebra]]s is described in

* [[Anton Zeitlin]], _Quasiclassical Lian-Zuckerman Homotopy Algebras, Courant Algebroids and Gauge Theory_ ([arXiv](http://arxiv.org/abs/0910.3652))

and argued to algebraically encode the [[effective QFT|effective]] [[string theory]] background encoded by the [[CFT]] given by the VOA.

### Relation to conformal nets

Subject to some conditions, from a vertex operator algebra one may induce a [[conformal net]] and conversely ([Capri-Kawahigahshi-Longo-Weiner 15](#CapriKawahigahshiLongoWeiner15)).

## Examples

A class of examples are _[[current algebras]]_ .

A database of examples is given by ([Gannon-H&#246;hn](#GannonHoehn)).

The [[Moonshine]] module over the [[Griess algebra]] admits the structure of a vertex operator algebra, which has

* rank 24;

* is a self-[[dual object]] in the category of VOAs;

* has trivial degree-1 subspaces.

A conjecture by Frenkel, Lepowsky and Meurman says that the Moonshine VOA is, up to isomorphism the unique VOA with these properties.

See at _[[monster vertex algebra]]_.

## Variants 

* [[Poisson vertex algebra]]

* [[rational vertex operator algebra]]

* [[super vertex operator algebra]]

* [[sheaf of vertex operator algebras]], [[vertex operator algebroid]]

## Related entries

* [[affine Lie algebra]]

* [[conformal field theory]], 

* [[factorization algebra]], 


## References

### General

* [[Victor Kac]], _Vertex algebras for beginners_, Amer. Math. Soc.  ([ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:0924.17023&format=complete))

* [[Edward Frenkel]], [[David Ben-Zvi]]: _Vertex algebras and algebraic curves_, Math. Surveys and Monographs __88__, AMS 2001,
xii+348 pp. (Bull. AMS. [review](http://www.ams.org/journals/bull/2002-39-04/S0273-0979-02-00955-2/S0273-0979-02-00955-2.pdf), [ZMATH entry](http://www.zentralblatt-math.org/zmath/en/advanced/?q=an:1106.17035&format=complete))

* [[Igor Frenkel]], [[Yi-Zhi Huang]], [[James Lepowsky]], _On Axiomatic approaches to Vertex Operator Algebras and Modules_ , Memoirs of the AMS Vol 104, No 494 (1993)
 {#FrenkenHuangLepowsky}

* [[Igor Frenkel]], [[James Lepowsky]], Arne Meurman, _Vertex operator algebras and the monster_, Pure and Applied Mathematics __134__, Academic Press, New York 1998.


### As algebras over the holomorphic sphere operad
 {#AsOperadAlgebras}

The original article with the interpretation of vertex operator algebras as holomorphic algebras over the holomorphic punctured sphere operad is

* {#Huang91} [[Yi-Zhi Huang]], _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA __88__ (1991) pp. 9964-9968

A standard textbook summarizing these results is

* {#HuangCFT} [[Yi-Zhi Huang]], _Two-dimensional conformal geometry and vertex operator algebras_, Progr. in Math. Birkhauser 1997, [gbooks](http://books.google.hr/books?isbn=0817638296)
 

As mentioned in the [acknowledgements](http://books.google.com/books?id=SUUdknTpYjEC&pg=PR11&lpg=PR11&dq=%22vertex+operator+algebras%22+%22trimble%22&source=bl&ots=v3GHx_ra2M&sig=TW5MzAtDi4n_gJjvUHb6eELoAXQ&hl=en&ei=9jdnSoXqKJiCtge6xqDuDw&sa=X&oi=book_result&ct=result&resnum=4) there, [[Todd Trimble]] and [[Jim Stasheff]] had a hand in making the operadic picture manifest itself here. Other operadic approaches are known, e.g. an earlier one in 

* Bojko Bakalov, Alessandro D'Andrea, [[Victor Kac]], _Theory of finite pseudoalgebras_, Adv. Math. __162__ (2001), no. 1, 1--140, [MR2003c:17020](http://www.ams.org/mathscinet-getitem?mr=2003c:17020) 

and even earlier treatments via coloured [[operads]] and [[generalized multicategories]], for references (Snydal, Soibelman, Beilinson-Drinfeld) see [[relaxed multicategory]].  

More recently Huang's student [[Liang Kong]] has been developing these results further, generalizing them to open-closed CFTs and to non-chiral, i.e. completely general CFTs. See 

* {#Kong08} [[Liang Kong]], _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008), [math.QA/0610293](http://arxiv.org/abs/math/0610293).

### As factorization algebras 

Discussion of vertex operator algebras as [[factorization algebras of observables]] is in section 6.3 and section 6.5 of 

* [[Owen Gwilliam]], _Factorization algebras and free field theories_ PhD thesis ([pdf](http://math.berkeley.edu/~gwilliam/thesis.pdf))
 {#Gwilliam}

### Relation to modular tensor categories

The [[representation categories]] of (rational) vertex operator algebras ([[modular tensor categories]]) are discussed in

* [[Yi-Zhi Huang]], _Vertex operator algebras, the Verlinde conjecture and modular tensor categories_ ([arXiv:math/0412261](http://arxiv.org/abs/math/0412261))
 {#Huang}

* {#GannonHoehn} [[Terry Gannon]], [[Gerald Höhn]], Hiroshi Yamauchi, _[The online database of Vertex Operator Algebras and Modular Categories](http://www.math.ksu.edu/~gerald/voas/)_
   

### As chiral algebras

An algebrogeometric version is due Beilinson and Drinfel'd and called the [[chiral algebra]].

* E. Frenkel, N. Reshetikhin, _Towards deformed chiral algebras_, [q-alg/9706023](http://arXiv.org/abs/q-alg/9706023)

* Ruthi Hortsch, [[Igor Kriz]], Ales Pultr, _A universal approach to vertex algebras_, [arxiv/1006.0027](http://arxiv.org/abs/1006.0027)

Much algebraic insight to algebaric structures in CFT is in unfinished notes

* [[A. Beilinson]], [[B. Feigin]], B. Mazur, _Notes on conformal field theory_, &lt;http://www.math.sunysb.edu/~kirillov/manuscripts.html>

### Relation to 2d conformal field theory

* [[Yi-Zhi Huang]], _Two-dimensional conformal geometry and vertex operator algebras_  Birkh&#228;user (1997)

Relation specifically to [[conformal nets]] is discussed in

* {#CapriKawahigahshiLongoWeiner15} [[Sebastiano Carpi]], [[Yasuyuki Kawahigashi]], [[Roberto Longo]], Mih&#225;ly Weiner, _From vertex operator algebras to conformal nets and back_ ([arXiv:1503.01260](http://arxiv.org/abs/1503.01260))

* {#Carpi16} [[Sebastiano Carpi]], _Operator algebras and vertex operator algebras_, Contribution to the Proceedings of the 14th Marcel Grossmann Meeting - MG14 (Rome, 2015) ([arXiv:1603.06742](http://arxiv.org/abs/1603.06742))

### Category of vertex operator algebras

* [[Keith Hubbard]], _The duality between vertex operator algebras and coalgebras, modules and comodules_, [pdf](http://www.faculty.sfasu.edu/hubbardke/duality.pdf)

### Relation to sporadic groups

* [[John Duncan]], _Vertex operator algebras and sporadic groups_, [pdf](http://arxiv.org/PS_cache/arxiv/pdf/0811/0811.1306v1.pdf); _Moonshine for Rudvalis's sporadic group I_, [pdf](http://arxiv.org/PS_cache/math/pdf/0609/0609449v2.pdf)

### Deformations

There is an interesting theory of deformation quantization of VOAs from

* [[Pavel Etingof]], [[David Kazhdan]], _Quantization of Lie bialgebras. V. Quantum vertex operator algebras_, 
Selecta Math. (N.S.) 6 (2000), no. 1, 105--130, [MR2002i:17022](http://www.ams.org/mathscinet-getitem?mr=2002i:17022)

Deformation quantization of chiral algebras are studied by

* [[Dmitry Tamarkin]], _Deformations of chiral algebras_, Proceedings of the ICM, Beijing 2002, vol. 2, 105--118 

A class of "free" vertex algebras are also quantized using [[Batalin-Vilkovisky formalism]], with results important for understanding [[mirror symmetry]], in

* Si Li, _Vertex algebras and quantum master equation_, [arxiv/1612.01292](https://arxiv.org/abs/1612.01292)


### Further references

* [what-is-the-motivation-for-a-vertex-algebra](http://mathoverflow.net/questions/53988/what-is-the-motivation-for-a-vertex-algebra) - a MathOverflow discussion on the motivation 
* [The online database of Vertex Operator Algebras and Modular Categories](http://www.math.ksu.edu/~gerald/voas)
* Yi-Zhi Huang, _Meromorphic open-string vertex algebras_, J. Math. Phys. __54__, 051702 (2013) [doi](http://dx.doi.org/10.1063/1.4806686)    

[[!redirects vertex algebra]]
[[!redirects vertex algebras]]
[[!redirects Vertex operator algebra]]

[[!redirects vertex operator algebras]]