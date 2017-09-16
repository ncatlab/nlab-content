#Definition#

Given a [[site]] $S$, every [[Set]]-valued [[presheaf]] $F$ in $PSh(S) := [S^{op}, Set]$ is [[local isomorphism|locally isomorphic]] (weakly equivalent) to a [[sheaf]] $\bar F$. This construction extends to a functor

$$
  \bar{(-)} : PSh(S) \to Sh(S)
  \,.
$$

This functor is **sheafification**. 

Sheafification is [[exact functor|left exact]] [[adjoint functor|left adjoint]] to the [[stuff, structure, property|fully faithful forgetful]] [[injection|subcategory]] [[functor]] $i : Sh(S) \hookrightarrow PSh(S)$. Therefore it constitutes a [[geometric morphism]] of [[Grothendieck topos|Grothendieck topoi]]

$$
  PSh(S) \stackrel{\stackrel{\bar {(-)}}{\to}}{\stackrel{i}{\leftarrow}}
  Sh(S)
  \,.
$$

## Sheafification for more general presheaves ##


For presheaves with values in categories other than
[[Set]], sheafification may be a difficult problem, unless one has some extra assumptions. 


### Sheafification with values in models for finit-limit theories ###

Consider a type of structure $T$ defined in terms of finite limits (such as groups, algebras, modules, etc.), then [[internal logic|internal]] $T$-models are preserved by both direct and inverse images of geometric morphisms.  Therefore, the adjunction between sheaves and presheaves of sets directly induces an adjunction between $T$-models in sheaves and presheaves.  And since finite limits of sheaves and presheaves are computed pointwise, $T$-models in the category of (pre)sheaves are the same as (pre)sheaves of $T$-models-in-$Set$.

### Sheafification using IPC-property

If a [[category]] $A$ satisfies the following assumptions, sheafification of presheaves in $[S^{op}, A]$ exists and is constructed analogously as for [[Set]]-valued sheaves.


* $A$ admits small [[limit]]s;
* $A$ admits small [[colimit]]s;
* small [[filtered category|filtered limit]]s in $A$ are exact;
* $A$ satisfies the [[IPC-property]] .

This is true for instance for

* the category [[Set]] of sets;

* the category [[Grp]] of groups;

* the category $k Alg$ of $k$-algebras;

* the category $Mod(R)$ of [[module]]s,

(but all of these are also $T$-models for finite-limit theories $T$).



+--{+ .query}
One should say more: there are so many applications
and fairly difficult theorems there; for example van    
Osdol's  work.

[[Mike Shulman|Mike]]: Another way to think about this is: if you have a type of structure $T$ defined in terms of finite limits (such as groups, algebras, modules, etc.), then [[internal logic|internal]] $T$-models are preserved by both direct and inverse images of geometric morphisms.  Therefore, the adjunction between sheaves and presheaves of sets directly induces an adjunction between $T$-models in sheaves and presheaves.  And since finite limits of sheaves and presheaves are computed pointwise, $T$-models in the category of (pre)sheaves are the same as (pre)sheaves of $T$-models-in-$Set$.

If $T$ is _not_ defined in terms of finite limits, then internal $T$-models in sheaves need not be the same as sheaves of $T$-models-in-$Set$.  My intuition would be that the former, rather than the latter, is the more interesting and important notion.  For instance, a local ring in a topos of sheaves is a sheaf of rings whose _stalks_ are local, rather than a sheaf taking values in the category of local rings, and this is usually what people care about.  But since people have studied the other version, there must be important examples of it as well?

[[Urs Schreiber|Urs]]: okay, I have added this
to the above now -- so is the IPC-property business
really unnecessary for the examples above?

[[Mike Shulman|Mike]]: I'm pretty sure it is not.  Does anyone have any examples where the IPC-property business is important?
=--


#Construction#

## In terms of local isomorphisms ##

Encoding the [[Grothendieck topology]] on $S$ equivalently in a system of [[local isomorphism]]s, sheafification can be expressed as follows.

Write $Ho_{PSh(S)}$ for the [[homotopy category]] induced by letting weak equivalences be the [[local isomorphism]]s with respect to a Grothendieck topology on $S$ as described at [[category of sheaves]].

Let $F \in PSh(S)$ be a [[presheaf]] on $S$. Its **sheafification** is the presheaf

$$
  \bar F : U \mapsto Hom_{Ho(PSh(S))}(Y(U), F)
  \,,
$$

where $Y$ denotes the [[Yoneda embedding]]. This can be computed explicitly as

$$
  \bar F(U) 
  =
   \colim_{ \hat U \stackrel{local iso}{\to} U } 
   Hom_{PSh(S)}(\hat U, F)
  \,,
$$




#Remarks#

* For more on the role of sheafification see [[category of sheaves]].

* The notion of sheafification generalizes from [[presheaf]] [[Grothendieck topos|Grothendieck topoi]] to arbitrary [[topos|topoi]] with [[Lawvere-Tierney topology]]. See the last.

* The notion of sheafification also generalizes from the 1-categorical to the [[(infinity,1)-category|(infinity,1)-categorical]] context. See [[(infinity,1)-category of (infinity,1)-sheaves]]. 

#References#

The description of sheafification in terms of local isomorphisms is in section 16.3 (for [[Set]]-valued presheaves) and section 17.4 (for more general presheaves) of

* Kashiwara--Schapira, [[Categories and Sheaves]]

The description in terms of [[dense monomorphism]]s using [[Lawvere-Tierney topology]] is in section V.3 of

* Mac Lane, Moerdijk, [[Sheaves in Geometry and Logic]]

Extension of sheafification of presheaves with values in other categories has been advanced in

* A. Heller, K. A. Rowe, On the category of sheaves, Amer. J. Math. 84, 1962, 205-216.

* Barr, Grillet and Van Osdol, Exact categories and categories of sheaves, Lecture Notes in Math., Vol. 236, Springer, Berlin, 1971 

* A. Rosenberg, Almost quotient categories, sheaves and localizations, 181 p. Seminar on supermanifolds 25, University of Stockholm, D. Leites editor, 1988 (in Russian; partial remake in English exists)