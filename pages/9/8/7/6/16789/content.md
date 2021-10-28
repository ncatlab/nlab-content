
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Spheres
+--{: .hide}
[[!include spheres -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The [[sphere]] of [[dimension]] 4.

## Properties

### Coset space structure
 {#CosetSpaceStructure}

As any [[sphere]], the [[4-sphere]] has the [[coset space]] [[structure]]

$$
  S^4 \simeq O(5)/O(4) \simeq SO(5)/SO(4) \simeq Spin(5)/Spin(4)\simeq Pin(5)/Pin(4).
$$

There is also this:

+-- {: .num_example #Sp2Sp1BySp1Sp1Sp1IsS4}
###### Example

The [[coset space]] of [[Sp(2).Sp(1)]] ([this Def.](SpnSp1#SpnSp1)) by [[Sp(1)Sp(1)Sp(1)]] ([this Def.](SpnSp1#Spin4Spin3)) is the [[4-sphere]]:

$$
  \frac{
    Sp(2)\cdot Sp(1)
  }
  {
    Sp(1)Sp(1)Sp(1)
  }
  \;\simeq\;
  S^4
  \,.
$$

This follows essentially from the [[quaternionic Hopf fibration]] and its $Sp(2)$-[[equivariant function|equivariance]]...

=--

(e.g. [Bettiol-Mendes 15, (3.1), (3.2), (3.3)](#BettiolMendes15))



### Homotopy groups

The [[homotopy groups]] of the 4-sphere in low degree are

| $k$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11  | 12 |
|-----|---|---|---|---|---|---|---|---|---|---|----|-----|----|
| $\pi_k(S^4)$ | $\ast$ | 0 | 0 | 0 | $\mathbb{Z}$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | $\mathbb{Z} \times \mathbb{Z}_2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_2^2$ | $\mathbb{Z}_{24} \times \mathbb{Z}_3$ | $\mathbb{Z}_{15}$ | $\mathbb{Z}_2$ | 

### Bundles over the 4-sphere

#### The quaternionic Hopf fibration

The 4-sphere participates in the [[quaternionic Hopf fibration]], the analog of the complex [[Hopf fibration]] with the field of [[complex numbers]] replaced by the division ring of [[quaternions]] or Hamiltonian numbers $\mathbb{H}$.

$$
  \array{
    S^3 &\hookrightarrow& S^7
    \\
    && \downarrow^\mathrlap{p}
    \\
    && S^4 &\stackrel{}{\longrightarrow}& \mathbf{B} SU(2)
  }   
$$

Here the idea is that $S^7$ may be construed as 

$$
  \array{
  S^7  
    &\simeq
  S(\mathbb{H}^4)
  \\
  & \simeq
  \{(x, y) \in \mathbb{H}^2: {|x|}^2 + {|y|}^2 = 1\}, 
 }
$$

with $p$ mapping $(x, y)$
to $x/y$ as an element in the [[projective line]] $\mathbb{P}^1(\mathbb{H}) \cong S^4$, with each [[fiber]] a [[torsor]] parameterized by quaternionic [[scalars]] $\lambda$ of unit [[norm]] (so $\lambda \in S^3$).  This canonical $S^3$-bundle (or $SU(2)$-bundle) is classified by a map $S^4 \to \mathbf{B} SU(2)$. 

{#HopfParameterization} There are other useful ways to parameterize the quaternionic Hopf fibration, such as the original _[[Hopf construction]]_, see there the section _[Hopf fibrations](Hopf+construction#HopfFibrations)_. By this parameterization $S^4$ is identified as $S^4 \simeq S(\mathbb{R} \oplus \mathbb{H})$.

#### The Calabi-Penrose fibration

See at _[[Calabi-Penrose fibration]]_.

#### The complex projective plane
 {#AsAQuotientOfTheComplexProjectivePlane}

+-- {: .num_prop}
###### Proposition
**([[Arnold-Kuiper-Massey theorem]])**

The 4-sphere is the [[quotient space]] of the [[complex projective plane]] by the [[action]] of [[complex conjugation]] (on homogeneous coordinates):

$$
  \mathbb{C}P^2 / (-)^*
  \simeq
  S^4
$$

=--


### Exotic smooth structures

It is open whether the 4-sphere admits an [[exotic smooth structure]]. See ([Freedman-Gompf-Morrison-Walker 09](#FreedmanGompfMorrisonWalker09)) for review.


### $SU(2)$ action
 {#QuaternionAction}

If we identify $\mathbb{R}^5 \simeq_{\mathbb{Q}} \mathbb{R} \oplus \mathbb{H}$ with the [[direct sum]] of the [[real line]] with the [[real vector space]] underlying the [[quaternions]], so that

$$
 S^4 \simeq S(\mathbb{R} \oplus \mathbb{H})
$$

as in the discussion of the quaternionic Hopf fibration [above](#HopfParameterization), then there is induced an [[action]] of the group [[special unitary group|SU(2)]] on the 4-sphere, by identifying 

$$
  SU(2) \simeq S(\mathbb{Q})
$$

and then acting by left multiplication.



#### Circle action
  {#CircleAction}


+-- {: .num_prop}
###### Proposition

Given an continuous [[action]] of the [[circle group]] on the [[topological space|topological]] [[4-sphere]], its [[fixed point]] space is of one of two types:

1. either it is the [[0-sphere]] $S^0 \hookrightarrow S^4$

1. or it has the [[rational homotopy theory|rational homotopy type]] of an even-dimensional sphere.

=--

([Félix-Oprea-Tanré 08, Example 7.39](#FelixOpreaTanre08))

For more see at _[[group actions on spheres]]_.


As a special case of the $SU(2)$-action from [above](#QuaternionAction), we discuss the induced circle action via the embedding

$$
  S^1 \simeq U(1) \hookrightarrow SU(2)
  \,.
$$

Consider the following [[circle group|circle]] [[group action on an n-sphere|group action on the 4-sphere]]:

+-- {: .num_defn #CircleActionOn4Sphere}
###### Definition
**($SU(2)$-action on 4-sphere)**

Regard

$$
  S^4 \simeq S(\mathbb{R} \oplus \mathbb{H})
$$

as the [[unit sphere]] inside the [[direct sum]] (as [[real vector spaces]]) of the [[real numbers]] with the [[quaternions]], and regard the [[special unitary group]] $SU(2)$ as the group of unit-norm quaternions

$$
  SU(2) \simeq S(\mathbb{H},\cdot)
$$

In particular this restricts to an [[action]] of the [[circle group]] 

$$
  S^1 \simeq U(1) \hookrightarrow SU(2)
$$

(as the [[diagonal matrices]] inside $SU(2)$) on the 4-sphere.


=--

The resulting ordinary [[quotient]] is $S^4/_{ord} S^1 \simeq S^3$ and the [[projection]] $S^4 \to S^3$ is the [[suspension]] of the [[complex Hopf fibration]] $S^3 \to S^2$.

The [[fixed point]] set of the action is the two poles 

$$
  S^0 \;=\; \{(\pm 1, 0,0,0,0)\} \;\in\; \mathbb{R} \oplus \mathbb{H}
$$

introduced by the suspension, hence forms the [[0-sphere]] space. Since this is not the [[empty set]], the [[homotopy quotient]] $S^4 // S^1$ of the [[circle action]] differs from $S^3$, but there is still the canonical [[projection]]

$$
  S^4//S^1 \longrightarrow S^4 / S^1 \simeq S^3
  \,.
$$ 

Hence both $S^4$ and $S^4 // S^1$ are canonically [[homotopy types]] over $S^3$. 

A [[minimal dg-module]] presentation in [[rational homotopy theory]] for these projections is given in [Roig & Saralegi-Aranguren 00, second page](#RoigSaralegiAranguren00):

+-- {: .num_prop #FourSphereOverThreeSphereMinimalDgModel}
###### Proposition
**([Roig & Saralegi-Aranguren 00, p. 2](#RoigSaralegiAranguren00))**

Write

$$
  CE(\mathfrak{l}(S^3))) = Sym^\bullet \langle \underset{\text{deg 3}}{\underbrace{h_3}} \rangle
$$

for the [[minimal Sullivan model]] of the [[3-sphere]]. Then [[rational homotopy theory|rational]] [[minimal dg-modules]] for the maps (via Def. \ref{CircleActionOn4Sphere})

$$
  \array{
    S^4
    \\
    \downarrow
    \\
    S^3
  }
  \,,\phantom{AA}
  \array{
    S^4//S^1
    \\
    \downarrow
    \\
    S^3
  }
  \,,\phantom{AA}
  \array{
    S^0
    \\
    \downarrow
    \\
    S^3
  }
$$ 

as [[dg-modules]] over $CE(\mathfrak{l}(S^3))$ are given as follows, respectively:

$$
  \label{FourSphereAndRelatedOverThreeSphereMinimalDGModels}
  \array{
  \text{fibration} & \array{\text{vector space underlying} \\ \text{minimal dg-model}} & \array{ \text{differential on} \\ \text{minimal dg-model} }
   \\
  \array{
    S^4
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet \langle 
    \underset{
      deg = 3
    }{
    \underbrace{
      h_3
    }}
  \rangle 
  \otimes
  \left\langle 
     \underset{deg = 2p}{
     \underbrace{
       \tilde\omega_{2p}
     }},
     \underset{deg = 2p + 4}{ 
     \underbrace{
       \omega_{2p + 4}
     }} \,\vert\, p \in \mathbb{N} 
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \tilde\omega_0 & \mapsto 0
      \\
      \tilde\omega_{2p+2} &\mapsto h_3 \wedge \tilde \omega_{2p}
      \\
      \omega_4 & \mapsto 0
      \\
      \omega_{2p+6} & \mapsto h_3 \wedge \omega_{2p + 4}
    \end{aligned}
    \right.
  \\
  \array{
    S^0
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet \langle 
    \underset{
      deg = 3
    }{
    \underbrace{
      h_3
    }}
  \rangle 
  \otimes
  \left\langle 
     \underset{deg = 2p}{
     \underbrace{
       \tilde \omega_{2p}
     }},
     \underset{
       deg = 2p
     }{ 
     \underbrace{
       \omega_{2p}
     }} \,\vert\, p \in \mathbb{N} 
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \tilde \omega_0 & \mapsto 0
      \\
      \tilde \omega_{2p+2} &\mapsto h_3 \wedge \tilde \omega_{2p}
      \\   
      \omega_0 & \mapsto 0
      \\
      \omega_{2p+2} &\mapsto h_3 \wedge \omega_{2p}
    \end{aligned}
    \right.
  \\
  \array{
    S^4//S^1
    \\
    \downarrow
    \\
    S^3
  }
  &
  Sym^\bullet  \langle 
    \underset{
      deg = 3
    }{
    \underbrace{
      h_3 
     }}
    ,
    \underset{
      deg = 2
    }{
    \underbrace{   
      \omega_2  
    }}
  \rangle 
   \otimes
  \left\langle 
    \underset{deg = 2p}{
    \underbrace{
      \tilde \omega_{2p}
    }},
    \underset{
      deg =2p + 4
    }{ 
    \underbrace{
      \omega_{2p + 4}
    }} \,\vert\, p \in \mathbb{N}
  \right\rangle
  &
  d \colon
  \left\{
    \begin{aligned}
      \tilde \omega_0 & \mapsto 0
      \\
      \tilde \omega_{2p+2} &\mapsto h_3 \wedge \tilde \omega_{2p}
      \\
      \omega_2 & \mapsto 0
      \\
      \omega_{2p+4} & \mapsto h_3 \wedge \omega_{2p + 2}
    \end{aligned}
  \right.
  }
$$

=--

Beware that in the model for $S^4//S^2$ the element $\omega_2$ induces its entire polynomial algebra as generator of the dg-module.

Notice that we changed the notation of the generators compared to [Roig & Saralegi-Aranguren 00, second page](#RoigSaralegiAranguren00), to bring out the pattern:

|  $\phantom{A}$Roig$\phantom{A}$  |  $\phantom{A}$here$\phantom{A}$    |
|------------|-----------------|
|   $\phantom{A}a\phantom{A}$    |        $\phantom{A}h_3\phantom{A}$    |
|  $\phantom{A}1\phantom{A}$    |  $\phantom{A}\tilde\omega_0\phantom{A}$     |
|  $\phantom{A}c_{2n}\phantom{A}$  | $\phantom{A}\tilde\omega_{2n+2}\phantom{A}$   |
| $\phantom{A}c_{2n+1}\phantom{A}$ | $\phantom{A}\omega_{2n+4}\phantom{A}$ |
|    $\phantom{A}e\phantom{A}$     |    $\phantom{A}\omega_2\phantom{A}$   |
| $\phantom{A}\gamma_{2n}\phantom{A}$ | $\phantom{A}\tilde\omega_{2n}\phantom{A}$ |
| $\phantom{A}\gamma_{2n+1}\phantom{A}$ | $\phantom{A}\omega_{2n}\phantom{A}$ |


#### M5-brane orbifolds

The [[supersymmetry|supersymmetric]] [[Freund-Rubin compactifications]] of [[11-dimensional supergravity]] which are [[Cartesian products]] of 7-dimensional [[anti-de Sitter spacetime]] with a compact 4-dimensional [[orbifold]]

$$
  AdS_7 \times X_4
$$

(the [[near horizon geometry]] of a [[black brane|black]] [[M5-brane]]) are all of the form

$$
  X_4 \simeq S^4//G
$$

where $G \subset SU(2)$ is a [[finite group|finite]] [[subgroup]] of $SU(2)$ (i.e. an [[ADE classification|ADE group]]), [[action|acting]] via the identification $S^4 \simeq S(\mathbb{R} \oplus \mathbb{H})$ as [above](#QuaternionAction), and where the double slash denotes the [[homotopy quotient]] ([[orbifold quotient]]).

See ([AFHS 98, section 5.2](#AFHS98), [MF 12, section 8.3](#MF12)).



### Free and cyclic loop space
  {#FreeLoopSpace}

We discuss the [[rational homotopy theory]] of the [[free loop space]] $\mathcal{L}(S^4)$ of $S^4$, as well as the [[cyclic loop space]] $\mathcal{L}(S^4)/S^1$  using the results from _[[Sullivan models of free loop spaces]]_:

+-- {: .num_example}
###### Example

Let $X = S^4$ be the [[4-sphere]]. The corresponding [[rational n-sphere]] has minimal Sullivan model

$$
  (\wedge^\bullet \langle g_4, g_7 \rangle, d)
$$

with 

$$
  d g_4 = 0\,,\;\;\;\; d g_7 = -\tfrac{1}{2} g_4 \wedge g_4
  \,.
$$

Hence  [this prop.](Sullivan+model+of+free+loop+space#SullivanModelForTheFreeLoopSpace) gives for the rationalization of 
$\mathcal{L}S^4$ the model

$$
  ( \wedge^\bullet \langle \omega_4, \omega_6, h_3, h_7 \rangle  , d_{\mathcal{L}S^4} ) 
$$



with

$$
  \begin{aligned}
    d_{\mathcal{L}S^4} h_3 & = 0
    \\
    d_{\mathcal{L}S^4} \omega_4 & = 0
    \\
    d_{\mathcal{L}S^4} \omega_6 & = h_3 \wedge \omega_4
    \\
    d_{\mathcal{L}S^4} h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4
    \\
  \end{aligned}
$$

and [this prop](Sullivan+model+of+free+loop+space#ModelForS1quotient)
gives for the rationalization of $\mathcal{L}S^4 / / S^1$ the model

$$
  ( \wedge^\bullet \langle \omega_2, \omega_4, \omega_6, h_3, h_7 \rangle  , d_{\mathcal{L}S^4 / / S^1} ) 
$$

with 

$$
  \begin{aligned}
    d_{\mathcal{L}S^4 / / S^1} h_3 & = 0
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_2 & = 0
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_4 & = h_3 \wedge \omega_2 
    \\
    d_{\mathcal{L}S^4 / / S^1} \omega_6 & = h_3 \wedge \omega_4
    \\
    d_{\mathcal{L}S^4 / / S^1} h_7 & = -\tfrac{1}{2} \omega_4 \wedge \omega_4 + \omega_2 \wedge \omega_6
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Let $\hat \mathfrak{g} \to \mathfrak{g}$ be a [[central extension|central]] [[Lie algebra extension]] by $\mathbb{R}$ of a finite dimensional Lie algebra $\mathfrak{g}$, and let $\mathfrak{g} \longrightarrow b \mathbb{R}$ be the corresponding [[L-∞ algebra cohomology|L-∞ 2-cocycle]] with coefficients in the [[line Lie n-algebra|line Lie 2-algebra]] $b \mathbb{R}$, hence ([[schreiber:The brane bouquet|FSS 13, prop. 3.5]]) so that there is a [[homotopy fiber sequence]] of [[L-∞ algebras]]

$$
  \hat \mathfrak{g}
    \longrightarrow
  \mathfrak{g}
    \overset{\omega_2}{\longrightarrow}
  b \mathbb{R}
$$

which is dually modeled by

$$
  CE(\hat \mathfrak{g})
    =
  ( \wedge^\bullet ( \mathfrak{g}^\ast \oplus \langle e \rangle ), d_{\hat \mathfrak{g}}|_{\mathfrak{g}^\ast} = d_{\mathfrak{g}},\;  d_{\hat \mathfrak{g}} e = \omega_2)
  \,.
$$

For $X$ a space with [[Sullivan model]] $(A_X,d_X)$ write $\mathfrak{l}(X)$ for the corresponding [[L-∞ algebra]], i.e. for the $L_\infty$-algebra whose [[Chevalley-Eilenberg algebra]] is $(A_X,d_X)$:

$$
  CE(\mathfrak{l}X) = (A_X,d_X)
  \,.
$$

Then there is an [[isomorphism]] of [[hom-sets]]

$$
  Hom_{L_\infty Alg}( \hat \mathfrak{g}, \mathfrak{l}(S^4) )
  \;\simeq\;
  Hom_{L_\infty Alg/b \mathbb{R}}( \mathfrak{g}, \mathfrak{l}( \mathcal{L}S^4 / S^1 ) )
  \,,
$$

with $\mathfrak{l}(S^4)$ from [this prop.](Sullivan+model+of+free+loop+space#SullivanModelForTheFreeLoopSpace) 
and $\mathfrak{l}(\mathcal{L}S^4 //S^1)$ from [this prop.](Sullivan+model+of+free+loop+space#ModelForS1quotient),
where on the right we have homs in the [[slice category|slice]] over the [[line Lie n-algebra|line Lie 2-algebra]], via [this prop.](Sullivan+model+of+free+loop+space#ModelForS1quotient)



Moreover, this isomorphism takes

$$
  \hat \mathfrak{g}
    \overset{(g_4, g_7)}{\longrightarrow}
  \mathfrak{l}(S^4) 
$$

to

$$
  \array{
    \mathfrak{g} 
      &&
      \overset{(\omega_2,\omega_4, \omega_6, h_3,h_7)}{\longrightarrow}
      &&
    \mathfrak{l}( \mathcal{L}X / S^1 )
    \\
    & 
    {}_{\mathllap{\omega_2}}\searrow 
      && 
    \swarrow_{\mathrlap{\omega_2}}
    \\
    && b \mathbb{R}
  }
  \,,
$$

where

$$
  \omega_4 = g_4 - h_3 \wedge e
  \;\,,
  \;\;\;
  h_7 = g_7 + \omega_6 \wedge e
$$

with $e$ being the central generator in $CE(\hat \mathfrak{g})$ from above, and where the equations take place in $\wedge^\bullet \hat \mathfrak{g}^\ast$ with the defining inclusion $\wedge^\bullet \mathfrak{g}^\ast \hookrightarrow \wedge^\bullet \mathfrak{g}^\ast$ understood.

=--

This is observed in ([FSS 16](Sullivan+model+of+free+loop+space#FiorenzaSatiSchreiber16), [FSS 16b](#FSS16b)), where it serves to formalize, on the level of [[rational homotopy theory]], the [[double dimensional reduction]] of [[M-branes]] in [[M-theory]] to [[D-branes]] in [[type IIA string theory]] (for the case that $\mathfrak{g}$ is type IIA [[super Minkowski spacetime]] $\mathbb{R}^{9,1\vert \mathbf{16}+ \overline{\mathbf{16}}}$ and $\hat \mathfrak{g}$ is 11d [[super Minkowski spacetime]] $\mathbb{R}^{10,1\vert \mathbf{32}}$, and the cocycles are those of [[schreiber:The brane bouquet]]).

+-- {: .proof}
###### Proof

By the fact that the underlying graded algebras are free, and since $e$ is a generator of odd degree, the given decomposition for $\omega_4$ and $h_7$ is unique.

Hence it is sufficient to observe that under this decomposition the defining equations

$$
  d g_4 = 0
  \,,\;\;\;
  d g_{7} = -\tfrac{1}{2} g_4 \wedge g_4
$$

for the $\mathfrak{l}S^4$-valued cocycle on $\hat \mathfrak{g}$ turn into the equations for a $\mathfrak{l} ( \mathcal{L}S^4 / S^1 )$-valued cocycle on $\mathfrak{g}$. This is straightforward:

$$
  \begin{aligned}
    & d_{\hat \mathfrak{g}} ( \omega_4 + h_3 \wedge e ) = 0
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_{\mathfrak{g}} (\omega_4 - h_3 \wedge \omega_2) = 0
    \;\;\; and \;\;\;
    d_{\mathfrak{g}} h_3 = 0
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_{\mathfrak{g}} \omega_4 = h_3 \wedge \omega_2
    \;\;\; and \;\;\;
    d_{\mathfrak{g}} h_3 = 0
  \end{aligned}
$$

as well as

$$
  \begin{aligned}
    & d_{\hat \mathfrak{g}} ( h_7 - \omega_6 \wedge e ) 
      = -\tfrac{1}{2}( \omega_4 + h_3 \wedge e ) \wedge (\omega_4 + h_3\wedge e)
   \\
    \Leftrightarrow \;\;\;\;
    &
    d_\mathfrak{g} h_7 - \omega_6 \wedge \omega_2
    =
    -\tfrac{1}{2}\omega_4 \wedge \omega_4
    \;\;\; and \;\;\;
    - d_\mathfrak{g} \omega_6 = - h_3 \wedge \omega_4 
    \\
    \Leftrightarrow \;\;\;\;
    &
    d_\mathfrak{g} h_7 = -\tfrac{1}{2}\omega_4 \wedge \omega_4  + \omega_6 \wedge \omega_2 
    \;\;\; and \;\;\;
    d_\mathfrak{g} h_6 = h_3 \wedge \omega_4
  \end{aligned}
$$

=--


The [[unit of an adjunction|unit]] of the [[double dimensional reduction]]-[[adjunction]] 

$$
  \infty Grpd
    \underoverset
      {\underset{\mathcal{L}(-)/S^1}{\longrightarrow}}
      {\overset{hofib}{\longleftarrow}}
      {\bot}
  \infty Grpd_{/B S^1}
$$


([this prop.](double+dimensional+reduction#GeneralReduction)) applied to the $S^1$-[[principal infinity-bundle]] 

$$
  \array{
    S^4  
    \\
    {}^{\mathllap{hofib(c)}}\downarrow
    \\
    S^4 / S^1
    &\underset{c}{\longrightarrow}&
    B S^1
  }
$$ 

is a natural map

$$
  S^4/S^1 \longrightarrow \mathcal{L}(S^4)/S^1
$$

from the [[homotopy quotient]] by the [[circle action]] (def. \ref{CircleActionOn4Sphere}), to the [[cyclic loop space]] of the 4-sphere.




### Diffeomorphism group

Counterexamples (via [[graph complexes]]) to the analogue of the [[Smale conjecture]] for the 4-sphere are claimed in [Watanabe 18](diffeomorphism+group#Watanabe18), reviewed in [Watanabe 21](diffeomorphism+group#Watanabe21).


## Related entries

[[spheres -- contents]]

* [[fuzzy 4-sphere]]

* [[2-sphere]]

* [[3-sphere]]

* [[5-sphere]]

* [[6-sphere]]

* [[7-sphere]]

* [[n-sphere]]





## References

### General

* {#FreedmanGompfMorrisonWalker09} [[Michael Freedman]], [[Robert Gompf]], [[Scott Morrison]], [[Kevin Walker]], _Man and machine thinking about the smooth 4-dimensional Poincar&#233; conjecture_, Quantum Topology, Volume 1, Issue 2 (2010), pp. 171-208 ([arXiv:0906.5177](http://arxiv.org/abs/0906.5177))

* {#RoigSaralegiAranguren00} [[Agustí Roig]], [[Martintxo Saralegi-Aranguren]], _Minimal Models for Non-Free Circle Actions_, Illinois Journal of Mathematics, volume 44, number 4 (2000) ([arXiv:math/0004141](https://arxiv.org/abs/math/0004141))

* {#AFHS98} [[Bobby Acharya]], [[José Figueroa-O'Farrill]], [[Chris Hull]], B. Spence, _Branes at conical singularities and holography_ , Adv. Theor. Math. Phys. 2 (1998) 1249&#8211;1286

* {#FelixOpreaTanre08} [[Yves Félix]], John Oprea, [[Daniel Tanré]], _Algebraic Models in Geometry_, Oxford University Press 2008

* {#MF12} [[Paul de Medeiros]], [[José Figueroa-O'Farrill]], _Half-BPS M2-brane orbifolds_, Adv. Theor. Math. Phys. Volume 16, Number 5 (2012), 1349-1408. ([arXiv:1007.4761](http://arxiv.org/abs/1007.4761), [Euclid](https://projecteuclid.org/euclid.atmp/1408561553))

* {#BettiolMendes15} Renato G. Bettiol, Ricardo A. E. Mendes, _Flag manifolds with strongly positive curvature_, Math. Z. 280 (2015), no. 3-4, 1031-1046 ([arXiv:1412.0039](https://arxiv.org/abs/1412.0039))

* Selman Akbulut, _Homotopy 4-spheres associated to an infinite order loose cork_ ([arXiv:1901.08299](https://arxiv.org/abs/1901.08299))

* Akio Kawauchi, _Smooth homotopy 4-sphere_ ([arXiv:1911.11904](https://arxiv.org/abs/1911.11904))


### Branched covers

All [[PL manifold|PL]] [[4-manifolds]] are _simple_ [[branched covers]] of the  [[4-sphere]]:

* {#Piergallini95} [[Riccardo Piergallini]], _Four-manifolds as 4-fold branched covers of $S^4$_, Topology Volume 34, Issue 3, July 1995 (<a href="https://doi.org/10.1016/0040-9383(94)00034-I">doi:10.1016/0040-9383(94)00034-I</a>, [pdf](https://core.ac.uk/download/pdf/82379618.pdf))

* {#IoriPiergallini02} Massimiliano Iori, [[Riccardo Piergallini]], _4-manifolds as covers of the 4-sphere branched over non-singular surfaces_, Geom. Topol. 6 (2002) 393-401 ([arXiv:math/0203087](https://arxiv.org/abs/math/0203087))


Speculative remarks on the possible role of maps from [[spacetime]] to the [[4-sphere]] in some kind of [[quantum gravity]] via [spectral geometry](spectral+triple) (related to the [[Connes-Lott-Chamseddine-Barrett model]]) are in 

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Quanta of Geometry: Noncommutative Aspects_, Phys. Rev. Lett. 114 (2015) 9, 091302 ([arXiv:1409.2471](https://arxiv.org/abs/1409.2471))

* {#ChamseddineConnesMukhanov14} [[Ali Chamseddine]], [[Alain Connes]], Viatcheslav Mukhanov, _Geometry and the Quantum: Basics_, JHEP 12 (2014) 098 ([arXiv:1411.0977](https://arxiv.org/abs/1411.0977))

* {#Connes17} [[Alain Connes]], section 4 of _Geometry and the Quantum_, in _Foundations of Mathematics and Physics One Century After Hilbert_, Springer 2018. 159-196 ([arXiv:1703.02470](https://arxiv.org/abs/1703.02470), [doi:10.1007/978-3-319-64813-2](https://www.springer.com/gp/book/9783319648125))

* [[Alain Connes]], from 58:00 to 1:25:00 in _Why Four Dimensions and the Standard Model Coupled to Gravity - A Tentative Explanation From the New Geometric Paradigm of NCG_, talk at IHES, 2017 ([video recording](https://www.youtube.com/watch?v=qVqqftQ92kA))

[[!redirects 4-spheres]]