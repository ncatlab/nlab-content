+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometric quantization
+-- {: .hide}
[[!include geometric quantization - contents]]
=--
#### Quantum field theory
+-- {: .hide}
[[!include functorial quantum field theory - contents]]
=--
#### Physics
+-- {: .hide}
[[!include physicscontents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The notion of _[[quantum field theory]]_ exists without reference to any predefined notion of _[[configuration space]]_ of _[[quantum fields]]_, _[[action functional]]_, _[[phase space]]_ etc.: 

A [[quantum field theory]] in [[FQFT]]-[[axiomatization]] is simply a consistent assignment of [[spaces of quantum states]], whereas in [[AQFT]]-[[axiomatization]] it is a consistent assignment of [[algebras of quantum observables]], and that's it. 

However, most (or maybe all?) quantum field theories of interest in actual [[physics]] (as opposed to as devices of pure [[mathematics]]) are not random models of these axioms, but do arise under a process called [[quantization]] from a ([[local Lagrangian|local]]/[[extended Lagrangian|extended]]) [[Lagrangian]], hence from an [[action functional]], defined on a [[configuration space]] of [[quantum fields]], or else arise as [[holographic duals]] of quantum field theories that arise by quantization. Moreover, the extra information provided by the Lagrangian is commonly used (and is maybe strictly necessary) to interpret the mathematical structure of the axiomatic QFT in actual [[physics]] (though notably in [[AQFT]] there are results that re-extract at least parts of this data from the axiomatic QFT, for instance the [[Doplicher-Roberts reconstruction theorem]] which extract the [[global gauge group]] from the [[local net of quantum observables]]).

There are in turn two formalizations of the notion of [[quantization]]: _algebraic [[deformation quantization]]_ and _[[geometric quantization]]_. In the latter one speaks of _[[prequantization]]_ when referring to a precursor step to the actual quantization step, in which the [[symplectic form]] on [[phase space]] is lifted to [[differential cohomology]], hence to a [[prequantum bundle]]. But in the context of [[higher geometry]] and [[higher geometric quantization]] this prequantization step is already part of the data of the [[Lagrangian]] itself: an [[extended Lagrangian]] already encodes not just the [[action functional]] but also the [[prequantum bundle]] and all the [[prequantum n-bundle|prequantum (n-k)-bundles]] in each [[dimension]] $k$. The action functional itself is the _[[prequantum 0-bundle]]_  in this context.

Therefore, in the refined picture of [[higher geometry]]/[[extended quantum field theory]] it makes good sense to refer in a unified way to **prequantum field theory** for all of the data related to [[Lagrangians]] that is not yet the final [[quantum field theory]]. 

In particular, an **extended prequantum field theory** of [[dimension]] $n$ is a rule that assigns

* to every (suitably [[orientation|oriented]]) [[closed manifold]] of [[dimension]] $k$ a [[prequantum n-bundle|prequantum (n-k)-bundle]]

* to every (suitably [[orientation|oriented]]) [[compact topological space|compact]] [[manifold with boundary]] $\Sigma_k$ a [[section]] of the prequantum $(n-k+1)$-bundle assigned to the [[boundary]] $\partial \Sigma_k$ and pulled back to the space of fields over $\Sigma_k$

such that this data is related suitably under [[transgression]].

The actual [[extended quantum field theory]] would be obtained from such a data by passing from the assignment of a given prequantum $(n-k)$-bundle to that of the [[n-vector space|(n-k)-vector space]] of [[polarization|polarized]] [[sections]] of a suitable [[associated infinity-bundle|associated]] [[fiber infinity-bundle|fiber bundle]].

This is summarized in the following table:

[[!include extended prequantum field theory - table]]

## Details

> under construction

We discuss local ("[[extended TQFT|extended]]") [[topological field theory|topological]] prequantum field theory. 

The following originates in the lecture notes ([Schreiber Pittsburgh13](#SchreiberPittLectures)) and draws on material that is discussed more fully in ([Fiorenza-Valentino](#FiorenzaValentino)) and ([hCSlpQFT](#hCSlpQFT)).

After a technical preliminary to set the stage in 

* _[The ambient topos](#TheTopos)_,

the first section gives the the definitions and general properties of 

* _[Local prequantum field theory](#LocalPrequantumFieldTheory)_.

To digest this the reader may first or in parallel want to look at the simplest examples of these general considerations, which we discuss below in the first subsections of

* _[Higher Dijkgraaf-Witten prequantum field theory](#HigherDijkgraafWittenLocalPrequantumFieldTheory)_.

After that we turn to the general case of examples of 

* _[Higher Chern-Simons prequantum field theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_.

### The ambient topos
 {#TheTopos}

Prequantum field theory deals with "spaces of [[field (physics)|physical fields]]". These spaces of [[field (physics)|fields]] are, in general, richer than just plain [[sets]] in two ways

1. Spaces of [[field (physics)|fields]] carry [[geometry|geometric]] structure, notably they may be [[smooth spaces]], meaning that there is a way to determine which collections of [[field (physics)|fields]] form a smoothly parameterized collection. This is for instance the structure invoked (often implicitly) when performing [[variational calculus]] on spaces of [[field (physics)|fields]] in order to find their classical [[equations of motion]]. 

1. Spaces of fields have [[gauge transformations]] between their points and possibly [[higher gauge transformations]] between these, meaning that they are in fact [[groupoids]] and possibly [[infinity-groupoid|higher groupoids]]. In the physics literature this is best known in the [[infinitesimal object|infinitesimal]] approximation to these gauge transformations, in which case the spaces of fields are described by [[BRST complexes]]: the dg-algebras of functions on a [[Lie algebroid]] or [[L-∞ algebroid]] of fields.

Taken together this means that spaces of fields are _[[(∞,1)-sheaf|geometric higher groupoids]]_, such as [[orbifolds]] and more generally [[Lie groupoids]], [[differentiable stacks]], [[Lie 2-groupoids]], ... [[smooth ∞-groupoids]].

A collection of all such geometric higher groupoids for a chosen flavor of [[geometry]] -- for instance [[topology]] or [[differential geometry]] or  [[supergeometry]] (for the description of [[fermion]] fields) or [[synthetic differential geometry]] or [[synthetic differential supergeometry]], etc. -- is called an _[[∞-topos]]_. 

Not quite every [[∞-topos]] $\mathbf{H}$ serves as a decent context for collections (moduli stacks) of [[physical fields]] though. In the following we need at least that $\mathbf{H}$ has a reasonable notion of _[[discrete objects]]_ so that we can identify the geometrically discrete spaces in there. We here need this to mean the following

+-- {: .num_defn #ShapeAndFlatModality}
###### Definition

An [[∞-topos]] $\mathbf{H}$ is called _[[locally ∞-connected (∞,1)-topos|locally ∞-connected]]_ and _[[globally ∞-connected (∞,1)-topos|globally ∞-connetced]]_ if the [[locally constant ∞-stack]]-functor $LConst \colon $ [[∞Grpd]] $\to \mathbf{H}$ is a [[reflective sub-(∞,1)-category|reflective embedding]]. 

The corresponding reflector we write

$$
  \Pi \colon \mathbf{H} \to \infty Grpd \hookrightarrow \mathbf{H}
$$

and also call the _[[shape modality]]_ of $\mathbf{H}$. By the discussion at [[adjoint triple]] it follows that $LConst$ is also a [[coreflective subcategory|coreflective]] embedding; the corresponding coreflector we write 

$$
  \flat \colon \mathbf{H} \stackrel{\Gamma}{\to} \infty Grpd \hookrightarrow \mathbf{H}
$$

and call the _[[flat modality]]_.

=--

+-- {: .num_example}
###### Example

Every [[cohesive (∞,1)-topos]] is in particular globally and locally $\infty$-connected, by definition. Standard canonical examples to keep in mind are

* $\mathbf{H} = $ [[∞Grpd]] for [[∞-Dijkgraaf-Witten theories]];

* $\mathbf{H} = $ [[Smooth∞Grpd]] for [[schreiber:∞-Chern-Simons theories]];

* $\mathbf{H} = $ [[SuperSmooth∞Grpd]] for [[schreiber:∞-Chern-Simons theories]] with [[fermions]] and [[supersymmetry]];

* $\mathbf{H} = $ [[SynthDiff∞Grpd]] for [[AKSZ sigma-models]].

=--


### Local prequantum field theory
 {#LocalPrequantumFieldTheory}

After sketching out the general 

* _[Idea](#PrequantumFieldTheoryIdea)_

we formulate first 

* _[Bulk field theory](#BulkFieldTheory)_,

which concerns the case where the [[worldvolume]]/[[spacetime]] on which the [[field (physics)|physical fields]] propagate has no [[boundaries]] with [[boundary conditions]] imposed (no "[[branes]]" or "[[domain walls]]" or "[[QFT with defects|defects]]"). The point of this section is to see how the "space of fields" -- or rather: the [[moduli stack]] of fields -- on a point induces the corresponding spaces/moduli stacks of fields on an arbitrary [[closed manifold]], and, correspondingly, how the [[prequantum n-bundle]] on the space over fields over the point induces the [[action functional]] in [[codimension]] 0.

However, what makes local prequantum field theory rich is that it naturally incorporates extra structure on [[boundaries]] of [[worldvolume]]/[[spacetime]]. In fact, under suitable conditions there is another local prequantum field theory just over the boundary, which is related to the corresponding bulk field theory possibly by a kind of [[holographic principle]]. This general mechanism we discuss in 

* _[Boundary field theory](#BoundaryFieldTheory)_.

But plain boundaries are just the first example of a general phenomenon known as "[[QFT with defects|defects]]" or "phase dualities" or "singularities" in field theories. Notably the boundary field theory itself may have boundaries, in which case this means that the original theory had _[[manifold with corners|corners]]_ where different boundary pieces meet. This we discuss in 

* _[Corner field theory](#CornerFieldTheory)_.

Generally there are fields theories with general such singularties:

[[!include field theory with boundaries and defects - table]]


#### Idea
 {#PrequantumFieldTheoryIdea}

A _prequantum field theory_ is, at its heart, an assignment that sends a piece of [[worldvolume]]/[[spacetime]] $\Sigma$ -- technically a [[cobordism]] with [[boundary]] and [[corners]] -- to the 

1. [[space]] of [[physical field|field configurations]] over incoming and outgoing pieces of worldvolume/spacetime;

1. the space of field configurations over the bulk worldvolume/spacetime -- the [[trajectories]] of fields;

1. an [[action functional]] that assigns to all these field configurations [[phases]] in a compatible manner. 

These field configurations and spaces of [[trajectories]] between them are represented by [[spans]]/[[correspondences]] of ([[moduli space|moduli]]-)spaces of fields ([[moduli stacks]], really), hence [[diagrams]] of the form

$$
  \mathbf{Fields}_{in}
  \leftarrow
  \mathbf{Fields}
  \rightarrow
  \mathbf{Fields}_{out}
  \,.
$$

Here $\mathbf{Fields}_{in}$ is to be thought of as the space of incoming fields, $\mathbf{Fields}_{out}$ that of outgoing fields, and $\mathbf{Fields}$ the space of all fields on some [[cobordism]] connecting the incoming and the outgoing pieces of [[worldvolume]]/[[spacetime]]. The left map sends such a trajectory to its starting configuration, and the right one sends it to its end configuration.

Given two such spans/correspondences, that share a common field configuration as in 

$$
  \array{
    && \mathbf{Fields}_1 && && \mathbf{Fields}_2
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \mathbf{Fields}_{in_1}
    && &&
    \mathbf{Fields}_{out_1} = \mathbf{Fields}_{in_2}
    && &&
    \mathbf{Fields}_{out_2}
  }
$$ 

can be [[composition|composed]], by forming consecutive trajectories from all pairs of trajectories that match in the middle. The space of these composed trajectories is the [[fiber product]] 
$\mathbf{Fields}_1 \underset{{\mathbf{Fields}_{out_1}} \atop {=\mathbf{Fields}_{in_2}}}{\times} \mathbf{Fields}_2$ which sits in a new [[span]]/[[correspondence]]

$$
  \mathbf{Fields}_{in_1}
  \leftarrow
  \mathbf{Fields}_1 \underset{{\mathbf{Fields}_{out_1}} \atop {=\mathbf{Fields}_{in_2}}}{\times} \mathbf{Fields}_2
  \rightarrow
  \mathbf{Fields}_{out_2}
$$

exhibiting the composite of the previous two. This way, spaces of fields with spans/correspondences between them form a [[category]], which we denote $Span_1(\mathbf{H})$ if $\mathbf{H}$ denotes the ambient context (a [[topos]]) in which the spaces of fields live. 

If two cobordisms run in parallel, then the field configurations on their union are pairs of the original field configurations, which are elements in the [[cartesian product]] of spaces of fields. Hence the operations

$$
  \left(
  \mathbf{Fields}_{in}
  \leftarrow
  \mathbf{Fields}
  \rightarrow
  \mathbf{Fields}_{out}
  \right)
  \otimes
  \left(
  \tilde \mathbf{Fields}_{in}
  \leftarrow
  \tilde \mathbf{Fields}
  \rightarrow
  \tilde\mathbf{Fields}_{out}
  \right)  
  \;\;\coloneqq\;\;
  \left(
    \mathbf{Fields}_{in} \times \tilde\mathbf{Fields}_{in}
    \leftarrow
    \mathbf{Fields} \times \tilde\mathbf{Fields}
    \to
    \mathbf{Fields}_{out} \times \tilde\mathbf{Fields}_{out}    
  \right)
$$

make this category of fields and correspondence into a [[monoidal category]]. 

Then a choice of field configurations for a (not yet localized) field theory in dimension $n \in \mathbb{N}$ is a [[monoidal functor]] from a [[category of cobordisms]] of dimension $n$ to such a category of [[spans]]/[[correspondences]]

$$
  \mathbf{Fields} \colon Bord_n^\otimes \to Span_1(\mathbf{H})^\otimes
  \,,
$$

namely a consistent assignment that to each [[closed manifold]] $\Sigma_{n-1}$ of dimension $(n-1)$ assigns a space of field configurations $\mathbf{Fields}(\Sigma_{n-1})$ and that to each [[cobordism]]

$$
  \Sigma_{in} \to \Sigma \leftarrow \Sigma_{out}
$$

assigns a [[span]]/[[correspondence]] of spaces of field configurations and trajectories

$$
  \mathbf{Fields}(\Sigma_{in})
  \leftarrow
  \mathbf{Fields}(\Sigma)
  \rightarrow
  \mathbf{Fields}_{\Sigma_{out}}
  \,.
$$

Apart from the field configurations themselves, prequantum field theory assigns to each [[trajectory]] a "[[phase]]" -- an element in the [[circle group]] $U(1)$ -- by a map called the (exponentiated) [[action functional]]. In order to nicely relate that to the expression of spaces of trajectories as [[spans]]/[[correspondences]] as above, it is useful to think of the [[circle group]] here as being the [[automorphisms]] of something. This is universally accomplished by taking it to be the automorphisms of the unique point in the [[delooping]] [[groupoid]] $\mathbf{B}U(1) = \{\ast \stackrel{c \in U(1)}{\to} \ast\}$. (A lightning review of [[groupoid]]-[[homotopy theory]] is below in [Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory).) In other words, we think of the group of phases $U(1)$ as the space of [[homotopies]] from the point to itself in the [[Eilenberg-MacLane space]] $\mathbf{B}U(1)$, expressed by the [[diagram]] (a [[homotopy fiber product]] diagram)

$$
  \array{
    && U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast 
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$

Using this, if we assume for simplicity that the in- and outgoing field configurations are sent constantly to the point in $\mathbf{B}U(1)$, then an (exponentiated) [[action functional]] on the space of trajectories $\exp(i S) \colon \mathbf{Fields} \to U(1)$ is equivalently a [[homotopy]] as shown on the left of the following diagram

$$
  \array{
    && \mathbf{Fields}
    \\
    & \swarrow && \searrow
    \\
    \mathbf{Fields}_{in}
    && \swArrow &&
    \mathbf{Fields}_{out}
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{0}}
    \\
    && \mathbf{B}U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && \mathbf{Fields}
    \\
    && \downarrow^{\mathrlap{\exp(i S)}}
    \\
    && U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}U(1)
  }
  \,.
$$

Hence action functionals are naturally incorporated into [[spans]]/[[correspondences]] of [[moduli spaces]] of fields simply by regarding these to be formed not in the ambient [[topos]] $\mathbf{H}$ itself, but in its [[slice topos]] $\mathbf{H}_{/\mathbf{B}U(1)}$, where each object is equipped with a map to $\mathbf{B}U(1)$ and each morphism with a [[homotopy]] in $\mathbf{B}U(1)$ between the corresponding maps.

We write $\mathrm{Span}_1(\mathbf{H}, \mathbf{B}U(1))$ for the category of spans/correspondences as before, but now equipped with maps to, and transformations over, $\mathbf{B}U(1)$ as in the above diagram. 

Then an [[action functional]] for a choice of field configurations that itself is given as a [[monoidal functor]] $\mathbf{Fields} \colon Bord_n^\otimes \to Span_1(\mathbf{H})$ as above is a monoidal functor

$$
  S \colon Bord_n^\otimes \to Span_1(\mathbf{H}, \mathbf{B}U(1))
$$

such that the spans of spaces of fields are those specified before, hence such that it fits as a lift into the diagram

$$
  \array{
     && Span_1(\mathbf{H}, \mathbf{B}U(1))
     \\
     & {}^{\mathllap{S}}\nearrow & \downarrow 
     \\
     Bord_n &\underset{\mathbf{Fields}}{\to}& Span_1(\mathbf{H})
  }
  \,,
$$

where the right vertical functor [[forgetful functor|forgets]] the phase assignments and just remembers the correspondences of field trajectories.


So far this is a non-local (or: not-necessarily local) prequantum field theory, since it assigns data only to entire $n$-dimensional cobordisms and $(n-1)$-dimensional [[closed manifolds]], but is not guaranteed to be obtained by integrating up local data over little pieces of these manifolds. The latter possibility is however the characteristic property of [[local quantum field theory]], which in turn is the flavor of quantum field theory that seems to matter in nature, and fundamentally.

In order to formalize this localization, we allow the cobordisms to contain higher-[[codimension]] pieces that are [[manifolds with corners]]. These then form not just a [[category of cobordisms]], but an [[(∞,n)-category]] of cobordisms, which we will still denote $Bord_n^\otimes$. If we now have a cobordism with [[codimension]]-2 [[corners]], then the field configurations over it now form a span-of-spans

$$
  \array{
    \mathbf{Fields}_{ii} &\leftarrow& \mathbf{Fields}_{ic} &\to& \mathbf{Fields}_{io}
    \\
    \uparrow && \uparrow && \uparrow
    \\
    \mathbf{Fields}_{ci} &\leftarrow& \mathbf{Fields}_{cc} &\to& \mathbf{Fields}_{co}
    \\
    \downarrow && \downarrow && \downarrow
    \\
    \mathbf{Fields}_{oi} &\leftarrow& \mathbf{Fields}_{oc} &\to& \mathbf{Fields}_{oo}
  }
  \,.
$$

Generally, for $n$-dimensional cobordism that are "localized" all the way to [[corners]] in codimension $n$, their field configurations and trajectories-of-trajectories etc. form $n$-dimensional cubes of spans-of-spans this way. We write $Span_n(\mathbf{H})$ for the resulting [[(∞,n)-category of spans]].

In order to still have an [[action functional]] on trajectories is [[codimension]]-0 associated with this in the above fashion, we need to [[delooping|deloop]] $U(1)$ $n$-times to the [[n-groupoid]] $\mathbf{B}^n U(1)$ (the [[circle n-group|circle (n+1)-group]]). Accordingly a local prequantum field theory in dimension $n$ is given by a [[monoidal (∞,n)-functor]]

$$
  S \colon Bord_n^\otimes \to Span_n(\mathbf{H}, \mathbf{B}^n U(1))
  \,.
$$

The point of local topological (prequantum) field theory is that by the [[cobordism theorem]] the above story reverses: the assignment of fields and their action functional in higher dimension is necessarily given by [[higher traces]] of the data assigned in lower dimension. Hence the whole assignment $S$ above is fixed by its value on the point, hence by a choice of one single map

$$
  \left[
    \array{
      \mathbf{Fields}(\ast)
      \\
      \downarrow^\mathrlap{S}
      \\
      \mathbf{B}U(1)
    }
  \right]
  \,,
$$

the fully localized action functional. Or rather, this is the case for pure bulk field theory, with no [[branes]] or [[domain walls]]. If these are present, then each type of them in dimension $k$ is specified by a [[k-morphism]] in $Span_n(\mathbf{H}, \mathbf{B}^n U(1))$.

All this we now describe more formally.

#### Bulk field theory
 {#BulkFieldTheory}

We now first consider the formalization of prequantum field theory
in the absence of any data such as [[boundary conditions]], [[domain walls]], [[branes]], [[QFT with defects|defects]], etc. This describes either field theories in which no such phenomena are taken to be present, or else it describes that part of those field theories where such phenomena are present in principle, but restricted to the "[[bulk]]" of [[worldvolume]]/[[spacetime]] where they are not. Therefore it makes sense to speak of _bulk field theory_ in this case.

+-- {: .num_defn #nCategoryOfCobordisms}
###### Definition

For $n \in \mathbb{N}$, write

$$
  Bord_n^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the [[symmetric monoidal (∞,n)-category]] [[(∞,n)-category of cobordisms|of cobordisms]] with $n$-dimensional [[framed manifold|framing]]. For $S \to O(n)$ a homomorphism of [[∞-groups]] (may be modeled by a homomorphism of [[topological groups]]) to the [[general linear group]] (or homotopy-equivalently its [[maximal compact subgroup]], the [[orthogonal group]]), we write 

$$
  (Bord_n^S)^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the corresponding symmetric monoidal $(\infty,n)$-category of cobordisms equipped with [[G-structure|S-structure]] on their $n$-stabilized [[tangent bundle]]. 

=--

+-- {: .num_remark}
###### Remark

In this notation we have an identification

$$
  Bord_n \simeq Bord_n^{S \coloneqq \ast}
$$

because a [[framing]] of the $n$-stabilized tangent bundle is a trivialization of that bundle and hence equivalently a [[G-structure]] for $G$ the trivial group. In ([LurieTFT](#LurieTFT)) this is denoted by "$Bord_n^{fr}$".

=--

+-- {: .num_remark}
###### Remark

The [[cobordism theorem]] asserts, essentially, that $Bord_n$ is the [[symmetric monoidal (∞,n)-category]] with [[fully dualizable objects|full duals]] which is [[free construction|free]] on a single generator, the point. In itself this is a deep statement about the [[homotopy type]] of [[categories of cobordisms]]. But for the following discussion the reader may just take this as the _definition_ of $Bord_n$. This then makes $Bord_n$ a very simple object, as long as we are just mapping out of it, which we do.

What this means then is that a [[monoidal (∞,n)-functor]] 

$$
  Z \colon Bord_n^\otimes \to \mathcal{C}^\otimes
$$

sends the point to some [[fully dualizable object]] $Z(\ast) \in \mathcal{C}$ and sends

* the [[circle]] $S^1$ to the [[trace]] of the identity on $Z(\ast)$, 

* the [[sphere]] $S^2$ to the 2-dimensional [[higher trace]] of the identity,

and so on.


=--

+-- {: .num_defn #CorrespondencesInInfinityTopos}
###### Definition

For $\mathbf{H}$ an [[∞-topos]], and $n \in \mathbb{N}$, write 

$$
  Span_n(\mathbf{H}) \in Cat_{(\infty,n)}
$$

for the [[(∞,n)-category of spans]] in $\mathbf{H}$. From the [[cartesian monoidal category]] structure of $\mathbf{H}$ this inherits the structure of a [[symmetric monoidal (∞,n)-category]] which we write 

$$
  Span_n(\mathbf{H})^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
  \,.
$$

=--

+-- {: .num_prop #FullSelfDualizabilityInSpan}
###### Proposition

Every object in $Span_n(\mathbf{H})$ is a self-[[fully dualizable object]]. The [[evaluation map]]/[[coevaluation map]] $k$-spans in dimension $k$ involve in top degree the spans

$$
  \ast \leftarrow X \stackrel{}{\to} [\Pi(S^k), X]
  \,.
$$

(...)

=--

+-- {: .num_defn #CorrespondencesOverB}
###### Definition

For $B \in Grp(\mathbf{H})$ an [[abelian ∞-group]] object in $\mathbf{H}$, spans in the [[slice (∞,1)-topos]]  $\mathbf{H}_{/B}$ inherits a monoidal structure given on objects by

$$  
  \otimes
    \;
    \colon
    \;
  \left[
    \array{
      X \\ \downarrow^{\mathrlap{f}} \\ B
    }
  \right]
  \times 
  \left[
    \array{
      Y \\ \downarrow^{\mathrlap{g}} \\ B
    }
  \right]
  \mapsto
  \left[
    \array{
      X \times Y \\ \downarrow^{\mathrlap{f \circ p_1 + g \circ p_2}}
     \\
     B
    }
    \;\;\;\;\;\;\;\;\;\;
  \right]
  \,.
$$

We write

$$
  Span_n(\mathbf{H}, B)^\otimes \in E_\infty Alg(Cat_{(\infty,n)})
$$

for the resulting [[symmetric monoidal (∞,n)-category]].

=--

+-- {: .num_remark}
###### Remark

In the case that $\mathbf{H} = $ [[∞Grpd]] this is a special case of ([LurieTFT, around prop. 3.2.8](#LurieTFT)), with the [[abelian ∞-group]] $B$ regarded as a special case of a [[symmetric monoidal (∞,1)-category]]. 

=--

+-- {: .num_remark}
###### Remark

Since the [[slice (∞,1)-category]] $\mathbf{H}_{/\flat \mathbf{B}^n U(1)}$ is itself an [[(∞,1)-topos]] -- the [[slice (∞,1)-topos]] -- we also have $Span_n(\mathbf{H}_{/\flat \mathbf{B}^n U(1)})$, according to def. \ref{CorrespondencesInInfinityTopos}. As an [[(∞,n)-category]] this is equivalent to $Span_n(\mathbf{H}, \flat \mathbf{B}^n U(1))$ from def. \ref{CorrespondencesOverB}, but the [[monoidal (∞,n)-category|monoidal structure]] is different. The [[cartesian product]] in the slice is given by [[homotopy fiber product]] in $\mathbf{H}$ over $\flat \mathbf{B}^n U(1)$, not by the addition in the [[∞-group]] structure on $\flat \mathbf{B}^n U(1)$, as in def. \ref{CorrespondencesOverB}.

=--

The central definition in the present context now is the following.

+-- {: .num_defn #LocalPrequantumFieldWithAction}
###### Definition

A **local prequantum bulk [[field (physics)|field]]** in [[dimension]] $n \in \mathbb{N}$ (in a given ambient [[cohesive (∞,1)-topos]] $\mathbf{H}$) is a [[monoidal (∞,n)-functor]]

$$
  \mathbf{Fields} \;\colon\; Bord^S_n \to Span_n(\mathbf{H})
$$

from the [[(∞,n)-category of cobordisms]] (with [[G-structure|S-structure]]), def. \ref{nCategoryOfCobordisms}, to the [[(∞,n)-category of n-fold correspondences]] in $\mathbf{H}$.

A **local action functional** on such a local prequantum bulk [[field (physics)|field]] is a monoidal lift $S$ of this in 

$$
  \array{
     && Span_n(\mathbf{H}, \flat \mathbf{B}^n U(1))
     \\
     & {}^{\mathllap{S}}\nearrow & \downarrow^{\mathrlap{Span_n\left(\underset{\flat \mathbf{B}^n U(1)}{\sum}\right)}}
     \\
     Bord_n^S 
     &\underset{\mathbf{Fields}}{\to}&
     Span_n(\mathbf{H})
  }
  \,.
$$

=--

For $\mathbf{H} = $ [[∞Grpd]] this is the perspective in ([FHLT, section 3](#FHLT)).

+-- {: .num_remark}
###### Remark

Since a monoidal $(\infty,n)$-functor $\mathbf{Fields} \colon Bord_n \to Span_n(\mathbf{H})$ is determined by its value on the point, we will often notationally identify it with this value and write

$$
  \mathbf{Fields} = \mathbf{Fields}(\ast) \in \mathbf{H} \hookrightarrow Span_n(\mathbf{H})
  \,.
$$



=--

As a corollary of prop. \ref{FullSelfDualizabilityInSpan} we have:

+-- {: .num_prop}
###### Proposition

Given $\mathbf{Fields} \colon Bord_n^\otimes \to Span_n(\mathbf{H})^\otimes$, it assigns to a [[k-morphism]] represented by a [[closed manifold]] $\Sigma_k$ the [[internal hom]] ([[mapping stack]]) from  $\Pi(\Sigma_k)$ (the [[shape modality]] of $\Sigma_k$, def. \ref{ShapeAndFlatModality}) into the moduli stack of fields

$$
  \mathbf{Fields}
  \colon
  \Sigma_k
  \mapsto
  [\Pi(\Sigma_k), \mathbf{Fields}]
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

By the defining property of the [[mapping stack]] construction, this means that if $\mathcal{C}$ is an [[(∞,1)-site]] of definition of the [[(∞,1)-topos]] $\mathbf{H}$, then $[\Pi(\Sigma_k), \mathbf{Fields}]$ is the [[∞-stack]] which to $U \in \mathcal{C}$ assigns the [[(∞,1)-categorical hom space]]

$$
  [\Pi(\Sigma_k), \mathbf{Fields}](U) \simeq
  \mathbf{H}(\Pi(\Sigma_k)\times U , \mathbf{Fields})
  \,,
$$

hence the [[∞-groupoid]] of fields on $\Pi(\Sigma_k) \times U$. 

If $\mathbf{Fields}$ is a [[moduli ∞-stack]] of [[gauge fields]] for some [[smooth ∞-group]] $G$, hence of the form $\mathbf{B}G_{conn}$, then this an $\infty$-groupoid of a kind of smoothly (or else geometrically) $U$-parameterized collections of [[flat ∞-connections]] on $\Sigma_k$.

=--

(...)

#### Boundary field theory
 {#BoundaryFieldTheory}

(...)

#### Corner field theory
 {#CornerFieldTheory}

(...)


### Higher Dijkgraaf-Witten local prequantum field theory
 {#HigherDijkgraafWittenLocalPrequantumFieldTheory}

We discuss here aspects of higher [[Dijkgraaf-Witten theory]]-type 
prequantum field theories, which are those prequantum field theories 
whose moduli stack $\mathbf{Fields}$ is a [[discrete ∞-groupoid]] 
(and usually also required to be finite, especially if its [[quantization]] is considered).
This is a special case of the higher Chern-Simons theories discussed below in _[Higher Chern-Simons local prequantum field theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_, and hence strictly speaking need not be discussed separately. We use it here as a means to review some of the relevant [[homotopy theory]] by way of pertinent examples.

The original [[Dijkgraaf-Witten theory]] is that in dimension 3 (reviewed in _[3d Local prequantum field theory](#3dDWLocalPrequantumFieldTheory)_ below), which was introduced in 
([Dijkgraaf-Witten 90](Dijkgraaf-Witten+theory#DijkgraafWitten90)) as a toy version of standard 3d [[Chern-Simons theory]] for [[simply connected topological space|simply connected]] [[gauge group]]. A comprehensive account with first indications of its role as a local (extended, multi-tiered) field theory
then appeared in 
([Freed-Quinn 93](Dijkgraaf-Witten+theory#FreedQuinn93)), and ever since this has served as a testing ground for understanding the general principles of local field theory, e.g. 
([Freed 94](Dijkgraaf-Witten+theory#Freed94)), 
independently of the subtleties of giving meaning to concepts such as the path integral when the space of fields is not finite.
In section 3 of ([FHLT 10](#FHLT)), the general prequantum formalization as in  def. \ref{LocalPrequantumFieldWithAction} is sketched for Dijkgraaf-Witten type theories, 
and in section 8 there the quantization of these
theories to genuine local quantum field theories is sketched.



#### 1d Dijkgraaf-Witten theory
 {#1dDWTheory}

[[Dijkgraaf-Witten theory]] in [[dimension]] 1 is what results when one regards a [[group character]] of a [[finite group]] $G$ as a local 
[[action functional]] in 
the sense of def. \ref{LocalPrequantumFieldWithAction}.
We give now an expository discussion of this simple but instructive example of a local prequantum field theory and in the course of it
introduce some of the relevant basics of the [[homotopy theory]] of [[groupoids]] ([[homotopy 1-types]]).

1. [Finite gauge groups](#FiniteGaugeGroups)

1. [Groupoids and basic homotopy 1-type theory](#GroupoidsAndBasicHomotopy1TypeTheory) 

1. [Correspondences of groupoids](#CorrespondencesOfGroupoids)

1. [1d DW local field theory](#1dDWLocalFieldTheory)

The punchline of this section is little theorem \ref{GroupCharacterPrequantumTheoryOnCircle} at the very end, which states that the 1d local prequantum field theory whose local action functional is the delooping of a [[group character]] assigns to the circle the [[action functional]] which is again that group character. The proof of this statement is an unwinding of the basic mechanisms of local prequantum field theories.


##### Finite gauge groups
 {#FiniteGaugeGroups} 

First some brief remarks, before we dive into the formalism.

A [[group character]] on a [[finite group]] $G$ is just a [[group]] [[homomorphism]] $G \to U(1)$ to the [[circle group]] (taken here as a [[discrete group]]).
In order to regard this as an [[action functional]], 
we are to take $G$ as the 
[[gauge group]] of a physical field theory. The simplest
such case is a field theory such that on the point there is 
just a single possible field configuration, to be denoted $\phi_0$.
The reader familiar with basics of traditional [[gauge theory]] may think of the fields as being 
[[gauge field]] [[connections]] ("[[vector potentials]]"), hence represented by  [[differential 1-forms]]. But on the point there is only the vanishing 1-form, hence just a single field configuration $\phi_0$.

Even though there is just a single such field, that $G$ is the [[gauge group]] means that for each [[element]] $g \in G$ there is a 
[[gauge transformation]] that takes
$\phi_0$ to itself, a state of affairs which we suggestively denote by the symbols
$$
  \phi_0 \stackrel{g}{\to}  \phi_0
  \,.
$$

Again, the reader familiar with 
traditional [[gauge theory]] may think of [[gauge transformations]] as in [[Yang-Mills theory]]. Over the point these form, indeed, just the [[gauge group]] itself, taking the trivial field configuration to itself.

That the [[gauge group]] is indeed a [[group]] means that gauge transformations can be  applied consecutively, which we express in symbols as

$$
  \array{
    && \phi_0
    \\
    & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
    \\
    \phi_0 && \underset{g_2 \cdot g_1}{\to} && \phi_0
  }
  \,.
$$

Regarded this way, we say the [[gauge group]] acting on the single field $\phi_0$ forms a _[[groupoid]]_, whose single _[[object]]_ is $\phi_0$ and whose set of _[[morphisms]]_ is $G$. 

Of course in richer field theories there may be more than one field configuration, clearly, with gauge transformations between them. If $\phi_0$ and $\phi_1$ are two field configurations and $g$ is a gauge transformation taking one to the other, we may usefully denote this by

$$
  \array{
    \phi_0 &\stackrel{g_1}{\to}& \phi_1
  }
   \,.
$$

Similarly then for yet another gauge configuration to another field configuration

$$
  \array{
    \phi_1 &\stackrel{g_2}{\to}& \phi_2
  }
$$


then composing them gives the picture

$$
  \array{
    && \phi_1
    \\
    & {}^{\mathllap{g_1}}\nearrow && \searrow^{\mathrlap{g_2}}
    \\
    \phi_0 && \underset{g_2 \cdot g_1}{\to} && \phi_2
  }
  \,.
$$

We now discuss this notion of [[groupoids]] more formally.

##### Groupoids and basic homotopy 1-type theory
 {#GroupoidsAndBasicHomotopy1TypeTheory}


The following is a quick review of basics of [[groupoids]] and their [[homotopy theory]] ([[homotopy 1-type]]-theory), geared towards the constructions and fact needed for 1-dimensional Dijkgraaf-Witten theory. 

+-- {: .num_defn #Groupoid}
###### Definition

A ([[small category|small]]) _[[groupoid]]_ $\mathcal{G}_\bullet$ is

* a pair of [[sets]] $\mathcal{G}_0 \in Set $ (the set of [[objects]]) and $\mathcal{G}_1 \in Set$ (the set of [[morphisms]])

* equipped with [[functions]]

  $$
    \array{
      \mathcal{G}_1 \times_{\mathcal{G}_0} \mathcal{G}_1
      &\stackrel{\circ}{\to}&
      \mathcal{G}_1
      & \stackrel{\overset{t}{\to}}{\stackrel{\overset{i}{\leftarrow}}{\underset{s}{\to}}}&
      \mathcal{G}_0
    }\,,
  $$

  where the [[fiber product]] on the left is that over $\mathcal{G}_1 \stackrel{t}{\to} \mathcal{G}_0 \stackrel{s}{\leftarrow} \mathcal{G}_1$, 

such that

* $i$ takes values in [[endomorphisms]];

  $$
    t \circ i = s \circ i =   id_{\mathcal{G}_0}, \;\;\; 
  $$

* $\circ$ defines a partial [[composition]] operation which is [[associativity|associative]] and [[unitality|unital]] for $i(\mathcal{G}_0)$ the [[identities]]; in particular

  $s (g \circ f) = s(f)$ and $t (g \circ f) = t(g)$;

* every morphism has an [[inverse]] under this composition.

=--

+-- {: .num_remark }
###### Remark

This data is visualized as follows. The set of morphisms is 

$$
  \mathcal{G}_1
  = 
  \left\{
    \phi_0 \stackrel{k}{\to} \phi_1
  \right\}
$$

and the set of pairs of composable morphisms is

$$
  \mathcal{G}_2 \coloneqq \mathcal{G}_1 \underset{\mathcal{G}_0}{\times} \mathcal{G}_1
  =
  \left\{
    \array{
      && \phi_1
      \\
      & {}^{\mathllap{k_1}}\nearrow && \searrow^{\mathrlap{k_2}}
      \\
      \phi_0 && \stackrel{k_2 \circ k_1}{\to} && \phi_2
    }
  \right\}
  \,.
$$

The functions $p_1, p_2, \circ \colon \mathcal{G}_2 \to \mathcal{G}_1$ are those which send, respectively, these triangular diagrams to the left morphism, or the right morphism, or the bottom morphism.

=--


+-- {: .num_example #DeloopingGroupoid}
###### Example

For $G$ a [[group]], its [[delooping]] [[groupoid]] $(\mathbf{B}G)_\bullet$ has

* $(\mathbf{B}G)_0 = \ast$;

* $(\mathbf{B}G)_1 = G$.

For $G$ and $K$ two groups, group homomorphisms $f \colon G \to K$
are in [[natural bijection]] with groupoid homomorphisms
$$
  (\mathbf{B}f)_\bullet
  \;\colon\;
  (\mathbf{B}G)_\bullet \to (\mathbf{B}K)_\bullet
  \,.
$$

In 
particular a [[group character]] $c \colon G \to U(1)$ is equivalently a groupoid homomorphism

$$
  (\mathbf{B}c)_\bullet 
   \;\colon\;
   (\mathbf{B}G)_\bullet 
     \to
   (\mathbf{B}U(1))_\bullet
  \,.
$$

Here, for the time being, all groups are [[discrete groups]]. Since the [[circle group]] $U(1)$ also has a standard structure of a [[Lie group]], and since later for the discussion of Chern-Simons type theories this will be relevant, we will write from now on

$$
  \flat U(1) \in Grp
$$

to mean explicitly the [[discrete group]] underlying the circle group. (Here "$\flat$" denotes the "[[flat modality]]".)

=--

+-- {: .num_example #ActionGroupoid}
###### Example

For $X $ a [[set]], $G$ a [[discrete group]] and $\rho \colon X \times G \to X$ an [[action]] of $G$ on $X$ (a [[permutation representation]]), the **[[action groupoid]]** or **[[homotopy quotient]]** of $X$ by $G$ is the groupoid

$$
  X//_\rho G
  = 
  \left(
    X \times G
    \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to}}
    X
  \right)
$$

with composition induced by the product in $G$. Hence this is the groupoid whose objects are the elements of $X$, and where [[morphisms]] are of the form

$$
  x_1 \stackrel{g}{\to} x_2 = \rho(x_1)(g)
$$

for $x_1, x_2 \in X$, $g \in G$.

=--

+-- {: .num_example }
###### Example

The [[interval]] $I$ is the groupoid with 

* $I_0 = \{a,b\}$;
* $I_1 = \{\mathrm{id}_a, \mathrm{id}_b, a \to  b \}$.

=--

+-- {: .num_example }
###### Example

For $\Sigma$ a [[topological space]], its [[fundamental groupoid]]
  $\Pi_1(\Sigma)$ is

* $\Pi_1(\Sigma)_0 = $ points in $X$;
* $\Pi_1(\Sigma)_1 = $ [[continuous function|continuous]] paths in $X$ modulo [[homotopy]] that leaves the endpoints fixed.

=--

+-- {: .num_example #PathSpaceGroupoid}
###### Example

For $\mathcal{G}_\bullet$ any groupoid, there is the [[path space]] groupoid $\mathcal{G}^I_\bullet$ with

* $\mathcal{G}^I_0 = \mathcal{G}_1 = \left\{ \array{ \phi_0 \\ \downarrow^{\mathrlap{k}} \\ \phi_1  } \right\}$;

* $\mathcal{G}^I_1 = $ [[commuting diagram|commuting squares]] in $\mathcal{G}_\bullet$ = 

  $$
    \left\{
       \array{
          \phi_0 &\stackrel{h_0}{\to}& \tilde \phi_0
          \\
          {}^{\mathllap{k}}\downarrow && \downarrow^{\mathrlap{\tilde k}}
          \\
          \phi_1 &\stackrel{h_1}{\to}& \tilde \phi_1
       }
    \right\}
    \,.
  $$   

This comes with two canonical homomorphisms

  $$
    \mathcal{G}^I_\bullet
     \stackrel{\overset{ev_1}{\to}}{\underset{ev_0}{\to}}
	   \mathcal{G}_\bullet
  $$

  which are given by endpoint evaluation, hence which send such a commuting square to either its top or its bottom hirizontal component.


=--

+-- {: .num_defn }
###### Definition

For $f_\bullet, g_\bullet : \mathcal{G}_\bullet \to \mathcal{K}_\bullet$
two morphisms between groupoids,
  a _[[homotopy]]_ $f \Rightarrow g$ 
(a [[natural transformation]]) is
  a homomorphism of the form $\eta_\bullet : \mathcal{G}_\bullet \to \mathcal{K}^I_\bullet$
  (with [[codomain]] the [[path space object]] of $\mathcal{K}_\bullet$ as in example \ref{PathSpaceGroupoid})
  such that it fits into the diagram as depicted here on the right:
  $$
    \array{
      & \nearrow  \searrow^{\mathrlap{f_\bullet}}
      \\
      \mathcal{G} &\Downarrow^{\mathrlap{\eta}}& \mathcal{K}
     \\
     & \searrow \nearrow_{\mathrlap{g_\bullet}}
    }

	\;\;\;\;
	\coloneqq
	\;\;\;\;
    \array{
      && \mathcal{K}_\bullet
      \\
      & {}^{\mathllap{f_\bullet}}\nearrow & \uparrow^{\mathrlap{(ev_1)_\bullet}}
      \\
      \mathcal{G}_\bullet
      &\stackrel{\eta_\bullet}{\to}&
      \mathcal{K}^I_\bullet
      \\
      & {}_{\mathllap{g_\bullet}}\searrow & \downarrow^{\mathrlap{(ev_0)_\bullet}}
      \\
      && \mathcal{K}
    }
    \,.
  $$

=--

+-- {: .num_defn }
###### Definition (Notation)

Here and in the following, the convention is that we write

* $\mathcal{G}_\bullet$ (with the subscript decoration) when we regard groupoids with just 
homomorphisms ([[functors]]) between them, 

* $\mathcal{G}$ (without the subscript decoration) when we regard groupoids
with homomorphisms ([[functors]]) between them and [[homotopies]] ([[natural transformations]]) between these

  $$
    \array{
      & \nearrow \searrow^{\mathrlap{f}}
      \\
      X &\Downarrow& Y
      \\
      & \searrow \nearrow_{g}
    }
    \,.
  $$

=--

+-- {: .num_example }
###### Example

For $X,Y$ two groupoids, the [[internal hom|mapping groupoid]] $[X,Y]$ or $Y^X$ is

* $[X,Y]_0 = $ homomorphisms $X \to Y$;
* $[X,Y]_1 = $ homotopies between such. 

=--

+-- {: .num_defn }
###### Definition

  A ([[homotopy equivalence|homotopy-]]) _[[equivalence of groupoids]]_ is a morphism
$\mathcal{G} \to \mathcal{K}$ which has a left and right [[inverse]] up to [[homotopy]].  

=--

+-- {: .num_example #BZIsPiSOne}
###### Example

The map

$$
  \mathbf{B}\mathbb{Z} \stackrel{}{\to} \Pi(S^1)
$$

which picks any point and sends $n \in \mathbb{Z}$ to the loop based at that point which winds around $n$ times, is an [[equivalence of groupoids]].

=--


+-- {: .num_prop #DiscreteGroupoidIsDijointUnioonOfDeloopings}
###### Proposition

  Assuming the [[axiom of choice]] in the ambient [[set theory]],
  every groupoid is equivalent to a disjoint union of 
  [[delooping]] groupoids,
  example \ref{DeloopingGroupoid} -- a _[[skeleton]]_.

=--

+-- {: .num_remark}
###### Remark

 The statement of prop. \ref{DiscreteGroupoidIsDijointUnioonOfDeloopings} 
 becomes false as when we pass to groupoids that are equipped with
 [[geometry|geometric]] structure. This is the reason why for discrete geometry all  [[Chern-Simons theory|Chern-Simons]]-type field theories (namely [[Dijkgraaf-Witten theory]]-type theories) fundamentally involve just groups (and higher groups),
 while for nontrivial geometry there are genuine groupoid theories, 
 for instance the [[AKSZ sigma-models]]. But even so, 
 [[Dijkgraaf-Witten theory]] is usefully discussed in terms of groupoid technology, in particular since the choice of equivalence in 
 prop. \ref{DiscreteGroupoidIsDijointUnioonOfDeloopings} is not canonical.

=--

+-- {: .num_defn #HomotopyFiberProductOfGroupoids}
###### Definition

Given two morphisms of groupoids 
$X \stackrel{f}{\leftarrow} B \stackrel{g}{\to} Y$
their _[[homotopy fiber product]]_

$$
  \array{
   X \underset{B}{\times} Y
   &\stackrel{}{\to}& X
   \\
   \downarrow &\swArrow& \downarrow^{\mathrlap{f}}
   \\
   Y &\underset{g}{\to}& B
  }
$$

is the [[limit]] [[cone]]

$$
  \array{
    X_\bullet \underset{B_\bullet}{\times} B^I_\bullet
    \underset{B_\bullet}{\times} Y_\bullet
    &\to& &\to& X_\bullet
    \\
    \downarrow && && \downarrow^{\mathrlap{f_\bullet}}
    \\
    && B^I_\bullet &\underset{(ev_0)_\bullet}{\to}& B_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    Y_\bullet &\underset{g_\bullet}{\to}& B_\bullet
  }
  \,,
$$

hence the ordinary iterated [[fiber product]] over the [[path space]] groupoid, as indicated.

=--

+-- {: .num_remark #FiberProductsOfGroupoidsComponentwise}
###### Remark

An ordinary fiber product $X_\bullet \underset{B_\bullet}{\times}Y_\bullet$ of groupoids is given simply by the fiber product of the underlying sets of objects and morphisms:

$$
  (X_\bullet \underset{B_\bullet}{\times}Y_\bullet)_i 
  =
  X_i \underset{B_i}{\times} Y_i
  \,.
$$

=--



+-- {: .num_example #LoopSpaceGroupoid}
###### Example

For $X$ a [[groupoid]] and $\ast \to X$ a point in it, we call

$$
  \Omega X
  \coloneqq
  \ast \underset{X}{\times} \ast
$$

the [[loop space object|loop space groupoid]] of $X$.

For $G$ a group and $\mathbf{B}G$ its  [[delooping]] groupoid from
  example \ref{DeloopingGroupoid}, we have
  $$
    G \simeq \Omega \mathbf{B}G = \ast \underset{\mathbf{B}G}{\times} \ast
    \,.
  $$

 Hence $G$ is the [[loop space object]] of its own [[delooping]], as it should be.

=--

+-- {: .proof}
###### Proof

We are to compute the ordinary limiting cone $\ast \underset{\mathbf{B}G_\bullet}{\times}  (\mathbf{B}G^I)_\bullet \underset{\mathbf{B}G_\bullet}{\times} \ast$ in

$$
  \array{
    &\to& &\to& \ast
    \\
    \downarrow && && \downarrow^{\mathrlap{}}
    \\
    && (\mathbf{B}G)^I_\bullet &\underset{(ev_0)_\bullet}{\to}& \mathbf{B}G_\bullet
    \\
    \downarrow && \downarrow^{\mathrlap{(ev_1)_\bullet}}
    \\
    \ast &\underset{}{\to}& \mathbf{B}G_\bullet
  }
  \,,
$$

In the middle we have the groupoid $(\mathbf{B}G)^I_\bullet$ whose objects are elements of $G$ and whose morphisms are pairs of elements in $G$ which act by left and right multiplication. 
Using remark \ref{FiberProductsOfGroupoidsComponentwise} 
the limiting cone precisely picks those morphisms such that these two elements are constant on the neutral element, hence just produces the elements of $G$.

=--

+-- {: .num_prop #FreeLoopSpaceOfGroupoid}
###### Proposition


The [[free loop space object]] is

  $$
    [\Pi(S^1), X]
	\simeq
	X \underset{[\Pi(S^0), X]}{\times}X
  $$

=--

+-- {: .proof}
###### Proof

Notice that $\Pi_1(S^0) \simeq \ast \coprod \ast$. Therefore
the [[path space object]] $[\Pi(S^0), X_\bullet]^I_\bullet$ has

* objects are pairs of morphisms in $X_\bullet$;

* morphisms are commuting squares of such.

Now the fiber product in def. \ref{HomotopyFiberProductOfGroupoids}
picks in there those pairs of morphisms for which both start at the same object, and both end at the same object. Therefore $X_\bullet \underset{[\Pi(S^0), X_\bullet]_\bullet}{\times} [\Pi(S^0), X_\bullet]^I_\bullet \underset{[\Pi(S^0), X_\bullet]_\bullet}{\times} X$ is the groupoid whose

* objects are diagrams in $X_\bullet$ of the form 

  $$
    \array{
       & \nearrow \searrow
       \\
       x_0 && x_1
       \\
       & \searrow \nearrow
    }
  $$

* morphism are cylinder-diagrams over these.

One finds along the lines of example 
\ref{BZIsPiSOne} that this is equivalent to maps from $\Pi_1(S^1)$ into $X_\bullet$ and homotopies between these.

=--

+-- {: .num_remark}
###### Remark

Even though all these models of the circle $\Pi_1(S^1)$ are equivalent,
below the special appearance of the circle in the proof of 
prop. \ref{FreeLoopSpaceOfGroupoid} as the combination of two semi-circles will be important for the following proofs. 
As we see in a moment, this is the natural way in which the circle
appears as the composition of an [[evaluation map]] with a [[coevaluation map]].

=--

+-- {: .num_example #AdjointActionGroupoidFromFreeLoopSpaceObject}
###### Example

For $G$ a [[discrete group]], the [[free loop space object]] of its [[delooping]] $\mathbf{B}G$ is $G//_{ad} G$, the [[action groupoid]], def. \ref{ActionGroupoid}, of the [[adjoint action]] of $G$ on itself:

$$
  [\Pi(S^1), \mathbf{B}G] \simeq G//_{ad} G
  \,.
$$

=--

+-- {: .num_example }
###### Example

For an [[abelian group]] such as $\flat U(1)$ we have

$$
  [\Pi(S^1), \mathbf{B}\flat U(1)]
  \simeq
  \flat U(1)//_{ad} \flat U(1)
  \simeq
  (\flat U(1)) \times (\mathbf{B}\flat U(1))
  \,.
$$

=--

+-- {: .num_example #GroupCharacterAsClassFunctionByFreeLoopSpace}
###### Example

Let $c \colon G \to \flat U(1)$ be a group homomorphism, hence a [[group character]]. By example \ref{DeloopingGroupoid} this has a [[delooping]] to a groupoid homomorphism 

$$
  \mathbf{B}c \;\colon\; \mathbf{B}G \to \mathbf{B}\flat U(1)
  \,.
$$

Unde the [[free loop space object]] construction this becomes

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  [\Pi(S^1), \mathbf{B}G]
  \to 
  [\Pi(S^1), \mathbf{B}\flat U(1)]
$$

hence 

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  G//_{ad}G
  \to 
  \flat U(1) \times \mathbf{B}U(1)
  \,.
$$

So by postcomposing with the [[projection]] on the first factor we recover from the general [[homotopy theory]] of groupoids the statement that a group character is a [[class function]] on [[conjugacy classes]]:

$$
  [\Pi(S^1), \mathbf{B}c]
  \;\colon\;
  G//_{ad}G
  \to 
  U(1)
  \,.
$$

=--


##### Correspondences of groupoids 
 {#CorrespondencesOfGroupoids}

With some basic homotopy theory of groupoids in hand, we can now talk about [[trajectories]] in finite gauge theories, namely about [[spans]]/[[correspondences]] of groupoids and their composition.

Before talking about correspondences of groupoids, we need to organize the groupoids themselves a bit more.

+-- {: .num_defn #TwoOneCategory}
###### Definition 

A  **[[(2,1)-category]]** $\mathcal{C}$ is 

1. a collection $\mathcal{C}_0$  -- the "collection of [[objects]]";

1. for each [[tuple]] $(X,Y) \in \mathcal{C}_0 \times \mathcal{C}_0$ a [[groupoid]] $\mathcal{C}(X,Y)$ -- the _[[hom-groupoid]]_ from $X$ to $Y$;

1. for each [[triple]] $(X,Y,Z) \in \mathcal{C}_0 \times \mathcal{C}_0 \times \mathcal{C}_0$ a groupoid homomorphism ([[functor]])

   $$
     \circ_{X,Y,Z} \colon \mathcal{C}(X,Y) \times \mathcal{C}(Y,Z) \to \mathcal{C}(X,Z)
   $$
  
   called _[[composition]]_ or _[[horizontal composition]]_ for emphasis;

1. for each [[quadruple]] $(W,X,Y,Z,)$ a [[homotopy]] -- the _[[associator]]_ --

   $$
     \array{
        \mathcal{C}(W,X) \times \mathcal{C}(X,Y) \times \mathcal{C}(Y,Z)
        &\stackrel{}{\to}&
        \mathcal{C}(W,Y) \times \mathcal{C}(Y,Z)
        \\
        \downarrow &\swArrow_{\alpha_{W,X,Y,Z}}& \downarrow
        \\
        \mathcal{C}(W,X) \times \mathcal{C}(X,Z)
        &\stackrel{}{\to}&
        \mathcal{C}(W,Z)
     }
   $$

   (...) and similarly a [[unitality]] homotopy (...)
   

such that for each [[quintuple]] $(V,W,X,Y,Z)$ the associators satisfy the [[pentagon identity]].

The [[objects]] of the [[hom-groupoid]] $\mathcal{C}(X,Y)$ we call the _[[1-morphisms]]_ from $X$ to $Y$, indicated by $X \stackrel{f}{\to} Y$, and the [[morphisms]] in $\mathcal{C}(X,Y)$ we call the [[2-morphisms]] of $\mathcal{C}$, indicated by

$$
  \array{
     \\
     & \nearrow \searrow^{\mathrlap{f}}
     \\
    X &\Downarrow&  Y
     \\
     & \searrow \nearrow_{\mathrlap{g}}
  }
  \,.
$$

If all associators $\alpha$ can and are chosen to be the [[identity]] then this is called a _[[strict 2-category|strict (2,1)-category]]_.

=--

+-- {: .num_defn}
###### Definition/Example

Write [[Grpd]] for the [[strict 2-category|strict]] [[(2,1)-category]], 
def. \ref{TwoOneCategory}, whose

* [[objects]] are [[groupoids]] $\mathcal{G}$;

* [[1-morphisms]] are [[functors]] $f \colon \mathcal{G} \to \mathcal{K}$;

* [[2-morphisms]] are [[homotopies]] between these.

=--


+-- {: .num_defn #OneSpansInOneGroupoids}
###### Definition/Example

Write $Span_1(Grpd)$ for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]];

* [[1-morphisms]] are [[spans]]/[[correspondences]] of [[functors]], hence 

  $$
    \array{
     A
      &\leftarrow&
      X
      &\rightarrow&
     B
     }
     \,;
  $$

* [[2-morphisms]] are [[diagrams]] in [[Grpd]] of the form

  $$
    \array{  
      && X_1
      \\
      & \swarrow &\downarrow& \searrow
      \\
      A &\seArrow& \downarrow^{\mathrlap{\simeq}} &\swArrow& B
      \\
      & \nwarrow &\downarrow& \nearrow
      \\
      && X_2
    }
  $$

* [[composition]] is given by forming the [[homotopy fiber product]], def. \ref{HomotopyFiberProductOfGroupoids}, of the two adjacent homomorphisms of two spans, hence for two spans

  $$
    X \stackrel{}{\leftarrow} K \rightarrow Y
  $$

  and

  $$
    Y \stackrel{}{\leftarrow} L \rightarrow Z
  $$
  
  their composite is the span which is the outer part of the diagram

  $$
    \array{
      && && K \underset{Y}{\times}L
      \\
      && & {}^{\mathllap{p_1}}\swarrow 
      && \searrow^{\mathrlap{p_2}}
      \\
      && K && \swArrow && L
      \\
      & \swarrow && \searrow && \swarrow && \searrow
      \\
      X && && Y && && Z
    }
    \,.
  $$

=--

+-- {: .num_defn }
###### Definition

There is the structure of a [[symmetric monoidal (2,1)-category]] on $Span_1(Grpd)$ by degreewise [[Cartesian product]] in [[Grpd]].

$$
  (X \leftarrow K \rightarrow Y)
  \otimes
  (\tilde X \leftarrow \tilde K \rightarrow \tilde Y)
  \;\coloneqq\;
  X \times \tilde X
  \leftarrow K \times \tilde K
  \rightarrow Y \times \tilde Y
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

An [[object]] $X$ of a [[symmetric monoidal (2,1)-category]] $\mathcal{C}^\otimes$ is [[fully dualizable object|fully dualizable]] if there exists

1. another object $X^\ast$, to be called the _[[dual object]]_;

1. a [[1-morphism]] $ev_X \colon X^\ast \otimes X \to \mathbb{I}$, to be called the _[[evaluation map]]_;

1. a [[1-morphism]]  $coev_X \colon \mathbb{I} \to X \otimes X^\ast$, to be called the [[coevaluation map]];

1. [[2-morphisms]] 

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Downarrow^{coev_{tr(X)}}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       \mathbb{I} 
         &\underset{coev_X}{\to}& 
       X^\ast \otimes X
        &\underset{ev_X}{\to}&
       \mathbb{I}
     }
   $$

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Uparrow^{ev_{tr(X)}}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       \mathbb{I} 
         &\underset{coev_X}{\to}& 
       X^\ast \otimes X
        &\underset{ev_X}{\to}&
       \mathbb{I}
     }
   $$

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Downarrow^{sa(X)}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       X^\ast \otimes X 
         &\underset{ev_X}{\to}& 
       \mathbb{I}
        &\underset{coev_X}{\to}&
       X^\ast \otimes X
     }
   $$

   (the [[saddle]])

   and

   $$
     \array{
       && \rightarrow
       \\
       & \nearrow &\Uparrow^{cosa(X)}& \searrow^{\mathrlap{id}_{\mathbb{I}}}
       \\
       X^\ast \otimes X 
         &\underset{ev_X}{\to}& 
       \mathbb{I}
        &\underset{coev_X}{\to}&
       X^\ast \otimes X
     }
   $$

   (the co-saddle)

such that these exhibit an [[adjunction]] and are themselves adjoint (...).

=--

+-- {: .num_defn }
###### Definition

Given a [[symmetric monoidal (2,1)-category]] $\mathcal{C}$, and a [[fully dualizable object]] $X \in \mathcal{C}$ and a [[1-morphism]]  $f \colon X \to X$, the [[trace]] of $f$ is the [[composition]]

$$
  tr(f)
   \;\colon\;
  \mathbb{I}
    \stackrel{coev_X}{\to}
  X \otimes X^\ast
    \stackrel{f \otimes id_{X^\ast}}{\to}
  X \otimes X^\ast
    \stackrel{ev_x}{\to}
  \mathbb{I}
  \,.
$$

=--


+-- {: .num_prop #GroupoidInSpanOneIsSelfDual}
###### Proposition

Every [[groupoid]] $X \in Grpd \hookrightarrow Span_1(Grpd)$ 
is a [[dualizable object]] in 
$Span_1(Grpd)$, and in fact is self-dual.

The [[evaluation map]] $ev_X$ is given by the [[span]]

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && && [\Pi_1(S^0),X] &\simeq& X \times X
  }
$$

and the [[coevaluation map]] $coev_X$ by the reverse span.

For $X \in Grpd \hookrightarrow Span_1(Grpd)$ any object,
the [[trace]] ("[[span trace]]") of the [[identity]] on it is its 
[[free loop space object]], prop. \ref{FreeLoopSpaceOfGroupoid}:

$$
  tr(id_X) \simeq 
  \left(
    \array{
      && [\Pi_1(S^1), X]
      \\
      & \swarrow && \searrow
      \\
      \ast && && \ast
    }
  \right)
  \,.
$$


The second order covaluation map on the [[span trace]] of the identity is 

$$
  \array{
    && && \ast
    \\
    && && \uparrow
    \\
    && && X
    \\
    && && \downarrow
    \\
    && && [\Pi(S^1), X]
    \\
    && & \swarrow & & \searrow
    \\
    \ast &\leftarrow& X &\rightarrow& [\Pi(S^0), X] &\leftarrow&
    X &\rightarrow& & \ast
  }
  \,.
$$

=--


+-- {: .proof}
###### Proof

By prop. \ref{GroupoidInSpanOneIsSelfDual}
the [[trace]] of the identity is given by the composite span

$$
  \array{
    && && X \underset{[\Pi_1(S^1), X]}{\times} X
    \\
    && & \swarrow && \searrow
    \\
    && X && \swArrow && X
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast
    &&
    &&
    [\Pi_1(S^0),X]
    &&
    &&
    \ast
  }
  \,.
$$

By prop. \ref{FreeLoopSpaceOfGroupoid} we have

$$
  X \underset{[\Pi_1(S^1), X]}{\times} X
  \simeq [\Pi_1(S^1), X]
  \,.
$$

Along these lines one checks the required [[zig-zag identities]].

=--

##### 1d DW local field theory 
 {#1dDWLocalFieldTheory}

We have now assembled all the ingredients need in order to formally regard a [[group character]] $c \colon G \to U(1)$ on a [[discrete group]] as a local action functional of a prequantum field theory, hence as a [[fully dualizable object]]

$$
  S
  \;\coloneqq\;
  \left[
    \array{
      \mathbf{B}G
      \\
      \downarrow^{\mathrlap{c}}
      \\
      \mathbf{B}\flat U(1)
    }
  \right]
  \;\in \;
  \mathrm{Span}_1(Grpd, \mathbf{B}\flat U(1))
$$

in a [[(2,1)-category]] of correspondences of groupoids as in def. \ref{OneSpansInOneGroupoids}, but equipped with maps and homotopies between maps to the [[coefficient]] over $\mathbf{B}\flat U(1)$. This is described in def. \ref{OneSpansInOneGroupoidsOverBU} below. In order to motivate this, consider the following.

+-- {: .num_example #HomotopyAsActionFunctional}
###### Example

Given a [[discrete groupoid]] $X$, [[functions]] 

$$
  \exp(i S) \colon X \to \flat U(1)
$$ 

are in [[natural bijection]] with [[homotopies]] of the form

$$
  \array{
    && X
    \\
    & \swarrow &&  \searrow
    \\
    \ast && \swArrow_{\phi} && ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \,,
$$

where the function corresponding to this homotopy is that given by the unique factorization through the [[homotopy fiber product]] $\flat U(1) \simeq \ast \underset{\mathbf{B}\flat U(1)}{\times} \ast$ as shown on the right of 

$$
  \array{
    && X
    \\
    & \swarrow &&  \searrow
    \\
    \ast && \swArrow_{\phi} && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \;\;\;\;
  \simeq
  \;\;\;\;
  \array{
    && X
    \\
    &\swarrow& \downarrow^{\mathrlap{S}} & \searrow
    \\
    && \flat U(1)
    \\
    \downarrow & \swarrow &&  \searrow & \downarrow
    \\
    \ast && \swArrow && ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }  
  \,,
$$

=--

This means that if we have an [[action functional]] on a space of [[trajectories]], and if these trajectories are given by [[spans]]/[[correspondences]] of groupoids as discussed above, then the action functional is naturally expressed as the homotopy filling a completion of the span to a square diagram over $\mathbf{B}\flat U(1)$. Therefore we cosider the following.

+-- {: .num_defn #OneSpansInOneGroupoidsOverBU}
###### Definition

Write $Span_1(Grpd, \flat\mathbf{B}U(1))$
for the [[(2,1)-category]] whose

* [[objects]] are [[groupoids]] $X$ equipped with a morpism

  $$
    \left[
      \array{
         X
         \\
         \downarrow^{\mathrlap{f}}
         \\
         \mathbf{B}\flat U(1)
      }
    \right]
  $$

* [[morphisms]] are [[spans]] $X_1 \leftarrow Y \rightarrow X_2$ equipped with a [[homotopy]] $\phi$ in 

  $$
    \array{
       && Y
       \\
       & {}^{\mathllap{f_1}}\swarrow && \searrow^{\mathrlap{f_2}}
       \\
       X_1 && \swArrow_{\phi} && X_2
       \\
       & \searrow && \swarrow
       \\
       && \mathbf{B}\flat U(1)
    }
  $$

* [[2-morphisms]] are morphism of spans compatible with the maps to $\mathbf{B}\flat U(1)$ in the evident way.

The operation of [[composition]] is as in $Span_1(Grpd)$, def. \ref{OneSpansInOneGroupoids} on the upper part of these diagrams, naturally extended to the whole diagrams by composition of the [[homotopies]] filling the squares that appear. 

=--



+-- {: .num_prop}
###### Proposition

$Span_1(Grpd, \mathbf{B}\flat U(1))$ carries the structure of a
[[symmetric monoidal (infinity,n)-category|symmetric monoidal (2,1)-category]] where the [[tensor product]] is given by

$$
  \left[
    \array{  
       X_1
       \\
       \downarrow^{\mathrlap{f_1}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \otimes
  \left[
    \array{  
       X_2
       \\
       \downarrow^{\mathrlap{f_2}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \;\;
  \coloneqq
  \;\;
  \left[
    \array{  
       X_1 \times X_2
       \\
       \downarrow^{\mathrlap{f_1 \circ p_1 + f_2 \circ p_2}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

There is an evident [[forgetful functor|forgetful]] [[(2,1)-functor]]

$$
  Span_1(Grpd, \mathbf{B}\flat U(1))
  \to 
  Span_1(Grpd)
$$ 

which forgets the maps to $\mathbf{B}\flat U(1)$ and the homotopies between them. This is a [[monoidal (infinity,1)-functor|monoidal (2,1)-functor]].

=--

As generalization of prop. \ref{GroupoidInSpanOneIsSelfDual} we now have the following:

+-- {: .num_prop}
###### Proposition

Every object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
  \in Span_1(Grpd,\mathbf{B}\flat U(1))
$$

is a [[dualizable object]], with dual object 

$$
  \left[
    \array{  
       X
       \\
       \downarrow^{-\mathrlap{f}}
       \\
       \mathbf{B}\flat U(1)
    }
  \right]
$$

and with [[evaluation map]] given by

$$
  \array{
    && X
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow_{\mathrlap{\simeq}} && X \times X
    \\
    & {}_{\mathllap{0}}\searrow && \swarrow_{\mathrlap{f \circ p_1 - f \circ p_2}}
    \\
    && \mathbf{B}\flat U(1)
  }
  \,.
$$


=--

In conclusion we can now compute what the 1-dimensional prequantum field theory defined by a group character $c \colon G \to U(1)$ regarded as a local action functional assigns to the [[circle]].

+-- {: .num_theorem #GroupCharacterPrequantumTheoryOnCircle}
###### Theorem

The prequantum field theory defined by a [[group character]]

  $$
    \left[
      \array{
	    \mathbf{Field}
		\\
                \downarrow^{\mathrlap{S}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]
	\;\;
	:=
	\;\;
    \left[
      \array{
	    \mathbf{B}G
		\\
                \downarrow^{\mathrlap{\mathbf{B}\mathrlap{c}}}
		\\
		\flat \mathbf{B}U(1)
	  }
	\right]	
      \in Span_1(Grpd,\mathbf{B}\flat U(1))
  $$

  assigns to the [[circle]] the [[trace]] of the identity on this object, which under the identifications of example \ref{LoopSpaceGroupoid}, example \ref{GroupCharacterAsClassFunctionByFreeLoopSpace}, and example \ref{HomotopyAsActionFunctional} is the group character itself:


$$
  \array{
    && && [\Pi_1(S^1), \mathbf{B}G]
    \\
    && & \swarrow && \searrow
    \\
    && \mathbf{B}G && \swArrow && \mathbf{B}G
    \\
    & \swarrow && \searrow && \swarrow && \searrow
    \\
    \ast && && \mathbf{B}G \times \mathbf{B}G && && \ast
    \\
    &{}_0\searrow & && \downarrow^{\mathrlap{S(p_1) - S(p_2)}}
    &&& \swarrow_{0}
    \\
    &&&& \mathbf{B}\flat U(1)
  }
  \;\;\;
   \simeq
  \;\;\;
  \array{
    && G//G
    \\
    && \simeq
    \\
    && [\Pi(S^1), \mathbf{B}G]
    \\
    && \downarrow^{\mathrlap{c}}
    \\
    && \flat U(1)
    \\
    & \swarrow && \searrow
    \\
    \ast && \swArrow && \ast
    \\
    & \searrow && \swarrow
    \\
    && \mathbf{B}\flat U(1)
  }
  \;\;\;
$$

Here the [[action functional]] on the right  sends a [[field configuration]] $g \in G = [\Pi(S^1), \mathbf{B}G]_0$
to its value $c(g) \in U(1) = (\flat \mathbf{B}U(1))_1$.

=--


#### 2d Dijkgraaf-Witten theory

The [[group character]] $c : G \to U(1)$ which defines 
1-dimensional prequantum Dijkgraaf-Witten theory
in [1d Dijkgraaf-Witten theory](#1dDWTheory) is equivalently a [[cocycle]] in degree-1 [[group cohomology]]

$$
  [c] \in H_{\mathrm{Grp}}(G,U(1))
  \,.
$$

More familiar are maybe cocycles in higher degree. 
In view of the above it is plausible that one may interpret a cocycle in degree-$n$ group cohomology, for 
all $n \in \mathbb{N}$ as a higher order [[action functional]]
$\mathbf{B}G \to \flat\mathbf{B}^n U(1)$ and induce an 
$n$-dimensional local prequantum Dijkgraaf-Witten-type theory
from it. 

Here we discuss the case of $n = 2$ where a group 2-cocycle is regarded as the local action functional of a 2-dimensional Digjkgraaf-Witten field theory. We use this as occasion to introduce a bit of the theory of [[2-groups]] and their [[homotopy theory]] ([[homotopy 2-type]]-theory). Below in _[3d DW theory](#3dDWLocalPrequantumFieldTheory)_ we then turn to the fully general case of [[∞-groupoid]]-theory.

##### 2-Groupoids and basic homotopy 2-type theory

(...)

#### 3d Dijkgraaf-Witten theory
 {#3dDWLocalPrequantumFieldTheory}


In view of the above it is plausible that one may interpret a cocycle in degree-$n$ group cohomology, for 
all $n \in \mathbb{N}$ as a higher order [[action functional]]
$\mathbf{B}G \to \flat\mathbf{B}^n U(1)$ and induce an 
$n$-dimensional local prequantum Dijkgraaf-Witten-type theory
from it. 

Here we review how to formalize this and then consider the
example of DW theory in dimension 3.


##### $\infty$-Groupoids and basic homotopy theory

We briefly recall here some basic definitions and facts of [[∞-groupoids]] and their [[homotopy theory]], geared towards their use in 3-dimensional [[Dijkgraaf-Witten theory]] and generally in [[∞-Dijkgraaf-Witten theory]].


+-- {: .num_defn #NerveOfGroupoid}
###### Definition

For $\mathcal{G}_\bullet$ a [[groupoid]], def. \ref{Groupoid}, we write

$$
  \mathcal{G}_n \coloneqq \mathcal{G}_1^{\times_{\mathcal{G}_0}^n}
$$ 

for the set of sequences of composable morphisms of length $n$, for $n \in \mathbb{N}$; schematically:

$$
  \mathcal{G}_n = 
  \left\{
    x_0 
      \stackrel{f_1}{\to} 
    x_1
      \stackrel{f_2}{\to}
    x_2
      \stackrel{f_2}{\to}
    \cdots
      \stackrel{f_n}{\to}
    x_n
  \right\}
  \,.
$$

For each $n \geq 1$, the two maps $d_0$ and $d_n$ that forget the first and the last morphism in such a sequence and the $n-1$ maps $d_k$ that form the composition of the $k$th morphism in the sequence with the next one, constitute $(n+1)$ [[functions]] denoted

$$
  d_k \colon \mathcal{G}_n \to \mathcal{G}_{n-1}
  \,.
$$

Moreover, the assignments $s_i$ that insert an [[identity]] morphism in position $i$ constitute [[functions]] denoted

$$
  s_i \colon \mathcal{G}_{n-1} \to \mathcal{G}_n
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

These collections of maps in def. \ref{NerveOfGroupoid} satisfy the [[simplicial identities]]. Moreover, they make $N(\mathcal{G}_\bullet)$ a Kan complex, where each [[horn]] has a _unique_ filler (extension to a [[simplex]]).

=--


+-- {: .num_defn }
###### Definition

The [[nerve]] operation constitutes a [[full and faithful functor]]

$$
  N \colon Grpd \to KanCplx \hookrightarrow sSet
  \,.
$$


=--


##### Homological algebra and abelian $\infty$-groups
 {}

An important class of examples of [[∞-groupoids]] are those which are presented under the [[Dold-Kan correspondence]] by [[chain complexes]] of abelian groups.

[[Dold-Kan correspondence]]


(...)

+-- {: .num_defn #DoldKanMap}
###### Definition


$$
  DK \;\colon\; 
  Ch_{\bullet \geq 0} 
  \stackrel{\simeq}{\to}
  sAb
  \stackrel{forget}{\to}
  KanCplx
  \hookrightarrow
  sSet
  \,.
$$

=--

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$ write

$$
  \mathbf{B}^n U(1) \coloneqq DK(U(1)[n])
  \,.
$$

=--

Below in _[Higher Chern-Simons theory](#HigherChern-SimonsLocalPrequantumFieldTheory)_ the _smooth_ version of the [[circle group]] plays a role. In order to amplify that here we are just dealing with the [[discrete group]] underlying $U(1)$, we write

$$
  \flat U(1) \coloneqq U(1)_{disc}
$$

for it. 

$$
  \mathbf{B}^n \flat U(1) \coloneqq DK([U(1)_{disc}[n]])
  \,.
$$

+-- {: .num_prop }
###### Proposition

By the [[Dold-Kan correspondence]] each $\mathbf{B}^n \flat U(1)$ is
naturally an [[∞-group]] and its [[delooping]] is indeed $\mathbf{B}^{n+1}\flat U(1)$

$$
  \Omega \mathbf{B}^{n+1} \flat U(1) \simeq \mathbf{B}^n \flat U(1)
  \,.
$$

=--



##### Group cohomology and local action functionals


+-- {: .num_prop #GroupCohomologyByHomotopyClassesOfMaps}
###### Proposition

For $G$ a [[discrete group]] and $A$ a discrete [[abelian group]], there is a natural isomorphism

$$
  H_{Grp}^n(G,A) \simeq \pi_0 Grpd_\infty(\mathbf{B}G, \mathbf{B}^n A)
$$

between the degree-$n$ [[group cohomology]] of $G$ with [[coefficients]] in $A$ and the connected components of maps of [[∞-groupoids]] from the [[delooping]] of $G$ to the $n$-fold [[delooping]] of $A$. 

=--

...

##### 3d DW local field theory

(...)

Let $[\alpha] \in H^3_{Grp}(G,U(1))$ be a 3-cocycle in [[group cohomology]]. By prop. \ref{GroupCohomologyByHomotopyClassesOfMaps}
this corresponds to a morphism of $\infty$-groupoids

$$
  \alpha \colon \mathbf{B}G \to \mathbf{B}^3 U(1) \flat U(1)
  \,.
$$

This is the local action functional of 3d-[[Dijkgraaf-Witten theory]] for this cocycle.

(...)

### Higher Chern-Simons local prequantum field theory
 {#HigherChern-SimonsLocalPrequantumFieldTheory}

By def. \ref{LocalPrequantumFieldWithAction}, a local prequantum [[bulk]] field theory in dimension $(n+1)$ is equivalently a morphism of the form 

$$
  \mathbf{Fields} \to \flat \mathbf{B}^{n+1}U(1)
  \,,
$$

for any object $\mathbf{Fields} \in \mathbf{H}$. 

First we observe in in 

* _[Universal topological Yang-Mills theory](#TopologicalYangMillsLocalPrequantumFieldTheory)_

that there is a fairly canonical such morphism $S^{n+1}_{tYM}$, namely the "[[atlas]] relative to [[manifolds]]" of $\flat \mathbf{B}^{n+1}U(1)$ given by the [[sheaf]] of [[differential forms|closed differential (n+1)-forms]]. Analyzing what this morphism is like, when regarded as a local prequantum field theory by def. \ref{LocalPrequantumFieldWithAction} shows that it is the "universal" higher [[topological Yang-Mills theory|topological Yang-Mills]] prequantum field theory. What exactly this means is then seem in 

* _[Higher Chern-Simons prequantum field theory](#HigherChernSimonsPrequantumFieldTheory)_

where we discuss how the boundary theories for $S^{n+1}_{tYM}$ are precisely the prequantum field theories of higher [[Chern-Simons theory]]-type, the _[[schreiber:∞-Chern-Simons theories]]_.






#### $d = n + 1$, Universal topological Yang-Mills theory
 {#TopologicalYangMillsLocalPrequantumFieldTheory}


+-- {: .num_prop }
###### Proposition

The canonical [[chain map]]

$$
  \array{  
    U(1)_{disc} &\to& 0 &\to& 0 &\to& \cdots &\to& 0
    \\
    \downarrow && \downarrow && \downarrow && \cdots && \downarrow
    \\
    C^\infty(-,U(1)) &\stackrel{d log}{\to}& \Omega^1 &\stackrel{d}{\to}& \Omega^2 &\stackrel{d}{\to}& \cdots &\to& \Omega^n_{cl}
  }
  \,,
$$

where the left map includes the sheaf of (locally) constant $U(1)$-valued functions into that of all $U(1)$-valued smooth functions, is a [[stalk]]-wise [[quasi-isomorphism]]. Hence under the [[Dold-Kan correspondence]], def. \ref{DoldKanMap}, both present the same [[smooth ∞-groupoid]]

$$
  \flat \mathbf{B}^n U(1) \simeq \mathbf{B}^n \flat U(1)
  \in Smooth\infty Grpd
  \,.
$$

=--

Accordingly we have a canonical inclusion:

+-- {: .num_defn #ClosedFormsInDeRhamCoefficients}
###### Definition

For $n \in \mathbb{N}$, write

$$
  \Omega^{n}_{cl} \in SmoothSpace \hookrightarrow Smooth \infty Grpd
$$

for the [[sheaf]] of closed smooth [[differential forms]] of degree $n$, regarded as a [[smooth space]], regarded as a [[smooth ∞-groupoid]]. Write

$$
  \Omega^{n}_{cl} \to \flat \mathbf{B}^n U(1)
$$

for the image in morphisms of [[Smooth∞Grpd]] under the [[Dold-Kan correspondence]], def. \ref{DoldKanMap}, of the [[chain map]]

$$
  \array{  
    0 &\to& 0 &\to& 0 &\to& \cdots &\to& \Omega^{n+1}_{cl}
    \\
    \downarrow && \downarrow && \downarrow && \cdots && \downarrow^{\mathrlap{id}}
    \\
    C^\infty(-,U(1)) &\stackrel{d log}{\to}& \Omega^1 &\stackrel{d}{\to}& \Omega^2 &\stackrel{d}{\to}& \cdots &\to& \Omega^n_{cl}
  }
  \,,
$$

=--

+-- {: .num_remark }
###### Remark

The map $\Omega^n_{cl} \to \flat \mathbf{B}^n U(1)$ in def. \ref{ClosedFormsInDeRhamCoefficients} may be characterized more abstractly as follows:

for every [[smooth manifold]] $\Sigma$, theinduced morphism of [[mapping spaces]]

$$
  [\Sigma, \Omega^n_{cl}] \to [\Sigma, \flat \mathbf{B}^n U(1)]
$$

is a [[1-epimorphism]], hence a [[stalk]]-wise [[epimorphism]] on [[connected components]].

=--

(...)

#### $d = n + 0$, Higher Chern-Simons field theories
 {#HigherChernSimonsPrequantumFieldTheory}


(...)


#### $d = n-1$, Topological Chern-Simons boundaries

(...)

#### $d = n-k$, Dimensional reduction

(...)

#### $d = n-1$, Wess-Zumino-Witten field theories

(...)

#### $d = n-2$, Wilson loop/Wilson surface field theories

(...)

## Related concepts

* [[prequantum geometry]]

* [[higher prequantum geometry]]

## References

The idea of formulating local prequantum field theory by spans in a slice over a "space of phases" in [[higher geometry]] has been expressed in the unpublished note

* [[Urs Schreiber]], _[[schreiber:Nonabelian cocycles and their quantum symmetries]]_ (2008)

A formulation of the idea for [[Dijkgraaf-Witten theory]]-type field theories is indicated in section 3 of 

* [[Daniel Freed]], [[Michael Hopkins]], [[Jacob Lurie]], [[Constantin Teleman]], _[[Topological Quantum Field Theories from Compact Lie Groups]]_ (2010)
 {#FHLT}

based on the considerations in section 3.2 of 

* [[Jacob Lurie]], _[[On the Classification of Topological Field Theories]]_ (2009).
 {#LurieTFT}

Based on the general formulation of the more general [[QFT with defects|field theory with defects]] described in section 4.3 there, in

* [[Domenico Fiorenza]], [[Alessandro Valentino]], _Boundary conditions in local TFTs_ (in preparation)
 {#FiorenzaValentino}

the structure of such [[domain walls]]/defects/[[branes]] are analyzed in the prequantum theory, hence with coefficients in an [[(∞,n)-category of spans]].

The study of local prequantum [[schreiber:∞-Chern-Simons theory]] with its codimension-1 [[schreiber:∞-Wess-Zumino-Witten theory]] and codimension 2-[[Wilson line]]-theory in this fashion, in an ambient [[cohesive (∞,1)-topos]] is discussed in 

* [[Domenico Fiorenza]], [[Urs Schreiber]] et al., _[[schreiber:Higher Chern-Simons local prequantum field theory]]_
 {#hCSlpQFT}

Much of the content of this entry here are, or arose as, lecture notes for


* [[Urs Schreiber]], _[[schreiber:Higher Chern-Simons theory Introduction]]_, at the workshop _[Chern-Simons Theory: Geometry, Topology and Physics](http://www.pitt.edu/~jdeblois/CS.html)_ University of Pittsburgh (May 2013)
 {#SchreiberPittLectures}

This forms one section of the more comprehensive lecture notes at

* _[[geometry of physics]]_

[[!redirects prequantum field theory]]
[[!redirects prequantum field theories]]
[[!redirects local prequantum field theory]]
[[!redirects local prequantum field theories]]

[[!redirects extended prequantum field theory]]
[[!redirects extended prequantum field theories]]

[[!redirects higher prequantum field theory]]
[[!redirects higher prequantum field theories]]