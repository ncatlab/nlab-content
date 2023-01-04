
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The notation "$\underset{\longleftarrow}{\lim}^1$" is common notation for the first [[derived functor]] $R^1 \underset{\longleftarrow}{\lim}$ of the [[limit]] functor. 

Here we consider the case of limits over [[sequential diagrams]] of [[abelian groups]] (prop. \ref{Lim1IsDerivedLimit} below).
In good cases, this is the only obstruction to a naive [[limit]] of homotopy sets being the homotopy classes of the correct [[homotopy limit]]. Such a situation is expressed by a [[short exact sequence|short exact]] _Milnor sequence_ ([below](#MilnorSequences)).


## Definition
 {#Definition}


+-- {: .num_defn #TheBoundaryMapDefiningLim1}
###### Definition

Given a [[tower]] $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \stackrel{f_2}{\to} A_2 \stackrel{f_1}{\to} A_1 \stackrel{f_0}{\to} A_0
$$

write

$$
  \partial
    \;\colon\;
  \underset{n}{\prod} A_n
    \longrightarrow
  \underset{n}{\prod} A_n
$$

for the homomorphism given by 

$$
  \partial \;\colon\; 
    (a_n)_{n \in \mathbb{N}} 
  \mapsto  
    (a_n - f_n(a_{n+1}))_{n \in \mathbb{N}}.
$$
=--

+-- {: .num_remark #LimitAsKernelAnalogousToLim1}
###### Remark

The [[limit]] of a sequence as in def. \ref{TheBoundaryMapDefiningLim1} -- hence the group $\underset{\longleftarrow}{\lim}_n A_n$ universally equipped with morphisms $\underset{\longleftarrow}{\lim}_n A_n \overset{p_n}{\to} A_n$ such that all

$$
  \array{
     && \underset{\longleftarrow}{\lim}_n A_n
     \\
     & {}^{\mathllap{p_{n+1}}}\swarrow && \searrow^{\mathrlap{p_n}}
     \\
     A_{n+1} && \overset{f_n}{\longrightarrow} && A_n
  }
$$

[[commuting diagram|commute]] -- is equivalently the [[kernel]] of the morphism $\partial$ in def. \ref{TheBoundaryMapDefiningLim1}.

=--

+-- {: .num_defn #Lim1ViaCokernel}
###### Definition

Given a [[tower]] $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \stackrel{f_2}{\to} A_2 \stackrel{f_1}{\to} A_1 \stackrel{f_0}{\to} A_0
$$

then $\underset{\longleftarrow}{\lim}^1 A_\bullet$ is the [[cokernel]] of the map $\partial$ in def. \ref{TheBoundaryMapDefiningLim1}, hence the group that makes a [[long exact sequence]] of the form

$$
  0 \to 
  \underset{\longleftarrow}{\lim}_n A_n
  \longrightarrow
  \underset{n}{\prod} A_n
   \stackrel{\partial}{\longrightarrow}
  \underset{n}{\prod} A_n
    \longrightarrow
  \underset{\longleftarrow}{\lim}^1_n A_n
  \to 0
  \,,
$$


=--

There is a generalization to groups (not necessarily abelian). ([Bousfield-Kan 72, IX.2.1](#BousfieldKan72))

## Properties

### Abstract characterizations

+-- {: .num_prop #PropertiesOfLim1}
###### Proposition

The [[functor]] $\underset{\longleftarrow}{\lim}^1 \colon Ab^{(\mathbb{N}, \geq)} \longrightarrow Ab$ (def. \ref{Lim1ViaCokernel}) satisfies

1. for every [[short exact sequence]] $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0 \;\;\; \in Ab^{(\mathbb{N}, \geq)}$ then the induced sequence

   $$
    0 
    \to
    \underset{\longleftarrow}{\lim}_n A_n
    \to
    \underset{\longleftarrow}{\lim}_n B_n
    \to
    \underset{\longleftarrow}{\lim}_n C_n
    \to
    \underset{\longleftarrow}{\lim}_n^1  A_n
    \to
    \underset{\longleftarrow}{\lim}_n^1 B_n
    \to
    \underset{\longleftarrow}{\lim}_n^1 C_n
    \to 0
   $$

   is a [[long exact sequence]] of abelian groups;

1. if $A_\bullet$ is a tower such that all maps are [[surjections]], then $\underset{\longleftarrow}{\lim}^1_n A_n \simeq 0$.

=--

(e.g. [Bousfield-Kan 72, ch IX, prop. 2.3 and 2.4](#BousfieldKan72), [Switzer 75, prop. 7.63](#Switzer75), [Goerss-Jardine 96, section VI. lemma 2.11](#GoerssJardine96))


+-- {: .proof}
###### Proof

For the first property: Given $A_\bullet$ a tower of abelian groups, write

$$
  L^\bullet(A_\bullet)
  \coloneqq
  \left[
    0
   \to 
  \underset{deg \, 0}{\underbrace{\underset{n}{\prod} A_n}}
    \overset{\partial}{\longrightarrow}
  \underset{deg\, 1}{\underbrace{\underset{n}{\prod} A_n}}
   \to 
   0
  \right]
$$

for the homomorphism from def. \ref{TheBoundaryMapDefiningLim1} regarded as the single non-trivial differential in a [[cochain complex]] of abelian groups.
Then by remark \ref{LimitAsKernelAnalogousToLim1} and def. \ref{Lim1ViaCokernel} we have $H^0(L(A_\bullet)) \simeq \underset{\longleftarrow}{\lim} A_\bullet$ and $H^1(L(A_\bullet)) \simeq \underset{\longleftarrow}{\lim}^1 A_\bullet$.

With this, then for a short exact sequence of towers $0 \to A_\bullet \to B_\bullet \to C_\bullet \to 0$ the long exact sequence in question is the [[long exact sequence in homology]] of the corresponding short exact sequence of complexes

$$
  0 
    \to 
  L^\bullet(A_\bullet) 
    \longrightarrow 
  L^\bullet(B_\bullet)
    \longrightarrow
  L^\bullet(C_\bullet)
    \to
  0
  \,.
$$

For the second statement: If all the $f_k$ are surjective, then inspection shows that the homomorphism $\partial$ in def. \ref{TheBoundaryMapDefiningLim1} is surjective. Hence its [[cokernel]] vanishes.

=--

+-- {: .num_lemma #TowersOfAbelianGroupsHasEnoughInjectives}
###### Lemma

The category $Ab^{(\mathbb{N}, \geq)}$ of [[towers]] of [[abelian groups]] has [[enough injectives]].


=--

+-- {: .proof}
###### Proof

The functor $(-)_n \colon Ab^{(\mathbb{N}, \geq)} \to Ab$ that picks the $n$-th component of the tower has a [[right adjoint]] $r_n$, which sends an abelian group $A$ to the tower

$$
  r_n
  \coloneqq
  \left[
    \cdots \overset{id}{\to}
    A \overset{id}{\to}
    \underset{= (r_n)_{n+1}}{\underbrace{A}} \overset{id}{\to}
    \underset{= (r_n)_n}{\underbrace{A}} 
       \overset{}{\to}
    \underset{= (r_n)_{n-1}}{\underbrace{0}}
    \to 
    0
    \to
    \cdots
    \to
    0
    \to 
    0
  \right]
  \,.
$$

Since $(-)_n$ itself is evidently an [[exact functor]], its right adjoint preserves injective objects ([prop.](injective+object#RightAdjointsOfExactFunctorsPreserveInjectives)). 

So with $A_\bullet \in Ab^{(\mathbb{N}, \geq)}$, let $A_n \hookrightarrow \tilde A_n$ be an injective resolution of the abelian group $A_n$, for each $n \in \mathbb{N}$. Then 

$$
  A_\bullet 
    \overset{(\eta_n)_{n \in \mathbb{N}}}{\longrightarrow}
  \underset{n \in \mathbb{R}}{\prod}
  r_n A_n
  \hookrightarrow
  \underset{n \in \mathbb{N}}{\prod} r_n \tilde A_n
$$

is an injective resolution for $A_\bullet$.

=--

+-- {: .num_prop #Lim1IsDerivedLimit}
###### Proposition

The [[functor]] $\underset{\longleftarrow}{\lim}^1 \colon Ab^{(\mathbb{N}, \geq)} \longrightarrow Ab$ (def. \ref{Lim1ViaCokernel}) is the [[derived functor in homological algebra|first right derived functor]] of the [[limit]] functor $\underset{\longleftarrow}{\lim} \colon Ab^{(\mathbb{N},\geq)} \longrightarrow Ab$.

=--

([Bousfield-Kan 72, chapter IX.2, remark 2.6](#BousfieldKan72))

+-- {: .proof}
###### Proof

By lemma \ref{TowersOfAbelianGroupsHasEnoughInjectives} there are [[enough injectives]] in $Ab^{(\mathbb{N}, \geq)}$. 
So for $A_\bullet \in Ab^{(\mathbb{N}, \geq)}$ the given tower of abelian groups, let 

$$
  0 
    \to 
  A_\bullet 
    \overset{j^0}{\longrightarrow} 
  J^0_\bullet 
    \overset{j^1}{\longrightarrow}
  J^1_\bullet
    \overset{j^2}{\longrightarrow}
  J^2_\bullet
    \overset{}{\longrightarrow}
  \cdots
$$

be an [[injective resolution]]. We need to show that 

$$
  \underset{\longleftarrow}{\lim}^1 A_\bullet
    \simeq
  ker(\underset{\longleftarrow}{\lim}(j^2))/im(\underset{\longleftarrow}{\lim}(j^1))
  \,.
$$

Since limits preserve [[kernels]], this is equivalently

$$
  \underset{\longleftarrow}{\lim}^1 A_\bullet
    \simeq
  (\underset{\longleftarrow}{\lim}(ker(j^2)_\bullet))/im(\underset{\longleftarrow}{\lim}(j^1))
$$

Now observe that each injective $J^q_\bullet$ is a tower of epimorphism. This follows by the defining [[right lifting property]] applied against the monomorphisms of towers of the following form

$$
  \array{
      \cdots &\to & 0 &\to& 0 &\longrightarrow& 0 &\longrightarrow& \mathbb{Z} &\overset{id}{\longrightarrow}& \cdots &\overset{id}{\longrightarrow}& \mathbb{Z} &\overset{id}{\longrightarrow}& \mathbb{Z}
     \\
     \cdots
     &&
     \downarrow^{\mathrlap{id}}
     &&
     \downarrow^{\mathrlap{id}}
     &&
     \downarrow^{\mathrlap{incl}}
     &&
     \downarrow^{\mathrlap{id}}
     &&
     &&
     \downarrow^{\mathrlap{id}}
     &&
     \downarrow^{\mathrlap{id}}
     \\
     \cdots &\to& 0 &\to& 0 &\to & \mathbb{Z} &\underset{id}{\longrightarrow}& \mathbb{Z} &\underset{id}{\longrightarrow}& \cdots &\underset{id}{\longrightarrow}& \mathbb{Z} &\underset{id}{\longrightarrow}& \mathbb{Z}
  }
$$

Therefore by the second item of prop. \ref{PropertiesOfLim1} the long exact sequence from the first item of prop. \ref{PropertiesOfLim1} applied to the [[short exact sequence]]

$$ 
  0
   \to 
  A_\bullet
   \overset{j^0}{\longrightarrow}
  J^0_\bullet
   \overset{j^1}{\longrightarrow}
  ker(j^2)_\bullet
   \to
  0
$$

becomes

$$
   0
     \to
   \underset{\longleftarrow}{\lim} A_\bullet
    \overset{\underset{\longleftarrow}{\lim} j^0}{\longrightarrow}
  \underset{\longleftarrow}{\lim} J^0_\bullet
    \overset{\underset{\longleftarrow}{\lim}j^1}{\longrightarrow}
  \underset{\longleftarrow}{\lim}(ker(j^2)_\bullet)
    \longrightarrow
  \underset{\longleftarrow}{\lim}^1 A_\bullet
    \longrightarrow 
  0 
  \,.
$$

Exactness of this sequence gives the desired identification 
$  \underset{\longleftarrow}{\lim}^1 A_\bullet
    \simeq
  (\underset{\longleftarrow}{\lim}(ker(j^2)_\bullet))/im(\underset{\longleftarrow}{\lim}(j^1))
 \,.
$

=--

+-- {: .num_prop #AbstractCharacterizationOfLim1}
###### Proposition

The [[functor]] $\underset{\longleftarrow}{\lim}^1 \colon Ab^{(\mathbb{N}, \geq)} \longrightarrow Ab$ (def. \ref{Lim1ViaCokernel}) is in fact the unique functor, up to [[natural isomorphism]], satisfying the conditions in prop. \ref{AbstractCharacterizationOfLim1}.

=--

+-- {: .proof}
###### Proof

The proof of prop. \ref{Lim1IsDerivedLimit} only used the conditions from prop. \ref{PropertiesOfLim1}, hence any functor satisfying these conditions is the first right derived functor of $\underset{\longleftarrow}{\lim}$, up to natural isomorphism.

=--


### Vanishing of $\lim^1$


+-- {: .num_defn #MittagLefflerCondition}
###### Definition

A tower $A_\bullet$ of [[abelian groups]]

$$
  \cdots \to A_3 \to A_2 \to A_1 \to A_0
$$

is said to satisfy the **[[Mittag-Leffler condition]]** if for all $k$ there exists $i \geq k$ such that for all $j \geq i \geq k$ the [[image]] of the [[homomorphism]] $A_i \to A_k$ equals that of $A_j \to A_k$
 
$$
  im(A_i \to A_k) \simeq im(A_j \to A_k)
  \,.
$$

=--

(e.g. [Switzer 75, def. 7.74](#Switzer75))

+-- {: .num_example #MittagLefflerSatisfiedInParticularForTowerOfSurjections}
###### Example

The Mittag-Leffler condition, def. \ref{MittagLefflerCondition}, is satisfied in particular when all morphisms $A_{i+1}\to A_i$ are [[epimorphisms]] (hence [[surjections]] of the underlying [[sets]]).

=--

+-- {: .num_prop #Lim1VanihesUnderMittagLeffler}
###### Proposition

If a tower $A_\bullet$ satisfies the [[Mittag-Leffler condition]], def. \ref{MittagLefflerCondition}, then its $\underset{\leftarrow}{\lim}^1$ vanishes:

$$
  \underset{\longleftarrow}{\lim}^1 A_\bullet = 0
  \,.
$$

=--

e.g. ([Switzer 75, theorem 7.75](#Switzer75), [Kochmann 96, prop. 4.2.3](#Kochmann96), [Weibel 94, prop. 3.5.7](#Weibel94))

+-- {: .proof}
###### Proof idea

One needs to show that with the Mittag-Leffler condition, then the [[cokernel]] of $\partial$ in def. \ref{TheBoundaryMapDefiningLim1} vanishes, hence that $\partial$ is an [[epimorphism]] in this case, hence that every $(a_n)_{n \in \mathbb{N}} \in \underset{n}{\prod} A_n$ has a preimage under $\partial$. So use the Mittag-Leffler condition to find pre-images of $a_n$ by [[induction]] over $n$.

=--

### Relation to $Ext$-groups


+-- {: .num_lemma #lim1AndExt1}
###### Lemma

Given a [[cotower]] 

$$
  A_\bullet = (A_0 \overset{f_0}{\to} A _1 \overset{f_1}{\to} A_2 \to \cdots)
$$ 

of [[abelian groups]], then for every abelian group $B \in Ab$ there is a [[short exact sequence]] of the form

$$
  0 
    \to 
  \underset{\longleftarrow}{\lim}^1_n Hom(A_n, B)
    \longrightarrow
  Ext^1( \underset{\longrightarrow}{\lim}_n A_n, B )
    \longrightarrow
  \underset{\longleftarrow}{\lim}_n Ext^1( A_n, B)
    \to
  0
  \,,
$$

where $Hom(-,-)$ denotes the [[hom-object|hom-group]],  $Ext^1(-,-)$ denotes the first [[Ext]]-group (and so $Hom(-,-) = Ext^0(-,-)$).

=--

+-- {: .proof}
###### Proof

Consider the homomorphism

$$
  \tilde \partial
  \;\colon\;
  \underset{n}{\oplus} A_n
    \longrightarrow
  \underset{n}{\oplus} A_n
$$

which sends $a_n \in A_n$ to $a_n - f_n(a_n)$. Its [[cokernel]] is the [[colimit]] over the cotower, but its [[kernel]] is  trivial (in contrast to the otherwise [[formal dual|formally dual]] situation in remark \ref{LimitAsKernelAnalogousToLim1}). Hence (as opposed to the long exact sequence in def. \ref{Lim1ViaCokernel}) there is a [[short exact sequence]] of the form

$$
  0 
    \to
  \underset{n}{\oplus} A_n
    \overset{\tilde \partial}{\longrightarrow}
  \underset{n}{\oplus} A_n
    \overset{}{\longrightarrow}
  \underset{\longrightarrow}{lim}_n A_n
   \to
  0
  \,.
$$

Every short exact sequence gives rise to a [[long exact sequence]] of [[derived functors]] ([prop.](derived+functor+in+homological+algebra#LongExactSequenceOfRightDerivedFunctorsFromShortExactSequence)) which in the present case starts out as

$$
  0
    \to
  Hom(\underset{\longrightarrow}{\lim}_n A_n,B)
    \longrightarrow
  \underset{n}{\prod} Hom( A_n, B )
    \overset{\partial}{\longrightarrow}
  \underset{n}{\prod} Hom( A_n, B )
    \longrightarrow
  Ext^1(\underset{\longrightarrow}{\lim}_n A_n,B)
    \longrightarrow
  \underset{n}{\prod} Ext^1(  A_n, B )
    \overset{\partial}{\longrightarrow}
  \underset{n}{\prod} Ext^1(  A_n, B )
    \longrightarrow
  \cdots
$$

where we used that [[direct sum]] is the [[coproduct]] in abelian groups, so that homs out of it yield a [[product]], and where the morphism $\partial$ is the one from def. \ref{TheBoundaryMapDefiningLim1} corresponding to the [[tower]]

$$
  Hom(A_\bullet,B)
  = 
  (  \cdots \to Hom(A_2,B) \to Hom(A_1,B) \to  Hom(A_0,B) )
  \,.
$$

Hence truncating this long sequence by forming kernel and cokernel of $\partial$, respectively, it becomes the short exact sequence in question.

=--

## Milnor exact sequences
 {#MilnorSequences}


### For homotopy groups

+-- {: .num_prop #MilnorExactSequence}
###### Proposition
**(Milnor exact sequence for homotopy groups)**

Let 

$$
  \cdots \to X_3 \overset{p_2}{\longrightarrow} X_2 \overset{p_1}{\longrightarrow} X_1 \overset{p_0}{\longrightarrow} X_0
$$

be a [[tower of fibrations]], for instance a tower of [[simplicial sets]] with each map a [[Kan fibration]] (and $X_0$, hence each $X_n$ a [[Kan complex]]), or a tower of [[topological spaces]] with each map a [[Serre fibration]]. Then for each $q \in \mathbb{N}$ there is a [[short exact sequence]]

$$
  0 
  \to
  \underset{\longleftarrow}{\lim}^1_i \pi_{q+1}(X_i)
  \longrightarrow
  \pi_q(\underset{\longleftarrow}{\lim}_i X_i)
  \longrightarrow
  \underset{\longleftarrow}{\lim}_i \pi_q(X_i)
  \to 
  0
  \,,
$$

for $\pi_\bullet$ the [[homotopy group]]-functor (exact as [[pointed sets]] for $i = 0$, as [[groups]] for $i \geq 1$) which says that 

1. the failure of the [[limit]] over the homotopy groups of the stages of the tower to equal the homotopy groups of the [[limit]] of the tower is at most in the [[kernel]] of the canonical comparison map;

1. that kernel is the $\underset{\longleftarrow}{\lim}^1$ (def. \ref{Lim1ViaCokernel}) of the homotopy groups of the stages. 


=--

e.g. ([Bousfield-Kan 72, chapter IX, theorem 3.1](#BousfieldKan72), [Goerss-Jardine 96, section VI. prop. 2.15](#GoerssJardine96))

+-- {: .proof}
###### Proof

With respect to the [[classical model structure on simplicial sets]] or the [[classical model structure on topological spaces]], a tower of fibrations as stated is a fibrant object in the injective [[model structure on functors]] $[(\mathbb{N},\geq), sSet]_{inj}$ ($[(\mathbb{N},\geq), Top]_{inj}$) ([prop](projectively+cofibrant+diagram#CofibrantCotowerDiagram)). Hence the plain [[limit]] over this diagram represents the [[homotopy limit]]. By the discussion there, up to weak equivalence that homotopy limit is also the pullback in 

$$
  \array{
    holim X_\bullet &\longrightarrow& \underset{n}{\prod} Path(X_n)
    \\
    \downarrow &(pb)& \downarrow
    \\
    \underset{n}{\prod} X_n &\underset{(id,p_n)_n}{\longrightarrow}&
    \underset{n}{\prod} X_ n \times X_n
  }
  \,,
$$

where on the right we have the product over all the canonical fibrations out of the [[path space objects]]. Hence also the left vertical morphism is a fibration, and so by taking its [[fiber]] over a basepoint, the [[pasting law]] gives a [[homotopy fiber sequence]]

$$
  \underset{n}{\prod} \Omega X_n
    \longrightarrow
  holim X_\bullet
    \longrightarrow
  \underset{n}{\prod} X_n
  \,.
$$

The [[long exact sequence of homotopy groups]] of this fiber sequence goes

$$
  \cdots
   \to
  \underset{n}{\prod} \pi_{q+1}(X_n)  
   \longrightarrow
  \underset{n}{\prod} \pi_{q+1}(X_n)
    \longrightarrow
  \pi_q (\underset{\longleftarrow}{\lim} X_\bullet)
    \longrightarrow
  \underset{n}{\prod} \pi_q(X_n)
    \longrightarrow
  \underset{n}{\prod} \pi_q(X_n)
   \to
  \cdots
  \,.
$$

Chopping that off by forming kernel and cokernel yields the claim for positive $q$. For $q = 0$ it follows by inspection.

=--

### For chain homology

+-- {: .num_example}
###### Example

Let 

$$
  \cdots \to C_3 \to C_2 \to C_1 \to C_0
$$

be a tower of [[chain complexes]] (of [[abelian groups]]) such that it satisfies degree-wise the [[Mittag-Leffler condition]], def. \ref{MittagLefflerCondition}, and write

$$
  C \coloneqq \underset{\longleftarrow}{\lim}_n C_n
$$

for its [[limit]]. Then for each $q \in \mathbb{Z}$ the [[chain homology]] $H_q(-)$ of the limit sits in a [[short exact sequence]] with the ordinary $\underset{\longleftarrow}{\lim}$ and the $\underset{\longleftarrow}{\lim}^1$ of the chain homologies:

$$
  0 \to \underset{\longleftarrow}{\lim}^1_i H_{q+1}(C_i)
  \longrightarrow H_q(C)
  \longrightarrow \underset{\longleftarrow}{\lim}_i H_q(C_i)
  \to 0
  \,.
$$

=--

(e.g. [Weibel 94, prop. 3.5.8](#Weibel94))


### For generalized cohomology groups
 {#MilnorSequenceForGeneralizedCohomology}


#### Of spaces

+-- {: .num_prop #MilorSequenceForReducedCohomologyOnCWComplex}
###### Proposition
**(Milnor exact sequence for generalized cohomology)**

Let $X$ be a [[pointed topological space|pointed]] [[CW-complex]], $X = \underset{\longrightarrow}{\lim}_n X_n$ and let $\tilde E^\bullet$ be an additive [[reduced cohomology theory]]. 

Then the canonical morphisms make a [[short exact sequence]]

   $$
     0 
      \to 
     \underset{\longleftarrow}{\lim}^1_n \tilde E^{\bullet-1}(X_n)
      \longrightarrow
     \tilde E^{\bullet}(X)
      \longrightarrow
     \underset{\longleftarrow}{\lim}_n \tilde E^{\bullet}(X_n)
     \to 
     0
     \,,
   $$

saying that 

1. the failure of the canonical comparison map $\tilde E^\bullet(X) \to \underset{\longleftarrow}{\lim} \tilde E^\bullet(X_n)$ to the [[limit]] of the [[cohomology groups]] on the finite stages to be an [[isomorphism]] is at most in a non-vanishing [[kernel]];

1. this kernel is precisely the $\lim^1$ (def. \ref{Lim1ViaCokernel}) of the cohomology groups at the finite stages in one degree lower.

=--

e.g. ([Switzer 75, prop. 7.66](#Switzer75), [Kochmann 96, prop. 4.2.2](#Kochmann96))


+-- {: .proof}
###### Proof

For 

$$
  X_\bullet
  = 
  \left(
    X_0 
      \overset{i_0}{\hookrightarrow}
    X_1 
      \overset{i_1}{\hookrightarrow}
    X_2 
      \overset{i_1}{\hookrightarrow}
    \cdots
  \right)
$$ 

the sequence of stages of the ([[pointed topological space|pointed]]) [[CW-complex]] $X = \underset{\longleftarrow}{\lim}_n X_n$, write

$$
  \begin{aligned}
    A_X 
    &\coloneqq 
    \underset{n \in \mathbb{N}}{\sqcup} X_{2n} \times [2n,{2n}+1];
  \\
    B_X 
    &\coloneqq 
    \underset{n \in \mathbb{N}}{\sqcup} X_{(2n+1)} \times [2n+1,{2n}+2].
  \end{aligned}
$$

for the [[disjoint unions]] of the [[cylinders]] over all the stages in even and all those in odd degree, respectively.

These come with canonical inclusion maps into the [[mapping telescope]] $Tel(X_\bullet)$ ([def.](mapping+telescope#MappingTelescope)), which we denote by

$$
  \array{
    A_X && && B_X
    \\
    & {}_{\mathllap{\iota_{A_x}}}\searrow && \swarrow_{\mathrlap{\iota_{B_x}}}
    \\
    && Tel(X_\bullet)
  }
  \,.
$$

Observe that 

1. $A_X \cup B_X \simeq Tel(X_\bullet)$;

1. $A_X \cap B_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_n$;

and that there are [[homotopy equivalences]]

1. $A_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_{2n+1}$

1. $B_X \simeq \underset{n \in \mathbb{N}}{\sqcup} X_{2n}$

1. $Tel(X_\bullet) \simeq X$.

The first two are obvious, the third is [this proposition](mapping+telescope#TelescopeOfCWComplexEquivalentToTheOriginal). 

This implies that the [[Mayer-Vietoris sequence]] ([prop.](generalized+cohomology#MayerVietorisSequenceInGeneralizedCohomology)) for $\tilde E^\bullet$ on the cover $A \sqcup B \to X$ is isomorphic to the bottom horizontal sequence in the following diagram:

$$
  \array{
     \tilde E^{\bullet-1}(A_X)\oplus \tilde E^{\bullet-1}(B_X)
      &\longrightarrow&
    \tilde E^{\bullet-1}(A_X \cap B_X)
      &\longrightarrow& 
    \tilde E^\bullet(X)
      &\overset{(\iota_{A_x})^\ast - (\iota_{B_x})^\ast}{\longrightarrow}&
    \tilde E^\bullet(A_X)\oplus \tilde E^\bullet(B_X)
      &\overset{}{\longrightarrow}&
    \tilde E^\bullet(A_X \cap B_X)
    \\
    \downarrow^{\mathrlap{\simeq}}
     &&
    \downarrow^{\mathrlap{\simeq}} 
      && 
    \downarrow^{\mathrlap{=}}
      &&
    {}^{\mathllap{(id, -id)}}\downarrow^{\mathrlap{\simeq}}
      &&
    \downarrow^{\mathrlap{\simeq}}
    \\
    \underset{n}{\prod}\tilde E^{\bullet-1}(X_n)
      &\underset{\partial}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^{\bullet-1}(X_n) 
      &\longrightarrow& 
    \tilde E^\bullet(X)
      &\overset{(i_n^\ast)_{n}}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^\bullet(X_n)
      &\underset{\partial}{\longrightarrow}&
    \underset{n}{\prod}\tilde E^\bullet(X_n)
  }
  \,,
$$

hence that the bottom sequence is also a [[long exact sequence]].

To identify the morphism $\partial$, notice that it comes from pulling back $E$-cohomology classes along the inclusions $A \cap B \to A$ and $A\cap B \to B$. Comonentwise these are the inclusions of each $X_n$ into the left and the right end of its cylinder inside the [[mapping telescope]], respectively. By the construction of the [[mapping telescope]], one of these ends is embedded via $i_n \colon X_n \hookrightarrow X_{n+1}$ into the cylinder over $X_{n+1}$. In conclusion, $\partial$ acts by

$$
  \partial
    \;\colon\;
  (a_n)_{n \in \mathbb{N}}
    \mapsto
  ( a_n - i_n^\ast(a_{n+1}) )
  \,.
$$

(The relative sign is the one in $(\iota_{A_x})^\ast - (\iota_{B_x})^\ast$ originating in the definition of the [[Mayer-Vietoris sequence]] and properly propagated to the bottom sequence while ensuring that $\tilde E^\bullet(X)\to \prod_n \tilde E^\bullet(X_n)$ is really $(i_n^\ast)_n$ and not $(-1)^n(i_n^\ast)_n$, as needed for the statement to be proven.)

This is the morphism from def. \ref{TheBoundaryMapDefiningLim1} for the sequence

$$
   \cdots
    \to 
  \tilde E^\bullet(X_{n+1}) 
    \overset{i_n^\ast}{\longrightarrow}
  \tilde E^\bullet(X_n)
    \overset{i_n^\ast}{\longrightarrow}
  \tilde E^{\bullet}(X_{n-1})
   \to
   \cdots
 \,.
$$

Hence truncating the above long exact sequence by forming kernel and cokernel of $\partial$, the result follows via remark \ref{LimitAsKernelAnalogousToLim1} and definition \ref{Lim1ViaCokernel}.

=--

In contrast:

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[pointed topological space|pointed]] [[CW-complex]], $X = \underset{\longrightarrow}{\lim}_n X_n$.

For $\tilde E_\bullet$ an additive reduced [[generalized homology theory]], then

   $$
     \underset{\longrightarrow}{\lim}_n \tilde E_\bullet(X_n)
     \overset{\simeq}{\longrightarrow}
     \tilde E_\bullet(X)
   $$

   is an [[isomorphism]].

=--

([Switzer 75, prop. 7.53](#Switzer75))

#### Of spectra
 {#ForGeneralizedCohomologyOfSpectra}


For $X, E \in Ho(Spectra)$ two [[spectra]], then the $E$-generalized cohomology of $X$ is the graded group of homs in the [[stable homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1-1#GradedAbelianGroupStructureOnHomsInTheHomotopyCategory), [exmpl.](Introduction+to+Stable+homotopy+theory+--+1-1#ForASpectrumXGeneralizedECohomology))

$$
  \begin{aligned}
    E^\bullet(X)
      & \coloneqq
    [X,E]_{-\bullet}
    \\
      & \coloneqq
    [\Sigma^\bullet X, E]
  \end{aligned}
  \,.
$$

The [[stable homotopy category]] is, in particular, the [[homotopy category of a model category|homotopy category]] of the stable [[model structure on orthogonal spectra]], in that its [[localization]] at the [[stable weak homotopy equivalences]] is of the form

$$
  \gamma
    \;\colon\;
  OrthSpec(Top_{cg})_{stable}
    \longrightarrow
  Ho(Spectra)
  \,.
$$

In the following when considering an [[orthogonal spectrum]] $X \in OrthSpec(Top_{cg})$, we use, for brevity, the same symbol for its image under $\gamma$.

+-- {: .num_prop #CohomologyOfSpectraMilnorSequence}
###### Proposition

For $X, E \in OrthSpec(Top_{cg})$ two [[orthogonal spectra]] (or two [[symmetric spectra]] such that $X$ is a [[semistable symmetric spectrum]]) then there is a [[short exact sequence]] of the form

$$
  0
    \to
  \underset{\longleftarrow}{\lim}^1_n E^{\bullet + n -1}(X_{n})
    \longrightarrow
  E^\bullet(X)
    \longrightarrow
  \underset{\longleftarrow}{\lim}_n E^{\bullet + n}(X_n)
    \to
  0
$$

where $\underset{\longleftarrow}{\lim}^1$ denotes the [[lim^1]], and where this and the limit on the right are taken over the following structure morphisms

$$
  E^{\bullet + n + 1}(X_{n+1})
    \overset{E^{\bullet+1n+1}(\Sigma^X_n)}{\longrightarrow}
  E^{\bullet+n+1}(X_n \wedge S^1)
    \overset{\simeq}{\longrightarrow}
  E^{\bullet + n}(X_n)
  \,.
$$

=--

([Schwede 12, chapter II prop. 6.5 (ii)](#Schwede12)) (using that symmetric spectra underlying orthogonal spectra are semistable ([Schwede 12, p. 40](#Schwede12)))


+-- {: .num_cor #WithSomeLefflerTheHomsOfSpectraAreHomotopicIfComponentsAre}
###### Corollary

For $X,E \in Ho(Spectra)$ two [[spectra]] such that the tower $n \mapsto E^{n -1}(X_{n})$ satisfies the [[Mittag-Leffler condition]] (def. \ref{MittagLefflerCondition}), then two morphisms of spectra $X \longrightarrow E$ are homotopic already if all their morphisms of component spaces $X_n \to E_n$ are.

=--

+-- {: .proof}
###### Proof

By prop. \ref{Lim1VanihesUnderMittagLeffler} the assumption implies that the $lim^1$-term in prop. \ref{CohomologyOfSpectraMilnorSequence} vanishes, hence by exactness it follows that in this case there is an [[isomorphism]]

$$
  [X,E] 
    \simeq
   E^0(X)
     \overset{\simeq}{\longrightarrow}
   \underset{\longleftarrow}{\lim}_n [X_n, E_n]
  \,.
$$

=--

## Related concepts

* [[homotopy limit]]

* [[spectral sequence of a tower of fibrations]]

* [[conditional convergence of spectral sequences]])

## References

* {#Milnor62} [[John Milnor]], _On axiomatic homology theory_, Pacific J. Math. Volume 12, Number 1 (1962), 337-341 ([Euclid](http://projecteuclid.org/euclid.pjm/1103036730))

* Z. Z. Yeh, _Higher Inverse Limits and Homology Theories_, Thesis, Princeton, 1959.

* {#BousfieldKan72} [[Aldridge Bousfield]], [[Daniel Kan]], section IX.2 of _Homotopy limits, completions and localization_, Springer 1972

* {#Switzer75} [[Robert Switzer]], section 7 from def. 7.57 on in _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975. 


* {#Weibel94} [[Charles Weibel]], section 3.5 of _[[An Introduction to Homological Algebra]]_, Cambridge University Press (1994)

* {#Kochmann96} [[Stanley Kochmann]], section 4.2 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#GoerssJardine99} [[Paul Goerss]], [[Rick Jardine]], section VI.2 of _[[Simplicial homotopy theory]]_, Modern Birkh&#228;user Classics (1999)

  (that's section VII.6 of the 1996 _Progress of Mathematics_ edition )

For generalized cohomology of spectra

* {#Schwede12} [[Stefan Schwede]], around prop.6.5 of _[[Symmetric spectra]]_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec-v3.pdf))



Discussion in the context of [[categories of fibrant objects]] is in 

* [[Kenneth Brown]], section 5 of _[[Abstract Homotopy Theory and Generalized Sheaf Cohomology]]_, Transactions of the American Mathematical Society, Vol. 186 (1973), 419-458

Discussion in the context of [[conditional convergence of spectral sequences]] is in

* {#Boardman99} [[Michael Boardman]], section I.1 of _Conditionally convergent spectral sequences_, 1999 ([pdf](http://www.uio.no/studier/emner/matnat/math/MAT9580/v12/undervisningsmateriale/boardman-conditionally-1999.pdf))

[[!redirects lim1 and Milnor sequences]]
[[!redirects lim1]]
[[!redirects lim^1]]
[[!redirects Milnor sequence]]
[[!redirects Milnor sequences]]
[[!redirects Milnor exact sequence]]
[[!redirects Milnor exact sequences]]
[[!redirects Milnor short exact sequence]]
[[!redirects Milnor short exact sequences]]
[[!redirects Milnor long exact sequence]]
[[!redirects Milnor long exact sequences]]
