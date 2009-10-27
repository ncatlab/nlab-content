#Idea#

The notion of  _monomorphism_ is the generalization of the notion of _injective map of  sets_ from the [[category]] [[Set]] to arbitrary [[category|categories]].

#Definition#

A **monomorphism** in a [[category]] $C$ is a [[morphism]] $f : X \to Y$ such that, equivalently,

* $f$ is an [[epimorphism]] in the [[opposite category]] $C^{op}$.

* for any object $A$ the induced morphism $f_* : C(A,X) \to C(A,Y)$ is injective.

The last condtition here states the usual arrow-theoretic way to say monomorphism:

The morphism $f : X \to Y$ is mono precisely if for all $g,h  : A \to X$ such that $f_*(h) : A \stackrel{g}{\to} X \stackrel{f}{\to}Y $ equals
$f_*(g) : A \stackrel{g}{\to} X \stackrel{f}{\to}Y $ we have $g = h$.

# related concepts #

* [[isomorphism]] classes of monomorphism define [[subobject]]s.

* for more details see [[epimorphism]].

[[!redirects monomorphisms]]
