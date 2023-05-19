

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

It is also possible to combine the cube layer and the tope layer together into one layer of exotypes, just as in traditional mathematics it is possible to combine the set layer and the logic layer into one layer of types:

#### Exotype layer

The exotype layer is a [[dependent type theory]] which consists of [[identity types]], [[dependent sum types]], [[dependent product types]], [[empty type]], [[unit type]], a [[type of all propositions]] which we shall call $\mathrm{Tope}$, and [[axiom K]] or [[uniqueness of identity proofs]]. 

With a [[type of all propositions]], one can define  [[propositional truncations]], the [[booleans type]] (as the type of all decidable propositions), and [[quotient sets]]. 

#### Shapes

Shapes can be defined from exotype predicates or subtypes: given an exotype $I$ and a family of topes $t:I \vdash \phi:\mathrm{Tope}$, one has the shape 

$$\sum_{t:I} \mathrm{El}_\mathrm{Tope}(\phi(t))$$ 

which is the type theoretic equivalent of the set $\{t:I \vdash \phi\}$ in set-builder notation. 

This is enough to define cofibrations used for extension types as well as the coherent theory of the interval used for [[simplicial type theory]]. 

#### Type layer

This type layer is a [[dependent type theory]] with some notion of [[identity type]], [[dependent product type]], [[dependent sum type]], and [[higher inductive types]], as well as [[judgmental equality]] to reflect the identity type of the exotype layer, and shape contexts in addition to the usual type contexts. The [[beta conversion]] and [[eta conversion]] rules for the types may either be typal or judgmental. 

We also state the rules in such a way that the following substitution rule is admissible:

$$\frac{\Xi \vdash s:I \quad \Xi, x:I \vert \Gamma \vdash a:A}{\Xi \vert \Gamma(s) \vdash a(s):A(s)}$$

We also have a rule which states that the identity type in the exotype layer behaves like judgmental equality in the type layer

$$\frac{\Xi \vdash I \; \mathrm{exotype} \quad \Xi \vdash s:I \quad \Xi \vdash t:I \quad \Xi \vdash p:s =_I t \quad \Xi, x:I \vert \Gamma \vdash a:A}{\Xi \vert \Gamma(s) \vdash a(s) \equiv a(t)}$$

Finally, we have rules which states that the type theory in the type layer respects the type theory in the exotype layer. This means that we have additional elimination, computation, and uniqueness rules for all the positive types in the exotype layer:

Elimination rules for the empty exotype
$$\frac{\Xi \vdash \mathbb{0} \; \mathrm{exotype} \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash C(x) \; \mathrm{type}}{\Xi, x:\mathbb{0} \vert \Gamma \vdash \mathrm{ind}_\mathbb{0}^C(x):C(x)}$$

Uniqueness rules for the empty exotype
$$\frac{\Xi \vdash \mathbb{0} \; \mathrm{exotype} \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash C(x) \; \mathrm{type} \quad \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash c(x):C(x)}{\Xi, x:\mathbb{0} \vert \Gamma \vdash c(x) \equiv \mathrm{ind}_\mathbb{0}^C(x):C(x)}$$

#### Cofibrations and extension types

A cofibration is a shape inclusion, which means the families of elements $t:I \vdash \phi:\mathrm{Tope}$ and $t:I \vdash \psi:\mathrm{Tope}$ representing shapes, and a family of elements $t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope}$ representing that one shape is a subtype of the other. 

Formation rules for dependent extension types
$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I, \phi:\mathrm{Tope} \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I, \phi:\mathrm{Tope} \vert \Gamma \vdash a:A
\end{array}
}{\Xi \vert \Gamma \vdash \langle \prod_{t:I, \psi:\mathrm{Tope}} A \vert_a^\phi \rangle \; \mathrm{type}}$$

Introduction rules for dependent extension types
$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I, \phi:\mathrm{Tope} \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I, \phi:\mathrm{Tope} \vert \Gamma \vdash a:A \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I, \psi:\mathrm{Tope} \vert \Gamma \vdash b:A \quad \Xi, t:I, \psi:\mathrm{Tope} \vert \Gamma \vdash b \equiv a:A
\end{array}
}{\Xi \vert \Gamma \vdash \lambda t^{I,\psi:\mathrm{Tope}}.b:\langle \prod_{t:I,\psi:\mathrm{Tope}} A \vert_a^\phi \rangle}$$

Elimination rules for dependent extension types
$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vert \Gamma \vdash f:\langle \prod_{t:I,\psi:\mathrm{Tope}} A \vert_a^\phi \rangle \quad \Xi \vdash s:I \quad \Xi \vdash \psi[s/t]
\end{array}
}{\Xi \vert \Gamma \vdash f(s):A}$$

$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vert \Gamma \vdash f:\langle \prod_{t:I,\psi:\mathrm{Tope}} A \vert_a^\phi \rangle \quad \Xi \vdash s:I \quad \Xi \vdash \psi[s/t]
\end{array}
}{\Xi \vert \Gamma \vdash f(s) \equiv a:A}$$

Computation rules for dependent extension types
$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I, \phi:\mathrm{Tope} \vert \Gamma \vdash A \; \mathrm{type} \quad \Xi, t:I, \phi:\Omega \vert \Gamma \vdash a:A \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, t:I, \psi:\mathrm{Tope} \vert \Gamma \vdash b:A \quad \Xi, t:I, \psi:\mathrm{Tope} \vert \Gamma \vdash b \equiv a:A \\
\end{array}
}{\Xi \vert \Gamma \vdash (\lambda t^{I, \psi:\mathrm{Tope}}.b)(s) \equiv b[s/t]:A}$$

Uniqueness rules for dependent extension types

$$\frac{
\begin{array}{l}
t:I \vdash \phi:\mathrm{Tope} \quad t:I \vdash \psi:\mathrm{Tope} \quad t:I, \phi:\mathrm{Tope} \vdash \psi:\mathrm{Tope} \\
\Xi \vert \Gamma \vdash f:\langle \prod_{t:I,\psi:\mathrm{Tope}} A \vert_a^\phi \rangle 
\end{array}
}{\Xi \vert \Gamma \vdash f \equiv \lambda t^{I,\psi:\mathrm{Tope}}.f(t):\langle \prod_{t:I,\psi:\mathrm{Tope}} A \vert_a^\phi \rangle}$$

## See also

* [[simplicial type theory]]
* [[cubical type theory]]
* [[two-level type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$