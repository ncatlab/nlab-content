> This [[HomePage|nLab]] page is for developing preliminary notes or making typographical experiments, etc. It may be edited by anybody, anytime. But you don't necessarily need to delete other people's ongoing notes here in order to add your own. In any case, overwritten edits may always be recovered from the [page history](/nlab/history/Sandbox).

> If this edit page here is seemingly locked by "Anonymous", just break the lock, as it is just caused by bot traffic. If the page is locked by an actual user, there is also the alternative *[[Sandbox2]]*.


***
\linebreak

* [[André Coimbra]], [[Charles Strickland-Constable]], [[Daniel Waldram]]: *Supergravity as Generalised Geometry II: $E_{d(d)} \times \mathbb{R}^+$ and M theory* \[<a href="https://doi.org/10.1007/JHEP03(2014)019">doi:10.1007/JHEP03(2014)019</a>, [arXiv:1212.1586 hep-th](https://arxiv.org/abs/1212.1586)\]

* Paulo Pires Pacheco, [[Daniel Waldram]]: *M-theory, exceptional generalised geometry and superpotentials*, J. High Energy Physics **2008** JHEP09 (2008) \[<a href="https://doi.org/10.1088/1126-6708/2008/09/123">doi:10.1088/1126-6708/2008/09/123</a>, <a href="https://arxiv.org/abs/0804.1362">arXiv:0804.1362</a>\]


* [[André Coimbra]], [[Charles Strickland-Constable]], [[Daniel Waldram]]: *$E_{d(d)} \times \mathbb{R}^+$ Generalised Geometry, Connections and M theory*,  J. High Energ. Phys. **2014** 54 (2014) \[<a href="https://doi.org/10.1007/JHEP02(2014)054">doi:10.1007/JHEP02(2014)054</a>, <a href="https://arxiv.org/abs/1112.3989">arXiv:1112.3989 hep-th</a>\]





\linebreak

\linebreak



$$
  \left(
  \begin{matrix}
    A & B 
    \\
    0 & C
  \end{matrix}
  \right)
  \left(
  \begin{matrix}
    A^{-1}
    & 
    - A^{-1} B C^{-1}
    \\
    0 & C^{-1}
  \end{matrix}
  \right)
  =
  \begin{matrix}
    1 & 
    \\
  \end{matrix}
$$

To define abstract algebraic varieties in the sense of Serre’ [[FAC]], we need an auxiliary concept.

+-- {: .num_defn}
###### Definition

([Görtz, Wedhorn 2020, Definition 1.35](#GortzWedhorn20)). Let $k$ be a field.

1. A **space with $k$-valued functions** is a [[ringed space]] $X$ whose structure is subsheaf of $k$-algebras of the sheaf of all $k$-valued functions on $X$.

2. A morphism of spaces with functions $(X,\mathcal{O}_X)\to (Y,\mathcal{O}_Y)$ is a continuous map $f:X\to Y$ such that for all $V\subseteq Y$ open and all $\varphi\in\mathcal{O}_Y(V)$, we have $\varphi\circ f|_{f^{-1}(V)}\in\mathcal{O}_X(f^{-1}(V))$.

=--

For instance, if $k=\mathbb{R}$ (resp., $k=\mathbb{C}$), the category of [[smooth manifold|smooth manifolds]] (resp., [[complex manifold|complex manifolds]] or more generally, reduced [[complex analytic space|complex analytic spaces]]) embed fully faithfully into the category of spaces with real-valued functions (resp., complex-valued functions).

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

See ([Guisado Villalgordo, Lemma 3.6](#GuisadoVillalgordo)). Thus, a $k$-valued functions that is locally ringed is just a “space with functions” as in ([Kempf 2013, Sect. 1.1](#Kempf13)).

+-- {: .num_remark #RemarkMorphismsSpaceskValuedFunctions}
###### Remark

If $X,Y$ are spaces with $k$-valued functions that are locally ringed, then the morphisms $X\to Y$ of spaces with $k$-valued functions are exactly the morphisms $X\to Y$ of locally ringed spaces over $k$, see ([Guisado Villalgordo, Proposition 3.9](#GuisadoVillalgordo)).

=--

Let $k$ be a field (in the context of algebraic geometry, $k$ is algebraically closed). Let $Z\subseteq\mathbb{A}_{k,\mathrm{class}}^n\coloneqq k^n$ be a Zariski closed subset (i.e., an algebraic set). A regular function on an open subset $U\subseteq Z$ is a function $U\to k$ that is _locally rational_, i.e., it is locally a quotient of polynomials in $k[x_1,\dots,x_n]$ (with non-vanishing denominator). The regular functions assemble into a sheaf $\mathcal{O}_Z$ that turns $(Z,\mathcal{O}_Z)$ into a space with $k$-valued functions that is a locally ringed space. See ([Milne 2017, Sect. 3.c](#Milne17)), ([Gathmann 2021, Sect. 3](#Gathmann21)).

+-- {: .num_defn}
###### Definition

1. A **classical affine $k$-variety** is a space with $k$-valued functions isomorphic to $(Z,\mathcal{O}_Z)$, for some algebraic set $Z$.

2. An **(abstract) $k$-prevariety** (in the sense of Serre’s [[FAC]]) is a space with $k$-valued functions $X$ which is locally isomorphic to a classical affine $k$-variety.

=--

Equivalently, by Remark \ref{RemarkMorphismsSpaceskValuedFunctions}, $X$ is a locally ringed space over $Spec k$ which is locally isomorphic over $Spec k$ to a classical affine $k$-variety). In [[FAC]] it is also required that $X$ is quasi-compact. A morphism of $k$-prevarieties, also called a [[regular map]], is a morphism of spaces with $k$-valued functions. The category of $k$-prevarieties has a product which is obtained by locally gluing products in the category of affine $k$-varieties. This enables defining a diagonal $X\to X\times X$. An abstract $k$-variety (in the sense of Serre’s [[FAC]]) is a separated $k$-prevariety, i.e., the diagonal is closed in Zariski topology (which is, of course, not a product of Zariski topologies of factors). Again, [[FAC]] requires quasi-compactness in the definition of abstract $k$-variety.

## Properties

### Relation to schemes

There is an [[equivalence of categories]] between the [[category]] of (separated) [[reduced schemes]] of finite type over $Spec\,k$, where $k$ is an [[algebraically closed field]], and the category of algebraic $k$-(pre)varieties. This is the *classical-schematic equivalence*. It is obtained in [[EGA IV]], 10.10 from a more general equivalence involving [[ultrascheme|ultra-schemes]]. Indeed, if $k$ is algebraically closed, a $k$-prevariety is essentially the same as an ultra-scheme over $Spec\, k$. The classical-schematic equivalence (with sometimes some additional adjectives in the varieties considered, like “connected,” “integral,” etc.) is also covered in ([Mumford 1999, II.3, Theorem 2](#Mumford99)), ([Hartshorne 1977, Ch. II, Proposition 2.6, Proposition 4.10](#Hartshorne77)), ([Görtz, Wedhorn 2020, Theorem 3.37](#GortzWedhorn20)), ([Guisado Villalgordo](#GuisadoVillalgordo)), ([Haiman](#Haiman)).

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

* {#GortzWedhorn20} Ulrich Görtz, [[Torsten Wedhorn]], *Algebraic Geometry I: Schemes*, Springer (2020) &lbrack;[doi:10.1007/978-3-658-30733-2](https://doi.org/10.1007/978-3-658-30733-2)

Lecture notes:

* Geir Ellingsrud, John Christian Ottem, _Algebraic Geometry I_, University of Oslo, 2023 [pdf](https://www.uio.no/studier/emner/matnat/math/MAT4210/data/mastermat4210-2024.pdf)

* {#Gathmann21} Andreas Gathmann, _Algebraic Geometry_, University of Kaiserslautern, 2021 [pdf](https://agag-gathmann.math.rptu.de/class/alggeom-2021/alggeom-2021.pdf)

For the equivalence between classical varieties and schemes, see:

* {#GuisadoVillalgordo} Elías Guisado Villalgordo, *[The Classical-Schematic Equivalence](https://eliasguisado.wordpress.com/wp-content/uploads/2025/09/the_classical_schematic_equivalence.pdf)*

* {#Haiman} Mark Haiman, *[Varieties as Schemes](https://math.berkeley.edu/~mhaiman/math256-fall18-spring19/varieties-as-schemes-v2.pdf)*