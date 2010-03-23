
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The Hochschild-Kostant-Rosenberg theory identifies the [[Hochschild cohomology]] and homology of certain function algebras with [[Kähler differential]]s and [[derivation]]s.

There is also a noncommutative analogue due to [[Alain Connes]]. 


## Details

The **[[Hochschild-Kostant-Rosenberg theorem]]** states that under suitable conditions, the Hochschild homology of an algebra (with coeficients in itself) computes the wedge powers of its [[Kähler differential]]s.

+-- {: .un_prop }
###### Proposition

For a $k$-algebra $R$, its module of [[Kähler differential]]s coincides with its first Hochschild homology

$$
  \Omega(R/k) \simeq H_1(R,R)
  \,.
$$


=--

Write $\Omega^0(R/k) := R \simeq HH_0(R,R)$.

For $n \geq 2$ Write $\Omega^n(R/k) = \wedge^n_R \Omega(R/k)$ for the $n$-fold [[exterior algebra|wedge product]] of $Omega(R/k)$ with itself: the degree $n$-K&#228;h&#246;er-differentials.

+-- {: .num_theorem }
###### Theorem

The isomorphism $\Omega^1(R/k) \simeq H_1(R,R)$ extends to a graded ring morphism

$$
  \psi : \Omega^\bullet(R/k) \to H_\bullet(R,R)
  \,.
$$

=--

If the $k$-algebra $R$ is sufficiently well-behaved, then this morphism is an [[isomorphism]] that identifies the Hochschild homology of $R$ in degree $n$ with $\Omega^n(R/k)$ for all $n$:

+-- {: .num_theorem }
###### Theorem
**(Hochschild-Kostant-Rosenberg theorem)**



If $k$ is a [[field]] and $R$ a commutative $k$-[[algebra]] which is 

* essentially of finite type 

* smooth over $R$

then there is an [[isomorphism]] of graded $R$-algebras

$$
  \psi : \Omega^\bullet(R/k) \stackrel{\simeq}{\to}
  H_\bullet(R,R)
  \,.
$$

Moreover, dually, there is an isomorphism of Hochschild cohomology with wedge products of derivations:

$$
  \wedge^\bullet_R Der(R,R) \simeq HH^\bullet(R,R)
$$


=--

+-- {: .proof}
###### Proof

This is reviewed for instance as theorem 9.4.7 of

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

or as theorem 9.1.3 in [Ginzburg](http://arxiv.org/PS_cache/math/pdf/0506/0506603v1.pdf#page=44).

=--






## References

The original source is

* Gerhard P. Hochschild, Bertram Kostant, Alex Rosenberg, _Differential forms on regular affine algebras_, Transactions AMS __102__ (1962), No.3, 383--408 (reprinted in G. P. Hochschild, Collected Papers. Volume I 1955-1966, Springer 2009, 265-290) [DOI:10.2307/1993614](http://dx.doi.org/10.2307/1993614).

Textbook references include

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_ section 9.4


and 

* [[Victor Ginzburg]], _Lectures on noncommutative geometry_ ([arXiv:math/0506603](http://arxiv.org/abs/math.AG/0506603)) section 4

where this appears as theorem 9.1.3.


[[!redirects Hochschild–Kostant–Rosenberg theorem]]
[[!redirects Hochschild--Kostant--Rosenberg theorem]]