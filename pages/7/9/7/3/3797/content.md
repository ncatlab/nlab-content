
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A **tileorder** is a *double order*, i.e. a set $T$ equipped with two [[partial orders]] $\le$ and $\sqsubseteq$, which can be realized by a dissection of a rectangle into finitely many subrectangles, the subrectangles being the elements of $T$, in such a way that $a\sqsubseteq b$ iff $a$ "lies below" $b$, while $a\le b$ iff $a$ "lies to the left of" $b$.  Interestingly and importantly, such orders can also be characterized in purely combinatorial, and effectively verifiable, terms.

Such orders are of interest in [[double category]] theory, since these are the arrangements of 2-cells in a double category which could potentially be composed (although in a general double category, not all of them can actually be composed).  

## Definition

Suppose given a dissection of a rectangle into finitely many subrectangles.  Define $T$ to be the set of subrectangles, and for $a,b\in T$ write $a\le b$ if there exists a finite list $a= x_0, x_1, \dots, x_n = b$ such that for each $i$, the right edge of $x_i$ intersects the left edge of $x_{i+1}$ in more than one point.  Define $a\sqsubseteq b$ similarly using top and bottom edges instead of left and right.  Clearly $\le$ and $\sqsubseteq$ are [[partial orders]].

A set $T$ equipped with two partial orders $\le$ and $\sqsubseteq$ (a priori, unrelated) is called a **double order**.  A double order which arises in this way from a rectangle dissection is called a **tileorder**.


## Characterizations

As proven by Dawson and Par&#233;, tileorders can be characterized in purely combinatorial terms in a couple of interesting ways.

### Using maximal chain properties

A double order $T$ is said to have the **$\sqsubset$-parallel maximal chain property** if whenever $K$ and $L$ are maximal $\sqsubseteq$-chains in $T$, and we have $k_1,k_2\in K$ and $l_1,l_2\in L$ with $k_1 \sqsubset k_2$, $k_1 \le l_1$, and $l_2 \le k_2$, then there exists an $e\in K\cap L$ such that $k_1\sqsubset e$, $l_1\sqsubset e$, $e\sqsubset k_2$, and $e\sqsubset l_2$.  In other words, two maximal $\sqsubseteq$-chains cannot "swap places" in the $\le$-order without intersecting.

Dually, we define the **$\lt$-parallel maximal chain property**.

A double order $T$ is said to have the **orthogonal maximal chain property** if every maximal $\le$-chain intersects every maximal $\sqsubseteq$-chain exactly once.

+-- {: .un_theorem}
###### Theorem
A double order is a tileorder iff it has both parallel maximal chain properties and the orthogonal maximal chain property.
=--


### Using local configuration structure

A double order is **strongly antisymmetric** if two unequal elements are never related (in either direction) by both $\lt$ and $\sqsubset$.  That is, if $a\neq b$, then at most one of $a\lt b$, $b\lt a$, $a\sqsubset b$, and $b\sqsubset a$ holds.

A double order is **rectangular** if $\exists c.(a\sqsubseteq c \le b)$ iff $\exists d.(a\le d \sqsubseteq b)$, and similarly $\exists c.(a\sqsubseteq c \ge b)$ iff $\exists d.(a\ge d \sqsubseteq b)$.

A double order is **total** if for any $a,b$, there exists a $c$ such that either $a\sqsubseteq c \le b$, or $a\sqsubseteq c \ge b$, or $b \le c \sqsubseteq a$, or $b\ge c \sqsubseteq a$.

A double order has the **first $\sqsubset$-orthogonal butterfly factorization property** if given $a,b,c,d$ with $c\sqsubseteq a$, $c\sqsubseteq b$, $d\sqsubseteq b$, and $d\le a$, there exists an $e$ with $c\sqsubseteq e \sqsubseteq b$ and $d\le e \le a$.  The **second** such property is defined by replacing $\le$ by $\ge$, but not changing $\sqsubseteq$.  The **$\lt$-orthogonal** such properties are defined by switching the roles of $\sqsubseteq$ and $\le$.

A double order has the **$\sqsubset$-parallel butterfly factorization property** if given $a,b,c,d$ with $c\sqsubseteq a$,  $b\le c$, $d\sqsubseteq b$, and $d\le a$, there exists an $e$ with $b\le e \le c$ and $d\le e \le a$.  The **$\lt$-parallel** such property is defined by switching the roles of $\sqsubseteq$ and $\le$.

+-- {: .un_theorem}
###### Theorem
A double order is a tileorder iff it is strongly antisymmetric, rectangular, total, and has all the orthogonal and parallel butterfly factorization properties.
=--


## References

* Dawson and Par&#233;, "Characterizing tileorders"


[[!redirects tileorders]]
[[!redirects double order]]
[[!redirects double orders]]
