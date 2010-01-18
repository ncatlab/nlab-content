
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _quasicoherent [[∞-stack]] of modules_ is the [[vertical categorification|categorification]] of that of [[quasicoherent sheaf]] of [[module]]s from the 1-[[category theory|categorical]] to the [[(∞,1)-category|(∞,1)-categorical context]].

The [[general abstract nonsense]] behind this notion is currently described a bit at [Quasicoherent modules in higher/derived context](http://ncatlab.org/nlab/show/quasicoherent+sheaf#Higher) and at [[schreiber:∞-vector bundle]]. The following describes more concrete realizations of this idea.

## Model category theoretic description

We survey some aspects of the [[model category]] theoretic description of quasicoherent $\infty$-stacks as developed in

* [[Bertrand Toen]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry I: Topos theory_ ([arXiv:0207028](http://arxiv.org/abs/math/0207028))

* [[Bertrand Toen]], [[Gabriele Vezzosi]], _Homotopical Algebraic Geometry II: geometric stacks and applications_ ([arXiv:0404373](http://arxiv.org/abs/math/0404373)).


### Setup

This uses the [[model structure on SSet-enriched presheaves]] in order to model [[derived stack]]s ([[∞-stack]]s on [[(∞,1)-category]]-sites) along the lines described at [[models for ∞-stack (∞,1)-toposes]].

So in this model an $infty$-stack is a [[simplicial presheaf]] $C^{op} \to SSet$ on a simplicial site $C$ that takes values in [[Kan complex]]es and satisfies [[descent]] with respect to [[hypercover]]s in the [[homotopy category]] of $C$.

In order to speak systematically of setups for [[derived algebraic geometry]] the authors consider setups where an affine [[generalized scheme]] is the formal dual to a commutative [[monoid]] in a fixed [[monoidal model category]] $\mathcal{C}$.

For instance 

* for $\mathcal{C} = $ [[Ab]] a monoid object in $\mathcal{C}$ is an ordinary [[ring]] and its formal dual an ordinary [[affine scheme]];

* for $\mathbb{C} = sAb$, the category of abelian [[simplicial group]]s, a monoid in $\mathcal{C}$ is a [[simplicial ring]] and its formal dual is one notion of affine [[derived scheme]]. 

### Derived $\infty$-stacks on $SSet$-sites and on model sites

A [[simplicially enriched category]] with the structure of a [[site]] is called an [[SSet-site]] ([def 3.1.1](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=18) in [ToVeI](http://arxiv.org/abs/math/0404373)). 

This may be presented by a [[model category]] with a site structure, called a pseudo [[model site]] ([def 4.1.1](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=43) in [ToVeI](http://arxiv.org/abs/math/0404373)).

The relation between the two concepts is discussed in [section 4.3](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=47) of [ToVeI](http://arxiv.org/abs/math/0404373).

The stack condition on a simplicial presheaf on an [[SSet-site]] may be expressed equivalently in terms of a simplicial presheaf on a [[model site]], using the model structure on simplicial presheaves on a model site from [theorem 4.6.1](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=53) of [ToVeI](http://arxiv.org/abs/math/0404373)).

These two model structures on simplicial presheaves are [[Quillen equivalence|Quillen equivalent]] ([theorem 4.7.1](http://arxiv.org/PS_cache/math/pdf/0207/0207028v4.pdf#page=55) in [ToVeI](http://arxiv.org/abs/math/0404373)).

There is a good structure of a [[model site]] on $C := Comm(\mathcal{C})^{op}$ (...details...).

### Quasicoherent $\infty$-stacks

For every commutative monoida $A \in \mathcal{C}$ There is naturally a [[model category]] structure on the category $A Mod$ of $A$-[[module]]s in $\mathcal{C}$.

(...general definition...)

For instance for $\mathcal{C} = SAb $ the model structure on $A Mod$ is that described at [[simplicial ring]].

Let $QC(Spec A) \subset A Mod$ be the non-full [[subcategory]] of cofibrant objects with weak equivalences between them. This yields a category-valued presheaf $QC : C^{op} \to Cat$ and by postcomposition with the [[nerve]] a [[simplicial presheaf]] $QC :C^{op} \to Cat \stackrel{N}{\to} SSet$: the simplicial presheaf of **quasicoherent modules**. 

This is [definition 1.3.7.1](http://arxiv.org/PS_cache/math/pdf/0404/0404373v7.pdf#page=96) in [ToVeII](http://arxiv.org/abs/math/0404373).

The claim now is that this presheaf is indeed an [[∞-stack]] on the [[model site]] $C := Comm(\mathcal{C})^{op}$.

This is [theorem 1.3.7.2](http://arxiv.org/PS_cache/math/pdf/0404/0404373v7.pdf#page=96) in [ToVeII](http://arxiv.org/abs/math/0404373).

