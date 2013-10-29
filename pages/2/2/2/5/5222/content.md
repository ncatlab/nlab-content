
#Contents#
* table of contents
{:toc}

## Idea

The _Fourier-Mukai transform_ is a [[categorification|categorified]] [[integral transform]] analogous to the standard [[Fourier transform]].

## Definition

Let $X$ and $Y$ be [[schemes]] over a [[field]] $K$.
Let $E \in D(QCoh(O_{X \times Y}))$ be an object in the [[triangulated categories of sheaves|derived category of quasi-coherent sheaves]].
The functor $\Phi(E) : D(QCoh(O_X)) \to D(QCoh(O_Y))$ defined by
  \[ F \mapsto \mathbf{R}q_*(\mathbf{L}p^*(F) \otimes^{\mathbf{L}} E), \]
where $p$ and $q$ are the [[projections]] from $X \times Y$ onto $X$ and $Y$, respectively, is called the **Fourier-Mukai transform of $E$**, or the **Fourier-Mukai functor induced by $E$**.

When $F : D(QCoh(O_X)) \to D(QCoh(O_Y))$ is isomorphic to $\Phi(E)$ for some $E \in D(QCoh(O_{X \times Y}))$, one also says that $F$ is **represented by $E$** or simply that $F$ is **of Fourier-Mukai type**.

## Properties

The key fact is as follows

+-- {: .num_thm}
###### Theorem ([[Orlov]])
Let $X$ and $Y$ be smooth projective [[varieties]] over a [[field]] $K$.  Let $F : D(X) \to D(Y)$ be a [[triangulated functor|triangulated]] [[fully faithful functor]].  Then $F$ is represented by some object $E \in D(X \times Y)$ which is unique up to isomorphism.
=--

See [Orlov 2003, 3.2.1](#OrlovSurvey) for a proof.  Though the theorem is stated there for $F$ admitting a [[right adjoint]], it follows from [Bondal-van den Bergh 2002](#BondalBergh2002) that every [[triangulated functor|triangulated]] [[fully faithful functor]] admits a [[right adjoint]] automatically.

It is generally believed that this theorem should be true for _all_ [[triangulated functors]].

On the level of the [[DG enhancements]], it is true for all smooth proper $K$-[[schemes]] that, in the [[homotopy category]] of [[DG categories]], _every_ functor corresponds bijectively to an isomorphism class of objects on $D(X \times Y)$.  See [(Toen 2006)](#Toen2006).

=--

## See also

* [[triangulated categories of sheaves]]

## References

* [[Dmitri Orlov]], _Derived categories of coherent sheaves and equivalences between them_, Russian Math. Surveys, 58 (2003), 3, 89-172, [translation](http://www.mi.ras.ru/~orlov/papers/Uspekhi2003.pdf).
 {#OrlovSurvey}

* Lutz Hille, Michel van den Bergh, _Fourier-Mukai transforms_ ([arXiv](http://arxiv.org/abs/math/0402043))

* [[Bertrand Toen]], _The homotopy theory of dg-categories and derived Morita theory_, 2006, [arXiv](http://arxiv.org/abs/math/0408337).

* [[Alexei Bondal]], [[Michel van den Bergh]].  _Generators and representability of functors in commutative and noncommutative geometry_, 2002, [arXiv](http://arxiv.org/abs/math/0204218)
 {#BondalBergh2002}

[[!redirects Fourier-Mukai transforms]]
[[!redirects Fourier-Mukai functor]]
[[!redirects Fourier-Mukai functors]]