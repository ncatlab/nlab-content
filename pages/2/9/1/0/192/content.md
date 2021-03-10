
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Categories of categories
+-- {: .hide}
[[!include categories of categories - contents]]
=--
=--
=--

# The category of sets
* table of contents
{: toc}

## Definition

__$Set$__ is the (or a) [[category]] with [[sets]] as [[objects]] and [[functions]] between sets as [[morphisms]]. 

This definition is somewhat vague by design. Rather than canonize a fixed set of principles, the nLab adopts a 'pluralist' point of view which recognizes different needs and foundational assumptions among mathematicians who use set theory. Thus, there are various axes to consider when formulating categorical properties one thinks $Set$ should satisfy, including 

* First-order vs. higher-order logic 

* Impredicative vs. [[predicative mathematics]] 

* 'Variability' vs. 'constancy' (Lawvere)  

* Classical logic vs. intuitionistic logic 

* Choice principles 

* Replacement or collection principles 

* Smallness structures 

just to name a few. Quite a bit of axiomatic fine-tuning can enter when one considers the panoply of hypotheses that might appeal to one or another school of intuitionism or constructivism, or various combinatorial or cardinal hypotheses one might attach to ZFC, etc. 

## Properties

### Characterization

The category $Set$ has many marvelous properties, which make it a common choice for serving as a '[[foundations|foundation]]' of mathematics.  For instance:

* It is a [[well-pointed category|well-pointed]] {:yes} [[topos]]{:}, 

  So in particular it is [[locally cartesian closed category|locally cartesian closed]].

* It is {:yes} [[locally small]]{:}.

* It is [[complete category|complete]] and [[cocomplete category|cocomplete]], and therefore $\infty$-[[extensive category|extensive]] (as is any cocomplete topos).{:data complete="yes" co-complete="yes"}

At least assuming [[classical logic]], these properties suffice to characterize $Set$ uniquely up to equivalence among all categories; see [[cocomplete well-pointed topos]].  Note, however, that the definitions of "locally small" and "(co)complete" presuppose a notion of _small_ and therefore a knowledge of what a _set_ (as opposed to a [[proper class]]) is.

As a groupoid, $Set$ is characterized by the fact that 

* $Set$ is the [[discrete object classifier]] in the category [[Grpd]] of [[groupoids]] and [[functors]], playing a similar role in classifying discrete groupoids in $Grpd$ that the set of truth values $\Omega$ does in classifying subsets in $Set$. The morphism $F:I \rightarrow Set$ is an [[indexed family]] of sets and $I$ is an index groupoid. 

As a [[topos]], $Set$ is also characterized by the fact that

* $Set$ is the [[terminal object]] in the [[category]] of [[Grothendieck toposes]] and [[geometric morphism]]s. The terminal morphism $\Gamma\colon E \to Set$ from any other topos $E$ is the [[global section]]s functor.

It is usually assumed that $Set$ satisfies the [[axiom of choice]] and has a [[natural numbers object]].  In Lawvere's theory [[ETCS]], which can serve as a foundation for much of mathematics, $Set$ is asserted to be a well-pointed topos that satisfies the axiom of choice and has a natural numbers object.  It follows that it is automatically "locally small" and "complete and cocomplete" relative to the notion of "smallness" defined in terms of itself (actually, this is true for any topos).

Conversely, $\Set$ in [[constructive mathematics]] cannot satisfy the axiom of choice (since this implies [[excluded middle]]), although constructivists might accept [[COSHEP]] (that $Set$ has [[projective object|enough projectives]]).  In [[predicative mathematics]], $\Set$ is not even a topos, although most predicativists would still agree that it is a [[pretopos]], and predicativists of the constructive school would even agree that it is a [[locally cartesian closed category|locally cartesian closed]] pretopos.


### Size

Above we considered $Set$ to be the category of _all_ sets, so that in particular $Set$ itself is a [[large category]].  Authors who assume a [[Grothendieck universe]] as part of their [[foundations]] often define $Set$ to be the category of *small* sets (those contained in the universe).  One often then writes $SET$ for the category of *large* sets, which is the [[universe enlargement]] of $Set$.

### Opposite category and Boolean algebras
 {#OppositeCategory}

+-- {: .num_prop}
###### Proposition

The [[power set]]-[[functor]]

$$
  \mathcal{P} \;\colon\; Set \to Bool^{op}
$$

is a [[faithful functor]] which in its [(eso+full, faithful) factorization](http://ncatlab.org/nlab/show/%28eso%2Bfull%2C+faithful%29+factorization+system) induces an [[equivalence of categories]] between $Set$ and the [[opposite category]] of that of [[complete atomic Boolean algebras]].

=--

See for instance [van Oosten, theorem 2.4](#vanOosten)

+-- {: .num_remark}
###### Remark

Restricted to [[FinSet]] this equivalence restricts to an equivalence with finite Boolean algebras. See at _[[Stone duality]]_ for more on this.

=--

+-- {: .num_remark}
###### Remark

In constructive mathematics, $\mathcal{P}$ defines an equivalence of $\Set$ with the opposite category of that of [[complete lattice|complete]] [[atom|atomic]] [[Heyting algebras]]. In fact, for any elementary [[topos]] $\mathcal{E}$, the [[power object]] functor defines an equivalence of $\mathcal{E}$ with the opposite category of that of internal complete atomic Heyting algebras. (This phrase can be interpreted using the [[internal language]] of $\mathcal{E}$.)

=--

## Related categories

A variant of $Set$ where [[functions]] are generalized to [[relations]] is _[[Rel]]_.

In [[higher category theory]] the role of _$Set$_ is played for instance by

* [[Pos]]

* [[Grpd]], [[∞Grpd]]

* [[Cat]],  [[(∞,1)Cat]]

* [[(∞,n)Cat]]

## References

* [[Jaap van Oosten]], _Basic category theory_ ([pdf](http://www.staff.science.uu.nl/~ooste110/syllabi/catsmoeder.pdf))
 {#vanOosten}

category: category

[[!redirects Sets]]
[[!redirects SET]]
[[!redirects category of sets]]
[[!redirects the category of sets]]

{:data
name="\(\mathbf{Set\}\)"
wp="Category of sets"
key=Set
desc="Sets with functions"
small="no"
concrete="yes"
skeleton="Cardinals"
abelian=no
imp_enrich=""
imp_monoidal="cartesian product"
imp_adj=""
imp_equ=""
Mono=Injections
Epi=Surjections
Co-Retr=Injections
Retr=Surjections
Iso=Bijections
Const="Constant maps"
Co-Const="\(\emptyset \to X\)"
Null="\(\emptyset \to X\)"
Gen="Non-empty sets"
Co-Gen="Sets with at least two elements"
Init="\(\emptyset\)"
Term="\(\{x\\\}\)"
Zero=none
Empty="\(\emptyset\)"
Co-Empty=none
Strong-Init=none
Strong-Term="\(\{x\\\}\)"
Prod="Cartesian product"
Co-Prod="Disjoint union"
Equal="any (common subsets)"
Co-Equal="any (by a minimal equivalence relation compatible with equality of the function values)"
}