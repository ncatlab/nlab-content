+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of _representation_ is closely related to, or even identical, to that of [[action]]: some object $C$ that has a notion of [[composition]] is _represented_ on some object $D$ that has a notion of composition. In this generality _representation_ is just another word for [[functor]] (or potentially $\infty$-[[infinity-functor|functor]]). But in practice the term _representation_ is typically used in the context of [[representation theory]], where we attempt to study $C$ in terms of its representations in $D$, where $D$ is typically rather more familiar.

Most specifically, one studies representations of a [[group]] by linear endomorphisms of a [[vector space]]; that is, $C$ is (the [[delooping]] of) a group and $D$ is [[Vect]].  However, the typical tools in representation theory these days involve vast generalizations of the notion of a linear representation of a group; for instance, one studies [[D-module]]s on [[action groupoid]]s $G //_{Ad}G$ and things like that. This may be thought of as studying representations with values in [[schreiber:∞-vector bundle|∞-vector space]]s.


##Historical Idea (with pedagogic overtones)

###Representing Groups

The notion of a [[group]] of 'operators' was already being used in about 1832 in work by Galois, and others, but there was not a definition of an abstract group until 40 years later when Cayley wrote:

> _A group is defined by the law of composition of its members._ 

(see the article on [The abstract group concept](http://www-history.mcs.st-and.ac.uk/HistTopics/Abstract_groups.html) in the St Andrews History of Mathematics archive.) Groups as well behaved sets of functions were beginning to be well understood and used, for instance in Klein's work on geometry. Cayley proved that every finite group could be realised as a group of permutations. The theory of representations grew from that.

An abstract group could be studied by mapping it into a group of permutations or of invertible matrices, as then you could bring techniques from one area of mathematics (linear algebra) to the assistance of another, the Theory of Abstract Groups. This was exploited fully by Frobenius, Burnside, Schur and later Bauer.

That is one theme: you take an abstract algebraic thing and study it by mapping it into a similar structure which you think you know more about!

This also uses another basic idea from the start of group theory.  The earlier pioneers thought of groups as groups of 'operators', but that means they have to operate on something. To make things more explicit, let $G$ be a finite group then we know there are homomorphisms from $G$ into $S_n$. (We could take $n$ to be the order of the group and use Cayley's theorem but we do not assume that is the case.) If we look at such a homomorphism we get an [[action]] of $G$ on an $n$-element set.

Similarly if we take a homomorphism from $G$ into a group of invertible matrices $Gl_n(K)$, for $K$ a field, say, then we get a linear action of $G$ on the vector space, $K^n$.

As you would expect, we can generalise and categorify this basic idea in several useful ways.

We can think of $G$ as a groupoid, $\mathbf{B}G$, (the [[delooping]] of $G$), and then a linear representation / action will be a functor from $\mathbf{B}G$ to $Vect$, the category of vector spaces over $K$.  We could replace $G$ by a general groupoid, or a general category, but then a representation of that is the same as a diagram of that 'shape' in $Vect$. We could replace $Vect$ by another more general category, or higher category, but if we are thinking of diagrams as representations, perhaps we should not totally forget that the term 'representation' did mean a process whereby the perhaps abstract 'syntactical' objects of the category gain a 'semantic' meaning, as 'operations' of some type, and which in turn, can be usefully used to gain information on the inherent structure. 


## General definition

In a rather general form, we therefore have a __representation__ of a category $C$ in a category $D$ is simply a [[functor]] $F\colon C \to D$.  Similarly, an [[homomorphism]] between representations ("[[intertwiner]]") is simply a [[natural transformation]] between functors when they are being thought of as representations. Thus we have a [[category of representations]].

The term 'representation' is most often used when one or more of the following conditions apply:

*  $D$ is the category $k$-[[Vect]] of vector spaces over some [[field]] $k$; one then has a __$k$-linear representation__.
*  $C$ is the [[delooping]] of a [[group]]; one then has a __group representation__ in $D$.  Such a representation gives us a specific object $V$ of $D$; we say that we have a representation of $G$ on $V$.
*  $C$ is the [[free category]] on a [[quiver]]; one then has a __quiver representation__.

The classical [[representation theory]] of groups is about representations of (finite, topological, smooth etc.) groups on (topological) vector spaces, that is when the first two conditions apply. 


There are also enriched, $k$-linear and other versions, hence one can talk about representations of [[Lie algebras]], [[vertex operator algebras]], etc. See also [[representation theory]]. 

## Examples

* [[trivial representation]]

* [[linear representation]], [[permutation representation]]

* [[regular representation]], [[alternating representation]]

* [[adjoint representation]], [[coadjoint representation]]

* [[induced representation]], [[coinduced representation]]

* [[Lie algebra representation]]

* [[Galois representation]]

* [[groupoid representation]]

## Related concepts

* [[quiver variety]]

* [[action]], [[∞-action]]

* [[module]], [[∞-module]]

* **representation**, [[∞-representation]]

  * [[faithful representation]]
  
  * [[virtual representation]]

  * [[2-representation]]

  * [[star-representation]]

    * [[representation of a C-star-algebra]]

  * [[representation sphere]]

* [[character]]

* [[singleton representation]]

* [[equivariant homotopy theory]], [[global equivariant homotopy theory]]

* [[equivariant stable homotopy theory]], [[global equivariant stable homotopy theory]]


[[!include homotopy type representation theory -- table]]


## References

See the references at _[[representation theory]]_.

[[!redirects representation]]
[[!redirects representations]]


[[!redirects group representation]]
[[!redirects group representations]]
[[!redirects representation of a group]]
[[!redirects representations of a group]]
[[!redirects representations of groups]]

[[!redirects quiver representation]]
[[!redirects quiver representations]]
[[!redirects representation of a quiver]]
[[!redirects representations of a quiver]]
[[!redirects representations of quivers]]
