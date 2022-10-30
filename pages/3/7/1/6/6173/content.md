Abstract localization functors among abelian categories have several descriptions. Additional descriptions exist if in addition the category is [[Grothendieck category|Grothendieck]]. 

A nonempty subcategory of an abelian category is __thick__ (in the sense of [[Pierre Gabriel]]) if it is closed under subobjects, quotients and extensions. In the special case of the abelian categories of $R$-modules (where $R$ is a ring) this agrees with the notion of a Serre subcategory (in general the latter is a stronger notion).

Following [[Jean-Pierre Serre]], given a thick subcategory $T$, define the __quotient category__ $A/T$ whose objects are the objects of $A$ and where the morphisms in $A/T$ are defined by 
$$\mathrm{Hom}_{A/T}(X,Y) := \mathrm{colim}\, \mathrm{Hom}_A(X',Y/Y'),$$
where the colimit is over all $X',Y'$ in $A$ such that $Y'$ and $X/X'$ are in $T$. There is a canonical __quotient functor__ $Q: A\to A/T$ which is the identity on objects. The quotient category $A/T$ is abelian.

* [[Pierre Gabriel]], [[Des catégories abéliennes]], Bulletin de la Soci&#233;t&#233; Math&#233;matique de France, 90 (1962), p. 323-448, [numdam](http://www.numdam.org/item?id=BSMF_1962__90__323_0)
* [[Francis Borceux]], Handbook of categorical algebra

[[!redirects localization in abelian categories]]
[[!redirects localization in an abelian category]]