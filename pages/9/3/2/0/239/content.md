
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
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

The term **tensor product** has many different but closely related meanings.

* In its original sense a _tensor product_  is a representing object for a suitable sort of _[[bilinear map]]_ and _[[multilinear map]]_.  The most classical versions are for [[vector spaces]] ([[modules]] over a [[field]]), more generally [[modules]] over a [[ring]], and even more generally [[algebra over a monad|algebras]] over a [[commutative monad]].  In modern language this takes place in a [[multicategory]].

* Consequently, the [[functor]] $\otimes : C \times C \to C$ which is part of the data of any [[monoidal category]] $C$ is also often called a _tensor product_, since in many examples of monoidal categories it is induced from a tensor product in the above sense (and in fact, _any_ monoidal category underlies a multicategory in a canonical way).  In parts of the literature (certain) [[abelian category|abelian]] monoidal categories are even addressed as _tensor categories_. 

* Given two objects in a [[monoidal category]] $(C,\otimes)$ with a right and left [[action]], respectively, of some [[monoid]] $A$, their _tensor product over $A$_ is the quotient of their tensor product in $C$ by this action.  If $A$ is commutative, then this is a special case of the tensor product in a multicategory.

* This generalizes to modules over [[monad|monads]] in a bicategory, which includes the notion of _[[tensor product of functors]]_.  

* Finally, tensor products in a multicategory and tensor products over monads in a bicategory are both special cases of tensor products in a [[virtual double category]].

## Definitions

### In a multicategory

+-- {: .num_defn}
###### Definition


For $M$ a [[multicategory]] and $A$ and $B$ [[objects]] in $M$, the **tensor product** $A \otimes B$ is defined to be an object equipped with a [[universal construction|universal]] [[multimorphism]]  $A,B\to A \otimes B$ in that any multimorphism  $A,B\to C$ factors uniquely through $A,B\to A \otimes B$ via a (1-ary) morphism $A \otimes B\to C$.

=--

+-- {: .num_example}
###### Example

$M$ is the category [[Ab]] of abelian groups, made into a [[multicategory]] using [[multilinear maps]] as the multimorphisms, then we get the usual [[tensor product of abelian groups]]. That is, $A \otimes B$ is equipped with a universal map from $A \times B$ (as a set) to $C$ such that this map is linear (a group homomorphism) in each argument separately.  This tensor product can also be constructed explicitly by

1. starting with the cartesian product $A\times B$ in sets,
1. generating a _free_ abelian group from it, and then
1. quotienting by relations $(a_1,b)+(a_2,b)\sim (a_1+a_2,b)$ and $(a,b_1)+(a,b_2)\sim (a,b_1+b_2)$.  (The 0-ary relations $(0,b)\sim 0$ and $(a,0)\sim 0$ follow automatically; you need them explicitly if you generalise to [[abelian monoid]]s.)

=--

Note that in this case, $A\otimes B$ is not a [[subobject]] _or_ a [[quotient]] of the [[cartesian product]] $A\times B$.  However, in many other cases the tensor product in a multicategory _can_ be obtained as a quotient of some other pre-existing product; see _[[tensor product of modules]]_ below.

Other examples of tensor products in multicategories:

+-- {: .num_example}
###### Example

The [[Gray tensor product]] of [[strict 2-category|strict 2-categories]] is a tensor product in the multicategory of 2-categories and [[cubical functor]]s.  Likewise for Sjoerd Crans' tensor product of Gray-categories.

=--

+-- {: .num_example}
###### Example


In particular, any [[closed category]] (even if not monoidal) has an underlying multicategory.  Tensor products in this multicategory are characterized by the adjointness relation
$$ \hom(A\otimes B, C) \cong \hom(A, \hom(B,C)). $$
This may be the oldest notion of tensor product, since the definition of the internal-hom of abelian groups and vector spaces, unlike that of their tensor product, is intuitively obvious.

=--


While the universal property referred to above (every bilinear map $A,B\to C$ factors uniquely through $A,B\to A\otimes B$ via a map $A\otimes B \to C$) suffices to define the tensor product, it does not suffice to prove that it is associative and unital.  For this we need the stronger property that any multilinear map $D_1,\dots,D_m,A,B,E_1,\dots, E_n \to C$ factors uniquely through $A,B\to A\otimes B$ via a multilinear map $D_1,\dots,D_m, A\otimes B ,E_1,\dots, E_n \to C$.

### In terms of heteromorphisms

An alternative approach is to define the tensor product via an inter-categorical universal property involving [[heteromorphism|heteromorphisms]]. Tensor products do not always arise via an adjunction, but we can observe that $ hom (a \otimes b, c) \simeq het (\langle a, b \rangle, c) $ in general. That is to say, any morphism from $a \otimes b$ to $c$ in some category $C$ corresponds to a heteromorphism from $\langle a, b \rangle$ in $C \times C$ to $c$ in $C$. In other words, the tensor product is a left representation of $het (\langle a, b \rangle, c)$.

When tensor products exist, we have a canonical het $\eta_{\langle a, b \rangle} \colon \langle a, b \rangle \to a \otimes b$ from $id_{a \otimes b} \in hom (a \otimes b, a \otimes b)$. Given another het $\phi \colon \langle a, b \rangle \to c$, we get the following commutative diagram.


$$
\begin{array}{cccC}
                                                 & {\langle a, b \rangle} &  &   & \\
          \eta_{\langle a, b \rangle} & \downarrow           & \overset{\phi}\searrow       &     & \\
                                                 & a \otimes b            & \underset{f}\dashrightarrow & c &  \\ \end{array}
$$



This represents an example of a more general method for translating universal properties in multicategories into ones involving heteromorphisms.

### Of modules in a monoidal category

Let $R$ be a [[commutative ring]] and consider the multicategory $R$[[Mod]] of $R$-[[modules]] and $R$-[[multilinear maps]].  In this case the 
[[tensor product of modules]] $A\otimes_R B$ of $R$-modules $A$ and $B$ can be constructed as the [[quotient]] of the [[tensor product of abelian groups]] $A\otimes B$ underlying them by the [[action]] of $R$; that is,
$$ A\otimes_R B = A\otimes B / (a,r\cdot b) \sim (a\cdot r,b). $$

More category-theoretically, this can be constructed as the [[coequalizer]] of the two maps
$$ A\otimes R \otimes B \;\rightrightarrows\; A\otimes B $$
given by the action of $R$ on $A$ and on $B$.  

If $R$ is a [[field]], then $R$-modules are vector spaces; this gives probably the most familiar case of a tensor product spaces, which is also probably the situation where the concept was first conceived.

This tensor product can be generalized to the case when $R$ is not commutative, as long as $A$ is a right $R$-module and $B$ is a left $R$-module.  More generally yet, if $R$ is a [[monoid]] in any [[monoidal category]] (a ring being a monoid in [[Ab]] with its tensor product), we can define the tensor product of a left and a right $R$-module in an analogous way.  If $R$ is a commutative monoid in a [[symmetric monoidal category]], so that left and right $R$-modules coincide, then $A\otimes_R B$ is again an $R$-module, while if $R$ is not commutative then $A\otimes_R B$ will no longer be an $R$-module of any sort.

* Not all tensor products in multicategories are instances of this construction.  In particular, the tensor product in [[Ab]] is not the tensor product of modules over any monoid in the cartesian monoidal category [[Set]].  Abelian groups _can_ be considered as "sets with an action by something," but that something is more complicated than a monoid: it is a special sort of [[monad]] called a [[commutative theory]].

* Conversely, if $R$ is a _commutative_ monoid in a symmetric monoidal category, there is a multicategory of $R$-modules whose tensor product agrees with the coequalizer defined above, but if $R$ is not commutative this is impossible.  However, see the section on tensor products in virtual double categories, below.

### Of modules in a bicategory

The tensor product of left and right modules over a noncommutative monoid in a monoidal category is a special case of the tensor product of modules for a [[monad]] in a [[bicategory]].  If $R: x\to x$ is a monad in a bicategory $B$, a right $R$-module is a 1-cell $A: y\to x$ with an action by $R$, a left $R$-module is a 1-cell $B: x\to z$ with an action by $R$, and their tensor product, if it exists, is a 1-cell $y\to z$ given by a similar coequalizer.  Regarding a monoidal category as a 1-object bicategory, this recovers the above definition.

For example, consider the bicategory $V-Mat$ of $V$-valued [[matrix|matrices]] for some monoidal category $V$.  A monad in $V-Mat$ is a $V$-[[enriched category]] $A$, an $(A,I)$-bimodule is a functor $A\to V$, an $(I,A)$-bimodule is a functor $A^{op}\to V$, and their tensor product in $V-Mat$ is a classical construction called the **[[tensor product of functors]]**.  It can also be defined as a [[coend]].

### In a virtual double category

A [[virtual double category]] is a common generalization of a multicategory and a bicategory (and actually of a [[double category]]).  Among other things, it has objects, 1-cells, and "multi-2-cells."  We leave it to the reader to define a notion of tensor product of 1-cells in such a context, analogous to the tensor product of objects in a multicategory.  A multicategory can be regarded as a 1-object virtual double category, so this generalizes the notion of tensor product in a multicategory.

On the other hand, in any bicategory (in fact, any double category) there is a virtual double category whose objects are monads and whose 1-cells are bimodules, and the tensor product in this virtual double category is the tensor product of modules in a bicategory defined above.  Thus, tensor products in a virtual double category include all notions of tensor product discussed above.


## Examples

* [[tensor product of abelian groups]]

* [[tensor product of groups]]

* [[tensor product of modules]]

* [[tensor product of vector spaces]]

  * [[inductive tensor product]]

* [[smash product]] of [[pointed sets]]

* [[tensor product of representations]]

* [[tensor product of vector bundles]]

* [[tensor product of algebras]]

* [[tensor product of algebras over a commutative monad]]

* [[tensor product of Lie algebras]]

* [[tensor product of chain complexes]]

* [[tensor product of Banach spaces]]

* [[tensor product of functors]]

* [[enriched product category|tensor product of enriched categories]]

* [[Deligne tensor product of abelian categories]]

* [[tensor product of presentable (infinity,1)-categories]]

* in terms of [[linear type theory]] the tensor product is the [[categorical semantics]] of the [[multiplicative conjunction]].


## Related concepts

* [[tensor calculus]]

* [[cartesian product]]

* [[external tensor product]]

* [[internal hom]]

* [[cotensor product]]

* [[pushout product]]

* [[multiplicative conjunction]], [[quantum entanglement]]

* [[composite system]]


[[!include homotopy-homology-cohomology]]



## References

Tensor products were introduced by [[Hassler Whitney]] in

* [[Hassler Whitney]], _Tensor products of Abelian groups_, Duke Mathematical Journal 4:3 (1938), 495-528.  [doi](https://doi.org/10.1215/s0012-7094-38-00442-9).

Lecture notes:

* [[Keith Conrad]], *Tensor products* &lbrack;part I:[pdf](http://www.math.uconn.edu/~kconrad/blurbs/linmultialg/tensorprod.pdf), [[Conrad-TensorProductsI:file]]; part II: [pdf](https://kconrad.math.uconn.edu/blurbs/linmultialg/tensorprod2.pdf), [[Conrad-TensorProductsII:file]]&rbrack;

For more on the  

* [[tensor product of modules]]

* [[tensor product of vector spaces]]

see there.

For the [[category theory|category theoretic]] formalization of tensor products see the references at

* *[[monoidal category]]* and *[[tensor category]]*

Formalization of tensor products in [[dependent linear type theory]]:

* {#Riley22Thesis} [[Mitchell Riley]], *A Bunched Homotopy Type Theory for Synthetic Stable Homotopy Theory*, PhD Thesis (2022) &lbrack;[doi:10.14418/wes01.3.139](https://doi.org/10.14418/wes01.3.139), [ir:3269](https://digitalcollections.wesleyan.edu/object/ir%3A3269), [pdf](https://mvr.hosting.nyu.edu/pubs/thesis.pdf)&rbrack;



[[!redirects tensor products]]
