
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Goodwillie calculus
+--{: .hide}
[[!include Goodwillie calculus - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

In the context of [[Goodwillie calculus]] the _Taylor tower_ of an [[(∞,1)-functor]] $F$ to a [[Goodwillie-differentiable (∞,1)-category]] is its stagewise approximation by [[n-excisive (∞,1)-functors]] $P_n F$ (its [n-excisive projections](n-excisive+%28?%2C1%29-functor#nExcisiveApproximation))

$$
  \cdots \to P_{n+1} F \to P_n F \to \cdots \to P_1 F \to P_0 F
  \,.
$$

which is [[analogy|analogous]] to the approximation of a [[smooth function]] by its [[Taylor series]].

If this tower converges to $F$, then $F$ is analogous to an [[analytic function]] and is called an _[[analytic (∞,1)-functor]]_.

The [[spectral sequence]] induced by the [[filtration]] given by the Goodwillie-Taylor tower is the _[[Goodwillie spectral sequence]]_.

## Properties

### Convergence

convergence for $\rho$-[[analytic (∞,1)-functors]] on $\rho$-[[n-connected object of an (infinity,1)-topos|connective objects]] (...) ([Goodwillie 03, theorem 1.13](#Goodwillie03), see also [Munson-Volic 15, theorem 10.1.51 and section 10.2.4](#MunsonVolic15))

## Examples

### Stable splitting of mapping spaces
 {#StableSplittingOfMappingSpaces}

Under some conditions, the Goodwillie-Taylor tower of [[mapping spaces]] into sufficiently high [[suspensions]] is a [[direct sum]] of [[suspension spectra]] of [[configuration spaces]]. This _[[stable splitting of mapping spaces]]_ is originally due to ([Snaith 74](#Snaith74), [Bödigheimer 87](#Boedigheimer87)) and was understood as a Goodwillie-Taylor tower in [Arone 99](#Arone99), see also [Ching 05](#Ching05).

## Related concepts

* [[n-excisive (∞,1)-functor]]

* [[Postnikov tower]], [[chromatic tower]]

## References

### General

The concept originates in 

* {#Goodwillie03} [[Thomas Goodwillie]], _Calculus III: Taylor Series_, Geom. Topol. 7(2003) 645-711 ([arXiv:math/0310481](http://arxiv.org/abs/math/0310481))

Review includes

* {#MunsonVolic15} [[Brian Munson]], [[Ismar Volic]], _Cubical homotopy theory_, Cambridge University Press, 2015 [pdf](http://palmer.wellesley.edu/~ivolic/pdf/Papers/CubicalHomotopyTheory.pdf)

See also

* [[Gregory Arone]], [[Michael Ching]], _A classification of Taylor towers of functors of spaces and spectra_ ([arXiv:1209.5661](http://arxiv.org/abs/1209.5661))

### Stable splitting of mapping spaces

The [[stable splitting of mapping spaces]] is originally due to 

* {#Snaith74} [[Victor Snaith]],  _A stable decomposition of $\Omega^n S^n X$_, Journal of the London Mathematical Society 7 (1974), 577 - 583 ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/snaiths.pdf))

Review and generalization is due to 

* {#Boedigheimer87} [[Carl-Friedrich Bödigheimer]], _Stable splittings of mapping spaces_, Algebraic topology. Springer 1987. 174-187 ([pdf](http://www.math.uni-bonn.de/~cfb/PUBLICATIONS/stable-splittings-of-mapping-spaces.pdf))

Further generalization and interpretation in terms of the Goodwillie-Taylor tower of mapping spaces is due to

* {#Arone99} [[Greg Arone]], _A generalization of Snaith-type filtration_, Transactions of the American Mathematical Society 351.3 (1999): 1123-1150. ([pdf](https://www.ams.org/journals/tran/1999-351-03/S0002-9947-99-02405-8/S0002-9947-99-02405-8.pdf))

* {#Ching05} [[Michael Ching]], _Calculus of Functors and Configuration Spaces_, Conference on Pure and Applied Topology Isle of Skye, Scotland, 21-25 June, 2005 ([pdf](https://www3.amherst.edu/~mching/Work/skye.pdf))
 

[[!redirects Goodwillie-Taylor towers]]

[[!redirects Taylor tower]]
[[!redirects Taylor towers]]

[[!redirects Goodwillie-Taylor series]]
