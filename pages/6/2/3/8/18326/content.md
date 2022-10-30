+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A **Freyd category** is one way to axiomatize models of [[call-by-value]] programming languages.
It abstracts the structure of the [[Kleisli category]] of a [[monad in computer science|monad]], consisting of a category $\mathbb{V}$ that model values and another category with the same objects $\mathbb{C}$ that model computations.

## Definition

A **Freyd category** (following [Levy 04](#Levy04)) may be defined as

* a [[category]] $\mathbb{V}$ with [[finite products]];
* a category $\mathbb{C}$, that has the same objects as $\mathbb{V}$[^sameObjs];
* an [[action]] of $\mathbb{V}$ on $\mathbb{C}$ (with the finite products providing a [[symmetric monoidal category|symmetric monoidal structure]] for $\mathbb{V}$)
* an [[identity-on-objects functor]] $\mathbb{V} \to \mathbb{C}$ that preserves the actions.

[^sameObjs]: Having the same objects is required or implied by having an identity-on-objects functor from $\mathbb{V}$ to $\mathbb{C}$.

An alternative but equivalent definition is as follows (following [Power, Thielecke](#PH99)):

A Freyd category is given by 

* a category $\mathbb{V}$ with finite products;
* a symmetric [[premonoidal category]] $\mathbb{C}$, that has the same objects as $\mathbb{V}$;
* an identity-on-objects functor $\mathbb{V} \to \mathbb{C}$ preserving strict symmetric premonoidal structure, whose image lies in the centre of $\mathbb{C}$. 

## Properties

### Relation to strong monads. 

If $T$ is a [[strong monad]] on a category $\mathbb{V}$ with finite products, then the Kleisli category of $T$ forms a Freyd category and $J$ has a right adjoint. 

Conversely, if $(\mathbb{V},\mathbb{C},J)$ is a Freyd category and $J$ has a right adjoint $R$, then the Freyd category arises as the Kleisli category of the monad $RJ$.

### Relation to Lawvere theories

[Staton 14](#Staton14) shows that a small Freyd category is equivalent to an [[enriched Lawvere theory]] relative to the empty [[sound doctrine]] where the enriching category is [[cartesian closed category|cartesian closed]].

## Related Concepts

* [[monad in computer science]]
* [[Kleisli category]]
* [[thunk-force category]]

## References

The above definition is due to

* {#Levy04} Paul Blain Levy, "Call-by-Push-Value. A Functional/Imperative Synthesis," Semantic Structures in Computation 2, Springer, 2004; appendix B* 

as paraphrased by 

* {#Staton14} _Staton, S., 2014. Freyd categories are Enriched Lawvere Theories. Electronic Notes in Theoretical Computer Science, Proceedings of the Workshop on Algebra, Coalgebra and Topology (WACT 2013) 303, 197&#8211;206. [doi:10.1016/j.entcs.2014.02.010](https://doi.org/10.1016/j.entcs.2014.02.010) (free)_. 

Freyd categories were first used in

* John Power and Hayo Thielecke "Environments, Continuation Semantics and&#160;Indexed Categories",  Theoretical Aspects of Computer Software, Third International Symposium, TACS '97

and named Freyd categories in

* {#PH99} John Power and Hayo Thielecke, "Closed Freyd- and $\kappa$-Categories", Automata, Languages and Programming, 26th International Colloquium, ICALP'99

and the longer journal version of that paper has more discussion:

* Paul Blain Levy, John Power and Hayo Thielecke, "Modelling environments in call-by-value programming languages",  Inf. Comput. 185(2): 182-210, 2003 [preprint pdf](https://www.cs.bham.ac.uk/~hxt/research/envcbv.pdf).


[[!redirects Freyd categories]]


