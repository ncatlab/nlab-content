
#Contents#
* table of contents
{:toc}

## Idea

In [[computer science]], originally in [[database theory]], a concept called  *lenses* is used to formally capture situations where some structure is converted to a different form -- a *view* -- in such a way that changes made to the view can be reflected as *updates* to the original structure. The same construction has been devised on numerous occasions ([Hedges](#Hedges)).

There are, in general, two different approaches to lenses:

* Lawful lenses are an algebraic structure which axiomatize product projections. The laws govern the ways views and updates relate. These are generalized into [[delta lens|Delta lenses]], which are more flexible lawful lenses.

* Lawless lenses, and in particular bi-directional or polymorphic lenses, separate the two directions of view and update so that the laws no longer type-check. These lawless lenses are used to organize bi-directional flow of data, and are generalized into [[optics (in computer science)|optics]] in the [[functional programming]] literature. 

An alternate generalization of lawless lenses is put forward in [Spivak 19](#Spivak19) as the Grothendieck construction of the fiberwise dual of an indexed category. This notion of lawless lens has been adopted in the context of categorical systems theory because they represent a *bidirectional stateful computation* which describes the way some systems expose and update their internal state. For instance, see ([Myers](#Myers)), ([Spivak-Niu](#SpivakPoly)), or ([Hedges 21](#Hedges21)).

In this sense, lawless lenses are applications of two mathematical frameworks which are interesting in their own right: [[fibration|fibrations]] and [[optics (in computer science)|optics]] (thus [[Tambara module|Tambara modules]]).



## Definition

Let $(\mathbf{C}, 1, \times)$ be a [[category]] with [[finite products]].

\begin{definition}
Let $S,V$ be objects of $\mathbf C$. 
A **(lawful) lens** $L$, with **source** $S$ and **view** $V$, is a pair of arrows $\mathrm{get} : S \to V$ and $\mathrm{put} : V \times S \to S$, often taken to satisfy the following equations, or _lens laws_:

1. (PutGet) the get of a put is the projection: 
$\mathrm{get} \mathrm{put} = \pi_0$.
2. (GetPut) the put for a trivially updated state is trivial: 
$\mathrm{put} \langle \mathrm{get}, 1_S \rangle = 1_S$.
3. (PutPut) composing puts does not depend on the first view update: $\mathrm{put}(1_V \times \mathrm{put}) = \mathrm{put} \pi_{0,2}$.

\end{definition}

\begin{remark}
The two morphisms comprising a lens can also be called 'view' and 'update'. More generally, they are referred to as the 'forward' and 'backward' parts of the lens.
\end{remark}

\begin{remark}
Sometimes a lens satisfying all three laws is said to be _lawful_. Sometimes it is said that a _well-behaved_ lens satisfies (1) and (2) and a _very well-behaved_ lens satisfies also (3).
\end{remark}

## The category of lenses

Lenses (regardless of their lawfulness) organize in a category $\mathrm{Lens}(\mathbf C)$ whose objects are the same as $\mathbf C$ and whose morphisms $X \to Y$ are lenses with states $X$ and views $Y$. The identity lens is given by $(1_X, \pi_1) :X \to X$. Composition of $(\mathrm{get}_1, \mathrm{put}_{1}):X \to Y$ and $(\mathrm{get}_2, \mathrm{put}_{2}):Y \to Z$ is given by:
$$
  \mathrm{get}_{12} = \mathrm{get}_1 \circ \mathrm{get}_2
$$
$$
  \mathrm{put}_{12} = \mathrm{put}_1 \circ \langle \mathrm{put}_2 \circ \langle 1_Z, \mathrm{get}_1\rangle, 1_X \rangle \circ \langle 1_Z, \Delta_X \rangle
$$
The $\mathrm{put}_{12}$ morphism is probably easier to describe using generalized elements:
$$
  \mathrm{put}_{12} : (z,x) \mapsto \mathrm{put}_1(\mathrm{put}_2(z, \mathrm{get}_1(x)), x)
$$

\begin{remark}
Crucially, associativity of this composition relies on [[monoidal category with diagonals|naturality of the diagonals]], which is a given in cartesian categories but not in more general monoidal categories. [[optic (in computer science)|Optics]] are a sweeping generalization of lenses which overcomes this obstacle.
\end{remark}

Moreover, the [[cartesian product]] of $\mathbf C$ endows $\mathrm{Lens}(\mathbf{C})$ of a [[monoidal product]].

## Properties 

\begin{proposition}
Lenses are [[algebra over a monad|algebras]] for a [[monad]] generated 
by the [[adjunction]]: 
\begin{centre}
\begin{tikzcd}
\mathbf{C}
\arrow[r, shift right=7pt, "\Delta_{V}"', "\bot"] & 
\mathbf{C} / V
\arrow[l, shift right=7pt, "\Sigma"']
\end{tikzcd}
\end{centre}
\end{proposition}
\begin{proof}
See ([Johnson-Rosebrugh-Wood 2010, Proposition 9](#JohnsonRosebrughWood10)). 
See also the [possibility](necessity+and+possibility#globally) operator.
\end{proof}

\begin{proposition}
Let $\mathbf{C} = Set$. 
Then every lens $L = (S, V, \mathrm{get}, \mathrm{put})$ is equivalent a "constant complement" lens whose **Get** is a product projection $\pi_{1} : C \times V \to V$ and whose **Put** is the function $\pi_{0,2} : C \times V \times V \to C \times V$ for some set $C$. 
\end{proposition}
\begin{proof}
See ([Johnson-Rosebrugh-Wood 2010, Corollary 13](#JohnsonRosebrughWood10)).
\end{proof}

\begin{proposition}
Let $\mathbf{C}$ be a cartesian closed category. 
Lenses in $\mathbf{C}$ are [[coalgebra over a comonad|coalgebras]] for a [[comonad]] (the [[store comonad]]) the generated by the [[adjunction]]: 
\begin{centre}
\begin{tikzcd}
\mathbf{C} 
\arrow[r, shift right=7pt, "{[V, -]}"', "\bot"] & 
\mathbf{C} 
\arrow[l, shift right=7pt, "{(-) \times V}"']
\end{tikzcd}
\end{centre}
\end{proposition}
\begin{proof}
See ([Gibbons-Johnson 2012, Section 3.2](#GibbonsJohnson12)).
\end{proof}

## Generalizations

There are many generalizations of lenses which have been proposed, however they can be broadly classified into those which satisfy analogues of the _lens laws_, and those without any axioms or laws. 

### Lenses without laws

* One generalization considers the lenses from the previous section as _monomorphic_ by contrast to _polymorphic_ lens which go between pairs of types, $\lambda: (S, T) \to (A, B)$, consisting of a view function, $v_{\lambda}: S \to A$, and an update function $u_{\lambda}: S \times B \to T$. Without further conditions, these are known as _bimorphic lenses_. To impose conditions comparable to the lens laws above requires that the types be related.

These sorts of lenses are generalized by [Spivak 19](#Spivak19). For a quick explanation of how these sorts of generalized lenses are of use in systems theory, see [Myers20](#Myers20); for a longer explanation, see Chapter 2 of [Myers](#Myers).

* An [[optic (in computer science)|optic]] generalizes the way lenses 'remember' state from the forward part to the backward part, avoiding the necessity of a cartesian structure by swapping it with a sufficiently rich actegorical context.

### Lenses with laws

* [[delta lens|Delta lenses]] are a generalization which does satisfy laws. Here we have categories $S$ and $V$ called the source and view, together with a *Get* functor $g : S \to V$ and a function $\varphi \colon S_{0} \times_{V_{0}} V_{1} \to S_{1}$ which takes a pair $(s \in S, u : gs \to v \in V)$ to a morphism 
$\varphi(s, u) : s \to p(s, u)$ in $S$ where $p(s, u) = cod(\varphi(a, u))$ is the *Put* function. The function $\varphi$ must also satisfy three lens laws. When $S$ and $V$ are [[indiscrete category|codiscrete categories]], delta lenses are equivalent to a lens in [[Set]]; see ([Johnson-Rosebrugh 2016, Proposition 4](#JohnsonRosebrugh16)). 

* A morphism between directed [[polynomial functor|containers]] is another kind of generalised lens satisfying laws called _update-update lenses_; see ([Ahman-Uustalu 2017, Section 5](#AhmanUustalu17)). These are equivalent to [[cofunctor|cofunctors]]. 

## Related entries

* [[optic (in computer science)]]

* [[polynomial functor]]

* [[delta lens]] 

## References

### Journal papers, conference proceedings, and preprints

* {#LastnameAnotherlastnameYear} Aaron Bohannon, Benjamin C. Pierce, Jeffrey A. Vaughan, _Relational lenses: a language for updatable views_, Proceedings of Principles of Database Systems (PODS), 2006 ([doi:10.1145/1142351.1142399](https://doi.org/10.1145/1142351.1142399))

* {#FosterGreenwald07} J. N. Foster, M. B. Greenwald, J. T. Moore, B. C. Pierce, A. Schmitt, _Combinators for bidirectional tree transformations: A linguistic approach to the view-update problem_, ACM Transactions on Programming Languages and Systems, 29, 2007 ([doi:x10.1145/1232420.1232424](https://doi.org/10.1145/1232420.1232424))

* {#JohnsonRosebrughWood10} [[Michael Johnson]], [[Robert Rosebrugh]], [[Richard Wood]], _Algebras and Update Strategies_, Journal of Universal Computer Science, 16, 2010 ([doi:10.3217/jucs-016-05-0729](http://dx.doi.org/10.3217/jucs-016-05-0729))

* {#GibbonsJohnson12} [[Jeremy Gibbons]], [[Michael Johnson]], _Relating Algebraic and Coalgebraic Descriptions of Lenses_, Electronic Communications of the EASST, 49, 2012 ([doi:10.14279/tuj.eceasst.49.726](http://dx.doi.org/10.14279/tuj.eceasst.49.726))

* [[Michael Johnson]], [[Robert Rosebrugh]], and  [[Richard J. Wood]].  _Lenses, fibrations and universal translations._ Math. Structures Comput. Sci., 22(1):25–42, 2012

* {#JohnsonRosebrugh16} [[Michael Johnson]], [[Robert Rosebrugh]], _Unifying Set-Based, Delta-Based and Edit-Based Lenses_, CEUR Workshop Proceedings, 1571, 2016 ([pdf](http://ceur-ws.org/Vol-1571/paper_13.pdf))

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))

* {#Riley} [[Mitchell Riley]], _Categories of optics_, preprint, 2018 ([arXiv:1809.00738](https://arxiv.org/abs/1809.00738))

* {#Spivak19} [[David Spivak]], _Generalized Lens Categories via functors $C^{op} \to Cat$_ ([arXiv:1908.02202](https://arxiv.org/abs/1908.02202))

* {#Myers20} [[David Jaz Myers]], _Double Categories of Dynamical Systems (Extended Abstract)_ ([arXiv:2005.05956](https://arxiv.org/abs/2005.05956))

* {#JohnsonRosebrugh20} [[Michael Johnson]], [[Robert Rosebrugh]], _The more legs the merrier: A new composition for symmetric (multi-)lenses_, EPTCS, 333, 2020 ([arXiv:2101.10482](https://arxiv.org/abs/2101.10482))

* {#Clarke20a} [[Bryce Clarke]], _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} [[Bryce Clarke]], _A diagrammatic approach to symmetric lenses_, EPTCS, 333, 2021 ([arXiv:2101.10481](https://arxiv.org/abs/2101.10481))

* {#Clarke20b} [[Bryce Clarke]], Derek Elkins, Jeremy Gibbons, [[Fosco Loregian]], [[Bartosz Milewski]], Emily Pillmore, Mario Román, _Profunctor optics, a categorical update_, ([arXiv:2001.07488](https://arxiv.org/abs/2001.07488))

### Blog posts, talk slides, and other material

* [[Jeremy Gibbons]], [Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)

* [[Bartosz Milewski]], [Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)

* {#Hedges} [[Jules Hedges]], _Lenses for philosophers_, [blog post](https://julesh.com/2018/08/16/lenses-for-philosophers/)

* {#SpivakACT19} [[David Spivak]], _Lenses:  applications and generalizations_, talk at [ACT 19](http://www.cs.ox.ac.uk/ACT2019/) ([slides](http://math.ucr.edu/home/baez/ACTUCR2019/ACTUCR2019_spivak.pdf), [[Spivak_Lenses.pdf:file]]) 

* {#Myers} [[David Jaz Myers]], _Categorical systems theory_, [github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book)

* {#SpivakPoly} [[David Spivak]], [[Nelson Niu]], _Polynomial Functors: A General Theory of Interaction_, [Current Draft](https://topos.site/poly-book.pdf)

* {#Hedges21} [[Jules Hedges]], _Lenses as a foundation for cybernetics_, CyberCat seminar, [youtube](https://www.youtube.com/watch?v=WkZPH3Vb5ug&t=1927s)

[[!redirects lenses (in computer science)]]

[[!redirects lens in computer science]]
