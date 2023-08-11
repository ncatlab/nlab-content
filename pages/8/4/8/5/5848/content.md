
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

\begin{definition}\label{FrobeniusFunctor}
**(Frobenius functor)**
\linebreak
An [[adjoint functor|adjoint pair]]  of [[functors]] 

$$
  (F\dashv G) \;\colon\; D \longrightarrow C
$$ 

is called a _Frobenius pair_ if $F$ is not only a [[left adjoint]] to $G$ but also a [[right adjoint]] to $G$, hence if we have an [[ambidextrous adjunction]], i.e. an [[adjoint triple]] of the form

$$
  (F \dashv G \dashv F) \;\colon\; D \longrightarrow C
  \,.
$$

This situation was called a *[[strongly adjoint pair]]* by [Morita 1965](#Morita65), but the [Caenepeel, Militaru & Zhu 1997](#CaenepeelMilitaruZhu97) (followed by [CGN 1998](#CGN98)) suggested to refer to such $F$ as *Frobenius functors*.
\end{definition}


\begin{remark}\label{Terminology}
**(terminology)**
\linebreak
The terminology "Frobenius functor" (Def. \ref{FrobeniusFunctor}) is motivated by the observation (Thm. 5.1 there, see [below](#FrobeniusExtensions)) of [Morita 1965](#Morita65) (who instead speaks of "[[strongly adjoint pairs]]"!) that the functor of [[restriction of scalars]] $f^\ast$ along a [[homomorphism]] $f$ of [[rings]] has coinciding [[left adjoint]] ([[extension of scalars]]) and [[right adjoint]] ([[coextension of scalars]]) iff $f$ is a [[ring extension]] which is a "Frobenius extension" in the sense of [Kasch 1961](#Kasch61).

The suggestion to therefore refer to Morita's "strongly adjoint pairs" as "Frobenius functors" is due to [Caenepeel, Militaru & Zhu 1997](#CaenepeelMilitaruZhu97), seconded by [CGN 1998](#CGN98).

Beware of the independent terminology of "*[[Frobenius monoidal functor]]*" which does *not* refer to Frobenius functors that are also [[monoidal functor|monoidal]]. (Similarly, one should *not* refer to Kasch's *Frobenius extensions* as "[[Frobenius morphisms]]"!)

On the other hand, the ([[comonad|co]])[[monads]] [induced](monad#RelationBetweenAdjunctionsAndMonads) by Frobenius adjunctions are the *[[Frobenius monads]]*, see the discussion [there](Frobenius+monad#Properties).
\end{remark}

## Examples

\begin{example}
\label{FrobeniusExtensions}
[Morita 1965](#Morita65) proved that the [[extension of scalars]] functor for a [[morphism]] of [[rings]] $f:R\to S$ is Frobenius iff the morphism $f$ itself is a Frobenius extension  in the sense of ([Kasch 1961](#Kasch61)), that is: ${}_R S$ is finitely generated [[projective object|projective]] and ${}_S S_R\cong Hom_R({}_R S, {}_R R)$ as $R-S$-[[bimodule]]s. 

  This is in the spirit of the finite-dimensional duality coded e.g. in the notion of [[Frobenius algebra]]. 
\end{example}

## References

The concept originates under the name "[[strongly adjoint pair]]" in:

* {#Morita65} [[Kiiti Morita]], *Adjoint pairs of functors and Frobenius extensions*, Science Reports of the Tokyo Kyoiku Daigaku, Section A **9** 202/208 (1965) 40-71 &lbrack;[jstor:43698658](https://www.jstor.org/stable/43698658)&rbrack;

in application to the notion of "Frobenius extension" due to

* {#Kasch61} [[Friedrich Kasch]], *Projektive Frobenius-Erweiterungen*, Sitzungsberichte der Heidelberger Akademie der Wissenschaften (1961) &lbrack;[doi:10.1007/978-3-662-25130-0](https://doi.org/10.1007/978-3-662-25130-0), [pdf](https://epub.ub.uni-muenchen.de/17643/1/17643.pdf)&rbrack;



The terminology "Frobenius functor" for this situation is due to:

* {#CaenepeelMilitaruZhu97}  [[Stefaan Caenepeel]], [[Gigel Militaru]], [[Shenglin Zhu]], *Doi-Hopf modules, Yetter-Drinfel’d modules and Frobenius type properties*, Trans. Amer. Math. Soc. **349** (1997) 4311-4342 &lbrack;[1997-349-11/S0002-9947-97-02004-7](https://www.ams.org/journals/tran/1997-349-11/S0002-9947-97-02004-7), [pdf](https://www.ams.org/journals/tran/1997-349-11/S0002-9947-97-02004-7/S0002-9947-97-02004-7.pdf)&rbrack;

* {#CGN98} F. Castaño Iglesias, [[José Gómez-Torrecillas]], C. Nastasescu, _Frobenius functors: applications_, Comm. Alg. __27__ 10  (1998) 4879-4900 &lbrack;[doi:10.1080/00927879908826735](https://doi.org/10.1080/00927879908826735)&rbrack;

Further discussion:

* {#CaenepeelDeGrooMilitaru02} [[Stefaan Caenepeel]], E. De Groot, [[Gigel Militaru]], *Frobenius Functors of the second kind*, Comm. Algebra **30** (2002) 5359-5391 &lbrack;[arXiv:math/0106109](https://arxiv.org/abs/math/0106109), [doi:10.1081/AGB-120015657](https://doi.org/10.1081/AGB-120015657)&rbrack;

* [[Stefaan Caenepeel]], [[Gigel Militaru]], [[Shenglin Zhu]], _Frobenius and separable functors for generalized module categories and nonlinear equations_, Springer Lec. Notes in Math. __1787__ (2002) &lbrack;[gBooks](http://books.google.hr/books?id=6erTEpKIUaYC&lpg=PA89&ots=-TGKqXRstB&dq=Frobenius%20functors&hl=en&pg=PA89#v=onepage&q&f=false)&rbrack;

 

[[!redirects Frobenious functor]]
[[!redirects Frobenious functors]]
[[!redirects Frobenius functors]]

[[!redirects Frobenius extension]]
[[!redirects Frobenius extensions]]


