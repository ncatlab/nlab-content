
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

* **algebraic theory** / [[Lawvere theory]] / [[2-Lawvere theory]] /  [[(∞,1)-algebraic theory]]

* [[monad]] / [[(∞,1)-monad]]

* [[operad]] / [[(∞,1)-operad]]

***


# Algebraic theories
* tic
{: toc}


## Idea

An _algebraic [[theory]]_ is a concept in [[universal algebra]] that describes a specific type of algebraic gadget, such as [[group|groups]] or [[ring|rings]]. An individual group or ring is a _model_ of the appropriate theory. Roughly speaking, an algebraic theory consists of a specification of operations and laws that these operations must satisfy.

Traditionally, algebraic theories were described in terms of [[logic]].  But _finitary_ algebraic theories (that is, those involving only finitary operations) can be understood category-theoretically as [[Lawvere theory|Lawvere theories]].  More generally, algebraic theories involving only operations of arity bounded by some [[cardinal number]] can be understood category-theoretically with a suitably generalization of Lawvere theories.  However, there are also algebraic theories with operations of unbounded arity, such as  the theory of algebras in which arbitrary sums are possible (one model of which is $[0,\infty]$), or the theory of [[complete lattice]]s; these can also be modeled by certain 'large Lawvere theories,' but the notion is not as well-behaved as in the bounded case; see [this thread](http://golem.ph.utexas.edu/category/2009/04/report_on_88th_peripatetic_sem.html#c023188).

Algebraic theories (finitary or otherwise) can also be understood through [[monad]]s; in fact, some category theorists define an [[algebraic category]] to be one that is [[monadic functor|monadic]] over [[Set]].  For example, the theory of a [[compact Hausdorff space]] $X$ can be seen as algebraic, with one operation for each [[direction|directed set]] $D$ that takes an [[net|ultranet]] indexed by $D$ to its limit; this is a finitary operation only when $D$ is finite (which is really the trivial case).  There is no Lawvere theory for compact Hausdorff spaces (at least, no small one), yet there is a monad for it, which maps each set $S$ to its set of [[ultrafilter]]s.

Here is the connection between the logical and categorial descriptions, based on [Johnstone][], &#167;&#167;3.7&8.  Say that a category $C$ is:

* _[[algebraic category|algebraic]]_ if it is given by a monad on the category of (small) sets;
* _small algebraic_ if it is given by a (small) set of operation symbols and equations;
* _large algebraic_ if it is given by a (possibly proper) class of operation symbols and equations.

Then any small algebraic category is algebraic, and any algebraic category is large algebraic, but neither implication may be reversed.

_[[essentially algebraic theory|Essentially algebraic theories]]_ allow for partially-defined operations.  Just as finitary algebraic theories can be understood as Lawvere theories, which live in the [[doctrine]] of [[cartesian monoidal category|cartesian monoidal categories]], so finitary essentially algebraic theories can be understood by a generalisation to [[finitely complete category|finitely complete categories]].

_[[commutative algebraic theory|Commutative algebraic theories]]_ form an important subclass. Their categories of models are closed: the Hom sets have a natural model-structure, and the enriched Hom-functor has a left adjoint, _tensor-product_. The theory of complete lattices and suprema-preserving functions is an interesting (non-finitary) example.


## Metaphor

Ring theory is a branch of mathematics with a well-developed terminology. A ring $A$ determines and is determined by an algebraic theory, whose models are left $A$-modules and whose n-ary operations have the form
$$(x_1,\ldots ,x_n) \to a_1x_1+\ldots +a_n x_n$$
for some n-ple $(a_1,\ldots ,a_n)$ of elements of $A$. We may call such an algebraic theory **annular**. The pun _model/module_ is due to Jon Beck. The notion that an algebraic theory is a generalized ring is often a fertile one, that automatically provides a slew of suggestive terminology and interesting problems. Many fundamental ideas of ring/module-theory are simply the restriction to annular algebraic theories of ideas that apply more widely to algebraic theories and their models.

Let us denote the category of models and homomorphisms (in $Set$) of an algebraic theory $A$ by $A Mod$.  Then compare the following to their counterparts in ring theory:
*  [[tensor product theory|Tensor Product of Theories]]
*  [[matrix theory|Matrix Theories]]
*  [[bimodel|Bimodels]]


## In higher category theory

* [[(∞,1)-algebraic theory]]


## References

* <span id="Johnstone"></span>
  [[Peter Johnstone]], _[[Stone Spaces]]_
  [Johnstone]: #Johnstone

_Someone should improve this article so that it gives a **definition** of 'algebraic theory' before considering special cases such as 'commutative algebraic theory'._


[[!redirects algebraic theories]]