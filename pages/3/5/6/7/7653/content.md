
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindestalx="0"}
### Context
#### Cohomology
+-- {: .hide}
[[!include cohomology - contents]]
=--
#### String theory
+-- {: .hide}
[[!include string theory - contents]]
=--
=--
=--

This entry contains lecture notes on 

* [**A)**](#Examples) [[twisted cohomology|twisted]] smooth [[cohomology]] structures appearing in [[string theory]]/[[M-theory]];

* [**B)**](#LocalPrequantumFieldTheory) the corresponding [[sigma model]] [[local prequantum field theory]]

formulated in [[cohesion|cohesive]] [[higher differential geometry]].


#Contents#
* table of contents
{:toc}




## **A)** Examples of twisted smooth cohomology in string theory
 {#Examples}

> This section originates in notes prepared along with a lecture series ([Schreiber ESI 2012](#SchreiberLect)) at the Erwin-Schr&#246;dinger institute in 2012.

This section discusses four classes of examples of twisted smooth cohomology in string theory

1. _[Geometric structure (generalized, exceptional)](#VielbeinFields)_

1. _[Spin-, String-, and Fivebrane structure](#SpinStringFivebraneStructures)

1. _[$Spin^c$-, $String^c$-, $Fivebrane^c$-structure](#TwistedK)_

1. _[Higher orientifold structure](#HigherOrientifold)_ 


### Idea

The [[background gauge fields]] on [[spacetime]] appearing in [[string theory]] are mathematically described by [[cocycles]] in [[twisted cohomology|twisted]] and [[differential cohomology|differential]] refinements of [[smooth infinity-groupoid|smooth]] [[cohomology]]. A famous example is the [[twisted K-theory]] that describes the [[B-field]]-twisted [[Yang-Mills fields]] over [[D-branes]] in [[type II string theory]]. But there are many more classes of examples of twisted / smooth / differential cohomology appearing throughout string theory.

This page provides a survey of and introduction to such examples, organized along a _[Table of twists](#TableOfTwists)_, that indicates how all of these are instances a single pattern. For further reading and more details see the list of _[references](#References)_ below.

We start with an introduction to the general notion of twisted smooth cohomology by way of the simple but instructive class of examples of

* **I)** _[Geometric structure (generalized, exceptional)](#VielbeinFields)_,

via [[reduction of structure groups]], which, simple as it is, serves as a blueprint for all of the examples to follow, and which we use to introduce the general machinery. It also serves to highlight the need and use of _smooth_ cohomology in addition to both [[generalized (Eilenberg-Steenrod) cohomology|ordinary topological/homotopical]] as well as [[differential cohomology]].

(The mathematically inclined reader wishing to see a more formal development of the general theory behind the discussion here should look at the section _[General theory](#GeneralTheory)_ below for pointers.)

Then we proceed in direct analogy, but now with ordinary [[gauge fields]] generalized to the genuine [[higher gauge fields]] of [[string theory]], and discuss aspects of the main classes of examples of twisted smooth cohomology appearing there. First we indicate how higher spin structures as such lead to higher smooth homotopy theory:

* II) _[Spin-, String-, and Fivebrane structure](#SpinStringFivebraneStructures)_.

Then we roughly indicate the relation between higher gauge fields and [[quantum anomalies]]:

* Interlude) _[Anomaly line bundle on smooth moduli stacks of fields](#Anomalies)_.

Finally we put the pieces together and scan through various situations appearing in string theory with their anomaly structure and discuss the smooth moduli $\infty$-stacks of anomaly-free field configurations / of twisted smooth cocycles:

* III) _[$Spin^c$-, $String^c$-, and $Fivebrane^c$-structure](#TwistedK)_ .

There are various further examples. As an outlook we indicate aspects of

* IV) _[Higher orientifold structure](#HigherOrientifold)_.


### Overview: The Table of Twists
 {#TableOfTwists} 

The following sections discuss classes of examples of [[twisted differential c-structures|twisted smooth structures]] in [[string theory]]. All these examples are governed by the the same general pattern of [[twisted cohomology]] refined to [[smooth infinity-groupoid|smooth cohomology]] (a gentle explanation/example follows [in a moment](#VielbeinFields), for formal details see further [below](#TwistedCohomology)). They are specified by a _universal local coefficient bundle_

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

which exists in a context of _[[cohesive homotopy type theory|geometric homotopy types]]_: an [[(∞,1)-topos|higher topos]] to be denoted $\mathbf{H} \coloneqq $ [[Smooth∞Grpd]], of [[smooth ∞-groupoids]]/smooth [[∞-stacks]]. 

Here

* $G$ is a [[smooth ∞-group]] -- a higher [[gauge group]];

* $\mathbf{B}G$ is the [[smooth ∞-groupoid|smooth]] [[moduli ∞-stack]] of $G$-[[principal ∞-bundles]];

* $F$ is a coefficient object equipped with a $G$-[[action]];

* $E \to \mathbf{B}G$ is the [[associated ∞-bundle|associated bundle]] to the $G$-[[universal principal ∞-bundle]] over the [[moduli ∞-stack]] $\mathbf{B}G$ of $G$-[[principal ∞-bundles]].

Given such, and given a [[spacetime]]/[[target space]] $X$, we have:

* a morphism $\phi : X \to \mathbf{B}G$ determines a _twisting bundle_ or _twisting [[background gauge field]]_ on $X$;

* a lift $\hat \phi$ in 

  $$
    \array{
      X &&\stackrel{\hat \phi}{\to}&& E
      \\
      & {}_{\mathllap{\phi}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{c}}}
      \\
      && \mathbf{B}G
    }
  $$

  is a $\phi$-[[twisted infinity-bundle|twisted bundle]], or $\phi$-twisted background gauge field.

The following table lists examples of such local coefficient bundles and tabulates the correspondings twisting fields and twisted fields. This is to be read as an extended table of contents. Explanations are in the sections to follow.


| class of examples | universal local coefficient bundle | twisting bundle | twisting field | twisted bundle | twisted field |
|---|---|---|---|---|---|
| **[0)](#GeneralTheory)** [[twisted differential c-structure|general pattern]] | | | | | |
| | $\array{ F &\to& E  \\ && \downarrow^{\mathrlap{\mathbf{c}}} \\ && \mathbf{B}G }$ | $G$-[[principal infinity-bundle|principal bundle]] | $G$-[[higher gauge field|gauge field]] [[instanton]]-sector | [[section]] of $\rho$-[[associated infinity-bundle|associated]] $F$-bundle | twisted $\Omega F$-[[gauge field]] [[instanton]] sector |
| | $\array{ \flat \mathbf{B}^n U(1) &\to& \mathbf{B}^n U(1) \\ && \downarrow^{\mathbf{curv}} \\ && \flat_{dR} \mathbf{B}^{n+1} U(1) }$ | [[de Rham cohomology|de Rham]] [[hypercohomology]] |  | [[circle n-bundle with connection]]  | [[higher gauge field|higher abelian gauge field]] |
| | $\array{ F_{conn} &\to& E_{conn}  \\ && \downarrow^{\mathrlap{\hat \mathbf{c}}} \\ && \mathbf{B}G_{conn} }$ | $G$-[[connection on an infinity-bundle|connection]] | $G$-[[higher gauge field|gauge field]]  | [[section]] of $\rho$-[[associated infinity-bundle|associated]] $F$-bundle | twisted $\Omega F$-[[gauge field]]|
| **[I)](#VielbeinFields)** [[reduction of structure group]]/[[G-structure|geometric structure]] | | | | | |
| | $\array{ GL(n)/O(n) &\to& \mathbf{B} O(n) \\ && \downarrow \\ && \mathbf{B} GL(n) }$ | [[manifold]] structure / [[tangent bundle]] |  | [[vielbein]] | [[gravity]] |
| | $\array{ GL(n)/O(n) &\to& \mathbf{B} O(n)_{conn} \\ && \downarrow \\ && \mathbf{B} GL(n)_{conn} }$ | [[affine connection]] |   | [[spin connection]] | [[gravity]] |
| | $\array{ O(2d,2d)/SU(d,d) &\to& \mathbf{B} SU(d,d) \\ && \downarrow  \\ && \mathbf{B} O(2d,2d) }$ | [[generalized tangent bundle]] | |  | [[generalized Calabi-Yau manifolds]] |
| | $\array{ O(n)\backslash O(n,n)/O(n) &\to& \mathbf{B} O(n) \times O(n) \\ && \downarrow \\ && \mathbf{B} O(n,n) }$ | [[generalized  tangent bundle]] |  | [[type II geometry]] | DFT [[type II supergravity]] | 
| | $\array{ SU(3)\backslash O(6,6) / SU(3) &\to& \mathbf{B} SU(3) \\ && \downarrow \\ && \mathbf{B} O(6,6) }$ | [[generalized tangent bundle]]  | | [[type II geometry]] | $d = 6$, $N=1$  [[type II supergravity]] [[Kaluza-Klein mechanism|comactifications]] | 
| |  $\array{ E_{7(7)}/SU(7) &\to& \mathbf{B} SU(7) \\ && \downarrow \\ && \mathbf{B}E_{7(7)} }$ | [[exceptional tangent bundle]] | [[E7]]-[U-duality](supergravity#UDuality) moduli ([[split real form]]) |  | $d = 7$, $N=1$ [[11-dimensional supergravity|11d supergravity]] [[Kaluza-Klein mechanism|compactifications]] |
| | $\array{ E_{n(n)}/H_n &\to& \mathbf{B}H_n \\ && \downarrow \\ && \mathbf{B}E_{n(n)} }$ | [[exceptional tangent bundle]]  | [U-duality](supergravity#UDuality) moduli | [[U-duality]] [[exceptional generalized geometry]] | [[Kaluza-Klein mechanism|compactification]] of [[11-dimensional supergravity|11d supergravity]] to $d = 11-n$ |
| | $\array{ \mathbf{B} U &\to& \mathbf{B} P U \\ && \downarrow^{\mathbf{dd}} \\ && \mathbf{B}^2 U(1) }$ | [[circle n-bundle with connection|circle 2-bundle]]/$U(1)$-[[bundle gerbe]] | [[B-field]] | [[twisted bundle|twisted unitary bundle]] | [[Yang-Mills field]] |
| | $\array{ \mathbf{B}String(E_8) &\to& \mathbf{B} E_8 \\ && \downarrow^{\mathrlap{\mathbf{a}}} \\ && \mathbf{B}^3 U(1)} $ | [[circle n-bundle with connection|circle 3-bundle]] / [[bundle 2-gerbe]] | [[supergravity C-field]] |  | [[twisted differential string structure|twisted String(E8)]]-2-form gauge field  |
| **[II)](#SpinStringFivebraneStructures)** [higher spin structures](spin+structure#Higher) | | | | | |
| | $\array{ \mathbf{B} Spin &\to& \mathbf{B} SO \\ && \downarrow^{\mathrlap{\mathbf{w}_2}} \\ && \mathbf{B}^2 \mathbb{Z}_2 }$ | [[second Stiefel-Whitney class]] | | [[twisted spin structure]] |  |
| | $\array{ \mathbf{B}String &\to& \mathbf{B} Spin  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\mathbf{p}_1}} \\ && \mathbf{B}^3 U(1)  }$ | [[circle n-bundle with connection|circle 3-bundle]]/$U(1)$-[[bundle 2-gerbe]] |  [[NS5-brane]] [[magnetic charge]] |  [[twisted differential string structure|twisted smooth string structure]] |  |
| | $\array{ \mathbf{B}String_{conn} &\to& \mathbf{B} Spin_{conn}  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\hat \mathbf{p}_1}} \\ && \mathbf{B}^3 U(1)_{conn}  }$ | [[circle n-bundle with connection|circle 3-bundle with connection]]| [[NS5-brane]] [[current|magnetic current]]  |  [[twisted differential string structure]] | [[Green-Schwarz mechanism]] [[gravity]]+[[B-field]] |
| | $\array{ \mathbf{B}Fivebrane &\to& \mathbf{B} String  \\ && \downarrow^{\mathrlap{\tfrac{1}{6}\mathbf{p}_2}} \\ && \mathbf{B}^7 U(1)  }$ | [[circle n-bundle with connection|circle 7-bundle]]| [[string]] [[electric charge]]  | [[twisted differential fivebrane structure|twisted smooth fivebrane structure]] |  |
| | $\array{ \mathbf{B}Fivebrane_{conn} &\to& \mathbf{B} String_{conn}  \\ && \downarrow^{\mathrlap{\tfrac{1}{6}\hat \mathbf{p}_2}} \\ && \mathbf{B}^7 U(1)_{conn}  }$ | [[circle n-bundle with connection|circle 7-bundle with connection]]| [[string]] [[current|electric current]] | [[twisted differential fivebrane structure]] | dual [[Green-Schwarz mechanism]] [[gravity]]+[[B6-field]] |
| **[III)](#TwistedK)** [higher spin^c-structures](spin^c+structure#Higher) | | | | | |
| | $\array{ \mathbf{B}Spin^c &\to& \mathbf{B} (SO \times U(1))  \\ && \downarrow^{\mathrlap{ w_2 - c_1}} \\ && \mathbf{B}^2 \mathbb{Z}_2  }$ |  |   | [[twisted spin^c structure]] |  |
|  | $\array{ \mathbf{B}(Spin^c)^{\mathbf{dd}} &\to& \mathbf{B} (PU \times SO) \\ && \downarrow^{\mathrlap{ \mathbf{dd} - \mathbf{W}_3 }} \\ && \mathbf{B}^2 U(1) }$ | [[circle n-bundle with connection|circle 2-bundle]] |  [[B-field]] | [[twisted spin^c structure]]  | [[Freed-Witten anomaly]] for [[type II superstring]] on [[D-brane]]  |
| | $\array{ \mathbf{B}String^{\mathbf{a}} &\to& \mathbf{B} Spin \times E_8  \\ && \downarrow^{\mathrlap{\tfrac{1}{2}\mathbf{p}_1 - 2 \mathbf{a}}} \\ && \mathbf{B}^3 U(1)  }$ | [[circle n-bundle with connection|circle 3-bundle]]/$U(1)$-[[bundle 2-gerbe]] |  [[supergravity C-field]] |  [[twisted differential string structure|twisted smooth string^c structure]] |  [[gravity]]+[[B-field]]+[[E8]]-[[gauge field]] |
| **[IV)](#HigherOrientifold)** Giraud-[[∞-gerbes]] | | | | | |
| | $\array{ \mathbf{B}^2 U(1) &\to& \mathbf{B}Aut(\mathbf{B}U(1)) \\ && \downarrow \\ && \mathbf{B}\mathbb{Z}_2 }$ | [[double cover]] |  | [[Jandl gerbe]] | [[orientifold]] [[B-field]] | 
| | $\array{ \mathbf{B}^3 U(1) &\to& \mathbf{B}Aut(\mathbf{B}^2 U(1)) \\ && \downarrow \\ && \mathbf{B}\mathbb{Z}_2 }$ | [[double cover]] |  | | [[Hořava-Witten theory|Hořava-Witten orientifold]] | 
 


### **I)** Geometric structure (generalized, exceptional)
 {#VielbeinFields}

The ordinary notion of _[[vielbein]]_ in [[differential geometry]] (equivalently: _[[soldering form]]_ or _[[orthogonal structure]]_) turns out to be a simple special case of the general notion of twisted smooth cohomology that we are concerned with here. Viewed from this perspective it already contains the seeds of all of the more sophisticated examples to be considered below. Therefore we discuss this case here as a warmup, such as to introduce the general theory by way of example. 

#### The class of the tangent bundle
 {#ClassOfTheTangentBundle}

Let $X$ be a [[smooth manifold]] of [[dimension]] $n$. 

By definition this means that there is an [[atlas]] 

$$
  \{ \mathbb{R}^n \underoverset{\simeq}{\phi_i^{-1}}{\to} U_i \hookrightarrow X\}
$$ 

of [[coordinate charts]]. On each overlap $U_i \cap U_j$ of two charts, the [[partial derivatives]] of the corresponding [[coordinate transformations]]

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

(here and in the following sums over an index appearing upstairs and downstairs are explicit)

hence the equation

$$
  \lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}
$$

in the [[group]] $C^\infty(U_i \cap U_j \cap U_k, GL(n))$ of smooth $GL(n)$-valued functions on the chart overlaps.

This is the _[[cocycle]] condition_ for a smooth [[Cech cohomology|Cech cocycle]] in degree 1 with coefficients in $GL(n)$ (precisely: with coefficients in the [[sheaf]] of [[smooth functions]] with values in $GL(n)$ ). We write

$$
  [(\lambda_{i j})] \in H^1_{smooth}(X, GL_n)
  \,.
$$

It is useful to reformulate this statement in the language of [[Lie groupoids]]/[[differentiable stacks]]. 

* $X$ itself is a Lie groupoid $(X \stackrel{\to}{\to} X)$ with trivial morphism structure;

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
    \,,
  $$

  whose objects are the points in the atlas, with morphisms identifying lifts of a point in $X$ to different charts of the atlas;

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

* the left morphism is [[stalk]]-wisse (around small enough [[neighbourhoods]] of each point) an [[equivalence of groupoids]] (we make this more precise in a moment);

* the horizontal functor has as components the functions $\lambda_{i j}$ and its functoriality is the cocycle condition $\lambda_{i j} \cdot \lambda_{j k} = \lambda_{i k}$.

A [[natural transformation|transformation]] of smooth functors $\lambda_1 \Rightarrow \lambda_2 : C(\{U_i\}) \to \mathbf{B} GL(n)$ is precisely a [[coboundary]] between two such cocycles.

#### Smooth moduli stacks
 {#SmoothModuliStacks}

We want to think of such a diagram as being directly a morphism of [[smooth infinity-groupoid|smooth groupoids]]


$$
  T X \; : \; X \to \mathbf{B} GL(n) \;\; \in \mathbf{H}
$$

in a suitable context $\mathbf{H}$,
such that this may be regarded as a smooth refinement of the underlying [[homotopy]] class of a  map into the [[classifying space]] $B GL(n)$

$$
  X \to B GL(n) \in Top  
  \,.
$$

Evidently, for this we need to turn the [[stalk]]-wise [[homotopy equivalence]] $C(\{U_i\}) \to X$ into an actual [[homotopy equivalence]]. This is a [[nonabelian cohomology|non-abelian/non-stable]] generalization of what happens in the construction of a [[derived category]], for instance in the theory of [[topological string|topological branes]].

To make this precise, first notice that every Lie groupoid $A = (A_1 \stackrel{\to}{\to} A_0)$ yields on each smooth manifold $U$ a groupoid of maps from $U$ into $A$

$$
  A : U \mapsto (C^\infty(U,A_1) \stackrel{\to}{\to} C^\infty(U,A_0))
  \,,
$$

the groupoid of _smooth $U$-families_ of elements of $A$.

Moreover, for every smooth function $U_1 \to U_2$ there is an evident restriction map $A(U_2) \to A(U_1)$ and so this yields a [[presheaf]] of groupoids, hence a functor $A \in Func(SmthMfd^{op}, Grpd)$. The [[Yoneda lemma]] says that thinking of Lie groupoids as presheaves of ordinary groupoids this way does not lose information --- and [[topos theory]] say that it is generally a good idea.

Let therefore

$$
  \mathbf{H} \coloneqq Func(SmthMfd^{op}, Grpd)[\{stalkwise\, h.e\}^{-1}]
$$

be the [[simplicial localization|localization]] of groupoid-valued presheaves that universally turns [[stalk]]wise [[homotopy equivalences]] into actual homotopy equivalences: if a [[natural transformation]] $\eta : A \to B$ in $Func(SmthMfd^{op}, Grpd)$ is such that for each $U \in $ [[SmthMfd]] and each $x \in U$ there is a [[neighbourhood]] $U_x \subset U$ of $x$ such that $\eta(U_x) : A(U_x) \to B(U_x)$ is an [[equivalence of groupoids]], then $\eta$ has a [[homotopy inverse]] in $\mathbf{H}$.

We call this $\mathbf{H}$ the _[[(2,1)-topos]]_ of _[[smooth infinity-groupoid|smooth groupoids]]_ or of _[[smooth infinity-groupoid|smooth stacks]]_.

Discussed there are tools for describing $\mathbf{H}$ concretely. For the moment we only need to know that

1. the [[Cech nerve]] projection $C(\{U_i\}) \to X$ of every [[open cover]] has a [[homotopy inverse]] in $\mathbf{H}$, as already used;

1. if the cover is _[[good open cover|good]]_ and $G$ is a Lie group, then every morphism $X \to \mathbf{B}G$ in $\mathbf{H}$ is presented by a [[anafunctor|zig-zag]] of the form $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \to \mathbf{B}G$.

Then we have

1. a morphism $X \to \mathbf{B} GL(n)$ in $\mathbf{H}$ is precisely a smooth real vector bundle on $X$;

1. a homotopy between two such morphisms in $\mathbf{H}$ is precisely a smooth $GL(n)$-[[gauge transformation]] between the two vector bundles.

Therefore $\mathbf{B}GL(n)$ regarded as an object of $\mathbf{H}$ is the _[[moduli stack]]_ of real vector bundles.

Of course there is a "smaller" Lie groupoid that also classifies real vector bundles, but whose gauge transformations are restricted to be [[orthogonal group]]-valued functions. Passing to this "smaller" Lie groupoid is what the choice of vielbein accomplishes, to which we now turn.


#### Reduction of the structure group
 {#ReductionOfTheStructureGroup}


Consider the defining inclusion of the [[orthogonal group]] into the [[general linear group]]

$$
  O(n) \hookrightarrow GL(n)
  \,.
$$

We may understand this inclusion geometrically in terms of the canonical [[metric]] on $\mathbb{R}^n$. We may also understand it purely [[Lie theory|Lie theoretically]] as the
inclusion of the [[maximal compact subgroup]] of $GL(n)$. This makes it manifest that the inclusion is trivial at the level of [[homotopy theory]] (it is a [[homotopy equivalence]] of the underlying [[topological spaces]]) and hence _only_ encodes geometric information.


The inclusion induces a corresponding inclusion ([[truncated object of an (infinity,1)-category|0-truncated morphism]]) of moduli stacks

$$
  \mathbf{Orth} : \mathbf{B} O(n) \to \mathbf{B} GL(n)
  \;\;\;
  \in \mathbf{H}
$$

simply by regarding it as a morphism of Lie groupoids

$$
  (O(n) \stackrel{\to}{\to} * )
  \to 
  (GL(n) \stackrel{\to}{\to} * )
$$

in the evident way.

Now we can say what a [[Riemannian metric]]/[[orthogonal structure]] on $X$ is: 

A choice of [[orthogonal structure]] on $T X$ is a factorization of the above $GL(n)$-valued cocycle $\lambda$ through $\mathbf{Orth}$, up to a smooth [[homotopy]] $E$ in $\mathbf{H}$, hence a [[diagram]]

$$
  \array{
     X &&\stackrel{h}{\to}&& \mathbf{B} O(n)
     \\
     & {}_{\mathllap{\lambda}}\searrow &\swArrow_{\mathrlap{E^{-1}}}& \swarrow_{\mathrlap{\mathbf{Orth}}}
     \\
     && \mathbf{B}GL(n)
  }
$$

in $\mathbf{H}$.

This consists of two pieces of data

* the morphism $h$ is (by the same reasoning as for $\lambda$ above) a $O(n)$-valued 1-cocycle -- a collection of _orthogonal transition functions_ --  hence on each overlap of coordinate patches a smooth function
  
  $$
    ((h_{i j}){}^a{}_b) : U_i \cap U_j \to O(n)
  $$
  
  such that 

  $$
    h_{i j} \cdot h_{j k} = h_{i k}
  $$

  on all triple overlaps of coordinate charts $U_i \cap U_j \cap U_k$;

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
The component $E$ is the corresponding **[[vielbein]]**. It exhibits an [[isomorphism]] 

$$
  E : T X \stackrel{\simeq}{\to} V
$$

between a [[vector bundle]] $V \to X$ with [[structure group]] explicitly being the [[orthogonal group]], and the [[tangent bundle]] itself, hence it exhibits the [[reduction of the structure group]] of $T X$ from $GL(n)$ to $O(n)$.

#### Moduli space of orthogonal structures: twisted cohomology
 {#ModuliSpaceOfOrhtogonalStructures}

We consider now the space of choices of vielbein fields on a given tangent bundle, hence the _[[moduli space]]_ or _[[moduli stack]]_ of [[orthogonal structures]]/[[Riemannian metrics]] on $X$.

This is usefully discussed in terms of the [[homotopy fiber]] of the morphism $\mathbf{c} : \mathbf{B}O(n) \to \mathbf{B}GL(n)$. One finds that the homotopy fiber  is the [[coset]] $O(n) \backslash GL(n)$.

This means that there is a diagram

$$
  \array{
     GL(n)/O(n) &\to& \mathbf{B}O(n)
     \\
     \downarrow &\swArrow_{\simeq}& \downarrow
     \\
     * &\to& \mathbf{B} GL(n)
  }
$$

in $\mathbf{H}$, and that $GL(n)/O(n)$ is [[universal property|universal]] with the property of sitting in such a diagram.

We may think of this _[[fiber sequence]]_ as being a bundle in $\mathbf{H}$ over the [[moduli stack]] $\mathbf{B}GL(n)$ with typical fiber $GL(n)/O(n)$. As such, it is  the smooth [[associated infinity-bundle|associated bundle]] to the smooth [[universal principal bundle|universal GL(n)-bundle]] induced by the canonical [[action]] of $GL(n)$ on $O(n)\backslash GL(n)$.

One basic properties of homotopy pullbacks is that they are preserved by forming [[derived hom-space|derived hom-spaces]] $\mathbf{H}(X,-)$ out of any other object $X$. This means that also

$$
  \array{
     C^\infty(X,GL(n)/O(n)) &\to& \mathbf{H}(X,\mathbf{B}O(n))
     &\to&
     \mathbf{H}(X, \mathbf{B}GL(n))
  }
$$

is a [[fiber sequence]]. This in turn says that orthogonal structures on $X$ such that the underlying tangent bundle is trivializable, are given by smooth functions into $GL(n)/O(n)$.

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

the tangent bundle _twists_ the functions $X \to GL(n)/O(n)$. If we think of an ordinary such function as a cocycle in degree-0 cohomology, then this means that a vielbein is a cocycle in $T X$-_[[twisted cohomology]]_ relative to the _twisting local coefficient bundle_ $\mathbf{c}$.

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

The above says that the space of vielbein fields is the [[cohomology]] of $T X$ in the [[over-(infinity,1)-topos|slice (2,1)-topos]] $\mathbf{H}_{/\mathbf{B}GL(n)}$ with coefficients in $\mathbf{Orth} : \mathbf{B}O \to \mathbf{B}GL(n)$

$$
  \mathbf{Orth} Struc_{TX}(X) 
  \coloneqq
  \mathbf{Orth}(T X)
   \coloneqq
  \mathbf{H}_{/\mathbf{B}GL(n)}(T X, \mathbf{Orth})
  \,.
$$

But also this space of choices of vielbein fields has a smooth structure, it is itself a smooth [[moduli stack]]. This is obtained by forming the [[internal hom]] in the slice over $\mathbf{B}GL(n)$ of the [[locally cartesian closed (infinity,1)-category|locally cartesian closed (2,1)-category]] $\mathbf{H}$.

$$
  \mathbf{OrthStruc}_{T X}(X)
  \coloneqq
  [T X, \mathbf{Orth}]_{\mathbf{B}GL(n)}
  \,.
$$

For more on this see also the discussion at _[[general covariance]]_.

#### Differential refinement: Spin connection
 {#SpinConnection}

We may further refine this discussion to [[differential cohomology]] to get genuine _differential_ $T X$-twisted $\mathbf{c}$-structures. 

Recall that the moduli stack $\mathbf{B}G$ is presented in $\mathbf{H}$ by the presheaf of groupoids

$$
  \mathbf{B} G : U \mapsto (C^\infty(U,G) \stackrel{\to}{\to} *)
  \,.
$$

We may think of this for each $U$ as being the groupoid of $G$-gauge transformations acting on the trivial $G$-bundle over $U$. A [[connection on a bundle|connection]] on the trivial $G$-bundle is a [[Lie algebra]] valued form $A \in \Omega^1(U, \mathfrak{g})$. Accordingly, the presheaf of groupoids

$$
  \mathbf{B}G_{conn} : U \mapsto (C^\infty(U,G) \times \Omega^1(U, \mathfrak{g}) \stackrel{\to}{\to} \Omega^1(U, \mathfrak{g}) )
$$

is that of $G$-connections and gauge transformations between them: the _[[groupoid of Lie-algebra valued forms]]_ over $U$. As an object of $\mathbf{H} = $ [[smooth infinity-groupoid|SmoothGrpd]] this the [[moduli stack]] of $G$-[[connection on a bundle|connections]]:

$$
  \mathbf{H}(X, \mathbf{B}G_{conn})
  \simeq
  G Bund_\nabla(X)
  \,.
$$

The morphism $\mathbf{Orth}$ has an evident differential refinement to a morphism between such differentially refined moduli stacks

$$
  \mathbf{Orth}_{conn} : \mathbf{B}O(n)_{conn} \to \mathbf{B}GL(n)_{conn}
$$

by acting on the differential forms with the induced inclusion of the [[orthogonal Lie algebra]] into the [[general linear Lie algebra]] $\mathfrak{o}(n) \hookrightarrow \mathfrak{gl}(n)$.

The [[homotopy fiber]] of this differential refinement turns out to be the same moduli space as before

$$
  \array{
    GL(n)/ O(n) &\to& \mathbf{B} O(n)_{conn}
    \\
    && \downarrow^{\mathrlap{\mathbf{Orth}_{conn}}}
    \\
    && \mathbf{B} GL(n)_{conn}
  }
  \,,
$$

so that the moduli space of "differential vielbein fields" is the same as that of plain vielbein fields. But we nevertheless do gain differential information: consider an [[affine connection]] on the tangent bundle, which is now given by a morphism from $X$ to the moduli stack

$$
  \nabla_{T X} : X \to \mathbf{B}GL(n)
  \,.
$$

This is a $GL(n)$-[[principal connection]] which locally on an atlas is given by the [[Christoffel symbols]] 

$$
  \Gamma_i = ((\Gamma_i)_\mu{}{}^{\alpha}{}_\beta)
  \in 
  \Omega^1(U_i, \mathfrak{gl}(n))
  \,.
$$

A $\nabla_{T X}$-twisted differential cocycle is now a diagram

$$
  \array{
    X &&\stackrel{\nabla_{V}}{\to}&& \mathbf{B}O_{conn}
    \\
    & {}_{\mathllap{\nabla_{T X}}}\searrow 
     &\swArrow_{E^{-1}}& 
    \swarrow_{\hat {\mathbf{Orth}}}
    \\
    && \mathbf{B}GL(n)_{conn}
  }
  \,.
$$

In components over the atlas, $\nabla_V$ is a "[[spin connection]]" given by local 1-forms $\{\omega_i \in \Omega^1(U_i, \mathfrak{o}(n))\}$

$$
  \omega_i = E_i d_{dR} E_i^{-1} + E_i \Gamma E_i^{-1}
$$

and the vielbeing $E$ now exhibits on each chart $U_i$ the familiar relation between the components of the spin connection and the Christoffel-symbols:

$$
  \omega{}^a{}_b 
   = 
   E_i^a{}_\nu d_{dR} E_i^\nu{}_b
   +
   E_i^a{}_\nu \Gamma_i {}^\nu{}_\lambda E_i^\lambda{}_b
   \,.
$$

#### Pullback of orthogonal structures
 {#PullbackOfOrthogonalStructures}

It is a familiar fact that many fields in physics "naturally pull back". For instance a [[scalar field]] on a [[spacetime]] $X$ is a [[function]] $\phi : X \to \mathbb{C}$, and for $f : Y \to X$ any [[smooth function]] between spactimes, there is the corresponding pullback function/field $f^* \phi : Y \to \mathbb{C}$.

Similarly for $\phi : X \to \mathbf{B}G_{conn}$ a gauge field, as discussed above, it has naturally a pullback along $f$ given simply by forming the composite $f^* \phi : Y \stackrel{f}{\to} X \stackrel{\phi}{\to} \mathbf{B}G_{conn}$.

But the situation is a little different for _twisted_ fields such as orthogonal structures/Riemannian metrics. If we think of a Riemannian metric as given by a non-degenerate rank-2 [[tensor]] on $X$, then the problem is that, while its pullback along $f$ will always be a rank-2 tensor, it is not in general non-degenerate anymore -- unless $f$ is a [[local diffeomorphism]].

This is also nicely formulated in the language used above, in a way that has a useful generalization when we come to higher twisted structures below: since the metric is encoded not just in a plain morphism $h : X \to \mathbf{B}O$, but one that fits into a triangle

$$
  \array{
     X && \stackrel{h}{\to} && \mathbf{B} O
     \\
     & {}_{\mathllap{T X}}\searrow & \swArrow_{E}& \swarrow_{\mathrlap{orth}}
     \\
     && \mathbf{B} GL
  }
$$ 

a simple precomposition with just a morphism $f : Y \to X$ is not the right operation to send this triangle based on $X$ to one based on $Y$. 

But since this triangle is a morphism $(h,E) : T X \to \mathbf{orth}$ in the [[slice topos]] $\mathbf{H}_{/\mathbf{B}GL}$, it is clear that it _does_ pull back precisely along refinements of $f : Y \to X$ to a morphism in $\mathbf{H}_{/\mathbf{B}GL}$.

Such a refinement is a commuting triangle of the form

$$
  \array{
    Y &&\stackrel{f}{\to}&& X
    \\
    & {}_{\mathllap{T Y}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{T X}}
    \\
    && \mathbf{B} GL
  }
$$

in $\mathbf{H}$. But this is evidently the same as an isomorphism $T Y \simeq f^* T X$ between the tangent bundle of $Y$ and the pullback of the tangent bundle on $X$. And this exhibits $f$ as a [[local diffeomorphism]]. 

#### Generalized vielbein fields: type II geometry, generalized CY and U-duality

The above discussion of ordinary [[vielbein]] fields is just a special case of an analogous discussion for general [[reduction of structure groups]], giving rise to [[generalized vielbein]] fields. Many geometric structures in string theory arise in this way, as indicated in the [table of twists](#TableOfTwists).

As one more out of these examples, we discuss in the above language of twisted smooth cohomology how a _[[type II geometry]]_ of [[type II supergravity]] is the [[reduction of the structure group]] of the [[generalized tangent bundle]] along the inclusion $O(d) \times O(d) \to O(d,d)$.

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

This induces the corresponding morphism of 
[[smooth infinity-groupoid|smooth]] [[moduli stacks]], which we denote

$$
  \mathbf{TypeII}
  :
  \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
  \to 
  \mathbf{B} \mathrm{O}(d,d)  
  \,.
$$

Forming the  [[homotopy fiber]] now yields the local coefficient bundle 

$$
  \array{
     O(d) \backslash O(d,d) / O(d)
     &\to&
    \mathbf{B}(\mathrm{O}(d) \times \mathrm{O}(d))
    \\
    && \downarrow^{\mathrlap{\mathbf{TypeII}}}
    \\
    && \mathbf{B} \mathrm{O}(d,d)  	
  }
  \,,
$$

There is also a canonical embedding

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

Under this inclusion, the 
[[tangent bundle]] of a $d$-[[dimension|dimensional]] 
[[manifold]] $X$ defines an $\mathrm{O}(d,d)$-[[cocycle]]

$$
  T X \oplus T^* X
  :
  
    X 
     \stackrel{T X}{\to}
    \mathbf{B}\mathrm{GL}(d)  
      \stackrel{}{\to}
    \mathbf{B} \mathrm{O}(d,d) 
  \,.
$$

The [[vector bundle]] canonically associated to this composite cocycle may 
canonically be identified with
the [[direct sum]] vector bundle $T X \oplus T^* X$, and so we will
refer to this cocycle by these symbols, as indicated. 
This is also called the **[[generalized tangent bundle]]** of $X$.


Therefore we may canonically consider the groupoid of 
$T X \oplus T^* X$-twisted $\mathbf{TypeII}$-structures, 
according to the general notion of [[twisted differential c-structures]].


A **type II generalized vielbein** on a [[smooth manifold]] $X$ is a diagram

$$
  \array{
    X &&\stackrel{\widetilde(T X \oplus T^* X)}{\to}&& \mathbf{B}(O(n) \times O(n))
    \\
    & {}_{\mathllap{T X \oplus T^* X}}\searrow &\swArrow_{E}& \swarrow_{\mathrlap{\mathbf{TypeII}}}
    \\
    && \mathbf{B} O(n,n)
  }
$$

in $\mathbf{H}$, hence a cocycle in the smooth [[twisted cohomology]]

$$
  E 
   \in 
  \mathbf{TypeII}Struc(X)
  \coloneqq
  \mathbf{H}_{/\mathbf{B} O(n,n)}(T X \oplus T^* X, \mathbf{TypeII})
  \,.
$$


+-- {: .un_prop }
###### Proposition / Definition

  The [[groupoid]] $\mathbf{TypeII}\mathrm{Struc}(X)$
  is that of "generalized vielbein fields" on $X$, as considered for instance 
  around equation (2.24) of ([GMPW](type+II+geometry#GMPW))
  (there only locally, though).
  
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




### **II)** Spin-, String- and Fivebrane-structure
 {#SpinStringFivebraneStructures}

Above we have seen ([[pseudo-Riemannian metric|pseudo]]-)[[Riemannian metric|Riemannian structure]] given by lifts through the inclusion $\mathbf{B} O(n) \to \mathbf{B} GL(n)$. Now we consider further lifts, through the [[Whitehead tower]] of $\mathbf{B}O$. This encodes 
_[higher spin structures](spin+structure#Higher)_.

Where a _[[spin structure]]_ on [[spacetime]] is necessary to cancel a [[quantum anomaly]] of the [[spinning particle]]/[[superparticle]] [[sigma-model]], so the [[heterotic string|heterotic]] [[superstring]] requires, in the absence of a [[gauge field]], a "[higher spin structure](#spin+structure#Higher)", called a _[[string structure]]_.  Further up in dimension, _[[dual heterotic string theory]]_ in the absence of the gauge field involves a  _[[fivebrane structure]]_.

In the presence of a nontrivial [[gauge fields]], string structures are generalized to _[[twisted differential string structure|twisted string structure]]_, which in [[heterotic string theory]] are part of the _[[Green-Schwarz mechanism]]_. These we discuss [below](#TwistedK).


#### Whitehead tower
 {#WhiteheadTower}

The nature of higher spin structures is governed by what is called the _[[Whitehead tower]]_ of the [[homotopy type]] of the [[classifying space]] [[BO|$B O$]] of the [[orthogonal group]], where in each stage a [[homotopy group]] is removed _from below_. This is [[duality|dual]] to the _[[Postnikov tower]]_, where in each stage a homotopy group is added from above.

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
    \\
    & \downarrow
    \\
    & B GL(n)
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

* the [[obstruction]] classes are the [[universal characteristic classes]]

  * [[first Stiefel-Whitney class]] $w_1$

  * [[second Stiefel-Whitney class]] $w_2$

  * [[Pontryagin class|first fractional Pontryagin class]] $\tfrac{1}{2}p_1$

  * [[Pontryagin class|second fractional Pontryagin class]] $\tfrac{1}{6}p_2$

* every possible square in the above is a [[homotopy pullback]] square (using the [[pasting law]]).

For instance $w_2$ can be identified as such by representing $B O \to \tau_{\leq 2} B O \simeq BO/_{\sim_n}$ by a [[Kan fibration]] (see at [[Postnikov tower]]) between [[Kan complexes]] so that then the [[homotopy pullback]] (as discussed there) is given by an ordinary pullback. Since $sSet$ is a [[simplicial model category]], $sSet(S^2,-)$ can be applied and preserves the pullback as well as the homotopy pullback, hence sends $ B O \to \tau_{\leq 2} B O$ to an isomorphism on connected components. This identifies  $B SO \to B^2 \mathbb{Z}$ as being an [[isomorphism]] on the second [[homotopy group]]. Therefore, by the [[Hurewicz theorem]], it is also an isomorphism on the [[cohomology group]] $H^2(-,\mathbb{Z}_2)$. Analogously for the other characteristic maps.

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

* the [[obstruction]] to lifting an [[orthogonal structure]] $T X : X \to B O$ to an [[orientation]] structure is the homotopy class $[w_1(T X)] \in H^1(B O, \mathbb{Z}_2)$ of $w_1(T X) : X \stackrel{T X}{\to} B O \stackrel{w_1}{\to} B \mathbb{Z}_2$, the [[first Stiefel-Whitney class]];

* the [[obstruction]] to lifting an [[orientation]] structure $T X : X \to B SO$ to an [[spin structure]] is the [[second Stiefel-Whitney class]] $w_2(T X) : X \stackrel{}{\to} B S \stackrel{w_2}{\to} B^2 \mathbb{Z}_2$;

* the [[obstruction]] to lifting a [[spin structure]] $X \to B Spin$ to an [[string structure]] is the [[first fractional Pontryagin class]];

* the [[obstruction]] to lifting a [[string structure]] $X \to B String$ to a [[fivebrane structure]] is the [[second fractional Pontryagin class]].


#### Necessity of smooth refinement
 {#NecessityOfSmoothRefinement}

We will below consider a _smooth refinement_ of the above Whitehead tower. Before we do so, here a few words on why we need to do this.

One way to state the general problem is:

1. _The [[classifying space]] of, say, the [[spin group]] is **not** a _[[fine moduli space]]_. 

   Because, while homotopy classes $Maps(X, B Spin)_\sim$ of maps $X \to B Spin$ are in bijection with equivalence classes of [[spin bundles]] on $X$, the homotopy classes $Maps(X, \Omega B Spin)_\sim = Maps(X, Spin)_\sim$ of [[homotopies]] from the trivial map $X \to * \to B Spin$ are _not_ in general in bijection with the [[gauge transformations]] of the trivial spin bundle: the latter form the set of [[smooth functions]] $C^\infty(X,Spin)$, not just the homotopy classes of these.

1. $Maps(X, B(-))_\sim$ does not give the right [[BRST-complex]]; hence speaking about [[gauge theory]] in terms of just bare (as opposed to geometric) [[homotopy theory]] does not yield an admissible starting point for [[quantization]] (by [[BV-BRST formalism]]).

1. $Maps(X, B(-))_\sim$ cannot distinguish a group from its [[maximal compact subgroup]], such as $O \hookrightarrow GL_n$, and hence cannot see [[vielbeins]], not [[generalized vielbeins]], not [[exceptional generalized geometry]]:

  in terms of classifying spaces the entire discussion [of vielbein fields above](#VielbeinFields) would collapse;

  higher analogs of this problem include for instance that $Maps(X, B(-))_\sim$ cannot distinguish over 10-dimensional spacetime $X$ an [[E8]]-[[gauge field]] from a [[NS5-brane]] [[magnetic charge]];

1. eventually an [[action functional]] on the space of fields is to be constructed as a [[smooth function]], or in fact as a smooth _[[flat section]]_ of a smooth [[circle n-bundle with connection|circle bundle with connection]] on the space of fields -- which requires some smooth structure on that space.

These problems are all fixed by refining [[classifying spaces]] such as $B Spin \in \infty Grpd$ to [[smooth infinity-groupoid|smooth]] [[moduli stacks]] such as $\mathbf{B} Spin \in Smooth \infty Grpd$.



#### Smooth refinement
 {#SmoothRefinement}

We considered [above](#SmoothModuliStacks) the smooth refinement of the [[classifying space]] $B G$ for $G$ a [[Lie group]] to a [[smooth infinity-groupoid|smooth]] [[moduli stack]] $\mathbf{B}G$. While that works well, one can see on general grounds that this cannot provide a smooth refinement of the higher stages of the Whitehead tower, if one asks the refinement to preserve [[obstruction]] theory. The problem is that a smooth stack is necessarily a smooth [[homotopy n-type|homotopy 1-type]] (even if its [[geometric realization]] is a higher type! see below), while the higher stages of the smooth Whitehead tower need to be smooth [[homotopy n-types]]/[[n-groupoids]] for higher $n$.


But there is an evident refinement of the above discussion to such _smooth $n$-types_. 

To that end we first need a good model for bare homotopy types. One observes that the [[nerve]] functor embeds [[groupoids]] into [[Kan complexes|Kan]] [[simplicial sets]], as precisley those which are [[coskeleton|2-coskeletal]], meaning that only their 0-cells and 1-cells are non-trivial. Accordingly, a [[Kan complex]] which is [[coskeleton|(n+1)-coskeletal]] may be regarded as an _[[n-groupoid]]_ modelling a [[homotopy n-type]], and hence a general Kan complex as an _[[∞-groupoid]]_.

$$
  \array{
    && Groupoids
    \\
    & \swarrow && \searrow^{\mathrlap{N}}
    \\
    Categories &&& & KanComplexes
    \\
    & {}_{\mathllap{N}}\searrow && \swarrow
    \\
    && QuasiCategories
    \\
    && \downarrow
    \\
    && SimplicialSets
  }
  \,.
$$

A morphism between groupoids $X \to Y$ is an [[equivalence of groupoids]] precisely if it is an [[essentially surjective functor]] and a [[full and faithful functor]].  This is equivalent to it inducing an [[isomorphism]] on [[isomorphism]] classes / connected components, and on [[automorphism groups]]. This in turn is equivalent to it inducing an isomorphism on the 0th and the first [[homotopy groups]] $\pi_0$ and $\pi_1$.

Accordingly, we say that a [[homotopy equivalence]] between [[Kan complexes]] is a morphism $X \to Y$ which induces an isomorphism on all [[homotopy groups]]. These can be defined for general [[simplicial sets]], and we say a morphism between these is a [[weak homotopy equivalence]] if it induces such isomorphisms.

Write  

$$
  \infty Groupoids \simeq SimplicialSets[ \{ weak\;homotopy\;equivalences\}^{-1} ]
$$

for the [[homotopy theory]] obtained by [[simplicial localization|localization]] at the weak homotopy equivalences: [[∞-groupoids]].


A [[topological space]] $X$ defines a Kan complex/ [[∞-groupoid]] by the [[singular simplicial complex]] construction $Sing X$, and this establishes an [[homotopy hypothesis|equivalence between]] the [[homotopy theory]] of topological spaces and simplicial sets

$$
  Top
   \stackrel{\stackrel{{\vert-\vert}}{\leftarrow}}{
     \underoverset{\simeq}{Sing}{\to}
   }
  sSet
  \,.
$$

In view of this, the [above](#WhiteheadTower) [[Whitehead tower]] can be understood entirely as taking place in Kan complexes.

For instance for $A$ an [[abelian group]], the [[2-groupoid]]

$$
  \mathbf{B}^2 U(1)_{disc}
  = 
  \left\{
    \array{
       && \to
       \\
       & \nearrow && \searrow
       \\
       *
       &&\Downarrow^{a \in A}&&
       *
       \\
       & \searrow && \nearrow
       \\
       && \to
    }
  \right\}
$$

corresponds to the [[Eilenberg-MacLane space]] $K(A,2)$.

More generally, for each [[chain complex]] $A_\bullet$ of [[abelian groups]] the [[Dold-Kan correspondence]] provides a Kan complex $\Xi(A_\bullet)$ whose [[simplicial homotopy groups]] are the [[chain homology]] groups of $A_\bullet$. A [[quasi-isomorphism]] $A_\bullet \to B_\bullet$ is sent to a weak homotopy equivalence $\Xi(A_\bullet) \to \Xi(B_\bullet)$. In this sense [[∞Grpd]] is a [[non-abelian cohomology|non-abelian]] generalization of chain complexes with quasi-isomorphisms inverted.

Using this, we can easily state the generalization of the definition of smooth stacks from above: we obtain a [[homotopy theory]] of _[[smooth ∞-groupoid|smooth ∞-stacks]]_ $\mathbf{H} \coloneqq $ _[[Smooth∞Grpd]]_ by considering simplicial sets parameterized over smooth manifolds and forcing [[stalk]]wise weak homotopy equivalences to become homotopy equivalences

$$
  \mathbf{H} \coloneqq Func(SmthMfd^{op}, sSet)[\{stalkwise\, w.h.e.\}^{-1}]
  \,.
$$

For instance there is the smooth 2-stack

$$
  \mathbf{B}^2 U(1) \in \mathbf{H}
$$

given by assigning to each test space $U$ the [[Eilenberg-MacLane space]] on the (discrete) abelian group of smooth functions $U \to U(1)$

$$
  \mathbf{B}^2 U(1) 
    : 
   U \mapsto 
   K(  C^\infty(U, U(1)), 2)
   = 
   \left\{
    \array{
       && \to
       \\
       & \nearrow && \searrow
       \\
       *
       &&\Downarrow^{c \in C^\infty(U,U(1))}&&
       *
       \\
       & \searrow && \nearrow
       \\
       && \to
    }
  \right\}
  \,.
$$

A morphism $X \to \mathbf{B}^2 U(1)$ in $\mathbf{H}$ is equivalently a zig-zag $X \stackrel{\simeq}{\leftarrow} C(\{U_i\}) \stackrel{\lambda}{\to} \mathbf{B}^2 U(1)$ through the [[Cech nerve]]. This now defines in degree 2 

$$
  \array{
    && (x,j)
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    (x,1) &&\to&& (x,k)
  }
  \;\;\;
  \mapsto
  \;\;\;
  \array{
    && *
    \\
    & \nearrow &\Downarrow^{\lambda_{i j k})(x}& \searrow
    \\
    * &&\to&& *
  }
$$

smooth functions $\lambda$ on triple overlaps 

$$
  \lambda_{i j k } 
    : 
  U_i \cap U_j \cap U_k \to U(1)
$$


and the condition on quadruple overlaps $U_i \cap U_j \cap U_k \cap U_l$ says that they satisfy

$$
  \lambda_{i j k}
  \lambda_{i k l}
   =
  \lambda_{j k l}
  \lambda_{i j k}
  \,.
$$

This now identifies $(\lamda_{i j k})$ with a cocycle in degree-2 [[Cech cohomology]]

$$
  [(\lambda_{i j k})] \in H^2_{smooth}(X, U(1)) 
  \,.
$$

This classifies a smooth [[circle n-bundle with connection|circle 2-bundle]] / [[bundle gerbe]].

Generally we have

$$
  \pi_0 \mathbf{H}(X, \mathbf{B}^n U(1))
  \simeq
  H^n_{smooth}(X, U(1))
$$

and for $X$ a smooth manifold

$$
  \cdots \simeq H^{n+1}(X, \mathbb{Z})
  \,.
$$

So apparently the smooth $n$-stack $\mathbf{B}^n U(1)$ is a _smooth refinement_ of the [[Eilenberg-MacLane space]] $K(\mathbb{Z},n+1)$.

This is made precise as follows.

**Theorem** There is an [[(∞,1)-functor]]

$$
  {\vert-\vert}
  : 
  Smooth\infty Grpd
   \stackrel{\Pi}{\to}
  \infty Grpd
   \stackrel{{\vert-\vert}}{\to}
  Top
$$

which is [[left adjoint|left]] [[adjoint (∞,1)-functor|adjoint]] to the functor that assigns [[constant ∞-stacks]].
We call this the _[[geometric realization]]_ of [[smooth ∞-groupoids]].

We say that a choice of lift of a diagram of bare homotopy types through geometric realization is a smooth _geomtric refinement_.

For instance one finds

$$
  {\vert \mathbf{B}^n U(1) \vert}
  \simeq
  B^n U(1)\simeq B^{n+1}\mathbb{Z} \simeq K(\mathbb{Z}, n+1)
$$

and hence $\mathbf{B}^n U(1)$ is a smooth geometric refinement of $K(\mathbb{Z}, n+1)$.

We now apply this to the above Whitehead tower.

#### Smooth Whitehead tower
 {#SmoothWhitehead}

We state the smooth refinement of the above Whitehead tower and then explain some aspects of how it is constructed.

**Theorem** There is a smooth geometric refinement of the [above Whitehead tower](#WhiteheadTower) of [[homotopy type|bare homotopy types]] to a tower of [[smooth infinity-groupoid|smooth homotopy types]]/[[smooth ∞-stacks]] of the form

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

and where 

* $\tfrac{1}{2} \mathbf{p}_1$ classifies the universal [[Chern-Simons circle 3-bundle]] and hence identifies it with $\mathbf{B}String \to \mathbf{B}Spin$;

* $\tfrac{1}{6} \mathbf{p}_2$ classifies the universal [[Chern-Simons circle 7-bundle]] and hence identifies it with $\mathbf{B}Fivebrane \to \mathbf{B}String$.

This is constructed using essentially the following three tools for presenting presheaves of higher groupoids:

1. The [[Dold-Kan correspondence]] 

   $$
     \Xi : Ch_{\geq 0} \stackrel{\simeq}{\to} sAb \to sSet
   $$ 

   and its prolongation to presheaves

   $$
     \Xi : [SmthMfd^{op}, Ch_{\geq 0}) \stackrel{\simeq}{\to} [SmthMfd^{op},sAb] \to [SmthMfd^{op},sSet]
   $$ 

   allows to use presheaves of [[chain complexes]] of [[abelian groups]] to present presheaves of strict $\infty$-groupoids with strict abelian group structure. 

   For instance
  
   $$
     \mathbf{B}^n U(1) \simeq \Xi( C^\infty(-,U(1))[n] )
   $$

   is equivalent to the image under the DK correspondence of the sheaf of chain complexes which is concentrated in degree $n$ on the group of $U(1)$-valued functions.

1. Some [nonabelian generalizations](Dold-Kan+correspondence#StatementGeneral) of the Dold-Kan correspondence allow to use chain complexes of not entirely abelian groups -- _[[crossed complexes]]_ -- to present a few more classes of $\infty$-groupoids. Notably nonabelian 2-term chain complexes, 

   $$
     G_1 \stackrel{\delta}{\to} G_0  
   $$

   called _[[crossed modules]]_, due to them being equipped with a compatible action $G_0 \to Aut(G_1)$, serve to equivalently present [[strict 2-groups]].

   For instance, one way to construct the [[string 2-group]] $String$ above is via the crossed module $(\hat \Omega_* Spin \to P_* Spin)$ induced from the [[Kac-Moody central extension]] of the [[loop group]] of $Spin$.

   For a given crossed module, the corresponding moduli 2-stack $\mathbf{B}(G_1 \stackrel{\delta}{\to} G_0)$ has [[2-morphism|2-cells]] that look like

   $$
      \mathbf{B}(G_1 \to G_0)
      =
      \left\{
        \array{
          && *
          \\
          & {}^{\mathllap{g_1}}\nearrow &\Downarrow^{\mathrlap{h}}& \searrow^{\mathrlap{g_2}}
          \\
          * &&\underset{\delta(h) g_2 g_1}{\to}&&
        }
        \;\;
        |
        \;\;
        g_1,g_2 \in G_0, h \in G_1
      \right\}
     \,.
   $$

1. The [[Lie integration]] $\tau_{\leq n} \exp(\mathfrak{g})$ of an [[L-∞ algebra]] $\mathfrak{g}$ yields the corresponding [[smooth ∞-group]] $G$. For instance the [[string 2-group]] $String$ above is also equivalently given by $\mathbf{B} String \simeq \tau_{\leq 2} \exp(\mathfrak{string})$, where $\mathfrak{string}$ is the [[string Lie 2-algebra]].

Using these tools, the stages of the above smooth Whitehead tower are constructed as follows:

* the morphism $\mathbf{w}_1 : \mathbf{B}O \to \mathbf{B} \mathbb{Z}_2$ is directly induced from the canonical Lie group homomorphism $O \to \mathbb{Z}_2$.

* the morphism $\mathbf{w}_2 : \mathbf{B}SO \to \mathbf{B}^2 \mathbb{Z}_2$ in $\mathbf{H}$ is presented by the [[infinity-anafunctor|zig-zag]] of crossed modules

  $$
    \array{
       (\mathbb{Z}_2 \to Spin) &\stackrel{}{\to}& (\mathbb{Z}_2 \to 1)
       \\
       {}^{\mathllap{\simeq}}\downarrow
       \\
       (1 \to SO)
    }
  $$

* the morphism $\tfrac{1}{2}\mathbf{p}_1 : \mathbf{B}Spin \to \mathbf{B}^3 U(1)$ is constructed ([FSSa](#FSSa)) as the [[Lie integration]] of the canonical [[infinity-Lie algebra cohomology|L-∞ 3-cocylce]] $\mathbf{B}\mu_3 : \mathbf{B}\mathfrak{so} \to \mathbf{B}^3 \mathbb{R}$.
  
* similarly $\tfrac{1}{6}\mathbf{p}_2 \simeq \exp(\mu_7)$ is the Lie integration of a canonical 7-cocycle $\mathbf{B}\mu_7 : \mathbf{B}\mathfrak{string} \to \mathbf{B}^7 \mathbb{R}$ ([FSSa](#FSSa)).


#### Differential refinement
 {#DifferentialRefinement}

While the [above](#SmoothWhitehead) smooth refinement of the Whitehead tower already improves on the [bare Whitehead tower](#WhiteheadTower) by remembering the correct spaces of [[gauge transformations]], it still only sees "[[instanton]] sectors" of [[gauge fields]] and [[higher gauge fields]], namely the underlying [[principal ∞-bundles]]. We add now the refinement from _smooth cohomology_ to [[differential cohomology]] such as to encode the actual [[higher gauge fields]] themselves. This differential cohomology in turn is naturally available in terms of _curvature twisted flat cohomology_ or equivalently _curvature-twisted [[local systems]]_.

$\,$

In order to get a feeling for what differential refinements of higher moduli stacks are going to be like, recall two structures that we have already seen above:

1. For $G$ a [[Lie group]] the smooth moduli stack of smooth $G$-[[principal connections]] from [above](#SpinConnection) is presented by

   $$
     \mathbf{B}G_{conn}
     =
     (C^\infty(-,G) \times \Omega^1(-, \mathfrak{g}) 
        \stackrel{\overset{}{\to}}{\underset{}{\to}}
      \Omega^1(-, \mathfrak{g}))
     =
     \left\{
        A \stackrel{g}{\to} (g^{-1} A g + g^{-1} d g)
        |
        A \in \Omega^1(-,\mathfrak{g}),
        g \in C^\infty(-,G)
     \right\}
     \,.
   $$

   In the special case that $G = U(1)$ is abelian, this is the image under the [[Dold-Kan correspondence]] of the length 1 complex of sheaves of abelian groups

   $$
     \mathbf{B}U(1)_{conn} = [C^\infty(-) \stackrel{d_{dR}}{\to} \Omega^1(-)]
      \,.
   $$

1. The smooth $n$-stack $\mathbf{B}^n U(1)$ is realized as the image under the [[Dold-Kan correspondence]] by the chain complex of sheaves $C^\infty(-,U(1))$

   $$
     \mathbf{B}^n U(1)
     \simeq
     [
       C^\infty(-,U(1))
       \to 0
       \to \cdots 
       \to 0
     ]
     \,.
   $$

From the look of these expressions there is already a plausible candidate for the differential refinement $\mathbf{B}^n U(1)_{conn}$, the moduli $n$-stack of [[circle n-bundles with connection]] -- it should be the _[[Deligne complex]]_:

$$
  \mathbf{B}^{n} U(1)_{conn}
    =
  \left[
  C^\infty(-,U(1))
  \stackrel{d_{dR} log}{\to}
  \Omega^1(-)
  \stackrel{d_{dR}}{\to}
  \Omega^2(-)
  \stackrel{d_{dR}}{\to}
  \cdots
  \stackrel{d_{dR}}{\to}
  \Omega^n(- )
  \right]
  \,.  
$$

For instance a cocycle $X \to \mathbf{B}^2 U(1)_{conn}$ in $\mathbf{H}$ is in $Funct(SmthMfd^{op}, sSet)$ and relative to a [[good open cover]] given by a morphism $C(\{U_i\}) \to \mathbf{B}^2 U(1)_{conn}$, which is

* on each $U_i$ a [[connection on a 2-bundle|connection 2-form]] $B_i \in \Omega^2(U_i)$;

* on each $U_i \cap U_j$ a 1-form $A_{i j} \in \Omega^1(U_i \cap U_j)$ such that $B_j - B_i = d_{dR} A_{i j} $;

* on each $U_i \cap U_j \cap U_k$ a smooth functor $\phi_{i j k} \in C^\infty(U_i \cap U_j \cap U_k, U(1))$ such that $A_{i j} + A_{j k} - A_{i k} = d_{dR} log \phi_{i j k}$ and such that on each $U_i \cap U_j \cap U_k \cap U_l$ the equation $\phi_{i j k} \phi_{i k l} = \phi_{i j l} \phi_{j k l}$ holds.

Tthe [[B-field]] on [[spacetime]] is (in the absence of various possible twists, to be discussed), such a cocycle $X \to \mathbf{B}^2 U(1)_{conn}$; and the [[C-field]] (similarly in the absence of possible twists, to be discussed below) is given by a morphism $X \to \mathbf{B}^3 U(1)_{conn}$.


Such cocycles in [[Deligne complex|Deligne]] [[hypercohomology]] define classes in _[[ordinary differential cohomology]]_ $H_{diff}^{n+1}(X)$:


$$
  H_{diff}^{n+1}(X)   
   = 
  \pi_0 \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
  \,.
$$


There is an evident morphism

$$
  \mathbf{B}^n U(1)_{conn} \to \mathbf{B}^n U(1)
$$

which [[forgetful functor|forgets]] the connection data. We say that $\mathbf{B}^n U(1)_{conn}$ is a _differential refinement_ of $\mathbf{B}^n U(1)$. 

We now want to construct a differential refinement of the above smooth Whitehead tower, hence of the smooth [[universal characteristic classes]] appearing in it. To do so, we now first provide a more conceptual way to think of $\mathbf{B}^n U(1)_{conn}$, a way to obtain this more abstractly from fundamental principles.

The key is that the [[(∞,1)-topos]] $\mathbf{H}$ of [[smooth ∞-groupoids|smooth ∞-stacks]] comes with a canonical notion of _[[local system]]_ or _[[connection on an ∞-bundle|flat ∞-connection]]_, and that we can _twist_ this to find a notion of [[curvature]]-twisted and hence non-flat [[connection on an ∞-bundle|∞-connection]]. The notion of local systems is induced from two basic derived adjoint functors that exist on $\mathbf{H}$

$$
  \mathbf{H}
   \stackrel{\overset{Disc}{\leftarrow}}{\underset{\Gamma}{\to}}
  \infty Grpd
  \,,
$$

where $\Gamma$ evaluates a presheaf on the point, and where $Disc$ sends an $\infty$-groupoid to the presheaf constant on that value. We form the composite 

$$
  \flat : \mathbf{H} \stackrel{\Gamma}{\to} \infty Grpd \stackrel{Disc}{\to} \mathbf{H}
  \,,
$$

to be pronounced "flat": for $A \in \mathbf{H}$ a smooth homotopy type, we call $\flat A$ the corresponding _flat local coefficient_ object. 

For instance if $G$ is a [[Lie group]], then $\Gamma \mathbf{B}G \simeq B (G_{disc}) = K(G_{disc}, 1)$, and so a morphism $X \to \flat \mathbf{B}G$ is equivalently a cocycle $X \to \mathbf{B} (G_{disc})$, hence a $G_{disc}$-covering space, hence a flat $G$-[[principal connection]].


Generally, we say that a morphism

$$
  X \to \flat A
$$

is an _$A$-[[local system]]_ or _$A$-valued [flat ∞-connection](cohesive+%28infinity,1%29-topos+--+structures#FlatDifferentialCohomology)_ on $X$.

There is a canonical forgetful morphism $u : \flat A \to A$ which forgets the flat connection: this is the $(\Disc \dashv \Gamma)$-[[counit of an adjunction|counit]]. Consider the coefficient object of those flat $G$-connections whose underlying $\mathbf{B}G$-[[principal ∞-bundle]] is trivial

$$
  \flat_{dR} \mathbf{B}G
  \coloneqq
  \left\{
    \nabla \in \flat \mathbf{B}G | (u(\nabla) \simeq * )
  \right\}
  \,.
$$

From the example of ordinary [[principal connections]] it is familiar that flat $G$-connections on trivial $G$-principal bundles are equivalently flat [[Lie algebra valued differential forms]].
Below we will see that for general [[smooth ∞-groups]] $G$, morphisms $X \to \flat_{dR} \mathbf{B}G$ are $\mathfrak{g}$-[[infinity-Lie algebroid-valued differential form|∞-Lie algebra valued differential forms]] on $X$.

Reading the above expression in [[homotopy type theory]], its [[categorical semantics]] is  the [[homotopy fiber]] of the counit

$$
  \flat_{dR} \mathbf{B}G \coloneqq * \times_{\mathbf{B}G} \flat \mathbf{B}G
  \,.
$$

By this construction and applying the [[pasting law]], there is a canonical morphism $\theta : G \to \flat_{dR} \mathbf{B}G$, hence a canonical $\mathfrak{g}$-valued form on any cohesive [[∞-group]] $G$: this identifies as the canonical _[[Maurer-Cartan form]]_ on the [[∞-group]] $G$.

$$
  \array{
    G &\to& *
    \\
    {}^{\mathllap{\theta}}\downarrow && \downarrow
    \\
    \flat_{dR} \mathbf{B}G &\to& \flat \mathbf{B}G
    \\
    \downarrow && \downarrow^{\mathrlap{u}}
    \\
    * &\to& \mathbf{B}G
  }
  \,.
$$

For the special class of cases $G = \mathbf{B}^n U(1)$ the [[circle n-group|circle (n+1)-group]] we call $curv_{\mathbf{B}^n U(1)}  \coloneqq  \mathbf{B}^n U(1) \to \flat_{dR} \mathbf{B}^{n+1} U(1)$ the _universal [[curvature]] class_ in degree $(n+1)$. 

Due to the existence of the further functor $\Pi : \mathbf{H} \to \infty Grpd$ discussed [above](#SmoothWhitehead) it follows that $\flat : \mathbf{H} \to \infty Grpd$ is a [[right adjoint]] and hence commutes with homotopy pullback. This in turn implies that by forming one more homotopy fiber above, we obtain the following differential version of a universal local coefficient bundle:

$$
  \array{
    \flat \mathbf{B}^n U(1) &\to& \mathbf{B}^n U(1)
    \\
    && \downarrow^{\mathrlap{curv}}
    \\
    && \flat_{dR} \mathbf{B}^{n+1} U(1)
  }
  \,.
$$

By the general concept of [[twisted cohomology]], we see that this defines a notion of _curvature twisted flat differential cohomology_ -- hence of differential cohomology. 

Specifically, for $F_X : X \to \Omega^{n+1}_{cl}(-)$ a closed [[differential form]] on $X$, a [[cocycle]] in $F_X$-[[twisted cohomology|twisted]] $\mathbf{curv}$-cohomology is equivalently a [[circle n-bundle with connection]] with that curvature

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B}^n U(1)
    \\
    & {}_{\mathllap{F}}\searrow &\swArrow_{\nabla}& \swarrow_{\mathrlap{\mathbf{curv}}}
    \\
    && \flat_{dR} \mathbf{B}^{n+1} U(1)_{conn}
  }
  \;\;
  \in
  \mathbf{H}_{\flat \mathbf{B}^{n+1}U(1)}(F_X, \mathbf{curv})
  \,.
$$

For varying $F$, the $\mathbf{curv}$-[[twisted cohomology]] in $\mathbf{H}$ identifies with [[ordinary differential cohomology]]: the [[homotopy pullback]] $\mathbf{B}^n U(1)_{conn}$ in

$$
  \array{
    \mathbf{B}^n U(1)_{conn} &\to& \Omega^{n+1}_{cl}(-)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}^n U(1) &\stackrel{curv}{\to}& \mathbf{B}^{n+1} U(1)_{conn}
  }
$$

is presented, under the [[Dold-Kan correspondence]],  by the [[Deligne complex]], discussed above. This exhibits ordinary differential cohomology as the curvature-twisted flat cohomology


$$
  \mathbf{H}_{diff}(X, \mathbf{B}^n U(1))
  =
  \mathbf{curv}Struc_{\Omega^{n+1}}(X)
  \,.
$$

Using this geometric-homotopy-type theoretic description of ordinary differential cohomology, we obtain now a natural notion of differential refinement of smooth [[universal characteristic classes]]
$\mathbf{c} : \mathbf{B}G \to \mathbf{B}^{n+1} U(1)$. We say that a _differential refinement_ of $\mathbf{c}$ is a morphism $\hat \mathbf{c}$ fitting into a diagram 

$$
  \array{
    \flat \mathbf{B}G &\stackrel{\flat \mathbf{c}}{\to}&
    \flat \mathbf{B}^{n+1} U(1)
    \\
    \downarrow && \downarrow 
    \\
    \mathbf{B}G_{conn} &\stackrel{\hat \mathbf{c}}{\to}& \mathbf{B}^{n+1} U(1)_{conn}
    \\
    \downarrow && \downarrow^{\mathrlap{curv}}
    \\
    \mathbf{B}G 
      &\stackrel{\mathbf{c}}{\to}&
    \mathbf{B}^{n+1} U(1)
  }
$$

that factors the [[natural transformation|naturality]] square of $\flat$ on $\mathbf{c}$.




#### Differential Whitehead tower
 {#DifferentialWhitehead}

**Theorem** ([SSSa](#SSSa), [FSSa](#FSS)) There exists a smooth differential refinement of the [Whitehead tower of BO](#WhiteheadTower) as follows:


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

This construction is a joint generalization of [[Chern-Weil theory]]
and [[Chern-Simons theory]] to [[∞-Chern-Weil theory]] and [[schreiber:∞-Chern-Simons theory]]

For instance 

* the differential refinement of the first fractional Pontryagin class above yields the action functional

  $$
    \exp(i S_{\tfrac{1}{2}\mathbf{p}_1}) 
      : 
    [\Sigma, \mathbf{B}Spin_{conn}]
      \stackrel{\tfrac{1}{2}\hat \mathbf{p}_1}{\to}
    [\Sigma, \mathbf{B}^{3}U(1)_{conn}]
      \stackrel{\exp(i \int_\Sigma(-))}{\to}
    U(1)
  $$

  of [[Spin]]-[[Chern-Simons theory]], refined to the integrated off-shell [[BRST-complex]] of the theory;

* the differential refinement of the second fractional Pontryagin class above yields the action functional

  $$
    \exp(i S_{\tfrac{1}{6}\mathbf{p}_2}) 
      : 
    [\Sigma, \mathbf{B}String_{conn}]
      \stackrel{\tfrac{1}{6}\hat \mathbf{p}_2}{\to}
    [\Sigma, \mathbf{B}^{7}U(1)_{conn}]
      \stackrel{\exp(i \int_\Sigma(-))}{\to}
    U(1)
  $$

  of 7-dimensional Chern-Simons theory on nonabelian String 2-form fields ([FSSb](#FSSb))

We indicate briefly how this is constructed.

(...)

### **Interlude)** Anomaly line bundle on smooth moduli stacks of fields
 {#Anomalies}


Before coming to the description in [[smooth ∞-groupoid|smooth]] [[moduli ∞-stacks]] below, we make some introductory comments on the general origin of twisted differential structures in higher gauge theory, following ([Freed](#Freed)). We add some stacky aspects to that and explain why.

In summary, we discuss how the [[action functional]] of higher gauge theory in the presence of electric and magnetic charge is a [[section]] of a [[circle n-bundle with connection|circle bundle with connection]] $\nabla_{higher\;gauge\;anomaly}$ on the [[smooth ∞-groupoid|smooth ∞-stack]] $[X, \mathbf{Fields}]$ of field configurations on a given [[spacetime]] $X$, exhibited by a morphism

$$
  \nabla_{higher\;gauge\;anomaly}
   \coloneqq
   \exp(2 \pi i \int_X \hat\mathbf{c}_{el} \cup \hat \mathbf{c}_{mag}  )
   : 
  [X, \mathbf{Fields}]
   \stackrel{}{\to}
  \mathbf{B} U(1)_{conn}
  \,,
$$

where $\hat\mathbf{c}_{el} \cup \hat \mathbf{c}_{mag} : \mathbf{Fields} \to \mathbf{B}^{dim X +2} U(1)_{conn}$ is the differential characteristic morphism induced by the [[differential cup product]] ([FSSd](#FSSd)) of universal electric and magnetic currents, and where $\exp(2\pi i \int_X(-))$ is [[fiber integration in ordinary differential cohomology]] refined to smooth $\infty$-stacks (this is the "$(dim X)+1$-dimensional [[schreiber:infinity-Chern-Simons theory]]" of $\hat\mathbf{c}_{el} \cup \hat \mathbf{c}_{mag}$ in [[codimension]] 1).

#### Higher gauge fields in the presence of magnetic charge current

[[gauge theory|Gauge theory]] starts maybe with [[James Clerk Maxwell|Maxwell]] around 1850, who discovered, in modern language, that the [[field strength]] of the [[electromagnetic field]] on [[spacetime]] is encoded in a closed [[differential form|differential 2-form]] $F \in \Omega^2_{cl}(X)$.
Then in the 1930s [[Paul Dirac|Dirac]]'s [famous argument](electromagnetic+field#ChargeQuantization) showed that more precisely -- _in the absence_ of, or _outside of_ the [[support]] of [[magnetic charge]] [[current]] -- this 2-form is the [[curvature]] of a [[circle group]]-[[principal bundle]] [[connection on a bundle|with connection]], a 2-cocycle $\hat F$ in [[ordinary differential cohomology]].

In view of this the [[gauge transformation|gauge]] [[equivalence classes]] of configurations of the electromagnetic field on $X$ form the set

$$
  H^2_{diff}(X) \coloneqq \tau_0 \mathbf{H}(X, \mathbf{B}U(1)_{conn})
$$ 

of differential cohomology classes in degree 2 on $X$.

Dirac's argument works outside the support of the magnetic current, where the situation is comparatively easier to handle. But the twists and anomalies that we are concerned with here arise when one completes Dirac's argument, and generalizes the model of the electromagnetic field to exist also over parts of spacetime where the magnetic current is non-trivial ([Freed](#Freed)). Among other things the following shows that twists by higher bundles and differential cohomology is not just something that arises in string theory, but is already present in dear-old electromagnetism.

To see what happens in that general case, notice that the original [[Maxwell equations]] on the [[field strength]]/[[curvature]] 2-form of the electromagnetic field are:

1. $d_{dR} F = J_{mag}$ ([[magnetic charge]] [[current]])

1. $d_{dR} \star F = J_{el}$ ([[electric charge]] [[current]])

where $\star$ is the [[Hodge star operator]] for the given [[pseudo-Riemannian metric|pseudo]] [[Riemannian metric]] (the field of [[gravity]]) on $X$.

1. The first one is _[[kinematics]]_. For $J_{mag} = 0$ it just expresses that the cuvature 2-form is closed, which is part of the fact that $\hat F$ is a differential cocycle, so it is satisfied by all kinematic field configurations, meaning: all elements of $H^{n+1}_{diff}(X)$. 

1. The second is _[[dynamics]]_, being the [[equations of motion]] of the system. The configurations that satisfy this form the [[covariant phase space]] ([[BV-BRST complex]]) $P \hookrightarrow [X, \mathbf{B}U(1)_{conn}]$ of the theory. For our purposes here this will not concern us, since the anomalies and twists are kinematic in nature, we work "off-shell".

While for experimentally observed electromagnetism it is consistent to assume that $J_{mag} = 0$, this is not the case for general gauge theories, notably not for [[heterotic supergravity]], as we discuss in a moment. There the gauge field and the field of gravity induce a non-vanishing "fivebrane magnetic current"

* $J^{NS5}_{mag}(\phi_{gr}, \phi_{ga}) = \langle F_\omega \wedge F_\omega\rangle -\langle F_A \wedge F_A\rangle$

But for a [[circle n-bundle with connection]] in $H^{n+1}_{diff}(X)$, the curvature is necessarily closed, $d_{dR} F = 0$. So there must be another way to refine $d F  = J_{mag}$ to differential cohomology.

(Notice for later that the natural home of $J_{mag}$ is not plain [[de Rham cohomology]], but [[compactly supported cohomology]]. The equation $d_{dR} F = J_{mag}$ is a trivialization of the image of $J_{mag}$ in de Rham cohomology, but not in general a trivialization of the magnetic current as an entity living in compactly supported cohomology.)

Consider therefore now the [[groupoid]]

$$
  \mathcal{H}^{n+1}_{diff}(X) \coloneqq 
   \tau_1 \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
  \,,
$$ 

whose 

* [[objects]] are [[cocycles]] in degree-$(n+1)$ differential cohomology: [[circle n-group]]-[[circle n-bundles with connection]];

* [[morphisms]] are equivalence classes of [[gauge transformations]] between these, hence equivalence classes of morphisms of higher bundles _with connection_.

This "[[categorification|categorifies]]" the cohomology set $H^{n+1}_{diff}(X)$ in that the letter is its [[decategorification]]: the set of [[isomorphism]] classes of objects.

For instance if differential cohomology is modeled by the [[Deligne complex]] with [[differential]] $D = d_{dR} \pm \delta$, then a morphism $\hat \alpha : \hat F_1 \to \hat F_2$ in $\mathcal{H}_{diff}^{n+1}(X)$ is a Deligne [[coboundary]] $D \hat \alpha = \hat F_2 - \hat F_1$. 

Or in terms of our smooth moduli stacks, this is a homotopy

$$
  \array{
    & \nearrow \searrow^{\mathrlap{\hat F_1}}
    \\
    X &\Downarrow^{ \hat \alpha }& \mathbf{B}^n U(1)_{conn}
    \\
    & \searrow \nearrow_{ \mathrlap{\hat F_2}  }
  }
  \,.
$$


Notice that, since morphisms in $\mathcal{H}^{n+1}_{diff}(X)$ preserve the [[connection on an infinity-bundle|higher connection]], a morphism

$$
  0 \to \hat F
$$

in $\mathcal{H}^{n+1}_{diff}(X)$ is a _flat section_ of the corresponding circle $n$-bundle, while a morphim

$$
  B \to \hat F
$$

for some $B \in \Omega^n(X) \hookrightarrow \mathcal{H}^{n+1}_{diff}(X)$ is a possibly non-flat section, hence a section just of the underlying [[circle n-group]]-[[principal ∞-bundle]]: it exhibits the fact that if the underlying bundle has a section, then the connection is equivalently given by a globally defined $n$-form $B$.

(Beware of this subtlety when comparing with ([Freed](#Freed)): a differential as on the fifth line of [p. 8](arxiv.org/pdf/hep-th/0011220v2.pdf#page=8) there may change the curvature by an exact term, hence may not preserve the connection, in contrast to the coboundaries further below on that page and on [p. 9](arxiv.org/pdf/hep-th/0011220v2.pdf#page=9), which are the ones we are considering here.) 

(Another reason for considering the groupoid $\mathcal{H}^{n+1}_{diff}(X)$ is that it is needed in order to construct the [[quadratic refinement]] of the [[secondary intersection pairing]] that defines the partition function of [[self-dual higher gauge theory]] ([Hopkins-Singer](#HopkinsSinger)). This underlies the discussion of flux quantization [below](#SuGraFluxQuantization).)

Using this, we may improve the definition of the electromagnetic field on $X$: take it to be a non-flat section 

$$
  \hat \mathbf{c} \stackrel{\hat F}{\to} c_{mag}
  \,.
$$

of a _magnetic charge [[circle n-bundle with connection|circle 2-bundle with connection]]_ $\hat \mathbf{c} \in \mathcal{H}^{3}_{diff}(X)$. Equivalently, in terms of the corresponding classifying morphisms in $\mathbf{H}$ this is a homotopy in a diagram of the form

$$
  \array{
    X &\to&
    \\
    {}^{\mathllap{c_{mag}}}\downarrow 
     &\swArrow_{\hat F}& 
    \downarrow^{\mathrlap{\hat \mathbf{c}}}
    \\
    \Omega^2(-) &\stackrel{}{\hookrightarrow}& \mathbf{B}^2 U(1)_{conn}
  }
  \,.
$$

If $\hat F$ is given by a Deligne cochain $(g_{i j}, A_i)$, $\hat \mathbf{c}$ by a cochain $(c_{i j k}, \gamma_{i j}, \beta_i)$ then this means that

$$
  \begin{aligned}
    D (g_{i j}, A_i)
    & \coloneqq 
    ((\delta g)_{i j k},\; A_j - A_i + d_{dR} log g_{i j},\; d_{dR} A_i)
    \\
    & = 
    ( c_{i j k}^{-1},\; -\gamma_{i j}, \;  c_{mag} - \beta_i )
  \end{aligned}
$$

We say that $\hat F$ is a _$\hat \mathbf{c}$-[[twisted infinity-bundle|twisted bundle]]_ with _twisted curvature_ being

$$
  F \coloneqq d A_i + \beta_i
  \,.
$$ 

This now correspondingly has a twisted [[Bianchi identity]], which is precisely so that it solves the first [[Maxwell equation]] in the presence of magnetic current: $d_{dR} F = J_{mag}$.

While we have been discussing this here for ordinary electromagnetism, this is precisely the mechanism by which also the higher cases will work: for the [[heterotic string theory|heterotic]] [[Green-Schwarz mechanism]] the analogy is

$$
  \array{
    twisted\;curvature & & d_{dR}(gauge\;potential) && twist
    \\
    F &=& d_{dR} A_i &+& \beta_i && general case
    \\
    \\
    H_i &=& d_{dR} B_i &+& CS(\omega_i) - CS(A_i) && heterotic\;sugra
  }
  \,.
$$

Before we get there, we need to observe that working with the 1-groupoid $\mathcal{H}^{n+1}_{diff}(X)$ is not sufficient. We discuss now that we necessarily need the full [[n-groupoid]] and moreover its smooth refinement to the full [[smooth infinity-groupoid|smooth n-stack]] $[X, \mathbf{B}^n U(1)_{conn}]$ in order to capture the physics situation.

#### Gauge transformations

To see that we need the full higher groupoid, just consider the question:
what is a [[gauge transformation]] between twisted electromagnetic fields, that are now identified with morphisms $\hat \mathbf{c} \stackrel{\hat F}{\to} c_{mag}$ as above? Clearly, for this we need the [[2-groupoid]] of differential cocycles $\tau_2 \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})$

to next say that the equivalenc class of a gauge transformation of twisted fields $\hat a : \hat F_1 \to \hat F_2$ is a [[2-morphism]]

$$
  \array{
    & \nearrow \searrow^{\mathrlap{\hat F_1}}
    \\
    \hat \mathbf{c} &\Downarrow^{\hat \alpha}& J_{mag}
    \\
    & \searrow \nearrow_{\mathrlap{\hat F_2}}
  }
  \;\;\;
  \in \tau_{2} \mathbf{H}(X, \mathbf{B}^n U(1)_{conn})
  \,.
$$

That we moreover need the full [[smooth infinity-groupoid|smooth n-groupoid]] $[X, \mathbf{B}^n U(1)_{conn}]$ has several reasons, we discuss three. The third one of these is related to the higher gauge anomalies proper.


#### Magnetic current induced by background fields


The magnetic twist $\hat \mathbf{c}$ will depend on other field configurations that induce magnetic charge. So it is not a constant, but _varies with the fields_. 

(In fact, only this way is it a non-trivial stricture, for if both $\hat c$ and $c_{mag}$ are independent of the fields, the above definition of the groupoid of $\hat F$s is [[equivalence of groupoids|equivalent]] to that of untwisted electromagnetic fields: because [[homotopy fibers]] only depend on the connected component of the base points, up to equivalence.)

Let therefore $G^{bg}$ be the gauge group of another [[background gauge field]], and let $\mathbf{B}G^{bg}_{conn}$ be its moduli stack of gauge field configurations. If a $G^{bg}$-field _induces_ magnetic current, then $\hat \mathbf{c}$ must depend on the fields, hence it should be a map

$$
  [X, \mathbf{B}G^{bg}_{conn}] \to [X, \mathbf{B}^2 U(1)_{conn}]
$$

between these spaces of fields, and it should be a _smooth_ such map. Moreover, in general this is not expected to depend specifically the specific choice of $X$, but just on the notion of $G^{bg}$-fields in general, so it should be given just by postcompositon

$$
  \hat \mathbf{c} : \mathbf{B}G^{bg}_{conn} \to \mathbf{B}^2 U(1)_{conn}
$$

with a universal smooth map on moduli. With that given, the above picture for the $\hat \mathbf{c}$-twisted higher electric field becomes

$$
  \array{
    X &\stackrel{\phi_{bg}}{\to}& \mathbf{B}G^{bg}_{conn}
    \\
    \downarrow &\swArrow_{\hat F}& \downarrow^{\mathrlap{\hat \mathbf{c}}}
    \\
    \Omega^2(-) &\stackrel{}{\to}& \mathbf{B}^n U(1)_{conn}
  }
  \,.
$$

We can then subsume all this and consider the smooth collection of all such twisting background fields $\phi^{bg}$ and twisted gauge fields $\hat F$. By general reasoning, this is given by the [[homotopy pullback]] that universally completes the above diagram

$$
  \array{
    \mathbf{Fields} &\stackrel{\phi_{bg}}{\to}& \mathbf{B}G^{bg}_{conn}{}^{univ}
    \\
    \downarrow &\swArrow_{\hat F^{univ}}& \downarrow^{\mathrlap{\hat \mathbf{c}}}
    \\
    \Omega^2(-) &\stackrel{}{\to}& \mathbf{B}^n U(1)_{conn}
  }
$$

#### Infinitesimal moduli stacks: BRST complexes

So far we are talking about [[gauge fields]] and [[higher gauge fields]] on which we are evaluating an [[action functional]] (see below). Eventually one wants to [[quantization|quantize]] such a setup. There are two issues with this: first of all the action functional needs to be well-defined in the first place, we get to in the next point. But second, once we have a well-defined action functional on gauge fields, the only way to quantize this is to invove [[BV-BRST formalism]]: we need the [[BRST complex]] of the gauge fields. 

or ordinary gauge theory this is the [[Lie algebroid]] of the smooth version $[X, \mathbf{B}G_{conn}]$

$$
  BRST  = C^\infty Lie([X, \mathbf{B}G_{conn}])
  \,.
$$

Similarly for higher gauge theory it is the [[L-infinity algebroid]].

#### Extended higher Chern-Simons-type functionals

The anomaly line bundle to be discussed in a moment [below](GaugeInteractionAndChargeAnomaly) is a special case of a general construction in extended "[[schreiber:∞-Chern-Simons theory]]". So before getting to that special case, we indicate here the general pattern.

The [[action functional]] of ordinary [[Chern-Simons theory]] is traditionally taken to be simply a [[function]], for a gven compact 3-manifold $\Sigma_3$, 

$$
  \exp( i S_{cs}) : G Bund_\nabla(\Sigma_3)
  \to U(1)
$$

on $G$-[[principal connections]] over $\Sigma_3$. This perspective can be refined.

First of all, since this function is [[gauge invariance|gauge invariant]] we may think of it as being defined on the full moduli stack

$$
  \exp( i S_{cs}) : [\Sigma_3, \mathbf{B}G_{conn}] \to U(1)
  \,.
$$

This also exhibits the smoothness of the action. 

An important construction in [[Chern-Simons theory]] is the [[geometric quantization]] of this action functional in the case that $\Sigma_3 = \Sigma_2 \times Interval$ , which yields a holomorphic line bundle with connection on the [[covariant phase space]] of the theory, which may be identified with the space of flat connections over a _2-dimensional_ $\Sigma_2$.
Generally, one expects to see a [[circle n-bundle with connection|circle k-bundle with connection]] assigned to a $\Sigma$ of [[codimension]] $k$.

[Above](#DifferentialWhitehead) we had already seen such a structure in top codimension: if $\Sigma = *$ is the point, then $[\Sigma, \mathbf{B}G_{conn}] \simeq [*, \mathbf{B}G_{conn}] \simeq \mathbf{B}G_{conn}$. So there should be a cricle 3-bundle with connection on this moduli stack. Taking $G = Spin$, for definiteness, then the differential first fractional Pontryagin class from [above](#DifferentialWhitehead) is precisely of this form:

$$
  \tfrac{1}{2} \hat \mathbf{p}_1 
    : 
  \mathbf{B} Spinn_{conn}
  \to 
  \mathbf{B}^3 U(1)
  \,.
$$

And indeed, as stated there, this induces the Chern-Simons action functional itself. Indeed, it induces a whole tower of higher circle bundles, in each codimension:

The operation of fiber integration of differential forms extends to an operation of [[fiber integration in ordinary differential cohomology]], which in turn, as discussed there, extends to a morphism of smooth moduli stacks of the form

$$
  \exp(2 \pi i \int_{\Sigma_k}(-))
  :
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
  \to
  \mathbf{B}^{n-k} U(1)_{conn}
  \,.
$$

If now

$$
  \hat \mathbf{c}
  : 
  \mathbf{B}G_{conn}
   \to 
  \mathbf{B}^n U(1)_{conn}
$$

is any universal differential characteristic map, and $\Sigma_k$ is compact closed of dimension $k$, then the composite

$$  
  \exp(2 \pi i \int_{\Sigma_k} \hat \mathbf{c})
  : 
  [\Sigma_k, \mathbf{B}G_{conn}]
   \stackrel{[\Sigma_k, \hat \mathbf{c}]}{\to}
  [\Sigma_k, \mathbf{B}^n U(1)_{conn}]
   \stackrel{\exp(2 \pi i \int_{\Sigma_k} (-))}{\to}
  \mathbf{B}^{n-k} U(1)_{conn}
$$ 

is a "$k$-extended action functional".

An important class of [[schreiber:∞-Chern-Simons theories]] arising this way come from $\hat \mathbf{c}$ that are [[cup product|cup products]] of two other differential classes ([FSSd](#FSSd)). For instance in ordinary abelian [[higher dimensional Chern-Simons theory]] one starts with the tautological differential class

$$
  \hat \mathbf{DD}  
    : 
  \mathbf{B}^{2k+1} U(1)_{conn} 
    \to 
  \mathbf{B}^{2k+1} U(1)_{conn}
$$

and then forms its [[differential cup product]] ([FSSd](#FSSd))

$$
  \hat \mathbf{c} 
  \coloneqq
  \mathbf{B}^{2k+1} U(1)_{conn}   
  \stackrel{}{\to}
  \mathbf{B}^{2k+1} U(1)_{conn} \times   
  \mathbf{B}^{2k+1} U(1)_{conn}
  \stackrel{\hat \mathbf{DD} \cup \hat \mathbf{DD}}{\to}
  \mathbf{B}^{4k + 3} U(1)_{conn}
  \,.
$$

The action functional induced by this is that of $(4k+3)$-dimensional [[higher dimensional Chern-Simons theory]] which sends those $(2k+1)$-form fields $C$ whose underlying bundle happens to be trivial to 
$\exp(2 \pi i\int_{\Sigma_{4k+3}} C \wedge d_{dR} C)$.

The anomaly line bundle which we now turn to arises in this kind of way, only for the slightly more general case that the [[schreiber:∞-Chern-Simons theory]] involved is not given by a differential square, but by a genuine differential cup of two different cocycles: the electric and the magnetic differential cocycles.


#### Gauge interaction and the charge anomaly
 {#GaugeInteractionAndChargeAnomaly}

We discuss now how the action functional of the (higher) gauge theory in the presence of [[electric charge]] [[current]] and [[magnetic charge]] [[current]] has in general an [[quantum anomaly|anomaly]], but this anomaly exhibits itself, in traditional language, as something living over _families_ of gauge fields. But by the formula for the [[internal hom]] of sheaves/stacks

$$
  [X, \mathbf{Fields}] : U \mapsto 
  \mathbf{H}(X \times U, \mathbf{B}G^{bg}_{conn})
  = 
  \{
   background\;gauge\;fields\; on\; X \times U
  \}
  = 
  \{
    U-parameterized\;famlily\;of\;gauge\;fields\; on\; X 
  \}
$$

this means effectively to work over the _smooth moduli stack of fields_ itself. Notably, the anomaly is going to be (the non-triviality of) a [[circle n-bundle with connection|circle bundle with connection]] on "the space of all fields", so we certainly need a smooth structure on that space. We indicate now how that line bundle 

$$
  \nabla_{anomaly} : [X, \mathbf{Fields}]  \to \mathbf{B}U(1)_{conn}
$$ 

appears.


First, the kinetic piece of the action functional is simply $\exp(i S_{kin}(\hat F)) = \exp(i \int_X F \wedge \ast F)$.

But suppose there is a charged particle with trajectory $\gamma : S^1 \to X$. Then there is an interaction term 
$\exp(2\pi i \int_{S^1} \gamma^* A)$. Let $J_{el}$ be the [[Poincare duality|Poincare dual]] form. Then $\cdots = \exp(i \int_X A \wedge J_{el})$. 

This may be expressed using the [[Beilinson-Deligne cup product]] and the [[fiber integration in ordinary differential cohomology]] as $\exp(2 \pi i \int_X \hat \mathbf{c}_{el} \cup \hat F)$. (Here is where we need $J_{el}$ to have [[compact support]].) This is a differential 2-cocycle on the [[moduli stack]] of field configurations: by the formula for the [[internal hom]] and for forms on a stack, we are evaluating for each test manifold $U$ on families of fields over $X \times U$ and then integrate out over $X$.

But in the case where there is non-trivial $\hat \mathbf{c}_{mag}$ this is no longer the case, there instead this is a trivialization of a twist

$$
  \omega \stackrel{\exp(2 \pi i \int_X \hat \mathbf{c}_{el} \cup \hat F)}{\to}
  \exp(2 \pi i \int_X \hat \mathbf{c}_{el} \cup \hat \mathbf{c}_{mag})
  \,.
$$

Moreover, this twist matters in [[compactly supported cohomology]] (this is what [[fiber integration in ordinary differential cohomology]] sees), where it is in general not trivialized. So the action functional is not a function, but a [[section]] of a line bundle. Its [[first Chern class]] is the 2-class of 

$$
  \nabla_{higher\;gauge\;anomaly}
  :
  [X, \mathbf{Fields}]
  \stackrel{
    \exp(2 \pi i \int_X \hat \mathbf{c}_{el} \cup \hat \mathbf{c}_{mag})
  }
  {
    \to
  }
  \mathbf{B} U(1)_{conn}
$$ 

This is the _anomaly line bundle with connection on the moduli stack of fields_.

For this to cancel, there needs to be a fermionic anomaly -- the [[Pfaffian line bundle]] of the [[Dirac operators]] on the fermions in the theory -- of the same structure. 

$$
  \nabla_{fermion\;anomaly}
  :
  [X, \mathbf{Fields}]
  \to 
  \mathbf{B} U(1)_{conn}
  \,.
$$

The total action functional (higher gauge fields and fermions) is a section of the [[tensor product]] of these two

$$
  \nabla_{total\;anomaly}
  = 
  \nabla_{higher\;gauge\;anomaly} \otimes \nabla_{fermion\;anomaly}  :
  [X, \mathbf{Fields}]
  \to 
  \mathbf{B} U(1)_{conn}
  \,.
$$

The action functional needs to be a flat [[section]] of $\nabla_{total\;anomaly}$. Hence the two line bundles need to be inverse to each other. 
This condition is the [[Green-Schwarz mechanism]].




### **III)** $Spin^c$-, $String^c$-, $Fivebrane^c$-structure 
 {#TwistedK}

In the [previous section](#SpinStringFivebraneStructures) we have considered higher differential structures originating in the [[orthogonal group]]. In applications to [[string theory]] these structures receive twists originating in the [[unitary group]] (or representations through the unitary group of groups like [[E8]]). (The orthogonal structures correspond to the field of [[gravity]], while the unitary structures correspond to [[gauge fields]].)

Accordingly, the [above Whitehead tower](#WhiteheadTower) of $\mathbf{B}O$ has stage-wise _[[unitary group|unitary]] twistings_. In the first stage this is given by the familiar [[spin^c]]-group, then there is a [[String^c 2-group]], etc.

After discussing some generalities of these higher unitary-twisted connected covers of the orthogonal group [below](#HigherUnitaryTwistedCovers) we then turn to discussing a list of twisted structures and their appearance in string theory:

| unitary-twisted higher orthogonal structure| role in string theory |
|--|--|
| [[twisted spin^c structure|twisted differential spin^c structure]] | [[Freed-Witten anomaly cancellation]] for [[type II string theory|type II strings]] on [[D-branes]]|
| [[supergravity C-field|twisted differential String^c-structure]] | flux quantization in [[11-dimensional supergravity|11d sugra]]/[[M-theory]] with [[M5-branes]] |
|  [[twisted differential string structure]] | [[Green-Schwarz mechanism]] in [[heterotic string theory]] |
|  [[twisted differential fivebrane structure]] | [[Green-Schwarz mechanism]] in [[dual heterotic string theory]] |




#### Higher unitary-twisted covers of $O$
 {#HigherUnitaryTwistedCovers}

The [[Lie group]] [[spin^c]] is traditionally defined by the formula

$$
  Spin^c \coloneqq Spin \times_{\mathbb{Z}_2} U(1) = (Spin \times U(1))/{\mathbb{Z}_2}
  \,,
$$

which denotes the [[quotient]] of the product $Spin \times U(1)$ by the [[diagonal]] [[action]] induced by the common canonical [[subgroup]] [[group of order 2|of order 2]].

For our purposes it is useful to think of this as follows. We have the $\mathbf{B}\mathbb{Z}_2$-[[associated infinity-bundle|higher fiber bundle]] classified by the smooth [[second Stiefel-Whitney class]]

$$
  \array{
    \mathbf{B} \mathbb{Z}_2 &\to& \mathbf{B} Spin
    \\
    && \downarrow
    \\
    && \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}
  }
$$

and we also have the [[associated infinity-bundle|higher fiber bundle]]

$$
  \array{
    \mathbf{B} U(1) &\stackrel{\cdot 2}{\to}& \mathbf{B} U(1)
    \\
    && \downarrow^{\mathrlap{\mathbf{c}_1 mod 2}}
    \\
    && \mathbf{B}\mathbb{Z}_2
  }
$$

which is $\mathbb{Z}_2$-[[associated infinity-bundle|associated]] to the [[universal principal bundle]] universal $\mathbb{Z}_2$-bundle.

One finds, using the presentation of these maps as discussed [above](#SmoothWhitehead), that $\mathbf{B}Spin^c$ is the corresponding [[associated infinity-bundle|associated bundle]], namely the [[homotopy pullback]]

$$
  \array{
    \mathbf{B}Spin^c &\to& \mathbf{B}U(1)
    \\
    \downarrow && \downarrow^{\mathrlap{\mathbf{c}_1 mod 2}}
    \\
    \mathbf{B} SO &\stackrel{\mathbf{w}_2}{\to}& \mathbf{B}^2 \mathbb{Z}_2
  }
  \,.
$$

Equivalently we may write this as a [[Mayer-Vietoris sequence]] and thus obtain the universal local $\mathbf{B}Spin^c$-coefficient bundle over $\mathbf{B}^2 \mathbb{Z}$

$$
  \array{
    \mathbf{B}Spin^c &\to& \mathbf{B} (SO \times U(1))
    \\
    && \downarrow^{\mathrlap{\mathbf{w}_2 - \mathbf{c}_1 mod 2}}
    \\
    && \mathbf{B}^2 \mathbb{Z}_2
  }
$$

We may read this as saying:

_Where the moduli stack $\mathbf{B}Spin$_ is the homotopy fiber of the smooth second Stiefel-Whitney class $\mathbf{w}_2$, the moduli stack  $\mathbf{B}Spin^c$ is that homotopy fiber universally twisted by the smooth [[first Chern class]] $\mathbf{c}_1 mod 2$._

In the following we consider higher analogs of this, where homotopy fibers of "orthogonal classes" are twisted by "unitary classes".

In particular, one step higher in the [Whitehead tower of BO](#WhiteheadTower), we can twist the smooth [[first fractional Pontryagin class]] with the smooth [[second Chern class]] to obtain the [[delooping]] of the smooth [[String^c 2-group]]

$$
  \array{
    \mathbf{B} String^{\mathbf{c}_2} &\to& \mathbf{B}(Spin \times SU)
    \\
    && \downarrow^{\mathrlap{\tfrac{1}{2}\mathbf{p}_1 - \mathbf{c}_2 }}
    \\
    && \mathbf{B}^3 U(1)
  }
  \,.
$$

This controls the [[supergravity C-field]] in [[M-theory]]/[[11-dimensional supergravity]] as well as the [[Green-Schwarz mechanism]] in [[heterotic string theory]], discussed below.

Before we come to that we consider another variant, since that leads to the most familiar twisting, that of [[twisted K-theory]]. 


One finds that there is also a universal local $\mathbf{B}Spin^c$-coefficient bundle over $\mathbf{B}^2 U(1)$, and this is given by the smooth third [[integral Stiefel-Whitney class]]:

$$
  \array{
    Spin^c &\to& \mathbf{B} SO
    \\
    && \downarrow^{\mathrlap{\mathbf{W}_3}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

Since that now lands in $\mathbf{B}^2 U(1)$, we can apply _one more_ unitary twist by a corresponding class. The canonical such class is the universal [[Dixmier-Douady class]] $\mathbf{dd}$ of (stable) [[projective unitary group|projective unitary]] bundles


$$
  \array{
    \mathbf{B}(Spin^c)^{\mathbf{dd}} &\to& \mathbf{B} ( SO \times PU )
    \\
    && \downarrow^{\mathrlap{\mathbf{W}_3 - \mathbf{dd}}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

This universal local coefficient bundle controls the [[Freed-Witten anomaly cancellation]] in [[type II string theory]]. To which we now turn.



#### **a)** Twisted differential $Spin^c$-structure: Freed-Witten mechanism
 {#BFieldInK}

We discuss aspects of the twisted smooth cohomology involved
over [[D-branes]] in [[type II string theory]]: the [[Freed-Witten anomaly cancellation]] mechanism in terms of [[twisted K-theory]].



For each $n$, the [[central extension]] of Lie groups

$$
  U(1) \to U(n) \to PU(n)
$$

that exhibits the [[unitary group]] as a [[circle group]]-extension of the [[projective unitary group]] induces the corresponding morphism of smooth [[moduli stacks]]

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
  \,.
$$

This is part of a [[fiber sequence|long fiber sequence]] which continues to the right by a [[connecting homomorphism]] $\mathbf{dd}_n$

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
   \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
$$

in $\mathbf{H}$. Here the last morphism is presented in simplicial presheaves by the zig-zag of sheaves of [[crossed modules]]

$$
  \array{
     [U(1) \to U(n)] &\to& [U(1) \to 1]   
     \\
     {}^{\mathllap{\simeq}}\downarrow
     \\
     PU(n)
  }
  \,.
$$

We have seen [above](#SmoothWhitehead) that a morphism $\phi : X \to \mathbf{B}^2 U(1)$ classifies a [[circle n-bundle with connection|circle 2-bundle]] encoded by a Cech 2-cocycle $(\phi_{i j k} : U_i \cap U_j \cap U_k \to U(1))$ . This means that the universal local coefficient bundle

$$
  \array{
     \mathbf{B} U(n) &\to& \mathbf{B} PU(n)
     \\
     && \downarrow^{\mathrlap{\mathbf{dd}_n}}
     \\
     && \mathbf{B}^2 U(1)
  }
$$

induces a notion of unitary bundles that are _twisted_ by a 2-bundle.

Indeed, unwinding the definition one finds that a $\phi$-twisted $\mathbf{dd}_n$ cocycle

$$
  \array{
    X &&\stackrel{h}{\to}&& \mathbf{B} PU(n)
    \\
    & {}_{\mathllap{\phi}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{dd}_n}}
    \\
    &&
    \mathbf{B}^2 U(1)
  }
$$

is, with respect to a resolution of $X$ a [[good open cover]] $\{U_i \to X\}$, given by maps $C(\{U_i\}) \to \mathbf{B}(U(1) \to U(n))$ whose components read

$$
  \left(
  \array{
      && (x,j)
      \\
      & \nearrow &\Downarrow& \searrow
      \\
     (x,i) &&\to&& (x,k)
  }
  \right)
  \;\;\;
  \mapsto
  \;\;\;  
  \left(
    \array{
       && *
       \\
       & {}^{\mathllap{h_{i j}(x)}}\nearrow 
         &\Downarrow^{\phi_{i j k}(x)}& 
  \searrow^{\mathrlap{h_{j k}}}
       \\
      * &&\underset{h_{i k}}{\to}&& *
   }    
  \right)
  \in 
  \mathbf{B}(U(1) \to U(n))
  \,.
$$

Hence these are collections of smooth $U(n)$-valued functions

$$
  (h_{i j} : U_i \cap U_j \to U(n))
$$

which satisfy on triple overlaps the equation

$$
  h_{i j} h_{j k} = h_{i k} \phi_{i j k}
  \,.
$$

If $\phi_{i j k}$ happens to be constant on the neutral element, then this is the condition for a cocycle in $H^1_{smooth}(X, U(n))$. So in general we say it is a _$\phi$-twisted_ such cocycle. And that $(h_{i j})$ classifies a  _$\phi$-[[twisted bundle|twisted unitary bundle]]_. 

In generalization of how unitary bundles constitute cocycles for [[K-theory]], these $\phi$-twisted unitary bundles constitute cocycles for [[twisted K-theory]].


For each $n \in \mathbb{N}$ there is a canonical inclusion $\mathbf{B} U(n) \to \mathbf{B} U(n+1)$, exhibiting the fact that a rank-$n$ complex vector bundle canonically induces a rank-$(n+1)$-bundle by added a trivial line bundle.

To get rid of the dependence on the rank $n$ -- to _stabilize_ the rank -- 
we may form the [[directed colimit]] of smooth moduli stacks

$$
  \mathbf{B}U \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} U(n)
$$


**Proposition** The smooth stack $\mathbf{B} U$ is a smooth refinement of the [[classifying space]] [[BU|$B U$]] of reduced [[K-theory]]. Also, for $X$ a [[compact topological space|compact]] [[smooth manifold]] smooth $U$-principal bundles and smooth $U$-gauge transformations on $X$ are represented by ordinary $U(n)$-bundles for some finite $n$.

$$
  \mathbf{H}(X, \mathbf{B}U)
  \simeq
  \underset{\rightarrow_n}{\lim} \mathbf{H}(X, \mathbf{B} U(n))
  \,.
$$

Now we think of the manifold $X$ as a [[target space]] for the [[type II superstring]], hence assume it to be orientable and spin: $w_1(X) = 0 $ and $w_2(X) = 0$. Consider moreover a [[submanifold]]

$$
  \iota : Q \hookrightarrow X
  \,,
$$

to be thought of as the [[worldvolume]] of a [[D-brane]], which is also or orientable and spin.

Assume first that $Q$ also admits a [[spin^c structure]], hence that also the third [[integral Stiefel-Whitney class]] vanishes $W_3(Q) = 0$.

We can consider then a cocycle in the $\iota$-[[relative cohomology]] with coefficients in $\mathbf{dd}$, namely a diagram

$$
  \array{
    Q &\stackrel{\phi_{ga}}{\to}& \mathbf{B} P U(n) 
    \\
    {}^{\mathllap{i}}\downarrow 
      &\swArrow_\simeq& \downarrow^{\mathrlap{\mathbf{dd}_n}}
    \\
    X &\stackrel{\phi_B}{\to}& \mathbf{B}^2 U(1)
  }
  \;\;\;\;
   \leftrightarrow
  \;\;\;
  \array{
    Q &&\stackrel{\phi_{ga}}{\to}&& \mathbf{B} P U(n)
    \\
    & {}_{\mathllap{\phi_B|_Q}}\searrow &\swArrow& \swarrow_{\mathrlap{\mathbf{dd}}}
    \\
    && \mathbf{B}^2 U(1)
  }
$$

in $\mathbf{H}$.


This is 

1. a [[circle n-bundle with connection|circle 2-bundle]] $\phi_B : X \to \mathbf{B}^2 U(1)$ on [[spacetime]] $X$: the underlying bundle of the [[B-field]];

1. a projective unitary bundle $\phi_{ga}$ on $Q$, a [[Chan-Paton bundle]] on the D-brane;

* together with an identification of the restriction $\phi_{B}|_Q$ of the $B$-field to the $D$-brane with the [[obstruction]] $\mathbf{dd}(\phi_{ga})$ to lift $\phi_{ga}$ to a genuine unitary bundle.

In [[cohomology]] this says that 

$$
  [\mathbf{dd}(\phi_{ga})] = [\phi_B|_Q] \;\; \in H^3(Q)
  \,.
$$

This is the _[[Freed-Witten anomaly cancellation]] condition_ for $D$-branes with [[spin^c structure]].

More generally, if $Q$ does not necessarily have $Spin^c$-structure, we consider $\iota$-[[relative cohomology]] with coefficients in the universal local coefficient bundle $\mathbf{dd} - \mathbf{W}_3$:

$$
  \array{
    Q &\stackrel{(T X, \phi_{ga})}{\to}& \mathbf{B} ( SO \times P U(n)) 
    \\
    {}^{\mathllap{i}}\downarrow 
      &\swArrow_\simeq& \downarrow^{\mathrlap{\mathbf{dd}_n - \mathbf{W}_3}}
    \\
    X &\stackrel{\phi_B}{\to}& \mathbf{B}^2 U(1)
  }
  \;\;\;\;
   \leftrightarrow
  \;\;\;
  \array{
    Q &&\stackrel{(T X, \phi_{ga})}{\to}&& \mathbf{B} (SO \times P U(n))
    \\
    & {}_{\mathllap{\phi_B|_Q}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{dd}_n-\mathbf{W}_3}}
    \\
    && \mathbf{B}^2 U(1)
  }
  \,.
$$

This now is equivalently a twisted Chan-Paton bundle and a $B$-field such that in cohomology

$$
  [\mathbf{dd}(\phi_{ga})] + [W_3(Q)] = [\phi_B|_Q] \;\;\; \in H^3(X, \mathbb{Z})
  \,.
$$

This is the [[Freed-Witten anomaly cancellation]] condition for general $Q$.

#### **b)** Twisted differential $String^{\mathbf{c}_2}$-structure: M-theory flux quantization
 {#SuGraFluxQuantization}

We discuss the twisted smooth cohomology of the
[[supergravity C-field]] in [[11-dimensional supergravity]]/[[M-theory]].
With the smooth and differential refinement of the 
Whitehead tower in hand, this proceeds essentially in higher analogy to the 
[previous example](#BFieldInK).

From the [[effective QFT]] of [[11-dimensional supergravity]] the bosonic massless field content consists locally of the [[graviton]] and a 3-form $C$. We have the following information on how a model of this field content must behave globally


1. Due to the existence of [[spinors]], the graviton must be part of a [[spin connection]]:

   $$
     \phi_{gr} : X \to \mathbf{B}Spin_{conn}
     \,.
   $$

1. Due to the coupling to the [[M2-brane]] the 3-form must lift to a well-dfined [[higher holonomy|3-holonomy]] and hence must globally be a [[circle n-bundle with connection|circle 3-bundle with connection]]

   $$
     \phi_C : X \to \mathbf{B}^3 U(1)_{conn}
     \,.
   $$

1. Due to the coupling to the [[M5-brane]], there is an auxiliary [[E8]]-bundle 

   $$
     \phi_{ga} : X \to \mathbf{B} E_8
   $$

   and these fields must satisfy what in string theory literature is called the _flux quantization condition_, and what in [Hopkins-Singer 05](#HopkinsSinger) is called an _[[differential integral Wu structure]]_, meaning that in [[cohomology]]

   $$
     [\phi_C]
     = 
     [\frac{1}{2}p_1(\phi_{gr})]
     +
     [2\mathbf{a}(\phi_{ga})]
     \;\;
     \in H^4(X, \mathbb{Z})
     \,.
   $$

(Depending on convention one may write "$2 \phi_C$" for "$\phi_C$" here, regarding the physical $C$-field as being "one half" of the differential cocycle $X \to \mathbf{B}^3 U(1)_conn$ above, see the remark [below (1.2)](arxiv.org/pdf/hep-th/9609122v2.pdf#page=2) in [[Edward Witten|Witten]]'s [arXiv:hep-th/9609122](http://arxiv.org/abs/hep-th/9609122)).

A [[discrete infinity-groupoid|discrete]] 1-groupoid model satisfying these points has been by [[Dan Freed|Freed]]-[[Greg Moore|Moore]] and others (see the references [here](supergravity+C-field#References)). Using [[cohesive homotopy type theory]] and following ([FSSc](#FSSc)) we now obtain naturally a genuine [[moduli infinity-stack|smooth moduli 3-stack]] of such field configurations: the [[categorical semantics|interpretation]] of the evident expression

$$
  \mathbf{CField}(X)
   \coloneqq
    \left\{
      \phi_{gr}, \phi_{ga}, \phi_{C}
      |
      \frac{1}{2}\mathbf{p}_1(\phi_{gr})
      +
      2\mathbf{a}(\phi_{ga})
      \simeq
      \phi_C
  \right\}
$$

in [[homotopy type theory]] is (see [[HoTT methods for homotopy theorists]] for how this works) the smooth $\infty$-stack 
$\mathbf{CField} \in \mathbf{H}$ given as the 
[[homotopy pullback]] 

$$
  \array{
     \mathbf{CField} &\to& \mathbf{B} Spin_{conn} \times \mathbf{B}E_8
	 \\
	 \downarrow &\swArrow_{\simeq}& \downarrow^{\tfrac{1}{2}\mathbf{p}_1 + 2\mathbf{a}}
	 \\
	 \mathbf{B}^3 U(1)_{conn} &\stackrel{}{\to}& \mathbf{B}^3 U(1)
  }
  \,.
$$

On the right this has the universal local coefficient bundle for $\mathbf{String}^{2\mathbf{a}}$ from [above](#HigherUnitaryTwistedCovers), and hence this identifies a [[gravity]]-[[supergravity C-field|C-field]] configuration as being (a partial differential refinement of) a $[\phi_C]$-twisted $String^{2\mathbf{a}}$-structure.



#### **c)** Twisted differential String-structure -- Green-Schwarz mechanism
 {#TwistedStringStructure}


By [[Hořava-Witten theory]], the 10-dimensional [[target space|target]] [[spacetime]] of the 
[[heterotic string]] may be understood as being a boundary 
(or rather $\mathbb{Z}_2$-[[orbifold]] fixed points, see [below](#HWCompactifications)) of the 11-dimensional
spacetime of [[11-dimensional supergravity|11d SuGra]]. 
Over this boundary 

1. the [[curvature]] 4-form $G_4(\phi_C)$ vanishes;

1. and the $E_8$-[[principal bundle]] picks up a [[connection on a bundle|connection]]. 

This means that the [above](#SuGraFluxQuantization) defining homotopy pullback for $\mathbf{CField}$ goes over
into the one that defines the differential refinement $String^{\mathbf{a}}_{conn'}$
of $String^{\mathbf{a}}$:

$$
  \array{
     \mathbf{B}String^{\mathbf{a}}_{conn'} 
       &\to& 
      \mathbf{B} Spin_{conn} \times \mathbf{B}(E_8 \times E_8)_{conn}
	 \\
	 \downarrow &{}^{\mathllap{\phi_B}}\swArrow_{\simeq}& 
         \downarrow^{\tfrac{1}{2}\hat \mathbf{p}_1  + \hat \mathbf{a}}
	 \\
	 \Omega^3_{cl}(-) & \stackrel{\phi_C}{\hookrightarrow} & \mathbf{B}^3 U(1)_{conn}
  }
  \,.
$$

On cohomology classes this means that 

$$
  [\tfrac{1}{2}p_1(\phi_{gr})] = [a(\phi_{ga})] \;\; \in H^4(X, \mathbb{Z})
  \,.
$$

This is the integral part of the [[Green-Schwarz mechanism]] for the [[heterotic string theory|heterotic string]]. 

Since this is now refined not just to cocycles, but to differential cocycles -- to $\mathrm{String}^{\mathbf{a}}$-[[connection on a 2-bundle|2-connections]], 
there is, locally over a cover $\{U_i \to X\}$, also an equation of differential 
forms that exhibits this in de Rham cohomology. 

A morphism $X \to String^{2\mathbf{a}}_{conn}$ classifies field content that is expressed with respect to a [[good open cover]] $\{U_i \to X\}$ in particular over single patches $U_i$ by  ([SSSa](#SSSa), [FSSa](#FSSa))

* the [[connection on a bundle|gauge connection]] $A_i \in \Omega^1(U_i, \mathfrak{e}_8 \oplus \mathfrak{e}_8)$;

* the [[spin connection]] $\omega_i \in \Omega^1(U_i, \mathfrak{so})$ (the field of [[gravity]] in [[first order formulation of gravity]]);

* the [[B-field]] $\phi_B \in \Omega^2(U_i)$;

which come with [[curvature]]/[[field strength]] forms

* $F_{A_i} = d_{dR} A_i + \tfrac{1}{2}[A_i \wedge A_i]$

* $F_{\omega_i} = d_{dR} \omega_i + \tfrac{1}{2}[\omega_i \wedge \omega_i]$;

* $H_i = d B_i + CS(\omega_i) - CS(A_i)$ ($B$-field strength shifted by the difference of the [[Chern-Simons forms]] of $A_i$ and $\omega_i$);

satisfying the (twisted) [[Bianchi identities]] ([SSSa](SSSa)))

* $d_{dR} F_{A_i} + [A_i \wedge F_{A_i}] = 0$;

* $d_{dR} F_{\omega_i} + [\omega_i \wedge F_{\omega_i}] = 0$;

* $d_{dR} H = \langle F_\omega \wedge F_\omega \rangle  - \langle F_A \wedge F_A \rangle$

(together with more local cocycle components on higher overlaps). Notably the twisted Bianchi identity of $H$ exhibits the above cohomological identity in de Rham cocycles. 

These formulas characterize the
[[Green-Schwarz mechanism|Green-Schwarz anomaly cancellation conditions]] on the [[background gauge field]] content, that makes the heterotic string be well defined. Accordingly, $String^{\mathbf{a}}_{conn}$ is the [[smooth infinity-groupoid|smooth]] [[moduli infinity-stack|moduli 2-stack]] of anomaly free heterotic background fields (in the massless bosonic sector).

Notice that if the twist $\tfrac{1}{2}\hat \mathbf{p_1}(\phi_{gr}) - \hat\mathbf{a}(\phi_{gau})$ happen to vanish (say because both the field of gravity and the gauge field are trivial), then the above homotopy pullback reduces to 

$$
  \array{
     \mathbf{B}^2 U(1)_{conn}
       &\to& 
      *
 	 \\
	 \downarrow &{}^{\mathllap{\phi_B}}\swArrow_{\simeq}& 
         \downarrow^{}
	 \\
	 \Omega^3_{cl}(-) & \stackrel{\phi_C}{\hookrightarrow} & \mathbf{B}^3 U(1)_{conn}
  }
$$

and exhibits $\phi_B$ as a genuine [[circle n-bundle with connection|circle 2-bundle with connection]] (and its 3-form curvature $H$ with $\phi_C$.). Conversely, this shows how in the general situation $\phi_B$ is a _twisted_ circle 2-bundle, with the twist given by the "magnetic fivebrane current" $\tfrac{1}{2}\hat \mathbf{p}_1(\phi_{gr}) - \hat \mathbf{a}(\phi_{ga})$.



#### **d)** Twisted differential Fivebrane structure -- dual Green-Schwarz mechanism

(...)






### **IV)** Higher orientifold structure 
 {#HigherOrientifold}



#### Orientifolds

An _[[orientifold]]_ [[target space]] for the bosonic string is a 
[[smooth manifold]] or more generally [[orbifold]] $X$ equipped with 

* a [[double cover]] $w_X : X \to \mathbf{B} \mathbb{Z}_2$;

* a twisted $\mathbb{Z}_2$-equivariant circle 2-bundle, given by a morphism $\phi_B : X \to \mathbf{B}Aut(\mathbf{B}U(1))$ whose underlying double cover is $w$.

This means that this background is a cocycle in $w$-twisted cohomology for the local coefficient bundle 

$$
  \array{
    \mathbf{B}U(1) &\to& \mathbf{B}Aut(\mathbf{B}U(1))
    \\
    && \downarrow^{\mathbf{J}}
    \\
    && \mathbf{B}\mathbb{Z}_2
  }
  \,.
$$

Hence the [[B-field]] is now a cocycle in $w$-twisted cohomology

$$
  \phi_b \in \mathbf{H}_{/\mathbf{B}\mathbb{Z}_2}( w_X , \mathbf{J})
  \,,
$$

or rather a differential refinement thereof. For $\Sigma$ the [[worldvolume]] of a [[string]], an orientifold string configuration is a cocycle

$$
  (\varphi, \nu) \in \mathbf{H}_{/\mathbf{B}\mathbb{Z}_2}(\mathbf{w}_1(\Sigma), w_X)
  \,,
$$


given in $\mathbf{H}$ by a diagram

$$
  \array{
    \Sigma &&\stackrel{\varphi}{\to}&& X
    \\
    & {}_{\mathllap{\mathbf{w}_1}}\searrow 
     &{}^{\nu}\swArrow_{\simeq}& \swarrow_{\mathrlap{w_X}}
    \\
    && \mathbf{B}\mathbb{Z}_2
  }
$$

consisting of 

* a map $\varphi : \Sigma \to X$;

* an [[isomorphism]] $\nu : \varphi^* w_X \to \mathbf{w}_1(\Sigma)$.


#### Ho&#345;ava-Witten compactifications
 {#HWCompactifications}


In [[Hořava-Witten theory]] there is similarly a twisted $\mathbb{Z}_2$-action on the [[supergravity C-field]], exhibited by a local coefficient bundle

$$
  \array{
    \mathbf{B}^2U(1) &\to& \mathbf{B}Aut(\mathbf{B}^2U(1))
    \\
    && \downarrow^{\mathbf{J}}
    \\
    && \mathbf{B}\mathbb{Z}_2
  }
  \,.
$$


### Further twists

There are various further twisted cohomological structures in string theory known or conjectured (for some of which possibly no smooth refinement has been constructed yet). We briefly list some of them.

#### Twisted super bundle
 {#TwistedSuperBundle}

In work like _[[Loop Groups and Twisted K-Theory]]_ the following structure plays a role:

for $G$ a [[group]], let 

$$
  \epsilon : G \to \mathbb{Z}_2
$$

be a fixed group homomorphism. Then for $E = E_0 \oplus E_1 \to X$ a [[super vector bundle]], an "$\epsilon$-twist" of $E$ is an [[action]] of $G$ on $E$ such that an element $g \in G$ acts by an even automorphism if $\epsilon(g)$ is even, and by an odd automorphism if $\epsilon(g)$ is odd ([Freed ESI lecture, (1.13)](#FreedLecture)).

This is a special case of the general notion of twist discussed here by considering the canonical morphism 

$$
  \array{
    \mathbf{B}Aut(E)
    \\
    \downarrow^{\mathbf{e}}
    \\
    \mathbf{B} \mathbb{Z}_2
  }
$$

as the local coefficient bundle, and considering $\epsilon$ as the twist: then an $\epsilon$-twisting as above is a cocycle in the twisted cohomology $\mathbf{H}_{/\mathbf{B}\mathbb{Z}_2}(\mathbf{B}\epsilon, \mathbf{e})$ given by a commuting triangle

$$
  \array{
     \mathbf{B}G &&\to&& \mathbf{B}Aut(E)
     \\
     & {}_{\mathllap{\mathbf{B}\epsilon}}\searrow && \swarrow_{\mathrlap{\mathbf{e}}}
     \\
     && \mathbf{B}\mathbb{Z}_2
  }
  \,.
$$

#### Relative fields
 {#RelativeFields}

Meanwhile in ([Freed-Teleman 2012](#FreedTeleman)) special cases of the general notion of _twisted fields_ [above](#TableOfTwists) are being called _relative fields_. We briefly spell out how the definitions considered in that article are examples of the general notion above. 

For $\pi \in Grp(Set) \hookrightarrow Grp(Smooth\infty Grpd)$ a [[discrete group]] and for $\overline{X} \in \mathbf{H} \coloneqq$ [[Smooth∞Grpd]] any object (for instance a [[smooth manifold]]) a morphism $\phi_{\overline{X}} \colon \overline{X} \to \mathbf{B}\pi$ modulates a $\pi$-[[principal bundle]] $X \to \overline{X}$ over $X$, hence a free $\pi$-[[action]] on $X$ such that $X \to \overline{X}$ is the [[quotient]] map. 

Then the corresponding [[twisted cohomology]] $\mathbf{H}_{/\mathbf{B}\pi}(-, \phi_{\overline{X}})$ has 

1. domains are objects $\Sigma$ equipped with a $\pi$-[[principal bundle]], modulated by a morphism $\phi_\Sigma \colon \Sigma \to \mathbf{B}\pi$;

1. cocycles are morphism $\phi_\Sigma \to \phi_X$ in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}\pi}$, hence [[diagrams]] of the form

   $$
     \array{
     \Sigma &&\stackrel{f}{\to}&& \overline{X}
     \\
     & {}_{\mathllap{\phi_\Sigma}}\searrow &\swArrow_{\theta}& \swarrow_{\mathrlap{\phi_X}}
     \\
     && \mathbf{B}\pi
     }
   $$

   in $\mathbf{H}$, hence maps $f \colon \Sigma \to \overline{X}$ equipped with equivalences

   $$
    \theta \colon f^* \phi_X \stackrel{\simeq}{\to} \phi_\Sigma
    \,.
   $$

This class of examples is what appears as def. 3.4 in ([Freed-Teleman](#FreedTeleman)). It contains in particular the above examples of _[Reduction of structure group](#ReductionOfTheStructureGroup)_ and [its differential refinement](#SpinConnection).

Next, consider a compact Lie group $\overline{G}$ and a central [[group extension]] $\pi \to G \to \overline{G}$. This is classified by a cocycle 

$$
  \mathbf{c} \colon \mathbf{B}\overline{G} \to \mathbf{B}^2 \pi
  \,.
$$

Then the corresponding twisted cohomology $\mathbf{H}_{/\mathbf{B}^2 \pi}(-, \mathbf{c})$ has

1. domains are objects $\Sigma$ equipped with a $\mathbf{B}\pi$-[[principal 2-bundle]]/[[bundle gerbe]] modulated by a morphism $\phi_\Sigma \colon \Sigma \to \mathbf{B}^2 \pi$;

1. cocycles are morphism $\phi_\Sigma \to \mathbf{c}$ in the [[slice (∞,1)-topos]] $\mathbf{H}_{/\mathbf{B}^2\pi}$, hence [[diagrams]] of the form

   $$
     \array{
     \Sigma &&\stackrel{f}{\to}&& \overline{X}
     \\
     & {}_{\mathllap{\phi_\Sigma}}\searrow &\swArrow_{\theta}& \swarrow_{\mathrlap{\mathbf{c}}}
     \\
     && \mathbf{B}^2\pi
     }
   $$

   in $\mathbf{H}$, hence maps $f \colon \Sigma \to \overline{X}$ equipped with equivalences

   $$
     \theta \colon \mathbf{c}(f) \stackrel{\simeq}{\to} \phi_\Sigma
   $$

   between the principal 2-bundle/bundle gerbe $\mathbf{c}(f)$ induced by the $\overline{G}$-principal bundle modulated by $f$, and the one modulated by $\phi_\Sigma$.

Alternatively one can use here the differential refinement of $\mathbf{B}\overline{G}$ to the [[moduli stack]] $\mathbf{B}\overline{G}_{conn}$ of $\overline{G}$-[[principal connections]].

Examples and further details are discussed in [Schreiber, section 7.1](#Schreiber).  In ([Freed-Teleman](#FreedTeleman)) this example appears as def. 4.6.





#### Twisted tmf

* twisted [[tmf]] and charges for M5-branes ([Ando-Sati](#Ando-Sati)).

#### Twisted Morava K-theory

* twisted  [[Morava K-theory]] ([Sati-Westerland](#SatiWesterland)).

* (...)



## **B)** Local boundary prequantum field theory from twisted smooth cohomology
  {#LocalPrequantumFieldTheory}

> This section originates in some talk notes ([Schreiber, Twists 2013](#SchreiberTwists2013)).

We indicate now how the twisted smooth cohomology data as in the examples above induces and in fact corresponds to data for [[prequantum field theory]] [[sigma-models]] _localized_ (in the sense of the [[cobordism hypothesis]]) to [[local prequantum field theory]] ([lpqft](#lpqft)).

In order to formalize this accurately, we first talk a bit more about the relevant [[cohesion]], [[differential cohesion]] and [[tangent cohesion]]. The way to understand this is as follows:

In full generality, [[cohomology]] (see there for details) is what is given by the [[(∞,1)-categorical hom-spaces]] in some [[∞-topos]]: for $X,A \in \mathbf{H}$ any two [[objects]], then

$$
  H(X,A) \coloneqq \pi_0 \mathbf{H}(X,A) 
$$

is the [[cohomology]] of $X$ with [[coefficients]] in $A$.

Therefore it is natural to ask: _What is an [[(∞,1)-topos]] to be like whose intrinsic [[cohomology]] is [[equivariant cohomology|equivariant]] [[twisted cohomology|twisted]] [[generalized (Eilenberg-Steenrod) cohomology|stable]] [[differential cohomology]]?_

And the answer we find is: it is to be the [[tangent (∞,1)-topos]] $T \mathbf{H}$ of a [[cohesive (∞,1)-topos]] $\mathbf{H}$.
  
For more on this see at _[[tangent cohesion]]_.

### Cohesive contexts for equivariant differential twisted cohomology

After the discovery of the role of [[topological K-theory]] in [[D-brane]] phenomena in [[string theory]], the observation that more generally [[M-theory]] involves various other [[twisted cohomology]] theories such as [[tmf]] and [[Morava K-theory]], has notably been highlighted by [[Hisham Sati]], surveyed in ([Sati 10](#Sati10)).

The suggestion that the right context for formulating the smooth and differential refinement of these twisted cohomology theories is the [[(∞,1)-topos]] We

$$
  \begin{aligned}
  \mathbf{H} 
    &= 
   Sh_\infty(SmthMfd) 
   \\
    & \simeq 
  Funct(SmoothMfd^{op}, KanCplx)[\{stalkwise\;homotopy\;equivalences\}^{-1}]
  \end{aligned}
$$

of [[∞-stacks]] over the [[site]] of [[smooth manifolds]] (the result of universally turning [[stalk|stalkwise]] [[homotopy equivalences]] on [[simplicial presheaf|presheaves of]] [[Kan complexes]] into actual [[homotopy equivalences]]) is due to ([Schreiber 09](#Schreiber09)). 

A full formalization of the classification of [[principal ∞-bundles]] in such [[(∞,1)-topos]], and their classification by [[nonabelian cohomology]] was later given in ([Nikolaus-Schreiber-Stevenson 12](#NSS)).
There it is shown that for $G \in Grp(\mathbf{H})$ an [[∞-group]] of twists, the corresponding [[twisted cohomology]] is the plain cohomology of the [[slice (∞,1)-topos]]

$$
  \mathbf{H}_{/\mathbf{B}G}  \;\; \in (\infty,1)Topos
  \,.
$$ 

Precisely, for $\rho \in \mathbf{H}_{\mathbf{B}G}$ a $G$-[[∞-action]] on some $V$ incarnated as its universal [[associated ∞-bundle]] (the [[local coefficient ∞-bundle]]) and for $\chi \colon X \longrightarrow \mathbf{B}G$ a twist, then the $\chi$-[[twisted cohomology]] with [[local coefficients]] in $V$ is

$$
  \mathbf{H}_{\mathbf{B}G}(\chi_X,\rho)
  =
  \left\{
    \array{
      X && \stackrel{\phi}{\longrightarrow} && V//G
      \\
      & {}_{\mathllap{\chi}}\searrow && \swarrow_{\mathrlap{\rho}}
      \\
      && \mathbf{B}G
    }
  \right\}
  \,.
$$

The observation that for the [[differential cohomology]]-refinement of this [[twisted cohomology|twisted]] geometric cohomology it is the [[adjoint quadruple]] of [[(∞,1)-functors]] between $\mathbf{H}$ to the [[base (∞,1)-topos]] ("[[cohesion]]")

$$
  \mathbf{H}
   \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

(with [[discrete object|Disc]] and [[codiscrete object|coDisc]] [[full and faithful (∞,1)-functors]] and the [[fundamental infinity-groupoid of a locally infinity-connected (infinity,1)-topos|fundamental ∞-groupoid]]/[[geometric realization of cohesive homotopy types|geometric realization]] $\Pi$ [[finite (∞,1)-limit|finite product]]-preserving) which governs all the theory was observed first in ([Sati-Schreiber-Stasheff 09 (11)](SatiSchreiberStasheff09))

There it was shown that this serves to construct and characterize the [[twisted differential string structures]] and [[twisted differential Fivebrane structures]] in ([[dual heterotic string theory|dual]]) [[heterotic string theory]].

A comprehensive theory of ([[twisted cohomology|twisted]] [[equivariant cohomology|equivariant]]) [[differential cohomology]] formulated by just this [[axiom]] of "[[cohesion]]" was then laid out in the thesis ([Schreiber 11](#Schreiber)). Parts of this appear in various articles, such as ([Fiorenza-Schreiber-Rogers 13](FiorenzaRogersSchreiber13)). 
See ([Schreiber Synthetic 13](#SchrThis ieiberSynthetic)) for a fairly comprehensive survey.

Notice that such [[cohesion]] is a very special property of some [[(∞,1)-toposes]], not a generic property. In particular the existence of $\Pi$ means that $\mathbf{H}$ is a [[locally ∞-connected (∞,1)-topos]] and a [[globally ∞-connected (∞,1)-topos]], and the existence of $coDisc$ means that it is a [[local (∞,1)-topos]].

Examples of [[cohesion|cohesive]] [[higher geometry]] established and discussed in ([Schreiber 11](#Schreiber)) include

* [[Euclidean topological ∞-groupoids]] $Sh_\infty(TopMfd)$ is cohesive

* [[smooth ∞-groupoids]] $Sh_\infty(SmoothMfd)$ is cohesive

* [[super ∞-groupoids]] $Sh_\infty(SuperPoints)$ is cohesive;

* [[smooth super ∞-groupoids]] $Sh_\infty(SuperMfd)$ is cohesive over [[super ∞-groupoids]];

* [[synthetic differential ∞-groupoids]] $Sh_\infty(FormalMfds)$ is even "[[differential cohesion|differentially cohesive]]", which allows to [[axiom|axiomatize]] also the notions of _[[manifold]]_, _[[jet bundle]]_ etc.;

* [[synthetic differential super ∞-groupoids]] $Sh_\infty(FormalSuperMfds)$ is [[differential cohesion|differentially cohesive]] over [[super ∞-groupoids]].

Clearly these examples are all of a similar kind (modeled on variants of [[manifolds]]). There are also some [[diagram]] categories which are usefully cohesive, for instance

* [[simplicial objects]] $\mathbf{H}^{\Delta^{op}}$ is cohesive over $\mathbf{H}$ (here $\Pi$ is [[geometric realization]] of simplicial objects in the [[(∞,1)-topos]] $\mathbf{H}$).

In October 2013 [[Charles Rezk]] announced a new kind of cohesion, namely:

* [[global equivariant homotopy theory]] $Sh_\infty(Orb)$ (hence [[(∞,1)-presheaves]] on the global [[orbit category]]) is cohesive (here $\Gamma$ produces [[homotopy quotients]] and $\Pi$ produces topological [[quotients]] of [[topological groups]] acting on [[topological spaces]]).

But of course a central feature desireable for [[cohomology theory]] is [[stabilization]] of cohesion/cohesive [[spectrum objects]].

In ([Bunke-Nikolaus-Völkl 2014](tangent+cohesion#BunkeNikolausVoelkl13)) is considered the [[stabilization]] of [[smooth ∞-groupoids|smooth cohesion]], hence the [[stable (∞,1)-category]] $Stab(Sh_\infty(SmthMfd))$ of [[spectrum object]] in [[smooth ∞-groupoids]], which carries an analogous [[adjoint quadruple]] over the [[(∞,1)-category of spectra]] $Stab(\infty Grpd) \simeq Spectra$

$$
  Stab(Sh_\infty(SmthMfd))
  \stackrel{\overset{\Pi^{stab}}{\longrightarrow}}{\stackrel{\overset{Disc^{stab}}{\leftarrow}}{\stackrel{\overset{\Gamma^{stab}}{\longrightarrow}}{\underset{coDisc^{stab}}{\leftarrow}}}}
  Spectra
  \,.
$$

But this stable aspect is unified with the unstable cohesion by the notion of "[[tangent cohesion]]". This we turn to now.


### Cohesive contexts for stable twisted cohomology


We first discuss generally how the [[tangent (∞,1)-category]] $T \mathbf{H}$ of an [[(∞,1)-topos]] $\mathbf{H}$ is itself an [[(∞,1)-topos]] over the tangent $\infty$-category of the original [[base (∞,1)-topos]] ([Joyal 08](#Joyal08)). Then we observe that $T \mathbf{H}$ is [[cohesion|cohesive]] if $\mathbf{H}$ is and is in fact an [[extension]] of the latter by its [[stabilization]].
 a choice 


#### Tangent $\infty$-topos

+-- {: .num_defn}
###### Definition

Let $seq$ be the [[diagram]] category as follows:

$$
  seq 
  \coloneqq
  \left\{
    \array{
    && \vdots && \vdots
    \\
    && \downarrow && 
    \\
    \cdots &\to& x_{n-1} &\stackrel{p_{n-1}}{\longrightarrow}& \ast
    \\
    &&{}^{\mathllap{p_{n-1}}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_n}} & \searrow^{\mathrm{id}}
    \\
    &&\ast &\underset{i_n}{\longrightarrow}& x_n &\stackrel{p_n}{\longrightarrow}& \ast
    \\
    && &{}_{\mathllap{id}}\searrow& {}^{\mathllap{p_n}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_{n+1}}}
    \\
    && && \ast &\stackrel{i_{n+1}}{\longrightarrow}& x_{n+1} &\to& \cdots
    \\
     && && && \downarrow
     \\
     && && && \vdots
    }
  \right\}_{n \in \mathbb{Z}}
  \,.
$$

=--

([Joyal 08, section 35.5](#Joyal08))

+-- {: .num_remark}
###### Remark

Given an [[(∞,1)-topos]] $\mathbf{H}$, an [[(∞,1)-functor]]

$$
  X_\bullet \;\colon\; seq \longrightarrow \mathbf{H}
$$

is equivalently 

1. a choice of [[object]] $B \in \mathbf{H}$ (the image of $\ast in seq$]);

1. a sequence of objects $\{X_n\} \in \mathbf{H}_{/B}$ in the [[slice (∞,1)-topos]] over $B$;a choi

1. a sequence of [[morphisms]] $X_n \longrightarrow \Omega_B X_{n+1}$ from $X_n$ into the [[loop space object]] of $X_{n+1}$ in the slice.

This is a [[prespectrum object]] in the [[slice (∞,1)-topos]] $\mathbf{H}_{/B}$. 

A [[natural transformation]] 
$f \;\colon \;X_\bullet \to Y_\bullet$ between two such functors with components

$$
  \left\{
  \array{
    X_n &\stackrel{f_n}{\longrightarrow}& Y_n
    \\
    \downarrow^{\mathrlap{p_n^X}} && \downarrow^{\mathrlap{p_n^Y}}
    \\
    B_1 &\stackrel{f_b}{\longrightarrow}& B_2
  }
  \right\}
$$

is equivalently a morphism of base objects $f_b \;\colon\; B_1 \longrightarrow B_2$ in $\mathbf{H}$ together with morphisms $X_n \longrightarrow f_b^\ast Y_n$ into the [[(∞,1)-pullback]] of the components of $Y_\bullet$  along $f_b$.


Therefore the [[(∞,1)-presheaf (∞,1)-topos]] 

$$
  \mathbf{H}^{seq}
  \coloneqq
  Func(seq, \mathbf{H})
$$ 

is the [[codomain fibration]] of $\mathbf{H}$ with "fiberwise pre-stabilization".

A genuine [[spectrum object]] is a [[prespectrum object]] for which all the structure maps $X_n \stackrel{\simeq}{\longrightarrow} \Omega_B X_{n+1}$ are [[equivalence in an (∞,1)-category|equivalences]]. The [[full sub-(∞,1)-category]] 

$$
  T \mathbf{H} \hookrightarrow \mathbf{H}^{seq}
$$

on the genuine [[spectrum objects]] is therefore the "fiberwise [[stabilization]]" of the [[codomain fibration]], hence the tangent $(\infty,1)$-category.

=--

+-- {: .num_lemma #SpectrificationLemma}
###### Lemma
**(spectrification is left exact reflective)**

The inclusion of [[spectrum objects]] into $\mathbf{H}$  is [[left exact (infinity,1)-functor|left]] [[reflective sub-(infinity,1)-category|reflective]], hence it has a [[left adjoint]] [[(∞,1)-functor]] $L$ which preserves [[finite (∞,1)-limits]].

$$
  T \mathbf{H}
  \stackrel{\overset{L_{lex}}{\leftarrow}}{\hookrightarrow}
  \mathbf{H}^{seq}
  \,.
$$


=--

([Joyal 08, section 35.1](#Joyal08))

+-- {: .proof}
###### Proof 

Forming degreewise [[loop space objects]] constitutes an [[(∞,1)-functor]] $\Omega \colon \mathbf{H}^{seq} \longrightarrow \mathbf{H}^{seq}$ and by definition of $seq$ this comes with a [[natural transformation]] out of the identity

$$
  \theta \;\colon\; id \longrightarrow \Omega
  \,.
$$

This in turn is compatible with $\Omega$ in that

$$
  \theta \circ \Omega \simeq \Omega \circ \theta
  \;\colon\;
  \Omega \longrightarrow \Omega \circ \Omega = \Omega^2
  \,.
$$

Consider then a sufficiently deep [[transfinite composition]] $\rho^{tf}$. By the [[small object argument]] available in the [[presentable (∞,1)-category]] $\mathbf{H}$ this stabilizes, and hence provides a [[reflective sub-(infinity,1)-category|reflection]] $L \;\colon\; \mathbf{H}^{seq} \longrightarrow T \mathbf{H}$.

Since [[transfinite composition]] is a [[filtered (∞,1)-colimit]] and since in an [[(∞,1)-topos]] these commute with [[finite (∞,1)-limits]], it follows that spectrum objects are an [[exact (∞,1)-functor|left exact]] [[reflective sub-(∞,1)-category]].

=--

+-- {: .num_prop}
###### Proposition

For $\mathbf{H}$ an [[(∞,1)-topos]] over the [[base (∞,1)-topos]] $\infty Grpd$, its [[tangent (∞,1)-category]] $T \mathbf{H}$ is an [[(∞,1)-topos]] over the base $T \infty Grpd$ (and hence in particular also over $\infty Grpd$ itself).

=--

([Joyal 08, section 35.5](#Joyal08))

+-- {: .proof}
###### Proof 

By the the spectrification lemma \ref{SpectrificationLemma} 
$T \mathbf{H}$ has a [[geometric embedding]] into the [[(∞,1)-presheaf (∞,1)-topos]] $\mathbf{H}^{seq}$, and this implies that it is an [[(∞,1)-topos]] (by the discussion there).

Moreover, since both [[adjoint (∞,1)-functor]] in the [[global section geometric morphism]] $\mathbf{H} \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}} \infty Grpd$ preserve [[finite (∞,1)-limits]] they preserve [[spectrum objects]] and hence their immediate [[(∞,1)-presheaf]] prolongation immediately restricts to the inclusion of spectrum objects

$$
  \array{
    T \mathbf{H} &\stackrel{\overset{T \Delta}{\leftarrow}}{\underset{T \Gamma}{\longrightarrow}}&
   T \infty Grpd
   \\
   \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
   \\
   \mathbf{H}
    &
    \stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}}
    &
   \infty Grpd
  }
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

We may think of the [[tangent (∞,1)-topos]] $T \mathbf{H}$ as being an [[extension]] of $\mathbf{H}$ by its [[stabilization]] $Stab(\mathbf{H}) \simeq T_\ast \mathbf{H}$:

$$
  \array{
    Stab(\mathbf{H}) &\stackrel{\overset{Stab(\Delta)}{\leftarrow}}{\underset{Stab(\Gamma)}{\longrightarrow}}&
    Spectra
    \\
    \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    T\mathbf{H} &\stackrel{\overset{T\Delta}{\leftarrow}}{\underset{T\Gamma}{\longrightarrow}}&
    T \infty Grpd
    \\
    \downarrow^{\mathrlap{base}} && \downarrow^{\mathrlap{base}}
    \\
    \mathbf{H} &\stackrel{\overset{\Delta}{\leftarrow}}{\underset{\Gamma}{\longrightarrow}}&
    \infty Grpd
  }
  \,.
$$

Crucial for the internal interpretation in [[homotopy type theory]] is that the [[homotopy types]] in $T_\ast \mathbf{H} \hookrightarrow T \mathbf{H}$ are [[stable homotopy types]].

=--

#### Tangent cohesive homotopy theory


Now consider the case that $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] over [[∞Grpd]], 
in that there is an [[adjoint quadruple]]

$$
  \mathbf{H}
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

with $Disc, coDisc$ being [[full and faithful (∞,1)-functors]] and $\Pi$ preserving finite [[(∞,1)-products]].

Since [[(∞,1)-limits]] and [[(∞,1)-colimits]] in an [[(∞,1)-presheaf (∞,1)-topos]] are computed objectwise, this [[adjoint quadruple]] immediately prolongs to $\mathbf{H}^{seq}$

$$
  \mathbf{H}^{seq}
    \stackrel{\overset{\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  \infty Grpd^{seq}
  \,.
$$

Moreover, all three [[right adjoints]] preserves the [[(∞,1)-pullbacks]] involved in the characterization of [[spectrum objects]] and hence restrict to $T \mathbf{H}$

$$
  T\mathbf{H}
    \stackrel{}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  T\infty Grpd
  \,.
$$

But then we have a further [[left adjoint]] given as the composite

$$
  T\mathbf{H}
  \hookrightarrow
  \mathbf{H}^{seq}
   \stackrel{\overset{\Pi^{seq}}{\longrightarrow}}{\underset{Disc^{seq}}{\leftarrow}}
  \infty Grpd^{seq}
   \stackrel{\overset{L}{\longrightarrow}}{\underset{}{\leftarrow}}
  T \infty Grpd
  \,.
$$

Again since $L$ is a [[left exact (∞,1)-functor]] this composite $L \Pi$ preserves finite [[(∞,1)-products]].

So it follows in conclusion that if $\mathbf{H}$ is a [[cohesive (∞,1)-topos]] then its tangent $(\infty,1)$-category $T \mathbf{H}$ is itself a [[cohesive (∞,1)-topos]] over the tangent $(\infty,1)$-category  $T \infty Grpd$ of the [[base (∞,1)-topos]], which is an [[extension]] of the cohesion of the $\infty$-topos $\mathbf{H}$ over $\infty Grpd$ by the cohesion of the stable $\infty$-category $Stab(\mathbf{H})$ over $Stab(\infty Grpd) \simeq Spec$:


$$
  \array{
    && Stab(\mathbf{H})
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
    &
    Stab(\infty Grpd) \simeq Spectra
    \\
    && \simeq && \simeq
    \\
    && T_\ast \mathbf{H} && T_\ast \infty Grpd
    \\
    && \downarrow^{\mathrlap{incl}} && \downarrow^{\mathrlap{incl}}
    \\
    \mathbf{H}
    &\stackrel{\overset{d}{\longrightarrow}}{\underset{\Omega^\infty \circ tot}{\leftarrow}}&
    T \mathbf{H}
    &
    \stackrel{\overset{L\Pi^{seq}}{\longrightarrow}}{\stackrel{\overset{Disc^{seq}}{\leftarrow}}{\stackrel{\overset{\Gamma^{seq}}{\longrightarrow}}{\underset{coDisc^{seq}}{\leftarrow}}}}
  &
  T \infty Grpd
  \\
  &&
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  && 
  {}^{\mathllap{base}}\downarrow \uparrow^{\mathrlap{0}} 
  \\
  &&
    \mathbf{H}
    &
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  &
  \infty Grpd
  }
  \,.
$$

Here

* $\Omega^\infty \circ tot \;\colon\; T \mathbf{H} \longrightarrow \mathbf{H}$ assigns the _total space_ of a spectrum bundle;

  its [[left adjoint]] is the [tangent complex functor](tangent+%28infinity%2C1%29-category#CotangentComplex);

* $base \;\colon\; T \mathbf{H} \longrightarrow \mathbf{H}$ assigns the _base space_ of a spectrum bundle;

  its [[left adjoint]] produces the 0-bundle.



Where the [[(∞,1)-categorical hom-space]] in a general [[(∞,1)-topos]] constitute a notion of [[cohomology]], those of a [[tangent (∞,1)-topos]] specifically constitute [[twisted generalized cohomology]], in fact [[twisted bivariant cohomology]].

For consider a [[spectrum object]] $E \in T_\ast \mathbf{H}$ and write $GL_1(E) \in Grp(\mathbf{H})$ for its [[∞-group of units]]. Then the [[∞-action]] of this on $E$ is (by the discussion there) exhibited by an object 

$$
  \left(
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right)
  \;\;\;
   \in
  \;\;\;
  T_{\mathbf{B}GL_1(E)}\mathbf{H} \hookrightarrow T\mathbf{H}
  \,.
$$

More generally, for $Pic(E) \in \mathbf{H}$ the [[Picard ∞-groupoid]] of $E$ there is the universal [[(∞,1)-line bundle]]

$$
  (\widehat{Pic(E)} \to Pic(E)) \in T \mathbf{H}
  \,.
$$

Now for any object $X \in \mathbf{H}$ we have

$$
  X \times E
  \simeq
  \left(
   \array{
     E \times X
     \\
     \downarrow
     \\
     X
   }
  \right)
  \;\;\;
   \in
  \;\;\;
  T_{X}\mathbf{H} \hookrightarrow T\mathbf{H}
  \,,
$$

then morphisms in $T \mathbf{H}$ from the latter to the former

$$
    \left(
   \array{
     E \times X
     \\
     \downarrow
     \\
     X
   }
  \right)
  \longrightarrow
  \left(
   \array{
     E//GL_1(E)
     \\
     \downarrow
     \\
     \mathbf{B}GL_1(E)
   }
  \right)
$$

are equivalently

1. a choice of [[twisted cohomology|twist of E-cohomology]] $\chi \;\colon \; X  \longrightarrow \mathbf{B}GL_1(E)$;

1. an element in the $\chi$-twisted $E$-cohomology of $X$, hence  $c \in E^{\bullet}(X,E)$.

If we consider the [[internal hom]] then we can use just $X$ instead of $X \times E$:

+-- {: .num_prop}
###### Proposition

For $X \in \mathbf{H} \stackrel{0}{\hookrightarrow} T \mathbf{H}$ a [[geometric homotopy type]] and $E \in Stab(\mathbf{H}) \simeq T_\ast \mathbf{H} \hookrightarrow T \mathbf{H}$ a [[spectrum object]], then the [[internal hom]]/[[mapping stack]]

$$
  [X,E]_{T \mathbf{H}} \in T \mathbf{H}
$$

(with respect to the Cartesian [[closed monoidal (∞,1)-category]] structure on the [[(∞,1)-topos]] is equivalently the [[mapping spectrum]]

$$
  [\Sigma^\infty X, E]_{Stab(\mathbf{H})} \in Stab(\mathbf{H}) \hookrightarrow T \mathbf{H}
  \,,
$$

in that 

$$
  [X,E]_{T \mathbf{H}} \simeq [\Sigma^\infty X,E]_{Stab(\mathbf{H})}
  \,.
$$

=--

+-- {: .proof}
###### Proof 

Notice that as an object of $T \mathbf{H} \hookrightarrow \mathbf{H}^{seq}$, the object $X$ is the constant [[(∞,1)-presheaf]] on $seq$. By the formula for the [[internal hom]] in an [[(∞,1)-category of (∞,1)-presheaves]] we have

$$
  [X,E]_\bullet \simeq \mathbf{H}^{seq}(X \times \bullet, E)
  \,.
$$

But since $X$ is constant the object $X \times \bullet$ is for each object of $seq$ the [[representable functor|presheaf represented]] by that object. Therefore by the [[(∞,1)-Yoneda lemma]] it follows that

$$
  [X,E]_\bullet \simeq [X,E_\bullet]
  \,.
$$

This is manifestly the same formula as for the [[mapping spectrum]] out of $\Sigma^\infty X$.

=--

By the same kind of argument we have the following more general statement.

+-- {: .num_prop}
###### Proposition

For $X \in \mathbf{H} \stackrel{0}{\hookrightarrow} T \mathbf{H}$ a [[geometric homotopy type]], for $E \in E_\infty(\mathbf{H})$ an [[E-∞ ring]]  with $(\widehat{Pic(E)} \to Pic(E)) \hookrightarrow T \mathbf{H}$ its universal [[(∞,1)-line bundle]] over its [[Picard ∞-groupoid]], then the [[internal hom]]/[[mapping stack]]

$$
  [X,\widehat{Pic(E)}]_{T \mathbf{H}} \in T \mathbf{H}
$$

is the object whose

* base homotopy type is the [[E-∞ ring]] $[X, Pic(E)]$ of $E$-[[twisted cohomology|twist]] on $X$;

* whose [[spectrum bundle]] is the collection of $\chi$-[[twisted cohomology|twisted E-cohomology spectra]] for all twists $\chi$.

=--



#### Cohesive and differential refinement in tangent cohesion
 {#CohesiveAndDifferentialRefinement}


Let $T\mathbf{H}$ be a tangent cohesive $(\infty,1)$-topos and write $T_\ast \mathbf{H}$ for the [[stable (∞,1)-category]] of [[spectrum objects]] inside it.

+-- {: .num_prop}
###### Proposition

For every $A \in T_\ast \mathbf{H}$ the [[natural transformation|naturality square]] 

$$
  \array{
    A &\stackrel{}{\longrightarrow}& A/\flat A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

(of the [[shape modality]] applied to the [[homotopy cofiber]] of the [[counit of a comonad|counit]] of the [[flat modality]]) is an [[(∞,1)-pullback]] square.

=--

This was observed in ([Bunke-Nikolaus-V&#246;lkl 13](tangent+cohesion#BunkeNikolausVoelkl13)). It is an incarnation of a [[fracture theorem]].

+-- {: .proof}
###### Proof 

By [[cohesive (infinity,1)-topos|cohesion]] and [[stable (infinity,1)-category|stability]] we have the diagram

$$
  \array{
    \flat A &\longrightarrow & A &\stackrel{}{\longrightarrow}& A/\flat A
    \\
    \downarrow^{\mathrlap{\simeq}} && \downarrow && \downarrow
    \\
    \Pi(\flat A) &\longrightarrow& \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

where both rows are [[homotopy fiber sequences]]. By [[cohesive (infinity,1)-topos|cohesion]] the left vertical map is an [[equivalence in an (infinity,1)-category|equivalence]]. The claim now follows with the [homotopy fiber characterization](homotopy+pullback#HomotopyFiberCharacterization) of [[homotopy pullbacks]].

=--

+-- {: .num_remark}
###### Remark


This means that in stable cohesion every cohesive stable homotopy type is in controled sense a cohesive extension/refinement of its [[geometric realization of cohesive infinity-groupoids|geometric realization]] [[discrete infinity-groupoid|geometrically discrete]] ("bare") stable [[homotopy type]] by the non-[[discrete object|discrete]] part of its cohesive structure;

In particular, $A/\flat A$ may be identified with differential cycle data. Indeed, by stability and cohesion it is the [flat de Rham coefficient object](cohesive+%28infinity,1%29-topos+--+structures#deRhamCohomology)


$$
  A/\flat A = \flat_{dR}\Sigma A
$$

of the [[suspension]] of $A$. So

$$
  \array{
    A &\stackrel{\theta_A}{\longrightarrow}& \flat_{dR}\Sigma A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
$$

exhibits $A$ as a [[differential cohomology]]-coefficient of the [[generalized cohomology theory]] $\Pi(A)$ ([Bunke-Nikolaus-V&#246;lkl 13](#BunkeNikolausVoelkl13)).

It follows by the discussion at [[schreiber:differential cohomology in a cohesive topos]] that the further differential refinement $\widehat{A}$ of $A$ should be given by a further [[homotopy pullback]]

$$
  \array{
    \widehat{A} &\longrightarrow& \Omega^1(-,Lie(A))
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    A &\stackrel{\theta_A}{\longrightarrow}& \flat_{dR}\Sigma A
    \\
    \downarrow &{}^{(pb)}& \downarrow
    \\
    \Pi(A) &\stackrel{}{\longrightarrow}& \Pi(A/\flat A)
  }
  \,.
$$


=--



### Local prequantum field theory

We describe the formulation of [[local prequantum field theory]] in a [[cohesive (∞,1)-topos]] $\mathbf{H}$ ([lpqft](#lpqft)).


A [[classical field theory]]/[[prequantum field theory]]
is traditionally defined by an [[action functional]]: given a [[smooth space]] $\mathbf{Fields}_{traj}$ "of [[trajectories]]" of a given [[physical system]], then the [[action functional]] is a [[smooth function]]

$$
  \array{
    \mathbf{Fields}_{traj}
    \\
    \downarrow^{\mathrlap{\exp(i S)}}
    \\
    U(1)
  }
$$

to the [[circle group]]. The idea of producing a [[quantum field theory]] from this is to 

1. choose a linearization in the form of the group [[homomorphism]] 
$U(1) \longrightarrow GL_1(\mathbb{C})$ to the [[group of units]] of the complex numbers, 

1. choose a [[measure]] $d\mu$ on $\mathbf{Fields}_{traj}$ 

and then declare that the [[integral]] ("[[path integral]]")

$$
  \underset{\phi \in \mathbf{Fields}_{traj}}{\int} \exp(i S(\phi))\, d\mu \in \mathbb{C}
$$ 

is the [[partition function]] of the theory a kind of [[expectation value]] with [[probabilities]] replaced by [[probability amplitudes]].

In order to make sense of this (for a full discussion of "[[motivic quantization]]" in this sense see ([Nuiten 13](#Nuiten13)), here we concentrate on the [[prequantum field theory|pre-quantum aspects]]), it is useful to allow some more conceptual wiggling room by passing to [[higher differential geometry]]. Notice that if we write $\mathbf{B}U(1)$ for the [[smooth groupoid|smooth]] universal [[moduli stack]] of [[circle group]]-[[principal bundles]], then an [[action functional]] as above is equivalently a [[homotopy]] of the form

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow &\downarrow^{\mathrlap{\exp(i S)}}& \searrow
    \\
    \ast &\leftarrow& U(1) &\rightarrow& \ast
    \\
    & {}_{\mathllap{0}}\searrow &{}^{(pb)}& \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \,,
$$

where on the right we used the [[universal property]] of the [[homotopy pullback]] [[diagram]] which exhibits the smooth [[circle group]] $U(1)$ as the [[loop space object]] of $\mathbf{B}U(1)$.

For instance for $X$ a [[smooth manifold]] ("[[spacetime]]") and $\nabla \;\colon\; X \longrightarrow \mathbf{B}U(1)_{conn}$ a [[circle group]]-[[principal connection]] ("[[electromagnetic field]] on [[spacetime]]") then for [[trajectories]] in $X$ of shape the [[circle]], the canonical [[action functional]] ("[[Lorentz force]] gauge [[interaction]]") is the [[holonomy]] [[nonlinear functional|functional]]

$$
  \exp(i S_{Lor})
  \coloneqq
  \exp(i \int_{S^1} [S^1, \nabla])
  \;\colon\;
  [S^1, X]
  \stackrel{[S^1, X]}{\longrightarrow}
  [S^1, \mathbf{B}U(1)_{conn}]
  \stackrel{\exp(i \int_{S^1}(-))}{\longrightarrow}
  U(1)
  \,.
$$

But more generally, if the [[trajectories]] have a [[boundary]], hence if they are of the shape of an [[interval]] $I \coloneqq [0,1]$, then the [[holonomy]] functional on [[smooth loop space]] $[S^1, X]$ generalizes to the [[parallel transport]] on the [[path space]] $[I,X]$ and there it is no longer a function, but exists only as a [[homotopy]] of the form

$$
  \array{
    && [I,X]
    \\
    & {}^{(-)|_0}\swarrow && \searrow^{\mathrlap{(-)|_1}}
    \\
    X && \swArrow_{\exp(i \int_{I}[I,\nabla])} && X
    \\
    & {}_{\mathllap{\chi_\nabla}}\searrow && \swarrow_{\mathrlap{\chi_\nabla}}
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$
 
Notice that this is a "local" description of the action functional: the data that determines it is the boundary

$$
  \array{
    X
    \\
    \downarrow^{\mathrlap{\nabla}}
    \\
    \mathbf{B}U(1)_{conn}
  }
$$

and from this the rest is induced by [[transgression]]. 

A related class of examples are [[prequantized Lagrangian correspondences]]: Let 

$$
  \array{
     X
     \\
     \downarrow^{\mathrlap{\omega}}
     \\
     \mathbf{\Omega}^2
  }
$$

be a [[symplectic manifold]]. Then a [[symplectomorphism]] $f \;\colon\; X \longrightarrow X$ is a [[correspondence]] of the form

$$
  \array{
    && graph(f)
    \\
    & \swarrow && \searrow
    \\
    X && && X
    \\
    & {}_{\mathllap{\omega}}\searrow && \swarrow_{\mathrlap{\omega}}
    \\
    && \mathbf{\Omega}^2
  }
  \,.
$$

A [[prequantization]] of $(X,\omega)$ is a lift $\nabla$ in

$$
  \array{
    X &\stackrel{\nabla}{\longrightarrow}& \mathbf{B}U(1)_{conn}
    \\
    & \searrow & \downarrow^{\mathrlap{F_{(-)}}}
    \\
    && \mathbf{\Omega}^2
  }
$$

and so a [[prequantized Lagrangian correspondence]] is

$$
  \array{
    && graph(f)
    \\
    & \swarrow && \searrow
    \\
    X && \swArrow && X
    \\
    & _{\mathllap{\nabla}}\searrow && \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \,.
$$

To conceptualize all this, write

$$
  \mathbf{H} \coloneqq SmoothGrpd \coloneqq
  Func(SmoothMfd^{op}, Grpd)[\{stalkwise\;equivalences\}^{-1}]
$$

for the [[homotopy theory]] obtained from the [[category]] of [[groupoid]]-valued [[presheaves]] on the [[category]] of all [[smooth manifolds]] by universally turning [[stalk|stalkwise]] [[equivalences of groupoids]] into genuine [[homotopy equivalences]] ("[[simplicial localization]]").

This is the [[(2,1)-topos]] of [[smooth groupoids]]/smooth ([[moduli stacks|moduli]]) [[stacks]].

Write 

$$
  Corr_1(\mathbf{H})
  \in 
  (2,1)Cat
$$ 

for the [[(2,1)-category]] of [[correspondences]] in $\mathbf{H}$. Write $\mathbf{H}_{/\mathbf{B}U(1)_{conn}}$ for the [[slice (infinity,1)-topos|slice]] [[(2,1)-topos]] over the smooth [[moduli stack]] of [[circle n-bundles with connection|circle bundles with connection]]. Then the abovve diagrams are morphisms in $Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$.

+-- {: .num_prop}
###### Proposition 

The [[automorphism group]] of $\nabla \in Corr_1(\mathbf{H}_{/\mathbf{B}U(1)_{conn}})$ is the [[quantomorphism group]] of $(X,\omega)$, hence the [[smooth group]] which is the [[Lie integration]] of the [[Poisson bracket]] [[Lie algebra]] of $(X,\omega)$.

A [[concrete object|concrete]] smooth 1-parameter subgroup

$$
  \mathbf{B}\mathbb{R} \longrightarrow
  \mathbf{B}\mathbf{Aut}_{/\mathbf{B}U(1)_{conn}}(\nabla)
  \hookrightarrow
  \mathbf{H}_{/\mathbf{B}U(1)_{conn}}
$$

is equivalently a choice $H \in C^\infty(X)$ of a smooth function and sends

$$
  t
  \;\;
   \mapsto
  \;\;
  \left(
  \array{
    X &&\stackrel{\exp(t \{H,-\})}{\longrightarrow}&& X
    \\
    & {}_{\mathllap{\nabla}}\searrow &\swArrow_{\mathrlap{\exp(i S_t)}}& \swarrow_{\mathrlap{\nabla}}
    \\
    && \mathbf{B}U(1)_{conn}
  }
  \right)
  \,,
$$

where

1. $\exp(t \{H,-\})$ is the [[Hamiltonian flow]] induced by $H$;

1. $S_t = \int_0^t L$ is the [[Hamilton-Jacobi theory|Hamilton-Jacobi]] [[action functional]], the [[integral]] of the [[Lagrangian]] of $H$, hence of its [[Legendre transform]].  

=--


(see [Schreiber 13](#SchreiberClassical)).

It is now clear how to pass from this to [[local prequantum field theory]] of higher dimension.

Let now more generally



$$
  \mathbf{H} \coloneqq 
  Smooth\infty Grpd
  \coloneqq
  Func(SuperMfd^{op}, KanCplx)[\{stalkwise\;homotopy\;equivalences\}^{-1}]
$$

be the [[homotopy theory]] obtained from the [[category]] of [[Kan complex]]-valued [[presheaves]] on the category of all [[supermanifolds]] by universally turning [[stalk|stalkwise]] [[homotopy equivalences]] into actual [[homotopy equivalences]].

We say that this is the [[(∞,1)-topos]] of _[[smooth super ∞-groupoids]]_/_[[supergeometry|supergeometric]] [[moduli ∞-stacks]]_.

Let 

$$
  Corr_n(\mathbf{H}) \in (\infty,n)Cat
$$

be the [[(∞,n)-category]] of $n$-fold [[correspondences]] in $\mathbf{H}$. This is a [[symmetric monoidal (∞,n)-category]] under the objectwise [[Cartesian product]] in $\mathbf{H}$.



[[Smooth∞Grpd]] has the special property that it is [[cohesive (∞,1)-topos|cohesive]] in that it is equipped with an [[adjoint quadruple]] of [[adjoint (∞,1)-functors]]

$$
  \mathbf{H}
  \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}
  \infty Grpd
$$

which induce an [[adjoint triple]] of [[idempotent monad|idempotent]] [[(∞,1)-monads]]/comonads


$$
  \left(
    \Pi \dashv \flat \dashv \sharp
  \right)
  \;\colon\;
  \mathbf{H} 
  \longrightarrow
  \mathbf{H}
$$

with $\Pi$ [[Cartesian product|product]]-preserving, called

* _[[shape modality]]_ $\dashv$ _[[flat modality]]_ $\dashv$ _[[sharp modality]]_ .

Here the [[shape modality]] $\Pi$ sends a [[simplicial manifold]] to the [[homotopy type]] of the [[geometric realization of simplicial topological spaces|fat geometric realization]] of the underlying [[simplicial topological space]], hence in particular sends a [[smooth manifold]] to its [[homotopy type]].
 
Write $Bord_n$ for the [[(∞,n)-category of cobordisms|(∞,n)-category of framed n-dimensional cobordisms]].

+-- {: .num_prop}
###### Proposition 

A [[monoidal (∞,n)-functor]] 

$$
  \mathbf{Fields}
  \;\colon\;
  Bord_n
  \longrightarrow
  Corr_n(\mathbf{H})
$$

is equivalently a choice of object $\mathbf{Fields} \in \mathbf{H}$. It sends a [[cobordism]] $\Sigma$ to the [[internal hom]] of its [[shape]] into the [[higher moduli stack]] $\mathbf{Fields}$:


$$
  \left(
    \array{
      && \Sigma
      \\
      & \nearrow && \nwarrow
      \\
      \Sigma_{in}
      && &&
      \Sigma_{out}
    }
  \right)
  \;\;
   \mapsto
  \;\;
  \left(
    \array{
       && [\Pi\Sigma, \mathbf{Fields}]
       \\
       & {}^{(-)|_{\Sigma_{in}}}\swarrow
       &&
       \searrow^{(-)|_{\Sigma_{out}}}
       \\
       [\Pi(\Sigma_{in}), \mathbf{Fields}]
       && &&
       [\Pi(\Sigma_{out}), \mathbf{Fields}]
    }
  \right)
  \,.
$$

=--

([lpqft](#lpqft))


+-- {: .num_prop}
###### Proposition 

Under the [[Dold-Kan correspondence]] 

$$
  DK \colon ChainComplexes \stackrel{\simeq}{\longrightarrow}
  SimplicialAbelianGroups
  \stackrel{forget}{\longrightarrow}
  KanComplexes
$$


we have for all $n \in \mathbb{N}$ an [[equivalence]]

$$
  \flat \mathbf{B}^{n+1}U(1)
   \simeq
  DK
  \left(
    \underline{U}(1)
    \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^1 
    \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^2
    \stackrel{\mathbf{d}}{\longrightarrow}
    \cdots  
   \stackrel{\mathbf{d}}{\longrightarrow}
    \mathbf{\Omega}^{n+1}_{cl}   
  \right)
$$

in $\mathbf{H}$.

=--

+-- {: .num_example #tYM}
###### Example

Consider the induced canonical inclusion

$$
  \mathbf{\Omega}^{n+1}
  \longrightarrow
  \flat \mathbf{B}^{n+1}U(1)
  \,.
$$

By the above we may regard this as an [[action functional]] for an $(n+1)$-dimensional [[prequantum field theory]] with [[moduli stack]] of [[field (physics)|fields]] being $\mathbf{\Omega}^{n+1}_{cl}$. As such we denote it

$$
  \array{
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     \downarrow^{\mathrlap{\exp(i S_{tYM})}}
     \\
     \flat \mathbf{B}^{n+1}U(1)
  }
  \,,
$$

where the subscript is supposed to refer to "universal higher [[topological Yang-Mills theory]]".

=--

+-- {: .num_prop}
###### Proposition 

[[monoidal (∞,n)-functors]]

$$
  \array{
     Bord_n
     &\stackrel{\exp(i S)}{\longrightarrow}&
     Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
     \\
     & {}_{\mathbf{Fields}} \searrow & \downarrow
     \\
     && Corr_n(\mathbf{H})
  }
$$

are equivalent to objects

$$
  \left(
  \array{
    \mathbf{Fields}
    \\
     \downarrow^{\mathrlap{\exp(i S)}}
    \\
    \flat \mathbf{B}^{n+1}U(1)
  }
  \right)
  \;\;\;
    \in
  \;\;\;
  \mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)}
  \hookrightarrow
  Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
  \,.
$$

This sends the dual point to $\exp(- i S)$
and sends the $k$-[[sphere]] to the [[transgression]]
of $\exp(i S)$ to the mapping space $[S^k , \mathbf{Fields}]$.

=--

([lpqft](#lpqft))

+-- {: .num_example}
###### Example

Consider the induced canonical inclusion

$$
  \mathbf{\Omega}^{n+1}
  \longrightarrow
  \flat \mathbf{B}^{n+1}U(1)
  \,.
$$

By the above we may regard this as an [[action functional]] for an $(n+1)$-dimensional [[prequantum field theory]] with [[moduli stack]] of [[field (physics)|fields]] being $\mathbf{\Omega}^{n+1}_{cl}$. As such we denote it

$$
  \array{
     \mathbf{\Omega}^{n+1}_{cl}
     \\
     \downarrow^{\mathrlap{\exp(i S_{tYM})}}
     \\
     \flat \mathbf{B}^{n+1}U(1)
  }
  \,,
$$

where the subscript is supposed to refer to "universal higher [[topological Yang-Mills theory]]".

=--


Observe that by the [[cobordism hypothesis]] $Bord_n$ is the [[free construction|free]] [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects]] generated from a single object $\ast$. 

$$
  Bord_n \simeq FreeSMwD(\{\ast\})
  \,.
$$

Let then

$$
  Bord_n^{\partial} \coloneqq FreeSMwD(\{\emptyset \longrightarrow \ast\})
$$

the free [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects]] generated from a single object $\ast$ and a single [[morphism]] $\emptyset \longrightarrow \ast$ from the [[tensor unit]] to the generating object. By the [[boundary field theory]]/[[defect field theory|defect]] version of the [[cobordism hypothesis]], this is equivalently the [[(∞,n)-category of cobordisms]] with possibly a [[boundary]] component of [[codimension]] $(n-1)$.

Hence a [[boundary field theory]] is

$$
  \array{
     Bord_n^\partial
     &\stackrel{\exp(i S)}{\longrightarrow}&
     Corr_n(\mathbf{H}_{/\flat \mathbf{B}^{n+1}U(1)})
     \\
     & {}_{\mathbf{Fields}^\partial} \searrow & \downarrow
     \\
     && Corr_n(\mathbf{H})
  }
$$

+-- {: .num_remark}
###### Remark

A [[boundary field theory]] as above is equivalently a [[diagram]] in $\mathbf{H}$ of the form

$$
  \array{
    && \mathbf{Fields}_{bdr}
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \mathbf{Fields}
    \\
    & \searrow && \swarrow_{\mathrlap{\exp(i S)}}
    \\
    && \flat \mathbf{B}^{n+1}U(1)
  }
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The _universal_ [[boundary field theory|boundary condition]] for
the universal higher topological Yang-Mills theory of example \ref{tYM} is the [[higher moduli stack]]
$\mathbf{B}^n U(1)_{conn}$ of [[circle n-bundle with connection]],
hence a general boundary condition for this 
higher [[topological Yang-Mills theory]] is a
[[schreiber:∞-Chern-Simons theory]]].



=--

The [[schreiber:∞-Wess-Zumino-Witten theory]] that we are after are boundaries of these boundary field theories, hence "corner field theories" ([Sati 11](#Sati11), [lpqft](#lpqft)) of the higher universal topological Yang-Mills theory. This we turn to now.


+-- {: .num_remark}
###### Remark


The earliest and the only rigorously understood example of the [[holographic principle]] is the [[AdS3-CFT2 and CS-WZW correspondence]] between the [[WZW model]] on a [[Lie group]] $G$ and 3d $G$-[[Chern-Simons theory]].

In ([Witten 98](7d+Chern-Simons+theory#Witten98)) it is argued that all examples of the [[AdS-CFT duality]] are governed by the [[schreiber:infinity-Chern-Simons theory|higher Chern-Simons theory]] terms in the [[supergravity]] [[Lagrangian]] on one side of the correspondence, hence that the corresponding [[conformal field theories] are higher dimensional analogs of the traditional [[WZW model]]: that they are "[[schreiber:∞-Wess-Zumino-Witten theory]]"-type models.

In particular for [[AdS7-CFT6]] this means that the [[6d (2,0)-superconformal QFT]] on the [[M5-brane]] [[worldvolume]] should be a 6d-dimensional WZW model holographically related to the [[7d Chern-Simons theory]] which appears when [[11-dimensional supergravity]] is [[KK-reduction|KK-reduced]] on a 4-[[sphere]]:

| [[schreiber:∞-Chern-Simons theory]] | $\leftarrow$[[holographic principle]]$\rightarrow$ | [[schreiber:∞-Wess-Zumino-Witten theory]] |
|---|---|---|
| 3d [[Chern-Simons theory]] |  | 2d [[Wess-Zumino-Witten model]] |
| [[7d Chern-Simons theory]] from [[11-dimensional supergravity]] |  | [[6d (2,0)-superconformal QFT]] on [[M5-brane]] |

In ([Witten 96](http://ncatlab.org/nlab/show/7d+Chern-Simons+theory#WittenI)) this is argued, by [[geometric quantization]] after [[transgression]] to [[codimension]] 1, for the _bosonic and abelian_  contribution in [[7d Chern-Simons theory]]. (The subtle [[theta characteristic]] involved was later formalized in [[Quadratic Functions in Geometry, Topology, and M-Theory|Hopkins-Singer 02]].) 


In order to formalize this in generality, one needs a general formalization of [[holography]] for [[local prequantum field theory]] as these. How are [[schreiber:∞-Wess-Zumino-Witten theory]]-models higher holographic boundaries of [[schreiber:∞-Chern-Simons theory]]? This we are dealing with at _[[Super Gerbes]]_.


=--



### Motivic quantization of twisted fields

So far we have considered [[configuration spaces]] of fields, refined to [[smooth ∞-groupoid|smooth]] [[moduli ∞-stacks]]. The next step is to consider aspects of the [[quantization]] of these fields, at least as an [[effective quantum field theory]] (the full [[string theory]] being the corresponding [[UV-completion]]).

By the [[holographic principle]] and specifically by [[AdS-CFT duality]], various of the twisted field configurations considered [above](#Examples) participate either in [[higher dimensional Chern-Simons theory]] or in the corresponding [[self-dual higher gauge theory]]. 

For instance the [[supergravity C-field]], after [[Kaluza-Klein mechanism|compactification]] to [[dimension]] 7 in the context of [AdS7-CFT6](AdS-CFT#AdS7CFT6), has a [[TQFT|topological]] [[action functional]] given by the [secondary intersection pairing](intersection+pairing#SecondaryIntersectionPairing) [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] (or in fact, if quantum corrections are taken into account, a generalization of that to $String$-2-form fields [FSSb](#FSSb)).

The [[geometric quantization]] of these higher CS theories yields canonical [[states]] in codimension 1, which by [[AdS-CFT]] are interpreted as parts of the [[partition function]] of [[self-dual higher gauge fields]].


This is described at _[[motivic quantization]]_ ([Nuiten 13](#Nuiten2013)).

#### Linearization by twisted $E$-cohomology spectra


Before actually quantizing a [[local prequantum field theory]] $\left[ \array{ \mathbf{Fields} \\ \downarrow^{\mathrlap{\exp(i S)}} \\ \mathbf{B}^n U(1)_{conn}}\right]$ as above, we choose linear [[coefficients]], given by 


1. a choice of ground [[E-∞ ring]] $E$ 

   (playing the role of the [[complex numbers]] in plain [[quantum mechanics]]);

1. a choice of [[∞-group]] homomorphism

   $$
     \rho \;\colon\; \mathbf{B}^{n-1}U(1) \longrightarrow GL_1(E)
   $$


   from the [[∞-group]] of [[phase and phase space in physics|phases]] to the [[∞-group of units]] of $E$, hence an [[∞-representation]] of the [[circle n-group]] on $E$ 

   (playing the role of the canonical $U(1) \hookrightarrow \mathbb{C}^\times$ in plain [[quantum mechanics]]).


Then for $X \longrightarrow \mathbf{B}^n U(1)$ modulating a [[circle n-bundle with connection|circle n-bundle]] on $X$, the composite

$$
  X
   \longrightarrow
  \mathbf{B}^n U(1)
    \stackrel{\rho}{\longrightarrow}
  B GL_1(E)
    \longrightarrow
  E Mod
$$

modulates the [[associated ∞-bundle]], which is an $E$-[[(∞,1)-module bundle]].


Specifically, given the [[higher prequantum bundle]] $\exp(i S) \;\colon\; \mathbf{Fields} \to \mathbf{B}^n U(1)_{conn}$ as above, the composite

$$
  \chi
   \;
   \colon
   \;
  \mathbf{Fields}
    \stackrel{\exp(i S)}{\longrightarrow}
  \mathbf{B}^n U(1)
    \stackrel{\rho}{\longrightarrow}
  \mathbf{B} GL_1(E)
    \stackrel{}{\longrightarrow}
  Pic(E)
    \longrightarrow
  E Mod
$$

modulates the associated _[[higher prequantum line bundle|higher prequantum E-line bundle]]_.

A [[section]] of $\chi$ is a _higher [[wavefunction]]_, hence a _higher [[quantum state]]_.

(At this point this looks un-[[polarization|polarized]], but in fact we will see in the next section that the notion of [[polarization]] in [[higher prequantum geometry]] is automatic, but appears in a [[holography|holographic]]/[[boundary field theory|boundary field theory]] way in [[codimension]] $(n-1)$ instead here in codimension $n$.)

Accordingly, the [[space of sections]] of $\chi$ is the higher [[space of quantum states]] in [[codimension]] 0. 

If $X$ is a [[discrete ∞-groupoid]] then the space of sections has a particularly nice description, on which we focus for a bit:

The space of co-sections is the [[(∞,1)-colimit]]

$$
  E_{\bullet + \chi}(X) 
  \; \coloneqq\;
  \underset{\to}{\lim}
  \chi
  \;
  \in E Mod
  \,.
$$

This is also known as the _$\chi$-twisted $E$-[[Thom spectrum]]_ of $X$ ([Ando-Blumberg-Gepner 10](#ABG)).

* a map $E \to E_{\bullet + \chi}(X)$ is a [[cycle]] in $\chi$-[[twisted cohomology|twisted]] $E$-[[generalized homology]] of $X$;

* a map $E_{\bullet + \chi}(X) \to E$ is a [[cocycle]] in $\chi$-[[twisted cohomology|twisted]] $E$-[[generalized cohomology]] of $X$

  Hence we write

  $$
    E^{\bullet + \chi}\left(X\right)
    \coloneqq
    \left[
      E_{\bullet + \chi}\left(X\right),
      \,
      E
    \right]
    \,.
  $$

Generally, for $\chi_i \colon X_i \to E Mod$ two $E$-[[(∞,1)-module bundles]] over two spaces, a map

$$
  E_{\bullet + \chi_1}(X_1)
  \longrightarrow
  E_{\bullet + \chi_2}(X_2)
$$

is a [[cocycle]] in $(\chi_1, \chi_2)$-[[twisted cohomology|twisted]] [[bivariant cohomology|bivariant]] $E$-[[cohomology]].

Now given a [[local action functional]] on a space of [[trajectories]], hence a [[correspondence]] as above, this induces an [[integral kernel]] for linear maps between sections of [[higher prequantum line bundles]]:

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
     && \swArrow_{\rho(\xi)} &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\chi_{in}}}\searrow
    &&
    \swarrow_{\mathrlap{\chi_{out}}}
    \\
    && E Mod
  }
  \;\;\;
  \coloneqq
  \;\;\;
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
     && \swArrow_\xi &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\exp(i S_{in})}}\searrow
    &&
    \swarrow_{\mathrlap{\exp(i S_{out})}}
    \\
    && \mathbf{B}^n U(1)
    \\
    && \downarrow
    \\
    && B GL_1(E)
    \\
    && \downarrow
    \\
    && Pic(E)
    \\
    && \downarrow
    \\
    && E Mod
  }
$$

This is the [[integral kernel]] induced by the action functional, and acting on spaces of sections of the [[higher prequantum line bundle]].

The [[linear map]] induced by these higher [[integral kernels]] is to be the _[[quantum propagator]]_. This we come to in the next section.

Notice that forming co-sections constitutes an [[(∞,1)-functor]]

$$
  E_{\bullet + (-)}(-)
  \;\colon\;
  \mathbf{H}_{/\mathbf{B}^n U(1)_{conn}}
  \longrightarrow
    E Mod
  \,.
$$

Therefore forming co-sections sends an [[integral kernel]] as above to a [[correspondence]] of $E$-[[(∞,1)-modules]]:

$$
  \array{
    && \mathbf{Fields}_{traj}
    \\
    & {}^{i_{in}}\swarrow && \searrow^{\mathrlap{i_{out}}}
    \\
    \mathbf{Fields}_{in}
     & & \swArrow_{\simeq}  & &
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{\chi_{in}}}\searrow
    &&
    \swarrow_{\mathrlap{\chi_{out}}}
    \\
    && E Mod
    \\
    \,
    \\
    \,
    \\
   E_{\bullet + \chi_{in}}(\mathbf{Fields}_{in})
    & \stackrel{(i_{in})_\ast}{\longleftarrow}&
   \array{
   E_{\bullet + i_{in}^\ast\chi_{in}}(\mathbf{Fields}_{traj})
    \\
    \simeq 
    \\
   E_{\bullet + i_{out}^\ast\chi_{out}}(\mathbf{Fields}_{traj})
    }
    & \stackrel{(i_{out})^\ast}{\longrightarrow}&
   E_{\bullet + \chi_{out}}(\mathbf{Fields}_{out})
  }
  \,.
$$


The actual [[quantization]]/[[path integral as a pull-push transform]] map now consists in forming [[dual morphism]] in $E Mod$ such as to turn one of the projections of such a correspondence arround a produce a [[quantum propagator]]

$$
  E^{\bullet + \chi_{in}}(\mathbf{Fields}_{in})
    \longrightarrow
  E^{\bullet + \chi_{out}}(\mathbf{Fields}_{out})
$$

that maps the incoming [[quantum states]]/[[wavefunctions]] to the outgoing ones.


#### Cohomological quantization by pull-push
 {#ExpositionCohomologicalQuantization}


What we need now for [[quantization]] is a [[path integral]]
map that adds up the values of the [[action functional]] over the space of trajectories, a functor of the form

$$
  \int (-)
  \;\;
   \colon
  \;\;
   Corr_n\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
  \to 
   (E Mod^{\Box^n})^\otimes
$$

As such this will in general only exist for [[schreiber:∞-Dijkgraaf-Witten theory]] where $\mathbf{Fields}$ is a [[discrete ∞-groupoid]] and hence has a "counting measure". This case has been considered in ([Freed-Hopkins-Lurie-Teleman 09](#FreedHopkinsLurieTeleman09), [Morton 10](#Morton10)).

In the general case the path integral requires that we _choose_ a suitable [[measure]]/[[orientation]] on the spaces of fields. 
We see below what this means, for the moment we just write 

$$
  Corr^{or}_n(\mathbf{H}_{/\mathbf{B}^n U(1)})^\otimes
$$ 

(i.e. with an ${(-)}^{or}$-superscript) as a mnemonic for a suitable [[(∞,n)-category]] of suitably oriented/measured spaces of fields with action functional. Then we may consider lifts of the action functional to _measure-valued_ action functionals

$$
  \exp(i S) \, d\mu
  \;\colon\;
  Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes

  \to
  \left(
   E Mod^{\Box^n}
  \right)^\otimes
  \,.
$$

A [[path integral]] is then to be a monoidal functor of the form

$$
  \int(-) \;\colon\;
  Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
  \to 
  \left(
    E Mod^{\Box^n}
  \right)^\otimes
  \,.
$$

This we discuss now below. Once we have such a [[path integral]] functor, the [[quantization]] 
process is its [[composition]] with the given [[prequantum field theory]] $\exp(i S) \, d \mu$ to obtain the genuine quantized [[quantum field theory]]:

$$
  \array{
    \underset{\phi \in \mathbf{Fields}}{\int} 
     \exp(i S(\phi)) \, d \mu(\phi)
    &
    \colon
    &
    Bord_n^\otimes
     &\stackrel{\exp(i S)\, d\mu}{\to}& 
    Corr_n^{or}\left(\mathbf{H}_{/\mathbf{B}^n U(1)}\right)^\otimes
    &\stackrel{\int (-) }{\to}&
    \left(
     E Mod^{\Box^n}
    \right)^\otimes
    \\
    && & {}_{\mathllap{Fields}}\searrow & \downarrow
    \\
    && && Corr_n\left(\mathbf{H}\right)^\otimes
  }
  \,.
$$


We realize this now by [[fiber integration in generalized cohomology]].

While traditionally the definition of [[path integral]] is notoriously elusive, here we make use of general abstract but basic facts of [[higher linear algebra]] in a _[[tensor (∞,1)-category]]_ (a [[stable (∞,1)-category|stable]] and [[symmetric monoidal (∞,1)-category|symmetric monoidal]] [[(∞,1)-category]]): the simple basic idea is that

_Cohomological integration_

1. _Fiber integration of $E$-modules along a map is forming the [[dual morphisms]]_ of pulling back $E$-modules.

1. The choice of _measure_ against which one integrates is the choice of identification of [[dual objects]].

More in detail, given a [[monoidal category]] $\mathcal{C}^\otimes$ and given a [[morphism]]

$$
  f \;\colon\; V_1 \to V_2
$$

in $\mathcal{C}$, an _[[fiber integration]]/[[push-forward in generalized cohomology|push-forward]]/[[index|index map]]_ is just

* forming the [[dual morphism]] $f^\vee \colon V_2^\vee \to V_1^\vee$;

* such that [[equivalences]] $V_i^\vee \simeq V_i$ exhbiting self-[[dual objects]] exist ([[Poincaré duality]]) and have been chosen ([[orientation in generalized cohomology|orientation]]).

This allows in total to have a morphism between the same objects, but in the opposite direction

$$
  f^! 
   \;\colon\;
  V_2
   \stackrel{\;\simeq\;}{\to} 
  V_2^\vee
   \stackrel{\; f^\vee \;}{\to}
  V_1^\vee
    \stackrel{\; \simeq \;}{\to}
  V_1
  \,.
$$

That this is also the mechanism of [[fiber integration in generalized cohomology]] is almost explicit in the literature ([[Alexander-Whitehead-Atiyah duality]]), if maybe not fully clearly so. The statement is discussed explicitly in ([Nuiten 13, section 4.1](#Nuiten13)).

First, the basic example to keep in mind of is integration in [[ordinary cohomology]]. Write $E = H R = H \mathbb{C}$ for the [[Eilenberg-MacLane spectrum]] of the [[complex numbers]]. Then for $X$ a manifold, the [[mapping spectrum]] 

$$
  H R^\bullet(X)
  \coloneqq
  [X,H R]
$$

is the [[ordinary cohomology]] of $X$, its dual the [[ordinary homology]], with [[coefficients]] in $R$.

For $X$ a [[closed manifold]], [[Poincaré duality]] asserts that  $H R^\bullet(X) \in H R Mod$ is essentially a self-[[dual object]], except for a shift in degree: a choice of [[orientation]] of $X$ induces an [[equivalence]]

$$
  H R^\bullet\left(X\right)
    \underoverset{\simeq}{\;\; PD_X\;\;}{\to} 
  \left( 
   H R^{\bullet+ dim(X)}\left(X\right)\right)^\vee
  \simeq
  H R_{\bullet + dim(X)}\left(X\right)
  \,.
$$

Using this, for $f \colon X \to Y$ a map of [[closed manifolds]] of [[dimension]] $d$, a compatible choice of [[orientation]] of both $X$ and $Y$ induces from the canonical push-forward map $f_\ast$ on homology the [[Umkehr map]]/push-forward map on cohomology, by the composition

$$
  f^!
  = 
  \int_f
    \;\colon\;
  H R^\bullet(X)
   \underoverset{\simeq}{\;PD_X\;}{\to}
  H R_{\bullet + dim(X)}(X)
   \stackrel{\; f_\ast \;}{\to}
  H R_{\bullet + dim(X)}(Y)
   \underoverset{\simeq}{\;PD_Y^{-1}\;}{\to}
  H R^{n-(dim(X)-dim(Y))}(Y)
  \,.
$$

This is ordinary [[integration]]: if $X$ and $Y$ are [[smooth manifolds]], then $H \mathbb{R}^\bullet(X)$ is modeled by [[differential forms]] on $X$, $PD_X$ is given by a choice of [[volume form]] and $f^! = \int_{f}$ is ordinary [[integration of differential forms]]. 

The shift in degree here seems to somewhat break the simple pattern. In fact this is not so, if only we realize that since we are working over spaces $X$, we should use a _relative/fiberwise_ point of view and regard not duality in $E Mod$ itself, but in the functor categories $Func(X, E Mod)$, which is fiberwise duality in $E Mod$.

Accordingly, given an $E$-[[(∞,1)-module bundle]]

$$
  \chi \;\colon \;  X \to E Mod
$$

we form not just the mapping space $E^\bullet(X) = [X, E]$ as above, but form the space of [[sections]] of this bundle, which we write:

$$
  E^{\bullet + \chi}(X) \coloneqq \Gamma_X(\chi)
$$

Here for $X$ a [[discrete ∞-groupoid]]

$$
  \Gamma_X(\chi) \coloneqq [\underset{\to}{\lim} \chi, E]
  \,.
$$

Consider now a morphism 

$$
  \array{
    X && \stackrel{f}{\to} && Y
    \\
    & {}_{\mathllap{f^\ast \chi}}\searrow &\swArrow& \swarrow_{\mathrlap{\chi}}
    \\
    && E Mod 
  }
$$

along which we want to integrate, whith $\chi$ invertible in $Func(Y, E Mod)$: $\left(\chi^\vee\right)^\vee \simeq \chi$.
 $\left(\chi^\vee\right)^\vee \simeq \chi$.

Observe that we have the pair of [[adjoint triples]] of left/right [[Kan extensions]] and [[colimits]]/[[limits]]

$$  
  \array{
    X &\stackrel{f}{\to}& Y &\stackrel{p}{\to}& \ast
    \\
    \\
    Func(X, E Mod)
     &\stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^\ast}{\leftarrow}}{\underset{f_\ast}{\to}}}
     &
    Func(Y, E Mod)
     &\stackrel{\overset{p_!}{\to}}{\stackrel{\overset{p^\ast}{\leftarrow}}{\underset{p_\ast}{\to}}}
    &
    E Mod
  }
  \,.
$$

Notice that $f^\ast$ preserves duals, but $f_!$ may not. 

If $f_! f^\ast \chi^\vee$ is a [[dualizable object]], say that a *choice of twisted orientation* of $f$ in $\chi$-[[twisted cohomology]] is a choice of $\beta \colon X \to E Mod$ together with a choice of a [[equivalence]] (if such exists) of the form

$$
  PD 
   \;\colon \;
  \left( f_! f^\ast \chi^\vee
  \right)^\vee
  \simeq
  f_!\left(
    f^\ast \chi + \beta
  \right)
  \,,
$$

hence a choice of correction of $f_!$ preserving the duality of $f^\ast \chi$.
 

Then the $(f_! \dashv f^\ast)$ [[counit of an adjunction|counit]]

$$
  f_! f^\ast \chi^\vee \to  \chi^\vee
$$

induces the [[dual morphism]]

$$
  \chi 
    \longrightarrow
  \left(f_! f^\ast \chi^\vee \right)^\vee 
    \underoverset{\simeq}{PD}{\longrightarrow}
  f_!\left(
    f^\ast \chi + \beta
  \right)
$$

and under $\left[ p_! \left( - \right), E \right]$ this becomes

$$
  \left[p_! f_! \left(f^\ast \chi + \beta\right), E\right]
  \longrightarrow
  \left[p_! \chi , E\right]
$$

which is 

$$
  \int_f
  \;\colon \;
  E^{\bullet + f^\ast \chi + \beta}(X)
  \longrightarrow
  E^{\bullet + \chi}(Y)
  \,.
$$

This we may call the the _[[twisted cohomology|twisted]] [[fiber integration in generalized cohomology|fiber integration]] along $f$_ in $E$-[[cohomology]], or the _twisted $E$-[[index]] map_ of $f$_, induced by $(\beta, PD)$. If $\beta = 0$ then we call $PD$ an _[[orientation in generalized cohomology|orientation]]_ of $f$ in $\chi$-twisted cohomology.


Notice that

* Under fiber integration in [[twisted cohomology]], the twist may change.

* Grading in cohomology is just one incarnation of twist. Hence the fact that the twist changes under duality was already seen above in the ordinary case of [[Poincaré duality]] in [[ordinary cohomology]]. 

* For the special case that $X$ is a [[manifold]], [[Atiyah duality]] identifies the dual cohomology spectrum with the [[Thom space]] cohomology spectrum. Then a choice of orientation amounts to a choice of [[Thom isomorphism]], as traditionally considered.




## General theory
 {#GeneralTheory}


We survey here some key aspects of a general theory of geometric twisted differential cohomology, following ([DCCT](#Schreiber)), in which the above examples find a formal home. This is meant as a reference for readers of the _[Examples](#Examples)_-section who wish to see pointers to formal details.

$\,$

We base the formulation of [[physics]]/[[string theory]] on the [[foundations]] of _[[homotopy type theory|homotopy type theory]]_, [[categorical semantics|interpreted]] in _[[(∞,1)-toposes]]_. This provides a nicely natural and expressive language for the purpose of twisted smooth cohomology in string theory. 

The following table indicates the hierarchy of [[axioms]] that we invoke, the fragments of [[theory]] that can be [[categorical semantics|interpreted]] with these and the [[models]] that we need. Essentially all of the above discussion works in the model [[Smooth∞Grpd]]. A more encompassing treatment uses [[supergeometry]] and works in the model [[SmoothSuper∞Grpd]].


| [[axioms]]  | [[syntax]] | [[semantics]] | typical [[models]] | expressiveness |
|--|---|---|---|---|
| bare minimum | [[homotopy type theory]] | [[(∞,1)-topos theory]] | [[∞Grpd]], [[Super∞Grpd]] | [[cohomology]], [[principal infinity-bundle|principal bundles]], [[twisted cohomology]], [[associated infinity-bundle|associated]] and [[twisted bundles]] |
| +[[local (∞,1)-topos|locality]]+[[locally infinity-connected (infinity,1)-topos|∞-connectedness]] | [[cohesive homotopy type theory]] | [[cohesive (∞,1)-topos]] |  [[Smooth∞Grpd]], [[SmoothSuper∞Grpd]] |  [[geometric realization]], [[differential cohomology]], [[infinity-Chern-Weil theory|Chern-Weil theory]] [[schreiber:infinity-Chern-Simons theory|Chern-Simons theory]], [[schreiber:infinity-geometric prequantization|geometric quantization]] |
| +[[cohesive (infinity,1)-topos -- infinitesimal cohesion|infinitesimals]] | differential homotopy type theory | [[cohesive (infinity,1)-topos -- infinitesimal cohesion|differential (∞,1)-topos]] | [[SynthDiff∞Grpd]] | [[de Rham space]], [[jet bundle]], [[étale infinity-groupoid|étale groupoid]], [[orbifold]]  |






### Homotopy type theory


Traditionally a _[[homotopy type]]_ is a [[topological space]] regarded up to [[weak homotopy equivalence]], hence equivalently an _[[∞-groupoid]]_. More generally, we think of parameterized homotopy types -- of _[[∞-stacks]]_ or _[[(∞,1)-sheaves]]_ -- as _geometric homotopy types_. The collection of such forms an _[[(∞,1)-topos]]_ $\mathbf{H}$. One regards [[(∞,1)-topos theory]] as part of [[homotopy theory]], and, more specifically, the [[internal language]] of $\mathbf{H}$ is a _[[homotopy type theory|homotopy-type theory]]_.

We discuss now some basic structures that are expressible in such bare homotopy-type theory. (The fundamentals are due to [[Charles Rezk|Rezk]] and [[Jacob Lurie|Lurie]], see _[[Higher Topos Theory]]_. We point out the perspective of [[twisted cohomology]] in slices and add some aspects about higher bundle theory from ([NSS](#NSS))). 

Where useful, we indicate some of the discussion in formal [[homotopy type theory]] [[syntax]], see _[[HoTT methods for homotopy theorists]]_ for more along such lines.


#### Cohomology
 {#Cohomology}

A [[group object in an (infinity,1)-category|group object]] in an [[(∞,1)-topos]] is a groupal [[A-∞ algebra|A-∞]]-homotopy type: an _[[∞-group]]_.


By [[looping and delooping]] there is an [[equivalence of (∞,1)-categories|equivalence]]

$$
  Grp(\mathbf{H})
   \stackrel{\overset{\Omega}{\leftarrow}}{\underoverset{\mathbf{B}}{\simeq}{\to}}
  \mathbf{H}_{\geq 1}^{*/}

$$

between group objects and [[pointed object|pointed]] 
[[n-connected object of an (∞,1)-topos|connected]] homotopy types.

+-- {: .num_remark #DeloopingInTypeTheory}
###### Remark

If $pt : \mathbf{B}G$ is the essentially uniqe point of the [[n-connected object of an (∞,1)-topos|connected]] type $\mathbf{B}G$, then the group type itself is simply

$$
  G \coloneqq \vdash (pt \simeq pt) : Type
  \,,
$$

the type of auto-equivalences of $pt$ in $\mathbf{B}G$.

=--

For $A$ a group object which admits an $n$-fold [[delooping]] $\mathbf{B}^n A$ and $X \in \mathbf{H}$ any object, we write

* $\mathbf{H}(X, \mathbf{B}^n A)$ for the space of degree-$n$ $A$-[[cocycles]] $c : X \to A$;

* $H^n(X,A) \coloneqq \pi_0 \mathbf{H}(X, \mathbf{B}^n A)$ for the degree-$n$ $A$-[[cohomology]] of $X$.


#### Principal bundles
 {#PrincipalBundles}

For $G \in Grp(\mathbf{H})$, $G$-cocycles on $X$ have an equivalent geometric interpretation as $G$-[[principal ∞-bundles]]: these are types 

$$
  \array{
    P 
    \\
    \downarrow
    \\
    X
  }
$$

over $X$ equipped with a $G$-[[action]] $\rho : P \times G \to P$ over $X$ such that the [[(∞,1)-colimit|∞-quotient]] of the action is $X$.

**Theorem** There is an [[equivalence of (∞,1)-categories|equivalence]] between the [[∞-groupoid]] of $G$-principal bundles over $X$, and the cocycle $\infty$-groupoid of $G$-cohomology over $X$.

$$
  \mathbf{H}(X, \mathbf{B}G)
   \stackrel{\overset{\underset{\to}{\lim}}{\leftarrow}}{\underoverset{fib}{\simeq}{\to}}
  G Bund(X)    
$$

From left to righr the equivalence is established by sending a cocycle $X\to \mathbf{B}G$ to its [[homotopy fiber]].

([NSS](#NSS))


+-- {: .num_remark }
###### Remark

With $G$ the type as in remark \ref{DeloopingInTypeTheory}, the principal bundle corresponding to a coycle $\phi : X \to \mathbf{B}G$ is

$$
  P 
   \;
    \coloneqq 
   \;
  x : X \vdash ( \phi(x)  \simeq  pt ) : Type
$$

And the action is 

$$
  \begin{aligned}
    & \rho : P \times G \to G
    \\
    & \;\;\coloneqq
    (( x : X; p : (\phi(x) \simeq pt)), g : (pt \simeq pt) )
    \mapsto
    (x : X; g \circ \phi)
  \end{aligned}
$$


=--

#### Twisted cohomology
 {#TwistedCohomology}


For $\mathbf{H}$ an [[(∞,1)-topos]] and $\mathbf{B}G \in \mathbf{H}$, the collection of morphisms into $\mathbf{B}G$ is the [[slice (∞,1)-topos]] $\mathbf{H}_{/ \mathbf{B}G}$.

The [[cohomology]] in $\mathbf{H}_{/\mathbf{B}G}$ is naturally interpreted as follows

1. a local coefficient object $\mathbf{c} : E \to \mathbf{B}G$ is a _universal bundle of local coefficients_;

1. a domain object $\phi : X \to \mathbf{B}G$ is a _twisting bundle_;

1. a [[cocycle]] 

   $$
     \array{
       X &&\stackrel{\sigma}{\to}&& E
       \\
       & {}_{\mathllap{\phi}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{c}}}
       \\
       && \mathbf{B}G
     }
   $$ 

   is equivalently a [[section]] of the [[(∞,1)-pullback]] bundle $\phi^* E \to X$;

   $$
     \array{  
        && \phi^* E &\to & E
        \\
        &{}^{\mathllap{\sigma}}\nearrow& \downarrow && \downarrow^{\mathbf{c}}
        \\
        X &\stackrel{id}{\to}& X &\stackrel{\phi}{\to}& \mathbf{B}G
     }
   $$

* the [[cohomology]] 

  $$
    \mathbf{c}Struc_{\phi}(X)
    \coloneqq
    \mathbf{c}(\phi)
    \coloneqq
    \mathbf{H}_{/\mathbf{B}G}(\phi, \mathbf{c})
  $$

  is the $\phi$-[[twisted cohomology]] of $X$ (with local coefficients in the [[homotopy fiber]] $F$ of $\mathbf{c}$).

+-- {: .num_remark }
###### Remark

In the [[syntax]] of the [[theory]] the [[type]] of twisted cocycles is

$$
  [\phi, \mathbf{c}]
   \coloneqq
  \vdash \prod_{b \in \mathbf{B}G} (X(b) \to E(b)) : Type
  \;\;
  =
  \;\;
  \vdash \prod_{x : X} E(\phi(x)) : Type
$$

(see [here](http://www.ncatlab.org/nlab/show/locally%20cartesian%20closed%20category#RelationCartesianClosureBaseChangeInTypeTheory)).

While on the right this expresses the collection of sections of the pullback bundle, the left hand side expresses explicitly a $\mathbf{B}G$-parameterized collection of cocycles $X(b) \to E(b)$.

=--

+-- {: .num_remark }
###### Remark

Cocycles in twisted cohomology relative to a local coefficient bundle
$\mathbf{c} : E \to \mathbf{B}G$ do not pull back along morphisms in $\mathbf{H}$ (unless $G$ is trivial), but do pull back along morphisms in $\mathbf{H}$ that are lifted to morphisms in the slice $\mathbf{H}_{/ \mathbf{B}G}$.

=--

#### Associated and twisted bundles
 {#AssociatedAndTwistedBundles}

For

$$
  \array{
    \mathbf{B}A &\to& \mathbf{B}\hat G
    \\
    && \downarrow^{\mathrlap{\mathbf{c}}}
    \\
    && \mathbf{B}G
  }
$$

a universal local coefficient bundle in $\mathbf{H}$ and $\phi : X \to \mathbf{B}G$ a twist and $\sigma : X \to \mathbf{B}\hat G$ a section, hence a cocycle in $\phi$-[[twisted cohomology]], the corresponding geometric object is the [[twisted ∞-bundle]] $\tilde \sigma$ on the total space $P$ of $\phi$

$$
  \array{
    \tilde P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    P &\stackrel{\tilde \sigma}{\to}& \mathbf{B}A &\to& * 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    X 
     &\stackrel{\sigma}{\to}&
   \mathbf{B}\hat G
     &\stackrel{\mathbf{c}}{\to}&
   \mathbf{B}G
  }
  \,.
$$

([NSS](#NSS))

(...)


### Cohesive homotopy type theory

In general the [[geometry]] encoded by an [[(∞,1)-topos]] can be exotic. Two extra axioms ensure that it is modeled locally on $\infty$-connected geometrical archetypes, such as for instance on _[[open disks]]_ for [[Euclidean-topological ∞-groupoid|Euclidean-topological geometry]] and _smooth open disks_ for [[smooth ∞-groupoid|smooth geometry]]. Following [[Bill Lawvere|Lawvere]], we call this refinement _[[cohesive homotopy type theory]]_ [[categorical semantics|interpreted]] in _[[cohesive (∞,1)-toposes]]_.





#### Geometric realization 


A [[cohesive (∞,1)-topos]] is in particular equipped with a [[left adjoint|left]] [[adjoint (∞,1)-functor|derived adjoint]] $\Pi$ to the [[locally constant ∞-stack]]-functor $Disc$

$$
  (\Pi \dashv Disc)
  : 
  \mathbf{H}
   \stackrel{\overset{\Pi}{\to}}{\underset{Disc}{\hookleftarrow}}
  \infty Grpd
  \,.
$$

We may think of $\Pi$ as being the functor that sends a [[smooth ∞-groupoid]] $X$ to its [[fundamental infinity-groupoid in a locally infinity-connected (infinity,1)-topos|fundamental path ∞-groupoid]]

Under the identification (see _[[homotopy hypothesis|homotopy hypothesis theorem]]_)

$$
  \infty Grpd \stackrel{{\vert-\vert}}{\to} Top
$$

this identifies with [[geometric realization]] of geometric homotopy types / [[∞-stacks]].

We say that a lift of a [[diagram]] in [[∞Grpd]] through $\Pi$ is a **geometric refinement** of the diagram.



#### Differential cohomology

Write $\mathbf{\Pi} \coloneqq Disc \circ \Pi$; 
and $\flat \coloneqq Disc \circ \Gamma$.

For $G$ an [[∞-group]], write $\flat_{dR} \mathbf{B}G \coloneqq * \times_{\mathbf{B}G} \flat \mathbf{B}G$: the _de Rham coefficient object_ for $\mathbf{B}G$.

There is a canonical morphism $\theta : G \to \flat_{dR} \mathbf{B}G$: this identifies as the canonical _[[Maurer-Cartan form]]_ on the [[∞-group]] $G$.

For $G = \mathbf{B}^n U(1)$ the [[circle n-group|circle (n+1)-group]] we call $curv  \coloneqq_{\mathbf{B}^n U(1)} : \mathbf{B}^n U(1) \to \flat_{dR} \mathbf{B}^{n+1} U(1)$ the _universal [[curvature]] class_ in degree $(n+1)$.

The $curv$-[[twisted cohomology]] in $\mathbf{H}$ identifies with [[ordinary differential cohomology]]. 

$$
  \array{
    \mathbf{B}^n U(1)_{conn} &\to& \Omega^{n+1}_{cl}(-)
    \\
    \downarrow && \downarrow
    \\
    \mathbf{B}^n U(1) &\stackrel{curv}{\to}& \mathbf{B}^{n+1} U(1)_{conn}
  }
$$


#### Chern-Weil theory

(...)

[[∞-Chern-Weil theory introduction]]




### Differential homotopy-type theory

(...)

[[cohesive (infinity,1)-topos -- infinitesimal cohesion|infinitesimals]]

#### de Rham stack

(...)

#### &#201;tale stacks / orbifolds 

(...)

## Related entries
 {#RelatedEntries}

An entry with discussion of and list of examples of twisted differential structures is

* _[[twisted differential c-structures]]_.


Related expositions include the following:

* [[geometry of physics]]

* [[fiber bundles in physics]]

* [[string theory FAQ]]

* [[twisted smooth cohomology in string theory]]

* [[motives in physics]]

* [[Hilbert's sixth problem]]

* [[model theory and physics]]

* [[L-infinity algebras in physics]]

* [[motivation for sheaves, cohomology and higher stacks]]

* [[applications of (higher) category theory]]

* [[motivation for higher differential geometry]]

* [[motivation for cohesion]]






## References
 {#References}

The string-theoretic aspects of the above discussion owe a lot to [[Hisham Sati]], who has pointed out the appearance of various twisted structures in string theory, notably in the series of articles

* [[Hisham Sati]], _[[Geometric and topological structures related to M-branes]]_ , part I ([arXiv:1001.5020](http://arXiv.org/abs/1001.5020)), part _II: Twisted $String$ and $String^c$ structures_ ([arXiv:1007.5419](http://arxiv/1007.5419)); part _III: Twisted higher structures_ ([arXiv:1008.1755](http://arxiv.org/abs/1008.1755))
  {#Sati10}

The notion of [[twisted cohomology]] by sections of twisting coeffcient $\infty$-bundles used here is similar to that in 

* [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81) ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 {#ABG}

but considered in the non-stable context of [[nonabelian cohomology]] and refined from bare homotopy types to [[cohesive homotopy type theory|geometric homotopy types]].

The fundamental observation that background gauge fields in string theory are modeled by (twisted) [[differential cohomology]] goes back to 

* [[Dan Freed]], _[[Dirac charge quantization and generalized differential cohomology]]_
 {#Freed}

and literature referenced there. For this classical literature, notably on the example of _[[twisted K-theory|twisted]]_ and _[[differential K-theory|differential]] [[K-theory]]_, as well as on _[[orientifolds]]_, see the lists of references provided at these entries, notably

* [[Dan Freed]], _K-Theory in Quantum Field Theory_, Current developments in Mathematics (2001) International Press Somerville ([arXiv:math-ph/0206031](http://arxiv.org/abs/math-ph/0206031))

The [[higher dimensional Chern-Simons theory|7d Chern-Simons theory]] that the [[supergravity C-field]] participates in, the relation of the flux quantization to the corresponding [[holographic principle|holographic]] description of the [[self-dual higher gauge field|self-dual]] field on the [[M5-brane]] has been discussed in 

* [[Edward Witten]], _Five-Brane Effective Action In M-Theory_ ([arXiv:hep-th/9610234](http://arxiv.org/abs/hep-th/9610234))
 {#Witten96}

* [[Edward Witten]], _On Flux Quantization In M-Theory And The Effective Action_, J.Geom.Phys.22:1-13 (1997) ([arXiv:hep-th/9609122](http://arxiv.org/abs/hep-th/9609122))
 {#Witten96b}

A precise mathematical formulation of the proposal made there is given in

* [[Mike Hopkins]], [[Isadore Singer]], _[[Quadratic Functions in Geometry, Topology, and M-Theory]]_
 {#HopkinsSinger}

in terms of [[quadratic refinement]] of [[secondary intersection pairing]] via [[differential integral Wu structures]]. This also lays the mathematical foundation of much of [[differential cohomology]].

The suggestion that it is the [[∞-stack (∞,1)-topos]] over the [[site]] of [[smooth manifolds]] which is the right context for studying the twisted differential smooth cohomology in string theory was made in 

* [[Urs Schreiber]], _[[schreiber:Background fields in twisted differential nonabelian cohomology]]_, talk at _[[Oberwolfach Workshop, June 2009 -- Strings, Fields, Topology]]_
 {#Schreiber09}


The smooth $\infty$-stack refinements of these structures, as discussed above, have been developed in articles including the following

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:L-∞ algebra connections]]_ 
 {#SSSa}

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]],_[[schreiber:Fivebrane structures]]_
 {#SSSb}

* [[Hisham Sati]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Twisted Differential String and Fivebrane Structures]]_, Communications in Mathematical Physics, October 2012, Volume 315, Issue 1, pp 169-213 ([arXiv:0910.4001](http://arxiv.org/abs/0910.4001))
 {#SatiSchreiberStasheff09}

* [[Domenico Fiorenza]], [[Urs Schreiber]], [[Jim Stasheff]], _[[schreiber:Cech Cocycles for Differential characteristic Classes]]_
 {#FSSa}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:7d Chern-Simons theory and the 5-brane|Multiple M5-branes, String 2-connections, and 7d nonabelian Chern-Simons theory]]_
 {#FSSb}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:The moduli 3-stack of the C-field]]_
 {#FSSc}

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_
 {#FSSd}

* [[Thomas Nikolaus]], [[Urs Schreiber]], [[Danny Stevenson]], _[[schreiber:Principal ∞-bundles -- theory, presentations and applications]]_ ([arXiv:1207.0248](http://arxiv.org/abs/1207.0248), [arXiv:1207.0249](#http://arxiv.org/abs/1207.0249))
 {#NSS}

* [[Domenico Fiorenza]] [[Chris Rogers]], [[Urs Schreiber]], _[[schreiber:Higher geometric prequantum theory]]_, 2013 ([arXiv:1304.0236](http://arxiv.org/abs/1304.0236))
  {#FiorenzaRogersSchreiber13}


* [[Urs Schreiber]] et. al., _[[schreiber:Local prequantum field theory]]_
  {#lpqft}

* [[Urs Schreiber]], _[[schreiber:Classical field theory via Cohesive homotopy types]]_
  {#SchreiberClassical}

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local boundary prequantum field theory]]_, Master thesis Utrecht 2013
  {#Nuiten2013}

* [[Urs Schreiber]], _[[schreiber:Synthetic Quantum Field Theory]]_
  {#SchreiberSynthetic}


A general theory of such smooth homotopy-types is laid out in 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_, Habilitation thesis, Hamburg 2011
 {#Schreiber}

The observation of the [[tangent (infinity,1)-topos]] is due to 

* [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))
  {#Joyal08}


$\,$

Section A) above originates in notes for an introductory lecture:

* [[Urs Schreiber]], _[Twisted differential structures in string theory](http://maths-old.anu.edu.au/esi/2012/program.html#Schreiber)_ at _[ESI Program on K-Theory and Quantum Fields](http://maths-old.anu.edu.au/esi/2012/)_ (2012)
 {#SchreiberLect}

Closely related lectures at the same program included

* [[Dan Freed]], _Lectures on twisted $K$-theory and orientifolds_ at _[ESI Program on K-Theory and Quantum Fields](http://maths-old.anu.edu.au/esi/2012/)_ (2012) ([pdf](http://www.ma.utexas.edu/users/dafr/ESI.pdf))
 {#FreedLecture}

Later, some special cases of the general notion of twisted fields considered [above](#TableOfTwists) are being called _relative fields_ in 

* [[Daniel Freed]], [[Constantin Teleman]], _Relative quantum field theory_ ([arXiv:1212.1692](http://arxiv.org/abs/1212.1692))
 {#FreedTeleman}

as discussed above in the section _[Relative fields](#RelativeFields)_ .

Section B) originates in notes for a talk 

* [[Urs Schreiber]], _[[schreiber:Local prequantum field theory|Local prequantum boundary field theory]]_, talk at _[Twists, generalised cohomology and applications](http://wwwmath.uni-muenster.de/sfb/sfb878/2013/twists.html)_, 2013
  {#SchreiberTwists2013}