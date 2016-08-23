
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Additive and abelian categories
+--{: .hide}
[[!include additive and abelian categories - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _semisimple category_ is a category in which each object is a [[direct sum]] of finitely many [[simple objects]], and all such direct sums exist.

## Definition

An [[abelian category]] is called **semisimple** if every [[object]] is a [[semisimple object]], hence a [[direct sum]] of finitely many [[simple objects]].  See [[semisimple abelian category]].

Alternatively, a [[monoidal category|monoidal]] [[linear category]] (that is, a [[monoidal category]] [[enriched category|enriched over]] [[Vect]]) is called **semisimple** if:

*  it has finite [[biproducts]] (usually called '[[direct sums]]'),
*  [[split idempotent|idempotents split]] (so we say that it 'has [[subobjects]]' or, perhaps better, 'has [[retract]]s'), and
*  there exist [[object]]s $X_i$ labeled by an index set $I$ such that $Hom(X_i, X_j) \cong \delta_{ij} k$ where $k$ is the [[ground field]] (such objects are called _[[simple object|simple]]_) and such that for any two objects $V$ and $W$ in the category, the natural composition map
   \[
     \bigoplus_{i \in I} Hom(V, X_i) \otimes Hom(X_i, W) \rightarrow Hom(V, W)
   \]
   is an isomorphism.

## Direct sums of simple objects 

Note that this definition implies that every object $V$ is a direct sum of simple objects $X_i$. To see this, note that the third item of the definition is equivalent to stipulating that the vector space $Hom(X_i, V)$ is in canonical duality with the vector space $Hom(V, X_i)$. Indeed, we have a canonical pairing
 \[
 Hom(V, X_i) \otimes Hom(X_i, V) \rightarrow k
\]
given by sending $f \otimes g \mapsto \langle f \circ g \rangle$ where the "$\langle \cdot \rangle$" notation refers to extracting [[scalars]] from endomorphisms of simple objects (each such endomorphism is a scalar multiple of the identity). We also have a canonical copairing
 \[
 k \rightarrow Hom(X_i, V) \otimes Hom(V, X_i)
\]
given by sending $\id_{X_i}$ to the "$i$th block" of the image of the identity $\id_V$ arrow under the isomorphism given in the definition. One can check that this pairing and copairing satisfy the snake equations. Hence if we choose a basis 
 \[
 \{ a_{i,p} : X_i \rightarrow V \}
\]
for each vector space $Hom(X_i, V)$, we get a corresponding dual basis
 \[
 \{ a_i^p : V \rightarrow X_i \}
\]
satisfying
 \[
 a_i^p a_{j,q} = \delta_{ij} \delta_p^q \quad and \quad \sum_{i,p} a_{i,p} a_i^p = \id_V.
\]
This says precisely that $V$ has been expressed as a direct sum of the $X_i$.


## Remarks

* The above definition definition of semisimple monoidal linear category (taken from the reference of M&#252;ger below) does not use the concept of [[abelian category]]. This is because the concepts that one thinks about with abelian categories such as [[kernel]]s and [[cokernel]]s do not play an important conceptual role in semisimple categories, being replaced by the more important concepts of [[biproduct]] and [[retract]]. Hence it is best to give a streamlined definition from first principles without going through the language of abelian categories which would have muddied the waters.

* For a category to be semisimple, it needs to have a certain directional symmetry in its hom-sets, namely that $Hom(V, W)$ must at least have the same dimension as$Hom(W,V)$. This is the easiest way to check if a category will _fail_ to be semisimple. For instance, the category $Rep(A)$ of [[representations]] of an algebra $A$ will rarely be semisimple, precisely because there is no relation between $Hom(V, W)$ and $Hom(W,V)$ in general. Again, this can be traced back to the original algebra $A$ not having any 'symmetry' like the inverse operation in a group. 

* As far as 'duality' on the hom-sets is concerned, one might have a $S: C \rightarrow C$ from the category to itself with the property that there are canonical isomorphisms
 \[
 Hom(V, W) \cong Hom(W, SV)^\vee
\]
where "$\vee$" denotes the ordinary linear dual of a vector space. Such a functor is called a _Serre functor_ in algebraic geometry, and indeed there is precisely such a functor on the derived category of coherent sheaves on a complex manifold --- it is given by tensoring with the canonical line bundle. 

* For [[2-Hilbert space|2-Hilbert spaces]], there is an antilinear $*$-operation on the hom-sets $* : Hom(V, W) \rightarrow Hom(W,V)$. The presence of this duality in fact forces the category to be semisimple (this comes down to the fact that a finite-dimensional $*$-algebra, such as the hom's between a bunch of objects in the category, must be a full matrix algebra)

## Examples

* The archetypical simple example is [[Vect]] itself, the category of (finite dimensional!) [[vector space]]s over some [[ground field]] $k$. This has a single [[isomorphism]] class of simple objects: given by $k$ itself.

* The category of finite-dimensional [[representations]] of a compact [[Lie group]] $G$ is semisimple, with the simple objects being precisely the [[irreducible representation]]s (this is the content of [[Schur's lemma]]). If $G$ is noncompact, one needs to pass from the concept of 'direct sum' to '[[direct integral]]'.

* Every [[fusion category]] is a semisimple category.

## References

* M. M&#252;ger, [From Subfactors to Categories and Topology I. Frobenius algebras in and Morita equivalence classes of tensor categories](http://arxiv.org/math.CT/9812040). 

There is related discussion on the $n$Forum [here](http://nforum.mathforge.org/discussion/1120/semisimple-category/?Focus=42783#Comment_42783).
