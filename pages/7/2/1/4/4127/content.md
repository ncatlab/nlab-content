
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

In a [[category]] $C$, a [[class]] $W\subseteq Mor(C)$ of [[morphisms]] is said to satisfy **2-out-of-6** if for any sequence of three composable morphisms

$$ X\xrightarrow{u} Y \xrightarrow{v} Z \xrightarrow{w} K$$

if $w v$ and $v u$ are in $W$, then so are $u$, $v$, $w$, and $w v u$.

## Examples

* The class of [[isomorphisms]] in any category satisfies 2-out-of-6.  This case is the archetype of most of the cases in which the property is invoked: 2-out-of-6 is characteristic of morphisms that have a notion of [[inverse]].

* A category equipped with a class of "[[category with weak equivalences|weak equivalences]]" containing the [[identity morphisms]] and satisfying 2-out-of-6 is called a [[homotopical category]].  In particular, this includes any [[model category]].

## Relation to other concepts

### 2-out-of-3

The 2-out-of-6 property implies the [[two-out-of-three]] property.  For on the one hand, if $f$ and $g$ are in $W$, then applying 2-out-of-6 to $\xrightarrow{f} \xrightarrow{1} \xrightarrow{g}$, we find that $g f\in W$.  On the other hand, if $f$ and $g f$ are in $W$, then applying 2-out-of-6 to $\xrightarrow{1} \xrightarrow{f} \xrightarrow{g}$, we find that $g\in W$, and similarly if $g$ and $g f$ are in $W$.

### Identities and isomorphisms

If $W$ satisfies 2-out-of-6 and contains the identities (i.e. $C$ is a homotopical category), then $W$ contains all isomorphisms.  For if $f$ has inverse $g$, then applying 2-out-of-6 to $\xrightarrow{g} \xrightarrow{f} \xrightarrow{g}$ we find that $g$ and $f$ are in $W$.

### Closure under retracts

The 2-out-of-6 property is closely related to the property that $W$ is closed under [[retracts]], as a [[subcategory]] of the [[arrow category]].  For instance, we have the following theorem due to [Blumberg-Mandell](#BlumbergMandell) (stated there in the context of [[Waldhausen categories]]):

+-- {: .num_theorem #CofibRetracts}
###### Theorem
Suppose a [[category with weak equivalences]] $\mathcal{C}$ has an additional class of maps called [[cofibrations]] which satisfy the following properties:

* All [[pushouts]] of cofibrations exist.

* The pushout of a cofibration that is also a weak equivalence is again a cofibration and a weak equivalence.

* Every weak equivalence factors as a weak equivalence that is a cofibration followed by a weak equivalence that is a [[retraction]].

Then if the weak equivalences in $\mathcal{C}$ are closed under retracts, they also satisfy 2-out-of-6.

=--

+-- {: .proof}
###### Proof

Suppose the first three assumptions on the cofibrations, and let 
$$A \xrightarrow{u} B \xrightarrow{v} C \xrightarrow{w} D$$
be a sequence of composable maps, with $w v$ and $v u$ weak equivalences.  Factor $v u\colon A\to C$ as $A \xrightarrow{i} C' \xrightarrow{p} C$ where $i$ is a cofibration weak equivalence and $p$ is a weak equivalence with a [[section]]] $s\colon C\to C'$.  Let $B'$ be the pushout
$$
  \array{
    A & \overset{i}{\to} & C'\\
  ^u\downarrow && \downarrow^h\\
  B& \underset{k}{\to} & B'}
$$

Since $p i = v u$, we have a unique map $g\colon B' \to C$ such that $g h = p$ and $g k = v$.  Define $f = h s$; then $g f = g h s = p s = 1_C$.

Since $i$ is a cofibration weak equivalence, so is $k$.  And since $w g k = w v\colon B\to D$ is a weak equivalence, by two-out-of-three, $w g\colon B' \to D$ is also a weak equivalence.  But now we have a commutative diagram

$$\array{C & \overset{f}{\to} & B' & \xrightarrow{g} & C \\
  ^w\downarrow && \downarrow^{w g} && \downarrow^w\\
  D& \underset{=}{\to} & D & \underset{=}{\to} & D}
$$

exhibiting $w$ as a retract of $w g$ in the arrow category.  Thus, by assumption $w$ is a weak equivalence.  By successive applications of two-out-of-three, so are $v$, $u$, and $w v u$.
=--

Of course, there is a dual theorem for fibrations.  Note that the fibrations in a [[category of fibrant objects]] satisfy (the duals of) all the above conditions.  They are not implied by the axioms for the cofibrations in a [[Waldhausen category]] (the factorization axiom is what is missing), but many Waldhausen categories do satisfy them.

### Saturation

The 2-out-of-6 property is also closely related to the property that $W$ is *saturated*, in the sense that any morphism which becomes an isomorphism in the [[localization]] $C[W^{-1}]$ is already a weak equivalence.  (This is unrelated to the notion of [[saturated class of maps]] used in the theory of [[weak factorization systems]].)

Clearly saturation implies 2-out-of-6, but we also have the following two converses.

+-- {: .num_theorem #FracSat}
###### Theorem

Suppose $W$ admits a [[calculus of fractions]].  Then $W$ satisfies two-out-of-six if and only if it is saturated.

=--
+-- {: .proof}
###### Proof

This is from 7.1.20 of _[[Categories and Sheaves]]_.  Suppose $f\colon X\to Y$ becomes an isomorphism in $\mathcal{C}[W^{-1}]$, and represent its inverse by $Y \xrightarrow{g} X' \overset{s}{\leftarrow} X$ with $s\in W$.  Then since $g f$ and $s$ represent the same morphism in $\mathcal{C}[W^{-1}]$, there is a morphism $t\colon X'\to X''$ in $W$ such that $t g f = t s$.  Since $t s\in W$, it follows by 2-out-of-3 that $g f\in W$.

Now applying this same argument to $g$, we obtain an $h$ such that $h g \in W$.  But then by 2-out-of-6, we have $f\in W$ as desired.
=--

+-- {: .num_theorem #CofSat}
###### Theorem

Suppose $C$ has a class of "cofibrations" satisfying the properties in Theorem \ref{CofibRetracts}, and moreover the pushout of any weak equivalence along a cofibration is a weak equivalence.  Then $W$ satisfies two-out-of-six if and only if it is saturated (and hence, if and only if it is closed under retracts).
=--
+-- {: .proof}
###### Proof
See [Blumberg-Mandell](#BlumbergMandell) for details; an outline follows.

We first observe that $W$ admits a [[homotopy calculus of left fractions]], and in particular that every morphism in $\mathcal{C}[W^{-1}]$ can be represented by a zigzag $A \to C \overset{\sim}{\leftarrow} B$ in which $B\xrightarrow{\sim} C$ is a cofibration and a weak equivalence.  See [Blumberg-Mandell](#BlumbergMandell), section 5 for a detailed proof.  The idea is that given any zigzag $A \overset{\sim}{\leftarrow} D \to B$, we factor $D\to A$ as a cofibration weak equivalence followed by a retraction weak equivalence, then push out the cofibration along $D\to B$ and use the section to obtain a map from $A$ into the pushout.

Now suppose $a\colon A\to B$ becomes an isomorphism in $C[W^{-1}]$, and represent its inverse by $B \xrightarrow{b} C \overset{c}{\leftarrow} A$ with $c$ a cofibration weak equivalence.  Since the composite $A \xrightarrow{b a} C \overset{c}{\leftarrow} A$ represents $1_A$, we have $b a \in W$.  Consider the following diagram where the squares are pushouts:
$$\array{ && A & \overset{a}{\to} & B & \xrightarrow{b} & C \\
 &&  ^c\downarrow && \downarrow && \downarrow\\
B & \underset{b}{\to} & C& \underset{}{\to} & B' & \underset{}{\to} & C'}$$
All the vertical maps are cofibration weak equivalences, by assumption.  Moreover, the bottom map $C\to C'$ is a weak equivalence, since it is the pushout of the weak equivalence $b a$ along the cofibration $c$.  And since the zigzag
$$ B \xrightarrow{b} C \to B' \overset{\sim}{\leftarrow} B $$
represents the same morphism as
$$ B \xrightarrow{b} C \overset{c}{\leftarrow} A \xrightarrow{a} B$$
which represents $1_B$, we have that $B\xrightarrow{b} C \to B'$ is a weak equivalence.  Thus, by 2-out-of-6, $b$ is a weak equivalence, hence so is $a$ by 2-out-of-3.
=--

Of course, there is a dual theorem for fibrations.

## References

* [[William Dwyer]], [[Philip Hirschhorn]], [[Daniel Kan]], [[Jeff Smith]], _[[Homotopy Limit Functors on Model Categories and Homotopical Categories]]_

* [[Andrew Blumberg]] and [[Michael Mandell]], *Algebraic $K$-theory and abstract homotopy theory*
{#BlumbergMandell}

* [[Masaki Kashiwara]], [[Pierre Schapira]], _[[Categories and Sheaves]]_

* Andrei Radulescu-Banu, *Cofibrations in Homotopy Theory*

[[!redirects two-out-of-six]]
[[!redirects two-out-of-six-property]]
[[!redirects 2-out-of-6 property]]
[[!redirects 2-out-of-6-property]]
[[!redirects 2-out-of-6]]
