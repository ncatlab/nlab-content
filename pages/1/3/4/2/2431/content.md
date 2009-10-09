
#Idea#

The classical Brown representability theorem says that certain functors on [[Top]]${}^{op}$ that look like assigning [[cohomology group]]s to [[topological space]]s -- in that they satisfy the [[Eilenberg-Steenrod axioms]] -- are [[representable functor|representable]] in that they may be realized by the assignments of homotopy classes of maps into a [[spectrum]].

For more background on this classical theorem see [[generalized (Eilenberg-Steenrod) cohomology]]

There are various generalizations of this result from the [[Top]] to more general [[model category|model categories]] and [[triangulated category|triangulated categories]]

The [[Eilenberg-Steenrod axioms]] were written down in an effort to axiomatize the notion of [[cohomology]] on [[topological space]]s by extrapolating crucial properties of ordinary [[integral cohomology]].
The classical Brown representability theorem and its generalizations show that these complicated axioms have a very simple repackaging. The theorem is one of the crucial ingredients that motivate the _definition_ of cohomology in terms of maps into certain coefficient objects. This general notion of cohomology is described at [[cohomology]].

#Classical Brown representability#

Axiom of sum: For any family $\{X_\alpha\}_{\alpha\in A}$ of pointed CW-complexes the morphism $(i_\beta)_*:F(\vee_\alpha X_\alpha)\to \prod_\alpha F(X_\alpha)$ induced by the inclusion $i_\beta:X_\beta\to \vee_\alpha X_\alpha$ is a bijection.

Mayer-Vietoris axiom: For every triad $(X; A_1, A_2)$ of CW-spaces (with $A_1\cup A_2 = X$) and any elements $x_1\in F(A_1)$, $x_2\in F(A_2)$, such that $x_1|A_1\cap A_2 = x_2|A_1\cap A_2$ there is $y\in F(X)$ such that $y|A_1 = x_1$ and $y|A_2 = x_2$. 

Brown representability theorem: A contravariant functor $F:CW^{op}_*\to Set_*$ from pointed CW-complexes to pointed sets which satisfies the axiom of sum and axiom of Mayer-Vietoris is representable. In other words, there is a pointed CW-complex $(Y,y_0)$ and a universal element $u\in F(Y,y_0)$ such that $T_u:[-;Y,y_0]\to F$ is a natural equivalence. 

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