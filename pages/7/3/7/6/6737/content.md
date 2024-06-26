#Contents#
* table of contents
{:toc}

## Idea

In a [[preorder]] or [[poset]] $P$, an **antichain** is a subset $S \subseteq P$ such that no two distinct elements of $S$ are comparable. 

Assuming $P$ has a bottom element $0$, a *strong antichain* is a subset $S \subseteq P$ such that for distinct $a, b \in S$, the only lower bound of $\{a, b\}$ is $0$. This definition may be extended to posets $P$ *without* a bottom element, by declaring $A \subseteq P$ to be a strong antichain if $A$ is a strong antichain in $P^+$, the poset formed by freely adjoining a bottom element to $P$. 

In the context of [[set theory]], for example in discussions of [[forcing]] and [[countable chain conditions]], "strong antichain" is often abbreviated to just "antichain". 

[[!redirects antichains]] 