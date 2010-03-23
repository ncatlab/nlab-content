# Dedekind cuts
* table of contents
{: toc}


## Idea

Dedekind cuts are a way to make precise the idea that a [[real number]] is that which can be approximated (in the [[absolute value]] metric) by [[rational numbers]].

In 1872, [[Richard Dedekind]] published _Stetigkeit und irrationale Zahlen_ (Continuity and irrational numbers), in which he pointed out that a real number may be uniquely determined its order relationships with rational numbers.  That is, the real number $x$ is determined by its __lower set__ $L_x$ and its __upper set__ $U_x$:
\[ \label{cuts} \begin {split}
   L_x \coloneqq \{ a\colon \mathbb{Q} \;|\; a \lt x \} \\
   U_x \coloneqq \{ b\colon \mathbb{Q} \;|\; b \gt x \}
   .\end {split} \]
Dedekind had found great success understanding the 'ideal numbers' of [[ring theory]] as certain sets, which are what we now understand as [[ideal of a ring|ideals]].  So he defined a 'real number' as a pair of sets of rational numbers, the lower and upper sets shown above.


## Definitions

Such a pair of sets of rational numbers is a __Dedekind cut__.  But which pairs of sets of rational numbers can appear this way?  The simplest definition may be *any* pair $(L,U)$ of [[inhabited sets]] of rational numbers satisfying two conditions:

1.  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.
2.  If $a \in L$ and $b \in U$, then $a \lt b$.

The second condition simply guarantees the [[transitive relation|transitivity]] rule that $a \lt x \lt b$ implies $a \lt b$ (where $x$ is the real number in question).  The point of the first condition (1) is that we can estimate $x$ as closely as we like by choosing appropriate rational numbers.

This is entirely [[constructive mathematics|constructive]].  We have $a_0 \in L$ and $b_0 \in U$ (because these sets are known to be inhabited), so if we wish to estimate $x$ to within a positive rational number $\epsilon$, then we simply let $n$ be $\lceil{2/\epsilon}\rceil$ and apply (1) to each of the finitely many ($\lceil{n(b_0-a_0)}\rceil$) rational numbers with denominator $n$ that lie between $a_0$ and $b_0$.  This will eventually give us a numerator $i$ such that $(i-1)/n \lt x \lt (i+1)/n$, so we have estimated $x$ within $2/n \leq \epsilon$.  Alternatively, to estimate $x$ to $n$ digits after a decimal point (with an uncertainty of $1$ in the last digit), apply (1) to each of the $\lceil{(b_0-a_0) \times 10^n}\rceil$ numbers between $a_0$ and $b_0$ that have $n$ digits after the decimal point.

If we define a real number to be *any* such pair $(L,U)$, then there is a slight redundancy.  We can either define $(L,U)$ and $(L',U')$ to be equal as real numbers if, for any rational numbers $a \lt b$, $a \in L$ or $b \in U'$ and $a \in L'$ or $b \in U$.  (More generally, we have $(L,U) \leq (L',U')$ if we always have $a \in L$ or $b \in U'$.)  Alternatively, we can pick a representative pair by adding two more requirements:

3.  If $a \in L$, then $b \in L$ for some $b \gt a$.
4.  If $b \in U$, then $a \in U$ for some $a \lt b$.

Every real number has a unique representative Dedekind cut satisfying all four conditions, and in that case the sets $L$ and $U$ are the sets $L_x$ and $U_x$ in (eq:cuts).


## One-sided cuts

...


## Unbounded cuts

...


[[!redirects Dedekind cut]]
[[!redirects Dedekind cuts]]
