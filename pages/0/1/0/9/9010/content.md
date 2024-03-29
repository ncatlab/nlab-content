
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Given a [[2-ring]] $R$, a _line 2-bundle_ or _2-line bundle_ is a _[[2-module bundle]]_ whose typical fiber is a [[2-line]] over $R$.

## Definition

### Recalling general 2-vector bundles

Let $R$ be a [[commutative ring]], or more generally an [[E-∞ ring]]. By the discussion at [[2-vector space]] consider the [[2-category]]

$$
  2 Vect_R \simeq Alg_R
$$ 

[[equivalence of 2-categories|equivalent]] to that whose objects are [[associative algebras]] (or generally [[A-∞ algebra|algebras]]) $A$ over $R$, (being placeholders for the 2-vector space $A Mod$ which is the category of [[modules]] over $A$) whose [[1-morphisms]] are [[bimodules]] between these algebras (inducing linear functors between the corresponding 2-vector spaces = categories of modules) and whose [[2-morphisms]] are [[homomorphisms]] between those. 

Under [[Isbell duality]] and by the discussion at _[Modules -- as generalized vector bundles](module#RelationToVectorBundlesInIntroduction)_  we may think of this 2-category as being that of (generalized) 2-vector bundles over a [[space]] called $Spec R$.

### Line 2-bundles

The [[2-category]] $2 Vect_R \simeq Alg_R$ is canonically a [[monoidal 2-category]]. An object in $2 Vect_R$ is a _[[line]]_ if it is an _invertible object_ with respect to this tensor product, hence if it is an _[[Azumaya algebra]]_. In terms of the above this means that it represents a 2-vector bundle over $Spec R$ which is a **line 2-bundle**.

The full inclusion

$$
  \mathbf{Br}(R) \hookrightarrow 2 Vect_R \simeq Alg_R
$$

of the maximal [[2-groupoid]] on the line 2-bundles over $Spec R$ is a [[braided 3-group]], the _[[Picard group|Picard 3-group]]_ of $Spec R$.  See _[Relation to Brauer group](#RelationToBrauerGroup)_ below for more.

## Properties

### Relation to Brauer group and Picard group
 {#RelationToBrauerGroup}

The [[braided 3-group]] $\mathbf{Br}(R)$ of line 2-bundles over $Spec R$ has as [[homotopy groups]]

* $\pi_0(\mathbf{Br}(R))$ the [[Brauer group]] of $R$;

* $\pi_1(\mathbf{Br}(R))$ the [[Picard group]] of $R$, hence the group of ordinary [[line bundles]] over $R$;

* $\pi_2(\mathbf{Br}(R))$ the [[group of units]] of $R$.



## Examples

### Super line 2-bundles and twisted K-theory
 {#SuperLine2BundlesAndTwistedK}

See at _[[super line 2-bundle]]_.

## Related concepts

* [[line bundle]]

* [[holomorphic line 2-bundle]], [[algebraic line 2-bundle]]

* [[line n-bundle]]

* [[line n-bundle with connection]]

[[!include moduli of higher lines -- table]]

## References

Line 2-bundles in [[supergeometry]] as a model for the [[B-field]] and [[orientifolds]] are discussed (even if not quite explicitly in the language of higher bundles) in 

* [[Daniel Freed]], _Lectures on twisted K-theory and orientifolds_ ([pdf](http://www.ma.utexas.edu/users/dafr/ESI.pdf))
 {#Freed}

based on

* [[Peter Donovan]], [[Max Karoubi]], _Graded Brauer groups and $K$-theory with local coefficients_, Publications Math&#233;matiques de l'IH&#201;S, 38 (1970), p. 5-25  ([numdam](http://www.numdam.org/item?id=PMIHES_1970__38__5_0))
 {#DonovanKaroubi}


and

* [[C. T. C. Wall]], _Graded Brauer groups_, J. Reine Angew. Math. 213 (1963/1964), 187-199. 
 {#Wall}

and developing constructions in 

* [[Jacques Distler]], [[Dan Freed]], [[Greg Moore]], _Orientifold Pr&#233;cis_ in: [[Hisham Sati]], [[Urs Schreiber]] (eds.) _[[schreiber:Mathematical Foundations of Quantum Field and Perturbative String Theory]]_ Proceedings of Symposia in Pure Mathematics, AMS (2011) ([arXiv:0906.0795](http://arxiv.org/abs/0906.0795), [slides](http://www.ma.utexas.edu/users/dafr/bilbao.pdf))
 {#Precis}

More on [[super line 2-bundles]] is secretly in 

* [[Daniel Freed]], [[Michael Hopkins]], [[Constantin Teleman]], _Loop groups and twisted K-theory I_ ([arXiv:0711.1906](http://arxiv.org/abs/0711.1906)) 
 {#FreedHopkinsTeleman}

The above higher supergeometric story is made explicit in 

* [[Domenico Fiorenza]], [[Hisham Sati]], [[Urs Schreiber]], _[[schreiber:A higher stacky perspective on Chern-Simons theory]]_
 {#FSS}

[[!redirects line 2-bundles]]
[[!redirects 2-line bundle]]
[[!redirects 2-line bundles]]

