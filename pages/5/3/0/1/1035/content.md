An **preadditive category** (sometimes just called *additive*) is a category [[enriched category|enriched]] over [[abelian group]]s with their [[tensor product]].  In elementary terms, this means that each [[hom-set]] is an abelian group and composition is bilinear.

+-- {+ .query}
WHO says additive for Ab-enriched ?? The only hesitation in homological algebra, I ever saw is that some people identify (for example Kashiwara-Shapira) Ab-enriched and preadditive while some include zero object into preadditive. I personally do not use term preadditive at all.

But I did not notice anybody in the field who takes additive to be only Ab-enriched, as far as I noticed in last 22 years, since I learned the notion in 1987. Additive category is a completely standard term at least since Grothendieck Tohoku article in 1957 (written 3 years earlier). 

[[Mike Shulman|Mike]]: I can't remember where I saw that usage.  I hope I didn't make it up.  It makes me sad that the meaning of "additive category" isn't parallel to "topological category" and "simplicial category" (in one of its meanings) and "differential graded category" in denoting merely an enrichment, but also for some reason requires the existence of certain limits.  But I suppose we're stuck with it.
=--

In a preadditive category, any [[initial object|initial]] or [[terminal object|terminal]] object is automatically a [[zero object]]; more generally, any finite [[product]] or [[coproduct]] is automatically a [[biproduct]].  (This does not extend to infinite or non-discrete limits.)

An **additive category** is a preadditive category in which all finite biproducts exist; by the previous paragraph, it\'s enough to say either that finite products exist or that finite coproducts exist.  But originally (and often still) this requirement is not included in the term 'additive'.

An especially important sort of additive category is an [[abelian category]].
