
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
 {#Idea}

In [[type theory]], the notion of *subtypes* is the analog of *[[subsets]]* in [[set theory]].

In the presence of a [[type universe]] [[Prop|$Prop$]] of [[propositions]] (alternatively denoted "$\Omega$"), the subtypes of a given $A \colon Type$ may be simply be identified with the [[function type]] from $A$ to $Prop$:

$$
  Sub(A)
  \;\;
  =
  \;\;
  Prop_A
  \;\;
  \equiv
  \;\;
  A \to Prop
  \;\;
  \equiv
  \;\;
  A \to \Omega
  \,.
$$

In [[topos theory|topos]]-[[categorical semantics of dependent type theory|semantics]], $Prop$ is interpreted as the *[[subobject classifier]]* and subtypes as *[[subobjects]]*.

Notice that with $Prop$ itself being a subtype of a [[type universe]] $Type$, the subtypes of $A$ are thus a special case of the $A$-[[dependent types]]

$$
  Type_A 
  \;\;
  \equiv
  \;\;
  A \to Type
  \,,
$$

namely those whose [[fiber type]] over $a \colon A$ is the proposition asserting that "$a$ is contained in the subtype".

This is equivalent to other definitions of subtypes, which one can make sense of also in the absence of a Prop-universe.

Notice here that in [[set theory]], there are in fact two notions of [[subsets]]:

* In [[material set theory]], a subset of a set $A$ is a set $B$ with the property that for all $x$, if $x \in B$, then $x \in A$, which by the definition of [[power set]] in [[material set theory]], is the same thing as an element $B \in \mathcal{P}(A)$. 

* In [[structural set theory]], a subset of a set $A$ is a set $B$ with an [[injection]] $i \colon B \hookrightarrow A$. 

In [[dependent type theory]], a similar distinction can be made between the two notions of subtypes, resulting in *material subtypes* and *structural subtypes*. 

## Definition ##

### Material subtypes

We work with a [[Russell type of all propositions]] $\Omega$. 

\begin{definition}
The **[[power set]]** of a type $A$ is defined as the function type from $A$ to the Russell type of all propositions $\Omega$, $\mathcal{P}(A) \coloneqq A \to \Omega$. 
\end{definition}

The power set of a type $A$ is always a set because its [[codomain]], the Russell type of all propositions $\Omega$, is a set due to the [[univalence axiom]] or [[propositional extensionality]]. 

\begin{definition}
A **material subtype** on $A$ is an element of the power set $B:\mathcal{P}(A)$. 
\end{definition}

\begin{definition}
The **local membership relation** $x \in_A B$ between elements $x:A$ and material subtypes $B:\mathcal{P}(A)$ is defined as 
$$x \in_A B \coloneqq B(x)$$
\end{definition}

### Structural subtypes

\begin{definition}
A **structural subtype** of $A$ is a type $B$ with an embedding $i:B \hookrightarrow A$. $A$ is a **supertype** of $B$. 
\end{definition}

### Comparison between material subtypes, structural subtypes, and predicates

| material subtype | predicate | structural subtype |
|-|-|-|
| $B:\mathcal{P}(A)$ | $x:A \vdash x \in_A B \coloneqq B(x)$ | $\sum_{x:A} x \in_A B$ |
| $\lambda x:A.B(x):\mathcal{P}(A)$ | $x:A \vdash B(x) \qquad x:A \vdash p(x):\mathrm{isProp}(B(x))$ | $\sum_{x:A} B(x)$ |
| $\left(\lambda x:A.\sum_{y:B} i(y) =_A x\right):\mathcal{P}(A)$ | $x:A \vdash \sum_{y:B} i(y) =_A x$ | $B \qquad i:B \hookrightarrow A$ |

## Operations on material and structural subtypes

### Material subtypes

\begin{definition}
Given a type $A$, the **[[improper subset|improper]] material subtype** on $A$ is the material subtype $\Im_A:\mathcal{P}(A)$ such that for all elements $x:A$, $x \in_A \Im_A$ is [[contractible type|contractible]]. 
\end{definition}

\begin{definition}
Given a type $A$, there is a binary operation $(-)\cap(-):\mathcal{P}(A) \times \mathcal{P}(A) \to \mathcal{P}(A)$ on the power set of $A$ called the **[[intersection]]**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $B \cap C$ is defined as
$$(B \cap C)(x) \coloneqq (x \in_A B) \wedge (x \in_A C)$$
for all $x:A$, where $A \wedge B \coloneqq [A \times B]$ is the [[disjunction]] of two [[types]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

\begin{definition}
Given a type $A$ and a type $I$, there is an function $\bigcap:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the **$I$-indexed [[intersection]]**, such that for all families of material subtypes $B:I \to \mathcal{P}(A)$, $\bigcap_{i:I} B(i)$ is defined as
$$\left(\bigcap_{i:I} B(i)\right)(x) \coloneqq \forall i:I.x \in_A B(i)$$
for all $x:A$, where 
$$\forall x:A.B(x) \coloneqq \left[\prod_{x:A} B(x)\right]$$ 
is the [[universal quantification]] of a [[type family]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

\begin{definition}
Given a type $A$, the **empty material subtype** on $A$ is the material subtype $\emptyset_A:\mathcal{P}(A)$ such that for all elements $x:A$, $x \in_A \emptyset_A$ [[equivalence of types|is equivalent to]] the [[empty type]]. 
\end{definition}

\begin{definition}
Given a type $A$, there is a binary operation $(-)\cup(-):\mathcal{P}(A) \times \mathcal{P}(A) \to \mathcal{P}(A)$ on the power set of $A$ called the **[[union]]**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $B \cup C$ is defined as
$$(B \cup C)(x) \coloneqq (x \in_A B) \vee (x \in_A C)$$
for all $x:A$, where $A \vee B \coloneqq [A + B]$ is the [[disjunction]] of two [[types]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

\begin{definition}
Given a type $A$ and a type $I$, there is an function $\bigcup:(I \to \mathcal{P}(A)) \to \mathcal{P}(A)$ called the **$I$-indexed [[union]]**, such that for all families of material subtypes $B:I \to \mathcal{P}(A)$, $\bigcup_{i:I} B(i)$ is defined as
$$\left(\bigcup_{i:I} B(i)\right)(x) \coloneqq \exists i:I.x \in_A B(i)$$
for all $x:A$, where 
$$\exists x:A.B(x) \coloneqq \left[\sum_{x:A} B(x)\right]$$ 
is the [[existential quantification]] of a [[type family]] and $[T]$ is the propositional truncation of $T$. 
\end{definition}

\begin{definition}
Given a type $A$, there is a binary relation $B:\mathcal{P}(A), C:\mathcal{P}(A) \vdash B \subseteq_A C$ on the power set of $A$ called the **subtype inclusion relation**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $B \subseteq_A C$ is defined as
$$B \subseteq_A C \coloneqq \prod_{x:A} (x \in_A B) \to (x \in_A C)$$
\end{definition}

\begin{definition}
Given a type $A$, there is a binary relation $B:\mathcal{P}(A), C:\mathcal{P}(A) \vdash \mathrm{Eq}_A(B, C)$ on the power set of $A$ called **observational equality**, such that for all material subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, $\mathrm{Eq}_{\mathcal{P}(A)}(B, C)$ is defined as
$$\mathrm{Eq}_{\mathcal{P}(A)}(B, C) \coloneqq \prod_{x:A} (x \in_A B) \simeq (x \in_A C)$$
\end{definition}

\begin{proposition}
**[[Axiom of extensionality]]**: Given a type $A$, for all subtypes $B:\mathcal{P}(A)$ and $C:\mathcal{P}(A)$, there is an equivalence of types between $B =_{\mathcal{P}(A)} C$ and $\mathrm{Eq}_{\mathcal{P}(A)}(B, C)$. 
\end{proposition}

\begin{proof}
For all $x:A$ and $B:\mathcal{P}(A)$, since $x \in_A B$ is propositions, by the introduction rules of the [[Russell type of all propositions]], $x \in_A B:\Omega$. The [[univalence axiom]] for $\Omega$ states that $(x \in_A B) \simeq (x \in_A C)$ is equivalent to $(x \in_A B) =_\Omega (x \in_A C)$. Thus, $\mathrm{Eq}_{\mathcal{P}(A)}(B, C)$ is equivalent to $\prod_{x:A} (x \in_A B) =_\Omega (x \in_A C)$. But by [[function extensionality]], there is an equivalence of types between $B =_{\mathcal{P}(A)} C$ and $\prod_{x:A} (x \in_A B) =_\Omega (x \in_A C)$; hence there is an equivalence of types between $B =_{\mathcal{P}(A)} C$ and $\mathrm{Eq}_{\mathcal{P}(A)}(B, C)$. 
\end{proof}

\begin{definition}
Given a type $A$, a **singleton subtype** on $A$ is a material subtype $S:\mathcal{P}(A)$ such that [[uniqueness quantifier|there exists a unique]] $x:A$ such that $x \in S$: 
$$\mathrm{isSingleton}(S) \coloneqq \exists!x:A.x \in S$$
\end{definition}

\begin{definition}
Given a type $T$, there is a binary function $(-) \times (-):\mathcal{P}(T) \times \mathcal{P}(T) \to \mathcal{P}(T \times T)$ called the **[[cartesian product]] of subtypes**, defined by 
$$(A \times B)(a, b) \coloneqq (a \in_T A) \wedge (b \in_T B)$$
for all elements $a:T$, $b:T$ and subtypes $A:\mathcal{P}(T)$ and $B:\mathcal{P}(T)$. 
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

\begin{definition}
Given a type $T$ and structural subtypes $R$ and $S$ with embeddings $i_R:R \hookrightarrow T$ and $i_S:S \hookrightarrow T$, the **[[cartesian product]]** of $R$ and $S$ is simply the [[product]] $R \times S$. The associated [[embedding]] $i_{R \times S}:(R \times S) \hookrightarrow (T \times T)$ is defined by 
$$i_{R \times S}(a) \coloneqq (i_R(\pi_1(a)), i_S(\pi_2(a)))$$
for all $a:R \times S$, where $\pi_1$ and $\pi_2$ are the first and second product projection functions defined in the [[inference rules]] of the negative [[product type]] $R \times S$. 
\end{definition}

## Decidable subtypes

Given a Russell type of propositions, a [[subtype]] $P:A \to \mathrm{Prop}$ is a **decidable subtype** if for all $x:A$, $P(x)$ satisfies the [[law of excluded middle]]

$$\mathrm{isDecidable}(P) \equiv \prod_{x:A} P(x) \vee \neg P(x)$$

Similarly, given a Tarski type of propositions, a [[subtype]] $P:A \to \mathrm{Prop}$ is a **decidable subtype** if for all $x:A$, $P(x)$ satisfies the [[law of excluded middle]]

$$\mathrm{isDecidable}(P) \equiv \prod_{x:A} \mathrm{El}(P(x) \vee \neg P(x))$$

For all types $A$, there exists an equivalence between the type of decidable subtypes of $A$ and the type of [[boolean-valued functions]] of $A$

$$\mathrm{toDecidSub}:\left(A \to \mathrm{Bool}\right) \simeq \left(\sum_{P:A \to \mathrm{Prop}} \mathrm{isDecidable}(P)\right)$$ 

The membership relation of decidable subsets is defined by whether the boolean-valued function evaluations is true

$$x \in P \coloneqq \mathrm{toDecidSub}^{-1}(P)(x) =_\mathrm{true}$$

Decidable subtypes are closed under the empty subtype, the improper subtype, and unions with a disjoint singleton subtype:

The empty subtype and improper subtype are given by 

$$\emptyset_A \coloneqq \mathrm{toDecidSub}(\lambda x:A.\mathrm{false}) \qquad \im_A \coloneqq \mathrm{toDecidSub}(\lambda x:A.\mathrm{true})$$

Singleton subtypes correspond to boolean-valued functions for which [[uniqueness quantifier|there exists a unique]] $x:A$ such that $f(x)$ is true, and is given by 

$$\sum_{f:A \to \mathrm{bool}} \exists!x:A.f(x) =_\mathrm{bool} \mathrm{true}$$

Unions of decidable subtypes correspond to lambda abstraction of the disjunction of boolean-valued function evaluations 

$$P \cup Q \coloneqq \mathrm{toDecidSub}(\lambda x:A.\mathrm{toDecidSub}^{-1}(P)(x) \vee \mathrm{toDecidSub}^{-1}(Q)(x))$$

and intersections of decidable subtypes correspond to lambda abstraction of the conjunction of boolean-valued function evaluations 

$$P \cap Q \coloneqq \mathrm{toDecidSub}(\lambda x:A.\mathrm{toDecidSub}^{-1}(P)(x) \wedge \mathrm{toDecidSub}^{-1}(Q)(x))$$

Two decidable subtypes are disjoint if their intersection is the empty subtype. 

## See also ##

* [[subobject]]

* [[embedding]], [[embedding type]]

* [[n-monomorphism]]

* [[coercion]]

* [[decidable subtype]]



## References
 {#References}

* {#HofmannPierce96} [[Martin Hofmann]], [[Benjamin Pierce]], *Positive Subtyping*, Information and Computation **126** 1 (1996) 11-33 &lbrack;[doi:10.1006/inco.1996.0031](https://doi.org/10.1006/inco.1996.0031)&rbrack;
  
  > (including early discussion of [[lenses in computer science]])

* [[Univalent Foundations Project]], [p. 111](https://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf#page=123) of: _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke19} [[Egbert Rijke]], §12.2 in: _[[Introduction to Homotopy Type Theory]]_ (2019)  &lbrack;[web](http://www.andrew.cmu.edu/user/erijke/hott/), [pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [GitHub](https://github.com/EgbertRijke/HoTT-Intro)&rbrack; 

* [[Martín Escardó]], *[The subtype classifier and other classifiers](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html#subtypeclassifier)*, in:  *Introduction to Univalent Foundations of Mathematics with Agda* &lbrack;[arXiv:1911.00580](https://arxiv.org/abs/1911.00580),  [webpage](https://www.cs.bham.ac.uk/~mhe/HoTT-UF-in-Agda-Lecture-Notes/HoTT-UF-Agda.html)&rbrack;

* [[Felix Cherubini]], [[Thierry Coquand]], [[Matthias Hutzler]], *A Foundation for Synthetic Algebraic Geometry* (2023) &lbrack;[arXiv:2307.00073](https://arxiv.org/abs/2307.00073)&rbrack;

  > (in the context of [[synthetic algebraic geometry]])

In [[Agda]]:

* [[UniMath project]], *[foundation-core.subtypes.html](https://unimath.github.io/agda-unimath/foundation-core.subtypes.html)*

* [[Ettore Aldrovandi]], *[Subtypes](https://www.math.fsu.edu/~ealdrov/teaching/2020-21/fall/MAS5932/agda/more-logic.html#subtypes)*, §4 in: *Propositions, Sets and Logic--Ⅱ* &lbrack;[web](https://www.math.fsu.edu/~ealdrov/teaching/2020-21/fall/MAS5932/agda/more-logic.html)&rbrack;

In [[Lean]]:

* [[Kyle Miller]], [pp. 22](https://math.berkeley.edu/~kmill/talks/2020-06-26-lean-seminar.pdf#page=22) in: *Doing math the Lean way*, Berkeley Lean Seminar (2020) &lbrack;[pdf](https://math.berkeley.edu/~kmill/talks/2020-06-26-lean-seminar.pdf#page=22), [[Miller-MathTheLeanWay.pdf:file]]&rbrack;


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

[[!redirects decidable subtype]]
[[!redirects decidable subtypes]]