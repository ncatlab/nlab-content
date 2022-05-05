## Idea 

*Scott's trick* (due to [[Dana Scott]]) is a technical device in a [[material set theory]] such as ZF, that is used to construe a [[quotient]] of a [[proper class]] as another class. 

## Discussion 

We work throughout with the theory [[ZF]], leaving it to the reader to consider how the discussion applies to other material set theories of comparable strength. 

A "class" is not a formal object of ZF, but a meta-object defined by a formula of ZF such as $x \notin x$. (Formally, then, a class is a formula considered up to logical equivalence.) To some extent such meta-objects can be handled like "sets" (the formal objects), so long as constructions remain safely within the confines of first-order, not higher-order logic. For example, there are various ZF hacks for defining the product of two classes as a class, the sum of two classes as a class, etc., but there is no way of forming exponentials of classes, or the power object of a class. In technical terms, the meta-category of classes and class functions may be regarded as a [[pretopos]], but not a [[topos]]. 

A critical case here is forming the quotient of a class by an equivalence relation. In the usual development of axiomatic set theory, the quotient of a set $X$ by an equivalence relation $\sim$ on $X$ is located within the power set $P X$: each $\sim$-equivalence class is an element of $P X$, and the set of equivalence classes is thus rendered as a definable subset of $P X$. This naive approach to defining quotients is not available for classes $C$, since in the first place we do not have a power class $P C$ to work with. 

As a workaround, Dana Scott introduced the following trick. In ZF set theory, we define the ordinal [[rank]] of a set by transfinite induction ([[recursion]]), giving a class function $V \to Ord$. This uses the axioms of [[axiom of foundation|foundation]] and of [[replacement axiom|replacement]]. The collection of sets of ordinal rank $\alpha$ or below is itself a set $V_\alpha$; this is the underpinning of the [[cumulative hierarchy]] picture of set theory. 

Thus, given an equivalence relation $\sim \subseteq C \times C$ on a class $C$, we may consider in each equivalence class just those sets whose rank is the minimum $\alpha$ within that class. The collection of those sets is again a set, a subset $c$ of $V_\alpha$, by the [[axiom of separation]]. We let those sets $c$ proxy as equivalence classes; those sets form a class, and this class is the desired quotient $Q$. Indeed, there is a quotient map $C \to Q$, taking $x \in C$ to the set of smallest-rank sets $\sim$-equivalent to $x$, and one may argue that this quotient map has the requisite universal property.


## Applications 

There are many applications of Scott's trick. See for instance 

* [[localization]] 

where the general construction for a large category involves passage to a quotient, and also 

* [[ultraproduct]] 

where standard discussions of ultrapowers of class-sized models take this technical trick into account. 

## References 

The eponymous trick was introduced in a conference: 

* [[Dana  Scott]], *Definitions by abstraction in axiomatic set theory*,  Meeting of the American Mathematical Society, University of British Columbia,  Vancouver, Canada (June 1955). ([web](http://www.ams.org/journals/bull/1955-61-05/S0002-9904-1955-09941-5/S0002-9904-1955-09941-5.pdf)) 

Scott's immediate application was to give a viable notion of cardinal number, not as a von Neumann ordinal which requires the [[well-ordering principle]], but via a proxy of the equivalence class for the equivalence relation "is in bijection with", as explained above. 

A brief textbook account (not mentioning Scott's name) is in 

* [[Thomas Jech]], *Set Theory*, 3rd millennium (revised) ed., Springer Monographs in Mathematics, Springer (2003). 

See particularly page 65. 

