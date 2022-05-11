
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
* table of contents
{:toc} 

## Idea

A [[topos]] may be thought of as a generalized [[topological space]]. Accordingly, the notions of 

* [[locally connected space]]

* locally 2-[[connected]] space

* etc. ...

* [[locally contractible space]]

have analogs for [[topos]]es and [[(∞,1)-topos]]es

* **locally connected topos**

* [[locally n-connected (n,1)-topos]] 

* etc. ...

## Definition


+-- {: .num_defn #ConnectedObject}
###### Definition

An [[object]] $A$ in a [[topos]] $\mathcal{E}$ is called a **[[connected object]]** if the [[hom-functor]] $\mathcal{E}\big(A, -\big)$ [[preserved limit|preserves]] [[finite coproduct|finite]] [[coproducts]]. 

Equivalently, an object $A$ is connected if it is non-empty (in that it is not [[generalized the|the]] [[initial object]]) and cannot be expressed as a [[coproduct]] of two nonempty [[subobjects]]. 

=--

+-- {: .num_defn}
###### Definition

A [[Grothendieck topos]] $\mathcal{E}$ is called a **locally connected topos** if every object  is a [[coproduct]] of [[connected objects]] (Def. \ref{ConnectedObject}), 
hence if for $A \in \mathcal{E}$ there exists $\big\{A_i \in \mathcal{E}\big\}_{i \in I}$ such that 
$$
  A 
  \;\simeq\; 
  \coprod_{i \in I} A_i
  \,.
$$  

=--

If this is the case, it  follows that the [[indexed set|index]] set $I$ is unique up to [[isomorphism]], and we denote it by

$$
  \pi_0(A) \;\coloneqq\; I
  \,.
$$

This construction defines a [[functor]] 

$$
  \array{
    \Pi_0 \colon & \mathcal{E} &\longrightarrow& Set 
    \\
    & A &\mapsto& \pi_0(A)
  }
$$ 

which is [[left adjoint]] to the [[locally constant sheaf]] functor, the [[left adjoint]] part of the [[global section]] [[geometric morphism]].  

This is the **connected component functor**. It generalizes the functor, also denoted $\pi_0$ or $\Pi_0$, which to a [[topological space]] assigns the set of [[connected components]] of that space. See the [examples](#Examples) below.


In summary, for a locally connected topos the [[terminal geometric morphism]] extends to an [[adjoint triple]] of this form:

\begin{tikzcd}[column sep=24pt]
  \mathcal{E}
  \ar[
    rr,
    shift left=16pt,
    "{ \Pi_0 }"
  ]
  \ar[
    from=rr,
    "{ \mathrm{LConst} }"{description}
  ]
  \ar[
    rr,
    shift right=16pt,
    "{ \Gamma }"{swap}
  ]
  \ar[rr, phantom, shift left=9pt, "{\scalebox{.6}{$\bot$}}"]
  \ar[rr, phantom, shift right=9pt, "{\scalebox{.6}{$\bot$}}"]  
  &&
  \mathrm{Set}
\end{tikzcd}



The following proposition asserts that the existence of $\Pi_0$ already characterizes locally connected toposes.

+-- {: .num_prop #LocalConnectednessByEssentialGeometricMorphism}
###### Proposition

A [[Grothendieck topos]] $\mathcal{E}$ is locally connected precisely if the [[global section]] [[geometric morphism]] $\Gamma : \mathcal{E} \to Set$ is an [[essential geometric morphism]] $(\Pi_0 \dashv L Const \dashv \Gamma) : \mathcal{E} \to Set$. 

=--




+-- {: .proof}
###### Proof

The "only if"-case was just claimed/argued above, we need to show the "if"-case. 

Hence suppose that $\Pi_0$ with $(\Pi_0 \dashv LConst)$ exists. We will show that then every object is a coproduct of connected objects. (A proof also appears as ([Johnstone, Lemma C.3.3.6](#Johnstone)).)

First we claim that an object $A$ is connected in the 
[above sense](#ConnectedObject) precisely if $\Pi_0(A) = \ast$. 

To see this, observe that 
\[
  \label{EmptyShapeImpliesInitialObject}
  \Pi_0(A) \;\simeq\; \varnothing
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  LConst \Pi_0(A) \;\simeq\; \varnothing
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  A \xrightarrow{\eta_{A}} \varnothing
  \;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;
  A \;\simeq\; \varnothing
  \,,
\]
where we used that $LConst$ is a [[left adjoint]] and that [[left adjoints preserve colimits]] ([hence](initial+object#InitialObjectIsEmptyColimit) [[preserved colimit|preserve]] [[initial objects]]), we used the [[adjunction unit]], and
where the last implication follows since the [[initial object]] in any topos is [[strict initial object|strict]].

But this gives
$$
  \Pi_0(A) \simeq \ast
  \;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;
  A \;\text{is connected}
  \,,
$$
because if $A$ as on the left were the coproduct of non-initial $A_1$, $A_2$, then also $\Pi_0(A)$ would be the coproduct of non-initial $\Pi_0(A_1)$, $\Pi_0(A_2)$, by (eq:EmptyShapeImpliesInitialObject), which would contradict the assumption that $\Pi_0(A) \simeq \ast$.

Conversely, to see 
$$
  A \;\text{is connected}
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;
  \Pi_0(A) \simeq \ast
$$
observe that the connectivity assumption implies in particular that 
\[
  \label{ASequenceOfIsos}
  Set
  \big(
    \Pi_0(A)
    ,\, 
    S
  \big)
  \;\simeq\;
  \mathcal{E}
  \left(
     A,\, 
     LConst 
     \coprod_S 
     \ast 
  \right) 
  \;\simeq\;
  \mathcal{E}
  \left(
    A
    ,\, 
   \coprod_S \,  LConst \ast
  \right) 
  \;\simeq\; 
  {\coprod}_S
  \, 
  \mathcal{E}
  \big(
    A
    ,\,
    \ast
  \big) 
  \;\simeq\; 
  \coprod_S \ast 
  \;\simeq\; 
  S
  \,,
\] 
for all $S \in Set$, 
where in the first step we used the $\big(\Pi_0 \dashv LConst\big)$-[hom isomorphism](adjoint+functor#InTermsOfHomIsomorphism). But this says that $\Pi_0(A)$ is connected as an object of [[Sets]], hence that it is [[generalized the|the]] [[singleton set]].

With this equivalence 
$$
  A \; \text{is connected}
  \;\;\;\;
  \Leftrightarrow
  \;\;\;\;
  \Pi_0(A) \simeq \ast
$$
in hand (given the extra left adjoint $\Pi_0$), 
we are now reduced to showing that every object of $\mathcal{E}$ is a coproduct of objects for which $\Pi_0(-)$ is the [[terminal object|point]].

For that purpose consider for $A \in \mathcal{E}$ the following [[pullback]] diagram

$$
  \array{
    i_A^* {\underset{\underset{\Pi_0(A)}{\longrightarrow}}{\lim}} \ast 
    &\xrightarrow{\phantom{----}}& 
    {\underset{\underset{\Pi_0(A)}{\longrightarrow}}{lim}} \ast 
    \\
    {}^{\mathllap{\simeq}}\big\downarrow 
    && 
    \big\downarrow{}^{\mathrlap{\simeq}}
    \\
    A 
    &\xrightarrow{\phantom{--}i_A\phantom{--}}& 
    LConst \Pi_0 (A)
    \,,
  }
$$

where the bottom morphism is the $(\Pi \dashv L Const)$-[[unit of an adjunction|unit]] and the right [[isomorphism]] is the identification of any set as the [[colimit]] (here: [[coproduct]]) of the functor over the set itself that is constant on the point. Since isomorphisms are preserved under pullback ([here](pullback#PullbackPreservesMonomorphisms)), it follows that also the left morphism is an isomorphism, as shown.

Now, by the fact that a [[topos]] has "[[universal colimits]]", this left morphism is equivalently 

$$
   \underset{
     \underset{s \in \Pi_0(A)}{\longrightarrow}
   }{\lim}
   (i_A^* \ast_s)
   \xrightarrow{\phantom{--}\sim\phantom{--}}
   A
$$

and hence expresses $A$ as a coproduct of objects $i_A^* *_s$, each of which is a [[pullback]]

$$
  \array{
    i_A^* \ast_s &\xrightarrow{\phantom{----}}& LConst *
    \\
    \big\downarrow && \big\downarrow{}^{\mathrlap{s}}
    \\
    A &\xrightarrow{\phantom{--}i_A\phantom{--}}& LConst \Pi_0 A
    \,,
  }
$$

where the right morphism includes the element $s$ into the set $\Pi_0 A$. By applying $\Pi_0$ to this diagram and [[pasting]] on the $(\Pi_0 \dashv L Const)$-[[counit of an adjunction|counit]] we get

$$
  \array{
    \Pi_0(i_A^* *_s) 
    &\xrightarrow{\phantom{-----}}& 
    \Pi_0 LConst \ast &\xrightarrow{\phantom{---}}& *
    \\
    \big\downarrow && \big\downarrow^{} && \big\downarrow 
    \\
    \Pi_0(A) 
    &\xrightarrow{\phantom{--}\Pi_0(i_A)\phantom{--}}& 
    \Pi_0 LConst \Pi_0 A
    &\xrightarrow{\phantom{----}}& 
    \Pi_0 A
  }
$$

and by the [[zig-zag identity]] the bottom morphism is the [[identity morphism|identity]]. This says that in 

$$
  \Pi_0
  \left( 
     \underset{\underset{\Pi_0 A}{\longrightarrow}}{\lim} 
     i_A^* \ast_s 
     \xrightarrow{\sim} 
     A
  \right)
  \simeq
  \left(
     \underset{\underset{\Pi_0 A}{\longrightarrow}}{\lim} 
     \Pi_0\big(i_A^* \ast_s\big) 
     \xrightarrow{\sim} 
     \Pi_0(A)
  \right)
$$

all the component maps out of the coproduct factor through the point. This means that this can only be an isomorphism if all these component maps are point inclusions, hence if $\Pi_0(i_A^* *_s) \simeq *$ for all $s \in \Pi_0 A$.

=--

However, this doesn't mean that essential geometric morphisms are the "relative" analog of locally connected toposes; in general one needs to impose an additional condition, which is automatic in the case of the global sections morphism, to obtain the notion of a [[locally connected geometric morphism]].


## Properties

### Characterization over locally connected sites

See at _[[locally connected site]]_.

### Equivalent conditions

+-- {: .num_defn}
###### Definition

For $C$ and $C$ [[cartesian closed categories]], a [[functor]] $F : C \to D$ that preserves [[product]]s is called a **[[cartesian closed functor]]** if the canonical [[natural transformation]]

$$
  F(B^A) \to (F(B))^{F(A)}
$$ 

(which is the [[adjunct]] of $F(A) \times F(B^A) \simeq F(A \times B^A) \to F(B)$) is an [[isomorphism]].

=--


+-- {: .num_prop}
###### Proposition

The [[constant sheaf]]-functor $\Delta : \mathcal{S} \to \mathcal{E}$ is a [[cartesian closed functor]] precisely if $\mathcal{E}$ is a locally connected topos.

=--



### Locally connected and connected {#Connected}


A [[topos]] $E$ is called a [[connected topos]] if the [[left adjoint]] $L Const : Set \to E$ is a [[full and faithful functor]].


+-- {: .num_prop}
###### Proposition
If $\Gamma \colon E\to Set$ is a locally connected topos, then it is also a [[connected topos]] --- in that $L Const$ is full and faithful --- if and only if the [[left adjoint]] $\Pi_0$ of $L Const$ preserves the 
[[terminal object]].
=--

This is ([Johnstone, C3.3.3](#Johnstone)).

Notice that for a connected and locally connected topos, the adjunction

$$
  Set \stackrel{\overset{\Pi_0}{\leftarrow}}{\hookrightarrow} E
$$

exhibits [[Set]] as a [[reflective subcategory]] of $E$. We may think then of [[Set]] as being the [[localization]] of $E$ at those morphisms that induce isomorphisms of connected components.


## Examples {#Examples}

+-- {: .num_example #LocallyConnectedTopologicalSpace}
###### Example

For $X$ a [[topological space]], the [[category of sheaves]] $Sh(X) \coloneqq Sh(Op(X))$ is a locally connected topos precisely if $X$ is a [[locally connected space]]. The functor $\Pi_0$ sends a sheaf $F \in Sh(X)$ to the set of connected components of the corresponding [[etale space]].

=--

+-- {: .num_example #SmoothSpaces}
###### Example

For $C = $ [[CartSp]] the [[site]] of [[Cartesian spaces]] with its [[good open cover]] [[coverage]], the topos $Sh(CartSp)$ of [[smooth spaces]] is locally connected.  An arbitrary $X \in Sh(CartSp)$ is sent to the [[colimit]] $\lim_\to X \in Set$. If $X$ is a [[diffeological space]] or even a [[smooth manifold]], then this is the set of connected components of the underlying topological space.

=--

+-- {: .num_example #LCC}
###### Example

Every locally connected geometric morphism is a [[locally cartesian closed functor]].

=--

+-- {: .num_example}
###### Example

Suppose that $C$ is a [[site]] such that constant [[presheaves]] on $C$ are [[sheaves]].  Then the left adjoint $\Pi_0$ exists and is given by the [[colimit]] functor: if we write $L : PSh(C) \to Sh(C)$ for [[sheafification]], then for any sheaf $X$, we have

  $$
    Hom_{Sh(C)}(X, L Const S)
    \simeq
    Hom_{PSh(C)}(X, L Const S)
    \simeq
    Hom_{PSh(C)}(X, Const S)
    \simeq
    Hom_{Set}(\lim_\to X, S)
    \,.
  $$

  In particular, this is the case if every covering [[sieve]] in $C$ is connected, i.e. $C$ is a [[locally connected site]].

  If $C$ furthermore has a terminal object $1$, then the global sections functor $\Gamma\colon Sh(C)\to Set$ (the right adjoint of $L Const$) is simply given by evaluation at $1$, and so the unit $S \to \Gamma L Const S \cong L Const S(1)$ is an isomorphism.  Thus in this case $Sh(C)$ is additionally [[connected topos|connected]].  This situation also applies to $C=CartSp$ in example \ref{SmoothSpaces} above.

=--

+-- {: .num_example }
###### Example

If $C$ is a category with all [[finite limits]] and if the unique functor $\pi \colon C \to \ast$ to the [[terminal category]] is a [[cover-preserving functor]] (for $\ast$ equipped with the trivial topology/[[coverage]]) then $Sh(C)$ is locally connected. 
(In particular, this holds for presheaf toposes). 
This is because the inclusion of the terminal object $i \colon \ast \to C$ provides a [[right adjoint]] to $\pi$, so that there is an 
[[adjoint quadruple]] of functors on [[presheaf categories]]

$$
  (\pi_! \simeq Lan_\pi)  
    \dashv 
  (\pi^\ast \simeq i_! \simeq Lan_i) 
   \dashv 
  (\pi_\ast \simeq i^\ast )
    \dashv
  (\pi^! \simeq i_* \simeq Ran_i)
  \;\colon\;
  PSh(C) \leftrightarrow PSh(\ast) \simeq Sh(C) \simeq Set
  \,,
$$

where $Lan_{(-)}$ and $Ran_{(-)}$ denote let and right [[Kan extension]], respectively. Now if $C \to \ast$ indeed preserves covers and using that $C \to \ast$ trivially preserves finite limits and hence is a [[flat functor]], then by the discussion at _[[morphism of sites]]_ the first three functors here descend to [[sheaves]] and hence exhibit $Sh(C)$ as being locally connected. 

But **beware** that the assumptions here are stronger than they may seem: that $C \to \ast$ preserves covers is not automatic, but is a strong condition. It is violated as soon as $C$ contains an empty object with [[empty set|empty]] cover, such as is the case in most categories of [[spaces]], notably in [[categories of open subsets]] $Op(X)$ of a [[topological space]] $X$, as in example \ref{LocallyConnectedTopologicalSpace}.

=--

## Related entries

* [[essential geometric morphism]]

* **locally connected topos** / [[locally ∞-connected (∞,1)-topos]]

* [[connected topos]] / [[∞-connected (∞,1)-topos]]

* [[totally connected topos]] / [[totally connected (∞,1)-topos]]

* [[local topos]] / [[local (∞,1)-topos]].

* [[cohesive topos]] / [[cohesive (∞,1)-topos]]

## References
 {#References}

Section C1.5 and C3.3 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_ .
{#Johnstone}

A variant is in

* [[Marta Bunge]], Funk, _Quasi locally connected toposes_ ([pdf](http://www.tac.mta.ca/tac/volumes/18/8/18-08.pdf))

Discussion of characterizations of [[sites]] of definition of locally connected toposes is in

* [[Olivia Caramello]], _Site characterizations for geometric invariants of toposes_, Theory and Applications of Categories, Vol. 26, 2012, No. 25, pp 710-728. ([TAC](http://www.tac.mta.ca/tac/volumes/26/25/26-25abs.html))

[[!redirects locally connected toposes]]
[[!redirects locally connected topoi]]

