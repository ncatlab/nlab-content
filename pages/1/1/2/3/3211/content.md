
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _quasicoherent [[∞-stack]] of modules_ is the anlog in [[(∞,1)-topos theory]] of the notion of [[quasicoherent sheaf]] in [[topos theory]]. 

A quasicoherent sheaf on a [[scheme]] $X$ is is equivalently a morphism of [[stack]]s $X \mapsto Mod$ into the canonical stack [[Mod]] $ : Spec A \mapsto A Mod$ of [[module]]s, which corresponds to the [[bifibration]] $Mod \to CRing$ over the category of commutative rings/algebras: this is the [[tangent category]] of [[CRing]].

This general abstract description of quasi-coherent sheaves has a fairly direct generalization to [[(∞,1)-topos theory]] over arbitrary [[(∞,1)-site]]s:

for $C$ any [[(∞,1)-site]], the [[tangent (∞,1)-category]] $T (C^{op}) \to C^{op}$ is the [[Cartesian fibration|bifibration]] whose [[fiber]]s over an object $A \in C^{op}$ plays the role of the [[∞-groupoid]] of [[module]]s over $A$. Under the [[(∞,1)-Grothendieck construction]] this corresponds to an [[(∞,1)-presheaf]] $\infty Mod : C^{op} \to \infty Cat$

$$
  \infty Mod : Spec R \mapsto Stab( C^{op}/R )
$$

or directly in terms of test spaces $U$: 

$$
  \infty Mod : U \mapsto Stab( U/C )
  \,.
$$


For the special case that $C = (sAlg^{op})^\circ$ [[opposite (∞,1)-category]] presented by the [[model structure on simplicial algebras]] over a characteristic 0 ground field we have (with example 8.6 of _[[Stable ∞-Categories]]_ ) this reproduces the notion of quasicoherent $\infty$-stack as considered in [[dg-geometry]].


## Definition

+-- {: .un_defn}
###### Definition

For $C$ an [[(∞,1)-site]] let the [[(∞,1)-functor]]

$$
  Mod_C : C^{op} \to (\infty,1)Cat
$$

be that corresponding under the [[(∞,1)-Grothendieck construction]] to the [[tangent (∞,1)-category]] $T C^{op} \to C^{op}$.


=--

Let $\mathbf{H} := Sh_{(\infty,1)}(C)$ be the [[(∞,1)-category of (∞,1)-sheaves]] over $C$. Notice that this sits inside $[C^{op}, (\infty,1)Cat]$.

+-- {: .un_defn}
###### Definition

For $X \in \mathbf{H}$, the **$(\infty,1)$-category of quasi-coherent $\infty$-stacks on $X$ is the [[(∞,1)-category of (∞,1)-functors]]

$$
  QC(X) := [C^{op}, (\infty,1)Cat](X, Mod)
  \,.
$$

=--


## Model category theoretic presentation

For [[derived geometry]] modeled on formal duals of [[algebras over an operad]], the [[model category]] presentation of quasi-coherent $\infty$-stacks is locally given by a [[model structure on modules over an algebra over an operad]].

The following considers the special case of the [[commutative operad]].

### For commutative monoids

Let $\mathcal{C}$ be a [[monoidal model category]]. Write $CMon(\mathcal{C})$ for the category of [[commutative monoid]]s in $\mathcal{C}$.

For instance 

* for $\mathcal{C} = $ [[Ab]] a monoid object in $\mathcal{C}$ is an ordinary [[ring]] and its formal dual an ordinary [[affine scheme]];

* for $\mathcal{C} = sAb$, the category of abelian [[simplicial group]]s, a monoid in $\mathcal{C}$ is a [[simplicial ring]] and its formal dual is one notion of affine [[derived scheme]]. 

In ([To&#235;nVezzosi, I](To&#235;nVezzosiI), [To&#235;nVezzosi, II](#To&#235;nVezzosiII)) are discussed structures of a [[model site]]/[[sSet-site]] on $CMon(\mathcal{C})$.

For every commutative monoid $A \in \mathcal{C}$ There is naturally a [[model category]] structure on the category $A Mod$ of $A$-[[module]]s in $\mathcal{C}$.


(...)

Let $[C^{op},sSet]_{proj,loc}$ the local [[model structure on sSet-presheaves]] that [[presentable (∞,1)-category|presents]] the [[(∞,1)-category of (∞,1)-sheaves]]/[[∞-stack]]s on $C$

$$
  ([C^{op}, sSet]_{proj,loc})^\circ \simeq \mathbf{H} := Sh_{(\infty,1)}(C)
  \,.
$$


as described as [[models for ∞-stack (∞,1)-toposes]].

So in this model an $\infty$-stack is a [[simplicial presheaf]] $C^{op} \to SSet$ on a simplicial site $C$ that takes values in [[Kan complex]]es and satisfies [[descent]] with respect to [[hypercover]]s in the [[homotopy category]] of $C$.


+-- {: .un_defn}
###### Definition

The [[simplicial presheaf]] of **quasicoherent $\infty$-stacks** is

$$
  QC : C^{op} \to sSet
$$

is given by

$$
  QC : Spec A \mapsto N( A Mod_{cof, \sim} )
  \,,
$$ 

where on the right we have the [[nerve]] of the non-full [[subcategory]] of the model category $A Mod$ on cofibrant objects and weak equivalences between them. 

=--

This appears as ([To&#235;nVezzosiII, definition 1.3.7.1](#ToenVezzosiII).

+-- {: .un_prop}
###### Proposition

This $QC$ is indeed an [[∞-stack]] on the [[model site]] $C := Comm(\mathcal{C})^{op}$ 

=--

This is ([To&#235;nVezzosiII, theorem 1.3.7.2](#ToenVezzsoi).

> notice: the $QC$ defined this way is not yet stabilized

## Related concepts

* [[quasicoherent sheaf]]

* **quasicoherent $\infty$-stack**

## References

The general discussion of the [[tangent (∞,1)-category]] is in

* [[Jacob Lurie]], _[[Deformation Theory]]_ .

The model category theoretic presentation over model sites of commutative monoids is discussed in

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv:0207028](http://arxiv.org/abs/math/0207028))
{#ToenVezzosiI}

* [[Bertrand Toën]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv:0404373](http://arxiv.org/abs/math/0404373))
{#ToenVezzosiII}

A discussion specific to [[dg-geometry]] with an emphasis on the [[geometric ∞-function theory]] of quasicoherent $\infty$-stacks over [[perfect ∞-stack]]s is in 

* [[David Ben-Zvi|Ben-Zvi]], [[John Francis]],  [[David Nadler]], _Integral transforms and Drinfeld centers in derived algebraic geometry_ ([arXiv](http://arxiv.org/abs/0805.0157))
{#Ben-ZviFrancisNadler}



[[!redirects quasicoherent ∞-stack]]
[[!redirects quasicoherent ∞-stacks]]
[[!redirects quasicoherent infinity-stacks]]

[[!redirects quasicoherent (∞,1)-sheaf]]
[[!redirects quasicoherent (∞,1)-sheaves]]
[[!redirects quasicoherent (infinity,1)-sheaf]]
[[!redirects quasicoherent (infinity,1)-sheaves]]
