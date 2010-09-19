
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents
{:toc}

## Idea

A **geometric embedding** is the right notion of embedding or inclusion of [[topoi]] $F \hookrightarrow E$, i.e. of [[subtopos]]es.

Notably the inclusion $Sh(S) \hookrightarrow PSh(S)$ of a [[category of sheaves]] into its [[presheaf]] [[topos]] or more generally the inclusion $Sh_j E \hookrightarrow E$ of sheaves in a topos $E$ into $E$ itself, is a geometric embedding. Actually every geometric embedding is of this form, up to equivalence of [[topos|topoi]].

Another perspective is that a geometric embedding $F \hookrightarrow E$ is the [[localizations]] of $E$ at the class $W$ or morphisms that the [[left adjoint]] $E \to F$ sends to isomorphisms in $F$.


## Definition

For $F$ and $E$ two [[topos|topoi]], a [[geometric morphism]]

$$
  F \stackrel{f}{\to}
  E
  \;\;\;\;
  F \stackrel{\stackrel{f_*}{\to}}{\underset{f^*}{\leftarrow}} E
$$

is a **geometric embedding** if the following equivalent conditions are satisfied

* the [[direct image]] functor $f_*$ is [[full and faithful functor|full and faithful]] (so that $F$ is a full [[subcategory]] of $E$);

* the counit $\epsilon :  f^* f_* \to Id_{F}$ of the [[adjoint functor|adjunction]] $(f^* \dashv f_*)$ is an [[isomorphism]]

* there is a [[Lawvere-Tierney topology]] on $E$ and an [[equivalence of categories]] $e : F \stackrel{\simeq}{\to} Sh_j E$ such that the diagram of geometric morphisms $\array{ F &\stackrel{f_*}{\to}& E \\ & {}_{e}\searrow^\simeq & \uparrow^{i} \\ && Sh_j E}$ commutes up to natural isomorphism $e^* i^* \simeq f^*$

That the first two conditions are equivalent is standard, that the third one is equivalent to the first two is for instance corollary 7 in section VII, 4 of 

* MacLane-Moerdijk, _Sheaves in geometry and logic_


## Relation to localization

There is a close relation between geometric embedding and
[[localization]]. 

Let $f : F \hookrightarrow E$ be a geometric embedding
and let $W \subset Mor(E)$ be the class of morphisms sent by $f^*$ to isomorphisms in $F$.

+-- {: .un_theorem}
###### Theorem

We have:
* $F$ is equivalent to the [[localization]] $E[W]^{-1}$;
* $F$ is equivalent to the full [[subcategory]] of $E$ on $W$-[[local objects]].

=--

This fact connects for instance the description of [[sheafification]] in terms of geometric embedding $Sh(S) \hookrightarrow PSh(S)$ as described for instance in 

* MacLane-Moerdijk, [[Sheaves in Geometry and Logic]]

with that in terms of [[localization]] at [[local isomorphisms]], as described in

* Kashiwara-Schapira, [[Categories and Sheaves]].

Moreover, this is the basis on which sheafification is generalized to [[(∞,1)-sheafification]] in

* [[Jacob Lurie]], [[Higher Topos Theory]] .

The following gives a detailed proof of the above assertion.

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

$W$ is a left [[calculus of fractions|multiplicative system]].

=--

+-- {: .proof}
###### Proof

This follows using the fact that $f^*$ is left exact and hence preserves finite limits.

In more detail:

We have already seen in the previous proposition that

* every isomorphism is in $W$;

* $W$ is closed under composition.

It remains to check the following points:

Given any 

$$
  \array{
     && a
     \\
     && \downarrow^w
     \\
     b &\stackrel{h}{\to}& c 
  }
$$

with $w \in W$, we have to show that there is

$$
  \array{
     d &\to& a
     \\
     \downarrow^{w'} && \downarrow^w
     \\
     b &\stackrel{h}{\to}& c 
  }
$$

with $w' \in W$.

To get this, take this to be the [[pullback]] diagram, 
$w' := h^* w$. 
Since $f^*$ preserves pullbacks, it follows that

$$
  \array{
     \bar d &\to& \bar a
     \\
     \downarrow^{\bar w'} && \downarrow^{\bar w}
     \\
     \bar b &\stackrel{\bar h}{\to}& \bar c 
  }
$$

is a pullback diagram in $F$ with $\bar w' = \bar h^* \bar w$. But by assumption $\bar w$ is an isomorphism. Therefore $\bar w'$ is an isomorphism, therefore $w'$ is in $W$.


Finally for every

$$
  a \stackrel{\stackrel{r}{\to}}{\stackrel{s}{\to}} b \stackrel{w}{\to} c
$$

with $w \in W$ such that the two composites coincide,
we need to find

$$
  d \stackrel{w'}{\to} a \stackrel{\stackrel{r}{\to}}{\stackrel{s}{\to}} b 
$$

with $w' \in W$ such that the composites again coincide.

To get this, take $w'$ to be the [[equalizer]]
of the two morphisms. Sending everything with $f^*$ to $F$ we find from 

$$
  \bar a \stackrel{\stackrel{\bar r}{\to}}{\stackrel{\bar s}{\to}} b \stackrel{\bar w}{\to} c
$$

that $\bar r = \bar s$, since $\bar w$ is an isomorphism. This implies that $\bar w'$ is the equalizer

$$
  \bar d \stackrel{\bar w'}{\to} a \stackrel{\stackrel{\bar r}{\to}}{\stackrel{\bar s}{\to}} b 
$$

of two equal morphism, hence an identity. So $w'$ is in $W$.


=--




+-- {: .un_prop}
###### Proposition

For every object $a \in E$ 

* the unit $\eta_a : a \to \bar a$ is in $W$;

* if $a$ is already in $F$ then the unit is already an isomorphism.

=--

+-- {: .proof}
###### Proof

This follows from the zig-zag identities
of the [[adjoint functors]]. 

$$
  \array{
     & 
     \nearrow &\Downarrow^{\eta}& \searrow^{Id_E}
     \\
     E 
       &\stackrel{\bar{(-)}}{\to}& 
     F
       &\hookrightarrow&
     E
       &\stackrel{\bar{(-)}}{\to}& 
     F
     \\
     &&&
     \searrow &\Downarrow^{\simeq}& \nearrow_{Id_F}
  }
  \;\;\;\;
  =
  \;\;\;\;
  \array{
     & \nearrow \searrow^{\bar{(-)}}
    \\
    E
    &\Downarrow^{Id}&
    F
    \\
    & \searrow \nearrow_{\bar{(-)}}
  }
$$

and

$$
  \array{
     &&& 
     \nearrow &\Downarrow^{\eta}& \searrow^{Id_E}
     \\
     F 
       &\hookrightarrow&
     E
       &\stackrel{\bar{(-)}}{\to}& 
     F
       &\hookrightarrow&
     E
     \\
     &
     \searrow &\Downarrow^{\simeq}& \nearrow_{Id_F}
  }
  \;\;\;\;
  =
  \;\;\;\;
  \array{
     & \nearrow \searrow
    \\
    F
    &\Downarrow^{Id}&
    E
    \\
    & \searrow \nearrow
  }
$$


In components they say that

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

Up to isomorphism, the $W$-local objects are precisely the objects of $F$ in $E$

=--

+-- {: .proof}
###### Proof

First assume that $a \in F$. We need to show that $a$ is $W$-local.

Notice that the existence of the required isomorphism
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

So $a \in F$ is $W$-local.


Now for the converse, assume that a given $a$ is $W$-local. 

By one of the above propositions we know that the unit
$\eta_a : a \to \bar a$ is in $W$, so by the $W$-locality of
$a$ it follows that

$$
  \array{
     a &\stackrel{\eta_a}{\to}& \bar a
     \\
     \downarrow^{Id_a}
     \\
     a
  }
$$

has an extension

$$
  \array{
     a &\stackrel{\eta_a}{\to}& \bar a
     \\
     \downarrow^{Id_a} & \swarrow_{\rho_a}
     \\
     a
  }
  \,.
$$

By the 2-out-of-3 property of $W$ shown in one of the above propositions, (using that $Id_a$, being an isomorphism, is in $W$) it follows that $\rho_a : \bar a \to a$ is in $W$. 

Since $\bar a$ is in $F$ and therefore $W$-local by the above, it follows that also

$$
  \array{
     \bar a &\stackrel{\rho_a}{\to}& a
     \\
     \downarrow^{Id_{\bar a}}
     \\
     \bar a
  }
$$

has an extension

$$
  \array{
     \bar a &\stackrel{\rho_a}{\to}& a
     \\
     \downarrow^{Id_{\bar a}} & \swarrow_{\lambda_a}
     \\
     \bar a
  }
  \,.
$$

So $\eta_a$ has a left inverse $\rho_a$ which itself has a left inverse $\lambda_a$. It follows that $\rho_a$ is also a right inverse to $\eta_a$, since

$$
  \begin{aligned}
    \stackrel{\rho_a}{\to}
    \stackrel{\eta_a}{\to}
    & =    
    \stackrel{\rho_a}{\to}
    \stackrel{\eta_a}{\to}
    \underbrace{
      \stackrel{\rho_a}{\to} 
       \stackrel{\lambda_a}{\to}
    }_{Id}
   \\
    & = 
    \stackrel{\rho_a}{\to}
    \underbrace{
      \stackrel{\eta_a}{\to}
      \stackrel{\rho_a}{\to} 
    }_{Id}
    \stackrel{\lambda_a}{\to}
    \\
    &=
    \stackrel{\rho_a}{\to}
    \stackrel{\lambda_a}{\to}
    \\
    &=
    Id
  \end{aligned}
  \,.
$$

So if $a$ is $W$-local we find that $\eta_a : a \to \bar a$ is an isomorphism, hence that $a$ is isomorphic to an object of $F$. 

=--

+-- {: .un_cor}
###### Corollary

$F$ is equivalent to the full [[subcategory]] $E_{W-loc}$ of $E$ on $W$-[[local objects]].

=--

+-- {: .proof}
###### Proof

By standard reasoning (e.g. [[Categories and Sheaves|KS lemma 1.3.11]]) there is a functor $F \to E_{W-loc}$ and a natural isomorphism

$$
  \array{
     F &&\hookrightarrow&& E
     \\
     & \searrow &\Downarrow^{\simeq}& \nearrow
     \\
     && E_{W-loc}
  }
  \,.
$$

Since $F \hookrightarrow E$ and $E_{W-loc} \hookrightarrow E$ are [[full and faithful functor|full and faithful]], so is $F \to E_{W-loc}$. Since by the above it is also essentially surjective, it establishes the equivalence $F \simeq E_{W-loc}$.

=--


+-- {: .un_prop}
###### Proposition

$F$ is [[equivalence of categories|equivalent]] to the [[localization]] $E[W^{-1}]$ of $E$ at $W$.

=--

+-- {: .proof}
###### Proof

By one of the above propositions we know that
$W$ is a [[calculus of fractions|left multiplicative systems]]. 

This implies that the localization $E[W^{-1}]$ is (equivalent to) the category with the same objects as $E$, and with [[hom-sets]] given by

$$
  Hom_{E[W^{-1}]}(a,b)
  =
  \underset{a' \stackrel{p \in W}{\to}a}{colim} Hom_E(a',b)
  \,.
$$

There is an obvious candidate for a functor

$$
  F \to E[W^{-1}] 
$$

given on objects by the usual embedding by $f_*$ and on morphism by the map which regards a morphism trivially as a [[span]] with left leg the identity

$$
  (a \to b) 
   \;\;
   \mapsto 
   \;\;
   \left(
   \array{
     a &\to& b
     \\
     \downarrow^{Id_a}
     \\
     a
  }
  \right)
  \,.
$$

For this to be an [[equivalence of categories]] we need to show that this is a [[essentially surjective functor|essentially surjective]] and [[full and faithful functor]].

To see essential surjectivity, let $a$ be any object in $E$ and let $\eta_a : a \to \bar a$ be the component of the unit of our adjunction on $a$, as above. By one of the above propositons, $\eta_a$ is in $W$. This means that the span

$$
  \array{
    a &\stackrel{Id_a}{\to}& a
    \\
    \downarrow^{\eta_a}
    \\
    \bar a
  }
$$

represents an element in $Hom_{E[W^{-1}]}(\bar a,a)$, and this element is clearly an isomorphism: the inverse is represented by

$$
  \array{
    a &\stackrel{\eta_a}{\to}& \bar a
    \\
    \downarrow^{Id_a}
    \\
    a
  }
  \,.
$$

Since every $\bar a$ is in the image of our functor, this shows that it is essentially surjective.

To see fullness and faithfulness, let $a, b\in F$ be any two objects. By one of the above propositions this means in particular that $b$ is a $W$-[[local object]]. As discussed above, this means that every span

$$
  \array{
    a' &\to& b
    \\
    \downarrow^w
    \\
    a
  }
$$

with $w \in W$ has a unique extension

$$
  \array{
    a' &\to& b
    \\
    \downarrow^w & \nearrow
    \\
    a
  }
  \,.
$$

But this implies that in the colimit that defines the [[hom-set]] of $E[W^{-1}]$ all these spans are identified
with spans whose left leg is the identiy. And these are clearly in bijection with the morphisms in $Hom_E(a,b) \simeq Hom_F(a,b)$ so that indeed

$$
  Hom_{E[W^{-1}]}(a,b)
  \simeq
  Hom_{F}(a,b)  
$$

for all $a,b \in F$. Hence our functor is also full and faithful and therefore define an [[equivalence of categories]]

$$
  F \stackrel{\simeq}{\to} E[W^{-1}]
  \,.
$$

=--


## References

section VII, 4 of 

* [[Saunders Mac Lane]] and [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ 


[[!redirects geometric embeddings]]