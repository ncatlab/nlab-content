
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

## Definition

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] is again decidable.  That is,
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee \neg(\exists x, P(x)) ,$$
or equivalently
$$ (\forall x, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x, P(x)) \vee (\forall x, \neg{P(x)}) .$$

We have not stated the domain of quantification of the variable $x$. If you take it to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the constantly [[true]] proposition, then the subsingleton is decidable follows, since $\forall x, P(x)$ holds, then either the subsingleton is [[inhabited set|inhabited]], in which $\exists x, P(x)$ holds, or the subsingleton is [[empty set|empty]], in which $\forall x, \neg P(x)$ holds. Thus, that $LPO$ holds for all subsingletons implies $EM$; conversely, $EM$ implies $LPO$ (over any domain). However, Bishop\'s $LPO$ takes the domain to be the set of [[natural numbers]], giving a weaker principle than $EM$.  (It appears that a [[realizability topos]] based on infinite-time [[Turing machine]]s validates $LPO$ but not $EM$; see [Bauer (2011)](#Bauer11).)  Note that propositions of the form $\exists x, P(x)$ when $P$ is decidable are the [[open truth values]] in the [[Rosolini dominance]].

We can also state the principle set-theoretically, with explicit reference to the domain of quantification.  Given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that, given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. Then Bishop\'s $LPO$ is $LPO_{\mathbb{N}}$, which applies to any [[infinite sequence]] of [[bits]]. Similarly here, if $A$ is a [[subsingleton]] corresponding to a given [[truth value]] and this principle is applied to the constant function at $1$, then the subsingleton $A$ is decidable, since if $\forall x. f(x) = 1$ holds, then either the subsingleton is [[inhabited set|inhabited]], in which $\exists x. f(x) = 1$ holds, or the subsingleton is [[empty set|empty]], in which $\forall x.f(x) = 0$ holds. 

While $LPO$ for $\mathbb{N}$ is a classic example of the difference between constructive and classical mathematics, $LPO$ holds for the set $\overline{\mathbb{N}}$ of [[extended natural number]]s; this is related to the fact that $\overline{\mathbb{N}}$ may constructively be given a [[compact space|compact]] topology. See [Escard&#243; (2011)](#Escardo11) for this and much more.

### Using exclusive disjunction

There is an equivalent version of the limited principle of omniscience which uses the [[exclusive disjunction]] instead of the inclusive [[disjunction]] for the definition of a [[decidable proposition]]:

The __limited principle of omniscience__ ($LPO$) states that the [[existential quantification]] of any [[decidable proposition]] on a sete $A$ is again decidable.  That is,
$$ (\forall x \in A, P(x) \underline{\vee} \neg{P(x)}) \Rightarrow (\exists x \in A, P(x)) \underline{\vee} \neg(\exists x \in A, P(x)) ,$$
or equivalently
$$ (\forall x \in A, P(x) \underline{\vee} \neg{P(x)}) \Rightarrow (\exists x, P(x)) \underline{\vee} (\forall x, \neg{P(x)}) .$$

We can also state the principle set-theoretically, with explicit reference to the domain of quantification.  Given a [[set]] $A$, the __limited principle of omniscience for $A$__ ($LPO_A$) states that, given any [[function]] $f$ from $A$ to the [[boolean domain]] $\{0,1\}$, either $f$ is the [[constant map]] to $0$ or $1$ belongs to the [[image]] of $f$. That is, 
$$ \forall f \in \{0,1\}^A, (\exists x \in A, f(x) = 1) \underline{\vee} \neg(\exists x \in A, f(x) = 1) ,$$
or equivalently
$$ \forall f \in \{0,1\}^A, (\exists x \in A, f(x) = 1) \underline{\vee} (\forall x \in A, f(x) = 0) .$$

### In dependent type theory

In the context of [[dependent type theory]], the usual limited principle of omniscience for a type $A$ is expressed as 

$$\prod_{f:A \to \mathbb{2}} \left[\left[\sum_{x:A} f(x) = 1\right] + \prod_{x:A} f(x) = 0\right]$$

However, there are in general two ways of interpreting predicate logic, the traditional interpretation using [[propositional truncations]], and the [[BHK interpretation]] which do not use propositional truncations. This results in four different versions of the limited principle of omniscience of $A$, depending on whether the [[existential quantifier]] is truncated or untruncated, and whether the [[disjunction]] is truncated or untruncated:

* the usual $\mathrm{LPO}_A$ states that 

$$\prod_{f:A \to \mathbb{2}} \left[\left[\sum_{x:A} f(x) = 1\right] + \prod_{x:A} f(x) = 0\right]$$

* the **disjunction-untruncated limited principle of omniscience for $A$** states that

$$\prod_{f:A \to \mathbb{2}} \left(\left[\sum_{x:A} f(x) = 1\right] + \prod_{x:A} f(x) = 0\right)$$

* the **quantifier-untruncated limited principle of omniscience for $A$** states that

$$\prod_{f:A \to \mathbb{2}} \left[\left(\sum_{x:A} f(x) = 1\right) + \prod_{x:A} f(x) = 0\right]$$

* the **fully untruncated limited principle of omniscience for $A$** states that

$$\prod_{f:A \to \mathbb{2}} \left(\left(\sum_{x:A} f(x) = 1\right) + \prod_{x:A} f(x) = 0\right)$$

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if the disjunction-untruncated $\mathrm{LPO}_A$ holds. 
\end{theorem}

\begin{proof}
By the equivalence of the definitions of [[decidable proposition]] using inclusive disjunction and exclusive disjunction, the versions of the $\mathrm{LPO}_A$ using inclusive and exclusive disjunctions are equivalent to each other. 

In dependent type theory, the [[exclusive disjunction]] of two types is formulated as the [[dependent sum type]]: 

$$A \underline{\vee} B \coloneqq \sum_{x:A + B} \prod_{y:A + B} x =_{A + B} y$$

The first projection function of the dependent sum types yields a function 

$$\pi_1:(A \underline{\vee} B) \to A + B$$

meaning that the $\mathrm{LPO}_A$ using exclusive disjunction implies the disjunction-untruncated $\mathrm{LPO}_A$. Finally, the disjunction-untruncated $\mathrm{LPO}_A$ implies the $\mathrm{LPO}_A$ using inclusive disjunction by the properties of [[propositional truncations]]. 

Thus, $\mathrm{LPO}_A$ holds if anad only if the disjunction-untruncated $\mathrm{LPO}_A$ holds. 
\end{proof}

## Properties

### LPO for a general set

Assuming an arbitrary set $A$, 

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if for every function $f:A \to \mathbb{N}$ from $A$ to the [[natural numbers]], either there exists an element $x$ in $A$ and a natural number $n$ such that $f(x) = n + 1$, or for all elements $x$ in $A$, $f(x) = 0$. 
\end{theorem}

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if the [[boolean domain]] is the [[initial object|initial]] $A$-overt $\emptyset$-overt [[dominance]]. 
\end{theorem}

Now, let us define an $A$-[[complete lattice]] to be a lattice which has all $A$-indexed joins, a lattice $L$ with a function 

$$\bigvee_{t:A} (-)(t):(A \to L) \to L$$

such that for all elements $x \in A$ and functions $f:A \to L$, 

$$f(x) \leq \bigvee_{t:A} f(t)$$

and for all elements $y \in L$ and functions $f:A \to L$, if $f(x) \leq y$ for all elements $x \in A$, then 

$$\bigvee_{t:A} f(t) \leq y$$

and let us define an $A$-[[frame]] to be a $A$-[[complete lattice]] in which meets distribute over the $A$-indexed joins: for all elements $x \in L$ and functions $f:A \to L$, 

$$a \wedge \bigvee_{t:A} f(t) = \bigvee_{t:A} a \vee f(t)$$

We say that a $A$-[[frame homomorphism]] is a lattice homomorphism which also preserves $A$-indexed joins. 

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if the [[boolean domain]] is the [[initial object|initial]] $A$-frame; i.e. the [[boolean domain]] is an $A$-frame and for every other $A$-frame $L$, [[uniqueness quantifier|there is a unique]] $A$-frame homomorphism from the [[boolean domain]] to $L$. 
\end{theorem}

When the set $A$ is the [[natural numbers]] $\mathbb{N}$, this yields the familiar theorem that $\mathrm{LPO}_\mathbb{N}$ holds if and only if the [[boolean domain]] is the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]]. 

The next statement relate the $\mathrm{LPO}_A$ with the axiom that [[tight apartness relation]] on the [[function set]] $\mathbb{2}^A$ is a [[decidable tight apartness]]. 

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if the [[function set]] $\mathbb{2}^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{2}^A$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

\begin{proof}
Given a set $A$, since the [[boolean domain]] is a [[boolean ring]], the function set $\mathbb{2}^A$ is also a [[boolean ring]] via pointwise addition, subtraction and multiplication of [[boolean-valued functions]]. Thus, for functions $f$ and $g$ from $A$ to $\mathbb{2}$, the [[tight apartness relation]] on the function set $\mathbb{2}^A$, defined by 
$$f \# g \coloneqq \exists x:A.f(x) \neq g(x)$$ 
is logically equivalent to $\exists x:A.f(x) - g(x) = 1$, since $f(x) \neq g(x)$ is logically equivalent to $f(x) = g(x) + 1$. 

Suppose $\mathrm{LPO}_A$ holds. Then for functions $f$ and $g$ from $A$ to $\mathbb{2}$, define the function $h$ by $h(x) = f(x) - g(x)$ for all $x \in A$. Then since $\mathrm{LPO}_A$ says that $\exists x:A.h(x) = 1$ is decidable, and $\exists x:A.h(x) = 1$ is logically equivalent to $f \# g$, then $f \# g$ is decidable. 

Conversely, assume that $f \# g$ is decidable. Then take $g$ to be the constant function at the boolean $0$, and $f \# \lambda x:A.0$ is logically equivalently to $\exists x:A.f(x) - 0 = 1$ and thus $\exists x:A.f(x) = 1$. Since $f \# g$ is decidable, then $\exists x:A.f(x) = 1$ is decidable, which is $\mathrm{LPO}_A$. 
\end{proof}

The next two statements relate the $\mathrm{LPO}_A$ with axioms that the [[tight apartness relation]] on certain other [[function sets]] are a [[decidable tight apartness]]. 

\begin{theorem}
More generally, given a [[finite set]] $S$ of [[cardinality]] $n \gt 1$, $\mathrm{LPO}_A$ holds if and only if that the [[function set]] $S^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $S^A$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

\begin{theorem}
$\mathrm{LPO}_A$ holds if and only if the [[function set]] $\mathbb{N}^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{N}^A$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

### LPO for all subsingletons

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

### Universe of types satisfying LPO

In [[dependent type theory]], given a [[univalent Tarski universe]] $(U, T)$, one can construct the universe of all types in $U$ which satisfy the limited principle of omniscience:

$$U_\mathrm{LPO} \coloneqq \sum_{A:U} \prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee
\left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

Since the type 

$$\prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee
\left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

is a [[mere proposition]] for all $A:U$, $U_\mathrm{LPO}$ is a [[subtype|sub]]-[[universe]] of $U$. 

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

Then the **internal LPO** for a [[family of sets]] $(A_z)_{z \in I}$ is the LPO for each $A_z$ stated in the internal logic of the set theory:

* For any internal predicate $i:P \hookrightarrow A_z$, if there is a function $\chi_P:A_z \to 2$, then the internal existential quantification of $P$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

or equivalently, as

* For any function $a:A_z \to 2$, the internal existential quantification of $P = \{x \in A_z \vert a(x) = 1\}$, $\exists_{A_z} P = \im(!_P)$ has a function $(\exists_{A_z} P) \to 2$ into the boolean domain. 

In particular, the internal LPO for the family of all [[subsingletons]] is internal excluded middle. Similarly, given a [[universe]] $U$, the internal LPO for the family of all sets in $U$ is excluded middle in $U$. 

The internal versions of the limited principles of omniscience, like all internal versions of axioms, are weaker than the external version of the limited principle of omniscience, since while [[bounded separation]] implies that one can convert any external predicate $x \in A \vdash P(x)$ on a set $A$ to an internal predicate $\{x \in A \vert P(x)\} \hookrightarrow A$, it is generally not possible to convert an internal predicate to an external predicate without a reflection rule which turns subsingletons in the set theory into propositions in the external logic. 

## LPO for the natural numbers

The term "limited principle of omniscience", without any specification of the set for which LPO holds, usually refers to the limited principle of omniscience for the natural numbers $\mathrm{LPO}_\mathbb{N}$. 

### Statements equivalent to $\mathrm{LPO}_\mathbb{N}$

Apart from the equivalent statements stated above for the LPO for a general set $A$, there are various other results that are equivalent specifically to the limited principle of omniscience for the natural numbers. 

Let us begin with the equivalence of the various truncated versions of the $\mathrm{LPO}_\mathbb{N}$ with the usual untruncated version of the $\mathrm{LPO}_\mathbb{N}$. 

\begin{theorem}
The $\mathrm{LPO}_\mathbb{N}$ implies the disjunction-untruncated $\mathrm{LPO}_\mathbb{N}$.  
\end{theorem}

\begin{theorem}
Given a sequnece of booleans $f:\mathbb{N} \to \mathbb{2}$, the [[preimage]] of $f$ at the boolean $1$ has a [[choice operator]]. 
\end{theorem}

\begin{proof}
See [Rijke 2022](#Rijke22) for a proof of the statement in [[dependent type theory]]. 
\end{proof}

\begin{theorem}
The disjunction-untruncated $\mathrm{LPO}_\mathbb{N}$ implies the fully untruncated $\mathrm{LPO}_\mathbb{N}$.  
\end{theorem}

\begin{proof}
...
\end{proof}

\begin{theorem}
$\mathrm{LPO}_\mathbb{N}$ and fully untruncated $\mathrm{LPO}_\mathbb{N}$ are equivalent. 
\end{theorem}

Next, we have the equivalence of the $\mathrm{LPO}_\mathbb{N}$ with the [[analytic LPO]] for various notions of [[real numbers]]. 

\begin{theorem}
The [[analytic LPO]] for the following sets of real numbers are equivalent to the LPO for the [[natural numbers]]: the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[Escardo-Simpson real numbers]]/[[HoTT book real numbers]] $\mathbb{R}_E$/$\mathbb{R}_H$, and the subfield of [[Dedekind real numbers]] $\mathbb{R}_\Sigma \subseteq \mathbb{R}_D$ which are constructed out of [[Dedekind cuts]] valued in the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma \subseteq \Omega$. 
\end{theorem}

Let $C$ denote the [[category]] of [[discrete field|discrete]] [[sequentially Cauchy complete]] [[Archimedean ordered fields]]. $C$ is a [[groupoid]] and a [[subsingleton]] [[principle of equivalence|up to]] [[uniqueness quantifier|unique]] [[isomorphism]]: for every two [[objects]] $R \in C$ and $R' \in C$ there exists a unique [[morphism]] between $R$ and $R'$ which is an [[isomorphism]]. 

\begin{theorem}
LPO for the natural numbers holds if and only if there is an object $\mathbb{R} \in C$, which will necessarily be unique up to unique isomorphism, and LPO for the natural numbers fails if and only if $C$ is an [[empty category]]. 
\end{theorem}

There are other equivalent statements from [[real analysis]]:

\begin{theorem}
[[sequentially compact space|Sequential compactness]] of the [[unit interval]] holds if and only if $\mathrm{LPO}_\mathbb{N}$ holds. 
\end{theorem}

\begin{theorem}
Every [[Cauchy real number]] is a [[rational number]] or has an strictly non-repeating base $b$ radix expansion if and only if $\mathrm{LPO}_\mathbb{N}$ holds. 
\end{theorem}

\begin{theorem}
The [[Cauchy real numbers]] are isomorphic to the [[radix notation|radix expansion]] in any base (e.g., a decimal expansion or binary expansion) iff $\mathrm{LPO}_\mathbb{N}$ holds. 
\end{theorem}

\begin{proof}
See [Feldman (2010)](#Mehkeri10). 
\end{proof}

Here are a few others:

* Every [[semi-decidable proposition]] is a [[decidable proposition]] if and only if $\mathrm{LPO}_\mathbb{N}$ holds. 

* The [[p-adic integers|$p$-adic integers]] being a [[discrete integral domain]] and the [[p-adic rationals|$p$-adic rationals]] being a [[discrete field]] are both equivalent to $\mathrm{LPO}_\mathbb{N}$ 

* The [[ring]] of [[rational numbers|rational]] [[power series]] $\mathbb{Q}[[x]]$ being a [[discrete integral domain]] is equivalent to $\mathrm{LPO}_\mathbb{N}$. Similarly, the [[Heyting field]] of [[rational numbers|rational]] [[Laurent series]] $\mathbb{Q}((x))$ being a [[discrete field]] is equivalent to $\mathrm{LPO}_\mathbb{N}$. 

### Statements implied by $\mathrm{LPO}_\mathbb{N}$

There are various statements that are implied by $\mathrm{LPO}_\mathbb{N}$. 

\begin{theorem}
$\mathrm{WLPO}_\mathbb{N}$ follows from $\mathrm{LPO}_\mathbb{N}$, but not conversely. 
\end{theorem}

\begin{proof}
If $P(x)$ is a decidable proposition, then so is $\neg{P(x)}$, and so $\mathrm{LPO}_\mathbb{N}$ gives
$$(\exists x, \neg{P(x)}) \vee (\forall x, \neg{\neg{P(x)}}), $$
which implies
$$\neg(\forall x, P(x)) \vee (\forall x, P(x))$$
as $P$ is decidable.
\end{proof} 

\begin{theorem}
$\mathrm{LLPO}_\mathbb{N}$ follows from $\mathrm{LPO}_\mathbb{N}$, but not conversely. 
\end{theorem}

\begin{proof}
$\mathrm{LLPO}_\mathbb{N}$ follows from $\mathrm{LPO}_\mathbb{N}$, $\mathrm{WLPO}_\mathbb{N}$ is equivalent to fully untruncated $\mathrm{LLPO}_\mathbb{N}$, which implies $\mathrm{LLPO}_\mathbb{N}$, and $\mathrm{WLPO}_\mathbb{N}$ follows from $\mathrm{LPO}_\mathbb{N}$. However, the converse does not necessarily hold, since in <http://www1.maths.leeds.ac.uk/~rathjen/Lifschitz.pdf> is a model by Michael Rathjen that separates $\mathrm{WLPO}_\mathbb{N}$ from $\mathrm{LLPO}_\mathbb{N}$. Similarly, [Grossack 24](#Grossack24) shows that Johnstone's topological topos separates $\mathrm{WLPO}_\mathbb{N}$ from $\mathrm{LLPO}_\mathbb{N}$. Thus $\mathrm{LLPO}_\mathbb{N}$ is separated from $\mathrm{LPO}_\mathbb{N}$. 
\end{proof}

See [Diener 2018](#Diener18) for more statements that are implied by $\mathrm{LPO}_\mathbb{N}$. 

### Statements that imply $\mathrm{LPO}_\mathbb{N}$

There are various other statements that imply $\mathrm{LPO}_\mathbb{N}$. 

The existence of various [[classical mathematics|classical]] [[universes]] or models of [[foundations of mathematics]] implies the $\mathrm{LPO}_\mathbb{N}$: 

\begin{theorem}
Any model $\mathcal{V}$ of bounded Zermelo set theory contains a [[pure set]] of [[real numbers]] $\mathbb{R}$.
\end{theorem}

\begin{proof}
One can collect all the pure sets of $\mathcal{V}$ which are in $\mathbb{R}$ and show that the resulting set is a subset of $\mathcal{V}$ and a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. Thus, the existence of stronger models of [[material set theory]] such as [[ZFC]] also imply $\mathrm{LPO}_\mathbb{N}$ for the entire foundations.
\end{proof} 

\begin{theorem}
The existence of a constructively [[well-pointed topos|well-pointed]] [[Boolean topos|Boolean]] [[W-topos]] $\mathcal{E}$ implies the $\mathrm{LPO}_\mathbb{N}$.
\end{theorem}

\begin{proof}
The hom-set $\mathrm{Hom}_\mathcal{E}(1, \mathbb{R})$, where $1 \in \mathcal{E}$ is the [[terminal object|terminal]] [[generator]] and  $\mathbb{R} \in \mathcal{E}$ is the [[real numbers object]] in $\mathcal{E}$, yields a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. Thus, the existence of any constructive model of [[ETCS]] also implies $\mathrm{LPO}_\mathbb{N}$ for the entire foundations. 
\end{proof}

\begin{theorem}
In [[dependent type theory]], there being a [[univalent Tarski universe]] $(U, T)$ closed under dependent product types, dependent sum types, and identity types and satisfying the axiom of infinity and [[excluded middle]] implies the $\mathrm{LPO}_\mathbb{N}$. 
\end{theorem}

\begin{proof}
One can construct an element $\mathbb{R}:U$ representing the $U$-small type of real numbers, whose type reflection $T(\mathbb{R})$ is a sequentially Cauchy complete Archimedean ordered field which satisfies the [[analytic LPO]], thus implying $\mathrm{LPO}_\mathbb{N}$ for the entire type theory. Thus, any univalent Tarski universe which has [[axiom of choice]] or a [[choice operator]] for the types in the universe also implies $\mathrm{LPO}_\mathbb{N}$ for the entire type theory. 
\end{proof}

Note that in all these cases, the real numbers $\mathbb{R}$ constructed from these universes or classical models of foundations of mathematics, while equivalent to the internal Dedekind real numbers constructed in the universe or model, are not necessarily equivalent to the external [[Dedekind real numbers]] in the foundations. 

Let $\Sigma$ be the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]], which is the initial $\mathbb{N}$-overt [[dominance]]. The [[axiom of choice]] for $\Sigma$-open entire relations from set $A$ says that for any set $B$ and any entire $\Sigma$-open relation $R:A \times B \to \Sigma$ from $A$ to $B$ there exists a function $f:A \to B$ such that for all $x$ in $A$ $R(x, f(x)) = \top$.

\begin{theorem}
The [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] implies $\mathrm{LPO}_\mathbb{N}$. 
\end{theorem}

\begin{proof}
The proof is similar to one direction of the proof of the [[Diaconescu-Goodman-Myhill theorem]]. 

Let $P$ be a $\Sigma$-open proposition. Quotient the [[boolean domain]] $\mathbb{2}$ by the [[equivalence relation]] where $0 = 1$ [[if and only if]] $P$ holds, resulting in a set $A$. Then we have an $\Sigma$-open entire relation $R$ between $\mathbb{2}$ and $A$, and there existws a function $f:\mathbb{2} \to A$ such that $R(x, f(x)) = \top$ if and only if $P$ is a [[decidable proposition]], and that it holds for all such $P$ is precisely $\mathrm{LPO}_\mathbb{N}$. Thus, the [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] implies $\mathrm{LPO}_\mathbb{N}$. 
\end{proof}

The full [[axiom of choice]] for $\Sigma$-open entire relations says that for any set $A$ and $B$ and any entire $\Sigma$-open relation $R:A \times B \to \Sigma$ from $A$ to $B$ there exists a function $f:A \to B$ such that for all $x$ in $A$ $R(x, f(x)) = \top$.

\begin{lemma}
The [[axiom of choice]] for $\Sigma$-open entire relations implies $\mathrm{LPO}_\mathbb{N}$. 
\end{lemma}

\begin{proof}
The [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] implies the [[axiom of choice]] for $\Sigma$-open entire relations from the [[boolean domain]] stated above, which in turn implies $\mathrm{LPO}_\mathbb{N}$. 
\end{proof}

\begin{theorem}
The [[full bar theorem]] implies the $\mathrm{LPO}_\mathbb{N}$
\end{theorem}

See [Diener 2018](#Diener18) for more statements that imply $\mathrm{LPO}_\mathbb{N}$. 

### Statements inconsistent with $\mathrm{LPO}_\mathbb{N}$

There are various statements in mathematics which are inconsistent with $\mathrm{LPO}_\mathbb{N}$. 

\begin{theorem}
$\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[canonicity]] or [[homotopy canonicity]] in [[dependent type theory]]. 
\end{theorem}

\begin{proof}
By $\mathrm{LPO}_\mathbb{N}$, we can define the sequence $f:\mathbb{N} \to \mathbb{2}$ to the booleans $\mathbb{2}$ by $f(n) = 1$ if $2 n + 2$ is the sum of two [[prime numbers]] and $f(n) = 0$ if $2 n + 2$ is not the sum of two prime numbers, since $2 n + 2$ being the sum of two prime numbers is a [[decidable proposition]]. Then [[Goldbach's conjecture]] states that the $f$ is equal to the constant sequence $\lambda n:\mathbb{N}.1$, and we can define a term $\mathrm{LPO}(\mathrm{Goldbach}, 0, 1):\mathbb{N}$ which is 0 or 1 according as the Goldbach conjecture is true or false. This term is not [[identification|identified with]] a [[canonical form]] (a numeral), contradicting [[homotopy canonicity]] and by extension [[canonicity]].
\end{proof}

\begin{theorem}
$\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[Brouwer's continuity principle]] for any one of the [[Cauchy real numbers]] $\mathbb{R}_C$, the [[HoTT book real numbers]] $\mathbb{R}_H$, or the [[Dedekind real numbers]] $\mathbb{R}_\Sigma$ defined using the initial $\sigma$-frame $\Sigma$. 
\end{theorem}

\begin{proof}
$\mathrm{LPO}_\mathbb{N}$ implies that $\mathbb{R}_C$, $\mathbb{R}_H$, and $\mathbb{R}_\Sigma$ are equivalent to each other, which means we can simply denote this set of real numbers as $\mathbb{R}$, and that the [[pseudo-order]] relation on $\mathbb{R}$ is decidable. As a result, we can define a pointwise-discontinuous function $f:\mathbb{R} \to \mathbb{R}$ by case analysis $f(x) = 1$ if $x \gt 0$ and $f(x) = 1$ if $x \leq 0$. This contradicts Brouwer's continuity principle which says that all functions $f:\mathbb{R} \to \mathbb{R}$ are pointwise-continuous. 
\end{proof}

\begin{theorem}
In the presence of the [[weak countable choice]] axiom $\mathrm{AC}_{\mathbb{N}, 2}$, $\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[Brouwer's continuity principle]] for the usual impredicative [[Dedekind real numbers]] defined using the [[frame of truth values]] $\Omega$. 
\end{theorem}

\begin{proof}
$\mathrm{AC}_{\mathbb{N}, 2}$ implies that the Cauchy real numbers and the Dedekind real numbers coincide. Since the previous theorem implies that $\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[Brouwer's continuity principle]] for the Cauchy real numbers, $\mathrm{AC}_{\mathbb{N}, 2}$ implies that $\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[Brouwer's continuity principle]] for the Dedekind real numbers. 
\end{proof}

This means that theories which accept both $\mathrm{LPO}_\mathbb{N}$ and [[Brouwer's continuity principle]] for the Dedekind real numbers, such as the [[internal logic]] of the [[cohesive (infinity,1)-topos]] of [[Euclidean-topological infinity-groupoids]], necessarily reject $\mathrm{AC}_{\mathbb{N}, 2}$. 

\begin{theorem}
$\mathrm{LPO}_\mathbb{N}$ is inconsistent with [[Phoa's principle]] for the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma$. 
\end{theorem}

\begin{proof}
$\mathrm{LPO}_\mathbb{N}$ is equivalent to the fact that the unique [[distributive lattice]] [[homomorphism]] from the [[boolean domain]] to the initial $\sigma$-frame $\Sigma$ is an [[isomorphism]]. However, the [[logical negation]] function $x \mapsto \neg x$ on the [[boolean domain]] does not satisfy the linear interpolation condition for Phoa's principle for the booleans; it is not true that $\neg x = (\neg 0) \wedge (x \vee \neg 1) = 1 \wedge (x \vee 0) = x$ on the booleans. As a result, $\mathrm{LPO}_\mathbb{N}$ is inconsistent with Phoa's principle for the initial $\sigma$-frame $\Sigma$. 
\end{proof}

\begin{lemma}
$\mathrm{LPO}_\mathbb{N}$ is inconsistent with synthetic quasi-coherence (i.e. the [[Kock-Lawvere axiom]]) for the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma$; that is, let $A$ be a finitely presented $\Sigma$-algebra, in the sense that $A$ is a [[distributive lattice]] equivalent to the quotient of $\Sigma[x_1 \ldots x_n]$ by finitely many relations, and let $\mathrm{Spec}_\Sigma(A)$ be the set of $\Sigma$-algebra homomorphisms. Then the canonical lattice homomorphism

$$a \mapsto (f \mapsto f(a)):A \to \Sigma^{\mathrm{Spec}_\Sigma(A)}$$

is an [[isomorphism]]
\end{lemma}

\begin{proof}
Synthetic quasi-coherence for the [[initial object|initial]] [[sigma-frame|$\sigma$-frame]] $\Sigma$ implies [[Phoa's principle]] for $\Sigma$, and so is thus inconsistent with $\mathrm{LPO}_\mathbb{N}$.  
\end{proof}

\begin{theorem}
$\mathrm{LPO}_\mathbb{N}$ is inconsistent with the existence of a [[Specker sequence]]. 
\end{theorem}

See [Diener 2018](#Diener18) for more statements that are inconsistent with $\mathrm{LPO}_\mathbb{N}$. 

### Models

* Assuming that [[Set]] is a [[Boolean topos]], then $LPO_{\mathbb{N}}$ (the LPO for natural numbers) holds in any [[presheaf topos]] over $Set$ and indeed in any [[locally connected topos]] over $Set$, essentially since then $2^N$ is a constant object.

* The LPO for natural numbers fails in Johnstone's [[topological topos]], due to its internal continuity principle.  Hence, the analytic LPO also fails, since the modulated Cauchy reals and Dedekind reals coincide in this topos. 

## Related concepts

* [[principle of omniscience]]

* [[weak limited principle of omniscience]]

* [[lesser limited principle of omniscience]]

* [[Markov's principle]]

* [[excluded middle]]

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Ishihara06} [[Hajime Ishihara]], _Reverse Mathematics in Bishop's Constructive Mathematics_, Philosophia Scienti&#230;, CS 6 (2006) ([doi:10.4000/philosophiascientiae.406](https://doi.org/10.4000/philosophiascientiae.406),  [pdf](https://philosophiascientiae.revues.org/pdf/406))

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Rathjen13} [[Michael Rathjen]], *Constructive Zermelo-Fraenkel set theory and the limited principle of omniscience*. &lbrack;[arXiv:1302.3037](https://arxiv.org/abs/1302.3037)&rbrack;

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 ([arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147))

* {#Diener18} [[Hannes Diener]], *Constructive reverse mathematics*, Habilitationsschrift Fakultät IV - Naturwissenschaftlich-Technische Fakultät, 2018. ([arXiv:1804.05495](https://arxiv.org/abs/1804.05495), [dspace:ubsi/1306](https://dspace.ub.uni-siegen.de/handle/ubsi/1306))

* {#Booij20} [[Auke Booij]], *Analysis in univalent type theory* (2020) &lbrack;[etheses:10411]( 	http://etheses.bham.ac.uk/id/eprint/10411), [pdf](https://etheses.bham.ac.uk/id/eprint/10411/7/Booij2020PhD.pdf)&rbrack;

* {#Ciraulo22} Francesco Ciraulo, *$\sigma$-locales in Formal Topology*, Logical Methods in Computer Science, Volume 18, Issue 1 (January 12, 2022) ([doi:10.46298/lmcs-18%281%3A7%292022](https://doi.org/10.46298/lmcs-18%281%3A7%292022), [arXiv:1801.09644](https://arxiv.org/abs/1801.09644))

* {#Rijke22} [[Egbert Rijke]], *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press ([arXiv:2212.11082](https://arxiv.org/abs/2212.11082))

* {#BirchfieldSwan24} Madeleine Birchfield, Andrew Swan (2024) on Category Theory Zulip, [LPO and sigma-frame structure on booleans](https://categorytheory.zulipchat.com/#narrow/stream/229199-learning.3A-questions/topic/LPO.20and.20sigma-frame.20structure.20on.20booleans)

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

* {#LombardiMahboubi24} [[Henri Lombardi]], [[Assia Mahboubi]], *Théories géométriques pour l'algèbre des nombres réels sans test de signe ni axiome de choix dépendant* ([arXiv:2406.15218](https://arxiv.org/abs/2406.15218))

This reference calls the fully untruncated limited principle of omniscience for the natural numbers simply by the term "limited principle of omniscience". However, the limited principle of omniscience usually refers to the fully truncated version. 

* {#UFP13} Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

These two references call the limited principle of omniscience simply by the term "principle of omniscience" or "omniscience principle". However, [[principle of omniscience]] can refer to multiple possible axioms. 

* {#Bauer11}  [[Andrej Bauer]] (2011) via constructivenews, [An Injection from $\mathbb{N}^{\mathbb{N}}$ to $\mathbb{N}$](http://math.andrej.com/wp-content/uploads/2011/06/injection.pdf) (pdf)

* {#Escardo11} [[Martín Escardó]] (2011) via constructivenews, [Infinite sets that satisfy the principle of omniscience in all varieties of constructive mathematics](http://www.cs.bham.ac.uk/~mhe/papers/omniscient-2011-07-06.pdf) (pdf)

[[!redirects LPO]]
[[!redirects limited principle of omniscience]]
[[!redirects limited principles of omniscience]]

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