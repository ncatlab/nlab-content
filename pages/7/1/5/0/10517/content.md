
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Universes
+-- {: .hide}
[[!include universe - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

A [[partial function]] $f \colon A\rightharpoonup B$ between two [[sets]] can be turned into a [[total function]] $\overline{f} \colon A\to B_\bot$ by adjoining a further [[element]] $\bot$ to $B$ and sending all $a\in A$ that are not in the [[domain]] of definition of $f$ to this new value $\bot$ = "undefined" and the rest just to their value under $f$. Conversely, every function with codomain $B_\bot$ corresponds to a unique partial function to $B$ whence $B_\bot$ is a 'classifying object' for these.

More generally, a **partial function classifier** or **partial map classifier** of an [[object]] $B$ in a [[category]] $\mathcal{C}$ is a [[representing object]] for [[partial maps]] with [[codomain]] $B$.

## Definition

Let $\mathcal{C}$ be a category with [[pullbacks]].  Recall that a **partial map** $A \rightharpoonup B$ in $\mathcal{C}$ is a [[span]] $A \leftarrow D \to B$ in which the map $D\to A$ is a [[monomorphism]].  The subobject $D \hookrightarrow A$ is called the [[domain]] of the partial map.  Two partial maps are considered *equal* if they are related by an isomorphism of spans; in this way we obtain a [[set]] of partial maps $Par_{\mathcal{C}}(A,B)$.

We can compose a partial map $A\rightharpoonup B$ with a map $B\to B'$ in an obvious way.  We can also compose it with a map $A'\to A$ by pulling back the mono $D\hookrightarrow A$ to $A'$.  In this way $Par_{\mathcal{C}}(-,-)$ becomes a [[profunctor]] from $\mathcal{C}$ to itself.  (In fact, it is the hom-set of another category with the same objects as $\mathcal{C}$.)

A **partial map classifier** for $B$ is an object $B_\bot$ together with an isomorphism
$$ \mathcal{C}(A,B_\bot) \cong Par_{\mathcal{C}}(A,B) $$
natural in $A$.  By the [[Yoneda lemma]] this means there is a universal partial map $B_\bot \rightharpoonup B$.

This can be unpacked into the following condition:

+-- {: .num_prop}
###### Proposition

A partial map classifier for $B$ is uniquely determined by a map $B \to B_\bot$ with the property that, for every partial map $A\rightharpoonup B$ depicted below, there is a unique $A \to B_\bot$ making a pullback square

\begin{tikzcd}
D \arrow[d, hook] \arrow[r]  & B \arrow[d]
\\ A \arrow[r, dotted] & B_\bot
\end{tikzcd}

=--

+-- {: .proof}
###### Proof

For any monomorphism $B \to B_\bot$, there is a natural transformation $\mathcal{C}(-,B_\bot) \to Par_{\mathcal{C}}(-,B)$ given by forming pullbacks along $B \to B_\bot$. It is a natural bijection iff it satisfies the condition of the proposition.

If $B \to B_\bot$ satisfies the condition of the proposition, then it is a monomorphism, by considering the (total) partial map $\id_B$.

=--

The existence of partial map classifiers $B_\bot$ for all objects $B$ in $\mathcal{C}$ amounts to the existence of a right adjoint for the inclusion $\mathcal{C}\hookrightarrow Par(\mathcal{C})$ where the latter is the usual category of partial maps of $\mathcal{C}$.

## Constructions

In a [[Boolean category|Boolean]] [[extensive category]] (such as a [[Boolean topos]]), we can define the partial map classifier as $B_\bot = B + 1$, where $1$ is the [[terminal object]].  This is because in an extensive category, a map $A\to B+1$ is equivalent to a decomposition of $A$ as a [[coproduct]] $D+E$ together with a map $D\to B$ (the map $E\to 1$ being unique), and in a Boolean category every subobject of $A$ is complemented and hence induces such a coproduct decomposition.  The universal partial map $B+1 \rightharpoonup B$ has domain the summand $B$, on which it is the identity.  Note that $B\mapsto B+1$ is also known as the [[maybe monad]].

Partial map classifiers also exist in every [[elementary topos]], but in the non-Boolean case they are harder to construct. Letting $t : 1 \to \Omega$ denote the top element, the [[dependent product]] $t_*(B)$ is precisely the map $B_\bot \to \Omega$ classifying $B \subseteq B_\bot$. To wit, with this definition,

$$
  \begin{aligned}
    \mathcal{C}(A, B_\bot)
    &\cong \coprod_{p : A \to \Omega} \mathcal{C}/\Omega(p, t_*(B))
    \\&\cong \coprod_{p : A \to \Omega} \mathcal{C}(t^*(p), B)
    \\&\cong \coprod_{A' \subseteq A} \mathcal{C}(A', B)
    \\&\cong Par_{\mathcal{C}}(A, B)
  \end{aligned}
$$

Alternatively, in the [[internal logic]], two ways of defining $B_\bot$ that more closely follow the classical construction are:

*  $B_\bot$ is a [[subobject]] of the [[power object]] $\mathcal{P}B$ consisting of the [[subsingleton]] subobjects of $B$.  In this case, the universal partial map $B_\bot \rightharpoonup B$ has domain the set of [[singleton]] subobjects of $B$, on which it is an isomorphism.

*  $B_\bot$ is the object of partial maps $1 \rightharpoonup B$.  In this case, the universal partial map $B_\bot \rightharpoonup B$ has domain the set of partial maps which are total, on which it is an isomorphism.

Note that neither of these constructions is [[predicative mathematics|predicative]].  The second makes more sense in a [[higher category]] (or in its internal logic such as [[homotopy type theory]]).

+-- {: .num_remark}
###### Remark

In an [[constructive mathematics|intuitionistic context]], $B + 1$ still classifies something: namely partial maps $A \rightharpoonup B$ whose domain of definition is a [[decidable subset|decidable subobject]] of $A$.

In [[type theory]] one uses the partiality [monad](monad+%28in+computer+science%29) to treat general recursion as an algebraic effect. In this we we obtain a classifier for recursively enumerable subsets. Is [this](http://www.cs.ox.ac.uk/ralf.hinze/WG2.8/22/slides/tarmo.pdf) the first appearance?
It is clear that this idea can be generalized to other classes of propositions.
=--

## Relative partial maps

Given objects $p : X \to S$ and $q : Y \to S$ of $\mathcal{C}/S$, a partial map from $p$ to $q$ can be described as a commutative diagram in $\mathcal{C}$.

\begin{tikzcd}
  A \arrow[r] \arrow[d, hook] & Y \arrow[d, "q"]
  \\ X \arrow[r, "p"] & S
\end{tikzcd}

A partial map classifier $Opt_S(q)$ for $q$ in $\mathcal{C}/S$ can be described as a representing object for the presheaf on $\mathcal{C}$ sending $X$ to the set of diagrams of this form (modulo choice of representatives for subobjects), together with its structure map $Opt_S(q) \to S$, which represents the natural transformation sending this diagram to $p \in \mathcal{C}(X, S)$.

+-- {: .num_prop}
###### Proposition

If $\mathcal{C}$ is a topos and $p : X \to S$ is an object of $\mathcal{C}/S$, there is a pullback in $\mathcal{C}$

\begin{tikzcd}
  \mathrm{Opt}_S(q) \arrow[r] \arrow[d] & X_\bot \arrow[d, "p"]
  \\ S \times \Omega \arrow[r] & S_\bot
\end{tikzcd}

where $Opt_S(q) \to X_\bot$ corresponds to forgetting the base of a relative partial map, and $Opt_S(q) \to S$ is the structure map, and $Opt_S(q) \to \Omega$ corresponds to giving the domain of definition.

=--

+-- {: .proof}
###### Proof

Let $A$ be an object of $\mathcal{C}$. It suffices to show this square is a pullback after applying $\mathcal{C}(A, -)$ and the isomorphism to the presheaves these objects represent.

An object of the pullback can be described as an arrow $A \to S$, a subobject $B \hookrightarrow A$, and a partial map $A \hookleftarrow B' \to X$ with the property that the induced partial maps $A \hookleftarrow B \to S$ and $A \hookleftarrow B' \to S$ are the same partial map (up to choice of representative for the subobject).

This is bijective with the set of commutative diagrams of the form

\begin{tikzcd}
B \arrow[r] \arrow[d, hook] & X \arrow[d, "q"]
\\ A \arrow[r] & S
\end{tikzcd}

and the projection to $\mathcal{C}(A, S)$ takes the bottom horizontal arrow.

=--

## Properties

* In a [[topos]], the partial map classifier $B_\bot$ of $B$ is [[injective object|injective]]. The canonical embedding $B\rightarrowtail B_\bot$ shows accordingly that a topos _has enough injectives_!

* In a topos, the [[subobject classifier]] $true:1\rightarrow\Omega$ coincides with the monomorphism $\eta_1:1\rightarrowtail 1_\bot$.

* In a topos, the assignment of $B_\bot$ to $B$ is functorial.


## References 
 {#References}

* [[Francis Borceux]], sec.5.5 in: *[[Handbook of Categorical Algebra]]* vol. 3, Cambridge UP (1994) 


* [[Peter Johnstone]], Section 1.2 of: _Topos theory_, London Math. Soc. Monographs __10__, Acad. Press 1977, xxiii+367 pp. (Dover reprint 2014)

* [[Peter Johnstone]], Section A2.4 in: *[[Sketches of an Elephant]]*

For related topics in [[homotopy type theory]]:

* [[Thorsten Altenkirch]], [[Nils Anders Danielsson]], [[Nicolai Kraus]], *Partiality, Revisited: The Partiality Monad as a Quotient Inductive-Inductive Type* &lbrack;[abs:1610.09254](https://arxiv.org/abs/1610.09254)&rbrack;

* [[Martín Escardó]], Cory Knapp, *Partial Elements and Recursion via Dominances in Univalent Type Theory* &lbrack;[doi:10.4230/LIPIcs.CSL.2017.21](https://doi.org/10.4230/LIPIcs.CSL.2017.21)&rbrack;

* {#PS25} [[Leoni Pugh]], [[Jonathan Sterling]], *When is the partial map classifier a Sierpiński cone?* ([arXiv:2504.06789](https://arxiv.org/abs/2504.06789))

Discussion for [[topological spaces]]:

* {#MaySigurdsson06} [[Peter May]], [[Johann Sigurdsson]], Def. 1.3.6 in: _[[Parametrized Homotopy Theory]]_,  Mathematical Surveys and Monographs, vol. 132, AMS 2006   ([ISBN:978-0-8218-3922-5](https://bookstore.ams.org/surv-132), [arXiv:math/0411656](https://arxiv.org/abs/math/0411656), [pdf](http://www.math.uchicago.edu/~may/EXTHEORY/MaySig.pdf))


[[!redirects partial function classifier]]
[[!redirects partial function classifiers]]

[[!redirects partial map classifier]]
[[!redirects partial map classifiers]]