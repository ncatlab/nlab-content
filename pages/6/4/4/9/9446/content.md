
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Monoid theory
+-- {: .hide}
[[!include monoid theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

Given a [[monoid]] (or [[semigroup]]) $S$, a __left ideal__ in $S$ is [[subset]] $A$ of $S$ such that $S A$ is contained in $A$.  Similarly, a __right ideal__ is a subset $A$ such that $A S \subseteq A$.  Finally, a __two-sided ideal__, or simply __ideal__, in $S$ is a subset $A$ that is both a left ideal and a right ideal.  

Given a [[monoidal category]] $(C, \otimes, I)$ and a [[monoid object]] (or semigroup object) $S$ of $C$, we can [[internalisation|internalise]] the above.  For instance, if $m: S \otimes S \to S$ is the binary multiplication and $\mu = m \circ (m \otimes 1_S) = m \circ (1_S \otimes m): S \otimes S \otimes S \to S$ the ternary multiplication, a two-sided ideal is a [[subobject]] $A$ of $S$, i.e., a mono $i: A \to S$ in $C$, such that the composite 

$$S \otimes A \otimes S \stackrel{1_S \otimes i \otimes 1_S}{\to} S \otimes S \otimes S \stackrel{\mu}{\longrightarrow} S$$

factors through $i: A \to S$. Clearly $i: A \to S$ is not necessarily a [[submonoid]], inasmuch as the monoid unit $e: I \to S$ need not factor through $i: A \to S$.

In particular for $C = $ [[Ab]], a monoid in $C$ is a [[ring]] and the corresponding notion of _[[ideal in a ring]]_ is the most common notion of ideal.

See [[ideal]] for ideals in more well known contexts: commutative idempotent monoids ([[semilattices]]) and monoids in [[Ab]] ([[rings]]).


## Properties and constructions 

An ideal $A$ (on either side) must be a [[subsemigroup]] of $S$, but it is a [[submonoid]] iff $1 \in A$, in which case $A = S$. 

### Ideals forming a quantale 

(Two-sided) ideals of a monoid $A$ are frequently the elements of a [[quantale]] whose multiplication is called taking the *product of ideals*. In the classical case of ideals over a [[ring]] $R$, the product $I J$ of ideals $I, J \subseteq R$ is the smallest ideal containing all products $i j: i \in I, j \in J$; the sup-lattice of such ideals ordered by inclusion is a [[residuated lattice]], in that there are also division operations where 

$$K/J \coloneqq \{r \in R: r J \subseteq K\}; \qquad I\backslash K = \{r \in R: I r \subseteq K\}$$ 

satisfying the expected [[adjunction|adjointness]] relations: $I \subseteq K/J$ iff $I J \subseteq K$ iff $J \subseteq I\backslash K$. 

A reasonably general context might be as follows. 

Let $\mathbf{C}$ be a [[well-powered category|well-powered]] [[regular category|regular]] [[cosmos]] ('cosmos' in the sense of complete cocomplete symmetric monoidal closed category). Just using the fact that $\mathbf{C}$ is a cosmos, we may construct a [[monoidal bicategory]] $Mod(\mathbf{C})$ whose objects are monoids $S$ in $\mathbf{C}$, whose 1-morphisms $S \to T$ are left-$S$ right-$T$ [[modules]], and whose 2-morphisms are bimodule homomorphisms. 

For each monoid $S$, there is a subbicategory of $Mod(\mathbf{C})$ whose only object is $S$; this is a  complete and cocomplete [[biclosed monoidal category]] $Mod_S$ whose objects are bimodules, i.e., 1-morphisms $S \to S$ in $Mod(\mathbf{C})$, and whose morphisms are bimodule homomorphisms. The unit of the monoidal product is $S$ with its standard $S$-bimodule structure, and hence the [[slice category|slice]] $Mod_S/S$ (see also [[semicartesian monoidal category]]) forms another complete and cocomplete biclosed monoidal category. 

An ideal of $S$ is just a subobject of $S$ in $Mod_S$. Under the assumption that $\mathbf{C}$ is well-powered, the category of subobjects $Sub(S) \hookrightarrow Mod_S/S$ is a (small) sup-lattice. Under the regularity assumption on $\mathbf{C}$, the subcategory $Sub(S) \hookrightarrow Mod_S/S$ is [[reflective subcategory|reflective]], and by applying the reflector to the monoidal product on $Mod_S/S$, we obtain a product on $Sub(S)$ which preserves arbitrary joins in each variable, hence a quantale. The unit of the quantale is the top element, namely $S$ considered as an ideal. 


## Related concepts

* [[sieve]]

* [[principal ideal of a monoid]]

* [[ideal of a ring]]

[[!redirects ideal of a monoid]]
[[!redirects ideals of a monoid]]
[[!redirects ideals of monoids]]
[[!redirects ideal in a monoid]]
[[!redirects ideals in a monoid]]
[[!redirects ideals in monoids]]

[[!redirects ideal of a semigroup]]
[[!redirects ideals of a semigroup]]
[[!redirects ideals of semigroups]]
[[!redirects ideal in a semigroup]]
[[!redirects ideals in a semigroup]]
[[!redirects ideal in semigroups]]
[[!redirects ideals in semigroups]]
