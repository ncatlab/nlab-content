If we think of a [[ring]] $R$ is a one-object category [[enriched category|enriched]] over [[Ab]], a module $M$ of $R$ is a functor 
$$   M: R \to Ab $$
enriched over $Ab$.

Don't panic: this definition is equivalent to [the one you're used to](http://en.wikipedia.org/wiki/Module_mathematics#Formal_definition).

The category $R Mod$ has $R$-modules as objects and $R$-module homomorphisms as morphisms.  More abstractly, this is the [[enriched category|enriched]] [[functor category]] $Ab^R$.  

(It's possible that exponential notation is bad for an enriched functor category; maybe $hom(R,Ab)$ is better.)

##Discussion##

[[Eric Forgy|Eric]]: The wikipedia page distinguishes left $R$-modules as covariant functors and right $R$-modules as contravariant functors. Is that distinction important?

[[John Baez|John]]: Yes, very --- but I didn't have the energy to get into that yet.  For any ring $R$ there's a ring $R^{op}$ in which $x y$ is redefined to be $y x$.   I defined a left $R$-module above; a right $R$-module is the same as a left $R^{op}$-module.  Eventually we'll have to discuss all this stuff, which becomes vastly more important when we start talking about bimodules.  If we want to show off, we'll do it all not just for rings, which are [[monoid|monoids]] in [[Ab]], but more generally for monoids in any [[symmetric monoidal category]].  For any monoid $M$ in a symmetric monoidal category we can define a new monoid $M^{op}$, and we can define left and right $M$-modules, and a right $M$-module is the same as a left $M^{op}$-module.

