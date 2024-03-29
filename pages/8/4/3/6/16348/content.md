
#Contents#
* table of contents
{:toc}

## Idea

A **connectology** on a [[set]] $X$ is a [[structure]] which abstracts the information about which [[subsets]] of $X$ are [[connected]].  Every [[topological space]] and every [[graph]] has an underlying connectology, but not every connectology is of these forms.

## Definition

A **connectology** on a set $X$ consists of a set of subsets of $X$, called *connected* sets, such that the following axioms hold.

1. If $C\subseteq \mathcal{P}(X)$ is a family of connected sets such that $\bigcap C \neq \emptyset$, then $\bigcup C$ is connected.

2. Every [[singleton]] $\{x\}$ is connected.

3. If $A$ and $B$ are nonempty, and $A$, $B$, and $A\cup B$ are connected, then there exists an $x\in A\cup B$ such that $A\cup\{x\}$ and $B\cup \{x\}$ are connected.

4. If $A,B,\{C_i\}_{i\in I}$ are disjoint connected sets such that $A\cup B\cup \bigcup_i C_i$ is connected, then there is a partition $I=J+K$ such that $A\cup \bigcup_{j\in J} C_j$ and $B\cup \bigcup_{k\in K} C_k$ are connected.

A set equipped with a connectology is sometimes called a **connective space**, although this may be confusing due to other meanings of the word [[connective]].

## Related concepts

* [[diffeology]]

## References

* Joseph Muscat and David Buhagiar, *Connective Spaces*, [PDF](http://www.math.shimane-u.ac.jp/memoir/39/D.Buhagiar.pdf).

[[!redirects connectologies]]
[[!redirects connective space]]
[[!redirects connective spaces]]
