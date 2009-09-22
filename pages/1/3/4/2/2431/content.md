
#Idea#

The classical Brown representability theorem says that certain functors on [[Top]]${}^{op}$ that look like assigning [[cohomology group]]s to [[topological space]]s -- in that they satisfy the [[Eilenberg-Steenrod axioms]] -- are [[representable functor|representable]] in that they may be realized by the assignments of homotopy classes of maps into a [[spectrum]].

For more background on this classical theorem see [[generalized (Eilenberg-Steenrod) cohomology]]

There are various generalizations of this result from the [[Top]] to more general [[model category|model categories]] and [[triangulated category|triangulated categories]]

The [[Eilenberg-Steenrod axioms]] were written down in an effort to axiomatize the notion of [[cohomology]] on [[topological space]]s by extrapolating crucial properties of ordinary [[integral cohomology]].
The classical Brown representability theorem and its generalizations show that these complicated axioms have a very simple repackaging. The theorem is one of the crucial ingredients that motivate the _definition_ of cohomology in terms of maps into certain coefficient objects. This general notion of cohomology is described at [[cohomology]].

#Details#

## version for ordinary (model) categories ##

+-- {: .un_theorem}
###### Theorem (Jardine)

Let $C$ be a [[simplicial model category]] such that

1. it has a [[zero object]] ${*}$;

1. there is a set $S$ of cofibrant [[compact object]] such that the weak equivalences in $C$ are precisely the $S$-[[local equivalence]]s.

Let $F : C^{op} \to Set_{*}$ be a [[functor]] to the category of pointed sets on $C^{op}$ such that 

1. $F$ is a [[homotopical functor]]

1. $F({*}) = {*}$

1. $F$ preserves small [[coproduct]]s of cofibrant objects in that the induced maps

   $$
     F(\coprod_i X_i) \to \prod_i(F(X_i))
   $$

   are bijections

1. **(Mayer-Vietoris property)**  For every [[pushout]] diagrams

   $$
     \array{
       A &\to& X
       \\
       \downarrow^i && \downarrow 
       \\
       B &\to& B \coprod_A X
     }
   $$  

   with all objects cofibrant and $i$ a cofibration the induced [[function]]

   $$
     F(B \coprod_A X) \to F(B) \times_{F(A)} F(X)
   $$
 
   is a [[surjection]].

Then $F$ is [[representable functor|representable]].

=--

+-- {: .un_remark }
###### Remarks

Notice that

* the existence of the 0-object is the generalized analogue of working with [[pointed object|pointed]] [[topological space]]s;

* the condition that the value of $F$ on the point ${*}$ is trivial means that this is about [[reduced cohomology theory]];

* that every representable functor has the given properties is immediate. The nontrivial statement is that these properties already characterize representable functors.

=--


## version for simplicially enriched (model) categories##



#References#

The generalizaton of the Brown representability theorem from [[topological space]]s to [[∞-stack]]s -- or rather to the standard  [[models for ∞-stack (∞,1)-toposes]] in terms of the standard [[model structure on simplicial presheaves]] -- is given in

* Jardine, _[[JardineBrownrep.pdf:file]]_ 

warning: this is probably implicialy about [[reduced cohomology theory]], as the functors considered always assign the trivial result to the [[terminal object]] (the [[point]] in the usual examples).

[[!redirects Brown representability]]