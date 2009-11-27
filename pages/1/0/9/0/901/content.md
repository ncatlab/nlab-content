# Idea #

An **ind-object** of a category $C$ is a "formal [[filtered colimit]]" of objects of $C$.  The category of ind-objects of $C$ is written $ind$-$C$.

Here, "ind" is short for "inductive system", as in the inductive systems used to define [[directed colimit]]s, as contrasted with "pro" in the [[pro-object|dual notion]] for "projective system".

+-- {: .query}
Would it make sense to take this opportunity on nLab to give this a new modern name? Maybe call it "colimit-object" or "filtered colimit" or something? Something more consistent with the rest of the nLab might be nice. Just a thought. - [[Eric Forgy|Eric]]

[[Tim Porter|Tim]]: As they are very special diagrams, I do not think that Eric's suggestion is a good one. The pro and ind terminology was to replace inverse and direct system which was already being used in the 1930s (I think?)  The 'ind' terminology is at least as old as 1960 (see Grothendeck's seminar on descent.)

[[Mike Shulman|Mike]]: I think the terminology "ind-object" is too well-established to be changed.  And I don't really think there's much reason to want to change it anyway; it may come historically from a terminology that we do not use, but it is unambiguous and the notion deserves its own name.  In particular, it is not a (filtered) colimit; the whole point is that you don't actually _take_ the colimit (or alternately, you only take it inside the free colimit-completion).

_Toby_:  Not to disparage 'ind-object', but I think that the term that Eric\'s looking for is 'formal filtered colimit'.
=--

Recalling the nature of [[filtered colimits]], this means that in particular chains of inclusions 

$$
  c_1 \hookrightarrow c_2 \hookrightarrow c_3 \hookrightarrow c_4 \hookrightarrow \cdots
$$

of objects in $C$ are regarded to converge to an object in $ind C$, even if that object does not exist in $C$ itself. 
Standard examples where ind-objects are relevant are categories $C$ whose objects are finite in some sense, such as finite sets or finite vector spaces. Their ind-categories contain then also the infinite versions of these objects as limits of sequences of inclusions of finite objects of ever increasing size. 

Moreover, ind-categories allow to handle "big things in terms of small things" also in another important sense: many [[large category|large categories]] are actually ([[equivalence of categories|equivalent]] to) ind-categories of [[small category|small categories]]. This means that, while [[large category|large]], they are for all practical purposes controlled by a [[small category]] (see the description of the [[hom-set]] of $ind-C$ in terms of that of $C$ below). Such [[large category|large categories]] equivalent to ind-categories are therefore called [[accessible category|accessible categories]].


# Definition #

There are several equivalent ways to define ind-objects


## as diagrams ##

One definition is to define the objects of $ind$-$C$ to be diagrams $F:D\to C$ where $D$ is a [[small category|small]] [[filtered category|filtered]] category.  
The idea is to think of these diagrams as being the placeholder for the [[colimit]] over them (possibly non-existent in $C$)
We identify an ordinary object of $C$ with the corresponding diagram $1\to C$.  To see what the morphisms should be between $F:D\to C$ and $G:E\to C$, we stipulate that

1. The embedding $C\to ind$-$C$ should be [[full and faithful functor|full and faithful]],
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

Here

* the first step is by assumption that each object is a suitable colimit;

* the second by the fact that the contravariant Hom sends colimits to limits (see properties of [[colimit]]);

* the third by the assumption that each object is [[finitely presentable object|finitely presentable]];

*  the last by the assumption that the embedding is a [[full and faithful functor]].

So then one _defines_ 

$$
  ind\text{-}C(F,G) := \cong lim_{d\in D} colim_{e\in E}\; C(F d, G e)
  \,.
$$

## as filtered colimits in presheaves ##

Recall the [[co-Yoneda lemma]] that every presheaf $X \in PSh(C)$ is a [[colimit]] over [[representable functor|representable presheaves]]:


there is some functor $\alpha : D \to C$ such that

$$
  X \simeq colim_{d \in D} Y(\alpha(d))
  \,.
$$

+-- {: .un_defn}
###### Definition

Let $ind\text{-}C \subset PSh(C)$ be the [[full subcategory]] of the [[presheaf]] [[category]] $PSh(C) = [C^{op},Set]$ on those [[functor]]s which are [[filtered colimits]] of [[representable functor|representables]], i.e. those for which 
$$
  X \simeq colim_{d \in D} Y(\alpha(d))
$$
with $D$ a [[filtered category]].
=--

##Remarks##

Given that $[C^{op},Set]$ is the [[free cocompletion]] of $C$, $ind$-$C$ defined in this way is its "free cocompletion under filtered colimits."

To compare with the first definition, notice that indeed the formula for the [[hom-set]]s s reproduced:

Generally we have

$$
  \begin{aligned}
     [C^{op},Set](X,Y)
     & \simeq
     [C^{op}, Set](colim_{d \in D} Y F d, colim_{d' \in D'} Y G d)
     \\
     & \simeq 
     lim_{d \in D} [C^{op}, Set]( Y F d, colim_{d' \in D'} Y G d)
  \end{aligned}
$$

by the fact that the [[hom-functor]] sends [[colimit]]s to [[limit]]s in its first argument (see _properties_ at [[colimit]]). 

By the [[Yoneda lemma]] this is

$$
  \cdots \simeq 
   lim_{d \in D} (colim_{d' \in D'} Y G d')(F d)
  \,.
$$

Using that [[colimit]]s in $PSh(C)$ are computed objectwise (see again _properties_ at [[colimit]]) this is

$$
  \cdots \simeq 
   lim_{d \in D} colim_{d' \in D'} 
   C(F d, G d')  \,.
$$




# Examples #

* Let $FinVect$ be the category of finite-dimensional vector spaces (over some field). Let $V$ be an infinite-dimensional vector space. Then $V$ can be regarded as an object of $ind-FinVect$ as the colimit $colim_{V' \hookrightarrow V} Y(V')$ over the [[filtered category]] whose objects are inclusions $V' \hookrightarrow V$ of finite dimensional vector spaces $V'$ into $V$ of the representables $Y(V') : FinVect^{op} \to Set$ ($Y$ is the [[Yoneda embedding]]).

* For $C$ the category of finitely presented objects of some equationally defined structure, $ind\text{-}C$ is the category of all these structures.

  * The catgeory [[Grp]] of groups is the ind-category of the category of finitely generated groups.

    * The catgeory [[Ab]] of abelian groups is the ind-category of the category of finitely generated abelian groups.


# Properties #

* If $C$ is a [[locally small category]] then so is $ind-C$.

* The inclusion $C \hookrightarrow ind\text{-}C$ is [[exact functor|right exact]].

* a functor $F : C^{op} \to Set$ is in $ind\text{-}C$ (i.e. is a [[filtered colimit]] of [[representable functor|representables]]) precisely if the [[comma category]] $(Y,const_F)$ (with $Y$ the [[Yoneda embedding]]) is [[filtered category|filtered]] and [[cofinally small category|cofinally small]].

* $ind\text{-}C$ admits small [[filtered colimits]] and the inclusion $ind\text{-}C\hookrightarrow PSh(C)$ commutes with these colimits.

* If $C$ admits finite [[colimit]]s, then $ind\text{-}C$ is the [[full subcategory]] of the [[presheaf]] category $PSh(C)$ consisting of those functors $F : C^{op} \to Set$ such that $F$ is [[exact functor|left exact]] and the [[comma category]] $(Y,F)$ (with $Y$ the [[Yoneda embedding]]) is [[cofinally small category|cofinally small]].

#Applications#

* One important use of categories of ind-objects is in [[abelian sheaf]]-theory: for every [[small category|small]] [[abelian category]] $C$ the category $ind\text{-}C$ is a [[Grothendieck category]] and hence a good coefficient object for [[abelian sheaf cohomology]].

# Generalizations #

## in $(\infty,1)$-catgeories ##

There is a notion of [[ind-object in an (infinity,1)-category]].

With regard to the third of the properties listed above, notice that the [[comma category]] $(Y,const_F)$ is the [[category of elements]] of $F$, i.e. the [[pullback]] of the [[generalized universal bundle|universal Set-bundle]] $U : Set_* \to Set$ along $F : C^{op} \to Set$. This means that the [[stuff, structure, property|forgetful functor]]
$
  (Y,const_F) \to C
$
is the fibration classified by $F$. 

This is the starting point for the definition at [[ind-object in an (infinity,1)-category]].


#References#

Ind-categories are discussed in

* Kashiwara-Schapira, [[Categories and Sheaves]], section 6

* Grothendieck et al. SGA4.I.6 [djvu file](http://modular.math.washington.edu/sga/djvu/SGA4-1.tif.djvu)

* A. Grothendieck, Techniques de d&#233;scente et th&#233;or&#232;mes d'existence en g&#233;om&#233;trie
alg&#233;brique, II: le th&#233;or&#232;me d'existence en th&#233;orie formelle des modules, Seminaire
Bourbaki, 195, 1960.

See also the remarks at the beginning of section 5.3 of

* [[Jacob Lurie]], [[Higher Topos Theory]]



***

# Discussion #

We had the following discussion  on the comma category $(Y,const_F)$. 

+-- {: .query}

[[David Roberts]]: I don't think this is true, since the fibration classified by $F$ would be $(F,U)$ (or $(U,F)$, whichever is suitable) where $U:Set_* \to Set$ is the forgetful functor$=$universal set bundle. The $F$ in $(Y,F)$ is to be considered an object of $Set^{C^{op}}$, not as a functor $C^{op} \to Set$. 

[[Urs Schreiber|Urs]]: Ahm, let me see. So $(Y,F)$ (which, yes, should more precisely be written $(Y,const_F)$) has as objects morphisms of presheaves $e : Y(c) \to F$, equivalently by Yoneda the objects are elements $e \in F(c)$. 

Its morphisms from $e : Y(c) \to F$ to $e' : Y(c')  \to F$ are given by morphisms $f : c \to c'$ in $C$ such that $f^* e' = e$. 

That seems to me to be the category which is also characterized as being the (strict) pullback of

$$
  \array{
    && Set_*
    \\
    && \downarrow^{U}
    \\
    C^{op} &\stackrel{F}{\to}& Set
  }
$$ 

No?

[[Urs Schreiber|Urs]]: Accordingly, I have now made the notation more precise by replacing "$F$" by "const_F" in the above. 

=--

