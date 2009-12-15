#Contents#
* automatic table of contents goes here
{:toc}


## Purpose of this page

The purpose of this page is to examine how much of the theory of [[Hilbert space]]s can be done in an "elementary" fashion.  More specifically, to develop as much as possible of the standard theory without using the fact that Hilbert spaces are special normed [[vector space]]s, or special [[metric space]]s.

The reason for trying this is in the spirit of [[centipede mathematics]].  One can view the theory of [[locally convex space|locally convex topological vector spaces]] as the result of pulling off most of the legs of Hilbert spaces, though perhaps one should go one step further and say that Hilbert spaces themselves are the result of pulling the "finite dimensional" leg off the Euclidean centipede.  Indeed, this is almost the standard treatment of LCTVSs except that the usual starting point is [[normed vector space|normed vector spaces]] rather than Hilbert spaces.  In that view, Hilbert spaces are special normed vector spaces rather than normed vector spaces being Hilbert spaces without a leg or two.

Although the intention is that the treatment be elementary, we shall remark on the relationship to the standard theory and thus the commentary will not necessarily be elementary.  For example, concepts that are traditionally defined by using the metric space structure of a Hilbert space will need recasting and we shall need to reassure the reader that the new definition is equivalent to the original.

We shall work over $\mathbb{C}$ throughout.

## Basic Definitions

We start with the basic definition of an inner product space.

+-- {: .num_defn #ipsp}
###### Definition
An **inner product space** is a vector space, say $V$, equipped with a function $|V| \times |V| \to \mathbb{C}$, written $\langle u, v \rangle$, satisfying:

1. $\langle v, u\rangle = \overline{\langle u, v\rangle}$,
2. $\langle v + \lambda w, u \rangle = \langle v, u \rangle + \lambda \langle w, u\rangle$,
3. $\langle v, v\rangle \in [0,\infty)$ with $\langle v, v\rangle = 0$ if and only if $v = 0$.
=--

Ideally, we want to deal solely with Hilbert spaces but first we need to figure out how to deal with completeness without recourse to metric space theory.  We do this by using orthonormal families.

+-- {: .num_defn #ofam}
###### Definition
Let $(V,\langle -, - \rangle)$ be an inner product space.  An **orthogonal family** in $V$ is a subset $B \subseteq V$ with the property that $\langle b, b'\rangle = 0$ whenever $b,b' \in B$ are distinct.

The family is said to be **orthonormal** if, in addition, $\langle b, b\rangle = 1$ for all $b \in B$.
=--

