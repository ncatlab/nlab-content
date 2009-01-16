#Idea#

A Hopf algebra is a generalization of:

* the [[group algebra]] of a [[group]]

* the algebra of functions on a group

* the [[universal enveloping algebra]] of a [[Lie algebra]]

All these algebras are actually [[bialgebra|bialgebras]], but furthermore they have a 'antipode' operation which mimics the inverse operation of a group.

#Definition#

A **Hopf algebra** is a [[bialgebra]] $A$ equipped with an **antipode** map 

$$S : A \to A$$

with the property that taking any element of $A$, applying the comultiplication map $\Delta : A \to A \otimes A$, applying either $1 \otimes S$ or $S \otimes 1$ to the resulting element of $A \otimes A$, and finally applying the multiplication map $m: A \otimes A \to A$, we obtain the same result as if we first applied the counit $e : A \to k$ and then the unit $i : k \to A$.

This should remind you of how taking a group element $g$, duplicating it to obtain $(g,g)$, taking the inverse of either component of this ordered pair, and then multiplying the two components, we obtain the identity element of our group.

An equivalent, more abstract definition of a (commutative) Hopf algebra is as a [[group|group object]] in $Alg^{op}$, where $Alg$ is the category of commutative algebras.  This works because the tensor product of commutative algebras is the categorical [[coproduct]], and hence the [[product]] in its [[opposite category]].

#References#

For a diagrammatic definition of a Hopf algebra, see the [Wikipedia entry](http://en.wikipedia.org/wiki/Hopf_algebra#Formal_definition).

_Word of caution_: In algebraic topology, it is common to talk of Hopf algebra without mentioning the antipode since in many topological cases of interest it exists automatically.  For example, this is the case if it is [[graded object|graded]] and "connected" in the sense that its degree-0 part is just the ground field (a property possessed by the homology or cohomology of any connected space).
