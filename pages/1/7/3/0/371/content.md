
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--


# Zero objects
* table of contents
{: toc}


## Definition

A **zero object**, or **null object**, is an [[object]] of a [[category]] that is both an [[initial object]] and a [[terminal object]].  Equivalently, a category has a zero object iff it has an initial object $\bot$ and a terminal object $\top$ and the unique morphism $\bot\to\top$ is an [[isomorphism]].  A category with a zero object is sometimes called a [[pointed category]].


## Examples

+-- {: .un_prop}
###### Proposition


* The [[category of pointed sets]] has a zero object, namely any one-element set.  

* The trivial group is a zero object in the category [[Grp]] of [[groups]] and [[Ab]] of [[abelian group|abelian groups]].  

* However, the zero [[ring]] is not a zero object in the category of [[ring|rings]], at least as long as rings are required to have units (and ring homomorphisms to preserve them).

* For every category $C$ with a [[terminal object]] $*$ the [[over category|under category]] $pt \downarrow C$ of [[pointed object]]s in $C$ has a zero object: the morphism $Id_{pt}$.

=--

+-- {: .un_prop}
###### Proposition

In any category $C$ [[enriched category|enriched]] over the [[category of pointed sets]] $(Set_*, \wedge)$ with [[tensor product]] the [[smash product]], any object that is either initial _or_ terminal object is automatically both and hence a zero object.  

=--

+-- {: .proof}
###### Proof

Write $* \in Set_*$ for the singleton pointed set. Suppose $t$ is [[terminal object|terminal]]. Then $C(x,t) = *$ for all $x$ and so in particular $C(t,t) = *$ and hence the [[identity]] morphism on $t$ is the basepoint in the pointed [[hom-set]]. By the axioms of a [[category]], every morphism $f : t \to x$ is equal to the composite

$$
  f : t \stackrel{Id}{\to} t \stackrel{f}{\to} x
  \,.
$$

By the axioms of an $(Set_*, \wedge)$-enriched category, since $Id_{t}$ is the basepoint in $C(t,t)$, also this composite is the basepoint in $C(t,x)$ and is hence the [[zero morphism]]. So $C(t,x) = *$ for all $x$ and therefore $t$ is also an [[initial object]].

Analogously from assuming $t$ to be initial it follows that it is also terminal.

=--

+-- {: .un_remark}
###### Remark


This is a special case of an [[absolute limit]].  

=--

+-- {: .un_remark}
###### Remark

Categories enriched in $(Set_*, \wedge)$ include in particular [[Ab]]-enriched categories. So any [[additive category]], hence every [[abelian category]] has a zero object.

=--


## Properties

In a category with a zero object 0, there is always a canonical morphism from any object $A$ to any other object $B$ called the _[[zero morphism]]_, given by the composite $A\to 0 \to B$. Thus, such a category becomes [[enriched category|enriched]] over the [[category of pointed sets]], a partial converse to the last example above.


## Related concepts

* [[pointed category]]
* [[zero object in a derivator]]


[[!redirects zero object]]
[[!redirects zero objects]]
[[!redirects 0 object]]
[[!redirects 0 objects]]
[[!redirects null object]]
[[!redirects null objects]]

[[!redirects 0-object]]
