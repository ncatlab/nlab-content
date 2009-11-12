> Lately I\'ve been thinking that, just as higher category theory is easier to learn if one already knows [[category theory]], so category theory itself is easier to learn if one already knows [[order theory]].  If I\'d said [[set theory]] (in a na&#239;ve sense) instead of order theory just now, then there would be nothing controversial about this; but many (not all) features of category theory that don\'t apply to groupoids or sets do already apply to posets, and it\'s pedagogically unsound to skip over those.  ---[[Toby Bartels]]

Consider the following table.  The basic thesis of this page is that, if you are having trouble understanding an item in the left column, then first you should understand the item in the right column.  (Each item on the right is the [[decategorification]] of the item on the left.)

| Category theory | Order theory |
| - | - |
| [[skeletal category]] | [[poset]] |
| [[strict category]] | [[proset]] |
| [[groupoid]] | [[set]] |
| [[limit]] | [[meet]] |
| [[colimit]] | [[join]] |
| [[functor]] | [[monotone function]] |
| [[dual adjunction]] | [[Galois connection]] |
| [[cartesian closed category]] | [[Heyting algebra]] |
| [[Grothendieck topos]] | [[locale]] |
| [[monad]] | [[Moore closure]] |
| ... | ... |

In the first several rows, we trust that people know about the order-theoretic concept before we teach them about category theory, so we can and do use these rows pedagogically.  But after that, we cannot trust that people know about the order-theoretic concepts, so we teach the category-theoretic concepts without them ---but *the order-theoretic concepts are still simpler*, so maybe we should teach (or learn) about them first.

This is an example of [[negative thinking]], but perhaps not more negative than normal.  It is common to go down as far as $0$-categories, but not so common to move to $(0,1)$-categories before pushing on to $1$-categories.