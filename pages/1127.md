#Idea#

A _Grothendieck category_ is an [[abelian category]] $C$ such that all [[complex]]es in $C$ (with respect to a [[category with translation|translation]]) are [[quasi-isomorphism|quasi-isomorphic]] to [[injective object|homotopically injective]] complexes.

#Definition#

A **Grothendieck category** is an [[abelian category|abelian]] [[small category]]

* that admits a [[generator]];

* that admits small [[colimit]]s;

* such that small [[filtered category|filtered]] [[colimit]]s are [[exact functor|exact]].


#Properties#

A Grothendieck category $C$ satisfies the following properties.

* it admits small [[limit]]s;

* if a functor $F : C^{op} \to Set$ commutes with small [[limit]]s, the $F$ is [[representable functor|representable]];

* if a functor $F : C^{op} \to Set$  commutes with small [[colimit]]s, then $F$ has a [[right adjoint]].

* If $C$ is equipped with [[category with translation|translation]] $T : C \to C$, then for every [[complex]] $X \in Cplx(C)$ there exists a [[quasi-isomorphism]] of [[complex]]es $X \to I$ such that $I$ is [[injective object|homotopically injective]].

* it satisfies Pierre Gabriel's sup property: every small family of subobjects of a given object $X$ has a supremum which is a subobject of $X$

#Examples#

* For $R$ a ring, $Mod(R)$ is a Grothendieck category.

* For $C$ a [[small category|small]] [[abelian category]], the category $Ind(C)$ of [[ind-object]]s in $C$ is a Grothendieck category.

* for $C$ a Grothendieck category, the category $C_c$ of [[complex]]es in $C$ is again a Grothendieck category.

#References#

Grothendieck categories are mentioned at the end of section 8.3 in

* Kashiwara-Schapira, [[Categories and Sheaves]]

The relation to complexes is in section 14.1