
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Lie algebra cohomology_ is the intrinsic notion of [[cohomology]] of [[Lie algebra]]s.

There is a precise sense in which Lie algebras $\mathfrak{g}$ are [[infinitesimal object|infinitesimal]] [[Lie group]]s. Lie algebra cohomology is the restriction of the definition of [[Lie group cohomology]] to Lie algebras.

In [[∞-Lie theory]] one studies the relation between the two via [[Lie integration]].

Lie algebra cohomology generalizes to [[nonabelian Lie algebra cohomology]] and to [[∞-Lie algebra cohomology]].

## Definition

There are several different but equivalent definitions of the [[cohomology]] of a [[Lie algebra]].

### As Ext-group or derived functor

The abelian [[cohomology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H^*_{Lie}(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(k,M)$ where $k$ is the ground field understood as a trivial module over the universal enveloping algebra $U\mathfrak{g}$. In particular it is a derived functor. 

### Via resolutions

Before this approach was advanced in Cartan-Eilenberg's _Homological algebra_, Lie algebra cohomology and homology were defined by Chevalley-Eilenberg with a help of concrete Koszul-type resolution which is in this case a cochain complex 

$$Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M),$$ 

where the first argument $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is naturally equipped with a differential to start with (see below).

WHERE  BELOW?

 The first argument in the Hom, i.e. $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is sometimes called the Chevalley-Eilenberg chain complex (cf. Weibel); the [[Chevalley-Eilenberg cochain complex]] is the whole thing, i.e. 

$$CE(\mathfrak{g},M) := Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M).$$

If $M$ is a trivial module $k$ then $CE(\mathfrak{g}) := Hom_k(\Lambda^* \mathfrak{g},k)$ and if $\mathfrak{g}$ is finite-dimensional this equals $\Lambda^* \mathfrak{g}^*$ with an appropriate differential and the exterior multiplication gives it a dg-algebra structure.

### Via $\infty$-Lie algebras

As discussed at [[Chevalley-Eilenberg algebra]], we may identify [[Lie algebra]]s $\mathfrak{g}$ as the duals $CE(\mathfrak{g})$ of [[dg-algebra]]s whose underlying graded algebra is the [[Grassmann algebra]] on the vector space $\mathfrak{g}^*$.

Similarly, a dg-algebra $CE(\mathfrak{h})$ whose underlying algebra is free on a [[graded vector space]] $\mathfrak{h}$ we may understand as exibiting an [[∞-Lie algebra]]-structure on $\mathfrak{h}$.

Then a morphism $\mathfrak{g} \to \mathfrak{h}$ of these $\infty$-Lie algebras is by definition just a morphism $CE(\mathfrak{g}) \leftarrow CE(\mathfrak{h})$ of dg-algebras. Such a morphis may be thought of as a cocycle in [[nonabelian Lie algebra cohomology]] $H(\mathfrak{g}, \mathfrak{h})$.

Specifically, write $b^{n-1} \mathbb{R}$ for the [[line Lie n-algebra]], the  $\infty$-Lie algebra given by the fact that $CE(b^{n-1}\mathbb{R})$ has a single generator in degree $n$ and vanishing differential. Then a morphism 


$$
  \mu : \mathfrak{g} \to b^{n-1} \mathbb{R}
$$

is a cocycle in the abelian Lie algebra cohomology $H^n(\mathfrak{g}, \mathbb{R})$. Notice that dually, by definition, this is a morphism of dg-algebras

$$
  CE(\mathfrak{g}) \leftarrow CE(b^{n-1} \mathbb{R}) : \mu
  \,.
$$

Since on the right we only have a single closed degree-$n$ generator, such a morphism is precily a closed degree $n$-element 

$$
  \mu \in CE(\mathfrak{g})
  \,.
$$

This way we recover the above definition of Lie algebra cohomology (with coefficient in the trivial module) in terms of the cochain complex cohomology of the CE-algebra.

## Properties

### Whitehead's lemma

The following lemma asserts that for semisimple Lie algebras $\mathfrak{g}$ only the cohomology $\mathfrak{g} \to b^{n-1} \mathbb{R}$ with coefficients in the trivial module is nontrivial.

+-- {: .num_prop}
###### Proposition
**(Whitehead's lemma)**

For $\mathfrak{g}$ a finite dimensional [[semisimple Lie algebra]] over a [[field]] of [[characteristic]] 0, and for $V$ a non-trivial finite-dimensional [[irreducible representation]], we have

$$
  H^p(\mathfrak{g}, V) = 0 \;\;\; for\;p \gt 0
  \,.
$$

=--

### Van Est isomorphism

The content of a [[van Est isomorphism]] is that the canonical comparison map from [[Lie group cohomology]] to Lie algebra cohomology (by [[differentiation]]) is an [[isomorphism]] whenever the Lie group is sufficiently connected.

### Hochschild-Serre spectral sequence
  {#HochschildSerreSpectralSequence}

+-- {: .num_defn #RelativeLieAlgebraCohomologyWithCoefficients}
###### Definition
**(relative Lie algebra cohomology with coefficents)**

Let 

1. $(\mathfrak{g}, [-,-])$ be a [[Lie algebra]] of [[finite number|finite]] [[dimension]];

1. $(V, \rho)$ a $\mathfrak{g}$-[[Lie algebra module]] of [[finite number|finite]] [[dimension]];

1. $\mathfrak{h} \hookrightarrow \mathfrak{g}$ a sub-Lie algebra.

Consider the $\mathbb{N}$-[[graded vector space]]

$$
  C^\bullet(\mathfrak{g}, \mathfrak{h}, V)
  \;\coloneqq\;
    \left(
      (
        \wedge^\bullet
        (\mathfrak{g}/\mathfrak{h})^\ast
      )
      \otimes V
    \right)^{\mathfrak{h}}
$$

consisting of the $\mathfrak{h}$-[[invariant|invariant elements]] in the [[tensor product]] of $V$ with the [[exterior algebra]] of the [[coset]] $\mathfrak{g}/\mathfrak{h}$.

On this graded vector space, the [[dual linear maps]] of the [[Lie bracket]] $[-,-]$, extended as a graded [[derivation]] to the exterior algebra, and the [[Lie algebra action]] $\rho$ define a [[differential]]

$$
  d_{CE} \coloneqq \rho^\ast  + [-,-]^\ast
  \,.
$$

The resulting [[cochain complex]] is the  _[[Chevalley-Eilenberg complex]] of $\mathfrak{g}$ relative $\mathfrak{h}$ with [[coefficients]] in $V$_.


Its [[cochain cohomology]]

$$
  H^\bullet(\mathfrak{g}, \mathfrak{h}; V)
  \;\coloneqq\;
  \left(
    \left(
      (
        \wedge^\bullet
        (\mathfrak{g}/\mathfrak{h})^\ast
      )
      \otimes V
    \right)^{\mathfrak{h}}
    ,
    d_{CE}
  \right)
$$

is the _Lie algebra cohomology of $\mathfrak{g}$ relative $\mathfrak{h}$ with [[coefficients]] in $V$_.

=--

(e.g. [Solleveld 02, def. 2.13 and def. 2.17](#Solleveld02))


If in def. \ref{RelativeLieAlgebraCohomologyWithCoefficients} $\mathfrak{h} = 0$ then the definition reduces to that of ordinary Lie algebra cohomology with coefficients:

$$
  H^\bullet(\mathfrak{g}, 0; V)
  =
  H^\bullet(\mathfrak{g}; V)
  \,.
$$


+-- {: .num_defn #LieAlgebraReductiveInAmbientLieAlgebra}
###### Definition
**([[reductive Lie algebra|Lie algebra reductive]] in ambient Lie algebra)**

A sub-[[Lie algebra]] 

$$
  \mathfrak{h} \hookrightarrow \mathfrak{g}
$$

is called _reductive_ if the [[adjoint representation|adjoint]] [[Lie algebra representation]] of $\mathfrak{h}$ on $\mathfrak{g}$ is [[reducible representation|reducible]].

=--

([Koszul 50](#Koszul50), recalled in e.g. [Solleveld 02, def. 2.27](#Solleveld02))

+-- {: .num_prop #InvariantsInLieAlgebraCohomologyComputedByRelativeLieAlgebraCohomology}
###### Proposition
**(invariants in Lie algebra cohomology computed by relative Lie algebra cohomology)**

Let 

1. $(\mathfrak{g}, [-,-])$ be a [[Lie algebra]] of [[finite number|finite]] [[dimension]];

1. $(V, \rho)$ a $\mathfrak{g}$-[[Lie algebra module]] of [[finite number|finite]] [[dimension]], which is [[reducible representation|reducible]];

1. $\mathfrak{h} \hookrightarrow \mathfrak{g}$ a sub-Lie algebra which is [[reductive Lie algebra|reductive]] in $\mathfrak{g}$ (Def. \ref{LieAlgebraReductiveInAmbientLieAlgebra}) in that its [[adjoint representation]] on $\mathfrak{g}$ is [[reducible representation|reducible]].

1. such that 

   $$
     \mathfrak{g} = \mathfrak{h} \ltimes \mathfrak{a}
   $$

   is a [[semidirect product Lie algebra]] (hence $\mathfrak{a}$ a [[Lie ideal]]).

Then the [[invariants]] in the Lie algebra cohomology of $\mathfrak{a}$ (either with respect to $\mathfrak{h}$ or all of $\mathfrak{g}$) coincide with the relative Lie algebra cohomology (Def. \ref{RelativeLieAlgebraCohomologyWithCoefficients}, using the invariant subcomplex!):

$$
   H^\bullet(\mathfrak{a}; V)^{\mathfrak{h}}
   \;\simeq\;
   H^\bullet(\mathfrak{g}, \mathfrak{h}; V)
   \,.   
$$


=--

([Solleveld 02, theorem 2.28](#Solleveld02))

Proof via the [[Hochschild-Serre spectral sequence]].

## Examples

Every [[invariant polynomial]] $\langle - \rangle \in W(\mathfrak{g})$ on a Lie algebra has a _transgression_ to a cocycle on $\mathfrak{g}$. See [[∞-Lie algebra cohomology]] for more.

For instance for $\mathfrak{g}$ a [[semisimple Lie algebra]], there  is the [[Killing form]] $\langle - ,- \rangle$. The corresponding 3-cocycle is

$$
  \mu = \langle -, [-,-] \rangle : CE(\mathfrak{g})
  \,,
$$

that is: the function that sends three Lie algebra elements $x, y, z$ to the number  $\mu(x,y,z) = \langle x, [y,z]\rangle$.

On the [[super Poincare Lie algebra]] in dimension (10,1) there is a 4-cocycle

$$
  \mu_4 = \bar \psi \wedge \Gamma^{a b} \Psi\wedge e_a \wedge e_b
  \in
  CE(\mathfrak{siso}(10,1))
$$


## Extensions
 
Every Lie algebra degree $n$ cocycle $\mu$ (with values in the trivial model) gives rise to an extension

$$
  b^{n-2} \mathbb{R} \to \mathfrak{g}_{\mu}
  \to \mathfrak{g}
  \,.
$$

In the language of [[∞-Lie algebra]]s this was observed in ([BaezCrans Theorem 55](#BaezCrans)).

In the dual [[dg-algebra]] language the extension is lust the relative [[Sullivan algebra]]

$$
  CE(\mathfrak{g}_\mu) \leftarrow CE(\mathfrak{g})
$$

obtained by gluing on a rational $n$-sphere. By this kind of translation between familiar statements in [[rational homotopy theory]] dually into the language of [[∞-Lie algebra]]s many useful statements in [[∞-Lie theory]] are obtained.

**Examples**

* The [[string Lie 2-algebra]] is the extension of a [[semisimple Lie algebra]] induced by the canonical 3-cocycle coming from the [[Killing form]].

* The [[supergravity Lie 3-algebra]] is the extension of the [[super Poincare Lie algebra]] by a 4-cocycle.

## Related concepts

* [[Hochschild-Serre spectral sequence]]

* [[signs in supergeometry]]

* [[infinity-Lie algebra cohomology]]

## References

### Ordinary Lie algebras

Accounts of the standard theory of Lie algebra cohomology include
 
* {#Koszul50} [[Jean-Louis Koszul]], _Homologie et cohomologie des alg&egrave;bres de Lie_, Bull. Soc. Math. France 78 (1950), 65-127

* [[Gerhard Hochschild]], [[Jean-Pierre Serre]], _Cohomology of Lie algebras_, Annals of Mathematics, Second Series, Vol. 57, No. 3 (May, 1953), pp. 591-603 ([JSTOR](http://www.jstor.org/stable/1969740))

* [[Werner Greub]], [[Stephen Halperin]], [[Ray Vanstone]], in chapter V in vol III of _[[Connections, Curvature, and Cohomology]]_ Academic Press (1973)

* [[Charles Weibel]], chapter 7 of _An introduction to homological algebra_, Cambridge Studies in Adv. Math. __38__, CUP 1994

* [[José de Azcárraga]], Jos&#233; M. Izquierdo, section 6 of _[[Lie Groups, Lie Algebras, Cohomology and Some Applications in Physics]]_, Cambridge monographs of mathematical physics, (1995)

* [[José de Azcárraga]], Jos&#233;  M. Izquierdo, J. C. Perez Bueno, _An introduction to some novel applications of Lie algebra cohomology and physics_ ([arXiv:physics/9803046](http://arxiv.org/abs/physics/9803046))

* {#Solleveld02} [[Maarten Solleveld]], _Lie algebra cohomology and
Macdonald’s conjectures_, 2002 ([pdf](https://www.math.ru.nl/~solleveld/scrip.pdf))

See also

* [[eom]] _[Lie algebra cohomology](http://eom.springer.de/C/c023140.htm)_

* [wikipedia](http://en.wikipedia.org/wiki/Lie_algebra_cohomology)


* scholarpedia: [An introduction to Lie algebra cohomology](http://www.scholarpedia.org/article/An_introduction_to_Lie_algebra_cohomology)

### Super Lie algebras
 {#ReferencesSuperLieAlg}


The cohomology of [[super Lie algebra]]s is analyzed via [[normed division algebra]]s in

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_ ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

See also [[division algebra and supersymmetry]].

This subsumes some of the results in

* [[José de Azcárraga]], [[Paul Townsend]], _Superspace geometry and classification of supersymmetric extended objects_, Phys. Rev. Lett. 62, 2579--2582 (1989) ([doi:10.1103/PhysRevLett.62.2579](https://doi.org/10.1103/PhysRevLett.62.2579))

The cohomology of the [[super Poincare Lie algebra]] in low dimensions $\leq 5$ is analyzed in

* [[Friedemann Brandt]], 

  _Supersymmetry algebra cohomology I: Definition and general structure_ 	J. Math. Phys.51:122302, 2010, [arXiv](http://arxiv.org/abs/0911.2118)

  _Supersymmetry algebra cohomology II: Primitive elements in 2 and 3 dimensions_ 	J. Math. Phys. 51 (2010) 112303 ([arXiv](http://arxiv.org/abs/1004.2978))

  _Supersymmetry algebra cohomology III: Primitive elements in four and five dimensions_ ([arXiv](http://arxiv.org/abs/1005.2102))

and in higher dimensions more generally in

* Michael Movshev, [[Albert Schwarz]], Renjun Xu, _Homology of Lie algebra of supersymmetries_ ([arXiv](http://arxiv.org/abs/1011.4731)) .

On [[Lie algebra cohomology]] of [[super Lie algebras]] (see also the [[Green-Schwarz action functional|brane scan]]) in relation to [[integration over supermanifolds|integrable forms]] of coset [[supermanifolds]]:

* [[Roberto Catenacci]], [[C. A. Cremonini]], [[Pietro Antonio Grassi]], [[Simone Noja]], _Cohomology of Lie Superalgebras: Forms, Integral Forms and Coset Superspaces_ ([arXiv:2012.05246](https://arxiv.org/abs/2012.05246))


### Extensions


The [[∞-Lie algebra]] [[∞-Lie algebra cohomology|extensions]] $b^{n-2} \to \mathfrak{g}_\mu \to \mathfrak{g}$ induced by a degree $n$-cocycle are considered 

* {#BaezCrans} [[John Baez]], [[Alissa Crans]], around theorem 55 in _Higher-Dimensional Algebra VI: Lie 2-Algebras_, Theory and Applications of Categories 12 (2004), 492-528.  [arXiv](http://arxiv.org/abs/math.QA/0307263)



[[!redirects Lie algebra cocycle]]
[[!redirects Lie algebra cocycles]]