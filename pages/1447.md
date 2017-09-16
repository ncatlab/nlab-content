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


+-- {: .un_defn}
###### Definition

Write $W$ for the class of morphism that are sent to isomorphism under $f^*$,

$$
  W = (f^*)^{-1}\{g: c\stackrel{\simeq}{\to} d \in Mor(E)\}
  \,.
$$

=--

+-- {: .un_prop}
###### Proposition

$E$ equipped with the class $W$ is a [[category with weak equivalences]], in that $W$ satisfies 2-out-of-3.

=--

+-- {: .proof}
###### Proof

Follows since isomorphisms satisfy 2-out-of-3.

=--


+-- {: .un_prop}
###### Proposition

For every object $a \in E$ the 

* the unit $\eta_a : a \to \bar a$ is in $W$;

* if $a$ is already in $F$ then the unit is already an isomorphism.

=--

+-- {: .proof}
###### Proof

This follows from the zig-zag identities
of the [[adjoint functor]]s. They say that

* for every $a \in E$ we have $(\bar a \stackrel{\bar \eta_a}{\to} \bar{\bar a} \stackrel{\simeq}{\to} \bar a) = Id_{\bar a}$

* for every $a \in F$ we have $(a \stackrel{\eta_a}{\to} \bar a \stackrel{\simeq}{\to} a)  = Id_a$

This implies the claim.

=--


+-- {: .un_defn}
###### Definition

An object $a \in E$ is **$W$-[[local object]]** if for every
$g : c \to d$ in $W$ the map

$$
  g^* : Hom_E(d,a) \stackrel{\simeq}{\to}
        Hom_E(c,a)
$$

obtained by precomposition is an isomorphism.

=--

+-- {: .un_prop}
###### Proposition

Every object $a \in F \hookrightarrow E$ is $W$-local.

=--

+-- {: .proof}
###### Proof

First notice that the existence of an isomorphism
$
  Hom_F(d,a) \simeq Hom_F(c,a)
$
is equivalent to the statement that for every diagram

$$
  \array{
     c &\stackrel{}{\to}& d
     \\
     \downarrow^{h}
     \\
     a
  }
$$

there is a unique extension

$$
  \array{
     c &\stackrel{}{\to}& d
     \\
     \downarrow^{h} & \swarrow
     \\
     a
  }
  \,.
$$

To see the existence of this extension, hit the original diagram with $f^*$ to get

$$
  \array{
     \bar c &\stackrel{\simeq}{\to}& \bar d
     \\
     \downarrow^{\bar h}
     \\
     \bar a \simeq a
  }
  \,.
$$

By the assumption that $c \to d$ is in $W$ the morphism $\bar c \to \bar d$ here is an isomorphism. By the assumption that $a$ is already in $F$ we have $\bar a \simeq a$ since the counit is an isomorphism. Therefore this diagram clearly has a unique extension

$$
  \array{
     \bar c &\stackrel{\simeq}{\to}& \bar d
     \\
     \downarrow^{\bar h} & \swarrow_{\exists ! k}
     \\
     \bar a \simeq a
  }
  \,.
$$

By the hom-isomorphism (using full faithfullness of $f_*$ to work entirely in $E$)

$$
  Hom_E(\bar d, a) \simeq Hom_E(d,a)
$$

this defines a morphism $k : d \to a$. Chasing $k$ through the naturality diagram of the hom-isomorphism

$$
  \array{
     Hom_E(\bar d, \bar a) &\stackrel{\simeq}{\to}& Hom_E(d,\bar a)
     \\
     \downarrow && \downarrow
     \\
     Hom_E(\bar c, \bar a) &\stackrel{\simeq}{\to}& Hom_E(c,\bar a)     
  }
  \,.
$$

shows that $k : d \to a$ does extend the original diagram. Again by the Hom-isomorphism, it is the unique morphism with this property.


=--

Conversely, for every $W$-local object we have
for every object $c$
$$
  Hom_E(c,a) \simeq Hom_E(\bar c,a)
  \,.
$$

To see this, use the proposition above which says that the  unit $\eta_c : c \to \bar c$ is in $W$. Then the claim follows from observing that by assumption of locality of $a$ every diagram

$$
  \array{
     c &\stackrel{\eta_c}{\to}& \bar c
     \\
     \downarrow^h
     \\
     a
  }
$$

has a unique extension $h'$. The map $h \mapsto h'$ is the desired isomorphism.

#References#

section VII, 4 of 

* Moerdijk-MacLane, _Sheaves in Geometry and logic_ 