
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Introduction

The axioms of [[synthetic differential geometry]] are intended to pin down the minimum [[category theory|general abstract]] [[axioms]] necessary for talking about the _differential_ aspect of [[differential geometry]] using concrete objects that model [[infinitesimal spaces]].

But the typical _models_ for the axioms -- the typical [[smooth toposes]] -- are constructed in close analogy to the general mechanism of [[algebraic geometry]]: [[Models for Smooth Infinitesimal Analysis|well-adapted models]] for [[smooth toposes]] use [[sheaf|sheaves]] on $C^\infty Ring^{op}$ (the [[opposite category]] of [[generalized smooth algebra|smooth algebras]]) where spaces in [[algebraic geometry]] (such as [[scheme]]s) uses [[sheaf|sheaves]] on [[CRing]]${}^{op}$.

In fact, for instance also the [[topos]] of [[presheaf|presheaves]] on $k-Alg^{op}$, which one may think of as being a context in which much of [[algebraic geometry]] over a [[field]] $k$ takes place, happens to satisfy the axioms of a [[smooth topos]] (see the examples there).

This raises the question:

+-- {: .standout}

**Questions**

To which degree do results in [[algebraic geometry]] depend on the choice of [[site]] [[CRing]]${}^{op}$ or similar?

To which degree are these results valid in a much wider context of any [[smooth topos]], or smooth topos with certain extra assumptions?

In the general context of [[structured (∞,1)-topos]]es and [[generalized scheme]]s: how much of the usual lore depends on the choice of the (simplicial)ring-theoretic Zariski or etale [[geometry (for structured (∞,1)-toposes)|(pre)geometry (for structured (∞,1)-toposes)]], how much works more generally?

=--

It is curious that the field of algebraic geometry has induced, first with [[Alexander Grothendieck]] now with [[Jacob Lurie]], so much [[category theory]] and [[higher category theory]], while at the same time it is common practice in this field to effectively disregard one of the major guidelines that practitioners in pure [[category theory]] are fond of adhering to: that of separation of context and implementation. [[Bill Lawvere]]'s famous dichotomy between _theory_ and _model_.

In fact, it seems that [[William Lawvere]] found the axioms of [[synthetic differential geometry]] not without the idea of capturing central structures in [[algebraic geometry]] this way, too. But, possibly due to the very term chosen, [[synthetic differential geometry]] it has apparently always (if at all) attracted more the attention of those interested in ordinary [[differential geometry]] than those interested in [[algebraic geometry]].

But at least in the light of [[Jacob Lurie|Lurie]]'s notion of [[structured (∞,1)-topos]]es and [[generalized scheme]]s, from the point of which ordinary [[algebraic geometry]] as well as [[derived algebraic geometry]] is just one realization of a more general concept of geometry, it seems to be worthwhile to reexamine the wealth of knowledge accumulated in algebraic geometry and see how much of it depends on just general context, how much on concrete implementation.

## Facts

### Functions in the big Zariski topos 

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[scheme]] and $Sh(Sch/X)$ the [[Zariski site|big Zariski topos]] associated to $X$. Denote by $\mathbb{A}^1$ (the [[affine line]]) the [[ring object]] $T \mapsto \Gamma(T,\mathcal{O}_T)$, i.e. the functor represented by the $X$-scheme $\mathbb{A}^1_X \coloneqq X \times Spec(\mathbb{Z}[t])$. Then:

* $\mathbb{A}^1$ is [[internal logic|internally]] a [[local ring]].

* $\mathbb{A}^1$ is internally a [[field]] in the sense that any nonzero element is invertible.

* Internally, any [[function]] $f : \mathbb{A}^1 \to \mathbb{A}^1$ is a [[polynomial]] function, i.e. of the form $f(x) = \sum_i a_i x^i$ for some coefficients $a_i : \mathbb{A}^1$. More precisely,
$$ Sh(Sch/X) \models \forall f : [\mathbb{A}^1,\mathbb{A}^1]. \bigvee_{n \in \mathbb{N}} \exists a_0,\ldots,a_n : \mathbb{A}^1. \forall x : \mathbb{A}^1. f(x) = \sum_i a_i x^i. $$
Furthermore, these coefficients are uniquely determined.

=--

+-- {: .proof}
###### Proof

See _[[affine line#InternalFormulation]]_.

=--

+-- {: .num_remark}
###### Remark

Since the big Zariski topos is [[cocomplete category|cocomplete]] (being a [[Grothendieck topos]]), one can also get rid of the external [[disjunction]] and refer to the object $\mathbb{A}^1[X]$ of internal polynomials: The canonical ring homomorphism $\mathbb{A}^1[X] \to [\mathbb{A}^1,\mathbb{A}^1]$ (given by evaluation) is an [[isomorphism]].

=--


## Questions

> this is old material that needs attention


### Coherent sheaves #


To which degree can the notion of [[quasicoherent sheaf]] generalize from a context modeled on the [[site]] [[CRing]] to a more general context. What is, for instance, a quasicoherent sheaf on a [[derived smooth manifold]]? If at all? What on a general [[generalized scheme]], if at all?


### geometric $\infty$-function theory ##

Closely related to that: [[David Ben-Zvi]] et al have developed a beautiful theory of integral transforms on [[derived stack|derived]] [[∞-stack]], as described at [[geometric ∞-function theory]]. 

But in their construction it is always assumed that the underlying [[site]] is the (derived) algebraic one, something like simplicial rings. 

 How much of their construction actually depends on that assumption? How much of this work carries over to other choices of [[geometry (for structured (∞,1)-toposes)|geometries]]?

For instance, when replacing the category of [[ring]]s /[[affine scheme]] in this setup with that of [[generalized smooth algebra|smooth algebra]] / [[smooth locus|smooth loci]], how much of the theory can be carried over?

It seems that the crucial and maybe only point where they use the concrete form of their underlying [[site]] is the definition of [[quasicoherent sheaf]] on a [[derived stack]] there, which uses essetnially verbatim the usual definition $QC(-) : Spec(A) \mapsto A Mod$.

What is that more generally? What is $A Mod$ for $A$ a [[generalized smooth algebra|smooth algebra]]?

If that doesn't have a good answer, maybe there is a more _intrinsic_ way to say what quasicoherent sheaves on an [[∞-stack]] are, such that it makes sense on more general [[generalized scheme]]s.





## References


Somebody points out the discussion here

* [http://www.mta.ca/~cat-dist/catlist/1999/finite-topos](http://www.mta.ca/~cat-dist/catlist/1999/finite-topos)

on formulating finitely-presented conditions internally in a topos. In particular [[William Lawvere]]'s message (the third one from the top).