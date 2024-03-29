+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Functional analysis
+--{: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

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

Two vectors, say $u$ and $v$, are said to be orthogonal if the family $\{u,v\}$ is an orthogonal family.
=--

Using orthogonal families, we can express the notion of completeness as follows.

+-- {: .num_defn #hilb}
###### Definition
A **Hilbert space** is an inner product space, $(H, \langle -, -\rangle)$ in which the following property holds.  Let $(b_n)$ be an orthonormal sequence and $(\lambda_n)$ a sequence of positive real numbers such that $\sum \lambda_n^2$ is bounded.  Then there is some $v \in H$ such that for all $u \in H$,
$$
\sum \lambda_n \langle b_n, u \rangle = \langle v, u \rangle.
$$
=--

+-- {: .un_remark}
###### Remark
We need to justify this notion of completeness.  One direction is simple: the sequence of partial sums of the series $\sum \lambda_n b_n$ is Cauchy and so if the space is complete, it has a limit and this limit satisfies the criterion.

The other direction takes a little more effort.  The quickest (but dirtiest) route is simply to observe that if that condition is satisfied then whenever we have an isometry from $\ell^0$ (with its standard inner product) into our space then it extends to $\ell^2$.  A slightly more concrete route is as follows.  Start with a Cauchy sequence in $H$, say $(x_n)$, and then apply the [[Gram–Schmidt process]].  This results in an orthonormal sequence, say $(b_n)$.  For each $k$, we define $\lambda_k$ as the limit (in $\mathbb{C}$) of $(\langle x_n, b_k\rangle)$.  We can make $\lambda_k$ a positive real number by taking the phase factor in to $b_k$.  Let $(s_n)$ be the sequence of partial sums of the series $\sum \lambda_k b_k$.  Then $(s_n)$ is Cauchy and the interpolation of $(s_n)$ and $(x_n)$ is also Cauchy.  By assumption, $(s_n)$ has a weak limit.  As it is Cauchy, the existence of a weak limit is enough to show that it has a strong limit.  Thus $(x_n)$ also converges and so $H$ is complete.

The tenor of the new definition and its equivalence to the standard one is a theme that will run throughout this page.  In our elementary treatment, weak definitions are to be preferred to the standard strong ones.  Their equivalence exposes some of the deep results of Hilbert space theory.
=--

As this is intended as an elementary treatment, it is likely that at some point we will want to assume that our Hilbert space is "small", by which (of course) we mean "[[separable space|separable]]".  Fortunately, it is not hard to formulate separability without recourse to metric spaces.

+-- {: .num_defn #sep}
###### Definition
An inner product space is **separable** if it contains a sequence, say $(x_n)$ with the property that $\langle x, x_n\rangle = 0$ for all $n$ implies that $x = 0$.
=--

## Cauchy--Schwarz

The Cauchy--Schwarz inequality is one of the basic results of Hilbert space theory.  As we wish to avoid any mention of a norm, we state it as follows.

+-- {: .num_proposition #csineq}
###### Proposition
Let $H$ be a Hilbert space, $u,v \in H$.  Then
$$
|\langle u, v \rangle|^2 \le \langle u, u \rangle \langle v, v \rangle
$$
with equality if and only if $u$ and $v$ are collinear.
=--

+-- {: .query}
I removed the square roots here, since there doesn\'t seem to be much point to them if you\'re not going to connect with a metric.  (On the other hand, surely even an elementary treatment of Hilbert spaces may deign to mention the geometric concept of distance?  It\'s one thing to not assume a knowledge of metric spaces, but it\'s another thing to refuse to even mention norms.)  ---Toby

As you can (probably) tell, I'm making this up as I go along!  I've not decided yet whether to allow distances or not, so at the moment I'm avoiding them if possible.  Part of my goal is to avoid overwhelming the "reader" with notation just for the sake of it.  So I may well implicitly use the norm as $\langle v, v\rangle$ but without introducing the $\|v\|$ notation.  But although I expect I'll be the main contributor here, I don't particularly want to be so I'm more than happy for others to weigh in with their opinions on what an "elementary treatment" would look like.  If I disagree then it'll force me to think carefully _why_ I disagree and that can only improve things.

Pondering a little more, I think that I'm avoiding distance not because I don't think it belongs in an elementary treatment - as you imply, what could be more simple to understand than distance? - but because it's a way of keeping metric spaces at bay: once I start talking about distances then it'll be easy to talk about metrics and the like.

I think you're right about the square roots, by the way.  ---Andrew

Since accidentally using metric space theory is always a danger, I understand not wanting to mention distances and norms right away.  On the other hand, I do think that any introductory treatment ought to mention them at some point, and even to prove that they satisfy the triangle inequality and Cauchy completeness.  But those should be theorems specifically about the concept of distance in a Hilbert space, not anything fundamental to the development of the general theory of Hilbert spaces.  So sure, keep them out for now.  ---Toby
=--

+-- {: .proof}
###### Proof
The "if and only if" part gives us the key to the most direct proof.  It will simplify matters a little if we assume that $u$ and $v$ are non-zero, the case where one of them is zero being easy to establish.

Now if $u$ and $v$ are collinear then there is some $\lambda \in \mathbb{C}$ such that $u = \lambda v$.  There is only one possibility for $\lambda$ which can be found by taking inner products with $v$: if $\lambda$ exists such that $u = \lambda v$ then $\lambda = \langle u, v\rangle/\langle v, v\rangle$.  So we consider the question: is $\langle v, v\rangle u = \langle u, v\rangle v$?  Or, equivalently, is $\langle v, v\rangle u - \langle u, v\rangle v = 0$?

We have a test for when a vector is non-zero using the inner product.  One of the axioms for an inner product says that a vector $w$ is zero if and only if $\langle w, w\rangle = 0$.  Moreover, we also know that in any case $\langle w, w\rangle \ge 0$.  Thus we have

\[
\label{csineq}
\left\langle \langle v, v\rangle u - \langle u, v\rangle v, \langle v, v\rangle u - \langle u, v\rangle v \right\rangle \ge 0
\]

with equality if and only if $u$ and $v$ are collinear.

Before expanding out the left hand side of this, we note that

$$
\left\langle \langle v, v\rangle u - \langle u, v\rangle v , v \right\rangle = 0
$$

whence \eqref{csineq} simplifies to

$$
\left\langle \langle v, v\rangle u - \langle u, v\rangle v, u \right\rangle \ge 0
$$

with equality if and only if $u$ and $v$ are collinear.  Expanding this out yields

$$
\langle v,v\rangle \langle u,u\rangle - \langle u, v \rangle \langle v, u\rangle \ge 0
$$

with equality if and only if $u$ and $v$ are collinear.  Rearranging and square-rooting produces the traditional statement of the Cauchy--Schwarz inequality.
=--

## Subspaces and Complements

