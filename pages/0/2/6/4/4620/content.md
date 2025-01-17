
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Principles of omniscience
* table of contents
{: toc}

## Idea

In [[logic and foundations]], a __principle of omniscience__ is any principle of [[classical mathematics]] that is not valid in [[constructive mathematics]].  The idea behind the name (which is due to [Bishop (1967)](#Bishop67)) is that, if we attempt to extend the [[computation|computational]] interpretation of constructive mathematics to incorporate one of these principles, we would have to know something that we cannot compute. The main example is the law of [[excluded middle]] ($EM$); to apply $p \vee \neg{p}$ computationally, we must know which of these [[disjunction|disjuncts]] hold; to apply this in all situations, we would have to know everything (hence 'omniscience').

Bishop\'s principles of omniscience may be seen as principles that extend classical logic from [[predicates]] (where $EM$ may happen to be valid, even constructively, for certain predicates) to their [[quantifications]] over infinite domains (where $EM$ is typically not constructively valid).

## Examples

Examples of principles of omniscience include 

* [[limited principle of omniscience]], a weak form of [[excluded middle]] applied to the [[existential quantifier]] for a [[decidable]] [[predicate]] on a given [[domain of discourse]]. 

* [[weak limited principle of omniscience]], a weak form of [[weak excluded middle]] applied to the [[existential quantifier]] for a [[decidable]] [[predicate]] on a given [[domain of discourse]]. 

* [[lesser limited principle of omniscience]], a weak form of [[de Morgan's law]] applied to the [[existential quantifier]] for a [[decidable]] [[predicate]] on a given [[domain of discourse]]. 

* [[Markov's principle]], a weak form of the [[double negation law]] applied to the [[existential quantifier]] for a [[decidable]] [[predicate]] on a given [[domain of discourse]]. 

Bishop's principles of omniscience take the [[domain of discourse]] to be the [[natural numbers]]. However, it is possible to use some other domain of discourse to get a different principle of omniscience. 

There are also the [[analytic principles of omniscience]], which are versions of Bishop's principles of omniscience that are used in [[real analysis]], including

* [[analytic LPO]]

* [[analytic WLPO]]

* [[analytic LLPO]]

* [[analytic Markov's principle]]

In addition, in [King 2024](#King24) there are more generalizations of the principles of omniscience listed above, which are equivalent to Bishop's principles of omniscience under the [[weak countable choice]] principle $\mathrm{AC}_{\mathbb{N}, 2}$. 

There are also generalisations of the [[principles of omniscience]] involving sets with tight apartness:

* Every set with tight apartness has [[decidable tight apartness]], which generalises [[LPO]] and [[analytic LPO]]

* Every set with tight apartness has [[decidable equality]], which generalises [[WLPO]] and [[analytic WLPO]]

* Every set with tight apartness has [[stable relation|stable]] [[tight apartness]], which generalises [[Markov's principle]] and [[analytic Markov's principle]]

The first one is equivalent to the [[category of sets]] being a [[boolean category]], since given a [[subsingleton]] $S$, that the function set $S \to \mathbb{2}$ from $S$ to the [[boolean domain]] $\mathbb{2}$ has decidable tight apartness is equivalent to $S$ being either a [[singleton]] or an [[empty set]], which is precisely the condition that [[Set]] is a boolean category. 

The latter two are all still weaker than [[Set]] being a [[boolean category]] since in general, the [[set of truth values]] is only an set with tight apartness if and only if [[excluded middle]] holds. 

## References

* {#Bishop67} [[Errett Bishop]]: _[[Foundations of Constructive Analysis]]_, McGraw-Hill (1967)
 
  > (in the introduction or chapter 1, I forget)

* {#Richman90} [[Fred Richman]], *Polynomials and linear transformations*. Linear Algebra and its Applications, Volume 131, 1 April 1990, Pages 131-137. &lbrack;<a href="https://doi.org/10.1016/0024-3795(90)90379-Q">doi:10.1016/0024-3795(90)90379-Q</a>&rbrack;

* {#King24} Christopher King, *What are these generalizations of the principles of omniscience called?*, MathOverflow, 15 February 2024. ([web](https://mathoverflow.net/questions/464247/what-are-these-generalizations-of-the-principles-of-omniscience-called))

[[!redirects principle of omniscience]]
[[!redirects principles of omniscience]]

[[!redirects omniscience principle]]
[[!redirects omniscience principles]]

category: disambiguation
