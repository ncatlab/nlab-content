
#Contents#
* table of contents
{:toc}

## Idea

In [[computer science]], originally in [[database theory]], a concept called  *lenses* is used to formally capture situations where some structure is converted to a different form -- a *view* -- in such a way that changes made to the view can be reflected as updates to the original structure. The same construction has been devised on numerous occasions ([Hedges](#Hedges)).

An insightful explanation and critique of the concept of "lenses" is offered in [Spivak 19](#Spivak19) (exposition in [Spivak ACT19](#SpivakACT19)), where it is argued that the notion may and should be regarded as a small fragment (namely that of [[trivial bundle|trivial]] [[display maps]]) of the general notion of ([[categorical model of dependent types|categorical semantics]] for) [[dependent type theory|dependent types]], such as discussed at *[[hyperdoctrine]]* and related entries.

More recently, lenses have been adopted in the context of categorical systems theory, since they represent a *bidirectional stateful computation* remindful of the way some systems expose and update their internal state. For instance, see first chapter of ([Myers and Spivak](#MyersSpivak)) or ([Spivak ACT19](#SpivakACT19)).

## Definition

Let $(\mathbf C, 1, \times)$ be a [[category]] with [[finite products]].

***Definition 1***. Let $S,V$ be objects of $\mathbf C$. A **lens** $L$, with *states* $S$ and *views* $V$, is a pair of arrows $\mathrm{get}:S \to V$ and $\mathrm{put}:V \times S \to S$, often taken to satisfy the following equations, or _lens laws_:

1. (PutGet) the get of a put is the projection: $\mathrm{get} \mathrm{put} = \pi_0$.
1. (GetPut) the put for a trivially updated state is trivial: $\mathrm{put} \langle \mathrm{get}, 1_S \rangle = 1_S$.
1. (PutPut) composing puts does not depend on the first view update: $\mathrm{put}(1_V \times \mathrm{put}) = \mathrm{put} \pi_{0,2}$.

**Remark 1**. The two morphisms comprising a lens can also be called 'view' and 'update'. More generally, they are referred to as the 'forward' and 'backward' parts of the lens.

**Remark 2**. Sometimes a lens satisfying all three laws is said to be _lawful_. Sometimes it is said that a _well-behaved_ lens satisfies (1) and (2) and a _very well-behaved_ lens satisfies also (3).

In other words, a (lawful) lens for a fixed $V$ is an [[algebra over a monad|algebra]] from the monad $V^{\ast} \cdot \Sigma$ (the [possibility](necessity+and+possibility#globally) operator):

$$
  \mathbf C/V
  \underoverset
    {\underset{V^{\ast}}{\longleftarrow}}
    {\overset{\Sigma}{\longrightarrow}}
    {\bot}
  \mathbf C.
$$

They are also [[coalgebra over a comonad|coalgebras]] for the [[store comonad]].

Lenses (regardless of their lawfulness) organize in a category $\mathrm{Lens}(\mathbf C)$ whose objects are the same as $\mathbf C$ and whose morphisms $X \to Y$ are lenses with states $X$ and views $Y$. The identity lens is given by $(1_X, \pi_1) :X \to X$. Composition of $(\mathrm{get}_1,g):X \to Y$ and $(\mathrm{get}_2,k):Y \to Z$ is given by:
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

**Remark 2**. Crucially, associativity of this composition relies on naturality of the diagonals $\Delta$, which is a distinctively cartesian feature. [[optic (in computer science)|Optics]] are a sweeping generalization of lenses which overcomes this obstacle.

Moreover, the [[cartesian product]] of $\mathbf C$ endows $\mathrm{Lens}(\mathbf C)$ of a [[monoidal product]].

## Generalizations

Many kinds of generalization have been proposed - asymmetric lenses, bimorphic lens, etc.

One generalization considers the lenses from the previous section as _monomorphic_ by contrast to _polymorphic_ lens which go between pairs of types, $\lambda: (S, T) \to (A, B)$, consisting of a view function, $v_{\lambda}: S \to A$, and an update function $u_{\lambda}: S \times B \to T$. Without further conditions, these are known as _bimorphic lenses_. To impose conditions comparable to the lens laws above requires that the types be related.

Another generalization are [[delta lens|delta lenses]]. Here we have categories $S$ and $V$ called the source and view, together with a *Get* functor $g : S \to V$ and a function $\varphi \colon S_{0} \times_{V_{0}} V_{1} \to S_{1}$ which takes a pair $(s \in S, u : gs \to v \in V)$ to a morphism 
$\varphi(s, u) : s \to p(s, u)$ in $S$ where $p(s, u) = cod(\varphi(a, u))$ is the *Put* function. The function $\varphi$ must also satisfy three lens laws. When $S$ and $V$ are [[indiscrete category|codiscrete categories]], delta lenses are equivalent to a lens in [[Set]]; see ([Johnson-Rosebrugh 2016, Proposition 4](#JohnsonRosebrugh16)). 

A morphism between directed [[polynomial functor|containers]] is another kind of generalised lens satisfying laws called _update-update lenses_; see ([Ahman-Uustalu 2017, Section 5](#AhmanUustalu17)). These are equivalent to [[cofunctor|cofunctors]]. 

An [[optic (in computer science)|optic]] generalizes the way lenses 'remember' state from the forward part to the backward part, avoiding the necessity of a cartesian structure by swapping it with a sufficiently rich actegorical context.

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


* {#SpivakACT19} [[David Spivak]], _Lenses:  applications and generalizations_, talk at [ACT 19](http://www.cs.ox.ac.uk/ACT2019/) ([slides](http://math.ucr.edu/home/baez/ACTUCR2019/ACTUCR2019_spivak.pdf), [[Spivak_Lenses.pdf:file]]) 

* {#Spivak19} [[David Spivak]], _Generalized Lens Categories via functors $C^{op} \to Cat$_ ([arXiv:1908.02202](https://arxiv.org/abs/1908.02202))

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))

* {#JohnsonRosebrugh16} [[Michael Johnson]], [[Robert Rosebrugh]], _Unifying Set-Based, Delta-Based and Edit-Based Lenses_, CEUR Workshop Proceedings, 1571, 2016 ([pdf](http://ceur-ws.org/Vol-1571/paper_13.pdf))

* {#JohnsonRosebrugh20} [[Michael Johnson]], [[Robert Rosebrugh]], _The more legs the merrier: A new composition for symmetric (multi-)lenses_, EPTCS, 333, 2020 ([arXiv:2101.10482](https://arxiv.org/abs/2101.10482))

* {#Clarke20a} [[Bryce Clarke]], _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} [[Bryce Clarke]], _A diagrammatic approach to symmetric lenses_, EPTCS, 333, 2020 ([arXiv:2101.10481](https://arxiv.org/abs/2101.10481))

* {#MyersSpivak} [[David Myers]], [[David Spivak]], _Categorical systems theory_, [github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book)

[[!redirects lenses (in computer science)]]

[[!redirects lens in computer science]]
