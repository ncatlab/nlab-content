
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc} 

## Definition


The _octonionic Albert algebra_ is the [[Jordan algebra]] of $3$-by-$3$ [[hermitian matrices]] over the [[octonions]] $\mathbb{O}$

$$
  \label{3Times3HermitianMatrix}
  \mathfrak{h}_3(\mathbb{O})
  \;\coloneqq\;
  \left\{
  \left(
    \array{
      (x_0 + x_1) & y & \psi_1
      \\
      y^\ast & (x_0 - x_1) & \psi_2
      \\    
      \psi_1^\ast & \psi_2^\ast & \phi
    }
  \right)
  \;|\;
  \array{
    x_0, x_1, \phi \in \mathbb{R} \hookrightarrow \mathbb{O}
    \\
    \psi_1, \psi_2 \in \mathbb{O}
  }
  \right\}
$$

Similarly the _split-octonionic Albert algebra_ is the algebra of $3$-by-$3$ [[hermitian matrices]] over the [[split-octonions]]. 

The construction is due to ([Albert 1934](#Albert)), originating in an algebraic approach to [[quantum mechanics]].

## Properties

### Uniqueness

The octonionic and split-octonionic Albert algebras are (up to [[isomorphism]]) the only [[simple algebra|simple]] [[finite-dimensional space|finite-dimensional]] [[formally real algebra|formally real]] [[Jordan algebras]] over the [[real numbers]] that are not [[special Jordan algebra|special]], together comprising the _real Albert algebras_.  

Their [[complexifications]] are [[isomorphism|isomorphic]], the _complex-octonionic Albert algebra_, or simply the _complex Albert algebra_.  Analogues exist over any [[field]].

An _exceptional Jordan algebra_ (over any [[field]]) is any [[Jordan algebra]] in which an Albert algebra appears as a [[direct summand]].  Every formally real Jordan algebra over the real numbers is either special or exceptional (so they all have excellent self-esteem).  The exceptional Jordan algebras are related to the [exceptional Lie algebras](exceptional+Lie+group#lie_algebras_2).

### Relation to 10d super-Spacetime
  {#RelationTo10dSuperSpacetime}

The form of the $3 \times 3$-hermitian matrix in (eq:3Times3HermitianMatrix) makes it manifest that the exceptional Jordan algebra is naturally a [[linear map|linear]] [[direct sum]] of the form

$$
  \mathfrak{h}_3(\mathbb{O})
  \;\simeq_{\mathbb{R}}\;
  \mathfrak{h}_2(\mathbb{O})
  \oplus 
  \mathbb{O}^2
  \oplus
  \mathbb{R}
$$

via

$$
  \underset{
    \mathfrak{h}_3(\mathbb{O})
  }{
  \underbrace{
  \left\{
  \left(
    \array{
      (x_0 + x_1) & y & \psi_1
      \\
      y^\ast & (x_0 - x_1) & \psi_2
      \\    
      \psi_1^\ast & \psi_2^\ast & \phi
    }
  \right)
  \right\}
  }}
  \;\simeq\;
  \underset{
    \mathfrak{h}_2(\mathbb{O})
  }{
  \underbrace{
  \left\{
  \left(
    \array{
      (x_0 + x_1) & y & 0
      \\
      y^\ast & (x_0 - x_1) & 0 
      \\    
      0  & 0 & 0
    }
  \right)
  \right\}
  }
  }
  \oplus
  \underset{
    \mathbb{O}^2
  }{
  \underbrace{
  \left\{
  \left(
    \array{
      0 & 0 & \psi_1
      \\
      0 & 0 & \psi_2
      \\    
      \psi_1^\ast  & \psi_2^\ast & 0
    }
  \right)
  \right\}
  }
  }
  \oplus
  \underset{
    \mathbb{R}
  }{
  \underbrace{
  \left\{
  \left(
    \array{
      0 & 0 & 0
      \\
      0 & 0 & 0
      \\    
      0  & 0 & \phi
    }
  \right)
  \right\}
  }
  }
$$

with

$$
\array{
    x_0, x_1, \phi \in \mathbb{R} \hookrightarrow \mathbb{O}
    \\
    \psi_1, \psi_2 \in \mathbb{O}
}$$

By the discussion at _[[geometry of physics -- supersymmetry]]_ in the section _[Real spinors in dimension 3,4,6,10](geometry+of+physics+--+supersymmetry#InTermsOfNormedDivisionAlgebraInDimension3To10)_ these summands may be further identified as follows:

* $\mathfrak{h}_2(\mathbb{O}) \simeq \mathbb{R}^{9,1}$ is the incarnation of 10-dimensional [[super-Minkowski spacetime]] via octonionic [[Pauli matrices]];

* under this identification $\mathbb{O}^2 \simeq \mathbf{16}$ is the [[Majorana-Weyl spinor]] [[real spin representation]] of the [[spin group]] $Spin(9,1)$.

$$
  \mathfrak{h}_3(\mathbb{O})
  \;
  \simeq_{\mathbb{R}}
  \;
  \underset{
    dim_{\mathbb{R}} = 26
  }{
  \underbrace{
    \mathbb{R}^{9,1}
      \oplus
    \mathbf{16}
  }}
  \oplus
  \mathbb{R}
  \,.
$$

Under these identifications, $\phi \in \mathbb{R}$ looks like the size of $S^1/(\mathbb{Z}/2)$ in [[Horava-Witten theory]].

This decomposition hence induces an [[action]] of the [[spin group]] $Spin(9,1)$ on the exceptional Jordan algebra. While only the subgroup $Spin(9) \hookrightarrow Spin(9,1)$ of that is an [[isomorphism]] of the [[Jordan algebra]]-[[structure]] itself, the full $Spin(9,1)$-[[action]] does preserve the [[determinant]] on $\mathfrak{h}_3(\mathbb{O})$.



### Automorphisms and exceptional Lie groups
 {#Automorphisms}

+-- {: .num_prop}
###### Proposition
**([[general linear group]] of $Mat_{3\times 3}^{herm}(\mathbb{O})$ preservin [[determinant]] is [[E6]])**

The [[group]] of [[determinant]]-preserving [[linear map|linear]] [[isomorphisms]] of the vector space underlying the octonionic Albert algebra is  the [[exceptional Lie group]] [[E6]]${}_{(-26)}$. 

=--

(see e.g. ([Manogue-Dray 09](#ManogueDray09))).

+-- {: .num_prop #JordanAutomorphisms}
###### Proposition
**([[Jordan algebra]] [[automorphism group]] of $Mat_{3\times 3}^{herm}(\mathbb{O})$ is [[F4]])**

The [[group]] of [[automorphism]] with resppect to the [[Jordan algebra]] structure on the octonionic Albert algebra is the [[exceptional Lie group]] [[F4]].

=--

(e.g. [Yokota 09, section 2.2](#Yokota09))




## References

* {#Albert} [[Abraham Adrian Albert]], _On a Certain Algebra of Quantum Mechanics_, Annals of Mathematics, Second Series 35 (1): 65&#8211;73, (1934)(doi:[10.2307/1968118](http://dx.doi.org/10.2307/1968118), [JSTOR](https://www.jstor.org/stable/1968118)).

* {#Baez02} [[John Baez]], [section 3.4](http://math.ucr.edu/home/baez/octonions/node12.html) _$\mathbb{O}P^2$ and the Exceptional Jordan Algebra_ of _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

* {#Yokota09} Ichiro Yokota, _Exceptional Lie groups_ ([arXiv:0902.0431](https://arxiv.org/abs/0902.0431))

* {#ManogueDray09} [[Corinne Manogue]], [[Tevian Dray]], _Octonions, $E_6$, and Particle Physics_, J.Phys.Conf.Ser.254:012005,2010 ([arXiv:0911.2253](http://arxiv.org/abs/0911.2253))

See also

* Wikipedia, _[Albert algebra](https://en.wikipedia.org/wiki/Albert_algebra)_


[[!redirects exceptional Jordan algebra]]
[[!redirects exceptional Jordan algebras]]

[[!redirects Albert algebra]]
[[!redirects Albert algebras]]

[[!redirects real Albert algebra]]
[[!redirects real Albert algebras]]

[[!redirects octonionic Albert algebra]]
[[!redirects octonionic Albert algebras]]

[[!redirects split-octonionic Albert algebra]]
[[!redirects split-octonionic Albert algebras]]
[[!redirects split octonionic Albert algebra]]
[[!redirects split octonionic Albert algebras]]

[[!redirects complex Albert algebra]]
[[!redirects complex Albert algebras]]
[[!redirects complexified Albert algebra]]
[[!redirects complexified Albert algebras]]
[[!redirects complex-octonionic Albert algebra]]
[[!redirects complex-octonionic Albert algebras]]
[[!redirects complex octonionic Albert algebra]]
[[!redirects complex octonionic Albert algebras]]
