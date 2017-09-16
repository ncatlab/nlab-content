#The idea

Given a category $C$, we obtain the 'opposite category' $C^{op}$ by turning all the arrows around.  This idea is important in understanding [[duality]].  For example, a [[comonoid]] in $C$ is the same as a [[monoid]] in $C^{op}$.  See also: [[opposite 2-category]].

# Definition

Given a category $C$, the **opposite category** $C^{op}$ has the same objects as $C$, but a morphism $f : x \to y$ in $C^{op}$ is the same as a morphism $f : y \to x$ in $C$, and a composite of morphisms $g f$ in $C^{op}$ is defined to be the composite $f g$ in $C$.

## Definition in enriched category theory ##

For $V$ a [[symmetric monoidal category]] and $C$ a $V$-[[enriched category]] the **opposite $V$-enriched category** $C^{op}$ is defined to be the $V$-enriched category with the same objects as $C$ and with

$$
  C^{op}(c,d) := C(d,c)
$$

and composition given by

$$
  C^{op}(b,c)\otimes C^{op}(a,b)
  :=
  C(c,b) \otimes C(b,a)
  \stackrel{\sigma}{\to}
  C(b,a) \otimes C(c,b)
  \stackrel{\circ_C}{\to} 
  C_{c,a}
  =:
  C^{op}(a,c)
  \,.
$$

The unit maps $j_a : I \to C^{op}(a,a)$ are those of $C$ under the identification $C^{op}(a,a) = C(a,a)$.


#Remarks#

Passing to the opposite category is a realization of abstract [[duality]]. 

This goes as far that some entities are _defined_ as objects in an opposite category. In particular, all generalizations of [[geometry]] which characterize [[space and quantity|spaces]] in terms of [[algebra|algebras]]. The idea of [[noncommutative geometry]] is essentially to define a category of _spaces_ as the opposite category of a category of algebras. Similarly, a [[locale]] is opposite to a [[frame]].

+--{.query}
Are there examples where algebras are defined as dual to spaces?
=--

Another example is the definition of the category of $L_\infty$-[[Lie infinity-algebroid|algebroids]] as that opposite to quasi-free differential graded algebras, identifying every $L_\infty$-algebra with its [[duality|dual]] [[Chevalley-Eilenberg algebra]].


#References#

for the definition in enriched category theory see page 12 of 

* Kelly, _Basic concepts of enriched category theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))