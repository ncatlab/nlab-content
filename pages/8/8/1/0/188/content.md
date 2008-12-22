#Definition#

A _monoid_ is the [[homset]] of a category with a single object.


##Remarks##

* This is equivalent to whatever definition you may be used to. In partiocular, this means that a monoid is a set $A$ equipped with a binary operation $p : A \times A \to A$ and special element $e \in A$ such that $e$ and $p$ satisfy the usual axioms of an associative product $p$ with unit $e$.

* For $A$ a monoid it makes sense to write $\mathbf{B}A$ for the corresponding category with single object $\bullet$  and with $A$ as its [[homset]], $A = Hom_{\mathbf{B}A}(\bullet, \bullet)$. 

##Examples##

* A monoid in which every element has an inverse is a [[group]]. For that reason monoids are often addressed as _semi-group_s.


#Generalizations#

The concept _monoid_ makes sense in any [[monoidal category]] $(C, \otimes)$: a monoid in $C$ is the [[hom-object]] of a $C$-enriched category with a single object.

For instance a "linear monoid" is a monoid in $Vect$, hence an [[algebra]]. 

Accordingly, the concept monoid makes sense in any [[bicategory]] $B$: a monoid in $B$  is the [[hom-object]] of a $B$-enriched category with a single object. Equivalently, this is the same as a [[monad]] in $B$. 

