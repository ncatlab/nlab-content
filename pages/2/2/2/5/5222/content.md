
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _Fourier-Mukai transform_ is a [[categorification|categorified]] [[integral transform]] roughly similar to the standard [[Fourier transform]].

Generally, for $X,Y$ two suitably well-behaved [[schemes]] (e.g. affine, smooth, complex) and with $D(X)$, $D(Y)$ their [[derived categories]] of [[quasicoherent sheaves]], then a _Fourier-Mukai transform_ with [[integral kernel]] $E \in D(X\times Y)$ is a [[functor]] (of [[triangulated categories]]/[[stable (infinity,1)-categories]])

$$
  \Phi \colon D(X)\longrightarrow D(Y)
$$

which is given as the composite of the ([[derived functor|derived]])  operations of 

1. pull ([[inverse image]]) along the [[projection]] $p_X\colon X\times Y \to X$ 

1. [[tensor product]] with $E$;

1. push ([[direct image]]) along the other projection $p_Y \colon X\times Y \to Y$

i.e.

$$
  \Phi(A) \coloneqq (p_Y)_\ast (E\otimes p_X^\ast A)
$$

(where here we implicitly understand all operations as [[derived functors]]). (e.g. [Huybrechts 08, page 4](#Huybrechts08))

Hence this is a pull-tensor-push [[integral transform]] through the product [[correspondence]]

$$
  \array{
    && X \times Y
    \\
    & \swarrow && \searrow
    \\
    X && && Y
  }
$$

with twist $E$ on the correspondence space.

Such concept of [[integral transform]] is rather general and may be considered also in [[derived algebraic geometry]] (e.g. [BenZvi-Nadler-Preygel 13](#BenZviNadlerPreygel13)) and lots of other contexts.

As discussed at _[[integral transforms on sheaves]]_ this kind of [[integral transform]] is a [[categorification]] of an integral transform/[[matrix multiplication]] of functions induced by an [[integral kernel]], the role of which here is played by $E\in D(X \times Y)$.

Indeed, the central kind of result of the theory (theorem \ref{OrlovTheorem}) says that every suitable linear functor $D(X)\to D(Y)$ arises as a Fourier-Mukai transform for some $E$, a statement which is the [[categorification]] of the standard fact from [[linear algebra]] that every [[linear function]] between finite dimensional [[vector spaces]] is represented by a [[matrix]].

The original Fourier-Mukai transform proper is the special case of the above where $X$ is an [[abelian variety]], $Y = X^\vee$ its [[dual abelian variety]] and $E$ is the corresponding [[Poincaré line bundle]].

If $X$ is a [[moduli space of bundles|moduli space of line bundles]] over a suitable [[algebraic curve]], then a slight variant of the Fourier-Mukai transform is the [[geometric Langlands correspondence]] in the abelian case ([Frenkel 05, section 4.4, 4.5](#Frenkel05)).


## Definition

Let $X$ and $Y$ be [[schemes]] over a [[field]] $K$.
Let $E \in D(QCoh(O_{X \times Y}))$ be an object in the [[triangulated categories of sheaves|derived category of quasi-coherent sheaves]] over their [[product]]. (This is a [[correspondence]] between $X$ and $Y$ equipped with a [[chain complex]] $E$ of [[quasi-coherent sheaves]]).

The functor $\Phi(E) : D(QCoh(O_X)) \to D(QCoh(O_Y))$ defined by
  \[ F \mapsto \mathbf{R}q_*(\mathbf{L}p^*(F) \otimes^{\mathbf{L}} E), \]
where $p$ and $q$ are the [[projections]] from $X \times Y$ onto $X$ and $Y$, respectively, is called the **Fourier-Mukai transform of $E$**, or the **Fourier-Mukai functor induced by $E$**.

When $F : D(QCoh(O_X)) \to D(QCoh(O_Y))$ is isomorphic to $\Phi(E)$ for some $E \in D(QCoh(O_{X \times Y}))$, one also says that $F$ is **represented by $E$** or simply that $F$ is **of Fourier-Mukai type**.

## Properties

The key fact is as follows

+-- {: .num_theorem #OrlovTheorem}
###### Theorem ([[Orlov]])

Let $X$ and $Y$ be smooth projective [[varieties]] over a [[field]] $K$.  Let $F : D(X) \to D(Y)$ be a [[triangulated functor|triangulated]] [[fully faithful functor]].  Then $F$ is represented by some object $E \in D(X \times Y)$ which is unique up to isomorphism.

=--

See [Orlov 2003, 3.2.1](#OrlovSurvey) for a proof.  

+-- {: .num_remark}
###### Remark

Though theorem \ref{OrlovTheorem} is stated there for $F$ admitting a [[right adjoint]], it follows from [Bondal-van den Bergh 2002](#BondalBergh2002) that every [[triangulated functor|triangulated]] [[fully faithful functor]] admits a [[right adjoint]] automatically (see e.g. [Huybrechts 08, p. 6](#Huybrechts08)).

=--

+-- {: .num_remark}
###### Remark

It was believed that theorem \ref{OrlovTheorem} should be true for _all_ [[triangulated functors]] (e.g. [Huybrechts 08, p. 5](#Huybrechts08)). However according to [(RVdB 2015)](#RVdB2015) this is not true.

=--

## Enhancements

For any [[quasicompact quasiseparated morphism|quasi-compact quasi-separated]] $k$-schemes $X$ and $Y$ there is a canonical equivalence of [[stable (∞,1)-categories]]

\[
\mathrm{Func}^L(D(X), D(Y)) \simeq D(X \times Y).
\]


## Related concepts

* [[triangulated categories of sheaves]]

* [[Grothendieck duality]]

## References

* {#Mukai81} [[Shigeru Mukai]],  _Duality between $D(X)$ and $D(\hat X)$ with its application to Picard sheaves_. Nagoya Mathematical Journal 81: 153&#8211;175. (1981)

* {#BondalBergh2002} [[Alexei Bondal]], [[Michel van den Bergh]].  _Generators and representability of functors in commutative and noncommutative geometry_, 2002, [arXiv](http://arxiv.org/abs/math/0204218)

* {#OrlovSurvey} [[Dmitri Orlov]], _Derived categories of coherent sheaves and equivalences between them_, Russian Math. Surveys, 58 (2003), 3, 89-172, [translation](http://www.mi.ras.ru/~orlov/papers/Uspekhi2003.pdf).

*  Lutz Hille, Michel van den Bergh, _Fourier-Mukai transforms_ ([arXiv:0402043](http://arxiv.org/abs/math/0402043))
 

* {#Huybrechts08} [[Daniel Huybrechts]], _Fourier-Mukai transforms_, 2008 ([pdf](http://www.math.uni-bonn.de/people/huybrech/Garda2.pdf))

* C. Bartocci, [[Ugo Bruzzo]], D. Hernandez Ruiperez, _Fourier-Mukai and Nahm transforms in geometry and mathematical physics_, Progress in Mathematics 276, Birkhauser 2009.

* {#RVdB2015} Alice Rizzardo, [[Michel Van den Bergh]], _An example of a non-Fourier-Mukai functor between derived categories of coherent sheaves_ 
([arXiv:1410.4039](http://arxiv.org/abs/1410.4039))

* {#Belmans} [[Pieter Belmans]], section 2.2 of _Grothendieck duality: lecture 3_, 2014 ([[BelmansDuality.pdf:file]])

Banerjee and Hudson have defined Fourier-Mukai functors analogously on [[algebraic cobordism]].

* Anandam Banerjee, Thomas Hudson, _Fourier-Mukai transformation on algebraic cobordism_, [pdf](https://sites.google.com/site/anandamb/research/fourier-mukai.pdf?attredirects=0).

Discussion of [[internal homs]] of [[dg-categories]] in terms of refined Fourier-Mukai transforms is in

* [[Bertrand Toën]], _The homotopy theory of dg-categories and derived Morita theory_, Invent. Math. 167 (2007), 615&#8211;667

* Alberto Canonaco, Paolo Stellari, _Internal Homs via extensions of dg functors_ ([arXiv:1312.5619](http://arxiv.org/abs/1312.5619))

Discussion in the context of [[geometric Langlands duality]] is in 

* {#Frenkel05} [[Edward Frenkel]], _Lectures on the Langlands Program and Conformal Field Theory_ ([arXiv:hep-th/0512172](http://arxiv.org/abs/hep-th/0512172))


For a discussion of Fourier-Mukai transforms in the setting of $(\infty,1)$-enhancements, see

* {#BenZviNadlerPreygel13} [[David Ben-Zvi]], [[David Nadler]], Anatoly Preygel.  _Integral transforms for coherent sheaves_,  [arXiv:1312.7164](http://arxiv.org/abs/1312.7164)


[[!redirects Fourier-Mukai transforms]]
[[!redirects Fourier-Mukai functor]]
[[!redirects Fourier-Mukai functors]]
[[!redirects Fourier-Mukai transformation]]