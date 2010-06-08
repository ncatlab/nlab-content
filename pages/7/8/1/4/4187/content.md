

This entry describes classes of examples of [[A-∞ category]]-valued  [[FQFT]]s.


#Contents#
* automatic table of contents goes here
{:toc}



## Overview 

Let $(X.\omega)$ be a [[compact space|compact]] [[symplectic manifold]]. 
At least in good cases to this is associated a [[Fukaya category]] 
$Fuk(X)$ of 
[[Lagrangian submanifold]]s and an enlarged version $Fuk^#(X)$.

Write $X^-$ for the symplectiv manifold $(X,-\omega)$.

Now if $(X_j, \omega_j)$ for $j = 0,1$ are two Lagrangian submanifolds and 
$L_{01} \subset  X^-_0 \times X_1$ a Lagrangian correspondence then we get
an [[A-∞ category|A-∞ functor]]  $\phi(L_{01}) : Fuk^#(X_0) \to Fuk^#(X_1)$

+-- {: .un_theorem}
###### Theorem
**(Wehrheim, Woodward)**

For  $L_{01} \subset X^{-}_0 \times X_1$ and $L_{12} \subset X^{-}_1 \times X_2$ Lagrangian submanifolds,  assuming monotonicity and Maslov conditions we have an $A_\infty$-homotopy

$$
  \Phi(L_{01}) \circ \Phi(L_{12}) \simeq \Phi(L_{01} \circ L_{12})
  \,,
$$

where on the right we have a natural notion of composition of Lagrangian submanifolds.

=--

This is the symplectic version of [[Mukai functor]]s.

**Example** For $X_0$ and $X_1$ a compact [[Riemann surface]]s and
$M(X_0), M(X_1)$

their [[moduli space]]s of fixed determinant rank $n$-bundles, and for $Y_{01}$ a [[cobordism]] (compact, oriented) from $X_0$ to $X_1$
then consider

$$
  L(Y_{01}) := Image(
      M(Y_{01}) \stackrel{restriction}{\to} M(X_0)^- \times M(X_1)
  )
$$

If $Y_{01}$ is _elementary_ in that there exists a [[Morse function]] $Y \to \mathbb{R}$ with $\leq 1$ critical points then $L(Y_{01})$ is a Lagrangian correspondence.

There should be a [[quantization]] of  $L(Y_{01})$ that should give something like quantum [[Chern-Simons theory]]


+-- {: .un_cor}
###### Corollary

The assignment

$$
  Y_{01} \mapsto \Phi(L(Y_{01}))
$$

defines a 2+1-dimensional [[FQFT]] for connected cobordisms with values in [[A-∞ categories]].

=--

This is supposed to be the 2+1-dimensional part of [[Donaldson theory]].

Other theories that fit into this framework:

1. symplectic [[Khovanov theory]] (Seidel-Smith and Rezazodegab)
  
1. [[Heegard-Floer theory]]

   $X$ a surface $\mapsto$ $Fuk^# sym X$
   
   elementary cobordisms $\mapsto$ $\Phi($vanishing cycle$)$
   
## Lagrangian correspondences

Write $X^-j = (X_j , -\omega_j)$ for a [[symplectic manifold]] with its symplectic form
reversed. 

+-- {: .un_def}
###### Definition

For $(X_j, \omega_j)$ two [[symplectic manifold]]s, a **[[Lagrangian correspondence]]** is a Lagrangian submanifold of $X^-_0 \times X_1$, that is

$$
  \iota : L_{0,1} \hookrightarrow X^-_0 \times X_1
$$

with $dim(L_{0,1}) = \frac{1}{2}(dim(x_0) + dim(X_1))$

and

$$
  \iota^*(-\pi_0^* \omega_0 + \pi_1^* \omega_1) = 0
  \,,
$$

where $\pi_i$ are the two projections out of the [[product]].



The **composition** of two Lagrangian submanifolds is

$$
  L_{01} \circ L_{12} := 
    \pi_{02}(L_{01} \times_{X_1} L_{12})
$$

which is a Lagrangian correspondence in $X^-_0 \times X_2$ if everything is suitably smoothly embedded by $\pi_{02}$.

=--

**Examples**

1. For $\phi : X_0 \to X_1$ a [[symplectomorphism]] we have

   $graph(\phi) \subset X_0^- \times X_1$ is a Lagrangian correspondence and 
   composition of syplectomorphisms corresponds to composition of 
   Lagrangian correspondences.

1. Let $X$ be a [[manifold]], $G= U(n)$ the [[unitary group]], 
   $P \to X$ a $G$-[[principal bundle]]
   and $D \to X$ a $U(1)$-bundle with [[connection on a bundle|connection]].
   
   Then there is the [[moduli space]] $M(X) = M(P,D)$ 
   of connections on $P$ with central curvature and given determinant.
   
   For example if $X$ has [[genus]] $g$ then
   
   $$
     M(X) = \{ (A,B, \cdots, A_g, B_g) \in G^{2g}\} 
   $$
   
   such that $\prod_{j=1}^g A_j B_j A_j^{-1} B_j^{-1} = diag(e^{2\pi i d/})/G$
   
   Let $Y_{01}$ be a [[cobordism]] from $X_0$ to $X_1$ with extension
   
   $$
     L(Y_{01}) = Image(M(Y_{01}) \stackrel{restr.}{\to} 
     M(X_0)^- \times M(X_1) )
   $$
   
   is a Lagrangian correspondence if $Y_{01}$ is sufficiently simple. 
   Further assuming this
   we have for composition that

   $$
      L(Y_{01} \circ Y_{12}) = L(Y_{01}) \circ L(Y_{12})
      \,.
   $$

   
## References

* [[Katrin Wehrheim]], [[Chris Woodward]]

  * _Functoriality for Lagrangian correspondences in Floer theory _ ([arXiv:0708.2851](http://arxiv.org/abs/0708.2851))

  * _Floer Cohomology and Geometric Composition of Lagrangian Correspondences_ ([arXiv:0905.1368](http://arxiv.org/abs/0905.1368))   






