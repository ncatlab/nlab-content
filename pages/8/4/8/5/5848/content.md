
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

An [[adjoint functor|adjoint]] pair of [[functor]]s 

$$
  (F\dashv G) : D \to C
$$ 

is a __Frobenius pair__ if $F$ is not only a [[left adjoint]] to $G$ but also a [[right adjoint]] to $G$, hence if we have an [[ambidextrous adjunction]], i.e. an [[adjoint triple]]

$$
  (F \dashv G \dashv F) : D \to C
  \,.
$$


In this case one often says that $F$ (or $G$) is a **Frobenius functor**. 

=--

+-- {: .num_note}
###### Note

There is _no_ relation to the notion of [[Frobenius monoidal functor]].

=--

## Properties

* K. Morita proved that the [[extension of scalars]] functor for a [[morphism]] of [[ring]]s $f:R\to S$ is Frobenius iff the morphism $f$ itself is Frobenius in the sense of ([Kasch](#Kasch)), that is: ${}_R S$ is finitely generated [[projective object|projective]] and ${}_S S_R\cong Hom_R({}_R S, {}_R R)$ as $R-S$-[[bimodule]]s. 

  This is in the spirit of the finite-dimensional duality coded e.g. in the notion of [[Frobenius algebra]]. 


## References

* Stefaan Caenepeel, Gigel Militaru, Shenglin Zhu, _Frobenius and separable functors for generalized module categories and nonlinear equations_, Springer Lec. Notes in Math. __1787__ (2002) xiv+354 pp, [gBooks](http://books.google.hr/books?id=6erTEpKIUaYC&lpg=PA89&ots=-TGKqXRstB&dq=Frobenius%20functors&hl=en&pg=PA89#v=onepage&q&f=false)

* F. Kasch, _Projektive Frobenius-Erweiterungen_, Sitzungsber, Heidelberger Akad. Wiss., Math.- Naturw. Kl. 1960/61 (1961), 89&#8211;109.
 {#Kasch}

[[!redirects Frobenious functor]]
[[!redirects Frobenious functors]]
[[!redirects Frobenius functors]]
