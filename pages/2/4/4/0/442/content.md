In his 1963 doctoral dissertation, Bill Lawvere introduced a new categorical method for doing [[universal algebra]], alternative to the usual way of presenting an algebraic concept by means of its logical signature (with generating operations satisfying equational axioms). The rough idea is to define an algebraic theory as a [[category]] with finite products and possessing a "generic algebra" (e.g., a generic group), and then define a model of that theory (e.g., a group) as a product-preserving [[functor]] coming out of that [[category]]. This type of category is what is nowadays called a _Lawvere algebraic theory_, or just Lawvere theory. 

A **Lawvere theory** or **finite-product theory** is a [[category]] $T$ with finite cartesian [[product|products]] in which every [[object]] is [[isomorphism|isomorphic]] to a finite cartesian power $x^n$ of a distinguished object $x$ (called the _generic object_ for the theory $T$). It is common to adopt the (slightly [[evil]]) convention that every object of $T$ is _equal_ to a chosen power of $x$. Thus, if $Fin$ is the category of finite cardinals and functions between them, then the unique (up to isomorphism) product-preserving functor 
$$Fin^{op} \to T$$ 
that takes the 1-element cardinal to $x$ is commonly supposed to be surjective on objects (rather than, less evilly, [[essentially surjective functor|essentially surjective]]). 

A _model_ of $T$ is a product-preserving functor $T \to Set$, and _homomorphism of models_ is a natural transformation between such functors. A _morphism_ of theories $T \to T'$ is again a product-preserving functor. Thus, $Fin^{op}$ (the "theory of [[equality]]") is initial in the category of Lawvere theories. 

## Discussion

As a running example, let us consider the theory of [[group]]s (defined however you like). To get the corresponding Lawvere theory $T$, let $F(n)$ (for any natural number $n \geq 0$) be a free group on $n$ generators, and define the Lawvere theory $T_{Grp}$ to be the category [[opposite category|opposite]] to the category of free groups $F(n)$ and group homomorphisms. The generic object $x$ of $T_{Grp}$ is taken to be $F(1)$. 

The category of free groups has finite coproducts since $F(m) + F(n) \cong F(m+n)$ (in other words, the inclusion 

$$FreeGroup \hookrightarrow Group$$ 

creates coproducts in $FreeGroup$), so $T_{Grp}$ has finite products, and we have $F(n) = x^n$ in $T_{Grp}$. Any group $G$ defines a product-preserving functor 

$$T_{Grp} = FreeGroup^{op} \hookrightarrow Group^{op} \stackrel{\hom(-, G)}{\to} Set$$ 

since contravariant hom-functors take coproducts to products. Thus any group gives a model of $T_{Grp}$. 

The other direction is more interesting. Let 

$$M: T_{Grp} \to Set$$ 

be a model of $T_{Grp}$, i.e., a product-preserving functor. We will define a group structure on $G = M(x)$, the underlying set of the group. 

To understand this, let's consider how group multiplication would be defined. The idea is that $x$ in $T_{Grp}$ is a "generic group", so we first need to understand how multiplication works there. The idea is that the product 
in the generic group 
$$m: x^2 \to x^1$$ 
corresponds to a homomorphism 
$$F(1) \to F(2)$$
which by freeness corresponds to an element $1 \to F(2)$, and the element we are after should the product $a b$ of the generators $a, b$ of the free group $F(2) = F(a, b)$. The generators $a, b$ themselves correspond to the two coproduct inclusions 
$$i_1: F(1) \to F(1) + F(1) = F(2) \qquad i_2: F(1) \to F(1) + F(1) = F(2)$$ 

Then, since $M$ is assumed to [[exact functor|preserve products]], we obtain a map 
$$G \times G = M(x) \times M(x) \cong M(x^2) \stackrel{M(m)}{\to} M(x) = G$$ 
and this defines the group multiplication on $G$. The group identity and group inversion on $G$ are defined by following similar recipes. 

It may be checked that the notion of homomorphism of $T_{Grp}$-models (as defined above) coincides with the usual notion of group homomorphism. In summary, the category of groups is equivalent to the category of models of $T_{Grp}$. 

In particular, any hom-functor 

$$\hom_{T_{Grp}}(x^n, -): T_{Grp} \to Set$$ 

preserves products, and so defines a group. This group is precisely the free group on $n$ generators, and a little thought shows that the $n$ generators correspond to the natural transformations 
$$\hom_{T_{Grp}}(x, -) \to \hom_{T_{Grp}}(x^n, -)$$
induced by the $n$ projection maps $x^n \to x$. 

All of the discussion above for the case of groups generalizes to any finitary [[algebraic theory]] (i.e., any single-sorted theory whose signature consists of function symbols of finite arity, subject to universally quantified equational axioms). In summary: 

* The Lawvere theory $T$ is the category opposite to the category of free algebras on finitely many generators, 

* The category of algebras is in turn equivalent to the category of product-preserving functors $T \to Set$, and 

* The free algebras are retrieved as the representable functors $T \to Set$. 

As discussed in the article on [[operad|operads]], the notion of Lawvere theory may also be formulated in terms of operads relative to the theory of [[cartesian monoidal category|cartesian monoidal categories]]. 

## Remarks

1. If $C$ is a category with finite products, then a group (object) in $C$ may be defined as a product-preserving functor $T_{Grp} \to C$. For example, a topological group may be identified with a functor $T_{Grp} \to Top$, and a Lie group with a product-preserving functor $T_{Grp} \to Man$ into the category of smooth [[manifold]]s. An analogous statement holds for any finitary algebraic theory, when formulated in terms of its Lawvere theory $T$. 

1. As _finite-product theories_, Lawvere theories are at one end of a spectrum of [[theory|theories]] of differing logical strengths. For example, there are left exact theories, regular theories, geometric theories, and so on, which require for their interpretation categories of differing degrees of strength in their [[internal logic]]. See also [[classifying topos]].

1. Some people use 'finite-product theory' to mean a category with finite products, not necessarily with the property that every object is isomorphic to a product of copies of a given object $x$, reserving 'Lawvere theory' to refer to finite product theories with this special property.  Some, but not all, the above discussion generalizes to this case.  There is, for example, a finite products theory for ring-module pairs.


[[!redirects finite-product theory]]
[[!redirects finite product theory]]
[[!redirects finite-products theory]]
[[!redirects finite products theory]]
[[!redirects Lawvere theories]]