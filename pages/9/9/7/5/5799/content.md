
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

> under construction

#Contents#
* table of contents
{:toc}

## Definition

Let $C_{et}$ be the [[etale site]] of complex [[scheme]]s of finite type. For $X$ a [[scheme]], its **infinitesimal site** $Cris(X)$ is the [[big site]] $C_{et}/X_{dR}$ of the [[de Rham space]] $X_{dR} : C_{et} \to Set$:

the site whose objects are pairs $(Spec A, (Spec A)_{red} \to X)$ of an affine $Spec A$ and a morphism from its reduced part ($(Spec A)_{red} = Spec (A/I)$ for $I$ the [[nilradical]] of $A$) into $X$.

More generally, for positive [[characteristic]], the definition is more involved than that.

## Properties

The [[abelian sheaf cohomology]] over $Cris(X)$ is the [[crystalline cohomology]] of $X$.

## Related concepts

* [[crystalline cohomology]]

* [[crystalline differential operator]]

## References

An original account of the definition of the crystalline topos is [section 7, page 299](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf#page=299) of

* [[Alexander Grothendieck]], _Crystals and de Rham cohomology of schemes_ , chapter IX in _Dix Exposes sur la cohomologie des schema_ ([pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf))

A review of some aspects is in

* [[Jacob Lurie]], Notes on [[crystal|Crystals]] and algebraic D-modules ([pdf](http://www.math.harvard.edu/~gaitsgde/grad_2009/SeminarNotes/Nov17-19%28Crystals%29.pdf))

and on page 7 of

* [[Carlos Simpson]], [[Constantin Teleman]], _deRham theorem for $\infty$-stacks_ ([pdf](http://math.berkeley.edu/~teleman/math/simpson.pdf))

In the article 

* Arthur Ogus, _Cohomology of the infinitesimal site_ Annales scientifiques de l'&#201;cole Normale Sup&#233;rieure, S&#233;r. 4, 8 no. 3 (1975), p. 295-318 ([numdam](http://www.numdam.org/item?id=ASENS_1975_4_8_3_295_0))

it is shown that if $X$ is proper over an algebraically closed field $k$ of [[characteristic]] $p$, and embeds into a smooth scheme over $k$, then the infinitesimal cohomology of $X$ coincides with [[etale cohomology]] with coefficients in $k$  (or more generally $W_n(k)$ if we work with the infinitesimal site of $X$ over $W_n(k)$). 

[[!redirects infinitesimal site]]
[[!redirects crystaline site]]
