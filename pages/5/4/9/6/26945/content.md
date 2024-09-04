
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

A *polynomial identity* in a [[ring]] $R$ is a noncommutative [[polynomial]] in a [[finite number]] of [[variables]] $x_1,\ldots,x_n$ which [[evaluation|evaluates]] to zero for any choice $a_1\ldots,a_n$ substituted in place of the variables. 

If $R$ is an [[associative algebra|algebra]] in [[characteristic]] $p$ then $p x$ is an identity in $R$; this is a rather trivial case. It is a very special property of a ring to admit a nontrivial polynomial identity.

## Definition 

A polynomial identity ring is a ring with at least one polynomial identity with at least one of the coefficients
$\pm 1$. 

## Examples

* The commutativity identity $x_1 x_2 - x_2 x_1$ holds in any commutative ring. 

* (Amitsur--Levitski theorem) In the ring $M_n(F)$ of $n\times n$-matrices over any field $F$ the Amitsur--Levitzki standard identity holds,
$$
\sum_{\pi\in\Sigma(2 n)} 
sign(\pi) x_{\pi(1)}\cdots x_{\pi(2n)},
$$
where $\Sigma(2n)$ is the symmetric group on $2n$ letters. In addition, no monic polynomial identity in degree less than $2n$ exists for $M_n(F)$. 

## Properties

([Artin1969](#Artin)) Let $k$ be a prime field of characteristic $p$. A ring $A$ which is also a $k$-algebra is an [[Azumaya algebra]] of rank $n^2$ over its zenter $Z(A)$ iff the two conditions hold:

(i) it does not have a representation over a field $K\supset k$ of dimension strictly less than $n$ 

(ii) it satisfies all polynomial identities which hold in the ring of $n\times n$-matrices in characteristic $p$

## Literature

* [[Irving Kaplansky]], _Rings with a polynomial identity_, Bull. Amer. Math. Soc. __54__ (1948) 575--580 

* [[Shimshon Amitsur|S. A. Amitsur]], _Polynomial identities_, Israel J. Math __19__ (1974) 183--199 

* [[S. A. Amitsur]], _Associative rings with identities_. In: I. N. Herstein (eds) Some Aspects of Ring Theory. C.I.M.E. Summer Schools __37__. Springer 2010 [doi](https://doi.org/10.1007/978-3-642-11036-8_1)

* J. Levitzki, _A theorem on polynomial identities_, Proc. Amer. Math. Soc. __1__ (1950) 449--463

* Vesselin Drensky, [[Edward Formanek]], *Polynomial identity rings*, Birkhauser (2004) viii+200 pp &lbrack;[doi:10.1007/978-3-0348-7934-7](https://doi.org/10.1007/978-3-0348-7934-7)&rbrack;

  review:

  [[Louis Rowen]], Bull. AMS __43__ 2 (2006) 259--267 &lbrack;[pdf](https://www.ams.org/journals/bull/2006-43-02/S0273-0979-06-01082-2/S0273-0979-06-01082-2.pdf), [doi:2006-43-02/S0273-0979-06-01082-2](https://www.ams.org/journals/bull/2006-43-02/S0273-0979-06-01082-2)&rbrack;

* Wikipedia: [Polynomial identity ring](https://en.wikipedia.org/wiki/Polynomial_identity_ring), [Amitsur--Levitski theorem](https://en.wikipedia.org/wiki/Amitsur%E2%80%93Levitzki_theorem)

* {#Artin} [[Michael Artin]], _On Azumaya algebras and finite-dimensional representations of rings_, J. Algebra __11__ (1969) 532--563 &lbrack;<a href="https://doi.org/10.1016/0021-8693(69)90091-X">doi:10.1016/0021-8693(69)90091</a>&rbrack;

* [[Claudio Procesi]], _On the theorem of Amitsur--Levitzki_, Israel Journal of Mathematics __207__: 151---154 ([arXiv:1308.2421](https://arxiv.org/abs/1308.2421) [doi](https://doi.org/10.1007/s11856-014-1118-8))

category: algebra

[[!redirects PI-ring]]
[[!redirects PI ring]]
[[!redirects PI-rings]]
[[!redirects PI rings]]
[[!redirects polynomial identity rings]]

