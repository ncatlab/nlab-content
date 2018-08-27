
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

The [[group]] of [[automorphism]] with respect to the [[Jordan algebra]] structure $\circ$ on the octonionic Albert algebra is the [[exceptional Lie group]] [[F4]]:

$$
  Aut\left(
    Mat_{3\times 3}^{herm}(\mathbb{O}), \circ
  \right)
  \;\simeq\;
  F_4
  \,.
$$

=--

(e.g. [Yokota 09, section 2.2](#Yokota09))


+-- {: .num_prop #JordanAlgebraAutomorphismsFixingAnImaginaryOctonion}
###### Proposition
**([[Jordan algebra]] [[automorphism group]] of $Mat_{3 \times 3}^{herm}(\mathbb{O})$ fixing an [[imaginary number|imaginary]] [[octonion]])**

Fix an [[imaginary number|imaginary]] [[octonion]] $i \in \mathbb{O}$, hence a $\mathbb{R}$-[[linear map|linear]] [[direct sum]] decomposition

$$
  \mathbb{O}
  \;\simeq_{\mathbb{R}}\;
  \mathbb{C} \oplus V
  \phantom{AA}\text{with}\phantom{AA}
  V \simeq_{\mathbb{R}} \mathbb{C}^3 
  \,,
$$

and let 

\[
  \label{ComponentwiseiFixingAutomorphism}
  \array{    
    Mat_{3 \times 3}^{herm}(\mathbb{O}) 
     &\overset{w}{\longrightarrow}&
    Mat_{3 \times 3}^{herm}(\mathbb{O}) 
  }
\]

be given componentwise by the identity on $\mathbb{C}^2$ and by multiplication with some fixed non-vanishing number on $V$.

Then the [[subgroup]] of the [[Jordan algebra]] [[automorphism]] group $Aut\left(Mat_{3\times 3}^{herm}(\mathbb{O}), \circ \right) \;\simeq\; F_4$ (Prop. \ref{JordanAutomorphisms}) of elements that commute with $w$ (eq:ComponentwiseiFixingAutomorphism)

$$
  F_4^w 
  \;\coloneqq\;
  \left\{
    \alpha \in F_4 \;\vert\;  w \alpha = \alpha w
  \right\}
$$

is 

$$
  F_4^w
  \;\simeq\;
  \big( 
    SU(3) \times SU(3)
  \big)/ \mathbb{Z}_3
  \,,
$$

where every element in the [[product group]] of the [[special unitary group]] with itself

$$
  (A, B) \in SU(3) \times SU(3)
$$

[[action|acts]] on an element

$$
  \underset{
    \in Mat_{3\times 3}^{herm}(\mathbb{O})
  }{\underbrace{\;X\;}}
  \;\simeq\;
  \underset{
    \in Mat_{3\times 3}^{herm}(\mathbb{C})
  }{\underbrace{\;X_{\mathbb{C}}\;}}
  \;+\;
  \underset{
    \in Mat_{3 \times 3}(\mathbb{C})
  }{\underbrace{X_{V}}}
$$

via [[matrix multiplication]] as 

\[
  \label{MatrixMultiplicationRepresentationOfiFixingJordanAutomorphism}
  X_{\mathbb{C}}
  +
  X_{\mathbb{V}}
  \;\mapsto\;
  A  X_{\mathbb{C}} A^\dagger
  \;+\;
  B X_{V} A^\dagger
\]

(with $(-)^\dagger$ being the [[conjugate transpose matrix]], hence the [[inverse matrix]] for the [[unitary matrices]] under consideration) and where the [[quotient group|quotient]] is by the [[cyclic group|cyclic]] [[subgroup]]

$$
  \mathbb{Z}_3
  \;\subset\;
  SU(3) \times SU(3)
$$

which is [[generators and relations|generated]] by the [[pair]] of [[diagonal matrices]]

\[
  \label{Z3Generator}
  \left(
    e^{2\pi i \tfrac{1}{3}}   \mathbf{1}_3
    \;,\;
    e^{2\pi i \tfrac{1}{3}}  \mathbf{1}_3
  \right)
  \;\in \;
  SU(3) \times SU(3)
  \,.
\]

=--

([Yokota 09, theorem 2.12.2](#Yokota09))


+-- {: .num_prop #StabilizerOf4dMinkowskiInsideOctonionicAlbertAlgebra}
###### Proposition

The further [[subgroup]] of
$
  F_4^w 
  \simeq
  \big(
    SU(3) \times SU(3)
  \big) / \mathbb{Z}_3
  \;\subset\;
  F_4    
$
(Prop. \ref{JordanAlgebraAutomorphismsFixingAnImaginaryOctonion}) which fixes a subspace

$$
  Mat_{2 \times 2}^{herm}(\mathbb{C})
  \;\subset\;
  \underset{
    Mat_{3 \times 3}^{herm}( \mathbb{O} )
  }{
  \underbrace{
    Mat_{3 \times 3}^{herm}(\mathbb{C}) 
    \;\oplus\;
    Mat_{3 \times 3}(V)
  }}
$$

is

$$
  \big(
    U(1)
    \times
    SU(2)
    \times
    SU(3)
  \big) /  \mathbb{Z}_6
  \,,
$$

where the [[quotient group|quotient]] is by the [[cyclic group|cyclic]] [[subgroup]] which is [[generators and relations|generated]] by the element

\[
  \left(
    \exp\left(2 \pi i \tfrac{1}{6}\right)\;,\;
    \exp\left(2 \pi i \tfrac{1}{2}\right) \mathbf{1}_2\;,\;
    \exp\left(2 \pi i \tfrac{1}{3}\right) \mathbf{1}_3   
  \right)
  \;\in\;
  U(1) \times SU(2) \times SU(3)
  \,.
\]

(Hence this group happens to coincide with the _exact_ [[gauge group]] of the [[standard model of particle physics]], see [there](standard+model+of+particle+physics#GaugeGroup)).

=--

This was claimed without proof in [Dubois-Violette & Todorov 18](#DuboisVioletteTodorov18).

+-- {: .proof}
###### Proof

By (eq:MatrixMultiplicationRepresentationOfiFixingJordanAutomorphism) it is clear that the subgroup in question is that represented by those [[pairs]] $(A,B) \in SU(3) \times SU(3)$ for which $A$ is $(1 + 2)$-block diagonal. Such matrices $A$ form the [[subgroup]] of $SU(3)$ of [[matrices]] that may be written in the form

$$
  diag\left(
    c^2, c^{-1} \mathbf{\sigma}
  \right)
$$

for $c \in U(1)$ and $\mathbf{\sigma} \in SU(2)$. The [[kernel]] of the [[group homomorphism]]

\[
  \label{IdentifyingU1SU2inSU3}
  \array{
    U(1) \times SU(2) &\longrightarrow& SU(3)
    \\
    (c,\mathbf{\sigma}) &\mapsto& diag\left(
    c^{2}, c^{-1} \mathbf{\sigma}
  \right)
  }
\]

is clearly the [[cyclic group]]

\[
  \label{Z2Generator}
  \left\{
    (1,\mathbf{1}_2)\;,\; 
    \left(
      e^{2\pi i \tfrac{1}{2}},e^{2\pi i \tfrac{1}{2}}\mathbf{1}_2
    \right) 
  \right\}
  \;\simeq\;
  \mathbb{Z}_2
  \,.
\]

Hence the subgroup in question is

$$
  \begin{aligned}
    \Big(
      \big( U(1) \times SU(2) \big)/ \mathbb{Z}_2
      \;\times\;
      SU(3)
    \Big)/ \mathbb{Z}_3
    & \simeq
    \Big(
    \Big(
      \big( U(1) \times SU(2) \big)
      \;\times\;
      SU(3)
    \Big) / \mathbb{Z}_2 
    \Big) / \mathbb{Z}_3
    \\
    &\simeq
    \Big(
      \big( U(1) \times SU(2) \big)
      \;\times\;
      SU(3)
    \Big) / \mathbb{Z}_6
    \,,
  \end{aligned}
$$

where in the first step we extended the $\mathbb{Z}_2$-[[action]] as the [[trivial action]] on the $SU(3)$-factor, and in the second step we used the evident [[isomorphism]] $\mathbb{Z}_2 \times \mathbb{Z}_3 \simeq \mathbb{Z}_6$ (an application of the "[[fundamental theorem of cyclic groups]]", if you wish).

It remains to see that the [[action]] of $\mathbb{Z}_6$ is as claimed. By the above identification $\mathbb{Z}_6 \simeq \mathbb{Z}_2 \times \mathbb{Z}_3$, it is generated by the _joint_ action of that of the generators of $\mathbb{Z}_3$ and of $\mathbb{Z}_2$, which, by (eq:Z3Generator) and (eq:Z2Generator), is

$$
  \underset{
    \text{generator of}\, \mathbb{Z}_3
  }{
  \underbrace{
  \Big(
    e^{2\pi i \tfrac{1}{3}}  \;,\;
    e^{2\pi i \tfrac{1}{3}}  \mathbf{1}_2\;,\;
    e^{2\pi i \tfrac{1}{3}}  \mathbf{1}_3
  \Big)
  }
  }
  \underset{
    \text{generator of} \, \mathbb{Z}_2
  }{
  \underbrace{
    \Big(
      1 , (e^{2 \pi i \tfrac{1}{2}}) (e^{2 \pi i \tfrac{1}{2}}\mathbf{1}_2), \mathbf{1}_3
    \Big)
  }
  }
  \;=\;
  \left(
    e^{2\pi i \tfrac{1}{3}} \;,\;
    \underset{ 
      = e^{2\pi i \tfrac{-1}{6}} 
    }{
    \underbrace{
      e^{2\pi i \tfrac{1}{2}} e^{2\pi i \tfrac{1}{3}}
    }} 
   \;
   ( e^{2 \pi i \tfrac{1}{2}} \mathbf{1}_2)
   \;,\;
    e^{2\pi i \tfrac{1}{3}} \mathbf{1}_3
  \right)
$$

as an element in $SU(3) \times SU(3)$, hence is 

$$
  \Big(
    e^{2\pi i \tfrac{1}{6}} \;,\;
    e^{2\pi i \tfrac{1}{2}}\mathbf{1}_2 \;,\;
    e^{2\pi i \tfrac{1}{3}}\mathbf{1}_3 \;,\;    
  \Big)
  \;\in\;
  U(1) \times SU(2) \times SU(3)
$$

under the lift through (eq:IdentifyingU1SU2inSU3).

=--




## References

* {#Albert} [[Abraham Adrian Albert]], _On a Certain Algebra of Quantum Mechanics_, Annals of Mathematics, Second Series 35 (1): 65&#8211;73, (1934)(doi:[10.2307/1968118](http://dx.doi.org/10.2307/1968118), [JSTOR](https://www.jstor.org/stable/1968118)).

* {#Baez02} [[John Baez]], [section 3.4](http://math.ucr.edu/home/baez/octonions/node12.html) _$\mathbb{O}P^2$ and the Exceptional Jordan Algebra_ of _The Octonions_,  Bull. Amer. Math. Soc. 39 (2002), 145-205. ([web](http://math.ucr.edu/home/baez/octonions/octonions.html)) 

* {#Yokota09} Ichiro Yokota, _Exceptional Lie groups_ ([arXiv:0902.0431](https://arxiv.org/abs/0902.0431))

* {#ManogueDray09} [[Corinne Manogue]], [[Tevian Dray]], _Octonions, $E_6$, and Particle Physics_, J.Phys.Conf.Ser.254:012005,2010 ([arXiv:0911.2253](http://arxiv.org/abs/0911.2253))

* {#DuboisVioletteTodorov18} Michel Dubois-Violette, Ivan Todorov, _Exceptional quantum geometry and particle physics II_ ([arXiv:1808.08110](https://arxiv.org/abs/1808.08110))

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
