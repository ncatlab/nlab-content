

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

The universal real Thom spectrum [[MO]] is a [[connective spectrum]] whose associated [[infinite loop space]] is the [[classifying space]] for [[cobordism]]:

$$
  \Omega^\infty M O \simeq \vert Cob_\infty \vert .
$$

In particular, $\pi_n M O$ is naturally identified with the set of [[cobordism classes]] of [[closed manifold|closed]] $n$-[[manifolds]] ([[Thom's theorem]]).

More abstractly, [[MO]] is the [[homotopy colimit]] of the [[J-homomorphism]] in [[Spectra]]

$$
  M O \simeq \underset{\longrightarrow}{\lim}(B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to Spectra)
$$

hence the "total space" of the universal [[spherical fibration]] on the [[classifying space]] $B O$ for (stable) [[real vector bundles]].

Given this, for any [[topological group]] $G$ equipped with a [[homomorphism]] to the [[orthogonal group]] there is a corresponding Thom spectrum

$$
  M G \simeq \underset{\longrightarrow}{\lim}(B G\to B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to Spectra)
  \,.
$$

This is considered particularly for the stages $G$ in the [[Whitehead tower]] of the [[orthogonal group]], where it yields $M$[[Spin group|Spin]], $M$[[String group]], etc. 

All these Thom spectra happen to naturally have the structure of [[E-∞ rings]] and $E_\infty$-ring homomorphisms $M O\to E$ into another $E_\infty$-ring $E$ are equivalently universal [[orientation in generalized cohomology|orientations in E-cohomology]]. On [[homotopy groups]] these are [[genera]] with [[coefficients]] in the underlying ring $\pi_\bullet(E)$.


## Definition

### For vector bundles
 {#ForVectorBundles}

First recall the following two basic facts about the construction of [[Thom spaces]]. See at _[[Thom space]]_ [this prop.](Thom+space#SuspensionOfThomSpaces).


+-- {: .num_prop #SuspensionOfThomSpaces}
###### Proposition

For $V \to X$ a [[vector bundle]], there is a [[homeomorphism]]

$$
  Th(\mathbb{R}^n \oplus V) \simeq S^n \wedge Th(V) = \Sigma^n Th(V)
$$

between, on the one hand, the [[Thom space]] of the [[direct sum of vector bundles]] of $V$ with the [[trivial vector bundle]] of [[rank]] $n$ and, on the other, the $n$-fold [[reduced suspension]] of the [[Thom space]] of $V$.

=--

+-- {: .num_prop #ThomSpaceOfExternalProductOfVectorBundles}
###### Proposition

For $V_1 \to X_1$ and $V_2 \to X_2$ to vector bundles, let $V_1 \boxtimes V_2 \to X_1 \times X_2$ be the [[direct sum of vector bundles]] of their [[pullbacks]] to $X_1 \times X_2$ (their [[external tensor product]]). The corresponding [[Thom space]] is the [[smash product]] of the individual Thom spaces:

$$
  Th(V_1 \boxtimes V_2)
  \simeq
  Th(V_1) \wedge Th(V_2)
  \,.
$$

=--

Prop. \ref{SuspensionOfThomSpaces} will give rise to universal Thom spectra in the following, while prop. \ref{ThomSpaceOfExternalProductOfVectorBundles} will give them the struture of [[ring spectra]].

+-- {: .num_defn #ThomSpectrumOfAVectorBundle}
###### Definition

For $V \to X$ a [[vector bundle]], its **Thom spectrum** is the [[suspension spectrum]] $\Sigma^\infty Th(V)$ of the [[Thom space]] of $V$. By prop. prop. \ref{SuspensionOfThomSpaces} this may be written as

$$
  (\Sigma^\infty Th(V)) 
  \simeq
  Th(\mathbb{R}^n \oplus V)
$$ 

with structure maps the equivalences

$$
  \sigma_n
    \;\colon\;
  \Sigma Th(\mathbb{R}^n \oplus V) 
    \stackrel{\simeq}{\longrightarrow} 
  Th(\mathbb{R}^{n+1} \oplus V) 
  \,.
$$

=--


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

where the bottom morphism is the canonical inclusion ([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne)). Under taking [[colimit]] over $k$, this produces the claimed pullback.

=--

+-- {: .num_defn}
###### Definition

The $n$-fold looping of the Thom spectrum, according to def. \ref{ThomSpectrumOfAVectorBundle}, of the rank-$n$ [[universal vector bundle]] is written

$$
  M O(n)
    \coloneqq
  \Sigma^{-n} \Sigma^\infty Th( E O(n) \underset{O(n)}{\times} \mathbb{R}^n )
  \,.
$$

The image of the top horizontal maps in prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction} under $\Sigma^{-n-1}Th(-)$ are, via prop. \ref{SuspensionOfThomSpaces}, maps of the form

$$
  M O(n) \longrightarrow M O(n+1)
$$

The [[homotopy colimit]] over these maps is the universal Thom spectrum:

$$
  M O \coloneqq {\lim_\to}_n M O(n) 
  \,.
$$

=--

More explicitly:

+-- {: .num_defn #UniversalThomSpectrum}
###### Definition

As a [[sequential spectrum]], the _universal Thom spectrum_ $M O$ is represented by the [[sequential prespectrum]] whose $n$th component space is the [[Thom space]] 

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


+-- {: .num_defn}
###### Definition

As an [[orthogonal ring spectrum]], the universal [[Thom spectrum]] $M O$ has

* component spaces 

  $$
    (M O)_V \coloneqq E O(V)_+ \underset{O(V)}{\wedge} S^V
  $$

  the [[Thom spaces]] of the [[universal vector bundle]] with fiber $V$;

* left $O(V)$-action induced by the remaining canonical left action of $E O(V)$;

* multiplication maps

  $$
    (E O(V_1)_+ \underset{O(V_1)}{\wedge} S^{V_1})
      \wedge
    (E O(V_2)_+ \underset{O(V_2)}{\wedge} S^{V_2}  
      \longrightarrow
    E O(V_1 \oplus V_2)_+ 
      \underset{O(V_1 \oplus V_2)}{\wedge} 
    S^{V_1 \oplus V_2}
  $$

  induced via prop. \ref{ThomSpaceOfExternalProductOfVectorBundles}

* unit maps given by

  $$
    S^V \simeq O(V)_+ \wedge_{O(V)} S^V
      \longrightarrow
    E O(V)_+ \wedge_{O(V)} S^V
  $$

  induced by the fiber inclusion $O(V) \to E O(V)$.

=--

For discussion of the refinement of the Thom spectrum $M O$
to a [[symmetric spectrum]] see ([Hovey-Shipley-Smith 00, example 6.2.3](#HoveyShipleySmith00), [Schwede 12, Example I.2.8](#Schwede12)). For the refinement to an [[orthogonal spectrum]] and [[globally equivariant spectrum]] see ([Schwede 15, section V.4](#Schwede15)).




More generally, there are universal Thom spectra associated with any other tangent structure ("[[(B,f)-structure]"), notably for the orthogonal group replaced by the [[special orthogonal groups]] $SO(n)$, or the [[spin groups]] $Spin(n)$, or the [[string 2-group]] $String(n)$, or the [[fivebrane 6-group]] $Fivebrane(n)$,..., or any level in the [[Whitehead tower]] of $O(n)$. To any of these groups there corresponds a Thom spectrum (denoted, respectively, $M SO$, $M Spin$, $M String$, $M Fivebrane$, etc.), which is in turn related to oriented cobordism, spin cobordism, string cobordism, et cetera.

Recall:

+-- {: .num_defn #BfStructure}
###### Definition

A [[(B,f)-structure]] $\mathcal{B}$, is a system of [[Serre fibrations]]

$$
  \array{
    B_n
    \\
    \downarrow^{\mathrlap{f_n}}
    \\
    B O(n)
  }
$$

for $n \in \mathbb{N}$, equipped with maps $j_n \colon B_n \to B_{n+1}$ covering the canonical maps $i_n \colon B O(n) \to B O(n+1)$ (([def.](classifying+space#InclusionOfBOnIntoBOnPlusOne))) in that there are [[commuting squares]]

$$
  \array{
    B_n &\overset{j_n}{\longrightarrow}& B_{n+1}
    \\
    \downarrow^{\mathrlap{f_n}}
      &&
    \downarrow^{\mathrlap{f_{n+1}}}
    \\
    B O(n)
      &\overset{i_n}{\longrightarrow}&
    B O(n+1)
  }
  \,.
$$

Similarly, an **$S^2$-$(B,f)$-structure** is a compatible system

$$
  f_{2n} \colon B_{2n} \longrightarrow B O(2n)
$$

indexed only on the even natural numbers.


=--

+-- {: .num_defn #VectorBundleAssociatedWithBfStructure}
###### Definition

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}), write

$$
  E^{\mathcal{B}}_n \coloneqq f_n^\ast ( E O(n) \underset{O(n)}{\times} \mathbb{R}^n )
$$

for the [[pullback]] of the rank-$n$ [[universal vector bundle]] from $B O(n)$ to $B_n$ along $f_n$.

=--

Observe that the analog of prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction} still holds:

+-- {: .num_prop #PullbackOfUniversalBfBundleUnderCoordinateRestriction}
###### Proposition

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}), then the pullback of its rank-$(n+1)$ vector bundle $E^{\mathcal{B}}_{n+1}$ (def. \ref{VectorBundleAssociatedWithBfStructure}) along the map $j_n \colon B_n \to B_{n+1}$ is the [[direct sum of vector bundles]] of the rank-$n$ bundle $E^{\mathcal{B}}_n$ with the trivial rank-1-bundle: there is a pullback square

$$
  \array{
    \mathbb{R} \oplus E^{\mathcal{B}}_n 
      &\longrightarrow&
    E^{\mathcal{B}}_{n+1}
    \\
    \downarrow &(pb)& \downarrow
    \\
    B_n &\underset{j_n}{\longrightarrow}& B_{n+1}
  }
  \,.
$$

=---

+-- {: .proof}
###### Proof

Unwinding the definitions, the pullback in question is

$$
  \begin{aligned}
    j_n^\ast E^{\mathcal{B}}_{n+1}
      & =
    j_n^\ast f_{n+1}^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
    \\
    & \simeq
    (j_n \circ f_{n+1})^\ast (E O(n+1)\underset{O(n+1)}{\times} \mathbb{R}^{n+1})
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
    &\simeq \mathbb{R} \oplus E^{\mathcal{B}_n}
    \,,
  \end{aligned}
$$

where the second but last step is due to prop. \ref{PullbackOfUniversalOnBundleUnderCoordinateRestriction}.

=--

+-- {: .num_defn}
###### Definition

Given a [[(B,f)-structure]] $\mathcal{B}$ (def. \ref{BfStructure}), its Thom spectrum $M \mathcal{B}$ is, as a [[sequential prespectrum]], given by component spaces being the [[Thom spaces]] of the $\mathcal{B}$-associated vector bundles of def. \ref{VectorBundleAssociatedWithBfStructure}

$$
  (M \mathcal{B})_n
  \coloneqq
  Th(E^{\mathcal{B}}_n)
$$

and with structure maps given via prop. \ref{SuspensionOfThomSpaces} by the top maps in prop. \ref{PullbackOfUniversalBfBundleUnderCoordinateRestriction}:

$$
  \sigma_n
    \;\colon\;
  \Sigma (M \mathcal{B})_n
    =
  \Sigma Th(E^{\mathcal{E}}_n)
    \simeq
  Th(\mathbb{R}\oplus E^{\mathcal{E}}_n)
    \longrightarrow
  Th(E^{\mathcal{E}}_{n+1})
  =
  (M \mathcal{B})_{n+1}
  \,.
$$

Similarly for a $(B,f)$-structure indexed on the even natural numbers, there is the corresponding Thom spectrum as an $S^2$-sequential spectrum ([def.](model+structure+on+topological+sequential+spectra#SequentialS2Spectra)).

If $B_n = B G_n$ for some natural system of groups $G_n \to O(n)$, then one usually writes $M G$ for $M \mathcal{B}$. For instance $M SO$, $M Spin$, $M U$ etc.

If the $(B,f)$-structure is multiplicative (def. \ref{BfStructure}), then the Thom spectrum $M \mathcal{B}$ canonical becomes a [[ring spectrum]]: the multiplication maps $B_{n_1} \times B_{n_2}\to B_{n_1 + n_2}$ are covered by maps of vector bundles

$$
  E^{\mathcal{B}}_{n_1} \boxtimes E^{\mathcal{B}}_{n_2}
  \longrightarrow
  E^{\mathcal{B}}_{n_1 + n_2}
$$

and under forming [[Thom spaces]] this yields, by prop. \ref{ThomSpaceOfExternalProductOfVectorBundles}, maps

$$
  (M \mathcal{B})_{n_1}
  \wedge
  (M \mathcal{B})_{n_2}
  \longrightarrow
  (M \mathcal{B})_{n_1 + n_2}
  \,.
$$


=--

+-- {: .num_example}
###### Example

The Thom spectrum of the _[[framing]] structure_ ([exmpl.](G-structure#ExamplesOfBfStructures)) is equivalently the [[sphere spectrum]]

$$
  M 1 \simeq \mathbb{S}
  \,.
$$

Because in this case $B_n \simeq \ast$ and so $E^{\mathcal{B}}_n \simeq \mathbb{R}^n$, whence $Th(E^{\mathcal{B}}_n) \simeq S^n$.

=--




### For spherical fibrations
 {#ForSphereBundles}

+-- {: .num_defn #ThomSpectrumForSphericalFibrations}
###### Definition

(...)

=--

### For $(\infty,1)$-module bundles
 {#ForInfinityModuleBundles}

We discuss the Thom spectrum construction for general [[(∞,1)-module bundles]].

+-- {: .num_prop}
###### Proposition

There is pair of [[adjoint (∞,1)-functors]]

$$
  (\Sigma^\infty \Omega^\infty \dashv gl_1)
   \colon
  E_\infty Rings
   \stackrel{\overset{\Sigma^\infty \Omega^\infty}{\leftarrow}}{\underset{gl_1}{\to}}
  Spec_{con}
  \,,
$$

where $(\Sigma^\infty \dashv \Omega^\infty) : Spec \to Top$ is the [[stabilization]] adjunction between [[Top]] and [[Spec]] ($\Sigma^\infty$ forms the [[suspension spectrum]]), restricted to connective spectra.  The [[right adjoint]] is the _[[∞-group of units]]_-[[(∞,1)-functor]], see there for more details.

=--

This is ([ABGHR, theorem 2.1/3.2](#ABGHR)).

+-- {: .num_remark}
###### Remark

Here $gl_1$ forms the "[[general linear group]]-of rank 1"-spectrum of an [[E-∞ ring]]: its [[∞-group of units]]". The adjunction is the generalization of the adjunction

$$
  (\mathbb{Z}[-] \dashv GL_1) : 
   CRing \stackrel{\overset{\mathbb{Z}[1]}{\leftarrow}}{\underset{GL_1}{\to}}
  Ab
$$

between [[CRing]] and [[Ab]], where $\mathbb{Z}[-]$ forms the [[group ring]].

=--

+-- {: .num_defn}
###### Definition

Write 

$$
  b gl_1(R) \coloneqq \Sigma gl_1(R)
$$

for the [[suspension]] of the group of units $gl_1(R)$. 

=--

This plays the role of the [[classifying space]] for $gl_1(R)$-[[principal ∞-bundle]]s. 

For $f : b \to b gl_1(R)$ a morphism (a [[cocycle]] for $gl_1(R)$-bundles) in [[Spec]], write $p \to b$ for the corresponding bundle: the [[homotopy fiber]]

$$
  \array{
     p &\to& * 
     \\
     \downarrow && \downarrow
     \\
     b &\stackrel{f}{\to}& b gl_1(R)
  }
  \,.
$$

Given a $R$-algebra $A$, hence an [[A-∞ algebra]] over $R$, exhibited by a morphism $\rho : R \to A$, the composite

$$
  \rho(f) : b \stackrel{f}{\to} b gl_1(R) \stackrel{\rho}{\to} b gl_1(A)
$$

is that for the corresponding [[associated ∞-bundle]].

We write capital letters for the underlying spaces of these spectra:

$$
  P \coloneqq \Sigma^\infty \Omega^\infty p
$$

$$
  B \coloneqq \Sigma^\infty \Omega^\infty b
$$

$$
  GL_1(R) \coloneqq \Sigma^\infty \Omega^\infty gl_1(R)
$$


+-- {: .num_defn #GeneralThomSpectrum}
###### Definition

The **Thom spectrum** $M f$ of $f : b \to gl_1(R)$ is the [[(∞,1)-pushout]]

$$
  \array{
    \Sigma^\infty \Omega^\infty R &\to& R
    \\
    \downarrow && \downarrow
    \\
    \Sigma^\infty \Omega^\infty p &\to& M f
  }
  \,,
$$

hence the [[derived functor|derived]] [[smash product]]

$$
  M f \simeq P \wedge_{GL_1(R)} R
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This means that a morphism $M f \to A$ is an $GL_1(R)$-equivariant map $P \to A$.

Notice that for $R = \mathbb{C}$ the [[complex number]]s, $B \to GL_1(R)$ is the cocycle for a [[circle bundle]] $P \to B$. A $U(1)$-equivariant morphism $P \to A$ to some [[representation]] $A$ is equivalently a [[section]] of the A-[[associated bundle]]. 

Therefore the Thom spectrum may be thought of as co-[[representable functor|representing]] spaces of sections of associated bundles

"$Hom(M f, A) \simeq \Gamma(P \wedge_{GL_1(R)} A)$".

=--

This is made precise by the following statement.

+-- {: .num_prop}
###### Proposition

We have an [[(∞,1)-pullback]] diagram

$$
  \array{
    E_\infty Alg_R(M f, A) &\stackrel{}{\to}& (...)
    \\
    \downarrow && \downarrow
    \\
    * &\stackrel{}{\to}& (...)
  }
$$

=--

This is ([ABGHR, theorem 2.10](#ABGHR)).

This definition does subsume the [above](ForSphereBundles) definition of Thom spectra for [[sphere bundles]] (hence also that for [[vector bundles]], by removing their [[zero section]]):

+-- {: .num_prop}
###### Proposition

Let $R = S$ be the [[sphere spectrum]]. Then for $f \colon b \to gl_1(S)$ a cocycle for an $S$-bundle, 

$$
  G \coloneqq \Omega^\infty g \colon B \to B GL_1(S)
$$

is the classifying map for a [[spherical fibration]] over $B \in Top$. 

The Thom spectrum $M f$ of def. \ref{GeneralThomSpectrum} is equivalent to the Thom spectrum of the spherical fibration, according to def. \ref{ThomSpectrumForSphericalFibrations}.

=--

This is in ([ABGHR, section 8](#ABGHR)).

Equivalently the Thom spectrum is characterized as follows:

+-- {: .num_defn #ThomSpectrumAsHomotopyColimit}
###### Definition/Proposition

For $\chi \colon X \to  R Line$ a map to the [[∞-group]] of $R$-[[(∞,1)-lines]] inside $R Mod$, the corresponding Thom spectrum is the [[(∞,1)-colimit]]

$$
  \Gamma(\chi) \coloneqq
  \underset{\rightarrow}{\lim}
  \left(
    X \stackrel{\chi}{\to} Pic(R) \hookrightarrow R Mod
  \right)
  \,.
$$

This construction evidently extendes to an [[(∞,1)-functor]]

$$
  \Gamma \colon \infty Grpd_{/R Line} \to R Mod
  \,. 
$$


=--



This is ([Ando-Blumberg-Gepner 10, def. 4.1](#ABG10)), reviewed also as ([Wilson 13, def. 3.3](#Wilson13)).

+-- {: .num_remark}
###### Remark

This is the $R$-[[(∞,1)-module]] of [[sections]] of the [[(∞,1)-module bundle]] classified by $X \stackrel{\chi}{\to} Pic(R) \hookrightarrow R Mod$.

By the [[universal property]] of the [[(∞,1)-colimit]] we have for $\underline{R} \colon X \to R Mod$ the trivial $R$-bundle that 

$$
  Hom_{[X, R Mod]}(\chi, \underline{R})
  \simeq
  Hom_{R Mod}(\Gamma(\chi), R)
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

The section/Thom spectrum functor is the left [[(∞,1)-Kan extension]] of the canonical embedding $R Line \hookrightarrow R Mod$ along the [[(∞,1)-Yoneda embedding]]

$$
  R Line \hookrightarrow [R Line^{op}, \infty Grpd]
  \simeq \infty Grpd_{/R Line}
$$

(where the [[equivalence of (∞,1)-categories]] on the right is given by the [[(∞,1)-Grothendieck construction]]). In other words, it is the essentially unique [[(∞,1)-colimit]]-preserving [[(∞,1)-functor]]  $\infty Grpd_{/ R Line} \to R Mod$ which restricts along this inclusion to the canonical embedding.

=--

This observation appears as ([Wilson 13, prop. 4.4](#Wilson13)).

## Properties

### Ring spectrum structure
 {#RingSpectrumStructure}


The universal Thom spectrum, def. \ref{UniversalThomSpectrum}, naturally inherits the structure of a [[ring spectrum]] as follows.

+-- {: .num_prop}
###### Proposition

There are canonical commuting diagrams

$$
  \array{
    ( E (O(k)\times O(\ell))\underset{O(k)\times O(\ell)}{\times}) 
    \mathbb{R}^k \oplus \mathbb{R}^\ell
    &\longrightarrow& 
    E O(k+\ell)\underset{O(k + ell)}{\times} \mathbb{R}^{k+\ell}
    \\
    \downarrow && \downarrow
    \\
    B O(k)\times B O(\ell)
    &\stackrel{}{\longrightarrow}&
    B O(k + \ell)
  }
  \,.
$$

Applying the [[Thom space]] functor to the top morphisms and using prop. \ref{ThomSpaceOfExternalProductOfVectorBundles} gives morphisms

$$
  M O(k) \wedge M O(\ell)
  \longrightarrow
  M O(k + \ell)
$$

that combine to a [[functor with smash products]] and hence give $M O$ the structure of a [[ring spectrum]].

=--

More abstractly, the sufficient condition for a Thom spectrum of an ∞-module bundle (as [above](#ForInfinityModuleBundles)) to have an [[E-∞ ring]] structure is that it arises as the [[(∞,1)-colimit]] of a homomorphism of [[E-∞ spaces]]  $B \to A Line$ ([ABG 10, prop.6.21](#ABG10)).




### Relation to the cobordism ring

+-- {: .num_prop}
###### Proposition

The [[cobordism ring|cobordism group]] of un[[oriented]] $n$-[[dimension]]al [[manifold]]s is [[natural isomorphism|naturally isomorphic]] to the $n$th [[homotopy group]] of the Thom spectrum $M O$. That is, there is a natural isomorphism

$$
  \Omega^{un}_\bullet \simeq \pi_\bullet M O 
   \coloneqq
  {\lim_{\to}}_{k \to \infty} \pi_{n+k} M O(k)
  \,.
$$

=--

This is a seminal result due to ([Thom 54](#Thom54)), whose proof proceeds by the [[Pontryagin-Thom construction]]. The presentation of the following proof follows ([Francis, lecture 3](#Francis3)).

+-- {: .proof}
###### Proof

We first construct a map $\Theta : \Omega_n^{un} \to \pi_n M O$. 

Given a class $[X] \in \Omega_n^{un}$ we can choose a representative $X \in $ [[SmthMfd]] and a [[closed embedding]] $\nu$ of $X$ into the [[Cartesian space]] $\mathbb{R}^{n+k}$ of sufficiently large [[dimension]]. By the [[tubular neighbourhood theorem]] $\nu$ factors as the embedding of the [[zero section]] into the [[normal bundle]] $N_\nu$ followed by an [[open embedding]] of $N_\nu$ into $\mathbb{R}^{n+k}$

$$
  \array{
     X &&\stackrel{\nu}{\hookrightarrow}&& \mathbb{R}^{n+k}
     \\
     & \searrow && \nearrow_{\mathrlap{i}}
     \\
     && N_\nu
  }
  \,.
$$

Now use the [[Pontrjagin-Thom construction]] to produce an element of the [[homotopy group]] first in the [[Thom space]] $Th(N_\nu)$ of $N_\nu$ and then eventually in $M O$.  To that end, let

$$
  \mathbb{R}^{n+k} \to (\mathbb{R}^{n+k})^+ \simeq S^{n+k}
$$

be the map into the [[one-point compactification]]. Define a map

$$
  t : S^{n+k} \simeq (\mathbb{R}^{n+k})^+ \to Disk(N_\nu)/Sphere(N_\nu) \simeq Th(N_\nu)
$$

by sending points in the image of $Disk(N_\nu)$ under $i$ to their preimage, and all other points to the collapsed point $Sphere(N_\nu)$. This defines an element in the [[homotopy group]] $\pi_{n+k}(Th(N_\nu))$.

To turn this into an element in the homotopy group of $M O$, notice that  since $N_\nu$ is a [[vector bundle]] of [[rank]] $k$, it is the [[pullback]] by a map $\mu$ of the universal rank $k$ vector bundle $\gamma_k \to B O(k)$

$$
  \array{
    N_\nu \simeq \mu^* \gamma_k &\to& \gamma_k
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\mu}{\to}& B O(k)
  }
  \,.
$$

By forming Thom spaces the top map induces a map

$$
  Th(N_\nu) \to Th(\gamma^k) =: M O(k)
  \,.
$$

Its composite with the map $t$ constructed above gives an element in $\pi_{n+k} M O(k)$

$$
  S^{n+k} \stackrel{t}{\to} Th(N_\nu) \to Th(\gamma^k) \simeq M O(k)
$$

and by $\pi_{n+k} M O(k) \to {\lim_\to}_k \pi_{n+k} M O(k) =: \pi_n M O$ this is finally  an element 

$$
  \Theta
  :
  [X]
   \mapsto
  (S^{n+k} \stackrel{t}{\to} Th(N_\nu) \to Th(\gamma^k) \simeq M O(k)) 
  \in
  \pi_n M O
  \,.
$$

We show now that this element does not depend on the choice of embedding $\nu : X \to \mathbb{R}^{n+k}$.

(...)

Finally, to show that $\Theta$ is an [[isomorphism]] we proceed by constructing an inverse.

For that, observe that the [[sphere]] $S^{n+k}$ is a [[compact topological space]] and in fact a [[compact object]] in [[Top]]. This implies that every map $f$ from $S^{n+k}$ into the [[filtered colimit]] 

$$
  Th(\gamma^k)  \simeq {\lim_\to}_s Th(\gamma^k_s)
  \,,
$$

factors through one of the terms as

$$
  f : S^{n+k} \to Th(\gamma^k_s) \hookrightarrow Th(\gamma^k)
  \,.
$$

By [[Thom's transversality theorem]] we may find an embedding $j : Gr_k(\mathbb{R}^s) \to Th(\gamma^k_s)$ by a [[transverse map]] to $f$. Define then $X$ to be the [[pullback]]

$$
  \array{
    X &\to& Gr_k(\mathbb{R}^s)
    \\
    \downarrow && \downarrow^{\mathrlap{j}}
    \\
    S^{n+k} &\stackrel{f}{\to}& Th(\gamma^k_s)
  }
  \,.
$$

We check that this construction provides an inverse to $\Theta$.

(...)

=--

+-- {: .num_remark }
###### Remark

The [[homotopy equivalence]] $\Omega^\infty M O \simeq \vert Cob_\infty \vert$ is the content of the [[Galatius-Madsen-Tillmann-Weiss theorem]], and is now seen as a part of the [[cobordism hypothesis]] theorem.

=--

### As a dual in the stable homotopy category
 {#AsDualObject}

Write [[Spec]] for the category of [[spectra]] and $Ho(Spec)$ for its standard [[homotopy category]]: the [[stable homotopy category]]. By the [[symmetric monoidal smash product of spectra]] this becomes a [[monoidal category]].

For $X$ any [[topological space]], we may regard it as an object in $Ho(Spec)$ by forming its [[suspension spectrum]] $\Sigma^\infty_+ X$. We may ask under which conditions on $X$ this is a [[dualizable object]] with respect to the smash-product monoidal structure.

It turns out that a sufficient condition is that $X$ a closed [[smooth manifold]] or more generally a [[compact topological space|compact]] Euclidean [[neighbourhood retract]]. In that case $Th(N X)$ -- the Thom spectrum of its [[normal bundle|stable normal bundle]] is the corresponding [[dual object]]. ([Atiyah 61](#Atiyah61), [Dold-Puppe 78](#DoldPuppe78)). This is called the [[Spanier-Whitehead dual]] of $\Sigma^\infty_+ X$.

Using this one shows that the [[trace]] of the identity on $\Sigma^\infty_+ X$ in $Ho(Spec)$ -- the categorical [[dimension]] of $\Sigma^\infty_+ X$ -- is the [[Euler characteristic]] of $X$.

For a brief exposition see ([PontoShulman, example 3.7](#PontoShulman)). For more see at _[[Spanier-Whitehead duality]]_.

### As the universal spherical fibration, from the $J$-homomorphism
 {#AsTheUniversalSphericalFibration}

The [[J-homomorphism]] is a canonical map $B O \to B gl_1(\mathbb{S})$ from the [[classifying space]] of the [[stable orthogonal group]] to the [[delooping]] of the [[infinity-group of units]] of the [[sphere spectrum]]. This classifies an "[[(∞,1)-vector bundle]]" of [[sphere spectrum]]-[[module spectrum|modules]] over $B O$ and this is the Thom spectrum.

So in terms of the [[(∞,1)-colimit]] description [above](#ForInfinityModuleBundles) we have

$$
  M O \simeq  \underset{\longrightarrow}{\lim}(B O \stackrel{J}{\to} B GL_1(\mathbb{S}) \to \mathbb{S}Mod = Spectra)
  \,.
$$

See at _[[orientation in generalized cohomology]]_ for more on this.





### As the infinite cobordism category
 {#AsTheInfiniteCobordismCategory}

The [[geometric realization]] for the  [[(infinity,n)-category of cobordisms]] for $n \to \infty$ is the Thom spectrum

$$
  \vert Bord_\infty \vert \simeq \Omega^\infty MO
  \,.
$$

This is implied by the [[Galatius-Madsen-Tillmann-Weiss theorem]] and  by [[Jacob Lurie]]'s proof of the [[cobordism hypothesis]]. See also ([Francis-Gwilliam, remark 0.9](Francis3)).

## Cohomology

Under the [[Brown representability theorem]] the Thom spectrum represents the [[generalized (Eilenberg-Steenrod) cohomology]] theory called [[complex cobordism cohomology theory|cobordism cohomology theory]].

## Related concepts

* [[cobordism theory]]


* [[Thom space]], [[Thom isomorphism]], [[Pontryagin-Thom collapse map]]

* [[cobordism ring]]

[[!include generalized fiber integration synonyms - table]]

## References


### General

The relation between the homotopy groups of the Thom spectrum and the cobordism ring is due to

* {#Thom54} [[René Thom]], _Quelques propri&#233;t&#233;s globales des vari&#233;t&#233;s diff&#233;rentiables_ Comment. Math. Helv. 28, (1954). 17-86

Further original articles include

* {#Atiyah61} [[Michael Atiyah]], _Thom complexes_, Proc. London Math. Soc. (3), 11:291&#8211;310, 1961. 10  ([pdf](http://www.maths.ed.ac.uk/~aar/papers/atiyahthom.pdf))

Textbook accounts include

* {#Adams74} [[Frank Adams]], part III, section 2 of _[[Stable homotopy and generalised homology]]_, 1974

* {#Kochmann96} [[Stanley Kochman]], section 1.5 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

Lecture notes include

* {#Francis3} [[John Francis]], _Topology of manifolds_ course notes (2010) ([web](http://math.northwestern.edu/~jnkf/classes/mflds/)) 

  Lecture 3 _Thom's theorem_ (notes by A. Smith) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/3thom.pdf))

  A remark of the relation of the Thom spectrum to [[(∞,n)-category of cobordisms]] for $n = \infty$ is in:

  Lecture 2 _Cobordisms_ (notes by [[Owen Gwilliam]]) ([pdf](http://math.northwestern.edu/~jnkf/classes/mflds/2cobordism.pdf))
  
* {#Ebert12} [[Johannes Ebert]], _A lecture course on Cobordism Theory_, 2012 ([pdf](http://wwwmath.uni-muenster.de/u/jeber_02/skripten/bordism-skript.pdf))

* {#Freed13} [[Dan Freed]], lecture 10 of _Bordism: old and new_, 2013 ([pdf](http://www.ma.utexas.edu/users/dafr/bordism.pdf))


As [[symmetric spectra]]:

* {#HoveyShipleySmith00} [[Mark Hovey]], [[Brooke Shipley]], [[Jeff Smith]], example 6.2.3 of _Symmetric spectra_, J. Amer. Math. Soc. 13 (2000), 149-208 ([arXiv:math/9801077](http://arxiv.org/abs/math/9801077))

* {#Schlichtkrull09} [[Christian Schlichtkrull]], _Thom Spectra that Are Symmetric Spectra_, Documenta Mathematica 14 (2009) 699-748 ([arXiv:0811.0592](http://arxiv.org/abs/0811.0592))

* {#Schwede12} [[Stefan Schwede]], Example I.2.6 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))

As [[orthogonal spectra]] and as [[equivariant spectra]]

* {#Schwede15} [[Stefan Schwede]], chapter V.4 of _[[Global homotopy theory]]_, 2015

Textbook discussion with an eye towards the [[generalized (Eilenberg-Steenrod) cohomology]] of [[topological K-theory]] and [[cobordism cohomology theory]] is in 

* {#Rudyak98} [[Yuli Rudyak]], _On Thom spectra, orientability and cobordism_, Springer Monographs in Mathematics, 1998 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/rudyakthom.pdf))
 
See also 

* [[Frank Quinn]], _Assembly maps in bordism-type theories_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/quinnass.pdf))

A generalized notion of Thom spectra in terms of [[(∞,1)-module bundles]] is discussed in 

* {#ABGHR} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _Units of ring spectra and Thom spectra_ ([arXiv:0810.4535](http://arxiv.org/abs/0810.4535))
  
a streamlined update of which is

* {#ABGHR14} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], [[Michael Hopkins]], [[Charles Rezk]], _An $\infty$-categorical approach to $R$-line bundles, $R$-module Thom spectra, and twisted $R$-homology_ ([arXiv:1403.4325](http://arxiv.org/abs/1403.4325))


Discussion of Thom spectra from the point of view of [[(∞,1)-module bundles]] is in 

* {#ABG10} [[Matthew Ando]], [[Andrew Blumberg]], [[David Gepner]], _Twists of K-theory and TMF_, in Robert S. Doran, Greg Friedman, [[Jonathan Rosenberg]], _Superstrings, Geometry, Topology, and $C^*$-algebras_, Proceedings of Symposia in Pure Mathematics [vol 81](http://www.ams.org/bookstore-getitem/item=PSPUM-81), American Mathematical Society ([arXiv:1002.3004](http://arxiv.org/abs/1002.3004))
 

which is reviewed in

* {#Wilson13} [[Dylan Wilson]], _Thom spectra from the $\infty$ point of view_, 2013 ([pdf](http://www.math.northwestern.edu/~bwill/thom/DWthom4.pdf)) 
 

and in the context of [[motivic quantization]] via [[fiber integration in generalized cohomology|pushforward]] in [[twisted cohomology|twisted]] [[generalized cohomology]] in section 3.1 of 

* [[Joost Nuiten]], _[[schreiber:master thesis Nuiten|Cohomological quantization of local prequantum boundary field theory]]_, master thesis 2013

### As dual objects in the stable homotopy category

The relation of Thom spectra to [[dualizable objects]] in the [[stable homotopy category]] is originally due to ([Atiyah 61](#Atiyah61)) and

* {#DoldPuppe78} [[Albrecht Dold]], [[Dieter Puppe]], _Duality, trace, and transfer_. In Proceedings of the International Conference on Geometric Topology (Warsaw, 1978), pages 81&#8211;102, Warsaw, 1980.
PWN.
 

* [[L. Gaunce Lewis, Jr.]], [[Peter May]], M. Steinberger, and J. E. McClure, _Equivariant stable homotopy theory_, volume 1213 of Lecture Notes in Mathematics. Springer-Verlag, Berlin, 1986. With
contributions by J. E. McClure. 


A brief exposition appears as example 3.7 in 

* {#PontoShulman} [[Kate Ponto]], [[Mike Shulman]], _Traces in symmetric monoidal categories_ ([arXiv:1107.6032](http://arxiv.org/abs/1107.6032), [slides](http://www.sandiego.edu/~shulman/papers/ccrtraces.pdf)).
 


[[!redirects Thom spectra]]

[[!redirects generalized Thom spectrum]]
[[!redirects generalized Thom spectra]]