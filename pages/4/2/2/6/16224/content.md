
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition ##

A [[topological space]] $X$ is called hemicompact iff there exists a sequence $(K_n)_{n\in\mathbb{N}}$ of compact subsets $K_n\subseteq X$ such that $X=\bigcup_{n\in\mathbb{N}} K_n$ and $K_n \subseteq int(K_{n+1})$ holds.

## Properties ##

If $X$ is hemicompact and $(K_n)$ a sequence as in the definition, then every compact subset $K\subseteq X$ is contained in one of the $K_n$. In other words: $\lbrace K_n \mid n\in\mathbb{N}\rbrace$ is [[cofinal]] in the set of all compact subsets (partially ordered by inclusion)

\begin{proposition}
[[locally compact|Locally compact]] (every point has a compact neighborhood) and $\sigma$-compact spaces are hemicompact (and also [[paracompact]]).
\end{proposition}

\begin{proposition}
A [[first-countable]] and hemicompact space is [[locally compact]] (every point has a compact neighborhood).
\end{proposition}

Here the condition to be [[first-countable]] can't be dropped as there are hemicompact spaces, which are not [[locally compact]]. An example is the [[Arens-Fort space]] as seen in [Joshi 83, Chapter 4, Section 2, Example 10](#Joshi83), which is not even [[compact]].

\begin{proposition}
A hemicompact space is $\sigma$-compact.
\end{proposition}

\begin{example}
The [[field]] of [[rational numbers]] $\mathbb{Q}$ is $\sigma$-compact, but not hemicompact.
\end{example}

([Willard 04, p. 126](#Willard04), answer by Eric Wofsey on [MSE/4209303](https://math.stackexchange.com/questions/4209303/a-sigma-compact-but-not-hemicompact-space))

## References

* {#Willard04} Stephen Willard. _General Topology_ (2004). Dover Publications. ISBN 0-486-43479-6. [pdf](https://books.google.de/books/about/General_Topology.html?id=-o8xJQ7Ag2cC&redir_esc=y)
* {#Joshi83} K. D. Joshi. _Introduction to General Topology_ (1983). New Age International. ISBN 978-0-47027-556-6. [pdf](https://books.google.de/books?id=fvCpXrube5wC)

## Related concepts

* [[orthocompact space]]

[[!redirects hemicompact]]
[[!redirects hemicompact spaces]]

[[!redirects countably hemicompact]]
[[!redirects countably hemicompact spaces]]