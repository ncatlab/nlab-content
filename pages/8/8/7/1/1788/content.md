### Super Fiber functors and their automorphism supergroups
 {#FiberFunctors}

The first step in exhibiting a given [[tensor category]] $\mathcal{A}$ as being a [[category of representations]] is to exhibit its objects as having an [[forgetful functor|underlying]] representation space of sorts, and then an [[action]] represented on that space. Hence a necessary condition on $\mathcal{A}$ is that there exists a [[forgetful functor]]

$$
   \omega \;\colon\; \mathcal{A} \longrightarrow \mathcal{V}
$$

to some other [[tensor category]], such that $\omega$ satisfies a list of properties, in particular it should be a [[symmetric monoidal functor|symmetric]] [[strong monoidal functor]].

Such functors are called _[[fiber functors]]_. The idea is that we think of $\mathcal{A}$ as a [[bundle]] over $\mathcal{V}$, and over each $V \in \mathcal{V}$ we find the [[fiber]] $\omega^{-1}(V)$ of that "bundle", consisting of all those objects in $\mathcal{A}$ whose underlying object in the given $V$.

The main point of [[Tannaka duality]] of tensor categories is the observation that if $\mathcal{A}$ is a [[category of representations]] of some [[group]] $G$, then $G$ also [[action|acts]] by [[automorphisms]] on that [[fiber functor]] (i.e. via [[natural isomorphisms]] of functors). In good cases then this may be turned around, and the full [[automorphism group]] of a fiber functor identified with the group $G$ for which the objects in its fibers are [[representations]], this is the process of [[Tannaka reconstruction]].

There are slight variants on what one requires of a fiber functor. For the present purpose we fix the following definition

+-- {: .num_defn #FiberFunctor} 
###### Definition

Let $\mathcal{A}$ and $\mathcal{T}$ be two $k$-[[tensor categories]] (def. \ref{TensorCategory}) such that 

1. all [[object of finite length|objects have finite length]];

1. all [[hom spaces]] are of [[finite number|finite]] [[dimension]] over $k$.

Let $R \in CMon(Ind(\mathcal{T}))$ be a [[commutative monoid in a symmetric monoidal category|commutative monoid]] (def. \ref{MonoidsInMonoidalCategory}) in the category of [[ind-objects]] in $\mathcal{T}$ (prop. \ref{IndObjectsInATensorCategory}).  

Then a **[[fiber functor]] on $\mathcal{A}$ over $R$** is a [[functor]]

$$
  \omega \;\colon\; \mathcal{A} \longrightarrow R Mod(Ind(\mathcal{T}))
$$ 

from $\mathcal{A}$ to the [[category of modules|category of]] [[module objects]] over $R$ (def. \ref{ModulesInMonoidalCategory}) in the [[category of ind-objects]] $Ind(\mathcal{T})$ (def. \ref{IndObjectsInATensorCategory}), which is

1. a [[braided monoidal functor|braided]] [[strong monoidal functor]];

1. an [[exact functor]] in both variables.

If here $\mathcal{T} = $ [[sVect]] (def. \ref{CategoryOfSuperVectorSpaces}), then this is called a **super fiber functor**.

=--

([Deligne 02, 3.1](#Deligne02))

+-- {: .num_prop #MonoidalTransformationBetweenFiberFunctorIsIso} 
###### Proposition

every [[monoidal natural transformation]] (def. \ref{LaxMonoidalFunctor}) between two [[fiber functors]] (def. \ref{FiberFunctor}) is an [[isomorphism]] (i.e. a [[natural isomorphism]]).

=--

([Deligne 02, lemma 3.2](#Deligne02))
