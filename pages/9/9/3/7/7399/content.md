
# Children's drawings (Dessins d'enfants)
* automatic table of contents goes here
{: toc}

## Idea and prehistory

It is an old result that any (finite) [[graph]] can be embedded in an orientable [[surface]]. (The result can be found, for instance in [White 1984](#White1984), in which he give an algorithm, calling it the _Edmonds algorithm_ and giving a date of 1960, (see [Edmonds 1960](#Edmonds1960)).)

In 1879 [[Felix Klein]] (see [Klein's dessins d'enfants](#KleinsDessins)) in his paper "&#220;ber die Transformationen elfter Ordnung der elliptischen Funktionen" ("On the transformations of order eleven of elliptic functions" ) classified some [[Riemann surfaces]] of a certain [[ramification]] type by associating to [[covering space|covers]] of the surface with certain [[monodromy]] group their "dessins d'enfants" which he called "Linienz&#252;ge".

The modern perception of dessins d'enfants begins with [[Grothendieck]], who showed how to describe, [[category theory|category theoretically]], the geometric structure corresponding to such embedded graphs, namely by the [[action]] of a certain [[cartographic group]] on sets.  His motivation was the way in which this shed light on the structure of [[Riemann surfaces]], and through that to the [[absolute Galois group]] $G$ of the [[rational numbers]]. The technical vehicle explicating this relation is [[Belyi's theorem]] from which follows that $G$ has a faithful [[action]] on Grothendieck's dessins d'enfants.


> A _dessin d'enfant_ (French for a "child's drawing", plural "dessins d'enfants", ''children's drawings") is a type of [[graph]] drawing used to study [[Riemann surfaces]] and to provide combinatorial [[Invariant (mathematics)|invariants]] for the action of the [[absolute Galois group]] of the [[rational numbers]].

> "Intuitively, a dessin d'enfant is simply a [[undirected graph|graph]], with its [[vertex|vertices]] colored alternating black and white, [[graph embedding|embedded]] onto an [[Orientability|oriented surface]] that, in many cases, is simply a [[plane]]. For the coloring to exist, the graph must be [[bipartite graph|bipartite]]. The faces of the embedding must be topological disks. The surface and the embedding may be described combinatorially using a [[rotation system]], a [[cyclic order]] of the edges surrounding each vertex of the graph that describes the order in which the edges would be crossed by a path that travels clockwise on the surface in a small loop around the vertex. Any dessin can provide the surface it is embedded on with a structure as a Riemann surface. It natural to ask which Riemann surfaces arise in this way. The answer is provided by [[Belyi's theorem]], which states that these are precisely those that can be defined over the field of algebraic numbers (when considered as algebraic curves). The absolute Galois group transforms these particular curves into each other, and thereby also transforms the underlying dessins." (wikipedia)



The original development does not, however, explicitly use bipartite graphs, rather it used a form of 1-complex, embedded in a surface (see below). The use of bipartite graphs simplifies the exposition.

## Definition

A [[topological map]] is an embedding of a connected graph $G$ (loops and multiple edges allowed) into a compact oriented surface $X$, such that it fills the surface, i.e. $X \setminus G$ is a disjoint union of open cells (referred to as the _faces_ of the map). Two maps $(X_1 , G_1 )$ and $(X_2 , G_2 )$ are called _equivalent_ if there exists a homeomorphism $f : X_1 \to X_2$ 
such that $f (G_1 ) = G_2$ .

A **hypermap** is a map together with a coloring of the vertices in black and white such that any two adjacent vertices have different colors.  Observe that any map (with vertices all colored in black) gives rise to a hypermap by placing a white vertex in the middle of every edge&#8212;so, hypermaps can be seen as maps with extra information, but also conversely as a generalization of maps (see Walsh 1975, "Hypermaps Versus Bipartite Maps").

Finally, a **dessin d'enfant** is a hypermap seen as a representation of a _Belyi function_: a [[meromorphic function]] $f : X \to \bar{\mathbb{C} }$ whose only critical values are 0, 1, and $\infty$.  Such a function determines a hypermap on the Riemann surface $X$ by considering the inverse image of the unit interval $H = f^{-1}([0,1])$, and coloring the preimages of 0 and 1 as black and white vertices, respectively.  Moreover, each face of $H$ contains exactly one _pole_, that is, one preimage of $\infty$.

Note that it is also possible to associate a dessin more generally to any function $f : X \to \bar{\mathbb{C}}$ with at most three critical values, since any such function may be normalized to have critical values in $\{0,1,\infty\}$ by applying a [[linear fractional transformation]].  Likewise, the dessin can also equivalently be seen as a representation of a [[branched cover of the Riemann sphere]], ramified over at most three points.

## Examples

* Any polynomial $f : \bar{\mathbb{C}} \to \bar{\mathbb{C}}$ with no critical values other than 0 or 1 (and more generally, after normalization, any polynomial with at most two critical values) may be associated with a dessin d'enfant which is a one-face hypermap, i.e., a plane [[tree]].  (This is because any polynomial has a unique pole, at $\infty$.)  For example, the dessin d'enfant representing $f(x) = x^n$ is the "star-tree", containing one black vertex surrounded by $n$ white vertices.

* It is well known that the bipartite graph $K_{3,3}$ is non-planar, so does not embed in the 2-sphere, but will embed in the torus, in such a way that its complement is a disjoint union of discs.


##Remark

The original work  was stated in terms of objects called [[cellular maps]], and the category of these cellular maps and isotopy classes of morphisms between them was shown to correspond to a category of finite $\mathbb{G}$-sets where $\mathbb{G}$ is a group called the [[cartographic group]], which has a simple presentation in terms of operations of a geometric /  combinatorial nature.



## A translated extract 

(from the [[Esquisse d'un programme]] describing the idea as seen by Grothendieck:)


"My interest in topological surfaces began to appear in 1974, when I proposed to Yves Ladegaillerie the theme of the isotopic study of embeddings 
of a topological 1-complex into a compact surface. Over the two following 
years, this study led him to a remarkable isotopy theorem, giving a complete algebraic description of the isotopy classes of embeddings of such 
1-complexes, or compact surfaces with boundary, in a compact oriented 
surface, in terms of certain very simple combinatorial invariants, and the 
fundamental groups of the protagonists. This theorem, which should be 
easily generalisable to embeddings of any compact space (triangulable to 
simplify) in a compact oriented surface, gives as easy corollaries several 
deep classical results in the theory of surfaces, and in particular Baer's isotopy theorem. 

 In the work of Ladegaillerie there is also a purely algebraic description, in terms 
of fundamental groups, of the "isotopic" category of compact surfaces X , 
equipped with a topological 1-complex K embedded in X . This description, 
which had the misfortune to run counter to ''today's taste'' and because of 
this appears to be unpublishable, nevertheless served (and still serves) as a 
precious guide in my later reflections, particularly in the context of absolute  algebraic geometry in characteristic zero."


## Related concepts

* [[adinkra]]

## References

The Wikipedia page on this is:

* [wikipedia](http://en.wikipedia.org/wiki/Dessin_d'enfant)

Fairly elementary sources for background material include:
 
* {#White1984} Arthur T. White: 1984 _Graphs, groups and surfaces_
  

This gives the Edmonds algorithm for the embedding. the original source for that is:

* {#Edmonds1960} J. Edmonds (1960), A combinatorial representation for polyhedral surfaces, Notices Amer. Math. Soc. 7, 646.
  

References on the deeper theory as developed by Grothendieck and his students, and including summaries of subsequent work,  include:

*  [[L. Schneps]], ed., 1994, _The Grothendieck theory of dessins d'enfants_, volume 200 of London Mathematical Society Lecture Note Series , Cambridge University Press, Cambridge, papers from the Conference on Dessins d'Enfant held in Luminy, April 19&#8211;24, 1993

* Marco Robalo, _Galois Theory towards Dessins d'Enfants_ ([pdf](https://dspace.ist.utl.pt/bitstream/2295/575330/1/dissertacao.pdf))

*  F. Herrlich, G. Schmith&#252;sen: [Dessins d'enfants and Origami curves](http://www.math.kit.edu/iag3/~schmithuesen/media/dessins.pdf)

The original work on the elementary theory was contained in 

* [[Christine Voisin]], [[Jean Malgoire]], Cartes cellulaires, Cahiers Math&#233;matiques, 12, Montpellier, 1977.

* [[Christine Voisin]], [[Jean Malgoire]], Factorisation de Stein topologique, d&#233;coupe, Cahiers Math&#233;matiques, 15, Montpellier, 1979.

* [[Christine Voisin]], [[Jean Malgoire]], Cartes topologiques infinies et rev&#234;tements ramifi&#233;s de la sph&#232;re, Cahiers Math&#233;matiques, 19, Montpellier, 1980. 

Other modern textbook accounts include:

* Sergei K. Lando, Alexander K. Zvonkin, _Graphs on Surfaces and Their Applications_, Springer, 2004.

* E. Girondo, G. Gonz&#225;lez-Diez, _Introduction to compact Riemann surfaces and dessins d'enfants_, 
London Mat. Soc. Student Texts __79__, 
Cambridge Univ. Press 2012. xii+298 pp. 

References on the history of dessins d'enfants

* Lieven Le Bruyn, Klein's dessins d'enfant and the buckyball, 2008. [web](http://www.neverendingbooks.org/index.php/kleins-dessins-denfant-and-the-buckyball.html){#KleinsDessins}

Relation to [[matrix models]] and [[integrable hierarchies]]:

* [[Jan Ambjørn]], Leonid Chekhov: *The matrix model for dessins d'enfants*, Ann. Inst. Henri Poincaré Ser D **1** 3 (2014) 337-361 &lbrack;[arXiv:1404.4240](https://arxiv.org/abs/1404.4240), [doi:10.4171/aihpd/10](https://doi.org/10.4171/aihpd/10)&rbrack;

On a relation to [[super multiplet]] classification via [[adinkras]]:

* [[Charles Doran]], [[Kevin Iga]], [[Greg Landweber]], [[Stefan Méndez-Diez]], _Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras_, Adv. Theor. Math. Phys. **19** 5 (2015) 1043-1113 &lbrack;[arXiv:1311.3736](https://arxiv.org/abs/1311.3736), [doi:10.4310/ATMP.2015.v19.n5.a4](https://dx.doi.org/10.4310/ATMP.2015.v19.n5.a4), [pdf](https://www.charlesdoran.net/uploads/6/7/5/1/6751141/22_geometrization_of_n_extended_1_dimensional_supersymmetry_algebras_i_2015.pdf)&rbrack;

* [[Charles Doran]], [[Kevin Iga]], Jordan Kostiuk, [[Stefan Méndez-Diez]], *Geometrization of $\mathcal{N}$-Extended 1-Dimensional Supersymmetry Algebras II*, Adv. Theor. Math> Physics **22** 3 (2018) &lbrack;[arXiv:1610.09983](https://arxiv.org/abs/1610.09983)&rbrack;



[[!redirects child's drawing]]
[[!redirects child's drawings]]
[[!redirects children's drawing]]
[[!redirects children's drawings]]
[[!redirects dessin d'enfant]]
[[!redirects dessins d'enfant]]
[[!redirects dessin d'enfants]]
[[!redirects dessins d'enfants]]