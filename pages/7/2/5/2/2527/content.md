+-- {: .standout}
To the extent that the contents of this page are precise at all, they are speculative.  As far as I know, nobody has formulated, much less proved, the logical consistency and independence results that would justify its formal claims.

If you are content with [[set theory|set-theoretic]] foundations for category theory, you may ignore the adjective 'strict' in 'strict category'; in 'strict functor' it basically means 'non-[[anafunctor|ana]]' (the usual default, but not necessarily the best concept).  If you are content with set-theoretic foundations using the full strength of the global [[axiom of choice]], then you can even ignore the 'non-ana' bit.
=--


A __strict category__ is a [[category]] with a notion of [[equality]] (not merely [[isomorphism]]) of its [[objects]].  In contrast, a __weak category__ is a category *without* an equality predicate on its objects.  When taking the [[nPOV]], we often adopt the philosophical position that [[category theory]] is fundamentally about weak categories.

In most [[foundations]] of mathematics (not only [[ZFC]] but also structural set theories such as [[ETCS]] and [[SEAR]]), every category is necessarily a strict category, because it has a [[set]] (or [[class]]) of objects, and elements of this can be compared for equality.  However, some foundations (including [[FOLDS]], [[SEAR+ε]], the [[type theories]] of Martin-L&#246;f and Thierry Coquand, and [[preset]] theories) allow one to naturally define the term 'category' so that a category is not inherently strict.

A __strict functor__ is a [[functor]] between strict categories that preserves equality: $F(x) = F(y)$ if $x = y$.  Again, in most foundations, this happens automatically, and one must pass to [[anafunctors]] to recover a properly weak notion of functor (although the [[axiom of choice]] shows that every anafunctor between strict categories is [[natural isomorphism|naturally isomorphic]] to a strict functor).  Note that a [[natural transformation]] between strict functors is automatically strict.

A [[2-category]] must have strict categories as its [[hom-categories]] to write down the definition of [[strict 2-category]]; a similar remark holds for [[strict 2-functors]].  As such, strictness in the sense of this page matches and extends strictness in the usual sense of [[higher category theory]].  However, we now get a notion of __strict $2$-natural transformation__ as a [[2-natural transformation]] that preserves equality.  (All [[modifications]] between strict transformations are automatically strict ... until we get to $3$-categories, of course!)

Even if one\'s foundations allow one to notice the difference between strict categories and weak categories, the practical content disappears in the presence of the [[axiom of choice]].  (This is just like the equivalence between functors and anafunctors in that case.)


[[!redirects strict category]]
[[!redirects strict categories]]
[[!redirects strict functor]]
[[!redirects strict functors]]
[[!redirects strict groupoid]]
[[!redirects strict groupoids]]
