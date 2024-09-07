
\tableofcontents

## Idea

In [[classical mathematics]], a *[[subsingleton]]* could either be defined as 

* a [[set]] $S$ such that for all [[elements]] $a \in S$ and $b \in S$, $a = b$

* a set $S$ which is either [[empty set|empty]] or a [[singleton]]. 

However, in [[constructive mathematics]], the two notions of subsingleton are no longer the same, because the [[axiom of excluded middle]] no longer holds true. Instead, one usually defines a subsingleton as the first definition, and the second definition is then referred to as about **decidable subsingletons**. 

Every subsingleton $S$ comes with an [[injection]] $i \colon S \to 1$ into a [[singleton]] $1$, and is thus is a (structural) [[subset]] of $1$. A subsingleton is also decidable in the subset sense: defining the relation $x \in_1 S$ as 
$$x \in_1 S \coloneqq \exists y \in 1.i(x) = y$$
for all elements $x \in 1$, $x \in_1 S$ or $\neg (x \in_1 S)$. 

Similarly for any [[decidable proposition]], the "or" used in the definition of a decidable subsingleton above can be either inclusive [[disjunction]] or [[exclusive disjunction]] - both definitions are equivalent to each other. 

Decidable subsingletons could be generalized from [[Set]] to any [[coherent category]]: they are precisely the [[decidable object|decidable]] [[subterminal objects]] in a coherent category. 

## Relation to the limited principle of omniscience

\begin{theorem}
Given a [[subsingleton]] $A$, suppose that the [[limited principle of omniscience]] for $A$ holds: for all functions $f$ from $A$ to the [[boolean domain]] $\{0, 1\}$, either there exists $x$ in $A$ such that $f(x) = 1$, or, for all $x$ in $A$, $f(x) = 0$. Then $A$ is a decidable subsingleton. 
\end{theorem}

\begin{theorem}
There are two definable functions from every subsingleton $A$ to the [[boolean domain]] $\{0, 1\}$, the [[constant functions]] $\lambda x:A.0$ and $\lambda x:A.1$. Suppose that either there exists $x:A$ such that $(\lambda x:A.0)(x) \neq (\lambda x:A.1)(x)$, or for all $x:A$, $(\lambda x:A.0)(x) = (\lambda x:A.1)(x)$. Then $A$ is a decidable subsingleton. 
\end{theorem}

\begin{proof}
We prove by case analysis. 

Suppose that there exists $x:A$ such that $(\lambda x:A.0)(x) \neq (\lambda x:A.1)(x)$. Then $A$ is a [[inhabited set|inhabited]] subsingleton and thus a decidable subsingleton. 

Then suppose that for all $x:A$, $(\lambda x:A.0)(x) = (\lambda x:A.1)(x)$. Then $A$ is [[empty set|empty]] and thus a decidable subsingleton, and the function set $\{0, 1\}^A$ is a [[singleton]] by the [[universal property]] of the empty set, with all functions equal to each other. 

This exhausts all options for decidable subsingletons, and exhausts all possible conditions in the hypothesis. 
\end{proof}

\begin{theorem}
Suppose that for sets $A$ and $B$ with [[decidable tight apartness relations]], the [[tight apartness relation]] on the function set $B^A$, defined by $f \# g \coloneqq \exists x:A.f(x) \neq g(x)$, is decidable. Then [[excluded middle]] holds. 
\end{theorem}

\begin{proof}
Every [[subsingleton]] $A$ has a [[decidable tight apartness relation]] where $x \# y$ is always [[false]]. The [[boolean domain]] $\{0, 1\}$ also has a decidable tight apartness relation where $x \# y$ is given by the [[denial inequality]] $x \neq y$. That the tight apartness relation on the function set $\{0, 1\}^A$ is decidable implies Theorem 2.2 above, which implies that every subsingleton $A$ is a decidable subsingleton, which is precisely the condition of [[excluded middle]]. 
\end{proof}

## Related concepts

* [[decidable proposition]]
* [[decidable subset]]
* [[decidable injection]]
* [[subsingleton]]

[[!redirects decidable subsingleton]]
[[!redirects decidable subsingletons]]

