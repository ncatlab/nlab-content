A [[subcategory]] $D$ of a category $C$ is called __replete__ if it respects [[isomorphism]] of morphisms in the [[arrow category]] of $C$.


## Definition

A subcategory $D$ of $C$ is __replete__ if for any $x$ in $D$ and any isomorphism $f:x\cong y$ in $C$, both $y$ and $f$ are also in $D$.

Equivalently, if $f \in D$ and $f \cong g$ in $Arr(C)$, then $g \in D$.

More generally, for $n\geq 0$, a subcategory $D$ of an $n$-category $C$ is replete if for any $0\leq (k-1)\lt n$ all $(k-1)$-equivalences in $C$ whose either source or target is in $D$ are themselves in $D$. In particular, all $(n-k)$-cells $(k-1)$-equivalent in $C$ to some $(n-k)$-cell in $D$ are themselves in $D$ (because they are sources or some $(k-1)$-equivalence in $D$). One could talk about $(k-1)$-replete $n$-subcategories if this is true up to $(k-1)$. Replete subcategories of 1-categories are those which are 0-replete in this convention (indeed, $0$-equivalence is an isomorphism). A subcategory $D$ of an $n$-category $C$ is $(k-1)$-replete iff for any two $(n-k)$-cells $x,y$ the hom $k$-category $\mathrm{hom}(x,y)$ is $(k-2)$-replete and for every $(n-k)$-cell in $D$ all $(n-k)$-cells $(k-1)$-equivalent to an $(n-k)$-cell in $D$ are themselves in $C$. 

+-- {: .query}
Do we need this parametrised [[equivalence]]?  I see that isomorphism is $0$-equivalence and equality is $(-1)$-equivalence, which is ugly enough but the sort of thing that does happen.  But I\'ve never actually heard anybody say that, for example, some objects of a $3$-category are $2$-equivalent.  Why not just say that they\'re equivalent?  (If anything, I\'d rather say that they\'re $2$-isomorphic and let 'equivalent' mean $\infty$-isomorphic always.)  ---Toby
=--