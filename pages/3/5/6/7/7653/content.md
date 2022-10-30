
> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

The [[background gauge fields]] on [[spacetime]] appearing in [[string theory]] are mathematically described by [[cocycles]] in [[twisted cohomology|twisted]] and [[differential cohomology|differential]] refinements of [[smooth infinity-groupoid|smooth]] [[cohomology]]. A famous example is the [[twisted K-theory]] that describes the [[B-field]]-twisted [[Yang-Mills fields]] over [[D-branes]] in [[type II string theory]], but there are many more classes of examples of twisted / smooth / differential cohomology appearing throughout string theory.

This page discusses such examples. An overview table of some is below in _[Table of twists](#TableOfTwists)_.

We start with an introduction to the general notion of twisted smooth cohomology by way of a simple but useful example below in 

* I) [Warmup example: geometric structure (generalized, exceptional)](#VielbeinFields),

which already serves as a blueprint for all of the examples to follow.

(The mathematically inclined reader wishing to see a more formal development of the general theory behind all of the discussion here should look at the section _[General theory](#GeneralTheory)_, but other readers should be able to safely skip this and possibly only come back to it later when in need of further detail.)

We then discuss three main further classes of examples

* II) [Spin-, String-, and Fivebrane structures](#SpinStringFivebraneStructures)

* III) [$Spin^c$-, $String^c$-, and $Fivebrane^c$-structures](#TwistedK)

* IV) [Higher orientifold structures](#HigherOrientifold)






## Examples
 {#Examples}

### Overview: The Table of Twists
 {#TableOfTwists} 

The following sections discuss classes of examples of [[twisted differential c-structures|twisted smooth structures]] in [[string theory]]. All these examples are governed by the the same general pattern of [[twisted cohomology]] discussed [above](#TwistedCohomology) and are specified by a _universal coefficient bundle_

$$
  \array{ 
    F &\to& E
    \\ 
    && 
    \downarrow^{\mathrlap{\mathbf{c}}} 
    \\ 
    && \mathbf{B}G 
   }
$$

in $\mathbf{H} = $ [[Smooth∞Grpd]], where

* $G$ is a [[smooth ∞-group]];

* $F$ is a coefficient object equipped with a $G$-[[action]] $\rho$;

* $E \to \mathbf{B}G$ is the [[associated ∞-bundle|associated bundle]] to the $G$-[[universal principal ∞-bundle]] over the [[moduli ∞-stack]] $\mathbf{B}G$ of $G$-[[principal ∞-bundles]].

Given such, and given a [[spacetime]]/[[target space]] $X$, we have

* a morphism $\phi : X \to \mathbf{B}G$ determines a _twisting bundle_ or _twisting [[background gauge field]]_ on $X$;

* a lift

  $$
    \array{
      X &&\stackrel{\hat \phi}{\to}&& P
      \\
      & {}_{\mathllap{\phi}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{c}}}
      \\
      && \mathbf{B}G
    }
  $$

  is a $\phi$-[[twisted infinity-bundle|twisted bundle]], or $\phi$-twisted background gauge field.

The following table lists examples of such coefficient bundles and tabulates the correspondings twisting fields and twisted fields. More details are in the sections to follow.


| | universal coefficient bundle | twisting bundle | twisting field | twisted bundle | twisted field |
|---|---|---|---|---|---|
| | $\array{ F &\to& E  \\ && \downarrow^{\mathrlap{\rho}} \\ && \mathbf{B}G }$ | $G$-[[principal infinity-bundle|principal bundle]] | $G$-[[higher gauge field|gauge field]] | [[section]] of $\rho$-[[associated infinity-bundle|associated]] $F$-bundle | twisted $\Omega E$-[[gauge field]]  | 
| [[reduction of structure group]]/[[G-structure|geometric structure]] | | | | | |
| | $\array{ GL(n)/O(n) &\to& \mathbf{B} O(n) \\ && \downarrow \\ && \mathbf{B} GL(n) }$ | [[manifold]] structure / [[tangent bundle]] |  | [[vielbein]] | [[gravity]] |
| | $\array{ GL(n)/O(n) &\to& \mathbf{B} O(n)_{conn} \\ && \downarrow \\ && \mathbf{B} GL(n)_{conn} }$ | [[affine connection]] |  | [[spin connection]] | [[gravity]] |
| | $\array{ && \mathbf{B} U(d,d) \\ && \downarrow  \\ && \mathbf{B} O(2d,2d) }$ | [[generalized tangent bundle]] | | [[generalized complex geometry]] | [[generalized Calabi-Yau manifolds]] |
| | $\array{ O(n)\backslash O(n,n)/O(n) &\to& \mathbf{B} O(n) \times O(n) \\ && \downarrow \\ && \mathbf{B} O(n,n) }$ | [[generalized  tangent bundle]] |  | [[type II geometry]] | DFT [[type II supergravity]] | 
| | $\array{ SU(3)\backslash O(6,6) / SU(3) &\to& \mathbf{B} SU(3) \\ && \downarrow \\ && \mathbf{B} O(6,6) }$ | [[generalized tangent bundle]]  | | [[type II geometry]] | $d = 6$, $N=1$  [[type II supergravity]] [[Kaluza-Klein mechanism|comactifications]] | 
| |  $\array{ && \mathbf{B} SU(7) \\ && \downarrow \\ && \mathbf{B}E_{7(7)} }$ | [[exceptional tangent bundle]] | |  | $d = 7$, $N=1$ [[11-dimensional supergravity|11d supergravity]] [[Kaluza-Klein mechanism|compactifications]] |
| | $\array{ E_{n(n)}/H_n &\to& \mathbf{B}H_n \\ && \downarrow \\ && \mathbf{B}E_{n(n)} }$ | [[exceptional tangent bundle]]  |  | [[U-duality]] [[exceptional generalized geometry]] | [[Kaluza-Klein mechanism|compactified]] [[11-dimensional supergravity|11d supergravity]] field |
| | $\array{ \mathbf{B} U &\to& \mathbf{B} P U \\ && \downarrow^{\mathbf{dd}} \\ && \mathbf{B}^2 U(1) }$ | [[circle n-bundle with connection|circle 2-bundle]]/$U(1)$-[[bundle gerbe]] | [[B-field]] | [[twisted bundle|twisted unitary bundle]] | [[Yang-Mills field]] |
| | $\array{ && \mathbf{B} E_8 \\ && \downarrow^{\mathrlap{\mathbf{a}}} \\ && \mathbf{B}^3 U(1)} $ | [[circle n-bundle with connection|circle 3-bundle]] / [[bundle 2-gerbe]] | [[supergravity C-field]] |  | [[E8]]-[[gauge field]] |
| [higher spin structures](spin+structure#Higher) | | | | | |
| | $\array{ \mathbf{B} Spin &\to& \mathbf{B} SO \\ && \downarrow^{\mathrlap{\mathbf{w}_2}} \\ && \mathbf{B}^2 \mathbb{Z}_2 }$ | [[second Stiefel-Whitney class]] | | [[twisted spin structure]] |  |
| | $\array{ \mathbf{B}String &\to& \mathbf{B} Spin  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\mathbf{p}_1}} \\ && \mathbf{B}^3 U(1)  }$ | [[circle n-bundle with connection|circle 3-bundle]]/$U(1)$-[[bundle 2-gerbe]] |  [[NS5-brane]] [[magnetic charge]] |  [[twisted differential string structure|twisted smooth string structure]] |  |
| | $\array{ \mathbf{B}String_{conn} &\to& \mathbf{B} Spin_{conn}  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\hat \mathbf{p}_1}} \\ && \mathbf{B}^3 U(1)_{conn}  }$ | [[circle n-bundle with connection|circle 3-bundle with connection]]| [[NS5-brane]] [[current|magnetic current]]  |  [[twisted differential string structure]] | [[Green-Schwarz mechanism]] [[gravity]]+[[B-field]] |
| | $\array{ \mathbf{B}Fivebrane &\to& \mathbf{B} String  \\ && \downarrow^{\mathrlap{\tfrac{1}{6}\mathbf{p}_2}} \\ && \mathbf{B}^7 U(1)  }$ | [[circle n-bundle with connection|circle 7-bundle]]| [[string]] [[electric charge]]  | [[twisted differential fivebrane structure|twisted smooth fivebrane structure]] |  |
| | $\array{ \mathbf{B}Fivebrane_{conn} &\to& \mathbf{B} String_{conn}  \\ && \downarrow^{\mathrlap{\tfrac{1}{6}\hat \mathbf{p}_2}} \\ && \mathbf{B}^7 U(1)_{conn}  }$ | [[circle n-bundle with connection|circle 7-bundle with connection]]| [[string]] [[current|electric current]] | [[twisted differential fivebrane structure]] | dual [[Green-Schwarz mechanism]] [[gravity]]+[[B6-field]] |
| [higher spin^c-structures](spin^c+structure#Higher) | | | | | |
| | $\array{ \mathbf{B}Spin^c &\to& \mathbf{B} (SO \times U(1))  \\ && \downarrow^{\mathrlap{ w_2 - c_1}} \\ && \mathbf{B}^2 \mathbb{Z}_2  }$ |  |   | [[twisted spin^c structure]] |  |
|  | $\array{ && \mathbf{B} (PU \times SO) \\ && \downarrow^{\mathrlap{ \mathbf{dd} - \mathbf{W}_3 }} \\ && \mathbf{B}^2 U(1) }$ | [[circle n-bundle with connection|circle 2-bundle]] |  [[B-field]] | [[twisted spin^c structure]]  | Freed-Witten anomaly for type II string on D-brane  |
| | $\array{ \mathbf{B}String^{\mathbf{a}} &\to& \mathbf{B} Spin \times E_8  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\mathbf{p}_1 - 2 \mathbf{a}}} \\ && \mathbf{B}^3 U(1)  }$ | [[circle n-bundle with connection|circle 3-bundle]]/$U(1)$-[[bundle 2-gerbe]] |  [[supergravity C-field]] |  [[twisted differential string structure|twisted smooth string^c structure]] |  [[gravity]]+[[B-field]]+[[E8]]-[[gauge field]] |
| Giraud-[[∞-gerbes]] | | | | | |
| | $\array{ \mathbf{B}^2 U(1) &\to& \mathbf{B}Aut(\mathbf{B}U(1)) \\ && \downarrow \\ && \mathbf{B}\mathbb{Z}_2 }$ | [[double cover]] |  | [[Jandl gerbe]] | [[orientifold]] [[B-field]] | 
| | $\array{ \mathbf{B}^3 U(1) &\to& \mathbf{B}Aut(\mathbf{B}^2 U(1)) \\ && \downarrow \\ && \mathbf{B}\mathbb{Z}_2 }$ | [[double cover]] |  | | [[Ho?ava-Witten theory|Ho?ava-Witten orientifold]] | 
 

### Geometric structure (generalized, exceptional)
 {#VielbeinFields}

The ordinary notion of _[[vielbein]]_ in [[differential geometry]] (equivalently: _[[soldering form]]_ or _[[orthogonal structure]]_) turns out to be a simple special case of the general notion of twisted smooth cohomology that we are concerned with here. Viewed from this perspective it already contains the seeds of all the more sophisticated examples to be considered below. Therefore we discuss this case here as a warmup such as to introduce the general theory by way of example. 

(The reader who wishes to see a systematic discussion of the general theory should instead go to the section _[General Theory](#GeneralTheory)_ and then come back here for a first example.) 

#### The class of the tangent bundle
 {#ClassOfTheTangentBundle}

For completeness, we first review how the [[tangent bundle]] of a [[smooth manifold]] is naturally incarnated as a [[cocycle]] in $GL(n)$-valued [[Cech cohomology]] and how this in turn is naturally formulated in terms of [[Lie groupoids]]/[[differentiable stack|smooth]] [[moduli stacks]]. The reader familiar with these basics should skip to the [next section](#ReductionOfTheStructureGroup).

Let $X$ be a [[smooth manifold]] of [[dimension]] $n$. 

By definition this means that there is an [[atlas]] $\{\phi_i^{-1} : \mathbb{R}^n \simeq U_i \hookrightarrow X\}$ of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two [[coordinate charts]] the [[partial derivatives]] of the corresponding [[coordinate transformations]]

$$
  \phi_j\circ \phi_i^{-1}
  : 
  U_i \cap U_j \subset \mathbb{R}^n \to \mathbb{R}^n
$$

form the [[Jacobian matrix]] of [[smooth functions]]

$$
  ((\lambda_{i j})^{\mu}{}_{\mu})
  \coloneqq
  \left[\frac{d}{d x^\nu} \phi_j \circ \phi_i^{-1} (x^\mu)
  \right]
  :
  U_i \cap U_j 
  \to 
  GL_n
$$

with values in invertible [[matrices]], hence in the
[[general linear group]] $GL(n)$. By construction (by the [[chain rule]]), these functions satisfy on triple overlaps of coordinate charts the [[matrix product]] equations

$$
  (\lambda_{i j})^\mu{}_\lambda (\lambda_{j k})^\lambda{}_{\nu} 
  = 
  (\lambda_{i k})^\mu{}_{\nu}
  \,,
$$

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlap.

This is the [[cocycle]] condition for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of smooth functions with values in $GL(n)$ ):

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

It is useful to formulate this statement in the language of [[Lie groupoids]]/[[differentiable stacks]]. 

* $X$ itself is trivially a Lie groupoid $(X \stackrel{\to}{\to} X)$;

* from the atlas $\{U_i \to X\}$ we get the corresponding [[Cech groupoid]] 
  $$
    C(\{U_i\}) = 
    (\coprod_{i, j} U_i \cap U_j \stackrel{\to}{\to} \coprod_i U_i)
    = 
    \left\{
      \array{
         && (x,j)
         \\
         & \nearrow &=& \searrow
         \\
        (x,i) &&\to&& (x,k)
      }
      \;\;\;
      for\, x \in U_i \cap U_j \cap U_k
    \right\}
  $$

* any [[Lie group]] $G$ induces its [[delooping]] [[Lie groupoid]] 
  
  $$
    \mathbf{B}G
    = 
    \left(
       G \stackrel{\to}{\to} * 
    \right)
    \,.
  $$

The above situation is neatly encoded in the existence of a [[diagram]] of Lie groupoids of the form

$$
  \array{
     C(\{U_i\}) &\stackrel{\lambda}{\to}& \mathbf{B} GL(n).
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     X
  }
  \,,
$$

where

* the left morphism is [[stalk]]-wise (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]];

* the horizontal functor has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.

A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

#### Smooth moduli stacks

We want to think of such a diagram as being directly a morphism of [[smooth infinity-groupoid|smooth groupoids]]


$$
  T X \; : \; X \to \mathbf{B} GL(n) \;\; \in \mathbf{H}
$$

such that this may be regarded as a smooth refinement of the underlying [[homotopy]] of a  map into the [[classifying space]] $B GL(n)$

$$
  X \to B GL(n) \in Top  
  \,.
$$

Evidently, for this we need to turn the [[stalk]]-wise [[homotopy equivalence]] $C(\{U_i\}) \to X$ into an actual [[homotopy equivalence]]. This is a non-abelian/non-stable generalization of what happens in the construction of a [[derived category]], say in the discussion of [[topological string|topological branes]].

To make this precise, first notice that every Lie groupoid $A = (A_1 \stackrel{\to}{\to} A_0)$ yields on each smooth manifold $U$ a groupoid of maps from $U$ into $A$

$$
  A : U \mapsto (C^\infty(U,A_1) \stackrel{\to}{\to} C^\infty(U,A_0))
  \,.
$$

Moreover, for every smooth function $U_1 \to U_2$ there is an evident restriction map $A(U_2) \to A(U_1)$ and so this yields a [[presheaf]] of groupoids, $A \in Func(SmthMfd^{op}, Grpd)$.

Let therefore

$$
  \mathbf{H} \coloneqq Func(SmthMfd^{op}, Grpd)[\{stalkwise\, h.e\}^{-1}]
$$

be the [[simplicial localization|localization]] that universally turns [[stalk]]wise [[homotopy equivalences]] into actual homotopy equivalences. We call this the _[[(2,1)-topos]]_ of _[[smooth infinity-groupoid|smooth groupoids]]_ or _[[smooth infinity-groupoid|smooth stacks]]_.

Then we have

1. a morphism $X \to \mathbf{B} GL(n)$ in $\mathbf{H}$ is precisely a smooth real vector bundle on $X$;

1. a homotopy between two such morphisms in $\mathbf{H}$ is precisely a smooth $GL(n)$-[[gauge transformation]] between the two vector bundles.

Therefore $\mathbf{B}GL(n)$ regarded as an object of $\mathbf{H}$ is the _[[moduli stack]]_ of real vector bundles.

Of course there is a "smaller" Lie groupoid that also classifies real vector bundles. Passing to this "smaller" Lie groupoid is what the choice of vielbein accomplishes, to which we now turn.


#### Reduction of the structure group
 {#ReductionOfTheStructureGroup}


Consider the defining inclusion of the [[orthogonal group]] into the [[general linear group]]

$$
  O(n) \hookrightarrow GL(n)
  \,.
$$

We may understand this inclusion geometrically in terms of the canonical [[metric]] on $\mathbb{R}^n$, but we may also understand it purely Lie theoretically as the
the inclusion of the [[maximal compact subgroup]] of $GL(n)$. This makes it manifest that the inclusion is trivial at the level of [[homotopy theory]] (it is a [[homotopy equivalence]]) and hence _only_ encodes geometric information.


The inclusion induces a corresponding inclusion ([[truncated object of an (infinity,1)-category|0-truncated morphism]]) of moduli stacks

$$
  \mathbf{OrthStruc} : \mathbf{B} O(n) \to \mathbf{B} GL(n)
  \,.
$$

Now we can say what a [[Riemannian metric]]/[[orthogonal structure]] on $X$ is: A choice of [[orthogonal structure]] on $T X$ is a factorization of the above $GL(n)$-valued cocycle $\lambda$ through $\mathbf{c}$, up to a smooth [[homotopy]] $E$, hence a [[diagram]]

$$
  \array{
     X &&\stackrel{h}{\to}&& \mathbf{B} O(n)
     \\
     & {}_{\mathllap{\lambda}}\searrow &\swArrow_{E^{-1}}& \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$.

This consists of two pieces of data

* the morphism $h$ is a $O(n)$-valued 1-cocycle -- a collection of _orthogonal transition functions_ --  hence on each overlap of coordinate patches a smooth function
  
  $$
    ((h_{i j}){}^a{}_b) : U_i \cap U_j \to O(n)
  $$
  
  such that 

  $$
    h_{i j} \cdot h_{j k} = h_{i k}
    \,;
  $$

* the homotopy $E$ is on each chart a function

$$
  E_i  = ((E_i)^a{}_\mu) : U_i \to GL(n)
$$

  * such that on each overlap of coordinate charts it intertwines the transition functions $\lambda$ of the tangent bundle with the new orthogonal transition functions, meaning that the equation

    $$
      (E_i)^a{}_{\mu} (\lambda_{i j})^{\mu}{}_\nu
      =
      (h_{i j})^a{}_b (E_j)^b{}_\nu
    $$

    holds. This exhibits the [[natural transformation|naturality]] [[diagram]] of $E$:

  $$
    \array{
       * &\stackrel{E_i}{\to}& * 
       \\
       {}^{\mathllap{\lambda_{i j}}}\downarrow && \downarrow^{\mathrlap{h_{i j}}}
       \\
       * &\stackrel{E_j}{\to}& * 
    }
  $$

The component $h$ defines an $O(n)$-[[principal bundle]] on $X$, or its [[associated bundle|associated]] [[vector bundle]].
The component $E$ is the corresponding **vielbein**. It exhibits an [[isomorphism]] 

$$
  E : T X \stackrel{\simeq}{\to} V
$$

between a [[vector bundle]] $V \to X$ with [[structure group]] explicitly being the [[orthogonal group]] and the [[tangent bundle]], hence it exhibits the [[reduction of structure groups|reduction of the structure group]] of $T X$ from $GL(n)$ to $O(n)$.

#### Moduli space of orthogonal structures: twisted cohomology
 {#ModuliSpaceOfOrhtogonalStructures}

In order to understand the space of choices of vielbein fields on a given tangent bundle, hence the _[[moduli space]]_ or _[[moduli stack]]_ of [[orthogonal structures]]/[[Riemannian metrics]] on $X$, it is useful to first consider the [[homotopy fiber]] of the morphism $\mathbf{c} : \mathbf{B}O(n) \to \mathbf{B}GL(n)$. One finds that this is the [[coset]] $O(n) \backslash GL(n)$. We may think of the [[fiber sequence]]

$$
  \array{  
    GL(n)/O(n) &\to& \mathbf{B} O(n)
    \\
    && \downarrow
    \\
    && \mathbf{B} GL(n)
  }
$$

as being a bundle in $\mathbf{H}$ over the [[moduli stack]] $\mathbf{B}GL(n)$ with typical fiber $GL(n)/O(n)$. It is  the smooth [[associated infinity-bundle|associated bundle]] to the smooth [[universal principal bundle|universal GL(n)-bundle]] induced by the canonical [[action]] of $GL(n)$ on $O(n)\backslash GL(n)$.

This means that if the tangent bundle $T X$ is trivializable, then the coset space $O(n)\backslash GL(n)$ is the moduli space for vielbein fields on $T X$: 

$$
  (T X \; trivializable)
  \Rightarrow
  SpaceOfVielbeinFieldsOn(T X)
  =
  \mathbf{H}(X, O(n)\backslash GL(n)) = C^\infty(X, O(n)\backslash GL(n))
  \,.
$$

However, if $T X$ is not trivial, then this is true only locally: there is then an [[atlas]] $\{U_i \to X\}$ such that restricted to each $U_i$ the moduli space of vielbein fields is $C^\infty(U_i, GL(n)/ O(n))$, but globally these now glue together in a non-trivial way as encoded by the tangent bundle: we may say that 

the tangent bundle _twists_ the functions $X \to GL(n)/O(n)$. If we think of an ordinary such function as a cocycle in degree-0 cohomology, then this means that a vielbein is a cocycle in $T X$-_[[twisted cohomology]]_ relative to the _twisting coefficient bundle_ $\mathbf{c}$.

We can make this more manifest by writing equivalently

$$
  \array{
    O(n)\backslash GL(n) &\to& (O(n)\backslash GL(n)) // GL(n)
    \\
    && \downarrow   
    \\
    && \mathbf{B}GL(n)
  }
  \,,
$$

where now on the right we have inserted the [[fibration]] resolution of the morphism $\mathbf{c}$ as provided by the [[factorization lemma]]: this is the morphism out of the [[action groupoid]] of the action of $GL(n)$ on $O(n)\backslash GL(n)$.


The pullback

$$
  \array{
    T X \times_{GL(n)} (O(n)\backslash GL(n)) 
      &\to&
    O(n)\backslash GL(n) // GL(n)
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{T X}{\to}& \mathbf{B}GL(n)
  }  
$$

gives the non-linear $T X$-associated bundle whose space of sections is the "twisted $O(n)\backslash GL(n)$-0-cohomology", hence the space of inequivalent vielbein fields.


#### Moduli stack of orthogonal structures

The above says that the space of vielbein fields is the [[cohomology]] of $T X$ in the [[over-(infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}GL(n)}$ with coefficients in $\mathbf{c} : \mathbf{B}O \to \mathbf{B}GL(n)$

$$
  O Struc_{TX}(X) \simeq \mathbf{H}_{/\mathbf{B}GL(n)}(T X, \mathbf{c})
  \,.
$$

But also this space of choices of vielbein fields has a smooth structure, it is itself a smooth [[moduli stack]]. This is obtained by forming the [[internal hom]] in the slice over $\mathbf{B}GL(n)$ of the [[locally cartesian closed (infinity,1)-category|locally cartesian closed (2,1)-category]] $\mathbf{H}$.

$$
  O \mathbf{Struc}_{T X}(X)
  = 
  [X, \mathbf{B}O]_{\mathbf{B}GL(n)}
$$

#### Differential refinement: Spin connection

We may further lift this discussion to [[differential cohomology]] to get genuine _differential_ $T X$-twisted $\mathbf{c}$-structures. 

Write $\mathbf{B}G_{conn}$ for [[groupoid of Lie-algebra valued forms]]. As an object of $\mathbf{H} = $ [[smooth infinity-groupoid|SmoothGrpd]] this the [[moduli stack]] of $G$-[[connection on a bundle|connections]].

The morphism $\mathbf{c}$ has an evident differential refinement

$$
  \mathbf{c}_{conn} : \mathbf{B}O(n)_{conn} \to \mathbf{B}GL(n)_{conn}
  \,.
$$

The [[homotopy fiber]] of this differential refinement is still the same as before

$$
  \array{
    GL(n)/ O(n) &\to& \mathbf{B} O(n)_{conn}
    \\
    && \downarrow
    \\
    && \mathbf{B} GL(n)_{conn}
  }
  \,,
$$

so that the moduli space of "differential vielbein fields" is the same as that of plain vielbein fields.

Consider an [[affine connection]]

$$
  \nabla_{T X} : X \to \mathbf{B}GL(n)
$$

hence a $GL(n)$-[[principal connection]] which locally on out atas is given by the [[Christoffel symbols]] 

$$
  \Gamma_i = ((\Gamma_i)_\mu{}{}^{\alpha}{}_\beta)
  \in 
  \Omega^1(U_i, \mathfrak{gl}(n))
  \,.
$$

A lift $(\nabla_V, E)$ in 

$$
  \array{
    X &&\stackrel{\nabla_{V}}{\to}&& \mathbf{B}O_{conn}
    \\
    & {}_{\mathllap{\nabla_{T X}}}\searrow 
     &\swArrow_{E^{-1}}& 
    \swarrow_{\mathbf{c}_{conn}}
    \\
    && \mathbf{B}GL(n)_{conn}
  }
$$

is in components


1. a "[[spin connection]]"

   $$
     \omega_\mu = E d E^{-1} + E \Gamma_\mu E^{-1}
   $$

   $$
     \omega_\mu{}^a{}_b 
      = 
      E^a{}_\nu \partial_\mu E^\nu{}_b
      +
      E^a{}_\nu \Gamma_\mu{}^\nu{}_\lambda E^\lambda{}_b
      \,.
   $$

This is the standard formula for the relation between the [[Christoffel symbols]] and the [[spin connection]] in terms of the vielbein.


#### Generalized vielbein fields: generalized complex and type II geometry

The above discussion of vielbein fields has straightforward generalizations to the [[generalized complex geometry]], [[type II geometry]] and [[exceptional generalized geometry]].


We discuss how a type II geometry is the [[reduction of the structure group]] of the [[generalized tangent bundle]] along the inclusion $O(d) \times O(d) \to O(d,d)$.

+-- {: .num_defn #InclusionForTypeIIGeometry}
###### Definition

Consider  the [[Lie group]] inclusion
$$
  \mathrm{O}(d) \times \mathrm{O}(d)
  \to 
  \mathrm{O}(d,d)
$$

of those [[orthogonal group|orthogonal transformations]], that preserve the positive definite part
or the negative definite part of the [[bilinear form]] of signature $(d,d)$, respectively.

If $\mathrm{O}(d,d)$ is presented as the group of $2d \times 2d$-[[matrix|matrices]] that 
preserve the [[bilinear form]] given by the $2d \times 2d$-matrix
$$
  \eta 
  \coloneqq
  \left( 
     \array{
       0 & \mathrm{id}_d
       \\
       \mathrm{id}_d & 0
     }
  \right)
$$

then this inclusion sends a pair $(A_+, A_-)$ of [[orthogonal group|orthogonal]] $n \times n$-matrices
to the matrix
$$
  (A_+ , A_-) 
    \mapsto 
  \frac{1}{\sqrt{2}}
  \left(
    \array{
	   A_+ + A_- & A_+ - A_-
	   \\
	   A_+ - A_- & A_+ + A_-
     }
  \right)
  \,.
$$

=--

This inclusion of [[Lie groups]] induces the corresponding morphism of 
[[smooth infinity-groupoid|smooth]] [[moduli stacks]]
of [[principal bundles]]

$$
  \mathbf{TypeII}
  :
  \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
  \to 
  \mathbf{B} \mathrm{O}(d,d)  
  \,.
$$

+-- {: .num_prop }
###### Proposition

There is a [[fiber sequence]] of [[smooth infinity-groupoid|smooth stacks]] 

  $$
      O(d) \backslash O(d,d) / O(d)
	 \to
  \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
     \stackrel{\mathbf{TypeII}}{\to}
    \mathbf{B} \mathrm{O}(d,d)  	
  \,,
  $$

where the fiber on the left is the [[coset space]] of the [[action]] of $O(d) \times O(d)$ on $O(d,d)$.

=--

+-- {: .num_defn }
###### Definition

There is a canonical embedding
$$
  \mathrm{GL}(d) \hookrightarrow \mathrm{O}(d,d)
$$

of the [[general linear group]].

In the above matrix presentation this is given by sending

$$
  a
  \mapsto 
  \left( 
     \array{
	    a & 0
		\\
		0 & a^{-T}
      }
  \right)
  \,,
$$

where in the bottom right corner we have the [[transpose matrix|transpose]] of the inverse matrix of the invertble
matrix $a$.

=--

+-- {: .num_defn }
###### Definition

Under inclusion of def. \ref{InclusionForTypeIIGeometry}, the 
[[tangent bundle]] of a $d$-[[dimension|dimensional]] 
[[manifold]] $X$ defines an $\mathrm{O}(d,d)$-[[cocycle]]

$$
  T X \otimes T^* X
  :
  
    X 
     \stackrel{T X}{\to}
    \mathbf{B}\mathrm{GL}(d)  
      \stackrel{}{\to}
    \mathbf{B} \mathrm{O}(d,d) 
  \,.
$$

The [[vector bundle]] canonically associated to this composite cocycles may 
canonically be identified with
the [[tensor product]] vector bundle $T X \otimes T^* X$, and so we will
refer to this cocycle by these symbols, as indicated. 
This is also called the **[[generalized tangent bundle]]** of $X$.

=--

Therefore we may canonically consider the groupoid of 
$T X \otimes T^* X$-twisted $\mathbf{TypeII}$-structures, 
according to the general notion of [[twisted differential c-structures]].


+-- {: .num_defn }
###### Definition

A **type II generalized vielbein** on a [[smooth manifold]] $X$ is a diagram

$$
  \array{
    X &&\stackrel{\widetilde(T X \otimes T^* X)}{\to}&& \mathbf{B}(O(n) \times O(n))
    \\
    & {}_{\mathllap{T X \otimes T^* X}}\searrow &\swArrow_{E}& \swarrow_{\mathrlap{\mathbf{TypeII}}}
    \\
    && \mathbf{B} O(n,n)
  }
$$

in $\mathbf{H} = $ [[Smooth∞Grpd]], hence a cocycle in the smooth [[twisted cohomology]]

$$
  E 
   \in 
  \mathbf{TypeII}Struc(X)
  \coloneqq
  \mathbf{H}_{/\mathbf{B} O(n,n)}(T X \otimes T^* X, \mathbf{TypeII})
  \,.
$$


=--

+-- {: .num_prop }
###### Proposition / Definition

  The [[groupoid]] $\mathbf{TypeII}\mathrm{Struc}(X)$
  is that of "generalized vielbein fields" on $X$, as considered for instance 
  around equation (2.24) of ([GMPW](#GMPW))
  (there only locally, but the globalization is evident).
  
  In particular, its set of equivalence classes is the set of 
  type-II generalized geometry structures on $X$.

=--

+-- {: .proof}
###### Proof

Over a local [[coordinate chart]] $\mathbb{R}^d \simeq U_i \hookrightarrow X$, the most general such generalized vielbein
(hence the most general $\mathrm{O}(d,d)$-valued function)
may be parameterized as
$$
  E = 
  \frac{1}{2}
  \left(
    \array{
	  (e_+ + e_-) + (e_+^{-T} - e_-^{-T})B & (e_+^{-T} - e_-^{-T})
	  \\
	  (e_+ - e_-) - (e_+^{-T} + e_-^{-T})B & (e_+^{-T} + e_-^{-T})
     }
  \right)
  \,,
$$

where $e_+, e_- \in C^\infty(U_i, \mathrm{O}(d))$ are thought of as two 
[[vielbein|ordinary vielbein]] fields, and where $B$ is any smooth skew-symmetric $n \times n$-matrix valued function on 
$\mathbb{R}^d \simeq U_i$. 

By an $\mathrm{O}(d) \times \mathrm{O}(d)$-[[gauge transformation]] this can always be brought
into a form where $e_+ = e_- =: \tfrac{1}{2}e$ such that
$$
  E = 
  \left(
    \array{
	  e & 0
	  \\
	  - e^{-T}B  & e^{-T}
	}
  \right)
  \,.
$$

The corresponding "generalized metric" over $U_i$ is

$$
  E^T 
  E
  = 
  \left(
    \array{
	  e^T & B e^{-1}
	  \\
	  0  & e^{-1}
    }
  \right)
  \left(
    \array{
	  e & 0
	  \\
	  - e^{-T}B  & e^{-T}
    }
  \right)
  = 
  \left(
    \array{
	  g - B g^{-1} B & B g^{-1}
	  \\
	  - g^{-1} B  & g^{-1}
     }
  \right)
  \,,
$$

where

$$
  g \coloneqq e^T e
$$

is the [[metric]] (over $\mathbb{R}^q \simeq U_i$ a smooth function with values in symmetric $n \times n$-matrices) 
given by the [[vielbein|ordinary vielbein]] $e$.

=--


#### Exceptional generalized geometry: U-duality geometry

$$
  \array{
     E_n/H_n &\to& \mathbf{B} H_n
     \\
     && \downarrow^{\mathrlap{}}
     \\
     && \mathbf{B} E_n
  }
$$


[[exceptional generalized geometry]], [[U-duality]]


### Spin-, String- and Fivebrane-structures
 {#SpinStringFivebraneStructures}

Above we have seen ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian metric|Riemannian structure]] given by lifts through the inclusion $\mathbf{B} O(n) \to \mathbf{B} GL(n)$. Now we consider further lifts, through the [[Whitehead tower]] of $\mathbf{B}O$. This encodes _[higher spin structures](spin structure#Higher)_.

Where a _[[spin structure]]_ on [[spacetime]] is necessary to cancel a [[quantum anomaly]] of the [[spinning particle]]/[[superparticle]] [[sigma-model]], so the [[heterotic string|heterotic]] [[superstring]] requires, in the absence of a [[gauge field]], a "[higher spin structure](#spin+structure#Higher)", called a _[[string structure]]_.  Further up in dimension, _[[dual heterotic string theory]]_ in the absence of the gauge field involves a  _[[fivebrane structure]]_.

In the presence of a nontrivial [[gauge fields]] string structures are generalized to _[[twisted differential string structure|twisted string structure]]_, which in [[heterotic string theory]] are part of the _[[Green-Schwarz mechanism]]_. These we discuss [below](#TwistedK).


#### Whitehead tower
 {#WhiteheadTower}

The nature of higher spin structures is governed by what is called the _[[Whitehead tower]]_ of the [[homotopy type]] of the [[classifying space]] $B O$ of the [[orthogonal group]], where in each stage a [[homotopy group]] is removed _from below_. This is [[duality|dual]] to the _[[Postnikov tower]]_, where in each stage a homotopy group is added from above.

The [[homotopy groups]] of $B O$ start out as

| $k =$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 
|---|---|---|---|---|---|---|---|---|---|
|$\pi_k(B O) = $  | * | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ | 0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

The Whitehead tower of $B O$ starts out as

$$
  \array{
    & Whitehead tower
    \\
    &\vdots
    \\
    & B Fivebrane &\to& \cdots &\to& *
    \\
    & \downarrow && && \downarrow
    \\
    second frac Pontr. class & B String &\to& \cdots &\stackrel{\tfrac{1}{6}p_2}{\to}&  B^8 \mathbb{Z}
    &\to& * 
    \\
    & \downarrow && && \downarrow && \downarrow
    \\
    first frac Pontr. class & B Spin && && &\stackrel{\tfrac{1}{2}p_1}{\to}& B^4 \mathbb{Z} &\to & * 
    \\
    & \downarrow && && \downarrow && \downarrow && \downarrow
    \\
    second SW class & B S O 
    &\to&
    \cdots
    &\to&
    &\to&
    & \stackrel{w_2}{\to} &
    \mathbf{B}^2 \mathbb{Z}_2
    &\to&
    *
    \\
    & \downarrow && && \downarrow && \downarrow &&  \downarrow && \downarrow
    \\
    first SW class & B O 
    &\to&
    \cdots
    &\to&
    \tau_{\leq 8 } B O
    &\to&
    \tau_{\leq 4 } B O
    &\to&
    \tau_{\leq 2 } B O
    &\stackrel{w_1}{\to}&
    \tau_{\leq 1 } B O
    \simeq
    B \mathbb{Z}_2
    &
    Postnikov  tower
  }
$$

where 

* the stages are the [[deloopings]] of

  ...
  $\to$
  [[fivebrane group]]
  $\to$
  [[string group]]
  $\to$
  [[spin group]]
  $\to$
  [[special orthogonal group]]
  $\to$
  [[orthogonal group]]

* the obstruction classes are the [[universal characteristic classes]]

  * [[first Stiefel-Whitney class]] $w_1$

  * [[second Stiefel-Whitney class]] $w_2$

  * [[Pontryagin class|first fractional Pontryagin class]] $\tfrac{1}{2}p_1$

  * [[Pontryagin class|second fractional Pontryagin class]] $\tfrac{1}{6}p_2$

* every possible square in the above is a [[homotopy pullback]] square (using the [[pasting law]]).

For instance $w_2$ is identified as such by using that $[S^2,-]$ preserves [[homotopy pullbacks]] and sends $ B O \to \tau_{\leq 2} B O$ to an isomorphism on connected components, so that $B SO \to B^2 \mathbb{Z}$ is an [[isomorphism]] on the second [[homotopy group]] and hence, by the [[Hurewicz theorem]], is also an isomorphism on the [[cohomology group]] $H^2(-,\mathbb{Z}_2)$. Analogously for the other characteristic maps.

In summary, more concisely, the tower is

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    B Fivebrane
    \\
    \downarrow
    \\
    B String &\stackrel{\tfrac{1}{6}p_2}{\to}& B^7 U(1) & \simeq B^8 \mathbb{Z}
    \\
    \downarrow
    \\
    B Spin &\stackrel{\tfrac{1}{2}p_1}{\to}& B^3 U(1) & \simeq B^4 \mathbb{Z}
    \\
    \downarrow
    \\
    B SO &\stackrel{w_2}{\to}& B^2 \mathbb{Z}_2
    \\
    \downarrow
    \\
    B O &\stackrel{w_1}{\to}& B \mathbb{Z}_2
    \\
    \downarrow^{\mathrlap{\simeq}}
    \\
    B GL
  }
  \,,
$$

where each "hook" is a [[fiber sequence]].

The [[universal property]] of [[homotopy pullbacks]] says that

* the obstruction to lifting an [[orthogonal structure]] $T X : X \to B O$ to an [[orientation]] structure is the homotopy class $[w_1(T X)] \in H^1(B O, \mathbb{Z}_2)$ of $w_1(T X) : X \stackrel{T X}{\to} B O \stackrel{w_1}{\to} B \mathbb{Z}_2$, the [[first Stiefel-Whitney class]];

* the obstruction to lifting an [[orientation]] structure $T X : X \to B SO$ to an [[spin structure]] is the [[second Stiefel-Whitney class]] $w_2(T X) : X \stackrel{}{\to} B S \stackrel{w_2}{\to} B^2 \mathbb{Z}_2$;

* the obstruction to lifting a [[spin structure]] $X \to B Spin$ to an [[string structure]] is the [[first fractional Pontryagin class]];

* the obstruction to lifting a [[string structure]] $X \to B String$ to a [[fivebrane structure]] is the [[second fractional Pontryagin class]].


#### Necessity of smooth refinement

The [[classifying space]] for, say, the [[spin group]] is _not_ a [[fine moduli space]]: while homotopy classes $Maps(X, B Spin)_\sim$ of maps $X \to B Spin$ are in bijection with equivalence classes of [[spin bundles]] on $X$, the homotopy classes $Maps(X, \Omega B Spin)_\sim = Maps(X, Spin)_\sim$ of [[homotopies]] from the trivial map $X \to * \to B Spin$ are _not_ in general in bijection with the [[gauge transformations]] of the trivial spin bundle: the latter form the set of [[smooth functions]] $C^\infty(X,Spin)$, not just the homotopy classes of these.

Problems include for instance:

* $Maps(X, B(-))_\sim$ does not give the right [[BRST-complex]];

* $Maps(X, B(-))_\sim$ cannot distinguish a group from its [[maximal compact subgroup]], such as $O \hookrightarrow GL_n$, and hence cannot see [[vielbeins]], not [[generalized vielbeins]], not [[exceptional generalized geometry]];

* $Maps(X, B(-))_\sim$ cannot distinguish (over 10-dimensional spacetime $X$) an [[E8]]-[[gauge field]] from a [[NS5-brane]] [[magnetic charge]];

* etc.

These problems are all fixed by refining the [[classifying space]] $B Spin \in \infty Grpd$ to the [[smooth infinity-groupoid|smooth]] [[moduli stack]] $\mathbf{B} Spin \in Smooth \infty Grpd$, and similarly for the other cases.

#### Smooth refinement

[[differential geometry|Differential geometry]] is modeled on [[smooth manifolds]],
and these in turn on smooth [[Cartesian spaces]] $\mathbb{R}^n \in CartSp$. A functor
$X : CartSp^{op} \to \infty Grpd$ encodes a smooth family version of a [[homotopy type]].
For this only the [[germs]] of [[open balls]] $D^n \hookrightarrow \mathbb{R}^n$
matter. Therefore we say that a morphism $X \to Y$ of 
[[smooth infinity-groupoid|smooth homotopy types]] is an 
[[equivalence in an (infinity,1)-category|equivalence]] if it is one restricted to such germs of $n$-disks ("on each [[stalk]]").

This defines a [[homotopy theory]] to be denoted _[[Smooth∞Grpd]]_. 


**Theorem** There is a lift of the [above Whitehead tower](#WhiteheadTower) of [[homotopy type|bare homotopy types]] to a tower of [[smooth infinity-groupoid|smooth homotopy types]]/[[smooth infinity-stacks]] through the [[geometric realization]] map

$$
  {\vert -\vert} : Smooth \infty Grpd \stackrel{\Pi}{\to} \infty Grpd \simeq Top
  \,.
$$

of the form

$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    \mathbf{B} Fivebrane
    \\
    \downarrow
    \\
    \mathbf{B} String &\stackrel{\tfrac{1}{6}\mathbf{p}_2}{\to}& \mathbf{B}^7 U(1) 
    \\
    \downarrow
    \\
    \mathbf{B} Spin &\stackrel{\tfrac{1}{2}\mathbf{p}_1}{\to}& \mathbf{B}^3 U(1) 
    \\
    \downarrow
    \\
    \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    \\
    \downarrow
    \\
    \mathbf{B} O &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B} \mathbb{Z}_2
    \\
    \downarrow
    \\
    \mathbf{B} GL
  }
  \,.
$$

where 

* $\mathbf{B}^{n+1} U(1)$ is the [[delooping]] of the smooth [[circle n-group]], the smooth moduli $(n+1)$-stack of smooth [[circle n-bundle with connection|circle n-bundles]];

* $\mathbf{B} String$ is the [[delooping]] of the [[smooth string 2-group]], the moduli 2-stack of smooth $String$-[[principal 2-bundles]]

* $\mathbf{B}Fivebrane$ is the delooping of the [[smooth fivebrane 6-group]], the smooth moduli 6-stack of smooth fivebrane-[[principal infinity-bundle|principal 6-bundles]].



#### Differential refinement


**Theorem** 


$$
  \array{
    \vdots
    \\
    \downarrow
    \\
    \mathbf{B} Fivebrane_{conn}
    \\
    \downarrow
    \\
    \mathbf{B} String_{conn} &\stackrel{\tfrac{1}{6}\hat \mathbf{p}_2}{\to}& \mathbf{B}^7 U(1)_{conn} 
    \\
    \downarrow
    \\
    \mathbf{B} Spin_{conn} &\stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}& \mathbf{B}^3 U(1)_{conn} 
    \\
    \downarrow
    \\
    \mathbf{B} S O_{conn} &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
    \\
    \downarrow
    \\
    \mathbf{B} O_{conn} &\stackrel{\mathbf{w}_1}{\to}& \mathbf{B} \mathbb{Z}_2
    \\
    \downarrow^{}
    \\
    \mathbf{B} GL_{conn}
  }
  \,.
$$

#### Twisted differential String-structure -- Green-Schwarz mechanism

(...)


#### Twisted differential Fivebrane structure -- dual Green-Schwarz mechanism

(...)



### Spin<sup>c</sup>-, String<sup>c</sup>-, Fivebrane<sup>c</sup>-structures 
 {#TwistedK}


The above Whitehead tower of $\mathbf{B}O$ has a stage-wise unitary twisting. In the first stage this is given by the familiar [[spin^c]]-group: instead of being the [[delooping]] of the [[homotopy fiber]] of the [[second Stiefel-Whitney class]] $w_2$, this is the [[homotopy pullback|homotopy fiber product]] of $w_2$ with the universal [[first Chern class]] $\mathbf{c}_1$. 

Analogous unitary twists exists for the [[string 2-group]] and the [[fivebrane 6-group]].



#### Twisted $(Spin^c)^{\mathbf{dd}}$-structures and twisted K-theory on D-branes

$$
  \mathbf{B}U \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} U(n)
$$

$$
  \mathbf{B} PU \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} PU(n)
$$

**Proposition** For $X$ a [[compact topological space|compact]] [[smooth manifold]]

$$
  \mathbf{H}(X, \mathbf{B}U)
  \simeq
  \underset{\rightarrow_n}{\lim} \mathbf{H}(X, \mathbf{B} U(n))
  \,.
$$


$$
  \array{
     \mathbf{B}U &\to& \mathbf{B} P U
     \\
     && \downarrow^{\mathrlap{dd}}
     \\
     && \mathbf{B}^2 U(1)
  }
$$

(...)


$$
  \array{
     \mathbf{B} Spin^{\mathbf{dd}} &\to& \mathbf{B} (P U \times SO)
     \\
     && \downarrow^{\mathrlap{dd} - \mathbf{W}_3}
     \\
     && \mathbf{B}^2 U(1)
  }
$$

(...)

#### Twisted $String^{2\mathbf{a}}$-structures on M5-branes

(...)


### Higher orientifold structures 
 {#HigherOrientifold}


#### Orientifolds

(...)

#### Ho&rcaron;ava-Witten compactifications

(...)

(...)


## General theory
 {#GeneralTheory}


We survey here some key aspects of a general theory of geometric twisted differential cohomology, following ([DCCT](#Schreiber)), in which all of the following examples find their formal home. This is meant as a reference. The reader should **skip** to the discussion of _[Examples](#Examples)_ below on first reading, and only come back here if and when need arises.

We base the formulation of [[physics]]/[[string theory]] on the [[foundations]] of [[homotopy type theory|homotopy-type theory]], [[categorical semantics|interpreted]] in [[(∞,1)-topos theory]]. This provides a nicely natural and expressive language for the purpose of twisted smooth cohomology in string theory.



| [[axioms]]  | [[syntax]] | [[semantics]] | typical [[models]] | expressiveness |
|--|---|---|---|---|
| bare minimum | [[homotopy type theory]] | [[(∞,1)-topos theory]] | [[∞Grpd]] | [[cohomology]], [[principal infinity-bundle|principal bundles]], [[twisted cohomology]], [[associated infinity-bundle|associated]] and [[twisted bundles]] |
| +[[local (∞,1)-topos|locality]]+[[locally infinity-connected (infinity,1)-topos|∞-connectedness]] | [[cohesive homotopy type theory]] | [[cohesive (∞,1)-topos]] |  [[Smooth∞Grpd]], [[Super∞Grpd]] |  [[geometric realization]], [[differential cohomology]], [[infinity-Chern-Weil theory|Chern-Weil theory]] [[schreiber:infinity-Chern-Simons theory|Chern-Simons theory]], [[schreiber:infinity-geometric prequantization|geometric quantization]] |
| +[[cohesive (infinity,1)-topos -- infinitesimal cohesion|infinitesimals]] | differential homotopy type theory | [[cohesive (infinity,1)-topos -- infinitesimal cohesion|differential (∞,1)-topos]] | [[SynthDiff∞Grpd]] | [[de Rham space]], [[jet bundle]], [[étale infinity-groupoid|étale groupoid]], [[orbifold]]  |






### Homotopy-type theory


#### Cohomology

(...)


[[looping and delooping]]

$$
  Grp(\mathbf{H})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}_{\geq 1}^{*/}
$$

$$
  H^n(X,A) \coloneqq \pi_0 \mathbf{H}(X, \mathbf{B}^n A)
$$


#### Principal bundles

(...)


$g : X \to \mathbf{B}G$

$$
  G \coloneqq (*_{\mathbf{B}G} \simeq *_{\mathbf{B}G}) : Type
$$

$$
  P \coloneqq \sum_{x : X} ( *_{\mathbf{B}G}  \simeq g(x)  ) : Type
$$

$$
  \begin{aligned}
    & \rho : P \times G \to G
    \\
    & \;\;\coloneqq
    (( x : X; p : (* \simeq g(x))), g : (* \simeq *) )
    \mapsto
    (x : X; p)
  \end{aligned}
$$

#### Twisted cohomology
 {#TwistedCohomology}


+-- {: .num_remark }
###### Remark


Let 

$$
  \array{
    F &\to& A
    \\
    && \downarrow^{\mathrlap{p}}
    \\
    && B 
  }
$$

be a universal coefficient $\infty$-bundle
and let $\phi : X \to B$ be a twist. Then the $\phi$-twisted $F$-cohomology is equivalent to the sections of the [[homotopy pullback|pullback]]-bundle $\phi^* A$, in fact there is an [[equivalence in an (infinity,1)-category|equivalence]] of [[cocycles]]

$$
  [X,A]_{(\phi, \mathbf{c})} \simeq \Gamma_X(\phi^* A)
  \,.
$$


Equivalently, in the [[syntax]] of [[homotopy type theory]], this is the statement

$$
  b : B \vdash (X(b) \to A(b)) : Type
  \;\;
  =
  \;\;
  b : B \vdash \prod_{x : X(b)} A(\phi(x)) : Type
  \,.
$$

While on the right this expresses the collection of the pullback bundle, the left hand side expresses explicitly a $B$-parameterized collection of cocycles $X(b) \to A(b)$.

=--

#### Associated and twisted bundles

(...)

### Cohesive homotopy-type theory



#### Geometric realization 

#### Differential cohomology

#### Chern-Weil theory


### Differential homotopy-type theory

#### de Rham stack

(...)

#### &Eacute;tale stacks / orbifolds 

(...)


## References

The string-theoretic aspects of the above discussion owe a lot to [[Hisham Sati]], who has pointed out the appearance of twisted structures in string theory notably in 

* _[[Geometric and topological structures related to M-branes]]_ , part I ([arXiv:1001.5020](http://arXiv.org/abs/1001.5020)), part _II: Twisted $String$ and $String^c$ structures_ ([arXiv:1007.5419](http://arxiv/1007.5419)); part _III: Twisted higher structures_ ([arXiv:1008.1755](http://arxiv.org/abs/1008.1755))

The smooth and differential refinements of these structures have been jointly developed in articles such as

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_

A general theory of smooth homotopy-type theory is laid out in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_
 {#Schreiber}

For references on the example of [[twisted K-theory|twisted]] and [[differential K-theory|differential]] [[K-theory]], as well as on [[orientifolds]], see there.

