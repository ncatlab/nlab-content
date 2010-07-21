

<div class="rightHandSide toc">
[[!include cohomology - contents]]
***
[[!include infinity-Lie theory - contents]]
</div>



#Contents#
* automatic table of contents goes here
{:toc}

## Definition as Ext-group or derived functor

The abelian [[cohomology]] of a $k$-[[Lie algebra]] $\mathfrak{g}$ with coefficients in the left $\mathfrak{g}$-module $M$ is defined as $H^*_{Lie}(\mathfrak{g},M) = Ext_{U\mathfrak{g}}^*(k,M)$ where $k$ is the ground field understood as a trivial module over the universal enveloping algebra $U\mathfrak{g}$. In particular it is a derived functor. 

## Definition via resolution

Before this approach was advanced in Cartan-Eilenberg's _Homological algebra_, Lie algebra cohomology and homology were defined by Chevalley-Eilenberg with a help of concrete Koszul-type resolution which is in this case a cochain complex 

$$Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M),$$ 

where the first argument $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is naturally equipped with a differential to start with (see below). The first argument in the Hom, i.e. $U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g}$ is sometimes called the Chevalley-Eilenberg chain complex (cf. Weibel); the [[Chevalley-Eilenberg cochain complex]] is the whole thing, i.e. 

$$CE(\mathfrak{g},M) := Hom_{\mathfrak{g}}(U\mathfrak{g}\otimes_k \Lambda^* \mathfrak{g},M)\cong Hom_k(\Lambda^* \mathfrak{g},M).$$

If $M$ is a trivial module $k$ then $CE(\mathfrak{g}) := Hom_k(\Lambda^* \mathfrak{g},k)$ and if $\mathfrak{g}$ is finite-dimensional this equals $\Lambda^* \mathfrak{g}^*$ with an appropriate differential and the exterior multiplication gives it a dg-algebra structure.

## Definition via $L_\infty$-morphisms

The degree $n$ Lie algebra cohomology with trivial coefficients computes the [[homotopy (as an operation)|homotopy]] classes of $L_\infty$-[[L-∞-algebra|algebra]] morphisms

$$
  \mathfrak{g} \to b^{n-1} \mathfrak{u}(1)
  \,.
$$

There is also [[nonabelian Lie algebra cohomology]] extending nicely the [[nPOV]] on Lie algebra cohomology.

## Extensions
 
Every Lie algebra degree $n$ cocycle $\mu$ gives rise to an extension

$$
  b^{n-2} \mathfrak{u}(1) \to \mathfrak{g}_{\mu}
  \to \mathfrak{g}
$$

of the [[Lie algebra]] by an $L_\infty$-[[L-∞-algebra|algebra]].   This is [[Theorem 55](http://arxiv.org/PS_cache/math/pdf/0307/0307263v6.pdf#page=42)] here:

* John Baez and Alissa Crans, Higher-Dimensional Algebra VI: Lie 2-Algebras, Theory and Applications of Categories 12 (2004), 492-528.  [arXiv](http://arxiv.org/abs/math.QA/0307263)

### Ordinary Lie algebras 

* [[String Lie 2-algebra]]


### Super Lie algebras 

* [[supergravity Lie 3-algebra]]

## References

### Ordinary Lie algebras

* [Springer online enc:Lie algebra cohomology](http://eom.springer.de/C/c023140.htm)

* [wikipedia](http://en.wikipedia.org/wiki/Lie_algebra_cohomology)

* Charles Weibel, _An introduction to homological algebra_, ch. 7, Cambridge Studies in Adv. Math. __38__, CUP 1994

* scholarpedia: [An introduction to Lie algebra cohomology](http://www.scholarpedia.org/article/An_introduction_to_Lie_algebra_cohomology)

### Super Lie algebras

* J. A. de Azc&#225;rraga and P. K. Townsend, _Superspace geometry and classification of supersymmetric extended objects_, Phys. Rev. Lett. 62, 2579--2582 (1989)
