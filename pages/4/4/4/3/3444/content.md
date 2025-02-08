
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[category]] of all [[representation]]s of [[algebra|algebraic]] structures $C$ of some kind.

## Definition

### Of groups, algebras, groupoids, algebroids, etc.

A typical such algebraic structure is a [[category]]. We may think of [[groups]] $G$ , and [[associative algebras]] $A$ as special cases of this by passing to their [[delooping]] $C = \mathbf{B}G$ or $C = \mathbf{B}A$. More generally $C$ may be a [[groupoid]] or [[algebroid]]. 

For all these cases, a [[representation]] of $C$ on [[objects]] in another [[category]] $D$ (for instance [[Set]] for [[permutation representations]] or  [[Vect]] for [[linear representations]]) is nothing but a [[functor]] $C \to D$. 

In this case the **representation category** $Rep(C)$ is nothing but the [[functor category]] 

$$
  Rep(C) = Func(C,D)
  \,.
$$

Notably when $G$ is a [[group]], an ordinary linear representation is a [[functor]] $\mathbf{B}G \to Vect$ from the [[delooping]] [[groupoid]] of $G$ to [[Vect]], and so the representation category is

$$
  Rep(G) = Func(\mathbf{B}G,Vect)
  \,.
$$

Often $C$ and $D$ are regarded as equipped with some extra [[structure]] (for instance [[topology]], [[smooth structure]]) and then the functors above are required to respect that structure.

### Higher and internal representations

In the context of [[homotopy theory]] and [[higher category theory]] there are analogous definitions of [[∞-representations]]. 

For $G$ an [[∞-group]] and $\mathbf{B}G$ its [[delooping]] [[∞-groupoid]], an $\infty$-representation on objects of some [[(∞,1)-category]] $D$ (such as that of [[(∞,n)-vector spaces]]) is the [[(∞,1)-category of (∞,1)-functors]]

$$
  Rep(G) = Func(\mathbf{B}G, D)
  \,.
$$

If $D  \simeq$ [[∞Grpd]] this are [[∞-permutation representations]] and by the [[(∞,1)-Grothendieck construction]] any such corresponds to an [[associated ∞-bundle]]

$$
  V \to V//G \to \mathbf{B}G
$$

over $\mathbf{B}G$ in such a way that we have an [[equivalence of (∞,1)-categories]]

$$
  Rep(G, \infty Grpd)
  \simeq
  \infty Grpd_{/\mathbf{B}G}
$$

with the [[over-(∞,1)-category]] of [[∞-groupoids]] over $\mathbf{B}G$.

This way of looking at categories of representations generalizes to every [[(∞,1)-topos]] $\mathbf{H}$ of [[homotopy dimension]] 0.

In this context any morphism $\rho : Q \to \mathbf{B}G$ encodes a representation of $G$ on the [[homotopy fiber]] $V$ of $\rho$, identifying $Q$ as $V//G$. 

The assumption that $\mathbf{H}$ has [[homotopy dimension]] 0 guarantees that the homotopy fiber exists (since a global point $* \to \mathbf{B}G$ exists) and is well defined up to [[equivalence in an (∞,1)-category]].

## Properties

### Tannakian reconstruction

Representation categories come with [[forgetful functor]]s that send a representation to the underlying object that carries the representation.

For instance for group representations the canonical inclusion ${*} \to \mathbf{B}G$ induces the functor $Func(\mathbf{B}G,Vect) \to Func(*,Vect)$, hence

$$
  F : Rep(G) \to Vect
$$

that sends a representation to its underlying [[vector space]]. The [[Tannakian reconstruction theorem]] says that the group $G$ may be recovered essentially as the group of [[automorphism]]s of the fiber functor $F$.

## Related concepts

* [[GSet]]

* [[tensor product of representations]]


## References

The lecture notes

* _Monoidal Categories_ MIT course (2009) ([pdf](http://ocw.mit.edu/courses/mathematics/18-769-topics-in-lie-theory-tensor-categories-spring-2009/lecture-notes/MIT18_769S09_lec01.pdf))

list some basic examples of [[monoidal category|monoidal]] representation categories from page 7 on.

A standard textbook on [[representation theory]] of [[compact space|compact]] [[Lie groups]] is

* Theodor Br&#246;cker, [[Tammo tom Dieck]], _Representations of compact Lie groups_ Graduate Texts in Mathematics, Springer (1985)

The stable [[triangulated category]] of representations of a [[finite group]]:

* [[Fernando Muro]], around slide 105 of _Triangulated categories_, 2009 [pdf](http://personal.us.es/fmuro/files/slides/htag.pdf)

category: category

[[!redirects categories of representations]]

[[!redirects GRep]]
[[!redirects G-Rep]]
[[!redirects Rep]]

[[!redirects representation category]]
[[!redirects representation categories]]



