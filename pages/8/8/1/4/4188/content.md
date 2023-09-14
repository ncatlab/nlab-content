
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
=--
=--

#Contents#
* table of contents 
{:toc}

## Idea

A _Lagrangian correspondence_ is a [[correspondence]] between two [[symplectic manifolds]] $(X_i,\omega_i)$ given by a [[Lagrangian submanifold]] of their [[product]] $(X_1 \times X_2, p_1^\ast \omega_1 - p_2^\ast \omega_2)$. The [[graph of a function|graph]] of any [[symplectomorphism]] induces a Lagrangian correspondence. 

Lagrangian correspondences are supposed to form, subject to some technicalities, the [[morphisms]] of a [[category]] to be called the _[[symplectic category]]_.

When [[symplectic geometry]] is used to model [[mechanics]] in [[physics]], then a [[symplectic manifold]] $(X,\omega)$ encodes the [[phase space]] of a [[mechanical system]] and a [[symplectomorphism]] 

$$
  \phi \;\colon\; (X_1,\omega_1) \to (X_2, \omega_2)
$$ 

encodes a process undergone by this system, for instance the time evolution induced by a [[Hamiltonian vector field]]. In particular if this is a [[Hamiltonian symplectomorphism]] then this is traditionally called a _[[canonical transformation]]_ in physics. Therefore Lagrangian correspondence have also been called _canonical relations_ ([Weinstein 83, p. 5](#Weinstein83)).



## Definition
 {#Definition}

+-- {: .num_defn}
###### Definition

For $(X_j, \omega_j)$ two [[symplectic manifold]]s, a **Lagrangian correspondence** is a [[correspondence]] $Z \to X^-_0 \times X_1$ which is a  [[submanifold]] of $X^-_0 \times X_1$

$$
  \iota : L_{0,1} \hookrightarrow X^-_0 \times X_1
$$

with $dim(L_{0,1}) = \frac{1}{2}(dim(X_0) + dim(X_1))$

and

$$
  \iota^*(-\pi_0^* \omega_0 + \pi_1^* \omega_1) = 0
  \,,
$$

where $\pi_i$ are the two projections out of the [[product]].

=--

+-- {: .num_defn}
###### Definition

The **composition** of two Lagrangian correspondences is

$$
  L_{01} \circ L_{12} := 
    \pi_{02}(L_{01} \times_{X_1} L_{12})
$$

which is itself a Lagrangian correspondence in $X^-_0 \times X_2$ if everything is suitably smoothly embedded by $\pi_{02}$.

=--

+-- {: .num_remark}
###### Remark

The category of Lagrangian correspondences is a [[full subcategory]] of that of correspondence of the [[slice topos]] $SmoothSpaces_{/\Omega^2_{cl}}$ of [[smooth spaces]] over the [[moduli space]] $\Omega^2_{cl}$ of closed [[differential 2-forms]]: 

a [[symplectic manifold]] $(X,\omega)$ is given by a map of [[smooth spaces]] $\omega \colon X \to \Omega^2_{cl}$ (generally this is a [[presymplectic manifold]]) and a correspondence in $SmoothSpaces_{/\Omega^2_{cl}}$ is a [[commuting diagram]] in [[smooth spaces|SmoothSpaces]] of the form

$$
  \array{
    && Z
    \\
    & {}^{\mathllap{i_1}}\swarrow && \searrow^{\mathrlap{i_2}}
    \\
    X_1 && {i_1^\ast \omega_1 = i_2^\ast \omega_2} && X_2
    \\
    & {}_{\mathllap{\omega_1}}\searrow && \swarrow_{\mathrlap{\omega_2}}
    \\
    && \Omega^2_{cl}
  }
  \,.
$$

If here $(i_1, i_2) \colon Z \to X \times Y$ is a manifold maximal with the property of fitting into the above diagram, then this is a Lagrangian correspondence.

From this is naturally induced the notion of a _[[prequantized Lagrangian correspondence]]_. See there for more details.

=--





## Examples

+-- {: .num_example}
###### Example

For $\phi : (X_0, \omega_0) \to (X_1, \omega_1)$ a [[symplectomorphism]] we have that its [[graph of a function|graph]] $graph(\phi) \subset X_0^- \times X_1$ is a Lagrangian correspondence and  composition of syplectomorphisms corresponds to composition of  Lagrangian correspondences.

=--

+-- {: .num_example}
###### Example

For a [[Hamiltonian action]] on a [[symplectic manifold]] $(X,\omega)$ of a [[Lie group]] $G$ given by a [[moment map]] $\mu$, the [[zero locus]] $\mu^{-1}(0)$ consitutes a Lagrangian correspondence between $(X,\omega)$ and its [[symplectic reduction]] $\mu^{-1}(0)/G$.

=--

+-- {: .num_example}
###### Example

Let $X$ be a [[manifold]], $G= U(n)$ the [[unitary group]], $P \to X$ a $G$-[[principal bundle]] and $D \to X$ a $U(1)$-bundle with [[connection on a bundle|connection]].
   
Then there is the [[moduli space]] $M(X) = M(P,D)$  of connections on $P$ with central curvature and given determinant.
   
For example if $X$ has [[genus]] $g$ then
   
$$
  M(X) = \{ (A,B, \cdots, A_g, B_g) \in G^{2g}\} 
$$
   
such that $\prod_{j=1}^g A_j B_j A_j^{-1} B_j^{-1} = diag(e^{2\pi i d/})/G$
   
Let $Y_{01}$ be a [[cobordism]] from $X_0$ to $X_1$ with extension
   
$$
  L(Y_{01}) = Image(M(Y_{01}) \stackrel{restr.}{\to} M(X_0)^- \times M(X_1) )
$$
   
is a Lagrangian correspondence if $Y_{01}$ is sufficiently simple. Further assuming this we have for composition that

$$
   L(Y_{01} \circ Y_{12}) = L(Y_{01}) \circ L(Y_{12})
   \,.
$$

=--

+-- {: .num_example}
###### Example

Given symplectic manifolds $(X_1, \omega_1)$ and $(X_2, \omega_2)$ and a [[symplectomorphism]] $(X_1 \times X_2 , p_1^\ast \omega_1 - p_2^\ast \omega_2) \stackrel{\simeq}{\longrightarrow} (X,\omega)$, then certain Lagrangian correspondences between $(X_1, \omega_1)$ and $(X_2, \omega_2)$ are identified with functions on $X$. This is identified with the calculus of generating functions for [[canonical transformations]] as used in [[classical mechanics]]. ([Weinstein 83, p. 5](#Weinstein83))

=--

## Related entries

* [[symplectic dual pair]]

* [[Weinstein symplectic category]]

* [[prequantized Lagrangian correspondence]]

* [[Lagrangian correspondences and category-valued TFT]]

* [[cosmic Galois group]]

## References

The notion originates somewhere around

* [[Lars Hörmander]], _Fourier Integral Operators I._, Acta Math. __127__ (1971)
 {#Hoermander71}

* [[Alan Weinstein]], _Symplectic manifolds and their lagrangian submanifolds_, Advances in Math. 6 (1971) <a href="http://dx.doi.org/10.1016/0001-8708(71)90020-X>doi</a> {#Weinstein71}

The use of Lagrangian correspondences for encoding [[symplectomorphisms]] was further highlighted in 

* [[Alan Weinstein]], _The symplectic "category"_, In Differential geometric methods in mathematical physics (Clausthal, 1980), volume 905 of Lecture Notes in Math., pages 45&#8211;51. Springer, Berlin, 1982.

and on p. 5 and then section 3

* [[Alan Weinstein]], _Lectures on Symplectic Manifolds_, volume 29 of CBMS Regional Conf. Series in Math. Amer. Math. Soc., 1983. third 
printing.
  {#Weinstein83}


Further developments include for instance

* [[Katrin Wehrheim]], [[Chris Woodward]], _Floer Cohomology and Geometric Composition of Lagrangian Correspondences_ ([arXiv:0905.1368](http://arxiv.org/abs/0905.1368))


A review of the way Lagrangian correspondences encode symplectomorphisms induced by Hamiltonian time evolution in the context of [[field theory]] and generalization to the broader context of [[BV-BRST formalism]] is in

* [[Alberto Cattaneo]], [[Pavel Mnev]], [[Nicolai Reshetikhin]], _Classical and quantum Lagrangian field theories with boundary_ ([arXiv:1207.0239](http://arxiv.org/abs/1207.0239))
 {#CattaneoMnevReshetikhin12}

 
[[!redirects Lagrangian correspondences]]
[[!redirects lagrangian correspondence]]
[[!redirects canonical relation]]
[[!redirects canonical relations]]
