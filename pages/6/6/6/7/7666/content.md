
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{:toc}

## Idea

Local boundedness of a [[category]] is a generalization of the notion of [[locally presentable category|local presentability]] that includes the category of [[topological spaces]].

## Context

Let $C$ be a [[small category|small]] [[cocomplete category]] with a proper [[factorization system]], i.e., an [[orthogonal factorization system]] $(E,M)$ where every [[morphism|map]] in $E$ is an [[epimorphism]] and every map in $M$ is a [[monomorphism]].

The $M$-**union** of a small family of $M$-[[subobjects]] $(A_j \to B)_{j \in J}$ is the unique $M$-subobject $A \to B$ containing the $A_j$ and so that the induced map $\sum_j A_j \to A$ is in $E$. The union is calculated by applying the $(E,M)$ factorization to the canonical map $\sum_j A_j \to B$. 

If the map $\sum_j A_j \to B$ is in $E$, we say $(A_j \to B)_{j \in J}$ is an $M$-**union**. The set $J$ is a preorder under the relation $j \leq k$ if $A_j \leq A_k$ as $M$-subobjects of $B$. Regarding the $A_j$ as a diagram of shape $J$, the family $(A_j \to B)_{j \in J}$ is an $M$-union if and only if the map colim$A_j \to B$ is in $E$. We say $(A_j \to B)_{j \in J}$ is a **filtered union of** $M$-**subobjects** if it is a union of $M$-subobjects and if the category $J$ is [[filtered category|filtered]].

A [[representable functor]] $C(X,-)$ **preserves** the $M$-union of $(A_j \to B)_{j \in J}$ if the functions $C(X,A_j) \to C(X,A)$ are jointly surjective, i.e., if each $X \to A$ factors through some $X \to A_j$.

## Definition

Let $\lambda$ be a [[regular cardinal]], and let $C$ be a cocomplete category with a proper factorization system $(E,M)$.

+-- {: .num_defn}
###### Definition (locally bounded)

An object $X$ in $C$ is $\lambda$-**bounded** if $C(X,-)$ preserves $\lambda$-[[filtered colimit|filtered]] [[unions]] of $M$-subobjects. 

=--

+-- {: .num_defn}
###### Definition ($(E,M)$-generator)

A small set $G$ of objects of $C$ is an $(E,M)$-**generator**  if $f \colon A \to B$ in $M$ is invertible whenever $f_* \colon C(X,A) \to  C(X,B)$ is [[bijection|bijective]] for all $X \in G$. Equivalently, $G$ is an $(E,M)$-**generator** if for each $A \in C$ the family of maps $X \to A$ is jointly in $E$, i.e., if the map $\sum_{X \in G} \sum_{C(X,A)} X \to A$ is in $E$.

=--

+-- {: .num_defn}
###### Definition (locally bounded category)

A [[category]] $C$ is called **locally** $\lambda$-**bounded** with respect to a proper factorization system $(E,M)$ if

* it has an $(E,M)$-generator $G$ each of whose objects is $\lambda$-bounded

* it has arbitrary cointersections (even large ones) of maps in $E$ --- that is, it is [[E-cocomplete category|E-cocomplete]].

=--

## Features

+-- {: .num_prop}
###### Proposition (relation to local presentability)
In a locally $\lambda$-presentable category, every $\lambda$-presentable object is $\lambda$-bounded. Hence a $\lambda$-presentable category is $\lambda$-bounded.
=--

+-- {: .proof}
###### Proof

This appears as Lemma 2.3.1 of [Freyd-Kelly](#FreydKelly)
=--

+-- {: .num_prop}
###### Proposition (completeness)
Locally bounded categories are necessarily complete
=--

+-- {: .proof}
###### Proof

This appears as Corollary 2.2 of [Kelly-Lack](#KellyLack).

The essential point is an $(E,M)$-variant of the special adjoint functor theorem: if $C$ is cocomplete, has a proper factorization system $(E,M)$, admits arbitrary $E$-cointersections, and has an $(E,M)$-generator, then every cocontinuous functor $C \to D$ has a right adjoint.
=--


##Examples

The following examples are discussed in Section 6.1 of Kelly's _Basic concepts of enriched category theory_.

* [[locally presentable category|Locally presentable categories]] such as the categories of [[simplicial sets]], [[categories]], [[abelian groups]], [[Set|sets]].

* [[compactly generated topological space|Compactly generated spaces]], and likewise based compactly generated spaces, with $E$ the surjections and $M$ the subspace inclusions. The point is an $(E,M)$-generator.

* [[quasi-topological space|Quasi-topological spaces]].  Note that this category is not $E$-well-copowered.

* [[Banach spaces]] with $E$ the epimorphisms, equivalently the dense maps, and $M$ the [[extremal monomorphisms]], equivalently the inclusions of closed subspaces with the induced norm. The base field is an $(E,M)$-generator.

## Related notions
The term **locally ranked** is sometimes used to refer to a locally bounded category which in addition is co-wellpowered. For example, this terminology is used in [Ad&#225;mek et. al.](#AHRT).

## References 

The contents of this page are taken from:

* [[Max Kelly]], [[Steve Lack]], _$V$-cat is locally presentable or locally bounded if $V$ is so_ TAC (2001)
 {#KellyLack}

See also:

* [[Max Kelly]], _Basic concepts of enriched category theory_.

* [[Peter Freyd]], [[Max Kelly]], _Categories of continuous functors_ J. Pure. Appl. Algebra 2 (1972) 169-191.
 {#FreyKelly}
* [[Jírí Adámek]], [[Horst Herrlich]], [[Jírí Rosickỳ]], [[Walter Tholen]], _On a generalized small-object argument for the injective subcategory problem_. Cah. Topol. G&#233;om. Diff&#233;r. Cat&#233;g 43 (2002) 83&#8211;106.
{#AHRT}


[[!redirects locally bounded categories]]
