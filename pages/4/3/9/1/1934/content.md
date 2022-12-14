
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Big and little toposes
* automatic table of contents goes here
{:toc}

## Idea

There are two different (related) relationships between [[Grothendieck topoi]] and a notion of _generalized [[space]]_.  (Recall that a Grothendieck topos $T$ is a [[category of sheaves]] $T = Sh(S)$ on some [[site]] $S$.)

On the one hand, we can regard the topos *itself* as a generalized space.  This tends to be a useful point of view when the site $S$ is the [[category of open subsets]] $Op(X)$ of a [[topological space]] $X$ (or some [[manifold]] or the like), or some other site which we regard as containing data from only "one space."  In this case, we refer to $T$ as a **little topos**, or (if we fail to translate the original French) a **petit topos**.

On the other hand, we can view a topos $T$ as a well-behaved category whose *objects* are generalized spaces.  This tends to be a useful point of view when the site $S$ is a category of _all test [[space]]s_ in some sense, such as [[Top]], [[Diff]], or [[CartSp]].  In this case, we refer to $T$ as a **big topos**, or (in French) a **gros topos**.

These distinctions carry over in a straightforward way to higher topoi such as [[(∞,1)-topoi]].


## Relationships

Objects in a big topos $Sh(S)$ may be thought of as [[space]]s _modeled on $S$_, in the sense described at [[motivation for sheaves, cohomology and higher stacks]] and at [[space]].

On the other hand, the objects of a petit topos, such as $Sh(X)$, can also be regarded as a kind of generalized spaces, but generalized spaces _over $X$_ on which the rigid structure of morphisms in $Op(X)$ (only inclusions of subsets, no more general maps) induces a correspondingly rigid structure so that they are not all that general.  In fact, $Sh(Op(X))$ is equivalent to the category of [[etale space]]s over $X$---i.e. spaces "modeled on $X$" in a certain sense.  More generally, for any topos $E$, the objects of $E$ can be identified with [[local homeomorphisms of toposes]] into $E$.

From the "little topos" perspective, it can be helpful to think of a "big topos" as a "fat point," which is not "spread out" very much spatially itself, but contains within that point lots of different types of "local data," so that even spaces which are "rigidly" modeled on that point can have a lot of interesting cohesion and local structure.  (One should not be misled by this into thinking that a big topos has *only* one [[point of a topos|point]], although it is usually a [[local topos]] and hence has an [[initial object|initial]] point.)


## The big and little topos of an object

If $X$ is a topological space, then the canonical little topos associated to $X$ is the sheaf topos $Sh(X)$.  On the other hand, if $S$ is a site of probes enabling us to regard $X$ as an object of a big topos $H = Sh(S)$, then we can also consider the topos $H/X$ as a representative of $X$.  These two toposes are often called the **little topos of $X$** (or **petit topos of $X$**) and the **big topos of $X$** (or **gros topos of $X$**) respectively.

There might be some debate about whether $H/X$ is, itself, "a little topos" or "a big topos."  While it certainly contains information about the space $X$ specifically, its objects are not "spaces locally modeled on $X$" but rather spaces locally modeled on the big site $S$ which happen to have a map to $X$.  The standard phrase "the big topos of $X$" is the most descriptive.

Note that if $X$ is actually an *object* of the site $S$, then $H/X$ can be identified with the topos of sheaves on the [[slice category|slice]] site $S/X$ (and otherwise, it can be identified with the topos of sheaves on the [[category of elements]] of $X\in Sh(S)$).  This site $S/X$ is often referred to as the [[big site]] of $X$, as compared to the [[little site]], which is $Op(X)$ (or appropriate replacement).  The topos $Sh(S/X)$ can thus be viewed as spaces modelled on $S$, but parameterised by the representable sheaf $X$.

Note that when $S=Top$ with its local-homeomorphism topology, there is a canonical functor $Op(X) \to S/X$ which preserves finite limits and both [[cover-preserving functor|preserves]] and [[cover-reflecting functor|reflects]] covering families.  Therefore, it induces both a geometric morphism $H/X \to Sh(X)$ and one $Sh(X) \to H/X$, of which the latter is the left adjoint of the former in [[Topos]].  In other words, the geometric morphism $H/X \to Sh(X)$ is [[local geometric morphism|local]], and in particular a [[homotopy equivalence of toposes]].  This fact relating the big and little toposes of $X$ also holds in other cases.


## Axiomatizations

* If a site $S$ is given by a [[Grothendieck pretopology]], then one can define an associated notion of a [[little site]] associated to any object of $S$, and hence both a little topos and a big topos, which are related as above.

* One proposed axiomatization of the notion of big topos is that of a [[cohesive topos]].

* In his early papers in the 80s, [[Lawvere]] emphasized the existence of a contractible [[subobject classifier]], a concept which together with the [[adjoint quadruple]] goes under the name [[sufficiently cohesive topos]] in the later axiomatization (modulo some fineprint).

## Examples

For $X$ a [[topological space]], the _little topos_ that it defines is the [[category of sheaves]] $Sh(X) := Sh(Op(X))$ on the [[category of open subsets]] of $X$. A general object in this topos can be regarded as an [[etale space]] over $X$. The space $X$ itself is incarnated as the [[terminal object]] $X = * \in Sh(X)$.

On the other hand, a _big topos_ in which $X$ is incarnated is a [[category of sheaves]] on a [[site]] of test spaces with which $X$ may be probed. For instance for $C =$ [[Top]], or [[Diff]] or [[CartSp]] with their standard [[coverage]]s, $Sh(C)$ is such a big topos. See for instance, [[topological topos]] and the [[quasi-topos]] of [[quasitopological space]]s.

In good cases, the intrinsic properties of $X$ do not depend on whether one regards it as a little topos or as an object of a gros topos. For instance at [[cohomology]] in the section <a href="http://ncatlab.org/nlab/show/cohomology#NonabelianSheafCohomology">Nonabelian sheaf cohomology with constant coefficients</a> it is discussed how the [[nonabelian cohomology]] of a [[paracompact space|paracompact]] [[manifold]] $X$ with constant coefficients gives the same answer in each case.

## Related entries

* [[functorial geometry]], [[space and quantity]]

* [[topological site]], [[continuous truth]]

* [[cohesive topos]]

  * [[sufficiently cohesive topos]]

  * [[infinitesimal cohesive (infinity,1)-topos]]

  * [[quality type]]

* [[étendue]]

* [[locally decidable topos]]


## References

The notion of a _gros topos_ of a _topological space_ is due to [[Jean Giraud]]. Some early results from the Grothendieck school appear in 

* {#SGA4}[[M. Artin]], [[A. Grothendieck]], [[J. L. Verdier]], _Th&#233;orie des Topos et Cohomologie Etale des Sch&#233;mas ([[SGA4]])_, Springer LNM **269** (1972). (expos&#233; IV, 2.5 pp.316-318, 4.10 pp.358-365)

In this context see also

* [[Saunders Mac Lane|S. Mac Lane]], [[Ieke Moerdijk|I. Moerdijk]], pp. 113, 325, 416 in: *[[Sheaves in Geometry and Logic]]*, Springer (1994) &lbrack;[doi:10.1007/978-1-4612-0927-0](https://link.springer.com/book/10.1007/978-1-4612-0927-0) &rbrack;

In the context of a discussion of the [[big Zariski topos]] [Lawvere (1976, p. 110)](#Lawvere76) calls the gros-petit distinction '_a surprising twist of logic that is not yet fully clarified_':

* {#Lawvere76} [[William Lawvere]], *Variable quantities and variable structures in topoi*, in [[Alex Heller]], [[Myles Tierney]] (eds.), *Algebra, Topology and Category Theory -- A Collection of Papers in Honor of [[Samuel Eilenberg]]*, Academic Press New York (1976) 101-131 &lbrack;[doi:10.1016/C2013-0-10841-0](https://doi.org/10.1016/C2013-0-10841-0)&rbrack;

The suggestion that a _general notion_ of gros topos is needed goes back to some remarks in _[[Pursuing Stacks]]_. A precise axiom system capturing the notion is first proposed in 

* {#Lawvere86} [[William Lawvere]], *Categories of spaces may not be generalized spaces, as exemplified by directed graphs*, Revista Colombiana de Matematicas **XX** (1986) 179-186, reprinted as: Reprints in Theory and Applications of Categories, **9** (2005) 1-7 &lbrack;[tac:tr9](http://www.tac.mta.ca/tac/reprints/articles/9/tr9abs.html)&rbrack;

"Axiom 0" ([[local topos|locality]]) used in [Lawvere 1986](#Lawvere86) for gros toposes  is argued in [Lawvere 1994](#Lawvere94) to be essentially an insight due to [[Georg Cantor]] and is called the *Cantorian Contrast* (namely between [[discrete spaces]] and [[codiscrete spaces]]) in [Lawvere & Rosebrugh (2003)](#LawvereRosebrugh03), [p. 245](http://patryshev.com/books/Sets%20for%20Mathematics.pdf#page=260).

* {#LawvereRosebrugh03} [[William Lawvere]], [[Robert Rosebrugh]], [p. 245](http://patryshev.com/books/Sets%20for%20Mathematics.pdf#page=260) in: *[[Sets for Mathematics]]*, Cambridge University Press  (2003) &lbrack;[doi:10.1017/CBO9780511755460](https://doi.org/10.1017/CBO9780511755460), [book homepage](http://www.mta.ca/~rrosebru/setsformath/), [pdf](http://patryshev.com/books/Sets%20for%20Mathematics.pdf)&rbrack;

The axioms 0 and 1 for _toposes of generalized spaces_ given in [Lawvere 1986](#Lawvere86) later became called the axioms for a *[[cohesive topos]]*

* {#Lawvere94} [[William Lawvere]], *[[Cohesive Toposes and Cantor's "lauter Einsen"]]*, Philosophia Mathematica **2** 1 (1994) 5-15 &lbrack;[doi:10.1093/philmat/2.1.5](https://doi.org/10.1093/philmat/2.1.5), [[LawvereCohesiveToposes.pdf:file]]&rbrack;

together with axiom 2 they make out a [[sufficiently cohesive topos]].



Further discussion of this axiomatics for gros toposes is in

* [[Bill Lawvere]], _Categories of space and quantity_ in: J. Echeverria et al (eds.), _The Space of mathematics_, de Gruyter, Berlin, New York (1992) &lbrack;[pdf](https://raw.githubusercontent.com/mattearnshaw/lawvere/master/pdfs/1992-categories-of-space-and-quantity.pdf)&rbrack;

where a proposal for a general axiomatization of [[homotopy]]/[[homology]]-like "extensive quantities" and [[cohomology]]-like "intensive quantities") as covariant and contravariant functors out of a distributive category are considered.

The following two papers contain Lawvere's early view of a trichotomy between big toposes vs. étendue and locally decidable toposes as paradigmatic "generalized spaces" with "infinitesimally cohesive" in between, with the latter subsumed into the fine structure of cohesion in more recent versions

* {#Law89a} [[F. W. Lawvere]], *Qualitative Distinctions between some Toposes of Generalized Graphs*, in *Categories in Computer Science and Logic*, Cont. Math. **92** (1989) 261-299 &lbrack;[doi:10.1090/conm/092](http://dx.doi.org/10.1090/conm/092), [pdf](https://github.com/mattearnshaw/lawvere/raw/master/pdfs/1989-qualitative-distinctions-between-some-toposes-of-generalized-graphs.pdf)&rbrack;

* {#Law91a} [[F. W. Lawvere]], *[[Some Thoughts on the Future of Category Theory]]*, 1-13 in Springer LNM **1488** (1991).

The [[left adjoint]]  in a cohesive topos is also mentioned in

* [[Bill Lawvere]], [page 14](http://www.tac.mta.ca/tac/reprints/articles/8/tr8.pdf#page=14) of: _Taking categories seriously_, Revista Colombiana de Matematicas **XX** (1986) 147-178, Reprints in Theory and Applications of Categories, **8** (2005) 1-24. &lbrack;[tac:tr8](http://www.tac.mta.ca/tac/reprints/articles/8/tr8abs.html), [pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf)&rbrack;


Under the term _categories of cohesion_ these axioms are discussed in

* [[Bill Lawvere]], _Axiomatic cohesion_, Theory and Applications of Categories **19** 3 (2007) 41-49 &lbrack;[tac:19-03](http://www.tac.mta.ca/tac/volumes/19/3/19-03abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/19/3/19-03.pdf)&rbrack;



Another definition of gros vs petit toposes and remarks on applications in [[Galois theory]] is in

* Nick Duncan, _Gros and petit toposes_ ([pdf](http://www.cheng.staff.shef.ac.uk/pssl88/pssl88-duncan.pdf))

and yet another one is in 

* [[Jacob Lurie]], _[[Spectral Algebraic Geometry]]_, chapter 20 "Fractured $\infty$-Topoi" ([pdf](http://www.math.harvard.edu/~lurie/papers/SAG-rootfile.pdf))

There is also something relevant in this article:

* [[Mathieu Anel]], _Grothendieck topologies from unique factorization systems_ ([arXiv:0902.1130](http://arxiv.org/abs/0902.1130))

* [[Mamuka Jibladze]], _Homotopy types for "gros" toposes_, thesis, [pdf](http://www.rmi.ge/~jib/pubs/thesis.pdf)

* [[Peter Johnstone]], _Calibrated Toposes_, Bull. Belgian Math. Soc. - Simon Stevin **19** 5 (2012) 889-907. &lbrack;[euclid:1354031555](http://projecteuclid.org/euclid.bbms/1354031555)&rbrack;

A discussion and comparison of big vs little approaches to $(\infty,1)$-topos theory began at these blog entries:

* [Cohesive (∞,1)-toposes](http://golem.ph.utexas.edu/category/2010/10/cohesive_toposes.html) and [Petit (∞,1)-toposes](http://golem.ph.utexas.edu/category/2010/10/petit_1toposes.html).


[[!redirects big topos]]
[[!redirects big toposes]]
[[!redirects big topoi]]
[[!redirects gros topos]]
[[!redirects gros toposes]]
[[!redirects gros topoi]]

[[!redirects little topos]]
[[!redirects little toposes]]
[[!redirects little topoi]]
[[!redirects petit topos]]
[[!redirects petit toposes]]
[[!redirects petit topoi]]

[[!redirects big or little topos]]
[[!redirects big or little toposes]]
[[!redirects big or little topoi]]
[[!redirects big and little topos]]
[[!redirects big and little toposes]]
[[!redirects big and little topoi]]
[[!redirects little or big topos]]
[[!redirects little or big toposes]]
[[!redirects little or big topoi]]
[[!redirects little and big topos]]
[[!redirects little and big toposes]]
[[!redirects little and big topoi]]
[[!redirects gros or petit topos]]
[[!redirects gros or petit toposes]]
[[!redirects gros or petit topoi]]
[[!redirects gros and petit topos]]
[[!redirects gros and petit toposes]]
[[!redirects gros and petit topoi]]
[[!redirects petit or gros topos]]
[[!redirects petit or gros toposes]]
[[!redirects petit or gros topoi]]
[[!redirects petit and gros topos]]
[[!redirects petit and gros toposes]]
[[!redirects petit and gros topoi]]

[[!redirects petit (∞,1)-topos]]
[[!redirects petit (infinity,1)-topos]]
[[!redirects petit (∞,1)-toposes]]
[[!redirects petit (infinity,1)-toposes]]

[[!redirects gros (∞,1)-topos]]
[[!redirects gros (infinity,1)-topos]]
[[!redirects gros (∞,1)-toposes]]
[[!redirects gros (infinity,1)-toposes]]