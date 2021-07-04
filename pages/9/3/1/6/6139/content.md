
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher category theory
+-- {: .hide}
[[!include higher category theory - contents]]
=--
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

For $X$ any kind of [[space]] (or possibly a [[directed space]], viewed as some sort of [[category]] or higher dimensional analogue of one), its [[loop space object]]s $\Omega_x X$ canonically inherit a [[monoidal category|monoidal structure]], coming from concatenation of [[loops]].

If $x \in X$ is essentially unique, then $\Omega_x X$ equipped with this monoidal structure remembers all of the structure of $X$: we say $X \simeq B \Omega_x X$ call $B A$ the _[[delooping]]_ of the monoidal object $A$.

What all these terms ("loops" $\Omega$, "delooping" $B$ etc.) mean in detail and how they are _presented_ concretely depends on the given setup. We discuss some of these below in the section [Examples](#Examples).



## Examples
 {#Examples}

### For plain groups delooping to groupoids
 {#ForPlainGroupsDeloopingToGroupoids}

Write 

* [[Grpd]] for the [[(2,1)-category]] of [[groupoids]] ([[objects]] are [[groupoids]], [[1-morphisms]] are [[functors]] between these and [[2-morphisms]] are [[natural transformations]] between those, which are necessarily [[natural isomorphisms]]), 

* [[Grp]] for the [[1-category]] of [[groups]] ([[discrete groups]]), also regarded as a [[(2,1)-category]]; 

* $Grpd^{\ast/}$ for the $(2,1)$-category of [[pointed objects]] in [[Grpd]], 

* $Grpd_{\geq 1} \hookrightarrow Grpd$ for the [[full sub-(infinity,1)-category|full sub-(2,1)-category]] of [[connected object in an (infinity,1)-topos|connected]] groupoids, those for which $\pi_0 \simeq \ast$;

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



### For topological spaces and $\infty$-groupoids

There is an [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd^{\ast/}_{\geq 1} 
    \stackrel{\overset{B}{\leftarrow}}{\underset{\Omega}{\to}}
  \infty Group
$$


between [[pointed object|pointed]] [[connected]] [[∞-groupoid]]s and [[∞-group]]s, where $\Omega$ forms [[loop space object]]s.

This is [[presentable (∞,1)-category|presented]] by a [[Quillen equivalence]] of [[model categories]]

$$
  sSet_* 
    \stackrel{\overset{\bar W}{\leftarrow}}{\underset{G}{\to}}
  sGrp  
$$

between the [[model structure on reduced simplicial sets]] and the [[transferred model structure]] on [[simplicial group]]s along the [[forgetful functor]] to the [[model structure on simplicial sets]].

(See [[groupoid object in an (infinity,1)-category]] for more details on this Quillen equivalence.)


### For parameterized $\infty$-groupoids ($\infty$-stacks / $(\infty,1)$-sheaves)

The following result makes precise for _parameterized [[∞-groupoid]]s_  -- for [[∞-stack]]s -- the general statement that $k$-fold [[delooping]] provides a correspondence between [[n-category|n-categories]] that have trivial [[k-morphism|r-morphism]]s for $r \lt k$ and  [[k-tuply monoidal n-category|k-tuply monoidal n-categories]].

+-- {: .num_defn}
###### Definition

An [[Ek-algebra]] object $A$ in an [[(∞,1)-topos]] $\mathbf{H}$ is called **groupal** if its [[homotopy groups in an (∞,1)-topos|connected components]] $\pi_0(A) \in \mathbf{H}_{\leq 0}$ is a [[group object]].

Write $Mon^{gp}_{\mathbb{E}[k]}(\mathbf{H})$ for the [[(∞,1)-category]] of groupal $E_k$-algebra objects in $\mathbf{H}$.

A groupal $E_1$-algebra -- hence an groupal [[A-∞ algebra]] object in $\mathbf{H}$ -- we call an _[[∞-group]]_ in $\mathbf{H}$. Write $\infty Grp(\mathbf{H})$ for the [[(∞,1)-category]] of [[∞-group]]s in $\mathbf{H}$.

=--

+-- {: .num_theorem #LoopingDeloopingForHigherStacks}
###### Theorem

Let $k \gt 0$, let $\mathbf{H}$ be an [[(∞,1)-category of (∞,1)-sheaves]] and let $\mathbf{H}_*^{\geq k}$ denote the [[full subcategory]] of the category $\mathbf{H}_{*}$ of [[pointed objects]], spanned by those pointed objects thar are $k-1$-[[connected]] (i.e. their first $k$ [[homotopy groups in an (∞,1)-topos|homotopy sheaves]]) vanish. Then there is a canonical equivalence of [[(∞,1)-category|(∞,1)-categories]]

$$
  \mathbf{H}^{\ast/}_{\geq k} \simeq Mon^{gp}_{\mathbb{E}[k]}(\mathbf{H}) \,.
$$

between the pointed $(k-1)$-[[connected]] objects and the groupal [[Ek-algebra]] objects in $\mathbf{H}$.

=--

This is _[[Higher Algebra|Higher Algebra, theorem 5.2.6.10]]_


Specifically for $\mathbf{H} = $ [[Top]], this reduces to the following classical theorem due to [[Peter May]], known as the [[May recognition theorem]].

+-- {: .num_theorem}
###### Theorem

Let $Y$ be a [[topological space]] equipped with an action of the [[little cubes operad]] $\mathcal{C}_k$ and suppose that $Y$ is grouplike. Then $Y$ is homotopy equivalent to a $k$-fold loop space $\Omega^k X$ for some pointed topological space $X$.

=--

This is _[[Higher Algebra|Higher Algebra, theorem 5.2.6.15]]_

+-- {: .num_remark #LoopingDeloopingDegree1InTopos}
###### Remark

For $k = 1$ we have a looping/delooping equivalence

$$
  Grp(\mathbf{H})
  \stackrel{\overset{\Omega}{\longleftarrow}}{\underset{\mathbf{B}}{\longrightarrow}}
  \mathbf{H}_{\geq 1}^{\ast /}
$$

between pointed connected objects in $\mathbf{H}$ and grouplike [[A-∞ algebra]] objects in $\mathbf{H}$: [[∞-group]] objects in $\mathbf{H}$.

=--

+-- {: .num_remark}
###### Remark

If the ambient [[(∞,1)-topos]] has [[homotopy dimension]] 0 then every connected object $E$ admits a point $* \to E$. Still, the [[(∞,1)-category]] of pointed connected objects differs from that of unpointed connected objects (because in the latter the [[natural transformation]]s may have nontrivial components on the point, while in the former case they may not).

The connected objects $E$ which fail to be [[∞-group]]s by failing to admit a point are of interest: these are the _[[∞-gerbes]]_ in the [[(∞,1)-topos]].

=--

### For cohesive $\infty$-groupoids

A special case of the parameterized $\infty$-groupoids above are [[cohesive ∞-groupoid]]s. Looping and delooping for these is discussed at
[[cohesive (∞,1)-topos -- structures]] in the section <a href="http://www.ncatlab.org/nlab/show/cohesive%20%28infinity,1%29-topos%20--%20structures#InfinGroups">Cohesive ∞-groups</a>.

### For $(\infty,n)$-categories

See [[delooping hypothesis]].

## Relation to looping and suspension

For $A$ any monoidal [[space]], we may [[forgetful functor|forget]] its monoidal structure and just remember the underlying [[space]].  The formation of [[loop space object]]s composed with this [[forgetful functor]] has a [[left adjoint]] $\Sigma$ which forms _[[suspension objects]]_.


## Related concepts

* [[May recognition theorem]]

* [[Quillen equivalence between simplicial groups and reduced simplicial sets]]

* [[loop space object]], [[free loop space object]],

  * [[delooping]], **looping and delooping**

  * [[loop space]], 

  * [[free loop space]], [[derived loop space]], [[free loop stack]]

* [[suspension object]]

  * [[suspension]], [[reduced suspension]]

[[!include k-monoidal table]]

## References

Section 6.1.2 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

Section 5.1.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieAlgebra}


[[!redirects looping]]
[[!redirects looping and delooping]]