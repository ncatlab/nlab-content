
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Differential geometry
+-- {: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_Differential calculus_ is one of the two halves of the [[infinitesimal]] [[calculus]], the other being [[integral calculus]].  (The two are linked by the [[fundamental theorem of calculus]].)  The differential calculus was developed in the 18th century by [[Isaac Newton]] and [[Gottfried Leibniz]] (acting independently).

In modern terms, the original differential calculus describes the behaviour of [[differentiation]] of [[smooth function|function]]s on the [[real line]].  From here, we move to the study of [[differential equation]]s and then to [[differential geometry]] ([[de Rham complex]]) and eventually generalize to a wide class of analogous situations (see for instance [[synthetic differential geometry]] and [[D-modules]]).

Differential calculus on non-finite dimensional spaces is also known as [[variational calculus]].

In the presence of [[Lie algebra]] [[actions]] a variant of differential caclulus is [[Cartan calculus]].

Since [[Hochschild homology]] and [[cyclic homology]] (see there) is closely related to differential forms and de Rham differentials, generalizations and abstractions of Hochschild (co)homology are also used as generalized _differential calculi_ .

## In cohesive homotopy theory
 {#InCohesiveHomotopyTheory}

We list how aspects of differential calculus are captured by the [[axioms]] of [[cohesion]] and [[differential cohesion]].

With the [[axioms]] of [[cohesion]] one may characterize the [[line object]] $\mathbb{A}^1 = \mathbb{R}^1$ (by the fact that its [[A1-homotopy theory|A1-homotopy localization]] is the [[localization]] [[modality]] which is exhibited by the given [[shape modality]]) and then one may essentially characterize a [[function]] 

$$
  \mathbf{d} \;\colon\; \mathbb{R} \longrightarrow \mathbf{\Omega}^1_{cl}
$$

which is the "[[universal characteristic class|universal]] [[de Rham differential]]". For any [[function]] $f \;\colon\; X \longrightarrow \mathbb{R}$, the [[composition|composite]]

$$
  \mathbf{d}f \;\colon\; X \stackrel{f}{\longrightarrow} \mathbb{R} \stackrel{\mathbf{d}}{\longrightarrow} \mathbf{\Omega}^1_{cl}
$$

is interpreted as the [[de Rham differential]] of $f$. This is discussed in some detail at _[[geometry of physics]]_ in the section _[4. Differentiation](http://ncatlab.org/nlab/show/geometry+of+physics#Differentiation)_.

A slight variant of this construction, using [[pullbacks]] of [[flat modality|flat modal]] [[types]] yields [[variational calculus]]. See there the section _[In terms of smooth spaces](http://ncatlab.org/nlab/show/variational+calculus#InTermsOfSmoothSpaces)_.

With the stronger [[axioms]] of [[differential cohesion]] one may similarly ask for the [[infinitesimal interval]] $D \hookrightarrow \mathbb{R}$. With this one can proceeed as in [[synthetic differential geometry]] and formulate for instance [[differential equations]] synthetically, as discussed there in the section _[In terms of synthetic differential geometry](http://ncatlab.org/nlab/show/differential+equation#InSynthDiff)_.

Moreover, [[differential cohesion]] induces [[de Rham spaces]] and hence the geometry in the [[slice (infinity,1)-topos|slice]] over them, [[dependent types]] over the [[infinitesimal shape modality]]. This is _[[D-geometry]]_ which is a general way of talking about [[differential equations]].

## Related concepts

* [[noncommutative differential calculus]]

* [[secondary calculus]]

* [[(∞,1)-category theory|((∞,1)-]][[categorification]]: [[Goodwillie calculus]]

## References

Discussion of differential calculus in terms of [[coinduction]] is in 

* [[Martín Escardó]], [[Duško Pavlović]], _Calculus in coinductive form_ (1998) ([pdf](http://www.isg.rhul.ac.uk/dusko/papers/1998-lapl-LICS.pdf))


[[!redirects differential calculus]]