

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Algebraic cobordism_ is the bigraded [[generalized cohomology theory]] represented by the [[motivic Thom spectrum]] $MGL$.  Hence it is the algebraic or [[motives|motivic]] analogue of [[complex cobordism]].  The $(2n,n)$-graded part has a geometric description via [[cobordism]] classes, at least over fields of characteristic zero.

## Definition

Let $S$ be a [[scheme]] and $MGL_S$ the [[motivic Thom spectrum]] over $S$.  **Algebraic cobordism** is the [[generalized motivic cohomology theory]] $MGL_S^{*,*}$ represented by $MGL_S$:

... formula here ...

## Properties

### The (2n,n)-graded part

Let $S = Spec(k)$ where $k$ is a field of characteristic zero.
A geometric description of the $(2n,n)$-graded part of algebraic cobordism was given by [[Marc Levine]] and [[Fabien Morel]].  More precisely, [Levine-Morel](#LevineMorel) constructed the universal _oriented cohomology theory_ $\Omega^* : \Sm_k \to CRing^*$.  Here _oriented_ signifies the existence of [[direct image]] or [[Gysin homomorphisms]] for [[proper morphisms of schemes]].  This implies the existence of[[Chern classes]] for [[vector bundles]].

+-- {: .num_theorem}
###### Theorem
**([Levine-Morel](#LevineMorel))**.
There is a canonical isomorphism of graded rings
  $$ \mathbf{L}^* \stackrel{\sim}{\longrightarrow} \Omega^*(\Spec(k)) $$
where $\mathbf{L}^*$ denotes the [[Lazard ring]] with an appropriate grading.
=--

+-- {: .num_theorem}
###### Theorem
**([Levine-Morel](#LevineMorel))**.
Let $i : Z \hookrightarrow X$ be a [[closed immersion]] of smooth $k$-schemes and $j : U \hookrightarrow X$ the complementary [[open immersion]].  There is a canonical exact sequence of graded abelian groups
  $$ \Omega^{*-d}(Z) \stackrel{i_*}{\to} \Omega^*(X) \stackrel{j^*}{\to} \Omega^*(U) \to 0, $$
where $d = \codim(Z, X)$.
=--

+-- {: .num_theorem}
###### Theorem
**([Levine-Morel](#LevineMorel))**.
Given an embedding $k \hookrightarrow \mathbf{C}$, the canonical homomorphism of graded rings
  $$ \Omega^*(k) \longrightarrow MU^{2*}(pt) $$
is invertible.
=--

+-- {: .num_theorem}
###### Theorem
**([Levine 2008](#Levine2008))**.
The canonical homomorphisms of graded rings
  $$ \Omega^*(X) \longrightarrow MGL^{2*,*}(X) $$
are invertible for all $X \in \Sm_k$.
=--

## Related concepts

* [[motivic Thom spectrum]]
* [[complex cobordism]]
* [[motivic homotopy theory]]
* [[motivic cohomology]]
* [[algebraic K-theory]]

\linebreak

[[!include flavours of cobordism cohomology theories -- table]]


## References

There are two notions of "algebraic cobordism", not closely related, one due to [Snaith 77](#Snaith77), and one due to [Levine-Morel 01](#LevineMorel01).


### Snaith's construction
 {#SnaithConstructiom}

* {#Snaith77} [[Victor Snaith]],  _Towards algebraic cobordism_,  Bull. Amer. Math. Soc. 83 (1977), 384-385 ([doi:10.1090/S0002-9904-1977-14281-X](https://doi.org/10.1090/S0002-9904-1977-14281-X))


* {#Snaith79} [[Victor Snaith]], _Algebraic Cobordism and K-theory_, Mem. Amer. Math. Soc. no 221 (1979) 

* {#GepnerSnaith08} [[David Gepner]], [[Victor Snaith]], _On the motivic spectra representing algebraic cobordism and algebraic K-theory_, Documenta Math.  2008 ([arXiv:0712.2817](http://arxiv.org/abs/0712.2817))
 
The construction in [Snaith 77](#Snaith77), motivated from the [[Conner-Floyd isomorphism]], uses a variant of his general construction ([[Snaith's theorem]]) of a periodic [[multiplicative cohomology theory]] $X(b)^*(-)$ out of a pair consisting of a homotopy commutative [[H-monoid]] $X$ and a class $b\in \pi_n(X)$: 

When $X = B S^1$ (the [[classifying space]] of the [[circle group]]) and $b$ is a generator of $\pi_2(BS^1)\cong\mathbb{Z}$ then $X(b)^*(-)$ is isomorphic with 2-periodic [[complex K-theory]]. 

When $X = B U$ and $b$ a generator of $\pi_2(BU)\cong\mathbb{Z}$ one obtains $MU^*[u_2,u_2^{-1}]$ where [[MU]] is the (topological) [[complex cobordism cohomology]] and $u_2$ is the periodicity element. 

Then Snaith introduces a variant of such constructions with a more general ring $A$ replacing the complex numbers; and uses the Quillen's description of [[algebraic K-theory]] of a ring $A$ in terms of the [[classifying space]] $B GL(A)$; this way he obtains an algebraic cobordism theory. 

Later, [Gepner-Snaith 08](#GepnerSnaith08) returned to the question of algebraic cobordism this time using the motivic version of algebraic cobordism of Voevodsky, namely the [[motivic spectrum]] $M GL$ representing universal oriented motivic cohomology theory (which is different from Morel-Voevodsky algebraic cobordism), and to the motivic version of [[Conner-Floyd isomorphism]] for which they give a comparably short proof.  


### Morel-Levine's construction

* {#LevineMorel01} [[Marc Levine]], [[Fabien Morel]], _Cobordisme alg&#233;brique I_, Note aux C.R. Acad. Sci. Paris, 332 S&#233;rie I, p. 723--728, 2001 (<a href="http://dx.doi.org/10.1016/S0764-4442(01)01833-X">doi:10.1016/S0764-4442(01)01833-X</a>); _Cobordisme alg&#233;brique II_, Note aux C.R. Acad. Sci. Paris, 332 S&#233;rie I, p. 815--820, 2001 (<a href="http://dx.doi.org/10.1016/S0764-4442(01)01832-8">doi:10.1016/S0764-4442(01)01832-8</a>).

* [[Marc Levine]], _Algebraic cobordism_, Proceedings of the ICM, Beijing 2002, vol. 2, 57--66, [math.KT/0304206](http://arxiv.org/abs/math/0304206)

* {#LevineMorel} [[Marc Levine]], [[Fabien Morel]], _Algebraic cobordism_, Springer 2007, [pdf](https://www.uni-due.de/~bm0032/publ/AlgCobordBook4.pdf).

* [[Marc Levine]], _A survey of algebraic cobordism_ ([pdf](http://www.uni-due.de/~bm0032/publ/SurveyAlgCobord.pdf&#8206;))

* [[Marc Levine]], _Three lectures on algebraic cobordism_, University of Western Ontario Mathematics Department, 2005, [Lecture I](http://www.uni-due.de/~bm0032/publ/CobordismLec1LS.pdf), [Lecture II](http://www.uni-due.de/~bm0032/publ/CobordismLec2LS.pdf), [Lecture III](http://www.uni-due.de/~bm0032/publ/CobordismLec4LS.pdf).

* [[Marc Levine]], [[Fabien Morel]], [[Oberwolfach]] Arbeitsgemeinschaft mit aktuellem Thema, April 2005 [report](http://www.ems-ph.org/journals/show_abstract.php?issn=1660-8933&vol=2&iss=2&rank=2), [notes](http://www.ems-ph.org/journals/show_pdf.php?issn=1660-8933&vol=2&iss=2&rank=2)



* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _A universality theorem for Voevodsky's algebraic cobordism spectrum_, Homology, Homotopy and Applications, 2008, 10(2), 211-226 ([arXiv:0709.4116](http://arxiv.org/abs/0709.4116))

* [[Ivan Panin]], K. Pimenov, [[Oliver Röndigs]], _On the relation of Voevodsky's algebraic cobordism to Quillen's K-theory_, Inventiones mathematicae, 2009, 175(2), 435-451, [doi:10.1.1.244.7301](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.244.7301), [arXiv:0709.4124](http://arxiv.org/abs/0709.4124).

* [[Marc Hoyois]], _From algebraic cobordism to motivic cohomology_, [pdf](http://math.mit.edu/~hoyois/papers/hopkinsmorel.pdf), [arXiv](http://arxiv.org/abs/1210.7182).

* [[Markus Spitzweck]], _Algebraic cobordism in mixed characteristic_ ([arXiv:1404.2542](http://arxiv.org/abs/1404.2542))


* [[Marc Levine]], [[Girja Shanker Tripathi]], _Quotients of MGL, their slices and their geometric parts_, [arXiv:1501.02436](http://arxiv.org/abs/1501.02436).

More chat about the relation to [[motivic homotopy theory]]:


* _Interdependence between A^1-homotopy theory and algebraic cobordism_, [MO/36659](http://mathoverflow.net/questions/36659/interdependence-between-a1-homotopy-theory-and-algebraic-cobordism/36698#36698).



A simpler construction was given in

* M. Levine, R. Pandharipande, _Algebraic cobordism revisited_ ([math.AG/0605196](http://arxiv.org/abs/math/0605196))

A [[Borel-Moore homology]] version of $MGL^{*,*}$ is considered in

* [[Marc Levine]], _Oriented cohomology, Borel-Moore homology and algebraic cobordism_, [arXiv](http://arxiv.org/abs/0807.2257).

The comparison with $MGL^{2*,*}$ is in

* {#Levine2008} [[Marc Levine]], _Comparison of cobordism theories_, Journal of Algebra, 322(9), 3291-3317, 2009, [arXiv](http://arxiv.org/abs/0807.2238).

The construction was extended to [[derived algebraic geometry|derived schemes]] in the paper

* Parker Lowrey, [[Timo Schuerg]].  _Derived algebraic bordism_, 2012, [arXiv:1211.7023](http://arxiv.org/abs/1211.7023).

The close connection of algebraic cobordism with [[K-theory]] is discussed in

* Jos&#233; Luis Gonz&#225;lez, Kalle Karu.  _Universality of K-theory_.  2013.  [arXiv:1301.3815](http://arxiv.org/abs/1301.3815).

An algebraic analogue of h-cobordism:

* Aravind Asok, Fabien Morel, _Smooth varieties up to $\mathbb{A}^1$-homotopy and algebraic h-cobordisms_, [arXiv:0810.0324](http://arxiv.org/abs/0810.0324)

[[!redirects algebraic cobordism spectrum]]
[[!redirects algebraic cobordism spectra]]

