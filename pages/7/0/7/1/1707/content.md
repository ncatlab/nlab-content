
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _group cohomology_  of a [[group]] $G$ is the [[cohomology]] of its [[delooping]] $\mathbf{B}G$.
This cohomology classifies [[group extensions]] of $G$.

More generally, the _group cohomology_  of an [[∞-group]] $G$ is the [[cohomology]] of its [[delooping]] $\mathbf{B}G$ and it classifies [[∞-group extensions]] of $G$ or equivalently [[principal ∞-bundles]] over $\mathbf{B}G$ (for [[coefficients]] with trivial [[∞-action]]) or [[associated ∞-bundles]] (for coefficients with nontrivial [[∞-action]]).

More in detail, if $A$ is any [[abelian group]] then a [[cocycle]] in $G$-group cohomology with [[coefficients]] in $A$ regarded as equipped with the trivial [[action]] is a morphism

$$
  c \colon \mathbf{B}G \to \mathbf{B}^n A
$$

and the [[cohomology group]] is the [[homotopy]] [[equivalence classes]] of this

$$
  H^n_{Grp}(G,A) \simeq \pi_0 \mathbf{H}(\mathbf{B}G,\mathbf{B}^n A)
  \,.
$$

More generally, $A$ here may be equipped with a $G$-[[action]] $\rho \colon A \times G \to A$. There is the the corresponding [[action groupoid]] or [[associated ∞-bundle]] $\mathbf{B}^n A\sslash G \to \mathbf{B}G$ and now a cocycle is a morphism $\mathbf{c} \colon \mathbf{B}G \to \mathbf{B}^n A\sslash G$ fitting into a diagram

$$
  \array{
    \mathbf{B}G && \stackrel{\mathbf{c}}{\longrightarrow}  && \mathbf{B}^n A \sslash G
    \\
    & \searrow &\swArrow& \swarrow 
    \\
    && \mathbf{B}G
  }
  \,.
$$

Equivalently this means that the group cohomology of $G$ with coefficients in an abelian group $A$ with $G$-[[action]] $\rho$ is the _[[twisted cohomology]]_ of the [[delooping]] $\mathbf{B}G$ with respect to the [[local coefficient ∞-bundle]] $\mathbf{B}^n A \sslash G$.

All this generalizes to $G$ itself any [[∞-group]] and $\mathbf{B}^n A$ replaced by any $G$-[[∞-action]] $\rho \colon V \times G \to G$ in which case a group cocycle is now a morphism

$$
  \array{
    \mathbf{B}G && \stackrel{\mathbf{c}}{\longrightarrow}  && V \sslash G
    \\
    & \searrow &\swArrow& \swarrow 
    \\
    && \mathbf{B}G
  }
$$

hence a cocycle in the [[twisted cohomology]] of $\mathbf{B}G$ with coefficients in the [[local coefficient ∞-bundle]] given by the universal $\rho$-[[associated ∞-bundle|associated]] $V$-[[fiber ∞-bundle]].

In other words, the general notion of group cohomology of $G$ is just the most general notion of cohomology of $\mathbf{B}G$.

This general definition we discuss below in 

* [Fully general definition in homotopy type theory](#InHomotopyTypeTheory).

The special case where $V = \mathbf{B}^n A$ is the $n$-fold [[delooping]] of an [[abelian group]] is important for applications and also because in this case powerful tools of [[homological algebra]] can be applied and group cohomology of ordinary groups may be computed in tersm of of [[Ext]]-functors. This we discuss in 

* [Of an ordinary group with abelian group coefficients - In terms of homological algebra](#InTermsOfHomologicalAlgebra).

Finally one can break this further down into components In 

* [Special case: Explicit formulas in low degree](#InLowDegree)

we give some standard formulas for group cohomology in low degree. 

## Definition

### Fully general: in homotopy type theory
 {#InHomotopyTypeTheory}

We give the general abstract definition in the language of [[(∞,1)-topos theory]] / [[homotopy type theory]].

Let $\mathbf{H}$ be an [[(∞,1)-topos]]. Let $G \in Grp(\mathbf{H})$ be a [[group object in an (∞,1)-category|group object]],  an [[∞-group]], in $\mathbf{H}$. Write $\mathbf{B}G \in \mathbf{H}$ for its [[delooping]].

An [[∞-action]] $\rho : V \times G \to V$ of $G$ on a $V \in \mathbf{H}$ is equivalently, as discussed there, exhibited by a [[fiber sequence]]

$$
  \array{
    V &\to& V \sslash G
    \\
    && \downarrow^{\mathrlap{\bar \rho}}
    \\
    && \mathbf{B}G
  }
  \,.
$$

Regarded as an object in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}G}$ this is the [[categorical semantics]] of what in the [[syntax]] of [[homotopy type theory]] this is the [[dependent type]]

$$
  x \colon \mathbf{B}G \;\vdash \; V(x) \colon Type
  \,.
$$

Also, $\bar \rho$ is the _[[local coefficient bundle]]_ for $G$-group cohomology with [[coefficients]] in $V$ equipped with this $G$-[[∞-action]]. this means that the 
 _group cohomology_ of $G$ with coefficients in $V$ is the hom in the [[slice (∞,1)-topos]] over $\mathbf{H}$ as [[base (∞,1)-topos]]

$$
  H^1_{Grp}(G,V) 
  \coloneqq
  \mathbf{H}_{/\mathbf{B}G}(\mathbf{B}G, V)
  \,,
$$

where we denote on the right by $\mathbf{B}G$ the [[terminal object]] in the slice $\mathbf{H}_{/\mathbf{B}G}$. Notice that in $\mathbf{H}$ this is the trivial [[fiber sequence]]

$$
  \array{
     * &\to& \mathbf{B}G
     \\
     && \downarrow^{\mathrlap{id}}
     \\
     && \mathbf{B}G
  }
$$

This is the [[categorical semantics]] of what in the [[syntax]] of [[homotopy type theory]] is 

$$
  \vdash \; \left(\prod_{x \colon \mathbf{B}G} \left(* \to V \right)\right) \colon Type
  \,.
$$

By the discussion at [[∞-action]], this expresses the [[invariant|∞-invariants]] of the [[conjugation action]] of $G$ on the morphisms $* \to V$ of the underlying objects. Since the action on the point is trivial, these are just the [[invariant|∞-invariants]] of $V$.

+-- {: .num_prop #GroupCohomologyInInfinityToposForTrivialAction}
###### Proposition

In the special case that the $G$-[[∞-action]] on $V$ is trivial, the group cohomology is equivalently just the set of connected components of the [[derived hom space|hom space]]

$$
  H_{Grp}(G,V) \simeq \pi_0 \mathbf{H}(\mathbf{B}G, V)
  \,.
$$

In particular if $V = \mathbf{B}^n A$ for $A$ an abelian group, this is

$$
  H^n_{Grp}(G,A) \coloneqq H_{Grp}(G,\mathbf{B}^n A)
  \simeq
  \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

=--

[[!include homotopy type representation theory -- table]]



### For an ordinary group and abelian coefficients: In terms of homological algebra
 {#InTermsOfHomologicalAlgebra}


Let $G$ be an ordinary [[group]], specifically a [[group object]] in a [[topos]] $\mathcal{T}$ such that the [[abelian category]] $Ab(\mathcal{T})$ has [[projective object|enough projectives]]. If $G$ is an ordinary [[discrete group]] then this means that in the ambient [[set theory]] we assume the [[axiom of choice]] or ar least the [[presentation axiom]].

Write then 

$$
  \mathbb{Z}[G] \in Ring
$$ 

for the [[group algebra]] of $G$ over the [[integers]].
Write 

$$
  \mathcal{A} \coloneqq \mathbb{Z}[G] Mod
$$ 

for the category $\mathbb{Z}[G]$[[Mod]] of [[modules]] over $\mathbb{Z}[G]$.

Notice that a [[module]] 

$$
  A \in \mathbb{Z}[G] Mod
$$ 

is equivalently an [[abelian group]] equipped with a $G$-[[action]]. This or rather its $n$-fold [[suspension of a chain complex|suspension as a chain complex]] 

$$
  A[n] \in Ch_\bullet(\mathbb{Z}[G]Mod)
$$

is the kind of [[coefficient]] for the group cohomology of $G$ to which the following statement applies. 

+-- {: .num_remark #InvariantsByHomFunctor}
###### Remark

For $A$ a $G$-[[module]], the [[invariant|invariants]] of $A$ are equivalently the $\mathbb{Z}[G]$-module homomorphisms from $\mathbb{Z}$ equipped with the trivial module structure

$$
  Invariants(A) \simeq Hom_{\mathbb{Z}[G]}(\mathbb{Z}, A)
  \,.
$$

This equivalence is [[natural isomorphism|natural]] and hence the contravariant [[hom functor]] is equivalently the invariants-functor

$$
  Invariants(-)\simeq Hom_{\mathbb{Z}[G]}(\mathbb{Z}, -)
  \,.
$$

=--

By the fully general discussion [above](#InHomotopyTypeTheory), group cohomology of $G$ with coefficients in some $A$ is the homotopy-version of the $G$-[[invariants]] of $A$. In the context of [[homological algebra]] and in view of remark \ref{InvariantsByHomFunctor}, this means that it is given by the [[derived functor]] of the [[hom functor]] out of the trivial $G$-module, hence by the [[Ext]]-functor:

+-- {: .num_defn}
###### Definition

For $A$ an [[abelian group]] equipped with a $G$-[[action]], the degree-$n$ _group cohomology_ of $G$ with [[coefficients]] in $A$ is the $n$th-[[Ext]]-group

$$
 H^n_{Grp}(G,A) \coloneqq Ext^n_{\mathbb{Z}[G]}(\mathbb{Z}, A)
  \,,
$$

where on the right $\mathbb{Z} \in \mathbb{Z}[G] Mod$ is regarded as equipped with the trivial $G$-action.

=--

+-- {: .num_remark}
###### Remark

By the discussion at _[[projective resolution]]_ this means more explicitly the following: let $F_\bullet \stackrel{\simeq_{qi}}{\to} \mathbb{Z}$ be a [[projective resolution]]  $Ch_\bullet(\mathbb{Z}[G]Mod)$ of $\mathbb{Z}$ equipped with the trivial $G$-[[action]], hence an [[exact sequence]]

$$
  \cdots \to F_3 \to F_2 \to F_1 \to F_0 \to \mathbb{Z} \to 0
$$

of $\mathbb{Z}[G]$-[[modules]]. Let

$$
  Hom_{\mathbb{Z}[G]Mod}(F_\bullet, A)
  = 
  \left[
    Hom_{\mathbb{Z}[G]Mod}(F_0, A) 
      \stackrel{d^0}{\longrightarrow} 
    Hom_{\mathbb{Z}[G]Mod}(F_1,A) 
      \stackrel{d^1}{\longrightarrow} 
    Hom_{\mathbb{Z}[G]Mod}(F_2,A) 
      \stackrel{d^2}{\longrightarrow} 
      \cdots
  \right]
$$

be the corresponding [[cochain complex]]. Then the degree-$n$ group cohomology of $G$ with coefficient in $A$ is the degree-$n$ [[cochain cohomology]] of this complex

$$
  H^n_{Grp}(G,A)
  \simeq
  H^n(Hom_{\mathbb{Z}[G]Mod}(F_0, A))
  \coloneqq
  ker(d^n)/im(d^{n-1})
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Give a [[normal subgroup]] $K \hookrightarrow G$ the [[invariant|invariants]]-functor may be decomposed as a [[composition]] of the functor that forms $K$-invariants with that which forms $(G/K)$-invariants for the [[quotient group]]. This decomposition gives rise to a [[Grothendieck spectral sequence]] for the group cohomology. This is called the _[[Hochschild-Serre spectral sequence]]_.

=--


## Special aspects and special cases

The fully general definition [above](#InHomotopyTypeTheory) subsumes various cases that are not always discussed on the same footing in traditional literature. For emphasis we highlight these special cases separately.

* [Simplicial constructions and explicit formulas in low degree](#InLowDegree)

* [Structured group cohomology](#StructuredCohomology)

* [Nonabelian group cohomology](#NonabelianGroupCohomology)


### Simplicial constructions and explicit formulas in low degree
 {#InLowDegree}

We unwind the general abstract definition of group cohomology 
[above](#InHomotopyTypeTheory) in terms of constructions on [[simplicial sets]] (for cohomology of [[discrete groups]]) and [[simplicial presheaves]] (for cohomology of general [[group objects]]).

$\,$

Let $G$ be a [[discrete group]] and $A$ an [[abelian group|abelian]] [[discrete group]], regarded as equipped with the trivial $G$-[[action]]. Let $n \in \mathbb{N}$.

Write $\overline{W}G = G^{\times^\bullet}\in$ [[sSet]] for the [[nerve]] of the [[groupoid]] $*\sslash G$ and write $DK(A[n]) \in $ [[sSet]] for the [[image]] under the [[Dold-Kan correspondence]] of the [[chain complex]] which is the $n$-fold [[suspension of a chain complex]] of $A$. 


+-- {: .num_prop #DiscreteGroupCohomologyBySimplicialHomotopy}
###### Proposition

Then the degree-$n$ group cohomology of $G$ with [[coefficients]] in $A$ is the set

$$
  H^n_{Grp}(G,A) \simeq \pi_0 sSet(\overline{W}G, DK(A[n]))
$$

of [[homomorphisms]] of [[simplicial sets]] modulo [[simplicial homotopy]].

=--

+-- {: .proof}
###### Proof

By prop. \ref{GroupCohomologyInInfinityToposForTrivialAction} the group cohomology is 

$$
  H^n_{Grp}(G,A) \simeq \pi_0 \mathbf{H}(\mathbf{B}G, \mathbf{B}^n A)
  \,.
$$

By assumption the relevant [[(∞,1)-topos]] here is $\mathbf{H} = $ [[∞Grpd]], which for emphasis we might write "[[Disc∞Grpd]]".
This is [[presentable (∞,1)-category|presented]] by the standard [[model structure on simplicial sets]], $Disc\infty Grpd \simeq L_{whe} sSet$.

By the discussion at _[[delooping]]_ and at _[[∞-group]]_,
a presentation in [[sSet]], necessarily [[cofibrant object|cofibrant]], of the [[delooping]] $\mathbf{B}G \in \mathbf{H}$ is the standard [[bar construction]]

$$
  \overline{W}G
  = 
  \left(
    \cdots \to G \times G \times G
    \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
    G  \times G
    \stackrel{\longrightarrow}{\longrightarrow}
    G
    \to 
    {*}
  \right)
  \,,
$$

which is equivalently the [[nerve]] of the [[groupoid]] $*\sslash G$.

Moreover, by the discussion at _[[Dold-Kan correspondence]]_ a presentation of the [[Eilenberg-MacLane object]] $\mathbf{B}^n A$ is $DK(A[n]) \in sSet$, and this is a [[Kan complex]] and hence a [[fibrant object]] in the [[model category]] structure. 

Therefore by the discussion at _[[derived hom-space]]_ we have that $sSet(\overline{W}G, DK(A[n]))$ is a [[Kan complex]] which presents the required hom-$\infty$-groupoid.

=--

For low values of $n$ it is useful and easily possible to describe these simplicial maps explicitly. This we turn to now.

#### Degree-$1$ group cohomology 
 {#Degree1}

A degree-one group cocycle $c$, $[c] \in H^1_{Grp}(G,A)$
is just [[group homomorphism]] $G \to A$ -- a [[character]] of $G$.

#### Degree-$2$ group cohomology 
 {#Degree2}

We discuss here in detail and in components the special case of degree-2 group cohomology of a [[discrete group]] $G$ with coefficients in $A$ an [[abelian group|abelian]] [[discrete group]] and regarded as being equipped with the trivial $G$-[[action]].


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

This may be taken as the _definition_ of degree-2 group cohomology (with coefficients in abelian groups and with trivial action). The following proof shows how this _follows_ from the general simplicial presentation of prop. \ref{DiscreteGroupCohomologyBySimplicialHomotopy}.

+-- {: .proof}
###### Proof

By prop. \ref{DiscreteGroupCohomologyBySimplicialHomotopy} we have $H^2_{Grp}(G,A) \simeq \pi_0 sSet(\overline{W}G, DK(A[2]))$.

Notice that fully explicitly the 2-[[simplices]] in $\overline{W}G$ are

$$
  (\overline{W}G)_2
  =
  \left\{
  \left.
  \array{
    && {*}
    \\
    & {}^{g_1}\nearrow && \searrow^{g_2}
    \\
    {*}
    &&\stackrel{g_1 g_2}{\longrightarrow}&& {*}
  }
  \right|
  g_1, g_2 \in G
  \right\}
  \,,
$$

and the 3-simplices are 

$$
  (\overline{W}G)_3
  =
  \left\{
  \left.
  \array{
    {*} &&\stackrel{g_2}{\longrightarrow}&& {*}
    \\
    \uparrow^{g_1} &&{}^{g_1 g_2}\nearrow&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\longrightarrow}&&
    {*}
  }
  \;\;\;\;
  \Rightarrow
  \;\;\;\;   
  \array{
    {*} &&\stackrel{g_2}{\longrightarrow}&& {*}
    \\
    \uparrow^{g_1} &&\searrow^{g_2 g_3}&& \downarrow^{g_3}
    \\
    {*}
    &&\stackrel{g_1 g_2 g_3}{\longrightarrow}&&
    {*}
  }
  \right|
  g_1, g_2, g_3 \in G
  \right\}
  \,.
$$

Therefore a homomorphism of simplical sets $c \colon \overline{W}G \to DK(A[2])$ is in degree 2 a function

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


i.e. a map $c : G \times G \to K$. To be a simplicial homomorphism this has to extend to 3-[[simplices]] as:

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

Since there is a unique 3-cell in $DK(A[2])$ whenever the oriented sum of the $A$-labels of the boundary of the corresponding tetrahedron vanishes, the existence of the 3-cell on the right here is precisely the claimed cocycle condition.

A similar argument gives the coboundaries

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

### Relation with comonoid

1. The simplex category \Delta, whose objects are {1,2,3..n} and
morphisms are nondecreasing functions, is the UNIVERSAL "category
equipped with a monoid".

2. Dually, \Delta^op is the UNIVERSAL "category equipped with a comonoid".

3. For a group G, there's an adjunction between (G-reps) and (Vector
Spaces) by the forgetful functor and the free G-rep functor. The
composition gives you a COMONAD of (G-rep).

4. A comonad is just a categorification of a comonoid. More concretely
a comonad is a comonoid in End( (G-rep), (G-rep) ).

5. Since \Delta^op is has a universal comonoid, we connect both
contexts naturally. No wonder there's nice cohomology theory for
groups!

(ref: Categories-for-the-Working-Mathematician-[Mac-Lane])

### Structured group cohomology (topological groups and Lie groups)
 {#StructuredCohomology}

If the groups in question are not plain groups ([[group object]]s internal to [[Set]]) but groups with extra structure, such as [[topological group]]s or [[Lie group]]s, then their cohomology has to be understood in the corresponding natural context.

In parts of the literature cohomology of structured groups $G$ is defined in direct generalization of the formulas above as homotopy classes of morphisms from the simplicial object

$$
  \left(
    \cdots G \times G\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}G \stackrel{\longrightarrow}{\longrightarrow} *
  \right)
$$

to a simplicial object $N (\mathbf{B}^n A)$.

This is what is described [above](#InLowDegree) for _[[discrete groups]]_. But this does **not** in general give the right answer for structured groups: while the [[simplicial set]] $\overline{W}G = G^{\times^\bullet}$ is [[cofibrant object|cofibrant]] in the relevant model category presenting the ambient [[(∞,1)-topos]] [[Disc∞Grpd]], for $G$ a structured group the [[simplicial object]] given by the same formula is not in general already cofibrant. It needs to be further resolved, instead.

Specifically, for a [[Lie group]] $G$, the object

$$
  \left(
    \cdots G \times G\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}G \stackrel{\longrightarrow}{\longrightarrow} *
  \right)
$$


has to be considered as an [[Lie ∞-groupoid]]: an object in the [[model structure on simplicial presheaves]] over a [[site]] such as [[Diff]] or [[CartSp]]. As such it is in general **not** both cofibrant and fibrant. To that extent plain morphisms out of this object do **not** compute the correct [[derived hom-space]]s. Instead, the right definition of structured group cohomology uses the correct fibrant and cofibrant replacements.

Doing requires more work. This is discussed at 

* _[[Lie group cohomology]]_

See below at _[References - For structured groups](#ReferencesOnStructuredGroupCohomology)_ for pointers to the literature.

### Nonabelian group cohomology
 {#NonabelianGroupCohomology}

If the coefficient group $K$ is nonabelian, its higher [[delooping]]s $\mathbf{B}^n K$ do not exist. But [[n-groupoid]]s approximating this non-existant delooping do exists. Cohomology of $\mathbf{B}G$ with coefficients in these is called [[nonabelian group cohomology]] or [[Schreier theory]]. See there for more details.

## Examples

### Specific examples

#### Simple examples

* [[carrying]]

#### Cohomology of $\mathbb{Z}/2\mathbb{Z}$

For group cohomology of the [[group of order 2]] $\mathbb{Z}_2 = \mathbb{Z}/2\mathbb{Z}$ 
see at _Groupprops_, _[Group cohomology of cyclic group Z2](http://groupprops.subwiki.org/wiki/Group_cohomology_of_cyclic_group:Z2)_

#### Cohomology of $U(n)$, $O(n)$, etc.

We consider for $G$ a [[topological group]] such as

* the [[unitary group]] $U(n)$;

* the [[special unitary group]] $SU(n)$;

* the [[symplectic group]] $Sp(n)$

the corresponding group cohomology in terms of the cohomology of the [[classifying space]]/[[delooping]] $B G$.

For all $n \in \mathbb{N}$ we have

$$
\begin{aligned}
 H^\bullet(BU(n);\mathbb{Z}) &= \mathbb{Z}[c_1,\cdots,c_n] 
 \\
 H^\bullet(BSU(n);\mathbb{Z}) &= \mathbb{Z}[c_2,\cdots,c_n] 
 \\
 H^\bullet(BSp(n);\mathbb{Z}) &= \mathbb{Z}[p_1,\cdots,p_n]
\end{aligned}
$$

where $c_i\in H^{2i}$ and $p_i\in H^{4i}$.  

#### Heisenberg cocycle

The additive group on the [[Cartesian space]] $\mathbb{R}^2$ with group operation

$$
  (a,b) + (a',b') = (a + a' , b + b')
$$

carries a degree-2 group cocycle $\omega$ with values in $\mathbb{R}$ given by

$$
  \omega : ((a_1,b_1), (a_2,b_2)) \mapsto a_1 \cdot b_2
  \,.
$$

The cocycle condition for this is the identity

$$
  a_1 \cdot (b_2 + b_3) + a_2 \cdot b_3 
  =
  a_1 \cdot b_2 + (a_1 + a_2) \cdot b_3
$$

The [[group extension]] classified by this cocycle is the [[Heisenberg group]].

#### Galileo 2-cocycle

* [[Galileo 2-cocycle]]

### Classes of examples

#### Galois cohomology

The group cohomology of [[Galois groups]] is called _[[Galois cohomology]]_. See there for more details.

#### Lie algebra cohomology

We may regard a [[Lie algebra]] as an [[infinitesimal object|infinitesimal]] group. Under this perspective [[Lie algebra cohomology]] and [[infinity-Lie algebra cohomology]] is a special case of (higher) group cohomology. See there for details.

## Related concepts

* **group cohomology**

  * [[nonabelian group cohomology]], [[groupoid cohomology]]

  * [[Galois cohomology]]

* [[group homology]]

* [[group extension]]

  * [[Baer sum]]

* [[Lie group cohomology]] 

  * [[∞-group cohomology]]

  * [[∞-Lie groupoid cohomology]]

* [[equivariant cohomology]]

* [[Friedlander-Milnor isomorphism conjecture]]

## References 

### Original references

* [[S. Eilenberg]], [[S. MacLane]], _Relations between Homology and Homotopy Groups_.  Proceedings of the National Academy of Sciences 29:5 (1943), 155–158.  [doi](https://doi.org/10.1073/pnas.29.5.155).

* [[Samuel Eilenberg]], [[Saunders MacLane]], _Relations Between Homology and Homotopy Groups of Spaces_.  The Annals of Mathematics 46:3 (1945), 480.  [doi](https://doi.org/10.2307/1969165).

* [[Samuel Eilenberg]], [[Saunders MacLane]], _Relations Between Homology and Homotopy Groups of Spaces. II_.  The Annals of Mathematics 51:3 (1950), 514.  [doi](https://doi.org/10.2307/1969365).

* [[Dmitri Faddeev]], _On factor-systems in Abelian groups with operators_. (Russian), Doklady Akad. Nauk SSSR (N. S.) 58, (1947). 361–364.

### General

Standard textbook references on group cohomology include

* [[Kenneth Brown]],  _Cohomology of Groups_ , Graduate Texts in Mathematics, 87 (1972)

and specifically with an eye towards cohomology of [[finite groups]]

* [[Michael Atiyah]], _Characters and cohomology of finite groups_, Publications Math&#233;matiques de l'IH&#201;S, 9 (1961), p. 23-64  ([Numdam](http://www.numdam.org/item?id=PMIHES_1961__9__23_0))

*  [[Alejandro Adem]], [[R. James Milgram]], _Cohomology of Finite Groups_, Springer 2004

Exposition includes

* [[Alejandro Adem]], _Lectures on the cohomology of finite groups_ ([pdf](http://www.math.uic.edu/~bshipley/ConMcohomology1.pdf))

* {#Epa10} [[Narthana Epa]], _Platonic 2-groups_, 2010 ([pdf](http://www.ms.unimelb.edu.au/documents/thesis/Epa-Platonic2-Groups.pdf))


An introduction to group cohomology of a group $G$ as the cohomology of the [[classifying space]] $B G$ is for instance in 

* Joshua Roberts, _Group cohomology: a classifying space perspective_ ([pdf](http://www.piedmont.edu/math/jroberts/notes/qualifyingtalk.pdf))

* _Advanced course on classifying spaces and cohomology of groups_ ([ps](www-irma.u-strasbg.fr/~henn/notes.ps))

Discussion of the cohomology of [[discrete groups]] with abelian coefficients in terms of [[crossed modules]] instead of [[chain complexes]] (an intermediate step in the [[Dold-Kan correspondence]]) is in chapter 12 of

* R. Brown, P. Higgins, R. Sivera, _Nonabelian algebraic topology_ ([pdf](http://www.bangor.ac.uk/%7Emas010/pdffiles/rbrsbookb-e040609.pdf), [web](http://www.bangor.ac.uk/~mas010/nonab-a-t.html))

Cohomology of [[simplicial groups]] is discussed for instance in

* Sebastian Thomas, _On the second cohomology group of a simplicial group_ ([pdf](http://www.math.rwth-aachen.de/~Sebastian.Thomas/publications/Thomas_On_the_second_cohomology_group_of_a_simplicial_group.pdf))


Much of what is called "[[nonabelian cohomology]]" in the existing literature concerns the case of nonabelian group cohomology with coefficients in the [[automorphism 2-group]] $AUT(H)$ of some possibly nonabelian group $H$.

This is the topic of [[Schreier theory]].

A random example for this use of terminology would be

* Roggenkamp, Scott, _Automorphisms and nonabelian cohomology_ ([pdf](http://www.math.virginia.edu/~lls2l/automorphisms_and_nonabelian.pdf))

For a conceptual discussion of nonabelian group cohomology see

* [[John Baez]], [[Mike Shulman]], _[[Lectures on n-Categories and Cohomology]]_ ([arXiv](http://arxiv.org/abs/math/0608420))

Group cocycles classify [[group extensions]]. This is often discussed only for 2-cocycles and extensions by ordinary groups. Higher cocycles classify extensions by [[2-group]]s and further by [[infinity-groups]]. In the context of [[crossed complexes]], which are models for _strict_ $\infty$-groups, this is discussed for instance in

* [[Johannes Huebschmann]], _Crossed $n$-fold extensions and group cohomology_ ([web](http://dx.doi.org/10.1007/BF02566688))


### On structured group cohomology
 {#ReferencesOnStructuredGroupCohomology}

In

* [[Jim Stasheff]], _Continuous cohomology of groups and classifying spaces_  Bull. Amer. Math. Soc. Volume 84, Number 4 (1978), 513-530 ([web](http://projecteuclid.org/DPubS?service=UI&version=1.0&verb=Display&handle=euclid.bams/1183540920))

$n$-cocycles on a topological group $G$ with values in a topological abelian group $A$ are considered as continuous maps $G^{\times n}\to A$ (p. 3 ).

A definition in terms of [[derived functor|Ext-functors]] and comparison with the naive definition is in 

* David Wigner, _Algebraic cohomology of topological groups_ Transactions of the American Mathematical Society, volume 178 (1973)([pdf](http://egg.epfl.ch/~nmonod/bonn/Wigner_1973.pdf))

A classical reference that considers the cohomology of Lie groups as topological spaces is

* [[Armand Borel]], _Homology and cohomology of compact connected Lie groups_ ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC1063923/pdf/pnas01596-0040.pdf))

A corrected definition of topological group cohomology has been given by Segal

* [[Graeme Segal]], _Cohomology of topological groups_ In Symposia Mathematica, Vol. IV (INDAM, Rome, 1968/69), pages 377{387. Academic Press, London, (1970).

* [[Graeme Segal]], _A classifying space of a topological group in the sense of Gel'fand-Fuks. Funkcional. Anal. i Prilozen.,
9(2):48{50, (1975).

For [[reductive algebraic groups]]:

* {#HKLV98} [[Hélène Esnault]], [[Bruno Kahn]], [[Marc Levine]], [[Eckart Viehweg]], _The Arason invariant and mod 2 algebraic cycles_,  J. Amer. Math. Soc. 11 (1998), 73-118  ([pdf](https://www.uni-due.de/~bm0032/publ/Arason.pdf),[publisher page](http://www.ams.org/journals/jams/1998-11-01/S0894-0347-98-00248-3/))


### On various topological groups
 {#OnTopologicalGroups}

Some references pertaining to the [[cohomology]] of the [[classifying space]]/[[delooping]] $B G$ for $G$ a [[topological group]] ([[characteristic class]]es).

#### Compact Lie groups

Cohomology of the [[classifying space]] $B G$ for $G$ the [[topological group]] underlying a [[compact topological space|compact]] [[Lie group]].

* [[John Milnor]], [[Jim Stasheff]], _Characteristic Classes_ , Princeton University Press and University of Tokyo Press, Princeton, New Jersey, (1974).
 {#MilnorStasheff}

* Mark Feshbach, _Some General Theorems on the Cohomology of Classifying Spaces of Compact Lie Groups_ Transactions of the American Mathematical Society Vol. 264, No. 1 (Mar., 1981), pp. 49-58 ([JSTOR](http://www.jstor.org/stable/1998409))

* [[Donald Yau]], _Cohomology of unitary and symplectic groups_ ([pdf](http://www.mathnet.ru/links/c8897bc54ec0a1a49d03ca681d53db7b/ljm147.pdf))

* D. Benson, [[John Greenlees]], _Commutative algebra for cohomology rings of classifying spaces of compact Lie groups_ ([pdf](http://hopf.math.purdue.edu/Benson-Greenlees/Liegroupca.pdf))

* [[Eric Friedlander]], Guido Mislin, _Cohomology of classifying spaces of complex Lie groups and related discrete groups_ Commentarii Mathematici Helvetici
Volume 59, Number 1, 347-361,

#### The unitary groups $U(n)$

For $U$ the [[unitary group]], the [[integral cohomology]] of the [[classifying space]] $B U(n)$ consists of the [[Chern class]]es, one in every even degree.

#### The (special) orthogonal groups $O(n)$, $SO(n)$

The cohomology of $B O(n)$ ([[orthogonal group]]) and $B SO(n)$ ([[special orthogonal group]]) with coefficients in $\mathbb{Z}_2$ is discussed in ([MilnorStasheff, 1974](#MilnorStasheff)).

The cohomology of $B O(n)$ with coefficients in $\mathbb{Z}$ and $\mathbb{Z}_{2 m}$ was found in 

* Emery Thomas , _On the cohomology of the real Grassman complexes and the characteristic classes of the $n$-plane bundle_ , Trans. Amer. Math. Soc. 96 (1960), 67&#8211;89.

The [[ring]]-structure on the cohomology with integer coefficients was given in

* E. Brown (Jr.), _The cohomology of $B SO(n)$ and $B O(n)$ with integer coefficients_ Proc. AMS Soc. 85 (1982)

* Mark Feshbach, _The integral cohomology rings of the classifying spaces of $O(n)$ and $SO(n)$, Indiana Univ. Math. J. 32 (1983), 511&#8211;516.

For [[twisted cohomology|local coefficients]] see

* {#Cadek99} [[Martin Čadek]], _The cohomology of $B O(n)$ with twisted integer coefficients_, J. Math. Kyoto Univ. 39 (1999), no. 2, 277&#8211;286 ([Euclid](http://projecteuclid.org/euclid.kjm/1250517912))

* Richard Lastovecki, _Cohomology of $B O(n_1) \times \cdots \times B O(n_m)$ with local integer coefficients_ Comment.Math.Univ.Carolin. 46,1 (2005)21&#8211;32 ([pdf](http://www.emis.de/journals/CMUC/pdf/cmuc0501/lastovec.pdf))

#### For spin-group, string-group, ... 

The [[Whitehead tower]] of the [[orthogonal group]] starts out with 

[[fivebrane group]] $\to$ [[string group]] $\to$ [[spin group]] $\to$ [[special orthogonal group]] $\to$ [[orthogonal group]]



Group cohomology of the [[spin group]] (cohomology of the [[classifying space]] $B Spin$) is discussed in

* Emery Thomas, _On the cohomology groups of the classifying space for the stable spinor group_ , Bol. Soc. Mex. (1962), 57 - 69

* Masana Harada, Akira Kono, _Cohomology mod 2 of the classifying space of $Spin^c(n)$_ Publications of the Research Institute for Mathematical Sciences archive
Volume 22 Issue 3, Sept. (1986) ([web](http://dl.acm.org/citation.cfm?id=23393)) 
 
Group cohomology of the [[string group]] (cohomology of the [[classifying space]] $B String$) is discussed in


* _On the integral cohomology of the seven-connective cover of B O_ Bull. Austral. Math. Soc. Vol 38 (1988) ([pdf](http://journals.cambridge.org/download.php?file=%2FBAZ%2FBAZ38_01%2FS0004972700027179a.pdf&code=8374f17b7aa6ffb83f42f347c677729f))

#### The exceptional Lie groups

Cohomology of [[classifying space]]s of [[exceptional Lie group]]s. 

* Akira Kono, Mamoru Mimura, _Cohomology mod 3 of the classifying space of the Lie group $E_6$_ , Math. Scand. 46 (1980) ([pdf](http://www.mscand.dk/article.php?id=2533))

#### Loop groups of compact Lie groups

* Daisuke Kishimoto, Akira Kono, _Cohomology of the classifying spaces of loop groups_ ([pdf](http://www.math.kyoto-u.ac.jp/preprint/2004/13kishimoto.pdf))

### Online references

Some of the above materiel is taken from discussion at

* MO, _[Group cohomology of compact Lie group with integer coeffient ](http://mathoverflow.net/questions/75389/group-cohomology-of-compact-lie-group-with-integer-coeffient)_

[[!redirects group cocycle]]
[[!redirects group cocycles]]