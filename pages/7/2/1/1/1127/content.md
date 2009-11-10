#Idea#

_Grothendieck categories_ are those [[abelian category|abelian categories]] $C$

* such that for [[presheaf|presheaves]] on a [[site]] with values in $C$ there is an existence theorem for the  [[sheafification]] functor;

* such that all [[complex]]es in $C$ (with respect to a [[category with translation|translation]]) are [[quasi-isomorphism|quasi-isomorphic]] to [[injective object|homotopically injective]] complexes (so that [[derived functor on a derived category|derived functor]] can be computed on homotopically injective replacements).


#Definition#

In terms of the AB$n$ hierarchy discussed at [[additive and abelian categories]] we have

A **Grothendieck category** is an [[additive and abelian categories|AB5-category]] which has a [[generator]].

This means that a **Grothendieck category** is an [[abelian category|abelian]] [[small category]]

* that admits a [[generator]];

* that admits small [[colimit]]s;

* such that small [[filtered category|filtered]] [[colimit]]s are _exact_ in the following sense:

  * for $I$ a [[direction|directed set]] and $0 \to A_i \to B_i \to C_i \to 0$ an [[exact sequence]] for each $i \in I$, then $0 \to colim_i A_i \to colim_i B_i \to colim_j B_j \to 0$ is also an [[exact sequence]].

Dually a *co-Grothendieck category* is an AB5$^*$ category 
with a [[cogenerator]]. The category of abelian groups is not a co-Grothendieck category. Any abelian category which is simultaneously Grothendieck and co-Grothendieck has just a single object (see Freyd's book, p.116). 

#Properties#

A Grothendieck category $C$ satisfies the following properties.

* it admits small [[limit]]s;

* if a functor $F : C^{op} \to Set$ commutes with small [[limit]]s, the $F$ is [[representable functor|representable]];

* if a functor $F : C^{op} \to Set$  commutes with small [[colimit]]s, then $F$ has a [[adjoint functor|right adjoint]].

* If $C$ is equipped with [[category with translation|translation]] $T : C \to C$, then for every [[complex]] $X \in Cplx(C)$ there exists a [[quasi-isomorphism]] of [[complex]]es $X \to I$ such that $I$ is [[injective object|homotopically injective]].

* it satisfies Pierre Gabriel's sup property: every small family of subobjects of a given object $X$ has a [[supremum]] which is a subobject of $X$

#Examples#

* For $R$ a ring, $Mod(R)$ is a Grothendieck category.

* For $C$ a [[small category|small]] [[abelian category]], the category $Ind(C)$ of [[ind-object]]s in $C$ is a Grothendieck category.

* for $C$ a Grothendieck category, the category $C_c$ of [[complex]]es in $C$ is again a Grothendieck category.

#References#

Grothendieck categories are mentioned at the end of section 8.3 in

* Kashiwara--Schapira, [[Categories and Sheaves]]

The relation to complexes is in section 14.1.

See also the book 

* Peter Freyd, Abelian categories, Harper 1966. 