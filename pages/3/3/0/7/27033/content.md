
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

One can equivalently use functions to the [[boolean domain]] instead of [[decidable subsets]]. The __limited principle of omniscience__ states that given any [[function]] $f$ from the [[natural numbers]] $\mathbb{N}$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. In this case, the limited principle of omniscience is also called **[[excluded middle]] for [[semidecidable truth values]]**, i.e. [[truth values]] of the form $\exists n, f(n) = 1$ for some [[boolean]]-valued [[sequence]] $f:\mathbb{N}\to \mathbf{2}$, or **$\Sigma^0_1$-[[excluded middle]]** ([Diener 2018](#Diener18)) in the sense of the [[arithmetical hierarchy]] in [[computability theory]]. 

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

### In dependent type theory

In the context of [[dependent type theory]], the usual limited principle of omniscience is expressed as 

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \exists x:\mathbb{N}.f(x) = 1) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

However, there are in general two ways of interpreting predicate logic, the traditional interpretation using [[propositional truncations]], and the [[BHK interpretation]] which do not use propositional truncations. This results in four different versions of the limited principle of omniscience, depending on whether the [[existential quantifier]] is truncated or untruncated, and whether the [[disjunction]] is truncated or untruncated:

* the usual limited principle of omniscience states that 

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \exists x:\mathbb{N}.f(x) = 1) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **disjunction-untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\exists x:\mathbb{N}.f(x) = 1\right) + \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **quantifier-untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\sum_{x:A} f(x) = 1\right) \vee \left(\prod_{x:\mathbb{N}} f(x) = 0\right)$$

* the **fully untruncated limited principle of omniscience** states that

$$\prod_{f:\mathbb{N} \to \mathbb{2}} \left(\left(\sum_{x:\mathbb{N}} f(x) = 1\right) + \prod_{x:\mathbb{N}} f(x) = 0\right)$$

Let us begin with the equivalence of the various truncated versions of the LPO with the usual untruncated version of the LPO. 

\begin{theorem}
The LPO implies the disjunction-untruncated LPO.  
\end{theorem}

\begin{proof}
Since any propositions $P$ and its negation $\neg P$ are [[mutually exclusive propositions|mutually exclusive]], the [[sum type]] $P + \neg P$ has a [[choice operator]], because $P$ and $\neg P$ being mutually exclusive implies that if the [[disjunction]] $P \vee Q$ holds, then [[exclusive disjunction]] holds: i.e. exactly one of $P$ and $\neg P$ holds. This is represented in dependent type theory by the sum type $P + \neg P$ being a [[contractible type]] $\mathrm{isContr}(P + \neg P)$, which by definition allows one to construct an element of $P + \neg P$. For $P$ being the [[existential quantifier]] $\exists n:\mathbb{N}.f(n) = 1$, $P \vee \neg P$ is truncated LPO while $P + \neg P$ is precisely the disjunction untruncated LPO. 
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

## Properties

\begin{theorem}
LPO holds if and only if for every function $f:\mathbb{N} \to \mathbb{N}$ from $\mathbb{N}$ to the [[natural numbers]], either there exists an element $x$ in $A$ and a natural number $n$ such that $f(x) = n + 1$, or for all elements $x$ in $\mathbb{N}$, $f(x) = 0$. 
\end{theorem}

Now, a [[sigma-complete lattice|$\sigma$-complete lattice]] is a lattice which has all $\mathbb{N}$-indexed joins, a lattice $L$ with a function 

$$\bigvee_{t:\mathbb{N}} (-)(t):(\mathbb{N} \to L) \to L$$

such that for all elements $x \in \mathbb{N}$ and functions $f:\mathbb{N} \to L$, 

$$f(x) \leq \bigvee_{t:\mathbb{N}} f(t)$$

and for all elements $y \in L$ and functions $f:\mathbb{N} \to L$, if $f(x) \leq y$ for all elements $x \in \mathbb{N}$, then 

$$\bigvee_{t:\mathbb{N}} f(t) \leq y$$

and a [[sigma-frame|$\sigma$-frame]] is a [[sigma-complete lattice|$\sigma$-complete lattice]] in which meets distribute over the $\mathbb{N}$-indexed joins: for all elements $x \in L$ and functions $f:v \to L$, 

$$a \wedge \bigvee_{t:\mathbb{N}} f(t) = \bigvee_{t:\mathbb{N}} a \vee f(t)$$

We say that a [[sigma-frame|$\sigma$-frame]] [[homomorphism]] is a lattice homomorphism which also preserves $\mathbb{N}$-indexed joins. 

\begin{theorem}
LPO holds if and only if the [[boolean domain]] is the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]; i.e. the [[boolean domain]] is a [[sigma-frame|$\sigma$-frame]] and for every other sigma-frame $L$, [[uniqueness quantifier|there is a unique]] sigma-frame homomorphism from the [[boolean domain]] to $L$. 
\end{theorem}

\begin{theorem}
LPO holds if and only if the [[boolean domain]] is the [[initial object|initial]] $\mathbb{N}$-overt $\emptyset$-overt [[dominance]]. 
\end{theorem}

\begin{proof}
We can rewrite the limited principle of omniscience for $\mathbb{N}$ in the form of for all functions $f:\mathbb{N} \to \mathbb{2}$, there exists a [[boolean]] $b \in \mathbb{2}$ such that $b = 1$ if and only if $\exists n \in \mathbb{N}, f(n) = 1$. 

By the induction principle of the [[booleans]], the set $\{b \in \mathbb{2} \vert (b = 1) \iff \exists n \in \mathbb{N}, f(n) = 1\}$ has a [[choice operator]] given by a function from the [[subsingleton]] $\{x \in \mathbb{1} \vert \exists b \in \mathbb{2} (b = 1) \iff \exists n \in \mathbb{N}, f(n) = 1\}$ to the set. This means that one can apply choice to get a specified boolean $b \in \mathbb{2}$ for all functions $f:\mathbb{N} \to \mathbb{2}$, which by [[currying]] results in a function $V:\mathbb{2}^\mathbb{N} \to \mathbb{2}$ such that $V(f) = 1$ if and only if $\exists n \in A, f(n) = 1$, meaning that $V$ is closed under $\mathbb{N}$-indexed joins. 

Since the [[booleans]] are a [[subobject|sub]][[lattice]] of the [[frame of truth values]] and the [[booleans]] are a [[dominance]], this implies that the booleans are $\emptyset$-overt, $\mathbb{N}$-overt, and initial, since the initial $\mathbb{N}$-overt dominance is by definition a subset of the [[frame of truth values]] and so coincide with the booleans under the limited principle of omniscience. Since [[existential quantification]] of [[booleans]] distributes over [[meets]] of [[booleans]], the $\sigma$-complete lattice is an $\sigma$-frame, and initiality of the $\sigma$-frame comes from the fact that the booleans are a dominance. 

Conversely, suppose that the [[booleans]] are the initial $\emptyset$-overt, $\mathbb{N}$-overt [[dominance]] or the initial $\sigma$-frame. The [[booleans]] are a [[subobject|sub]]-$\sigma$-complete lattice of the [[frame of truth values]], so we can treat the $\mathbb{N}$-indexed joins $V:\mathbb{2}^\mathbb{N} \to \mathbb{2}$ as [[existential quantification]] over $\mathbb{N}$. Then by the function $V:\mathbb{2}^\mathbb{N} \to \mathbb{2}$ we have that for all functions $f:\mathbb{N} \to \mathbb{2}$, $V(f) = 1$ if and only if $\exists n \in \mathbb{N}, f(n) = 1$, which implies the limited principle of omniscience. 
\end{proof}

The next statement relate LPO with the axiom that [[tight apartness relation]] on the [[function set]] $\mathbb{2}^\mathbb{N}$ is a [[decidable tight apartness]]. 

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

The next two statements relate the LPO with axioms that the [[tight apartness relation]] on certain other [[function sets]] are a [[decidable tight apartness]]. 

\begin{theorem}
More generally, given a [[finite set]] $S$ of [[cardinality]] $n \gt 1$, LPO holds if and only if that the [[function set]] $S^\mathbb{N}$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $S^\mathbb{N}$ be defined as 

$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$
\end{theorem}

\begin{theorem}
LPO holds if and only if the [[function set]] $\mathbb{N}^\mathbb{N}$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{N}^\mathbb{N}$ be defined as 

$$f \# g \coloneqq \exists x \in \mathbb{N}.f(x) \neq g(x)$$
\end{theorem}

### Statements equivalent to LPO

There are various other results that are equivalent specifically to the limited principle of omniscience. 

#### Real analysis

Next, we have the equivalence of the LPO with the [[analytic LPO]] for various notions of [[real numbers]]. 

\begin{theorem}
The [[analytic LPO]] for the following sets of real numbers are equivalent to the LPO: the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]] $\mathbb{R}_E$/$\mathbb{R}_H$, and the subfield of [[Dedekind real numbers]] $\mathbb{R}_\Sigma \subseteq \mathbb{R}_D$ which are constructed out of [[Dedekind cuts]] valued in the set of [[Sierpinski semi-decidable truth values]] $\Sigma \subseteq \Omega$. 
\end{theorem}

Let $C$ denote the [[category]] of [[discrete field|discrete]] [[sequentially Cauchy complete]] [[Archimedean ordered fields]]. $C$ is a [[groupoid]] and a [[subsingleton]] [[principle of equivalence|up to]] [[uniqueness quantifier|unique]] [[isomorphism]]: for every two [[objects]] $R \in C$ and $R' \in C$ there exists a unique [[morphism]] between $R$ and $R'$ which is an [[isomorphism]]. 

\begin{theorem}
LPO holds if and only if there is an object $\mathbb{R} \in C$, which will necessarily be unique up to unique isomorphism, and LPO fails if and only if $C$ is an [[empty category]]. 
\end{theorem}

There are other equivalent statements from [[real analysis]]:

\begin{theorem}
[[sequentially compact space|Sequential compactness]] of the [[unit interval]] holds if and only if LPO holds. 
\end{theorem}

\begin{theorem}
Every [[Cauchy real number]] is a [[rational number]] or has an strictly non-repeating base $b$ radix expansion if and only if LPO holds. 
\end{theorem}

\begin{theorem}
The [[Cauchy real numbers]] are isomorphic to the [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff LPO holds. 
\end{theorem}

\begin{proof}
See [Feldman (2010)](#Mehkeri10). 
\end{proof}

#### Other statements

* Every [[semi-decidable proposition]] is a [[decidable proposition]] if and only if LPO holds. 

* The [[p-adic integers|$p$-adic integers]] being a [[discrete integral domain]] and the [[p-adic rationals|$p$-adic rationals]] being a [[discrete field]] are both equivalent to LPO 

* The [[ring]] of [[rational numbers|rational]] [[power series]] $\mathbb{Q}[[x]]$ being a [[discrete integral domain]] is equivalent to LPO. Similarly, the [[Heyting field]] of [[rational numbers|rational]] [[Laurent series]] $\mathbb{Q}((x))$ being a [[discrete field]] is equivalent to LPO. 

### Statements implied by LPO

There are various statements that are implied by LPO. 

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

See [Diener 2018](#Diener18) for more statements that are implied by LPO. 

### Statements that imply LPO

There are various other statements that imply LPO, some of which are listed in this section. See [Diener 2018](#Diener18) for more statements that imply LPO. 

#### Universes and models of foundations

The existence of various [[classical mathematics|classical]] [[universes]] or models of [[foundations of mathematics]] implies the LPO: 

\begin{theorem}
Any model $\mathcal{V}$ of bounded Zermelo set theory contains a [[pure set]] of [[real numbers]] $\mathbb{R}$.
\end{theorem}

\begin{proof}
One can collect all the pure sets of $\mathcal{V}$ which are in $\mathbb{R}$ and show that the resulting set is a subset of $\mathcal{V}$ and a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire foundations. Thus, the existence of stronger models of [[material set theory]] such as [[ZFC]] also imply LPO for the entire foundations.
\end{proof} 

\begin{theorem}
The existence of a constructively [[well-pointed topos|well-pointed]] [[Boolean topos|Boolean]] [[W-topos]] $\mathcal{E}$ implies the LPO.
\end{theorem}

\begin{proof}
The hom-set $\mathrm{Hom}_\mathcal{E}(1, \mathbb{R})$, where $1 \in \mathcal{E}$ is the [[terminal object|terminal]] [[generator]] and  $\mathbb{R} \in \mathcal{E}$ is the [[real numbers object]] in $\mathcal{E}$, yields a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire foundations. Thus, the existence of any constructive model of [[ETCS]] also implies LPO for the entire foundations. 
\end{proof}

\begin{theorem}
In [[dependent type theory]], there being a [[univalent Tarski universe]] $(U, T)$ closed under dependent product types, dependent sum types, and identity types and satisfying the axiom of infinity and [[excluded middle]] implies the LPO. 
\end{theorem}

\begin{proof}
One can construct an element $\mathbb{R}:U$ representing the $U$-small type of real numbers, whose type reflection $T(\mathbb{R})$ is a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying LPO for the entire type theory. Thus, any univalent Tarski universe which has [[axiom of choice]] or a [[choice operator]] for the types in the universe also implies LPO for the entire type theory. 
\end{proof}

Note that in all these cases, the real numbers $\mathbb{R}$ constructed from these universes or classical models of foundations of mathematics, while equivalent to the internal Dedekind real numbers constructed in the universe or model, are not necessarily equivalent to the external [[Dedekind real numbers]] in the foundations. 

#### Choice principles

Let $\Sigma$ be the [[initial sigma-frame|initial $\sigma$-frame]], which is the initial $\mathbb{N}$-overt [[dominance]]. The [[axiom of choice]] for $\Sigma$-open entire relations to set $B$ says that for any set $A$ and any entire $\Sigma$-open relation $R:A \times B \to \Sigma$ from $A$ to $B$ there exists a function $f:A \to B$ such that for all $x$ in $A$ $R(x, f(x)) = \top$.

\begin{theorem}
The [[axiom of choice]] for $\Sigma$-open entire relations to the [[boolean domain]] implies LPO. 
\end{theorem}

\begin{proof}
The proof is similar to one direction of the proof of the [[Diaconescu-Goodman-Myhill theorem]]. 

Let $P$ be a $\Sigma$-open proposition. Quotient the [[boolean domain]] $\mathbb{2}$ by the [[equivalence relation]] where $0 = 1$ [[if and only if]] $P$ holds, resulting in a set $A$. Then we have an $\Sigma$-open entire relation $R$ between $A$ and $\mathbb{2}$, and there exists a function $f:A \to \mathbb{2}$ such that $R(x, f(x)) = \top$ if and only if $P$ is a [[decidable proposition]], and that it holds for all such $P$ is precisely LPO. Thus, the [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] implies LPO. 
\end{proof}

The full [[axiom of choice]] for $\Sigma$-open entire relations says that for any set $A$ and $B$ and any entire $\Sigma$-open relation $R:A \times B \to \Sigma$ from $A$ to $B$ there exists a function $f:A \to B$ such that for all $x$ in $A$ $R(x, f(x)) = \top$.

\begin{lemma}
The [[axiom of choice]] for $\Sigma$-open entire relations implies LPO. 
\end{lemma}

\begin{proof}
The [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] implies the [[axiom of choice]] for $\Sigma$-open entire relations to the [[boolean domain]] stated above, which in turn implies LPO. 
\end{proof}

\begin{theorem}
The [[full bar theorem]] implies the LPO
\end{theorem}

#### Constructive ordinals

There are also some results from constructive [[ordinal]] theory:

\begin{theorem}
If every pair of [[ordinals]] $\alpha$ and $\beta$ has a binary [[meet]], then LPO holds. 
\end{theorem}

\begin{proof}
See the proof of Proposition 5.2 in [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26). 
\end{proof}

\begin{theorem}
If binary [[joins]] exist for non-successor [[ordinals]] $\alpha$ and $\beta$, then LPO holds. 
\end{theorem}

\begin{proof}
See the proof of Proposition 6.2 in [de Jong, Kraus, Mohammadzadeh, & Forsberg 2026](#JKMF26). 
\end{proof}

#### Cubical objects

In [[triangulated type theory]], certain properties of the [[directed interval]] imply the LPO. 

\begin{theorem}
Suppose that the [[directed interval]] $\mathbb{I}$ is a [[sigma-frame|$\sigma$-frame]]. Then LPO holds. 
\end{theorem}

\begin{proof}
Suppose that $\mathbb{I}$ is a [[sigma-frame|$\sigma$-frame]]. Then the [[discrete]] [[coreflection]] $\flat \mathbb{I}$ is also a $\sigma$-frame, and since $\flat \mathbb{I}$ is in [[bijection]] with the [[boolean domain]] in triangulated type theory, this implies LPO in the discrete mode of simplicial type theory. Triangulated type theory satisfies the [[axiom of cohesion|axiom of $\mathbb{I}$-coheson]]: every discrete type is $\mathbb{I}$-null, which implies the [[axiom of punctual cohesion]] because $\mathbb{I}$ is a [[pointed type]]. Finally, by an adaptation of theorem 8.29 of [Shulman 2018](#Shulman18), punctual cohesion and LPO in the discrete mode implies LPO in the non-discrete mode. 
\end{proof}

### Statements inconsistent with LPO

There are various statements in mathematics which are inconsistent with LPO. 

\begin{theorem}
LPO is inconsistent with [[canonicity]] or [[homotopy canonicity]] in [[dependent type theory]]. 
\end{theorem}

\begin{proof}
By LPO, we can define the sequence $f:\mathbb{N} \to \mathbb{2}$ to the booleans $\mathbb{2}$ by $f(n) = 1$ if $2 n + 2$ is the sum of two [[prime numbers]] and $f(n) = 0$ if $2 n + 2$ is not the sum of two prime numbers, since $2 n + 2$ being the sum of two prime numbers is a [[decidable proposition]]. Then [[Goldbach's conjecture]] states that the $f$ is equal to the constant sequence $\lambda n:\mathbb{N}.1$, and we can define a term $\mathrm{LPO}(\mathrm{Goldbach}, 0, 1):\mathbb{N}$ which is 0 or 1 according as the Goldbach conjecture is true or false. This term is not [[identification|identified with]] a [[canonical form]] (a numeral), contradicting [[homotopy canonicity]] and by extension [[canonicity]].
\end{proof}

\begin{theorem}
LPO is inconsistent with [[Brouwer's continuity principle]] for any one of the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[HoTT book real numbers]] $\mathbb{R}_H$, or the [[Dedekind real numbers]] $\mathbb{R}_\Sigma$ defined using the initial $\sigma$-frame $\Sigma$. 
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

\begin{theorem}
LPO is inconsistent with [[Phoa's principle]] for the [[initial sigma-frame|initial $\sigma$-frame]] $\Sigma$. 
\end{theorem}

\begin{proof}
LPO is equivalent to the fact that the unique [[distributive lattice]] [[homomorphism]] from the [[boolean domain]] to the initial $\sigma$-frame $\Sigma$ is an [[isomorphism]]. However, the [[logical negation]] function $x \mapsto \neg x$ on the [[boolean domain]] does not satisfy the linear interpolation condition for Phoa's principle for the booleans; it is not true that $\neg x = (\neg 0) \wedge (x \vee \neg 1) = 1 \wedge (x \vee 0) = x$ on the booleans. As a result, LPO is inconsistent with Phoa's principle for the initial $\sigma$-frame $\Sigma$. 
\end{proof}

\begin{lemma}
LPO is inconsistent with synthetic quasi-coherence (i.e. the [[Kock-Lawvere axiom]]) for the [[initial sigma-frame|initial $\sigma$-frame]] $\Sigma$; that is, let $A$ be a finitely presented $\Sigma$-algebra, in the sense that $A$ is a [[distributive lattice]] equivalent to the quotient of $\Sigma[x_1 \ldots x_n]$ by finitely many relations, and let $\mathrm{Spec}_\Sigma(A)$ be the set of $\Sigma$-algebra homomorphisms. Then the canonical lattice homomorphism

$$a \mapsto (f \mapsto f(a)):A \to \Sigma^{\mathrm{Spec}_\Sigma(A)}$$

is an [[isomorphism]]
\end{lemma}

\begin{proof}
Synthetic quasi-coherence for the [[initial sigma-frame|initial $\sigma$-frame]] $\Sigma$ implies [[Phoa's principle]] for $\Sigma$, and so is thus inconsistent with LPO.  
\end{proof}

\begin{corollary}
The [[directed interval]] $\mathbb{I}$ is not the [[initial sigma-frame|initial $\sigma$-frame]] in [[triangulated type theory]]. 
\end{corollary}

\begin{proof}
The directed interval $\mathbb{I}$ satisfies [[Phoa's principle]] in [[triangulated type theory]], while the directed interval $\mathbb{I}$ being a $\sigma$-frame implies LPO as proven above. LPO then implies that the [[initial sigma-frame |initial$\sigma$-frame]] $\Sigma$ is the [[boolean domain]], and it is inconsistent for the boolean domain to satisfy [[Phoa's principle]] because of the [[negation]] [[endofunction]] on the boolean domain. 
\end{proof}

\begin{theorem}
LPO is inconsistent with the existence of a [[Specker sequence]]. 
\end{theorem}

See [Diener 2018](#Diener18) for more statements that are inconsistent with LPO. 

## Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO$ holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* LPO fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the modulated Cauchy reals and Dedekind reals coincide in this topos. 

* LPO fails in the parameterized [[realizability topos]] constructed in [Bauer & Hanson 2024](#BauerHanson24). 

* It appears that a [[realizability topos]] based on infinite-time [[Turing machine]]s validates $LPO$ but not $EM$; see [Bauer (2011)](#Bauer11). 

## In the internal logic

In [[set theory]], there are actually two different notions of logic: there is the external predicate logic used to define the set theory itself, and there is the internal predicate logic induced by the set operations on [[subsingletons]] and [[injections]]. In particular, 

* An internal *[[proposition]]* is a set $P$ such that for all elements $x \in A$ and $y \in A$, $x = y$. 

* The internal proposition *[[true]]* is a [[singleton]] $\top$. 

* The internal proposition *[[false]]* is the [[empty set]]

* The internal conjunction of two internal propositions $P$ and $Q$ is the [[cartesian product]] $P \times Q$ of $P$ and $Q$. 

* The internal disjunction of two internal propositions $P$ and $Q$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_{P \uplus Q}:P \uplus Q \to 1$ from the [[disjoint union]] of $P$ and $Q$ to the [[singleton]] $\top$. 

$$P \vee Q = \mathrm{im}(!_{P \uplus Q})$$

* The internal implication of two internal propositions $P$ and $Q$ is the [[function set]] $P \to Q$ between $P$ and $Q$. 

* The internal negation of an internal proposition $P$ is the function set from $P$ to the [[empty set]]

$$\neg P = P \to \emptyset$$

* An internal proposition $P$ is a [[decidable proposition]] if it comes with a function $\chi_P:P \to 2$ from $P$ to the [[boolean domain]] $2$. 

* An *internal predicate* on a set $A$ is a [[set]] $P$ with [[injection]] $i:P \hookrightarrow A$, whose family of propositions indexed by $x \in A$ is represented by the [[preimages]] $i^*(x)$.

* The internal [[existential quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[image]] of the [[uniqueness quantifier|unique]] function $!_P:P \to \top$ into the singleton $\top$.

$$\exists_A P = \im(!_P)$$

* The internal [[universal quantifier]] of an internal predicate $i:P \hookrightarrow A$ is the [[dependent product]] of the preimages
 
$$\forall_A P = \{f \in P^A \vert \forall x \in A, f(x) \in i^*(x) \}$$

* An internal predicate $i:P \hookrightarrow A$ is a [[decidable proposition]] if it comes with a function $\chi_P(x):i^*(x) \to 2$ into the [[boolean domain]] for all elements $x \in A$, or equivalently if it comes with a function $\chi_P:A \to 2$ from $A$ to the [[boolean domain]] $2$. 

Then the **internal LPO** says that:

* For any internal predicate $i:P \hookrightarrow \mathbb{N}$, if there is a function $\chi_P:\mathbb{N} \to 2$, then the internal existential quantification of $P$, $\exists_{\mathbb{N}} P = \im(!_P)$ has a function $(\exists_{\mathbb{N}} P) \to 2$ into the boolean domain. 

or equivalently, as

* For any function $a:\mathbb{N} \to 2$, the internal existential quantification of $P = \{x \in \mathbb{N} \vert a(x) = 1\}$, $\exists_{\mathbb{N}} P = \im(!_P)$ has a function $(\exists_{\mathbb{N}} P) \to 2$ into the boolean domain. 

The internal versions of the limited principles of omniscience, like all internal versions of axioms, are weaker than the external version of the limited principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in \mathbb{N} \vdash P(x)$ to an internal predicate $\{x \in \mathbb{N} \vert P(x)\} \hookrightarrow \mathbb{N}$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## Generalizations

### Choiceless limited principle of omniscience

There is a generalization of the limited principle of omniscience defined in [King 2024](#King24), which was suggested to be called the **choiceless limited principle of omniscience**. The choiceless limited principle of omniscience states that given and a pair of [[predicates]] $P$ and $Q$ on $\mathbb{N}$ such that $P(x) \vee Q(x)$ holds for all $x \in \mathbb{N}$, then either there exists $x \in \mathbb{N}$ such that $P(x)$ or for all $x \in \mathbb{N}$, $Q(x)$. The idea behind the term "choiceless" is that one isn't forced to choose between $P(x)$ or $Q(x)$ in this version of the limited principle of omniscience. One gets back the usual limited principle of omniscience if $P(x)$ and $Q(x)$ are [[mutually exclusive propositions]] for all $x \in A$, from which $Q(x)$ [[if and only if]] $\neg P(x)$ for all $x \in \mathbb{N}$. 

We can also state the principle set-theoretically. The __choiceless limited principle of omniscience__ states that given [[subsets]] $P, Q \in \mathcal{P}(\mathbb{N})$, if $P \cup Q = \mathbb{N}$, then either $P$ is [[inhabited subset|inhabited]] or $Q = \mathbb{N}$. One gets back the usual limited principle of omniscience if $P$ and $Q$ are [[disjoint subsets]] $P \cap Q = \emptyset$, from which $Q = \bar{P}$, where $\bar{P}$ is the [[complement]] of $P$. 

The choiceless limited principle of omniscience implies the [[analytic limited principle of omniscience]] for all sets of [[real numbers]], as shown in [King 2024](#King24), thus also implying that the real numbers coincide with each other. 

### Generalizations to other domain of discourses

One can consider generalizing the [[domain of discourse]] of the limited principle of omniscience from the [[natural numbers]] to an arbitrary [[set]] $A$. The __limited principle of omniscience__ for set $A$ ($\mathrm{LPO}_A$) states that the [[existential quantification]] of any [[decidable proposition]] on $A$ is again decidable.  That is,
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in A, P(x)) \vee \neg(\exists x \in A, P(x)) ,$$
or equivalently
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in A, P(x)) \vee (\forall x \in A, \neg{P(x)}) .$$

If you take the domain of discourse to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the constantly [[true]] proposition, then the subsingleton is decidable follows, since $\forall x \in A, P(x)$ holds, then either the subsingleton is [[inhabited set|inhabited]], in which $\exists x \in A, P(x)$ holds, or the subsingleton is [[empty set|empty]], in which $\forall x \in A, \neg P(x)$ holds. Thus, that $LPO$ holds for all subsingletons implies $EM$; conversely, $EM$ implies $LPO$ (over any domain). Note that propositions of the form $\exists x, P(x)$ when $P$ is decidable are the [[open truth values]] in the [[Rosolini dominance]].

We can also state the principle set-theoretically: given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that given a [[subset]] $P \in \mathcal{P}(A)$, if $P$ is a [[decidable subset]] of $A$ ($P \cup \bar{P} = A$), then either $P$ is [[inhabited subset|inhabited]] or $\bar{P} = A$, where $\bar{P}$ is the [[complement]] of $P$. 

One can equivalently use functions to the [[boolean domain]] instead of [[decidable subsets]]. Given a [[set]] $A$, the __limited principle of omniscience for $A$__ states that given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. Then Bishop\'s $LPO$ is $LPO_{\mathbb{N}}$, which applies to any [[infinite sequence]] of [[bits]]. Similarly here, if $A$ is a [[subsingleton]] corresponding to a given [[truth value]] and this principle is applied to the constant function at $1$, then the subsingleton $A$ is decidable, since if $\forall x. f(x) = 1$ holds, then either the subsingleton is [[inhabited set|inhabited]], in which $\exists x. f(x) = 1$ holds, or the subsingleton is [[empty set|empty]], in which $\forall x.f(x) = 0$ holds. 

While $LPO$ for $\mathbb{N}$ is a classic example of the difference between constructive and classical mathematics, $LPO$ holds for the set $\overline{\mathbb{N}}$ of [[extended natural number]]s; this is related to the fact that $\overline{\mathbb{N}}$ may constructively be given a [[compact space|compact]] topology. See [Escard&#243; (2011)](#Escardo11) for this and much more.

#### LPO for all subsingletons

There is a [[constant function]] $x \mapsto 1$ from every subsingleton $A$ to the [[boolean domain]] $\mathbb{2}$ taking every element $x \in A$ to the boolean $1 \in \mathbb{2}$. 

\begin{theorem}
Given a [[subsingleton]] $A$, suppose that $\mathrm{LPO}_A$ holds: either there exists $x \in A$ such that $(x \mapsto 1)(x) = 1$, or for all $x \in A$, $(x \mapsto 1)(x) = 0$. Then $A$ is a [[decidable subsingleton]]. 
\end{theorem}

\begin{proof}
We prove by case analysis. 

Suppose that there exists $x:A$ such that $(x \mapsto 1)(x) = 1$. Then $A$ is a [[inhabited set|inhabited]] subsingleton and thus a decidable subsingleton. 

Then suppose that for all $x:A$, $(x \mapsto 1)(x) = 0$. Then $A$ is [[empty set|empty]] and thus a decidable subsingleton. 

This exhausts all options for decidable subsingletons, and exhausts all possible conditions in the hypothesis. 
\end{proof}

\begin{theorem}
Suppose that for sets $A$ and $B$ with [[decidable tight apartness relations]], the [[tight apartness relation]] on the function set $B^A$, defined by $f \# g \coloneqq \exists x:A.f(x) \neq g(x)$, is decidable. Then [[excluded middle]] holds. 
\end{theorem}

\begin{proof}
Every [[subsingleton]] $A$ has a [[decidable tight apartness relation]] where $x \# y$ is always [[false]]. The [[boolean domain]] $\mathbb{2}$ also has a decidable tight apartness relation where $x \# y$ is given by the [[denial inequality]] $x \neq y$. We proved earlier in the article that $\mathrm{LPO}_A$ is equivalent to the tight apartness relation on the function set $\mathbb{2}^A$ being decidable, and $\mathrm{LPO}_A$ implies that every subsingleton $A$ is a decidable subsingleton, which is precisely the condition of [[excluded middle]]. 
\end{proof}

There is also a [[constant function]] $x \mapsto 0$ from every subsingleton $A$ to the [[boolean domain]] $\mathbb{2}$ taking every element $x \in A$ to the boolean $0 \in \mathbb{2}$. 

\begin{theorem}
Given a [[subsingleton]] $A$, suppose that either there exists $x \in A$ such that $(x \mapsto 1)(x) \neq (x \mapsto 0)(x)$, or for all $x \in A$, $(x \mapsto 1)(x) = (x \mapsto 0)(x)$. Then $A$ is a [[decidable subsingleton]]. 
\end{theorem}

\begin{proof}
We prove by case analysis. 

Suppose that there exists $x \in A$ such that $(x \mapsto 1)(x) \neq (x \mapsto 0)(x)$. Then $A$ is a [[inhabited set|inhabited]] subsingleton and thus a decidable subsingleton. 

Then suppose that for all $x \in A$, $(x \mapsto 1)(x) = (x \mapsto 0)(x)$. Then $A$ is [[empty set|empty]] and thus a decidable subsingleton, since $(x \mapsto 1) = (x \mapsto 0)$ by [[function extensionality]]. 

This exhausts all options for decidable subsingletons, and exhausts all possible conditions in the hypothesis. 
\end{proof}

#### Universe of types satisfying LPO

In [[dependent type theory]], given a [[univalent Tarski universe]] $(U, T)$, one can construct the universe of all types in $U$ which satisfy the limited principle of omniscience:

$$U_\mathrm{LPO} \coloneqq \sum_{A:U} \prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee
\left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

Since the type 

$$\prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee
\left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

is a [[mere proposition]] for all $A:U$, $U_\mathrm{LPO}$ is a [[subtype|sub]]-[[universe]] of $U$. 

### Generalizations to other sets of propositions

One can also consider generalizing from the [[decidable propositions]] to other types of propositions. Let $\Sigma$ be a [[subobject|sub]][[lattice]] of the [[frame of truth values]] $\Omega$. Then for a given set $A$, the __limited principle of omniscience__ $\mathrm{LPO}_{A, \Sigma}$ states that, given any [[function]] $f$ from $A$ to $\Sigma$, there exists an element $p \in \Sigma$ such that $p = \top$ [[if and only if]] there exists an element $x \in A$ such that $f(x) = \top$. 

$$\forall f:A \to \Sigma.\exists p \in \Sigma.p = \top \iff \exists x \in A.f(x) = \top$$

The usual limited principle of omniscience is then $\mathrm{LPO}_{\mathbb{N}, \mathbb{2}}$ for the [[booleans]] $\mathbb{2}$:
$$\forall f:\mathbb{N} \to \mathbb{2}.\exists p \in \mathbb{2}.(p = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$
Now by recursion of the booleans we have either that $p = \bot$ or $p = \top$, so the statement 
$$\forall f:\mathbb{N} \to \mathbb{2}.\exists p \in \mathbb{2}.(p = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$ 
is equivalent to 
$$\forall f:\mathbb{N} \to \mathbb{2}.(\top = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top) \vee (\bot = \top) \iff (\exists x \in \mathbb{N}.f(x) = \top)$$
and since $\top = \top$ is true and $\bot = \top$ is false, we have
$$\forall f:\mathbb{N} \to \mathbb{2}.(\exists x \in \mathbb{N}.f(x) = \top) \vee \neg (\exists x \in \mathbb{N}.f(x) = \top)$$
which is precisely the usual limited principle of omniscience.

For the [[natural numbers]] $\mathbb{N}$ and the set of [[semi-decidable propositions]] $\Sigma_0^1$, the limited principle of omniscience $\mathrm{LPO}_{\mathbb{N}, \Sigma_0^1}$ is equivalent to the [[Rosolini dominance]] being a [[dominance]] and the [[Cauchy real numbers]] being [[Dedekind complete]] via [[semi-decidable]] [[Dedekind cuts]]. 

For the set of truth values $\Omega$, the limited principle of omniscience $\mathrm{LPO}_{A, \Omega}$ is always true for set $A$ because $\Omega$ is a [[frame]] and thus closed under existential quantification over $A$. 

## Related concepts

* [[principle of omniscience]]

* [[weak limited principle of omniscience]]

* [[lesser limited principle of omniscience]]

* [[Markov's principle]]

* [[excluded middle]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Mandelkern82} [[Mark Mandelkern]], *Components of an open set*, Journal of the Australian Mathematical Society, Volume 33, Issue 2, October 1982, pp. 249 - 261, &lbrack;[doi:10.1017/S1446788700018383](https://doi.org/10.1017/S1446788700018383), [pdf](https://www.cambridge.org/core/services/aop-cambridge-core/content/view/87B279B7B200821168EC5A5A4BE62A4E/S1446788700018383a.pdf/components-of-an-open-set.pdf)&rbrack;

* {#Mandelkern88} [[Mark Mandelkern]]: *Limited Omniscience and the Bolzano-Weierstrass Principle*, Bulletin of the London Mathematical Society **20** 4 (1988) 319--320, &lbrack;[doi:10.1112/blms/20.4.319](https://doi.org/10.1112/blms/20.4.319), [pdf](https://www.zianet.com/mandelkern/mandelkern_bwp.pdf)&rbrack;

* {#Richman91} [[Fred Richman]], *Polynomials and linear transformations*. Linear Algebra and its Applications, Volume 131, 1 April 1990, Pages 131-137. &lbrack;<a href="https://doi.org/10.1016/0024-3795(90)90379-Q">doi:10.1016/0024-3795(90)90379-Q</a>&rbrack;

* {#Ishihara06} [[Hajime Ishihara]]: _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS **6** (2006) &lbrack;[doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406), [pdf](https://philosophiascientiae.revues.org/pdf/406)&rbrack;

* {#Tanaka07} [[Yasuhito Tanaka]]: *The Gibbard–Satterthwaite theorem of social choice theory in an infinite society and LPO (limited principle of omniscience)*, Applied Mathematics and Computation **193** 2 (2007) 475--481 &lbrack;[doi:10.1016/j.amc.2007.04.001](https://doi.org/10.1016/j.amc.2007.04.001), [pdf archived](https://web.archive.org/web/20211011144745/http://hokuriku.me/kiishimizu/pdf/AMC12363.pdf)&rbrack;

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Rathjen13} [[Michael Rathjen]], *Constructive Zermelo-Fraenkel set theory and the limited principle of omniscience*. &lbrack;[arXiv:1302.3037](https://arxiv.org/abs/1302.3037)&rbrack;

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Diener18} [[Hannes Diener]], *Constructive reverse mathematics*, Habilitationsschrift Fakultät IV - Naturwissenschaftlich-Technische Fakultät, 2018. ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))

* {#Booij20} [[Auke Booij]], *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#Bauer21} [[Andrej Bauer]], *Instance reducibility and Weihrauch degrees*, Logical Methods in Computer Science, August 9, 2022, Volume 18, Issue 3, &lbrack;<a href="https://doi.org/10.46298/lmcs-18(3:20)2022">doi:10.46298/lmcs-18(3:20)2022</a>,[arXiv:2106.01734](https://arxiv.org/abs/2106.01734), [pdf](https://lmcs.episciences.org/9906/pdf)&rbrack;

* {#Ciraulo22} Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#BirchfieldSwan24} Madeleine Birchfield, Andrew Swan (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#BauerHanson24} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

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

[[!redirects internal LPO]]
[[!redirects internal limited principle of omniscience]]
[[!redirects internal limited principles of omniscience]]

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