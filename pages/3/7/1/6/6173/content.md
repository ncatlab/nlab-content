Abstract localization functors among abelian categories have several descriptions. Additional descriptions exist if in addition the category is [[Grothendieck category|Grothendieck]]. 

A nonempty subcategory of an abelian category is __thick__ (in the sense of [[Pierre Gabriel]]; called _dense_ in Popescu) if it is closed under subobjects, quotients and extensions (in particular it is full and abelian). Some authors say Serre subcategory for a thick subcategory, though a stronger version of the notion of Serre subcategory may be appropriate (and is occasionally so defined) if the Abelian category is not the full subcategory of modules over a ring or ringoid (when the two notions agree).

Following [[Jean-Pierre Serre]], given a thick subcategory $T$, define the __quotient category__ $A/T$ whose objects are the objects of $A$ and where the morphisms in $A/T$ are defined by 
$$\mathrm{Hom}_{A/T}(X,Y) := \mathrm{colim}\, \mathrm{Hom}_A(X',Y/Y'),$$
where the colimit is over all $X',Y'$ in $A$ such that $Y'$ and $X/X'$ are in $T$. There is a canonical __quotient functor__ $Q: A\to A/T$ which is the identity on objects. The quotient category $A/T$ is abelian.

* [[Pierre Gabriel]], [[Des catégories abéliennes]], Bulletin de la Soci&#233;t&#233; Math&#233;matique de France, 90 (1962), p. 323-448, [numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0)
* [[Francis Borceux]], Handbook of categorical algebra
* Chapter 15 in [[Carl Faith]], _Algebra: Rings, Modules, Categories_, vol. 1,  Grundlehren der mathematischen Wissenschaften **190**, Springer (1973) &lbrack;[doi:10.1007/978-3-642-80634-6](https://doi.org/10.1007/978-3-642-80634-6)&rbrack;
* N. Popescu, [[Abelian categories with applications to rings and modules]], London Mathematical Society Monographs 3, Academic Press 1973, xii + 470 pp

[[!redirects localization in abelian categories]]
[[!redirects localization in an abelian category]]