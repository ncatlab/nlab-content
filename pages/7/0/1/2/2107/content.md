
#Contents#
* automatic table of contents goes here
{:toc}

## Motivation

Sometimes in the place where we expect [[Lie algebra]]s, some noncommutative phenomena occur and we need to drop out the requirement of antisymmetry of the brackets. 

[[Jean-Louis Loday]] introduced Leibniz algebras, because of considerations in [[algebraic K-theory]]. Roughly speaking the [[Lie algebra homology]] is related to the appearance of cyclic homology (as it is manifest in the original work of Tsygan and then of Loday-Quillen). 

* [[Jean-Louis Loday]], [[Daniel Quillen]], _Cyclic homology and the Lie algebra homology of matrices_, 	Comm. Math. Helv. __59__, n. 1, 565-591 (1984), [doi](http://dx.doi.org/10.1007/BF02566367)

Lie algebra homology involves the [[Chevalley-Eilenberg chain complex]], which in turns involves the exterior powers of the Lie algebra. Loday found that there is a noncommutative generalization where roughly speaking one has the tensor and not the exterior powers of the Lie algebra in the complex; this new complex defines the __Leibniz homology__ of Lie algebras. The Leibniz homology is related to the [[Hochschild homology]] the same way the Lie algebra homology is related to the cyclic homology. 

* C. Cuvier, _Homologie de Leibniz et homologie de Hochschild_, C.R. Acad. Sci. Paris, Ser. A-B313, 569-572 (1991)

In fact this new complex for Leibniz homology further generalizes to the case of Leibniz algebras, where it computes certain [[Tor]] groups for corepresentations of Leibniz algebras. 

## Definition

Given a [[commutative unital ring]] $k$ (usually a [[field]]), a Lebniz $k$-algebra $A$ is a particular kind of [[nonassociative algebra]] over $k$ which is somewhat more general than a [[Lie algebra]] over $k$.

A __left Leibniz $k$-algebra__ is $k$-[[module]] $L$ equipped with a bracket, which is a $k$-linear map $[,]:A\otimes A \to A$ satisfying the __left Leibniz identity__

$$ [a, [b,c]] = [[a,b],c]+[b,[a,c]] $$

In other words, the left $ad$-map, $a \mapsto (ad_l a = [a,-]:L\to L)$ is a [[derivation]] of $L$ as a nonassociative algebra. Similarly, there are right Leibniz algebras, for which the right $ad$-map $ad_r :a\mapsto [-,a]:L\to L$ is a derivation. In the presence of antisymmetry, the left Leibniz identity is equivalent to the [[Jacobi identity]], though this is not true in general; thus a Lie algebra is precisely an antisymmetric (or alternating) Leibniz algebra.

## Relation to Lie algebras in Loday-Pirashvili category

There is a remarkable observation of Loday and Pirashvili that in the [[Loday–Pirashvili tensor category]] of linear maps with (exotic) "infinitesimal tensor product", the category of internal Lie algebras has the category of, say left, Leibniz $k$-algebras as a full subcategory.  

## Terminology

Some people dislike the term (left/right) Leibniz algebra (which is allegedly due to Loday), and prefer other names, including 'Loday algebras' and many longer descriptive names.  

## Corepresentations and representations

..

[[!redirects Leibniz algebras]]
[[!redirects Loday algebra]]
[[!redirects Leibniz rule]]
[[!redirects Leibniz rules]]
[[!redirects Leibniz identity]]
[[!redirects Leibniz identities]]
