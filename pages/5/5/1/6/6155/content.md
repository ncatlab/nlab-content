[[!redirects Reconstruction of groups]] 

This entry is to try understanding the article 

* [[A. L. Rosenberg]], _Reconstruction of groups_, Selecta Math. N.S. 9:1 (2003) [doi](http://dx.doi.org/10.1007/s00029-003-0322-x)

aimed at a reasonably general reconstruction theorem for [[locally compact topological groups]] from a suitable category of continuous infinite-dimensional representations, generalizing the [[Pontrjagin duality]] theorem for locally compact abelian groups and the [[Tannaka-Krein theorem]] for compact groups. More precisely,  it asks 

> what are conditions on a monoidal subcategory of the category of continuous representations of a locally compact group sufficient to reconstruct the group?

The first generalization of that type is the Tatsuuma reconstruction theorem

* N. Tatsuuma, _A duality theorem for locally compact groups_, J. Math., Kyoto Univ. 6 (1967), 187&#8211;293.

which asserts that for a monoidal subcategory $C$ of the category of [[unitary representation]]s of a locally compact group $G$ to be sufficient for the reconstruction from the [[fiber functor]] $C\to Hilb$, it suffices that $C$ contains  the regular representation of $G$ on $L^2(G,\mu)$ where $\mu$ is the left Haar measure on $G$. 

Table of contents

$1.$ $\ast$-categories, $\ast$-functors

Here monoidal categories, monoidal functors and their morphisms are reviewed and (antilinear) $\ast$-involutions on $\mathbb{C}$-linear monoidal categories. (Small)  monoidal $\ast$-categories form a category $Cat^\ast$. For any (monoidal) $\ast$-category, and any group $G$, the category $Rep^G(C)$ of representation of $G$ in objects in $C$ has a structure of a (monoidal) $\ast$-category $Rep^G(C)^{\tilde\ast}$ and the forgetful functor $Rep^G(C)\to C$ is a strict monoidal functor of $\ast$-categories. 

$2.$ Duality construction

$2.1$ The case of abstract groups

Here a basic pair of adjoint functors is defined $\mathcal{R}_{C\tilde{}^\ast}\dashv Aut(C\tilde{}^\ast)$ where $Aut(C\tilde{}^\ast): Cat^\ast/C\tilde{}^\ast\to Group$ gives the group of automorphisms of a monoidal $\ast$-functor with codomain $C\tilde^\ast$ and its left adjoint is $\mathcal{R}_{C\tilde{}^\ast} : G\mapsto Rep^G(C)\tilde{}^\ast$.

$2.2$ The case of topological groups

Here one supposes that $C$ is enriched over the category of topological (complex) vector spaces, so that $Aut(V)$ is a topological group for all $V\in Ob C$. The construction of an adjoint pair of functors above works with the category $Group$ replaced by $TopGroup$. However, in the representation theory one assumes only that the representations are continuous in the [[weak operator topology]]; and the group of invertibles in $End V$ in the enriched sense is not always a topological group in that topology. Instead one works with the category of groups with a topology in which only left and right translations are required to be continuous. 

$2.3$ Reflexivity

Reflexive monoidal categories are defined: they have an involution $\sigma$ and functorial isomorphisms $\sigma(X)\otimes X\to Id$ for all objects $X$. For example, rigid symmetric monodial categories and rigid braided monoidal categories are in that class; the category of Hilbert spaces and if a category is reflexive than the category of representations of a group is reflexive. 

$2.4$ The reconstruction problem

From now on a full subcategory $C\tilde{}$ of the category of reflexive locally convex topological complex vector spaces is fixed with a real structure; it is equipped with a monoidal product such that the forgetful functor to vector spaces is monoidal with help of maps $F(V)\otimes_{\mathbb{C}} F(W)\to F(V\otimes W)$ which are injective and with dense image in weak topology on the tensor product. Given a topological group $G$, one chooses a full (monodial) $\ast$-subcategory $\mathfrak{C}\tilde{}$ of the $\ast$-category of continuous uniformly bounded representations of $G$ in $C\tilde{}$. The group of automorphisms of the forgetful functor $F_{\mathfrak{C}} : \mathfrak{C}{\tilde{}}\to Vec$ is equipped with weak operator topology and the canonical morphism $G\to Aut^\ast(F_{\mathfrak{C}})$ is continuous; however $Aut^\ast(F_{\mathfrak{C}})$
is not a topological group in general. The reconstruction problem is, under which conditions on $\mathfrak{C}{\tilde{}}$, the canonical isomorphism is an isomorphism of topological groups.  

$3.$ The algebra of matrix elements  

One considers the set $A(\mathfrak{C}\tilde{})$
of matrix elements of representations belonging to the subcategory $A(\mathfrak{C}\tilde{})$. It appears to be a subalgebra of the Banach $\ast$-algebra of complex valued continuous functions on $G$, and is closed with respect to involution $\sigma: f\to f\circ (-)^{-1}$, $f^\sigma(x) = f(x^{-1})$, closed under complex conjugation (which is an anti-involution) and an $M(G)$-submodule. It is proved that each elements of $Aut^\ast(F_{\mathfrak{C}\tilde{}})$ determine an automorphism of the algebra with involution $A(\mathfrak{C})$. 

subset  of the algebra of bounded 

$4.$ Conditions of continuity

Here certain lemmas on certain category $B\mathfrak{A}$ of algebras with involutions and anti-involutions is proved. 

$5.$ Reconstruction theorems 

Among several theorems, the theorem 5.3 states that if $G$ is locally compact then a subcategory $\mathfrak{C}\tilde{}$ then for a $\ast$-category of uniformly bounded continuous representations the canonical map $G\to Aut^\ast(F_{\mathfrak{C}\tilde{}})$
to be an isomorphism of topological groups it is sufficient that the following simultaneously hold:

* it separates the elements of $G$

* the algebra $A(\mathfrak{C})$ of matrix elements has nonzero intersection with $L^p(G,\mu)$ for some $p\gt 0$, where $\mu$ is a left-invariant measure on $G$

Classical corollaries are also shown. For example, for Tannaka-Krein one notes that all matrix elements of a compact group are in $L^1(G,\mu)$, hence only the separation property is needed. For Tatsuuma duality one notes that the matrix elements of the regular representation are convolutions of functions from $L^2(G,\mu)$ and uses stronger theorem 5.1 from the paper. Pontrjagin duality is a known corollary of Tatsuuma's duality theorem. 
