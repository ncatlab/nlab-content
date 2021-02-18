
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
#### Integration theory
+--{: .hide}
[[!include integration theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea


Generally, for $E$ an [[E-∞ ring]] [[spectrum]], and $P \to X$ a [[sphere spectrum]]-bundle, an _$E$-orientation_ of $P$ is a trivialization of the [[associated bundle|associated]] $E$-bundle.

Specifically, for $P = Th(V)$ the [[Thom space]] of a [[vector bundle]] $V \to X$, an $E$-orientation of $V$ is an $E$-orientation of $P$.

More generally, for $A$ an $E$-algebra spectrum, an $E$-bundle is $A$-orientable if the associated $A$-bundle is trivializable. For more on this see [[(∞,1)-vector bundle]].

The existence of an $E$-orientation is necessary in order to have a notion of [[fiber integration]] in $E$-cohomology.


## Definition

### Concretely
 {#TraditionalDefinition}

#### Orientation of a vector bundle

+-- {: .num_defn #EOrientationOfAVectorBundle}
###### Definition

Let $E$  be a [[multiplicative cohomology theory]] and let $V \to X$ be a topological [[vector bundle]] of [[rank]] $n$. Then an **$E$-orientation** or **$E$-[[Thom class]]** on $V$ is an element of degree $n$ 

$$
  u \in \tilde E^n(Th(V))
$$ 

in the [[reduced cohomology|reduced]] $E$-[[cohomology ring]] of the [[Thom space]] of $V$, such that for every point $x \in X$ its [[pullback in cohomology|restriction]] $i_x^* u$ along 

$$
  i_x 
    \;\colon\; 
  S^n \simeq Th(\mathbb{R}^n) \overset{Th(j_x)}{\longrightarrow} Th(V)
$$ 

(for $\mathbb{R}^n \overset{fib_x}{\hookrightarrow} V$ the [[fiber]] of $V$ over $x$) is a _generator_, in that it is of the form

$$
  i^\ast u = \epsilon \cdot \gamma_n 
$$

for

* $\epsilon \in \tilde E^0(S^0) $ a [[unit]] in $E^\bullet$;

* $\gamma_n \in \tilde E^n(S^n)$ the image of the multiplicative unit
  under the [[suspension isomorphism]] $\tilde E^0(S^0) \stackrel{\simeq}{\to}\tilde E^n(S^n)$.   

=--

(e.g. [Kochman 96, def. 4.3.4](#Kochman96))


#### Orientation of a manifold

+-- {: .num_defn #EOrientationOfAManifold}
###### Definition

Let $E$  be a [[multiplicative cohomology theory]] and let $X$ be a [[manifold]], possibly [[manifold with boundary|with boundary]], of [[dimension]] $n$. An **$E$-orientation** of $X$ is a class in the $E$-[[generalized homology]]

$$
  \iota \in E_n(X,\partial X)
$$

with the property that for each point $x \in Int(X)$ in the [[interior]], it maps to a generator of $E_\bullet(\ast)$ under the map

$$
  E_\bullet(X,\partial X)
    \longrightarrow
  E_\bullet(X,\; X - \{x\})
    \simeq
  E_\bullet(D^n, S^{n-1})
    \simeq
  E_{\bullet-n}(\ast)
  \,,
$$

where the isomorphism is the excision isomorphism ([def.](generalized+homology#excision)) for the complement of a closed [[n-ball]] around $x$.

=--

(e.g.  [Kochman 96, p. 134](#Kochman96))

+-- {: .num_prop}
###### Proposition

$E$-orientations of manifolds (def. \ref{EOrientationOfAManifold}) are equivalent to $E$-orientations of their stable [[normal bundle]] (def. \ref{EOrientationOfAVectorBundle}).

=--

(e.g. [Rudyak 98, chapter V, theorem 2.4](#Rudyak98)) (also [Kochman 96, prop. 4.3.5](#Kochman96), but maybe that proof needs an extra argument)

#### Universal orientation of vector bundles
 {#UniversalOrientationOfVectorBundles}

+-- {: .num_remark}
###### Remark

Recall that a _[[(B,f)-structure]]_ $\mathcal{B}$ is a system of [[Serre fibrations]] $B_n \overset{f_n}{\longrightarrow} B O(n)$ over the [[classifying spaces]] for [[orthogonal structure]] equipped with maps  

$$
  j_n \;\colon\; B_n \longrightarrow B_{n+1}
$$ 

covering the canonical inclusions of classifying spaces. For instance for $G_n \to O(n)$ a compatible system of [[topological group]] [[homomorphisms]], then the $(B,f)$-structure given by the [[classifying spaces]] $B G_n$ (possibly suitably resolved for the maps $B G_n \to B O(n)$ to become Serre fibrations) defines _[[G-structure]]_. 

Given a $(B,f)$-structure, then there are the [[pullbacks]] $V^{\mathcal{B}}_n \coloneqq f_n^\ast (E O(n)\underset{O(n)}{\times}\mathbb{R}^n)$ of the [[universal vector bundles]] over $B O(n)$, which are the _universal vector bundles equipped with $(B,f)$-structure_

$$
  \array{
    V^{\mathcal{B}}_n &\longrightarrow& E O(n)\underset{O(n)}{\times} \mathbb{R}^n
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_n & \underset{f_n}{\longrightarrow} & B O(n)
  }
  \,.
$$

Finally recall that there are canonical morphisms ([prop.](Thom+spectrum#PullbackOfUniversalOnBundleUnderCoordinateRestriction))

$$
  \phi_n 
    \;\colon\; 
  \mathbb{R} \oplus V^{\mathcal{B}}_n 
    \longrightarrow 
  V^{\mathcal{B}}_{n+1}
$$

=--


+-- {: .num_defn #EOrientationOfABfStructure}
###### Definition

Let $E$  be a [[multiplicative cohomology theory]] and let $\mathcal{B}$ be a multiplicative [[(B,f)-structure]]. Then a **universal $E$-orientation for vector bundles with $\mathcal{B}$-structure** is an $E$-orientation, according to def. \ref{EOrientationOfAVectorBundle}, for each rank-$n$ universal vector bundle with $\mathcal{B}$-structure:

$$
  \xi_n 
    \in 
  \tilde E^n(Th(V_n^{\mathcal{B}}))
  \;\;\;\;
  \forall n \in \mathbb{N}
$$

such that these are compatible in that

1. for all $n \in \mathbb{N}$ then

   $$  
     \xi_n = \phi_n^\ast \xi_{n+1}
     \,,
   $$

   where 

   $$
     \xi_n 
      \in 
     \tilde E^n(Th(V_n)) 
       \simeq 
     \tilde E^{n+1}(\Sigma Th(V_n))
        \simeq 
     \tilde E^{n+1}(Th(\mathbb{R}\oplus V_n))   
   $$

   (with the first isomorphism is the [[suspension isomorphism]] of $E$ and the second exhibiting the [[homeomorphism]] of Thom spaces $Th(\mathbb{R} \oplus V)\simeq \Sigma Th(V)$ ([prop.](Thom+space#SuspensionOfThomSpaces))) and where 

   $$
     \phi_n^\ast
     \;\colon\;
      \tilde E^{n+1}(Th(V_{n+1}))
      \longrightarrow
     \tilde E^{n+1}(Th(\mathbb{R}\oplus V_n))
   $$

   is pullback along the canonical $\phi_n \colon \mathbb{R}\oplus V_n \to V_{n+1}$ ([prop.](Thom+spectrum#PullbackOfUniversalOnBundleUnderCoordinateRestriction)).

1. for all $n_1, n_2 \in \mathbb{N}$ then

   $$
     \xi_{n+1} \cdot \xi_{n+2} = \xi_{n_1 + n_2}
     \,.
   $$

=--

+-- {: .num_prop #UniversalEOrientationsAreEquivalentlyMorphismsOfRingSpectra}
###### Proposition

A universal $E$-orientation, in the sense of def. \ref{EOrientationOfABfStructure}, for vector bundles with [[(B,f)-structure]] $\mathcal{B}$, is equivalently (the homotopy class of) a homomorphism of [[homotopy-commutative ring spectra]]

$$
  \xi \;\colon\; M\mathcal{B} \longrightarrow E
$$

from the universal $\mathcal{B}$-[[Thom spectrum]] to a spectrum which, via the [[Brown representability theorem]], represents the given [[generalized (Eilenberg-Steenrod) cohomology theory]] $E$ (and which we denote by the same symbol).

=--

+-- {: .proof}
###### Proof

The [[Thom spectrum]] $M\mathcal{B}$ has a standard structure of a [[CW-spectrum]]. Let now $E$ denote a [[sequential spectrum|sequential]] [[Omega-spectrum]] representing the multiplicative cohomology theory of the same name. Since, in the standard [[model structure on topological sequential spectra]], [[CW-spectra]] are cofibrant ([prop.](Introduction+to+Stable+homotopy+theory+--+1#CellSpectraAreCofibrantInModelStructureOnTopologicalSequentialSpectra)) and Omega-spectra are fibrant ([thm.](Introduction+to+Stable+homotopy+theory+--+1#StableModelStructureOnSequentialSpectraIsModelCategory)) we may represent all morphisms in the [[stable homotopy category]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#TheStableHomotopyCategory)) by actual morphisms 

$$
  \xi
   \;\colon\;
  M \mathcal{B}
    \longrightarrow
  E
$$

of sequential spectra (due to [this lemma](Introduction+to+Stable+homotopy+theory+--+P#HomsOutOfCofibrantIntoFibrantComputeHomotopyCategory)).

Now by definition ([def.](Introduction+to+Stable+homotopy+theory+--+1#SequentialSpectra)) such a homomorphism is precissely a sequence of base-point preserving [[continuous functions]]

$$
  \xi_n 
    \;\colon\;
  (M\mathcal{B})_n
   =
  Th(V_n^{\mathcal{B}})
    \longrightarrow
  E_n
$$

for $n \in \mathbb{N}$, such that they are compatible with the structure maps $\sigma_n$ and equivalently with their $(S^1 \wedge(-)\dashv Maps(S^1,-)_\ast)$-[[adjuncts]] $\tilde \sigma_n$, in that these diagrams commute:

$$
  \array{
    S^1 \wedge Th(V^{\mathcal{B}}_n)
     &\overset{S^1 \wedge \xi_n}{\longrightarrow}&
    S^1 \wedge E_n
    \\
    {}^{\mathllap{\sigma^{M\mathcal{B}}_n}}\downarrow 
      && 
    \downarrow^{\mathrlap{\sigma^E_n}}
    \\
    Th(V^{\mathcal{B}}_{n+1})
      &\underset{\xi_{n+1}}{\longrightarrow}&
    E_{n+1}
  }
  \;\;\;\;\;\;\;\;\;
  \leftrightarrow
  \;\;\;\;\;\;\;\;\;
  \array{
     Th(V^{\mathcal{B}}_n)
       &\overset{\xi_n}{\longrightarrow}&
     E_n
     \\
     {}^{\mathllap{\tilde \sigma^{M\mathcal{B}}_n}}\downarrow 
       && 
     \downarrow^{\mathrlap{\tilde \sigma^E_n}}
     \\
     Maps(S^1,Th(V^{\mathcal{B}}_{n+1}))
       &\underset{Maps(S^1,\xi_{n+1})_\ast}{\longrightarrow}&
     Maps(S^1, E_{n+1})_{\ast}
  }
$$

for all $n \in \mathbb{N}$. 

First of all this means (via the identification given by the [[Brown representability theorem]], see [this prop.](Introduction+to+Stable+homotopy+theory+--+S#AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum)) that the components $\xi_n$ are equivalently representatives of elements in the [[cohomology groups]]

$$
  \xi_n \in \tilde E^n(Th(V^{\mathcal{B}}_n))
$$

(which we denote by the same symbol, for brevity).

Now by the definition of universal [[Thom spectra]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrum), [def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrumForBfStructure)), the structure map $\sigma_n^{M\mathcal{B}}$ is just the map $\phi_n \colon \mathbb{R}\oplus Th(V^{\mathcal{B}}_n)\to Th(V_{n+1}^{\mathcal{B}})$ from above.

Moreover, by the [[Brown representability theorem]], the [[adjunct]]   $\tilde \sigma_n^E \circ \xi_n$ (on the right) of $\sigma^E_n \circ S^1 \wedge \xi_n$ (on the left) is what represents (again by [this prop.](Introduction+to+Stable+homotopy+theory+--+S#AdditiveReducedCohomologyTheoryRepresentedByOmegaSpectrum)) the image of 

$$
  \xi_n \in E^n(Th(V^{\mathcal{B}}_n))
$$

under the [[suspension isomorphism]]. Hence the [[commutative square|commutativity]] of the above squares is equivalently the first compatibility condition from def. \ref{EOrientationOfABfStructure}: $\xi_n \simeq \phi_n^\ast \xi_{n+1}$ in $\tilde E^{n+1}(Th(\mathbb{R}\oplus V_n^{\mathcal{B}}))$ 

Next,  $\xi$ being a homomorphism of [[ring spectra]] means equivalently (we should be modelling $M\mathcal{B}$ and $E$ as [[structured spectra]] ([here.](Introduction+to+Stable+homotopy+theory+--+1#DiagramSpectra)) to be more precise on this point, but the conclusion is the same) that for all $n_1, n_2\in \mathbb{N}$ then

$$
  \array{
    Th(V_{n_1}^{\mathcal{B}}) \wedge Th(V_{n_2}^{\mathcal{B}})
      &\overset{}{\longrightarrow}&
    Th(V_{n_1 + n_2})
    \\
    {}^{\mathllap{\xi_{n_1} \wedge \xi_{n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\xi_{n_1 + n_2}}}
    \\
    E_{n_1} \wedge E_{n_2}
      &\underset{\cdot}{\longrightarrow}&
    E_{n_1 + n_2}
  }
  \,.
$$

This is equivalently the condition $\xi_{n_1} \cdot \xi_{n_2} \simeq \xi_{n_1  + n_2}$.

Finally, since $M\mathcal{B}$ is a [[ring spectrum]], there is an essentially unique multiplicative homomorphism from the [[sphere spectrum]]

$$
  \mathbb{S}
    \overset{e}{\longrightarrow}
  M\mathcal{B}
  \,.
$$

This is given by the component maps

$$
  e_n 
    \;\colon\;
  S^n 
    \simeq
  Th(\mathbb{R}^n)
    \longrightarrow
  Th(V_{n}^{\mathcal{B}})
$$

that are induced by including the fiber of $V_{n}^{\mathcal{B}}$. 

Accordingly the composite 

$$
  \mathbb{S}
    \overset{e}{\longrightarrow}
  M\mathcal{B}
    \overset{\xi}{\longrightarrow}
  E
$$

has as components the restrictions $i^\ast \xi_n$ appearing in def. \ref{EOrientationOfAVectorBundle}. At the same time, also $E$ is a ring spectrum, hence it also has an essentially unique multiplicative morphism $\mathbb{S} \to E$, which hence must agree with $i^\ast \xi$, up to homotopy. If we represent $E$ as a [[symmetric ring spectrum]], then the canonical such has the required property: $e_0$ is the identity element in degree 0 (being a unit of an ordinary ring, by definition) and hence $e_n$ is necessarily its image under the suspension isomorphism, due to compatibility with the structure maps and using the above analysis.

=--


### Abstractly

Let $E$ be a [[E-∞ ring]] [[spectrum]]. Write $\mathbb{S}$ for the [[sphere spectrum]].

For the following see also May,Sigurdsson: _[[Parametrized Homotopy Theory]]_ ([MO comment](http://mathoverflow.net/a/107837/381))

#### $GL_1(R)$-principal $\infty$-bundles

Write $R^\times$ or $GL_1(R)$ for the [[general linear group]] of the $E_\infty$-ring $R$: it is the subspace of the degree-0 space $\Omega^\infty R$ on those points that map to multiplicatively invertible elements in the ordinary ring $\pi_0(R)$.

Since $R$ is $E_\infty$, the space $GL_1(R)$ is itself an [[infinite loop space]]. Its one-fold [[delooping]] $B GL_1(R)$ is the [[classifying space]] for $GL_1(R)$-[[principal ∞-bundle]]s (in [[Top]]): for $X \in Top$ and $\zeta : X \to B GL_1(R)$ a map, its [[homotopy fiber]]


$$
  \array{
    GL_1(R) &\to& P &\to& *
    \\
    \downarrow && \downarrow && \downarrow
    \\
    * &\stackrel{x}{\to}& X
   &\stackrel{\zeta}{\to}&
   B GL_1(R)
  }
$$

is the $GL_1(R)$-principal $\infty$-bundle $P \to X$ classified by that map.


+-- {: .num_example}
###### Example

For $R = \mathbb{S}$ the [[sphere spectrum]], we have that $B GL_1(\mathbb{S})$ is the [[classifying space]] for spherical fibrations.

=--

+-- {: .num_example}
###### Example

There is a canonical morphism

$$
  B O \to B GL_1(\mathbb{S})
$$

from the classifying space of the [[orthogonal group]] to that of the [[infinity-group of units]] of the [[sphere spectrum]], called the _[[J-homomorphism]]_. Postcomposition with this sends real [[vector bundle]]s $V \to X$ to sphere bundles. This is what is modeled by the [[Thom space]] construction


$$
  J : V \mapsto S^V
$$

which sends each fiber to its [[one-point compactification]].

=--


#### $GL_1(R)$-associated $\infty$-bundles

For $P \to X$ a $GL_1(R)$-[[principal ∞-bundle]] there is canonically the corresponding [[associated ∞-bundle]] with fiber $R$. Precisely, in the [[stable (∞,1)-category]] $Stab(Top)$ of [[spectra]], regarded as the [[stabilization]] of the [[(∞,1)-topos]] [[Top]]


$$
  Stab(Top) \simeq Spectra
   \stackrel{\overset{\Sigma^\infty}{\leftarrow}}{\underset{\Omega^\infty}{\to}}
  Top
$$


the associated bundle is the [[smash product]] over $\Sigma^\infty GL_1(R)$

$$
  X^\zeta := \Sigma^\infty P \wedge_{\Sigma^\infty GL_1(R)} R
  \,.
$$

This is the generalized **[[Thom spectrum]]**. For $R = K O$ the real [[K-theory spectrum]] this is given by the ordinary [[Thom space]] construction on a [[vector bundle]] $V \to X$.

An $E$-orientation of a vector bundle $V \to X$ is a trivialization of the $E$-module bundle $E \wedge S^V$, where we fiberwise form the [[smash product]] of $E$ with the [[Thom space]] of $V$.

+-- {: .num_prop}
###### Proposition

For $f : R \to S$ a morphism of $E_\infty$-rings, and $\zeta : X \to B GL_1(R)$ the classifying map for an $R$-bundle, the corresponding associated $S$-bundle classified by the composite

$$
  X \stackrel{\zeta}{ \to } B GL_1(R) \stackrel{f}{\to} B GL_1(S)
$$

is given by the [[smash product]]

$$
  X^{f \circ \zeta} \simeq X^\zeta \wedge_R S
  \,.
$$

=--

This appears as ([Hopkins, bottom of p. 6](#Hopkins)).

#### $R$-Orientations

For $X \stackrel{\zeta}{\to} B GL_1(\mathbb{S})$ a sphere bundle, an **$R$-orientation** on $X^\zeta$ is a trivialization of the associated $R$-bundle $X^\zeta \wedge R$, hence a trivialization (null-homotopy) of the classifying morphism

$$
  X \stackrel{\zeta}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
  \,,
$$

where the second map comes from the unit of $E_\infty$-rings $\mathbb{S} \to R$ (the [[sphere spectrum]] is the [[initial object]] in $E_\infty$-rings).

Specifically, for $V : X \to B O$  a [[vector bundle]], an $E$-orientation on it is a trivialization of the $R$-bundle associated to the associated [[Thom space]] sphere bundle, hence a trivialization of the morphism

$$
  \array{
  B O &\stackrel{J}{\to}& B GL_1(\mathbb{S})
    &\stackrel{\iota}{\to}&
   B GL_1(R)
   \\
   {}^{\mathllap{V}}\uparrow & \nearrow_{\mathrlap{\zeta}}
   \\
   X
  }
  \,.
$$

This appears as ([Hopkins, p.7](#Hopkins)).

A natural $R$-orientation of _all_ vector bundles is therefore a trivialization of the morphism

$$
  B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
 \,.
$$

Similarly, an $R$-orientation of _all_ [[spinor bundle]]s is a trivialization of

$$
  B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

and an $R$-orientation of all [[string group]]-bundles a trivialization  of

$$
  B String \to B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

and so forth, through the  [[Whitehead tower]] of $B O$.

Now, the [[Thom spectrum]] [[MO]] is the [[spherical fibration]] over $B O$ [[associated infinity-bundle|associated]] to the $O$-[[universal principal bundle]]. In generalization of the way that a trivialization of an ordinary $G$-principal bundle $P$ is given by a $G$-equivariant map $P \to G$, one finds that trivializations of the morphism

$$
  B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

correspond to $E_\infty$-maps

$$
  M O \to R
$$

from the [[Thom spectrum]] to $R$. Similarly trivialization of 

$$
  B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

corresponds to morphisms 

$$
  M Spin \to R
$$

and trivializations of 

$$
  B String \to B Spin \to B O \stackrel{J}{\to} B GL_1(\mathbb{S})
    \stackrel{\iota}{\to}
   B GL_1(R)
$$

to morphisms

$$
  M String \to R
$$

and so forth.

This is the way orientations in generalized cohomology often appear in the literature.


+-- {: .num_example}
###### Example

The construction of the [[string orientation of tmf]], hence a morphism

$$
  M String \to tmf
$$

is discussed in ([Hopkins, last pages](#Hopkins)).

=--


## Properties

### Relation to top Chern class

\begin{prop}
  The [[top Chern class]] of a [[complex vector bundle]] $\mathcal{V}_X$ equals the [[pullback in cohomology|pullback]] of any [[Thom class]] 
$th \;\in\; H^{2n}\big( \mathcal{V}_X; \mathbb{Z} \big)$ on $\mathcal{V}_X$ along the [[zero-section]]:

$$
  \mathcal{V}_X
  \;
  \text{has complex rank}\;n
  \;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;   
  c_n
  \big(
    \mathcal{V}_X
  \big)
  \;\;\;  
    =
  \;\;\;
  (0_X)^\ast
  (th)
  \;\;
  \in
  \;
  H^{2n}
  \big(
    X ;
    \,
    \mathbb{Z}
  \big)
$$
\end{prop}

For [[ordinary cohomology]] this is [Bott-Tu 82, Prop. 12.4](top+Chern+class#BottTu82). For [[Whitehead-generalized cohomology]] see at _[[universal complex orientation on MU]]_.

### Relation to the Todd class 

+-- {: .num_prop #RationalToddClassIsChernCharacterOfThomClass} 
###### Proposition
**([[rational Todd class is Chern character of Thom class]])**

Let $V \to X$ be a [[complex vector bundle]] over a [[compact topological space]]. Then the [[Todd class]] $Td(V) \,\in\, H^{ev}(X; \mathbb{Q})$ of $V$ in [[rational cohomology]] equals the [[Chern character]] $ch$ of the [[Thom class]] $th(V) \,\in\, K\big( Th(V) \big)$ in the [[complex topological K-theory]] of the [[Thom space]] $Th(V)$, when both are compared via the [[Thom isomorphisms]] $\phi_E \;\colon\; E(X) \overset{\simeq}{\to} E\big( Th(V)\big)$:

$$
  \phi_{H\mathbb{Q}}  
  \big( 
    Td(V)
  \big) 
  \;=\;
  ch\big( th(V) \big)
  \,.
$$

More generally , for $x \in K(X)$ any class, we have

$$
  \phi_{H\mathbb{Q}}  
  \big(
    ch(x)
    \cup
    Td(V)
  \big) 
  \;=\;
  ch\big( \phi_{K}(x) \big)
  \,,
$$

which specializes to the previous statement for $x = 1$.

=--

([Karoubi 78, Chapter V, Theorem 4.4](rational+Todd+class+is+Chern+character+of+Thom+class#Karoubi78))


### Relation to trivializations

The relation (equivalence) between choices of [[Thom classes]] and trivializations of [[(∞,1)-line bundles]] is 
discussed e.g. in [Ando-Hopkins-Rezk 10, section 3.3](#AndoHopkinsRezk10)

### Relation to genera
 {#RelationToGenera}

Let $G$ be a [[topological group]] equipped with a [[homomorphism]] to the [[stable orthogonal group]], and write $B G \to B O$ for the corresponding map of [[classifying spaces]]. Write $J \colon B O \longrightarrow B GL_1(\mathbb{S})$ for the [[J-homomorphism]].

For $E$ an [[E-∞ ring]], there is a canonical homomorphism $B GL_1(\mathbb{S}) \to B GL_1(E)$ between the [[deloopings]] of the [[∞-groups of units]]. A trivialization of the total composite

$$
  B G \to B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to B GL_1(E)
$$

is a universal $E$-orientation of [[G-structures]]. Under [[(∞,1)-colimit]] in $E Mod$ this induces a homomorphism of $E$-[[∞-modules]]

$$
  \sigma \;\colon\; M G \to E
$$

from the universal $G$-[[Thom spectrum]] to $E$. 

If here $G \to GL_1(\mathbb{S})$ is the $\Omega^\infty$-component of a map of [[spectra]] then this $\sigma$ is a homomorphism of [[E-∞ rings]] and in this case there is a [[bijection]] between universal orientations and such $E_\infty$-ring homomorphisms ([Ando-Hopkins-Rezk 10, prop. 2.11](#AndoHopkinsRezk10)).

The latter, on passing to [[homotopy groups]], are [[genera]] on manifolds with [[G-structure]].

### Relation to cubical structures

For $E$ a [[multiplicative cohomology theory|multiplicative]] [[weakly periodic cohomology theory|weakly periodic]] [[complex orientable cohomology theory]] then $Spec E^0(B U\langle 6\rangle)$ is naturally equivalent to the space of [[cubical structure on a line bundle|cubical structures]] on the trivial line bundle over the [[formal group]] of $E$.

In particular, [[homotopy classes]] of maps of [[E-infinity ring]] spectra $MU\langle 6\rangle \to E$ from the [[Thom spectrum]] to $E$, and hence universal $MU\langle 6\rangle$-[[orientation in generalized cohomology|orientations]] (see there) of $E$ are in natural bijection with these cubical structures.

See at _[[cubical structure]]_ for more details and references.
This way for instance the [[string orientation of tmf]] has been constructed. See there for more.

 
## Examples

### Orientations related to genera and indices

[[!include genera and partition functions - table]]

### Complex orientation

An $E_\infty$ [[complex oriented cohomology theory]] $E$ is indeed equipped with a universal complex orientation given by an $E_\infty$-ring homomorphism $MU \to E$, see [here](complex+oriented+cohomology+theory#InTermsOfGenera).




## Related concepts

* [[differential Thom class]]

* [[differential orientation]], [[fiber integration in differential cohomology]]

* [[(infinity,1)-vector bundle]]

## References

Discussion in terms of [[Thom classes]]:

* [[Frank Adams]], part III, section 10 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Kochman96} [[Stanley Kochman]], section 4.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* {#Rudyak98} [[Yuli Rudyak]], _In Thom spectra, Orientability and Cobordism_, Springer 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))

* [[Jacob Lurie]], lecture 5 of _[[Chromatic Homotopy Theory]]_, 2010 ([pdf](http://www.math.harvard.edu/~lurie/252xnotes/Lecture5.pdf))

* [[eom]], _[Orientation](http://eom.springer.de/o/o070200.htm)_

* [[Manifold Atlas]], _[Orientation of manifolds in generalized cohomology theories](http://www.map.mpim-bonn.mpg.de/Orientation_of_manifolds_in_generalized_cohomology_theories)_


A comprehensive account of the general abstract perspective (with predecessors in [Ando-Hopkins-Rezk 10](#AndoHopkinsRezk10)) is in 

* {#ABGHR} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
 

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], section 6 of _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 
Lecture notes on this include

* {#Hopkins} [[Mike Hopkins]] (notes by [[André Henriques]]), _The String orientation of tmf_  ([arXiv:0805.0743](http://arxiv.org/abs/0805.0743))
 

which are motivated towards constructing the [[string orientation of tmf]], based on 

* {#AndoHopkinsRezk10} [[Matthew Ando]], [[Mike Hopkins]], [[Charles Rezk]], _Multiplicative orientations of KO-theory and the spectrum of topological modular forms_, 2010 ([pdf](http://www.math.uiuc.edu/~mando/papers/koandtmf.pdf))

For an informal exposition in terms of spectra, see

* Mattia Coloma, [[Domenico Fiorenza]], Eugenio Landi, _An exposition of the topological half of the Grothendieck-Hirzebruch-Riemann-Roch theorem in the fancy language of spectra_, ([arXiv:1911.12035](https://arxiv.org/abs/1911.12035))




[[!redirects Thom class]]
[[!redirects Thom classes]]


[[!redirects orientations in generalized cohomology]]

[[!redirects E-orientation]]
[[!redirects E-orientations]]
