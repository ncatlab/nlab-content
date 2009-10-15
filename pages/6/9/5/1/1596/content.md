A [[subcategory]] $D$ of a category $C$ is called __replete__ if it respects [[isomorphism]] of morphisms in the [[arrow category]] of $C$.  It is a subcategory for which the property of (strictly) belonging to it is not [[evil]].


## Definition

A subcategory $D$ of $C$ is __replete__ if for any $x$ in $D$ and any isomorphism $f:x\cong y$ in $C$, both $y$ and $f$ are also in $D$.

Equivalently, if $f \in D$ and $f \cong g$ in $Arr(C)$, then $g \in D$.

## Repletion and replete images

Note that the inclusion functor of any replete subcategory must be [[pseudomonic functor|pseudomonic]].  Conversely, any subcategory whose inclusion functor is pseudomonic has a **repletion**.  The repletion $repl(D)$ of $D\subset C$ defined to consist of those objects of $C$ admitting an isomorphism to some object of $D$, with the morphisms $x\to y$ in $repl(D)$ being those morphisms $f\colon x\to y$ in $C$ such that $g f h^{-1}$ is in $D$ for some isomorphisms $g\colon x\to x'$ and $h\colon y\to y'$ with $x', y'\in D$.  Note that $D\subset C$ must be pseudomonic for this condition to be independent of the choice of $g$ and $h$.

Repleteness and repletions are most often applied to [[full subcategories]], in which case the repletion is simply the full subcategory of $C$ determined by those objects which are isomorphic to some object of $D$.

The **replete image** of a functor which is full on isomorphisms is the repletion of its image (which is pseudomonic).  The **replete full image** of a functor is the repletion of its [[full image]], i.e. the full subcategory of its target determined by those objects isomorphic to some object in its image.  See also [[essential image]].


## Higher-categorical versions

More generally, for $n\geq 0$, a subcategory $D$ of an $n$-[[n-category|category]] $C$ is replete if all [[equivalence]]s in $C$ whose either source or target is in $D$ are themselves in $D$. In particular, all $k$-cells equivalent in $C$ to some $k$-cell in $D$ are themselves in $D$ (because they are sources of some equivalence in $D$).  Then replete subcategories of $1$-[[1-category|categories]] are those which are replete in this sense.

Here we are using the weakest notion of equivalence; one could also talk about $k$-replete $n$-subcategories if every $k$-equivalences in $C$ belongs to $D$ if either its source or target does.  Then using the usual definition of 'category' as a model for $1$-categories, replete subcategories are already those which are $0$-replete (indeed, $0$-equivalence is isomorphism in this model); but using a model of $1$-categories in which [[hom-sets]] are [[setoid]]s (as is common, for example, in [[type theory|type-theoretic]] [[foundations]]), we must insist on $1$-repleteness.

Note that a subcategory $D$ of an $n$-category $C$ is $(k-1)$-replete if and only if:
*  for every $(n-k)$-cell in $D$ all $(n-k)$-cells $(k-1)$-equivalent to an $(n-k)$-cell in $D$ are themselves in $C$, and
*  for any two $(n-k)$-cells $x,y$ the hom $k$-category $hom(x,y)$ is $(k-2)$-replete.

+-- {: .query}
Do we want this parametrised [[equivalence]]?  I see that isomorphism is $0$-equivalence and equality is $(-1)$-equivalence, which is ugly enough but the sort of thing that does happen.  But I\'ve never actually heard anybody say that, for example, some objects of a $3$-category are $2$-equivalent.  Why not just say that they\'re equivalent?  (If anything, I\'d rather say that they\'re $2$-isomorphic and let 'equivalent' mean $\infty$-isomorphic always.)  ---Toby

[[Mike Shulman|Mike]]: Definitely, unqualified "equivalent" in an $n$-category should mean $(n-1)$-equivalent, or equivalently (if you like your $n$-categories to be secretly $\infty$-categories) it should mean $\infty$-equivalent.  I think that is by far the most common usage, so it won't have to change.  However, there are occasionally reasons to speak about stronger sorts of equivalence; for instance in a strict 2-category it is occasionally important to distinguish between isomorphism and equivalence.  People do also talk about "biequivalence" for bicategories and "2-equivalence" for 2-categories.  I would venture that $k$-equivalence in an $n$-category for $k\lt n-1$ is not likely to be useful unless your $n$-category is some sort of semistrict, but in that case it might occasionally turn out to be helpful.

[[Zoran Škoda]]: The $0$-cells in $n$-category are by default $(n-1)$-equivalent (what is of course maximal weakness and equals infty-equivalent), while it is possible that they are equivalent in more strict sense, for example isomorphic (there is a strictly invertible 1-arrow in between); for higher cells equivalence is the same as equivalence in lower dimension category which is its hom, thuis the number is not $(n-1)$ by default for k cells k bigger than 0; of course you are right that all these maximal equivalences are in the same time equivalences in higher sense because there is no difference since higher dimensional cells do not exist different than identities. But regarding that sometimes stricter versions are needed, not  only maximal the terminology can be kept precise. 
For example in Cat one can consider both isomorphic and
equivalent categories and these are two different notions;
and of course equal categories as the strictest possible notion of (-1)-equivalence. I do not recall if I first read this in print from Leinster's book, but before that Igor explained me those after his readings of Australian school works. 

_Toby_:  Not every concept of $n$-category even has a concept of equivalence of objects other than $(n-1)$-equivalence (or more generally a concept of equivalence for $k$-morphisms other than $(n-k-1)$-equivalence).  I find it confusing to put in all of these prefixes to describe what even you, Zoran, agree is the default notion.  So I have given this default first, and then added a note about using stricter levels of equivalence when available.

Zoran, you might also want to address these issues at [[equivalence]].
=--

[[!redirects replete image]]
