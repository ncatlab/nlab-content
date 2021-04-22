
> This entry is about Thom's theorem in [[cobordism theory]]. For the isomorphism in [[cohomology]] induced by [[Thom classes]] see at _[[Thom isomorphism]]_.

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cobordism theory
+--{: .hide}
[[!include cobordism theory -- contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

What is called _Thom's theorem_ or the _Pontrjagin-Thom isomorphism_ (due to [Thom 54](#Thom54), [Pontrjagin 55](#Pontrjagin55)) states that for a given universal [[tangential structure]] the [[homotopy group of a spectrum|stable homotopy groups]] of the universal [[Thom spectrum]] $M G$, with its canonical [[ring spectrum]] structure, form the [[cobordism ring]]

$$
  \Omega^G_\bullet \simeq \pi_\bullet(M G)
$$

of manifolds with that [[tangential structure]]; and that this [[isomorphism]] is exhibited by the [[Pontryagin-Thom construction]] (see [there](Pontrjagin-Thom+collapse+map#ForEmbeddingsIntoAnNSphere)).

More generally, for $X$ a [[topological space]], the group of $G$-bordism classes of $G$-manifolds in $X$ is isomorphic to the [[generalized homology]] of $X$ with [[coefficients]] in $M G$:

$$
  \Omega^G_\bullet(X)
   \simeq
  \pi_\bullet( M G \wedge X_+)
   \simeq
  M G_\bullet(X)
$$

## Ingredients
 {#Ingredients}

### Tangential structure on the Stable normal bundle

+-- {: .num_defn #ClassifyingMapOfNormalBundle}
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$ and equipped with an [[embedding]] 

$$
  i \;\colon\; X \hookrightarrow \mathbb{R}^k
$$

for some $k \in \mathbb{N}$, then the **classifying map of its normal bundle** is the function

$$
  g_i \;\colon\; X \to Gr_{k-n}(\mathbb{R}^k) \hookrightarrow B O(k-n)
$$ 
  
which sends $x \in X$ to the normal of the [[tangent space]] 

$$
  N_x X = (T_x X)^{\perp} \hookrightarrow \mathbb{R}^k
$$

regarded as a point in $G_{k-n}(\mathbb{R}^k)$.

The [[normal bundle]] of $i$ itself is the subbundle of the [[tangent bundle]]

$$
  T \mathbb{R}^k \simeq \mathbb{R}^k \times \mathbb{R}^k
$$

consisting of those vectors which are [[orthogonal]] to the [[tangent vectors]] of $X$:

$$
  N_i 
    \coloneqq 
  \left\{
    x\in X, v \in T_{i(x)}\mathbb{R}^k
    \;\vert\;
    v \,\perp\, i_\ast T_x X \subset T_{i(x)}\mathbb{R}^k
  \right\}
  \,.
$$

=--

+-- {: .num_defn #BfStructure}
###### Definition

A **[[tangential structure|(B,f)-structure]]** is 

1. for each $n\in \mathbb{N}$ a [[pointed topological space|pointed]] [[CW-complex]] $B_n \in Top_{CW}^{\ast/}$

1. equipped with a pointed [[Serre fibration]] 

   $$
     \array{
       B_n
       \\
       \downarrow^{\mathrlap{f_n}}
       \\
       B O(n)
     }
   $$

   to the [[classifying space]] $B O(n)$ ([def.](classifying+space#EOn));

1. for all $n_1 \leq n_2$ a pointed continuous function

   $g_{n_1, n_2} \;\colon\; B_{n_1} \longrightarrow B_{n_2}$

   which is the identity for $n_1 = n_2$;

such that for all $n_1 \leq n_2 \in \mathbb{N}$ these [[commuting square|squares commute]]

$$
  \array{
    B_{n_1} &\overset{g_{n_1,n_2}}{\longrightarrow}& B_{n_2}
    \\
    {}^{\mathllap{f_{n_1}}}\downarrow && \downarrow^{\mathrlap{f_{n_2}}}
    \\
    B O(n_1) &\longrightarrow& B O(n_2)
  }
  \,,
$$

where the bottom map is the canonical one from def. \ref{InclusionOfBOnIntoBOnPlusOne}.

The $(B,f)$-structure is **multiplicative** if it is moreover equipped with a system of maps $\mu_{n_1,n_2} \colon B_{n_1}\times B_{n_2} \to B_{n_1 + n_2}$ which cover the canonical multiplication maps ([def.](classifying+space#WhitneySumMapOnClassifyingSpaces))

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{\mu_{n_1, n_2}}{\longrightarrow}&
    B_{n_1 + n_2}
    \\
    {}^{\mathllap{f_{n_1} \times f_{n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{f_{n_1 + n_2}}}
    \\
    B O(n_1) \times B O(n_2)
     &\longrightarrow&
    B O(n_1 + n_2)
  }
$$
 
and which satisfy the evident [[associativity]] and [[unitality]], for $B_0 = \ast$ the unit, and, finally, which commute with the maps $g$ in that all $n_1,n_2, n_3 \in \mathbb{N}$ these squares commute:


$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{id \times g_{n_2,n_2+n_3}}{\longrightarrow}&
    B_{n_1} \times B_{n_2 + n_3}
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1,n_2 + n_3}}}
    \\
    B_{n_1 + n_2}
      &\underset{g_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
$$

and

$$
  \array{
    B_{n_1} \times B_{n_2}
      &\overset{g_{n_1,n_1+n_3} \times id}{\longrightarrow}&
    B_{n_1+n_3} \times B_{n_2 }
    \\
    {}^{\mathllap{\mu_{n_1, n_2}}}\downarrow 
      && 
    \downarrow^{\mathrlap{\mu_{n_1 + n_3 , n_2}}}
    \\
    B_{n_1 + n_2}
      &\underset{g_{n_1+n_2, n_1 + n_2 + n_3}}{\longrightarrow}&
    B_{n_1 + n_2 + n_3}
  }
  \,.
$$


Similarly, an **$S^2$-$(B,f)$-structure** is a compatible system

$$
  f_{2n} \colon B_{2n} \longrightarrow B O(2n)
$$

indexed only on the even natural numbers.

Generally, an **$S^k$-$(B,f)$-structure** for $k \in \mathbb{N}$, $k \geq 1$ is a compatible system

$$
  f_{k n} \colon B_{k n} \longrightarrow B O(k n)
$$

for all $n \in \mathbb{N}$, hence for all $k n \in k \mathbb{N}$.

We write $V^\mathcal{B}_n$ for the [[universal vector bundle]] pulled back to the corresponding space of the $(B,f)$-structure and with

$$
  \array{
    V^{\mathcal{B}}
      &\overset{}{\longrightarrow}&
    E O(n) \underset{O(n)}{\times} \mathbb{R}^n
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_n &\underset{f_n}{\longrightarrow}& B O(n)
  }
$$

and we write $e_{n_1,n_2}$ for the maps of total space of vector bundles over the $g_{n_1,n_2}$:

$$
  \array{
    V^{\mathcal{B}}_{n_1}
     &\overset{e_{n_1,n_2}}{\longrightarrow}&
    V^{\mathcal{B}}_{n_2}
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_{n_1} &\underset{g_{n_1,n_2}}{\longrightarrow}& B_{n_2}
  }
  \,.
$$

=--

+-- {: .num_example #ExamplesOfBfStructures}
###### Example

Examples of $(B,f)$-structures (def. \ref{BfStructure}) include the following:

1. $B_n = B O(n)$ and $f_n = id$ is **orthogonal structure** (or "no structure");

1. $B_n = E O(n)$ and $f_n$ the [[universal principal bundle]]-projection is **[[framing]]-structure**;

1. $B_n = B SO(n) = E O(n)/SO(n)$ the classifying space of the [[special orthogonal group]] and $f_n$ the canonical projection is **[[orientation]] structure**;

1. $B_n = B Spin(n) = E O(n)/Spin(n)$ the classifying space of the [[spin group]] and $f_n$ the canonical projection is **[[spin structure]]**.

Examples of $S^2$-$(B,f)$-structures (def. \ref{BfStructure}) include

1. $B_{2n} = B U(n) = E O(2n)/U(n)$ the classifying space of the [[unitary group]], and $f_{2n}$ the canonical projection is **[[almost complex structure]]** (or rather: **[[almost Hermitian structure]]**).

1. $B_{2n} = B Sp(2n) = E O(2n)/Sp(2n)$ the classifying space of the [[symplectic group]], and $f_{2n}$ the canonical projection is **[[almost symplectic structure]]**.

Examples of $S^4$-$(B,f)$-structures (def. \ref{BfStructure}) include

1. $B_{4n} = B U_{\mathbb{H}}(n) = E O(4n)/U_{\mathbb{H}}(n)$ the classifying space of the [[quaternionic unitary group]], and $f_{4n}$ the canonical projection is **[[almost quaternionic structure]]**.


=--


+-- {: .num_defn #ManifoldWithBfStructure}
###### Definition

Given a [[smooth manifold]] $X$ of [[dimension]] $n$, and given a $(B,f)$-structure as in def. \ref{BfStructure}, then a **$(B,f)$-structure on the stable normal bundle of the manifold** is an [[equivalence class]] of the following structure:

1. an [[embedding]] $i_X \; \colon \; X \hookrightarrow \mathbb{R}^k$ for some $k \in \mathbb{N}$;

1. a [[homotopy class]] of a  [[lift]] $\hat g$ of the classifying map $g$ of the normal bundle (def. \ref{ClassifyingMapOfNormalBundle})

   $$
     \array{
       && B_{k-n}
       \\
       &{}^{\mathllap{\hat g}}\nearrow& \downarrow^{\mathrlap{f_{k-n}}}
       \\
       X &\overset{g}{\longrightarrow}& B O(k-n)
     }
     \,.
   $$

The equivalence relation on such structures is to be that generated by the relation $((i_{X})_1, \hat g_1) \sim ((i_{X})_2, \hat g_2)$ if 

1. $k_2 \geq k_1$

1. the second inclusion factors through the first as 

   $$
     (i_X)_2 
       \;\colon\; 
     X 
       \overset{(i_X)_1}{\hookrightarrow}
     \mathbb{R}^{k_1} 
       \hookrightarrow
     \mathbb{R}^{k_2}
   $$

1. the lift of the classifying map factors accordingly (as homotopy classes)

   $$
     \hat g_2
       \;\colon\;
     X 
       \overset{\hat g_1}{\longrightarrow}
     B_{k_1-n}
       \overset{g_{k_1-n,k_2-n}}{\longrightarrow}
     B_{k_2-n}
     \,.
   $$

=--



###  Bordism

Throughout, let $\mathcal{B}$ be a multiplicative [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)).

+-- {: .num_defn #NegativeOfManifoldWithBfStructure}
###### Definition

Write $I \coloneqq [0,1]$ for the standard interval, regarded as a [[smooth manifold]] [[manifold with boundary|with boundary]]. For $c \in \mathbb{R}_+$ Consider its embedding

$$
  e \;\colon\; I \hookrightarrow \mathbb{R}\oplus \mathbb{R}_{\geq 0}
$$

as the arc

$$
  e \;\colon\; t \mapsto \cos(\pi t) \cdot e_1 + \sin(\pi t) \cdot e_2
  \,,
$$

where $(e_1, e_2)$ denotes the canonical [[linear basis]] of $\mathbb{R}^2$, and equipped with the structure of a manifold with normal [[framing]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#ExamplesOfBfStructures)) by equipping it with the canonical framing

$$
  fr \;\colon\; t \mapsto \cos(\pi t) \cdot e_1 + \sin(\pi t) \cdot e_2
$$

of its [[normal bundle]]. 

Let now $\mathcal{B}$ be a [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)).  Then for $X \overset{i}{\hookrightarrow}\mathbb{R}^k$ any embedded manifold with $\mathcal{B}$-structure $\hat g \colon X \to B_{k-n}$ on its [[normal bundle]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)), define its **negative** or **orientation reversal**  $-(X,i,\hat g)$ of $(X,i, \hat g)$ to be the restriction of the structured manifold

$$
  (X \times I \overset{(i,e)}{\hookrightarrow} \mathbb{R}^{k+2}, \hat g \times fr)
$$

to $t = 1$. 

=--


+-- {: .num_defn #BordismRelation}
###### Definition

Two closed manifolds of [[dimension]] $n$ equipped with normal $\mathcal{B}$-structure $(X_1, i_1, \hat g_1)$ and $(X_2,i_2,\hat g_2)$ ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)) are called **bordant** if there exists a [[manifold with boundary]] $W$ of dimension $n+1$ equipped with $\mathcal{B}$-strcuture $(W,i_W, \hat g_W)$ if its [[boundary]] with $\mathcal{B}$-structure restricted to that boundary is the [[disjoint union]] of $X_1$ with the negative of $X_2$, according to def. \ref{NegativeOfManifoldWithBfStructure}

$$
  \partial(W,i_W,\hat g_W)
    \simeq
  (X_1, i_1, \hat g_1)
    \sqcup
  -(X_2, i_2, \hat g_2)
  \,.
$$

=--

+-- {: .num_prop #BordismIsAnEquivalenceRelation}
###### Proposition

The [[relation]] of $\mathcal{B}$-[[bordism]] (def. \ref{BordismRelation}) is an [[equivalence relation]].

Write $\Omega^\mathcal{B}_{\bullet}$ for the $\mathbb{N}$-graded set of $\mathcal{B}$-bordism classes of $\mathcal{B}$-manifolds.

=--

+-- {: .num_prop #BordismGroupAndBordismRing}
###### Proposition

Under [[disjoint union]] of manifolds, then the set of $\mathcal{B}$-bordism equivalence classes of def. \ref{BordismIsAnEquivalenceRelation} becomes an $\mathbb{Z}$-graded [[abelian group]]

$$
  \Omega^{\mathcal{B}}_\bullet \in Ab^{\mathbb{Z}}
$$

(that happens to be concentrated in non-negative degrees). This is called the **$\mathcal{B}$-bordism group**.

Moreover, if the [[(B,f)-structure]] $\mathcal{B}$ is multiplicative ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)), then [[Cartesian product]] of manifolds followed by the multiplicative composition operation of $\mathcal{B}$-structures makes the $\mathcal{B}$-bordism ring into a [[commutative ring]], called the **$\mathcal{B}$-bordism ring**.

$$
  \Omega^{\mathcal{B}}_\bullet \in CRing^{\mathbb{Z}}
  \,.
$$

=--

e.g. ([Kochmann 96, prop. 1.5.3](#Kochmann96))


### Thom spaces

+-- {: .num_defn #ThomSpace}
###### Definition

Let $X$ be a [[topological space]] and let $V \to X$ be a [[vector bundle]] over $X$ of [[rank]] $n$, which is [[associated bundle|associated]] to an [[orthogonal group|O(n)]]-[[principal bundle]]. Equivalently this means that $V \to X$ is the [[pullback]] of the [[universal vector bundle]] $E_n \to B O(n)$ (def. \ref{EOn}) over the [[classifying space]]. Since $O(n)$ preserves the [[metric]] on $\mathbb{R}^n$, by definition, such $V$ inherits the structure of a [[metric space]]-[[fiber bundle]]. With respect to this structure:

1. the **unit disk bundle** $D(V) \to X$ is the subbundle of elements of [[norm]] $\leq 1$;

1. the **[[unit sphere]] bundle** $S(V)\to X$ is the subbundle of elements of norm $= 1$;

   $S(V) \overset{i_V}{\hookrightarrow} D(V) \hookrightarrow V$;

1. the **[[Thom space]]** $Th(V)$ is the [[cofiber]] (formed in [[Top]] ([prop.](Top#DescriptionOfLimitsAndColimitsInTop))) of $i_V$ 

   $$
     Th(V) \coloneqq cofib(i_V)
   $$

   canonically regarded as a [[pointed topological space]].

$$
  \array{
    S(V) &\overset{i_V}{\longrightarrow}& D(V)
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V)
  }
  \,.
$$

If $V \to X$ is a general real vector bundle, then there exists an isomorphism to an $O(n)$-[[associated bundle]] and the Thom space of $V$ is, up to based [[homeomorphism]], that of this orthogonal bundle.

=--


+-- {: .num_remark #ThomSpaceForRankZeroBundle}
###### Remark

If the [[rank]] of $V$ is positive, then $S(V)$ is non-empty and then the Thom space (def. \ref{ThomSpace}) is the [[quotient topological space]]

$$
  Th(V) \simeq D(V)/S(V)
  \,.
$$

However, in the degenerate case that the [[rank]] of $V$ vanishes, hence the case that $V = X\times \mathbb{R}^0 \simeq X$, then $D(V) \simeq V \simeq X$, but $S(V) = \emptyset$. Hence now the [[pushout]] defining the cofiber is

$$
  \array{
    \emptyset &\overset{i_V}{\longrightarrow}& X
    \\
    \downarrow &(po)& \downarrow
    \\
    \ast &\longrightarrow& Th(V) \simeq X_*
  }
  \,,
$$

which exhibits $Th(V)$ as the [[coproduct]] of $X$ with the point, hence as $X$ with a basepoint freely adjoined.

$$
  Th(X \times \mathbb{R}^0) = Th(X) \simeq X_+
  \,.
$$

=--

+-- {: .num_prop #ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks}
###### Proposition

Let $V_1,V_2 \to X$ be two real [[vector bundles]]. Then the Thom space (def. \ref{ThomSpace}) of the [[direct sum of vector bundles]] $V_1 \oplus V_2 \to X$ is expressed in terms of the Thom space of the [[pullbacks]] $V_2|_{D(V_1)}$ and $V_2|_{S(V_1)}$ of $V_2$ to the disk/sphere bundle of $V_1$ as

$$
  Th(V_1 \oplus V_2)
  \simeq
  Th(V_2|_{D(V_1)})/Th(V_2|_{S(V_1)})
  \,.
$$

=--

+-- {: .proof}
###### Proof

Notice that 

1. $D(V_1 \oplus V_2) \simeq D(V_2|_{Int D(V_1)}) \cup S(V_1)$;

1. $S(V_1 \oplus V_2) \simeq S(V_2|_{Int D(V_1)}) \cup Int D(V_2|_{S(V_1)})$.

(Since a point at radius $r$ in $V_1 \oplus V_2$ is a point of radius $r_1 \leq r$ in $V_2$ and a point of radius $\sqrt{r^2 - r_1^2}$ in $V_1$.)

=--

+-- {: .num_prop #SuspensionOfThomSpaces}
###### Proposition

For $V$ a [[vector bundle]] then the Thom space (def. \ref{ThomSpace}) of $\mathbb{R}^n \oplus V$, the [[direct sum of vector bundles]] with the trivial rank $n$ vector bundle, is [[homeomorphism|homeomorphic]] to the [[smash product]] of the Thom space of $V$ with the $n$-[[sphere]] (the $n$-fold [[reduced suspension]]).


$$
  Th(\mathbb{R}^n \oplus V) \simeq S^n \wedge Th(V) = \Sigma^n Th(V)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Apply prop. \ref{ThomSpaceOfDirectSumAsQuotientOfThomSpacesOfPullbacks} with $V_1 = \mathbb{R}^n$ and $V_2 = V$. Since $V_1$ is a trivial bundle, then

$$
  V_2|_{D(V_1)} \simeq V_2\times D^n
$$

(as a bundle over $X\times D^n$) and similarly

$$
  V_2|_{S(V_1)} \simeq V_2\times S^n
  \,.
$$


=--


+-- {: .num_example}
###### Example

By prop. \ref{SuspensionOfThomSpaces} and remark \ref{ThomSpaceForRankZeroBundle}  the Thom space (def. \ref{ThomSpace}) of a trivial vector bundle of rank $n$ is the $n$-fold [[suspension]] of the base space 

$$
  \begin{aligned}
    Th(X \times \mathbb{R}^n) 
    & \simeq S^n \wedge Th(X\times \mathbb{R}^0) 
    \\
    & \simeq S^n \wedge (X_+)
  \end{aligned}
  \,.
$$

Therefore a general Thom space may be thought of as a "twisted suspension", with twist encoded by a vector bundle (or rather by its underlying [[spherical fibration]]). See at _[Thom spectrum -- For infinity-module bundles](Thom+spectrum#ForInfinityModuleBundles)_ for more on this.

=--

+-- {: .num_prop #ThomSpaceOfExternalProductOfVectorBundles}
###### Proposition

For $V_1 \to X_1$ and $V_2 \to X_2$ to vector bundles, let $V_1 \boxtimes V_2 \to X_1 \times X_2$ be the [[direct sum of vector bundles]] of their [[pullbacks]] to $X_1 \times X_2$. The corresponding Thom space (def. \ref{ThomSpace}) is the [[smash product]] of the individual Thom spaces:

$$
  Th(V_1 \boxtimes V_2)
  \simeq
  Th(V_1) \wedge Th(V_2)
  \,.
$$

=--


### Universal Thom spectra $M G$

+-- {: .num_prop #PullbackOfUniversalOnBundleUnderCoordinateRestriction}
###### Proposition

For each $n \in \mathbb{N}$ the [[pullback]] of the [[rank]]-$(n+1)$ [[universal vector bundle]] to the [[classifying space]] of rank $n$ vector bundles is the [[direct sum of vector bundles]] of the rank $n$ universal vector bundle with the trivial rank-1 bundle: there is a [[pullback]] [[diagram]] of [[topological spaces]] of the form

$$
  \array{
    \mathbb{R}\oplus (E O(n)\underset{O(n)}{\times} \mathbb{R}^n)
    &\longrightarrow&
    E O(n+1) \underset{O(n+1)}{\times} \mathbb{R}^{n+1}
    \\
    \downarrow &(pb)& \downarrow
    \\
    B O(n) &\longrightarrow& B O(n+1)
  }
  \,,
$$

where the bottom morphism is the canonical one ([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne)).

=--

(e.g. [Kochmann 96, p. 25](#Kochmann96))

+-- {: .proof}
###### Proof

For each $k \in \mathbb{N}$, $k \geq n$ there is such a pullback of the canonical vector bundles over [[Grassmannians]]

$$
  \array{
    \left\{
      {V_{n}\subset \mathbb{R}^k, }
      \atop
      {v \in V_n, v_{n+1} \in \mathbb{R}}
    \right\}
    &\longrightarrow&
    \left\{
      {V_{n+1} \subset \mathbb{R}^{k+1}},
      \atop
      v \in V_{n+1}
    \right\}
    \\
    \downarrow && \downarrow
    \\
    Gr_n(\mathbb{R}^k)
    &\longrightarrow&
    Gr_{n+1}(\mathbb{R}^{k+1})
  }
$$

where the bottom morphism is the canonical inclusion ([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne)). 

Now we claim that taking the [[colimit]] in each of the four corners of this system of pullback diagrams yields again a pullback diagram, and this proves the claim. 

To see this, remember that we work in the category $Top_{cg}$ of [[compactly generated topological spaces]] ([def.](Introduction+to+Stable+homotopy+theory+--+P#kTop)). By their nature, we may test the [[universal property]] of a would-be [[pullback]] space already by mapping [[compact topological spaces]] into it. Now observe that all the inclusion maps in the four corners of this system of diagrams are [[relative cell complex]] inclusions, by prop. \ref{CWComplexStructure}. Together this implies (via [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)) that we may test the universal property of the colimiting square at finite stages. And so this implies the claim by the above fact that at each finite stage there is a pullback diagram.


=--


+-- {: .num_defn #UniversalThomSpectrum}
###### Definition

The **universal real [[Thom spectrum]]** $M O$ is the [[spectrum]], which is represented by the [[sequential prespectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#SequentialSpectra)) whose $n$th component space is the [[Thom space]] (def. \ref{ThomSpace})

$$
  (M O)_n \coloneqq Th(E O(n)\underset{O(n)}{\times}\mathbb{R}^n)
$$ 

of the rank-$n$ [[universal vector bundle]], and whose structure maps are the image under the [[Thom space]] functor $Th(-)$ of the top morphisms in prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction}, via the homeomorphisms of prop. \ref{SuspensionOfThomSpaces}:

$$
  \sigma_n
   \;\colon\;
  \Sigma (M O)_n
    \simeq 
  Th(\mathbb{R}\oplus (E O(n)\underset{O(n)}{\times} \mathbb{R}^n))
    \stackrel{}{\longrightarrow} 
  Th(E O(n+1) \underset{O(n+1)}{\times} \mathbb{R}^{n+1}) 
    = 
  (M O)_{n+1}
  \,.
$$

=--



More generally, there are universal Thom spectra associated with any other tangent structure ("[[(B,f)-structure]]"), notably for the orthogonal group replaced by the [[special orthogonal groups]] $SO(n)$, or the [[spin groups]] $Spin(n)$, or the [[string 2-group]] $String(n)$, or the [[fivebrane 6-group]] $Fivebrane(n)$,..., or any level in the [[Whitehead tower]] of $O(n)$. To any of these groups there corresponds a Thom spectrum (denoted, respectively, $M SO$, [[MSpin]], $M String$, $M Fivebrane$, etc.), which is in turn related to oriented cobordism, spin cobordism, string cobordism, et cetera.:


+-- {: .num_defn #VectorBundleAssociatedWithBfStructure}
###### Definition

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}),  write $V^\mathcal{B}_n$ for the [[pullback]] of the [[universal vector bundle]] (def. \ref{EOn}) to the corresponding space of the $(B,f)$-structure and with

$$
  \array{
    V^{\mathcal{B}}
      &\overset{}{\longrightarrow}&
    V O(n) \underset{O(n)}{\times} \mathbb{R}^n
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_n &\underset{f_n}{\longrightarrow}& B O(n)
  }
$$

and we write $e_{n_1,n_2}$ for the maps of total space of vector bundles over the $g_{n_1,n_2}$:

$$
  \array{
    V^{\mathcal{B}}_{n_1}
     &\overset{e_{n_1,n_2}}{\longrightarrow}&
    V^{\mathcal{B}}_{n_2}
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_{n_1} &\underset{g_{n_1,n_2}}{\longrightarrow}& B_{n_2}
  }
  \,.
$$


=--

Observe that the analog of prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction} still holds:

+-- {: .num_prop #PullbackOfUniversalBfBundleUnderCoordinateRestriction}
###### Proposiiton

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}), then the pullback of its rank-$(n+1)$ vector bundle $V^{\mathcal{B}}_{n+1}$ (def. \ref{VectorBundleAssociatedWithBfStructure}) along the map $g_{n,n+1} \colon B_n \to B_{n+1}$ is the [[direct sum of vector bundles]] of the rank-$n$ bundle $V^{\mathcal{B}}_n$ with the trivial rank-1-bundle: there is a pullback square

$$
  \array{
    \mathbb{R} \oplus V^{\mathcal{B}}_n 
      &\overset{e_{n,n+1}}{\longrightarrow}&
    V^{\mathcal{B}}_{n+1}
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_n &\underset{g_{n,n+1}}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

Unwinding the definitions, the pullback in question is

$$
  \begin{aligned}
    (g_{n,n+1})^\ast V^{\mathcal{B}}_{n+1}
      & =
    (g_{n,n+1})^\ast f_{n+1}^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
    \\
    & \simeq
    (g_{n,n+1} \circ f_{n+1})^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
    \\
    & \simeq
    ( f_n \circ i_n )^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
    \\
    & \simeq
    f_n^\ast i_n^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
    \\
    & \simeq
    f_n^\ast (\mathbb{R} \oplus (E O(n)\underset{O(n)}{\times} \mathbb{R}^{n}))
    \\
    &\simeq \mathbb{R} \oplus V^{\mathcal{B}_n}
    \,,
  \end{aligned}
$$

where the second but last step is due to prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction}.

=--

+-- {: .num_defn #UniversalThomSpectrumForBfStructure}
###### Definition

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}), its **universal Thom spectrum** $M \mathcal{B}$ is, as a [[sequential prespectrum]], given by component spaces being the [[Thom spaces]] (def. \ref{ThomSpace}) of the $\mathcal{B}$-associated vector bundles of def. \ref{VectorBundleAssociatedWithBfStructure}

$$
  (M \mathcal{B})_n
    \coloneqq
  Th(V^{\mathcal{B}}_n)
$$

and with structure maps given via prop. \ref{SuspensionOfThomSpaces} by the top maps in prop. \ref{PullbackOfUniversalBfBundleUnderCoordinateRestriction}:

$$
  \sigma_n
    \;\colon\;
  \Sigma (M \mathcal{B})_n
    =
  \Sigma Th(V^{\mathcal{E}}_n)
    \simeq
  Th(\mathbb{R}\oplus V^{\mathcal{E}}_n)
    \overset{Th(e_{n,n+1})}{\longrightarrow}
  Th(V^{\mathcal{E}}_{n+1})
  =
  (M \mathcal{B})_{n+1}
  \,.
$$

Similarly for an $S^k-(B,f)$-structure indexed on every $k$th natural number (such as [[almost complex structure]], [[almost quaternionic structure]], example \ref{ExamplesOfBfStructures}), there is the corresponding Thom spectrum as a sequential $S^k$ spectrum ([def.](Introduction+to+Stable+homotopy+theory+--+1#SequentialTSpectra)).

If $B_n = B G_n$ for some natural system of groups $G_n \to O(n)$, then one usually writes $M G$ for $M \mathcal{B}$. For instance $M SO$, [[MSpin]], [[MU]], [[MSp]] etc.

If the $(B,f)$-structure is multiplicative (def. \ref{BfStructure}), then the Thom spectrum $M \mathcal{B}$ canonical becomes a [[ring spectrum]]: the multiplication maps $B_{n_1} \times B_{n_2}\to B_{n_1 + n_2}$ are covered by maps of vector bundles

$$
  V^{\mathcal{B}}_{n_1} \boxtimes V^{\mathcal{B}}_{n_2}
  \longrightarrow
  V^{\mathcal{B}}_{n_1 + n_2}
$$

and under forming [[Thom spaces]] this yields ([prop.](Thom+space#ThomSpaceOfExternalProductOfVectorBundles)) maps

$$
  (M \mathcal{B})_{n_1}
    \wedge
  (M \mathcal{B})_{n_2}
    \longrightarrow
  (M \mathcal{B})_{n_1 + n_2}
$$

which are [[associativity|associative]] by the associativity condition in a multiplicative $(B,f)$-structure. The unit is 


$$
  (M \mathcal{B})_0
  =
  Th(V^{\mathcal{B}}_0)
    \simeq
  Th(\ast)
    \simeq
  S^0
  \,,
$$

by remark \ref{ThomSpaceForRankZeroBundle}.

=--

+-- {: .num_example}
###### Example

The universal [[Thom spectrum]] (def. \ref{UniversalThomSpectrumForBfStructure}) for _[[framing]] structure_ ([exmpl.](tangential+structure#ExamplesOfBfStructures)) is equivalently the [[sphere spectrum]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#StandardSphereSpectrum))

$$
  M 1 \simeq \mathbb{S}
  \,.
$$

Because in this case $B_n \simeq \ast$ and so $E^{\mathcal{B}}_n \simeq \mathbb{R}^n$, whence $Th(E^{\mathcal{B}}_n) \simeq S^n$.

=--



### Pontrjagin-Thom construction

+-- {: .num_defn #TubularNeighbourhood}
###### Definition

For $X$ a [[smooth manifold]] and $i \colon X \hookrightarrow \mathbb{R}^k$ an [[embedding]], then a **[[tubular neighbourhood]]** of $X$ is a subset of the form

$$
  \tau_i X
  \coloneqq
  \left\{
    x \in \mathbb{R}^k \;\vert\; d(x,i(X)) \lt \epsilon
  \right\}
$$

for some $\epsilon \in \mathbb{R}$, $\epsilon \gt 0$, small enough such that the map 

$$
  N_i X \longrightarrow \tau_i X
$$

from the [[normal bundle]] (def. \ref{ClassifyingMapOfNormalBundle}) given by

$$
  (i(x),v) \mapsto (i(x), \epsilon (1-e^{- {\vert v\vert}}) v )
$$

is a [[diffeomorphism]]. 

=--

+-- {: .num_prop}
###### Proposition
**([[tubular neighbourhood theorem]])**

For every [[embedding]] of [[smooth manifolds]], there exists a [[tubular neighbourhood]] according to def. \ref{TubularNeighbourhood}.

=--

+-- {: .num_remark #IngredientsOfPontrjaginThomConstruction}
###### Remark

Given an embedding $i \colon X \hookrightarrow \mathbb{R}^k$ with a tubuluar neighbourhood $\tau_i X \hookrigtharrow \mathbb{R}^k$ (def. \ref{TubularNeighbourhood}) then by construction:

1. the [[Thom space]] (def. \ref{ThomSpace}) of the [[normal bundle]] (def. \ref{ClassifyingMapOfNormalBundle}) is [[homeomorphism|homeomorphic]] to the [[quotient topological space]] of the [[topological closure]] of the tubular neighbourhood by its [[boundary]]:

   $Th(N_i(X)) \simeq \overline{ \tau_i(X)}/\partial \overline{\tau_i(X)}$;

1. there exists a continous function

   $$
     \mathbb{R}^k 
       \longrightarrow 
     \overline{ \tau_i(X)}/\partial \overline{\tau_i(X)}
   $$

   which is the identity on $\tau_i(X)\subset \mathbb{R}^k$ and is constant on the basepoint of the quotient on all other points.

=--

+-- {: .num_defn #PontrjaginThomConstruction}
###### Definition

For $X$ a [[smooth manifold]] of [[dimension]] $n$ and for $i \colon X \hookrightarrow \mathbb{R}^k$ an [[embedding]], then the **[[Pontrjagin-Thom collapse map]]** is, for any choice of [[tubular neighbourhood]] $\tau_i(X)\subset \mathbb{R}^k$ (def. \ref{TubularNeighbourhood}) the composite map of [[pointed topological spaces]]

$$
  S^k
    \overset{\simeq}{\to}
  (\mathbb{R}^k)^\ast
    \longrightarrow
  \overline{ \tau_i(X)}/\partial \overline{\tau_i(X)}
   \overset{\simeq}{\to}
  Th(N_i X)
$$

where the first map identifies the [[n-sphere|k-sphere]] as the [[one-point compactification]] of $\mathbb{R}^k$; and where the second and third maps are those of remark \ref{IngredientsOfPontrjaginThomConstruction}.

The **Pontrjagin-Thom construction** is the further composite

$$
  \xi_i
  \;\colon\;
  S^k 
   \longrightarrow
  Th(N_i X)
   \overset{Th(e_i)}{\longrightarrow}
  Th( E O(k-n) \underset{O(k-n)}{\times} \mathbb{R}^{k-n} )
    \simeq
  (M O)_{k-n}
$$

with the image under the [[Thom space]] construction of the morphism of vector bundles 

$$
  \array{
     \nu &\overset{e_i}{\longrightarrow}& E O(k-n)\underset{O(k-n)}{\times} \mathbb{R}^{k-n}
     \\
     \downarrow &(pb)& \downarrow
     \\
     X &\underset{g_i}{\longrightarrow}& B O(k-n)
  }
$$

induced by the classifying map $g_i$ of the normal bundle (def. \ref{ClassifyingMapOfNormalBundle}).


This defines an element 

$$
  [S^{n+(k-n)} \overset{\xi_i}{\to} (M O)_{k-n}]
    \in 
  \pi_{n} M O
$$

in the $n$th [[stable homotopy group]] ([def.](Introduction+to+Stable+homotopy+theory+--+1#StableHomotopyGroups)) of the [[Thom spectrum]] $M O$ (def. \ref{UniversalThomSpectrum}).

More generally, for $X$ a smooth manifold with normal [[(B,f)-structure]] $(X,i,\hat g_i)$ according to def. \ref{ManifoldWithBfStructure}, then its Pontrjagin-Thom construction is the composite

$$
  \xi_i
    \;\colon\;
  S^k 
   \longrightarrow
  Th(N_i X)
   \overset{Th(\hat e_i)}{\longrightarrow}
  Th( V^{\mathcal{B}}_{k-n} )
    \simeq
  (M \mathcal{B})_{k-n}
$$

with

$$
  \array{
     \nu &\overset{\hat e_i}{\longrightarrow}& V^{\mathcal{B}}_{k-n}
     \\
     \downarrow &(pb)& \downarrow
     \\
     X &\underset{\hat g_i}{\longrightarrow}& B O(k-n)
  }
  \,.
$$





=--

+-- {: .num_prop #PontrjaginThomConstructionGivesWellDefinedStableHomotopyGroup}
###### Proposition

The [[Pontrjagin-Thom construction]] (def. \ref{PontrjaginThomConstruction}) respects the equivalence classes entering the definition of manifolds with stable normal $\mathcal{B}$-structure (def. \ref{ManifoldWithBfStructure}) hence descends to a [[function]] (of [[sets]])

$$
  \xi
  \;\colon\;
  \left\{
    {n\text{-}manifolds\;with\;stable}
    \atop
    {normal\;\mathcal{B}\text{-}structure}
  \right\}
    \longrightarrow
  \pi_n(M\mathcal{B})
  \,.
$$

=--

+-- {: .proof}
###### Proof

It is clear that the homotopies of classifying maps of $\mathcal{B}$-structures that are devided out in def. \ref{ManifoldWithBfStructure} map to homotopies of representatives of stable homotopy groups. What needs to be shown is that the construction respects the enlargement of the embedding spaces.

Given a embedded manifold $X \overset{i}{\hookrightarrow}\mathbb{R}^{k_1}$ with normal $\mathcal{B}$-structure 

$$
  \array{
    && B_{k_1-n}
    \\
    & {}^{\mathllap{\hat g_i}}\nearrow & \downarrow^{\mathrlap{f_{k-n}}}
    \\
    X &\underset{g_i}{\longrightarrow}& B O(k_1-n)
  }
$$

write

$$
  \alpha
   \;\colon\;
  S^{n+(k_1-n)}
    \overset{}{\longrightarrow}
 Th(E^{\mathcal{B}_{k_1-n}})
$$

for its image under the [[Pontrjagin-Thom construction]] (def. \ref{PontrjaginThomConstruction}). Now given $k_2 \in \mathbb{N}$, consider the induced embedding $X \overset{i}{\hookrightarrow} \mathbb{R}^{k_1}\hookrightarrow \mathbb{R}^{k_1 + k_2}$ with normal $\mathcal{B}$-structure given by the composite

$$
  \array{
    && 
    B_{k_1-n}
      &\overset{g_{k_1-n, k_1+ k_2 -n}}{\longrightarrow}&  
    B_{k_1 + k_2-n}
    \\
    & {}^{\mathllap{\hat g_i}}\nearrow 
    &
       \downarrow^{\mathrlap{f_{k_1 - n} \times f_{k_2}}}
     &&
       \downarrow^{\mathrlap{f_{k_1 + k_2-n}}}
    \\
    X 
      &\underset{g_i}{\longrightarrow}& 
    B O(k_1-n) 
      &\longrightarrow& 
    B O(k_1 + k_2-n)
  }
  \,.
$$

By prop. \ref{PullbackOfUniversalBfBundleUnderCoordinateRestriction} and using the [[pasting law]] for [[pullbacks]], the classifying map $\hat g'_i$ for the enlarged normal bundle sits in a diagram of the form

$$
  \array{
    (\nu_i \oplus \mathbb{R}^{k_2})
      &\overset{(\hat e_i \oplus id)}{\longrightarrow}&
    (V^{\mathcal{B}}_{k_1-n} \oplus \mathbb{R}^{k_2})
      &\overset{e_{k_1-n,k_1+k_2-n}}{\longrightarrow}&
    V^{\mathcal{B}}_{k_1 + k_2 - n}
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow
    \\
    X 
      &\underset{\hat g_i}{\longrightarrow}& 
    B_{k_1-n}
      &\underset{g_{k_1-n, k_1 + k_2 - n}}{\longrightarrow}&
    B_{k_1 +k_2 - n}
  }
  \,.
$$

Hence the Pontrjagin-Thom construction for the enlarged embedding space is (using prop. \ref{SuspensionOfThomSpaces}) the composite

$$
  \alpha_{k_2}
  \;\colon\;
  S^{n + (k_1+ k_2 - n)}
   \simeq
  Th(\mathbb{R}^{k_2}) \wedge S^{n + (k_1 - n)}
    \overset{}{\longrightarrow}
  Th(\mathbb{R}^{k_2}) \wedge Th(\nu_i)
    \overset{Th(id)\wedge Th(\hat e_i)}{\longrightarrow}
  Th(\mathbb{R}^{k_2}) \wedge Th(E^{\mathcal{B}}_{k_1-n}))
    \overset{Th(e_{k_1-n, k_1 + k_2 - n})}{\longrightarrow}
  Th(V^{\mathcal{B}}_{k_1 + k_2 - n})
  \,.
$$

The composite of the first two morphisms here is $S^{k_k}\wedge \alpha$, while last morphism $Th(\hat e_{k_1-n,k_1+k_2-n})$ is the structure map in the Thom spectrum (by def. \ref{UniversalThomSpectrumForBfStructure}):

$$
  \alpha_{k_2}
   \;\colon\;
  S^{k_2} \wedge S^{n + (k_1 - n)}
    \overset{S^{k_2} \wedge \alpha}{\longrightarrow}
  S^{k_2} \wedge Th(E^{\mathcal{B}}_{k_1 + k_2 - n})
    \overset{\sigma^{M \mathcal{B}}_{k_1-n,k_1 + k_2 - n} }{\longrightarrow}
  Th(V^{\mathcal{B}}_{k_1+k_2 - n})
$$

This manifestly identifies $\alpha_{k_2}$ as being the image of $\alpha$ under the component map in the sequential colimit that defines the stable homotopy groups ([def.](Introduction+to+Stable+homotopy+theory+--+1#StableHomotopyGroups)). Therefore $\alpha$ and $\alpha_{k_2}$, for all $k_2 \in \mathbb{N}$, represent the same element in $\pi_{\bullet}(M \mathcal{B})$.

=--

## Thom's theorem
 {#ThomTheorem}

Recall that the [[Pontrjagin-Thom construction]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#PontrjaginThomConstruction)) associates to an embbeded manifold $(X,i,\hat g)$ with normal $\mathcal{B}$-structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#ManifoldWithBfStructure)) an element in the [[stable homotopy group]] $\pi_{dim(X)}(M \mathcal{B})$ of the universal $\mathcal{B}$-[[Thom spectrum]] in degree the dimension of that manifold.

+-- {: .num_lemma #PontrjaginThomIsRingHomomorphims}
###### Lemma

For $\mathcal{B}$ be a multiplicative [[(B,f)-structure]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#BfStructure)),
the $\mathcal{B}$-[[Pontrjagin-Thom construction]] ([def.](Introduction+to+Stable+homotopy+theory+--+S#PontrjaginThomConstruction)) is compatible with all the relations involved to yield a graded [[ring]] [[homomorphism]]

$$
  \xi
  \;\colon\;
  \Omega^{\mathcal{B}}_\bullet
    \longrightarrow
  \pi_\bullet(M \mathcal{B})
$$

from the $\mathcal{B}$-[[bordism ring]] (def. \ref{BordismGroupAndBordismRing}) to the [[stable homotopy groups]] of the universal $\mathcal{B}$-[[Thom spectrum]] equipped with the ring structure induced from the canonical [[ring spectrum]] structure ([def.](Introduction+to+Stable+homotopy+theory+--+S#UniversalThomSpectrumForBfStructure)).

=--

+-- {: .proof}
###### Proof

By prop. \ref{PontrjaginThomConstructionGivesWellDefinedStableHomotopyGroup} the underlying function of sets is well-defined before dividing out the bordism relation (def. \ref{BordismRelation}). To descend this further to a function out of the set underlying the bordism ring, we need to see that the Pontrjagin-Thom construction respects the bordism relation. But the definition of bordism is just so as to exhibit under $\xi$ a [[left homotopy]] of representatives of homotopy groups.

Next we need to show that it is 

1. a group homomorphism;

1. a ring homomorphism.

Regarding the first point:

The element 0 in the [[cobordism group]] is represented by the empty manifold. It is clear that the Pontrjagin-Thom construction takes this to the trivial stable homotopy now.

Given two $n$-manifolds with $\mathcal{B}$-structure, we may consider an embedding of their [[disjoint union]] into some $\mathbb{R}^{k}$ such that the [[tubular neighbourhoods]] of the two direct summands do not intersect. There is then a map from two copies of the [[n-cube|k-cube]], glued at one face

$$
  \Box^k \underset{\Box^{k-1}}{\sqcup} \Box^k
  \longrightarrow
  \mathbb{R}^k
$$

such that the first manifold with its tubular neighbourhood sits inside the image of the first cube, while the second manifold with its tubular neighbourhood sits indide the second cube. After applying the Pontryagin-Thom construction to this setup, each cube separately maps to the image under $\xi$ of the respective manifold, while the union of the two cubes manifestly maps to the sum of the resulting elements of homotopy groups, by the very definition of the group operation in the homotopy groups ([def.](Introduction+to+Stable+homotopy+theory+--+P#HomotopyGroupsOftopologicalSpaces)). This shows that $\xi$ is a group homomorphism.

Regarding the second point:

The element 1 in the [[cobordism ring]] is represented by the manifold which is the point. Without restriction we may consoder this as embedded into $\mathbb{R}^0$, by the identity map. The corresponding [[normal bundle]] is of [[rank]] 0 and hence (by remark \ref{ThomSpaceForRankZeroBundle}) its [[Thom space]] is $S^0$, the [[0-sphere]]. Also $V^{\mathcal{B}}_0$ is the rank-0 vector bundle over the point, and hence $(M \mathcal{B})_0 \simeq S^0$ (by def. \ref{UniversalThomSpectrumForBfStructure}) and so $\xi(\ast) \colon (S^0 \overset{\simeq}{\to} S^0)$ indeed represents the unit element in $\pi_\bullet(M\mathcal{B})$.


Finally regarding respect for the ring product structure: for two manifolds with stable normal $\mathcal{B}$-structure, represented by embeddings into $\mathbb{R}^{k_i}$, then the normal bundle of the embedding of their [[Cartesian product]] is the [[direct sum of vector bundles]] of the separate normal bundles bulled back to the product manifold. In the notation of prop. \ref{ThomSpaceOfExternalProductOfVectorBundles} there is a diagram of the form

$$
  \array{
    \nu_1 \boxtimes \nu_2
      &\overset{\hat e_1 \boxtimes \hat e_2}{\longrightarrow}&
    V^{\mathcal{B}}_{n_1} \boxtimes V^{\mathcal{B}}_{n_2}
      &\overset{\kappa_{n_1,n_2}}{\longrightarrow}&
    V^{\mathcal{B}}_{n_1 + n_2}
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow
    \\
    X_1 \times X_2
      &\underset{\hat g_1 \times \hat g_2}{\longrightarrow}&
    B_{k_1-n_1} \times B_{k_2-n_2}
      &\underset{\mu_{k_1-n_1,k_2-n_2}}{\longrightarrow}&
    B_{k_1 + k_2 - n_1 - n_2}
  }
  \,.
$$ 

To the Pontrjagin-Thom construction of the product manifold is by definition the top composite in the diagram

$$
  \array{
    S^{n_1 +n_2 + (k_1 + k_2 - n_1 - n_2)}
      &\overset{}{\longrightarrow}&
    Th(\nu_1 \boxtimes \nu_2)
      &\overset{Th(\hat e_1 \boxtimes \hat e_2)}{\longrightarrow}&
    Th(V^{\mathcal{B}}_{k_1-n_1} \boxtimes V^{\mathcal{B}}_{k_2-n_2})
      &\overset{\kappa_{k_1-n_1, k_2-n_2}}{\longrightarrow}&
    Th(V^{\mathcal{B}}_{k_1 + k_2 - n_1 - n_2})
    \\
    {}^{\mathllap{\simeq}}\downarrow 
      && 
    \downarrow^{\mathrlap{\simeq}}
      && 
    \downarrow^{\mathrlap{\simeq}}
      &&
    \downarrow^{\mathrlap{=}}
    \\
    S^{n_1 + (k_1 - n_1)}
      \wedge
    S^{n_2 + (k_2 - n_2)}
      &\overset{}{\longrightarrow}&
    Th(\nu_1) \wedge Th(\nu_2)
      &\overset{Th(\hat e_1)\wedge Th(\hat e_2)}{\longrightarrow}&
    Th(V^{\mathcal{B}}_1) \wedge Th(V^{\mathcal{B}}_2)
      &\overset{\kappa_{k_1-n_1, k_2-n_2}}{\longrightarrow}&
    Th(V^{\mathcal{B}}_{k_1 + k_2 - n_1 - n_2})
   }
   \,,
$$

which hence is equivalently the bottom composite, which in turn manifestly represents the product of the separate PT constructions in $\pi_\bullet(M\mathcal{B})$.


=--

+-- {: .num_theorem #MorphismFromCobordismRingToStableHomotopyGroupsOfThomSpectrumIsIso}
###### Theorem

The ring homomorphsim in lemma \ref{PontrjaginThomIsRingHomomorphims} is an [[isomorphism]].

=--

Due to ([Thom 54](#Thom54), [Pontrjagin 55](#Pontrjagin55)). See for instance ([Kochmann 96, theorem 1.5.10](#Kochmann96)).

+-- {: .proof}
###### Proof idea

Observe that given the result $\alpha \colon S^{n+(k-n)} \to Th(V_{k-n})$ of the Pontrjagin-Thom construction map, the original manifold $X \overset{i}{\hookrightarrow} \mathbb{R}^k$  may be recovered as this [[pullback]]:

$$
  \array{
    X &\overset{i}{\longrightarrow}& S^{n + (k-n)}
    \\
    {}^{\mathllap{g_i}}\downarrow &(pb)& \downarrow^{\mathrlap{\alpha}}
    \\
    B O(k-n) &\longrightarrow& Th(V^{B O}_{k-n})
  }
  \,.
$$

To see this more explicitly, break it up into pieces:

$$
  \array{
   X &\longrightarrow& X_+ &\hookrightarrow& S^{n + (k-n)}
   \\
   \downarrow &(pb)& \downarrow &(pb)& \downarrow
    \\
    X &\longrightarrow& X_+ \simeq Th(X) &\overset{Th(0)}{\longrightarrow}& Th(\nu_i)
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow
    \\
    B_{k-n}
      &\longrightarrow& 
    (B_{k-n})_+ \simeq Th(B_{k-n}) 
    &\underset{Th(0)}{\longrightarrow}& Th(V^{\mathcal{B}}_{k-n})
    \\
    \downarrow &(pb)& \downarrow &(pb)& \downarrow
    \\
    B O(k-n)
      &\longrightarrow& 
    (B O(k-n))_+ \simeq Th(B O(k-n)) 
      &\longrightarrow& 
    Th(V^{B O}_{k-n})
  }
  \,.
$$

Moreover, since the [[n-spheres]] are [[compact topological spaces]], and since the [[classifying space]] $B O(n)$, and hence its universal Thom space, is a [[sequential colimit]] over [[relative cell complex]] inclusions, the right vertical map factors through some finite stage (by [this lemma](Introduction+to+Stable+homotopy+theory+--+P#CompactSubsetsAreSmallInCellComplexes)), the manifold $X$ is equivalently recovered as a pullback of the form

$$
  \array{
    X &\longrightarrow& S^{n + (k-n)}
    \\
    {}^{\mathllap{g_i}}\downarrow &(pb)& \downarrow
    \\
    Gr_{k-n}(\mathbb{R}^k) 
      &\overset{i}{\longrightarrow}&
    Th( V_{k-n}(\mathbb{R}^k) \underset{O(k-n)}{\times} \mathbb{R}^{k-n})
  }
  \,.
$$

(Recall that $V^{\mathcal{B}}_{k-n}$ is our notation for the [[universal vector bundle]] with $\mathcal{B}$-structure, while $V_{k-n}(\mathbb{R}^k)$ denotes a [[Stiefel manifold]].)

The idea of the proof now is to use this property as the blueprint of the construction of an [[inverse]] $\zeta$ to $\xi$: given an element in $\pi_{n}(M \mathcal{B})$ represented by a map as on the right of the above diagram, try to define $X$ and the structure map $g_i$ of its normal bundle as the pullback on the left.

The technical problem to be overcome is that for a general continuous function as on the right, the pullback has no reason to be a smooth manifold, and for two reasons:

1. the map $S^{n+(k-n)} \to Th(V_{k-n})$ may not be smooth around the image of $i$;

1. even if it is smooth around the image of $i$, it may not be [[transversal map|transversal]] to $i$, and the intersection of two non-transversal smooth functions is in general still not a smooth manifold.

The heart of the proof is in showing that for any $\alpha$ there are small homotopies relating it to an $\alpha'$ that is both smooth around the image of $i$ and transversal to $i$.

The first condition is guaranteed by [[Sard's theorem]], the second by [[Thom's transversality theorem]].

(...)








=--



## Related entries

* [[Pontryagin-Thom collapse map]]

* [[Thom's transversality theorem]]

* [[Cohomotopy cohomology theory]], [[Cohomotopy charge]]


## References


[[!include Pontryagin-Thom construction -- references]]





[[!redirects Thom theorem]]

[[!redirects Pontrjagin-Thom theorem]]
[[!redirects Pontrjagin-Thom isomorphism]]

[[!redirects Pontryagin-Thom theorem]]
[[!redirects Pontryagin-Thom isomorphism]]