+-- {: .standout}
To the extent that the contents of this page are precise at all, they are speculative.  Nobody has formulated, much less proved, the logical consistency and independence results that would formally justify its claims.
=--


A __strict category__ is a [[category]] with a notion of [[equality]] (not merely [[isomorphism]]) of its [[objects]].

In most [[foundations]] of mathematics (not only [[ZFC]] but also structural set theories such as [[ETCS]] and [[SEAR]]), every category is necessarily a strict category, because it has a [[set]] (or [[class]]) of objects, and elements of this can be compared for equality.  However, some foundations (including [[FOLDS]], [[SEAR+ε]], the [[type theories]] of Martin-L&#246;f and Thierry Coquand, and [[preset]] theories) allow one to naturally define the term 'category' so that a category is not inherently strict.

A __strict functor__ is a [[functor]] between strict categories that preserves equality: $F(x) = F(y)$ if $x = y$.  Again, in most foundations, this happens automatically, and one must pass to [[anafunctors]] to recover a properly weak notion of functor.  All [[natural transformations]] between strict functors are automatically strict.

A [[2-category]] must have strict categories as its [[hom-categories]] to write down the definition of [[strict 2-category]]; a similar remark holds for [[strict 2-functors]].  As such, strictness in the sense of this page matches and extends strictness in the usual sense of [[higher category theory]].  However, we now get a notion of __strict $2$-natural transformation__ as one that preserves equality.  (All [[modifications]] between strict transformations are automatically strict ... until we get to $3$-categories, of course!)

Even if one\'s foundations allow one to notice the difference between strict categories and properly weak categories, the practical content disappears in the presence of the [[axiom of choice]].  (This is just like the equivalence between functors and anafunctors in that case.)


[[!redirects strict categories]]
[[!redirects strict functor]]
[[!redirects strict functors]]
[[!redirects strict groupoid]]
[[!redirects strict groupoids]]