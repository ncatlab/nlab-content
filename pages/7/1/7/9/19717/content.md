
#Contents#
* table of contents
{:toc}

## Idea
In [[computer science]], originally in [[database theory]], **lenses** are used in situations where some structure is converted to a different form -- a *view* -- in such a way that changes made to the view can be reflected as updates to the original structure. The same construction has been devised on numerous occasions ([Hedges](#Hedges)).

More recently, lenses (and their [[monoidal category|non-cartesian]] generalization, [[optic (in computer science)|optics]], have been adopted in the context of categorical systems theory, since they represent a *bidirectional stateful computation* remindful of the way some systems expose and update their internal state. For instance, see first chapter of ([Myers and Spivak](#MyersSpivak)) or ([Spivak](#SpivakACT19)).

## Definition

Let $C$ be a [[category]] with [[finite products]]. A **lens** in C denoted $L =(S,V,g,p)$ has states $S$ and view states $V$ which are objects of $C$, and two arrows of C, a *Get* arrow $g:S \to V$ and a *Put* arrow $p:V \times S \to S$, often taken to satisfy the following equations, or _lens laws_:

1. (PutGet) the Get of a Put is the projection: $g p= \pi_0$.
1. (GetPut) the Put for a trivially updated state is trivial: $p \langle g, 1_S \rangle = 1_S$.
1. (PutPut) composing Puts does not depend on the first view update: $p(1_V \times p) = p \pi_{0,2}$.

Sometimes a lens satisfying all three laws is said to be _lawful_. Sometimes it is said that a _well-behaved_ lens satisfies (1) and (2) and a _very well-behaved_ lens satisfies also (3).

In other words, a (lawful) lens for a fixed $V$ is an [[algebra over a monad|algebra]] from the monad $V^{\ast} \cdot \Sigma$ (the [possibility](necessity+and+possibility#globally) operator):

$$
  C/V
  \underoverset
    {\underset{V^{\ast}}{\longleftarrow}}
    {\overset{\Sigma}{\longrightarrow}}
    {\bot}
  C.
$$

They are also [[coalgebra over a comonad|coalgebras]] for the [[store comonad]].

## Generalizations

Many kinds of generalization have been proposed - asymmetric lenses, bimorphic lens, etc.

One generalization considers the lenses from the previous section as _monomorphic_ by contrast to _polymorphic_ lens which go between pairs of types, $\lambda: (S, T) \to (A, B)$, consisting of a view function, $v_{\lambda}: S \to A$, and an update function $u_{\lambda}: S \times B \to T$. Without further conditions, these are known as _bimorphic lenses_. To impose conditions comparable to the lens laws above requires that the types be related.

Another generalization are [[delta lens|delta lenses]]. Here we have categories $S$ and $V$ called the source and view, together with a *Get* functor $g : S \to V$ and a function $\varphi \colon S_{0} \times_{V_{0}} V_{1} \to S_{1}$ which takes a pair $(s \in S, u : gs \to v \in V)$ to a morphism 
$\varphi(s, u) : s \to p(s, u)$ in $S$ where $p(s, u) = cod(\varphi(a, u))$ is the *Put* function. The function $\varphi$ must also satisfy three lens laws. When $S$ and $V$ are [[indiscrete category|codiscrete categories]], delta lenses are equivalent to a lens in [[Set]]; see ([Johnson-Rosebrugh 2016, Proposition 4](#JohnsonRosebrugh16)). 

A morphism between directed [[polynomial functor|containers]] is another kind of generalised lens satisfying laws called _update-update lenses_; see ([Ahman-Uustalu 2017, Section 5](#AhmanUustalu17)). These are equivalent to [[cofunctor|cofunctors]]. 

An [[optic (in computer science)|optic]] defines a symmetric monoidal functor from SymmMonCat to itself. Evaluating the result for different symmetric monoidal categories gives these various generalizations such as Prisms which use the disjoint union in Set. ([Riley Theorem 2.0.8](#Riley))

## Related entries

* [[optic (in computer science)]]

* [[polynomial functor]]

* [[delta lens]] 

##References

* Bohannon, A., Vaughan, J. and Pierce, B. (2006)  _Relational Lenses: A language for updatable views._ Proceedings of Principles of Database Systems (PODS) 2006

* Foster, J., Greenwald, M., Moore, J., Pierce, B. and Schmitt, A. (2007)  _Combinators for bidirectional  tree  transformations:  A  linguistic  approach  to  the  view  update  problem._ ACM Transactions on Programming Languages and Systems 29

* [[Michael Johnson]], [[Robert Rosebrugh]], and R. J. Wood.  _Lenses, fibrations and universal translations._ Math. Structures Comput. Sci., 22(1):25–42, 2012

* [[Bartosz Milewski]], [Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)

* Jeremy Gibbons, [Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)

* {#Hedges} [[Jules Hedges]], _Lenses for philosophers_, [blog post](https://julesh.com/2018/08/16/lenses-for-philosophers/)

* {#Riley} [[Mitchell Riley]], _Categories of optics_, ([arXiv:1809.00738](https://arxiv.org/abs/1809.00738))

* {#SpivakACT19} [[David Spivak]], _Lenses:  applications and generalizations_, [slides](http://math.ucr.edu/home/baez/ACTUCR2019/ACTUCR2019_spivak.pdf) of talk at ACT 19. 

* {#Spivak19} [[David Spivak]], _Generalized Lens Categories via functors $C^{op} \to Cat$_, preprint, 2019 ([arXiv:1908.02202](https://arxiv.org/abs/1908.02202))

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))

* {#JohnsonRosebrugh16} [[Michael Johnson]], [[Robert Rosebrugh]], _Unifying Set-Based, Delta-Based and Edit-Based Lenses_, CEUR Workshop Proceedings, 1571, 2016 ([pdf](http://ceur-ws.org/Vol-1571/paper_13.pdf))

* {#JohnsonRosebrugh20} [[Michael Johnson]], [[Robert Rosebrugh]], _The more legs the merrier: A new composition for symmetric (multi-)lenses_, EPTCS, 333, 2020 ([arXiv:2101.10482](https://arxiv.org/abs/2101.10482))

* {#Clarke20a} Bryce Clarke, _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} Bryce Clarke, _A diagrammatic approach to symmetric lenses_, EPTCS, 333, 2020 ([arXiv:2101.10481](https://arxiv.org/abs/2101.10481))

* {#MyersSpivak} David J. Myers, David I. Spivak, _Categorical systems theory_, [github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book)

[[!redirects lenses (in computer science)]]