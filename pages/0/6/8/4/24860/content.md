
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computation
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

(...)

[[computations]]/[[algorithms]] whose outcome is [indefinite](necessity+and+possibility#RelationToPotentiality).

(...)

## Examples

The [[cut-elimination]] of [[differential linear logic]] is a nondeterministic computation. It takes in entry a proof of type $\Gamma \vdash \Delta$ and returns in output a sum of proofs of type $\Gamma \vdash \Delta$. During the procedure, several proofs can be formed to eliminate cuts from the proof in the previous step, these different possibilities are summed and thus the algorithm returns a [[formal sum]] of proofs. The nondetermism is here realized by the [[addition]] of proofs as formal sums of proofs that can be understood as a [[disjunction]] but in not exactly the same way that the [[linear disjunction]] because it's a disjunction of proofs and not of formulas. An algorithm which returns $\pi_{1} + \pi_{2}$ where $\pi_{1},\pi_{2}$ are two proofs of the same type $\Gamma \vdash \Delta$ returns in fact the disjunction of $\pi_{1}$ and $\pi_{2}$ because it can't chose between the two possibilities. On the level of the syntactic proof theory, one cannot code this sum only by the intermediate of a [[biproduct]] in a [[semiadditive category]], because it would imply that the algorithm would introduce [[cuts]] that will not be eliminated: in a semiadditive category, the sum is defined by combining the structural morphisms of the products and coproducts, which are then equal, through composition, ie. through the [[cut rule]]. One thus works in a [[CMon-enriched symmetric monoidal category]] where we have access to a sum of morphism without necessarily biproducts. In the case where one considers the additive connectors in the logic, the [[additive disjunction]] and the [[additive conjunction]]  are then equated under the presence of formal sums and one can reobtain this formal sum through the biproduct in the semantics. But the semantics is not able to explain the syntactic subtleties related to cut elimination and the difference between a formal sum of two proofs and a sum obtained through cuts and biproducts.

In contradistinction, the cut elimination of [[linear logic]] is a deterministic algorithm and doesn't imply formal sums of proofs. Thus, in linear logic, if one includes the [[additive disjunction]] and the [[additive conjunction]], they are not necessarily equated forming a [[biproduct]] in the syntax, as in differential linear logic.

From ([Ehrhard (2008), Introduction](#Ehrhard08)) : "when one linearizes a proof obtained by contracting two linear inputs of a proof, one has to choose between these two inputs, and there is no canonical way of doing so: we take the non-deterministic superposition of the two possibilities. Syntactically, this means that one must accept the possibility of adding proofs of the same formula, which is standard in mathematics, but hard to accept as a primitive logical operation on proofs".
 
## Related concepts

* [[computation]], [[quantum computation]]

* [[repeat-until-success computing]]

* [[reversible computation]]

* [[parallel computing]]


## References

* Wikipedia, *[Nondeterministic algorithm](https://en.wikipedia.org/wiki/Nondeterministic_algorithm)*

Concerning the example of cut elimination in differential linear logic:

* {#Ehrhard08}[[Thomas Ehrhard]], *An introduction to Differential Linear Logic: proof-nets, models and antiderivatives*, Mathematical Structure in Computer Science **28** 7 (2018) 995-1060 ([arXiv:1606.01642](https://arxiv.org/abs/1606.01642), [doi:10.1017/S0960129516000372](https://doi.org/10.1017/S0960129516000372))

[[!redirects nondeterministic computations]]

[[!redirects nondeterministic algorithm]]
[[!redirects nondeterministic algorithms]]

[[!redirects nondeterministic computing]]


[[!redirects non-deterministic computation]]
[[!redirects non-deterministic computations]]

[[!redirects non-deterministic algorithm]]
[[!redirects non-deterministic algorithms]]



[[!redirects indeterministic computation]]
[[!redirects indeterministic computations]]

[[!redirects indeterministic algorithm]]
[[!redirects indeterministic algorithms]]

[[!redirects indeterministic computing]]

[[!redirects in-deterministic computation]]
[[!redirects in-deterministic computations]]

[[!redirects in-deterministic algorithm]]
[[!redirects in-deterministic algorithms]]








