

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
#### Variational calculus
+--{: .hide}
[[!include variational calculus - contents]]
=--
#### Geometric quantization
+--{: .hide}
[[!include geometric quantization - contents]]
=--
#### Quantum field theory
+--{: .hide}
[[!include functorial quantum field theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _extended Lagrangian_ is the notion of [[Lagrangian]] refined to [[extended quantum field theory]] (or "localized" or "multi-tiered" quantum field theory). At the same time is is the [[prequantum n-bundle]] of the theory in its [[higher geometric quantization]] in top codimension, hence over the point.

## Motivation and Survey
 {#MotivationAndSurvey}

> under construction

1. [Ingredients of fundamental physics](#IngredientsOfFundamentalPhysics)

1. [Topological local Lagrangian gauge field theory](#TopologicalLocalLagrangianGaugeFieldTheory)

1. [Chern-Simons field theory as a toy example](#ChernSimonsTheoryAsAToyExample)

1. [Topological local field theory in higher category theory](#TopologicalLocalFieldTheoryInHigherGeometry)

1. [Topological local Lagrangian field theory in higher geometry](#TopologcalLocalLagrangianFieldTheoryInHigherGeometry)

1. [∞-Chern-Simons theory as the general example](#InfinityChern-SimonsTheoryAsTheGeneralExample)

### Ingredients of fundamental physics
 {#IngredientsOfFundamentalPhysics}

Ever since [[Issac Newton]], [[theories of physics]] are formulated in the language of [[mathematics]]. Modern physics is formulated in terms of modern mathematics in the most intimate way.
We aim to give here an account at least of central parts of modern physics in terms of  the mathematics of [[higher geometry]] that we discussed above. 

The physics that we are concerned with is _fundamental} physics_,
that part of the large subject of physics which is concerned with elementary  processes and phenomena of physics from which all others are thoght to _emerge_ as approximations to collective effects of complex configurations of the elementary 
entities.

The best theory of fundamental physics as presently understood 
is

_[[Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory]]_

| Einstein- | Maxwell- | Yang-Mills- |  Dirac- | Higgs |
|----------|---------|------------|--------|-------|
|  [[gravity]] | [[electromagnetism]] | [[electroweak  field|electroweak]] and [[strong nuclear force]] | [[fermion|fermionic ]] [[matter]] | [[scalar field]] |

While fundamental, this theory has free parameters which index different flavors of the same general mechanism. Notably the species and the masses of the fundamental particles are such parameters, as 
is their ([[Yukawa coupling|Yukawa]]-coupling) strengths to the force fields.

Specifying these parameters is called constructing a 
_[[model (in theoretical physics)|model]]_ in physics  and specifically as a [[phenomenology|phenomenological model]] of fundamental physics, 
if aimed at making the observations that are predicetd by the theory to closely match those that are being made in experiments. The global choice of these parameters that make the predictions  match all available data to the currently best possible degree is called the _standard model_, specifically the  _[[standard model of particle physics]]_ for the sector in which the large-scale description of the 
force of gravity is approximately negligible, and the 
_[[standard model of cosmology]]_
which focuses on that large scale structure.

### Topological local Lagrangian gauge field theory
 {#TopologicalLocalLagrangianGaugeFieldTheory}

While the standard model of fundamental physics is a specification of the general  framework of Einstein-Maxwell-Yang-Mills-Dirac-Higgs theory, that theory itself is a particular realization of several deep general principles  of theoretical physics: it is 

1. a **[[field (physics)|field]]** theory;
1. a **[[gauge theory|gauge]]** theory;
1. a **[[Lagrangian]]** theory;
1. a **[[local quantum field theory|local]]** theory;
1. a **[[topological field theory|topological]] theory.

We briefly indicate what this means, a formal discussion of these notions will be given in the  main part below.

* A **[[field (physics)|field]]** theory identifies the basic configurations of a physical system with generalized functions on spacetime, such as [[tensor fields]], and more generally with [[sections]] $\phi$ of some [[fiber bundle]] over spacetime

  $$
    \array{ 
      && E 
      \\
      & {}^{\mathllap{\phi}} & \downarrow^{\mathrlap{field\;bundle}}   
      \\
      X &\stackrel{id}{\to}& X
     }
   $$

* A **[[gauge theory|gauge]]** theory in the broad sense has not just a [[set]] or [[smooth space]] of field configurations but has a [[groupoid]] or [[stack]]/[[smooth groupoid]] of field configurations: there are equivalences between nominally different field configurations called [[gauge transformation]]

  $$
    \phi \stackrel{\simeq}{\to} \phi'
  $$

   A gauge theory in the original sense specifically has a groupoid of [[principal connections]] as its configurations. (Notice that gauge transformations are not in general just a redundancy of the description of the theory, but are genuine data: there are in general non-trivial gauge [[automorphisms]] of a field and the stack of gauge field configurations is not in general equivalent to a plain [[sheaf]].)

* A **[[Lagrangian]]** theory is one which is specified by a function on the space of all its configurations, called the (exponentiated) _[[action functional]]_ $\exp(i S)$. This function is assumed to be the [[integration of differential forms|integral]] of a [[differential form]] on [[spacetime]] that itself is a function of the field configurations and called the [[Lagrangian]] of the theory. 

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\right)\left(x\right) \right) 
  $$

  The [[critical locus]]

  $$
    \left\{
	 \phi \in \mathbf{Fields}(\Sigma)		|
		d_{\mathrm{var}} S_\phi = 0
	  \right\}
  $$

  of the action functional is called the _[[phase space]]_ of the theory, a point of this is said to be a solution to the _[[equations of motion]]_ of the theory.

* A **[[local quantum field theory|local]]** theory has a Lagrangian form which at each point of spacetime only depends on the values of the fields at that point, and of finitely many derivatives of the fields at that point.

  $$
    \exp(i S(\phi)) = \exp\left(i \int_X L\left(\phi\left(x\right), \nabla \phi\left(x\right)\right)\right) 
  $$

  This means that a _[[local Lagrangian]]_ is a horizontal form on the [[jet bundle]] of the field bundle of which the fields are sections.

* A **[[topological field theory|topological]]** theory finally is one where the field bundle is naturally associated to every smooth manifold, typically of some fixed dimension and possibly equipped with  topological [[G-structure]] such as an orientation, but not equipped with any further geometric structure: all geometric structure such as metrics on spacetime are themselves regarded as parts of the field content in a topological theory.


### Chern-Simons field theory as a toy example

Most of this was fairly well understood decades ago, by the 1960s. But even with all this conceptual understanding of the structure of fundamental physics available, there were and are a lot of implications of 
_topological local Lagrangian gauge field theory_ which remained elusive.
In the 1980s attention turned to -other_ topological local Lagrangian gauge field theories than that governing the standard model: it turns out that there are many such  [[theories of physics]] that share crucial properties with the standard model but which  otherwise predict, if considered as phenomenological models, physics  radically different from that
which we actually observe experimentally. For instance there are respectable theories of fundamental 
pyhsics which describe physics in dimensions other than the three spatial and one time dimension which we clearly observe, theories that contain no force of gravity, others that contain only the force of gravity, theories that contain mirror partners of every species of matter or contain no matter at all, etc.

In short, it was gradually realized and realized to be important that, in the platonic world of mathemtics and of theoretical physics, there is a whole space of field theories, in which the one underlying the standard model of observed physics is only one single point.

A crucial step forward happened when around 1989 [[Edward Witten]], in this vein,  introduced the study of what is now called _[[Chern-Simons theory]]_ a topological local Lagrangian gauge field theory which, as such, shares
some crucial principles with Einstein-Maxwell-Yang-Mills theory, while at the  same time being  radically different and most importantly: 
much simpler to analyze. 

The dimension of Chern-Simons theory is 3 instead of 4, but 
Chern-Simons theory has a gauge field just as Yang-Mills theory does.
For $G$ a simply connected  gauge group, this is mathematically represented
by a [[Lie algebra valued 1-form]] $A \in \Omega^1(\Sigma_3, \mathfrak{g})$.

The [[Lagrangian]] is simply the [[Chern-Simons 3-form]]

$$
  L(A)
  :=
  \mathrm{CS}_3(A)
  :=
  \langle A \wedge d A\rangle
  + 
  c
  \langle A \wedge [A \wedge A]\rangle
$$

and hence the Chern-Simons action functional is

$$
  \exp(iS(A)) 
  =
   \exp\left(
     2 \pi i \int_{\Sigma_X} \mathrm{CS}_3(A)
	\right)
$$


At the same time Chern-Simons theory is still being rich in phenomena, 
in fact so rich in phenomena that it helped illuminate deep mathematical problems that had not
otherwise been understood (properties called [[knot invariants]]).

### Topological local field theory in higher category theory
 {#TopologicalLocalFieldTheoryInHigherGeometry}

Another pleasant effect of the introduction of the Chern-Simons ""toy model"  for topological field theory was that, 
due to its conceptual simplicity, its basic structure could be appreciated also by mathematicians not trained in theoretical physics, who would otherwise fail to see through all the  physics jargon involved in the available discussion of realistic models. Accordingly, shortly after th introduction of Chern-Simons field theory,  the first mathematically precise axiomatizations of an $n$-dimensional _[[topological field theory]]_ was proposed, by [[Michael Atiyah]]: "[[functorial quantum field theory]]".

This axiomatization demands, in particular, for each [[closed manifold]] of [[dimension]] $(n-1)$ the assignment of a vector space

$$
  \Sigma_{n-1} \mapsto Z(\Sigma_{n-1}) \in \mathrm{Vect}
$$

thought of as the _[[space of physical states]]_ of the theory on the
spatial slice $\Sigma_{n-1}$ of spacetime. 

This axiomatization did not capture the full notion of _[[local quantum field theory|local]]_ theories: the space of states are assigned globally to a space $\Sigma_{n-1}$ and is not required to be obtained by "integrating up local data" over $\Sigma_{n-1}$. 

In order to refine this, one cleraly wants an axiomatization of field theory that assigns data also to manifolds $\Sigma_{k}$ of [[dimension]] $0 \leq k \leq n$. This should be such that the data to a torus $\Sigma_{k} \times S^1$ is the [[trace]] in a suitable sense, of the data assigned to $\Sigma_{k}$ itself. It turns out that the way to capture this is to think of $Z(\Sigma_k)$ as being a vector space in [[higher category theory]]/[[directed homotopy type theory]]: an [[n-vector space|(n-k)-vector space]].

$$
  \Sigma_k \mapsto Z(\Sigma_k) \in (n-k)\mathrm{Vect}
$$

That something like this should work was hypothetized as the [[cobordism hypothesis]], the formulation was later given by [[Jacob Lurie]]. In the literature the resulting axiomatization is called _[[extended topological field theory]]_ (with "extended" referring to extending the axioms from [[codimension]] 1 to higher codimension ) or _[[multi-tiered field theory]]_ (thinking of the data in higher [[codimension]] as being higher "tieres" of the theory). But in the [[physics]]-community there is also the well-established of _[[local quantum field theory]]_ which is meant to refer to what the axioms of "extended TQFT" capture. Hence we should think of this as formalizing _topological local field theory_.


### Topological local *Lagrangian* field theory in higher geometry
 {#TopologcalLocalLagrangianFieldTheoryInHigherGeometry}

The formalization of [[extended topological field theory]] thus captures the [[local quantum field theory|local]] aspect of [[field (physics)|field]] [[theory (physics)|physics]]. But we saw [above](#TopologicalLocalLagrangianGaugeFieldTheory) that the theories of fundamental physics have one more crucial property: they are _[[Lagrangian]]_. Here we indicate how to formulate Lagrangian theories that are also local in the sense of [[extended field theory]].

For a 1-tiered thery the traditional answer is given by the formalization of the notion of _[[quantization]]_ known as _[[geometric quantization]]_. This considers a [[complex line bundle]] on the space of fields over $\Sigma_{n-1}$ (or rather on the space of fields on $\Sigma_{n-1} \times [0,1]$ which satisfy the [[equations of motion]]: the _[[phase space]]_) called the [[prequantum line bundle]] and then identifies the physical states with _half_ of the [[sections]] of this line bundle: the _[[wave functions]]_.

$$
  Z(\Sigma_{n-1}) 
  \coloneqq
  \{wave\; functions\}
  \coloneqq
  \left\{
    polarized\;sections\;of\;prequantum\;line\;bundle
  \right\}
  \,.
$$

In order to refine this to local (extended, multitiered) 
[[prequantum field theory]] we need [[circle n-bundle with connection|higher line bundles]].

| | | [[extended prequantum field theory|local/extended Lagrangian field theory]] |  | [[extended quantum field theory|local/extended quantum field theory]]  |
|--|--|--|--|--|
| closed piece of [[spacetime]] of [[dimension]] $0 \leq k \leq n$ |  [[prequantum field theory]] | [[prequantum n-bundle|prequantum (n-k)-bundle]] | [[geometric quantization]] | [[space of states|space of]] $(n-k)$-[[wave functions]] |
| [[closed manifold]] of [[dimension]] $0 \leq k \leq n$ | $\stackrel{local\;prequantum\;field\;theory}{\mapsto}$ | [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on [[moduli stack]] of [[field (physics)|field configurations]] | $\stackrel{polarized\; sections}{\mapsto}$ | [[n-vector space|(n-k)-vector space of states]] | 
| $\Sigma_k$ | $\mapsto$ | $\exp(2 \pi i \int_{\Sigma_k}[\Sigma_k,\mathbf{L}]) : [\Sigma_k, \mathbf{Fields}] \to \mathbf{B}^{n-k} U(1)_{conn}$ | $\mapsto$ | $Z(\Sigma_{n-k})$ |



For [[Chern-Simons theory]] notice

$$
  H^4(BG , \mathbb{Z}) \simeq \mathbb{Z}
$$

(...)

$$
  c : B G \to  B^3 U(1) \simeq K(\mathbb{Z},4)
  \,.
$$

| [[dimension]] |  | [[prequantum n-bundle|prequantum (3-k)-bundle]] |  |
|---------------|--|-------------------------------------------------|--|
| $k = 0$ | [[twisted differential string structure|differential fractional first Pontryagin class]] | $\hat \mathbf{c} \;\colon\; \mathbf{B}G_{conn} \to \mathbf{B}^3 U(1)_{conn}$ |  ([FSS](#FSS))  |
| $k = 1$ | [[WZW model]] [[background gauge field|background]] [[B-field]] | $G \to [S^1, \mathbf{B}G_{conn}] \stackrel{[S^1, \hat \mathbf{c}]}{\to} [S^1, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{S^1} (-))}{\to} \mathbf{B}^2 U(1)_{conn}$ |  |
| $k = 2$ | off-sheff [[prequantum bundle]] | $[\Sigma_2, \mathbf{B}G_{conn}] \stackrel{[\Sigma_2, \hat \mathbf{c}]}{\to} [\Sigma_2, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_2} (-))}{\to} \mathbf{B} U(1)_{conn}$ | | 
| $k = 3$ | [[action functional]] | $[\Sigma_3, \mathbf{B}G_{conn}] \stackrel{[\Sigma_3, \hat \mathbf{c}]}{\to} [\Sigma_3, \mathbf{B}^3 U(1)_{conn}] \stackrel{\exp(2 \pi i \int_{\Sigma_3} (-))}{\to} U(1)$


Here the [[WZW model|WZW]] [[B-field]] is the topological part of a 2-dimensional local Lagrangian field theory called the _[[Wess-Zumino-Witten model]]_. One says this is 

$$
  \mathcal{CS}_3 \stackrel{dual}{\mapsto} \mathcal{WZW}_2 
$$


also standard model of this form?

unclear in detail, but for instance [[closed string field theory]] is of this form and gives 
[[Einstein-Yang-Mills theory]] under [[KK-reduction]].

also proposals for Einstein-Maxwell as certain limits of [[Chern-Simons gravity]].

This pattern is expected to continue. Witten shows that for the abelian case

$$
  \array{
    \mathcal{CS}_7 &\stackrel{dual}{\mapsto}& \mathcal{X}_6
    \\
    && \downarrow^{\mathrlap{cpt}.}
    \\
    && \mathcal{YM}_4
  }
$$

this is generalized in FSS...






### $\infty$-Chern-Simons theory as the general example

(...)

## Definition

Let $\mathbf{H}$ be an ambient [[(∞,1)-topos]], typically a [[cohesive (∞,1)-topos]] such as [[Smooth∞Grpd]] or one of its [[slice (∞,1)-topos|slices]]. For $n \in \mathbb{N}$ let $\mathbf{B}^n U(1)_{conn} \in \mathbf{H}$ be the [[moduli ∞-stack]] of [[circle n-bundles with connection]]. Let moreover $\mathbf{Fields} \in \mathbf{H}$ be the given [[moduli ∞-stack]] of [[field (physics)|field configurations]], so that for $\Sigma$ some [[worldvolume]] [[manifold]] a [[field (physics)|field]] configuration on $\Sigma$ is a map in $\mathbf{H}$ of the form

$$
  \phi \colon \Sigma \to \mathbf{Fields}
$$

a [[gauge transformation]] $\phi \Rightarrow \phi'$ is a [[homotopy]] between two such maps, and a [[higher gauge transformation]] is a higher homotopy.

Then an **extended Lagrangian** or [[prequantum n-bundle]] for an $n$-dimensional [[quantum field theory]] with fields classified by $\mathbf{Fields}$ is a map in $\mathbf{H}$ of the form

$$
  \mathbf{L}
  \;\colon\;
  \mathbf{Fields}
  \to 
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

By post-[[composition]] this sends a field $\pho \colon \Sigma_n \to \mathbf{Fields}$ to the [[circle n-bundle with connection]] on $\Sigma_n$ modulated by

$$
  \mathbf{L}(\phi)
  \;\colon\;
  \Sigma_n 
  \stackrel{\phi}{\to}
  \mathbf{Fields}
  \stackrel{\mathbf{L}}{\to}
  \mathbf{B}^n U(1)_{conn}
  \,.
$$

This is locally  -- restricted to some [[good cover]] $U \to \Sigma_n$ of $\Sigma_b$) given by a [[differential n-form]] 

$$
  L(\phi) \omega \in \Omega^n(U)
  \,,
$$

where $L(\phi) \in C^\infty(U)$ is a [[smooth function]] and where $\omega \in \Omega^n(U)$ is some [[volume form]] or some other prespecified [[measure]]. This function $L(\phi)$ is the ordinary [[Lagrangian]]. 

Over an [[orientation|oriented]] [[closed manifold]] $\Sigma_n$ of [[dimension]] $n$ the corresponding [[action functional]] is the [[transgression]] of $\mathbf{L}$ to the mapping stack/[[internal hom]] out of $\Sigma_n$, hence the composite

$$
  \exp\left(
    2\pi i \int_{\Sigma_n} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_n, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_n, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_n})(-) }{\to}
  U(1)
  \,,
$$

where the first map is the [[internal hom]] on morphisms and the second is the [[higher holonomy]] map of a [[circle n-bundle with connection]] over $\Sigma_n$, hence the [[fiber integration in ordinary differential cohomology]]. 

For $\phi : \Sigma_n \to \mathbf{Fields}$ a field such that the [[circle n-group|circle (n-1)-group]] [[principal ∞-bundle]] underlying $\mathbf{L}(\phi)$ is trivializable and trivialized, the differential form $L(\phi)\omega$ discussed above descends to $X$ itself and the [[action functional]] is simply the [[integration of differential forms]]

$$
  \phi \mapsto \exp\left(2 \pi i \int_{\Sigma_n} L(\phi) \omega \right)
  \,.
$$

This special case is the relation between [[Lagrangians]] and [[action functionals]] as traditionally considered.

Generally, for $0 \leq k \leq n$ and $\Sigma_{k}$ an oriented [[closed manifold]] of [[dimension]] $k$, transgression as above yields a map in $\mathbf{H}$ of the form

$$
  \exp\left(
    2\pi i \int_{\Sigma_k} [\Sigma_n, \mathbf{L}]
  \right)
  \;\colon\;
  [\Sigma_k, \mathbf{Fields}]
  \stackrel{[\Sigma_n, \mathbf{L}]}{\to}
  [\Sigma_l, \mathbf{B}^n U(1)_{conn}]
  \stackrel{\exp(2 \pi in \int_{\Sigma_k})(-) }{\to}
  \mathbf{B}^{n-k}U(1)_{conn}
$$

which modulates a [[circle n-bundle with connection|circle (n-k)-bundle with connection]] on the [[moduli infinity-stack]] of fields on $\Sigma_k$. At least for large classes of theories, this is the (off-shell) [[prequantum n-bundle|prequantum (n-k)-bundle]] of the theory.

## Examples

### Higher gauge theory

If $G \in Grp(\mathbf{H})$ is an [[∞-group]] (a [[smooth ∞-group]] if $\mathbf{H}$ is [[Smooth∞Grpd]]) and 

$$
  \mathbf{Fields}  
  \simeq
  \mathbf{B}G_{conn}
$$

is a [[moduli ∞-stack]] of $G$-[[principal ∞-bundle|principal]] [[connection on an ∞-bundle|∞-connections]], then the theory in question is a ([[higher gauge theory|higher]]) [[gauge theory]]. In this case the map

$$
  \mathbf{c} \;\colon\; \mathbf{B}G \to \mathbf{B}^n U(1)
$$

underlying the extended Lagrangian is a [[cocycle]] that induces an [[extension of ∞-groups]], fitting a [[homotopy fiber sequence]]

$$
  \mathbf{B}^{n-1}U(1) \to \mathbf{B}\hat G
\stackrel{}{\to} \mathbf{B}G \stackrel{\mathbf{c}}{\to} \mathbf{B}^n U(1)
  \,.
$$

In this case the extended Lagrangian also plays the role as the universal differential refinement of the [[obstruction]] class to [[lift of structure groups]] through $\hat G \to G$. More generally, its [[homotopy fiber products]] are [[moduli ∞-stacks]] of [[twisted differential c-structures]]. See there for more examples.

### Higher Chern-Simons theory

Various examples are discussed at 

* [[schreiber:∞-Chern-Simons theory]]

* [[higher dimensional Chern-Simons theory]]

  * [[1d Chern-Simons theory]]

  * [[Chern-Simons theory]]

  * [[5d Chern-Simons theory]]

  * [[7d Chern-Simons theory]]

  * [[AKSZ sigma-models]]

  * [[string field theory]]

  * [[infinite-dimensional Chern-Simons theory]]

## Related concepts

[[!include extended prequantum field theory - table]]
  


## References

Expositions, examples and further pointers are in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:Extended higher cup-product Chern-Simons theories]]_

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_

Lecture notes are in _[[geometry of physics]]_, and section 1.2 of 

* [[Urs Schreiber]], _[[schreiber:differential cohomology in a cohesive topos]]_

A general abstract discussion is in section 3 there, further discussion of examples in section 5.



[[!redirects extended Lagrangians]]




