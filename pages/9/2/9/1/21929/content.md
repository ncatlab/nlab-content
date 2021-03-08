
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _$f$-invariant_ ([Laures 99](#Laures99)) is the third in a sequence of [[homotopy invariants]] of "stable maps", i.e. of [[morphisms]] in the [[stable homotopy category]] (in particular: of [[stable homotopy groups of spheres]]), being elements of [[Ext-groups]] between the [[homology groups]]/[[cohomology groups]] of the [[domain]] and [[codomain]] of the map, with respect to some suitable choice of [[Whitehead-generalized cohomology theory]] $E$. 

The previous two invariants in the sequence are the _[[d-invariant]]_ and the _[[e-invariant]]_. All these are elements that appear on the second page of the $E$-[[Adams spectral sequence]].

In higher analogy to how the [[e-invariant]] exists if the [[d-invariant]] vanishes and then makes sense for $E = KU$ ([[complex topological K-theory]]), so the f-invariant exists when the [[e-invariant]] vanishes and then makes sense of $E$ an [[elliptic cohomology theory]].

Moreover, in higher analogy to how the [[e-invariant]], when expressed in terms of [[MU]]-[[bordism theory]], computes the [[Todd genus]]/[[A-hat genus]] of a [[manifold with corners]] (see [there](Adams+e-invariant#AsACobordismInvariantOfManifoldsWithBoundary)), so the f-invariant computes an [[elliptic genus]] of a [[manifold with corners]] ([Laures 00](#Laures00)).


(...)

Let $X \overset{\phi}{\longrightarrow} Y$ be morphism in the [[stable homotopy category]] out of a [[finite spectrum]] $X$ (for instance the image under [[suspension]] $\Sigma^\infty$ of a morphism in the [[classical homotopy category]] of [[pointed homotopy types]] out of a [[finite CW-complex]]).

If $E$ be a [[multiplicative cohomology theory]] satisfying the flatness assumptions used in the [[Adams spectral sequence]], and such that the [[e-invariant]] of $\phi$ in $E$ vanishes. Then the _$f$-invariant_ of $\phi$ ([Laures 99](#Laures99)) is a certain element in the second [[Ext-group]] $Ext^2_{E_\bullet(E)}\big( E_\bullet(X), E_\bullet(Y) \big)$.

(...)



## Related concepts

* [[Adams spectral sequence]]

* [[d-invariant]], [[e-invariant]]

* [[manifold with corners]]

* [[MUFr]]


## References

The concept is due to 

* {#Laures99} Gerd Laures, _The topological $q$-expansion principle_, Topology Volume 38, Issue 2, March 1999, Pages 387-425 (<a href="https://doi.org/10.1016/S0040-9383(98)00019-6">doi:10.1016/S0040-9383(98)00019-6</a>)

* {#Laures00} Gerd Laures, _On cobordism of manifolds with corners_, Trans. Amer. Math. Soc. 352 (2000) ([doi:10.1090/S0002-9947-00-02676-3](https://doi.org/10.1090/S0002-9947-00-02676-3))

  > (see [Genauer 12](manifold+with+boundary#Genauer12) for more on the bordism classes of [[manifolds with corners]])

Further discussion in:


* Hanno von Bodecker, _On the geometry of the f-invariant_ ([arXiv:0808.0428](https://arxiv.org/abs/0808.0428))

* [[Mark Behrens]], Gerd Laures, _$\beta$-family congruences and the f-invariant_ ([arXiv:0809.1125](https://arxiv.org/abs/0809.1125))

* [[Ulrich Bunke]], [[Niko Naumann]], _The f-invariant and index theory_, Manuscripta Math. 132, 365–397 (2010) ([arXiv:0808.0257](https://arxiv.org/abs/0808.0257), [https://doi.org/10.1007/s00229-010-0351-7](https://doi.org/10.1007/s00229-010-0351-7))

* Gerd Laures, _Toda brackets and congruences of modular forms_ ([arXiv:1102.3783](https://arxiv.org/abs/1102.3783), [euclid:agt/1513715257](https://projecteuclid.org/euclid.agt/1513715257))

See also:

* [[Lennart Meier]], [MO comment](https://mathoverflow.net/a/179639/381), 2014
