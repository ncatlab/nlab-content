+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

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

There is a [[model structure on cubical sets]] with the same [[homotopy theory]] as the standard [[model structure on simplicial sets]] ([Jardine 02](#Jardine02)), which models [[homotopy types]]/[[infinity-groupoids]]. 

In fact ([Jardine 02, theorem 29, theorem 30](#Jardine02)) gives an [[adjunction]] between the [[model categories]] which, while not quite a [[Quillen adjunction]], does have [[unit of an adjunction|unit]] and [[counit of an adjunction|counit]] being [[weak equivalences]]. Hence by the discussion at _[[adjoint (∞,1)-functor]]_  it should indeed follow that the [[derived functors]] of the adjunction exhibit the [[simplicial localizations]] of cubical sets equivalent to that of simplicial sets, hence make their [[(∞,1)-categories]] [[equivalence of (∞,1)-categories|equivalent]] (hence equivalent to [[∞Grpd]]). 

This generalizes to a local [[model structure on cubical presheaves]] over any [[site]], which has at least the same [[homotopy category]] as the corresponding local [[model structure on simplicial presheaves]].

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


## Related concepts

* [[cubical object]]

* [[model structure on cubical presheaves]]

* [[simplicial set]], [[globular set]], [[cellular set]], [[dendroidal set]]

* [[simplicial object]]

  * [[simplicial object in an (∞,1)-category]]

* [[semi-simplicial object]]

  * [[semisimplicial set]]



## References

Early references include

* [[Jean-Pierre Serre]], _Homologie singuli&#232;re des espaces fibr&#233;s_ , Ann.
Math. **54** no.3 (1951), pp.425-505. ([pdf](http://www.college-de-france.fr/media/jean-pierre-serre/UPL7235285843586540944_Serre_The_se.pdf))

* [[Dan Kan]], _Abstract homotopy I_ , Proc. Nat. Acad. Sci. U.S.A. **41** (1955) pp.1092&#8211;1096. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC528202/pdf/pnas00727-0082.pdf))
 {#Kan}

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

[[!redirects cubical sets]]