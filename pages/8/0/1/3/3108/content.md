The "prototypical" example of a [[weak factorization system]] is ([[injection|mono]], [[surjection|epi]]) on [[Set]].  That this is a WFS is equivalent to the [[axiom of choice]], but various weaker things can be said in more generality.

* (complemented mono, split epi) is a WFS in any [[extensive category]], without any need for choice and even in [[intuitionistic logic]].  A factorization of $X\to Y$ is $X\to X+Y \to Y$.  In this WFS, every object is "cofibrant" (that is, $0\to X$ is in the left class) while an object is "fibrant" (i.e. $X\to 1$ is in the right class) if and only if it admits a [[global element]].

* Thus, [[classical logic]] (which says that any subset is complemented) is equivalent to saying that (mono, split epi) is a WFS on Set.

* Since the [[axiom of choice]] is equivalent to saying that any epic in Set is split, (mono, epi) is a WFS if and only if AC holds.

We might also ask for WFS on Set (or more general categories) whose left class or right class consists of monics or epics, respectively, with the other class being whatever it must be.

* On any [[topos]], there is a WFS (mono, relative injective), where a map $f\colon X\to Y$ in a category $C$ is *relatively injective* if it is an [[injective object]] in the [[slice category]] $C/Y$.  Factorizations are provided by the fact that any topos has enough injectives (i.e. any object can be embedded in an injective), and any slice category of a topos is again a topos.  See also [this answer](http://mathoverflow.net/questions/10246/model-category-structure-on-set-without-axiom-of-choice/10368#10368) by [[Denis-Charles Cisinski]] on MO.  In this model structure every object is "cofibrant," while the "fibrant" objects are the injectives; thus we might call this the *injective model structure*.

* On any extensive category, there is a WFS whose right class is the epimorphisms if and only if there exist enough [[projective objects]] (i.e. every object admits an epimorphism from a projective one).  For if such a WFS exists, then clearly the "cofibrant" objects are the projectives, so cofibrant replacement provides a projective cover of any object.  Conversely, if there are enough projectives, then we take the left class to be the complemented monics with projective complement; a factorization of $X\to Y$ is provided by $X\to X+Y' \to Y$, where $Y'\to Y$ is a projective cover.  In particular, there is a WFS on Set whose right class is the epimorphisms if and only if [[COSHEP]] holds.  As remarked above, the "cofibrant" objects here are the projective ones, while the "fibrant" objects are the "well-supported ones;" thus we might call this the *projective model structure*.

Looking at the "projective" and "injective" model structures above, by analogy with the [[model structures on chain complexes]] we might also be tempted to call (complemented mono, split epi) the *Hurewicz WFS*.

[[!redirects weak factorization systems on Set]]
[[!redirects WFS on Set]]
[[!redirects wfs on Set]]
