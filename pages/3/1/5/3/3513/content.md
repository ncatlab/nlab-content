
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **model structure for right fibrations** $(SSet/S)_{rfib}$ is a [[model category]] structure on the [[overcategory]] $SSet/S$ of [[simplicial set]]s over a given [[quasi-category]] $S$, that [[presentable (∞,1)-category|presents]] the [[(∞,1)-category]] of [[right Kan fibration]]s [[fibrations of quasi-categories|of quasi-categories]] over $S$

$$
  ((SSet/S)_{rfib})^\circ \simeq RFib(S)
  \,.
$$

This is the $(\infty,1)$-analog of the $(2,1)$-category $Fib_{grpd}(S)$ of [[category fibered in groupoids|categories fibered in groupoids]] over a category $S$.

Similarly there is an analogous **model structure for left fibrations** that models [[left Kan fibration]]s, i.e.  op-fibrations in [[∞-groupoid]]s

$$
  ((SSet/S)_{lfib})^\circ \simeq LFib(S)
  \,.
$$

The extension of this from right fibrations to [[Cartesian fibration]]s and from left fibrations to [[coCartesian fibration]]s is the [[model structure for coCartesian fibrations]].

The [[(∞,1)-Grothendieck construction]] relates this to the [[global model structure on functors]] that presents the [[(∞,1)-category of (∞,1)-functors]] $Fun(S,\infty Grpd)$ (for left fibrations) and $Fun(S^{op},\infty Grpd)$ (for right fibrations).

## Motivation {#Motivation}

The following [[model category]] structure is best understood with the [[(∞,1)-Grothendieck construction]] in mind, which it serves to model.

Recall from the discussion there that given a morphism $p : X \to S$ of [[quasi-categories]], the [[(∞,1)-functor]] $S^{op} \to \infty Grpd$ that the left adjoint to the Grothendieck construction extracts from it is all encoded in the [[pushout]] $X^{\triangleleft} \coprod_X S$ in

$$
  \array{
    X &\stackrel{p}{\to}& S
    \\
    \downarrow && \downarrow
    \\
    X^{\triangleleft} &\to& X^{\triangleleft} \coprod_X S
  }
  \,,
$$

where $X^\triangleleft = (*) \star X $ is the [[join of quasi-categories|join]] of $X$ with the point, i.e. $X$ with an [[initial object]] freely adjoined to it.

More discussion of why this is the case is at [Adjoints to the Grothendieck construction](http://ncatlab.org/nlab/show/Grothendieck+construction#adjunction).

The model category structure described below declares that a morphism in the [[overcategory]] $sSet/S$ is a weak equivalence if it induces a weak equivalence of the quasi-categories given by these pushouts. So this is effectively saying that we regard a morphism of right fibration of quasi-categories as a weak equivalences, if under the left adjoint to the $(\infty,1)$-Grothendieck construction it induces a weak equivalences of the $(\infty,1)$-functors that classify these fibrations.


## Definition

For $f : X \to S$ a morphism of [[simplicial set]]s, write $C^{\triangleleft}(f)$ for the [[pushout]]

$$
  \array{
    X &\hookrightarrow& X^{\triangleleft}
    \\
    \downarrow && \downarrow
    \\
    S &\to& S \coprod_{X} X^{\triangleleft} & =: C^{\triangleleft}(f) 
  }
$$

in the category [[sSet]] of simplicial sets. Call this the  **left cone** over $f$.

The [[colimit]]s in [[sSet]] are computed componentwise, so that the set of vertices $C^{\triangleleft}(f)_0$ is the disjoint union of the vertices of $S$ and one extra vertex $v$, the **cone point**.

+-- {: .num_defn}
###### Definition

([[Higher Topos Theory|HTT, def. 2.1.4.5]])


The **model structure for left fibrations** or **covariant model structure** $(sSet/S)_{lfib}$ on $SSet/S$ is given by

A morphism $f : X \to Y$ is 

* a cofibration if the underlying morphism of simplicial sets is a cofibration in the standard [[model structure on simplicial sets]], i.e. a [[monomorphism]];

* a weak equivalence if the induced morphism of cones

  $$
    X^{\triangleleft} \coprod_X S
    \to 
    Y^{\triangleleft} \coprod_Y S
  $$

  is a weak equivalence in the Joyal [[model structure for quasi-categories]], where $X^{\triangleleft}$ is the [[join of simplicial sets|join]] $X^{\triangleleft} := {*} \star X$.

=--

+-- {: .num_prop #BasicProperties}
###### Proposition


This is a 

* [[proper model category|left proper]]

* [[simplicial model category|simplicial]]

* [[combinatorial model category]].

([[Higher Topos Theory|HTT, prop 2.1.4.7, 2.1.4.8]])

We have 

* The fibrant objects are precisely the [[left fibration]]s 
  ([[Higher Topos Theory|HTT, corollary 2.2.3.12]])

* Every left anodyne morphism is an acyclic cofibration. 
  ([[Higher Topos Theory|HTT, prop 2.1.4.9]])


=--

An alternative characterization of this model structure is:

+-- {: .num_theorem #AsLocalization}
###### Theorem
The model structure for left fibrations is the left [[Bousfield localization]] of the [[model structure on an overcategory|overcategory]] model structure on $SSet/X$ induced by the [[model structure for quasicategories]] on $SSet$ at the set of maps $\{ \Lambda^n_0 \hookrightarrow \Delta^n | n\ge 0, \Delta^n \to X \}$ indexed by all the simplices of $X$.
=--

This is mentioned in [Heuts-Moerdijk](#HeutsMoerdijk13), p.5; see also [this discussion](http://nforum.ncatlab.org/discussion/915/model-structure-for-left-fibrations/?Focus=53814#Comment_53814).

## Properties

### Weak equivalences {#WeakEquivalences}

+-- {: .num_prop}
###### Proposition

Let $S$ be any [[simplicial set]]. Every morphism

$$
  \array{
    X &&\to&& Y
    \\
    & \searrow && \swarrow
    \\
    && S
  }
$$

in $sSet_S$ for which $X\to Y$ is [[left fibration|left anodyne]] is a weak equivalence in the model structure for left fibrations.

=--

This is [[Higher Topos Theory|HTT, prop. 2.1.4.6]].

+-- {: .proof}
###### Proof

Recall from <a href="http://ncatlab.org/nlab/show/right%2Fleft+Kan+fibration#PropRightAnodyne">here</a> that left anodyne morphisms are the weakly saturated class generated by the [[horn]] inclusions (i.e. under [[transfinite composition]] of [[retract]]s of [[pushout]]s). Therefore it is sufficient to check the statement for these generating morphisms.

By the definition of weak equivalences above, this means that we need to check that 

$$
  (\Lambda[n]_i)^{\triangleleft} \coprod_{\Lambda[n]_i} S
  \to
  (\Delta[n])^{\triangleleft} \coprod_{\Delta[n]_i} S
$$

is a weak equivalence in $sSet_{Quillen}$.

Observe that this is a [[pushout]] 

$$
   \array{
       \Lambda[n+1]_{i+1} &\to& (\Lambda[n]_i)^{\triangleleft} \coprod_{\Lambda^n_i} S
      \\
       \downarrow && \downarrow 
       \\
       \Delta[n+1] &\to& (\Delta[n])^{\triangleleft} \coprod_{\Delta^n} S
   }
$$

of the [[inner fibration|inner anodyne morphism]] $\Lambda[n+1]_{i+1} \to \Delta[n+1]$ and therefore a weak equivalence.

To illustrate the above pushout property set $n = 2$ for example. Start with a 2-simplex $\sigma$ in $S$. Then $(\Delta^2)^{\triangleleft} \coprod_{\Delta^2} S$ is the original simplicial set $S$ together with a tetrahedron $\Delta^3$ built over $\sigma$. One face of the tetrahedron is the original 2-simplex $\sigma$ in $S$, the three others "stick out" of $S$:

The simplicial set $(\Lambda^2_1)^{\triangleleft} \coprod_{\Lambda^2_1} S$ is accordingly the simplicial set $S$ with only two of the three faces of this tetrahedron over $\sigma$ erected.

The map $(\Lambda^3_2) \to (\Delta^2)^{\triangleleft} \coprod_{\Delta^2} S $ identifies the horn of this tetrahedron given by these two new faces and the original face $\sigma$.

The pushout therefore glues in the remaining face of the tetrahedron and fills it with a 3-cell.

=--


### Change of base 
 {#ChangeOfBase}

For every morphism $j : S \to S'$ we have the corresponding [[adjunction]] on [[overcategories]]

$$
  (j_! \dashv j^*)
  :
  sSet/S \stackrel{\overset{f_!}{\to}}{\underset{j^*}{\leftarrow}}
  sSet/{S'}
  \,,
$$

where

* $j_!$ is given by postcomposition of $j$;

* $j^*$ is given by [[pullback]] along $j$.



+-- {: .num_prop}
###### Proposition
**(change of base)**

This is a [[Quillen adjunction]] with respect to the model structures 
for left fibrations over $S$ and $S'$, respectively. ([[Higher Topos Theory|HTT, prop. 2.1.4.10]])

If $j$ is a [[model structure for quasi-categories|weak equivalence in]] $sSet_{Joyal}$, then this is a [[Quillen equivalence]]. ([[Higher Topos Theory|HTT, remark. 2.1.4.11]])


=--

### Grothendieck construction
 {#GrothendieckConstruction}

+-- {: .num_prop}
###### Proposition
**($(\infty,1)$-Grothendieck construction)**

For $C$ a [[simplicially enriched category]] and $S = N(C)$ its [[homotopy coherent nerve]], there is a [[Quillen equivalence]]

$$
  (sSet/S)_{lfib} \stackrel{\leftarrow}{\to}
  [C, sSet_{Quillen}]
$$

between the model structure for left fibrations over $S$ and the [[global model structure on functors|global model structure on sSet-functors]] on $C$ with values in [[sSet]] equipped with the standard [[model structure on simplicial sets]].

=--

For more on this see [[(∞,1)-Grothendieck construction]].

## Related concepts

The [[operad|operadic]] generalization is the

* [[model structure for dendroidal left fibrations]].


## References

This is the content of section 2.1.4 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

There the model structure $(sSet/S)_{lfib}$ is called the **covariant model structure** and the model structure $(sSet/S)_{rfib}$  the **contravariant model structure**.

The alternative construction as a localization is mentioned in

* {#HeutsMoerdijk13} [[Gijs Heuts]], [[Ieke Moerdijk]], _Left fibrations and homotopy colimits_, Mathematische Zeitschrift **279** (2015) 723–744 &lbrack;[doi:10.1007/s00209-014-1390-7](http://dx.doi.org/10.1007/s00209-014-1390-7), [arXiv:1308.0704](http://arxiv.org/abs/1308.0704)&rbrack;

* [[Gijs Heuts]], [[Ieke Moerdijk]], *Left fibrations and homotopy colimits II* &lbrack;[arXiv:1602.01274](https://arxiv.org/abs/1602.01274)&rbrack;

Further discussion:

* {#Stevenson15} [[Danny Stevenson]], *Covariant Model Structures and Simplicial Localization*, North-West. Eur. J. Math. **3** (2017) 141-202 &lbrack;[arXiv:1512.04815](http://arxiv.org/abs/1512.04815)&rbrack;


[[!redirects model structure for right fibrations]]
[[!redirects covariant model structure]]
[[!redirects contravariant model structure]]
