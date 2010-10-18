
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An _Eilenberg--Mac Lane space_ is a connected [[topological space]] with nontrivial [[homotopy groups]] only in a single degree.

## Definition

For $G$ a [[group]], the Eilenberg--Mac Lane space $K(G,1)$ is the image under the [[homotopy hypothesis]] [[Quillen equivalence]] $|-| : \infty Grpd \to Top$ of the one-object groupoid $\mathbf{B}G$ whose [[hom-set]] is $G$:

$$
  K(G,1) = | \mathbf{B} G |
  \,.
$$

If $G$ is a group and $n \geq 1$ then an **Eilenberg--Mac Lane space** $K(G,n)$ is a connected space  with its only non-trivial homotopy group being $G$ in dimension $n$, thus $G$ must necessarily be abelian for $n \geq 2$. 

The construction of such a space can be given for $n \geq 2$ using the standard [[Dold-Kan correspondence]] between chain complexes and simplicial abelian groups: let $C(G,n)$ be the chain complex which is $G$ in dimension $n$ and trivial elsewhere; the geometric realisation of the corresponding simplicial abelian group is then a $K(G,n)$. 

We can include the case $n=1$ when $G$ may be nonabelian, by regarding $C(G,n)$ as a [[crossed complex]]. Its [[classifying space]] $B(C(G,n))$ is then a $K(G,n)$. (This also includes the case $n=0$ when $G$ is just a set!) This method also allows for the construction of $K(M,n;G,1)$ where $G$ is a group, or groupoid,  and $M$ is a $G$-module. This gives a space with $\pi_1 =G$, $\pi_n=M$ all other homotopy trivial, and with the given operation of $\pi_1$ on $\pi_n$. 


For $A$ an abelian group, the Eilenberg--Mac Lane space $K(A,n)$ is the image of the [[∞-groupoid]] $\mathbf{B}^n A$ that is the [[strict ∞-groupoid]] given by the [[crossed complex]] $[\mathbf{B}^n A]$ that is trivial everywhhere except in degree $n$, where it is $A$:

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

Therefore Eilenberg--Mac Lane spaces constitute a [[spectrum]]: the [[Eilenberg?Mac Lane spectrum]].

In general, if $A$ is an abelian [[topological group]], then there exist a model for the [[classifying space]] $\mathcal{B}A$ which is an abelian topological group. Iterating this construction, one has a notion of $\mathcal{B}^n A$ and a model for it which is an abelian topological group. If moreover $A$ is discrete, then $\mathcal{B}A=|\mathbf{B}A|=K(A,1)$, and one inductively sees that $\mathcal{B}^n A=|\mathbf{B}^n A|=K(A,n)$. Therefore one has a model for $K(A,n)$ which is an abelian topological group.



## Cohomology 

One common use of Eilenberg--Mac Lane spaces is as coefficient objects for "ordinary" [[cohomology]].

The $n$th "ordinary" [[cohomology]] of a [[topological space]] $X$ with coefficients in $G$ (when $n=1$) or $A$ (generally) is the collection of [[homotopy]] classes of maps from $X$ into $K(G,1)$ or $K(A,n)$, respectively:

$$
  H^1(X,G) = Ho_{Top}(X, K(G,1)) = Ho_{\infty Grpd}(X, \mathbf{B} G)
$$

$$
  H^n(X,A) = Ho_{Top}(X, K(A,n)) = Ho_{\infty Grpd}(X, \mathbf{B}^n A)
  \,.
$$

Here on the right $Ho_{Top}$ and $Ho_{\infty Grpd}$ denotes the [[homotopy category]] of the [[(∞,1)-categories]] of [[topological spaces]] and of [[∞-groupoids]], respectively. 

Not only the set $\pi_0\mathbf{Top}(X, K(A,n))=Ho_{Top}(X, K(A,n))$ is related to the cohomology of $X$ with coefficients in $A$, but also the higher homotopy groups $\pi_i\mathbf{Top}(X, K(A,n))$ are, and in the most obvious way: if $X$ is a connected CW-complex, then
$$
H^{n-i}(X,A)=\pi_i\mathbf{Top}(X, K(A,n))=\pi_i\mathbf{\infty Grpd}(X, \mathbf{B}^n A),
$$
for any choice of base point on the right hand sides. This fact, which appears to have first been remarked by Thom and Federer, is an immediate consequence of the natural homotopy equivalences
$$
\Omega\mathbf{H}(X,Y)\simeq \mathbf{H}(X,\Omega Y)
$$
and
$$
\Omega K(A,n)\simeq K(A,n-1)
$$
one has in every $(\infty,1)$-[[(infinity,1)-topos|topos]], see [[loop space object]]. For $G$ a nonabelian group, Gottlieb proves the following nonabelian analogue of the above result: let $X$ be a finite dimensional connected CW-complex; for a fixed map $f:X\to K(G,1)$, let $C_f$ be the centralizer in $G=\pi_1 K(G,1)$ of $f_*(\pi_1(X))$. Then the connected component of $f$ in $\mathbf{Top}(X,K(G,1))$ is a $K(C_f,1)$.

Notice that for $G$ a nonabelian group, $H^1(X,G)$ is a simple (and the most familiar) example of [[nonabelian cohomology]]. Nonabelian cohomology in higher degrees is obtained by replacing here the coefficient $\infty$-groupoids of the simple for $\mathbf{B}^n A$ with more general $\infty$-groupoids.

## Generalizations

The notion of [[Eilenberg?Mac Lane object]] makes sense in every $(\infty,1)$-[[(infinity,1)-topos|topos]], not just in [[Top]].


[[!redirects Eilenberg-MacLane space]]
[[!redirects Eilenberg--MacLane space]]
[[!redirects Eilenberg?MacLane space]]
[[!redirects Eilenberg-Mac Lane space]]
[[!redirects Eilenberg--Mac Lane space]]
[[!redirects Eilenberg?Mac Lane space]]
[[!redirects Eilenberg-MacLane spaces]]
[[!redirects Eilenberg--MacLane spaces]]
[[!redirects Eilenberg?MacLane spaces]]
[[!redirects Eilenberg-Mac Lane spaces]]
[[!redirects Eilenberg--Mac Lane spaces]]
[[!redirects Eilenberg?Mac Lane spaces]]