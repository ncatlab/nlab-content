
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[constructive mathematics]], a set $A$ is **exhaustible** or **omniscient** if it satisfies a version of the [[limited principle of omniscience]] for the set $A$ rather than the natural numbers $\mathbb{N}$: For all functions $f$ from $A$ to the [[booleans]] $\{0, 1\}$, either there exists an element $x \in A$ such that $f(x) = 1$, or for all elements $x \in A$, $f(x) = 0$. 

One can equivalently use [[decidable subsets]] instead of functions into the booleans. A set $A$ is **exhaustible** or **omniscient** if the [[existential quantification]] of any [[decidable proposition]] on $A$ is again decidable. That is,
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in A, P(x)) \vee \neg(\exists x \in A, P(x)) ,$$
or equivalently
$$ (\forall x \in A, P(x) \vee \neg{P(x)}) \Rightarrow (\exists x \in A, P(x)) \vee (\forall x \in A, \neg{P(x)}) .$$

If you take the set $A$ to be the [[subsingleton]] corresponding to a given [[truth value]] and apply this principle to the constantly [[true]] proposition, then the subsingleton is decidable follows, since $\forall x \in A, P(x)$ holds, then either the subsingleton is [[inhabited set|inhabited]], in which $\exists x \in A, P(x)$ holds, or the subsingleton is [[empty set|empty]], in which $\forall x \in A, \neg P(x)$ holds. Thus, that every subsingleton is exhaustible implies $EM$; conversely, $EM$ implies that every set is exhaustible (over any domain). Note that propositions of the form $\exists x, P(x)$ when $P$ is decidable are the [[open truth values]] in the [[Rosolini dominance]].

We can also state the principle set-theoretically: a [[set]] $A$ is **exhaustible** or **omniscient** if for all [[subsets]] $P \in \mathcal{P}(A)$, if $P$ is a [[decidable subset]] of $A$ ($P \cup \bar{P} = A$), then either $P$ is [[inhabited subset|inhabited]] or $\bar{P} = A$, where $\bar{P}$ is the [[complement]] of $P$. 

While $\mathbb{N}$ being exhaustible is the [[limited principle of omniscience]], the set $\overline{\mathbb{N}}$ of [[extended natural number]]s is provably exhaustible in constructive mathematics; this is related to the fact that $\overline{\mathbb{N}}$ may constructively be given a [[compact space|compact]] topology. See [Escard&#243; (2011)](#Escardo11) for this and much more.

## Properties

+-- {: .standout}
This section appears to be original research, as there doesn't seem to be any existing literature on these properties. Note that the material in this section originally appeared on the article [[limited principle of omniscience]] before being moved here, so please check that article for the history of this material. 
=--

\begin{theorem}
A set $A$ is exhaustible if and only if the [[function set]] $\mathbb{2}^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{2}^A$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

\begin{proof}
Since the [[boolean domain]] is a [[boolean ring]], the function set $\mathbb{2}^A$ is also a [[boolean ring]] via pointwise addition, subtraction and multiplication of [[boolean-valued functions]]. Thus, for functions $f$ and $g$ from $A$ to $\mathbb{2}$, the [[tight apartness relation]] on the function set $\mathbb{2}^A$, defined by 
$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$ 
is logically equivalent to $\exists x \in A.f(x) - g(x) = 1$, since $f(x) \neq g(x)$ is logically equivalent to $f(x) = g(x) + 1$. 

Suppose that $A$ is exhaustible holds. Then for functions $f$ and $g$ from $A$ to $\mathbb{2}$, define the function $h$ by $h(x) = f(x) - g(x)$ for all $x \in \mathbb{N}$. Then since $A$ being exhaustible says that $\exists x \in A.h(x) = 1$ is decidable, and $\exists x \in A.h(x) = 1$ is logically equivalent to $f \# g$, then $f \# g$ is decidable. 

Conversely, assume that $f \# g$ is decidable. Then take $g$ to be the constant function at the boolean $0$, and $f \# \lambda x \in A.0$ is logically equivalently to $\exists x \in A.f(x) - 0 = 1$ and thus $\exists x \in A.f(x) = 1$. Since $f \# g$ is decidable, then $\exists x \in A.f(x) = 1$ is decidable, which is precisely that $A$ is exhaustible. 
\end{proof}

The next two statements relate a set $A$ being exhaustible with axioms that the [[tight apartness relation]] on certain other [[function sets]] are a [[decidable tight apartness]]. 

\begin{theorem}
More generally, given a [[finite set]] $S$ of [[cardinality]] $n \gt 1$, a set $A$ is exhaustible if and only if that the [[function set]] $S^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $S^A$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

\begin{theorem}
A set $A$ is exhaustible if and only if the [[function set]] $\mathbb{N}^A$ has [[decidable relation|decidable]] [[tight apartness]], where the [[tight apartness relation]] on the [[function set]] $\mathbb{N}^\mathbb{N}$ be defined as 

$$f \# g \coloneqq \exists x \in A.f(x) \neq g(x)$$
\end{theorem}

### Exhaustible subsingletons and excluded middle

There is a [[constant function]] $x \mapsto 1$ from every subsingleton $A$ to the [[boolean domain]] $\mathbb{2}$ taking every element $x \in A$ to the boolean $1 \in \mathbb{2}$. 

\begin{theorem}
Given a [[subsingleton]] $A$, suppose that $A$ is exhaustible: either there exists $x \in A$ such that $(x \mapsto 1)(x) = 1$, or for all $x \in A$, $(x \mapsto 1)(x) = 0$. Then $A$ is a [[decidable subsingleton]]. 
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
Every [[subsingleton]] $A$ has a [[decidable tight apartness relation]] where $x \# y$ is always [[false]]. The [[boolean domain]] $\mathbb{2}$ also has a decidable tight apartness relation where $x \# y$ is given by the [[denial inequality]] $x \neq y$. We proved earlier in the article that a set $A$ being exhaustible is equivalent to the tight apartness relation on the function set $\mathbb{2}^A$ being decidable, and every subsingleton $A$ being exhaustible implies that every subsingleton $A$ is a decidable subsingleton, which is precisely the condition of [[excluded middle]]. 
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

## In dependent type theory

+-- {: .standout}
This section appears to be original research, as there doesn't seem to be any existing literature on the universe of types that satisfy the principle of omniscience. Note that the material in this section originally appeared on the article [[limited principle of omniscience]] before being moved here, so please check that article for the history of this material. 
=--

In [[dependent type theory]], given a [[univalent Tarski universe]] $(U, T)$, one can construct the universe of all types in $U$ which are exhautible:

$$U_\mathrm{exh} \coloneqq \sum_{A:U} \prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee
\left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

Since the type 

$$\prod_{f:T(A) \to \mathrm{bool}} (\exists x:T(A).f(x) =_{\mathrm{bool}} 1) \vee \left(\prod_{x:T(A)} f(x) =_{\mathrm{bool}} 0\right)$$

is a [[mere proposition]] for all $A:U$, $U_\mathrm{exh}$ is a [[subtype|sub]]-[[universe]] of $U$. 

## Related concepts

* [[limited principle of omniscience]]

## References

* {#Escardo08} [[Martín Escardó]]: *Exhaustible sets in higher-type computation*, Logical Methods in Computer Science, Volume 4, Issue 3 (August 27, 2008) &lbrack;[doi:10.2168/LMCS-4(3-3)2008](https://doi.org/10.2168/LMCS-4%283%3A3%292008), [arXiv:0808.0441v2](https://arxiv.org/abs/0808.0441v2)&rbrack;

* {#Escardo11} [[Martin Escardo]]: *TypeTopology.CompactTypes*, TypeTopology Agda library, [web](https://martinescardo.github.io/TypeTopology/TypeTopology.CompactTypes.html). 

* {#Escardo13} [[Martín Escardó]]: *Infinite sets that satisfy the principle of omniscience in any variety of constructive mathematics.* The Journal of Symbolic Logic, Vol 78, September 2013, pp. 764-784. &lbrack;[doi:10.2178/jsl.7803040](https://doi.org/10.2178/jsl.7803040), [pdf](https://martinescardo.github.io/papers/omniscient-journal-revised.pdf)&rbrack;

These are also called *weakly compact types* in: 

* {#Escardo18} [[Martin Escardo]]: *TypeTopology.WeaklyCompactTypes*, TypeTopology Agda library, [web](https://martinescardo.github.io/TypeTopology/TypeTopology.WeaklyCompactTypes.htmll). 

[[!redirects exhaustible set]]
[[!redirects exhaustible sets]]

[[!redirects omniscient set]]
[[!redirects omniscient sets]]