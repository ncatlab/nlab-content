
#Contents#
* automatic table of contents goes here
{:toc}

#Introduction#

The axioms of [[synthetic differential geometry]] are intended to pin down the minimum [[category theory|abstract nonsense]] necessary for talking about the _differential_ aspect of [[differential geometry]] using concrete objects that model [[infinitesimal space]]s.

But the typical _models_ for the axioms -- the typical [[smooth topos]]es -- are constructed in close analogy to the general mechanism of [[algebraic geometry]]: [[Models for Smooth Infinitesimal Analysis|well-adapted models]] for [[smooth topos]]es use [[sheaf|sheaves]] on $C^\infty Ring^{op}$ (the [[opposite category]] of [[generalized smooth algebra|smooth algebra]]s) where spaces in [[algebraic geometry]] (such as [[scheme]]s) uses [[sheaf|sheaves]] on [[CRing]]${}^{op}$.

In fact, for instance also the [[topos]] of [[presheaf|presheaves]] on $k-Alg^{op}$, which one may think of as being a context in which much of [[algebraic geometry]] over a [[field]] $k$ takes place, happens to satisfy the axioms of a [[smooth topos]] (see the examples there).

This raises the question:

+-- {: .standout}

**Questions**

To which degree do results in [[algebraic geometry]] depend on the choice of [[site]] [[CRing]]${}^{op}$ or similar?

To which degree are these results valid in a much wider context of any [[smooth topos]], or smooth topos with certain extra assumptions?

In the general context of [[structured (∞,1)-topos]]es and [[generalized scheme]]s: how much of the usual lore depends on the choice of the (simplicial)ring-theoretic Zariski or etale [[geometry (for structured (∞,1)-toposes)|(pre)geometry (for structured (∞,1)-toposes)]], how much works more generally?

=--

It is curious that the field of algebraic geometry has induced, first with [[Alexander Grothendieck]] now with [[Jacob Lurie]], so much [[category theory]] and [[higher category theory]], while at the same time it is common practice in this field to effectively disregard one of the major guidelines that practitioners in pure [[category theory]] are fond of adhering to: that of separation of context and implementation. [[Bill Lawvere]]'s famous dichotomy between _theory_ and _model_ .

In fact, it seems that [[Lawvere]] dreamed up the axioms of [[synthetic differential geometry]] not without the idea of capturing central structures in [[algebraic geometry]] this way, too. But, possibly due to the very term chosen, [[synthetic differential geometry]] it has apparently always (if at all) attracted more the attention of those interested in ordinary [[differential geometry]] than those interested in [[algebraic geometry]].

But at least in the light of [[Jacob Lurie|Lurie]]'s notion of [[structured (∞,1)-topos]]es and [[generalized scheme]]s, from the point of which ordinary [[algebraic geometry]] as well as [[derived algebraic geometry]] is just one realization of a more general concept of geometry, it seems to be worthwhile to reexamine the wealth of knowledge accumulated in algebraic geometry and see how much of it depends on just general context, how much on concrete implementation.


#Qestions#


## Coherent sheaves ##


To which degree can the notion of [[quasicoherent sheaf]] generalize from a context modeled on the [[site]] [[CRing]] to a more general context. What is, for instance, a quasicoherent sheaf on a [[derived smooth manifold]]? If at all? What on a general [[generalized scheme]], if at all?


## geometric $\infty$-function theory ##

Closely related to that: [[David Ben-Zvi]] et al have developed a beautiful theory of integral transforms on [[derived stack|derived]] [[∞-stack]], as described at [[geometric ∞-function theory]]. 

But in their construction it is always assumed that the underlying [[site]] is the (derived) algebraic one, something like simplicial rings. 

 How much of their construction actually depends on that assumption? How much of this work carries over to other choices of [[geometry (for structured (∞,1)-toposes)|geometries]]?

For instance, when replacing the category of [[ring]]s /[[affine scheme]] in this setup with that of [[generalized smooth algebra|smooth algebra]] / [[smooth locus|smooth loci]], how much of the theory can be carried over?

It seems that the crucial and maybe only point where they use the concrete form of their underlying [[site]] is the definition of [[quasicoherent sheaf]] on a [[derived stack]] there, which uses essetnially verbatim the usual definition $QC(-) : Spec(A) \mapsto A Mod$.

What is that more generally? What is $A Mod$ for $A$ a [[generalized smooth algebra|smooth algebra]]?

If that doesn't have a good answer, maybe there is a more _intrinsic_ way to say what quasicoherent sheaves on an [[∞-stack]] are, such that it makes sense on more general [[generalized scheme]]s.

### a proposed reply ###

>[[Urs Schreiber|Urs]]:

Here is a proposal for how one might answer this very generally:

One observation is that the [[monoidal Dold-Kan correspondence]] identifies (co)simplicial algebras with [[dg-algebra]]s. To say [[dg-algebra]] in a general context we need to say [[module]], which may be hard in generalized situations such as working over [[generalized smooth algebra]]s. On the other hand, it is straightforward to speak of cosimplicial smooth algebras of course.

This is the idea underlying the discussion at [[schreiber:∞-quantity]]. To that we add the observation that cosimplicial algebras that under the [[monoidal Dold-Kan correspondence]] maps to a _graded commutative_ [[dg-algebra]] may be thought of as a [[schreiber:∞-Lie algebroid|∞-Lie algebroid]], as explained there. In its ordinary incarnation (see [[L-infinity algebroid]]) this is a complex of modules over the degree 0  algebra with some extra structure. So in light of this a cosimplicial algebra that maps under monoidal Dold-Kan to something graded-commutative might be a good very general abstract nonsense substitute for complexes of modules.

So for $\ell A$ a [[smooth locus]] or similar, consider [[(∞,1)-category]] $\infty Lie Algd/\ell A$ of cosimplicial algebras _under_ $A$ that have graded commutative Dold-Kan image.

Then maybe a good substitute for QC(-) is 

$$
  QC(-) : \ell A \mapsto \infty LieAld/\ell A
  \,.
$$

Being an [[over category]], this would match well with the reasoning at [[geometric function object]].

## further questions ##

will go here...


