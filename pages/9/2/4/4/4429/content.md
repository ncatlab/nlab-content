
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
  \langle F_A \wedge \cdots \wedge F_A \rangle 
    \;\in\; 
  \Omega^{2n}_{clsd}(X)
$$ 

of the [[curvature]] [[differential 2-form|2-form]] $F_A \in \Omega^2(P, \mathfrak{g})$ of any [[connection on a bundle|connection]] on $P$, and for each [[invariant polynomial]] $\langle -\rangle$ of arity $n$ on $\mathfrak{g}$.

This is a map from the first [[nonabelian cohomology]] of $X$ with coefficients in $G$ to the [[de Rham cohomology]] of $X$

$$
  char 
  \;\colon\; 
  H^1(X,G) 
    \longrightarrow 
  \textstyle{\prod_{n_i}} H_{dR}^{2 n_i}(X)
  \,,
$$

where $i$ runs over a set of generators of the [[invariant polynomials]]. This is the analogue in ordinary [[nonabelian cohomology|nonabelian]] [[differential cohomology]] of the generalized [[Chern character]] map in [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg-Steenrod]]-[[differential cohomology]].


## Plain Chern-Weil homomorphism

We give an outline of construction of Weil homomorphism following [Kobayashi & Nomizu 1963](#KobayashiNomizu63).

\linebreak

 Let $G$ be a [[Lie group]] and $\mathfrak{g}$ be its [[Lie algebra]]. Given an element $g\in G$, the [[adjoint action]]   $Ad(g) \,\colon\, G \longrightarrow G$  is defined as $Ad(g)(h)=g  h g^{-1}$. For $g\in G$, let $ad(g) \,\colon\,\mathfrak{g}\rightarrow \mathfrak{g}$ be the differential of $Ad(g) \,\colon\, G\rightarrow G$ at $e\in G$. 

 Let $I^k(G)$ denote the set of symmetric, multilinear maps 
$$
  f  
  \,\colon\,
  \underset{
    k \; \text{factors}
  }{
    \underbrace{
      \mathfrak{g}\times\cdots\times\mathfrak{g}
    }
  }
   \longrightarrow 
  \mathbb{R}
$$
that are $G$-invariant in that 
$$
  f\big(
    ad(g)(t_1),\cdots,ad(g)(t_k)
  \big) 
  \;=\; 
  f(t_1,\cdots,t_k)
$$
for all $g\in G$ and $t_i\in \mathfrak{g}$. These $I^k(G)$ are [[real vector spaces]]. Let $I(G)$ denote the $\mathbb{R}$ algebra $\oplus_{k=0}^{\infty}I^k(G)$.

Let $M$ be a [[smooth manifold]] and $H^*(M,\mathbb{R})$ be the deRham cohomology ring of $M$. 

Given a $G$-[[principal bundle]] over $M$, say $\pi \colon P\rightarrow M$, the Weil homomorphism gives a homomorphism $I(G)\rightarrow H^*(M,\mathbb{R})$. Though it does not depend on connection on $P(M,G)$, the construction of this map is done after fixing a connection on $P(M,G)$.  Outline of the construction is as follows:

1. Fix a connection $\Gamma$ on $P(M,G)$. Let $\Omega$ denote the curvature of $\Gamma$.

2. Given an element $f\in I^k(G)$, define a $2k$-form $f(\Omega)$ on $P$.

   Prove that the $2k$ form $f(\Omega)$ on $P$ projects uniquely to a $2k$ form on $M$ and call it $\tilde{f}(\Omega)$ i.e., $\pi^*\big(\tilde{f}(\Omega)\big) = f(\Omega)$.

3.  Next step is to prove that $\tilde{f}(\Omega)$ is closed $2k$ form on $M$.  To prove $\tilde{f}(\Omega)$ is closed, it suffices to prove that $f(\Omega)$ is closed. 

4. For a **special** $k$-form $\varphi$ on $P$, the [[exterior differential]] $d\varphi$ coincides with the exterior covariant differential $D\varphi$ of $\varphi$ i.e., $d\varphi=D\varphi$. That **special** property is  that $\varphi=\pi^*\sigma $ for some $k$-form $\sigma$ on $M$.

5. As $f(\Omega)$ has that **special** property, we see that $d\big(f(\Omega)\big) = D\big(f(\Omega)\big)$.

6. By Bianchi's identity, we have $D\Omega=0$. We then see that $D\Omega=0$ implies that $D(f(\Omega))=0$   i.e., $d(f(\Omega))=D(f(\Omega))=0$ for $f\in I^k(G)$ i.e., $f(\Omega)$ is a closed $2k$-form on $P$. Thus, $\tilde{f}(\Omega)$ is a closed $2k$-form on $M$, giving an element in the deRham cohomology $H^{2k}(M,\mathbb{R})$.

7. Next step is to prove that, this assignment $f\mapsto \tilde{f}(\Omega)$ does not depend on the connection $\Gamma$ that we have started with i.e., for connections $\Gamma_0$ (with curvature form $\Omega_0$) and $\Gamma_1$ (with curvature form $\Omega_1$), the elements $\tilde{f}(\Omega_0)$ and $\tilde{f}(\Omega_1)$ are in the same equivalence class i.e., $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)$ is an exact form i.e., $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)=d\tilde{\Phi}$ for some $2k-1$ form $\tilde{\Phi}$ on $M$.

8. Using lemma \ref{useful}, to prove $\tilde{f}(\Omega_0)-\tilde{f}(\Omega_1)=d\tilde{\Phi}$ for some $2k-1$ form $\tilde{\Phi}$ on $M$,  it suffices to prove that 
$f(\Omega_0)-f(\Omega_1)=d \Phi$ for some $2k-1$ form $\Phi$ on $P$ that projects to a unique $2k-1$ form $\tilde{\Phi}$ on $M$. 

9. We then see that $f(\Omega_0)-f(\Omega_1)=d \Phi$ for some $2k-1$ form $\Phi$ on $P$ that projects to a unique $2k-1$ form $\tilde{\Phi}$ on $M$. This confirm that the assignment $f\mapsto f(\Omega)$ is independent of the connection $\Gamma$ that we have started with. We can extend this linearly to $I(G)\rightarrow H^*(M,\mathbb{R})$.

 Given a principal bundle $\pi \,\colon\, P\rightarrow M$ the morphism  defined above $I(G)\rightarrow H^*(M,\mathbb{R})$ is called the Weil homomorphism.


## Refined Chern–Weil homomorphism

We describe the _refined_ Chern–Weil homomorphism (which associates a class in [[ordinary differential cohomology]] to a [[principal bundle]] with [[connection on a bundle|connection]]).

The modern construction is rather short and elegant,
and appears in the work of Bunke–Nikolaus–Völkl and Schreiber.
For an exposition, see, for example, Section 13.1 in Amabel–Debray–Haine [TODO: add reference].

The input data is an arbitrary [[Lie group]] $G$,
an [[invariant polynomial]] $P$ on the [[Lie algebra]] of $G$, and a [[level]] $c\in H^k(B G,\mathbf{Z})$
whose image under the homomomorphism
$$H^k(B G,\mathbf{Z}) \to H^k(B G,\mathbf{R})$$
equals the image of $P$.

The output data is a morphism of [[(∞,1)-sheaves]]
$$B_\nabla G\to B^{2k-1} \mathrm{U}(1)$$
whose image under the characteristic class map equals $c$
and under the curvature map equals the classical Chern–Weil homomorphism associated to $P$.

Perhaps the quickest way to construct this refinement is to observe that $B^{2k-1} \mathrm{U}(1)$ is the [[homotopy pullback]] of $\Omega^{2k}_{closed}$ and $B^{2k}\mathbf{Z}$ over $B^{2k}\mathbf{R}$.
Using the universal property of [[homotopy pullbacks]],
it suffices to construct a compatible pair of maps
$$B_\nabla G\to B^{2k} \mathbf{Z}, \qquad B_\nabla G\to \Omega^{2k}_{closed}.$$
The former map is given by $c$, the latter is given by $P$ via the classical Chern–Weil homomorphism.
They are compatible by assumption on the input data.

## Refined Chern–Weil homomorphism: old construction

Here is a description of an older construction in terms of the [[universal connection]] on the [[universal principal bundle]], following ([HopkinsSinger, section 3.3](#HopkinsSinger)).
It makes an additional assumption that $G$ is compact, which is not necessary in the other approaches.


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

* [[Cartan's map]] in [[equivariant de Rham cohomology]]

* [[Cheeger-Simons homomorphism]]

## References

[[!include Chern-Weil homomorphism -- references]]

### Chern-Weil theory

See also the references at

* [[Chern-Weil theory]]

* [[Chern-Simons forms]]

[[!redirects Weil homomorphism]]
