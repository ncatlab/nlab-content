
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea
 {#Idea}

Equivariant elliptic cohomology is, or is supposed to be, an [[equivariant cohomology|equivariant]] version of [[elliptic cohomology]], hence a higher [[chromatic homotopy theory|chromatic]] analogue of [[equivariant K-theory]].

As usual in [[equivariant cohomology]], there is a "naive" version and refinements thereof, and typically it is these refinements that one is really interested in. The traditional motivation of these from [[algebraic topology]]/[[homotopy theory]] are indicated below in

* _[Motivation from algebraic topology](#MotivationFromAlgebraicTopology)_

Despite that motivation, the precise nature of the resulting "genuine" equivariant elliptic cohomology may tend to seem a bit mysterious and also a bit baroque in its technical ingredients, some of which may appear a bit unexpected in the literature. A clear conceptual picture of what equivariant elliptic cohomology is about is obtained by regarding it as encoding aspects of low dimensional [[quantum field theory]] and [[worldsheet]] [[string theory]]; this is indicated further below in 


* _[Interpretation in Quantum field theory/String theory](#InterpretationInQuantumFieldTheory)_.

### Motivation from algebraic topology
 {#MotivationFromAlgebraicTopology}

Given any [[cohomology theory]] $E$ which may be evaluated on arbitrary [[topological spaces]], then for $G$ a [[compact Lie group]] the "naive" $G$-[[equivariant cohomology|equivariant E-cohomology]] of the point is the $E$-cohomology of the [[classifying space]] $B G$ of $G$ (which is equivalently the [[delooping]] 

$$
  B G \simeq \ast //G
$$

of $G$ regarded as an [[∞-group]], see at _[[∞-action]]_ for how that encodes actions on structures above it):

$$
  E_G^\bullet(\ast)_{naive} \coloneqq E^\bullet(B G)
  \,.
$$

In a discussion in the context of [[geometric homotopy theory]] it is clear what is "naive" about this definition: since $G$ has geometric structure of which $B G$ remembers only the underlying [[geometrically discrete infinity-groupoid|bare homotopy type]], one would instead want to use the something like the [[smooth stack]] $\mathbf{B}G$ (the [[moduli stack]] of $G$-[[principal bundle]]), then somehow make good sense of $\mathbf{E}^\bullet(\mathbf{B}G)$ where now $\mathbf{E}$ is some [[sheaf of spectra]] and then declare this to be the actual $G$-equivariant $E$-cohomology.

The traditional argument however proceeds as follows: if $E$ is a [[complex oriented cohomology theory]] then (essentially by definition) for $G = U(1)$ the [[circle group]] then  $E^\bullet(B U(1)) \simeq E^\bullet(\ast)[ [ c_1^E ] ]$  is the algebra of [[formal power series]] which one may think of as the [[algebra of functions]] on the [[formal geometry|formal]] [[neighbourhood]] of a point in some larger [[space]] $M_{S^1}$. 

For instance in the simpler case of [[equivariant K-theory]] this has long been well understood: here the genuine $U(1)$-equivariant cohomology of the point is the [[representation ring]] $K_{U(1)}(\ast) \simeq  \mathbb{Z}[ [ t^{-1}, t] ]$ which happens to be the [[algebra of functions]] on the [[multiplicative group]]; while by [[complex oriented cohomology theory|complex orientation]] the naive equivariant cohomology $K^\bullet(B U(1)) \simeq \mathbb{Z}[ [t] ]$ is equivalently the algebra of functions on (just) the formal multiplicative group.


Based on this one may want to consider an $E$-[[(∞,1)-module bundle|∞-line bundle]] over the full space $M_{S^1}$ and take the genuine $E$-equivariant cohomology to be the [[global sections]] of that. (Specifically in [[elliptic cohomology]] that space $M_{S^1}$ is equivalent to the [[elliptic curve]] $C$ that gives the theory its name, but in some sense discussed [below](#InterpretationInQuantumFieldTheory) the spaces $M_{S^1}$ and $C$ arise conceptually differently and it is a fairly deep coincidence that they are in fact equivalent, which one may want to remember.)

In this way equivariant elliptic cohomology was defined in ([Grojnowski 94](#Grojnowski94), [Ginzburg-Kapranov-Vasserot 95](#GinzburgKapranovVasserot95), ), see also ([Ando 00, sections II.8, II.9](#Ando00)). 

More generally then genuine $G$-equivariant elliptic cohomology should assign to every $G$-action on some [[space]] $X$ a sheaf $\mathcal{F}$ of algebras over the $G$-equivariant cohomology of the point, and then the $G$-equivariant elliptic cohomology of $X$ should be the global sections of this. 

While this can be made to work, it remains maybe unclear what these spaces $M_G$ "mean" and what makes them related to equivariance and elliptic cohomology. Specifically, $M_G$ turns out to be essentially the [[moduli space of flat connections]] ($G$-[[principal connections]]) on the given elliptic curve (see remark \ref{ModuliSpaceOfFlatConnections} below), which suggests strong relations to [[Chern-Weil theory]] that are not apparent here. That is considerably clarified by regarding elliptic cohomology as the [[coefficients]] for  [[motivic quantization|cohomological quantization]] of 3d and 2d [[quantum field theory]], to which we now turn.
 

### Interpretation in Quantum field theory/String theory
 {#InterpretationInQuantumFieldTheory}

We now try to give a maybe more conceptual explanation of what genuine equivariant (and [[twisted cohomology|twisted]]) elliptic cohomology is about, when regarded over all [[elliptic curves]] (hence: "genuine equivariant twisted [[tmf]]").


The conceptual role of plain [[elliptic cohomology]] (not equivariant) was considerably clarified when ([Witten 87](Witten+genus#Witten87)) identified the  [[elliptic genus]] (an element in the elliptic cohomology of a point) with the ([[large volume limit]] of) the [[partition function]] of a [[2d superconformal field theory]] -- the [[worldsheet]] [[quantum field theory]] of the "[[superstring]]" -- where the [[worldsheet]] [[Riemann surface]] of the string is identified with the given [[elliptic curve]].

If the [[superstring]] here is specifically the [[heterotic string]] then its dynamics and hence its [[partition function]] depends in general not just on the [[target space|target spacetime]] $X$ (of which it yields the [[elliptic genus]]) but also on a [[background field|background]] [[gauge field]] for some [[gauge group]] $G$, underlying which is a $G$-[[principal bundle]] over that spacetime. In ([Kefeng Liu, 95](Witten+genus#KL95)) a succinct description of these "twisted" elliptic genera, twisted by a $G$-principal bundle, was given in terms of [[Kac-Weyl characters]] of [[associated bundle|associated]] [[loop group]] bundles. In ([Distler-Sharpe 07](#DistlerSharpe07)) the chiral [[WZW-model]] part of the [[heterotic string]] [[2d SCFT]] which emobodies the effect of this background gauge bundle was realized geometrically as a bundle of [[parameterized WZW models]] over $X$, and ([Ando 07](#Ando07)) highlighted (see [Distler-Sharpe 07, section 8.5](#DistlerSharpe07)) that this provides the string theoretic interpretation of ([Kefeng Liu, 95](Witten+genus#KL95)), in particular ([Ando 07](#Ando07)) indicates that the corresponding twisted Witten genus lands in $G$-equivariant elliptic cohomology.

Now in the special case that $X$ here is the point, then any [[parameterized WZW model]] over $X$ is just the plain single [[WZW model]], while the plain [[Witten genus]] of $X$ vanishes. So in this case the interpretation of ([Ando 07](#Ando07)) says that the [[partition function]] of the $G$-[[WZW model]] should be an element in the $G$-equivariant elliptic cohomology of the point. But that partition function is an element in the space of [[conformal blocks]] of the WZW-model over a [[torus]] worldsheet, hence over a complex [[elliptic curve]]. Therefore the $G$-equivariant elliptic cohomology of the point should accommodate the [[conformal blocks]] of the WZW model over the given elliptic curve. (See also below at _[Properties -- Relation to conformal blocks](#RelationToConformalBlocks)_).

Next, by the [[holographic principle]] of the [[AdS3-CFT2 and CS-WZW correspondence|3dCS/2dWZW-correspondence]], the space of [[conformal blocks]] of the [[WZW model]] on a surface is identified with the [[space of quantum states]] of [[Chern-Simons theory]] over that surface. This in turn, by the general rules of [[geometric quantization]] and specifically by the discussion at _[[quantization of 3d Chern-Simons theory]]_, is the space of [[holomorphic sections]] of a [[prequantum line bundle]] over the [[moduli space of flat connections]] ($G$-[[principal connections]]) $M_G$ over the given elliptic curve. And _that_ is indeed what $G$-equivariant elliptic cohomology assigns to the point.

In other words, universal $G$-equivariant elliptic cohomology (meaning: we vary over the [[moduli space of elliptic curves]]), hence _$G$-equivariant [[tmf]]_ of the point, is essentially the [[modular functor]] of [[3d Chern-Simons theory]]. This last statement appears as ([Lurie 09, remark 5.2](#Lurie)). 

But observe that actually it is a bit more: a [[modular functor]] assigns just an abstract vector space to a surface, which however is meant to be obtained by the process of [[quantization]] of [[3d Chern-Simons theory]], explicitly as the space of holomorphic sections of the [[prequantum line bundle]] (over [[phase space]], which here is the [[moduli space of flat connections]] $M_G$ on the given elliptic curve). (Beware that, while this is true over the complex numbers, as discussed [here](moduli+space+of+connections#FlatConnectionsOverATorus), it is at least subtle in the algebro geometric context of elliptic cohomology, see Jacob Lurie's MO comment [here](http://mathoverflow.net/a/226716/381)). Equivariant elliptic cohomology/tmf actually remembers this [[quantization]] process and not just the resulting [[space of quantum states]] in that it actually assigns to an [[elliptic curve]] $C$ and suitable [[Lie group]] $G$ that [[prequantum line bundle]] over the [[moduli space of elliptic curves]] (or equivalently its [[sheaf]] of sections). Notice that this [[local prequantum field theory|pre-quantum]] information is crucial for deep aspects in the context of [[3d Chern-Simons theory]] and the 2d [[Wess-Zumino-Witten model]]: the [[holographic principle|holographic relation]] that identifies the latter as the [[boundary field theory]] of the former (explicitly so by the [[FRS-theorem on rational 2d CFT]]) needs as input not just the quantized Chern-Simons [[3d TQFT]], which will assign an "abstract" vector space to a surface, but needs to know how this space arose via [[quantization]] by choosing [[polarizations]] in the form of [[conformal structures]] on the elliptic curves, such as to be actually identified with a space of [[conformal blocks]]. (In the context of the [[Reshetikhin-Turaev construction]] of the Chern-Simons [[3d TQFT]] this information is in a choice of [[equivalence of categories|equivalence]] of the given [[modular tensor category]] with the [[category of representations]] of a rational [[vertex operator algebra]]).

In summary we have as a **slogan** that: 

* _$G$-Equivariant $tmf$ over the point is essentially an incarnation of the [[local prequantum field theory|pre-quantum]] [[modular functor]]_ of [[3d Chern-Simons theory|3d G-Chern-Simons theory]] over [[genus of a surface|genus]]-1 surfaces/[[elliptic curves]]_, together with the [[quantization]]-process of that to the actual [[modular functor]]_.


Moreover, by the above reasoning via ([Ando 07](#Ando07)) and using the [[AdS3-CFT2 and CS-WZW correspondence|3dCS/2dWZW holographic correspondence]] we also have the interpretation of $G$-equivariant tmf (universal $G$-equivariant elliptic cohomology) over a more general space $X$: the space of [[conformal blocks]] of a bundle of [[parameterized WZW models]] over $X$, regarded pointwise as the gauge coupling part of the twisted [[Witten genus]].

Here all the statements on the QFT/string theory side involve a parameter called the "level", which is the [[characteristic class]] of the [[universal Chern-Simons circle 3-bundle]] that is the [[prequantum n-bundle|prequantum 3-bundle]] governing the [[3d Chern-Simons theory]] (whose [[transgression]] to the [[moduli space of flat connections]] is the "theta"-[[prequantum line bundle]] there). On the cohomological side this corresponds to a [[twisted cohomology|twist]] of the cohomology theory.

Now with equivariant $tmf$ identified with the [[quantization of Chern-Simons theory]] in [[dimension]] 2 this way (the [[modular functor]] together with its pre-quantum origin via [[geometric quantization]]), the physical desireability of [[local quantum field theory]] ("[[extended TQFT]]") suggests to ask for a refinement of this also to dimensions 1 and 0, such that the higher dimensional data arises by "tracing"/[[transgression]]. There is such a [[local prequantum field theory]] refinement of 3d Chern-Simons theory, governed in dimension 0 by the [[universal Chern-Simons circle 3-bundle]] regarded as a [[prequantum n-bundle|prequantum 3-bundle]]. Indeed, the [[transgression]] of that to the [[moduli space of flat connections]] is precisely the [[prequantum bundle]] over $M_G$ that appears in the above discussion (e.g. [[schreiber:Extended higher cup-product Chern-Simons theories|FSS 12]], [[schreiber:A higher stacky perspective on Chern-Simons theory|FSS 13]]).

Now that [[universal Chern-Simons circle 3-bundle]] in turn is modulated by the geometric refinement of the universal [[second Chern class]]/[[first fractional Pontryagin class]] given by a map of [[smooth infinity-stacks]] of the form $\mathbf{B}G \to \mathbf{B}^3 U(1)$. This exhibits a homomorphism of [[smooth infinity-group]] $G \to \mathbf{B}^2 U(1)$ (to the [[circle n-group|circle 3-group]]) and so one might wonder if there is a way to "globalize" the equivariance of equivariant elliptic cohomology (in the sense of "[[global equivariant homotopy theory]]") such that it may be evaluated also on [[n-group|3-groups]] such as $\mathbf{B}^2 U(1)$ and such that the homomorphism above then _induces_ the previous 1-equivariant data by transgression.

Such a "localization" of equivariant elliptic cohomology seems to be just what is being vaguely hinted at in ([Lurie, section 5.1](#Lurie)) under the name "[2-equivariant elliptic cohomology](#2EquivariantEllipticCohomology)", we discuss this in more detail [below](#2EquivariantEllipticCohomology). 

Hence we arrive at a refinement of the above **slogan**: 

* _2-Equivariant $tmf$ over the point should be [[3d Chern-Simons theory]] in dimension 2 (hence the [[modular functor]]) [[extended TQFT|localized]] to dimensions 1 and 0 as a [[local prequantum field theory]] and including its [[higher geometric quantization]] in these dimensions 0,1, and 2_. 

> A formal systematic discussion of this story in [[schreiber:Quantization via Linear homotopy types|cohomological quantization]] is going to be in ([Nuiten-S.](#NS)). It essentially amounts to the discussion of diagram ([0.0.4 b)](#ESI14).

[[!include moduli of higher lines -- table]]



## Definition 

### 1-Equivariant elliptic cohomology

Let $G$ be a [[compact Lie group]]. Write $T \hookrightarrow G$ for its [[maximal torus]] and $W$ for its [[Weyl group]].

Let $E \in CRing_\infty$ be an [[elliptic spectrum|elliptic]] [[E-∞ ring]] [[spectrum]] with [[elliptic curve]] $A \to Spec E$. 

+-- {: .num_defn #TheModuliSpace}
###### Definition

Write 

$$
  A_G \coloneqq \left[\left[T,\mathbb{T}\right],A\right]/W
  \;\;
  \in Sch_{/Spec E}
$$

for the [[derived scheme]] formed from the [[character group]] of the [[maximal torus]] mapped into the given [[elliptic curve]].

=--

+-- {: .num_remark}
###### Remark

This $A_G$ is the [[moduli space|moduli scheme]] of [[stable bundle|semistable]] $G$-[[principal bundles]] over the dual elliptic curve $A^\vee$ ([Ginzburg-Kapranov-Vasserot 95, (1.4.5)](#GinzburgKapranovVasserot95)). 

=--

+-- {: .num_remark #ModuliSpaceOfFlatConnections}
###### Remark

For geometry over the [[complex numbers]] and  $A = \mathbb{C}/\tau$ a 2-[[torus]], the scheme $A_G$ is the [[moduli space of flat connections]] on $A$, by the discussion at _[moduli space of connections -- flat connections over a torus](moduli+space+of+connections#FlatConnectionsOverATorus)_.

=--


Wtite $L Top_G$ for the collection of [[G-CW complexes]].
Write $Orb(G)$ for the [[orbit category]] of $G$.

By [[Elmendorf's theorem]] we have a [[equivalence of (∞,1)-categories]]

$$
  L Top_G
  \stackrel{\simeq}{\longrightarrow}
  PSh_\infty(Orb(G))
  \,.
$$

Let the [[global points]] of the [[elliptic curve]] $A$ over $Spec E$ be equipped with an _orientation_ in the sense of a non-degenerate [[∞-group]] homomorphism of the form

$$
  B U(1) \longrightarrow A(Spec E)
$$


+-- {: .num_prop}
###### Proposition

Induced form this (...) is an [[essential geometric morphism]]

$$
  PSh_\infty(Orb(G))
  \stackrel{\overset{(-)\otimes_G A}{\longrightarrow}}{\stackrel{\overset{}{\leftarrow}}{\underset{}{\longrightarrow}}}
  Sh_\infty(Aff_E)_{/A_G}
$$

to the [[slice (∞,1)-topos]] over $A_G$. 

=--

([Gepner 05, theorem 3](#Gepner05))

+-- {: .num_defn}
###### Definition

Let 

$$

  \mathcal{O}
  \;\colon\;
  Sh_\infty(Aff_E)
  \longrightarrow
  Aff_E 
  \simeq
  E Alg^{op}
$$ 

be the [[left adjoint]] to the [[(∞,1)-Yoneda embedding]] as discussed at _[[function algebras on ∞-stacks]]_.

=--

+-- {: .num_prop}
###### Proposition

The composite

$$
  L Top_G
  \hookrightarrow
  PSh_\infty(Orb(G))
   \stackrel{(-)\otimes_G A}{\longrightarrow}
  Sh_\infty(Aff_E)_{/A_G}
  \stackrel{\mathcal{O}}{\longrightarrow}
  E Alg^{op}
$$

takes a space with $G$-[[action]] to its $G$-equivariant elliptic cohomology spectrum.

=--

([Gepner 05, theorem 4](#Gepner05))


### 2-Equivariant elliptic cohomology
 {#2EquivariantEllipticCohomology}

> under construction, tentative

In ([Lurie, section 5.1](#Lurie)) is a vague mentioning of a more general perspective, where one evaluates elliptic cohomology not just on [[action groupoids]] of a [[group]], such as $B G$ but also on [[homotopy quotients]] of [[2-groups]], such as notably the [[string 2-group]], and how that gives a more conceptual picture. 

The following are some remarks on how to possibly realize this and at the same time refine it to geometric cohomology ([[differential cohomology]]). Tentative. Handle with care.


So let $G$ be a simple, simply connected [[compact Lie group]].

Regard $\mathbf{B}G$ in [[Smooth∞Grpd]] = $Sh_\infty(SmthMfd)$. Then by the discussion at [[Lie group cohomology]] we have

$$
  \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}\mathbb{C}^\times)
  \simeq
  H(B G, K(\mathbb{Z},4))
  \simeq
  \mathbb{Z}
  \,.
$$

The [[∞-group extension]] classified by $k \in \mathbb{Z} \in \pi_0\mathbf{H}(\mathbf{B}G, \mathbf{B}\mathbb{C}^\times)$ is the [[string 2-group]] at level $k$

$$
  \array{
    \mathbf{B}\mathbb{C}^\times &\longrightarrow& \mathbf{B}String_k(G)
    \\
    && \downarrow
    \\
    && \mathbf{B}G &\stackrel{k\mathbf{c}}{\longrightarrow}& \mathbf{B}^3 \mathbb{C}^\times
  }
$$ 

This cocycle has a [[differential cohomology]]-refinement to the [[universal Chern-Simons 3-connection]]

$$
  k \mathbf{L} \;\colon\; \mathbf{B}G_{conn} \longrightarrow \mathbf{B}^3 \mathbb{C}^\times_{conn}
$$

Now given a [[torus]] $E = T^2$, regarded, for the moment, as a [[smooth manifold]], we have the [[transgression]] of the definition cocycle

$$
  \exp\left(
    \tfrac{i}{\hbar}
    \int_{E} k \mathbf{L}
  \right)
  \;\colon\;
  [E, \mathbf{B}G_{conn}]
   \stackrel{[E, k \mathbf{L}]}{\longrightarrow}
  [E, \mathbf{B}^3 \mathbb{C}^\times_{conn}]
   \stackrel{\exp\left(\tfrac{i}{\hbar} \int_{E}(-)\right)}{\longrightarrow}
  \mathbf{B}\mathbb{C}^\times_{conn}
$$ 

which now defines a $\mathbb{C}^\times$ [[bundle with connection]] on the [[moduli stack of connections]] on $E$.  We can restrict to the [[moduli stack of flat connections]], the [[phase space]] of $G$-[[Chern-Simons theory]]. This is the [[Hitchin connection]].

Consider then a collection of tori $E$ parameterized trivially over some parameter space $B$. 

$$
  E \times B \to B
  \,.
$$

Then the above yields

$$
  [(\Pi E) \times B, \mathbf{B}G]
   \stackrel{}{\longrightarrow}
  \mathbf{B}[B,\mathbb{C}^\times]
$$

hence yields a $[B,\mathbb{C}^\times]$-bundle over the [[moduli space]] of $B$-collections of flat connections on $E$.

Now we want to consider this for the case that $B$ is a space in [[spectral geometry]].

To that end, pass to the larger [[(∞,1)-topos]] of [[smooth E-∞ groupoids]] over the [[complex numbers]].

Let $\mathbb{G}_m$ there denote the object which to a pair consisting of a [[smooth manifold]] $U$ and an [[E-∞ ring]] $R$ assigns

$$
  \mathbb{G}_m \;\colon\; (U, R) \mapsto GL_1(R) \otimes C^\infty(U,\mathbb{C}^\times) 
$$ 

hence the [[tensor product]] of the [[∞-group of units]] of $R$ with the underlying [[abelian group]] of [[smooth functions]] on $X$ with values in $\mathbb{C}^\times$. 

Let then $A \in CAlg_\infty$ be an [[E-∞ ring]], and take now $B = Spec(A)$. Write 

$$
  E \to Spec(A)
$$

for a $B$-collection of [[tori]], now taken to be an [[elliptic curve]] over $Spec(A)$.

Since for a [[torus]] its [[fundamental group]] is [[isomorphic]] to its [[character group]] (via the canonical non-degenrarate [[bilinear form]] on both), we take the [[fundamental groupoid]] $\Pi(E)$ now to be

$$

  \mathbf{B}[E, \mathbb{G}_m]
  \,.
$$


Then since $\mathbb{C}^\times = \mathbb{G}_m$ is the [[multiplicative group]] in this context, we have now (and there is a subtlety here...) that maps 

$$
  Spec(A) \longrightarrow \mathbb{G}_m
$$

are equivalently elements in the [[∞-group of units]] of $A$. So we should get an $A$-[[(∞,1)-module bundle]] modulated by

$$
  \chi
   \colon
  [ \mathbf{B}[E,\mathbb{G}_m], \mathbf{B}G ]
  \longrightarrow
  \mathbf{B}GL_1(A)
  \,.
$$

Forming its space of co-sections yields, by the discussion at [[Thom spectrum]], the $\chi$-[[twisted cohomology|twisted]] A-[[cohomology]] [[spectrum]]

$$
  A^\chi([ \mathbf{B}[E,\mathbb{G}_m], \mathbf{B}G ])
  \,.
$$

And that should be the $G$-"equivariant" elliptic cohomology of the point. Actually the [[motivic quantization]] of $G$-[[Chern-Simons theory]].

(...)






## Properties
 {#Properties}

### Relation to conformal blocks of the WZW model
 {#RelationToConformalBlocks}


For $G$ a compact, simple and simply connected Lie group,
consider the [[string 2-group]] [[∞-group extension]]

$$
  \array{
    \mathbf{B}^2 U(1) &\to& \mathbf{B}String
    \\
    && \downarrow
    \\
    && \mathbf{B}G
  }
  \,.
$$

The corresponding [[higher moduli stacks]] of [[flat ∞-connections]] on an [[elliptic curve]] $T$ form the [[∞-group extension]]

$$
  \array{
    [\Pi(T),\mathbf{B}^2 U(1)] &\to& [\Pi(T),\mathbf{B}String]
    \\
    && \downarrow
    \\
    && [\Pi(T), \mathbf{B}G]
  }
  \,.
$$

Now passing to the [[0-truncation]] turns the bottom piece into the [[moduli space of flat connections]] on the torus, which is $A_G$, def. \ref{TheModuliSpace}, remark \ref{ModuliSpaceOfFlatConnections}.

By the discussion at [smooth higher holonomy](smooth+infinity-groupoid#StrucChernSimons) the 0-truncation of the top left piece is $U(1)$, so under 0-truncation we should get a $U(1)$-[[principal bundle]]

$$
  \array{
    U(1) &\longrightarrow& \tau_0 [\Pi(T),\mathbf{B}String]
    \\
    && \downarrow
    \\
    && A_G
  }
  \,.
$$

This state of affairs is hinted at in ([Lurie, section 5.1](#Lurie)).

More in detail, notice that the [[string 2-group]] extension is modulated by a map

$$
  \mathbf{c} \;\colon\; \mathbf{B}G_{conn} \longrightarrow \mathbf{B}^3 U(1)_{conn}
$$

and the above circle-bundle is modulated by the [[transgression]] of that 

$$
  \exp\left(
    \tfrac{i}{\hbar}
    \int_{T} \mathbf{c}
  \right)
  \;\colon\;
  [T, \mathbf{B}G_{conn}]
   \stackrel{[T,\mathbf{c}]}{\longrightarrow}
  [T, \mathbf{B}^3 U(1)_{conn}]
   \stackrel{\exp(\tfrac{i}{\hbar} (-) )}{\longrightarrow}
  \mathbf{B}U(1)_{conn}
  \,.
$$

(By the discussion at [[schreiber:differential cohomology in a cohesive topos|dcct]].)

By the general discussion at [[quantization of Chern-Simons theory]] and the [[holography|holograpic]] [[AdS3-CFT2 and CS-WZW correspondence|CS-WZW correspondence]], the space of [[sections]] of this line bundle is the space of [[conformal blocks]] of the [[Wess-Zumino-Witten model]] on $T$. 

(This statement also appears as ([Lurie, remark 5.2](#Lurie))). 


### Relation to loop group representations
 {#RelationToLoopGroupRepresentations}

When restricting the above general construction
to the [[Tate curve]], then the conformal blocks become
[[loop group representations]] (when over the complex numbers, at least, [Ando00, theorem 10.10](#Ando00)).

In terms of differential geometry ([[schreiber:differential cohomology in a cohesive topos|dcct]]) consider the map

$$
  G \longrightarrow [S^1, \mathbf{B}G_{conn}]
$$

which locally sends a group elemnent $g$ to the constant [[principal connection]] on the circle with $g$ as its [[holonomy]].

This induces an inclusion

$$
  [S^1, G]
    \hookrightarrow
  [S^1, [S^1, \mathbf{B}G_{conn}]]
    \simeq
  [T, \mathbf{B}G_{conn}]
$$ 

and pulling the above WZW circle bundle back along this inclusion
yields the bundle on the [[loop group]] which is the [[prequantum bundle]]
whose [[geometric quantization]] yields the [[loop group representations]]
of [[positive energy representations|positive energy]].

Algebraically, this corresponds to evaluating equivariant elliptic cohomology on the [[Tate curve]], this is ([Lurie, theorem 5.1](#Lurie)).

+-- {: .num_remark}
###### Remark

In the full [[derived algebraic geometry]] the space of sections of the line
bundle on the moduli space has the structure of a $K((q))$-[[∞-module]], hence of an actual [[spectrum]] ([Lurie, below remark 5.4](#Lurie)).

=--

(...)

### Relation to the Chern-Simons $\infty$-line bundle on $\mathbf{B}G$
 {#RelationToLineBundleOnBSpin}

Given an [[E-∞ ring]] $A$ with an oriented [[derived elliptic curve]] $\Sigma \to Spec(A)$ there are a priori two different $A$-[[∞-line bundles]] on $B Spin$.

On the one hand there is the bundle classified by

$$
  J_A
  \;\colon\;
  B Spin 
  \stackrel{}{\longrightarrow}
  B O
  \stackrel{J}{\longrightarrow}
  B GL_1(\mathbb{S})
  \longrightarrow
  B GL_1(A)
  \,,
$$

where $\mathbb{S}$ is the [[sphere spectrum]], $GL_1(-)$ the [[∞-group of units]]-construction and $J$ the [[J-homomorphism]].  (This is what appears as $\mathcal{A}_s$ in [Lurie, middle of p.38](#Lurie)). Notice that by ([Ando-Blumberg-Gepner 10, section 8](#AndoBlumbergGepner10)), for the case $A = $ [[tmf]] this is equivalently the $A$-[[∞-line bundle]] [[associated ∞-bundle|associated]] to the [[universal Chern-Simons line 3-bundle]]

$$
  A(\tfrac{1}{2}p_1)
  \;\colon\;
  B Spin
  \stackrel{\tfrac{1}{2}p_1}{\longrightarrow}
  B^4 \mathbb{Z}
  \stackrel{\tilde \sigma}{\longrightarrow}
  B GL_1(A)
  \,,
$$

where $\tfrac{1}{2}p_1$ is the [[first fractional Pontryagin class]] and $\tilde \sigma$ is an [[adjunct]] of the [[string orientation of tmf]].

In addition, by equivariant elliptic cohomology there is the [[theta line-bundle]]

$$
  \theta \;\colon\; Loc_{Spin}(\Sigma) \longrightarrow \mathbf{B} \mathbb{G}_m
$$

on the derived [[moduli stack of flat connections]] $Loc_{Spin}(\Sigma)$
(where in ([Lurie](#Lurie)) $Loc_{Spin}(\Sigma)$ is denoted $M_{Spin}$). Evaluating this bundle on [[global points]] yields the $A$-[[∞-line bundle]]

$$
  \Gamma_{Spec(A)}(\theta) \;\colon\; \Gamma_{Spec(A)}(Loc_{Spin}(\Sigma))
  \longrightarrow B GL_1(A)
  \,.
$$

So there are a priori two $A$-$\infty$-oine bundles on bare homotopy types here. But (by 2-equivariance, [Lurie, bottom of p. 38](#Lurie)) there is a canonical map between their base spaces

$$
   \phi \;\colon\; B Spin \longrightarrow \Gamma_{Spec(A)}(Loc_{Spin}(\Sigma))
  \,.
$$

Heuristically, this is the map that includes the trivial $Spin$-local system and its [[gauge transformations]] into the (points of the) [[moduli stack]] of all local systems.

Hence the pullback of $\Gamma_{Spec(A)}(Loc_{Spin}(\Sigma))$ yields another $A$-line bundle $\phi^\ast \Gamma_{Spec(A)}(\theta)$ over $B Spin$.

These are equivalent

$$
  J_A \simeq  \phi^\ast \Gamma_{Spec(A)}(\theta)
  \,.
$$

This is ([Lurie, theorem 5.2](#Lurie)).


$$
  \array{
    && Loc_{Spin}(\ast)
    \\
    & \swarrow && \searrow^{\mathrlap{\phi}}
    \\
    Loc_{Spin}(\ast)
    && 
     \swArrow_{\simeq}
    &&
    Loc_{Spin}(\Sigma)
    \\
    & {}_{\mathllap{J_A}}\searrow && \swarrow_{\mathrlap{\theta}}
    \\
    && B GL_1(A)
  }
$$


## Related concepts

* [[twisted ad-equivariant Tate K-theory]]

* [[equivariant elliptic genus]]

* [[rigidity theorem for elliptic genera]]

* [[orbifold cohomology]]

  * [[orbifold K-theory]]

* related but different: [[modular equivariant elliptic cohomology]]

* [[equivariant K-theory]]

* [[equivariant algebraic K-theory]]


## References


[[!include elliptic cohomology -- references]]


### Of quiver varieties

On [[equivariant elliptic cohomology]] of [[quiver varieties]] in relation to the [[AGT correspondence]]:

* [[Mina Aganagic]], [[Andrei Okounkov]], _Elliptic stable envelopes_ ([arXiv:1604.00423](https://arxiv.org/abs/1604.00423))

* [[Andrei Okounkov]], _Inductive construction of stable envelopes and applications, I. Actions of tori. Elliptic cohomology and K-theory_ ([arXiv:2007.09094](https://arxiv.org/abs/2007.09094))

following the analogous non-elliptic discussion in:

* [[Davesh Maulik]], [[Andrei Okounkov]], _Quantum Groups and Quantum Cohomology_, Asterisque 408(2019) ([arXiv:1211.1287](https://arxiv.org/abs/1211.1287), [ISBN: 978-2-85629-900-5](https://bookstore.ams.org/ast-408))

Review in:

* Andrey Smirnov, _Stable envelopes for $A_n$, $\widehat A_n$-quiver varieties_, 2019 ([pdf](https://math.mit.edu/events/quantum/a_smirnov.pdf))

[[!redirects equivariant elliptic cohomology theory]]
[[!redirects equivariant elliptic cohomology theories]]