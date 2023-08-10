
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
  (F\dashv G) \;\colon\; D \longrightarrow C
$$ 

is a __Frobenius pair__ if $F$ is not only a [[left adjoint]] to $G$ but also a [[right adjoint]] to $G$, hence if we have an [[ambidextrous adjunction]], i.e. an [[adjoint triple]] of the fomr

$$
  (F \dashv G \dashv F) \;\colon\; D \longrightarrow C
  \,.
$$


In this case one often says that $F$ (or $G$) is a **Frobenius functor**. 

=--

\begin{remark}
There is _no_ relation to the notion of [[Frobenius monoidal functor]], but there *is* a close relation to *[[Frobenius monads]]*.
\end{remark}

## Properties

* [Morita 1965](#Morita65) proved that the [[extension of scalars]] functor for a [[morphism]] of [[rings]] $f:R\to S$ is Frobenius iff the morphism $f$ itself is Frobenius in the sense of ([Kasch](#Kasch)), that is: ${}_R S$ is finitely generated [[projective object|projective]] and ${}_S S_R\cong Hom_R({}_R S, {}_R R)$ as $R-S$-[[bimodule]]s. 

  This is in the spirit of the finite-dimensional duality coded e.g. in the notion of [[Frobenius algebra]]. 


## References

The concept originates under the name "[[strongly adjoint pair]]" in:

* {#Morita65} [[Kiiti Morita]], *Adjoint pairs of functors and Frobenius extensions*, Science Reports of the Tokyo Kyoiku Daigaku, Section A **9** 202/208 (1965) 40-71 &lbrack;[jstor:43698658](https://www.jstor.org/stable/43698658)&rbrack;

The terminology "Frobenius functor":

* Stefaan Caenepeel, Gigel Militaru, Shenglin Zhu, _Frobenius and separable functors for generalized module categories and nonlinear equations_, Springer Lec. Notes in Math. __1787__ (2002) &lbrack;[gBooks](http://books.google.hr/books?id=6erTEpKIUaYC&lpg=PA89&ots=-TGKqXRstB&dq=Frobenius%20functors&hl=en&pg=PA89#v=onepage&q&f=false)&rbrack;

* {#Kasch} F. Kasch, _Projektive Frobenius-Erweiterungen_, Sitzungsber, Heidelberger Akad. Wiss., Math.- Naturw. Kl. 1960/61 (1961) 89-109.
 

[[!redirects Frobenious functor]]
[[!redirects Frobenious functors]]
[[!redirects Frobenius functors]]
