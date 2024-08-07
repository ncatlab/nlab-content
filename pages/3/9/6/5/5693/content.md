
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

[Milnor 1964](#Milnor64) introduced the notion of the *link group* as a way to study [[links]].  The notion of equivalence of links that Milnor used is slightly different to that obtained by extending the usual notion of equivalence of [[knots]].  In Milnor's paper, the crucial aspect of links was the interactions between distinct components.  Thus for Milnor, a link in a manifold $M$ is a map $\coprod_n S^1 \to M$ such that the components have disjoint images.  Similarly, two links are **homotopic** if there is a [[homotopy]] between the maps which is a link at every time.  Thus links can be deformed in such a manner that individual components can pass through themselves, but not through other components.  Also link components can have self-intersections or the map on a component can be a constant map.  Milnor uses the term **proper link** to refer to a link in which the map is a homeomorphism onto its image.

The [[Whitehead link]] is a simple example of a link that is not trivial under ambient [[isotopy]] but is trivial under Milnor's notion of homotopy.

The $\mu$-[[invariants]] come from explicit descriptions of the link groups of particular links.  Specifically, Milnor calls a link _almost trivial_ if every proper sublink is trivial (see [[Brunnian link]]).  Such a link corresponds to an element in a particular link group which can be completely described by certain numbers.

## Link Group

Let us begin by describing the link group.  Milnor's alternative description is as follows.  Consider the complement of a link $L$ in an open $3$-manifold $M$.  We choose a [[basepoint]] in this complement and so have the [[fundamental group]].  We define a relation on this group as follows: two loops $\alpha$, $\beta$ are equivalent if the link $L \cup \alpha^{-1} \beta$ is homotopic in $M$ to one of the form $L' \cup 1$ (where $1$ is the constant loop at the basepoint).  The **link group** is the group of equivalence classes of such loops.

A more practical description is the following.

+-- {: .num_defn #linkgroup}
###### Definition
Let $L$ be a link in an open $3$-manifold $M$.
Let $G(L)$ be the fundamental group of the complement of $L$.  Let $L^i$ denote the sublink obtained by deleting the $i$th component of $L$.  Let $A_i(L)$ be the kernel of the natural inclusion $G(L) \to G(L^i)$ and $[A_i]$ its commutator subgroup.  Let $E(L) = [A_1] [A_2] \cdots [A_n]$.  This is a normal subgroup of $G(L)$.  The quotient, $\mathcal{G}(L) \coloneqq G(L)/E(L)$ is the **link group** of $L$.
=--

Milnor's first theorem on this group was to show that this group is an invariant of the homotopy class of the link, at least for proper links.

+-- {: .num_theorem #htyinv}
###### Theorem ([Milnor, Theorem 1](#jmLinkGroups)) ######
If two proper links are homotopic, then their link groups are isomorphic.
=--

To study this group for a particular link, we need to find some particular elements in it.  These are the **meridians** and the **parallels**.  Basically, a meridian goes around one component of the link once, in a specific direction, whilst a parallel goes along it.  Technically, the parallels of a link are not _elements_ of its link group, but cosets.

Choose a component $L_i$ of the link $L$.  Choose orientations of the ambient manifold, $M$, and of the circle.
To define the meridian and parallel of $L_i$ we need to choose a path from the basepoint, $x_0$, to a point on the image of $L_i$ which does not intersect the image of $L$ at any other time.  Let $p$ be such a path, so then $p(1)$ is a point on the image of $L_i$.

+-- {: .num_defn #meridian}
###### Definition
The **$i$th meridian** of $L$ is the element $\alpha_i \in \mathcal{G}(L)$ defined as follows.  Choose a small neighbourhood $N$ of $p(1)$.  Define a path by going along $p$ until we are inside $N$, then go around a closed loop in $N$ which has linking number $+1$ with the part of the image of $L_i$ inside $N$.  Then return to $x_0$ along $p$.
=--

+-- {: .num_defn #parallel}
The **$i$th parallel** of $L$ is the coset $\beta_i \mathcal{A}_i \in \mathcal{G}(L^i)$ defined as follows.  The subgroup $\mathcal{A}_i$ is the kernel of the homomorphism $\mathcal{G}(L) \to \mathcal{G}(L^i)$.  Go along $p$ to its end.  Then go around the image of $L_i$ according to the orientation of the circle.  Finally return to $x_0$ along $p$.  The preimage of this element defines a coset in $\mathcal{G}(L)$ which we write as $\beta_i \mathcal{A}_i$.
=--

The basic method of studying a link via link groups is to consider a link as an element of the link group of the link obtained by removing one of its components.  To show that this is a reasonable thing to do, Milnor proved the following theorem.

+-- {: .num_theorem #conjelts}
###### Theorem ([Milnor, Theorem 3](#jmLinkGroups)) ######
Let $L$ be a proper link with $n$ components.  Let $f$, $f'$ be closed loops in the complement of $L$.  If they represent conjugate elements of $\mathcal{G}(L)$ then the links $(L,f)$ and $(L,f')$ are homotopic.
=--

## $\mu$-Invariants

For [[Brunnian links]], which Milnor calls **almost trivial** links, the classification question reduces to looking at elements of the link group of trivial links.  It is important to note that the ambient space here is Euclidean space, $\mathbb{R}^3$.

Let $L$ be an $n$-component Brunnian link.  Then we consider the element $\beta'_n \in \mathcal{G}(L^n)$ corresponding to the $n$th parallel.  Upon removing a further component, say the $n-1$st, this element becomes trivial since we are then looking at $L^{n-1}$ which is trivial.  Thue $\beta'_n \in \mathcal{A}_{n-1}(L^n)$, the kernel of $\mathcal{G}(L^n) \to \mathcal{G}(L^{n-1,n})$ (here $L^{n-1,n}$ is $L$ with both the $n-1$st and $n$th components removed).  Now $\mathcal{A}_{n-1}(L^n)$ is the smallest normal subgroup containing the meridian $\alpha_{n-1}$ (since removing the $n-1$st component is the same thing as allowing the meridian $\alpha_{n-1}$ to collapse) and so every element of $\mathcal{A}_{n-1}$ can be written as a word in alphabet of powers and conjugates of $\alpha_{n-1}$.  Milnor uses the notation
$$
\alpha_{n-1}^\sigma, \quad \sigma \in \mathcal{R}(L^{n-1,n})
$$
to write this.  The exponent $\sigma$ itself decomposes as
\[
\label{muinvs}
\sigma = \sum \mu(i_1 \cdots i_{n-2}, n-1 n) k_{i_1} \cdots k_{i_{n-2}}
\]
where the summation is over all permutations $i_1 \cdots i_{n-2}$ of $1$, $2$, ..., $n-2$.

+-- {: .num_theorem #muinvs}
###### Theorem ([Milnor, Section 5](#jmLinkGroups))
The integers $\mu(i_1 \cdots i_{n-2}, n_1 n)$ are homotopy invariants of $L$.  The homotopy class of $L$ is completely specified by these integers.
=--

There was nothing special about the choice of components.  A similar procedure works for any pair of components.  The resulting integers obey the following rules:

\[
\begin{aligned}
\mu(i_1 i_2 \cdots i_{n-2}, i_{n-1} i_n) &= \mu(i_n i_1 i_2 \cdots i_{n-3}, i_{n-2} i_{n-2}) \\
\mu(i_1 \cdots i_{\nu} r j_1 \cdots j_{n-\nu-2} s) &= (-1)^{n-\nu} \sum \mu(h_1 \cdots h_{n-2} r s)
\end{aligned}
\]

In the second identity, the summation is over all shuffle products of $(i_1 \cdots i_{\nu})$ with $(j_1 \cdots j_{n - \nu - 2})$.

Let us expand on the definition of the $\mu$-invariants.  We start with the exponential notation.  The following holds for an arbitrary proper link, $L$, embedded in an open $3$-manifold $M$.

Let $J \mathcal{G}(L)$ be the integral group ring of $\mathcal{G}(L)$.  As mentioned above, any element of $\mathcal{A}_i(L)$ is a product of powers of conjugates of $\alpha_i$.  We can write such an element in the form $\alpha_i^s$ for $s \in J \mathcal{G}(L)$ by interpreting:
$$
\begin{aligned}
\alpha_i^{x + y} &= \alpha_i^x \alpha_i^y \\
\alpha_i^{k x} &= (\alpha_i^x)^k \\
\alpha_i^\beta &= \beta \alpha \beta^{-1}
\end{aligned}
$$
where $x, y \in J\mathcal{G}(L)$, $k \in \mathbb{Z}$, and $\beta \in \mathcal{G}(L)$.

We write the kernel of $J \mathcal{G}(L) \to J \mathcal{G}(L^i)$ as $\mathcal{K}_i(L)$.  Using these, we define:
$$
\mathcal{R}(L) \coloneqq J \mathcal{G}(L) / \mathcal{K}_1(L)^2 + \cdots + \mathcal{K}_n(L)^2
$$

Now the notation $\alpha_i^s$ for an element of $\mathcal{A}_i(L)$ does not provide an injective map from $J\mathcal{G}(L)$ to $\mathcal{A}_i(L)$.  The kernel is the ideal $\mathcal{K}_i(L) + (\mathcal{K}_1(L)^2 + \cdots + \mathcal{K}_n(L)^2)$ which is naturally isomorphic to $\mathcal{R}(L^i)$.

+-- {: .num_theorem #trivlink}
###### Theorem ([Milnor, Theorem 5](#jmLinkGroups))
Let $L$ be a link which is homotopic to one in with the $i$th component is constant.  Then every element of $\mathcal{A}_i(L)$ can be expressed uniquely in the form $\alpha_i^\sigma$ with $\sigma \in \mathcal{R}(L^i)$.
=--

Now let us suppose that $L$ is trivial.  Then $G(L)$ is the free product of the fundamental group of $M$ with the infinite cyclic groups generated by the (elements representing the) meridians of $L$.  Let these be $a_1$, ..., $a_n$ and let $k_i = a_i - 1$ in $J G(L)$.  Milnor defines a **canonical word** to be a product of the form $\phi_0 k_{j_1} \phi_1 k_{j_2} \phi_2 \cdots k_{j_p} \phi_p$ with $p \ge 0$, $\phi_i \in \pi_1(M)$, and $1 \le j_i \le n$.  A **canonical sentence** is a sum or difference of any number of canonical words.  It turns out ([Milnor, Theorem 7](#jmLinkGroups)) that each element of $\mathcal{R}(L)$ is represented by a unique canonical sentence.

Now let us return to the case of the almost trivial link in Euclidean space.  From above, we have the element $\beta'_n \in \mathcal{A}_i(L^n)$ corresponding to the $n$th parallel.  Removing any other component allows us to trivialise $\beta'_n$ since removing, say, the $i$th component leaves us with $L^i$ which is homotopic to the trivial link on $n-1$ components.  Removing the $i$ component corresponds to setting $a_i$ to $1$ in $J G(L^n)$, equivalently to setting $k_i = 0$.  So upon setting $k_i = 0$ we must have that $\beta'_n \mapsto 1$ and thus (by uniqueness) $\sigma \mapsto 0$.  Hence $k_i$ divides $\sigma$, and so every canonical word in $\sigma$ is of the form $k_{i_1} \cdots k_{i_{n-2}}$ for some permutation of $1$, $2$, ..., $n-2$.  Sorting them out by permutation, we get the expression in \eqref{muinvs}.

Now, how do we interpret or calculate these invariants?  We need to work out what an expression of the form in \eqref{muinvs} is saying.  Consider a canonical word, $k_{i_1} \cdots k_{i_{n-2}}$.  The corresponding element is:
$$
\alpha_{n-1}^{k_{i_1} \cdots k_{i_{n-2}}}
$$
Let us write $\alpha = \alpha_{n-1}$.  Now $\alpha^{k_1}$ is $\alpha^{a_1 - 1} = a_1 \alpha a_1^{-1} \alpha^{-1}$.  Thus this tells us to go around $L_1$, then $L_{n-1}$, back around $L_1$, and finally back around $L_{n-1}$.  Each time we introduce a new power, we do the same except that we replace the loop around $L_{n-1}$ with the loop so far constructed.

So the general method is as follows: choose two components of the link.  Write one of them as a word in the meridians of the others.  Then simplify this word using the other chosen link as the "base": namely, write everything in terms of conjugates of that base.  This will then separate out into the desired form and, hopefully, the link invariants can be read off.



## References

* {#Milnor64} [[John Milnor]]: *Link groups*, Ann. of Math. **2** 59 (1954) 177-195 &lbrack;[doi:10.2307/1969685](https://doi.org/10.2307/1969685), [jstor:1969685](https://www.jstor.org/stable/1969685), [MR](http://www.ams.org/mathscinet-getitem?mr=71020)&rbrack;

* Wikipedia, *[Link group](https://en.wikipedia.org/wiki/Link_group)*

[[!redirects Milnor mu-bar invariants]]


[[!redirects link group]]
[[!redirects link groups]]

