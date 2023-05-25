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

## Idea

In [[set theory]], there are two notions of [[subsets]]

* In [[material set theory]], a subset of a set $A$ is a set $B$ with the property that for all $x$, if $x \in B$, then $x \in A$, which by the definition of [[power set]] in [[material set theory]], is the same thing as an element $B \in \mathcal{P}(A)$. 

* In [[structural set theory]], a subset of a set $A$ is a set $B$ with an [[injection]] $i:B \hookrightarrow A$. 

In [[dependent type theory]], a similar distinction can be made between the two notions of subtypes, resulting in *material subtypes* and *structural subtypes*. 

## Definition ##

### Material subtypes

Let $(\Omega, \mathrm{El}_\Omega)$ denote the [[type of all propositions]] and its type reflector type family. Let $T$ be a type. 

\begin{definition}
The **power set** of a type $A$ is defined as the function type from $A$ to the type of all propositions $\Omega$, $\mathcal{P}(A) \coloneqq A \to \Omega$. 
\end{definition}

The power set of a type $A$ is always a set because its [[codomain]], the type of all propositions $\Omega$, is a set due to the [[univalence axiom]] or [[propositional extensionality]]. 

\begin{definition}
A **material subtype** on $A$ is an element of the power set $B:\mathcal{P}(A)$. 
\end{definition}

\begin{definition}
The **local membership relation** $x \in_A B$ between elements $x:A$ and material subtypes $B:\mathcal{P}(A)$ is defined as 
$$x \in_A B \coloneqq \mathrm{El}_\Omega(B(x))$$
\end{definition}

### Structural subtypes

\begin{definition}
A **structural subtype** of $A$ is a type $B$ with an embedding $i:B \hookrightarrow A$. $A$ is a **supertype** of $B$. 
\end{definition}

### Comparison between material subtypes, structural subtypes, and predicates

In the [[inference rules]] for the [[type of all propositions]], one has an operation $(-)_\Omega$ which takes a proposition $P$ and turns it into an element of the [[type of all propositions]] $P_\Omega:\Omega$. 

| material subtype | predicate | structural subtype |
|-|-|-|
| $B:\mathcal{P}(A)$ | $x:A \vdash x \in_A B \coloneqq \mathrm{El}_\Omega(B(x))$ | $\sum_{x:A} x \in_A B$ |
| $\lambda x:A.(B(x))_\Omega:\mathcal{P}(A)$ | $x:A \vdash B(x) \qquad x:A \vdash p(x):\mathrm{isProp}(B(x))$ | $\sum_{x:A} B(x)$ |
| $\lambda x:A.\left(\sum_{y:B} i(y) =_A x\right)_\Omega:\mathcal{P}(A)$ | $x:A \vdash \sum_{y:B} i(y) =_A x$ | $B \qquad i:B \hookrightarrow A$ |

## Operations on material and structural subtypes

### Material subtypes

\begin{definition}
Given a type $A$, the **[[improper subset|improper]] material subtype** on $A$ is the material subtype $\Im_A:\mathcal{P}(A)$ such that for all elements $x:A$, $x \in_A \Im_A$ is [[contractible type|contractible]]. 
\end{definition}

\begin{definition}
Given a type $A$, there is a binary operation $(-)\cap(-):\mathcal{P}(A) \times \mathcal{P}(A) \to \mathcal{P}(A)$ on the power set of $A$ called the **[[intersection]]**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $B \cap C$ is defined as
$$(B \cap C)(x) \coloneqq ((x \in_A B) \times (x \in_A C))_\Omega$$
for all $x:A$.
\end{definition}

\begin{definition}
Given a type $A$ and a type $I$, there is an function $\bigcap:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the **$I$-indexed [[intersection]]**, such that for all families of material subtypes $B:I \to \mathcal{P}(A)$, $\bigcap_{i:I} B(i)$ is defined as
$$\left(\bigcap_{i:I} B(i)\right)(x) \coloneqq \left(\prod_{i:I} x \in_A B(i)\right)_\Omega$$
for all $x:A$. 
\end{definition}

\begin{definition}
Given a type $A$, the **empty material subtype** on $A$ is the material subtype $\emptyset_A:\mathcal{P}(A)$ such that for all elements $x:A$, $x \in_A \emptyset_A$ [[equivalence of types|is equivalent to]] the [[empty type]]. 
\end{definition}

\begin{definition}
Given a type $A$, there is a binary operation $(-)\cup(-):\mathcal{P}(A) \times \mathcal{P}(A) \to \mathcal{P}(A)$ on the power set of $A$ called the **[[union]]**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $B \cup C$ is defined as
$$(B \cup C)(x) \coloneqq ((x \in_A B) \vee (x \in_A C))_\Omega$$
for all $x:A$, where $A \vee B \coloneqq [A + B]$ is the [[disjunction]] of two [[types]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

\begin{definition}
Given a type $A$ and a type $I$, there is an function $\bigcup:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the **$I$-indexed [[union]]**, such that for all families of material subtypes $B:I \to \mathcal{P}(A)$, $\bigcup_{i:I} B(i)$ is defined as
$$\left(\bigcup_{i:I} B(i)\right)(x) \coloneqq (\exists i:I.x \in_A B(i))_\Omega$$
for all $x:A$, where 
$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$ 
is the [[existential quantification]] of a [[type family]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

### Structural subtypes

\begin{definition}
Given a type $T$, $T$ is the **improper structural subtype**, with embedding given by the identity function on $T$. 
\end{definition}

\begin{definition}
Given a type $T$ and structural subtypes $R$ and $S$ with embeddings $i_R:R \hookrightarrow T$ and $i_S:S \hookrightarrow T$, the **intersection** of $R$ and $S$ is the dependent sum type
$$R \cap S \coloneqq \sum_{r:R} \sum_{s:S} i_R(r) =_T i_S(s)$$
\end{definition}

\begin{definition}
Given a type $T$, the [[empty type]] is the **empty structural subtype**, with embedding given by any function from the empty type to $T$. 
\end{definition}

\begin{definition}
Given a type $T$ and structural subtypes $R$ and $S$ with embeddings $i_R:R \hookrightarrow T$ and $i_S:S \hookrightarrow T$, the **[[union]]** of $R$ and $S$ is the [[pushout type]] 
$$R \cup S \coloneqq R \sqcup^{R \cap S}_{\pi_1 ; \pi_1' \circ \pi_2} S$$
where $\pi_1$ and $\pi_2$ are the first and second projection functions for the first dependent sum type and $\pi_1'$ is the first projection function for the second dependent sum type for the intersection as defined above ($\sum_{r:R} \sum_{s:S} i_R(r) =_T i_S(s)$)
\end{definition}

## See also ##

* [[subobject]]

* [[embedding]], [[embedding type]]

* [[n-monomorphism]]

* [[coercion]]

[[!redirects subtype]]
[[!redirects subtypes]]
[[!redirects subtyping]]

[[!redirects material subtype]]
[[!redirects material subtypes]]

[[!redirects structural subtype]]
[[!redirects structural subtypes]]

[[!redirects supertype]]
[[!redirects supertypes]]

[[!redirects type of subtypes]]