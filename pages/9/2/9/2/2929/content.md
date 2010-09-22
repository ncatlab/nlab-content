# Bicategories of relations
* tic
{: toc}


## Idea

A *bicategory of relations* is a [[(1,2)-category]] which behaves like the 2-category of internal [[relations]] in a [[regular category]].  The notion is due to Carboni and Walters.


## Definition

[Note: in this article, the direction of composition is diagrammatic (i.e., "anti-Leibniz"). 

A **bicategory of relations** is a [[cartesian bicategory]] which is [[locally posetal 2-category|locally posetal]] and moreover in which for every object $X$, the [[diagonal morphism|diagonal]] $\Delta\colon X\to X\otimes X$ and [[codiagonal]] $\nabla\colon X\otimes X\to X$ satisfy the [[Frobenius condition]]:
$$\nabla\Delta = (1\otimes \Delta)(\nabla \otimes 1).$$

Of course, in the locally posetal case the definition of cartesian bicategory simplifies greatly: it amounts to a symmetric monoidal [[Pos]]-[[enriched category]] for which every object carries a commutative [[comonoid]] structure, for which the structure maps $\Delta_X: X \to X \otimes X$, $\varepsilon_X: X \to 1$ are [[left adjoint]] 1-morphisms, and for which every morphism $R: X \to Y$ is a colax morphism of comonoids in the sense that the following inequalities hold: 

$$R \Delta_Y \leq \Delta_{X \otimes X} (R \otimes R), \qquad R \varepsilon_Y \leq \varepsilon_X.$$

We remark that such structure is unique when it exists (being a cartesian bicategory is a property of, as opposed to structure on, a bicategory). The [[tensor product]] $\otimes$ behaves like the ordinary product of [[relation]]s. Note this is not a cartesian product in the sense of the usual universal property; nevertheless, it is customary to write it as a product $\times$, and we follow this custom below. It does become a cartesian product if one restricts to the subcategory of left adjoints (called _maps_), which should be thought of as functional relations. 

We record a few consequences of this notion. 

+-- {: .un_prop} 
######Proposition 
(Separability condition) $\Delta\nabla = 1$.
=-- 

+-- {: .proof} 
######Proof
In one direction, we have the 2-cell $1 \leq \Delta\nabla$ which is the unit of the adjunction $\Delta \dashv \Delta_* = \nabla$. In the other direction, there is an adjunction $\varepsilon \dashv \varepsilon_*$ between the counit and its dual, and the unit of this adjunction is a 2-cell $1 \leq \varepsilon\varepsilon_*$, from which we derive 

$$\Delta\nabla = \Delta\Delta_* \leq \Delta (1 \times \varepsilon)(1 \times \varepsilon_*)\Delta_* = 1$$ 

where the last equation follows from the equation $\Delta(1 \times \varepsilon) = 1$ and its dual $(1 \times \varepsilon_*)\Delta_* = 1$. 
=--

+-- {: .un_prop}
######Proposition 
(Dual Frobenius condition) $\nabla \Delta = (\Delta \times 1)(1 \times \nabla)$.
=-- 

+-- {: .proof} 
######Proof
The locally full subcategory whose 1-cells are _maps_ (= left adjoints) has finite products, in particular a symmetry involution $\sigma$ for which 

$$\Delta_X \sigma_{X X} = \Delta_X$$

Additionally, the right adjoint $\sigma_{X Y *}$ is the inverse $\sigma_{X Y}^{-1} = \sigma_{Y X}$. Hence the equation above is mated to $\sigma_{X X} \nabla_X = \nabla_X$, and we calculate 

$$\array{
\nabla_X \Delta_X & = & \sigma_{X X}\nabla_X \Delta_X \sigma_{X X} \\
 & = & \sigma_{X X} (1 \times \Delta)(\nabla \times 1) \sigma_{X X} \\
 & = & (\Delta_X \times 1_X) \sigma_{X \times X, X} \sigma_{X \times X, X} (1_X \times \nabla_X) \\
 & = & (\Delta_X \times 1_X) (\sigma_{X X} \times 1) (1 \times \sigma_{X X}) (1 \times \nabla_X) \\
 & = & (\Delta_X \times 1_X)(1_X \times \nabla_X)
}$$ 

which gives the dual equation. 
=--

+-- {: .un_thm}
######Theorem
In a bicategory of relations, each object is dual to itself, making the bicategory a compact closed bicategory. 
=-- 

+-- {: .proof} 
Both the unit and counit of the desired adjunction $X \dashv X$ are given by equality predicates: 

$$\eta_X = (1 \stackrel{\varepsilon_*}{\to} X \stackrel{\Delta}{\to} X \times X \qquad \theta_X = (X \times X \stackrel{\nabla}{\to} X \stackrel{\varepsilon}{\to} 1)$$

One of the triangular equations follows from the commutative diagram 

$$\array{
X & \stackrel{1 \times \varepsilon_*}{\to} & X \times X & \stackrel{1 \times \Delta}{\to} & X \times X \times X \\
 & {}_1\searrow & \downarrow \mathrlap{\nabla} & & \downarrow \mathrlap{\nabla \times 1} \\
 & & X & \overset{\Delta}{\to} & X \times X \\
 & &  & {}_{1}\searrow & \downarrow \mathrlap{\varepsilon \times 1} \\
 & & & & X
}$$

where the square expresses a Frobenius equation. The other triangular equation uses the dual Frobenius equation. 
=--

The compact closure allows us to define the opposite of a relation $R: X \to Y$ as the 1-morphism mate: 

$$R^{op} = (Y \stackrel{1_Y \times \eta_X}{\to} Y \times X \times X \stackrel{1_Y \times R \times 1_X}{\to} Y \times Y \times X \stackrel{\theta_Y \times 1_X}{\to} X)$$ 

In this way, a bicategory of relations becomes a $\dagger$-[[dagger-compact category|compact]] $Pos$-enriched category. It may be shown that if $f: X \to Y$ is a map, then $f^{op}: Y \to X$ equals the right adjoint $f_*$. Also, it may be shown that maps coincide with strict comonoid morphisms. 

+-- {: .un_prop}
######Proposition
If $f, g: X \to Y$ are maps and $f \leq g$, then $f = g$. Thus, the locally full subcategory whose morphisms are maps is locally discrete (the hom-posets are discrete). 
=-- 

+-- {: .proof} 
######Proof 
A 2-cell inequality $\alpha: f \leq g$ is mated to a inequality $g_* \leq f_*$. On the other hand, whiskering $1_Y \times \alpha \times 1_X$ with $1_Y \times \eta_X$ and $\theta_Y \times 1_X$, as in the construction of opposites above, gives $\alpha^{op}: f^{op} \leq g^{op}$. Thus we obtain $f^{op} = g^{op}$, and because the dagger operation $(-)^{op}$ is involutory, we obtain $f = g$. 
=--

## See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegories]]

* [[1-category equipped with relations]]


## References

* Carboni and Walters, "Cartesian Bicategories, I"

* [blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html) showing that any bicategory of relations is an [[allegory]]. Indeed, a bicategory of relations is equivalent to a unitary pretabular allegory.


[[!redirects bicategories of relations]]