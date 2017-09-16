#Idea#

An _Eilenberg-MacLane space_ is a connected [[topological space]] with nontrivial [[homotopy group]]s only in a single degree.

#Definition#

For $G$ a [[group]], the Eilenberg-MacLane space $K(G,1)$ is the image under the [[homotopy hypothesis]] [[Quillen equivalence]] $|-| : \infty Grpd \to Top$ of the one-object groupoid $\mathbf{B}G$ whose [[hom-set]] is $G$:

$$
  K(G,1) = | \mathbf{B} G |
  \,.
$$

For $A$ an abelian group, the Eilenberg-MacLane space $K(A,n)$ is the image of the [[infinity-groupoid]] $\mathbf{B}^n A$ that is the [[strict omega-groupoid]] given by the [[crossed complex]] $[\mathbf{B}^n A]$ that is trivial everywhhere except in degree $n$, where it is $A$:

$$
  \begin{aligned}
    [\mathbf{B}^n A] &=
     (  \cdots \to [\mathbf{B}^n A]_{n+1} \to [\mathbf{B}^nA]_{n} \to 
     [\mathbf{B}^n A]_{n-1} \cdots \to [\mathbf{B}^n A]_{1} \stackrel{\to}{\to} [\mathbf{B}^n A]_{0})
      \\ &=
    (  \cdots \to {*} \to A \to 
    {*} \cdots \to {*} \stackrel{\to}{\to} {*})
  \end{aligned}
  \,.
$$


So

$$
  K(A,n) = |\mathbf{B}^n A|
  \,.
$$

Therefore Eilenberg-MacLane spaces constitute a [[spectrum]]: the [[Eilenberg-MacLane spectrum]].

# Cohomology #

One common use of Eilenberg-MacLane spaces is as coefficient objects for "ordinary" [[cohomology]].

The $n$th "ordinary" [[cohomology]]_ of a [[topological space]] $X$ with coefficients in $G$ (when $n=1$) or $A$ (generally) is the collection of [[homotopy]] classes of maps from $X$ into $K(G,1)$ or $K(A,n)$, respectively:

$$
  H^1(X,G) = Ho_{Top}(X, K(G,1)) = Ho_{\infty Grpd}(X, \mathbf{B} G)
$$

$$
  H^n(X,A) = Ho_{Top}(X, K(A,n)) = Ho_{\infty Grpd}(X, \mathbf{B}^n A)
  \,.
$$

Here on the right $Ho_{Top}$ and $Ho_{\infty Grpd}$ denotes the [[homotopy category]] of the [[(infinity,1)-category|(infinity,1)-categories]] of [[topological space]]s and of [[infinity-groupoid]]s, respectively.

Notice that for $G$ a nonabelian group, $H^1(X,G)$ is a simple (and the most familiar) example of [[nonabelian cohomology]]. Nonabelian cohomology in higher degrees is obtained by replacing here the coefficient $\infty$-groupoids of the simple for $\mathbf{B}^n A$ with more general $\infty$-groupoids.