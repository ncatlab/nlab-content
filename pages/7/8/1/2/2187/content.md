+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

A **subfunctor** is a [[subobject]] in a [[functor category]].

A subfunctor of a [[functor]] $G:C\to D$ between [[categories]] $C$ and $D$ is a pair $(F,i)$ where $F:C\to D$ is a functor and $i:F\to G$ is a [[natural transformation]] such that its components $i_M:F(M)\to G(M)$ are [[monomorphism|monic]]. 

In fact one often by a subfunctor means just an [[equivalence class]] of such monic natural transformations; compare [[subobject]].

A subfunctor is also called a **sub[[presheaf]]** . A subfunctor of a [[representable functor]] $Hom(-,x)$ is precisely a [[sieve]] over the representing object $x$.

## Properties

In a [[concrete category]] with [[image]]s one can choose a representative of a subfunctor where the components of $i$ are genuine inclusions of the underlying sets; then a subfunctor is just a natural transformation whose components are inclusions.  The naturality in terms of concrete inclusions just says that for all $f:c\to d$, $F(f)=G(f)|_{F(c)}$. If the set-theoretic circumstances allow consideration of a [[functor category|category of functors]], then a subfunctor is a [[subobject]] in such a category.

A *subfunctor $(F,i)$ of the identity* $id_C:C\to C$ in a category with images is an often used case: it amounts to a natural assignment $c\mapsto F(c)\stackrel{i}\hookrightarrow c$ of a subobject to each object $c$ in $C$. For concrete categories with images then $F(f)=f|_{F(c)}$.

[[!redirects subfunctors]]

[[!redirects subpresheaf]]
[[!redirects subpresheaves]]