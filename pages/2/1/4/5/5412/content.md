
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topos Theory
+-- {: .hide}
[[!include topos theory - contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

For $\mathcal{T}$ a [[topos]] and $X \in \mathcal{T}$ any [[object]] the [[over category]] $\mathcal{T}/X$ -- the **slice topos** or **over-topos** -- is itself a topos: the "big [[little topos]]" incarnation of $X$.  This fact is sometimes called the "Fundamental Theorem of Topos Theory".

## Definition / Existence
 {#Definition}

+-- {: .num_prop}
###### Proposition

For $\mathcal{T}$ a [[topos]] and $X \in \mathcal{T}$ any [[object]], the [[slice category]] $\mathcal{T}_{/X}$ is itself again a [[topos]].

=--

A proof is spelled out for instance in [MacLane-Moerdijk, IV.7 theorem 1](#MacLaneMoerdijk). In particular we have

+-- {: .num_prop}
###### Proposition

If $\Omega \in \mathcal{T}$ is the [[subobject classifier]] in $\mathcal{T}$, then the [[projection]] $\Omega \times X \to X$ regarded as an object in the slice over $X$ is the subobject classifier of $\mathcal{T}_{/X}$.

=--

## Properties

### &#201;tale geometric morphism {#EtaleGeometricMorphism}

+-- {: .num_prop}
###### Proposition

For $\mathcal{T}$ a [[Grothendieck topos]] and $X \in \mathcal{T}$ any object, the canonical projection functor $X_! : \mathcal{T}/X \to \mathcal{T}$ is part of an [[essential geometric morphism]]

$$
  (X_! \dashv X^* \dashv X_*)
  : 
  \mathcal{T}/X \stackrel{\overset{X_!}{\to}}{\stackrel{\overset{X^*}{\leftarrow}}{\underset{X_*}{\to}}}
  \mathcal{T}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The functor $X^*$ is given by taking the [[product]] with $X$:

$$
  X^* : K \mapsto (p_2 : K \times X \to X)
  \,,
$$

since [[commuting diagram]]s

$$
  \array{
    A &&\to&& K \times X
    \\
    & \searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

are evidently uniquely specified by their components $A \to K$.

Moreover, since in the Grothendieck topos $\mathcal{T}$ we have [[universal colimits]], it follows that $(-) \times X$ preserves all [[colimit]]s. Therefore by the [[adjoint functor theorem]] a further [[right adjoint]] $X_*$ exists. 

=--

+-- {: .num_remark}
###### Remark

One also says that $X_!$ is the _[[dependent sum]]_ operation and $X_*$ the [[dependent product]] operation. As discussed there, this can be seen to compute spaces of [[section]]s of [[bundles]] over $X$.

Moreover, in terms of the [[internal logic]] of $\mathcal{T}$ the functor $X_!$ is the _[[existential quantifier]]_ $\exists$ and $X_*$ is the _[[universal quantifier]]_ $\forall$.

=--


+-- {: .num_defn}
###### Definition

A [[geometric morphism]] $\mathcal{E} \to \mathcal{T}$ equivalent to one of the form $(X_! \dashv X^* \dashv X_*)$ is called an
**[[etale geometric morphism]]**.

=-- 

More generally:

+-- {: .num_prop #GeneralEtaleGeometricMorphism}
###### Proposition

For $\mathcal{E}$ a [[Grothendieck topos]] and $f : X \to Y$ a [[morphism]] in $\mathcal{E}$,
there is an induced [[essential geometric morphism]]

$$
  (f_! \dashv  f^* \dashv f_*)
  :
  \mathcal{E}/X
    \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  \mathcal{E}/Y
  \,,
$$

where $f_!$ is given by postcomposition with $f$ and $f^*$ by [[pullback]] along $X$.

=--

+-- {: .proof}
###### Proof

By [[universal colimit]]s in $\mathcal{E}$ the [[pullback]] functor $f^*$ preserves both [[limit]]s and [[colimit]]s. By the [[adjoint functor theorem]] and using that the over-toposes are [[locally presentable categories]], this already implies that it has a [[left adjoint]] and a [[right adjoint]]. That the left adjoint is given by postcomposition with $f$ follows from the universality of the pullback: for $(a : A \to X)$ in $\mathcal{E}/X$ and $(b : B \to Y)$ in $\mathcal{E}/Y$ we have unique factorizations

$$
  \array{
    A &\to& X \times_X B &\to& B
    \\
    &{}_{\mathllap{a}}\searrow& \downarrow^{\mathrlap{f^*(b)}} && \downarrow^{\mathrlap{b}}
    \\
    && X &\stackrel{f}{\to}& Y
  }
$$

in $\mathcal{E}$, hence an isomorphism

$$
  \mathcal{E}/Y(f_*(A \to X), (B \to Y)) \simeq
  \mathcal{E}/X((A \to X), f^*(B \to Y))
  \,.
$$


=--

### Presheaf over-topos {#PresheafOverTopos}

We discuss special properties of over-[[presheaf toposes]].

Let $C$ be a [[small category]], $c$ an [[object]] of $C$ and let $C/c$ be the [[over category]] of $C$ over $c$. 

Write

* $PSh(C/c) = [(C/c)^{op}, Set]$ for the [[category of presheaves]] on $C/c$ 

* and write $PSh(C)/Y(y)$ for the [[over category]] of [[presheaf|presheaves]] on $C$ over the presheaf $Y(c)$, where $Y : C \to PSh(c)$ is the [[Yoneda embedding]]. 

+-- {: .num_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  e : PSh(C/c) \stackrel{\simeq}{\to} PSh(C)/Y(c)
  \,.
$$

=--


+-- {: .proof}
###### Proof

The functor $e$ takes $F \in PSh(C/c)$ to the presheaf
$F' : d \mapsto \sqcup_{f \in C(d,c)} F(f)$ which is equipped with the natural transformation $\eta : F' \to Y(c)$ with component map 

$$
  \eta_d : \sqcup_{f \in C(d,c)} F(f) \to C(d,c)
  : ((f \in C(d,c), \theta \in F(f)) \mapsto f
  \,.
$$

A weak inverse of $e$ is given by the functor 
$$
  \bar e : PSh(C)/Y(c) \to PSh(C/c)
$$
which sends $\eta : F' \to Y(c)$ to $F \in PSh(C/c)$ given by
$$
  F : (f : d \to c) \mapsto F'(d)|_c
  \,,
$$
where $F'(d)|_c$ is the [[pullback]]
$$
  \array{
     F'(d)|_c &\to& F'(d)
     \\
     \downarrow && \downarrow^{\eta_d}
     \\
     pt &\stackrel{f}{\to}& C(d,c)
  }
  \,.
$$ 

=--

+-- {: .num_lemma}
###### Example

Suppose the presheaf $F \in PSh(C/c)$ does not actually depend on the morphisms to $c$, i.e. suppose that it factors through the forgetful functor from the [[over category]] to $C$:
$$
  F : (C/c)^{op} \to C^{op} \to Set
  \,.
$$

Then
$
  F'(d) = \sqcup_{f \in C(d,c)} F(f)
  = \sqcup_{f \in C(d,c)} F(d)
  \simeq
  C(d,c) \times F(d) 
$
and hence $F ' = Y(c) \times F$ with respect to the [[closed monoidal structure on presheaves]].

=--

### Geometric morphisms by slicing {#GeometricMorphismBySlicing}

+-- {: .num_prop #SliceGeometricMorphism}
###### Proposition

For $(f^* \dashv f_*) : \mathcal{T} \to \mathcal{E}$ a [[geometric morphism]] of toposes and $X \in \mathcal{E}$ any [[object]], there is an induced geometric morphism between the slice-toposes

$$
  (f^*/X \dashv f_*) : \mathcal{T}/f^*X \to \mathcal{E}/X
  \,,
$$

where the [[inverse image]] $f^*/X$ is the evident application of $f^*$ to diagrams in $\mathcal{E}$.

=--

+-- {: .proof}
###### Proof

The slice adjunction $(f^*/X \dashv f_*/X)$ is discussed  <a href="http://ncatlab.org/nlab/show/adjoint+(infinity%2C1)-functor#OnSlices">here</a>: the [[left adjoint]] $f^*/X$ is the evident induced functor. Since <a href="http://ncatlab.org/nlab/show/limit+in+a+quasi-category#InOvercategories">limits in an over-category</a> $\mathcal{E}/X$ are computed as limits in $\mathcal{E}$ of diagrams with a single bottom element $X$ adjoined, $f^*/X$ preserves finite limits, since $f^*$ does, so that $(f^*/X \dashv f_*/X)$ is indeed a [[geometric morphism]].

=--

### Topos points {#Points}

We discuss [[point of a topos|topos points]] of over-toposes.


+-- {: .num_prop}
###### Observation

Let $\mathcal{E}$ be a [[topos]], $X \in \mathcal{E}$ an [[object]] and 

$$
  (e^* \dashv e_*)  : Set \to \mathcal{E}
$$

a [[point of a topos|point]] of $\mathcal{E}$. Then for every element $x \in e^*(X)$ there is a point of the slice topos $\mathcal{E}/X$ given by the composite

$$
  (e,x)
  :
  Set \stackrel{\overset{x^*}{\leftarrow}}{\underset{x_*}{\to}}
  Set/e^*(X) 
  \stackrel{\overset{e^*/X}{\leftarrow}}{\underset{e_*/X}{\to}}
  \mathcal{E}/X
  \,.
$$

=--

Here $(e^*/X \dashv e_*/X)$ is the slice geometric morphism of $e$ over $X$ discussed [above](SliceGeometricMorphism) and $(x^* \dashv x_*)$ is the &eacute;tale geometric morphism discussed [above](GeneralEtaleGeometricMorphism) induced from the morphism 
$* \stackrel{x}{\to} e^*(X)$.

Hence the [[inverse image]] of $(e,x)$ sends $A \to X$ to the [[fiber]] of $e^*(A) \to e^*(X)$ over $x$.

+-- {: .num_prop}
###### Corollary

If $\mathcal{E}$ has [[point of a topos|enough point]]s then so does the slice topos $\mathcal{E}/X$ for every $X \in \mathcal{E}$.

=--

+-- {: .proof}
###### Proof

That $\mathcal{E}$ has enough points means that a morphism $f : A \to B$ in $\mathcal{E}$ is an [[isomorphism]] precisely if for every [[point of a topos|point]] $e : Set \to \mathcal{E}$ the function $e^*(f) : e^*(A) \to e^*(B)$ is an isomorphism.

A morphism in the slice topos, given by a diagram

$$
  \array{
     A &&\stackrel{f}{\to}&& B
     \\
     & \searrow && \swarrow
     \\
     && X
  }
$$

in $\mathcal{E}$ is an isomorphism precisely if $f$ is. By the above observation we have that under the [[inverse image]]s of the slice topos points $(e,x \in e^*(X))$ this maps to the fibers of

$$
  \array{
     e^*(A) &&\stackrel{e^*(f)}{\to}&& e^*(B)
     \\
     & \searrow && \swarrow
     \\
     && e^*(X)
  }
$$

over all points $* \stackrel{x}{\to} e^*(X)$. Since in [[Set]] every object $S$ is a [[coproduct]] of the point indexed over $S$, $S \simeq \coprod_S *$ and using [[universal colimits]] in $S$, we have that if $x^* e^*(f)$ is an isomorphism for all $x \in e^*(X)$ then $e^*(f)$ was already an isomorphism.

The claim the follows with the assumption that $\mathcal{E}$ has enough points.

=--


## Related concepts

* [[over-category]] 

  * [[slice category]] 

  * [[under category]] 

  * **over-topos**


* [[over (∞,1)-category]],

  * [[model structure on an over category]] 

  * [[over-(∞,1)-topos]]

## References

Section IV.7 of 

* [[Saunders MacLane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_
 {#MacLaneMoerdijk}

[[!redirects over topos]]
[[!redirects over toposes]]
[[!redirects over-toposes]]
[[!redirects over topoi]]
[[!redirects over-topoi]]
[[!redirects slice topos]]
[[!redirects slice toposes]]
[[!redirects slice topoi]]
