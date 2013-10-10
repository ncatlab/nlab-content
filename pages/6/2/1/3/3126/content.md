
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### $(\infty,2)$-Topos theory
+--{: .hide}
[[!include (infinity,2)-topos theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

For $K$ a [[locally presentable (∞,1)-category]] whose objects we think of as [[space]]s of sorts, its **tangent $(\infty,1)$-category**

$$
  (T_{K^{op}})^{op} \to K
$$

is an [[(∞,1)-category]] over $K$, whose objects may be thought of as spaces that are **[[infinitesimal space|infinitesimal]] thickenings** of those of $K$.

More concretely, the tangent $(\infty,1)$-category $T_C \to C$ for $C = K^{op}$ is the fiberwise [[stabilization]] of the [[codomain fibration]] $Func(\Delta[1], C) \to C$.  

This generalizes -- as discussed at [[deformation theory]] -- the classical example of the [[bifibration]] [[Mod]] $\to$ [[CRing]] of the category of all [[module]]s over the cateory [[CRing]] of all commutative rings: 

the fiber of the tangent $(\infty,1)$-category $T_C$ over an object $A \in C$ may be thought of as the $(\infty,1)$-category of **square-0-extensions** $A \oplus N$ of $A$, for $N$ a [[module]] over $A$. Dually, in $K = C^{op}$ we may think of these as being infinitesimal neighbourhoods of 0-sections of [[vector bundle]]s -- or rather of [[quasicoherent sheaves]] -- over whatever [[space]] $A$ is regarded to be the algebra of functions on.
 
A remarkable amount of information about the geometry of these spaces/objects in $K$ is encoded in the fiber of the tangent $(\infty,1)$-category over them. Notably the [[left adjoint|left]] [[adjoint (∞,1)-functor]] 

$$
  \Omega : C \to T_C
$$

to the domain projection $dom : T_C \to C$ turns out to send each $A$ to its [[cotangent complex]] $\Omega(A)$, to be thought of as the module of [[Kähler differential]]s on the space that $A$ is functions on.

A [[category theory|1-categorical]] approximation to the notion of tangent $(\infty,1)$-category is that of [[tangent category]].

## Definition

Let $\mathcal{C}$ be a [[locally presentable (∞,1)-category]].

+-- {: .num_defn #FiberwiseStabilization}
###### Definition
**(fiberwise stabilization)**

For $\mathcal{C}' \to \mathcal{C}$ a [[model structure for quasi-categories|categorical fibration]], [[generalized the|the]] **fiberwise stabilization** $Stab(\mathcal{C}' \to \mathcal{C})$ is -- roughly -- the fibration universal with the property that for each $A \in C$ its [[fiber]] over $A$ is the [[stabilization]] $Stab(\mathcal{C}'_A)$ of the fiber $\mathcal{C}'_A$ over $A$.


=--

This is ([Lurie, section 1.1](#Lurie)) formulated in view of ([Lurie, remark 1.1.8](#Lurie)). There $Stab(\mathcal{C}' \to \mathcal{C})$ is called the _stable envelope_ .

+-- {: .num_defn #TangentCategory}
###### Definition
**(tangent $(\infty,1)$-category)**

[[generalized the|The]] **tangent $(\infty,1)$-category** $T_{\mathcal{C}} \to \mathcal{C}$ is [[generalized the|the]] _fiberwise stabilization_ of the [[codomain fibration]]  $cod : \mathcal{C}^{\Delta^1} \to \mathcal{C}$:

$$
  (T_{\mathcal{C}} \stackrel{p}{\to} \mathcal{C}) := Stab(Func(\Delta[1], \mathcal{C}) \stackrel{cod}{\to} \mathcal{C}  )
  \,.
$$

=--

This is [[Deformation Theory|DT, def 1.1.12]].

Explicitly, the tangent $\infty$-category is given as follows.

+-- {: .num_remark #TangentCatByExplicitFiberwiseStabilization}
###### Remark

Given a presentable [[(∞,1)-category]] $\mathcal{C}$, the [[(∞,1)-functor]] 

$$
  \chi_{cod} \colon \mathcal{C}^{op} \to (\infty,1)Cat
$$

which classifies the [[codomain fibration]] $cod \colon \mathcal{C}^{\Delta^1} \to \mathcal{C}$ under the [[(∞,1)-Grothendieck construction]] factors through the wide non-full inclusion

$$
  (\infty,1)Cat^R \to (\infty,1)Cat
$$

of [[(∞,1)-functors]] which are [[right adjoint|right]] [[adjoint (∞,1)-functors]].  For these the further (now full) inclusion

$$
  i \colon (\infty,1)StabCat^R \hookrightarrow (\infty,1)Cat^R
$$

of the [[stable (∞,1)-categories]] has a [[right adjoint|right]] [[adjoint (∞,1)-functor]]

$$
  (i \dashv Stab)
$$

given by [[stabilization]]. (Note that this is not a functor on all of $(\infty,1)Cat$, where instead the obstructions to functoriality are given by [[Goodwillie calculus]].) 

So the classifying map of the codomain fibration factors through this and hence we can postcompose with the [[stabilization]] functor to obtain

$$
  i \circ Stab i \chi_{cod} \colon \mathcal{C}^{op} \to (\infty,1)Cat
  \,.
$$

This sends an object $c \in \mathcal{C}$ to the [[stabilization]] of the [[slice (∞,1)-category]] over $c$:

$$
  Stab \circ \chi_{cod} \colon c \mapsto Stab(\mathcal{C}_{/c})
  \,.
$$

Again by the [[(∞,1)-Grothendieck construction]] this classifies a [[Cartesian fibration]] over $\mathcal{C}$ and this now is the tangent $(\infty,1)$-category projection

$$
  \array{
    T_{\mathcal{C}}
    \\
    \downarrow^{\mathrlap{p}}
    \\
    \mathcal{C}
  }
  \,.
$$

=--

This is the first part of the proof of [[Deformation Theory|DT. prop. 1.1.9]].


## Properties

### Presentability and limits
 {#PresentabilityAndLimits}

+-- {: .num_prop}
###### Proposition

The tangent $(\infty,1)$-category $T_C$ of the [[locally presentable (∞,1)-category]] $C$ is itself a locally presentable $(\infty,1)$-category.

In particular, it admits all [[(∞,1)-limit]]s and [[(∞,1)-colimit]]s.

=--

This is ([Lurie, prop. 1.1.13](#Lurie)).

Moreover:

+-- {: .num_prop}
###### Proposition

A diagram in the tangent $(\infty,1)$-category $T_{\mathcal{C}}$ is an [[(∞,1)-limit|(∞,1)-(co-)limit]] precisely if

1. it is a [[relative (infinity,1)-limit|relative (∞,1)-(co-)limit]] with respect to the projection $p \colon T_{\mathcal{C}} \to \mathcal{C}$;

1. its image under this projection is an [[(∞,1)-limit|(∞,1)-(co-)limit]] in $\mathcal{C}$.

=--

([Lurie, HigherAlgebra, prop. 8.3.1.12](#LurieHigherAlgebra))



### Relation to modules
 {#RelationToModules}

We discuss how the tangent $(\infty,1)$-category construction indeed generalizes the equivalence between the [[tangent category]] over [[CRing]] and the category [[Mod]] of all [[modules]] over commutative rings.

+-- {: .num_prop}
###### Proposition

Let $\mathcal{O}^\otimes$ be a [[coherent (∞,1)-operad]] and let $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ be a [[stable (∞,1)-category|stable]] $\mathcal{O}$-[[monoidal (∞,1)-category]]. 

Let 

$$
  A \in Alg_\mathcal{O}(\mathcal{C})
$$

be an $\mathcal{O}$-[[algebra over an (infinity,1)-operad|algebra]] in $\mathcal{C}$. Then the [[stabilization]] of the [[over-(∞,1)-category]] over $A$ is canonically equivalent to $Func_\mathcal{O}(\mathcal{O}, Mod_A^\mathcal{O}(\mathcal{C}))$

$$
  Stab( Alg_\mathcal{O}(\mathcal{C})/A)
  \simeq
  Func_\mathcal{O}(\mathcal{O}, Mod_A^\mathcal{O}(\mathcal{C}))
  \,.
$$

=--

This is ([Lurie, theorem 1.5.14](#Lurie)).

+-- {: .num_prop}
###### Proposition

Let $\mathcal{O}^\otimes$ be a [[coherent (∞,1)-operad]] and let $\mathcal{C}^\otimes \to \mathcal{O}^\otimes$ be a [[presentable (∞,1)-category|presentable]] [[stable (∞,1)-category|stable]] $\mathcal{O}$-[[monoidal (∞,1)-category]]. Then there is a canonical [[equivalence of (∞,1)-categories|equivalence]]

$$
  \phi : T_{Alg_\mathcal{O}(\mathcal{C})}
    \stackrel{\simeq}{\to}
  Alg_\mathcal{O}(\mathcal{C}) 
   \times_{Func(\mathcal{O}, Alg_\mathcal{O}(\mathcal{C}))}
  Func_\mathcal{O}(\mathcal{O}, Mod^\mathcal{O}(\mathcal{C}))
$$

of presentble [[Cartesian fibration|fibrations]] over $Alg_\mathcal{O}(\mathcal{C})$.

=--

This is ([Lurie, theorem, 1.5.19](#Lurie)).

In words this says that under the given assumptions, objects of $T_{\mathcal{C}}$ may be identified with pairs

$$
  (A, N)
$$

where 

* $A$ is an $\mathcal{O}$-[[∞-algebra over an (∞,1)-operad|algebra]] in $\mathcal{C}$;

* $N$ is an $A$-[[∞-module over an ∞-algebra over an (∞,1)-operad|module]].


### Tangent $\infty$-topos of an $\infty$-topos

In ([Joyal 08](#Joyal08)) is an argument which should show that for 
$\mathbf{H}$ an [[(∞,1)-topos]] then also the tangent $(\infty,1)$-category $T \mathbf{H}$ is an [[(∞,1)-topos]].

The argument proceeds along the following lines.

Let $seq$ be the [[diagram]] category

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
    &&{}^{\mathllap{p_{n-1}}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_n}}
    \\
    &&\ast &\underset{i_n}{\longrightarrow}& x_n &\stackrel{p_n}{\longrightarrow}& \ast
    \\
    && && {}^{\mathllap{p_n}}\downarrow &\swArrow& \downarrow^{\mathrlap{i_{n+1}}}
    \\
    && && \ast &\stackrel{i_{n+1}}{\longrightarrow}& x_{n+1} &\to& \cdots
    \\
     && && && \downarrow
     \\
     && && && \vdots
    }
  \right\}
  \,.
$$

Given an [[(∞,1)-topos]] $\mathbf{H}$, an [[(∞,1)-functor]]

$$
  X_\bullet \;\colon\; seq \longrightarrow \mathbf{H}
$$

is equivalently 

1. a choice of [[object]] $B \in \mathbf{H}$

1. a sequence of objects $\{X_n\} \in \mathbf{H}_{/B}$ in the [[slice (∞,1)-topos]] over $B$;

1. a sequence of [[morphisms]] $X_n \longrightarrow \Omega X_{n+1}$ from $X_n$ into the [[loop space object]] of $X_{n+1}$ in the slice.

This is a [[prespectrum object]] in $\mathbf{H}_{/B}$. The [[(∞,1)-presheaf (∞,1)-topos]] $\mathbf{H}^{seq}$ is hence the self-indexing of $\mathbf{H}$ with "fiberwise pre-stabilization".

A genuine [[spectrum object]] is a [[prespectrum object]] for which all the structure maps $X_n \stackrel{\simeq}{\longrightarrow}X_{n+1}$ are [[equivalence in an (∞,1)-category|equivalences]]. The [[full sub-(∞,1)-category]] 

$$
  T \mathbf{H} \hookrightarrow \mathbf{H}^{seq}
$$

on the genuine [[spectrum objects]] is the tangent $(\infty,1)$-category.

One observes that the inclusion of spectrum objects into prespectrum objects has a [[left adjoint]] given by a [[filtered (∞,1)-colimit]] construction. Since these filtered colimits commute with [[finite (∞,1)-limits]], it follows that spectrum objects are a left [[exact (∞,1)-functor|exact]] [[reflective sub-(∞,1)-category]] 

$$
  T \mathbf{H} \stackrel{\overset{lex}{\leftarrow}}{\hookrightarrow} \mathbf{H}^{seq}
  \,.
$$

But this means that $T \mathbf{H}$ is an [[(infinity,1)-topos]].

(...)



## Cotangent complex
 {#CotangentComplex}

From its definition as the fiberwise stabilization of the [[codomain fibration]] $cod : Func(\Delta[1], C) \to C$ the tangent $(\infty,1)$-category $p : T_C \to C$ inherits a second $(\infty,1)$-functor to $C$, coming from the _domain_ evaluation

$$
  dom : T_C \to C
  \,.
$$ 

+-- {: .num_prop #CotangentComplexAdjunction}
###### Definition/Proposition
**(cotangent complex)**

The domain evaluation $dom : T_C \to C$ admits a [[left adjoint|left]] [[adjoint (∞,1)-functor]]

$$
  (\Omega \dashv dom) : T_C \stackrel{\overset{\Omega}{\leftarrow}}{\underset{dom}{\to}}
  C
$$

that is also a [[section]] of $p : T_C \to C$ in that 

$$
  (C \stackrel{\Omega}{\to} T_C \stackrel{p}{\to} C) \simeq Id_C
$$ 

and which hence exhibits $C$ as a [[retract]] of $T_C$.

This $\Omega$ is the **cotangent complex $(\infty,1)$-functor** : for $A \in C$ the object $\Omega(A)$ is the [[cotangent complex]] of $A$.

=--


This is ([Lurie, def. 1.1.2, remark 1.2.3](#Lurie)).

In more detail this adjunction is the composite 

$$
  (\Omega \dashv dom)
  \;\colon\;
  T_C
  \stackrel{\overset{\Sigma^\infty_C}{\leftarrow}}{\underset{\Omega^\infty_{C}}{\to}}
  C^{\Delta^1}
  \stackrel{\overset{const}{\leftarrow}}{\underset{dom}{\to}}
  C
  \colon
  \Omega
  \,,
$$

where $(\Sigma^\infty_C \dashv \Omega^\infty_C)$ is the fiberwise [[stabilization]] relative adjunction, def. \ref{FiberwiseStabilization}.

## Examples 

### Of $E_\infty$-rings

+-- {: .num_cor}
###### Corollary

Let $E_\infty$ be the [[(∞,1)-category]] of [[E-∞ ring]]s and let $A \in E_\infty$. Then the [[stabilization]] of the [[over-(∞,1)-category]] over $A$ 

$$
  Stab(E_\infty/A) \simeq A Mod(Spec)
$$

is equivalent to the category of $A$-[[module spectra]].

=--

([Lurie, cor. 1.5.15](#Lurie)).


### Of an $\infty$-topos
 {#ExamplesTangentOfAnInfinityTopos}

We discuss here aspects of the tangent $\infty$-categories of [[(∞,1)-toposes]].


First consider the [[base (∞,1)-topos]] $\mathbf{H} = $ [[∞Grpd]]. 


+-- {: .num_remark #SliceOfinfinityGroupoidsIsFunctorCategory}
###### Remark

For each [[∞-groupoid]]/[[homotopy type]] $X \in \infty Grpd$.
there is a [[natural equivalence|natural]] [[equivalence of (∞,1)-categories]]

$$
  \infty Grpd_{/X}
  \simeq
   Func(X, \infty Grpd)
$$

between the [[slice (∞,1)-category]] of [[∞Grpd]] over $X$ and the [[(∞,1)-functor (∞,1)-category]] of maps $X \to \infty Grpd$.

=--

+-- {: .proof}
###### Proof 

By the [[(∞,1)-Grothendieck construction]].

=--


+-- {: .num_prop}
###### Proposition

For each [[∞-groupoid]]/[[homotopy type]] $X \in \infty Grpd$.
there is a [[natural equivalence|natural]] [[equivalence of (∞,1)-categories]]

$$
  T_X (\infty Grpd) \simeq Func(X, Spec)
$$

between the fiber of the tangent (∞,1)-category of [[∞Grpd]] over $X$, def. \ref{TangentCategory}, and the [[(∞,1)-category]] of [[parameterized spectra]] over $X$.

=--

+-- {: .proof}
###### Proof 

Applying remark \ref{SliceOfinfinityGroupoidsIsFunctorCategory} in remark \ref{TangentCatByExplicitFiberwiseStabilization} yields that

$$
 T_X(\infty Grpd) \simeq Stab(Func(X,\infty Grpd))
  \,.
$$

The statement then follows with the "[stable Giraud theorem](stable%20%28infinity,1%29-category#StabGiraud)".

=--

+-- {: .num_remark}
###### Remark

This means that the tangent $(\infty,1)$-category $T(\infty Grpd)$
is equivalently what in ([Joyal 08, section 30.34](#Joyal08))
is denoted $D(Kan, X)$ in the case that $X = Spec$ is the [[(∞,1)-category of spectra]].

=--


+-- {: .num_prop #TangentOfInfinityGrpdIsTopos}
###### Proposition

The tangent $(\infty,1)$-category $T (\infty Grpd)$ is itself 
an [[(∞,1)-topos]].

=--

+-- {: .proof}
###### Proof 

With the above equivalence this is ([Joyal 08, section 35.5, 35.6](#Joyal08) (with [[Georg Biedermann]])).

=--

+-- {: .num_remark}
###### Remark

The [[terminal object in an (∞,1)-category|terminal object]] in $T \infty Grpd$ should be the [[zero spectrum]] regarded as a parameterized spectrum over the point

$$
  0 \colon \ast \to Spec
  \,.
$$

=--

From this it follows that

+-- {: .num_remark}
###### Remark

The [[global elements]]/[[global sections]] functor (which forms the [[derived hom space|(∞,1)-categorical mapping space]] out of the terminal object)

$$
  \Gamma \coloneqq Hom(\ast, -) 
  \;\colon\; T(\infty Grpd) \to \infty Grpd
$$

sends an $X$-[[parameterized spectrum]] to its base homotopy type $X$.


This functor has a [[left adjoint|left]] and [[right adjoint|right]] [[adjoint (∞,1)-functor]] both given by sending $X$ to the [[zero spectrum]] bundle over $X$.

So we have an infinite chain of [[adjoint (∞,1)-functors]] 

$$
  (\cdots base \dashv 0 \dashv base \dashv 0 \dashv \cdots)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

The functor $0$ is a [[full and faithful (∞,1)-functor]]

$$
  0 \;\colon\; \infty Grpd \hookrightarrow T \infty Grpd
$$

and so the tangent $(\infty,1)$-category is [[cohesive (∞,1)-topos|cohesive]] over [[∞Grpd]], hence by prop. \ref{TangentOfInfinityGrpdIsTopos} $T(\infty Grpd)$ is a [[cohesive (∞,1)-topos]]:


$$
  (\Pi \dashv Disc \dashv \Gamma \dashv coDisc)
  \;
  \colon
  \;
  T(\infty Grpd)
  \stackrel{\overset{base}{\longrightarrow}}{\stackrel{\overset{0}{\leftarrow}}{\stackrel{\overset{base}{\longrightarrow}}{\underset{0}{\leftarrow}}}}
  \infty Grpd
  \,.
$$

Recalling that here $base = cod \circ \Omega^\infty$, we have one more adjunction, the [[cotangent complex]] adjunction due to prop. \ref{CotangentComplexAdjunction}

$$
  \infty Grpd
  \stackrel{
     \overset{\Omega}{\longrightarrow}
  }
  {\underset{dom\circ \Omega^{\infty}}{\leftarrow}}
  T(\infty Grpd)
  \stackrel{\overset{base}{\longrightarrow}}{\stackrel{\overset{0}{\leftarrow}}{\stackrel{\overset{base}{\longrightarrow}}{\underset{0}{\leftarrow}}}}
  \infty Grpd
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

For $\mathbf{H}$ a general [[(∞,1)-topos]] the above discussion goes through essentially verbatim. If $\mathbf{H}$ is itself [[cohesive (∞,1)-topos|cohesive]], then we end up with

$$
  \mathbf{H}
  \stackrel{\overset{\Omega}{\longrightarrow}}{\underset{dom}{\leftarrow}}
  T\mathbf{H}
  \stackrel{\overset{base}{\longrightarrow}}{\stackrel{\overset{0}{\leftarrow}}{\stackrel{\overset{base}{\longrightarrow}}{\underset{0}{\leftarrow}}}}
  \mathbf{H}
  \stackrel{}{\stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{coDisc}{\leftarrow}}}}}
  \infty Grpd
  \,.
$$

=--

+-- {: .num_prop #DifferentialOfCohesiveGlobalSections}
###### Proposition

For $\mathbf{H}$ a [[locally ∞-connected (∞,1)-topos]] (hence in particular for a [[cohesive (∞,1)-topos]]), there are canonical [[(∞,1)-functors]]

$$
  T \mathbf{H} \stackrel{\overset{T Disc}{\leftarrow}}{\underset{T \Gamma}{\longrightarrow}} T \infty Grpd
$$

and such that $T \Gamma$ covers the [[global section]] [[geometric morphism]] $\Gamma \;\colon\; \mathbf{H} \longrightarrow \infty Grpd$ in that it fits into a square  

$$
  \array{
    T \mathbf{H}
    &\stackrel{}{\stackrel{}{\stackrel{\overset{T\Gamma}{\longrightarrow}}{}}}&
    T \infty Grpd
    \\
    {}^{\mathllap{0}}\uparrow\downarrow^{base}
    && 
    {}^{\mathllap{0}}\uparrow\downarrow^{base}
    \\
    \mathbf{H} &\stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{}}}& \infty Grpd
  }
$$


=--

+-- {: .proof}
###### Proof 

By definition of [[stabilization]], $T \mathbf{H}$ is the [[(∞,1)-Grothendieck construction]] of 

$$
  X \mapsto 
  \underset{\leftarrow}{\lim}
  \left(
    \cdots \stackrel{\Omega}{\to} \mathbf{H}^{\ast/}_{/X} \stackrel{\Omega}{\to} \mathbf{H}^{\ast/}_{/X} \stackrel{\Omega}{\to} \cdots
  \right)
  \,.
$$

Since the [[loop space object]] [[(∞,1)-functor]] $\Omega$ is an [[(∞,1)-limit]] construction and since the [[right adjoint]] [[global section]] functor $\Gamma$ preserves all [[(∞,1)-limits]], there is a homotopy-[[commuting diagram]]

$$
  \array{
    \cdots &\stackrel{\Omega}{\to}& \mathbf{H}^{\ast/}_{/X} &\stackrel{\Omega}{\to}& \mathbf{H}^{\ast/}_{/X} &\stackrel{\Omega}{\to}& \cdots
    \\
    && \downarrow^{\mathrlap{\Gamma}} && \downarrow^{\mathrlap{\Gamma}}
    \\
    \cdots &\stackrel{\Omega}{\to}& \infty Grpd^{\ast/}_{/\Gamma(X)} &\stackrel{\Omega}{\to}& \infty Grpd^{\ast/}_{/\Gamma(X)} &\stackrel{\Omega}{\to}& \cdots
  }
$$

in [[(∞,1)Cat]]. This induces a natural morphism 

$$
  Stab(\mathbf{H}_{/X})
  \longrightarrow
  Stab(\infty Grpd_{/\Gamma(X)})
$$

and hence a morphism 

$$
  T \mathbf{H} 
  \simeq 
  \int_{X \in \mathbf{H}} Stab(\mathbf{H}_{/X}) \longrightarrow \int_{X \in \mathbf{H}} Stab(\infty Grpd_{\Gamma(X)})
  \,.
$$

The morphism in question is the postcomposition of this with pullback/restriction of the [[(∞,1)-Grothendieck construction]] along the [[reflective sub-(∞,1)-category|reflective inclusion]] (by assumption on $\mathbf{H}$) $Disc \;\colon\; \infty Grpd \longrightarrow \mathbf{H}$


$$
  T \mathbf{H} 
  \simeq
  \int_{X \in \mathbf{H}} Stab(\mathbf{H}_{/X})
  \longrightarrow 
  \int_{X \in \mathbf{H}} Stab(\infty Grpd_{/\Gamma(X)})
  \longrightarrow 
\int_{S \in \infty Grpd} Stab(\infty Grpd_{/S})
  \simeq
  T \infty Grpd
  \,,
$$

where we used that by reflectivity $\Gamma \circ Disc \simeq id$.

=--

+-- {: .num_remark}
###### Remark

When $T \mathbf{H}$ is an $\infty$-topos it should carry another structure $\otimes$ of a [[symmetric monoidal (∞,1)-category]], induced by fiberwise [[smash product]] of [[spectrum objects]].... 

=--


## References

The definition and study of the notion of _tangent $(\infty,1)$-categories_ is from 

* [[Jacob Lurie]], _[[Deformation Theory]]_
 {#Lurie}

and section 7.3 of 

* [[Jacob Lurie]], _[[Higher Algebra]]_
 {#LurieHigherAlgebra}

The [[(infinity,1)-topos]] structure on tangent $(\infty,1)$-categories
is discussed in 35.5 of

* [[André Joyal]], _Notes on Logoi_, 2008 ([pdf](http://www.math.uchicago.edu/~may/IMA/JOYAL/Joyal.pdf))
  {#Joyal08}

[[!redirects tangent (infinity,1)-categories]]
[[!redirects tangent (∞,1)-category]]
[[!redirects tangent (∞,1)-categories]]