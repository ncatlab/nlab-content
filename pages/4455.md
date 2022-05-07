
# Dedekind completions
* table of contents
{: toc}

## Idea

The _Dedekind completion_ of a [[linear order]] $L$ is a new linear order $\widebar{L}$ that contains [[suprema]] for all [[inhabited set|inhabited]] [[bounded subsets]], and such that a supremum in $L$ is still a supremum in $\widebar{L}$. 

While Dedekind completeness was traditionally described in the context of the [[real numbers]], it can be stated for any [[linear order]], although it really works best for [[dense order|dense]] and unbounded (without [[top]] or [[bottom]]) linear orders. Intuitively, a linear order is _Dedekind complete_ if [[Dedekind cuts]] don't give any 'new' elements.

## Definitions

Let $S$ be a [[set]] equipped with the structure of a [[dense linear order]] without [[top]] or [[bottom]] elements (endpoints).

+-- {: .num_defn}
###### Definition

A __cut__ in $S$ is a pair of [[subsets]] $L, U \subset S$ of $S$ that satisfy the following eight properties:

1.  $L$ is [[inhabited subset|inhabited]];
2.  Dually, $U$ is inhabited;
3.  If $x \lt y \in L$, then $x \in L$;
4.  Dually, if $x \gt y \in U$, then $x \in U$;
5.  If $x \in L$, then $x \lt y \in L$ for some $y$;
6.  Dually, $x \in U$, then $x \gt y \in U$ for some $y$;
7.  If $x \lt y$, then $x \in L$ or $y \in U$;
8.  If $x \in L$ and $y \in U$, then $x \lt y$.
=--

+-- {: .num_defn}
###### Definition

The linearly ordered set $S$ is **Dedekind complete** if every cut $(L,U)$ is of the form
$$ L = \{x \;| \;x \lt a\},\; U = \{x \;|\; x \gt a\}$$
for some unique $a \in S$.
=--

+-- {: .num_defn}
###### Definition

If $T$ is also an unbounded dense linear order, $S$ is Dedekind complete, and we have a [[universal arrow]] $u\colon T \to S$ in the [[category]] of linear orders, then $S$ (equipped with $u$) is [[the]] **Dedekind completion** of $T$.
=--

The set of Dedekind cuts of [[rational numbers]] --the set of [[real numbers]]-- is Dedekind complete. In fact, starting with any unbounded dense linearly ordered set $S$, the set of Dedekind cuts is isomorphic to the reals as long as $S$ is a [[countably infinite set]]. 

The operation of forming the set of Dedekind cuts is idempotent, so the Dedekind completion can be constructed as the set of Dedekind cuts.  More precisely, the Dedekind-complete linear orders form a [[reflective subcategory]] of the category of dense unbounded linear orders, so that Dedekind completion is a kind of [[completion]] in the abstract categorial sense.

### Using open intervals ###

A set $F$ with a [[linear order]] is **Dedekind complete** if 

* For all elements $a \in F$ and $b \in F$, the open interval $(a,b)$ is inhabited. 

* For all elements $a \in F$, the upper unbounded open interval $(a,\infty)$ is inhabited. 

* For all elements $a \in F$, the lower unbounded open interval $(-\infty,a)$ is inhabited.

* For all elements $a \in F$ and $b \in F$, $a \lt b$ if and only if $(b,\infty)$ is a subinterval of $(a,\infty)$

* For all elements $a \in F$ and $b \in F$, $b \lt a$ if and only if $(-\infty,b)$ is a subinterval of $(-\infty,a)$

* For all elements $a \in F$ and $b \in F$, if $a \lt b$, then $F$ is a subinterval of the union of $(a, \infty)$ and $(-\infty, b)$

* For all elements $a \in F$ and $b \in F$, the intersection of $(a,\infty)$ and $(-\infty,b)$ is a subinterval of the [[open interval]] $(a,b)$

## Generalisations

### In predicative constructive mathematics

In predicative mathematics, subsets are large and therefore are proper classes. Instead, in the manner of [[formal topology]], predicative mathematicians typically use pairs of functions $L, U: \mathbb{Q} to \Sigma$ representing the open subsets of $\mathbb{Q}$ to define __predicative cuts__, where $\Sigma$ is a [[sigma-frame|$\sigma$-frame]]. The definitions then become

+-- {: .num_defn}
###### Definition
Given a [[sigma-frame|$\sigma$-frame]] $\Sigma$ and a linearly ordered set $S$, a __cut__ in $S$ is a pair of functions $L, U: S to \Sigma$ that satisfy the following eight properties:

1.  There is an element $a \in S$ such that $L(a) = \top$.
2.  There is an element $b \in S$ such that $U(b) = \top$.
3.  If $a \lt b$ are elements of $S$ with $L(b) = \top$, then $L(a) = \top$.
4.  If $a \lt b$ are elements of $S$ with $U(a) = \top$, then $U(b) = \top$.
5.  If $L(a) = \top$, then there is an element of $S$ $a \lt b$ such that $L(b) = \top$.
6.  If $U(b) = \top$, then there is an element of $S$ $a \lt b$ for some $U(a) = \top$.
7.  If $a \lt b$ are elements of $S$, then $L(a) = \top$ or $U(b) = \top$.
8.  If $L(a) = \top$ and $U(b) = \top$, then $a \lt b$.
=--

+-- {: .num_defn}
###### Definition

The linearly ordered set $S$ is $\Sigma$-**Dedekind complete** if for every cut $(L,U)$ there exists a unique element $a \in S$ such that for all elements $x \in S$, $x \lt a$ implies $L(x) = \top$ and $x \gt a$ implies $U(x) = \top$.
=--

### Quasiorders

+-- {: .standout}
Any paragraph containing the string 'duiq' is original research (although lower duiqs at least are known in [[domain theory]]).
=--

One can generalise Dedekind completion from [[linear orders]] to [[quasiorders]].

+-- {: .num_defn}
###### Definition

A __duiq__ (**d**ense **u**nbounded **i**nhabited **q**uasiorder) is a [[quasiordered set]] $S$ such that, given finite (here always meaning [[Kuratowski-finite]]) [[subsets]] $F$ and $G$ of $S$ such that $x \lt z$ whenever $x \in F$ and $z \in G$, we have some $y$ in $S$ such that $x \lt y \lt z$ whenever $x \in F$ and $z \in G$.
=--

Note that, for $S$ a [[linear order]], $S$ is a duiq iff $S$ is dense, unbounded, and [[inhabited set|inhabited]], hence the term 'duiq'.  (Using linearity, we may assume that $F$ and $G$ are [[subsingletons]]; then two [[singleton subsets]] is denseness, one singleton subset and one [[empty subset]] is unboundedness, and two empty subsets is inhabitedness.)

+-- {: .num_defn}
###### Definition

Given a duiq $S$, a __cut__ is a pair $(L,U)$ of [[subsets]] such that:

1.  $L$ is [[inhabited subset|inhabited]] (which is a special case of (5) for $F$ the [[empty subset]]);
2.  Dually, $U$ is inhabited (a special case of (6));
3.  If $x \lt y \in L$, then $x \in L$;
4.  Dually, if $x \gt y \in U$, then $x \in U$;
5.  If $F$ is a finite subset of $L$ (which we may assume inhabited if we include (1)), then for some $x \in L$, every $y \in F$ satisfies $y \lt x$;
6.  Dually, if $F$ is a finite (inhabited) subset of $U$, then for some $x \in U$, every $y \in F$ satisfies $y \gt x$;
7.  If $L \lt x \lt U$ and $L \lt y \lt U$, then $x = y$;
8.  If $x \in L$ and $y \in U$, then $x \lt y$.
=--

We then define __Dedekind-complete__ duiqs and __Dedekind completions__ of duiqs the same as for dense linear orders, using this notion of cut.

A good example of a duiq is the set of [[rational number|rational]]-valued [[functions]] on any [[set]] $X$; the Dedekind completion is the set of [[real number|real]]-valued functions on $X$.

Sections 4.31--39 of _[[HAF]]_ do things in even more generality, but I don\'t really understand it yet.

## One-sided Dedekind completions

At least in [[classical mathematics]], considering only $L$ (for a __lower cut__) or $U$ (for an __upper cut__) doesn\'t really give us anything new for linear orders; we have only the technicality that $\infty \coloneqq (S,\empty)$ or $-\infty \coloneqq (\empty,S)$ is a cut (depending on the side), and we can rule even these out by simply requiring that $L$ have an upper bound or that $U$ have a lower bound.

In [[constructive mathematics]], one-sided cuts are more general; see [[one-sided real number]] for a discussion of the case where $S$ is the linear order of [[rational numbers]].

Even in classical mathematics, one-sided cuts do give us something new for quasiorders.  Here, we have first more general one-sided notions of duiqs: a __lower duiq__ need only satisfy the condition of a duiq for $G$ a [[singleton]], and an __upper duiq__ need only satisfy the condition for $F$ a singleton.  Then the __lower Dedekind completion__ of a lower duiq is its set of lower cuts, and the __upper Dedekind completion__ of an upper duiq is its set of upper cuts.

For example, let $X$ be a [[compactum]] and let $S$ be the quasiordered set of [[continuous map|continuous]] real-valued functions on $X$.  Then $S$ is a duiq, hence both a lower and upper duiq.  Its lower Dedekind completion is the set of lower [[semicontinuous map|semicontinuous]] functions on $X$ taking values in the [[lower reals]] (which classically are all either real or $\infty$); and dually on the upper side.  Even working classically and ignoring the technicality of $\infty$, semicontinuous functions are much more general than continuous ones.


## References

*  [[Paul Taylor]]\'s [page on Dedekind cuts](http://www.paultaylor.eu/ASD/dedras/classical)

*  Page 249&250 of _Continuous Lattices and Domains_ ([Google book](http://books.google.com/books?id=xPF9Hb7DPLgC)) covers lower Dedekind completions of duiqs (although not under that name) in the context of [[domain theory]].

* Univalent Foundations Project, [[HoTT book|Homotopy Type Theory – Univalent Foundations of Mathematics]] (2013)

* Auke B. Booij, Extensional constructive real analysis via locators, ([abs:1805.06781](https://arxiv.org/abs/1805.06781))

* Steve Vickers, “Localic Completion Of Generalized Metric Spaces I”, [TAC](http://www.tac.mta.ca/tac/volumes/14/15/14-15abs.html)

[[!redirects Dedekind completion]]
[[!redirects Dedekind completions]]
[[!redirects Dedeking completion]]

[[!redirects Dedekind-complete]]
[[!redirects Dedekind complete]]
[[!redirects Dedekind completeness]]

[[!redirects Dedekind-complete order]]
[[!redirects Dedekind-complete orders]]
[[!redirects Dedekind complete order]]
[[!redirects Dedekind complete orders]]


[[!redirects sigma Dedekind completion]]
[[!redirects sigma Dedekind completions]]
[[!redirects sigma Dedeking completion]]
[[!redirects sigma-Dedekind completion]]
[[!redirects sigma-Dedekind completions]]
[[!redirects sigma-Dedeking completion]]
[[!redirects Sigma Dedekind completion]]
[[!redirects Sigma Dedekind completions]]
[[!redirects Sigma Dedeking completion]]
[[!redirects Sigma-Dedekind completion]]
[[!redirects Sigma-Dedekind completions]]
[[!redirects Sigma-Dedeking completion]]

[[!redirects sigma Dedekind-complete]]
[[!redirects sigma Dedekind complete]]
[[!redirects sigma Dedekind completeness]]
[[!redirects sigma-Dedekind-complete]]
[[!redirects sigma-Dedekind complete]]
[[!redirects sigma-Dedekind completeness]]
[[!redirects Sigma Dedekind-complete]]
[[!redirects Sigma Dedekind complete]]
[[!redirects Sigma Dedekind completeness]]
[[!redirects Sigma-Dedekind-complete]]
[[!redirects Sigma-Dedekind complete]]
[[!redirects Sigma-Dedekind completeness]]

[[!redirects sigma Dedekind-complete order]]
[[!redirects sigma Dedekind-complete orders]]
[[!redirects sigma Dedekind complete order]]
[[!redirects sigma Dedekind complete orders]]
[[!redirects sigma-Dedekind-complete order]]
[[!redirects sigma-Dedekind-complete orders]]
[[!redirects sigma-Dedekind complete order]]
[[!redirects sigma-Dedekind complete orders]]
[[!redirects Sigma Dedekind-complete order]]
[[!redirects Sigma Dedekind-complete orders]]
[[!redirects Sigma Dedekind complete order]]
[[!redirects Sigma Dedekind complete orders]]
[[!redirects Sigma-Dedekind-complete order]]
[[!redirects Sigma-Dedekind-complete orders]]
[[!redirects Sigma-Dedekind complete order]]
[[!redirects Sigma-Dedekind complete orders]]