
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Algebra
+-- {: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Definition

In [[constructive mathematics]]: 

\begin{definition}\label{TheDefinition}
A **Heyting field** is a [[local ring]] where every non-[[invertible]] [[element]] is [[equal]] to [[zero]]. More specifically, it is a [[commutative ring]] $R$ such that 

1. $R$ is non-trivial ($0 \neq 1$);

2. given elements $a \in R$ and $b \in R$, if $a + b$ is invertible, then either $a$ is invertible or $b$ is invertible;

3. given an element $a \in R$, if $a$ is non-invertible, then $a = 0$.

\end{definition}

Equivalently, a Heyting field is:

* a [[local ring]] $R$ whose [[quotient ring]] by the [[ideal]] of non-invertible elements is [[isomorphic]] to $R$;

* a local ring $R$ such that the canonical [[apartness relation]] $\#$ --- defined as $a \# b$ if and only if $a - b$ is invertible --- is a [[tight apartness relation]]. 

\begin{remark}\label{TrivialRingAsAField}
In [Lombardi & Quitté (2010)](#LombardiQuitté2010), the authors' definition of Heyting field do not include the non-equational axiom $1 \neq 0$. Instead, they define non-invertible to mean that if the element is invertible, then $1 = 0$. With such a definition, the [[trivial ring]] counts as a Heyting field and constitutes the [[terminal object]] in the [[category|categories]] of Heyting fields.
\end{remark}

## Properties

### Stable and decidable equality. 

Every [[Heyting field]] $R$ has [[stable equality]], because it has a [[tight apartness relation]] defined as $a \# b$ if and only if $a - b$ is invertible. For all elements $a \in R$ and $b \in R$, $\neg \neg \neg (a \# b) \iff \neg (a \# b)$, and because $\neg (a \# b) \iff a = b$, $\neg \neg (a = b) \iff a = b$, and thus $R$ has stable equality. 

A Heyting field with [[decidable equality]] is a [[discrete field]]. 

### Relation to Johnstone residue fields

[Johnstone (1977)](#Johnstone77) defined a *residue field* to be a [[commutative ring]] which only satisfy [[axioms]] 1 and 3 in Def. \ref{TheDefinition}; we shall call these *[[Johnstone residue fields]]* in this article to not confuse them with the notion of [[residue field]] in [[algebraic geometry]]. 

If every Johnstone residue field with decidable equality is a Heyting field, then [[excluded middle]] follows. The following proof is due to Mark Saving: 

\begin{definition}
Let $p$ be a proposition. We define the set $R_p$ to be the union of $\mathbb{Z}$ and $\{x \in \mathbb{Q} \vert p\}$
\end{definition}

$R_p$ is a [[subring]] of the [[rational numbers]] $\mathbb{Q}$. 

Since $R_p$ is a [[subset]] of $\mathbb{Q}$ and $\mathbb{Q}$ has decidable equality, $R_p$ also has decidable equality. And of course $0\neq 1$ in $R_p$. 

\begin{theorem}
$R_p$ is a Johnstone residue field iff $\neg \neg p$. 
\end{theorem}

\begin{proof}
Given a [[proposition]] $p$, suppose its [[double negation]] $\neg \neg p$, and consider some $x\in R_p$. Suppose $x$ does not have a multiplicative inverse. Now suppose $x\neq 0$. Then we see that $x^{-1}$ is not in $R_p$. If $p$ held, we would have $x{-1} \in R_p$. So we know $\neg p$ holds. But this is a [[contradiction]]. Therefore, $x$ must be zero (using decidable equality).

Conversely, suppose $R_p$ is a Johnstone residue field. If $\neg p$ held, we would have $R_p = \mathbb{Z}$, which clearly is not a Johnstone residue field since $2$ is neither invertible nor zero. So we must have $\neg \neg p$.
\end{proof}

\begin{theorem}
$R_p$ is a Heyting field iff it is the case that $p$ iff $R_p$ is a discrete field. 
\end{theorem}

\begin{proof}
Suppose $R_p$ is a Heyting field. Then either $2$ or $3$ has a multiplicative inverse, so either $2^{-1} \in R_p$ or $3^{-1} \in R_p$. In either case, we see that $p$ holds. If $p$ holds, then $R_p = \mathbb{Q}$, which is a discrete field. And if $R_p$ is a discrete field, it is clearly a Heyting field.
\end{proof}

\begin{theorem}
If every Johnstone residue field with discrete equality is Heyting, then [[excluded middle]] is valid.
\end{theorem}

\begin{proof}
From the lemmas above, if every Johnstone residue field with decidable equality is a Heyting field, then $p \iff \neg \neg p$ holds for all propositions $p$. So we have full excluded middle.
\end{proof}

## See also

* [[field]]

* [[local ring]]

* [[ordered field]]

## References

* {#Johnstone77} [[Peter Johnstone]], *Rings, Fields, and Spectra*, Journal of Algebra **49** (1977) 238-260 &lbrack;doi:[10.1016/0021-8693(77)90284-8](https://doi.org/10.1016/0021-8693%2877%2990284-8)&rbrack;

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) &lbrack;[doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf)&rbrack;

[[!redirects Heyting field]]
[[!redirects Heyting fields]]
[[!redirects heyting field]]
[[!redirects heyting fields]]