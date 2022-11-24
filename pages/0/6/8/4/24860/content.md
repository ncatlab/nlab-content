
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

The [[cut-elimination]] of [[differential linear logic]] is a nondeterministic computation. It takes in entry a proof of type $\Gamma \vdash \Delta$ and returns in output a sum of proofs of type $\Gamma \vdash \Delta$. During the procedure, several proofs can be formed to eliminate cuts from the proof in the previous step, these different possibilities are summed and thus the algorithm returns a sum. The nondetermism is here realized by the [[addition]] that can be understood as a [[disjunction]]. An algorithm which returns $A + B$ return in fact the disjunction of $A$ and $B$ because it can't chose between the two possibilities. In contradistinction, the cut elimination of [[linear logic]] is a deterministic algorithm.

From ([Ehrhard (2008), Introduction](#Ehrhard08)) : "when one linearizes a proof obtained by contracting two linear inputs of a proof, one has to choose between these two inputs, and there is no canonical way of doing so: we take the non-deterministic superposition of the two possibilities. Syntactically, this means that one must accept the possibility of adding proofs of the same formula, which is standard in mathematics, but hard to accept as a primitive logical operation on proofs".
 
## Related concepts

* [[computation]], [[quantum computation]]

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








