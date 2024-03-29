+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Definition

Let $U: C\to D$ be a [[forgetful functor]] and $x\in D$ an [[object]] of the [[category]] $D$.  

A **free $C$-object** on $x$ with respect to $U$ is an [[object]] of $C$ that satisfies the [[universal property]] that $F(x)$ would have, if $F$ were a [[left adjoint]] to $U$ (the corresponding [[free functor]]) (the _[[free construction]]_ on $x$).  

If $U$ actually has a [[left adjoint]], then $F(x)$ is a free $C$-object on $x$ for every $x$, and conversely if there exists a free $C$-object on every $x\in D$ then $U$ has a left adjoint.  But individual free objects can exist without the whole left adjoint functor existing.  In general, we have a "partially defined adjoint", or $J$-[[relative adjoint]] where $J$ is the inclusion of a [[full subcategory]] (on those objects admitting free objects).

More precisely: a __free $C$-object on $x$__ consists of an object $y\in C$ together with a [[morphism]] $\eta_x \colon x\to U y$ in $D$ such that for any other $z\in C$ and morphism $f\colon x\to U z$ in $D$, there exists a unique $g\colon y\to z$ in $C$ with $U(g) \circ \eta_x = f$.  

In other words, it is an [[initial object]] of the [[comma category]] $(x/U)$.  A free $C$-object on $x$ is also sometimes called a **universal arrow** from $x$ to the functor $U$.  It can also be identified with a [[semi-final lift]] of an empty $U$-structured [[sink]]. 

Sometimes one says an object $c$ of $C$ is free (relative to a forgetful functor $U: C \to D$ which is often tacitly understood) if there is some object $x$ of $D$ and some arrow $x \to U c$ that is initial in $(x/U)$. For example, the [[Quillen-Suslin theorem]] says that [[finitely generated module|finitely generated]] [[projective modules]] over [[polynomial algebras]] over a [[field]] are free; the tacit forgetful functor is from the category of modules over a polynomial algebra to $Set$. In this way, freeness is understood as a [[stuff, structure, property|property]] of an object. 

Similarly, a __cofree object__ is given by a [[cofree functor]].

## Examples

* [[free abelian group]]

* [[free module]]

* [[distributivity pullback]]

For more examples see at _[[free construction]]_. 

A general way to construct free objects is with a [[transfinite construction of free algebras]] (in [[set theory|set-theoretic]] foundations), or with an [[inductive type]] or [[higher inductive type]] (in [[type theory|type-theoretic]] foundations).

## Related concepts

* [[free functor]], [[relative adjoint]], [[universal property]]

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

  * [[projective module]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* **free object**, [[free resolution]]
 
  * [[free module]]

* flat object, [[flat resolution]]

  * [[flat module]]





[[!redirects free object]]
[[!redirects free objects]]

[[!redirects cofree object]]
[[!redirects cofree objects]]
[[!redirects co-free object]]
[[!redirects co-free objects]]
[[!redirects fascist object]]
[[!redirects fascist objects]]

[[!redirects free property]]
[[!redirects free properties]]
