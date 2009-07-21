A [[subcategory]] $D$ of a category $C$ is called __replete__ if it respects [[isomorphism]] of morphisms in the [[arrow category]] of $C$.  It is a subcategory for which the property of (strictly) belonging to it is not [[evil]].


## Definition

A subcategory $D$ of $C$ is __replete__ if for any $x$ in $D$ and any isomorphism $f:x\cong y$ in $C$, both $y$ and $f$ are also in $D$.

Equivalently, if $f \in D$ and $f \cong g$ in $Arr(C)$, then $g \in D$.

More generally, for $n\geq 0$, a subcategory $D$ of an $n$-[[n-category|category]] $C$ is replete if for any $0\leq (k-1)\lt n$ all $(k-1)$-equivalences in $C$ whose either source or target is in $D$ are themselves in $D$. In particular, all $(n-k)$-cells $(k-1)$-equivalent in $C$ to some $(n-k)$-cell in $D$ are themselves in $D$ (because they are sources or some $(k-1)$-equivalence in $D$). One could talk about $(k-1)$-replete $n$-subcategories if this is true up to $(k-1)$. Replete subcategories of 1-categories are those which are 0-replete in this convention (indeed, $0$-equivalence is an isomorphism). A subcategory $D$ of an $n$-category $C$ is $(k-1)$-replete iff for any two $(n-k)$-cells $x,y$ the hom $k$-category $\mathrm{hom}(x,y)$ is $(k-2)$-replete and for every $(n-k)$-cell in $D$ all $(n-k)$-cells $(k-1)$-equivalent to an $(n-k)$-cell in $D$ are themselves in $C$. 

+-- {: .query}
Do we want this parametrised [[equivalence]]?  I see that isomorphism is $0$-equivalence and equality is $(-1)$-equivalence, which is ugly enough but the sort of thing that does happen.  But I\'ve never actually heard anybody say that, for example, some objects of a $3$-category are $2$-equivalent.  Why not just say that they\'re equivalent?  (If anything, I\'d rather say that they\'re $2$-isomorphic and let 'equivalent' mean $\infty$-isomorphic always.)  ---Toby

[[Mike Shulman|Mike]]: Definitely, unqualified "equivalent" in an $n$-category should mean $(n-1)$-equivalent, or equivalently (if you like your $n$-categories to be secretly $\infty$-categories) it should mean $\infty$-equivalent.  I think that is by far the most common usage, so it won't have to change.  However, there are occasionally reasons to speak about stronger sorts of equivalence; for instance in a strict 2-category it is occasionally important to distinguish between isomorphism and equivalence.  People do also talk about "biequivalence" for bicategories and "2-equivalence" for 2-categories.  I would venture that $k$-equivalence in an $n$-category for $k\lt n-1$ is not likely to be useful unless your $n$-category is some sort of semistrict, but in that case it might occasionally turn out to be helpful.

[[Zoran Škoda]]: The $0$-cells in $n$-category are by default $(n-1)$-equivalent (what is of course maximal weakness and equals infty-equivalent), while it is possible that they are equivalent in more strict sense, for example isomorphic (there is a strictly invertible 1-arrow in between); for higher cells equivalence is the same as equivalence in lower dimension category which is its hom, thuis the number is not $(n-1)$ by default for k cells k bigger than 0; of course you are right that all these maximal equivalences are in the same time equivalences in higher sense because there is no difference since higher dimensional cells do not exist different than identities. But regarding that sometimes stricter versions are needed, not  only maximal the terminology can be kept precise. 
For example in Cat one can consider both isomorphic and
equivalent categories and these are two different notions;
and of course equal categories as the strictest possible notion of (-1)-equivalence. I do not recall if I first read this in print from Leinster's book, but before that Igor explained me those after his readings of Australian school works. 
=--
