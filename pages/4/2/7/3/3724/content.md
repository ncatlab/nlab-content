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


## Definitions

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


### Motivation

The point of condition (7) is that we can estimate $x$ as closely as we like by choosing appropriate rational numbers.

This is entirely [[constructive mathematics|constructive]].  We have $a_0 \lt x$ for some $a_0$ (by 1) and $x \lt b_0$ for some $b_0$ (by 2), so if we wish to estimate $x$ to within a positive rational number $\epsilon$, then we simply let $n$ be $\lceil{2/\epsilon}\rceil$ and apply (7) to each of the finitely many ($\lceil{n(b_0-a_0)}\rceil$) rational numbers with denominator $n$ that lie between $a_0$ and $b_0$.  This will eventually give us a numerator $i$ such that $(i-1)/n \lt x \lt (i+1)/n$, so we have estimated $x$ within $2/n \leq \epsilon$.  Alternatively, to estimate $x$ to $n$ digits after a decimal point (with an uncertainty of $1$ in the last digit), apply (1) to each of the $\lceil{(b_0-a_0) \times 10^n}\rceil$ numbers between $a_0$ and $b_0$ that have $n$ digits after the decimal point.  (We can never constructively determine the final digit with perfect certainty; for example, if we successively estimate $x$ as $0.5, 0.50, 0.500, \ldots$, no finite number of such estimates can ever ensure that $x$ won\'t come out to $0.4999\cdots9998$ when we go one digit farther.)

Besides giving us a place to begin our estimation, (1&2) ensure that $x$ is finite.  Condition (8) enforces us the [[transitivity]] law $a \lt x \lt b \implies a \lt b$; (3&4) are likewise forms of transitivity.  (5&6) ensure that, even if $x$ happens to be a rational number, we are using the sets $L_x$ and $U_x$ given in (eq:cuts) instead of their closures (defined with $\leq$ instead of $\lt$).


### Dedekind completion

We define $x \lt y$ to mean that there exist a rational number $a$ such that $x \lt a \lt y$; that is, some rational number belongs to both the upper set of $x$ and the lower set of $y$.  It is then straightforward to prove that $\lt$ is a [[linear order]]:

*  Asymmetry:  If $x \lt y$ and $y \lt x$, pick $a$ such that $x \lt a \lt y$ and $b$ such that $y \lt b \lt x$.  Applying (8) in two ways, $a \lt b$ and $b \lt a$, which is impossible.
*  Comparison:  If $x \lt z$ and $y$ is a Dedekind cut, then pick $a$ such that $x \lt a \lt z$.  Using (5) or (6), we can generalise this to two rational numbers $a$ and $b$ such that $x \lt a \lt b \lt z$.  Applying (7) to $a \lt b$, we get $x \lt y$ (if $a \lt y$) or $y \lt z$ (if $y \lt b$).
*  Connectedness:  Suppose that $x \lt y$ and $y \lt x$ both fail, and suppose that $a \lt y$.  By (5), we have $a \lt b \lt y$ for some $b$.  Applying (7), we have $a \lt x$ or $x \lt b$.  Since $x \lt b \lt y$ contradicts our assumptions, we have $a \lt x$.  In summary, $a \lt y \implies a \lt x$.  We can prove $a \lt x \implies a \lt y$, $b \lt x \implies b \lt y$, and $b \lt y \implies b \lt x$ similarly.  Therefore, $x$ and $y$ are equal (as pairs of subsets).

We can also derive a Dedekind cut from any rational number $x$ by taking (eq:cuts) to be the definition of $x$ as a Dedekind cut.  Thus every rational number is interpreted as a real number.  This is a strict inclusion of linear orders:

*  If $x \lt y$ as rational numbers, then let $a$ be the rational number $(x+y)/2$; we have $x \lt a \lt y$, so $x \lt y$ as real numbers.

In this way, the Dedekind cuts form an extension of the linearly ordered set of rational numbers.  More than that, this extension is [[Dedekind completion|Dedekind-complete]], which basically means that you cannot extend further by taking Dedekind cuts of Dedekind cuts.

To be explicit, suppose that $(L,U)$ is a pair of sets of Dedekind cuts (rather than of rational numbers) that satisfies (1--8), using Dedekind cuts in place of rational numbers.  Let $\sup L$ be the union of the left halves of the cuts that appear in $L$, and let $\inf U$ be the union of the right halves of the cuts that appear in $U$.  Then one can prove that $x \coloneqq (\sup L, \inf U)$ is a Dedekind cut (of rational numbers), and furthermore that $L$ and $U$ may be recovered from $x$ as in (eq:cuts), again using Dedekind cuts in place of rational numbers.

We say that the Dedekind cuts form the [[Dedekind completion]] of the linear order $\mathbb{Q}$.


## Variations

The conditions (5&6) are not really necessary.  If you leave them out, then the proof that $\lt$ is a [[connected relation]] on Dedekind cuts fails; but instead we identify cuts $x$ and $y$ whenever neither $x \lt y$ nor $y \lt x$.  Then the set $\mathbb{R}$ of real numbers becomes a [[quotient set]] of the set of Dedekind cuts.  In a similar vein, we can even weaken (3,4,7) as follows:

* 3':  If $a \lt b$ are rational numbers with $b \in L$, then $a' \in L$ for some $a' \lt a$.
* 4':  If $a \lt b$ are rational numbers with $a \in U$, then $b' \in U$ for some $b' \gt b$.
* 7':  If $a \lt b$ are rational numbers, then $a' \in L$ for some $a' \lt a$ or $b' \in U$ for some $b' \gt b$.

Just as (3,4) follow from (7,8), so (3',4') follow from (7',8).  Again, $\lt$ is no longer connected, but we still get a linear order on a quotient set.  (Incidentally, you can also recover the original definition using (3,4,7') in place of (7).)

...


[[!redirects Dedekind cut]]
[[!redirects Dedekind cuts]]
