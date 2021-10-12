
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The "fundamental theorem" of [[topos theory]], in the terminology of [McLarty 1992](#McLarty92), asserts that for $\mathcal{T}$ any [[topos]] and $X \,\in\, \mathcal{T}$ any [[object]], also the [[slice category]] $\mathcal{T}_{/X}$ is a topos: the *[[slice topos]]*.

If $\mathcal{T} \,\simeq\, Sh(\mathcal{S})$ is a [[category of sheaves]], hence a [[Grothendieck topos]], then so its its slice: $\mathcal{T}_{/X} \,\simeq\, Sh\big( \mathcal{S}_{/X} \big)$ ([SGA4.1, p. 295](#SGA41)).

The analogous statement holds for [[slice (infinity,1)-category|slice $\infty$-categories]] of [[(infinity,1)-toposes|$\infty$-toposes]]: *[[slice (infinity,1)-toposes|slice $\infty$-toposes]]* ([Lurie 2009, Prop. 6.5.3.1](#Lurie09)).

The archetypical special case is that [[slice categories]] $PSh(\mathcal{S})_{/y(s)}$ of [[categories of presheaves]] over a [[representable functor|representable]] are [[equivalence of categories|equivalently]] categories of presheaves on the slice site $\mathcal{S}_{/s}$. This is exhibited by the [[functor]] which sends a [[bundle]] $E \to y(X)$ [[internalization|internal]] to [[presheaves]] to its system $U_X \mapsto \Gamma_U(E)$ of sets of [[local sections]]:

$$
  PSh(\mathcal{S})_{/y(X)}
  \underoverset
    {\sim}
    { \Gamma_{(-)}(-) }
    {\longrightarrow}
  PSh
  \big(
     \mathcal{S}_{/X}
  \big)
$$

The [[model structure on sSet-enriched presheaves|sSet-enriched]] [[derived functor]] of this construction yields the analogous statement for [[(infinity,1)-categories of (infinity,1)-presheaves|$\infty$-categories of $\infty$-presheaves]], see at *[[slice of presheaves is presheaves on slice]]* for details.

## Related concepts


* [[slice of presheaves is presheaves on slice]]

* [[base change]]

* [[Giraud's theorem]]


## References

Discussion for [[Grothendieck toposes]]:

* {#SGA41}[[Michael Artin]], [[Alexander Grothendieck]], [[Jean-Louis Verdier]], _Théorie des Topos et Cohomologie Etale des Schémas_ ([[SGA4]]) Tome 1: *Théorie des Topos* Springer **LNM** **269** (1972) ([doi:10.1007/BFb0081551](https://link.springer.com/book/10.1007/BFb0081551), [pdf](http://www.cmls.polytechnique.fr/perso/laszlo/sga4/SGA4-1/sga41.pdf))

  (In particular, exposé III.5 and exposé IV.5 on the "induced topos" - _topos induit_ = slice topos)

Discussion in the generality of [[elementary toposes]]:

* {#McLarty92} [[Colin McLarty]], *[[Elementary Categories, Elementary Toposes]]*, Oxford University Press 1992 ([ISBN:9780198514732](https://global.oup.com/academic/product/elementary-categories-elementary-toposes-9780198514732?cc=ae&lang=en&))

See also:

* Wikipedia, *[Fundamental theorem of topos theory](https://en.wikipedia.org/wiki/Fundamental_theorem_of_topos_theory)*

Discussion for [[slice (infinity,1)-toposes|slices of]] Grothendieck [[(infinity,1)-toposes|$\infty$-toposes]]:

* {#Lurie09} [[Jacob Lurie]], Section 6.3.5 of: *[[Higher Topos Theory]]*, Annals of Mathematics Studies 170, Princeton University Press 2009 ([pup:8957](https://press.princeton.edu/titles/8957.html), [pdf](https://www.math.ias.edu/~lurie/papers/HTT.pdf))

The terminology "fundamental theorem of $\infty$-topos theory" for this is used in 

* [[Marco Vergura]], Rem. 2.2.10 in: *Theory in an Infinity Topos*, 2019 ([pdf](https://ir.lib.uwo.ca/cgi/viewcontent.cgi?article=8583&context=etd), [ir.lib.uwo.ca:etd/6257](https://ir.lib.uwo.ca/etd/6257))

  > (in a context of [[localization of an (infinity,1)-category|localizations]] motivated by [[modal homotopy type theory]])

[[!redirects fundamental theorem of (infinity,1)-topos theory]]
[[!redirects fundamental theorem of (∞,1)-topos theory]]
