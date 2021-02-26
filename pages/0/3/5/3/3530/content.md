
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

**Crystalline cohomology** is the [[abelian sheaf cohomology]] with respect to the _[[crystalline site]]_ of a [[scheme]]. Hence, put more generally, it is the [[cohomology]] of [[de Rham spaces]]/[[coreduced objects]].

Crystalline cohomology serves to refine the notion of [[de Rham cohomology]] for [[schemes]].

Crystalline cohomology is in particular a [[Weil cohomology]] and is generalized by the notion of [[rigid cohomology]].

## Definition

Let $X$ be a [[scheme]] over a base $S$. The **[[crystalline site]]** $Cris(X/S)$ of $X$ is

* the [[category]] whose objects are all nilpotent $S$-immersions $U \hookrightarrow T$, where $U$ is an open set of $X$ and and the ideal on $T$ defining this immersion being endowed with a nilpotent divided power structure (...details...).;

* the [[Grothendieck topology]] on this category is the Zariski topology.

If $S$ is of characteristic 0, then $Cris(X/S)$ coincides with the **infinitesimal site** of $X$. (...details...).

## Properties

### Relation to de Rham space

Crystalline cohomology of $X$ is the [[cohomology]] of the [[de Rham space]]
of $X$. See there for more. 

### Relation to de Rham cohomology

* [[comparison theorem (crystalline cohomology)]]

### Relation to differential homotopy type theory

In [[differential homotopy type theory]] the [[infinitesimal flat modality]]
sends [[coefficients]] to coefficients for crystalline cohomology.

## Related concepts

* [[p-adic cohomology]]

* [[de Rham cohomology]]

* [[Weil cohomology]]

  * [[étale cohomology]]

## References

Related entries: [[crystal]], [[infinitesimal site]], [[rigid cohomology]], [[Dieudonné module]], [[Monsky-Washnitzer cohomology]], [[Grothendieck connection]]

An original account of the definition of the crystalline topos is [section 7, page 299](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf#page=299) of

* [[Alexander Grothendieck]], _Crystals and de Rham cohomology of schemes_ , chapter IX in _Dix Exposes sur la cohomologie des schemas ([pdf](http://www.math.jussieu.fr/~leila/grothendieckcircle/DixExp.pdf))

A more recent account is

* [[Luc Illusie]], _Crystalline cohomology_, in _Motives_, Proc. Sympos. Pure Math., vol. 55, part 1, Amer. Math. Soc. Providence, RI, 1994, 43&#8211;70.


Discussion of this in the modern context of [[higher geometry]]/[[D-geometry]] is in

* {#LurieCrystals} [[Jacob Lurie]], _Notes on Crystals and algebraic D-modules_ ([[LurieCrystals.pdf:file]])



A [[p-adic cohomology]] for [[varieties]] in [[characteristic]] $p$ it was it was discussed in

* [[Pierre Berthelot]], _Cohomologie cristalline des sch&#233;mas de caract&#233;ristique $g \gt 0$, Lecture Notes in Mathematics, Vol. 407, Springer- Verlag, Berlin, 1974. MR 0384804

The [[comparison theorem (crystalline cohomology)]] shown there (theorem V2.3.2) shows that the crystalline cohomology over $\mathbb{Z}/p$ is canonically identified with the [[de Rham cohomology]] of a lift to [[p-adic geometry]] if one exists. See also

* [[Pierre Berthelot]], A. Ogus, _Notes on crystalline cohomology_, Princeton Univ. Press 1978. vi+243, ISBN0-691-08218-9

* [[Pierre Berthelot]], A. Ogus, _$F$-Isocrystals and de Rham Cohomology_, I, Invent. math. 72, 1983, pp. 159-199

Discussion of this in terms of [[Cech cohomology]] is in 

* [[Bhargav Bhatt]], [[Aise Johan de Jong]], _Crystalline cohomology and de Rham cohomology_ ([pdf](http://www.math.columbia.edu/~dejong/papers/crystalline-comparison.pdf))


See also 

* wikipedia [crystalline cohomology](http://en.wikipedia.org/wiki/Crystalline_cohomology)