#Contents#

* automatic table of contents goes here
{:toc}

#Definition#

A **cubical set** is a [[presheaf]] on the [[cube category]] $\Box$. 

#Idea#

The definition is to be understood from the point of view of [[space and quantity]]: a _cubical set_ is a [[space]] characterized by the fact that and how it may be _probed_ by mapping standard cellular [[cubes]] into it: the set $S_n$ assigned by a cubical set to the standard $n$-[[cube]] $[n]$ is the set of $n$-[[cubes]] in this space, hence the way of mapping a standard $n$-[[cube]] into this spaces.

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

+-- {: .query}
[[David Corfield]]: Is this cubical set the same as Pratt is talking about on p. 13 [here](http://boole.stanford.edu/pub/es.pdf)?

"...the duality of bipointed sets, sets with two distinguished elements, and Boolean algebras without top or bottom. Contemplation of this duality, which Bill Lawvere suggested to me in a phone conversation as a simple construction of the theory of cubical sets". 

If so, given that the real interval is a final coalgebra on bipointed sets, is there some dual to it in cubical sets?

Also shouldn't we have something on this page about Grandis's use of cubical sets in [directed algebraic topology](http://www.dima.unige.it/~grandis/DAT.Intro.pdf), e.g., p. 3 ? 

[[Todd Trimble]]: The passage from Pratt's paper is a bit brief, but my impression is that they are discussing the Lawvere algebraic theory of two constants, which is a cartesian prop, and which contains more figures than the pro given by the monoidal category of [[cube]]s. In particular, there are diagonal maps in the cartesian prop which aren't present in the category of cubes in the sense here (and which aren't reflected as far as I can tell by cubical sets with connection). Perhaps we need some disambiguation then? 

And please correct me if I'm wrong, but I believe the interval as final coalgebra is a coalgebra for the join-square endofunctor $x \mapsto x \vee x$ acting on the category of bipointed sets (where the two points are distinct). The condition that the two points are distinct is non-algebraic, so I can't see a clear connection which would point to something dual in cubical sets in Pratt's sense. But maybe there's more going on than meets my eyes. 

[[David Corfield]]: Thanks Todd. I think you're right about Pratt's work, see example 5 [here](http://cs.nyu.edu/pipermail/fom/1998-March/001627.html). If his usage is at all prevalent, we should disambiguate. So, next question, which are Grandis's cubical sets? He seems to be able to do some remarkable things with them, e.g., the link to noncommutative spaces in section 3 of [this](http://www.dima.unige.it/~grandis/DAT.Intro.pdf). 

[[Todd Trimble]]: I believe Grandis is talking about cubes as we are here. [His paper](http://www.emis.de/journals/TAC/volumes/11/8/11-08.pdf) with Luca Mauri gives a rather thorough introduction to various categories of cubes (including, e.g., cubes with connections). The cartesian version doesn't appear in that paper; I am guessing that most (all?) people who consider the category of cubes as Pratt does are in very close contact with Lawvere. The only items I found through google on this are one's with Pratt's name attached. But just to be on the safe side, I'll write a brief note of disambiguation. 
=--

# Cubical sets in homotopy theory #

[[Daniel Kan]]'s early work on [[homotopy theory]] used cubical sets instead of [[simplicial set]]s. But then a bit later it was found that plain cubical sets suffer from three disadvantages when it comes to modelling [[homotopy type|homotopy n-type]]s:

1. normalization of chains is essential

1. [[cubical group]]s are not automatically fibrant

1. the [[geometric realization]] of a cubical set (see [geometric realization](#geometric realization) below) tends to have the wront [[homotopy n-type|homotopy type]]:

   for instance the geometric realization of the cubical set $I \times I$ has non-trivial [[homotopy group]]s and hence does not model the [[topological space]] given by the standard square, which is contractible

It was then realized that none of these problems is shared by [[simplicicial set]]:

1. (to be filled in)

1. every [[simplicial group]] is necessarily a [[Kan complex]] and therefore fibrant in the standard [[model structure on simplicial sets]]

1. [[geometric realization]] of [[simplicial set]]s is well behaved and in fact constitutes a [[cartesian monoidal category|cartesian monoidal]] [[Quillen equivalence]] 

   $$
      |-| : SSet \stackrel{\leftarrow}{\to} Top : S(-)
   $$

   between [[SSet]] and [[Top]]. For more on this see [[homotopy hypothesis]].

These observations led to a widespread use of simplicial methods, while cubical methods coexisted only with a kind of underground existence, to this date, being studied and developed notably by [[Ronnie Brown]] and his collaborators in their work on [[nonabelian algebraic topology]].

But in fact it turns out that the second and third of the above disadvantages of [[cubical set]]s over [[simplicial set]]s in [[homotopy theory]] can be dealt with.

1. The first problem can't be avoided. See

   Rosa, Antolini and Bert Wiest, _The singular cubical set of a topological space_ , Mathematical Proceedings of the Cambridge Philosophical Society, 126 (1),  (1999)

1. The second problem is resolved by using [[connection on a cubical set|cubical sets with connection]]. See

   A. P. Tonks, _Cubical sets which are Kan_, J. Pure Appl. Algebra, 81 (1),  (1992) 

1. Maltsiniotis in his work resolves the problem of the geometric realization developing the discussion in section 8.4 of

   Denis-Charles Cisinski, _Les pr&#233;faisceaux comme mode&#232;le des types d'homotopie_, Ast&#233;risque, 308 (2006) 


## Geometric realization ##

If $X$ is a cubical set, the [[geometric realization]] $|X|$ may be defined as the [[weighted colimit]] (a [[coend]]) in [[Top]] 

$$X \otimes_{\Box} I^{\bullet} = \int^{n \in \Box} X(n) \cdot I^n$$ 

where $I^{\bullet}: (\Box, \otimes, I) \to (\Top, \times, 1)$ is the unique (up to isomorphism) monoidal functor mapping the generating object $int$ to $[0, 1]$, and for $k = 0, 1$, mapping $i_k$ to the inclusion $\{k\} \hookrightarrow [0, 1]$. This is parallel to one way of defining the [[geometric realization]] of a [[simplicial set]]. 
Geometric realization is a functor [[adjoint functor|left adjoint]] to the functor 
$$cub: Top \to Set^{\Box^{op}}$$ 
which takes a space $S$ to the functor $\hom_{Top}(I^{\bullet}-, S)$. 


# Background# 

The notion of cubical set and of homology theory and homotopy theory based on singular cubes goes way back in the literature. Serre's work on spectral sequences and fibre spaces was based on cubes. Kan's early work on combinatorial homotopy was based on cubes. However the category of cubical sets was found to have a major disadvantage compared with simplicial sets, in that the cartesian product in this category failed to have the correct homotopy type. 

Nonetheless cubical sets continued to have a kind of underground existence. 

Brown and Higgins introduced the extra structure of [[connection on a cubical set|connections]] $\Gamma^\pm_i$ on cubical sets, and included this structure into their cubical  [[∞-groupoids]]. All this structure was essential for the equivalence with [[crossed complexes]] and for the applications to homotopy theory. For example these omega-groupoids have a canonical structure of [[thin elements]], defined as any composition of elements of the form $\pm \epsilon_j x, \pm \Gamma^\pm_i$. Such elements have "commuting boundary". 

The geometric realisation of cubical sets with connections, and the relation with cartesian products, has not yet been analysed. 

Nonetheless, the advantages of cubes are:

1. Easy notions of multiple compositions (compared with the globular pasting schemes); 

1. Good notions of tensor product, because of the rule $I^m \times I^n \cong I^{m+n}$, and hence easy conceptual handling of homotopies.  

For the first of these, we refer to [[compositions in cubical sets]]. 

#References#

* Grandis, M. and Mauri, L. Cubical sets and their site, _Theory Applic. Categories_ {11} (2003) 185--201.

This discusses variations on the cubical set theme and normal forms in several cases. 


* Brown, R. and Higgins, P. J., Tensor products and homotopies for $\omega$-groupoids and crossed complexes.
 _J. Pure Appl. Algebra_ 47 (1987) 1--33.

* Massey, W. S.,   _Singular homology theory_, _Graduate Texts in
  Mathematics_, Volume~70. Springer-Verlag, New York (1980).


Section 2 of

* Sjoerd Crans, _Pasting schemes for the monoidal biclosed structure on $\omega$-$\mathbf{Cat}$_ ([web](http://crans.fol.nl/papers/thten.html), [ps](http://crans.fol.nl/papers/thten.ps.gz), [[thten.pdf|pdf:file]])

gives a general discussion of the cube category and of cubical sets. 
The **cubical identities** satisfied by a cubical set are given in proposition 2.8 on p. 9.

Cubical sets are what Brown and Higgins based their long series of articles on [[strict ∞-groupoids]] on. For instance

* [[Ronnie Brown|Brown]], Higgins, _The equivalence of $\omega$-groupoids and cubical $T$-complexes_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 22 no. 4 (1981), p. 349-370  ([pdf](http://archive.numdam.org/ARCHIVE/CTGDC/CTGDC_1981__22_4/CTGDC_1981__22_4_349_0/CTGDC_1981__22_4_349_0.pdf)).

and generally

* [[Ronnie Brown]], Philip J. Higgins and Rafael Sivera, _Nonabelian algebraic topology_ ([web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html)).

[[!redirects cubical sets]]