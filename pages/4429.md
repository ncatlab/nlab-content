
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

The [[differential geometry|differential-geometric]] "Chern-Weil"-construction (evaluating [[curvature 2-forms]] of [[connection on a principal bundle|connections]] in [[invariant polynomials]]) is due to

* [[Henri Cartan]], Section 7 of: _Cohomologie réelle d'un espace fibré principal différentiable. I : notions d'algèbre différentielle, algèbre de Weil d'un groupe de Lie _, Séminaire Henri Cartan, Volume 2  (1949-1950), Talk no. 19, May 1950  ([numdam:SHC_1949-1950__2__A18_0](http://www.numdam.org/item/?id=SHC_1949-1950__2__A18_0))

  \linebreak

  [[Henri Cartan]], Section 7 of: _Notions d'algèbre différentielle; applications aux groupes de Lie et aux variétés o&ugrave; opère un groupe de Lie_, in: Centre Belge de Recherches Mathématiques, _Colloque de Topologie (Espaces Fibrés) Tenu &agrave; Bruxelles du 5 au 8 juin 1950_, Georges Thon 1951 ([GoogleBooks](https://books.google.de/books/about/Colloque_de_topologie_espaces_fibres.html?id=sagqHQAACAAJ&redir_esc=y))

  \linebreak

  (These two articles have the same content, with the same section outline, but not the same wording. The first one is a tad more detailed.)

and around equation (10) of:

* {#Chern50} [[Shiing-shen Chern]], _Differential geometry of fiber bundles_, in: Proceedings of the International Congress of Mathematicians, Cambridge, Mass., (August-September 1950), vol. 2, pages 397-411,  Amer. Math. Soc., Providence, R. I. (1952) ([[Chern-DifferentialGeometryOfFiberBundles.pdf:file]], [full proceedings vol 2 pdf](https://www.mathunion.org/fileadmin/ICM/Proceedings/ICM1950.2/ICM1950.2.ocr.pdf))

It is the independence of this construction under the choice of connection which [Chern 50](#Chern50) atributes (below (10)) to 

* [[André Weil]], _Géométrie différentielle des espaces fibres_, unpublished, item [1949e] in: _André Weil Oeuvres Scientifiques / Collected Papers_, vol. 1 (1926-1951), 422-436, Springer 2009 ([ISBN:978-3-662-45256-1](https://www.springer.com/gp/book/9783662452561))

But the main result of [Chern 50](#Chern50) is that this differential-geometric "Chern-Weil" construction is equivalent to the topological ([[homotopy theory|homotopy theoretic]]) construction of pulling back the [[universal characteristic classes]] from the [[classifying space]] $B G$ along the [[classifying map]] of the given [[principal bundle]]:

This claim is equation (15) in [Chern 50](#Chern50), using (quoting from the same page):

> methods initiated by [[Eli Cartan|E. Cartan]] and recently developed with success by [[Henri Cartan|H. Cartan]], [[Claude Chevalley|Chevalley]], [[Jean-Louis Koszul|Koszul]], [[Jean Leray|Leray]], and [[André Weil|Weil]] [13]

Here reference 13 is:

* [[Jean-Louis Koszul]], _Homologie et cohomologie des algebres de Lie_, Bull. Soc. Math. France vol. 78 (1950) pp. 65-127 ([numdam:BSMF_1950__78__65_0](http://www.numdam.org/item/BSMF_1950__78__65_0))

Later, an independent proof of the universal topological "Chern-Weil"-construction $inv(\mathfrak{g}) \to H^\bullet(B G)$ is given in:

* [[Raoul Bott]], _On the Chern-Weil homomorphism and the continuous cohomology of Lie-groups_, Advances in Mathematics Volume 11, Issue 3, December 1973, Pages 289-303 (<a href="https://doi.org/10.1016/0001-8708(73)90012-1">doi:10.1016/0001-8708(73)90012-1</a>)

Review of the Chern-Weil construction :

* [[Shiing-Shen Chern]], [[James Simons]], Section 2 of: _Characteristic Forms and Geometric Invariants_, Annals of Mathematics Second Series, Vol. 99, No. 1 (Jan., 1974), pp. 48-69 ([jstor:1971013](https://www.jstor.org/stable/1971013))

  (in the context of [[Chern-Simons forms]])

* Adel Rahman, _Chern-Weil theory_, 2017 ([[RahmanChernWeilTheory.pdf:file]])


Textbook accounts include

* {#KobayashiNomizu63} Shoshichi Kobayashi, Katsumi Nomizu, _Foundations of Differential Geometry_, Wiley 1963 ([web](https://www.zuj.edu.jo/download/foundations-of-differential-geometry-vol-1-kobayashi-nomizu-pdf/), [Wikipedia](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry))

* [[John Milnor]], [[Jim Stasheff]], Appendix C of: _Characteristic classes_, Princeton Univ. Press (1974) ([ISBN:9780691081229](https://press.princeton.edu/books/paperback/9780691081229/characteristic-classes-am-76-volume-76))

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)




The description of the refined Chern-Weil homomorphism in terms of [[differential function complex]]es is in section 3.3. of 

* {#HopkinsSinger} [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology,and M-Theory]]_
 


For more references see [[Chern-Weil theory]].


[[!redirects Weil homomorphism]]
