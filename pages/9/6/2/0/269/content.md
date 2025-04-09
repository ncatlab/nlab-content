\tableofcontents

\section{Definition}

\begin{notn} We make use of the notation of [[category of cubes]]. \end{notn}

\begin{defn} The _category of cubical sets_ is the [[free co-completion]] of $\square$, the category of cubes. \end{defn}

\begin{rmk} The free co-completion of a small category can be constructed as the category of [[presheaf | presheaves]] of sets on this category. Thus we can also think of the category of cubical sets as the category of presheaves of sets on $\square$. \end{rmk}

\begin{notn} We denote the category of cubical sets by $\mathsf{Set}^{\square^{op}}$. \end{notn}

\begin{defn} A _cubical set_ is an object of $\mathsf{Set}^{\square^{op}}$. \end{defn} 

\begin{rmk} When we think of the category of cubical sets as the category of presheaves of sets on $\square$, we consequently think of a cubical set as a presheaf of sets on $\square$. \end{rmk}

\begin{defn} A _morphism_ of cubical sets is an arrow of $\mathsf{Set}^{\square^{op}}$. \end{defn}

## Idea

The definition is to be understood from the point of view of [[space and quantity]]: a _cubical set_ is a [[space]] characterized by the fact that, and the ways in which, it may be _probed_ by mapping standard cellular [[cubes]] into it: the set $S_n$ assigned by a cubical set to the standard $n$-[[cube]] $[n]$ is the set of $n$-[[cubes]] in this space, hence the way of mapping a standard $n$-[[cube]] into this spaces.

Being a [[functor]] $S : \Box^{op} \to Set$, a cubical set $S$ also assigns maps between its sets $S_n$ of $n$-cubes which determine in which way smaller cubes sit inside larger cubes.

The **face maps**  go from sets $S_{n+1}$ of $(n+1)$-dimensional cubes to the corresponding set $S_{n}$ of $n$-dimensional cubes and can be thought of as sending each cube in the cubical set to one of its faces, for instance for $n=1$ the set $S_2$ of 2-cubes  would be sent in four different ways by four different face maps to the set of $1$-cubes, for instance one of the face maps would send

$$
  \left(
  \array{
     a &\to& b
     \\
     \downarrow &\Downarrow^F& \downarrow
     \\
     c &\to& d
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
     a &\to& b
  }
  \right)
$$

another one would send

$$
  \left(
  \array{
     a &\to& b
     \\
     \downarrow &\Downarrow^F& \downarrow
     \\
     c &\to& d
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
     a
     \\
     \downarrow
     \\
     c
  }
  \right)
  \,.
$$

On the other hand, the **degeneracy maps** go the other way round and send sets $S_n$ of $n$-cubes to sets $S_{n+1}$ of $(n+1)$-cubes by regarding an $n$-cube as a degenerate or "thin" $(n+1)$-cube in the various different ways that this is possible. For instance again for $n=1$ a degeneracy map may act by sending

$$
  \left(
  \array{
     a
     &\stackrel{f}{\to}&
     b
  }
  \right)
  \;\;
  \mapsto
  \;\;
  \left(
  \array{
     a &\stackrel{f}{\to}& b
     \\
     \downarrow^{Id} &\Downarrow^{Id}& \downarrow^{Id}
     \\
     a &\stackrel{f}{\to}& b
  }
  \right)
  \,.
$$

Notice the $Id$-labels, which indicate that the edges and faces labeled by them are "thin" in much the same way as an [[identity morphism]] is thin (notice however that a cubical set by itself is not equipped with a notion of composition of cubes. If it were, we'd call it a [[cubical ∞-category]]).

In an ordinary cubical set all degeneracy maps act in the kind of way depicted above. One might also want to require a cubical set to contain "thin" cells between equal _adjacent_ faces. These **extra degeneracy maps** act by sending 1-cells to degenerate 2-cells of the form

$$\left(\array{
a&\stackrel{f}{\to}&b
}\right)
\;\;
\mapsto
\;\;
\left(\array{
a & \stackrel{f}{\to} & b \\
\downarrow^{f} & \Downarrow & \downarrow^{Id} \\
b & \stackrel{Id}{\to} & b
}\right)
\,.
$$

If the cubical set has this additional property, one calls it a [[connection on a cubical set|cubical set with connection]].

## Monoidal structure

The strict monoidal structure of $\square$ gives rise to a (non-strict) monoidal structure on $\mathsf{Set}^{\square^{op}}$, by [[Day convolution]]. The unit of the monoidal structure is $\square^{0}$, in the notation of Notation \ref{NotationFreeStandingNCube}. Whenever we use the symbol $\otimes$ when working with cubical sets or morphisms of cubical sets, we shall always refer to the functor $- \otimes -$ of this monoidal structure.

## Notation

### Free standing $n$-cube, and an $n$-cube of a cubical set

+-- {: .num_defn #NotationFreeStandingNCube}
###### Notation

Let $y : \square \rightarrow \mathsf{Set}^{\square^{op}}$ denote the [[Yoneda embedding]] functor. Let $n \geq 0$ be an integer. We denote the cubical set $y(I^{n})$ by $\square^{n}$.

=--

+-- {: .num_defn}
###### Terminology

We refer to $\square^{n}$ as the _free-standing $n$-cube_.

=--

+-- {: .num_defn}
###### Terminology

Let $X$ be a cubical set. Let $n \geq 0$ be an integer. By an _$n$-cube_ of $X$, we shall mean a morphism of cubical sets $\square^{n} \rightarrow X$.

=--

+-- {: .num_defn #NotationOneCubePictorial}
###### Notation

Let $f$ be a 1-cube of $X$. We shall often depict $f$ as $f : x_{0} \rightarrow x_{1}$ or as follows. 

$$
   \array{x_{0} & \overset{f}{\rightarrow} & x_{1}}
$$

In this case, $x_{0}$ is to be understood to be the $0$-cube $f \circ y(i_{0})$ of $X$, and $x_{1}$ is to be understood to be the $1$-cube $f \circ y(i_{1})$ of $X$. 

=--

+-- {: .num_defn #NotationTwoCubePictorial}
###### Notation

Let $\sigma$ be a 2-cube of $X$. We shall often depict $\sigma$ as follows.

$$
   \array{
      x_{0}            & \overset{f_{0}}{\rightarrow}  & x_{1} \\
      f_{2} \downarrow & \sigma                & \downarrow f_{1} \\
      x_{2}            & \underset{f_{3}}{\rightarrow} & x_{3}
   }
$$

In this case, $f_{0}$ is to be understood to be the $1$-cube $\sigma \circ y(i_{0} \otimes I^{1})$ of $X$, $f_{1}$ is to be understood to be the $1$-cube $\sigma \circ y(I^{1} \otimes i_{1})$ of $X$, $f_{2}$ is to be understood to be the $1$-cube $\sigma \circ y(I^{1} \otimes i_{0})$ of $X$, and $f_{3}$ is to be understood to be the 1-cube $\sigma \circ y(i_{1} \otimes I^{1})$ of $X$.

It can be checked that this notation is consistent with Notation \ref{NotationOneCubePictorial}.

=--

### Boundary of the free standing $n$-cube, and of an $n$-cube of a cubical set

+-- {: .num_defn}
###### Notation

Let $n \geq 1$ be an integer. We denote by $\partial : \mathsf{Set}^{\square^{op}} \rightarrow \mathsf{Set}^{\square^{op}}$ the functor given by defined by $sk_{n-1} \circ tr_{n-1}$, where $tr_{n-1}$ is the $(n-1)$-[[cubical truncation, skeleton, and co-skeleton | truncation]] functor for cubical sets, and $sk_{n-1}$ is the $(n-1)$-[[cubical truncation, skeleton, and co-skeleton | skeleton]] functor for cubical sets.

=--

+-- {: .num_defn}
###### Terminology

Let $n \geq 0$ be an integer. We refer to $\partial \square^{n}$ as the _boundary_ of $\square^{n}$.

=--

+-- {: .num_defn}
###### Notation

We also denote by $\partial \square^{0}$ (recalling that $\mathsf{Set}^{\square^{op}}$ is, by construction, co-complete) the initial object of $\mathsf{Set}^{\square^{op}}$.

=--

+-- {: .num_defn}
###### Notation

Let $n \geq 1$ be an integer. We denote by $i_{n} : \partial \square^{n} \rightarrow \square^{n}$ the morphism of cubical sets corresponding, under the adjunction between $sk_{n-1}$ and $tr_{n-1}$ described at [[cubical truncation, skeleton, and co-skeleton]], to the identity arrow $tr_{n}(\square^{n}) \rightarrow tr_{n}(\square^{n})$ in $\mathsf{Set}^{\square_{n-1}^{op}}$.

=--

+-- {: .num_defn}
###### Terminology

Let $n \geq 0$ be an integer, and let $\sigma : \square^{n} \rightarrow X$ be an $n$-cube of a cubical set $X$. We refer to the morphism of cubical sets

$$
   \array{\partial \square^{n} & \overset{i_{n}}{\rightarrow} & \square^{n} & \overset{\sigma}{\rightarrow} & X }
$$

as the _boundary_ of $\sigma$.

=--

+-- {: .num_defn #NotationTwoCubeBoundaryPictorial}
###### Notation

Let $\sigma$ be a 2-cube of $X$ as follows.

$$
   \array{
      x_{0}            & \overset{f_{0}}{\to}  & x_{1} \\
      f_{2} \downarrow & \sigma                & \downarrow f_{1} \\
      x_{2}            & \underset{f_{3}}{\to} & x_{3}
   }
$$

We shall often depict the boundary of $\sigma$ as follows.

$$
   \array{
      x_{0}            & \overset{f_{0}}{\to}  & x_{1} \\
      f_{2} \downarrow &                     & \downarrow f_{1} \\
      x_{2}            & \underset{f_{3}}{\to} & x_{3}
   }
$$

=--

### Horns of the free-standing $n$-cube

+-- {: .num_defn #NotationHorn}
###### Notation

We define inductively, for any integer $n \geq 1$, any integer $1 \leq i \leq n$, and any integer $0 \leq \epsilon \leq 1$, a cubical set $\sqcap^{n,i,\epsilon}$ and a morphism of cubical sets $i_{i, \epsilon} : \sqcap^{n,i,\epsilon} \rightarrow \square^{n}$.

When $n=1$, we define both $\sqcap^{1,1,0}$ and $\sqcap^{1,1,1}$ to be $\square^{0}$. We define $i_{1,0} : \square^{0} \rightarrow \square^{1}$ to be $y(i_{0})$, and define $i_{1,1} : \square^{0} \rightarrow \square^{1}$ to be $y(i_{1})$.

Suppose that, for some integer $n \geq 1$, we have defined $\sqcap^{n,i,\epsilon}$ and a morphism of cubical sets $i_{i, \epsilon} : \sqcap^{n,i,\epsilon} \rightarrow \square^{n}$ for all integers $1 \leq i \leq n$, and all integers $0 \leq \epsilon \leq 1$. For $1 \leq i \leq n$, we define (recalling that $\mathsf{Set}^{\square^{op}}$ is co-complete by construction) $\sqcap^{n+1,i, \epsilon}$ to be a cubical set fitting into a [[pushout | co-cartesian square]] in $\mathsf{Set}^{\square^{op}}$ as follows.

$$
   \array{
      \sqcap^{n,i,\epsilon} \sqcup \sqcap^{n,i,\epsilon} & \overset{\big( \sqcap^{n,i,\epsilon} \otimes y(i_{0}) \big) \sqcup \big( \sqcap^{n,i,\epsilon} \otimes y(i_{1}) \big)}{\rightarrow}  & \sqcap^{n,i,\epsilon} \otimes \square^{1} \\
       \mathllap{i_{i,\epsilon} \sqcup i_{i,\epsilon}} \downarrow    &                                    & \downarrow \mathrlap{r_{0}} \\
      \square^{n} \sqcup \square^{n}  & \underset{r_{1 }}{\rightarrow} & \sqcap^{n+1,i,\epsilon}
   }
$$

We denote by $i_{i,\epsilon} : \sqcap^{n+1,i,\epsilon} \rightarrow \square^{n+1}$ the canonical arrow determined, by means of the universal property of $\sqcap^{n+1,i,\epsilon}$, by the following commutative square in $\mathsf{Set}^{\square^{op}}$.

$$
   \array{
      \sqcap^{n,i,\epsilon} \sqcup \sqcap^{n,i,\epsilon} & \overset{\big( \sqcap^{n,i,\epsilon} \otimes y(i_{0}) \big) \sqcup \big( \sqcap^{n,i,\epsilon} \otimes y(i_{1}) \big)}{\rightarrow}  & \sqcap^{n,i,\epsilon} \otimes \square^{1} \\
       \mathllap{i_{i,\epsilon} \sqcup i_{i,\epsilon}} \downarrow    &                                    & \downarrow \mathrlap{i_{i,\epsilon} \otimes \square^{1}} \\
      \square^{n} \sqcup \square^{n}  & \underset{\big( \square^{n} \otimes y(i_{0}) \big) \sqcup \big( \square^{n} \otimes y(i_{1}) \big)}{\rightarrow} & \square^{n+1}
   }
$$

We define $\sqcap^{n+1, n+1, \epsilon}$ to be a cubical set fitting into a [[pushout | co-cartesian square]] in $\mathsf{Set}^{\square^{op}}$ as follows.

$$
   \array{
      \sqcap^{n,n,\epsilon} \sqcup \sqcap^{n,n,\epsilon} & \overset{\big( y(i_{0}) \otimes \sqcap^{n,n,\epsilon} \big) \sqcup \big( y(i_{1}) \otimes \sqcap^{n,n,\epsilon} \big)}{\rightarrow}  & \square^{1} \otimes \sqcap^{n,n,\epsilon} \\
       \mathllap{i_{n,\epsilon} \sqcup i_{n,\epsilon}} \downarrow    &                                    & \downarrow \mathrlap{r_{0}} \\
      \square^{n} \sqcup \square^{n}  & \underset{r_{1}}{\rightarrow} & \sqcap^{n+1,n+1,\epsilon}
   }
$$

We denote by $i_{n+1,\epsilon} : \sqcap^{n+1,n+1,\epsilon} \rightarrow \square^{n+1}$ the canonical arrow determined, by means of the universal property of $\sqcap^{n+1,n+1,\epsilon}$, by the following commutative square in $\mathsf{Set}^{\square^{op}}$.

$$
   \array{
      \sqcap^{n,n,\epsilon} \sqcup \sqcap^{n,n,\epsilon} & \overset{\big( y(i_{0}) \otimes \sqcap^{n,n,\epsilon} \big) \sqcup \big( y(i_{1}) \otimes \sqcap^{n,n,\epsilon} \big)}{\rightarrow}  & \square^{1} \otimes \sqcap^{n,n,\epsilon} \\
       \mathllap{i_{n,\epsilon} \sqcup i_{n,\epsilon}} \downarrow    &                                    & \downarrow \mathrlap{\square^{1} \otimes i_{n,\epsilon}} \\
      \square^{n} \sqcup \square^{n}  & \underset{\big( y(i_{0}) \otimes \square^{n} \big) \sqcup \big( y(i_{1}) \otimes \square^{n} \big)}{\rightarrow} & \square^{n+1}
   }
$$

=--

+-- {: .num_defn}
###### Terminology

We refer to $\sqcap^{n, i, \epsilon}$ together with the morphism $i_{i,\epsilon}$ as a _horn_ of $\square^{n}$. 

=--

### Morphism from $\square^{n}$ to $\square^{0}$

+-- {: .num_defn}
###### Notation

We denote by $p : \square^{n} \rightarrow \square^{0}$ the arrow $y(\underbrace{p \otimes p \otimes \cdots p}_{n})$ of $\mathsf{Set}^{\square^{op}}$, making use of the fact that $\underbrace{\square^{0} \otimes \square^{0} \otimes \cdots \square^{0}}_{n}$ is $\square^{0}$, since $\square^{0}$ is the unit of the monoidal structure of $\mathsf{Set}^{\square^{op}}$.

=--


## Cubical sets in homotopy theory 
 {#InHomotopyTheory}

[[Daniel Kan]]'s early work on [[homotopy theory]] used cubical sets instead of [[simplicial set]]s. But then a bit later it was found that plain cubical sets suffer from three disadvantages when it comes to modelling [[homotopy type|homotopy n-type]]s:

1. [[Moore complex|normalization of chains]] is essential

1. [[cubical group]]s are not automatically fibrant

1. the [[geometric realization]] of [[cartesian product]]s of cubical sets (see [geometric realization](#GeometricRealization) below) tends to have the wrong [[homotopy n-type|homotopy type]]:

   for instance the geometric realization of the cubical set $I \times I$ has non-trivial [[homotopy group]]s and hence does not model the [[topological space]] given by the standard square, which is [[contractible]].

It was then realized that none of these problems is shared by [[simplicial sets]]:

1. Eilenberg and Mac Lane proved a normalisation theorem which may be found in Mac Lane's book 'Homology'. 

1. every [[simplicial group]] is necessarily a [[Kan complex]] and therefore fibrant in the standard [[model structure on simplicial sets]]

1. [[geometric realization]] of [[simplicial set]]s is well behaved and in fact constitutes a [[cartesian monoidal category|cartesian monoidal]] [[Quillen equivalence]] 

   $$
      |-| : SSet \stackrel{\leftarrow}{\to} Top : S(-)
   $$

   between [[SSet]] and [[Top]]. For more on this see [[homotopy hypothesis]].

These observations led to a widespread use of simplicial methods, while cubical methods coexisted only with a kind of underground existence, to this date.

There is, however, a proof of parts of the [[homotopy hypothesis]] also for cubical sets: their [[homotopy category]] is equivalent, after all, to the standard homotopy catgeory [[Top]]. This is described at [[model structure on cubical sets]].


Also, it turns out that the second and third of the above disadvantages of [[cubical set]]s over [[simplicial sets]] in [[homotopy theory]] can be dealt with to some extent.

1. The first problem can't be avoided. See

   Rosa Antolini and Bert Wiest, _The singular cubical set of a topological space_ , Mathematical Proceedings of the Cambridge Philosophical Society, 126 (1),  (1999)

1. The second problem is resolved, at least when restricting to [[strict omega-groupoid]]s by using [[connection on a cubical set|cubical sets with connection]]. See

   A. P. Tonks, _Cubical groups which are Kan_, J. Pure Appl. Algebra, 81 (1),  (1992) 

1. the third problem is due to the fact that the [[cube category]] is a [[test category]] but not a [[strict test category]]. However, the category of cubes _[[connection on a cubical set|with connection]]_ is a strict test category, as shown by [[Georges Maltsiniotis]], based on work by [[Denis-Charles Cisinski]]. See _[[connection on a cubical set]]_ for details.


### Geometric realization
 {#GeometricRealization}

If $X$ is a cubical set, the [[geometric realization]] $|X|$ may be defined as the [[weighted colimit]] (a [[coend]]) in [[Top]] 

$$X \otimes_{\Box} I^{\bullet} = \int^{n \in \Box} X(n) \cdot I^n$$ 

where $I^{\bullet}: (\Box, \otimes, I) \to (\Top, \times, 1)$ is the unique (up to isomorphism) monoidal functor mapping the generating object $int$ to $[0, 1]$, and for $k = 0, 1$, mapping $i_k$ to the inclusion $\{k\} \hookrightarrow [0, 1]$. This is parallel to one way of defining the [[geometric realization]] of a [[simplicial set]]. 
Geometric realization is a functor [[adjoint functor|left adjoint]] to the functor 
$$cub: Top \to Set^{\Box^{op}}$$ 
which takes a space $S$ to the functor $\hom_{Top}(I^{\bullet}-, S)$. 

### Subdivision and fibrant replacement 

A cubical subdivision functor $sd$ is discussed in [Jardine 0, Section 5](#Jardine02). It is an obvious subdivision of an $n$-cube, which is just a product of barycentric subdivisions of intervals. The (functorial) subdivision $sd X$ of a cubical set $X$ is constructed from this naive subdivision of the $n$-cube in the end.
See [Jardine's lecture notes](#Jardine02) for details. There is a natural sequence of maps of cubical sets


$$
\cdots  \to sd^n X \to \cdots  \to sd X  \to X
$$

defined similar to its [[Kan fibrant replacement|simplicial counterparts]]. Let its [[right adjoint]] be
denoted as usual by $Ex X$. So $n$-cubes of $Ex X$ are cubical maps from subdivision of the $n$-cube to $X$ (similar to the definition of [[Kan fibrant replacement|simplicial
Ex-functor]]). We therefore get maps

$$
 X  \to Ex X \to Ex^2 X  \to \cdots
$$

Let $Ex^\infty X$ be the union of the latter maps (similar to simplicial $Ex^\infty$).

**question**: Is $Ex^\infty X$  a fibrant cubical set for any cubical set $X$?. 

Recall that a cubical set is fibrant if any
cubical horn has a filler (similar to [[simplicial set]]: any [[Kan complex|Kan fibrant]] simplicial set has [[horn]] fillers). See also ([Cisinski 2006](#Cisinski06)) or [Jardine's lectures on cubical sets](#JardineLecture) for definitions.


The first question is probably not true in general, but if we consider cubical sets with [[connection on a cubical set|connections]] in the sense of Brown-Higgins (we
add some degeneracy maps to cubical sets), see e.g. [Maltsiniotis paper](http://people.math.jussieu.fr/~maltsin/ps/cubique.ps) then the cubical subdivision remains the same and the $Ex^\infty X$ is
defined similarly. The question is whether $Ex^\infty X$ with $X$ a cubical set with connections is fibrant. **Is it true?**


### Model category structure and homotopy theory
 {#ModelCategoryStructureAndHomotopyTheory}

There is a [[Cisinski model structure]] on cubical sets with the same [[homotopy theory]] as the standard [[model structure on simplicial sets]] ([Jardine 02](#Jardine02)), which models [[homotopy types]]/[[infinity-groupoids]]. See the article [[model structure on cubical sets]] for more information.

In fact ([Jardine 02, theorem 29, theorem 30](#Jardine02)) gives an [[adjunction]] between the [[model categories]] which, while not quite a [[Quillen adjunction]], does have [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]] being [[weak equivalences]]. Hence by the discussion at _[[adjoint (∞,1)-functor]]_  it should indeed follow that the [[derived functors]] of the adjunction exhibit the [[simplicial localizations]] of cubical sets equivalent to that of simplicial sets, hence make their [[(∞,1)-categories]] [[equivalence of (∞,1)-categories|equivalent]] (hence equivalent to [[∞Grpd]]). 

This generalizes to a local [[model structure on cubical presheaves]] over any [[site]], which has at least the same [[homotopy category]] as the corresponding local [[model structure on simplicial presheaves]].

The category of cubical sets also admits a Joyal-type model structure, which admits a [[Quillen equivalence]] to the [[Joyal model structure]] on [[simplicial sets]].
See the article [[model structure for cubical quasicategories]] for more information.

## Background

The notion of cubical set and of homology theory and homotopy theory based on singular cubes goes way back in the literature. Serre's work on spectral sequences and fibre spaces was based on cubes. Kan's early work on combinatorial homotopy was based on cubes. However the category of cubical sets was found to have a major disadvantage compared with simplicial sets, in that the [[cartesian product]] in this category failed to have the correct [[homotopy type]]. This is in striking contrast to the cartesian product on [[simplicial set]]s.

Nonetheless cubical sets continued to have a kind of underground existence. 

Brown and Higgins introduced the extra structure of [[connection on a cubical set|connections]] $\Gamma^\pm_i$ on cubical sets, and included this structure into their cubical  [[strict ∞-groupoids]]. All this structure was essential for the equivalence with [[crossed complexes]] and for the applications to homotopy theory. For example these $\omega$-groupoids have a canonical structure of [[thin elements]], defined as any composition of elements of the form $\pm \epsilon_j x, \pm \Gamma^\pm_i$. Such elements have "commuting boundary". 

The geometric realisation of cubical sets with connections, and the relation with cartesian products, has been analysed by Maltsiniotis in the paper referred to below. 

Nonetheless, the advantages of cubes are:

1. Easy notions of multiple compositions (compared with the globular pasting schemes); we refer to [[compositions in cubical sets]]. 

1. Good notions of tensor product, because of the rule $I^m \times I^n \cong I^{m+n}$, and hence easy conceptual handling of homotopies.  This is exploited in the paper by Brown and Higgins on tensor products,  and also in the following paper

* Al-Agl, F. A., [[Ronnie Brown]],  and Steiner, R. Multiple categories: the equivalence of a globular and a   cubical approach. _Adv. Math._ 170~(1) (2002) 71--118.

which gives a monoidal closed structure on cubical $\omega$-categories with connections, allowing the transfer of this to globular $\omega$-categories. The tensor product here generalises the [[Gray  tensor product]] of 2-categories. This is also convenient in the [[homotopical structure on C*-algebras]].

Cubical methods are a key feature in using higher homotopy groupoids to prove homotopy classification results.  

## Related entries

### General

* [[bicubical sets]]

* [[cubical object]]

### Applications of cubical sets

* [[cubical type theory]]

#### In higher category theory

* [[fundamental groupoid of a cubical set and the cubical nerve of a groupoid]]

* [[homotopy hypothesis for 1-types]]

* [[cubical infinity-groupoid]]

### Theory of cubical sets

* [[category of cubes]]

* [[cubical geometric realisation]]

* [[cubulation]]

* [[cubical truncation, skeleton, and co-skeleton]]

* [[homotopy groups of a cubical Kan complex]]

* [[model structure on cubical sets]]

* [[model structure on cubical presheaves]]

## References

The original reference for cubical sets (based on the 1950 paper by [[Samuel Eilenberg]] and [[J. A. Zilber]] on [[simplicial sets]]) is

* [[Daniel M. Kan]], _Abstract homotopy.  I_, Proceedings of the National Academy of Sciences 41:12 (1955), 1092–1096.  [doi](http://dx.doi.org/10.1073/pnas.41.12.1092).

Kan switched to [[simplicial sets]] in Part III of the series.

Another early reference is

* [[Jean-Pierre Serre]], _Homologie singuli&#232;re des espaces fibr&#233;s_ , Ann.
Math. **54** no.3 (1951), pp.425-505. ([pdf](http://www.college-de-france.fr/media/jean-pierre-serre/UPL7235285843586540944_Serre_The_se.pdf))

General introductions of the cube category and of cubical sets are in 

* {#JardineLecture} [[Rick Jardine]], _Cubical sets_, Lecture 12 in [Fields Lectures on simplicial presheaves](https://www.uwo.ca/math/faculty/jardine/courses/fields/fields-01.pdf) (unpublished).
 

* [[Sjoerd Crans]], section 2 of _Pasting schemes for the monoidal biclosed structure on $\omega$-$\mathbf{Cat}$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

The **cubical identities** satisfied by a cubical set are given there in proposition 2.8 on p. 9.


Cubical [[singular homology]] is discussed in

* Massey, W. S.,   _Singular homology theory_, _Graduate Texts in
  Mathematics_, Volume~70. Springer-Verlag, New York (1980).


An axiomatization of cubical sets in [[constructive set theory]]/[[type theory]] (with the aim of building models of [[homotopy type theory]]) is in

* {#BezemCoquandHuber13} Marc Bezem, [[Thierry Coquand]], [[Simon Huber]], _A model of type theory in cubical sets_, 2013  ([web](http://drops.dagstuhl.de/opus/volltexte/2014/4628/), [pdf](http://drops.dagstuhl.de/opus/volltexte/2014/4628/pdf/7.pdf))

* {#KaposiAltenkirch14} Ambrus Kaposi, [[Thorsten Altenkirch]], _A syntax for cubical type theory_ ([pdf](http://mazzo.li/dump/aim-kaposi-pres.pdf))

* {#Docherty14} Simon Docherty, _A model of type theory in cubical sets with connection_, 2014 ([pdf](http://www.illc.uva.nl/Research/Publications/Reports/MoL-2014-12.text.pdf))

See also

* [[Dan Licata]], [[Guillaume Brunerie]], _A cubical approach to synthetic homotopy theory_ ([pdf](http://dlicata.web.wesleyan.edu/pubs/lb15cubicalsynth/lb15cubicalsynth.pdf))

For more on this see at _[[relation between category theory and type theory]]_.

The [[homotopy theory]] / [[model category]] structure on cubical sets is discussed in 

* {#Jardine02} [[Rick Jardine]], _Cubical homotopy theory: a beginning_ (2002) ([pdf](https://web.archive.org/web/20201229182153/http://hopf.math.purdue.edu/Jardine/cubical2.pdf)) 
 

The fact that the [[exponential object]] of two fibrant cubical sets is again fibrant follows from remark 8.4.33 in 

* {#Cisinski06} [[Denis-Charles Cisinski]], _[[joyalscatlab:Les préfaisceaux comme type d'homotopie]]_, Astérisque, Volume 308, Soc. Math. France (2006), 392 pages ([pdf](http://www.mathematik.uni-regensburg.de/cisinski/ast.pdf))
 

in the context of [[Cisinski model structures]].

Finally cubical sets as [[categorical semantics]] for [[homotopy type theory]] with [[univalence]] is discussed in

* {#Cisinski14} [[Denis-Charles Cisinski]], _Univalent universes for elegant models of homotopy types_ ([arXiv:1406.0058](http://arxiv.org/abs/1406.0058))


The [[strict test category]] nature of cubical sets with connection is discussed in

* [[Georges Maltsiniotis]], _La cat&#233;gorie cubique avec connexions est une cat&#233;gorie test stricte_. Homology, Homotopy Appl. 11~(2) (2009) 309--326.

There is also the old work

* Victor Gugenheim, _On supercomplexes_ Trans. Amer. Math. Soc. 85 (1957), 35&#8211;51 [PDF](https://www.ams.org/journals/tran/1957-085-01/S0002-9947-1957-0086299-1/S0002-9947-1957-0086299-1.pdf)

in which "supercomplexes" are discussed, that combine simplicial sets and cubical sets (def 5). There are functors from simplicial sets to supercomplexes (after Defn 5) and, implicitly, from supercomplexes to cubical sets (in Appendix II). This was written in 1956, long before people were thinking as formally as nowadays and long before Quillen model theory, but a comparison of the homotopy categories might be in there.


A discussion of cubical sets and normal forms in several cases is in

* [[Marco Grandis]], and Mauri, L. Cubical sets and their site, _Theory Applic. Categories_ {11} (2003) 185--201.


Cubical sets as models for [[strict ∞-groupoids]] are discussed in

* [[Ronnie Brown]], P. Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

Their use for monoidal closed structures  and homotopy classification is given in 

* [[Ronnie Brown]] and P. Higgins,  Tensor products and homotopies for $\omega$-groupoids and crossed complexes.  _J. Pure Appl. Algebra_ 47 (1987) 1--33.

and are essential in 

* [[Ronnie Brown]], Philip J. Higgins and Rafael Sivera, _[[Nonabelian Algebraic Topology]]_ EMS Tracts in Math vol 15, 703 pages, August, 2011. ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).

Essential subtoposes of $Set^{\Box^{op}}$ are discussed in the context of Lawvere's dialectical theory of dimension in

* {#KRRZ10} C. Kennett, [[Emily Riehl|E. Riehl]], M. Roy, M. Zaks, _Levels in the toposes of simplicial sets and cubical sets_ , JPAA **215** no.5 (2011) pp.949-961. ([preprint](http://arxiv.org/abs/1003.5944))

A [[constructive mathematics|constructive]] model of [[homotopy type theory]] in a [[Quillen model category]] of [[cubical sets]] that [[classical mathematics|classically]] presents the usual [[homotopy theory]] of [[spaces]]:

* [[Steve Awodey]], [[Evan Cavallo]], [[Thierry Coquand]], [[Emily Riehl]], [[Christian Sattler]], *The equivariant model structure on cartesian cubical sets* ([arXiv:2406.18497](https://arxiv.org/abs/2406.18497))

[[!redirects Cubical set]]
[[!redirects Cubical Set]]
[[!redirects Cubical set]]
[[!redirects cubical set]]
[[!redirects category of cubical sets]]
[[!redirects cubical sets]]
[[!redirects cubical set - exposition]]