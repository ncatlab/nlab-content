
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Given a [[multiplicative cohomology theory]], hence an [[E-∞ ring]] $E$, equipped with a multiplicative universal [[orientation in generalized cohomology|orientation]] for manifolds with [[G-structure]], hence a [[homomorphism]] of $E_\infty$-rings $M G \longrightarrow E$ from the $G$-[[Thom spectrum]] $M G$, then $E$ canonically becomes an $M G$-[[∞-module]] and so one may consider the functor

$$
  X \mapsto M G_\bullet(X) \otimes_{M G_\bullet} E_\bullet
  \,.
$$ 

If this is first of all a [[generalized homology theory]] itself, hence [[Brown representability theorem|represented]] by a [[spectrum]], then one may ask if this spectrum coincides with the original $E$, hence if there is an [[natural equivalence]]


$$
  M G_\bullet(-) \otimes_{M G_\bullet} E_\bullet \simeq E_\bullet(-)
  \,.
$$

If so one often says that _the cobordism theory determines the homology theory_ (e.g. [Hopkins-Hovey 92](#HopkinsHovey92)). 

## Examples

Originally this was shown to be the case by ([Conner-Floyd 66](#ConnerFloyd66)) for $E= $[[KU]] with its canonical [[complex oriented cohomology theory|complex orientation]] $MU \to KU$ (they also showed the case for [[KO]] with $M Sp \to KO$). Later the [[Landweber exact functor theorem]] ([Landweber 76](#Landweber76)) generalized this to all [[complex oriented cohomology theories]] $M U \to E$. 

The generalization to the actual [[Atiyah-Bott-Shapiro orientations]] of [[topological K-theory]], namely $M Spin^c \to KU$ and $M Spin \to KO$ is due to ([Hopkins-Hovey 92](#HopkinsHovey92)). 

For [[elliptic cohomology]] with the [[SO orientation of elliptic cohomology]] $M SO \to Ell$ the statement is due to ([Landweber-Ravenel-Stong 93](#LandweberRavenelStong93)). For the refinement to the [[spin orientation of elliptic cohomology]] of ([Kreck-Stolz 93](#KreckStolz93)) a statement is due to ([Hovey 95](#Hovey95)).


## Refereces

* {#ConnerFloyd66} [[Pierre Conner]], [[Edwin Floyd]], _The relation of cobordism to K-theories_, Lecture Notes in Mathematics 28, 1966 ([pdf](http://www.maths.ed.ac.uk/~aar/surgery/cf.pdf))

* {#Landweber76} [[Peter Landweber]], _Homological properties of comodules over $MU^\ast(MU)$ and $BP^\ast(BP)$_, American Journal of Mathematics (1976): 591-610.


* {#HopkinsHovey92} [[Michael Hopkins]], [[Mark Hovey]], _Spin cobordism determines real K-theory_, Mathematische Zeitschrift 210.1 (1992): 181-196. ([[HopkinsHoveyCobordismK.pdf:file]])

* {#LandweberRavenelStong93} [[Peter Landweber]], [[Douglas Ravenel]], [[Robert Stong]], _Periodic cohomology theories defined by elliptic curves_, in [[Haynes Miller]] et. al. (eds.), _The Cech centennial: A conference on homotopy theory_, June 1993, AMS (1995) ([pdf](http://www.math.sciences.univ-nantes.fr/~hossein/GdT-Elliptique/Landweber-Ravenel-Stong.pdf))


* {#KreckStolz93} [[Matthias Kreck]], [[Stefan Stolz]], _$HP^2$-bundles and elliptic homology_, Acta Math, 171 (1993) 231-261 ([[KreckStolzElliptic.pdf:file]])

* {#Hovey95} [[Mark Hovey]], _Spin Bordism and Elliptic Homology_, Mathematische Zeitschrift 219, 163-170 1995 ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.53.3277))