
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

For $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$, a $G$-[[principal bundle]] $P \to X$ on a [[smooth manifold]] $X$ induces a collection of classes in the [[de Rham cohomology]] of $X$: the classes of the [[curvature characteristic form]]s 

$$
  \langle F_A \wedge \cdots F_A \rangle \in \Omega^{2n}_{closed}(X)
$$ 

of the [[curvature]] 2-form $F_A \in \Omega^2(P, \mathfrak{g})$ of any [[connection on a bundle|connection]] on $P$, and for each [[invariant polynomial]] $\langle -\rangle$ of arity $n$ on $\mathfrak{g}$.

This is a map from the first [[nonabelian cohomology]] of $X$ with coefficients in $G$ to the [[de Rham cohomology]] of $X$

$$
  char : H^1(X,G) \to \prod_{n_i} H_{dR}^{2 n_i}(X)
$$

where $i$ runs over a set of generators of the invariant polynomials. This is the analogy in [[nonabelian cohomology|nonabelian]] [[differential cohomology]] of the generalized [[Chern character]] map in [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg-Steenrod]]-[[differential cohomology]].


## Plain Chern-Weil homomorphism

This subsection is to give an outline of construction of Weil homomorphism as in  [Kobayashi-Nomizu 63](#KobayashiNomizu63)

 Let $G$ be a [[Lie group]] and $\mathfrak{g}$ be its [[Lie algebra]]. Given an element $g\in G$, the adjoint map   $Ad(g):G\rightarrow G$  is defined as $Ad(g)(h)=ghg^{-1}$. For $g\in G$, let $ad(g):\mathfrak{g}\rightarrow \mathfrak{g}$ be the differenial of $Ad(g):G\rightarrow G$ at $e\in G$. 

 Let $I^k(G)$ denote the set of symmetric, multilinear maps 
$$
f:\underbrace{\mathfrak{g}\times\cdots\times\mathfrak{g}}_{k ~\text{times}}\rightarrow \mathbb{R}
$$
that are $G$ invariant in the sense that 
$f(ad(g)(t_1),\cdots,ad(g)(t_k))=f(t_1,\cdots,t_k)$
 for all $g\in G$ and $t_i\in \mathfrak{g}$. These $I^k(G)$ are vector spaces over $\mathbb{R}$. Let $I(G)$ denote the $\mathbb{R}$ algebra $\oplus_{k=0}^{\infty}I^k(G)$.

Let $M$ be a manifold and $H^*(M,\mathbb{R})$ be the deRham cohomology ring of $M$. 

Given a principal $G$ bundle over $M$, say $\pi:P\rightarrow M$, Weil homomorphism gives a homomorphism $I(G)\rightarrow H^*(M,\mathbb{R})$. Though it does not depend on connection on $P(M,G)$, the construction of this map is done after fixing a connection on $P(M,G)$.  Outline of the construction is as follows. 

1. Fix a connection $\Gamma$ on $P(M,G)$. Let $\Omega$ denote the curvature of $\Gamma$.

2. Given an element $f\in I^k(G)$, define  a $2k$-form $f(\Omega)$on $P$.
\item Prove that the $2k$ form $f(\Omega)$ on $P$ projects uniquely to a $2k$ form on $M$ and call it $\tilde{f}(\Omega)$ i.e., $\pi^*(\tilde{f}(\Omega))=f(\Omega)$.

3.  Next step is to prove that $\tilde{f}(\Omega)$ is closed $2k$ form on $M$.  To prove $\tilde{f}(\Omega)$ is closed, it suffices to prove that $f(\Omega)$ is closed. 

4. For a **special** $k$-form $\varphi$ on $P$, the exterior differential $d\varphi$ coincides with the exterior covariant differential $D\varphi$ of $\varphi$ i.e., $d\varphi=D\varphi$. That **special** property is  that $\varphi=\pi^*\sigma $ for some $k$-form $\sigma$ on $M$.

5. As $f(\Omega)$ has that **special** property, we see that $d(f(\Omega))=D(f(\Omega))$.

6. By Bianchi's identity, we have $D\Omega=0$. We then see that $D\Omega=0$ implies that $D(f(\Omega))=0$   i.e., $d(f(\Omega))=D(f(\Omega))=0$ for $f\in I^k(G)$ i.e., $f(\Omega)$ is a closed $2k$-form on $P$. Thus, $\tilde{f}(\Omega)$ is a closed $2k$-form on $M$, giving an element in the deRham cohomology $H^{2k}(M,\mathbb{R})$.

7. Next step is to prove that, this assignment $f\mapsto \tilde{f}(\Omega)$ does not depend on the connection $\Gamma$ that we have started with i.e., for connections $\Gamma_0$ (with curvature form $\Omega_0$) and $\Gamma_1$ (with curvature form $\Omega_1$), the elements $\tilde{f}(\Omega_0)$ and $\tilde{f}(\Omega_1)$ are in the same equivalence class i.e., $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)$ is an exact form i.e., $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)=d\tilde{\Phi}$ for some $2k-1$ form $\tilde{\Phi}$ on $M$.

8. Using lemma \ref{useful}, to prove $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)=d\tilde{\Phi}$ for some $2k-1$ form $\tilde{\Phi}$ on $M$,  it suffices to prove that 
$f(\Omega_0)-f(\Omega_1)=d \Phi$ for some $2k-1$ form $\Phi$ on $P$ that projects to a unique $2k-1$ form $\tilde{\Phi}$ on $M$. 

9. We then see that $f(\Omega_0)-f(\Omega_1)=d \Phi$ for some $2k-1$ form $\Phi$ on $P$ that projects to a unique $2k-1$ form $\tilde{\Phi}$ on $M$. This confirm that the assignment $f\mapsto f(\Omega)$ is independent of the connection $\Gamma$ that we have started with. We can extend this linearly to $I(G)\rightarrow H^*(M,\mathbb{R})$.

 Given a principal bundle $\pi:P\rightarrow M$ the morphism  defined above $I(G)\rightarrow H^*(M,\mathbb{R})$ is called the Weil homomorphism.


## Refined Chern-Weil homomorphism

We describe the _refined_ Chern-Weil homomorphism (which associates a class in [[ordinary differential cohomology]] to a [[principal bundle]] with [[connection on a bundle|connection]]) in terms of the [[universal connection]] on the [[universal principal bundle]]. We follow ([HopkinsSinger, section 3.3](#HopkinsSinger)).


* Let $G$ be a [[compact space|compact]] [[Lie group]]

* with [[Lie algebra]] $\mathfrak{g}$;

* and write $inv(\mathfrak{g})$ for the [[dg-algebra]] of [[invariant polynomial]]s on $\mathfrak{g}$ (which has trivial differential).

* Write $B^{(n)}G$ for the smooth level $n$ [[classifying space]] 

* and $B G := {\lim_\to}_n B^{(n)}G$ for the [[colimit]], a smooth model of the [[classifying space]] of $G$.

* Write $\nabla_{univ}$ for the [[universal connection]] on $E G \to B G$.

* Let $[c] \in H^k(B G, \mathbb{Z})$ be a [[characteristic class]] 

* and choose a refinement $[\hat \mathbf{c}] \in H_{diff}^k(B G)$ in [[ordinary differential cohomology]] represented by a [[differential function complex|differential function]]

  $$
    (c, h, w) \in C^k(B G, \mathbb{Z}) \times C^{k-1}(B G, \mathbb{R}) \times (W(\mathfrak{g}) \simeq C^k(B G, \mathbb{R}))^k
    \,.
  $$

+-- {: .num_defn}
###### Definition

For $X$ a [[smooth manifold]], $P \to X$ a smoth $G$-[[principal bundle]] with smooth classifying map $f : X \to B G$ and [[connection on a bundle|connection]] $\nabla$. 
Write $CS(\nabla, f^* \nabla_{univ})$ for the [[Chern-Simons form]] for the interpolation between $\nabla$ and the pullback of the universal connection along $f$.

Then defined the cocycle in [[ordinary differential cohomology]] given by the [[differential function complex|function complex]]

$$
  \hat \mathbf{c} :=
  (f^* c , f^* h + CS(\nabla, f^* \nabla_{univ}), w(F_{\nabla_t}))
  \in
    (c, h, w) \in C^k(B G, \mathbb{Z}) \times C^{k-1}(B G, \mathbb{R}) \times \Omega_{cl}^k(X)
    \,.  
$$

=--

+-- {: .num_prop}
###### Proposition

The above construction constitutes a map

$$
  \hat \mathbf{c} : G Bund_\nabla(X)_\sim \to H_{diff}^k(X)
$$

from [[equivalence class]]es of $G$-[[principal bundle]]s with [[connection on a bundle|connection]] to degree $k$ [[ordinary differential cohomology]].

=--


 


## Examples

* [[Gauss-Bonnet theorem]]

## Related concepts

* [[Sullivan model of classifying space]]


## References

Original articles:

* [[Henri Cartan]], Section 7 of: _Notions d'alg&#233;bre diff&#233;rentielle; applications aux groupes de Lie et aux vari&#233;t&#233;s o&#249; op&#232;re un groupe de Lie_ ,  Coll. Topologie Alg&#233;brique Bruxelles (1950)
15-28

  
* [[Shiing-shen Chern]], _Differential geometry of fiber bundles_ Proceedings of the International Congress of Mathematicians, Cambridge, Mass., 1950, vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952)


* [[Raoul Bott]], _On the Chern-Weil homomorphism and the continuous cohomology of Lie-groups_, Advances in Mathematics Volume 11, Issue 3, December 1973, Pages 289-303 (<a href="https://doi.org/10.1016/0001-8708(73)90012-1">doi:10.1016/0001-8708(73)90012-1</a>)

Textbook accounts include

* {#KobayashiNomizu63} Shoshichi Kobayashi, Katsumi Nomizu, _Foundations of Differential Geometry_, Wiley 1963 ([web](https://www.zuj.edu.jo/download/foundations-of-differential-geometry-vol-1-kobayashi-nomizu-pdf/), [Wikipedia](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry))

* [[John Milnor]], [[Jim Stasheff]], Appendix C of: _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76))

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

Review:

* Adel Rahman, _Chern-Weil theory_, 2017 ([[RahmanChernWeilTheory.pdf:file]])



The description of the refined Chern-Weil homomorphism in terms of [[differential function complex]]es is in section 3.3. of 

* {#HopkinsSinger} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
 


For more references see [[Chern-Weil theory]].


[[!redirects Weil homomorphism]]
