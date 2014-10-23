
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

The _diffeomorphism group_ $Diff(X)$ of a [[smooth manifold]] $X$ is the [[group]] of its [[diffeomorphism]]s: the [[automorphism group]] of $X$ as an [[object]] of the [[category]] [[SmoothMfd]].

## Examples

### Of the 3-sphere

+-- {: .num_theorem #SmaleConjecture}
###### Theorem

The diffemorphism group of the 3-sphere is [[homotopy equivalence|homotopy equivalent]] to the [[orthogonal group]] $O(4)$, the equivalence being exhibited by the canonical inclusion

$$
  O(4) \hookrightarrow Diff(S^3)
  \,.
$$

=--

After being conjectured by Smale, this was proven in ([Hatcher 1983](#Hatcher)).

### Of general 3-manifolds

+-- {: .num_theorem}
###### Theorem

For every [[smooth manifold]] $X$ of [[dimension]] 3 the canonical map

$$
  Diff(X) \to Homeo(X)
$$

sending [[diffeomorphisms]] to their underlying [[homeomorphisms]] of [[topological spaces]] is a [[weak homotopy equivalence]]. 

=--

That this follows from the Smale cojecture, theorem \ref{SmaleConjecture}, was shown in [Cerf](#Cerf). For discussion see [Hatcher, 1978](#Hatcher78).


## Properties

### Relation to homotopy equivalences

For the following kinds of manifolds $\Sigma$ it is true that every [[homotopy equivalence]] 

$$
  \alpha \colon \Pi(\Sigma) \stackrel{\simeq}{\longrightarrow} \Pi(\Sigma)
$$

(hence every [[equivalence of infinity-groupoids|equivalence]] of their [[fundamental infinity-groupoids]]) is [[homotopy|homotopic]] to a [[diffeomorphism]]

$$
  a \colon \Sigma \stackrel{\simeq}{\longrightarrow} \Sigma
$$

i.e. that given $\alpha$ there is $a$ with

$$
  \alpha \simeq \Pi(a)
  \,.
$$


* for $\Sigma$ any [[surface]] ([Zieschang-Vogt-Coldeway](#ZieschangVogtColdeway))

* for $\Sigma$ a [[Haken 3-manifold]] ([Waldhausen](#Waldhausen68)) 

* for $\Sigma$ any  [[hyperbolic manifold]] of finite [[volume]] and of [[dimension]] $\geq 3$ (by [[Mostow rigidity theorem]]) (check)



## References

### For 2-manifolds (surfaces)

* {#ZieschangVogtColdeway} Zieschang, Vogt and Coldeway, _Surfaces and planar discontinuous groups_


### For 3-manifolds

* {#Cerf} J. Cerf, _Sur les diff&#233;omorphismes de la sph&#232;re de dimension trois ($\Gamma_4 = 0$)_, Lecture Notes in Math., vol. 53, Springer-Verlag, Berlin and New York, 1968_
 

* {#Hatcher78} [[Allen Hatcher]], _Linearization in 3-dimensional topology_, Proceedings of the international congress of Mathematicians, Helsinki (1978)
 
* {#Hatcher} [[Allen Hatcher]], _A proof of the Smale conjecture, $Diff(S^3) \simeq O(4)$, Annals of Mathematics 117 (1983) ([jstor](http://www.jstor.org/pss/2007035))
 

* {#Waldhausen68} [[Friedhelm Waldhausen]], _On Irreducible 3-Manifolds Which are Sufficiently Large_, Annals of Mathematics
Second Series, Vol. 87, No. 1 (Jan., 1968), pp. 56-88 ([JSTOR](http://www.jstor.org/stable/1970594))

[[!redirects diffeomorphism groups]]
[[!redirects Smale conjecture]]