
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

In [[computer science]], originally in [[database theory]], a data structure called *lenses* &lbrack;[Bohannon, Pierce & Vaughan (2006, §3)](#BohannonPierceVaughan06), [Foster, Greenwald, Moore, Pierce & Schmitt  (2007, §3)](#FosterGreenwaldMoorePierceSchmitt07)&rbrack; is used to formally capture situations where from  some [[data]]([[database|-base]]) may be extracted a specific *view* (say one field  in a record structure) in such a way that changes made to the view can be reflected as *updates* to the original data. 

The same construction has been devised on numerous occasions (cf. [Hedges (2018)](#Hedges18)).

In particular, "well-behaved lenses" ([BPV06, Def. 3.2](#BohannonPierceVaughan06)those for which updates of the "view" completely overwrite any previous such changes) turn out to equivalently be just the [[coalgebra over a comonad|coalgebras]] of the [[costate comonad]] (cf. *[[monads in computer science]]*),  an observation due to [O’Connor (2010)](#O’Connor10), [(2011)](#O’Connor11);  see Prop. \ref{LensesAreCostateCoalgebras} below.
 
More generally, there are two different approaches to lenses:

* Lawful lenses are an algebraic structure which axiomatize product projections. The laws govern the ways views and updates relate. These are generalized into [[delta lens|Delta lenses]], which are more flexible lawful lenses.

* Lawless lenses, and in particular bi-directional or polymorphic lenses, separate the two directions of view and update so that the laws no longer type-check. These lawless lenses are used to organize bi-directional flow of data, and are generalized into [[optics (in computer science)|optics]] in the [[functional programming]] literature. 

An alternate generalization of lawless lenses is put forward in [Spivak 19](#Spivak19) as the [[Grothendieck construction]] of the fiberwise dual of an [[indexed category]]. This notion of lawless lens has been adopted in the context of [[categorical systems theory]] because they represent a *bidirectional stateful computation* which describes the way some systems expose and update their internal state. For instance, see [Myers](#Myers), [Spivak & Niu](#SpivakPoly) or [Hedges (2021)](#Hedges21).

In this sense, lawless lenses are applications of two mathematical frameworks which are interesting in their own right: [[fibration|fibrations]] and [[optics (in computer science)|optics]] (thus [[Tambara module|Tambara modules]]).



## Definition
 {#Definition}

\begin{definition}\label{Lens}
**(lenses)**
\linebreak
Given a [[category]] $(\mathbf{C}, 1, \times)$  with [[finite products]], a *lens* in $\mathbf{C}$ is:

1. a [[pair]] of [[objects]] of $\mathbf{C}$

   1. ("source") 

      $$S \,\in\, \mathbf{C}$$
   
   1. ("view") 

      $$V \,\in\, \mathbf{C}$$

1. a [[pair]] of [[morphisms]] of the form

   1. ("view", "read-out", "forward operation") 

      $$
        \mathrm{get} 
          \;\colon\; 
        S \longrightarrow V
      $$ 

   1. ("update", "write", "backward operation") 

      $$
        \mathrm{put} 
          \;\colon\; 
        V \times S \longrightarrow S
        \,.
      $$ 

The lens is called *well-behaved* if this data satisfies:

* (PutGet) "what has just been written is read out as such": 

  $$
    v \colon V
    ,\,
    s \colon S
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    get\big(
      put 
     (v,\,s) 
    \big)
    \;=\; 
    v
    \,,
  $$

and

* (GetPut) "writing what has just been read out means no change":

  $$
    s \colon S
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    put\big(
      get(s) 
      ,\,
      s
    \big)   
    \;=\;
    s
  $$

and it is called *very well-behaved* or *lawful* if in addition it satisfies:

* (PutPut) "writing means to over-write previous edits":

  $$
    v,\,v' \colon V
    ,\;
    s \colon S
    \;\;\;\;\;\;
    \vdash
    \;\;\;\;\;\;
    put\Big(
      v',\,
      put\big(
        v,\, s 
      \big)
    \Big)
    \;=\;
    put(v',\, s)
  $$

\end{definition}

([Bohannon, Pierce & Vaughan 2006](#BohannonPierceVaughan06), cf. eg. [Johnson, Rosebrugh & Wood 2010, Def. 8](#JohnsonRosebrughWood10))


## The category of lenses

Lenses (regardless of their lawfulness) organize in a category $\mathrm{Lens}(\mathbf C)$ whose objects are the same as $\mathbf C$ and whose morphisms $X \to Y$ are lenses with states $X$ and views $Y$. The identity lens is given by $(1_X, \pi_1) :X \to X$. Composition of $(\mathrm{get}_1, \mathrm{put}_{1}):X \to Y$ and $(\mathrm{get}_2, \mathrm{put}_{2}):Y \to Z$ is given by:
$$
  \mathrm{get}_{12} = \mathrm{get}_2 \circ \mathrm{get}_1
$$
$$
  \mathrm{put}_{12} = \mathrm{put}_1 \circ ((\mathrm{put}_2 \circ (1_Z \times \mathrm{get}_1)) \times 1_X) \circ (1_Z \times \Delta_X)
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

### Monadicity over Possibility monad
 {#PossibilityMonadicity}

\begin{proposition}
\label{LawfulLensesArePossibilityModales}
**(lawful lenses are possibility modales)**
\linebreak
Lawful lenses in $\mathbf{C}$ with view $V$ (Def. \ref{Lens})
are equivalently the [[module of a monad|modules]] ([[modales]]) of the left [[base change]] [[monad]] on the [[slice category]] over $V$ (the $V$-[possibility](necessity+and+possibility#globally)-[[modality]] $\lozenge_V$):

\[
  \label{PossibilityMonadOverTheViewObject}
\]
\begin{tikzcd}
  \mathbf{C}
  \ar[
    r,
    shift right=8pt,
    "{
      \times V
    }"{swap}
  ]
  \ar[
    from=r,
    shift right=8pt,
    "{
      \coprod_{V}
    }"{swap}
  ]
  \ar[
    r,
    phantom,
    "{ \scalebox{.7}{$\bot$} }"
  ]
  &
  \mathbf{C}_{/V}
    \ar[out=40, in=-40,
      looseness=4.5, 
      shorten=-3pt,
      "{
        \lozenge_{V}
      }"{description},
    ]  
\end{tikzcd}

where 

1. $view \,\colon\, S \to V$ is identified with the slicing morphism,

1. $get \,\colon\, V \times S \to S$ is identified with the module action $\lozenge_V(S) \to S$.

\end{proposition} 
\begin{proof}
The objects are identified as shown by direct unwinding of the definitions, as in [Johnson, Rosebrugh & Wood 2010, Prop. 9](#JohnsonRosebrughWood10). (Notice that [JRW10, Def. 10](#JohnsonRosebrughWood10) then *defines* the morphisms of lawful $V$-lenses to coincide with those of $\lozenge_V$-modales.)
\end{proof}


\begin{proposition}
\label{LawfulLensesMonadicity}
  If the ambient category $\mathbf{C}$ is a [[topos]] (such as [[Sets]]) and the view $V$ is [[inhabited object|inhabited]],  then the adjunction (eq:PossibilityMonadOverTheViewObject) is [[monadic functor|monadic]].
\end{proposition}
For the case $\mathbf{C} = Sets$ this is [Johnson, Rosebrugh & Wood 2010, Thm. 12, Cor. 13](#JohnsonRosebrughWood10).
\begin{proof}
 The [[monadicity theorem]] ([here](monadicity+theorem#BeckMonadicityTheoremAlternative)) readily gives that the above adjunction (eq:PossibilityMonadOverTheViewObject) is [[monadic functor]]: $(\text{-})\times V$ [[preserved colimit|preserves]] all colimits (cf. [[universal colimits]]) hence in particular the relevant [[coequalizers]], and it is [[conservative functor|conservative]] by the assumption that $V$ is inhabited (this is clear by inspection in [[Sets]] -- which is what [JRW10](#JohnsonRosebrughWood10) observe on their p. 13 --  for the general case use [[Sketches of an Elephant|Johnstone 2002, vol 1, Lem. 1.3.2]]).
\end{proof}

\begin{remark}
  Prop. \ref{LawfulLensesMonadicity} says that the category of $\lozenge_V$-[[modales]] among objects in $\mathbf{C}_{/V}$ is equivalent to $\mathbf{C}$. This makes good sense when viewing $\lozenge_V$ as the [[possibility]]-[[modality]], see the discussion of *potentiality* [there](necessity+and+possibility#RelationToPotentiality).
\end{remark}

### Monadicity over the CoState comonad
 {#MonadicityOverStateMonade}

\begin{proposition}\label{LensesAreCostateCoalgebras}
**(well-behaved  lenses are the [[costate comonad|costate]] [[coalgebra over a comonad|coalgebras]])**

For $\mathbf{C}$ a [[cartesian closed category]],  the well-behaved lenses in $\mathbf{C}$ are equivalently the [[coalgebra over a comonad|coalgebras]] of the [[costate comonad|CoState]] [[comonad]],  i.e. that induced by the [[internal hom]]-[[adjoint functor|adjunction]]: 

\begin{centre}

\begin{tikzcd}
  \mathbf{C} 
  \arrow[r, shift right=7pt, "{[V, -]}"', "\bot"] 
   & 
  \mathbf{C} 
  \arrow[l, shift right=7pt, "{(-) \times V}"']
\end{tikzcd}

\end{centre}
 
\end{proposition}
This is due to [O’Connor (2010)](#O’Connor10),  [O’Connor (2011)](#O’Connor11), for further discussion see  [Gibbons & Johnson (2012), Section 3.2](#GibbonsJohnson12).

## Generalizations

There are many generalizations of lenses which have been proposed, however they can be broadly classified into those which satisfy analogues of the _lens laws_, and those without any axioms or laws. 

### Lenses without laws

* One generalization considers the lenses from the previous section as _monomorphic_ by contrast to _polymorphic_ lens which go between pairs of types, $\lambda: (S, T) \to (A, B)$, consisting of a view function, $v_{\lambda}: S \to A$, and an update function $u_{\lambda}: S \times B \to T$. Without further conditions, these are known as _bimorphic lenses_. To impose conditions comparable to the lens laws above requires that the types be related.

These sorts of lenses are generalized by [Spivak 19](#Spivak19). For a quick explanation of how these sorts of generalized lenses are of use in systems theory, see [Myers20](#Myers20); for a longer explanation, see Chapter 2 of [Myers](#Myers).

* An [[optic (in computer science)|optic]] generalizes the way lenses 'remember' state from the forward part to the backward part, avoiding the necessity of a cartesian structure by swapping it with a sufficiently rich actegorical context.

### Lenses with laws

* [[delta lens|Delta lenses]] are a generalization which does satisfy laws. Here we have categories $S$ and $V$ called the source and view, together with a *Get* functor $g : S \to V$ and a function $\varphi \colon S_{0} \times_{V_{0}} V_{1} \to S_{1}$ which takes a pair $(s \in S, u : g s \to v \in V)$ to a morphism 
$\varphi(s, u) : s \to p(s, u)$ in $S$ where $p(s, u) = cod(\varphi(a, u))$ is the *Put* function. The function $\varphi$ must also satisfy three lens laws. When $S$ and $V$ are [[indiscrete category|codiscrete categories]], delta lenses are equivalent to a lens in [[Set]]; see ([Johnson-Rosebrugh 2016, Proposition 4](#JohnsonRosebrugh16)). 

* A morphism between directed [[polynomial functor|containers]] is another kind of generalised lens satisfying laws called _update-update lenses_; see ([Ahman-Uustalu 2017, Section 5](#AhmanUustalu17)). These are equivalent to [[cofunctor|cofunctors]]. 

## Related entries

* [[optic (in computer science)]]

* [[polynomial functor]]

* [[delta lens]] 


## References

### General

* {#BohannonPierceVaughan06} Aaron Bohannon, [[Benjamin C. Pierce]], Jeffrey A. Vaughan, *Relational lenses: a language for updatable views*, Proceedings of Principles of Database Systems (PODS) (2006) 338-347 &lbrack;[doi:10.1145/1142351.1142399](https://doi.org/10.1145/1142351.1142399), [pdf](https://www.cis.upenn.edu/~bcpierce/papers/dblenses-pods.pdf)&rbrack;

* {#FosterGreenwaldMoorePierceSchmitt07} J. N. Foster, M. B. Greenwald, J. T. Moore, [[Benjamin C. Pierce]], A. Schmitt, _Combinators for bidirectional tree transformations: A linguistic approach to the view-update problem_, ACM Transactions on Programming Languages and Systems **29** 3 (2007) 17-es &lbrack;[doi:x10.1145/1232420.1232424](https://doi.org/10.1145/1232420.1232424)&rbrack;

* {#JohnsonRosebrughWood10} [[Michael Johnson]], [[Robert Rosebrugh]], [[Richard Wood]], _Algebras and Update Strategies_, Journal of Universal Computer Science **16** (2010) &lbrack;[doi:10.3217/jucs-016-05-0729](http://dx.doi.org/10.3217/jucs-016-05-0729)&rbrack;

* [[Michael Johnson]], [[Robert Rosebrugh]], and  [[Richard J. Wood]], *Lenses, fibrations and universal translations* Math. Structures Comput. Sci. **22** 1 (2012) 25–42 &lbrack;[doi:10.1017/S0960129511000442](https://doi.org/10.1017/S0960129511000442)&rbrack;

* {#JohnsonRosebrugh16} [[Michael Johnson]], [[Robert Rosebrugh]], *Unifying Set-Based, Delta-Based and Edit-Based Lenses*, CEUR Workshop Proceedings **1571** (2016) &lbrack;[pdf](http://ceur-ws.org/Vol-1571/paper_13.pdf)&rbrack;

* {#AhmanUustalu17} Danel Ahman, [[Tarmo Uustalu]], _Taking updates seriously_, CEUR Workshop Proceedings, 1827, 2017 ([pdf](http://ceur-ws.org/Vol-1827/paper11.pdf))

* {#Riley} [[Mitchell Riley]], _Categories of optics_, preprint, 2018 ([arXiv:1809.00738](https://arxiv.org/abs/1809.00738))

* {#Spivak19} [[David Spivak]], _Generalized Lens Categories via functors $C^{op} \to Cat$_ ([arXiv:1908.02202](https://arxiv.org/abs/1908.02202))

* {#Myers20} [[David Jaz Myers]], _Double Categories of Dynamical Systems (Extended Abstract)_ ([arXiv:2005.05956](https://arxiv.org/abs/2005.05956))

* {#JohnsonRosebrugh20} [[Michael Johnson]], [[Robert Rosebrugh]], *The more legs the merrier: A new composition for symmetric (multi-)lenses*, EPTCS **333** (2021) 92-107 &lbrack;[arXiv:2101.10482](https://arxiv.org/abs/2101.10482), [doi:10.4204/EPTCS.333.7](https://doi.org/10.4204/EPTCS.333.7)&rbrack;

* {#Clarke20a} [[Bryce Clarke]], _Internal lenses as functors and cofunctors_, EPTCS, 323, 2020 ([doi:10.4204/EPTCS.323.13](http://dx.doi.org/10.4204/EPTCS.323.13))

* {#Clarke20b} [[Bryce Clarke]], _A diagrammatic approach to symmetric lenses_, EPTCS, 333, 2021 ([arXiv:2101.10481](https://arxiv.org/abs/2101.10481))

* {#Clarke20b} [[Bryce Clarke]], Derek Elkins, Jeremy Gibbons, [[Fosco Loregian]], [[Bartosz Milewski]], Emily Pillmore, Mario Román, _Profunctor optics, a categorical update_, ([arXiv:2001.07488](https://arxiv.org/abs/2001.07488))


### Relation to the costate comonad
 {#ReferencesRelationToCostateComonad}

The observation that lenses are equivalently nothing but the [[coalgebra over a comonad|coalgebras]] of the [[costate comonad]] (cf.  *[[monads in computer science]]*) is due  to:

* {#O’Connor10} [[Russell O’Connor]], *Lenses Are Exactly the Coalgebras for the Store Comonad* (30th Nov 2010) &lbrack;[r6research:23705](https://r6research.livejournal.com/23705.html)&rbrack;

* {#O’Connor11} [[Russell O'Connor]], *Functor is to Lens as Applicative is to Biplate: Introducing Multiplate*, contribution to [ICFP '11: ACM SIGPLAN International Conference on Functional Programming](https://dl.acm.org/doi/proceedings/10.1145/2036918) (2011) &lbrack;[arXiv:1103.2841](https://arxiv.org/abs/1103.2841)&rbrack;

Early review:

* [[Jeremy Gibbons]], *[Lenses are the coalgebras for the costate comonad](https://patternsinfp.wordpress.com/2011/01/31/lenses-are-the-coalgebras-for-the-costate-comonad/)* (2011)

Further details:

* {#GibbonsJohnson12} [[Jeremy Gibbons]], [[Michael Johnson]], *Relating Algebraic and Coalgebraic Descriptions of Lenses*, Electronic Communications of the EASST **49** (2012) &lbrack;[doi:10.14279/tuj.eceasst.49.726](http://dx.doi.org/10.14279/tuj.eceasst.49.726), [pdf](http://www.cs.ox.ac.uk/jeremy.gibbons/publications/colens.pdf)&rbrack;

Further review:

* [[Bartosz Milewski]], *[Lenses, Stores, and Yoneda](https://bartoszmilewski.com/2013/10/08/lenses-stores-and-yoneda/)* (2013)



### Blog posts, talk slides, and other material

* {#Hedges18} [[Jules Hedges]], _Lenses for philosophers_ (2018) &lbrack;[blog post](https://julesh.com/2018/08/16/lenses-for-philosophers/)&rbrack;

* {#SpivakACT19} [[David Spivak]], _Lenses:  applications and generalizations_, talk at [ACT 19](http://www.cs.ox.ac.uk/ACT2019/) ([slides](http://math.ucr.edu/home/baez/ACTUCR2019/ACTUCR2019_spivak.pdf), [[Spivak_Lenses.pdf:file]]) 

* {#Myers} [[David Jaz Myers]], *Categorical systems theory*, &lbrack;[github](https://github.com/DavidJaz/DynamicalSystemsBook/tree/master/book), [pdf](http://davidjaz.com/Papers/DynamicalBook.pdf)&rbrack;

* {#SpivakPoly} [[David Spivak]], [[Nelson Niu]], _Polynomial Functors: A General Theory of Interaction_ &lbrack;[webpage](https://topos.site/poly-course/), [pdf](https://topos.site/poly-book.pdf)&rbrack;

* {#Hedges21} [[Jules Hedges]], _Lenses as a foundation for cybernetics_, CyberCat seminar, [youtube](https://www.youtube.com/watch?v=WkZPH3Vb5ug&t=1927s)

[[!redirects lenses (in computer science)]]

[[!redirects lens in computer science]]
[[!redirects lenses in computer science]]


