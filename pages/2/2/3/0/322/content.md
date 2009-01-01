## The idea ## 

An _operad_ is a gadget used to describe algebraic theories internally in categories beyond $Set$. It is like a Lawvere [[algebraic theory]] in that it deals with theories defined by finitary operations, but unlike Lawvere theories, operads can be applied to general symmetric monoidal categories where the tensor product might not be the cartesian product. 

Actually the notion of operad (and allied notions such as [[prop]], [[club]], [[multicategory]] and so on) come in many flavors. Originally used in algebraic topology to provide a systematic formalism for describing the internal operations which exist on iterated loop spaces, the basic idea is quite flexible and adaptable to many categorical situations, and the importance of operads continues to grow. 

## The definition ## 

The original definition is due to J.P. May and was given in his book _The Geometry of Iterated Loop Spaces_. We outline here an efficient one-sentence definition first worked out by G.M. Kelly, after a few preliminaries which are important in their own right. 

1. Let $\mathbb{P}$ be the groupoid of finite cardinals and bijections thereon. Since $\mathbb{P}$ is the underlying groupoid of the category $Fin$ of finite cardinals and functions between them, the tensor product given by the coproduct on $Fin$ restricts to a symmetric monoidal product on $\mathbb{P}$. Under this symmetric monoidal structure, $\mathbb{P}$ may be characterized as the free symmetric strict monoidal category on one generator. 

1. The symmetric monoidal product on $\mathbb{P}$ extends along the Yoneda embedding to a symmetric monoidal product $F \otimes G$ on the category $Set^{\mathbb{P}^{op}}$ of presheaves on $\mathbb{P}$; this is an instance of [[day convolution|Day convolution]]. The [[presheaf]] category is cocomplete, and Day convolution is cocontinuous in each of its separate arguments $F, G$; we say in that case that $Set^{\mathbb{P}^{op}}$ is symmetric monoidally cocomplete. 

$\mathbb{P}$ is also a skeleton of the category $FB$ of finite sets and bijections; a functor $FB^{op} \to Set$ (or what is more or less the same thing, a functor $FB \to Set$) is called a [[species]]. The Day convolution product on the category of species may be described by the rule 

$$(F \otimes G)[S] = \sum_{S = T + U} F[T] \times G[U]$$ 

where the sum is over all ways of partitioning the finite set $S$ into two (possibly empty) parts. 

1. According to the yoga of presheaf categories and Day convolution, given a symmetric monoidally cocomplete category $D$, a symmetric monoidal functor 
$$X: \mathbb{P} \to D$$
extends uniquely up to isomorphism to a symmetric monoidal _cocontinuous_ functor 
$$\hat{X}: Set^{\mathbb{P}^{op}} \to D,$$ 
taking a presheaf $F: \mathbb{P}^{op} \to Set$ to the [[weighted limit|weighted colimit]] $F \otimes_X D$. Putting items 1. and 2. together, we may therefore describe $Set^{\mathbb{P}^{op}}$ up to equivalence as the free symmetric monoidally cocomplete category on a single generator. 

[To be continued...]