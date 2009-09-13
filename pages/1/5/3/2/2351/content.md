## Idea 

A cartesian bicategory is a bicategory with properties that make it behave like a bicategory of generalized relations. The bicategory of relations of a regular category, the bicategory of spans in a finitely complete category, and the bicategory of modules (profunctors) in a finitely complete category are all examples of cartesian bicategories. 

The rough idea is that a cartesian bicategory, viewed as an abstract bicategory of relations, should possess a tensor product which behaves like cartesian product on relations, and therefore as a categorical product for relations that are "functional". The structure of such a tensor is property-like (is uniquely specifiable in terms of properties). A cartesian bicategory is like an allegory, but is more general insofar as it embraces cases like $Span$ and $Mod$. 

The original idea, due to Carboni and Walters, clearly envisioned these various examples but was initially confined to the locally posetal case; in part this was due to the lack at the time (circa 1987) of a solid theory of symmetric monoidal bicategories. In more recent years a full bicategorical treatment has been given, due principally to Carboni, Kelly, Verity, and Wood. The alternative treatment which we give below has not yet appeared in the literature as far as this author ([[Todd Trimble]]) is aware. 

## Technical preliminaries

We work with familiar notions of bicategory but in some cases under new names. Our notion of morphism between bicategories has gone under various names: "homomorphism" in the sense of B&#233;nabou, also known as "pseudofunctor" or weak 2-functor, where the structural constraints are isomorphisms. Here they are simply called **2-functors**. 

Each bicategory $B$ gives rise to a hom 2-functor $hom: B^{op} \times B \to Cat$, which we denote by $B(-, -)$, with the contravariant argument in the first place as is customary. 

Given 2-functors $F, G: B \to C$, it is for our purposes convenient to use the [[lax natural transformation|lax notion of morphism]] $\theta: F \to G$ between 2-functors for which the structural cells $\theta \cdot f$ (for 1-cells $f: a \to b$ in $B$) point in the direction 

$$\array{
F a & \overset{\theta a}{\to} & G a\\
F f \downarrow & \overset{\theta \cdot f}{\Rightarrow} & \downarrow G f\\
F b & \underset{\theta b}{\to} & G b
}$$ 

These are called "oplax transformations" by B&#233;nabou and "lax transformations" by other authors such as Johnstone; on this page we will simply call them **transformations**. A transformation is **strong** if the structural cells $\theta \cdot f$ are isomorphisms. 

There is a well-known notion of morphism between transformation which has been called [[modification]]. We retain this usage, but note that for the purposes of higher category theory, it is probably ill-advised to invent a new term (e.g. "perturbation" between modifications) each time we reach a new depth of morphism -- a more uniform terminology is called for. The term "transfor" has been gaining some recent currency; modifications may also be called **2-transfors**. 

Given bicategories $B$ and $C$, we have then a bicategory of 2-functors, strong transformations and modifications from $B$ to $C$; this will be denoted $Hom_s(B, C)$. We have also the bicategory of 2-functors, transformations, and modifications; this will be denoted $Hom_l(B, C)$. 

A **2-adjunction** $F \dashv G$ consists of 2-functors $F: B \to C$, $G: C \to B$, and an adjoint equivalence 

$$C(F -, -) \simeq B(-, G -)$$ 

in the bicategory $Hom_s(B^{op} \times C, Cat)$. In more elementary terms, the data of a 2-adjunction is given by strong transformations 

[...]

Let $B$ be a bicategory. By definition, a *map* in $B$ is a 1-cell in $B$ that possesses a right adjoint. They should be thought of as "functional relations". We let $Map(B)$ be the locally full sub-bicategory whose 0-cells are those of $B$ and whose 1-cells are the maps in $B$. 

