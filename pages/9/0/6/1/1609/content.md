> This page need to be seriously rewritten, see "Oops" and "Oops 2" below.

Oops 2... _Category with involution_ is differently defined by [Springer](http://eom.springer.de/C/c020780.htm) and [Wikipedia](http://en.wikipedia.org/wiki/Dagger_category). Need to bring that to order.

Oops... I found that my notion of _partially ordered category with inverses_ is the same (oh, well, except of requiring that even isomorphism is unitary) as the known notion of _category with involution_ (see http://eom.springer.de/C/c020780.htm) Oh, well, with the additional requirement that the involution preserves the order. The conclusion: this page should be rewritten in order to mirror the customary terminology instead of my unnecessary neologisms. Sorry me.

_Partially ordered category_ is a category together with [[partial order]]ing $\subseteq$ of its morphisms such that
$$ f_1 \subseteq f_2 \;\wedge\; g_1 \subseteq g_2 \;\Rightarrow\; g_1 \circ f_1 \subseteq g_2 \circ f_2 $$
for any morphisms $f_1$, $g_1$, $f_2$, $g_2$ such that the composites above are defined.

For a _partially ordered category_ its set of objects is partially ordered by the formula $A \subseteq B \Leftrightarrow 1_A \subseteq 1_B$.

Compare the notion of [[locally partially ordered category]].  A partially ordered category in which the [[source]] and [[target]] maps preserve the partial order is a category *[[internal category|internal]] to* the category [[Pos]] of [[poset]]s, while a locally partially ordered category is a category *[[enriched category|enriched]] over* $Pos$.  Similarly, such a partially ordered category is a special kind of [[double category]], while a locally partially ordered category is a special kind of $2$-[[2-category|category]].

## Partially ordered dagger categories ##

**TODO: Create special page for _categories with inverses_.**

  I will call a _precategory with inverses_ a [[precategory]] together
  with a function $x \mapsto x^{- 1}$ defined on the set of morphisms, which
  reverses source and destination of the morphism, subject to the following
  equalities for any morphisms $f$, $g$:
 $(f^{- 1})^{- 1} = f$;
 $(g \circ f)^{- 1} = f^{- 1} \circ g^{- 1}$.

  I will call a _category with inverses_ a precategory with inverses
  which is a category with additional requirement that for any isomorphism its
  inverse is the reverse isomorphism.

+-- {: .query}
[[Mike Shulman|Mike]] (edited by [[Toby Bartels|Toby]], who concurs): What you call a "category with inverses" is the same as a [[dagger category]] in which every isomorphism is unitary.

The name "inverses" doesn't really seem appropriate, since they are not (necessarily) inverses in the sense with which that word is generally used in category theory.  They could be, of course, but most interesting dagger categories are not groupoids.

>[[VictorPorton|Victor]]: So suggest me how to rename "category with inverses". I have not yet published (only put on my Web site) the article where I define "category with inverses". So it is yet not late to rename. My email: porton@narod.ru.

>_Toby_: How about 'category with duals'?  That\'s a vague term that some people use to mean a dagger category but which can have other meanings, like a dagger compact category, which is more specific.  So it should be available for use in one paper or another for another concept more specific than dagger category, such as yours.  (Using a vague term leaves open the possibility of changing it later, or other people calling it a 'Porton category' if it really takes off, or even deciding that you want to write only about dagger categories later.)  But I think that it would definitely be best to speak of the 'dual' rather than the 'inverse' of a morphism, since 'inverse' is so widely used for what you have called the 'reverse isomorphism'.  That is, if you say 'every morphism has an inverse', then people will easily get confused, but not if you say 'every morphism has a dual'.

[[VictorPorton|Victor]]: Contrary to what you may expect, I would not like it be called 'Porton category' because among of these kinds of categories I present on this Wiki page, I invented at least yet two (well, five kinds of categories counting also my categories of continuous morphisms) categories... I will return later (it is in my TODO list) to change the terminology on this page.

>Another possibility: 'unitary dagger category'.  (Or see if what you\'re doing actually makes sense for arbitrary dagger categories and then use those.)

Preservation of identities is automatic once you have an involution that preserves binary composition.
$$
1_x^\dagger = 1_x^\dagger \circ 1_x = 1_x^\dagger \circ (1_x^\dagger)^\dagger = (1_x^\dagger \circ 1_x)^\dagger = (1_x^\dagger)^\dagger = 1_x.
$$
Note that in a dagger category, a morphism is called _unitary_ if its adjoint $f^\dagger$ is its inverse (in the usual sense, i.e. $f f^\dagger = 1$ and $f^\dagger f=1$).
=--

For a partially ordered (pre)category with inverses I will additionally
require (for any morphisms $f$ and $g$)
\[ f^{- 1} \subseteq g^{- 1} \Leftrightarrow f \subseteq g. \]

  For a partially ordered category with inverses I will call
  _monovalued_ morphism such a morphism $f$ that $f \circ f^{- 1}
  \subseteq 1_{\mathrm{Dst} f}$.

  For a partially ordered category with inverses I will call _entirely defined morphism_ such a morphism $f$ that $f^{- 1} \circ f \supseteq
  1_{\mathrm{Src} f}$.

+--{: .query}
[[Mike Shulman|Mike]]: I'm not sure what examples you have in mind, but you may be interested in reading about the theory of allegories and categories of [[relation]]s.

Answer: I have in mind categories in which arise the notion of _generalized continuity_: see [Generalized Continuity](http://www.mathematics21.org/binaries/continuousness.pdf) article at my [Algebraic General Topology site](http://www.mathematics21.org/algebraic-general-topology.html). Allegories seem not the best tool I could use, because I don't use intersections but am more interested in union of morphisms.

[[Tim Porter|Tim]]: The particular case of an ordered groupoid (in which each $f^{-1}$ is the inverse of $f$) is called an ordered groupoid.  This has been studied extensively by Mark Lawson, for instance see

Lawson, Mark V.
Constructing ordered groupoids. Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 46 no. 2 (2005), p. 123-138,
URL stable: http://www.numdam.org/item?id=CTGDC_2005__46_2_123_0

or his book: M.V. Lawson,  Inverse semigroups: the theory of partial symmetries, World Scientific, 1998. 

He makes the point that they were initially studied by Ehresmann and are very closely related to inverse semi-groups.  
=--

See more in [this online article](http://www.mathematics21.org/binaries/ordered-cats-with-inv.pdf). Feel free to copy the information from this my article to nLab wiki.

## See also ##
* [[generalized continuity]]
