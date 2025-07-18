
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Combinatorics
+-- {: .hide}
[[!include combinatorics - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
#### Quantum Field Theory
+--{: .hide}
[[!include AQFT and operator algebra contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

The _associahedra_ or _Stasheff polytopes_ $\{K_n\}_{n \in \mathbb{N}}$ are [[CW complexes]] that naturally arrange themselves into a [[topological operad]] that [[resolution|resolves]] the standard [[associative operad]]: an [[A-infinity-operad]]. 

These were introduced by [Stasheff 1963](#Stasheff1963) in order to describe [[topological spaces]] equipped with a multiplication operation that is associative up to [[coherence|coherent]] [[higher homotopy]]:

The [[vertices]] of $K_n$ correspond to ways in which one can bracket a product of $n$ [[variables]], the edges correspond to rebracketings, the faces relate different sequences of rebracketings that lead to the same result, and so on.

Much later, the associahedra also found use in [[quantum field theory]] as a generalization of the "[[amplituhedron]]" in the discussion of certain [[scattering amplitudes]]. 


## Definition

Here is the rough idea, copied, for the moment, verbatim from Markl94 [p. 26] (http://arxiv.org/PS_cache/hep-th/pdf/9411/9411208v1.pdf#page=26) (for more details see references below):

For $n \geq 1$ the **associahedron** $K_n$ is an $(n-2)$-dimensional polyhedron whose $i$-dimensional cells are, for $0 \leq i \leq n-2$, indexed by all (meaningful) insertions of $(n-i-2)$ pairs of brackets between $n$ independent indeterminates, with suitably defined incidence maps. 

[[simplicial set|Simplicially]] ${ }$ [[subdivision|subdivided]] associahedra (complete with simplicial [[operad|operadic]] structure) can be presented efficiently in terms of an abstract [[bar construction]]. Let $\mathcal{O}: Set/\mathbb{N} \to Set/\mathbb{N}$ be the [[monad]] which takes a [[graded set]] $X$ to the non-permutative [[non-unital operad]] freely generated by $X$, with monad multiplication denoted $m: \mathcal{O}\mathcal{O} \to \mathcal{O}$. Let $t_+$ be the graded set $\{X_n\}_{n \geq 0}$ that is [[empty set|empty]] for $n = 0, 1$ and [[terminal object|terminal]] for $n \geq 2$; this carries a unique non-unital non-permutative operad structure, via a structure map $\alpha: \mathcal{O}t_+ \to t_+$. The bar construction $B(\mathcal{O}, \mathcal{O}, t_+)$ is an (augmented) simplicial graded set (an object in $Set^{\Delta^{op} \times \mathbb{N}}$) whose face maps take the form 

$$\ldots \mathcal{O}\mathcal{O}\mathcal{O}t_+ 
\stackrel{\stackrel{\overset{m\mathcal{O} t_+}{\to}}{\underset{\mathcal{O}m t_+}{\to}}}{\underset{\mathcal{O}\mathcal{O}\alpha}{\to}}
\mathcal{O}\mathcal{O}t_+ \stackrel{\overset{m t_+}{\to}}{\underset{\mathcal{O}\alpha}{\to}} \mathcal{O}t_+ \stackrel{\alpha}{\to} t_+.$$ 

Intuitively, the (graded set of) $0$-cells $\mathcal{O}t_+$ consists of planar trees where each inner node has two or more incoming edges, with trees graded by number of leaves; the extreme points are binary trees [corresponding to complete binary bracketings of words], whereas other trees are barycenters of higher-dimensional faces of Stasheff polytopes. The construction $B(\mathcal{O}, \mathcal{O}, t_+)$ carries a simplicial (non-permutative non-unital) operad structure, where the [[geometric realization]] of the simplicial set at grade (or [[arity]]) $n$ defines the barycentric subdivision of the Stasheff polytope $K_n$. As the operad structure on $B(\mathcal{O}, \mathcal{O}, t_+)$ is expressed in [[doctrine|finite product logic]] and geometric realization preserves finite products, the (simplicially subdivided) associahedra form in this way the components of a topological operad. 

## Loday's realization

[[Jean-Louis Loday]] gave a simple formula for realizing the Stasheff polytopes as a convex hull of integer coordinates in Euclidean space [(Loday 2004)](#Loday04).  Let $Y_n$ denote the set of (rooted planar) binary trees with $n+1$ leaves (and hence $n$ internal vertices).  For any binary tree $t \in Y_n$, enumerate the leaves by left-to-right order, denoted $\ell_1, \ldots, \ell_{n+1}$, and enumerate the internal vertices as $v_1, \ldots, v_n$ where $v_i$ is the closest common ancestor of $\ell_i$ and $\ell_{i+1}$. Define a vector $M(t) \in \mathbb{R}^n$ whose $i$th coordinate is the product $a_i b_i$ of the number $a_i$ of leaves that are left descendants of $v_i$ and the number $b_i$ of leaves that are right descendants of $v_i$.

+-- {: .un_thm}
###### Theorem (Loday)
The convex hull of the points $\{ M(t) \in \mathbb{R}^n \mid t \in Y_n \}$ is a realization of the Stasheff polytope of dimension $n-1$, and is included in the affine hyperplane $\{(x_1, \ldots, x_n): x_1 + \ldots + x_n = \binom{n}{2}\}$. 
=-- 


## Illustrations

* **$K_1$** is the [[empty set]], a degenerate case not usually considered.

* **$K_2$** is simply the shape of a binary operation:
$$ x \otimes y ,$$
which we interpret here as a single [[point]].

* **$K_3$** is the shape of the usual [[associator]] or associative law
$$ (x \otimes y) \otimes z \to x \otimes (y \otimes z) ,$$
consisting of a single [[interval]].

* {#K4} **$K_4$** The fourth associahedron $K_4$ is the [[pentagon identity|pentagon]] which expresses the different ways a product of four elements may be bracketed

\begin{tikzcd}[column sep = -3.1em, row sep = 10em, every label/.append style = {font = \Large}, font=\Large]
    & & (w \otimes x) \otimes (y \otimes z) \arrow[drr, "a_{w, x, y \otimes z}"] & & \\
    ((w \otimes x) \otimes y) \otimes z \arrow[urr, "a_{w \otimes x, y, z}"] \arrow[dr,"a_{w,x,y} \otimes \mathrm{id}_{z}", swap] & & & & w \otimes (x \otimes (y \otimes z)) \\
    & (w \otimes (x \otimes y)) \otimes z \arrow[rr, "a_{w, x \otimes y, z}", swap] & & w \otimes ((x \otimes y) \otimes z) \arrow[ur, "\mathrm{id}_{w} \otimes a_{x,y,z}", swap] &
\end{tikzcd}

One can also think of this as the top-level structure of the 4th [[oriental]]. This controls in particular the _pentagon identity_ in the definition of [[monoidal category]], as discussed there.

* **$K_5$** is the [dual polyhedron](http://en.wikipedia.org/wiki/Dual_polyhedron) to the [triaugmented triangular prism](http://en.wikipedia.org/wiki/Triaugmented_triangular_prism) 

+--{: style="text-align:center"}
<img src="https://ncatlab.org/nlab/files/K5associahedron.png" alt="">
<br />

(image from the [Wikimedia Commons](http://commons.wikimedia.org/wiki/File:Polytope_K3.svg))
=--


* One can rotate and explore Stasheff polyhedra in [this interactive associahedron app](https://ltrujello.github.io/associahedron/).


* Illustrations of some polytopes, including $K_5$, can also be found [here](http://irma.math.unistra.fr/~chapoton/galerie.html).

*  A template which can be cut out and assembled into a $K_5$ can be found in Appendix B of [ChengLauda2004](#ChengLauda2004).

## Relation to other structures

### Relation to orientals 

The above list shows that the first few Stasheff polytopes are nothing but the first few [[oriental]]s. This doesn't remain true as $n$ increases.
The orientals are free **strict** [[omega-category|omega-categories]] on [[simplex]]es as parity complexes. This means that certain interchange cells (e.g., Gray tensorators) show up as thin in the oriental description. 

The first place this happens is the sixth oriental: where there are three tensorator squares and six pentagons in Stasheff's $K_5$, the corresponding tensorator squares coming from $O(5)$ are collapsed. 

It was when [[Todd Trimble]] made this point to [[Ross Street]] that Street began to think about using associahedra to define weak [[n-category|n-categories]].


### Categorified associahedra 
 {#Categorification}

There is a [[vertical categorification|categorification]] of associahedra discussed in

* S. Saneblidze, R. Umble, Diagonals on the permutahedra, multiplihedra and associahedra, Homology Homotopy Appl. 6(1) (2004) 363--411.
* {#Forcey12} [[Stefan Forcey]], _Quotients of the multiplihedron as categorified associahedra_, Homology Homotopy Appl. __10__:2 (2008) 227--256 ([Euclid](http://projecteuclid.org/euclid.hha/1251811075))


### Tamari lattice

The associahedron is closely related to a structure known as the _Tamari lattice_, which is especially well-studied in [[combinatorics]].  The Tamari lattice $T_n$ can be defined as the [[poset]] of all parenthesizations of $n+1$ variables with the order generated by rightwards reassociation $(a b)c \le a(b c)$, or equivalently as the poset of all binary trees with $n$ internal nodes (and hence $n+1$ leaves), with the order generated by rightwards tree rotation.  (Note the off-by-one offset from the convention for associahedra: the Tamari lattice $T_n$ corresponds to the associahedron $K_{n+1}$.)  It was originally introduced by Dov Tamari in his thesis "Mono&#239;des pr&#233;ordonn&#233;s et cha&#238;nes de Malcev" (Universit&#233; de Paris, 1951), around a decade before Jim Stasheff's work.[^Stash]

[^Stash]: [[Jim Stasheff]] comments on this in an essay titled "How I 'met' Dov Tamari" [(Tamari Memorial Festschrift 2012)](#TomariFestschrift), writing that the "so-called Stasheff polytope ... more accurately should be called the Tamari or Tamari-Stasheff polytope".

As the name suggests, the Tamari lattice also carries the structure of a [[lattice]].  This property was originally established by Haya Friedman and Tamari (1967), and later simplified by Samuel Huang and Tamari (1972).

## Related concepts

* [[S-matrix]]

* [[scattering amplitudes]]

* [[Yang-Mills theory]]

  * [[super Yang-Mills theory]]

  * [[Tr(ϕ³)]]

* [[amplituhedron]]

* [[cosmohedron]]

## References

The original articles that define associahedra (and in which the [[operad]] $K$ that gives $A(\infty)$-topological spaces is implicit)

* {#Stasheff1963} [[Jim Stasheff]]: *Homotopy associativity of H-spaces I*, Trans. Amer. Math. Soc. **108** (1963) 275-312 &lbrack;[jstor:1993608](http://www.jstor.org/stable/1993608)&rbrack;

  *Homotopy associativity of H-spaces II*, Trans. Amer. Math. Soc. **108* (1963) 293-312 &lbrack;[jstor:1993609](http://www.jstor.org/stable/1993609)&rbrack;

A textbook discussion (slightly modified) is in section 1.6 of the book

* [[Martin Markl]], [[Steven Shnider]], [[Jim Stasheff]], _Operads in Algebra, Topology and Physics_ ([web](http://books.google.de/books?id=fMhZjT9lQo0C&pg=PA56&lpg=PA56&dq=Stasheff+associahedra&source=bl&ots=ZuGXjT4zbp&sig=V-taGG2LHS0msHK-PTxmUXXCvEY&hl=de#PPP1,M1))

Loday's original article on the Stasheff polytope is

* {#Loday04} [[Jean-Louis Loday]], Realization of the Stasheff polytope, _Archiv der Mathematik_ 83 (2004), 267-278. ([doi](https://dx.doi.org/10.1007%2Fs00013-004-1026-y))

Further explanations and references are collected at

* [AMS entry on associahedra](http://www.ams.org/featurecolumn/archive/associahedra.html)

* [[Alexander Postnikov]], _Permutohedra, associahedra and beyond_, [math.CO/0507163](http://arxiv.org/abs/math/0507163) [pdf](http://math.mit.edu/~apost/papers/permutohedron.pdf)

The connection to Tamari lattices as well as other developments are in

* {#TomariFestschrift} Folkert M&#252;ller-Hoissen, Jean Marcel Pallo, [[Jim Stasheff]] (editors), _Associahedra, Tamari Lattices, and Related Structures: Tamari Memorial Festschrift_, Birkh&#228;user, 2012. ([google books](https://books.google.fr/books?id=Y01d6g5UemQC&lpg=PP1&pg=PP1#v=onepage&q&f=false))

For a template of $K_5$, see Appendix B of the following.

* {#ChengLauda2004} [[Eugenia Cheng]], [[Aaron Lauda]], _Higher-dimensional categories: an illustrated guidebook_, 2004, [available here](http://eugeniacheng.com/guidebook/). 

For the combinatorics of associahedra, see

* [[Viviane Pons]], *Combinatorics of the Permutahedra, Associahedra, and Friends* ([arXiv:2310.12687](https://arxiv.org/abs/2310.12687))

For the use of associahedra in [[scattering amplitudes]]: 

* [[Nima Arkani-Hamed]], Yuntao Bai, Song He & Gongwang Yan, _Scattering forms and the positive geometry of kinematics, color and the worldsheet_, Journal of High Energy Physics, Volume 2018, article number 96, (2018) &lbrack;<a href="https://doi.org/10.1007/JHEP05(2018)096">doi:10.1007/JHEP05(2018)096</a>, [arXiv:1711.09102](https://arxiv.org/abs/1711.09102)&rbrack;

* [[Nima Arkani-Hamed]], Song He, Giulio Salvatori, Hugh Thomas, _Causal diamonds, cluster polytopes and scattering amplitudes_, Journal of High Energy Physics, Volume 2022, article number 49, (2022) &lbrack;<a href=" https://doi.org/10.1007/JHEP11(2022)049">doi:10.1007/JHEP11(2022)049</a>, [arXiv:1912.12948](https://arxiv.org/abs/1912.12948)&rbrack;

* Kristian Ranestad, Bernd Sturmfels, Simon Telen: *What is Positive Geometry?* &lbrack;[arXiv:2502.12815](https://arxiv.org/abs/2502.12815)&rbrack;

* Ross Glew, Tomasz Lukowski, _Amplitubes: Graph Cosmohedra_ &lbrack;[arXiv:2502.17564](https://arxiv.org/abs/2502.17564)&rbrack;

Some discussion about the use of associahedra in physics occurred on the category theory Zulip [here](https://categorytheory.zulipchat.com/#narrow/channel/411259-theory.3A-science/topic/Amplituhedron.2C.20associahedron.2C.20and.20related.20approaches). 

category: combinatorics
[[!redirects associahedra]]
[[!redirects Stasheff polytope]]
[[!redirects Tamari polytope]]
[[!redirects Tamari-Stasheff polytope]]