#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

Given a [[category]] $C$ whose objects are thought of as _test spaces_ a very general useful notion of 

* [[space]] modeled on the objects of $C$ is a [[presheaf]] on $C$, i.e. a [[functor]] $X : C^{op} \to $ [[Set]].

* [[quantity]] modeled on $C$ is a [[presheaf|copresheaf]] on $C$, i.e. a functor $A : C \to Set$.

There are various specializations of interest on this

* [[higher category theory|higher categorical]] version

  * [[∞-space]] modeled on $C$ is a [[simplicial presheaf]] on $C$, i.e. a functor $X : C^{op} \to $ [[SSet]].

  * [[∞-quantity]] modeled on $C$ is a cosimplicial copresheaf on $C$, i.e. a functor $X : C \to CoSSet$ .

* infinitesimal version

  * [[infinitesimal space]]

  * [[infinitesimal quantity]]

For some discussion of why this is a useful general notion see [[motivation for sheaves, cohomology and higher stacks]].

With the advent of [[Higher Topos Theory]] abstract concepts of _space and quantity_ have been realized fully in the context of [[(∞,1)-topos]]es in terms of [[structured (∞,1)-topos]]es and [[generalized scheme]]s. For a summary see the tables at [notions of space](http://ncatlab.org/nlab/show/A+Survey+of+Elliptic+Cohomology+-+the+derived+moduli+stack+of+derived+elliptic+curves#NotionsOfSpace).

## Details

As indicated in

* F. W. Lawvere, _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

from [page 17](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf#page=17) on, the general situation involving

* (generalized) spaces;

* (generalized) quantities (e.g. function algebras);

* the [[duality]] between the two;

which underlies much of mathematics is at its heart controled by the following elementary category theoretic reasoning:

Let $S$ be some category whose objects we want to think of as certain simple spaces on which we want to model more general kinds of spaces. For instance $S = \Delta$, the simplicial category, or $S = $ [[CartSp]]. 

An ordinary [[manifold]], for instance, is a space required to be _locally isomorphic_ to an object in $S = CartSp$. But more generally, a space $X$ modeled on $S$ need only be _probeable_ by objects of $S$, giving a rule which to each test object $U \in S$ assigns the collection of admissible maps from $U$ to $X$,  such that this assignment is well-behaved with respect to morphisms in $S$. Such an assignment is nothing but a [[presheaf]] on $S$, i.e. a contravariant functor
$$
  X : S^{op} \to Set
  \,.
$$
Therefore general spaces modeled on $S$ are nothing but presheaves on $S$:
$$
  Spaces_S := PSh(S)
  \,.
$$
Of course this is an extremely general notion of spaces modeled on $S$. 

We have the [[Yoneda lemma|Yoneda embedding]]  $S \hookrightarrow Spaces_S$ and using this we can say that the collection of _functions_ on a generalized space $X$ with values in $U \in S$ is 
$$
  C(X,U) := Hom_{Spaces_S}(X,U)
  \,.
$$
This assignment is manifestly covariant in $U$, and hence more generally we can consider the functions on $X$, $C(X)$ to be a copresheaf on $S$, namely a covariant functor
$$
  C(X) := Hom(X,-) : S \to Sets
  \,.
$$
One can think of $C(X)$ as being a generalized quantity which may be _co-probed_ by objects of $S$.

In this vein, one can say, generally, that co-presheaves on $S$ are generalized quantities modeled on $S$, and we write
$$
  Quantities_S := CoPrSh(S)
  \,.
$$

Given any such generalized quantity $A \in Quantities_S$, we can ask which generalized space it behaves like the algebra of functions on. This generalized space should be called $Spec(A)$ and can be defined as a presheaf by the assignment
$$
  Spec(A) 
  :
  U \mapsto Hom_{Quantities_S}(A, C(U))
  \,.
$$

In  total this yields an adjoint pair of functors between generalized spaces and generalized quantities:

$$
  Spaces_S
\stackrel{\stackrel{C(-)}{\to}}{\stackrel{Spec(-)}{\leftarrow}}
  Quantities_S
  \,.
$$

(That this is an adjunction can be understood as a special case of [[Stone duality]] induced by a [[dualizing object]].)

Lawvere addresses this adjoint pair as **Isbell conjugation**.

In conclusion, the grand [[duality]] between spaces and quantities is a consequence of the [[duality|formal duality]] which reverses the arrows in the category $S$ of test spaces.

This story generalizes straightforwardly from [[presheaf|presheaves]] with values in [[Set]] to presheaves with values in other categories. Of relevance are in particular presheaves with values in the category [[Top] of [[topological space]]s and presheaves with values in the category of [[spectrum|spectra]]. See the examples below. 

## Examples

### Examples for generalized spaces


*  A [[sheaf]] is a generalized space in the above sense which satisfies a certain extra natural condition which encodes that it is _locally well behaved_. The [[sheaf]] condition on a [[presheaf]] says that the generalized space whose probes form a [[presheaf]] is such that the probes by a big test object $U$ can be reconstructed from those probes by smaller test objects $\{V_i\}$ [[coverage|covering]] $U$ which are given by restricting the probe by $U$ to all of the $V_i$. So generalized spaces which are given not just by presheaves but by sheaves satisfy a very natural locality conditions: they can be _built up from smaller pieces_. 

* Arbitrary generalized spaces given by sheaves can still be much more general than an "ordinary space". A **concrete sheaf** is (the collection of probes of) a generalized space which at least shares with an ordinary space the property that it has an _underlying set of points_. Important examples of generalized spaces given by concrete sheaves are the Chen-smooth or diffeological spaces discussed at [[generalized smooth space]]. 

* There is a natural generalization of the above examples for generalized spaces whose presheaves of probes take values not in [[Set]] but in [[Top]] (equivalently in [[SSet]]): when these satisfy the respective locality condition they are called [[infinity-stack]]s or [[(infinity,1)-sheaf|(infinity,1)-sheaves]]. For instance, [[Lie groupoid]]s also known as [[differentiable stack]]s  and more generally [[Lie infinity-groupoid]]s are examples of this.


* A pedagogical discussion of generalized spaces (from this perspective) is at

  * [[motivation for sheaves, cohomology and higher stacks]]

* The idea of a _space equipped with a structure sheaf_ generalizes in the above sense to a mix of a copresheaf and a presheaf, see [[structured generalized space]].

### Examples for generalised quantities

It would be nice if we had some of these, although [[structured generalized space]] above is sort of a mixture.

#References#

The _duality of space and quantity_ in the above sense is described in

* F. W. Lawvere, [Taking categories seriously](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf)

A related blog discussion is here:

*  _Space and Quantity_ ([blog](http://golem.ph.utexas.edu/category/2008/03/space_and_quantity.html))

