

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

Type theory with shapes is a [[layered type theory]] consisting of a [[dependent type theory]] over a [[type theory|typed]] [[predicate logic]] with [[finite product]] types. The type layer of the typed predicate logic is called the **cube layer**, whose types are called **cubes**, the [[propositional logic]] layer of the typed predicate logic is called the **tope layer**, whose types are called **topes**, and the type layer of the dependent type theory is called the **type layer**, whose types are called **types**. Shapes are then built out of cubes and topes. 

Type theory with shapes is used in some formalizations of [[simplicial type theory]] and [[cubical type theory]]. 

## Syntax

### With three layers

#### Cube layer

The cube layer is a [[type theory]] which consists of [[finite product]] types. 

$$\frac{}{() \; \mathrm{cubectx}} \qquad \frac{\Xi \; \mathrm{cubectx} \quad \Xi \vdash I \; \mathrm{cube}}{\Xi, t:I \; \mathrm{cubectx}} \quad \frac{\Xi, t:I, \Xi' \; \mathrm{cubectx}}{\Xi, t:I, \Xi' \vdash t:I}$$

$$\frac{\Xi \; \mathrm{cubectx}}{\Xi \vdash \mathbb{1} \; \mathrm{cube}} \qquad \frac{\Xi \vdash I \; \mathrm{cube} \quad \Xi \vdash J \; \mathrm{cube}}{\Xi \vdash I \times J \; \mathrm{cube}}$$

#### Tope layer

The tope layer is an [[intuitionistic logic]] over the cube layer, and the types in the tope layer are called topes because they can be interpreted as [[polytopes]] embedded in a cube. There is a tope representing [[equality]] of terms of cubes, called the *equality tope* and given the symbol $\equiv_I$ for cube $I$. The equality tope is used to define the eta and beta conversion rules for finite product cubes. 

$$\frac{\Xi \; \mathrm{cubectx}}{\Xi \vert () \; \mathrm{topectx}} \qquad \frac{\Xi \vert \Phi \; \mathrm{topectx} \quad \Xi \vert \Phi \vdash \phi \; \mathrm{tope}}{\Xi \vert \Phi, \phi \; \mathrm{topectx}} \quad \frac{\Xi \vert \Phi, \phi, \Phi' \; \mathrm{topectx}}{\Xi \vert \Phi, \phi, \Phi' \vdash \phi}$$

#### Shapes

Shapes are a cube with a tope in the context of a term of the cube

$$\frac{\Xi \vdash I \: \mathrm{cube} \quad \Xi, t:I \vdash \phi \; \mathrm{tope}}{\Xi \vdash \{t:I \vert \phi \} \; \mathrm{shape}}$$

#### Type layer

This type layer is a [[dependent type theory]] with some notion of [[identity type]], [[dependent product type]], [[dependent sum type]], and [[higher inductive types]], as well as [[judgmental equality]] to reflect the equality tope of the tope layer, and cube contexts and tope contexts in addition to the usual type contexts. The [[beta conversion]] and [[eta conversion]] rules for the types may either be typal or judgmental. In addition, there is no equality reflection rule, which makes the dependent type theory an [[intensional type theory]]. 

#### Extension types

Formation rules for non-dependent extension types
$$\frac{\{t:I \vert \phi\} \; \mathrm{shape} \quad \{t:I \vert \psi\} \; \mathrm{shape} \quad t:I \vert \phi \vdash \psi \quad \Xi \vert \Phi \vdash \Gamma \; \mathrm{ctx} \quad \Xi \vert \Phi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I \vert \Phi, \phi \vert \Gamma \vdash a:A}{\Xi \vert \Phi \vert \Gamma \vdash \langle \{t:I \vert \psi\} \to A \vert_a^\phi \rangle \; \mathrm{type}}$$

### With two layers

It is also possible to combine the cube layer and the tope layer together into one layer, just as in traditional mathematics it is possible to combine the set layer and the logic layer into one layer of types:

#### Shape layer

The Shape layer is a [[dependent type theory]] which consists of [[identity types]], [[dependent sum types]], [[empty type]], [[unit type]], [[propositional truncations]], [[booleans type]], [[axiom K]] or [[uniqueness of identity proofs]], [[judgmental equality]], and an [[equality reflection]] rule making the type theory into an [[extensional type theory]]. This is enough to define the coherent theory of the interval used for [[simplicial type theory]]. General types are called "shapes" or "cubes", and types which are (-1)-truncated are called "topes". 

Given a cube or shape $I$ and a family of topes $t:I \vdash \phi(t)$ - a family of cubes with a family of witnesses that each cube is (-1)-truncated - the shape formed by the cube and the tope is the dependent sum type 

$$\{t:I \vert \phi \} \coloneqq \sum_{t:I} \phi(t)$$

#### Type layer

This type layer is a [[dependent type theory]] with some notion of [[identity type]], [[dependent product type]], [[dependent sum type]], and [[higher inductive types]], as well as [[judgmental equality]] to reflect the equality tope of the tope layer, and cube contexts and tope contexts in addition to the usual type contexts. The [[beta conversion]] and [[eta conversion]] rules for the types may either be typal or judgmental. In addition, there is no equality reflection rule, which makes the dependent type theory an [[intensional type theory]]. 

#### Extension types

Formation rules for non-dependent extension types
$$\frac{\sum_{t:I} \phi(t) \; \mathrm{shape} \quad \sum_{t:I} \psi(t) \; \mathrm{shape} \quad t:I, \alpha:\phi(t) \vdash \beta:\psi(t) \; \mathrm{type} \quad \Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, z:\sum_{t:I} \phi(t) \vert \Gamma \vdash a:A}{\Xi \vert \Gamma \vdash \langle \left(\sum_{t:I} \phi(t)\right) \to A \vert_a^\phi \rangle \; \mathrm{type}}$$

## See also

* [[simplicial type theory]]
* [[cubical type theory]]
* [[two-level type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$