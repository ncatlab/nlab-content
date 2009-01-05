#The idea

Given a category $C$, we obtain the 'opposite category' $C^{op}$ by turning all the arrows around.  This idea is important in understanding [[duality]].  For example, a [[comonoid]] in $C$ is the same as a [[monoid]] in $C^{op}$.

# Definition

Given a category $C$, the **opposite category** $C^{op}$ has the same objects as $C$, but a morphism $f : x \to y$ in $C^{op}$ is the same as a morphism $f : y \to x$ in $C$, and a composite of morphisms $g f$ in $C^{op}$ is defined to be the composite $f g$ in $C$.

#Remarks#

Passing to the opposite category is a realization of abstract [[duality]]. 

This goes as far that some entities are _defined_ as objects in an opposite category. In particular, all generalizations of [[geometry]] which characterize [[space and quantity|spaces]] in terms of [[algebra|algebras]]. The idea of [[noncommutative geometry]] is essentially to define a category of _spaces_ as the opposite category of a category of algebras. Similarly, a [[locale]] is opposite to a [[frame]].

+--{.query}
Are there examples where algebras are defined as dual to spaces?
=--

Another example is the definition of the category of [[L-infinity algebroid|L-infinity algebroids]] as that opposite to quasi-free differential graded algebras, identifying every $L_\infty$-algebra with its [[duality|dual]] [[Chevalley-Eilenberg algebra]].