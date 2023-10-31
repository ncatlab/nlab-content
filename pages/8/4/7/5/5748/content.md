+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
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

### Complex structure on vector spaces
 {#ComplexStructureOnAVectorSpace}

\begin{definition}
\label{LinearComplexStructure}
Given a [[ground field]] $\mathbb{K}$,
a _complex structure_ on a $\mathbb{K}$-[[vector space]] $V$ is a $\mathbb{K}$-[[linear map|linear]] [[automorphism]] 
$$
  J 
    \,\colon\, 
  V \longrightarrow V
$$ 
that squares to minus the [[identity morphism|identity]]: 
$$
  J \circ J = - Id_V
  \,.
$$
\end{definition}

The idea here is that $J$ acts by multiplication with the would-be [[imaginary unit]] $\mathrm{i}$, and indeed: A [[real vector space]] ($\mathbb{K}$ the [[real numbers]]) equipped with a complex structure $J$ as in Def. \ref{LinearComplexStructure} becomes a [[complex vector space]] by declaring that $\mathrm{i}$ acts via $J$:
$$
  \array{
    \mathbb{C} \times V &\longrightarrow& V
    \\
    \big(
      x + \mathrm{i} \cdot y
      ,\;
      v
    \big)
    &\mapsto&  
    x \cdot v + y \cdot J(v)
  }
$$

Here a real-[[linear map]] $\phi \colon V \to V$ is complex-linear iff it commutes with the complex structure in that:
$$
  \phi \circ J \,=\, J \circ \phi
  \,.
$$



### Complex structure on manifolds

More generally, an almost complex structure on a [[smooth manifold]] is a smoothly varying [[fiber]]wise complex structure in the sense of Def. \ref{LinearComplexStructure} on its [[tangent spaces]] (which *a priori* are [[real vector spaces]]):

+-- {: .num_defn}
###### Definition

An _almost complex structure_ on a [[smooth manifold]] $X$ (of even [[dimension]]) is a rank $(1,1)$-[[tensor field]] $J$, hence a smooth [[section]] $J \in \Gamma(T X \otimes T^* X)$, such that, over each point $x \in X$, $J$ is a linear complex structure, def. \ref{LinearComplexStructure}, on that [[tangent space]] $T_x X$ under the canonical identification $End T_x X \simeq T_x X\otimes T_x^* X$. 

=--

Equivalently, stated more intrinsically:

+-- {: .num_defn}
###### Definition

An _almost complex structure_ on a [[smooth manifold]] $X$ of [[dimension]] $2 n$ is a [[reduction of the structure group]] of the [[tangent bundle]] to the [[complex numbers|complex]] [[general linear group]] along $GL(n,\mathbb{C}) \hookrightarrow GL(2n,\mathbb{R})$.

=--

+-- {: .num_remark #InTermsOfSmoothStacks}
###### Remark

In terms of modulating maps of bundles into their [[smooth infinity-groupoid|smooth]] [[moduli stacks]], this means that an almost complex structure is a lift in the following [[diagram]] in [[Smooth∞Grpd]]:

$$
  \array{
    && \mathbf{B} GL(n,\mathbb{C})
    \\
    & {}^{\mathllap{alm.compl.str.}}\nearrow & \downarrow^{\mathrlap{}}
    \\
    X
    &\underoverset{\tau}{tang.\,bund.}{\to}&
    \mathbf{B} GL(2n,\mathbb{R})
  }
  \,.
$$

By further [[reduction of the structure group|reduction]] along the [[maximal compact subgroup]] inclusion of the [[unitary group]] this yields an [[almost Hermitian structure]]

$$
  \array{
    && \mathbf{B} U(n)
    \\
    & {}^{\mathllap{herm.alm.compl.str.}}\nearrow & \downarrow^{\mathrlap{}}
    \\
    X
    &\underoverset{\tau}{tang.\,bund.}{\to}&
    \mathbf{B} GL(2n,\mathbb{R})
  }
  \,.
$$


=--

+-- {: .num_defn}
###### Definition

A _complex structure_ on a [[smooth manifold]] $X$ is the structure of a [[complex manifold]] on $X$. Every such defines  an almost complex structure and almost complex structures arising this way are called _integrable_  (see also at _[[integrability of G-structures]]_ the section _[Examples -- Complex structure](integrability+of+G-structures#ExampleComplexStructure)_).

=--


## Properties

### Characterizations of integrability

The _[[Newlander-Nirenberg theorem]]_ states that an almost complex structure $J$ on a smooth manifold is integrable (see also at _[[integrability of G-structures]]_) precisely if its [[Nijenhuis tensor]] vanishes, $N_J = 0$.

See also at _[[integrability of G-structures]]_ the section _[Examples -- Complex structure](integrability+of+G-structures#ExampleComplexStructure)_.

### On 2-dimensional manifolds


+-- {: .num_prop}
###### Proposition

Every [[Riemannian metric]] on an [[orientation|oriented]] 2-[[dimension|dimensional]] [[manifold]] induces an almost complex structure given by forming orthogonal tangent vectors.

=--

+-- {: .num_prop #In2dAnyAlmostComplexStructureIsIntegrable}
###### Proposition

Every almost complex structure on a 2-[[dimension|dimensional]] [[manifold]] is integrable, hence is a complex structure.

=--

In the special case of [[real analytic manifolds]] this fact was known to [[Carl Friedrich Gauss]]. For the general case see for instance [Audin, remark 3 on p. 47](#Audin).


### Relation to $Spin^c$-structures

Every almost complex structure canonically induces a [[spin^c-structure]] by postcomposition with the universal [[characteristic map]] $\phi$ in the [[diagram]]

$$
  \array{
    \mathbf{B}U(n) &\stackrel{\phi}{\to}& \mathbf{B}Spin^c &\to& \mathbf{B}U(1)
    \\
    &\searrow& \downarrow && \downarrow^{\mathrlap{}}
    \\
    && \mathbf{B}SO(2n) &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

See at _[[spin^c-structure]]_ for more.

### Relation to Hermitian and K&#228;hler structure

* An almost complex structure equipped with a compatible [[Riemannian metric]] is a _[[Hermitian structure]]_.

* An almost complex structure equipped with a compatible [[Riemannian structure]] and [[symplectic structure]] is a _[[Kähler structure]]_.

| [[complex structure]] | + [[Riemannian structure]] | + [[symplectic structure]] |
|--|--|--|
[[complex structure]] | [[Hermitian structure]] | [[Kähler structure]] |

### Moduli stacks of complex structures

One may consider the [[moduli stack of complex structures]] on a given manifold. For 2-dimensional manifolds these are famous as the Riemann [[moduli stacks of complex curves]]. They may also be expressed as moduli stacks of almost complex structures, see [here](moduli+space+of+curves#OverTheComplexNumbers).

## Related concepts

* [[stable complex structure]]

* [[real structure]]

* [[quaternionic structure]]

* [[holomorphic vector bundle]], [[pseudoholomorphic vector bundle]]

* [[para-complex structure]]

## References

### Complex structure on vector spaces

Textbook accounts:

* [[Shoshichi Kobayashi]], [[Katsumi Nomizu]], p. 114 in: _Foundations of differential geometry_, Volume 1 (1963), Volume 2 (1969) Interscience Publishers, reprinted by Wiley Classics Library (1996) &lbrack;[ISBN:978-0-470-55558-3](https://www.wiley.com/en-us/Foundations+of+Differential+Geometry%2C+2+Volume+Set-p-9780470555583), [Wikipedia entry](https://en.wikipedia.org/wiki/Foundations_of_Differential_Geometry)&rbrack; 

See also: 

* Wikipedia, *[Linear complex structure](https://en.wikipedia.org/wiki/Linear_complex_structure)*

Fiberwise complex structure on [[real vector bundles]]:

* Emery Thomas, *Complex Structures on Real Vector Bundles*, American Journal of Mathematics **89** 4 (1967) 887-908 &lbrack;[arXiv;10.2307/2373409](https://doi.org/10.2307/2373409), [jstor:2373409](https://www.jstor.org/stable/2373409)&rbrack;


### Complex structure on manifolds

Lecture notes include

* {#Audin} Mich&#232;le Audin, _Symplectic and almost complex manifolds_ ([pdf](http://www-irma.u-strasbg.fr/~maudin/HolomorphicChapII.pdf))

Discussion from the point of view of [[integrable G-structures]] includes

* [[Robert Bryant]], _Remarks on the geometry of almost complex 6-manifolds_, The Asian Journal of Mathematics, vol. 10 no. 3 (September, 2006), pp. 561--606. ([arXiv:math/0508428](http://arxiv.org/abs/math/0508428))

A discussion of deformations of complex structures is in

* [[Domenico Fiorenza]], _[[domenicofiorenza:The periods map of a complex projective manifold. An oo-category perspective]]_

The _[[moduli space of complex structures]]_ on a manifold is discussed for instance from page 175 on of 

* [[Yongbin Ruan]], _Symplectic topology and complex surfaces_ in _Geometry and analysis on complex manifolds_ (1994)

and in

* Yurii M. Burman, _Relative moduli spaces of complex structures: an example_ ([arXiv:math/9903029](http://arxiv.org/abs/math/9903029))



[[!redirects complex structures]]

[[!redirects almost complex structure]]
[[!redirects almost complex structures]]


[[!redirects almost complex manifold]]
[[!redirects almost complex manifolds]]

[[!redirects linear complex structure]]
[[!redirects linear complex structures]]
