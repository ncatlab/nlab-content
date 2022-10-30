
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--


# Bicategories of relations
* table of contents
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

## Properties

We record a few consequences of this notion. 

+-- {: .num_prop} 
######Proposition 
(Separability condition) $\Delta\nabla = 1$.
=-- 

+-- {: .proof} 
######Proof
In one direction, we have the 2-cell $1 \leq \Delta\nabla$ which is the unit of the adjunction $\Delta \dashv \Delta_* = \nabla$. In the other direction, there is an adjunction $\varepsilon \dashv \varepsilon_*$ between the counit and its dual, and the unit of this adjunction is a 2-cell $1 \leq \varepsilon\varepsilon_*$, from which we derive 

$$\Delta\nabla = \Delta\Delta_* \leq \Delta (1 \times \varepsilon)(1 \times \varepsilon_*)\Delta_* = 1$$ 

where the last equation follows from the equation $\Delta(1 \times \varepsilon) = 1$ and its dual $(1 \times \varepsilon_*)\Delta_* = 1$. 
=--

+-- {: .num_prop}
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
 & = & \sigma_{X X} (1 \times \Delta_X)(\nabla_X \times 1) \sigma_{X X} \\
 & = & (\Delta_X \times 1_X) \sigma_{X \times X, X} \sigma_{X \times X, X} (1_X \times \nabla_X) \\
 & = & (\Delta_X \times 1_X) (\sigma_{X X} \times 1) (1 \times \sigma_{X X}) (1 \times \nabla_X) \\
 & = & (\Delta_X \times 1_X)(1_X \times \nabla_X)
}$$ 

which gives the dual equation. 
=--

+-- {: .num_theorem}
######Theorem
In a bicategory of relations, each object is dual to itself, making the bicategory a compact closed bicategory. 
=-- 

+-- {: .proof} 
######Proof
Both the unit and counit of the desired adjunction $X \dashv X$ are given by equality predicates: 

$$\eta_X = (1 \stackrel{\varepsilon_*}{\to} X \stackrel{\Delta}{\to} X \times X) \qquad \theta_X = (X \times X \stackrel{\nabla}{\to} X \stackrel{\varepsilon}{\to} 1)$$

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

In this way, a bicategory of relations becomes a [[dagger-compact category|†-compact]] $Pos$-enriched category. 

Recall (again) that a **map** in the bicategory of relations is the same as a 1-cell that has a right adjoint. 

+-- {: .num_prop #strict} 
###### Proposition 
If $f \colon X \to Y$ is a map, then $f$ is a strict morphism of comonoids. 
=-- 

+-- {: .proof} 
###### Proof 
If $g$ is the right adjoint of $f$, we have $\Delta_X g \leq (g \times g)\Delta_Y$ since $g$, like any morphism, is a lax comonoid morphism. But this 2-cell is mated to a 2-cell $(f \times f)\Delta_X \to \Delta_Y f$, inverse to the 2-cell $\Delta_Y f \to (f \times f)\Delta_X$ that comes for free. So $f$ preserves comultiplication strictly. A similar argument shows $f$ preserves the counit strictly. 
=-- 

+-- {: .num_prop}
###### Proposition 
If $f \colon X \to Y$ is a map, then $f^{op}: Y \to X$ equals the right adjoint $f_\ast$. 
=-- 

+-- {: .proof} 
###### Proof 
The proof is much more perspicuous if we use [[string diagram|string diagrams]]. But the key steps are given in two strings of equalities and inequalities. The first gives a counit for $f \dashv f^{op}$, and the second gives a unit. We have 

$$\array{
f f^{op} & \stackrel{0}{=} & f \circ (\varepsilon_Y \times 1)(\nabla_Y\times 1)(1 \times f \times 1)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \\
& \stackrel{1}{=} & (\varepsilon_Y \times 1)(\nabla_Y \times 1)(1 \times f \times f)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \\ 
 & \stackrel{2}{=} & (\varepsilon_Y \times 1)(\nabla_Y \times 1)(1 \times \Delta_Y)(1 \times f)(1 \times \varepsilon_X_\ast)\\ 
 & \stackrel{3}{\leq} & (\varepsilon_Y \times 1)(\nabla_Y \times 1)(1 \times \Delta_Y)(1 \times \varepsilon_Y_\ast) \\
 & \stackrel{4}{=} & (\varepsilon_Y \times 1)\Delta_Y \nabla_Y(1 \times \varepsilon_Y_\ast) \\
 & \stackrel{5}{=} & 1_Y
}$$ 

where (0) uses the definition of $f^{op}$, (1) uses properties of monoidal categories, (2) uses the fact that $f$ strictly preserves comultiplication, (3) is mated to the fact that $f$ laxly preserves the counit, (4) is a Frobenius condition, and (5) uses comonoid and dual monoid laws. We can also "almost" run the same calculation backwards to get the unit: 

$$\array{
1_X & \stackrel{0}{=} & (\varepsilon_X \times 1)\Delta_X \nabla_X(1 \times \varepsilon_X_\ast) \\ 
 & \stackrel{1}{=} & (\varepsilon_X \times 1)(\nabla_X \times 1)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \\
 & \stackrel{2}{=} & (\varepsilon_Y \times 1)(f \times 1)(\nabla_X\times 1)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \\ 
 & \stackrel{3}{\leq} & (\varepsilon_Y \times 1)(\nabla_Y \times 1)(f \times f \times 1)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \\ 
 & \stackrel{4}{=} & (\varepsilon_Y \times 1)(\nabla_Y \times 1)(1 \times f \times 1)(1 \times \Delta_X)(1 \times \varepsilon_X_\ast) \circ f \\
 & \stackrel{5}{=} & f^{op} f
}$$ 

where (0) uses comonoid and dual monoid laws, (1) uses a Frobenius condition, (2) uses the fact that $f$ preserves the counit, (3) is mated to the fact that $f$ laxly preserves comultiplication, (4) uses properties of monoidal categories, and (5) uses the definition of $f^{op}$. 
=-- 

In fact, what this proof really proves is a converse of the earlier [proposition](#strict): 

+-- {: .num_prop}
###### Proposition 
If $f$ is a strict comonoid morphism, then $f$ has a right adjoint: $f \dashv f^{op}$. 
=-- 

+-- {: .num_prop}
######Proposition
If $f, g: X \to Y$ are maps and $f \leq g$, then $f = g$. Thus, the locally full subcategory whose morphisms are maps is locally discrete (the hom-posets are discrete). 
=-- 

+-- {: .proof} 
######Proof 
A 2-cell inequality $\alpha: f \leq g$ is mated to a inequality $\alpha_*: g_* \leq f_*$. On the other hand, whiskering $1_Y \times \alpha \times 1_X$ with $1_Y \times \eta_X$ and $\theta_Y \times 1_X$, as in the construction of opposites above, gives $\alpha^{op}: f^{op} \leq g^{op}$. Since $f^{op} = f_*$ and $g^{op} = g_*$, we obtain $f^{op} = g^{op}$, and because $f^{op op} = f$, we obtain $f = g$. 
=--

## The Beck-Chevalley condition 

Bicategories of relations $\mathbf{B}$ satisfy a Beck-Chevalley condition, as follows. Let $Prod(B_0)$ denote the free category with finite products generated by the set of objects of $\mathbf{B}$. According to the results at [[free cartesian category]], $Prod(B_0)$ is finitely complete. 

Since $Map(\mathbf{B})$ has finite products, there is a product-preserving functor $\pi: Prod(B_0) \to \Map(\mathbf{B})$ which is the identity on objects. Again, according to the results of [[free cartesian category]], we have the following result. 

+-- {: .num_lemma}
###### Lemma 
If a diagram in $Prod(B_0)$ is a pullback square, then application of $\pi$ to that diagram is a pullback square in $Map(\mathbf{B})$. 
=--

Let us call pullback squares of this form in $Map(\mathbf{B})$ _product-based_ pullback squares. 

+-- {: .num_prop}
######Proposition 
Given a product-based pullback square 
$$\array{
W & \stackrel{h}{\to} & X \\
k \downarrow & & \downarrow f \\
Y & \underset{g}{\to} & Z
}$$
in $Map(\mathbf{B})$, the Beck-Chevalley condition holds: $h_* k = f g_*$. 
=-- 

See Brady-Trimble for further details. The critical case to consider is the pullback square 

$$\array{
X & \overset{\Delta}{\to} & X \times X \\
\mathllap{\Delta} \downarrow & & \downarrow \mathrlap{\Delta \times 1} \\
X \times X & \underset{1 \times \Delta}{\to} & X \times X \times X
}$$

where the Beck-Chevalley condition is exactly the Frobenius condition. 

One way of interpreting this result is by viewing $\mathbf{B}$ as a hyperdoctrine or monoidal fibration over $Prod(B_0)$, where the fiber over an object $B$ is the local hom-poset $\hom(B, 1)$. Each $f: A \to B$ in the base induces a pullback functor, by precomposing $R: B \to 1$ with $\pi(f): A \to B$ in $Map(\mathbf{B})$. Existential quantification is interpreted by precomposing with right adjoints $\pi(f)_*$. The Beck-Chevalley condition exerts compatibility between quantification and pullback/substitution functors. 

## Relation to allegories 

Any bicategory of relations is an [[allegory]]. Recall that an allegory is a $Pos$-enriched $\dagger$-category whose local homs are meet-semilattices, satisfying Freyd's modular law: 

$$R S \cap T \leq (R \cap T S^{op})S$$ 

A proof of the modular law is given in the blog post by R.F.C. ("Bob") Walters referenced below. 

In fact, we may prove a little more: 

+-- {: .num_theorem} 
######Theorem 
The notion of bicategory of relations is equivalent to the notion of unitary pretabular allegory. 
=-- 

+-- {: .proof} 
######Proof 
A bicategory of relations has a unit $1$ in the sense of allegories: 

* $1$ is a partial unit: we have $\varepsilon_1 = id_1: 1 \to 1$, and for any $R: 1 \to 1$ we have $R = R\varepsilon_1 \leq \varepsilon_1 = id_1$. 

* Any object $X$ is the source of a map $\varepsilon_X: X \to 1$, which being a map is entire. Thus $1$ is a unit. 

A bicategory of relations is also pretabular, for the maximal element in $\hom(X, Y)$ is tabulated as $(\pi_X)_* \pi_Y$, where $\pi_X$, $\pi_Y$ are the product projections for $X \times Y$. 

In the other direction, suppose $\mathbf{A}$ is a unitary pretabular allegory.  There is a faithful embedding, which preserves the unit, of $\mathbf{A}$ into its coreflexive splitting, which is unitary and tabular, and hence equivalent to $Rel$ of the regular category $Map(\mathbf{A})$.  By the proposition below, then, $\mathbf{A}$ is a full sub-2-category of a bicategory of relations.  Because the product of two Frobenius objects is again Frobenius, it suffices to show that $\mathbf{A}$ is closed under products in its coreflexive splitting.  The inclusion of $\mathbf{A}$ into the latter preserves the unit and the property of being a map, and hence preserves top elements of hom sets, while any allegory functor must preserve tabulations.  So the tabulation $(\pi^{X Y}_X, \pi^{X Y}_Y)$ of $\top_{X Y}$ in $\mathbf{A}$ is a tabulation of $\top_{1_X 1_Y}$ in the coreflexive splitting, and hence $1_{X \times Y} \cong 1_X \times 1_Y$.
=--


+-- {: .num_prop}
###### Proposition
If $C$ is a [[regular category]], then the bicategory $Rel C$ of [[Rel|relations]] in $C$ is a bicategory of relations.
=--
+-- {: .proof}
###### Proof
By theorem 1.6 of Carboni--Walters, $\mathbf{A}$ is a [[Cartesian bicategory]] if:

* $Map(\mathbf{A})$ has finite products.

* $\mathbf{A}$ has local finite products, and $id_1$ is the top element of $\mathbf{A}(1,1)$.

* The tensor product defined as
$$ R \otimes S =  (p R p_*) \cap (p' S p'_*) $$
is functorial, where $p$ and $p'$ are the appropriate product projections.

The first two are obvious, and for the third we may reason in the [[internal language]] of $C$.  Clearly
$$ 1 \otimes 1 = [x = x \wedge x' = x'] = 1  $$
The formula whose meaning is by $R S \otimes R' S'$ is
$$ (\exists y. R x y \wedge S y z) \wedge (\exists y'. R' x' y' \wedge S' y' z') $$
and we may use [[Frobenius reciprocity]] to get
$$
\begin{aligned}
  & \exists y. (R x y \wedge S y z \wedge y^* \exists y'. R' x' y' \wedge S' y' z') \\
  & \equiv \exists y. (R x y \wedge S y z \wedge  \exists y'. y^* (R' x' y'   \wedge S' y' z')) \\
  & \equiv \exists y, y'. R x y \wedge S y z \wedge R' x' y' \wedge S' y' z' \\
\end{aligned}
$$
which is the meaning of $(R \otimes R')(S \otimes S')$.  Finally, the Frobenius law is
$$ [\exists x'. (x_1, x_2) = (x', x') = (x_3, x_4)]
= [\exists x'. (x_1, x') = (x_3, x_3) \wedge (x_2, x_2) = (x_4, x')]  $$
which follows from transitivity and symmetry of equality.
=--


## See also

Other attempted axiomatizations of the same idea "something that acts like the category of relations in a regular category" include:

* [[allegories]]

* [[1-category equipped with relations]]

## Related concepts

* [[category of correspondences]]

* [[(infinity,n)-category of correspondences]]

## References

* [[Aurelio Carboni]], [[Bob Walters]], _Cartesian Bicategories, I_, [article](https://doi.org/10.1016/0022-4049%2887%2990121-6)

* [[Aurelio Carboni]], [[Max Kelly]], [[Bob Walters]], [[Richard Wood]], _Cartesian Bicategories II_, ([arXiv:0708.1921](https://arxiv.org/abs/0708.1921))

* [[Bob Walters]], [blog post](http://rfcwalters.blogspot.com/2009/10/categorical-algebras-of-relations.html), showing that any bicategory of relations is an [[allegory]]. Indeed, a bicategory of relations is equivalent to a unitary pretabular allegory.

* [[Evan Patterson]], _Knowledge Representation in Bicategories of Relations_, ([arXiv:1706.00526](https://arxiv.org/abs/1706.00526)

This article shows how one can model RDF (Resource Description Framework) and parts of OWL (Ontology Web Language) in bicategories of relations, whose internal logic is [[regular logic]]. He ends by showing how one can extend these to [[distributive bicategories of relations]] whose internal logic is [[coherent logic]], which is equivalent in expressivity to first order logic.


[[!redirects bicategories of relations]]