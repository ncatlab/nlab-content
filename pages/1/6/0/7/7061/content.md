
# Contents
* tic
{: toc}

## Idea

Recall that the $n$th [[symmetric product]] (or symmetric power) of a space, say $X$, is what you get if you take $n$ points in $X$ without considering the order in which they appear.  Since repetitions are allowed, one has to think carefully as to how to deal with multiplicities: either to respect them or to ignore them.
The first case, respecting multiplicities, means that $\{0,1,1\}$ and $\{0,0,1\}$ are not considered equivalent.  The second means that they are.

On this page we use the first definition, respecting multiplicities, and work with the [[circle]], $S^1$, as our original space.  The resulting spaces have straightforward descriptions and simple [[homotopy types]]: all are homotopic to the circle.  These descriptions can be found in [MR0210096](#MR0210096)

There is a link between this space and the [[unitary group]] of a finite dimensional complex [[Hilbert space]].  The conjugacy class of a [[unitary matrix]] is determined completely by its [[eigenvalue]]s with their multiplicities in that two unitary matrices are conjugate if and only if their sets-with-multiplicities ([[multiset|bags]]) of eigenvalues are the same.  The eigenvalues of a unitary matrix lie on a circle, but as we are considering the collections as sets and not ordered sets, we must consider the set of eigenvalues as a point in the symmetric product of the circle.  Hence knowing this space tells us about the space of conjugacy classes of unitary matrices.


## Definition

The notion of the *symmetric product* of a [[topological space]] is an application of the construction of the [[symmetric power]] in a symmetric monoidal category, where the category is $\Top$ and the monoidal structure is given by the cartesian product.

+-- {: .num_defn #sympcircle}
###### Definition
Let $X$ be a topological space.  Let $n \in \mathbb{N}$.  The **$n$th symmetric product** of $X$, written $SP^n(X)$, is quotient of $X^n$ by the action of the $n$th symmetric group acting by permuting the coordinates.
=--

On this page, we are most interested in the case $X = S^1$ but it will be instructive to consider also $\mathbb{C}^*$, the non-zero complex numbers, and $\mathbb{R}$.  This is because of the existence of the inclusion $S^1 \to \mathbb{C}^*$ and the exponential map $\mathbb{R} \to S^1$.

## Properties

The main property of $SP^n(S^1)$ is the following description, due to H. R. Morton in [MR0210096](#MR0210096).

+-- {: .num_prop #symcirdesc}
###### Proposition
The topological space $SP^n(S^1)$ is a fibre bundle over $S^1$ with fibre an $n-1$ [[simplex]].  If $n$ is odd, the bundle is orientable; if $n$ is even then it is not.

In particular, $SP^2(S^1)$ is a M&#246;bius strip.
=--

Before proving this, let us give the descriptions of $SP^n(\mathbb{C}^*)$ and $SP^n(\mathbb{R})$.

+-- {: .num_prop #symcplx}
###### Proposition
The topological space $SP^n(\mathbb{C}^*)$ is homeomorphic to $\mathbb{C}^{(n-1)} \times \mathbb{C}^*$.
=--

+-- {: .proof}
###### Proof
The proof rests on giving an alternative description of $SP^n(\mathbb{C}^*)$ in which the lack of ordering of the points is built in at the start.  This description is given by taking the polynomial whose roots are the points (here we can see why it is important to take note of the multiplicities).

We define a map $SP^n(\mathbb{C}^*) \to \Poly_n$, the space of polynomials of degree at most $n$, by sending $[\zeta_1,\dots,\zeta_n]$ to the monic polynomial $(z - \zeta_1)\cdots (z - \zeta_n)$.  This is a [[homeomorphism]] onto its image.  That image is the space of monic polynomials with non-zero constant term (as all the $\zeta_j$ are non-zero).  There is an obvious homeomorphism of this space to $\mathbb{C}^{n-1} \times \mathbb{C}^*$ given by taking coefficients.
=--

This space is relevant because the construction $SP^n(-)$ respects homotopy equivalences.  Hence $SP^n(S^1)$ is homotopy equivalent to $S^1$ and the map $SP^n(S^1) \to S^1$ is given by multiplying the $n$ elements of a point in $SP^n(S^1)$.

+-- {: .num_cor #sphaus}
###### Corollary
The space $SP^n(S^1)$ is Hausdorff.
=--

+-- {: .proof}
###### Proof
It embeds in the Hausdorff space $SP^n(\mathbb{C}^*)$.
=--

+-- {: .num_prop #symreal}
###### Proposition
The space $SP^n(\mathbb{R})$ is homeomorphic to $\mathbb{R} \times (\mathbb{R}_+)^{n-1}$.
=--

+-- {: .proof}
###### Proof
The idea of this proof is that although in $SP^n(\mathbb{R})$ an $n$-tuple of points has no intrinsic order (due to the action of the symmetric group), we can always impose an order from "outside" by taking the points in the order in which they occur in $\mathbb{R}$.  Thus any element of $SP^n(\mathbb{R})$ has a unique representation as $(t_1,t_2,\dots,t_n)$ where $t_j \le t_{j+1}$.  We define the map $SP^n(\mathbb{R}) \to \mathbb{R} \times (\mathbb{R}_+)^{n-1}$ by:
$$
(t_1,t_2, \dots, t_n) \mapsto (t_1, t_2 - t_1, t_3 - t_2, \dots, t_n - t_{n-1}).
$$

There is another map which is worth mentioning.  The space $\mathbb{R}^n$ has an invariant subspace under the action of the symmetric group (the $n$-fold diagonal) and it is possible to find a homeomorphism $SP^n(\mathbb{R}) \to \mathbb{R} \times (\mathbb{R}_+)^{n-1}$ where the first map is the orthogonal projection onto this subspace.  The projection is given by the map which sends $\{t_1,\dots,t_n\}$ to the average value.  The fibre of this map is the quotient by the action of the symmetric group of the space of vectors in $\mathbb{R}^n$ whose components sum to zero.  As they sum to zero, knowing the differences between the points (in the order imposed from $\mathbb{R}$) is enough to specify the points themselves.  The resulting map is thus:
$$
(t_1,t_2,\dots,t_n) \mapsto \left(\frac{1}{n} \sum t_j, t_2 - t_1, \dots, t_n - t_{n-1}\right).
$$
=--

+-- {: .proof}
###### Proof of Proposition \ref{symcirdesc} ######

Now let us prove the proposition.  Guided by the description for $SP^n(\mathbb{C}^*)$, we define $p \colon SP^n(S^1) \to S^1$ by $p(\{\zeta_1,\dots,\zeta_n\}) = \zeta_1 \dots \zeta_n$.  Let us show that this is a fibre bundle.  For $\lambda \in S^1$ we define a map $p^{-1}(\lambda) \times (S^1 \setminus \{\overline{\lambda}\}) \to p^{-1}(S^1 \setminus \{\overline{\lambda}\})$ by:

$$
p(\{\zeta_1,\dots,\zeta_n\},\lambda e^{i t}) = \{\zeta_1 e^{i t/n}, \dots, \zeta_n e^{i t/n}\}
$$

where $t \in (-\pi,\pi)$.

It remains to determine the fibre at $1$ and the gluing map at, say, $-1$.

To do this, we consider the exponential map $SP^n(\mathbb{R}) \to SP^n(S^1)$.  We use the second description of $SP^n(\mathbb{R})$ as $\mathbb{R} \times (\mathbb{R}_+)^{n-1})$ to view $SP^n(\mathbb{R})$ as a bundle over $\mathbb{R}$.  With this picture, the exponential map $SP^n(\mathbb{R}) \to SP^n(S^1)$ is a bundle map covering the exponential map $\mathbb{R} \to S^1$.  In particular, we have an induced map $(\mathbb{R}_+)^{n-1} \to p^{-1}(1)$ given by the following recipe:

1. Start with $(r_1,r_2,\dots,r_{n-1}) \in (\mathbb{R}_+)^{n-1}$.
2. Form the sequence of partial sums $(s_1,s_2,\dots,s_n)$ where $s_k = \sum_{j \lt k} r_j$.  Note that $s_1 = 0$.
3. Adjust so that their average (equivalently, sum) is $0$ by setting $t_k = s_k - \frac{1}{n} \sum s_j$.
4. Apply the exponential function to produce $\{e^{2 \pi i t_k}\}$ in $SP^n(S^1)$.

To use this to identify the fibre of $p^{-1}(1)$ we restrict this to a simplex.  The simplex that we choose at the start is:
$$
\Delta^n = \{(r_1,r_2,\dots,r_{n-1}) \in [0,1]^n : \sum r_j \le 1\}.
$$
At the second step, this becomes:
$$
\{(s_1,s_2,\dots,s_n) \in [0,1]^n : s_j \le s_{j+1}\}.
$$
At the third step, this becomes:
$$
\{(t_1,t_2,\dots,t_n) \in \mathbb{R} : \sum t_j = 0,\; t_n \le t_1 + 1\}.
$$
Thus far, all the maps are by homeomorphisms of their ambient spaces and so are homeomorphisms as they are bijections.

We now wish to determine the image of this in $SP^n(S^1)$.  Let $\{\zeta_1,\dots,\zeta_n\}$ be a point in $p^{-1}(1)$.  We order them cyclically around the circle going anticlockwise.  To turn this into a proper order, we need to choose a first point.  If that point is a multiple point, we do not assume that the other points follow immediately after it: some may but the others may occur at the end of the list when we have gone all around the circle.  With a multiple point then the decision that that contains the first point also contains a partition of the multiplicities into "at the start of the list" and "at the end of the list".

Having chosen the first point, we now choose a preimage of that point in $\mathbb{R}$, say $t_1$.  This defines a logarithm on the circle with branch cut at the first point.  We then proceed around the circle, lifting the other points to $\mathbb{R}$ using the same logarithm.  If the chosen point had multiplicities and some are at the end of the list, then these are lifted consistently with having gone around the circle, which means that they are lifted to $t_1 + 1$.  The result of this lifting is a set of points $(t_1,t_2,\dots,t_n)$ with $t_j \le t_{j+1}$ and $t_n \le t_1 + 1$.  The sum of these points in the line is in the preimage of the product of the points in the circle and thus is an integer.

To see that we can obtain any integer for the sum, consider what happens if we change our choice of first point to the next point anticlockwise.  If our original point was multiple and there are others at the start of the list then this means that we shift one point to the end of the list.  If we have moved to a new point and it is multiple, then we put all of its points at the start of the list and none at the end.  When looking at what happens to the logarithm, we have shifted the cut around (possibly) and now lift starting at $t_2$.  The last point that we reach is the one below $t_1$, but we have gone around the circle so we actually reach $t_1 + 1$.  Thus the lift of the $n$-tuple of points is now $(t_2,t_3,\dots,t_n,t_1+1)$.  The sum has increased by $1$.  Hence by choosing the right first point, and the right start to the logarithm, we can ensure that we get an $n$-tuple of points in $\mathbb{R}$ which sum to $0$.  The conclusion of all of this is that at the fourth step, when restricting everything to the simplex, the map is surjective onto $p^{-1}(1)$.

It is also injective.  The above discussion shows that changing the choice of first point changes the sum by integral values and it is also clear that changing the starting point of the logarithm changes it by multiples of $n$.  It is therefore not possible to find two distinct starting points and two distinct lifts which both sum to $0$.

As the simplex is compact and $p^{-1}(1)$ is Hausdorff, the map $\Delta^n \to p^{-1}(1)$ is thus a homeomorphism.

The last step is to identify the transition map.  As we go around the circle, we need to adjust the above to take into account the variation in sum.  This can be done at the last step where we map to $SP^n(S^1)$ by multiplying each term by $e^{2 \pi i \tau/n}$, where $e^{2 \pi i \tau}$ is the desired product of all the points.  The effect that this has on the logarithm is, after a complete revolution, to add $\frac{1}{n}$ to each component.  This results in an $n$-tuple with sum $1$ so to correct that we have to move one term from the end to the beginning.  This results in a coordinate transformation $(t_1,t_2,\dots,t_n) \mapsto (t_n - 1, t_1, t_2, \dots, t_{n-1})$ which is orientable if $n$ is odd and unorientable if $n$ is even.
=--

Let us illustrate this for the case $n = 2$.  Then $SP^2(S^1)$ consists of equivalence classes of pairs of points $\{\zeta_1,\zeta_2\}$ in $S^1$, with repetition allowed.  In the fibre of $p$ at $1$ we have the condition $\zeta_1 \zeta_2 = 1$ and so we can write our pair as $\{\zeta,\overline{\zeta}\}$.

On the subset $\zeta \ne -1$ there is a clear parametrisation with domain $[0,1)$ given by $t \mapsto \{e^{i \pi t}, e^{-i \pi t}\}$.  The claim is that this extends to a homeomorphism $[0,1] \to p^{-1}(1)$ by sending $1$ to $\{-1,-1\}$.  We can define the inverse map directly by sending $\zeta$ to $\Re(\zeta)$ and then composing with an appropriate inverse trigonometric function, but it is more instructive to consider why this works.

Let us imagine that we approach $\{-1,-1\}$ and pass through it.  Both before and after, we have two dots moving around the circle mirroring each other.  At the crucial time, they meet at $-1$, and then move apart again.  Since they are mirroring each other, one comes back along the top part of the circle and one along the bottom.  The crucial piece of the puzzle is that we cannot tell which is which.  So as far as we are concerned, the two dots may have passed through each other or may have bounced back off each other again.

Hence the fibre at $p^{-1}(1)$ is $[0,1]$.

Now consider what happens as we move around the circle.  Suppose that we look at a path on the boundary which starts at the image of $0$ as we move around, then when we are at $e^{2 \pi i t} \in S^1$, we have two points at $e^{\pi i t}$.  After going round a full revolution, our double point has only reached $e^{\pi i} = -1$ which is the image of $1$.  Hence we have a M&#246;bius strip.


## Conjugacy Classes of Unitary Matrices

The symmetric product $SP^n(S^1)$ can be identified with the space of conjugacy classes of unitary transformations on $\mathbb{C}^n$, aka unitary $n \times n$-matrices.  This is because the conjugacy class of a unitary transformation is characterised by the eigenvalues of a matrix in the class, including their multiplicities, and these lie in $S^1$.  Hence $U_n/conj \simeq SP^n(S^1)$ and the induced map $U_n \to S^1$ is the [[determinant]] mapping.


## References

* Morton, H. R. (1967). Symmetric products of the circle. _Proc. Cambridge Philos. Soc._, _63_, 349&#8211;352.  [MR0210096](http://www.ams.org/mathscinet-getitem?mr=210096)
{#MR0210096}
