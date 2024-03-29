
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Induction
+-- {: .hide}
[[!include induction - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[dependent type theory]], a version of the [[identity type]] where elements from two different types can be compared for equality. Given types $A$ and $B$ and an [[equivalence of types]] $e:A \simeq B$, the two-type identity type between two elements $x:A$ and $y:B$ is a type $\mathrm{Id}_{A,B}(e, x, y)$ whose elements witness that $x$ and $y$ are "equal" over or modulo the equivalence $e$. 

The phrase “two-type identity type” is a placeholder name for a concept which may or may not have another name in the type theory literature. The idea however is that two-type identity types are the "non-dependent" versions of [[dependent identity types]] in that it directly compares elements between two equivalent types, rather than between a family of dependent types which are equivalent via [[transport]] across an [[identification]] in the index type. 

## Definition

Given types $A$ and $B$, two-type identity types are an [[inductive family]] of [[types]] 

$$e:A \simeq B, x:A, y:B \vdash \mathrm{Id}_{A, B}(e, x, y)$$

generated by the family of elements

$$x:A \vdash \mathrm{trefl}_{A}(x):\mathrm{Id}_{A, A}(\mathrm{id}_A, x, x)$$

where $\mathrm{id}_A$ is the [[identity equivalence]] on $A$. 

### Inference rules

The inference rules for forming two-type identity types and terms are as follows.  First the inference rule that defines the two-type identity type itself, as a [[dependent type]], in some [[context]] $\Gamma$.

Formation rule for two-type identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \quad \Gamma \vdash e:A \simeq B \quad \Gamma \vdash x:A \quad \Gamma \vdash y:B}{\Gamma \vdash \mathrm{Id}_{A, B}(e, a, b) \; \mathrm{type}}$$ 

Now the basic "introduction" rule, which says that everything is equal to itself in a canonical way.

Introduction rule for two-type identity types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash x:A}{\Gamma \vdash \mathrm{trefl}_{A}(x):\mathrm{Id}_{A, A}(\mathrm{id}_A, x, x)}$$ 

Next we have the "elimination" rule: 

Elimination rule for two-type identity types:
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, e:A \simeq B, x:A, y:B, q:\mathrm{Id}_{A, B}(e, x, y) \vdash C(e, x, y, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{x:A} C(\mathrm{Id}_A, x, x, \mathrm{trefl}_{A, A}(x)) \\
      \Gamma \vdash e:A \simeq B \quad \Gamma \vdash x:A \quad \Gamma \vdash y:B \quad \Gamma \vdash q:\mathrm{Id}_{A, B}(e, x, y, q)
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{Id}_{A, B}}(t, e, x, y, q):C(e, x, y, q)}$$

The elimination rule then says that if:

1. for any equivalence $e:A \simeq B$, any elements $x:A$ and $y:B$, and any two-type identification $q:\mathrm{Id}_{A, B}(e, x, y)$ we have a type $C(e, x, y, q)$, and
1. we have a specified dependent function 
$$t:\prod_{x:A} C(\mathrm{id}_A,x,x,\mathrm{trefl}_{A, A}(x))$$

then we can construct a canonically defined term called the *eliminator*
$$\mathrm{ind}_{\mathrm{Id}_{A, B}}(t,e,x,y,q):C(e,x,y,q)$$ 
for *any* $e$, $x$, $y$, and $q$. 

Then, we have the [[computation rule]] or [[beta-reduction]] rule. This says that for all elements $x:A$, substituting the dependent function $t:\prod_{x:A} C(\mathrm{id}_A,x,x,\mathrm{trefl}_{A,A}(x))$ into the eliminator along the constructor for $x$ yields an element equal to $t(x)$ itself.  Normally "equal" here means [[judgmental equality]] (a.k.a. definitional equality), but it is also possible for it to mean [[propositional equality]] (a.k.a. typal equality), so there are two possible computation rules

Computation rules for two-type identity types:

* Judgmental computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, e:A \simeq B, x:A, y:B, q:\mathrm{Id}_{A, B}(e, x, y) \vdash C(e, x, y, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x)) \quad \Gamma \vdash x:A
    \end{array}
  }{\Gamma \vdash \mathrm{ind}_{\mathrm{Id}_{A, B}}(t, \mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x)) \equiv t(x):C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x))}$$

* Propositional computational rule
$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, e:A \simeq B, x:A, y:B, q:\mathrm{Id}_{A, B}(e, x, y) \vdash C(e, x, y, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x)) \quad \Gamma \vdash x:A
    \end{array}
  }{\Gamma \vdash \beta_{\mathrm{Id}_{A, B}}(t, x):\mathrm{Id}_{C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x))}(\mathrm{ind}_{\mathrm{Id}_{A, B}}(t, \mathrm{id}_A, x, x, \mathrm{trefl}_{A, B}(x), t(x))}$$

Finally, one might consider a [[uniqueness rule]] or [[eta-conversion]] rule.  But similar to the case for [[identity types]], a judgmental uniqueness rule for two-type identity types implies that the type theory is an [[extensional type theory]], in which case there is not much need for two-type identity types, so such a rule is almost never written down.  And as for identity types and other inductive types, the propositional/typal uniqueness rule is provable from the other four inference rules, so we don't write it out explicitly.

### Dependent universal property

The elimination, typal computation, and typal uniqueness rules for two-type identity types state that two-type identity types satisfy the **dependent universal property of two-type identity types**. With the [[uniqueness quantifier]], the dependent universal property of two-type identity types could be simplified to the following rule:

$$\frac{
    \begin{array}{l}
      \Gamma \vdash A \; \mathrm{type} \quad \Gamma \vdash B \; \mathrm{type} \\
      \Gamma, e:A \simeq B, x:A, y:B, q:\mathrm{Id}_{A,B}(e, x, y) \vdash C(e, x, y, q) \; \mathrm{type} \\
      \Gamma \vdash t:\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x)) \quad \Gamma \vdash x:A
    \end{array}
  }{\Gamma \vdash \mathrm{up}_{\mathrm{Id}_{A, B}}(t, x):
\begin{array}{c}
\exists!J:\left(\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x))\right) \\ 
\to \left(\prod_{e:A \simeq B} \prod_{a:A} \prod_{b:B} \prod_{s:\mathrm{Id}_{A, B}(e, a, b)} C(e, a, b, s)\right) \\
.\mathrm{Id}_{C(\mathrm{id}_A, x, x)}(J(t, \mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x)), t(x))
\end{array}
}$$

In natural language this states that given types $A$ and $B$, and given a type family $C(e, x, y, q)$ indexed by elements $e:A \simeq B$, $x:A$, $y:B$, and $q:\mathrm{Id}_{A, B}(e, x, y)$, for all elements $t:\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x))$ and $x:A$, there exists a unique function $J$ with domain 
$$\prod_{x:A} C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x))$$
and codomain 
$$\prod_{e:A \simeq B} \prod_{a:A} \prod_{b:B} \prod_{s:\mathrm{Id}_{A, B}(e, a, b)} C(e, a, b, s)$$
such that $J(t, \mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x))$ is equal to $t(x)$ in the type $C(\mathrm{id}_A, x, x, \mathrm{trefl}_{A}(x))$. 

## Properties

### Relation with identity types

One could then show that there exist equivalences between identity types and two-type identity types

$$\mathrm{Id}_{A, B}(e, x, y) \simeq \mathrm{Id}_{B}(e(x), y)$$

and 

$$\mathrm{Id}_{A, B}(e, x, y) \simeq \mathrm{Id}_{A}(x, e^{-1}(y))$$

for all $e:A \simeq B$, $x:A$, and $y:B$. 

### Relation with dependent identity types

Dependent identity types $\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z)$ are two-type identity type for which the equivalence used is [[transport]] $\mathrm{transport}_{x:A.B(x)}(a, b, p):B(a) \simeq B(b)$ across the given identification $p:a =_A b$:

$$\mathrm{hId}_{x:A.B(x)}(a, b, p, y, z) \coloneqq \mathrm{Id}_{B(a), B(b)}(\mathrm{transport}_{x:A.B(x)}(a, b, p), y, z)$$

On the other hand, every two-type identity type $\mathrm{Id}_{A, B}(e, x, y)$ can be made into a dependent identity type. We first define a dependent type from the [[interval type]] $x:\mathbb{I} \vdash C(x)$ defined as 

* $C(\mathrm{left}) \equiv A$, 

* $C(\mathrm{right}) \equiv B$, and 

* $\mathrm{transport}_{x:\mathbb{I}.C(x)}(\mathrm{left}, \mathrm{right}, \mathrm{segment}) \equiv e$

Then, 

$$\mathrm{hId}_{x:\mathbb{I}.C(x)}(\mathrm{left}, \mathrm{right}, \mathrm{segment}, x, y) \simeq \mathrm{Id}_{A, B}(e, y, z)$$

#### Universes

Given a [[Tarski universe]] $(U, T)$, there is an equivalence 

$$\mathrm{Id}_{T(A), T(B)}(\mathrm{transport}_U(A, B, p), x, y) \simeq \mathrm{hId}_{X:U.T(X)}(A, B, p, x, y)$$

One could treat [[Russell universes]] as a [[Tarski universe]] whose type family is represented by the zero-width whitespace instead of $T$, yielding

$$\mathrm{hId}_{X:U.(X)}(A, B, p, x, y)$$ 

for the dependent identity type and

$$\mathrm{Id}_{A, B}(\mathrm{idtoequiv}_U(A, B, p), x, y) \simeq \mathrm{hId}_{X:U.(X)}(A, B, p, x, y)$$

for the equivalence. 

Given a [[Tarski universes]] $(U, T)$, if $U$ is univalent with [[equivalence]]

$$\mathrm{ua}_U(A, B):(A =_U B) \simeq (T(A) \simeq T(B))$$

then there is an equivalence of types

$$\mathrm{Id}_{T(A), T(B)}(e, x, y) \simeq \mathrm{hId}_{X:U.T(X)}(A, B, \mathrm{ua}_U(A, B)^{-1}(e), x, y)$$

for $U$-small types $A:U$ and $B:U$ and equivalence $e:A \simeq B$

For Russell universes $U$, the [[univalence axiom]] is represented by 

$$\mathrm{ua}_U(A, B):(A =_U B) \simeq (A \simeq B)$$

and the above equivalence is represented by

$$\mathrm{Id}_{A, B}(e, x, y) \simeq \mathrm{hId}_{A, B}(\mathrm{ua}_U(A, B)^{-1}(e), x, y)$$

for the equivalence. 

### One-to-one correspondence structure

Two-type identity types are [[one-to-one correspondences]]. Given an equivalence $e:A \simeq B$, 

* for all elements $y:B$, there exists a unique element $x:A$ such that $\mathrm{Id}_{A, B}(e, x, y)$; the witness is given by the right projection function of the equivalence $e:A \simeq B$

$$\pi_2(e):\prod_{y:B} \exists!x:A.\mathrm{Id}_{A, B}(e, x, y)$$

* for all elements $x:A$, there exists a unique element $y:B$ such that $\mathrm{Id}_{A, B}(e, x, y)$; the witness is given by the right projection function of the inverse equivalence $e^{-1}:B \simeq A$

$$\pi_2(e^{-1}):\prod_{x:A} \exists!y:B.\mathrm{Id}_{A, B}(e, x, y)$$

## Related concepts

* [[identity type]]

* [[dependent identity type]]

[[!redirects two-type identity type]]
[[!redirects two-type identity types]]

[[!redirects two-type path type]]
[[!redirects two-type path types]]

[[!redirects two-type identification type]]
[[!redirects two-type identification types]]

[[!redirects two-type equality type]]
[[!redirects two-type equality types]]