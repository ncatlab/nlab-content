
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Classically in [[complex geometry]], an _elliptic curve_ is a connected [[Riemann surface]] (a connected compact 1-dimensional [[complex manifold]]) of [[genus of a surface|genus]] 1, hence it is a [[torus]] equipped with the structure of a [[complex manifold]], or equivalently with [[conformal structure]]. 

The curious term "elliptic" is a remnant from the 19th century, a back-formation which refers to [[elliptic functions]] (generalizing circular functions, i.e., the classical trigonometric functions) and their natural domains as Riemann surfaces. 

In more modern frameworks and in the generality of [[algebraic geometry]], an elliptic curve over a [[field]] $k$ or indeed over any [[commutative ring]] may be defined as a complete irreducible non-singular [[algebraic curve]] of [[arithmetic genus]]-1 over $k$, or even as a certain type of algebraic [[group scheme]]. 

Elliptic curves have many remarkable properties, and their deeper arithmetic study is one of the most profound subjects in present-day mathematics. 

The [[moduli stack of elliptic curves]] equipped with its canonical map to the [[moduli stack of formal group laws]] plays a central role in [[chromatic homotopy theory]] at [[chromatic level]] 2, where it serves to parameterize [[elliptic cohomology theories]].

Elliptic curves over the complex numbers are also interpreted as those [[worldsheets]] in [[string theory]] whose [[correlators]] are the [[superstring]]'s [[partition function]], which is the [[Witten genus]]. Via the [[string orientation of tmf]] this connects to to the role of elliptic curves in [[elliptic cohomology theory]].


## Definition 

### Over a general ring
 {#DefinitionOverGeneralRing}

Elliptic curves over a general [[commutative ring]] $R$ (hence in [[arithmetic geometry]]) are the well-behaved 1-dimensional [[group objects]] parameterized over the [[space]] $Spec(R)$ (the [[prime spectrum of a commutative ring|prime spectrum]] of $R$). (Notice the count of dimension: over the complex numbers a torus is complex 1-dimensional and in this sense one is looking at 1-dimensional group schemes here.) This we discuss below in 

* [Conceptual definition](#OverGeneralRingConceptualDefinition)

More concretely there are various explicit and standard [[coordinates|coordinazations]] of elliptic curves as [[affine schemes]], hence as solution spaces to [[polynomial]] [[equations]]. This we discuss below in 

* [Coordinatized as solutions to cubic equations](#OverGeneralRingAsSolutionsToEquations)


#### Conceptual definition
 {#OverGeneralRingConceptualDefinition}

\begin{defn} \label{DefinitionEllipticCurve} {#EllipticCurve}

An **elliptic curve** over a  [[commutative ring]] $R$ is a [[group scheme]] (a [[group object]] in the [[category]] of [[schemes]]) over $Spec(R)$ that is a relative 1-dimensional, [[smooth scheme|smooth]], [[proper scheme|proper]] curve over $R$. 

\end{defn} 

+-- {: .num_remark}
###### Remark

This implies that an elliptic curve has [[arithmetic genus]] $1$ (by a direct argument concerning the [[Chern class]] of the [[tangent bundle]].)

=--

+-- {: .num_defn}
###### Definition

An elliptic curve over a [[field]] of [[positive characteristic]] whose [[formal group law]] has [[height of a formal group|height]] equal to 2 is called a _[[supersingular elliptic curve]]_. Otherwise the height equals 1 and the elliptic curve is called _ordinary_.

=--

#### Coordinatized as solutions to cubic Weierstrass equations
 {#OverGeneralRingAsSolutionsToEquations}

Elliptic curves are examples of solutions to [[Diophantine equations]] of degree 3. We start by giving the equation valued over general rings, which is fairly complicated compared to the special case that it reduces to in the classical case over the [[complex numbers]]. The more elements in the ground ring are invertible, the more the equation may be simplified.

(See [Silverman 09, III.1](#Silverman09) for a textbook account and for instance ([QuickIntro](#QuickIntro)) for a quick survey.)

##### Weierstrass cubic, discriminant and $j$-invariant
 {#WeierstrassCubicDiscriminantAndJInvariant}

+-- {: .num_defn #GeneralWeierstrassCubic}
###### Definition

Let $R$ be a [[commutative ring]], then [[Zariski topology|Zariski locally]] over $Spec(R)$ a [[cubic curve]] is a solution in the corresponding [[projective space]] to an [[equation]] of the form

$$
  y^2 + a_1 x y + a_3 y = x^3 + a_2 x^2 + a_4 x + a_6
$$

for [[coefficients]] $a_1, a_2, a_3, a_4, a_6$.  This is called the _[[Weierstrass equation]]_. 

=--

+-- {: .num_remark}
###### Remark

Much of the literature on elliptic curves considers def. \ref{GeneralWeierstrassCubic} for the case that $R$ is an [[algebraically closed field]], in which case there is no need to pass to a cover. But for the true global discussion necessary for the [[moduli stack of elliptic curves]] one needs the full generality.

=--


The [[non-singular algebraic variety|non-singular]] such solutions are the elliptic curves over $R$. Non-singularity is embodied in coordinates  as follows.

+-- {: .num_defn #DiscriminantAndJInvariant}
###### Definition

Let

$$
  \begin{aligned}
    b_2 & \coloneqq a_1^2 + 4 a_2
    \\
    b_4 &\coloneqq a_1 a_3 + 2a_4
    \\
    b_6 & \coloneqq a_3^2 + 4 a_6
    \\
    b_8 & \coloneqq a_1^2 a_6 - a_1 a_3 a_4 + a_2 a_3^2 + 4 a_2 a_6 - a_4^2
  \end{aligned}
$$

and in terms of these

$$
  \begin{aligned}
     c_4 & \coloneqq b_2^2 - 24 b_4
     \\
     c_6 & \coloneqq - b_2^3 + 36 b_2 b_4 - 216 b_6
     \\
     \Delta &\coloneqq - b_2^2 b_8 - 8 b_4^3 - 27 b_6^2 + 9 b_2 b_4 b_6
  \end{aligned}
  \,.
$$

Here $\Delta$ is called the **[[discriminant]]**.  

Finally let

$$
  j \coloneqq c_4^3/\Delta
  \,,
$$

called the **[[j-invariant]]**.

=--

+-- {: .num_remark #RelationBetweenDiscriminantAndTheModularInvariants}
###### Remark

In def. \ref{DiscriminantAndJInvariant} the discriminant satisfies the relation

$$
  1728 \Delta = c_4^3 - c_6^2
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Over $R = \mathbb{C}$ the [[complex numbers]] the quantities $c_4$ and $c_6$ in def. \ref{DiscriminantAndJInvariant} are proportional to the [[modular forms]] called the [[Eisenstein series]] (see there)  $G_4$ and $G_6$.

=--

##### Elliptic curves, Nodal curves, Cuspidal curves
 {#EllipticCurvesNodalCurvesCuspidalCurves}

The following is a definition if one takes the coordinate-description as fundamental. If one takes the more abstract characterization of def. \ref{EllipticCurve} as fundamental then the following is a proposition.

+-- {: .num_defn}
###### Definition/Proposition

A solution to the Weierstrass cubic, def. \ref{GeneralWeierstrassCubic}, with modular invariants $c_4$, $c_6$ and discriminant $\Delta$ according to def. \ref{DiscriminantAndJInvariant} is

1. an _elliptic curve_ iff $\Delta \neq 0$;

1. a _[[nodal curve]]_ or _[[cubic curve]] with nodal [[singular point of an algebraic variety|singularity]]_  iff $\Delta = 0$ and $c_4 \neq 0$;

1. a _[[cuspidal curve]]_ or _[[cubic curve]] with [[cusp]] [[singular point of an algebraic variety|singularity]]_  iff $\Delta = 0$ and $c_4 = 0$ (which by remark \ref{RelationBetweenDiscriminantAndTheModularInvariants} is equivalent to $c_4 = 0$ and $c_6 = 0$)

=--

+-- {: .num_remark}
###### Remark

Adding the nodal curve to the [[moduli stack of elliptic curves]] yields its [[compactification]], and the [[formal neighbourhood]] of the nodal curve in that compactification is known as the _[[Tate curve]]_.

=--

##### Localization at 2 and 3

+-- {: .num_prop #WeierstrassEquationLocalAt2And3}
###### Proposition

If $2$ is invertible in $R$ (is a [[unit]] ), and hence generally over the [[localization of a ring|localization]] $R[\frac{1}{2}]$ of $R$ at 2, the general [[Weierstrass equation]], def. \ref{GeneralWeierstrassCubic}, is equivalent, to the equation

$$
  y^2  = 4 x^3  + b_2 x^2 + 2 b_4 x + b_6
$$

with the [[coefficients]] identified as in def. \ref{DiscriminantAndJInvariant}.

If moreover $3$ is also invertible in $R$, hence generally over $R[\frac{1}{2}, \frac{1}{3}]$ then this equation is equivalent to just

$$
  y^2 = x^3 - 27 c_4 x - 54 c_6
 \,.
$$

=--


### Over the complex numbers
 {#OverTheComplexNumbers}


#### In terms of algebraic geometry

+-- {: .num_remark}
###### Remark

If the [[ring]] $R= \mathbb{C}$ is the [[complex numbers]], then complex tori are indeed the solutions to the [[Weierstrass equation]] as in prop. \ref{WeierstrassEquationLocalAt2And3},  parameterized by a [[torus]] $z \in \mathbb{C}/\Lambda$ (as discussed in the section [in terms of complex geometry](#InTermsOfCpomplexGeometry)) via the [[Weierstrass elliptic function]] $\wp$ as
$(x = \wp(z), y = \wp'(z), )$ in the form

$$
  \wp'(z)^2 + 4 \wp(z)^3 - g_2 p(z) - g_3
  \,.
$$

=--

See e.g. ([Hain 08, section 5](#Hain08)) on how complex elliptic curves are expressed in this algebraic geometric fashion.


#### In terms of complex geometry
 {#InTermsOfCpomplexGeometry}


+-- {: .num_prop #CharacterizationOverC}
###### Proposition

An [[elliptic curve]], def. \ref{EllipticCurve}, over the [[complex numbers]] $\mathbb{C}$ is equivalently

* a [[Riemann surface]] $X$ of [[genus]] 1 with a base point $P \in X$ (e.g.[Hain 08, def. 1.1](#Hain08))

* a quotient $\mathbb{C}/\Lambda$ where $\Lambda$ is a [[lattice]] in $\mathbb{C}$;

* a compact complex [[Lie group]] of dimension 1.

* a [[smooth scheme|smooth]] [[algebraic curve]] of degree 3 in $\mathcal{P}$.

=--

+-- {: .num_remark}
###### Remark

From the second definition it follows that to study the 
[[moduli space of elliptic curves]] it suffices to study the [[moduli space]] of [[lattices]] in $\mathbb{C}$.

=--

+-- {: .num_defn}
###### Definition

A **[[framed elliptic curve]]** is an elliptic curve $(X,P)$ in the sense of the first item in prop. \ref{CharacterizationOverC}, together with an [[ordering|ordered]] [[basis]] $(a,b)$ of $H_1(X, \mathbb{Z})$ with $(a \cdot b) = 1 $

For $n$ a natural number, a **[[level n-structure on an elliptic curve]]** over the complex numbers is similar data but with [[coefficients]] only in the [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$.

A **framed lattice** in $\mathbb{C}$ is a lattice $\Lambda$ together with an ordered basis $(\lambda_1, \lambda_2)$ of $\Lambda$ such that $Im(\lambda_2/\lambda_1) \gt 0$.


=--

Hence a framed elliptic curve is the quotient of the complex plane by a lattice _together_ with the information on how this quotient was obtained. This is useful for describing the [[moduli stack of elliptic curves]] over the complex numbers.


### Over the rational numbers
 {#OverTheRationalNumbers}

Over the [[rational numbers]]: [Sagemath: Elliptic curves over the rational numbers](http://www.sagemath.org/doc/reference/plane_curves/sage/schemes/elliptic_curves/ell_rational_field.html)

### Over the $p$-adic integers and $p$-adic numbers
 {#OverpAdics}

Over the [[p-adic integers]], see ([Conrad 07](#Conrad07)).

Over the [[p-adic numbers]], see ([Winter 11](#Winter11)).

## Level structures

In the case over the [[complex numbers]] an elliptic curve $\Sigma$ is equivalently the [[quotient]] of the [[complex plane]] by a framed [[lattice]]. If here one remembers the structure given by that framed lattice, this means equivalently to remember an ordered basis

$$
  (a_1, a_2)\in H_1(\Sigma, \mathbb{Z})
$$

of the [[ordinary homology]] group of $\Sigma$ with [[coefficients]] in the [[integers]].

If here one replaces the integers by a [[cyclic group]] $\mathbb{Z}/n\mathbb{Z}$ then one obtains what is called a
_[[level structure on an elliptic curve|level-n structure on an elliptic curve]]_. Level-$n$ structures on elliptic curves may also be defined over general rings. 

These structures are useful in that the [[moduli stack]] of [[elliptic curves with level-n structure]] (a _[[modular curve]]_ in the case over the complex numbers) provides a finite [[covering]] of the full [[moduli stack of elliptic curves]].

## Group structure

A vital reason for the importance of elliptic curves in number theory, arithmetic geometry, and elsewhere is their group structure. This group structure is present by fiat in Definition \ref{DefinitionEllipticCurve}, and can be constructed given a Weierstrass equation. 

The [[torsion element|torsion elements]] of this group structure when the elliptic curve is defined over a [[number field]] have good Galois-theoretic properties. See [[torsion points of an elliptic curve]] for more.

## Constructions

### Formal group law 

Given an [[elliptic curve]] over $R$, $E \to Spec R$, we get a [[formal group]] $\hat E$ by completing $E$ along its identity [[section]] $\sigma_0$

$$
  E \to Spec(R) \stackrel{\sigma_0}{\to} E
  \,,
$$

we get a [[ringed space]] $(\hat E, \hat O_{E,0})$


+-- {: .num_example}
###### Example


If $R$ is a [[field]] $k$, then the [[structure sheaf]] $\hat O_{E,0} \simeq k[ [z] ]$

then 

$$
  \hat O_{E \times E, (0,0)} \simeq
  \hat O_{E,0}
  \hat \otimes_k
  \hat O_{E,0}
  \simeq 
  k[[x,y]]
$$

=--

+-- {: .num_example}
###### Example

**(Jacobi quartics)**

$$
  y^2 = 1- 2 \delta x^2 + \epsilon x^4
$$

defines $E$ over $R = \mathbb{Z}[Y_Z,\epsilon, \delta]$.

The corresponding [[formal group law]] is **Euler's formal group law**

\[
  \label{EulerFormalGroupLaw}
  f(x,y) 
    \;=\; 
  \frac{
x{\sqrt{1- 2 \delta y^2 + \epsilon y^4}} + y{\sqrt{1- 2 \delta x^2 + \epsilon x^4}}
  }
  {1- \epsilon x^2 y^2}
\]

if $\Delta \coloneqq \epsilon(\delta^2 - \epsilon)^2 \neq 0$ then this is a non-trivial elliptic curve.

=--

If $\Delta = 0$ then $f(x,y) \simeq G_m, G_a$ ([[additive group|additive]] or [[multiplicative group|multiplicative]] formal group law corresponding to [[ordinary cohomology]] and [[topological K-theory]] [[KU]], respectively).

### Elliptic cohomology 

Elliptic curves, via their [[formal group law]]s, give the name to [[elliptic cohomology]] theories.

See also

* [[A Survey of Elliptic Cohomology - formal groups and cohomology]]

## Related concepts

* [[abelian variety]]

* [[Tate curve]]

* [[Szpiro's conjecture]]

* [[cubic curve]]

* [[moduli stack of elliptic curves]]

  * [[modular form]], [[Jacobi form]]

  * [[topological modular form]]

* [[modularity theorem]]

* [[elliptic fibration]]

* [[elliptic cohomology]], [[tmf]]


## References

Classical accounts of the general case:

* [[Pierre Deligne]], [[Michael Rapoport]], _Les Schémas de Modules de Courbes Elliptiques_ In: Deligne P., Kuijk W. (eds) _Modular Functions of One Variable II_, Lecture Notes in Mathematics, vol 349. Springer (1973) ([doi:10.1007/978-3-540-37855-6_4](https://doi.org/10.1007/978-3-540-37855-6_4))
 
* [[Pierre Deligne]], _Courbes Elliptiques: Formulaire (d'apres J. Tate)_ ([web](http://modular.math.washington.edu/Tables/antwerp/deligne/))

* [[Nicholas Katz]], [[Barry Mazur]], _Arithmetic moduli of elliptic curves, Annals of Mathematics Studies_ **108** Princeton University Press (1985) &lbrack;[jstor:j.ctt1b9s05p](https://www.jstor.org/stable/j.ctt1b9s05p)&rbrack;

* [[Joachim Wehler]]: *Modular Forms and Elliptic Curves* (2021) &lbrack;[pdf](https://www.mathematik.uni-muenchen.de/~wehler/ModularFormsScript.pdf)&rbrack;


Introductory lecture notes for elliptic curves over the complex numbers:

* {#Hain08} Richard Hain, _Lectures on Moduli Spaces of Elliptic Curves_ ([arXiv:0812.1803](http://arxiv.org/abs/0812.1803))

* {#Neeman07} [[Amnon Neeman]], section 1.2 of _Algebraic and analytic geometry_, London Math. Soc. Lec. Note Series __345__, 2007 ([publisher](http://www.cambridge.org/us/academic/subjects/mathematics/geometry-and-topology/algebraic-and-analytic-geometry))

and for the general case:

* {#QuickIntro} _A quick introduction to elliptic curves_ ([pdf](http://people.reed.edu/~jerry/311/ecintro.pdf))

* R. Sujatha, _Elliptic Curves & Number Theory_ ([[SujahtaElliptic.pdf:file]])

* {#Sutherland21} [[Andrew Sutherland]], _Elliptic curves_, 2021 ([web](https://ocw.mit.edu/courses/18-783-elliptic-curves-spring-2021/))

See also

* {#AndoHopkinsStrickland01} [[Matthew Ando]], [[Michael Hopkins]], [[Neil Strickland]], appendix B of: _Elliptic spectra, the Witten genus, and the theorem of the cube_, Inventiones Mathematicae, 146:595&#8211;687, 2001,  ([pdf](http://www.math.rochester.edu/people/faculty/doug/otherpapers/musix.pdf), [doi:10.1007/s002220100175](https://doi.org/10.1007/s002220100175))

  (review of general elliptic curves in the context of [[elliptic genera]], [[elliptic spectra]] and the [[string orientation of tmf]])

Discussion of the [[formal group law]] of elliptic curves:

* Antonia W. Bluher, _Formal groups, elliptic curves, and some theorems of Couveignes_, in: J.P. Buhler (eds.) _Algorithmic Number Theory_ ANTS 1998. Lecture Notes in Computer Science, vol 1423. Springer 1998 ([arXiv:math/9708215](https://arxiv.org/abs/math/9708215), [doi:10.1007/BFb0054887]( https://doi.org/10.1007/BFb0054887))


* {#Friedl17} Stefan Friedl, _An elementary proof of the group law for elliptic curves_ ([arXiv:1710.00214](https://arxiv.org/abs/1710.00214))

For more along these lines see also at _[[arithmetic geometry]]_.



In the context of [[elliptic fibrations]]:

* [[Rick Miranda]], _The basic theory of elliptic surfaces_, lecture notes 1988 ([pdf](http://www.math.colostate.edu/~miranda/BTES-Miranda.pdf))

A general textbook account is

* {#Silverman09} [[Joseph Silverman]], _The arithmetic of elliptic curves_, second ed., Graduate Texts in Mathematics, vol. 106, Springer, Dordrecht, 2009. MR 2514094 (2010i:11005)

Discussion over the [[rational numbers]] includes

* Sagemath _[Elliptic curves over the rational numbers](http://www.sagemath.org/doc/reference/plane_curves/sage/schemes/elliptic_curves/ell_rational_field.html)_

Discussion of elliptic curves over the [[p-adic numbers]] includes

* {#Conrad07} [[Brian Conrad]]: *Arithmetic moduli of generalized elliptic curves*, J. Inst. Math. Jussieu **6** 2 (2007) 209-278 &lbrack;[doi:10.1017/S1474748006000089](https://doi.org/10.1017/S1474748006000089), [pdf](http://math.stanford.edu/~conrad/papers/kmpaper.pdf)&rbrack;

* {#Winter11} Rosa Winter, _Elliptic curves over $\mathbb{Q}_p$_, 2011 ([pdf](http://www.math.leidenuniv.nl/scripties/BachWinter.pdf))



See also

* _[[A Survey of Elliptic Cohomology - elliptic curves]]_


[[!redirects elliptic curves]]