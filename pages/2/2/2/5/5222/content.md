
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

### General

The original article:

* {#Mukai81} [[Shigeru Mukai]]: _Duality between $D(X)$ and $D(\hat X)$ with its application to Picard sheaves_, Nagoya Mathematical Journal **81** (1981) 153-175 &lbrack;[doi:10.1017/S002776300001922X](https://doi.org/10.1017/S002776300001922X)&rbrack;

Further discussion:

* {#BondalBergh2002} [[Alexei Bondal]], [[Michel van den Bergh]].  _Generators and representability of functors in commutative and noncommutative geometry_, 2002, [arXiv](http://arxiv.org/abs/math/0204218)

* {#OrlovSurvey} [[Dmitri Orlov]], _Derived categories of coherent sheaves and equivalences between them_, Russian Math. Surveys, 58 (2003), 3, 89-172, [translation](http://www.mi.ras.ru/~orlov/papers/Uspekhi2003.pdf).

*  Lutz Hille, Michel van den Bergh, _Fourier-Mukai transforms_ ([arXiv:0402043](http://arxiv.org/abs/math/0402043))
 

* {#Huybrechts08} [[Daniel Huybrechts]], _Fourier-Mukai transforms_ (2008) &lbrack;[pdf](http://www.math.uni-bonn.de/people/huybrech/Garda2.pdf), [[Huybrechts-FourierMukai.pdf:file]]&rbrack;

* Claudio Bartocci, [[Ugo Bruzzo]], Daniel Hernandez Ruiperez: *Fourier-Mukai and Nahm transforms in geometry and mathematical physics*, Progress in Mathematics **276**, Birkhäuser (2009) &lbrack;[doi:10.1007/b11801](https://doi.org/10.1007/b11801)&rbrack;

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


### For T-duality
 {#ReferencesForTDuality}

Discussion of the effect of [[T-duality]] on [[RR-field]] [[flux densities]] (in [[ordinary cohomology]] or in [[topological K-theory]]) as a Fourier-Mukai-like transform goes back to:

* [[Kentaro Hori]], [[Yaron Oz]], Section 3.1 of: *F-Theory, T-Duality on K3 Surfaces and $N=2$ Supersymmetric Gauge Theories in Four Dimensions*, Nucl. Phys. B **501** (1997) 97-108 &lbrack;[arXiv:hep-th/9702173](https://arxiv.org/abs/hep-th/9702173), <a href="https://doi.org/10.1016/S0550-3213(97)00361-1">doi:10.1016/S0550-3213(97)00361-1</a>&rbrack;

* [[Kentaro Hori]]: (1.1) and pp. 13 of: *D-branes, T-duality, and Index Theory*, Adv. Theor. Math. Phys. **3** 2 (1999) 281-342 &lbrack;[arXiv:hep-th/9902102](https://arxiv.org/abs/hep-th/9902102), [doi:10.4310/ATMP.1999.v3.n2.a5](https://dx.doi.org/10.4310/ATMP.1999.v3.n2.a5),  journal:[pdf](https://www.intlpress.com/site/pub/files/_fulltext/journals/atmp/1999/0003/0002/ATMP-1999-0003-0002-a005.pdf)&rbrack;
  > (whence "Hori's formula")

with explicit formulation in the context if [[topological T-duality]]:

* {#BouwknegtEvslinMathai04} [[Peter Bouwknegt]], [[Jarah Evslin]], [[Varghese Mathai]], (1.9) in: _T-Duality: Topology Change from H-flux_, Commun. Math. Phys. **249** (2004) 383-415 &lbrack;[hep-th/0306062](http://arxiv.org/abs/hep-th/0306062), [doi:10.1007/s00220-004-1115-6](https://doi.org/10.1007/s00220-004-1115-6)&rbrack; 


Survery and Review:

* Martin Ruderer, *Fourier-Mukai Transforms from T-Duality*, PhD thesis, Regensburg (2015)  &lbrack;[urn:nbn:de:bvb:355-epub-314033](https://nbn-resolving.org//urn:nbn:de:bvb:355-epub-314033), [pdf](https://epub.uni-regensburg.de/31403/6/final.pdf)&rbrack;

* Bjorn Andreas, Daniel Hernandez Ruiperez: *Fourier Mukai Transforms and Applications to String Theory*, Rev. R. Acad. Cienc. Exactas Fis. Nat. Ser. A Mat **99** 1 (2005) 29-77 &lbrack;[arXiv:math/0412328](https://arxiv.org/abs/math/0412328), [spire:667425](https://inspirehep.net/literature/667425), journal: [pdf](https://mat.usal.es/ruiperez/Site/Papers_files/4_ANDREAS.PDF)&rbrack;

For [[non-abelian T-duality]]:

* Eva Gevorgyan, [[Gor Sarkissian]]: *Defects, Non-abelian T-duality, and the Fourier-Mukai transform of the Ramond-Ramond fields*,  J. High Energ. Phys. **2014** 35 (2014) \[<a href="https://doi.org/10.1007/JHEP03(2014)035">doi:10.1007/JHEP03(2014)035</a>, [arXiv:1310.1264](https://arxiv.org/abs/1310.1264)\]


On [[superspace]]:

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]]: Prop. 6.4 in: *[[schreiber:T-Duality from super Lie n-algebra cocycles for super p-branes]]*, Adv. Theor. Math. Phys **22** 5 (2018) &lbrack;[arXiv:1611.06536](https://arxiv.org/abs/1611.06536), [doi:10.4310/ATMP.2018.v22.n5.a3](https://dx.doi.org/10.4310/ATMP.2018.v22.n5.a3)&rbrack;


For [[spherical T-duality]]:

* [[Peter Bouwknegt]], [[Jarah Evslin]], [[Varghese Mathai]]: *Spherical T-duality and the spherical Fourier–Mukai transform*, Journal of Geometry and Physics **133** (2018) 303-314 &lbrack;[doi:10.1016/j.geomphys.2018.07.020](https://doi.org/10.1016/j.geomphys.2018.07.020), [arXiv:1502.04444](https://arxiv.org/abs/1502.04444)&rbrack;







[[!redirects Fourier-Mukai transforms]]
[[!redirects Fourier-Mukai functor]]
[[!redirects Fourier-Mukai functors]]
[[!redirects Fourier-Mukai transformation]]