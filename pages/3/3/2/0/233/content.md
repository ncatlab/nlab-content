#General concept#

Generally, a (right) module over a [[monoid]] $A$ [[internalization|internal to]] a [[monoidal category]] $V$ is an object $N$ of $V$ equipped with a morphism

$$
  \rho : N \otimes A \to N
$$

in $C$ which satisfies the usual axioms of an [[action]].  

Equivalently, regarding the [[monoid]] $A$ as a one-object $V$-[[enriched category]] $\mathbf{B}A$, the module together with its action are given by a $V$-functor

$$
  \rho : \mathbf{B}A \to V
  \,.
$$

Correspondingly, a _left_ module over $A$ is a functor

$$
  \rho : (\mathbf{B}A)^{\mathrm{op}} \to V
  \,.
$$

In this language the concept directly generalizes to the [[horizontal categorification]] of monoids $A$. Let $K$ be _any_ $V$-[[enriched category]], then $V$-functors
$
  \rho : K \to V
$
give right modules and functors
$
  \rho : K^{\mathrm{op}} \to V
$ give left modules over $K$. Accordingly, for $K$ and $L$ two $V$-enriched categories one says that $V$-functors

$$
  K^{op} \otimes L \to V
$$

are _$K$-$L$-[[bimodule]]s_, also known as _profunctors_ or _[[distributor]]s_ from $K$ to $L$.





#Modules over rings#

Recalling that a [[ring]] $R$ is a monoid in the category [[Ab]] of abelian groups, hence equivalently a one-object $Ab$-enriched category $\mathbf{B}R$,
a module $M$ over a $R$ is a module in [[Ab]] in the above sense, hence in particular
an $Ab$-functor 
$$   
  M: \mathbf{B}R \to Ab 
  \,.
$$

Don't panic: this definition is equivalent to [the one you're used to](http://en.wikipedia.org/wiki/Module_mathematics#Formal_definition).

The category $R Mod$ has $R$-modules as objects and $R$-module homomorphisms as morphisms.  More abstractly, this is the [[enriched category|enriched]] [[functor category]] $[R,Ab]$ (see [page 29](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf#page=29) of Kelly's book.)


##Discussion##

[[Eric Forgy|Eric]]: The wikipedia page distinguishes left $R$-modules as covariant functors and right $R$-modules as contravariant functors. Is that distinction important?

[[John Baez|John]]: Yes, very --- but I didn't have the energy to get into that yet.  For any ring $R$ there's a ring $R^{op}$ in which $x y$ is redefined to be $y x$.   I defined a left $R$-module above; a right $R$-module is the same as a left $R^{op}$-module.  Eventually we'll have to discuss all this stuff, which becomes vastly more important when we start talking about bimodules.  If we want to show off, we'll do it all not just for rings, which are [[monoid|monoids]] in [[Ab]], but more generally for monoids in any [[symmetric monoidal category]].  For any monoid $M$ in a symmetric monoidal category we can define a new monoid $M^{op}$, and we can define left and right $M$-modules, and a right $M$-module is the same as a left $M^{op}$-module.

