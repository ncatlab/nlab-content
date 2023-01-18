

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

It is also possible to combine the cube layer and the tope layer together into one layer of shapes, just as in traditional mathematics it is possible to combine the set layer and the logic layer into one layer of types:

#### Shape layer

The shape layer is a [[dependent type theory]] which consists of [[identity types]], [[dependent sum types]], [[dependent product types]], [[empty type]], [[unit type]], [[propositional truncations]], [[booleans type]], [[quotient sets]], and [[axiom K]] or [[uniqueness of identity proofs]]. This is enough to define cofibrations used for extension types as well as the coherent theory of the interval used for [[simplicial type theory]]. 

#### Type layer

This type layer is a [[dependent type theory]] with some notion of [[identity type]], [[dependent product type]], [[dependent sum type]], and [[higher inductive types]], as well as [[judgmental equality]] to reflect the identity type of the shape layer, and shape contexts in addition to the usual type contexts. The [[beta conversion]] and [[eta conversion]] rules for the types may either be typal or judgmental. 

We also state the rules in such a way that the following substitution rule is admissible:

$$\frac{\Xi \vdash s:I \quad \Xi, x:I \vert \Gamma \vdash a:A}{\Xi \vert \Gamma(s) \vdash a(s):A(s)}$$

We also have a rule which states that the identity type in the shape layer behaves like judgmental equality in the type layer

$$\frac{\Xi \vdash I \; \mathrm{shape} \quad \Xi \vdash s:I \quad \Xi \vdash t:I \quad \Xi \vdash p:s =_I t \quad \Xi, x:I \vert \Gamma \vdash a:A}{\Xi \vert \Gamma(s) \vdash a(s) \equiv a(t)}$$

Finally, we have rules which states that the type theory in the type layer respects the type theory in the shape layer. This means that we have additional elimination, computation, and uniqueness rules for all the positive types in the shape layer:

Elimination rules for the empty shape
$$\frac{\Xi \vdash \mathbb{0} \; \mathrm{shape} \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash C(x) \; \mathrm{type}}{\Xi, x:\mathbb{0} \vert \Gamma \vdash \mathrm{ind}_\mathbb{0}^C(x):C(x)}$$

Uniqueness rules for the empty shape
$$\frac{\Xi \vdash \mathbb{0} \; \mathrm{shape} \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash C(x) \; \mathrm{type} \quad \quad \Xi, x:\mathbb{0} \vert \Gamma \vdash c(x):C(x)}{\Xi, x:\mathbb{0} \vert \Gamma \vdash c(x) \equiv \mathrm{ind}_\mathbb{0}^C(x):C(x)}$$

#### Cofibrations and extension types

A cofibration is a shape inclusion, which means shapes $A$ and $B$ and an embedding of shapes $i:A \hookrightarrow B$. 

Formation rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x)
\end{array}
}{\Xi \vert \Gamma \vdash \langle \prod_{y:B} C(y) \vert_c^A \rangle \; \mathrm{type}}$$

Introduction rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x) \\
\Xi, y:B \vert \Gamma \vdash d(y):C(y) \quad \Xi, x:A \vert \Gamma \vdash d(i(x)) \equiv c(x):C(x) \\
\end{array}
}{\Xi \vert \Gamma \vdash \lambda y^B.d(y):\langle \prod_{y:B} C(y) \vert_c^A \rangle}$$

Elimination rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle \quad \Xi \vdash b:B
\end{array}
}{\Xi \vert \Gamma \vdash f(b):C(b)}$$

$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle \quad \Xi \vdash a:A
\end{array}
}{\Xi \vert \Gamma \vdash f(i(a)) \equiv c(a):C(a)}$$

Computation rules for dependent extension types
$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vdash \Gamma \; \mathrm{ctx} \quad \Xi, y:B \vert \Gamma \vdash C(y) \; \mathrm{type} \quad \Xi, x:A \vert \Gamma \vdash c(x):C(x) \\
\Xi, y:B \vert \Gamma \vdash d(y):C(y) \quad \Xi, x:A \vert \Gamma \vdash d(i(x)) \equiv c(x):C(x) \quad \Xi \vert b:B\\
\end{array}
}{\Xi \vert \Gamma \vdash (\lambda y^B.d(y))(b) \equiv d(b):C(b)}$$

Uniqueness rules for dependent extension types

$$\frac{
\begin{array}{l}
\Xi \vdash A \; \mathrm{shape} \quad \Xi \vdash B \; \mathrm{shape} \quad \Xi \vdash i:A \hookrightarrow B \\
\Xi \vert \Gamma \vdash f:\langle \prod_{y:B} C(y) \vert_c^A \rangle
\end{array}
}{\Xi \vert \Gamma \vdash f \equiv \lambda y^B.f(y):\langle \prod_{y:B} C(y) \vert_c^A \rangle}$$

## See also

* [[simplicial type theory]]
* [[cubical type theory]]
* [[two-level type theory]]

## References

* {#RiehlShulman17} [[Emily Riehl]], [[Michael Shulman]], *A type theory for synthetic $\infty$-categories* $[$[arXiv:1705.07442](https://arxiv.org/abs/1705.07442)$]$