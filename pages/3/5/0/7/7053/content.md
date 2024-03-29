
# Tietze transformations
* table of contents
{: toc}

## Idea

Tietze transformations are a formalisation of the informal substitution methods that are natural when working with [[group presentations]].


## The four transformations

Let $G= \langle X: R\rangle$ be a [[group presentation]], where the 'specified isomorphism to $G$' is unspecified!

The following transformations do not change the group $G$:

T1:  Adding a superfluous relation

$\langle X: R\rangle$ becomes $\langle X: R^'\rangle$, where $R^' = R \cup \{r\}$ and $r\in N(R)$ the normal closure of the relations in the free group on $X$, i.e., $r$ is a consequence of $R$;

T2: Removing a superfluous relation

$\langle X: R\rangle$ becomes $\langle X: R^'\rangle$ where $R^' = R - \{r\}$, and $r$ is a consequence of $R^'$;

T3: Adding a superfluous generator

$\langle X: R\rangle$ becomes $\langle X^': R^'\rangle$, where $X^' = X\cup \{ g\}$, $g$ being a new symbol not in $X$, and $R^' = R\cup\{wg^{-1}\}$, where $w$ is a word in the other generators, that is $w$ is in the image of the inclusion of $F(X)$ into $F(X^')$;

T4: Removing a superfluous generator

$\langle X: R\rangle$ becomes $\langle X^': R^'\rangle$, where $X^' = X - \{ g\}$, and $R^' = R-\{wg^{-1}\}$ with $w\in F(X^')$ and $wg^{-1}\in R$ and no other members of $R\prime$ involve $g$.


## Tietze's theorem

+-- {: .un_theo}
###### Theorem
Given two finite presentations of the same group, one can be obtained from the other by a finite sequence of Tietze transformations.
=--


## References

Tietze's original paper is 

* H. Tietze, _&#220;ber die topologischen Invarianten mehrdimensionaler Mannigfaltigkeiten_, Monatsschr. Math. Phys., 19 (1908) 1 --118.

See also 

* W. Magnus and B. Chandler, _The history of combinatorial group theory_, Springer (1982).


category : group theory

[[!redirects Tietze transformation]]
[[!redirects Tietze transformations]]
[[!redirects Tietze's transformation]]
[[!redirects Tietze's transformations]]
