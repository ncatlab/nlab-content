
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Basic definition

We state the definition below in Def. \ref{HRManifold}. First we need the following preliminaries:

Denote by $\mathbf{D}$ the duplex (sometimes called _paracomplex_ or _hyperbolic_) numbers, which is the [[associative algebra]] over the [[real numbers]] $\mathbf{R}$ generated by the elements $1, \mathbf{k}$ s.t. $\mathbf{k}^2 = 1 $, in other words the real [[Clifford algebra]] $C\ell _{1, 0} (\mathbf{R})$. A [[PDE]] theory analogous to complex holomorphy may be developed based on this algebra; for a function $\psi = (\psi_1 , \psi_2) : \mathbf{D} \rightarrow \mathbf{D}$ (under an identification of $\mathbf{D}$ with $\mathbf{R}^2$), paracomplex linearity of $d \psi$ means the real components of $\psi$ must satisfy the equations $\partial_1 \psi_2 = \partial_2 \psi_1$ and $\partial_1 \psi_1 = \partial_2 \psi_2$. These are the hyperbolic analogue of the [[Cauchy-Riemann equations]], although clearly not defining an [[elliptic differntial equation|elliptic system]] since the components of $\psi$ therefore satisfy the [[wave equations]] $\Box \psi_i =0$. In the context of [[differential geometry]] over $\mathbf{D}$, such functions are sometimes called _paraholomorphic_.

As with [[CR geometry]], one can study real hypersurfaces of manifolds carrying such hyperbolic structure (discussed [below](#hypmanifold)):


+-- {: .num_defn #HRManifold}
###### Definition
**(HR manifold)**

An _HR manifold_ (for "hyperbolic-real") is a [[differentiable manifold]] $M$ together with a [[sub-bundle]] $H$ of the hyperbolified [[tangent bundle]], $H \subset TM \otimes_\mathbf{R} \mathbf{D}$ such that $[H, H ] \subset H$ and $H \cap H^{\dagger} =\{ 0 \} $, where $\dagger$ is the bundle [[involution]] s.t. $\mathbf{k} \mapsto - \mathbf{k}$.

=--

### As $G$-structure 
  {#hypmanifold}

[[G-structures]] of this type only exist on even-dimensional differentiable manifolds, and have been known since the classical contributions of Libermann. Explicitly, an _almost-hyperbolic_ structure on a real $2n$-manifold $M$ is determined by a [[reduction of the structure group]] $\text{GL}(n, \mathbf{D}) \hookrightarrow \text{GL}(2n, \mathbf{R})$, defining a bundle [[automorphism]] $K \in \text{End}(TM)$ s.t. $K^2 = \text{id}_{TM}$. Locally this means that $K$, when integrable, is of the form: 
$$
\left( \begin{matrix}
0 & I_n \\
I_n & 0 
\end{matrix} \right)
$$
on fibers, so that the [[transition functions]] of $M$ satisfy the [[wave equations]] just discussed. One can also give various integrability conditions of $K$, although as a Dirac structure the simplest to state is the vanishing of the [[Nijenhuis tensor]] $N_K (X, Y) = [KX, KY] + [X, Y] - K ([KX, Y] + [X, KY]) $, a sign away from its complex analogue.


## Examples 

(...)

## Other Properties

(...)


## Other Clifford-type Hypersurfaces

* [[BR manifold]]

* [[CR manifold]]


## References 

The classical articles are:

* P. Libermann, _Sur le probleme d’equivalence de certaines structures infinitesimales_, Ann. Mat. Pura Appl., 36 (1954), 27-120.

* P. Libermann, _Sur les structures presque paracomplexes_, C.R. Acad. Sci. Paris, 234 (1952), 2517-2519.

A convenient modern survey appears in::

* V. Cruceanu, P. Fortuny and P. M. Gadea, _A Survey on Paracomplex Geometry_ , Rocky Mountain J. Math. Volume 26, Number 1 (1996), 83-115.

And a more recent article done in the style of [[generalized complex geometry]] is:

* Aïssa Wade, _Dirac structures and paracomplex manifolds_, C. R. Acad. Sci. Paris, Ser. I 338 (2004) 889–894.


[[!redirects HR manifolds]]

[[!redirects HR-manifold]]
[[!redirects HR-manifolds]]

[[!redirects HR geometry]]
[[!redirects HR geometries]]