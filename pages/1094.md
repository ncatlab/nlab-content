
#Definition#

Given a [[site]] $S$, every [[presheaf]] $F$ in $PSh(S) := [S^{op}, Set]$ is [[local isomorphism|locally isomorphic]] (weakly eqiuivalent) to a [[sheaf]] $\bar F$. This construction extends to a functor

$$
  \bar{(-)} : PSh(S) \to Sh(S)
  \,.
$$

This functor is **sheafification**. 

Sheafification is [[left adjoint]] to the [[stuff, structure, property|fully faithful forgetful]] [[injection|subcategory]] [[functor]] $i : Sh(S) \hookrightarrow PSh(S)$.

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


#References#

The description of sheafification in terms of local isomorphisms is in section 16.3 (for [[Set]]-valued presheaves) and section 17.4 (for more general presheaves) of

* Kashiwara-Schapira, [[Categories and Sheaves]]