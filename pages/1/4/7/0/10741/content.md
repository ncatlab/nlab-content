
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

For $n \in \mathbb{N}$ with $n \gt 1$, consider [[continuous functions]] between [[spheres]] of the form

$$
  \phi \;\colon\; S^{2n-1} \longrightarrow S^n
  \,.
$$

The [[homotopy cofiber]] of $\phi$ 

$$
  cofib(\phi) \simeq S^n \underset{S^{2n-1}}{\cup} D^{2n}
$$

has [[ordinary cohomology]] 

$$
  H^k(cofib(\phi), \mathbb{Z})
  \simeq
  \left\{
    \array{  
      \mathbb{Z} & for\; k = n, 2n;
      \\
      0 &  otherwise
    }
  \right.
  \,.
$$

Hence for $\alpha, \beta$ generators of the cohomology groups in degree $n$ and $2n$ (unique up to choice of sign), respectively, there exists an [[integer]] $h(\phi)$ which expresses the [[cup product]] square of $\alpha$ as a multiple of $\beta$:

$$
  \alpha \cup \alpha = h(\phi) \cdot \beta 
  \,.
$$

This integer $h(\phi) \in \mathbb{Z}$ is called the _Hopf invariant_ of $\phi$.

It depends on the choices made only up to sign. In particular it has a well-defined image $[h(\phi)] \in \mathbb{F}_2 = \mathbb{Z}/2\mathbb{Z}$, and as such it is the [[Steenrod square]] 

$$
  [h(\phi)] \cdot (-)
    \;\colon\; 
  \mathbb{F}_2
    \simeq
  H^n(cofib(\phi), \mathbb{F}_2) 
   \stackrel{Sq^n}{\longrightarrow}
  H^{2n}(cofib(\phi), \mathbb{F}_2) 
   \simeq
  \mathbb{F}_2
  \,.
$$

## Properties

### Generic values

For $n$ odd, the Hopf invariant necessarily vanishes. For $n$ even however, then there is a homomorphism

$$
  \pi_{2n-1}(S^n) \longrightarrow  \mathbb{Z}
$$

whose [[image]] contains at least the even integers.

### Hopf invariant one

Hence a famous open question in the 1950s was for which maps $\phi$ one has Hopf invariant one, $h(\phi) = 1$.

The _[[Hopf invariant one theorem]]_ ([Adams60](Hopf+invariant+one#Adams60)) states that the only maps of Hopf invariant one, $h(\phi) = 1$, are the [[Hopf constructions]] on the four real [[normed division algebras]]:

* the [[real Hopf fibration]];

* the [[complex Hopf fibration]];

* the [[quaternionic Hopf fibration]];

* the [[octonionic Hopf fibration]].

## Related concepts

* [[Hopf degree theorem]]

* [[EHP spectral sequence]]

## References

* {#Husemoller66} [[Dale Husemöller]], chapter 15 of _Fibre Bundles_, Graduate Texts in Mathematics 20, Springer New York (1966)

* [[John Michael Boardman]], B. Steer, _On Hopf Invariants_  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/boarstee.pdf))

* Michael Crabb, [[Andrew Ranicki]], _The geometric Hopf invariant_ ([pdf](http://www.maths.ed.ac.uk/~aar/slides/hopfbeam.pdf))

See also:

* Wikipedia, _[Hopf invariant](http://en.wikipedia.org/wiki/Hopf_invariant)_


Discussion via [[differential forms]]/[[rational homotopy theory]]:

* [[J. H. C. Whitehead]], _An expression of Hopf's invariant as an integral_, Proc. Nat. Acad. Sci. U. S. A.33 (1947), 117–123 ([jstor:87688](https://www.jstor.org/stable/87688))

* [[André Haefliger]], p. 3 of _Whitehead products and differential forms_, In: P.A. Schweitzer (ed.), _Differential Topology, Foliations and Gelfand-Fuks Cohomology_, Lecture Notes in Mathematics, vol 652. Springer 1978 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Prop. 17.22 in _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* {#SinhaWalter13} Dev Sinha, Ben Walter, _Lie coalgebras and rational homotopy theory II: Hopf invariants_, Trans. Amer. Math. Soc. 365 (2013), 861-883  ([arXiv:0809.5084](https://arxiv.org/abs/0809.5084), [doi:10.1090/S0002-9947-2012-05654-6](https://doi.org/10.1090/S0002-9947-2012-05654-6))

[[!redirects Hopf invariants]]
