\tableofcontents

## Idea

An _Archimedean ordered integral domain_ is an [[ordered integral domain]] that satisfies the [[Archimedean property]].

## Examples

Archimedean ordered integral domains include

* [[integers]]
* [[rational numbers]]
* [[decimal rational numbers]]
* [[dyadic rational numbers]]
* [[real numbers]]

Non-Archimedean ordered integral domains include

* [[p-adic integers]].

## Properties

\begin{theorem}
The [[integers]] are the [[initial object|initial]] Archimedean ordered integral domain. 
\end{theorem}

\begin{theorem}
The [[Dedekind real numbers]] are the [[terminal object|terminal]] Archimedean ordered integral domain. 
\end{theorem}

For an [[ordered integral domain]], we say that $x$ is [[tight apartness relation|apart from]] $y$ [[if and only if]] $x \lt y$ [[disjunction|or]] $x \gt y$. 

\begin{theorem}
Every Archimedean ordered integral domain $R$ with an element $x$ in $R$ [[tight apartness|apart from]] every integer is a [[dense linear order]]. 
\end{theorem}

\begin{proof}
Since $x$ is apart from every [[integer]], there exists an integer $a$ such that $0 \lt x - a \lt 1$, and since $R$ is Archimedean, it does not have either infinite or infinitesimal elements, which means there exists a natural number $b$ such that $1 \lt b(x - a)$. In addition, $0 \lt x - a \lt 1$ implies $0 \lt (d - c)(x - a) \lt d - c$ and $c \lt (d - c)(x - a) + c \lt d$ for all $c$ and $d$ in $R$. Let $y = (d - c)(x - a) + c$. Since there exists an element $y$ such that $c \lt y \lt d$ for all $c$ and $d$, $R$ is a [[dense linear order]]. 
\end{proof}

\begin{theorem}
The [[Dedekind completion]] of ordered integral domain $R$ with an element $x$ in $R$ apart from every integer is the integral domain of [[Dedekind real numbers]]. 
\end{theorem}

\begin{proof}
The [[Dedekind completion]] of every [[dense linear order]] is the [[Dedekind real numbers]]. Since by the previous theorem, $R$ is a dense linear order, the Dedekind completion of $R$ is the Dedekind real numbers. 
\end{proof}

\begin{theorem}
That the [[Dedekind completion]] of every [[Archimedean ordered integral domain]] is [[isomorphic]] to either the [[integers]] $\mathbb{Z}$ or the [[Dedekind real numbers]] $\mathbb{R}$ is equivalent to the analytic $\mathrm{LPO}$ for $\mathbb{R}$. 
\end{theorem}

\begin{proof}
Let $\mathbb{Z}[x]$ denote the [[free commutative ring]] on a [[singleton]] and let $I$ be a [[ideal]] of $\mathbb{Z}[x]$. Consider an Archimedean ordered integral domain $R$ which is ring isomorphic to a [[quotient ring]] $\mathbb{Z}[x] / I$, $R \cong \mathbb{Z}[x] / I$, with element $x \in R$. The Dedekind completion of $R$ is the integers if and only if $x$ is equal to an integer, and the Dedekind completion of $R$ is the Dedekind real numbers if and only if $x$ is [[tight apartness|apart from]] an integer. However, $x$ is equal to an integer or apart from an integer for all $x \in R$ if and only if $R$ is a [[discrete integral domain]], and the claim that every Archimedean ordered integral domain is discrete is equivalent to the analytic $\mathrm{LPO}$ for the Dedekind real numbers. 
\end{proof}

## Related concepts

* [[Archimedean ordered field]]

* [[Archimedean group]]

* [[archimedean difference protoring]]

* [[enriched set]]

[[!redirects archimedean ordered integral domain]]
[[!redirects archimedean ordered integral domains]]

[[!redirects Archimedean ordered integral domain]]
[[!redirects Archimedean ordered integral domains]]

[[!redirects archimedean integral domain]]
[[!redirects archimedean integral domains]]

[[!redirects Archimedean integral domain]]
[[!redirects Archimedean integral domains]]
