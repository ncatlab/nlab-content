
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
 {#Idea}

Broadly speaking *nondeterministic* [[computations]]/[[algorithms]] are those whose outcome is [indefinite](necessity+and+possibility#RelationToPotentiality), or else dependent on parameters that are not known or specified when the computation/algorithm is laid out (they may become known at "runtime").

Beware that in [[complexity theory]], at least, by a "non-determinstic algorithm" one really refers instead (or more specifically) to the *shortest path* that a non-deterministic machine *could* potentially take to arrive at a desired result (cf. the [NIST entry](#NIST)). This is the sense in which "non-determinism" appears for instance in the name of the [[complexity class]] "[[NP]]" .

(...)

## Formalizations

### Via indefiniteness-effects
 {#FormalizationViaIndefinitenessEffects}

A basic [[programming language]]-model of non-determinism is via dependence of a [[program]] on an unspecified parameter $b \colon B$, whose value is indefinite but imagined to become known at execution time -- say via user input, or by [[observation|observing]] the actual value of a [[random variable]] in an [[experiment]] and/or by making a [[measurement]] of a [[stochastic process]] or a [[quantum measurement]] of a [[quantum state]] (see [below](#ExamplesQuantumComputation)). 

In this model, a non-deterministic program taking input [[data]] of [[data type]] $D$ and producing output data of *nominal* type $D'$ would be an actual (determinstic) program of the form

$$  
  prog \;\colon\; D \longrightarrow \big( B \to D' \big)
  \,,
$$

whose *de facto* output [[data type]] is not $D'$ but the [[function type]] $B \to D'$. This means that the $D'$-result of computing $prog(d)$ for any $d \colon D$ remains "un-determined" or "indefinite" unless and until a parameter $b \colon B$ is somehow chosen (say "randomly", "experimentally" or in whichever way), in which case only we obtain definite data $prog(d)(b) \;\colon\; D'$.

It makes sense to say that the data type 

$$
  \bigcirc_B D' \;\coloneqq\; \big( B \to D'\big)
$$

exhibits a "$B$-indefinitess effect" that goes along with the execution of the program, making its output indefinite. Such *side effects* in computing may be modeled by [[monads in computer science]] (see [there](monad+in+computer+science#BasicIdea) for more). Indeed $\bigcirc_B$ is a classical example of such a monad, often called the *$B$-[[reader monad]]*, reflecting the idea that it postpones returning definite output data until it has "read in" an otherwise unspecified parameter.

> Incidentally, in terms of [[modal logic]] the parameter type $B$ plays the role of the set of "[[possible worlds]]" in which the given non-deterministic computation may take definite values. For more on this modal logic perspective see at *[[necessity and possibility]]* the section *[relation to potentiality](necessity+and+possibility#RelationToPotentiality)*.

Now the [[monad]]-[[structure]] on $\bigcirc_B$ allows to *carry along* this *indefiniteness effect* so that followup programs, nominally waiting for input data in $D'$, are consistently treated as non-deterministic, dependent on specification of $b \colon B$, too.

Concretely, if 

$$
  prog \;\colon\; D \to \bigcirc_B D'
$$

and

$$
  prog' \;\colon\; D' \to \bigcirc_B D''
$$

are two such non-deterministic programs but conditioned on the *same* global random variable $b \colon B$, then their consistent [[composition]], as such, is their [[Kleisli composition]] (which involves the categorical [[multiplication]]-operation in the [[reader monad]], see there for details):

$$
  prog 
    \;\;\text{>>=}\;\;
  prog'
  \;\;\;\;
  \equiv
  \;\;\;\;
  bind^{\bigcirc_B} prog' \;\circ\; prog
  \;\colon\;
  D \to \bigcirc_B D''
  \,.
$$

Of course, in general the non-determinism of a program need not be parameterized over a fixed parameter type $B$. If the sequence $(B_i)_{i \colon I}$ of parameters is known beforehand, one can form their [[product type]] $B \equiv \prod_i B_i$ and proceed as above, but in general even that sequence may not be pre-specified and further effect handling besides a fixed [[reader monad]] needs to be considered (...).


## Examples

### Quantum computation
 {#ExamplesQuantumComputation}

A fundamental example of non-deterministic computation is [[quantum computation]], where the process of [[quantum measurement]] produces outcomes that -- to the best knowledge of the current state of [[fundamental physics]] -- are fundamentally non-deterministic in that there is not even in principle a way to predict a given outcome with certainty (only their [[probability distribution]] is fixed by [[quantum theory]]).

The possible results of a [[quantum measurement]] are indexed by a "measurement basis" which is exactly a ([[finite set|finite]]) [[set]] $B$ serving as the parameter type in the [[modal logic]]-discussion [above](#FormalizationViaIndefinitenessEffects). 
The only difference for quantum computation is that quantum data types are [[linear types]], so that the relevant [[reader monad]] here is a linear version of the classical reader monad -- see at *[[quantum reader monad]]* for details.

A formulation of (non-deterministic) [[quantum computation]] in terms of the resulting $\bigcirc_B$-[[modal type theory|modal]] [[linear type theory]] is discussed at *[[quantum circuits via dependent linear types]]*.

But in fact the [[quantum reader monad]] is (for [[finite set|finite]] $B$) a [[Frobenius monad]] and as such [[isomorphism|isomorphic]] (see [here](quantum+reader+monad#QuantumReaderMonadIsSpecialFrobeniusWriterMonad)) to the "classical structures" Frobenius monad has long been proposed to model [[quantum measurement]] in [[quantum information theory via dagger-compact categories]] ([Coecke & Pavlović (2008)](quantum+information+theory+via+dagger-compact+categories#CoeckePavlović08))



### Differential linear logic
 {#ExamplesDifferentialLinearLogic}


Something reminiscent of --  but different from -- non-deterministic computation appears (see the quotes [below](#QuotesForDifferentialLinearLogic)) in [[differential linear logic]], where the [[cut-elimination]] procedure has been argued to "intuitively correspond" to non-determinism:

The differential linear cut rule receives as input a [[proof]] of type $\Gamma \vdash \Delta$ and returns as output a [[formal sum]] of proofs of type $\Gamma \vdash \Delta$. During the procedure, several proofs can be formed to eliminate cuts from the proof in the previous step, these different possibilities are summed and thus the algorithm returns a [[formal sum]] of proofs. The nondetermism is here realized by the [[addition]] of proofs as formal sums of proofs that can be understood as a [[disjunction]] but in not exactly the same way that the [[linear disjunction]] because it's a disjunction of proofs and not of formulas. An algorithm which returns $\pi_{1} + \pi_{2}$ where $\pi_{1},\pi_{2}$ are two proofs of the same type $\Gamma \vdash \Delta$ returns in fact the disjunction of $\pi_{1}$ and $\pi_{2}$ because it can't chose between the two possibilities. On the level of the syntactic proof theory, one cannot code this sum only by the intermediate of a [[biproduct]] in a [[semiadditive category]], because it would imply that the algorithm would introduce [[cuts]] that will not be eliminated: in a semiadditive category, the sum is defined by combining the structural morphisms of the products and coproducts, which are then equal, through composition, ie. through the [[cut rule]]. One thus works in a [[CMon-enriched symmetric monoidal category]] where we have access to a sum of morphism without necessarily biproducts. In the case where one considers the additive connectors in the logic, the [[additive disjunction]] and the [[additive conjunction]]  are then equated under the presence of formal sums and one can reobtain this formal sum through the biproduct in the semantics. But the semantics is not able to explain the syntactic subtleties related to cut elimination and the difference between a formal sum of two proofs and a sum obtained through cuts and biproducts.

In contradistinction, the cut elimination of [[linear logic]] is a deterministic algorithm and doesn't imply formal sums of proofs. Thus, in linear logic, if one includes the [[additive disjunction]] and the [[additive conjunction]], they are not necessarily equated forming a [[biproduct]] in the syntax, as in differential linear logic.

{#QuotesForDifferentialLinearLogic} From [Ehrhard (2008), Introduction](#Ehrhard08): 

> "when one linearizes a proof obtained by contracting two linear inputs of a proof, one has to choose between these two inputs, and there is no canonical way of doing so: we take the non-deterministic superposition of the two possibilities. Syntactically, this means that one must accept the possibility of adding proofs of the same formula, which is standard in mathematics, but hard to accept as a primitive logical operation on proofs."

However, [Erhardt & Regnier (2009), p. 3](differential+linear+logic#EhrhardtRegnier09) admit that:

> "Notice that in our axiomatization of sums in the differential lambda-calculus, the non-deterministic reduction rule $s + s' \to s$ will not be valid, but sums will nevertheless intuitively correspond to a version of non-deterministic choice where all the actual choice operations are postponed: the result of a term reduction will in general be a large formal sum of terms, and we can reduce the really "non-deterministic" part of the computation to a unique ultimate step consisting in choosing one term of that sum. This step is however a fiction and will not appear as a reduction rule of our calculus"

 


## Related concepts

* [[computation]], [[quantum computation]]

* [[non-deterministic automaton]]

* [[repeat-until-success computing]]

* [[reversible computation]]

* [[parallel computing]]


## References

* {#Sipser2012} [[Michael Sipser]], §1.2 in: *Introduction to the Theory Of Computation*, 3rd ed: Cengage Learning (2012) &lbrack;ISBN:978-1-133-18779-0,[pdf](https://www.mog.dog/files/SP2019/Sipser_Introduction.to.the.Theory.of.Computation.3E.pdf), [pdf](https://fuuu.be/polytech/INFOF408/Introduction-To-The-Theory-Of-Computation-Michael-Sipser.pdf)&rbrack;

See also:

* Wikipedia, *[Nondeterministic algorithm](https://en.wikipedia.org/wiki/Nondeterministic_algorithm)*

Nondeterministic Turing machines:

* [Sipser (2012), §3.2](#Sipser2012)

* Wikipedia, *[Nondeterministic Turing machine](https://en.wikipedia.org/wiki/Nondeterministic_Turing_machine)*


The notion in [[complexity theory]]:

* {#NIST} NIST, *[nondeterministic algorithm](https://xlinux.nist.gov/dads/HTML/nondetermAlgo.html)*

The above treatment of non-deterministic [[quantum computation]] via the [[quantum reader monad]] is made explicit in

* {#CQTS22} [[CQTS]], *[Quantum Data Types via Linear HoTT](https://ncatlab.org/schreiber/show/QDataInLHoTT#QTML2022)*, talk at *[Workshop on Quantum Software](https://quasar.unina.it/qtml2022/workshop.php)* @ *[QTML 2022](https://quasar.unina.it/qtml2022.html)* (Nov 2022) &lbrack;[pdf](/schreiber/files/QuantumDataInLHoTT-221117.pdf)&rbrack;


Concerning the quasi-example of cut elimination in differential linear logic:

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








