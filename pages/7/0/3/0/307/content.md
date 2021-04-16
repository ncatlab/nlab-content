
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Definition

A **terminal object** in a [[category]] $C$ is an [[object]] $1$ of $C$ satisfying the following [[universal property]]: 

for every object $x$ of $C$, there exists a unique [[morphism]] $!:x\to 1$.  The terminal object of any category, if it exists, is unique up to unique [[isomorphism]].  If the terminal object is also [[initial object|initial]], it is called a [[zero object]].


## Remarks

* Less usual synonyms are _final object_ and _terminator_.

* A terminal object is often written $1$, since in [[Set]] it is a 1-element set, and also because it is the unit for the cartesian [[product]].  Other notations for a terminal object include $*$ and $pt$.

## Properties

* A terminal object may also be viewed as a [[limit]] over the [[empty diagram]].  Conversely, a limit over a diagram is a terminal cone over that diagram.

* For any object $x$ in a category with terminal object $1$, the categorical [[product]] $x\times 1$ and the [[exponential object]] $x^1$ both exist and are canonically isomorphic to $x$.


+-- {: .num_prop }
###### Proposition

Let $\mathcal{C}$ be a [[category]].

1. The following are equivalent:

   1. $\mathcal{C}$ has a [[terminal object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[right adjoint]]

      $$
        \ast 
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \mathcal{C}
      $$

    Under this equivalence, the [[terminal object]] is identified with the image under the right adjoint of the unique object of the [[terminal category]].

1. Dually, the following are equivalent:

   1. $\mathcal{C}$ has an [[initial object]];

   1. the unique [[functor]] $\mathcal{C} \to \ast$ to the [[terminal category]] has a [[left adjoint]]

      $$
        \mathcal{C}
          \underoverset
             {\underset{}{\longrightarrow}}
             {\overset{}{\longleftarrow}}
             {\bot}
        \ast
      $$

    Under this equivalence, the [[initial object]] is identified with the image under the left adjoint of the unique object of the [[terminal category]].

=--


+-- {: .proof}
###### Proof

Since the unique [[hom-set]] in the [[terminal category]] is [[generalized the|the]] [[singleton]], the hom-isomorphism characterizing the [[adjoint functors]] is directly the [[universal property]] of an [[initial object]] in $\mathcal{C}$
 
$$
  Hom_{\mathcal{C}}( L(\ast) , X )
  \;\simeq\;
  Hom_{\ast}( \ast, R(X) ) 
  =
  \ast 
$$

or of a [[terminal object]]

$$
  Hom_{\mathcal{C}}( X , R(\ast) )
  \;\simeq\;
  Hom_{\ast}( L(X), \ast ) = \ast
  \,,
$$

respectively.

=--



## Examples

Some examples of terminal objects in notable categories follow:

* The terminal object of a [[partial order|poset]] is its [[top element]], if it exists.

* Any [[one-element set]] is a terminal object in the category [[Set]].

* The terminal object of [[Top]] is the [[point space]].

* The [[trivial group]] is the terminal object of [[Grp]] and, as an [[abelian group]], of [[Ab]].

* The terminal object of [[Ring]] is the [[zero ring]].  (Note however that if [[ring|rings]] have unities and ring [[homomorphism|homomorphisms]] must preserve them, then the zero ring is not a [[zero object]] of [[Ring]].)

* Including most of the above, the terminal object of an [[algebraic category]] is its [[trivial algebra]].

* The terminal object of [[Cat]] is the [[discrete category]] with just one object, the [[trivial category]].

* The terminal object of a [[over category|slice category]] $C/x$ is the [[identity morphism]] $x \to x$.


## Related concepts

* [[initial object]]

* [[unit type]]

* [[terminal object in a quasi-category]].

* [[strict terminal object]]


[[!redirects terminator]]
[[!redirects terminal object]]
[[!redirects terminal objects]]
[[!redirects terminal]]
[[!redirects final object]]
[[!redirects final objects]]