As indicated in

* F. W. Lawvere, _Taking categories seriously_, Reprints in Theory and Applications of Categories, No. 8, 2005, pp. 1&#8211;24. ([pdf](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf))

from [page 17](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf#page=17) on, the general situation involving

* (generalized) spaces;

* (generalized) quantities (e.g. function algebras);

* the [[duality]] between the two;

which underlies much of mathematics is at its heart controled by the following elementary category theoretic reasoning:

Let $S$ be some category whose objects we want to think of as certain simple spaces on which we want to model more general kinds of spaces. For instance $S = \Delta$, the simplicial category, or $S = $ [[CartSp]]. 

An ordinary manifold, for instance, is a space required to be _locally isomorphic_ to an object in $S = CartSp$. But more generally, a space $X$ modeled on $S$ need only be _probeable_ by objects of $S$, giving a rule which to each test object $U \in S$ assigns the collection of admissible maps from $U$ to $X$,  such that this assignment is well-behaved with respect to morphisms in $S$. Such an assignment is nothing but a [[presheaf]] on $S$, i.e. a contravariant functor
$$
  X : S^{op} \to Sets
  \,.
$$
Therefore general spaces modeled on $S$ are nothing but presheaves on $S$:
$$
  Spaces_S := PrSh(S)
  \,.
$$
Of course this is an extremely general notion of spaces modeled on $S$. 

We have the [[Yoneda lemma|Yoneda embedding]]  $S \hookrightarrow Spaces_S$ and using this we can say that the collection of _functions_ on a generalized space $C$ with values in $U \in S$ is 
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
\stackrel{\stackrel{C(-)}{\leftarrow}}{\stackrel{Spec(-)}{\to}}
  Quantities_A
  \,.
$$

(That this is an adjunction can be understood as a special case of [[Stone duality]] induced by a [[dualizing object]].)

Lawvere addresses this adjoint pair as **Isbell conjugation**.

In conclusion, the grand duality between spaces and quantities is a consequence of the [[duality|formal duality]] which reverses the arrows in the category $S$ of test spaces.

##References##

* F. W. Lawvere, [Taking categories seriously](http://www.emis.de/journals/TAC/reprints/articles/8/tr8.pdf)
*  _Space and Quantity_ ([blog](http://golem.ph.utexas.edu/category/2008/03/space_and_quantity.html))