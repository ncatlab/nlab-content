
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic geometry
+--{: .hide}
[[!include algebraic geometry - contents]]
=--

#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic geometry]], __algebraic variety__  (not to be confused with [[variety of algebras]]) is a [[scheme]] which is [[integral scheme|integral]], [[separated scheme|separated]] and of [[finite type]] over an [[algebraically closed field]] $k$.

Classically, the term algebraic variety referred to a [[scheme]] as above which is further [[quasi-projective scheme|quasi-projective]], i.e. admits a locally closed embedding into [[projective space]].  Thus, these were objects which locally are cut out inside [[projective space]] as the geometric locus of zeros of a set of [[polynomial]] equations in finitely many variables.  (The first example of an algebraic variety which is not quasi-projective was given by [[Nagata]].)

Historically, there were several formalisms of various schools including the Italian school of [[algebraic geometry]] in the early 20th century (Veronese, Castelnuovo, Severi, ...), the American school between the two wars ([[Oscar Zariski]]), [[Andre Weil]]), the abstract varieties of [[Jean-Pierre Serre]] and finally the language of [[schemes]] introduced by the [[Grothendieck]] school. One should note that in the case of (esp. [[projective variety|projective]]) varieties over complex numbers there is an additional possibility to work using complex-analytic tools and complex topology.

## Definition

Given an [[algebraically closed field]] $k$, an __algebraic $k$-variety__ usually means either a [[quasiprojective variety]] or an abstract variety (in the sense of Serre). 'Quasiprojective' unifies affine, quasiaffine, [[projective variety|projective]] and embedded  quasiprojective $k$-varieties. Many modern sources by a variety mean a reduced separated scheme of finite type over a field, often requiring also irreducibility (that is integral = reduced and irreducible). 

* An embedded affine $k$-variety (or an affine algebraic set) is a set of zeros of a locus of common zeros of a set of polynomial equations in the affine space $\mathbf{A}^n_k$. By the Hilbert [[Nullstellensatz]] there is a more invariant definition. __[[affine variety|Affine]]__ $k$-varieties are [[maximal spectrum|maximal spectra]] (= sets of [[maximal ideals]]) of finitely generated [[noetherian ring|noetherian]] (commutative unital) $k$-[[commutative algebra|algebras]] without [[nilpotent element|nilpotents]] with the [[Zariski topology]]; the algebra can be recovered as the coordinate ring of the variety; this correspondence is an equivalence of categories, if the morphisms are properly defined.

  Affine varietes can be embedded as closed subvarieties into an [[affine space]] (in the sense of algebraic geometry). As topological spaces affine varieties are [[noetherian space|noetherian]]. 

* __[[projective variety|Projective]]__ $k$-varieties are obtained in a similar way from [[graded algebra|graded]] $k$-algebras, or, in embedded incarnation, as loci of zeros of a set of homogeneous polynomials in projective space $\mathbf{P}^n_k$. 

* Embedded __quasiaffine__ $k$-varieties are Zariski-open subspaces of affine $k$-varieties. 

* Embedded __quasiprojective__ $k$-varieties are Zariski-open subspaces of projective $k$-varieties. We can remove the embedding by equipping them with the sheaf of regular functions and therefore considering them as [[locally ringed space]]s. In the category of locally ringed spaces, projective, affine, and quasiaffine varieties are (isomorphic to) special cases of quasiprojective. Alternatively, we can put all 4 classes without sheaves into a category, by defining regular maps directly, and we get an isomorphic category of varieties.

  In fact, by noticing that the affine $k$-space is Zariski open in a projective space of the same dimension, we see that the quasiprojective case includes all others. 

Morphisms between varieties are sometimes called [[regular map]]s.  

Sometimes a smooth algebraic variety may also be called __algebraic manifold__.

To define abstract algebraic varieties in the sense of Serre’ [[FAC]] (see \ref{DefinitionVarietyFAC}), we need an auxiliary concept:

+-- {: .num_defn}
###### Definition

([Görtz, Wedhorn 2020, Definition 1.35](#GortzWedhorn20)). Let $k$ be a field.

1. A **space with $k$-valued functions** is a [[ringed space]] $X$ whose structure is subsheaf of $k$-algebras of the sheaf of all $k$-valued functions on $X$.

2. A morphism of spaces with functions $(X,\mathcal{O}_X)\to (Y,\mathcal{O}_Y)$ is a continuous map $f:X\to Y$ such that for all $V\subseteq Y$ open and all $\varphi\in\mathcal{O}_Y(V)$, we have $\varphi\circ f|_{f^{-1}(V)}\in\mathcal{O}_X(f^{-1}(V))$.

=--

This concept goes by the name “ringed space” in ([Milne 2017, Sect. 3.b](#Milne17)) ([Ellingsrud, Ottem 3.14](#EllingsrudOttem)); this definition for the morphisms also appears in ([Gathmann 2021, Definition 4.3](#Gathmann21)). For instance, if $k=\mathbb{R}$ (resp., $k=\mathbb{C}$), the category of [[smooth manifold|smooth manifolds]] (resp., [[complex manifold|complex manifolds]] or more generally, reduced [[complex analytic space|complex analytic spaces]]) embed fully faithfully into the category of spaces with real-valued functions (resp., complex-valued functions).

The advantage of this notion of morphism between spaces with $k$-valued functions is that it is a _property_, rather than additional data (as in a morphism of [[ringed spaces]]). “Being a morphism” is a property that is local in both the source and target in the following sense: Let $f:X\to Y$ be a function between spaces with $k$-valued functions and let $\bigcup_i U_i=X$ and $\bigcup_i V_i=Y$ be open covers such that $f(U_i)\subseteq V_i$. Then $f$ is a morphism if and only if $f|_{U_i}:U_i\to V_i$ is a morphisms for every $i$ ([Gathmann 2021, Lemma 4.6](#Gathmann21)). See also Remark \ref{RemarkMorphismsSpaceskValuedFunctions}.

+-- {: .num_lemma}
###### Lemma

Let $k$ be a field. Let $X$ be a space with $k$-valued functions. The following are equivalent:

1. $X$ is a [[locally ringed space]].

2. The following conditions hold:

   * For all open $U\subseteq X$ and all sections $f\in\mathcal{O}_X(U)$, if $f(x)\neq 0$ for all $x\in U$, then $f^{-1}\in\mathcal{O}_X(U)$.
   * For all open $U\subseteq X$ and all sections $f\in\mathcal{O}_X(U)$, if $f(x)\neq 0$ at some $x\in U$, then there is a neighborhood $V\subseteq U$ of $x$ such that $f(x)\neq 0$ for all $x\in V$. Equivalently, if $k$ is given the [[cofinite topology]], $f:U\to k$ is continuous for all $f\in\mathcal{O}_X(U)$ and all open $U\subseteq X$.

3. For all open $U\subseteq X$ and all sections $f\in\mathcal{O}_X(U)$, if $f(x)\neq 0$ at some $x\in U$, then there is a neighborhood $V\subseteq U$ of $x$ such that $f(x)\neq 0$ for all $x\in V$ and $f|_{V}^{-1}\in\mathcal{O}_X(V)$. 

4. For all open $U\subseteq X$ and all sections $f\in\mathcal{O}_X(U)$, the set $D(f)\coloneqq \{x\in U\mid f(x)\neq 0\}$ is open and $f|_{D(f)}^{-1}\in\mathcal{O}_X(D(f))$.

=--

+-- {: .proof}
###### Proof

The sheaf condition implies the equivalence between 3 and 4. For the equivalence between the first three conditions, see ([Guisado Villalgordo, Lemma 3.6](#GuisadoVillalgordo)).

=--

Thus, a space with $k$-valued functions that is locally ringed is just a “space with functions” as in ([Kempf 2013, Sect. 1.1](#Kempf13)).

+-- {: .num_remark #RemarkMorphismsSpaceskValuedFunctions}
###### Remark

If $X,Y$ are spaces with $k$-valued functions that are locally ringed, then the morphisms $X\to Y$ of spaces with $k$-valued functions are exactly the morphisms $X\to Y$ of locally ringed spaces over $k$, see ([Guisado Villalgordo, Proposition 3.9](#GuisadoVillalgordo)).

=--

Let $k$ be a field (in the context of algebraic geometry, $k$ is algebraically closed). Let $Z\subseteq\mathbb{A}_{k,\mathrm{class}}^n\coloneqq k^n$ be a Zariski closed subset (i.e., an algebraic set). A regular function on an open subset $U\subseteq Z$ is a function $U\to k$ that is _locally rational_, i.e., it is locally a quotient of polynomials from $k[x_1,\dots,x_n]$ (with non-vanishing denominator). The regular functions assemble into a sheaf $\mathcal{O}_Z$ that turns $(Z,\mathcal{O}_Z)$ into a space with $k$-valued functions that is a locally ringed space. See ([Milne 2017, Sect. 3.c](#Milne17)), ([Gathmann 2021, Sect. 3](#Gathmann21)).

+-- {: .num_defn #DefinitionVarietyFAC}
###### Definition

Let $k$ be an algebraically closed field.

1. A **classical affine $k$-variety** is a space with $k$-valued functions isomorphic to $(Z,\mathcal{O}_Z)$, for some algebraic set $Z$.

2. An **(abstract) $k$-prevariety** (in the sense of Serre’s [[FAC]]) is a space with $k$-valued functions which is locally isomorphic to a classical affine $k$-variety.

=--

Equivalently, by Remark \ref{RemarkMorphismsSpaceskValuedFunctions}, an (abstract) $k$-prevariety is a locally ringed space over $Spec k$ which is locally isomorphic over $Spec k$ to a classical affine $k$-variety. In [[FAC]] it is also required that $X$ is quasi-compact. A morphism of $k$-prevarieties, also called a [[regular map]], is a morphism of spaces with $k$-valued functions. The category of $k$-prevarieties has a product which is obtained by locally gluing products in the category of affine $k$-varieties. This enables defining a diagonal $X\to X\times X$. An abstract $k$-variety (in the sense of Serre’s [[FAC]]) is a separated $k$-prevariety, i.e., the diagonal is closed in Zariski topology (which is, of course, not a product of Zariski topologies of factors). Again, [[FAC]] requires quasi-compactness in the definition of abstract $k$-variety.

## Properties

### Relation to schemes

There is an [[equivalence of categories]] between the [[category]] of (separated) [[reduced schemes]] of finite type over $Spec\,k$, where $k$ is an [[algebraically closed field]], and the category of algebraic $k$-(pre)varieties. This is the *classical-schematic equivalence*. It is obtained in [[EGA IV]], 10.10 from a more general equivalence involving [[ultrascheme|ultra-schemes]]. Indeed, if $k$ is algebraically closed, a $k$-prevariety is essentially the same as an ultra-scheme over $Spec\, k$. The classical-schematic equivalence (with sometimes some additional adjectives imposed in the varieties considered, like “connected,” “integral,” etc.) is also covered in ([Mumford 1999, II.3, Theorem 2](#Mumford99)), ([Hartshorne 1977, Ch. II, Propositions 2.6, 4.10](#Hartshorne77)), ([Görtz, Wedhorn 2020, Theorem 3.37](#GortzWedhorn20)), ([Guisado Villalgordo](#GuisadoVillalgordo)), and ([Haiman](#Haiman)).

Of course, given a variety the corresponding [[scheme]] and variety have different sets of points; the points in common are the closed points of the scheme. The remaining points are the generic points of subvarieties. In fact, the associated scheme is the [[sober topological space#Reflection|sobrification]] of the given variety (see [[ultrascheme#equivalence_of_categories_with_schemes|Equivalence of categories with schemes]]). Generic points were often used, without proper foundations, in other language, already in the works of the Italian school. 

Some modern algebraic geometers mean, by varieties, objects of certain slightly bigger categories of relative $S$-schemes of finite type (where $S$ is not necessarily $Spec\,k$ for $k$ a field); typically they are required to be [[separated scheme|separated]] [[reduced scheme|reduced]] $S$-[[relative scheme|schemes]] [[morphism of finite type|of finite type]].

## Related concepts

* [[geometric point]]

* [[singular point of an algebraic variety]]

* [[complete algebraic variety]]

* [[semialgebraic manifold]]

## References

* Igor Shafarevich, _Basic algebraic geometry_, vol. I
* {#Milne17} J. S. Milne, _Algebraic geometry_, 2017 [pdf](http://www.jmilne.org/math/CourseNotes/AG.pdf)
* Joe Harris, _Introductory algebraic geometry_
* {#Kempf13} George R. Kempf, _Algebraic Varieties_, Cambridge University Press, 2013

See also the first chapter in each of the following three books:

* {#Mumford99} [[David Mumford]]: *Red book of varieties and schemes*, Lecture Notes in Mathematics **1358**, Springer (1999) &lbrack;[doi:10.1007/b62130](https://doi.org/10.1007/b62130)&rbrack;

* {#Hartshorne77} [[Robin Hartshorne]], _Algebraic geometry_, Springer (1977)

* {#GortzWedhorn20} Ulrich Görtz, [[Torsten Wedhorn]], *Algebraic Geometry I: Schemes*, Springer (2020) &lbrack;[doi:10.1007/978-3-658-30733-2](https://doi.org/10.1007/978-3-658-30733-2)&rbrack;

Lecture notes:

* {#EllingsrudOttem} Geir Ellingsrud, John Christian Ottem, _Algebraic Geometry I_, University of Oslo, 2023 [pdf](https://www.uio.no/studier/emner/matnat/math/MAT4210/data/mastermat4210(1).pdf)

* {#Gathmann21} Andreas Gathmann, _Algebraic Geometry_, University of Kaiserslautern, 2021 [pdf](https://agag-gathmann.math.rptu.de/class/alggeom-2021/alggeom-2021.pdf)

For the equivalence between classical varieties and schemes, see:

* {#GuisadoVillalgordo} Elías Guisado Villalgordo, *[The Classical-Schematic Equivalence](https://eliasguisado.wordpress.com/wp-content/uploads/2025/09/the_classical_schematic_equivalence.pdf)*

* {#Haiman} Mark Haiman, *[Varieties as Schemes](https://math.berkeley.edu/~mhaiman/math256-fall18-spring19/varieties-as-schemes-v2.pdf)*

An amusing discussion on the differences between schemes and varieties can be found at _Secret blogging seminar_: [algebraic geometry without prime ideals](http://sbseminar.wordpress.com/2009/08/06/algebraic-geometry-without-prime-ideals).

category: algebraic geometry
[[!redirects algebraic varieties]]
[[!redirects affine algebraic variety]]
[[!redirects affine algebraic varieties]]
[[!redirects algebraic manifold]]
[[!redirects algebraic manifolds]]
[[!redirects quasiaffine variety]]
[[!redirects quasiaffine varieties]]
[[!redirects quasiaffine algebraic variety]]
[[!redirects quasiaffine algebraic varieties]]

[[!redirects quasi-projective variety]]
[[!redirects quasiprojective variety]]
[[!redirects quasi-projective varieties]]
[[!redirects quasiprojective varieties]]
[[!redirects quasi-projective algebraic variety]]
[[!redirects quasiprojective algebraic variety]]
[[!redirects quasi-projective algebraic varieties]]
[[!redirects quasiprojective algebraic varieties]]

[[!redirects quasi-projective scheme]]
[[!redirects quasi-projective scheme]]

[[!redirects Var]]
[[!redirects Varieties]]


