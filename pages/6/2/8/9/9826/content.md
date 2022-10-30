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

It is possible to define a [[synthetic mathematics|synthetic]]/[[axiom|axiomatic]] notion of "projective line", somewhat analogously to the synthetic definition of [[projective plane]].  It is less obvious how to do this, since there is no relation of "incidence" inside a projective line.  One approach, due to [(Buekenhout)](#Buekenhout74), is to axiomatize the collection of "central collineations" of a projective line.

In general, a *central collineation* of an $n$-dimensional [[projective space]] $\pi$ (with $n\ge 2$) is an automorphism $\sigma$ of $\pi$ such that

1. there exists a point $O$, called the *center*, such that $\sigma$ fixes every line through $O$ (setwise, i.e.\ it sends every point on that line to a point on the same line), and
2. there exists a hyperplane $H$ (an $(n-1)$-dimensional subspace), called the *axis*, which $\sigma$ fixes pointwise (i.e.\ it sends every point on $H$ to itself).

If $\pi$ has dimension $\ge 3$, so that it has nontrivial sub-projective-spaces of dimension $\ge 2$, then the restriction of a central collineation of $\pi$ to any such sub-projective-space containing the center $O$ and not contained in the axis $H$ is again a central collineation.  Conversely, every central collineation of any subspace of such a $\pi$ is induced from a central collineation of $\pi$ itself (see for instance [Beutelspacher-Rosenbaum, Theorem 3.1.10](#BeutelspacherRosenbaum)).  The latter fact uses Desargues' theorem, but this is true since $\pi$ must be of dimension $\ge 3$ to have any nontrivial sub-projective-spaces.

Indeed, by a theorem of Baer ([Beutelspacher-Rosenbaum, Theorem 3.1.8](#BeutelspacherRosenbaum)), whenever $\pi$ (of dimension $\ge 2$) is Desarguesian, a central collineation is uniquely determined by its axis, its center, and one more pair of corresponding points.  Thus, given $O$ and $H$, the central collineations with center $O$ and axis $H$ act freely and transitively on $\pi \setminus (H\cup \{O\})$.

Of course, when $\pi$ is of dimension $\ge 2$, before we can talk about central collineations, we need to already know what the "hyperplanes" are.  However, in the hypothetical 1-dimensional case, hyperplanes are just points, so that the center and axis are both points, and we can imagine giving structure to $\pi$ by *axiomatizing* its central collineations instead of *defining* them.  This is done by the following definition, due to Buekenhout ([paper](#Buekenhout74), [book (chapter 6)](#BuekenhoutCohen)).

+-- {: .num_defn}
###### Definition
**(Buekenhout)**
A **projective line** is a set $\ell$ of cardinality $\ge 3$ together with the following.

1. For each $p,q\in \ell$, a group $\Lambda(p,q)$ whose elements are called *central collineations with center $p$ and axis $q$*.  Note that $q$ need not be distinct from $p$.
1. $\Lambda(p,q)$ acts on $\ell$ fixing $p$ and $q$, and if an element of it fixes a point $r \notin \{p,q\}$, then it is the identity.  In particular, the action is [[faithful action|faithful]], and therefore embeds each $\Lambda(p,q)$ in the [[permutation group]] $Aut(\ell)$.
1. If $p\neq q$, then $\Lambda(p,q)$ and $\Lambda(q,p)$ commute with each other.
1. For any $\sigma\in\Lambda(r,s)$ and any $p,q$, we have $\sigma \Lambda(p,q) \sigma^{-1} = \Lambda(\sigma(p),\sigma(q))$.
1. The composite of two collineations with center $p$ (possibly with different axes) is again a collineation with center $p$, and dually the composite of two collineations with axis $q$ (possibly with different centers) is again a collineation with axis $q$.  Thus we have two groups $\Lambda(p) = \bigcup_q \Lambda(p,q)$ and $\Lambda^\vee(q) = \bigcup_p\Lambda(p,q)$.

A projective line is **Desarguesian** if in addition $\Lambda(p,q)$ acts [[transitive action|transitively]] on $\ell \setminus \{p,q\}$.  In other words, if $r,s\in \ell\setminus \{p,q\}$, there is a (necessarily unique) $\sigma\in\Lambda(p,q)$ with $\sigma(r)=s$.
=--

### Examples

#### Lines in projective planes

We saw above that when $\pi$ is of dimension $\ge 3$, then every central collineation of a subspace (of dimension $\ge 2$) is induced by some central collineation of $\pi$.  Even though this required Desargues' theorem to prove, which might not be true in a projective plane (dimension $2$), we can still take the point of view that every "central collineation" of a line in a projective plane ought to be induced by a central collineation of the plane itself.

This yields the following construction: Given a projective plane $\pi$ (not necessarily Desarguesian), and a line $\ell$ in $\pi$, for any $p,q\in \ell$ define $\Lambda(p,q)$ to be the set of permutations of $\ell$ that are the restriction to $\ell$ of some central collineation of $\pi$ with center $p$ and axis containing $q$.  It is straightforward to verify that this makes $\ell$ into a "projective line" in the above sense.

#### Trivial examples

There are, however, plenty of projective lines not arising from projective planes.  For instance, we might set $\Lambda(p,q) = 1$ for all $p,q$.

#### Analytic examples

Let $k$ be a [[division ring]] and $V$ a 2-dimensional right [[vector space]] over $k$.  Then $\mathbb{P}(V)$ has the structure of a Desarguesian projective line, where

* if $p\neq q$, then $\Lambda(p,q)$ is the image in $PGL(V)$ of those automorphisms in $GL(V)$ fixing $q$ pointwise and $p$ setwise.
* if $p= q$, then $\Lambda(p,q)$ is the image in $PGL(V)$ of those automorphisms $\alpha\in GL(V)$ such that $\alpha(p)=p$ and $\alpha(x)-x\in p$ for all $x\in V$.

Conversely, every Desarguesian projective line arises from a division ring in this way.  Fix three points $0,1,\infty \in \ell$ and define

* $k=\ell\setminus\{\infty\}$.
* $a+b = t_b(a)$, where $t_b$ is the unique element of $\Lambda(\infty,\infty)$ with $t_b(0)=b$.
* $a b = \lambda_a(b)$, where $\lambda_b$ is the unique element of $\Lambda(0,\infty)$ with $t_a(1)=a$.

It follows that every Desarguesian projective line can be embedded into a Desarguesian projective plane, and indeed a projective space of any dimension.  See [Buekenhout-Cohen, Chapter 6](#BuekenhoutCohen) for details.


## References

* {#BeutelspacherRosenbaum} Albrecht Beutelspacher and Ute Rosenbaum, *Projective Geometry: from foundations to applications*.  Cambridge University Press, 1998. ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/beutel.pdf))

* {#Buekenhout74} Francis Buekenhout, *Foundations of one Dimensional Projective Geometry based on Perspectivities*.  Abhandlungen aus dem Mathematischen Seminar der Universit&#228;t Hamburg, 43 (1975) 21-29. doi:[10.1007/BF02995931](https://doi.org/10.1007/BF02995931)

* {#BuekenhoutCohen} Francis Buekenhout and Arjeh M. Cohen, *Diagram Geometry: Related to Classical Groups and Buildings*.  Springer, 2013, doi:[10.1007/978-3-642-34453-4](https://doi.org/10.1007/978-3-642-34453-4) ([author pdf](http://www.win.tue.nl/~amc/buek/))

[[!redirects projective lines]]
