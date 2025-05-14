+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

\tableofcontents

## Idea

The _circle type_ is an [[axiom|axiomatization]] of the [[homotopy type]] of the ([[shape modality|shape]] of) the [[circle]] in the context of [[homotopy type theory]].

## Definition

There are two ways to define the circle type: one can define it in terms of explicit [[inference rules]], or one can use the notion of [[higher inductive type]].  We will discuss both formulations.

* [with inference rules](#ExplicitDefinition).

* [in terms of higher inductive types](#InTermsOfHigherInductiveTypes)

### With inference rules
{#ExplicitDefinition}

Let $a =_A b$ denote the [[identification type]] between elements $a:A$ and $b:A$ of type $A$, and let $y =_{x:A.B(x)}^{(a, b, p)} z$ denote the [[heterogeneous identification type]] between elements $y:B(a)$ and $z:B(b)$ of type family $x:A \vdash B(x)$, given elements $a:A$ and $b:A$ and [[identification]] $p:a =_A b$. Let $\mathrm{apd}_f(a, b, p)$ denote the [[dependent function application]] of the [[dependent function]] $f:\prod_{x:A} B(x)$ to the [[identification]] $p:a =_A b$

In the [[natural deduction]] formulation of [[dependent type theory]], the circle type is given by the following [[inference rules]]:

First the rule that defines the circle type itself in some context $\Gamma$.

**[[type formation]]**
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash S^1 \; \mathrm{type}}$$

Now the basic “introduction” rule, which says that the circle type consists of a base point $\mathrm{base}:S^1$ and a loop identification $\mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}$.

**[[term introduction]]**:
$$\frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{base}:S^1} \qquad \frac{\Gamma \; \mathrm{ctx}}{\Gamma \vdash \mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}}$$

#### Induction principle

There are different induction principles associated with the [[circle type]], depending on whether [[judgmental equalities]] or [[identifications]] are used; if the former are used, this results in **strict circle types**, and if the latter are used, this results in **weak circle types**. 

The induction principle for strict circle types states that if:

1. For all $x:S^1$ we have a type $C(x)$

1. For any term $c_\mathrm{base}:C(\mathrm{base})$ and any heterogeneous identification $c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself across $\mathrm{loop}$

then we have a dependent function $c:\prod_{x:S^1} C(x)$ such that evaluating $c$ at $\mathrm{base}$ results in $c_\mathrm{base}$ and applying $c$ across $\mathrm{loop}$ results in $c_\mathrm{loop}$.

$$c(\mathrm{base}) \equiv c_\mathrm{base} \qquad \mathrm{apd}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv c_\mathrm{loop}$$

The induction principle for weak circle types states that if:

1. For all $x:S^1$ we have a type $C(x)$

1. For any term $c_\mathrm{base}:C(\mathrm{base})$ and any heterogeneous identification $c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself across $\mathrm{loop}$

there exists a dependent function $c:\prod_{x:S^1} C(x)$ and an identification $p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}$ such that applying $c$ across $\mathrm{loop}$ is equal to $c_\mathrm{loop}$ across $p$. 

$$\mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}$$

These are both formalized via the elimination and computation rules for the circle type:

Elimination rules for the circle type:
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop}):\prod_{x:S^1} C(x)}$$

**Computation rules for the strict circle type**
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) \equiv c_\mathrm{base}:C(\mathrm{base})}$$

* Judgmental path constructors

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{apd}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}$$

* Propositional path constructors

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{apd}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}} c_\mathrm{loop}}$$

**Computation rules for the weak circle type**
$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}}$$

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \beta_{S^1}^{\mathrm{loop}}(c_\mathrm{base}, c_\mathrm{loop}):\mathrm{apd}_{\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(\mathrm{ind}_{S^1}(c_\mathrm{base}, c_\mathrm{loop})(\mathrm{base}), c_\mathrm{base}, \beta_{S^1}^{\mathrm{base}}(c_\mathrm{base}, c_\mathrm{loop}))} c_\mathrm{loop}}$$

For weak circle types, we can package the elimination and propositional computation rules together using [[dependent sum types]] to get a single rule for the induction principle of the circle type:

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_\mathrm{base}, c_\mathrm{loop}):\sum_{c:\prod_{x:S^1} C(x)} \sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{apd}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

Since the [[circle type]] is a [[positive type]], it is not necessary to include a [[uniqueness rule]] for the induction principle circle types, since the propositional uniqueness rule can be proven from the the other inference rules for the circle type. Nevertheless, one can include the uniqueness rule in the combined single induction rule by turning the dependent sum type into a [[uniqueness quantifier]], resulting in the **dependent universal property of the circle type**. 

$$\frac{\Gamma, x:S^1 \vdash C(x) \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C(\mathrm{base}) \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} c_\mathrm{base}}{\Gamma \vdash \mathrm{ind}_{S^1}^{x:S^1.C(x)}(c_\mathrm{base}, c_\mathrm{loop}):\exists!c:\prod_{x:S^1} C(x).\sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{apd}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C(\mathrm{base}).z =_{x:S^1.C(x)}^{(\mathrm{base}, \mathrm{base}, \mathrm{loop})} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

#### Recursion principle

In general, given a type $C$, by the [[weakening rule]] of [[dependent type theory]], one can form the constant type family $C$ indexed by $x:S^1$; then one can get the recursion principle of the circle type from the induction principle on $C$ regarded as a constant type family: 

The recursion principle for strict circle types states that if:

1. We have a type $C$

1. For any term $c_\mathrm{base}:C$ and any identification $c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself

then we have a function $c:S^1 \to C$ such that evaluating $c$ at $\mathrm{base}$ results in $c_\mathrm{base}$ and applying $c$ across $\mathrm{loop}$ results in $c_\mathrm{loop}$.

$$c(\mathrm{base}) \equiv c_\mathrm{base} \qquad \mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv c_\mathrm{loop}$$

The recursion principle for weak circle types states that if:

1. We have a type $C$

1. For any term $c_\mathrm{base}:C$ and any identification $c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}$ that $c_\mathrm{base}$ is equal to itself

there exists a function $c:S^1 \to C$ and an identification $p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}$ such that applying $c$ across $\mathrm{loop}$ is equal to $c_\mathrm{loop}$ across $p$. 

$$\mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C.z =_{C} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}$$

The recursion principle for weak circle types can be presented as a single rule via the use of a [[dependent sum type]]:

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \mathrm{rec}_{S^1}^{C}(c_\mathrm{base}, c_\mathrm{loop}):\sum_{c:S^1 \to C} \sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C.z =_{C} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

and similarly, the (non-dependent) **universal property of the circle type** is presented as a single rule by replacing the dependent sum type in the recursion principle with a uniqueness quantifier

$$\frac{\Gamma \vdash C \; \mathrm{type} \quad \Gamma \vdash c_\mathrm{base}:C \quad \Gamma \vdash c_\mathrm{loop}:c_\mathrm{base} =_{C} c_\mathrm{base}}{\Gamma \vdash \mathrm{rec}_{S^1}^{C}(c_\mathrm{base}, c_\mathrm{loop}):\exists!c:S^1 \to C.\sum_{p:c(\mathrm{base}) =_{C(\mathrm{base})} c_\mathrm{base}} \mathrm{ap}_c(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{z:C.z =_{C} z}^{(c(\mathrm{base}), c_\mathrm{base}, p)} c_\mathrm{loop}}$$

#### Large recursion principle
{#LargeRecursionPrinciple}

There is also a large recursion principle which allows one to construct a family of types indexed by the circle type from a type and an [[autoequivalence]]: 

The large recursion principle for circle types states that if:

1. We have a type $A$

1. We have an autoequivalence $e:A \simeq A$

then we have a type family $x:S^1 \vdash C(x)$ such that $C(\mathrm{base})$ results in $A$ and [[transport]] across $\mathrm{loop}$ results in $e$.

$$C(\mathrm{base}) \equiv A \qquad \mathrm{tr}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv e$$

Usually, the second computation principle is given by a typal equality, similarly to the recursion and induction principles

$$\beta_{S^1}^{\mathrm{loop},A}(e):\mathrm{tr}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{A \simeq A} e$$

There are also typal computation rules for the type as well, which postulate an equivalence of types instead of a judgmental equality, with

$$\beta_{S^1}^{\mathrm{base},A}(e):C(\mathrm{base}) \simeq A \qquad \beta_{S^1}^{\mathrm{base},A}(e) \circ \mathrm{tr}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \circ \beta_{S^1}^{\mathrm{base},A}(e)^{-1} \equiv \circ e$$

Similarly, the second computation principle can be given by a typal equality, similarly to the recursion and induction principles:

$$\beta_{S^1}^{\mathrm{loop},A}(e):\beta_{S^1}^{\mathrm{base},A}(e) \circ \mathrm{tr}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \circ \beta_{S^1}^{\mathrm{base},A}(e)^{-1} =_{A \simeq A} e$$

If one is working in a [[dependent type theory with type variables]] which has [[identity type#IdentityTypesBetweenTypes|identity types between types]], then one can also use identifications of types instead of equivalences of types to express large recursion of the circle type:

1. We have a type $A$

1. We have an self-identification of types $p:A = A$

then we have a type family $x:S^1 \vdash C(x)$ such that $C(\mathrm{base})$ results in $A$ and the [[action on identifications]] across $\mathrm{loop}$ results in $p$: 

$$C(\mathrm{base}) \equiv A \qquad \mathrm{ap}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv p$$

Usually, the second computation principle is given by a typal equality, similarly to the recursion and induction principles

$$\beta_{S^1}^{\mathrm{loop},A}(p):\mathrm{tr}_{S^1}^C(\mathrm{base}, \mathrm{base}, \mathrm{loop}) =_{A = A} p$$

...

### In terms of higher inductive types
{#InTermsOfHigherInductiveTypes}

As a [[higher inductive type]], the circle is given by

    Inductive Circle : Type
      | base : Circle
      | loop : Id Circle base base

This says that the type is inductively constructed from 

1. a [[term]] of circle type whose [[semantics|interpretation]] is as the [[base point]] of the circle, 

1. a term of the [[identification type]] between these two terms, whose interpretation is as the 1-cell of the circle

   $$
     base \stackrel{loop}{\to} base
     \,
   $$

   Hence as a non-constant path from the base point to itself.

## Properties 
 {#Properties}

### Relation to axiom K

\begin{theorem}
Suppose that the strict circle type has an identification $K:\mathrm{refl}_{S^1}(\mathrm{base}) = \mathrm{loop}$. Then every type is a [[set]]. 
\end{theorem}

\begin{proof}
For all types $A$, terms $x:A$, and self-identifications $p:x =_A x$, by the recursion principle of the strict circle type, we have the function $\mathrm{rec}_{S^1}(x, p):S^1 \to A$ such that 
$\mathrm{rec}_{S^1}(x, p)(\mathrm{base}) \equiv x$ and $\mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv p$. We also have by definition of $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}$ that 
$$\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{refl}_{S^1}(\mathrm{base})) \equiv \mathrm{refl}_{A}(\mathrm{rec}_{S^1}(x, p)(\mathrm{base})) \equiv \mathrm{refl}_A(x)$$ 
By applying $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base})$ to $K$, we have identification 
$$\mathrm{ap}_{\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base})}(\mathrm{refl}_{S^1}(\mathrm{base}), \mathrm{loop}, K):\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{refl}_{S^1}(\mathrm{base})) = \mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{loop})$$
which reduces down to 
$$\mathrm{ap}_{\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base})}(\mathrm{refl}_{S^1}(\mathrm{base}), \mathrm{loop}, K):\mathrm{refl}_{A}(x) = p$$
which is precisely [[axiom K]] for type $A$. Thus every type $A$ is a set.
\end{proof}

\begin{theorem}
Suppose that the loop of the circle is [[judgmentally equal]] to [[reflexivity]] of the base of the circle $\mathrm{refl}_{S^1}(\mathrm{base}) \equiv \mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}$. Then the judgmental [[K rule]] holds.
\end{theorem}

\begin{proof}
For all types $A$, terms $x:A$, and self-identifications $p:x =_A x$, by the recursion principle of the strict circle type, we have the function $\mathrm{rec}_{S^1}(x, p):S^1 \to A$ such that 
$\mathrm{rec}_{S^1}(x, p)(\mathrm{base}) \equiv x$ and $\mathrm{ap}_{\mathrm{rec}_{S^1}^A(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv p$. We also have by definition of $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}$ that 
$$\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{refl}_{S^1}(\mathrm{base})) \equiv \mathrm{refl}_{A}(\mathrm{rec}_{S^1}(x, p)(\mathrm{base})) \equiv \mathrm{refl}_A(x)$$ 
Since functions preserve judgmental equality, by applying the function $\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base})$ to the judgmental equality $\mathrm{refl}_{S^1}(\mathrm{base}) \equiv \mathrm{loop}:\mathrm{base} =_{S^1} \mathrm{base}$, we have a judgmental equality 
$$\mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{loop}) \equiv \mathrm{ap}_{\mathrm{rec}_{S^1}(x, p)}(\mathrm{base}, \mathrm{base}, \mathrm{refl}_{S^1}(\mathrm{base})):x =_A x$$
which reduces down to 
$$p \equiv \mathrm{refl}_A(x):x =_A x$$
which is precisely the judgmental [[K rule]] for type $A$. 
\end{proof}

### Types equivalent to the circle type

The circle type is equivalent to the following types

* The [[suspension type]] $\Sigma \mathrm{Bool}$ of the [[type of booleans]]. 

* The [[coequalizer type]] of any two [[endofunctions]] on the [[unit type]]

$$\mathbf{1} \rightrightarrows \mathbf{1} \to S^1$$

* Following [[synthetic homotopy theory]], the [[coequalizer type]] of the pair of functions on the [[line type]]

$$
A^1\underoverset{\quad s \quad}{\mathrm{id}_{A^1}}{\rightrightarrows}A^1 \to S^1
$$

* Given a [[univalent universe]] $U$, the type of $U$-small $\mathbb{Z}$-torsors. One can then prove that this type satisfies the same induction principle (propositionally). This is due to [[Dan Grayson]].

### Induction principle without heterogeneous identifications

There is a version of the induction principle which uses a type $C$ and a function $f:C \to S^1$ instead of a type family $P(x)$ indexed by $x:S^1$. It has the benefit of not requiring that one has first defined [[heterogeneous identification types]], whether as an [[inductive family]] of types or by using [[transport]]. 

The induction principle of the circle type says that given a type $C$ and a function $f:C \to S^1$, as well as 

* an element $c_\mathrm{base}:C$

* identifications $c_\mathrm{loop}:c_\mathrm{base} =_C c_\mathrm{base}$ and $p_\mathrm{base}:f(c_\mathrm{base}) =_{S^1} \mathrm{base}$ such that $\mathrm{ap}_f(c_\mathrm{loop})$, $p_\mathrm{base}$, $p_\mathrm{base}$, and $\mathrm{loop}$ form a square


$$
\begin{array}{c}
    & f(c_\mathrm{base}) & \overset{\mathrm{ap}_{f}(c_\mathrm{loop})}= & f(c_\mathrm{base}) &  \\
    p_\mathrm{base} & \Vert &  & \Vert & p_\mathrm{base}\\
    & \mathrm{base} & \underset{\mathrm{loop}}= & \mathrm{base} & \\
\end{array}
$$

* an identification saying that the square commutes

$$p_\mathrm{loop}:\mathrm{ap}_f(c_\mathrm{loop}) \bullet p_\mathrm{base} =_{f(c_\mathrm{base}) =_{S^1} \mathrm{loop}} p_\mathrm{base} \bullet \mathrm{loop}$$

one can construct 

* a function 

$$g:S^1 \to C$$

* a homotopy witnessing that $g$ is a [[section]] of $f$:

$$\mathrm{sec}_g:\prod_{x:S^1} f(g(x)) =_{S^1} x$$

such that 

$$g(\mathrm{base}) \equiv c_\mathrm{base} \quad \mathrm{sec}_g(\mathrm{base}) \equiv p_\mathrm{base} \quad \mathrm{ap}_{g}(\mathrm{loop}) \equiv c_\mathrm{loop}$$

$$\mathrm{ind}_{=}\left(\lambda x:S^1.\mathrm{refl}_{f(g(x)) =_{S^1} x}(\mathrm{sec}_g(x)), \mathrm{base}, \mathrm{base}, \mathrm{loop}\right) \equiv p_\mathrm{loop}$$

The last condition needs some explanation. Since $g$ is a section of $f$, the composite $f \circ g$ is [[generalized the|the]] [[identity function]] on the [[circle type]], up to [[identification]]. Now, given any identity function on the circle type $i:S^1 \to S^1$ with homotopy

$$j:\prod_{x:S^1} i(x) =_{S^1} x$$

we have the following square for all $x:S^1$, $y:S^1$, and $q:x =_{S^1} y$:

$$
\begin{array}{c}
    & i(x) & \overset{\mathrm{ap}_{i}(q)}= & i(y) &  \\
    j(x) & \Vert &  & \Vert & j(y)\\
    & x & \underset{q}= & y & \\
\end{array}
$$

This [[commutative square|square commutes]] via the [[J rule]]: it suffices to construct an element of 

$$\mathrm{ap}_{i}(\mathrm{refl}_{S^1}(x)) \bullet j(x) =_{i(x) =_{S^1} x} j(x) \bullet \mathrm{refl}_{S^1}(x)$$

But $\mathrm{ap}_{i}(\mathrm{refl}_{S^1}(x)) \bullet j(x)$ reduces down to $j(x)$ via 
$$\mathrm{ap}_{i}(\mathrm{refl}_{S^1}(x)) \bullet j(x) \equiv \mathrm{refl}_{S^1}(i(x)) \bullet j(x) \equiv j(x)$$ 
and similarly $j(x) \bullet \mathrm{refl}_{S^1}(x)$ reduces down to $j(x)$, so just take reflexivity of $j(x)$. 

So the naturality square is inductively defined by 

$$\mathrm{ind}_{=}\left(\lambda x:S^1.\mathrm{refl}_{i(x) =_{S^1} x}(j(x)), x, y, q\right):\mathrm{ap}_{i}(q) \bullet j(y) =_{i(x) =_{S^1} y} j(x) \bullet q$$

When $i \coloneqq f \circ g$, $j \coloneqq \mathrm{sec}_g$, $x \coloneqq \mathrm{base}$, $y \coloneqq \mathrm{base}$, and $q \coloneqq \mathrm{loop}$, this results in the identification 

$$\mathrm{ind}_{=}\left(\lambda x:S^1.\mathrm{refl}_{f(g(x)) =_{S^1} x}(\mathrm{sec}_g(x)), \mathrm{base}, \mathrm{base}, \mathrm{loop}\right)$$

which is of the same type as $p_\mathrm{loop}$ due to the [[judgmental equalities]] in the other computation rules. 

One gets back the usual induction principle of the interval type when $C \equiv \sum_{x:S^1} P(x)$ and $f \equiv \pi_1$ the first projection function of the dependent sum type, and one gets back the recursion principle of the interval type when $C \equiv S^1 \times P$ and $f \equiv \pi_1$ the first projection function of the product type.

### Extensionality principle of the circle type

The extensionality principle of the circle type says that there is an equivalence of types between the identification type $\mathrm{base} =_{S^1} \mathrm{base}$ and the type of integers $\mathbb{Z}$:

$$\mathrm{ext}_{S^1}:(\mathrm{base} =_{S^1} \mathrm{base}) \simeq \mathbb{Z}$$

Equivalently, that the [[loop space type]] $\Omega(S^1, \mathrm{base})$ is equivalent to the [[integers]]. 

Thus, the extensionality principle of the circle type implies that the integers and thus the natural numbers are [[contractible types]] if [[axiom K]] or [[uniqueness of identity proofs]] hold for the entire type theory. If the extensionality principle of the natural numbers also hold in the type theory, then every type is contractible. 

One can prove the extensionality principle of the circle type, given a [[univalent universe]] where the circle is small relative to the universe. The [[HoTT book]] provides a number of such proofs. 

If one doesn't have a type of integers or a [[type universe]], then the extensionality principle of the [[circle type]] says that the [[identity types]] $\mathrm{base} =_{S^1} \mathrm{base}$ satisfy the [[dependent universal property of the integers type]] with respect to the element $\mathrm{refl}_{S^1}(\mathrm{base}):\mathrm{base} =_{S^1} \mathrm{base}$ and the equivalence 
$$\lambda p:\mathrm{base} =_{S^1} \mathrm{base}.p \bullet \mathrm{loop}:(\mathrm{base} =_{S^1} \mathrm{base}) \simeq (\mathrm{base} =_{S^1} \mathrm{base})$$

This is a special case of the extensionality principle of [[coequalizer types]] and [[pushout types]] as detailed in [Kraus and Raumer (2019)](#KrausRaumer19). 

The [[circle type#LargeRecursionPrinciple|large recursion principle]] of the circle type also implies the extensionality principle of the circle type. 

### The circle type and infinity

The extensionality principle of the circle type says that the loop space of the circle at its base point $\Omega(S^1, \mathrm{base})$ is a [[denumerable set]]. However, there is a weaker axiom that one can add to the circle type: that $\Omega(S^1, \mathrm{base})$ is an [[infinite set|infinite]] type. 

By the recursion principle of the natural numbers, there is a function 

$$\mathrm{rec}_{\mathbb{N}}(\mathrm{refl}_{S^1}(\mathrm{base}), \lambda l:\Omega(S^1, \mathrm{base}).l \bullet \mathrm{loop}):\mathbb{N} \to \Omega(S^1, \mathrm{base})$$

which takes zero to reflexivity of $\mathrm{base}$ and the successor function to concatenation of a self-identification by $\mathrm{loop}$. That $\Omega(S^1, \mathrm{base})$ is an infinite set, states that the above function is an [[embedding of types]], 
$$\mathrm{inf}_{S^1}:\mathrm{isEmbed}\left(\mathrm{rec}_{\mathbb{N}}(\mathrm{refl}_{S^1}(\mathrm{base}), \lambda l:\Omega(S^1, \mathrm{base}).l \bullet \mathrm{loop})\right)$$
or equivalently that application of the above function is an equivalence for all natural numbers $m:\mathbb{N}$, $n:\mathbb{N}$

$$\mathrm{inf}_{S^1}:\prod_{m:\mathbb{N}} \prod_{n:\mathbb{N}} \mathrm{isEquiv}\left(\mathrm{ap}_{\mathrm{rec}_{\mathbb{N}}(\mathrm{refl}_{S^1}(\mathrm{base}), \lambda l:\Omega(S^1, \mathrm{base}).l \bullet \mathrm{loop})}(m, n)\right)$$

If one doesn't have a [[natural numbers type]], the loop space $\Omega(S^1, \mathrm{base})$ of the circle type at its base point $\mathrm{base}:S^1$ is an [[infinite set]] if and only if $\Omega(S^1, \mathrm{base})$ is equivalent to the [[sum type]] $\Omega(S^1, \mathrm{base}) + \Omega(S^1, \mathrm{base})$. 

$$\mathrm{inf}_{S^1}:\Omega(S^1, \mathrm{base}) \simeq (\Omega(S^1, \mathrm{base}) + \Omega(S^1, \mathrm{base}))$$

See [Rasekh 21](#Rasekh21) for proving this statement in the presence of the [[univalence axiom]]. 

### Kuratowski-finiteness

The circle type is [[Kuratowski-finite]]. (Cf [Frumin et al. 18](#FGGW))

### H-space structures on the circle type

The type of [[H-spaces]] on the circle type is a [[contractible type]]. 

## Related concepts

* [[circle]], [[unit circle]], [[circle group]], [[circle object]]

* [[interval type]]

* [[line type]]

* [[minimal simplicial circle]]

* [[suspension type]]

* [[sphere type]]

* [[homotopy groups of spheres]]

* [[Jordan curve]]

* [[lemniscate type]]


## References
 {#References}

The formalization of the [[shape modality|shape]] [[homotopy type]] $&#643; S^1 \simeq \mathbf{B}\mathbb{Z}$ of the circle as a [[higher inductive type]] in [[homotopy type theory]], along with a proof that $\Omega &#643;S^1\simeq {\mathbb{Z}}$ (and hence $\pi_1(&#643;S^1) \simeq \mathbb{Z}$):

* {#LicataShulman13} [[Dan Licata]], [[Mike Shulman]], *Calculating the Fundamental Group of the Circle in Homotopy Type Theory*, LICS '13: Proceedings of the 2013 28th Annual ACM/IEEE Symposium on Logic in Computer Science June 2013 ([arXiv:1301.3443](http://arxiv.org/abs/1301.3443), [doi:10.1109/LICS.2013.28](https://doi.org/10.1109/LICS.2013.28))

  > blog announcements: 

  > [A formal proof that $\pi_1(S^1) = \mathbb{Z}$](https://homotopytypetheory.org/2011/04/29/a-formal-proof-that-pi1s1-is-z/)

  > [A simpler proof that $\pi_1(S^1) = \mathbb{Z}$](http://homotopytypetheory.org/2012/06/07/a-simpler-proof-that-%cf%80%e2%82%81s%c2%b9-is-z/)

Formalization in [[proof assistants]]:

in [[Coq]]:

* The HoTT Coq library: [theories/hit/Circle.v](https://github.com/HoTT/HoTT/blob/master/theories/hit/Circle.v)

in [[Agda]]:

* The HoTT Agda library: [homotopy/LoopSpaceCircle.agda](https://github.com/HoTT/HoTT-Agda/blob/2.0/homotopy/LoopSpaceCircle.agda)

Exposition and review:

* {#UFP13} [[Univalent Foundations Project]], §8.1 *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

Alternative construction of the circle type as the type of $\mathbb{Z}$-torsors:

* {#BezemBuchholtzGraysonShulman19} [[Marc Bezem]], [[Ulrik Buchholtz]], [[Daniel Grayson]], [[Michael Shulman]], _Construction of the Circle in UniMath_, Journal of Pure and Applied Algebra Volume 225, Issue 10, October 2021, 106687 ([arXiv:1910.01856](https://arxiv.org/abs/1910.01856))

Alternative construction of the circle type as a coequalizer:

* {#Shulman15} [[Mike Shulman]], Section 9 of  _Brouwer's fixed-point theorem in real-cohesive homotopy type theory_, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

For the fact that the type of H-space structures on a circle type is contractible:

* [[Ulrik Buchholtz]], [[J. Daniel Christensen]], [[Jarl G. Taxerås Flaten]], [[Egbert Rijke]], *Central H-spaces and banded types* &lbrack;[arXiv:2301.02636](https://arxiv.org/abs/2301.02636)&rbrack;

For the fact that the circle type is Kuratowski-finite:

* {#FGGW} [[Dan Frumin]], [[Herman Geuvers]], [[Léon Gondelman]], [[Niels van der Weide]], _Finite Sets in Homotopy Type Theory_, in *CPP 2018: Proceedings of the 7th ACM SIGPLAN International Conference on Certified Programs and Proofs* (2018) 201–214 &lbrack;[doi:10.1145/3167085](https://doi.org/10.1145/3167085), [pdf](http://cs.ru.nl/~nweide/FiniteSetsInHoTT.pdf)&rbrack;

For the fact that one can construct a [[natural numbers type]] from the circle type:

* {#Rasekh21} [[Nima Rasekh]], _Every Elementary Higher Topos has a Natural Number Object_, Theory and Applications of Categories **37** 13 (2021) 337-377.  ([arXiv:1809.01734](https://arxiv.org/abs/1809.01734), [tac:37-13](http://www.tac.mta.ca/tac/volumes/37/13/37-13abs.html))

For the induction principle of the identity types of the circle type:

* {#KrausRaumer19} [[Nicolai Kraus]], [[Jakob von Raumer]], *Path Spaces of Higher Inductive Types in Homotopy Type Theory*. &lbrack;[arXiv:1901.06022](https://arxiv.org/abs/1901.06022)&rbrack;

[[!redirects circle type]]
[[!redirects circle types]]

[[!redirects strict circle type]]
[[!redirects strict circle types]]
[[!redirects weak circle type]]
[[!redirects weak circle types]]

[[!redirects dependent universal property of the circle type]]
[[!redirects dependent universal property of circle types]]

[[!redirects universal property of the circle type]]
[[!redirects universal property of circle types]]

[[!redirects dependent universal property of the identity types of the circle type]]
[[!redirects dependent universal property of the identity types of circle types]]
[[!redirects dependent universal property of identity types of the circle type]]
[[!redirects dependent universal property of identity types of circle types]]

[[!redirects universal property of the identity types of the  the circle type]]
[[!redirects universal property of the identity types of circle types]]
[[!redirects universal property of identity types of the  the circle type]]
[[!redirects universal property of identity types of circle types]]