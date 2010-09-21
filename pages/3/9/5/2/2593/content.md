
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### $(\infty,1)$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

_Lie algebra cohomology_ is the intrinsic notion of [[cohomology]] of [[Lie algebra]]s.

There is a precise sense in which Lie algebras $\mathfrak{g}$ are [[infinitesimal object|infinitesimal]] [[Lie group]]s. Lie algebra cohomology is the restriction of the definition of [[Lie group cohomology]] to Lie algebras.

In [[∞-Lie theory]] one studies the relation between the two via [[Lie integration]].

Lie algebra cohomology generalizes to [[nonabelian Lie algebra cohomology]] and to [[∞-Lie algebra cohomology]].

## Defintion

There are several different but equivalent definitions of the [[cohomology]] of a [[Lie algebra]].

### As Ext-group or derived functor

The abelian [[cohomology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H^*_{Lie}(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(k,M)$ where $k$ is the ground field understood as a trivial module over the universal enveloping algebra $U\mathfrak{g}$. In particular it is a derived functor. 

### Via resolutions

Before this approach was advanced in Cartan-Eilenberg's _Homological algebra_, Lie algebra cohomology and homology were defined by Chevalley-Eilenberg with a help of concrete Koszul-type resolution which is in this case a cochain complex 

$$Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M),$$ 

where the first argument $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is naturally equipped with a differential to start with (see below). The first argument in the Hom, i.e. $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is sometimes called the Chevalley-Eilenberg chain complex (cf. Weibel); the [[Chevalley-Eilenberg cochain complex]] is the whole thing, i.e. 

$$CE(\mathfrak{g},M) := Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M).$$

If $M$ is a trivial module $k$ then $CE(\mathfrak{g}) := Hom_k(\Lambda^* \mathfrak{g},k)$ and if $\mathfrak{g}$ is finite-dimensional this equals $\Lambda^* \mathfrak{g}^*$ with an appropriate differential and the exterior multiplication gives it a dg-algebra structure.

### Via $\infty$-Lie algebras

As discussed at [[Chevalley-Eilenberg algebra]], we may identify Lie algebras $\mathfrak{g}$ as the duals $CE(\mathfrak{g})$ of [[dg-algebra]]s whose underlying graded algebra is the [[Grassmann algebra]] on the vector space $\mathfrak{g}^*$.

Similarly, a dg-algebra $CE(\mathfrak{h})$ whose underlying algebra is free on a [[graded vector space]] $\mathfrak{h}$ we may understand as exibiting an [[∞-Lie algebra]]-structure on $\mathfrak{h}$.

Then a morphism $\mathfrak{g} \to \mathfrak{h}$ of these $\infty$-Lie algebras is by definition just a morphism $CE(\mathfrak{g}) \leftarrow CE(\mathfrak{h})$ of dg-algebras. Such a morphis may be thought of as a cocycle in [[nonabelian Lie algebra cohomology]] $H(\mathfrak{g}, \mathfrak{h})$.

Specifically, write $b^{n-1} \mathbb{R}$ for the $\infty$-Lie algebra given by the fact that $CE(b^{n-1}\mathbb{R})$ has a single generator in degree $n$ and vanishing differential. Then a morphism 


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


## References

### Ordinary Lie algebras

* [Springer online enc:Lie algebra cohomology](http://eom.springer.de/C/c023140.htm)

* [wikipedia](http://en.wikipedia.org/wiki/Lie_algebra_cohomology)

* Charles Weibel, _An introduction to homological algebra_, ch. 7, Cambridge Studies in Adv. Math. __38__, CUP 1994

* scholarpedia: [An introduction to Lie algebra cohomology](http://www.scholarpedia.org/article/An_introduction_to_Lie_algebra_cohomology)

### Super Lie algebras

The cohomology of [[super Lie algebra]]s is analyzed via [[normed division algebra]]s in

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry I_ ([arXiv:0909.0551](http://arxiv.org/abs/0909.0551))

* [[John Baez]], [[John Huerta]], _Division algebras and supersymmetry II_ ([arXiv:1003.34360](http://arxiv.org/abs/1003.3436))

See also [[division algebra and supersymmetry]].

This subsumes some of the results in

* J. A. de Azc&#225;rraga and P. K. Townsend, _Superspace geometry and classification of supersymmetric extended objects_, Phys. Rev. Lett. 62, 2579--2582 (1989)

### Extensions

An elementary introduction to Lie algebra cohomology is at the beginning of 

* J. A. de Azcarraga, J. M. Izquierdo, J. C. Perez Bueno, _An introduction to some novel applications of Lie algebra cohomology and physics_ ([arXiv](http://arxiv.org/abs/physics/9803046))

The [[∞-Lie algebra]] extensions $b^{n-2} \to \mathfrak{g}_\mu \to \mathfrak{g}$ induced by a degree $n$-cocycle are considered around theorem 55 in

* John Baez and Alissa Crans, Higher-Dimensional Algebra VI: Lie 2-Algebras, Theory and Applications of Categories 12 (2004), 492-528.  [arXiv](http://arxiv.org/abs/math.QA/0307263)
{#BaezCrans}
