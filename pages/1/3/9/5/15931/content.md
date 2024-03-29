
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

In [[constructive mathematics]], _proof relevance_ refers to the concept that mathematical [[proofs]] are mathematical objects themselves and that besides just knowing that a [[proposition]] has _some_ [[proof]] it is relevant to remember the way a given proof is constructed (and to remember possibly different proofs of the same proposition). 

This idea is formalized notably by the idea of [[propositions as types]] in [[type theory]] where a proof is an actual [[term]] (the _proof term_) of some [[type]].

For instance logical [[disjunction]] "A or B" in [[type theory]] (in particular in [[homotopy type theory]]) may be exhibited by the [[sum type]] $A + B$ of the types representing the individual propositions, and a proof/term of $A + B$ carries in it the information of whether it proved $A$ or $B$ to (hence) prove their disjunction.  Similarly, a proof of $C \to (A + B)$ will include the information of which proofs of $C$ lead to proofs of $A$ and which proofs of $C$ lead to proofs of $B$.


## References

### General

* [[UF-IAS-2012|Univalent Foundations Project]], section 1.11 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_


### Prehistory

In 

* [[Georg Hegel]], _[[Phenomenology of Spirit]]_ (1807)

the following complaint about mathematical proof (in section _[12 Historical and mathematical proof](https://www.marxists.org/reference/archive/hegel/works/ph/phprefac.htm#12)_ of the Preface) might be read as being a complaint about the traditional non-[[constructive mathematics|constructive]] concept of proof and about the traditional lack of proof relevance:

> All the same, while proof is essential in the case of mathematical
knowledge, it still does not have the significance and nature of being
a moment in the result itself; the proof is over when we get the
result, and has disappeared. The process of mathematical proof does not belong to the object; it is a function that takes place outside the matter in hand.

> [footnote 42](https://www.marxists.org/reference/archive/hegel/help/finpref.htm#m042): Mathematical truths are not thought to be known unless proved true. Their demonstrations are not, however, kept as parts of what they prove, but are only our subjective means towards knowing the latter. In philosophy, however, consequences always form part of the essence made manifest in them, which returns to itself in such expressions.

See also earlier conceptions of proofs expressing the 'cause' of a theorem, where [[proof by contradiction|proofs by contradiction]] in particular were taken generally to fail. Such an idea goes back to Aristotle for whom a proper answer to the question "Why is the angle in a semicircle a right-angle?" gives its cause.

* Paolo Mancosu, _Philosophy of Mathematics and Mathematical Practice in the Seventeenth Century_, OUP, 1996.


[[!redirects proof relevance]]
[[!redirects proof relevant]]
[[!redirects proof-relevant]]
