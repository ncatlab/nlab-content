

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

An object in a [[model category]] is fibrant if all morphisms into it have extensions along acyclic cofibrations. An **algebraic fibrant object** is a fibrant object equipped with a _choice_ of such extensions.

Under mild conditions, the category $Alg C$ of algebraic fibrant objects in a model category $C$ forms itself naturally a model category which is [[Quillen equivalence|Quillen equivalent]] to $C$, and in which all objects are fibrant.  Notably, $Alg C$ is always a [[category of fibrant objects]].


## Definition

+-- {: .un_defn}
###### Definition

Let $C$ be a [[cofibrantly generated model category]] such that 

* all acyclic cofibrations are [[monomorphism]]s.

Choose a set $\{A_j \to B_j\}_{j \in J}$ of acyclic cofibrations such that 

* the [[domain]]s $A_j$ are [[small object]]s;

* an object $X \in C$ is fibrant precisely if it has the [[right lifting property]] against these morphisms.

An **algebraic fibrant object** in $C$ is a fibrant object of $C$ together with a choice of lifts ("fillers") $\sigma_j : B_j \to X$ in

$$
  \array{
    A_j &\to& X
    \\
    \downarrow & \nearrow_{\mathrlap{\sigma_j}}
    \\
    B_j
  }
$$

for each morphism $A_j \to X$, $j \in J$. 

Write $Alg C$ for the category whose objects are algebraic fibrant objects in $C$ and whose morphisms are morphisms in $C$ that respect the chosen lifts.

=--

+-- {: .un_remark}
###### Remark

The set $J$ can be taken to be that of all generating acyclic cofibrations, if their domains are small. But often there are smaller subsets that still characterize all fibrant objects.

=--

+-- {: .un_theorem #ModelStructureTheorem}
###### Theorem

The [[forgetful functor]] [[adjunction]]

$$
  (F \dashv U) : Alg C \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}} C 
$$

induces the [[transferred model structure]] on $Alg C$: the fibrations
and weak equivalences in $Alg C$ are those of the underlying morphisms in $C$.

In particular, every object in $Alg C$ is fibrant.

The [[Quillen adjunction]] $(F \dashv U)$ is a [[Quillen equivalence]].


=--


This is ([Nikolaus, theorem 2.18](#Nikolaus))

+-- {: .un_remark}
###### Remark

Since fibrations in $Alg C$ are created in $C$, and any algebraically fibrant object is, in particular, fibrant, every object in the model category $Alg C$ is fibrant.  Thus almost any model category is equivalent to one in which all objects are fibrant.  However, in general not all objects in $Alg C$ will be cofibrant, even if this was true in $C$ itself.

=--

## Details

We spell out the constructions and lemmas that yield the [theorem on the model structure](#ModelStructureTheorem). In the course of this we also discuss a few results of interest in their own right, such as the monadicity, local presentability and combinatoriality of $Alg C$.

### The left adjoint

We describe explicitly the [[left adjoint]] $F : C \to Alg C$ to the [[forgetful functor]] $U : Alg C \to C$. This follows [[Richard Garner]]'s improved version of the [[small object argument]] ([Garner](#Garner)).


For $X \in C$ define a new object $X_\infty$ inductively as follows.

+-- {: .un_defn}
###### Definition

$X_1$ is the [[pushout]] (in $C$) 

$$
  \array{
     \coprod A_j &\to& X
     \\
     \downarrow && \downarrow
     \\
     \coprod B_j &\to& X_1
  }
  \,,
$$

here the disjoint unition is taken over all $j$ and all morphisms $A_j \to X$.

=--

+-- {: .un_defn}
###### Remark

This pushout adds all possible "horn" fillers to $X$, given by the $B_j \to X_1$. However, after adding the new fillers there may also appear new horns. So we continue this procedure iteratively by filling these new horn.

Since $\coprod A_j \to \coprod B_j$ is an acylcic cofibration in $C$, so is its its pushout, hence by assumption the pushout $X \to X_1$ is a monomorphism. This implies that if an $A_j \to X_1$ factors through $X \to X_1$ then it does so uniquely.

=--

+-- {: .un_defn #DefOfXInfty}
###### Definition

Let $X_2$ be the [[pushout]]

$$
  \array{
     \coprod A_j &\to& X_1
     \\
     \downarrow && \downarrow
     \\
     \coprod B_j &\to& X_2
  }
  \,,
$$

where now the coproduct is over those morphisms $A_j \to X$ that do _not_ factor throuth $X \to X_1$.

Proceeding this way yields a sequence of acyclic cofibrations

$$
  X \to X_1 \to X_2 \to X_3 \to \cdots 
  \,.
$$

We set

$$
  X_\infty :=  \lim_\to (X \to X_1 \to X_2 \to X_3 \to \cdots )
$$

be the [[colimit]] over this sequence.

=--

+-- {: .un_observation}
###### Observation

The object $X_\infty$ inherits canonical fillers: since by all $A_j$ are [[small object]]s we have that every morphism $A_j \to X_\infty$ factors through one of the intermediate $X_i$. Then for any of the morphisms $A_j \to B_j$ in $J$ the corresponding morphism $B_j \to X_{i+1} \to X_\infty$ provides a filler. 

=--

+-- {: .un_prop}
###### Proposition

The assignment  $F : X \to X_\infty$ with $X_\infty$ regarded as an algebraic fibrant objects as above constitutes a left [[adjoint functor]] $F : C \to Alg C$ to the [[forgetful functor]] $U : Alg C \to C$.

The unit of this [[adjunction]] is the inclusion $X \to X_\infty$ given by the above construction and is hence a weak equivalence.

=--

+-- {: .proof}
###### Proof

We establish the hom-isomorphism of the [[adjunction]] and its construction by the unit of the adjunction: For any $Z \in Alg C$ and $\phi : X \to U(Z)$ any morphism in $C$, we need to show that there is a unique [[commuting diagram]]

$$
  \array{
    X &\stackrel{\phi}{\to}& Z
    \\
    \downarrow & \nearrow_{\exists ! \phi_\infty}
    \\
    X_\infty
  }
  \,.
$$

Since by assumption $Z$ has all fillers we have commuting diagrams

$$
  \array{
      A_j &\to& X 
     \\
     \downarrow && \downarrow^{\mathrlap{\phi}}
     \\
     B_j &\to& Z
  }
  \,.
$$

By the universality of the pushout these induce unique morphisms 

$$
  \array{
    X &\stackrel{\phi}{\to}& Z
    \\
    \downarrow & \nearrow_{\phi_1 }
    \\
    X_1
  }
  \,.
$$

By induction this induces morphisms $\phi_n : X_n \to Z$ that form a [[cocone]] under $(X \to X_1 \to X_2 \to \cdots )$. Therefore there is a unique morphusm $\phi_\infty$ as indicated.

=--

+-- {: .un_corollary}
###### Corollary

The morphisms $F(j) : F A_j \to F B_j$ have [[retract]]s.

=--


+-- {: .proof}
###### Proof

Since $F$ is [[left adjoint]] to $U$ the condition that $F A_j \to F B_j \stackrel{r}{\to} F A_j$ is the [[identity]] is equivalent to its [[adjunct]], the diagonal in

$$
  \array{
    A_j &\stackrel{j}{\to}& B_j &\stackrel{r}{\to}& A_j
    \\
    \downarrow && \downarrow &\searrow^{\mathrlap{\tilde r}}& \downarrow
    \\
    U F A_j &\stackrel{U F (j)}{\to}& U F B_j &\stackrel{U F r}{\to} & U F A_j
  }
$$

being the unit of the adjunction $A_j \to U F A_j$. Take $\tilde r$ to be the (unique) filler for this morphism.

=--

### Monadicity of the forgetful functor {#Monadicity}

We now give a formal justification for calling the objects of $Alg C$ _algebraic_ objects by showing that $Alg C$ is the category of algebras over an [[algebraic theory]] in $C$, or more precisely that it is the category of [[algebras over a monad|algebra over the monad]] $F \circ U$ on $C$ 

+-- {: .un_theorem}
###### Theorem

The functor $U : Alg C \to C$ is [[monadic]].

=--

This is ([Nikolaus, prop. 24](#Nikolaus))


+-- {: .proof}
###### Proof

By one of the equivalent statements of [[Beck's monadicity theorem]] we have to check that

1. $U$ has a [[left adjoint]],
1. $U$ reflects [[isomorphisms]] (i.e. it is [[conservative functor|conservative]]), and
1. $D$ has, and $U$ [[preserved limit|preserves]], coequalizers of $U$-split pairs.


The first item we already checked above. 

For the second item it is sufficient to observe that if $f : X \to Y$ is a morphism in $Alg C$ such that $U f$ has an inverse $g : U Y \to U X$, then it follows that $g$ must preserve fillers, hence itself constitutes the underlying morphism of an inverse if $f$ in $Alg C$.

For the third item, let $f,g : X \to Y$ be two morphisms in $Alg C$ such that the [[coequalizer]]

$$
  U X \stackrel{\overset{U f}{\to}}{\underset{U g}{\to}}
  U Y
  \stackrel{\pi}{\to}
  Q
$$

exists in $C$, together with [[section]]s $s$ of $\pi$ and $t$ of $U(f)$ such that $s \circ \pi = U(t) \circ t$. We need to equip $Q$ with fillers such that it becomes the coequalizer of $f,g$ in $Alg C$.

For $h : A_j \to Q$ a horn, declare that its filler is the the chosen filler of $s \circ h$

$$
  \array{
    A_j &\stackrel{h}{\to}& Q 
    \\
    \downarrow && \downarrow^{\mathrlap{s}} & \searrow^{\mathrlap{Id}}
    \\
    B_j &\to& Y &\stackrel{\pi}{\to} & Q
  }
  \,.
$$

We check now that this choice indeed makes $Q$ the coequalizer in $Alg C$.

First of all we need to check that $\pi$ preserves the chosen fillers.

So given a filler 

$$
  \array{
    A_j &\stackrel{k}{\to}& Y
    \\
    \downarrow & \nearrow_{\mathrlap{\hat k}}
    \\
    B_j
  }
$$

it is sent by $\pi$ to the filler

$$
  \array{
    A_j &\stackrel{k}{\to}& Y &\stackrel{\pi}{\to}& Q
    \\
    \downarrow & \nearrow && \nearrow_{\pi \hat k}
    \\
    B_j
  }
$$

of $k \pi$. This is supposed to be the same as

$$
  \array{
    A_j &\stackrel{k}{\to}& Y &\stackrel{\pi}{\to}& Q &\stackrel{s}{\to}& Y &\stackrel{\pi}{\to}& Q
    \\ 
    \downarrow && && & \nearrow_{\hat r} && \nearrow_{\pi \hat r}
    \\
    B_j 
  }
  \,.
$$

Now use the relation $U(f) t = Id$ to rewrite the first diagram equivalently as

$$
  \array{
    A_j &\stackrel{k}{\to}& Y &\stackrel{t}{\to}& X &\stackrel{U(f)}{\to}& 
    Y &\stackrel{\pi}{\to}& Q
    \\
    \downarrow &&&&&  \nearrow_{\mathrlap{\hat g}} &&  \nearrow_{\pi \hat k}
    \\
    B_j
  }
$$

and the relation $U(g) t =  s \pi$ to rewrite the second diagram equivalently as

$$
  \array{
    A_j &\stackrel{k}{\to}& Y &\stackrel{t}{\to}& X &\stackrel{U(g)}{\to}& Y &\stackrel{\pi}{\to}& Q
    \\ 
    \downarrow && && & \nearrow_{\hat r} && \nearrow_{\pi \hat r}
    \\
    B_j 
  }
  \,.
$$

This show that the fillers $\hat k$ and $\hat r$ are images under $U(f)$ and $U(g)$, respectively, of a single filler in $X$. Since $\pi$ coequalizes, it follows that $\pi \hat k = \pi \hat r$.

Finally we need to show that the coequalizing morphism $\pi$ in $Alg C$ thus established is indeed universal with this property.

For $\phi : Y \to Z$ a coequalizing morphism in $Alc C$, the fact that $Q$ is a coequalizer in $C$ already gives a unique morphism $\phi_Q$ in

$$
  \array{
    X & \stackrel{\overset{f}{\to}}{\underset{g}{\to}} & Y
    &\stackrel{\pi}{\to} & Q
    \\
    && {}^{\mathllap{\phi}}\downarrow & \swarrow_{\mathrlap{\exists ! \phi_Q}}
    \\
    && Z
  }
  \,.
$$

So it is sufficient to observe that $\phi_Q$ preserves chosen fillers. But this is true be the above construction, which says that the chosen fillers in $Q$ are the images of the chosen fillers in $Y$.

=--


### Solidity of the forgetful functor {#Solidity}


+-- {: .un_prop}
###### Proposition

The [[forgetful functor]] $U : Alg C \to C$ is a [[solid functor]].

=--

We discuss the proof for a slightly simpler statement, from which the full statement follows easily. 

+-- {: .un_lemma #SolidityLemma}
###### Lemma

Let $Y$ be an algebraic fibrant object, $X$ an object in $C$ and 

$$
  f : Y \to X
$$

a morphism in $C$ (really: $U(X) \to Y$). Then there is an algebraic fibrant object $X^f_\infty$ and a morphism $X \to X^f_\infty$ such that the composite 

$$
  Y\to X \to X^f_{\infty}
$$

is a morphism of algebraic fibrant objects and it is [[initial object|initial]] with this property: 

for every morphism $\phi : X \to Z$ in $C$ with $Z$ an algebraic fibrant object such that the composite $Y \to X \to Z$ preserves distinguished fillers, there exists a unique morphism $\phi_\infty : X^f_\infty \to Z$ such that we have a [[commutative diagram]]

$$
  \array{
    Y 
    \\
    {}^{\mathllap{f}}\downarrow & \searrow^{\mathrlap{alg}}
    \\
    X &\stackrel{\phi}{\to}& Z
    \\
    \downarrow & \nearrow_{\mathrlap{\exists ! \phi_\infty}}
    \\
    X^f_\infty
  }
  \,.
$$

Moreover, if $f$ is a [[monomorphism]] in $C$, then $X \to X^f_\infty$ is an acyclic cofibration.

=--

This is ([Nikolaus, prop. 2.6](#Nikolaus)).

The naive idea would be to equip $X$ with distinguished fillers $f \hat k$

$$
  \array{
    A_j &\stackrel{k}{\to}& Y &\stackrel{f}{\to}& X
    \\
    \downarrow & \nearrow_{\mathrlap{\hat k}} && \nearrow_{f \mathrlap{\hat k}}
    \\
    B_j
  }
$$

for each distinguished filler $\hat k$. But since the composite may factor through $Y$ in many ways, this will not give a unique notion of filler. Therefore we shall iteratetively form colimits that equate these potentially different fillers.

+-- {: .proof}
###### Proof

Let $H$ be the set of morphisms of the form $h : A_j \to X$ that factor through $f : Y \to X$. For each $h \in H$ let $F_h$ be the set of images of distinuished fillers $B_j \to X$.

Set

$$
  X_H := \lim_\to
  \left(
     \array{
       (B_j)_h && (B_{j'})_{h'} && \cdots
       \\
       & {}_{\mathllap{\phi \in F_h}}\searrow & \downarrow^{\mathrlap{\phi' \in F_{h'}}}
       & \cdots
       \\
       && X
     }
  \right)
$$

where on the right we take the [[colimit]] over the diagram with one object $(B_j)_h$ per morphism $h : A_j \to X$ that factors through $Y$,  and one morphism $(B_j)_h \to X$ per induced distinguished filler obtained from a choice of factorization through $Y$.


This comes with a canonica [[cocone]]-morphism $X \to X_H$. Continue this way to build $X_{H'}$ by coequalizing the different ways morphisms into $X_H$ may factor through $X$, etc. to obtain a sequence

$$
  X \to X_H \to X_{H'} \to X_{H''} \to \cdots
$$

and set

$$
  X_0^f := \lim_\to (X \to X_H \to X_{H'} \to X_{H''} \to \cdots)
  \,.
$$

Notice that if $f$ is a [[monomorphism]] then all factorizations are unique and hence $X \to X_0^f$ is an [[isomorphism]].


The object $X_0^f$ can be seen to have the desired universal factorization property. But it may not yet be itself algebraically fibrant.  So we conclude by essentially applying the construction of the left adjoint $F$. But we start with letting $X_1^f$ be the pushout

$$
  \array{
    \coprod_j A_j &\to& X_0^f
    \\ 
    \downarrow && \downarrow
    \\
    \coprod_j B_j &\to& X_1^f
  }
$$

where now the coproduct is over all morphisms that do not factor through $Y$. After that we proceed exactly as we did for the construction for $F$ and obtain a sequence

$$
  X_0^f \to X_1^f \to X_2^f \to \cdots
  \,.
$$

Finally we set

$$
  X_\infty^f := \lim_\to(X_0^f \to X_1^f \to X_2^f \to \cdots)
  \,.
$$


One checks that this has the claimed properties (...).

As before, the inclusion $X_0^f \to X_\infty^f$ is an acyclic cofibration. Hence by the above remarks in the case that $f$ is a monomorphism also $X \to X_\infty^f$ is an acyclic cofibration.

=--

By replacing in this proof factorization through a single $Y$ by factorization through a family of $Y$s one finds that $U$ is a [[solid functor]].

### Limits and colimits of algebraic objects {#LimitsAndColimits}

+-- {: .un_prop }
###### Proposition

The category $Alg C$ has all [[limit]]s and [[colimit]]s in $C$.

The limits and the [[filtered colimit]]s (but not the general colimit)s are [[created limit|created]] by $U$.


=--

+-- {: .proof}
###### Proof

Consider first limits: for $K : J \to Alg C$ a [[diagram]] and $\lim_{\leftarrow} U K$ its limit in $C$, let $A_j \to \lim_{\leftarrow} U K$ be a horn. Since all the composite maps $A_J \to \lim_{\leftarrow} U K \to U K(j)$ have distinguished fillers and since the morphisms between these respect these fillers, we get a cone of fillers with tip $B_j$ over $U K$. The universal cone morphism $B_j \to \lim_{\leftarrow} U K$ provides then a distinguished filler for the limit. By the same argument, any cone $const_T \to \lim_{\leftarrow} U K$ in $Alg_C$ whose underlying cone in $C$ is a limiting cone is also limiting in $Alg C$.

Now consider [[filtered colimit]]s. By assumption the domains $A_j$ are [[small object]]s. Therefore for $K : I \to C$ a [[filtered diagram]] and $L := \lim_{\to} K$ its [[filtered colimit]], any morphism $A_j \to L$ factors through one of the $K_i$.  This provides a filler $B_j \to K_i \to L$. Observe that while neither $i$ nor the filler $B_j \to K_i$ are uniquely determined, its image in $L$ is. This makes $L$ an object in $Alg C$. By the same argument one finds that it is the universal cocone under $K$ in $Alg C$.


Now for $K : J \to Alg C$ a general diagram with colimit $X := \lim_\to U K$ in $C$, we use the above fact that $U$ is a [[solid functor]] to deduce that $X_\infty^f$ is the colimit of $K$ in $Alg C$.

=--

While this gives a general prescription for computing colimits, the following lemma asserts a slightly simpler way for computing certain [[pushout]]s in $Alg C$. This will be needed for establishing the model category structure.

+-- {: .un_lemma #PushoutLemma}
###### Lemma

Let $i : A \to B$ be a morphism in $C$ and 

$$
  \array{
    F A &\to& Y
    \\
    {}^{\mathllap{F i}}\downarrow
    \\
    F B
  }
$$

a diagram in $Alg C$. Then

* its [[pushout]] in $Alg C$ is $(B \coprod_A U Y)_\infty^f$, where $f : U Y \to B \coprod_A U Y$ is the canonical morphism;

* if $i : A \to B$ is an acyclic cofibration then so is $Y\to (B \coprod_A U Y)_\infty^f$.
=--

This is ([Nikolaus, prop 2.14](#Nikolaus)).

+-- {: .proof}
###### Proof


First check that $(B \coprod_A U Y)_\infty^f$ has the universal property of the pushout: for any $Z \in Alg C$ we have by the [above proposition](#SolidityLemma) that morphisms $(B \coprod_A U Y)_\infty^f \to Z$ are in bijection to morphisms $B \coprod_A U Y \to U Z$ in $C$ such that the composition 

$$
  U Y \stackrel{f}{\to} B \coprod_A U Y \to U Z
$$

preserves distinguished fillers.

This in turn is the same as a morphism $g_1 : Y \to Z$ in $Alg C$ and a morphism $g_2 : B \to U Z$ in $C$ that agree on $A$. By [[adjunction]] $(F \dashv U)$ this corresponds to an [[adjunct]] $\tilde g_2: F B \to Z$. This establishes the pushout property of $(B \coprod_A U Y)_\infty^f$.

To show that $Y \to (B \coprod_A U Y)_\infty^f$ is an acyclic cofibration of $i : A \to B$ is, recall that this morphism is the composite

$$
  Y \stackrel{f}{\to} B \coprod_A U Y \to (B \coprod_A U Y)_\infty^f
  \,.
$$

Here the first morphism $f$ is an acyclic cofibration because it is the [[pushout]] of the acyclic cofibration $i$. Therefore by assumption $f$ is a [[monomorphism]] and by the [remarks in the solidity lemma](#SolidityLemma) the morphism $B \coprod_A U Y \to (B \coprod_A U Y)_\infty^f$ is an acyclic cofibration. Hence so is the composite of the two.

=--


### Transferred model structure



+-- {: .un_theorem}
###### Theorem

Under the above conditions, $Alg C$ becomes a [[model category]] with the $U$-[[transferred model structure]]: weak equivalences and fibrations in $Alg C$ are those morphisms that are so in $C$.

=--

This appears as ([Nikolaus, def. 2.15](#Nikolaus)).

+-- {: .proof}
###### Proof

This follows from the [above result](#Solidity) that $U$ is a _solid functor_ as described in detail at [[solid functor]] by observing that the _acyclicity condition_ required there follows as in the discussion of the solidity of $U$ [above](#SolidityLemma), using the assumption that all acyclic cofibrations in $C$ are [[monomorphism]]s.

We spell out the argument, following ([Nikolaus](#Nikolaus)).

By the conditions listed at [[transferred model structure]] it is sufficient to check that

1. $U$ preserves [[small object]], which is the case in particular if it preserves [[filtered colimit]]s;

1. $U$ sends [[sequential colimit]]s of [[pushout]]s of images under $F$ of generating acyclic cofibrations to weak equivalences.

The first item is true by the [above discussion](#LimitsAndColimits) of filtered colimits in $Alg C$.

That the second item holds follows from the above [pushout lemma](#PushoutLemma) which asserts that $U$-images of pushouts of $F$-images of generating acyclic cofibrations are acylic cofibrations, and again by the fact that $U$ preserves filtered colimits, which implies that it preserves the [[transfinite composition]] of these acyclic cofibrations.

=--

+-- {: .un_corllary}
###### Corollary

The functor $U$ preserves acyclic cofibrations.

=--

+-- {: .un_theorem}
###### Theorem

The [[Quillen adjunction]] 

$$
  (F \dashv U) : Alg C \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}
  C
$$

is a [[Quillen equivalence]].
=--

This appears as ([Nikolaus, theorem 2.18](#Nikolaus))

+-- {: .proof}
###### Proof


We observe that the unit and counit of $(F \dashv U)$ are both weak equivalences:

the unit of the adjunction is $X \to X_\infty$ is by the [above construction](#DefOfXInfty) a [[transfinite composition]] of acyclic cofibrations (in fact a fibrant replacement) hence in particular a weak equivalence. Moreover, the unit is a [[section]] of the counit in that 

$$
  \array{
     X &\to& F X
     \\
     & {}_{\mathllap{Id}}\searrow & \downarrow
     \\
     && X
  }
  \,.
$$

Hence by [[category with weak equivalences|2-out-of-3]] also $X \to F X$ is a weak equivalence. 

This implies that $(F \dashv U)$ induces an [[equivalence of categories]] on the [[homotopy categories]]. Since $R$ equals its total right [[derived functor]] (since every object in $Alg C$ is fibrant) this means that $(F \dashv)$ is a Quillen equivalence.

=--

### Local presentability and combinatoriality {#LocalPresentability}

+-- {: .un_prop}
###### Proposition

If $C$ is a [[locally presentable category]] then so is $Alg C$.

=--

+-- {: .proof}
###### Proof

By the [above](#Monadicity) we know that $Alg C$ is the category of [[algebras over a monad]] $U\circ F : C \to C$.

We invoke the <a href="http://ncatlab.org/nlab/show/locally%20presentable%20category#AlgebrasOverAnAccessibleMonad">theorem on local presentability of categories of algebras</a> discussed at [[locally presentable category]]. This says that it is sufficient to check that $U \circ F$ is an [[accessible functor]], hence that it preserves [[filtered colimit]]s. Now $F$ is a left adjoint and hence preserves all colimits, while we checked [above](#LimitsAndColimits) that $U$ preserves filtered colimits.

=--

+-- {: .un_corollary}
###### Corollary

If $C$ is a [[combinatorial model category]] then so is $Alg C$.

=--


## Examples

### Algebraic $\infty$-groupoids {#AlgebaicHigherCategories}

The standard [[model structure on simplicial sets]] $sSet_{Quillen}$ models the [[(∞,1)-category]] [[∞Grpd]] of [[∞-groupoid]]s: its fibrant objects are precisely the [[Kan complex]]es. But a Kan complex is a model for an $\infty$-groupoid in which composites and inverses of [[k-morphism]]s are only guaranteed to exist, but are not specifically _chosen_ .

An algebraic fibrant object in $sSet_{Quillen}$ is a [[Kan complex]] with a chosen filler for each [[horn]]: an **[[algebraic Kan complex]]** (see [[simplicial T-complex]] for a related but much stricter notion). This means precisely that all possible composites and all possible inverses are chosen. So the Quillen equivalence

$$
  sSet_{Quillen} \stackrel{\leftarrow}{\to} Alg sSet_{Quillen} 
$$

induces an equivalence from an [[algebraic definition of higher category|algebraic definition of ∞-groupoids]] to a [[geometric definition of higher categories|geometric definition]].

### Algebraic $(\infty,1)$-categories

Similarly, the [[model structure for quasi-categories]] $sSet_{Joyal}$ models [[(∞,1)-categories]]: its fibrant objects are precisely the [[quasi-categories]]: an **[[algebraic quasi-category]]**. Again, these form a model for $(\infty,1)$-categories in which composition is only a relation, not an operation.

But equipping a quasi-category with the structure of an algebraic fibrant object precisely means choosing such composites. Accordingly, the [[Quillen equivalence]]

$$
  sSet_{Joyal} \stackrel{\leftarrow}{\to} Alg sSet_{Joyal} 
$$

establishes an equivalence of an algebraic with the standard geometric model for $(\infty,1)$-categories.


## References

The model structure on algebraic fibrant objects was introduced and discussed in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

A survey is in

* [[Thomas Nikolaus]] Talk on _Algebraic models for higher categories_ ([here](http://www.math.uni-hamburg.de/home/nikolaus/AlgMod.pdf))

The refined [[small object argument]] that is being used in the construction of the left adjoint $F : C \to Alg C$ is along the lines of the discussion in

* [[Richard Garner]], _Understanding the small object argument_ Applied Categorical Structures, 17(3):247&#8211;285, 2009 ([pdf](http://www.dpmms.cam.ac.uk/~rhgg2/CT07/CT07.pdf))
{#Garner}