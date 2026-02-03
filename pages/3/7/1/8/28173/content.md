
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
#### Integration
+-- {: .hide}
[[!include integration theory - contents]]
=--
=--
=--

# Contents
* Cousin\'s Theorem
{: toc}


## Idea

Cousin\'s Theorem, attributed to [[Pierre Cousin]], is a generalization of the [[Heine–Borel theorem]] (which Cousin also proved), and an important lemma to prove the nontriviality of the [[Henstock–Kurzweil integral]].


## Statements

The basic result (containing the hard part of the proof) can be distilled to the following:

+-- {: .num_theorem #basic}
###### Theorem

Let $a \leq b$ be [[real numbers]], and let $\mathcal{U}$ be an [[open cover]] of the [[interval]] $[a, b]$.  Then there exists a partition (in the sense of [[Riemann sum]]s) $a = x_0 \leq \cdots \leq x_n = b$ such that each subinterval $[x_i, x_{i+1}]$ (for $0 \leq i \lt n$) is contained in some $U_i \in \mathcal{U}$.
=--

We give a proof valid in both [[classical mathematics]] and [[intuitionistic mathematics]].  (See [below](#constructive) for other forms of [[constructive mathematics]].)  This proof is based on one that appeared uncredited on [Wikipedia](#Wikipedia).

+-- {: .proof}
###### Proof

Let $S$ be the set of real numbers $r \in [a, b]$ such that $[a, r]$ has a partition of the desired form; we will show that $S$ is all of $[a, b]$.

If $r \in S$, with a partition ending with $x_n = r$ and $[x_{n-1}, x_n]$ contained in some $U_{n-1} \in \mathcal{U}$, then we can (if $r \lt b$) increase $x_n$ slightly and keep $[x_{n-1}, x_n]$ within $U_{n-1}$, showing that $S$ is open on the right.  Similarly, we can (if $r \gt a$) decrease $x_n$ slightly as long as $x_{n-1} \lt x_n$, to show that $S$ is open on the left; to deal with the possibility that $x_{n-1} = x_n$ and keep the argument intuitionistically valid, note that in any case $x_{n-1} \lt x_n$ or $x_{n-1} \gt a$, so we can either decrease $x_n$ as originally planned, or lower $n$ by $1$ and decrease the new $x_n$ (the old $x_{n-1}$) instead (which requires comparing with the old $x_{n-2}$ and so on, but since there are only finitely many subintervals, this process will eventually end).  Therefore, $S$ is open.

Now suppose that $s \in [a, b]$ and $[a, s) \subseteq S$; we will show that $[a, s] \subseteq S$.  So suppose $r \in [a, s]$, and let $U$ be a member of $\mathcal{U}$ such that $s \in U$; note that (even intuitionistically) $r \lt s$ or $r \in U$.  If $r \lt s$, then we already have a partition of $[a, r]$; if $r \in U$, then we can (if $r \gt a$) take $t \lt r$ with $t \in U$, get a partition of $[a, t]$ and extend it with $[t, r]$ to get a $1$-step longer partition of $[a, r]$.  To handle intuitionistically the possibility that $r = a$, let $V$ be a member of $\mathcal{U}$ such that $a \in V$, so that $a \lt r$ or $r \in V$; if $a \lt r$, then we can proceed as in the previous sentence, while if $r \in V$, then we can just use $[a, r]$ as a $1$-step partition.

Now we use the [[open induction principle]], a form of completeness of the [[real line]] that is both classically and intuitionistically valid, which states that if $S$ is an open subset of $[a, b]$, and $[a, s] \subseteq S$ whenever $[a, s) \subseteq S$, then $S = [a, b]$.
=--

Sometimes it\'s desired that every subinterval have positive length, so that $x_i \lt x_{i+1}$ for $0 \leq i \lt n$.  This is trivial classically; simply throw out any duplicates among the list of $x$s.  Intuitionistically, we can\'t expect this to be possible in all situations; if $a \lt b$ then we obviously need $n \gt 0$, while if $a = b$ then we need $n = 0$ to have all subintervals of positive length, but we can\'t expect to be able to decide this.  However, this is the only hang-up:

+-- {: .num_theorem #positive}
###### Corollary

If $a \lt b$, then there exists a partition in which each subinterval has positive length.
=--

+-- {: .proof}
###### Proof

Form a partition as above; because $a \lt b$, we have $n \gt 0$.  By performing a finite number of comparisons, we can verify $x_i \lt x_{i+1}$ for all $i \lt n$, or find some $i \lt n$ such that $x_i \in U_{i+1}$ (unless $i = n - 1$, since there is no $U_n$) and $x_{i+1} \in U_{i-1}$ (unless $i = 0$, since there is no $U_{-1}$).  Since $n \gt 0$, we have $x_i \in U_{i+1}$ *or* $x_{i+1} \in U_{i-1}$ no matter what value $i$ takes, and this allows us to remove $x_{i+1}$ or $x_i$ (respectively) from the list of $x$s.  Repeating this (for a maximum of $n - 1$ times), we eventually get a partition with only positive-length subintervals.
=--


## Cousin\'s Lemma

This is the form needed for the [[Henstock–Kurzweil integral]]; see there for now.


## Constructive version {#constructive}

See at [[locale of real numbers]] for now.


## References

* {#Wikipedia} Wikipedia (English). [Cousin\'s theorem](https://en.wikipedia.org/wiki/Cousin%27s_theorem). Accessed 2026-02-02.


[[!redirects Cousin's theorem]]
[[!redirects Cousin's Theorem]]
[[!redirects Cousin theorem]]
[[!redirects Cousin Theorem]]
[[!redirects Cousin’s theorem]]
[[!redirects Cousin’s Theorem]]
[[!redirects Cousin\'s theorem]]
[[!redirects Cousin\'s Theorem]]

[[!redirects Cousin's lemma]]
[[!redirects Cousin's Lemma]]
[[!redirects Cousin lemma]]
[[!redirects Cousin Lemma]]
[[!redirects Cousin’s lemma]]
[[!redirects Cousin’s Lemma]]
[[!redirects Cousin\'s lemma]]
[[!redirects Cousin\'s Lemma]]
