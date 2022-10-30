# Projective lines

* table of contents
{: toc}

## Idea

A projective line is a [[projective space]] of [[dimension]] 1.

## Analytic projective lines

If $k$ is a field, the projective line over $k$ is typically denoted $\mathbb{P}^1(k)$.  Set-theoretically it is a disjoint union $k \sqcup \{\infty\}$ where each $a \in k$ has homogeneous coordinates $[a, 1]$ and $\infty$ has homogeneous coordinates $[1, 0]$.

The classical case of a projective line is over the complex numbers $\mathbb{C}$, where $\mathbb{P}^1(\mathbb{C})$ is also known as the [[Riemann sphere]]. A [[meromorphic function]] on $\mathbb{C}$ may be naturally interpreted as a [[holomorphic function]] $\mathbb{C} \to \mathbb{P}^1(\mathbb{C})$. 

In particular, a [[rational function]] $p/q \in \mathbb{C}(z)$ may be interpreted as a holomorphic function $[p/q]: \mathbb{P}^1(\mathbb{C}) \to \mathbb{P}^1(\mathbb{C})$; concretely, if $p(z), q(z)$ are relatively prime and of degrees $m, n$ respectively, then we may homogenize by setting $p(x, y) \coloneqq y^m p(x/y)$ and $q(x, y) \coloneqq y^n q(x/y)$, and define $[p/q]$ by the mapping on homogeneous coordinates $[x, y] \mapsto [p(x, y), q(x, y)]$. In fact, there is a bijective correspondence between such holomorphic endomaps on $\mathbb{P}^1(\mathbb{C})$ and rational functions on $\mathbb{C}$ (well, almost: the constant holomorphic map valued at $\infty$ corresponds to the illegitimate "rational function" $1/0$). 

## Synthetic projective lines

It is possible to define a synthetic/axiomatic notion of "projective line", somewhat analogously to the synthetic definition of [[projective plane]].  It is less obvious how to do this, since there is no relation of "incidence" inside a projective line.  One approach, due to [(Buekenhout)](#Buekenhout74), is to axiomatize the collection of "central collineations" of a projective line.

In general, if $\ell$ is a hyperplane (an $(n-1)$-dimensional subspace) in an $n$-dimensional [[projective space]] $\pi$, a *central collineation* of $\ell$ is a [[projectivity]] from it to itself determined as the composite of two [[perspectivities]].  That is, we pick some other hyperplane $h$ and two points $O$ and $O'$ not on either $\ell$ or $h$, and we map a point $P\in\ell$ first to $P' = PO \cap h$ and then to $P'' = P'O'\cap \ell$.  This is a [[collineation]], i.e. it preserves incidence relations.  The point $OO' \cap \ell$ is called the *center* of the central collineation, and the $(n-2)$-dimensional space $\ell\cap h$ is called its *axis*.

This construction still works even when $n=2$, but of course since $\ell$ is only a line it has no "incidence structure" to be preserved, so the name "collineation" is not very appropriate.

+-- {: .un_defn}
###### Definition
**(Buekenhout)**
A **projective line** is a set $\ell$ of cardinality $\ge 3$ together with

1. For each $p\in \ell$, a group $\Lambda(p)$ of *collineations with center $p$*, which acts on $\ell$ fixing $p$.
1. Each collineation with center $p$ is assigned an *axis* $q\in \ell$, which it also fixes.  The collineations with center $p$ and axis $q$ form a subgroup $\Lambda(p,q)$.  Note that $q$ need not be distinct from $q$.
1. If a collineation with center $p$ and axis $q$ fixes a point $r \notin \{p,q\}$, then it is the identity.  In particular, the action is [[faithful action|faithful]], and therefore embeds each $\Lambda(p)$ in the [[permutation group]] $Aut(\ell)$.
1. If $p\neq q$, then $\Lambda(p,q)$ and $\Lambda(q,p)$ commute with each other.
1. For any central collineation $\sigma$ and any $p,q$, we have $\sigma \Lambda(p,q) \sigma^{-1} = \Lambda(\sigma(p),\sigma(q))$.

A projective line is **Desarguesian** if in addition $\Lambda(p,q)$ acts [[transitive action|transitively]] on $\ell \setminus \{p,q\}$.  In other words, if $r,s\in \ell\setminus \{p,q\}$, there is a (necessarily unique) $\sigma\in\Lambda(p,q)$ with $\sigma(r)=s$.
=--

+--{: .query}
[[Mike Shulman]]: I've copied this definition from Buekenhout; the only point I'm not entirely sure about is that when he talks about "perspectivities with center $p$ and axis $q$" he means what I'm calling "collineations with center $p$ and axis $q$" here.  If that *is* what he means, then I don't agree with his definition; I don't see how to prove that $\Lambda(p,q)$ is closed under composition without Desargues's theorem, or how to prove that $\Lambda(p)$ is closed under composition without Pappus's theorem.
=--


## References

* Francis Buekenhout, *Foundations of one Dimensional Projective Geometry based on Perspectivities*.  Abhandlungen aus dem Mathematischen Seminar der Universit&#228;t Hamburg, 43 (1975) 21-29
{#Buekenhout74}


[[!redirects projective lines]]
