<div class="rightHandSide toc">
[[!include higher category theory - contents]]

***

[[!include higher algebra - contents]]

</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The notion of _$(\infty,1)$-operad_ is to that of [[(∞,1)-category]] as [[operad]] is to [[category]].

So, roughly, an $(\infty,1)$-operad is an algebraic structure that has for each given type of input and one type of output an [[∞-groupoid]] of operations that take these inputs to that output.

## Definitions

Two models for $(\infty,1)$-operads exist to date, one by Cisinski-[[Ieke Moerdijk|Moerdijk]], the other by [[Jacob Lurie|Lurie]].

### In terms of dendroidal sets

Here [[simplicial set]]s are generalized to [[dendroidal set]]s. The theory of $(\infty,1)$-operads is then formulated in terms of dendroidal sets in close analogy to how the theory of [[(∞,1)-category|(∞,1)-categories]] is formulated in terms of [[simplicial set]]s.

There is a [[model  structure on dendroidal sets]] whose fibrant objest are the **quasi-operad**s in direct analogy to the notion of [[quasi-category]]. 

Here are two blog entries on talks on this stuff:

* [Dendroidal Sets and Infinity-Operads](http://golem.ph.utexas.edu/category/2009/02/dendroidal_sets.html)

* [Moerdijk on Infinity Operads](http://golem.ph.utexas.edu/category/2009/02/moerdijk_on_infinityoperads.html)

### In terms of $(\infty,1)$-categories of operators

Every [[operad]] $A$ encodes and is encoded by its [[category of operators]] $C_A$. In the approach to $(\infty,1)$-operators described below, the notion of category of operators is generalized to an [[(∞,1)-category]] of operators.

In this approach an $(\infty,1)$-operad $C^\otimes$ is regarded as an [[(∞,1)-category]] $C$ -- the unary part of the $(\infty,1)$-operad to be described-- with extra structure that determines [[(∞,1)-functor]]s $C^{\times n} \to C$.

This and the conditions on these are encoded in requiring that $C^\otimes$ is an $(\infty,1)$-functor $C^\otimes \to \Gamma$ over [[Segal's category]] $\Gamma$ of pointed finite sets, satisfying some conditions.

In particular, any [[symmetric monoidal (∞,1)-category]] yields an example of an $(\infty,1)$-operad in this sense.  In fact, symmetric monoidal $(\infty,1)$-categories can be *defined* as $(\infty,1)$-operads such that the functor $C^\otimes \to \Gamma$ is a [[coCartesian fibration]].  (For the moment, see [[monoidal (infinity,1)-category]] for more comments and references on higher operads in this context.)

This is the approach described in (the new version of !)

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))

### Model for $(\infty,1)$-categories of operators {#ModelForinfOpera}

There is a [[model category]] that [[presentable (infinity,1)-category|presents]] the [[(∞,1)-category]] $(\infty,1)Cat_{Oper}$ of $(\infty,1)$-categories of operations.

+-- {: .un_prop}
###### Proposition

There exists a 

* [[proper model category|left proper]]

* [[combinatorial model category|combinatorial]]

[[model category]] $\mathcal{P} Op_{(\infty,1)}$

* whose underlying [[category]] has

  * [[object]]s are [[marked simplicial set]] $S$ equipped with a morphism $S \to N(FinSet_*)$ such that marked edges map to inert morphisms in $FinSet_*$ (those for which the preimage of te marked point contains just the marked point)

  * [[morphism]]s are morphisms of [[marked simplicial set]]s $S \to T$ such that the triangle

    $$
      \array{
        S &&\to&& T
        \\
        & \searrow && \swarrow
        \\
        && N(FinSet_*)
      }
    $$
    
    commutes;

* which is canonically an [[SSet]]-[[enriched category]];  

* and whose [[model category|model structure]] is given by

  * cofibrations are those morphisms whose underlying morphisms of [[simplicial set]]s ate cofibrations, hence [[monomorphism]]s
  
  * weak equivalences are those morphisms $S \to T$ such that for all $A \to N(FinSet_*)$ that are $(\infty,1)$-categories of operations by the above definition, the morphism of [[SSet]]-[[hom object]]s

    $$
      \mathcal{P}Op_\infty(T,A) \to 
      \mathcal{P}Op_\infty(S,A)
    $$

    is a homotopy equivalence of simplicial sets.

  * an object is fibrant if and only if it is an $(\infty,1)$-category of operations, by the above definition.

=--

+-- {: .proof}
###### Proof

This is prop 1.8 4 in

* [[Jacob Lurie]], _Commutative algebra_ ([pdf](http://www.math.harvard.edu/~lurie/papers/DAG-III.pdf))


=--



[[!redirects (∞,1)-operad]]
[[!redirects (∞,1)-operads]]
[[!redirects (infinity,1)-operads]]