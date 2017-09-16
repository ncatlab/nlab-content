# Idea #

An **ind-object** of a category $C$ is a "formal [[filtered category|filtered]] colimit" of objects of $C$.  The category of ind-objects of $C$ is written $ind$-$C$.

"Ind" is short for "inductive limit," an old term for a [[colimit]], as contrasted with "pro" in the [[pro-object|dual notion]] for "projective limit," the old term for [[limit]].

+-- {: .query}
Would it make sense to take this opportunity on nLab to give this a new modern name? Maybe call it "colimit-object" or "filtered colimit" or something? Something more consistent with the rest of the nLab might be nice. Just a thought. - [[Eric Forgy|Eric]]

[[Tim Porter|Tim]]: By the way, 'pro' in pro-object is short for 'projective system' NOT 'projective limit'.  Similarly ind-object is, I have always understood, an abbreviation for 'inductive system'. As they are very special diagrams, I do not think that Eric's suggestion is a good one. The pro and ind terminology was to replace inverse and direct system which was already being used in the 1930s (I think?) 

=--

Recalling the nature of [[filtered category|filtered]] colimits, this means that in particular chains of inclusions 

$$
  c_1 \hookrightarrow c_2 \hookrightarrow c_3 \hookrightarrow c_4 \hookrightarrow \cdots
$$

of objects in $C$ are regarded to converge to an object in $ind-C$, even if that object does not exist in $C$ itself. 
Standard examples where ind-objects are relevant are categories $C$ whose objects are finite in some sense, such as finite sets or finite vector spaces. Their ind-categories contain then also the infinite versions of these objects as limits of sequences of inclusions of finite objects of ever increasing size. 

Moreover, ind-categories allow to handle "big things in terms of small things" also in another important sense: many [[large category|large categories]] are actually ([[equivalence of categories|equivalent]] to) ind-categories of [[small category|small categories]]. This means that, while [[large category|large]], they are for all practical purposes controlled by a [[small category]] (see the description of the [[hom-set]] of $ind-C$ in terms of that of $C$ below). Such [[large category|large categories]] equivalent to ind-categories are therefore called [[accessible category|accessible categories]].



# Definition #

There are many ways to make this notion precise.  

## as diagrams ##

One definition is to define the objects of $ind$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|filtered]] category.  
The idea is to think of these diagrams as being the placeholder for the [[colimit]] over them (possibly non-existant in $C$)
We identify an ordinary object of $C$ with the corresponding diagram $1\to C$.  To see what the morphisms should be between $F:D\to C$ and $G:E\to C$, we stipulate that

1. The embedding $C\to ind$-$C$ should be full and faithful,
1. each diagram $F:D\to C$ should be the colimit of itself (considered as a diagram in $ind$-$C$ via the above embedding), and
1. the objects of $C$ should be [[finitely presentable object|finitely presentable]] in $ind$-$C$.

Thus, we should have

$$
\begin{aligned}
  ind\text{-}C(F,G) &= ind\text{-}C(colim_{d\in D} F d, colim_{e\in E} G   e)\\
   &\cong lim_{d\in D}\; ind\text{-}C(F d, colim_{e\in E} G e)\\
   &\cong lim_{d\in D} colim_{e\in E}\; ind\text{-}C(F d, G e)\\
   &\cong lim_{d\in D} colim_{e\in E}\; C(F d, G e)
\end{aligned}$$

So then one _defines_ 

$$
  ind\text{-}C(F,G) := \cong lim_{d\in D} colim_{e\in E}\; C(F d, G e)
  \,.
$$

## as filtered colimits ##

Another, equivalent, definition is to let $ind$-$C$ be the [[full subcategory]] of the [[presheaf]] [[category]] $[C^{op},Set]$ determined by those [[functor]]s which are [[filtered category|filtered]] colimits of [[representable functor|representables]].  This is reasonable since $[C^{op},Set]$ is the [[free cocompletion]] of $C$, so $ind$-$C$ defined in this way is its "free cocompletion under filtered colimits."

# Examples #

* Let $FinVect$ be the category of finite-dimensional vector spaces (over some field). Let $V$ be an infinite-dimensional vector space. Then $V$ can be regarded as an object of $ind-FinVect$ as the colimit $colim_{V' \hookrightarrow V} Y(V')$ over the [[filtered category]] whose objects are inclusions $V' \hookrightarrow V$ of finite dimensional vector spaces $V'$ into $V$ of the representables $Y(V') : FinVect^{op} \to Set$ ($Y$ is the [[Yoneda embedding]]).

* For $C$ the category of finitely presented objects of some equationally defined structure, $ind\text{-}C$ is the category of all these structures.

  * The catgeory [[Grp]] of groups is the ind-category of the category of finitely generated groups.

    * The catgeory [[Ab]] of abelian groups is the ind-category of the category of finitely generated abelian groups.


# Properties #

* If $C$ is a [[locally small category]] then so is $ind-C$.

* The inclusion $C \hookrightarrow ind\text{-}C$ is [[exact functor|right exact]].

* a functor $F : C^{op} \to Set$ is in $ind\text{-}C$ (i.e. is a [[filtered category|filtered]] colimit of [[representable functor|representables]]) precisely if the [[comma category]] $(Y,F)$ (with $Y$ the [[Yoneda embedding]]) is [[filtered category|filtered]] and [[cofinally small category|cofinally small]].

* $ind\text{-}C$ admits small [[filtered category|filtered]] [[colimit]]s and the inclusion $ind\text{-}C\hookrightarrow PSh(C)$ commutes with these colimits.

* If $C$ admits finite [[colimit]]s, then $ind\text{-}C$ is the full [[subcategory]] of the [[presheaf]] category $PSh(C)$ consisting of those functors $F : C^{op} \to Set$ such that $F$ is [[exact functor|left exact]] and the [[comma category]] $(Y,F)$ (with $Y$ the [[Yoneda embedding]]) is [[cofinally small category|cofinally small]].

# Generalizations #

* There is a notion of [[ind-object (infinity,1)-category]].

Notice that the [[comma category]] $(Y,F)$ is the [[pullback]] of the [[generalized universal bundle|universal Set-bundle]] $Set_* \to Set$ along $F : C^{op} \to Set$. This means that the canonical

$$
  (Y,F) \to C
$$

is the fibration classified by $F$. 

(...or close, let me check this...)

+-- {. :query}

[[David Roberts]]: I don't think this is true, since the fibration classified by $F$ would be $(F,U)$ (or $(U,F)$, whichever is suitable) where $U:Set_* \to Set$ is the forgetful functor$=$universal set bundle. The $F$ in $(Y,F)$ is to be considered an object of $Set^{C^{op}}$, not as a functor $C^{op} \to Set$. 

=--

This is the starting point for the definition at [[ind-object in an (infinity,1)-category]].


#References#

Ind-categories are discussed in

* Kashiwara-Schapira, [[Categories and Sheaves]], section 6

* Grothendieck et al. SGA4.I.6 <a href="http://modular.math.washington.edu/sga/djvu/SGA4-1.tif.djvu">djvu file</a>

See also the remarks at the beginning of section 5.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]