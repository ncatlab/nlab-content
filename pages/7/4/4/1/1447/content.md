#Idea#

A **geometric embedding** is the right notion of embedding or inclusion of [[topos|topoi]] $F \hookrightarrow E$.

Notably the inclusion $Sh(S) \hookrightarrow PSh(S)$ of a [[category of sheaves]] into its [[presheaf]] [[topos]] or more generally the inclusion $Sh_j E \hookrightarrow E$ of sheaves in a topos $E$ into $E$ itself, is a geometric embedding. Actually every geometric embedding is of this form, up to equivalence of [[topos|topoi]].

Another perspective is that a geometric embedding $F \hookrightarrow E$ is the [[localization]]s of $E$ at the class $W$ or morphisms that the [[left adjoint]] $E \to F$ sends to isomorphisms in $F$.

#Definition#

For $F$ and $E$ two [[topos|topoi]], a [[geometric morphism]]

$$
  F \stackrel{f}{\to}
  E
  \;\;\;\;
  F \stackrel{\stackrel{f_*}{\to}}{\stackrel{f^*}{\leftarrow}} E
$$

is a **geometric embedding** if the following equivalent conditions are satisfied

* the [[direct image]] functor $f_*$ is [[full and faithful functor|full and faithful]] (so that $F$ is a full [[subcategory]] of $E$);

* the counit $\epsilon :  f^* f_* \to Id_{F}$ of the [[adjoint functor|adjunction]] $(f^* \dashv f_*)$ is an [[isomorphism]]

* there is a [[Lawvere-Tierney topology]] on $E$ and an [[equivalence of categories]] $e : F \stackrel{\simeq}{\to} Sh_j E$ such that the diagram of geometric morphisms $\array{ F &\stackrel{f_*}{\to}& E \\ & {}_{e}\searrow^\simeq & \uparrow^{i} \\ && Sh_j E}$ commutes up to natural isomorphism $e^* i^* \simeq f^*$

That the first two conditions are equivalent is standard, that the third one is equivalent to the first two is for instance corollary 7 in section VII, 4 of 

* MacLane-Moerdijk, _Sheaves in geometry and logic_


#Details#

We unwrap some consequences of this definition.

Write $\eta : Id_E \to f_* f^*$ for the unit of the
adjunction. 

Since $f_*$ is fully faithful we will identify objects and
morphism of $F$ with their images in $E$. To further trim down the notation write $\bar {(-)} := f^*$ for the left adjoint.


Then the zig-zag identities say that

* for every $a \in E$ we have $(\bar a \stackrel{\bar \eta_a}{\to} \bar{\bar a} \stackrel{\simeq}{\to} \bar a) = Id_{\bar a}$

* for every $a \in F$ we have $(a \stackrel{\eta_a}{\to} \bar a \stackrel{\simeq}{\to} a)  = Id_a$

If we write $W$ for the class of morphisms in $E$ which are sent to isomorphisms by $f^*$, then this says that

* for every $a$ the unit $\eta_a : a \to \bar a$ is in $W$;

* for $a$ in $F$ the unit is already an isomorphism.



#References#

section VII, 4 of 

* Moerdijk-MacLane, _Sheaves in Geometry and logic_ 