# Dedekind cuts
* table of contents
{: toc}


## Idea

Dedekind cuts are a way to make precise the idea that a [[real number]] is that which can be approximated (in the [[absolute value]] metric) by [[rational numbers]].

In 1872, [[Richard Dedekind]] published _Stetigkeit und irrationale Zahlen_ (Continuity and irrational numbers), in which he pointed out that a real number may be uniquely determined its order relationships with rational numbers.  That is, the real number $x$ is determined by its __lower set__ $L_x$ and its __upper set__ $U_x$:
\[ \label{cuts} \begin {split}
   L_x \coloneqq \{ a\colon \mathbb{Q} \;|\; a \lt x \} \\
   U_x \coloneqq \{ b\colon \mathbb{Q} \;|\; x \lt b \}
   .\end {split} \]
Dedekind had found great success understanding the 'ideal numbers' of [[ring theory]] as certain sets, which are what we now understand as [[ideal of a ring|ideals]].  So he defined a 'real number' as a pair of sets of rational numbers, the lower and upper sets shown above.  Such a pair of sets of rational numbers he called a 'Schnitt' (English 'cut'), nowadays called a 'Dedekind cut'.


## Definition

Exactly which pairs of sets of rational numbers can appear this way?  We will define a __Dedekind cut__ to be any pair $(L,U)$ of sets of rational numbers satisfying these conditions:

1.  $L$ is [[inhabited set|inhabited]]; that is, some rational number belongs to $L$.
2.  Similarly, $U$ is inhabited.
3.  $L$ is downward-closed; that is, if $a \lt b$ are rational numbers with $b \in L$, then $a \in L$.
4.  Similarly, $U$ is downward-closed: if $a \lt b$ are rational numbers with $a \in U$, then $b \in U$.
5.  $L$ is upward-open; that is, if $a \in L$, then $a \lt b$ for some $b \in L$.
6.  Similarly, $U$ is downward-open; that is, if $b \in U$, then $a \lt b$ for some $a \in U$.
7.  If $a \lt b$ are rational numbers, then $a \in L$ or $b \in U$.
8.  If $a \in L$ and $b \in U$, then $a \lt b$.

Actually, this definition is redundant; any pair $(L,U)$ that satisfies (7&8) must also satisfy (3&4).  However, we state (3&4) explicitly to simplify the description of the variations below.

If $x \coloneqq (L,U)$ is a Dedekind cut, then we define $a \lt x$ to mean that $a \in L$ and define $x \lt b$ to mean that $b \in U$.


## Motivation

The point of condition (7) is that we can estimate $x$ as closely as we like by choosing appropriate rational numbers.

This is entirely [[constructive mathematics|constructive]].  We have $a_0 \lt x$ for some $a_0$ (by 1) and $x \lt b_0$ for some $b_0$ (by 2), so if we wish to estimate $x$ to within a positive rational number $\epsilon$, then we simply let $n$ be $\lceil{2/\epsilon}\rceil$ and apply (7) to each of the finitely many ($\lceil{n(b_0-a_0)}\rceil$) rational numbers with denominator $n$ that lie between $a_0$ and $b_0$.  This will eventually give us a numerator $i$ such that $(i-1)/n \lt x \lt (i+1)/n$, so we have estimated $x$ within $2/n \leq \epsilon$.  Alternatively, to estimate $x$ to $n$ digits after a decimal point (with an uncertainty of $1$ in the last digit), apply (1) to each of the $\lceil{(b_0-a_0) \times 10^n}\rceil$ numbers between $a_0$ and $b_0$ that have $n$ digits after the decimal point.  (We can never constructively determine the final digit with perfect certainty; if we successively estimate $x$ as $0.5, 0.50, 0.500, \ldots$, no finite number of such estimates can ever ensure that $x$ won\'t come out to $0.4999\cdots9998$ when we go one digit farther.)

Besides giving us a place to begin our estimation, (1&2) ensure that $x$ is finite.  Condition (8) enforces us the [[transitivity]] law $a \lt x \lt b \implies a \lt b$; (3&4) are likewise forms of transitivity.  (5&6) ensure that, even if $x$ happens to be a rational number, we are using the sets $L_x$ and $U_x$ given in (eq:cuts) instead of their closures (defined with $\leq$ instead of $\lt$).


## Forming a Dedekind-complete linear order

We define $x \lt y$ to mean that there exist a rational number $a$ such that $x \lt a \lt y$; that is, some rational number belongs to both the upper set of $x$ and the lower set of $y$.  It is then straightforward to prove that $\lt$ is a [[linear order]]:

...


We can also intepret derive a Dedekind cut from any rational number $x$ by taking (eq:cuts) to be the definition of $x$ as a Dedekind cut.  Thus every rational number is interpreted as a real number.  This is an inclusion of linear orders:

...


## Variations

...


[[!redirects Dedekind cut]]
[[!redirects Dedekind cuts]]
