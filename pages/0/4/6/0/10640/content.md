
#Contents#
* table of contents
{:toc}

## Definition

Let $G$ be a [[compact Lie group]] and write $L G$ for its [[loop group]]. See there for details and notation.

We discuss the [[quantization]] of loop groups in the sense of [[geometric quantization]] of their canonical [[prequantum bundle]].

Let $G$ be a [[compact Lie group]].
Let $T \hookrightarrow G$ be the inclusion of a [[maximal torus]]. There is a [[fiber sequence]]

$$
  \array{
    G/T &\to& L G / T
    \\
    && \downarrow
    \\
    && L G / G & \simeq \Omega G
  }
  \,.
$$

+-- {: .num_remark }
###### Remark

By the discussion at _[[orbit method]]_, if $G$ is a [[semisimple Lie group]], then $G/T$ is isomorphic to the [[coadjoint orbit]] of an element $\langle \lambda , -\rangle \in \mathfrak{g}^*$ for which $T \simeq G_\lambda$ is the [[stabilizer subgroup]].

If moreover $G$ is [[simply connected topological space|simply connected]], then the [[weight lattice]] $\Gamma_{wt} \subset \mathfrak{t}^* \simeq \mathfrak{t}$ of the Lie group $G$ is [[isomorphism|isomorphic]] to the group of [[group characters]]

$$
  \Gamma_{wt} \stackrel{\simeq}{\to} Hom_{LieGrp}(G,U(1))
  \,.
$$


=--

+-- {: .num_prop }
###### Proposition

The [[irreducible representation|irreducible]] [[projective representation|projective]] [[positive energy representations]] of $L G$ correspond precisley to the possible [[geometric quantizations]] of $L G / T$ (as in the [[orbit method]]). 

More in detail:

The degree-2 [[integral cohomology]] of $L G / T$ is

$$
  H^2(L G / T) \simeq \mathbb{Z} \oplus H^2(G / T, \mathbb{Z}) \simeq \mathbb{Z} \oplus \hat T
  \,.
$$

Writing $L_{n,\lambda}$ for the corresponding [[complex line bundle]] with level $n \in \mathbb{Z}$ and weight $\lambda \in \hat T$ we have that 

1. the space of [[holomorphic sections]] of $L_{n,\lambda}$ is either zero or is an irreducible positive energy representation;

1. every such arises this way;

1. and is non-zero precisely if $(n,\lambda)$ is positive  in the sense that for each positive [[coroot]] $h_\alpha$ of $G$

   $$
     0 \leq \lambda(h_\alpha) \leq n \langle h_\alpha, h_\alpha\rangle
    \,.
   $$

=--

This appears for instance as ([Segal, prop. 4.2](#Segal)).


## References

The standard textbook on loop groups is

* Andrew Pressley, [[Graeme Segal]], _Loop groups_ Oxford University Press (1988)
  {#PressleySegal}

A review talk is 

* [[Graeme Segal]], _Loop groups_ ([pdf](http://people.mpim-bonn.mpg.de/zagier/files/doi/10.1007/BFb0084581/chapter08.pdf))
 {#Segal}

