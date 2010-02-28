# Contents
* table of contents
{: toc}

## Definition

A **quantale** is a [[closed monoidal category|closed monoidal]] [[suplattice]].  Equivalently, it is a [[monoid|monoid object]] in the closed symmetric monoidal category of suplattices. This means it is a poset having all [[join]]s and an associative, unital tensor product $\otimes$ which distributes over joins (the internal-homs then come automatically by the [[adjoint functor theorem]]).  The internal-homs in a quantale are sometimes called _residuations_ and written $x\backslash y$ and $y/x$. 

As a monoid in suplattices, a quantale is essentially the same thing as a 1-object [[quantaloid]], i.e., a 1-object category enriched in suplattices. 

## Quantales and Frames

Additional conditions often imposed on a quantale include:

* Commutativity: $x\otimes y = y\otimes x$
* Idempotence: $x\otimes x = x$
* The unit for $\otimes$ is the top element: $1=\top$.

If all three of commutativity, idempotence, and $1=\top$ are assumed, they force $\otimes$ to be the [[meet]] and therefore the quantale to be a [[frame]].  General quantales are sometimes considered to be a "noncommutative" version of a frame, whose [[opposite category]] would be a category of "noncommutative [[locale]]s."

(This is the origin of the name "quantale," a [portmanteau](http://en.wikipedia.org/wiki/Portmanteau) of "quantum" and "locale".  Note, though, that quantales seem to be generally treated in the literature more as "quantum frames" than "quantum locales," and in particular their morphisms usually go in the "frame direction."  Possibly this can be explained by the fact that in the past, it was common to use the word "locale" for what we now call a "frame" and simply distinguish between "locale homomorphisms" (now called "frame homomorphisms") and "continuous maps.")

## Enrichment over quantales

A different way of thinking about quantales views them as a [[(0,1)-category|(0,1)-categorical]] analogue of a [[cosmos]] (in the sense of Benabou).  In particular, one can then study [[enriched categories]] over a quantale. A classic example is Lawvere [[metric space]]s, seen as categories enriched in the quantale $([0, \infty], \geq)$ with $+$ taken as tensor product. 

Enrichment is often particularly interesting for $*$-quantales (see below), where one can study $*$-enriched categories. 

## Examples ##

Quantales are a surprisingly commonplace structure in computer science. A very simple example is the powerset of strings (i.e., the powerset of the free monoid over some set of characters $\Sigma$). The order is the inclusion order on sets, and meet and join are just intersection and union, respectively. Taking $\epsilon$ to be empty string, and $a \cdot b$ to the join of two string, the quantalic operations are then:

* $1 = \{\epsilon\}$
* $L \otimes M = \{ l\cdot m \;|\; l \in L, m \in M \}$ 

This example generalizes as follows: given any [[monoidal category|monoidal]] [[preorder]] $M$ (for instance, a monoid equipped with the discrete order, as in the previous example), the collection of down-closed subsets of $M$ carries a quantale structure given by [[Day convolution]] with respect to categories enriched in $\mathbf{2} = TV$, the [[Heyting algebra]] of truth values. Explicitly, if $e$ denotes the unit of $M$ and $\cdot$ the multiplication, then 

* $1 = \{x \in M: x \leq e\}$ 
* $L \otimes M = \{x \in M: \exists_{l \in L} \exists_{m \in M} x \leq l \cdot m\}$

Another class of examples: internal homs $\hom_{sLat}(X, X)$ in the closed monoidal category of suplattices. For example, when the suplattice $X$ is a power set $P(S)$, one may identify $\hom_{sLat}(P(S), P(S))$ with the poset of binary relations $P(S \times S)$, ordered by inclusion and where the quantalic multiplication is relational composition. 

Quantales, as monoids in the symmetric monoidal category $sLat$, can be tensored to produce new quantales. 


##$*$-quantale##

A $*$-quantale is a quantale $Q$ equipped with an additional structure of an involution 

$$ * : Q \to Q$$ 

for which $(x \otimes y)^* = y^* \otimes x^*$ and $1^* = 1$, where $1$ denotes the monoidal unit. (The operator is assumed to be covariant with respect to the poset structure.) 

An example of a $*$-quantale is the quantale of binary relations on a set $S$, where the $*$-operation is relational opposite: 

* $R^* = \{(y, x): (x, y) \in R\}$ 

Another example is obtained by taking the quantale of down-closed subsets of a $*$-monoidal poset $M$ (which is the same thing as a $*$-[[star-monoid|monoid]] in the [[cartesian monoidal category]] of posets), with the quantale structure given by Day convolution as described above, and the $*$-operator obtained by cocontinuously extending the $*$-operator on $M$. Explicitly, 

* $L^* = \{x^*: x \in L\}$ 

A _$*$-enriched category_ over a $*$-quantale $Q$ is a category $(X, d: X \times X \to Q)$ enriched in the underlying quantale, such that 

$$d(y, x) = d(x, y)^*$$ 

This notion can also be expressed in terms of lax morphisms of $*$-quantales; see below. 

## Morphisms of quantales ##

There is a variety of notions of morphism of quantale, just as there is a variety of notions of morphism between closed monoidal categories. All the notions considered here are morphisms between the underlying sup-lattices, in other words preserve arbitrary joins, hence are left adjoints as functors between the underlying categories. 

* At the weak end of the scale, one may consider _lax morphisms_ of quantales, i.e., (lax) [[monoidal functor]]s of quantales seen as monoidal categories. 

  * An important example of this is that [[enriched category|categories enriched]] in a monoidal poset $M$, such as Lawvere [[metric space]]s, amount to the same thing as lax quantale morphisms of the form $2^d: 2^{M} \to 2^{X \times X}$ where the domain is the quantale of upward-closed subsets of $M$ with the Day convolution structure, and the codomain is the quantale of binary relations on $X$, with multiplication being relational composition. 

* A stronger notion is of _strong morphisms_ of quantales seen as monoidal categories. As noted above, all quantale morphisms considered here are already left adjoints in $Cat$, and if the adjunction lifts to $MonCat$ (the 2-category of monoidal categories, lax monoidal functors, and monoidal transformations), then the left adjoint is strong monoidal. This often occurs in practice. 

* An even stronger notion is where the morphisms also strongly preserve the closed structure, i.e., the internal homs or residuations. (An example is to be developed for [[building]]s.) 

* There are corresponding notions of morphisms of $*$-quantales, where in each case morphisms strongly respect the $*$ operations. For instance, the notion of $*$-enriched category over a $*$-monoidal poset $M$ can be equivalently recast as a lax morphism between $*$-quantales, $2^d: 2^M \to 2^{X \times X}.$
