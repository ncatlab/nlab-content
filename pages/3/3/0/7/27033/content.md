
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

+-- {: .standout}
This page is currently under heavy revision. There are many errors on this page that need to be fixed. 
=--

## Definition

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] on the [[natural numbers]] is again decidable.  That is,
$$ (\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in \mathbb{N}, P(x)) \vee \neg(\exists x \in \mathbb{N}, P(x)) ,$$
or equivalently
$$ (\forall x \in \mathbb{N}, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in \mathbb{N}, P(x)) \vee (\forall x \in \mathbb{N}, \neg{P(x)}) .$$

We can also state the principle set-theoretically. The __limited principle of omniscience__ ($LPO$) states that given a [[subset]] $P \in \mathcal{P}(\mathbb{N})$ of the [[natural numbers]] $\mathbb{N}$, if $P$ is a [[decidable subset]] of $\mathbb{N}$ ($P \cup \bar{P} = \mathbb{N}$), then either $P$ is [[inhabited subset|inhabited]] or $\bar{P} = \mathbb{N}$, where $\bar{P}$ is the [[complement]] of $P$. 

One can equivalently use functions to the [[boolean domain]] instead of [[decidable subsets]]. The __limited principle of omniscience__ states that given any [[function]] $f$ from the [[natural numbers]] $\mathbb{N}$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. In this case, the limited principle of omniscience is also called **[[excluded middle]] for [[semidecidable truth values]]**, i.e. [[truth values]] of the form $\exists n, f(n) = 1$ for some [[boolean]]-valued [[sequence]] $f:\mathbb{N}\to \mathbf{2}$, or **$\Sigma^0_1$-[[excluded middle]]** ([Diener 2018](#Diener18), [Kawai 2018](#Kawai18)) in the sense of the [[arithmetical hierarchy]] in [[computability theory]]. 

One can also formulate the limited principle of omniscience for natural numbers in terms of [[streams]] of [[booleans]] instead of the [[function set]] $\mathbb{2}^\mathbb{N}$. Let $\mathrm{Stream}(A)$ be the set of streams of the set $A$, with head function $h:\mathrm{Stream}(A) \to A$ and tail function $t:\mathrm{Stream}(A) \to \mathrm{Stream}(A)$. Streams and sequences of any set $A$ are interdefinable with each other: given a stream $f \in \mathrm{Stream}(A)$, the sequence is given by $(h(t^n(f)))_{n \in \mathbb{N}}$, where $t^n$ is the $n$-th functional power of the tail function $t$, and the head and tail functions for the sequence set $A^\mathbb{N}$ are given by $f \mapsto f(0)$ and $f \mapsto (f(n + 1))_{n \in \mathbb{N}}$ respectively. Then the limited principle of omniscience state that given a stream $f \in \mathrm{Stream}(\mathbb{2})$ of booleans, either there exists $n \in \mathbb{N}$ such that $h(t^n(f)) = 1$ or for all $n \in \mathbb{N}$, $h(t^n(f)) = 0$. 

### In the antithesis interpretation

In the [[antithesis interpretation]] of constructive mathematics, propositions are functions from from the [[boolean domain]] $\{0,1\}$ to the [[set of truth values]] $\Omega$. Given any [[set]] $\mathbb{N}$ and [[function]] $f$ from $\mathbb{N}$ to $\{0,1\}$, the antithesis proposition $b \mapsto f(x) = b$ is [[mutually exclusive propositions|mutually exclusive]] and [[decidable proposition|decidable]] by the [[induction principle]] of the [[boolean domain]]. As a result, the [[affine logic|affine]] [[existential quantifier]] $\bigsqcup_{x \in \mathbb{N}} (b \mapsto f(x) = b)$ is mutually exclusive and affirmative and the the [[affine logic|affine]] [[universal quantifier]] $\bigsqcap_{x \in \mathbb{N}} (b \mapsto f(x) = b)$ is mutually exclusive and refutative. The __limited principle of omniscience__ ($LPO$) states that, given any [[function]] $f$ from $\mathbb{N}$ to the [[boolean domain]] $\{0,1\}$, $\bigsqcup_{x \in \mathbb{N}} (b \mapsto f(x) = b)$ or $\bigsqcap_{x \in \mathbb{N}} (b \mapsto f(x) = b)$ is decidable. 

### Using exclusive disjunction

There is an equivalent version of the limited principle of omniscience which uses the [[exclusive disjunction]] instead of the inclusive [[disjunction]] for the definition of a [[decidable proposition]]:

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] on the natural numbers is again decidable.  That is,
$$ (\forall x \in \mathbb{N}, P(x) \underline{\vee} \neg{P(x)}) \Rightarrow (\exists x \in \mathbb{N}, P(x)) \underline{\vee} \neg(\exists x \in \mathbb{N}, P(x)) ,$$
or equivalently
$$ (\forall x \in \mathbb{N}, P(x) \underline{\vee} \neg{P(x)}) \Rightarrow (\exists x \in \mathbb{N}, P(x)) \underline{\vee} (\forall x \in \mathbb{N}, \neg{P(x)}) .$$

We can also state the principle set-theoretically: the __limited principle of omniscience__ ($LPO$) states that, given any [[function]] $f$ from the [[natural numbers]] $\mathbb{N}$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. That is, 
$$ \forall f \in \{0,1\}^\mathbb{N}, (\exists x \in \mathbb{N}, f(x) = 1) \underline{\vee} \neg(\exists x \in \mathbb{N}, f(x) = 1) ,$$
or equivalently
$$ \forall f \in \{0,1\}^\mathbb{N}, (\exists x \in \mathbb{N}, f(x) = 1) \underline{\vee} (\forall x \in \mathbb{N}, f(x) = 0) .$$

## Equivalent statements

There are various results that are equivalent to the limited principle of omniscience. 

\begin{theorem}
LPO holds if and only if the [[function set]] $\mathbb{2}^\mathbb{N}$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{2}^\mathbb{N}$ be defined as 

$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$
\end{theorem}

\begin{proof}
Since the [[boolean domain]] is a [[boolean ring]], the function set $\mathbb{2}^\mathbb{N}$ is also a [[boolean ring]] via pointwise addition, subtraction and multiplication of [[boolean-valued functions]]. Thus, for functions $f$ and $g$ from $\mathbb{N}$ to $\mathbb{2}$, the [[tight apartness relation]] on the function set $\mathbb{2}^\mathbb{N}$, defined by 
$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$ 
is logically equivalent to $\exists x \in \mathbb{N}.f(x) - g(x) = 1$, since $f(x) \neq g(x)$ is logically equivalent to $f(x) = g(x) + 1$. 

Suppose LPO holds. Then for functions $f$ and $g$ from $\mathbb{N}$ to $\mathbb{2}$, define the function $h$ by $h(x) = f(x) - g(x)$ for all $x \in \mathbb{N}$. Then since LPO says that $\exists x \in \mathbb{N}.h(x) = 1$ is decidable, and $\exists x \in \mathbb{N}.h(x) = 1$ is logically equivalent to $f \# g$, then $f \# g$ is decidable. 

Conversely, assume that $f \# g$ is decidable. Then take $g$ to be the constant function at the boolean $0$, and $f \# \lambda x \in \mathbb{N}.0$ is logically equivalently to $\exists x \in \mathbb{N}.f(x) - 0 = 1$ and thus $\exists x \in \mathbb{N}.f(x) = 1$. Since $f \# g$ is decidable, then $\exists x \in \mathbb{N}.f(x) = 1$ is decidable, which is LPO. 
\end{proof}

### Other statements

We have the equivalence of LPO with the [[analytic LPO]] for various notions of [[real numbers]]. 

* The [[analytic LPO]] for the following sets of real numbers are equivalent to LPO: the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]] $\mathbb{R}_E$/$\mathbb{R}_H$, and the subfield of [[Dedekind real numbers]] $\mathbb{R}_\Sigma \subseteq \mathbb{R}_D$ which are constructed out of [[Dedekind cuts]] valued in the set of [[quasidecidable propositions]] $\Sigma \subseteq \Omega$. 

Proofs of this theorem are available at the article [[analytic LPO]]. 

One also has:

* The [[Bolzano-Weierstrass theorem]] states that the [[unit interval]] is [[sequentially compact space|sequentially compact]], and it holds of the [[Cauchy real numbers]] if and only if LPO holds; see [Mandelkern 1988](#Mandelkern88). 

* The [[Cauchy real numbers]] are isomorphic to the [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff LPO holds; see [Feldman (2010)](#Mehkeri10). 

* Every [[semidecidable proposition]] is a [[decidable proposition]] if and only if LPO holds; see [Diener 2018](#Diener18).

* Every [[quasidecidable proposition]] is a [[decidable proposition]] if and only if LPO holds; see at [[quasidecidable proposition]] for a proof.

+-- {: .standout}
These statements beneath this standout box currently do not have proofs on the nLab or references to literature containing a proof of the statement. Please add such proofs or references to the article, or delete them if these statements are not true. 
=--

* Every [[Cauchy real number]] is a [[rational number]] or has an strictly non-repeating base $b$ radix expansion if and only if LPO holds. 

* LPO holds if and only if for every function $f:\mathbb{N} \to \mathbb{N}$ from $\mathbb{N}$ to the [[natural numbers]], either there exists an element $x \in \mathbb{N}$ and a natural number $n$ such that $f(x) = n + 1$, or for all elements $x \in \mathbb{N}$ we have $f(x) = 0$. 

* Given a [[finite set]] $S$ of [[cardinality]] $n \gt 1$, LPO holds if and only if that the [[function set]] $S^\mathbb{N}$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $S^\mathbb{N}$ be defined as 
$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$

* The [[p-adic integers|$p$-adic integers]] being a [[discrete integral domain]] and the [[p-adic rationals|$p$-adic rationals]] being a [[discrete field]] are both equivalent to LPO. 

* LPO holds if and only if the [[function set]] $\mathbb{N}^\mathbb{N}$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{N}^\mathbb{N}$ be defined as 
$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$

* The [[ring]] of [[rational numbers|rational]] [[power series]] $\mathbb{Q}[[x]]$ being a [[discrete integral domain]] is equivalent to LPO. Similarly, the [[Heyting field]] of [[rational numbers|rational]] [[Laurent series]] $\mathbb{Q}((x))$ being a [[discrete field]] is equivalent to LPO. 

Let $C$ denote the [[category]] of [[discrete field|discrete]] [[sequentially Cauchy complete]] [[Archimedean ordered fields]]. $C$ is a [[groupoid]] and a [[subsingleton]] [[principle of equivalence|up to]] [[uniqueness quantifier|unique]] [[isomorphism]]: for every two [[objects]] $R \in C$ and $R' \in C$ there exists a unique [[morphism]] between $R$ and $R'$ which is an [[isomorphism]]. 

* LPO holds if and only if there is an object $\mathbb{R} \in C$, which will necessarily be unique up to unique isomorphism, and LPO fails if and only if $C$ is an [[empty category]]. 

## Consequences

There are various statements that are consequences of LPO. 

\begin{theorem}
[[WLPO]] follows from LPO, but not conversely. 
\end{theorem}

\begin{proof}
If $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so LPO gives
$$(\exists x \in \mathbb{N}, \neg{P(x)}) \vee (\forall x \in \mathbb{N}, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x \in \mathbb{N}, P(x)) \vee (\forall x \in \mathbb{N}, P(x))$$
as $P$ is decidable.
\end{proof} 

\begin{theorem}
[[LLPO]] follows from LPO, but not conversely. 
\end{theorem}

\begin{proof}
[[LLPO]] follows from LPO, WLPO is equivalent to fully untruncated LLPO, which implies LLPO, and WLPO follows from LPO. However, the converse does not necessarily hold, since in <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates WLPO from LLPO. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates WLPO from LLPO. Thus LLPO is separated from LPO. 
\end{proof}

## Statements that imply LPO

There are various other statements that imply LPO, some of which are listed in this section. 

* [[full bar induction]] implies LPO; see [Troelstra & van Dalen 1988](#TvD88) and [Kawai 2018](#Kawai18)

There are also some results from constructive [[ordinal]] theory:

* If every pair of [[ordinals]] $\alpha$ and $\beta$ has a binary [[meet]], then LPO holds; this is Proposition 5.2 in [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26). 

* If binary [[joins]] exist for non-successor [[ordinals]] $\alpha$ and $\beta$, then LPO holds; this is Proposition 6.2 in [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26). 

### Universes and models of foundations

The existence of various [[classical mathematics|classical]] [[universes]] or models of [[foundations of mathematics]] implies LPO: 

\begin{theorem}
Any model $\mathcal{V}$ of bounded Zermelo set theory contains a [[pure set]] of [[real numbers]] $\mathbb{R}$.
\end{theorem}

\begin{proof}
One can collect all the pure sets of $\mathcal{V}$ which are in $\mathbb{R}$ and show that the resulting set is a subset of $\mathcal{V}$ and a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire foundations. Thus, the existence of stronger models of [[material set theory]] such as [[ZFC]] also imply LPO for the entire foundations.
\end{proof} 

\begin{theorem}
The existence of a constructively [[well-pointed topos|well-pointed]] [[Boolean topos|Boolean]] [[W-topos]] $\mathcal{E}$ implies LPO.
\end{theorem}

\begin{proof}
The hom-set $\mathrm{Hom}_\mathcal{E}(1, \mathbb{R})$, where $1 \in \mathcal{E}$ is the [[terminal object|terminal]] [[generator]] and  $\mathbb{R} \in \mathcal{E}$ is the [[real numbers object]] in $\mathcal{E}$, yields a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire foundations. Thus, the existence of any constructive model of [[ETCS]] also implies LPO for the entire foundations. 
\end{proof}

\begin{theorem}
In [[dependent type theory]], there being a [[univalent Tarski universe]] $(U, T)$ closed under dependent product types, dependent sum types, and identity types and satisfying the axiom of infinity and [[excluded middle]] implies LPO. 
\end{theorem}

\begin{proof}
One can construct an element $\mathbb{R}:U$ representing the $U$-small type of real numbers, whose type reflection $T(\mathbb{R})$ is a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire type theory. Thus, any univalent Tarski universe which has [[axiom of choice]] also implies LPO for the entire type theory. 
\end{proof}

Note that in all these cases, the real numbers $\mathbb{R}$ constructed from these universes or classical models of foundations of mathematics, while equivalent to the internal Dedekind real numbers constructed in the universe or model, are not necessarily equivalent to the external [[Dedekind real numbers]] in the foundations. 

## Statements inconsistent with LPO

There are various statements in mathematics which are inconsistent with LPO, some of which are listed here. 

* LPO is inconsistent with the existence of a [[Specker sequence]]; see [Diener 2018](#Diener18). 

* LPO is inconsistent with [[Phoa's principle]] and [[synthetic quasi-coherence]] for the set of [[quasidecidable propositions]]; see at [[quasidecidable proposition]] for a proof. 

### In real analysis

\begin{theorem}
LPO is inconsistent with [[Brouwer's continuity principle]] for any one of the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[HoTT book real numbers]] $\mathbb{R}_H$, or the [[Dedekind real numbers]] $\mathbb{R}_\Sigma$ defined using the set of [[quasidecidable propositions]]. 
\end{theorem}

\begin{proof}
LPO implies that $\mathbb{R}_C$, $\mathbb{R}_H$, and $\mathbb{R}_\Sigma$ are equivalent to each other, which means we can simply denote this set of real numbers as $\mathbb{R}$, and that the [[pseudo-order]] relation on $\mathbb{R}$ is decidable. As a result, we can define a pointwise-[[discontinuous function]] $f:\mathbb{R} \to \mathbb{R}$ by case analysis: $f(x) = 1$ if $x \gt 0$ and $f(x) = 0$ if $x \leq 0$. This contradicts Brouwer's continuity principle which says that all functions $f:\mathbb{R} \to \mathbb{R}$ are pointwise-continuous. 
\end{proof}

\begin{theorem}
In the presence of the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, 2}$, LPO is inconsistent with [[Brouwer's continuity principle]] for the usual impredicative [[Dedekind real numbers]] defined using the [[frame of truth values]] $\Omega$. 
\end{theorem}

\begin{proof}
$\mathrm{AC}_{\mathbb{N}, 2}$ implies that the Cauchy real numbers and the Dedekind real numbers coincide. Since the previous theorem implies that LPO is inconsistent with [[Brouwer's continuity principle]] for the Cauchy real numbers, $\mathrm{AC}_{\mathbb{N}, 2}$ implies that LPO is inconsistent with [[Brouwer's continuity principle]] for the Dedekind real numbers. 
\end{proof}

This means that theories which accept both LPO and [[Brouwer's continuity principle]] for the Dedekind real numbers, such as the [[internal logic]] of the [[cohesive (infinity,1)-topos]] of [[Euclidean-topological infinity-groupoids]], necessarily reject $\mathrm{AC}_{\mathbb{N}, 2}$. 

## Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO$ holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* LPO fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the modulated Cauchy reals and Dedekind reals coincide in this topos. 

* LPO fails in the parameterized [[realizability topos]] constructed in [Bauer & Hanson 2024](#BauerHanson24). 

* It appears that a [[realizability topos]] based on infinite-time [[Turing machine]]s validates $LPO$ but not $EM$; see [Bauer (2011)](#Bauer11). 

## In dependent type theory

+-- {: .standout}
This section appears to be original research, as there doesn't seem to be any existing literature on the "disjunction-untruncated" and "quantifier-untruncated" versions of the limited principle of omniscience in [[dependent type theory]]. 
=--

In the context of [[dependent type theory]], the usual limited principle of omniscience is expressed as 

$$\prod_{f:\mathbb{N} \to \mathbb{2}} (\exists x:\mathbb{N}.f(x) = 1) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

However, there are in general two ways of interpreting predicate logic, the traditional interpretation using [[propositional truncations]], and the [[BHK interpretation]] which do not use propositional truncations. This results in four different versions of the limited principle of omniscience, depending on whether the [[existential quantifier]] is truncated or untruncated, and whether the [[disjunction]] is truncated or untruncated:

* the usual limited principle of omniscience states that 

$$\prod_{f:\mathbb{N} \to \mathbb{2}} (\exists x:\mathbb{N}.f(x) = 1) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **disjunction-untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\exists x:\mathbb{N}.f(x) = 1\right) + \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **quantifier-untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\sum_{x:\mathbb{N}} f(x) = 1\right) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **fully untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\left(\sum_{x:\mathbb{N}} f(x) = 1\right) + \prod_{x:\mathbb{N}} f(x) = 0\right)$$

Let us begin with the equivalence of the various truncated versions of LPO with the usual untruncated version of LPO. 

\begin{theorem}
LPO implies the disjunction-untruncated LPO.  
\end{theorem}

This proof is due to Urs Schreiber from [here](https://nforum.ncatlab.org/discussion/18354/limited-principle-of-omniscience/?Focus=127196#Comment_127196). 

\begin{proof}
Let $f:\mathbb{N} \to \mathbb{2}$ be a sequence of booleans. We define the following types

$$P \coloneqq \exists n:\mathbb{N}.f(n) = 1 \qquad Q \coloneqq \prod_{n:\mathbb{N}} f(n) = 0$$

The fully truncated LPO is thus the statement $[P + Q]$, while the disjunction-untruncated LPO is the statement $P + Q$. 

Both $P$ and $Q$ are mere propositions, $P$ by definition of [[propositional truncation]] while $Q$ by [[weak function extensionality]] and the fact that equality on the booleans is a [[mere proposition]]. 

Secondly, we construct a function $(P \times Q) \to \emptyset$. Namely, suppose we have an element of $Q$, meaning an element that $\prod_{n:\mathbb{N}} f(n) = 0$. We wish to map $P$ to $\emptyset$. Because $\emptyset$ is a [[mere proposition]], we may apply the [[universal property]] of [[propositional truncation]] to eliminate out of $P$. This means we can legitimately assume we have a specific pair $(n, p)$ where $p:f(n) = 1$. Applying our element of $Q$ to $n$ yields a proof that $f(n) = 0$. Thus, $1 = 0$ in the [[boolean domain]], which is a contradiction yielding an element of $\emptyset$. 

Now, every given any two [[mere propositions]] $P$ and $Q$ with a function $(P \times Q) \to \emptyset$, the [[sum type]] $P + Q$ has a [[choice operator]] $[P + Q] \to (P + Q)$; see proof at the article [[choice operator]]. By applying the choice operator to our premise, the standard LPO provided by the element of $[P + Q]$, we extract a valid element of $P + Q$. 

This established the disjunction-untruncated LPO. 
\end{proof}

\begin{theorem}
Given a sequence of booleans $f:\mathbb{N} \to \mathbb{2}$, the [[preimage]] of $f$ at the boolean $1$ has a [[choice operator]]. 
\end{theorem}

\begin{proof}
See [Rijke 2022](#Rijke22) for a proof of the statement in [[dependent type theory]]. 
\end{proof}

\begin{theorem}
The disjunction-untruncated LPO implies the fully untruncated LPO.  
\end{theorem}

\begin{proof}
By [[weak function extensionality]], the type $\prod_{n:\mathbb{N}} f(n) = 0$ is a proposition and so is equivalent to its own [[propositional truncation]] $\forall n:\mathbb{N}.f(n) = 0$, which is the negation of $\exists n:\mathbb{N}.f(n) = 1$. Given a function $f:A \to B$ and a type $C$ one can construct the function $(f + \mathrm{id}_C):(A + C) \to (B + C)$ by the [[pullback stability]] of [[sum types]], where $\mathrm{id}_C$ is the [[identity function]] on type $C$. 
$$
\begin{array}{c}
A & \rightarrow & A + C & \leftarrow & C \\
\downarrow & & \downarrow & & \downarrow \\
B & \rightarrow & B + C & \leftarrow & C \\
\end{array}
$$
Thus, since the type $\sum_{n:\mathbb{N}}.f(n) = 1$ has a choice operator, one can construct the function 
$$\epsilon + \mathrm{id}_{\prod_{n:\mathbb{N}} f(n) = 0}$$
from the disjunction-untruncated LPO
$$(\exists n:\mathbb{N}.f(n) = 1) + \left(\prod_{n:\mathbb{N}} f(n) = 0\right)$$ 
to the fully untruncated LPO
$$\left(\sum_{n:\mathbb{N}} f(n) = 1\right) + \left(\prod_{n:\mathbb{N}} f(n) = 0\right)$$
\end{proof}

\begin{theorem}
LPO and fully untruncated LPO are logically interderivable from each other. 
\end{theorem}

\begin{proof}
The converses follow from the fact that by the inference rules of [[propositional truncations]], one has a function $\mathrm{trunc}_P:P \to [P]$ for all types $P$. 
\end{proof}

\begin{theorem}
LPO is inconsistent with [[canonicity]] or [[homotopy canonicity]] in [[dependent type theory]]. 
\end{theorem}

\begin{proof}
By LPO, we can define the sequence $f:\mathbb{N} \to \mathbb{2}$ to the booleans $\mathbb{2}$ by $f(n) = 1$ if $2 n + 2$ is the sum of two [[prime numbers]] and $f(n) = 0$ if $2 n + 2$ is not the sum of two prime numbers, since $2 n + 2$ being the sum of two prime numbers is a [[decidable proposition]]. Then [[Goldbach's conjecture]] states that the $f$ is equal to the constant sequence $\lambda n:\mathbb{N}.1$, and we can define a term $\mathrm{LPO}(\mathrm{Goldbach}, 0, 1):\mathbb{N}$ which is 0 or 1 according as the Goldbach conjecture is true or false. This term is not [[identification|identified with]] a [[canonical form]] (a numeral), contradicting [[homotopy canonicity]] and by extension [[canonicity]].
\end{proof}

## Generalizations

### Choiceless limited principle of omniscience

There is a generalization of the limited principle of omniscience defined in [King 2024](#King24), which was suggested to be called the **choiceless limited principle of omniscience**. The choiceless limited principle of omniscience states that given and a pair of [[predicates]] $P$ and $Q$ on $\mathbb{N}$ such that $P(x) \vee Q(x)$ holds for all $x \in \mathbb{N}$, then either there exists $x \in \mathbb{N}$ such that $P(x)$ or for all $x \in \mathbb{N}$, $Q(x)$. The idea behind the term "choiceless" is that one isn't forced to choose between $P(x)$ or $Q(x)$ in this version of the limited principle of omniscience. One gets back the usual limited principle of omniscience if $P(x)$ and $Q(x)$ are [[mutually exclusive propositions]] for all $x \in A$, from which $Q(x)$ [[if and only if]] $\neg P(x)$ for all $x \in \mathbb{N}$. 

We can also state the principle set-theoretically. The __choiceless limited principle of omniscience__ states that given [[subsets]] $P, Q \in \mathcal{P}(\mathbb{N})$, if $P \cup Q = \mathbb{N}$, then either $P$ is [[inhabited subset|inhabited]] or $Q = \mathbb{N}$. One gets back the usual limited principle of omniscience if $P$ and $Q$ are [[disjoint subsets]] $P \cap Q = \emptyset$, from which $Q = \bar{P}$, where $\bar{P}$ is the [[complement]] of $P$. 

The choiceless limited principle of omniscience implies the [[analytic limited principle of omniscience]] for all sets of [[real numbers]], as shown in [King 2024](#King24), thus also implying that the real numbers coincide with each other. 

### Exhaustible sets

One can consider generalizing the [[domain of discourse]] of the limited principle of omniscience from the [[natural numbers]] to an arbitrary [[set]] $A$. Such sets satisfying the limited principle of omniscience are called [[exhaustible sets]]. 

### Generalizations to other sets of propositions

+-- {: .standout}
This section appears to be original research, as there doesn't seem to be any existing literature on such a generalization of the limited principle of omniscience. 
=--

One can also consider generalizing from the [[decidable propositions]] to other types of propositions. Let $\Sigma$ be a [[subobject|sub]][[lattice]] of the [[frame of truth values]] $\Omega$. Then the __limited principle of omniscience__ $\mathrm{LPO}_{\Sigma}$ states that, given any [[function]] $f$ from $\mathbb{N}$ to $\Sigma$, there exists an element $p \in \Sigma$ such that $p = \top$ [[if and only if]] there exists an element $x \in A$ such that $f(x) = \top$. 

$$\forall f:\mathbb{N} \to \Sigma.\exists p \in \Sigma.p = \top \iff \exists x \in \mathbb{N}.f(x) = \top$$

The usual limited principle of omniscience is then $\mathrm{LPO}_{\mathbb{2}}$ for the [[booleans]] $\mathbb{2}$:
$$\forall f:\mathbb{N} \to \mathbb{2}.\exists p \in \mathbb{2}.(p = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$
Now by recursion of the booleans we have either that $p = \bot$ or $p = \top$, so the statement 
$$\forall f:\mathbb{N} \to \mathbb{2}.\exists p \in \mathbb{2}.(p = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$ 
is equivalent to 
$$\forall f:\mathbb{N} \to \mathbb{2}.(\top = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top) \vee (\bot = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$
and since $\top = \top$ is true and $\bot = \top$ is false, we have
$$\forall f:\mathbb{N} \to \mathbb{2}.(\exists x \in \mathbb{N}.f(x) = \top) \vee \neg (\exists x \in \mathbb{N}.f(x) = \top)$$
which is precisely the usual limited principle of omniscience.

For the set of [[semi-decidable propositions]] $\Sigma_0^1$, the limited principle of omniscience $\mathrm{LPO}_{\Sigma_0^1}$ is equivalent to the [[Rosolini dominance]] being a [[dominance]] and the [[Cauchy real numbers]] being [[Dedekind complete]] via [[semi-decidable]] [[Dedekind cuts]]. 

For the set of truth values $\Omega$, the limited principle of omniscience $\mathrm{LPO}_{\Omega}$ is always true for because $\Omega$ is a [[frame]] and thus closed under existential quantification over $\mathbb{N}$. 

## Related concepts

* [[principle of omniscience]]

* [[weak limited principle of omniscience]]

* [[lesser limited principle of omniscience]]

* [[Markov's principle]]

* [[excluded middle]]

* [[exhaustible set]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Mandelkern82} [[Mark Mandelkern]], *Components of an open set*, Journal of the Australian Mathematical Society, Volume 33, Issue 2, October 1982, pp. 249 - 261, &lbrack;[doi:10.1017/S1446788700018383](https://doi.org/10.1017/S1446788700018383), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/87B279B7B200821168EC5A5A4BE62A4E/S1446788700018383a.pdf/components-of-an-open-set.pdf)&rbrack;

* {#Mandelkern88} [[Mark Mandelkern]]: *Limited Omniscience and the Bolzano-Weierstrass Principle*, Bulletin of the London Mathematical Society **20** 4 (1988) 319--320, &lbrack;[doi:10.1112/blms/20.4.319](https://doi.org/10.1112/blms/20.4.319), [pdf](https://www.zianet.com/mandelkern/mandelkern_bwp.pdf)&rbrack;

* {#TvD88} [[Anne Sjerp Troelstra]], [[Dirk van Dalen]]: *Constructivism in Mathematics -- An introduction*, Volume I, Studies in Logic and the Foundations of Mathematics **121**, North Holland (1988) &lbrack;[ISBN:9780444702661](https://www.elsevier.com/books/constructivism-in-mathematics-vol-1/troelstra/978-0-444-70266-1)&rbrack;

* {#Richman91} [[Fred Richman]], *Polynomials and linear transformations*. Linear Algebra and its Applications, Volume 131, 1 April 1990, Pages 131-137. &lbrack;<a href="https://doi.org/10.1016/0024-3795(90)90379-Q">doi:10.1016/0024-3795(90)90379-Q</a>&rbrack;

* {#Ishihara06} [[Hajime Ishihara]]: _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS **6** (2006) &lbrack;[doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406), [pdf](https://philosophiascientiae.revues.org/pdf/406)&rbrack;

* {#Tanaka07} [[Yasuhito Tanaka]]: *The Gibbard–Satterthwaite theorem of social choice theory in an infinite society and LPO (limited principle of omniscience)*, Applied Mathematics and Computation **193** 2 (2007) 475--481 &lbrack;[doi:10.1016/j.amc.2007.04.001](https://doi.org/10.1016/j.amc.2007.04.001), [pdf archived](https://web.archive.org/web/20211011144745/http://hokuriku.me/kiishimizu/pdf/AMC12363.pdf)&rbrack;

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (trans. buTania K. Roblo): *Commutative algebra: Constructive methods (Finite projective modules)*, Springer (2015) &lbrack;[doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf)&rbrack;

* {#Rathjen13} [[Michael Rathjen]]: *Constructive Zermelo-Fraenkel set theory and the limited principle of omniscience* &lbrack;[arXiv:1302.3037](https://arxiv.org/abs/1302.3037)&rbrack;

* {#Kawai18} [[Tatsuji Kawai]]: *Principles of bar induction and continuity on Baire space* &lbrack;[arXiv:1808.04082](https://arxiv.org/abs/1808.04082)&rbrack;

* {#Shulman18} [[Mike Shulman]]: *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science **28** 6 (2018) 856--941 &lbrack;[arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147)&rbrack;

* {#Diener18} [[Hannes Diener]], *Constructive Reverse Mathematics*, Habil. thesis, Univ. Siegen (2018) &lbrack;[arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306)&rbrack;

* {#Booij20} [[Auke Booij]]: *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411](http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#Bauer21} [[Andrej Bauer]]: *Instance reducibility and Weihrauch degrees*, Logical Methods in Computer Science **18** 3 (2022) &lbrack;<a href="https://doi.org/10.46298/lmcs-18(3:20)2022">doi:10.46298/lmcs-18(3:20)2022</a>,[arXiv:2106.01734](https://arxiv.org/abs/2106.01734), [pdf](https://lmcs.episciences.org/9906/pdf)&rbrack;

* {#Ciraulo22} Francesco Ciraulo: *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science **18** 1 (2022) &lbrack;[doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644)&rbrack;

* {#Rijke22} [[Egbert Rijke]]: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2025) &lbrack;[doi:10.1017/9781108933568](https://doi.org/10.1017/9781108933568), [arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;

* {#BauerHanson24} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#BirchfieldSwan24} [[Madeleine Birchfield]], [[Andrew Swan]] (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#LombardiMahboubi24} [[Henri Lombardi]], [[Assia Mahboubi]], *Théories géométriques pour l'algèbre des nombres réels sans test de signe ni axiome de choix dépendant* ([arXiv:2406.15218](https://arxiv.org/abs/2406.15218))

* {#King24} Christopher King, *What are these generalizations of the principles of omniscience called?*, MathOverflow, 15 February 2024. ([web](https://mathoverflow.net/questions/464247/what-are-these-generalizations-of-the-principles-of-omniscience-called))

* {#JKMF26} [[Tom de Jong]], [[Nicolai Kraus]], [[Aref Mohammadzadeh]], [[Fredrik Nordvall Forsberg]], *Generalized Decidability via Brouwer Trees* ([arXiv:2602.10844](https://arxiv.org/abs/2602.10844))

This reference calls the fully untruncated limited principle of omniscience for the natural numbers simply by the term "limited principle of omniscience". However, the limited principle of omniscience usually refers to the fully truncated version. 

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

These two references call the limited principle of omniscience simply by the term "principle of omniscience" or "omniscience principle". However, [[principle of omniscience]] can refer to multiple possible axioms. 

* {#Bauer11}  [[Andrej Bauer]] (2011) via constructivenews, [An Injection from $\mathbb{N}^{\mathbb{N}}$ to $\mathbb{N}$](http://math.andrej.com/wp-content/uploads/2011/06/injection.pdf) (pdf)

* {#Escardo11} [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)

[[!redirects LPO]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

[[!redirects antithesis LPO]]
[[!redirects antithesis limited principle of omniscience]]
[[!redirects antithesis limited principles of omniscience]]

[[!redirects affine LPO]]
[[!redirects affine limited principle of omniscience]]
[[!redirects affine limited principles of omniscience]]

[[!redirects truncated LPO]]
[[!redirects truncated limited principle of omniscience]]
[[!redirects truncated limited principles of omniscience]]

[[!redirects untruncated LPO]]
[[!redirects untruncated limited principle of omniscience]]
[[!redirects untruncated limited principles of omniscience]]

[[!redirects disjunction-untruncated LPO]]
[[!redirects disjunction-untruncated limited principle of omniscience]]
[[!redirects disjunction-untruncated limited principles of omniscience]]

[[!redirects disjunction untruncated LPO]]
[[!redirects disjunction untruncated limited principle of omniscience]]
[[!redirects disjunction untruncated limited principles of omniscience]]

[[!redirects existential-quantifier-untruncated LPO]]
[[!redirects existential-quantifier-untruncated limited principle of omniscience]]
[[!redirects existential-quantifier-untruncated limited principles of omniscience]]

[[!redirects existential quantifier untruncated LPO]]
[[!redirects existential quantifier untruncated limited principle of omniscience]]
[[!redirects existential quantifier untruncated limited principles of omniscience]]

[[!redirects existential-quantification-untruncated LPO]]
[[!redirects existential-quantification-untruncated limited principle of omniscience]]
[[!redirects existential-quantification-untruncated limited principles of omniscience]]

[[!redirects existential quantification untruncated LPO]]
[[!redirects existential quantification untruncated limited principle of omniscience]]
[[!redirects existential quantification untruncated limited principles of omniscience]]

[[!redirects quantifier-untruncated LPO]]
[[!redirects quantifier-untruncated limited principle of omniscience]]
[[!redirects quantifier-untruncated limited principles of omniscience]]

[[!redirects quantifier untruncated LPO]]
[[!redirects quantifier untruncated limited principle of omniscience]]
[[!redirects quantifier untruncated limited principles of omniscience]]

[[!redirects quantification-untruncated LPO]]
[[!redirects quantification-untruncated limited principle of omniscience]]
[[!redirects quantification-untruncated limited principles of omniscience]]

[[!redirects quantification untruncated LPO]]
[[!redirects quantification untruncated limited principle of omniscience]]
[[!redirects quantification untruncated limited principles of omniscience]]

[[!redirects fully untruncated LPO]]
[[!redirects fully untruncated limited principle of omniscience]]
[[!redirects fully untruncated limited principles of omniscience]]

[[!redirects choiceless LPO]]
[[!redirects choiceless limited principle of omniscience]]
[[!redirects choiceless limited principles of omniscience]]