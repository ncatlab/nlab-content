A **quantale** is a [[closed monoidal category|closed monoidal]] [[suplattice]].  Equivalently, it is a [[monoid|monoid object]] in the closed symmetric monoidal category of suplattices. This means it is a poset having all [[join]]s and an associative, unital tensor product $\otimes$ which distributes over joins (the internal-homs then come automatically by the [[adjoint functor theorem]]).  The internal-homs in a quantale are sometimes called _residuations_ and written $x\backslash y$ and $y/x$.

Additional conditions often imposed on a quantale include:

* Commutativity: $x\otimes y = y\otimes x$
* Idempotence: $x\otimes x = x$
* The unit for $\otimes$ is the top element: $1=\top$.

If all three of commutativity, idempotence, and $1=\top$ are assumed, they force $\otimes$ to be the [[meet]] and therefore the quantale to be a [[frame]].  General quantales are sometimes considered to be a "noncommutative" version of a frame, whose [[opposite category]] would be a category of "noncommutative [[locale]]s" (hence the name, a [portmanteau](
http://en.wikipedia.org/wiki/Portmanteau) of "quantum" and "locale").

+--{: .query}
Now, if you really thought of quantales as quantum locales, then you would define a morphism of quantales to go backwards.  What does the literature say about that?  ---Toby

[[Mike Shulman|Mike]]: I think that whatever the origins of the name, quantales are generally treated in the literature as more like "quantum frames" than "quantum locales."  Note, though, that in the past, it was common to use the word "locale" for what we now call a "frame" and simply distinguish between "locale homomorphisms" and "continuous maps."

_Toby_:  That explains it then, thanks.
=--

### Examples ###

Quantales are a surprisingly commonplace structure in computer science. A very simple example is the powerset of strings (i.e., the powerset of the free monoid over some set of characters $\Sigma$). The order is the inclusion order on sets, and meet and join are just intersection and union, respectively. Taking $\epsilon$ to be empty string, and $a \cdot b$ to the join of two string, the quantalic operations are then:

* $1 = \{\epsilon\}$
* $L \otimes M = \{ l\cdot m \;|\; l \in L, m \in M \}$ 

This example generalizes as follows: given any [[monoidal category|monoidal]] [[preorder]] $M$ (for instance, a monoid equipped with the discrete order, as in the previous example), the collection of down-closed subsets of $M$ carries a quantale structure given by [[Day convolution]] with respect to categories enriched in $\mathbf{2} = TV$, the [[Heyting algebra]] of truth values. Explicitly, if $e$ denotes the unit of $M$ and $\cdot$ the multiplication, then 

* $1 = \{x \in M: x \leq e\}$ 
* $L \otimes M = \{x \in M: \exists_{l \in L} \exists_{m \in M} x \leq l \cdot m\}$

Another class of examples: internal homs $\hom_{sLat}(X, X)$ in the closed monoidal category of suplattices. For example, when the suplattice $X$ is a power set $P(S)$, one may identify $\hom_{sLat}(P(S), P(S))$ with the poset of binary relations $P(S \times S)$, ordered by inclusion and where the quantalic multiplication is relational composition. 

Quantales, as monoids in the symmetric monoidal category $sLat$, can be tensored to produce new quantales. 

###$*$-quantale###

A $*$-quantale is a quantale $Q$ equipped with an additional structure of an involution 

$$ * : Q \to Q$$ 

for which $(x \otimes y)^* = y^* \otimes x^*$ and $1^* = 1$, where $1$ denotes the monoidal unit. (The operator is assumed to be covariant with respect to the poset structure.) 

An example of a $*$-quantale is the quantale of binary relations on a set $S$, where the $*$-operation is relational opposite: 

* $R^* = \{(y, x): (x, y) \in R\}$ 

Another example is obtained by taking the quantale of down-closed subsets of a $*$-monoidal poset $M$ (which is the same thing as a $*$-[[star-monoid|monoid]] in the [[cartesian monoidal category]] of posets), with the quantale structure given by Day convolution as described above, and the $*$-operator obtained by cocontinuously extending the $*$-operator on $M$. Explicitly, 

* $L^* = \{x^*: x \in L\}$ 

### Morphisms of quantales ### 

There is a variety of notions of morphism of quantale, just as there is a variety of notions of morphism between closed monoidal categories. All the notions considered here are morphisms between the underlying sup-lattices, in other words preserve arbitrary joins, hence are left adjoints as functors between the underlying categories. 

At the weak end of the scale, one may consider _lax morphisms_ of quantales seen as just monoidal categories. 

A stronger notion is of _strong morphisms_ of quantales seen as monoidal categories. As noted above, all quantale morphisms considered here are already left adjoints in $Cat$, and if the adjunction lifts to $MonCat$ (the 2-category of monoidal categories, lax monoidal functors, and monoidal transformations) -- as is perhaps what usually happens in practice -- then the left adjoint is strong monoidal. So it is arguable that most lax morphisms of quantales which arise in practice are already strong. 

An even stronger notion is where the morphisms also strongly preserve the closed structure, i.e., the internal homs or residuations. (An example is to be developed for [[building]]s.) 
