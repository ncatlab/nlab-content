
> This entry contains one chapter of _[[geometry of physics]]_.

> previous chapters: _[[geometry of physics -- homotopy types|homotopy types]]_, _[[geometry of physics -- smooth homotopy types|smooth homotopy types]]_

> next chapters, _[[geometry of physics -- principal bundles|principal bundles]]_, _[[geometry of physics -- representations and associated bundles|representations and associated bundles]]_

***

#Contents#
* table of contents
{:toc}


## Groups

The modern mathematical terminology _group_ is short for _group of [[symmetries]]_ (e.g. [Klein 1872](Klein+geometry#Klein1872)). Mathematicians and physicist tend to marvel at the ubiquity and profoundness that the concept of symmetry groups has turned out to exhibit since its conception in the 19th century. Indeed it is a fundamental concept in a sense whose full depth becomes clear (only) in [[homotopy theory]]: _groups_ are equivalently the [[pointed object|pointed]] [[connected object in an (infinity,1)-topos|connected]] [[homotopy types]].

In traditional literature this fact is fully appreciated typically only in rather advanced corners of [[algebraic topology]], and even that mostly just somewhat secretly. But while it is true that this fact has very sophisticated consequences, at its heart it is a simple fundamental fact that is visible and useful already in elementary [[group theory]] and [[representation theory]].

We being in 

* _[1-Groups](#1Groups)_

with a discussion of the simplest case of ordinary discrete groups from this natural perspective of regarding them as pointed connected [[homotopy 1-types]], their [[delooping]] [[groupoids]]. Then we gradually generalize to the study of [[infinity-group]] objects in general [[(infinity,1)-toposes]].

### Model Layer

#### 1-Groups
 {#1Groups}

##### Discrete groups as pointed connected groupoids

We discuss how, via [[looping and delooping]], [[discrete groups]] are equivalent to pointed connected [[groupoids]].

Write 

* [[Grpd]] for the [[(2,1)-category]] of [[groupoids]] ([[objects]] are [[groupoids]], [[1-morphisms]] are [[functors]] between these and [[2-morphisms]] are [[natural transformations]] between those, which are nessecarily [[natural isomorphisms]]), 

* [[Grp]] for the [[1-category]] of [[groups]] ([[discrete groups]]), also regarded as a [[(2,1)-category]]; 

* $Grpd^{\ast/}$ for the $(2,1)$-category of [[pointed objects]] in [[Grpd]], 

* $Grpd_{\geq 1} \hookrightarrow Grpd$ for the [[full sub-(infinity,1)-category|full sub-(2,1)-category]] on [[connected object in an (infinity,1)-topos|connected]] groupoids, those for which $\pi_0 \simeq \ast$;

* $Grp^{\ast/}_{\geq 1}$ for the [[pointed objects]] in connected groupoids.

* $\pi_1(X,x) \in Grp$ for the [[fundamental group]] of a pointed groupoid $(\ast \stackrel{x}{\to} X) \in Grpd^{\ast/}$ at the given basepoint.

* $\mathbf{B}G \in Grpd$, given a group $G$, for the groupoid $(G\stackrel{\longrightarrow}{\longrightarrow} \ast)$, with composition given by the product in the group. There are two possible choices of conventions, we agree that 

  $$
    \array{
      && \ast
      \\
      & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
      \\
      \ast && \underset{g_1 \cdot g_2}{\longrightarrow} && \ast
    }
    \,.
  $$

+-- {: .num_prop #SkeletalRepresentativesForConnectedGroupoids}
###### Proposition

The [[(2,1)-category]] $Grp_{\geq 1}$ of connected groupoids is equivalent to its [[full sub-(infinity,1)-category|full sub-(2,1)-category]] on those objects of the form $\mathbf{B}G$, for $G$ a group.

=--

+-- {: .proof}
###### Proof

Given a connected groupoid $X$, pick any basepoint $x\in X$ and consider the canonical inclusion $\mathbf{B}\pi_1(X,x) \longrightarrow X$. By construction this is [[fully faithful functor|fully faithful]] and by assumption of connectedness it is [[essentially surjective functor|essentially surjective]], hence it is an [[equivalence of groupoids]].

=--

+-- {: .num_prop #HomsBetweenBGs}
###### Proposition

The [[hom-groupoids]] between connected groupoids with fundamental groups $G$ and $H$, respectively, are equivalent to the [[action groupoids]] of the set of group [[homomorphisms]] $G \to H$ [[action|acted]] on by [[conjugation]] with elements of $H$: 

$$
  Grpd(\mathbf{B}G, \mathbf{B}H)
  \simeq
   Grp(G,H)//_{ad}H
$$

Given two group homomorphisms $\phi_1, \phi_2 \colon G \longrightarrow H$ then an [[isomorphism]] between them in this hom-groupoid is an element $h \in H$ such that 

$$
  \phi_2 = Ad_h \circ \phi_1 \coloneqq h^{-1}\cdot \phi_1(-) \cdot h
  \,.
$$

=--

+-- {: .proof}
###### Proof


By direct inspection of the naturality square for the [[natural transformations]] which are the morphisms in $Grpd(\mathbf{B}G, \mathbf{B}H)$:

$$
  \array{
    \ast && && \ast &\stackrel{h}{\longrightarrow}& \ast
    \\
    \downarrow^{\mathrlap{g_1}} && && \downarrow^{\mathrlap{\phi_1(g_1)}} && 
    \downarrow^{\mathrlap{\phi_2(g_1)}}
    \\
    \ast && && \ast &\stackrel{h}{\longrightarrow}& \ast
    \\
    \downarrow^{\mathrlap{g_2}}
    && &&
    \downarrow^{\mathrlap{\phi_1(g_2)}}
    &&
    \downarrow^{\mathrlap{\phi_2(g_2)}}
    \\
    \ast && && \ast &\stackrel{h}{\longrightarrow}& \ast
  }
  \,.
$$

=--


+-- {: .num_remark #piAs2Functor}
###### Remark

The operation of forming $\pi_1$ is equivalently the operation of forming the [[homotopy fiber product]] of the point inclusion with itself, and hence extends to a [[(2,1)-functor]]

$$
  \pi_1 \colon Grpd^{\ast/} \longrightarrow Grp
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Restricted to [[connected object in an (infinity,1)-topos|connected groupoids]] among the pointed groupoids, the functor $\pi_1 \colon Grpd^{\ast/}_{\geq 1} \longrightarrow Grp$ of remark \ref{piAs2Functor} is an [[equivalence of (2,1)-categories]].

=--

+-- {: .proof}
###### Proof

It is clear that the functor is essentially surjective: for $G$ any [[group]] then  $\pi_1(\mathbf{B}G,\ast) \simeq G$.

The more interesting point to notice is that $\pi_1$ is indeed a fully faithful [[(2,1)-functor]], in that for any $(X,x), (Y,y) \in Grpd^{\ast/}_{\geq 1}$ then the functor

$$
  (\pi_1)_{X,Y}
  \colon
  Grpd^{\ast/}((X,y),(Y,y))
  \longrightarrow
  Grp(\pi_1(X,x), \pi_1(Y,y))
$$

is an [[equivalence of groupoids|equivalence]] of [[hom-groupoids]]. By prop. \ref{SkeletalRepresentativesForConnectedGroupoids} it is sufficient to check this for $X = \mathbf{B}G$ and $Y = \mathbf{B}H$ with their canonical basepoints, hence to check that for any two groups  $G,H$ the functor

$$
  (\pi_1)_{X,Y}
  \;\colon\;
  Grpd^{\ast/}((\mathbf{B}G,\ast),(\mathbf{B}H,\ast))
  \longrightarrow
  Grp(G,H)
$$

is an equivalence. 

To see this, observe that, by definition of [[pointed objects]] via the [[undercategory]] under the point, a morphism in $Grpd^{\ast/}$ between groupoids of this form $\mathbf{B}(-)$ is a diagram in $Grp$ (unpointed) of the form

$$
  \array{
    && \ast
    \\
    & \swarrow &\swArrow_{h}& \searrow
    \\
    \mathbf{B}G
    &&
    \underset{\mathbf{B}\phi}{\longrightarrow}
    &&
    \mathbf{B}H
  }
$$

where the [[natural isomorphism]] is equivalently just the choice of an element $h \in H$. Hence these morphisms are pairs $(\phi,h)$ of a group homomorphism and an element of the domain. 

We claim that the [[(2,1)-functor]] $\pi_1$ takes such $(\phi,h)$ to the homomorphism $Ad_{h^{-1}} \circ \phi \;\colon\; G \longrightarrow H$. To see this, consider via remark \ref{piAs2Functor} this functor as forming loops:


$$
  \pi_1(\mathbf{B}G,\ast)
  =
  \left\{
    \array{
      && \ast
      \\
      & \swarrow && \searrow
      \\
      \ast && \swArrow_{\mathrlap{g}} && \ast
      \\
      & \searrow && \swarrow
      \\
      && \mathbf{B}G
    }
  \right\}_{g\in G}
  \,.
$$

This shows that on a morphism as above this acts by forming the [[pasting]]

$$
  \array{
    && \ast
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\mathrlap{g}} && \ast
    \\
    & \searrow && \swarrow &\swArrow_{\mathrlap{h}}& \searrow
    \\
    && \mathbf{B}G && \underset{\phi}{\longrightarrow} && \mathbf{B}H
  }
  \;\;\;\;
  =
  \:\;\;\;
  \array{
    && && \ast
    \\
    && & \swarrow && \searrow
    \\
    && \ast && \swArrow_{\mathrlap{h\phi(g)h^{-1}}} && \ast
    \\
    & \swarrow & \swArrow_{\mathrlap{h}} & \searrow && \swarrow 
    \\
    \mathbf{B}G && \underset{\phi}{\longrightarrow} && \mathbf{B}H
  }
  \,.
$$

Unwinding the [[whiskering]] of [[natural transformations]] here, the claim follows, as indicated by the label of the upper 2-morphisms on the right.


One observes now that these extra labels $h$ are precisely the information that "trivializes" the conjugation action which in prop. \ref{HomsBetweenBGs} prevents the bare set of group homomorphism: a [[2-morphism]] $(\phi_1, h_1) \Rightarrow (\phi_2,h_2)$ in $Grp^{\ast/}$  is a natural isomorphism of groupoids

$$
  \array{
    \mathbf{B}G
    &\stackrel{\phi_1}{\longrightarrow}& 
    \mathbf{B}H
    \\
    {}^{\mathllap{id}}\downarrow &\Downarrow^{\mathrlap{h}}& \downarrow^{\mathrlap{id}}
    \\
    \mathbf{B}G
    &\underset{\phi_2}{\longrightarrow}& 
    \mathbf{B}H    
  }
$$

(encoding a conjugation relation $\phi_2 = Ad_{h} \circ \phi_1$ as above) such that we have the [[pasting]] relation

$$
  \array{
    && \ast
    \\
    & \swarrow &\swArrow_{h_1}& \searrow
    \\
    \mathbf{B}G
    &&
    \stackrel{\phi_1}{\longrightarrow}
    &&
    \mathbf{B}H
    \\
    {}^{\mathllap{id}}\downarrow && \Downarrow^{\mathrlap{h}} && \downarrow^{\mathrlap{id}}
    \\
    \mathbf{B}G
    &&\underset{\phi_2}{\longrightarrow} && 
    \mathbf{B}H    
  }
  \;\;\;\;\;
  =
  \;\;\;\;\;  
  \array{
    && \ast
    \\
    & \swarrow &\swArrow_{h_2}& \searrow
    \\
    \mathbf{B}G
    &&
    \underset{\phi_2}{\longrightarrow}
    &&
    \mathbf{B}H
  }
  \,.
$$

But this says in components that $h_2 = h_1\cdot h$. Hence there is a _at most one_ morphism in $Grpd^{\ast/}((\mathbf{B}G,\ast),(\mathbf{B}H,\ast))$ from $(\phi_1,h_1)$ to $(\phi_2,h_2)$: it exists if $\phi_2 = Ad_h \circ \phi_1$ and $h_2 = h_1\cdot h$.

But since, by the previous argument, the functor $\pi_1$ takes $(\phi_1,h_1)$ to $Ad_{h_1^{-1}} \circ \phi_1$, this means that such a morphism exists precisely if both $(\phi_1,h_1)$ and $(\phi_2,h_2)$ are taken to the same group homomorphism by $\pi_1$

$$
  Ad_{h_2^{-1}} \circ \phi_2
  =
  Ad_{h^{-1}\cdot h_1^{-1}}\circ \phi_2
  = 
  Ad_{h_1^{-1}} \circ \phi_1
  \,.
$$

This establishes that $\pi_1$ is alspo an equivalence on all [[hom-groupoids]].

=--

This proof also shows that $\mathbf{B}(-)$ is in fact the inverse equivalence:

+-- {: .num_cor}
###### Corollary

There is an [[equivalence of (2,1)-categories]] between pointed connected groupoids and plain groups

$$  
  Grp
  \stackrel{\underoverset{\simeq}{\pi_1 = \Omega_\ast}{\longleftarrow}}{\underset{\mathbf{B}}{\longrightarrow}}
  Grpd^{\ast/}_{\geq 1}
$$

given by forming [[loop space objects]] and by forming deloopings.

=--


##### Discrete group cohomology

One of the remarkable conceptual simplifications brought about by general [[homotopy theory]] pertains to the general concept of [[cohomology]]: effectively every flavor of cohomology that has been considered turns out to be nothing but the theory of [[derived hom space|(infinity,1)-categorical hom spaces]] in a suitable [[(infinity,1)-topos]].

Specifically for the case of [[group cohomology]], this is the following simple statement.


Let $A$ be an [[abelian group]]. For $n \in \mathbb{N}$ write

$$
  (\mathbf{B}^n A)_\bullet \in KanCplx
$$

for the [[Kan complex]] underlying the [[simplicial group]] which is the image of the [[chain complex]] $A[-1]$ concentrated on $A$ in degree $n$ under the [[Dold-Kan correspondence]] $DK \colon Ch_{\bullet \geq 0}(Ab)\stackrel{\simeq}{\longrightarrow} sAb \stackrel{forget}{\longrightarrow} KanCplx$

$$
  (\mathbf{B}^n A)_\bullet
  \coloneqq
  DK(A[-n])
  \,.
$$

For $G$ any [[discrete group]], not necessarily [[abelian group|abelian]], write

$$
  (\mathbf{B}G)_\bullet \in KanCplx
$$

for the [[nerve]] of the [[groupoid]] (G\stackrel{\longrightarrow}{\longrightarrow} \ast).

See at _[[geometry of physics -- homotopy types]]_ for detailed discussion of these two constructions.

+-- {: .num_prop}
###### Proposition/Definition

Given a [[discrete group]] $G$, then a degree-$n$ [[cocycle]] in [[group cohomology]] of $G$ with [[coefficients]] in $A$ is equivalently a morphism

$$
  (\mathbf{B}G)_\bullet \longrightarrow (\mathbf{B}^n A)_\bullet
  \,.
$$

A [[homotopy]] between two such morphisms is equivalently a [[coboundary]] between two such cocycles.

The [[group cohomology]] [[cohomology group|group]] of $G$ with coefficients in $A$ is the [[equivalence classes]] of cocycles modulo coboundaries, hence is the connected components of the [[hom-groupoid]]:

$$
  H^n_{Grp}(G,A)
  \simeq
  \pi_0 Hom(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

=--

It is instructive to spell this out in low degree.

+-- {: .num_prop #2CocyclesAndCoboundaries}
###### Proposition

Let $G$ be a [[discrete group]] and $A$ an [[abelian group|abelian]] [[discrete group]], regarded as being equipped with the trivial $G$-[[action]].

Then a **group 2-[[cocycle]]** on $G$ with coefficients in $A$ is a [[function]]

$$
  c \colon G \times G \to A
$$

such that for all $(g_1, g_2, g_3) \in G \times G \times G$ it satisfies the [[equation]]

\[
  \label{2CocycleConditionForCentralExtension}
  c(g_1, g_2)
  -
  c(g_1, g_2 \cdot g_3)
  +
  c(g_1 \cdot g_2, g_3)
  - 
  c(g_2, g_3)
  = 
  0
  \;\;\;\; \in A
\]

(called the **group 2-cocycle condition**). 

For $c, \tilde c$ two such cocycles, a **[[coboundary]]** $h \colon c \to \tilde c$ between them is a [[function]]

$$
  h \colon G \to A
$$

such that for all $(g_1,g_2) \in G \times G$ the [[equation]]

\[
  \label{Group2CoboundaryEquation}
  \tilde c(g_1,g_2)
  = 
  c(g_1,g_2) + (d h)(g_1,g_2)
\]

holds in $A$, where

$$
  (d h)(g_1, g_2) \coloneqq h(g_1 g_2) - h(g_1) - h(g_2)
$$

is the **group 2-coboundary** encoded by $h$.

The degree-2 **group cohomology** is the set 

$$
  H^2_{Grp}(G,A) = 2Cocycles(G,A) / Coboundaries(G,A)
$$

of [[equivalence classes]] of group 2-cocycles modulo group 2-coboundaries. This is itself naturally an [[abelian group]] under pointwise addition of cocycles in $A$

$$
  [c_1] + [c_2] = [c_1 + c_2]
$$

where

$$
  c_1 + c_2 \colon (g_1, g_2) \mapsto c_1(g_1,g_2) + c_2(g_1, g_2)
  \,.
$$
   

=--

+-- {: .proof}
###### Proof

The 2-simplices in $(\mathb{B}G)_\bullet$ are 

$$
  (\mathbf{B}G)_2
  =
  \left\{
  \left.
  \array{
    && {*}
    \\
    & {}^{g_1}\nearrow && \searrow^{g_2}
    \\
    {*}
    &&\stackrel{g_1 g_2}{\to}&& {*}
  }
  \right|
  g_1, g_2 \in G
  \right\}
  \,,
$$

and the 3-simplices are 

$$
  (\mathbf{B}G)_3
  =
  \left\{
  \left.
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{\mathrlap{g_1}} &&{}^{g_1 g_2}\nearrow&& \downarrow^{\mathrlap{g_3}}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\to}&&
    {*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{\,mathrlap{g_1}} &&\searrow^{g_2 g_3}&& \downarrow^{\mathrlap{g_3}}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\to}&&
    {*}
  }
  \right|
  g_1, g_2, g_3 \in G
  \right\}
  \,.
$$

The 2-simplices in $(\mathb{B}^2 A)_\bullet$ are 

$$
  (\mathbf{B}^2 A)_2
  =
  \left\{
  \left.
  \array{
    && {*}
    \\
    & {}^{}\nearrow &\Downarrow^{\mathrlap{c}}& \searrow^{}
    \\
    {*}
    &&\stackrel{}{\to}&& {*}
  }
  \right|
  c\in A
  \right\}
  \,,
$$

and the 3-simplices are 

$$
  (\mathbf{B}^2 A)_3
  =
  \left\{
  \left.
  \array{
    {*} &&\stackrel{}{\to}&& {*}
    \\
    \uparrow^{\mathrlap{}} &\swArrow_{c_1}&{}^{}\nearrow&\swArrow_{c_2}& \downarrow^{\mathrlap{}}
    \\
    {*}
    &&\stackrel{}{\to}&&
    {*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{}{\to}&& {*}
    \\
    \uparrow^{\mathrlap{}} &\swArrow_{c_3}&\searrow^{}&\swArrow_{c_4}& \downarrow^{\mathrlap{}}
    \\
    {*}
    &&\stackrel{}{\to}&&
    {*}
  }
  \right|
  c_1, c_2, c_3 \in A;
  c_4 = c^3 - c_1 - c_2
  \right\}
  \,.
$$




Therefore a homomorphism of [[Kan complexes]]/[[simplical sets]] $c \colon (\mathbf{B}G)_\bullet \to (\mathbf{B}^2 A)_\bullet$ is in degree 2 a function

$$
  c_2
  \;\;
  :
  \;\; 
  \left(
  \array{
    && {*}
    \\
    & {}^{g_1}\nearrow && \searrow^{g_2}
    \\
    {*}
    &&\stackrel{g_2 g_1}{\to}&& {*}
  }
  \right)
  \;\;\;
  \mapsto
  \;\;\;
  \left(
  \array{
    && {*}
    \\
    & {}^{{*}}\nearrow &\Downarrow^{c(g_1,g_2)}& \searrow^{{*}}
    \\
    {*}
    &&\stackrel{{*}}{\to}&& {*}
  }
  \right)
$$


i.e. a map $c \;\colon\; G \times G \to K$. To be a simplicial homomorphism this has to extend to 3-[[simplices]] as:

$$
  \begin{aligned}
  c_3
  \;\;\;
  &:
  \;\;\;
  \left(
  \array{
    {*} && \stackrel{g_2}{\longrightarrow} && {*}
    \\
    \uparrow^{g_1} &&{}^{g_2 g_1}\nearrow&& \downarrow^{g_3}
    \\
    {*}
    && \stackrel{g_3 g_2 g_1}{\longrightarrow} && {*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{g_2}{\to}&& {*}
    \\
    \uparrow^{g_1} &&\searrow^{g_3 g_2}&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_3 g_2 g_1}{\to}&&{*}
  }
  \right)
  \\
  & \mapsto
  \left(
  \array{
    {*} &\stackrel{}{\longrightarrow} & &\stackrel{}{\longrightarrow}& {*}
    \\
    \uparrow &\Downarrow^{c(g_1,g_2)}
    &\nearrow&\Downarrow^{c(g_2,g_3)}& 
    \downarrow
    \\
    {*}
    &\longrightarrow&&\longrightarrow&{*}
  }
  \;\;\;\;
  \stackrel{}{\Rightarrow}
  \;\;\;\;   
  \array{
    {*} &\longrightarrow&&\longrightarrow& {*}
    \\
    \uparrow &\Downarrow^{c(g_1,g_2 g_3)}
    &\searrow &\Downarrow^{c(g_2, g_3)}& \downarrow
    \\
    {*}
    &\longrightarrow&&\longrightarrow&{*}
  }
  \right)
  \end{aligned}  
  \,.
$$

Hence this is the cocycle condition.


A similar argument gives the coboundaries.

=--

We discuss now how in the computation of $H^2_{Grp}(G,A)$ one may concentrate on the _normalized_ cocycles.

+-- {: .num_defn #Normalized2Cocycle}
###### Definition

A group 2-cocycle $c \colon G \times G \to A$, def. \ref{2CocyclesAndCoboundaries} is called **normalized** if 

$$
  \forall_{g_0,g_1 \in G}
  \;\;
  \left(g_0 = e \;or\; g_1 = e \right)
  \Rightarrow
  \left( c(g_0,g_1) = e \right)
  \,.
$$

=--


+-- {: .num_lemma #2CocycleOngeisSameasOnee}
###### Lemma

For $c \colon G \times G \to A$ a group 2-cocycle, we have for all $g \in G$
that 

$$
  c(e,g) = c(e,e) = c(g,e)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The cocycle condition (eq:2CocycleConditionForCentralExtension) evaluated on

$$
  (g^{-1},  g,  e) \in G^3
$$

says that

$$
 c(g^{-1}, g) + c(e, e) = c(g, e) + c(g^{-1}, g )
$$

hence that

$$
  c(e,e) = c(g, e)
  \,.
$$

Similarly the 2-cocycle condition applied to 

$$
  (e,  g,  g^{-1}) \in G^3
$$

says that

$$
  c(e,g) + c(g,g^{-1}) = c(g,g^{-1}) + c(e,e)
$$

hence that

$$
  c(e,g) = c(e,e)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Every group 2-cocycle $c \colon G \times G \to A$ is 
cohomologous to a normalized one, def. \ref{Normalized2Cocycle}.

=--

+-- {: .proof}
###### Proof

By lemma \ref{2CocycleOngeisSameasOnee} it is sufficient to 
show that $c$ is cohomologous to a cocycle $\tilde c$ satisfying
$\tilde c(e,e) = e$.
Now given $c$, Let $h \colon G \to A$ be given by 

$$
  h(g) \coloneqq c(g,g)
  \,.
$$

Then $\tilde c \coloneqq c + d c$ has the desired property, with (eq:Group2CoboundaryEquation):

$$
  \begin{aligned}
    \tilde c(e,e)
    & \coloneqq
    (c + d h)(e,e) 
    \\
    & = 
    c(e,e)  + c(e \cdot e, e \cdot e) - c(e,e) - c(e,e)
    \\  
    & = 
    0
  \end{aligned}
  \,.
$$

=--



##### Topological and Lie groups

* [[topological group]]

* [[Lie group]]

#### Simplicial groups


##### Discrete

* [[simplicial group]]

##### Abelian

* [[abelian group]]

##### Topological and Lie simplicial groups

* [[simplicial topological space]]

* [[geometric realization of simplicial topological spaces]]

#### Connected groupoids

any [[Lie group]] $G$ induces its [[delooping]] [[Lie groupoid]] 
  
$$
  \mathbf{B}G
  =
  * \sslash G
  = 
  \left(
     G \stackrel{\to}{\to} * 
  \right)
  \,.
$$


#### 2-Groups

##### Discrete

* [[2-group]]

* [[crossed module]]

##### Braided and abelian

* [[braided 2-group]]

* [[symmetric 2-group]]

#### Abelian $\infty$-groups

##### Chain complex

* [[chain complex]]

##### Spectrum

* [[spectrum]], [[infinite loop space]]

##### Dold-Kan correspondence

* [[simplicial group]], [[Dold-Kan correspondence]], [[chain complex]]

* [[stable Dold-Kan correspondence]]

+-- {: .num_defn #DKMap}
###### Definition

Write 

$$
  DK 
  \colon
  Ch_\bullet(Ab(Smooth0Type))
  \stackrel{\Xi}{\to}
  sAb(Smooth0Type)
  \to
  Smooth0Type^{\Delta^{op}}
  \to
  L_{whe} Smooth0Type^{\Delta^{op}}
  \simeq
  Smooth \infty Grpd
$$

for the functor that sends a [[chain complex]] of [[abelian group|abelian]] [[group objects]] in [[smooth spaces]] first to the [[simplicial abelian group]] in [[smooth spaces]] given by the [[Dold-Kan correspondence]], then [[forgetful functor|forgets]] the abelian group structure and finally regards the resulting [[simplicial object|simplicial]] smooth space as a [[smooth ∞-groupoid]] under [[simplicial localization]].

=--

#### Cohomology

* [[cohomology]]

##### Nonabelian cohomology


* [[nonabelian cohomology]]

##### Abelian sheaf cohomology
 {#AbelianSheafCohomology}

* [[abelian sheaf cohomology]]

* [[Cech cohomology]]


### Semantic Layer

#### $A_\infty$-types

* [[A-infinity space]]

#### $\infty$-Groups

* [[infinity-group]]

* [[looping and delooping]]



### Syntactic Layer


#### Pointed connected types

* [[connected type]]

#### Identity types of connected types

(...)