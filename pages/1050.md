#Idea#

A functor is left _exact_ or [[flat functor|flat]] if it preserves finite [[limit]]s.

#Definition#

* A [[functor]] $F : C \to D$ is **right exact** if for all [[object]]s $d \in D$ the [[comma category]] $F/d$ is [[filtered category|filtered]].

* A [[functor]] $F : C \to D$ is **left exact** if for all [[object]]s $d \in D$ the [[opposite category|opposite]] [[comma category]] $(d/F)^{op}$ is [[filtered category|filtered]].

* A [[functor]] is **exact** if it is both left and right exact.

+-- {: .un_prop}
###### Proposition

* A left exact functor preserves every finite [[limit]] that exists in $C$.

* If $C$ admits all finite [[limit]]s then a functor is left exact precisely if it preserves these limits.  
=--



#Remark on terminology#

Frequently the term "left exact" is restricted to the case that $C$ has all finite [[limit]]. If so,  then the general case is called a [[flat functor]]. 

+-- {: .query}
Conceivably, it might be used also in the more general case, but to refer to a weaker notion: a functor that preserves those finite limits that exist.  Certainly that\'s how I would interpret 'finitely continuous functor'.  ---Toby
=--

Left exactness is sometimes abbreviated **lex**.  In particular, $Lex$ is the 2-category of categories with finite limits and lex functors.  See also [[continuous functor]].

#References#

for instance section 3.3 of

* Kashiwara, Schapira, [[Categories and Sheaves]]
