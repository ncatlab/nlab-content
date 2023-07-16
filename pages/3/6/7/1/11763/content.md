
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Equality and Equivalence
+-- {: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

The principle of _identity of indiscernibles_ states that two objects are [[identical]] if they have all the same [[properties]].

This is also known as "Leibniz's Law", in honor of [[Gottfried Leibniz]] (not to be confused with his [[product rule]], also so-called).

\begin{imagefromfile}
    "file_name": "LeibnizOnIndiscernibles-Phil7SecXIX.jpg",
    "float": "right",
    "width": 490,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 40
    },
    "caption": "G. W. Leibniz around 1700, from [Gerhard 1890, p. 288](#Gerhard1890)"
\end{imagefromfile}


{#LeibnizWroteTheFollowing} Concretely, Leibniz wrote the following,  (in translation from [Lewis 1918, p. 373](#Lewis18) with original Latin terms in parenthesis; see also [Cartwright 1971, p. 119](#Cartwright71) and [Gries & Schneider 1998](#GriesSchneider98)):


> Two terms are the *same* (*eadem*) if one can be substituted for the other without altering the truth of any statement (*[[salva veritate]]*). If we have $A$ and $B$, and $A$ enters into some true proposition, and the substitution of $B$ for $A$ wherever it appears results in a new proposition that is likewise true, and if this can be done for every proposition, then $A$ and $B$ are said to be the same; ...

This sentence of Leibniz in fact closes with a statement of the converse, often known as the "[[principle of substitutivity]]" but which may deserve to be called the *indiscernibility of identicals*:

> ... conversely, if $P$ and $Q$ are the same, they can be substituted for one another.

The paragraph ends with the assertion that 

> $A$ and $A$ are, of course, said to be the same

This is what [[Grundlage der gesamten Wissenschaftslehre|Fichte 1794]] later called the "first, absolutely unconditioned principle" and [[Science of Logic|Hegel 1812-]] [called](https://ncatlab.org/nlab/show/Science+of+Logic#875) the "[[first law of thought]]". 

From the perspective of [[homotopy type theory]], the "[[first law of thought]]" is the [[term introduction]]-rule for [[identity types]], and "indiscernability of identicals" is the [[transport]]-rule, which together with "identiy of indiscernible" is implied by the [[induction]]-rule of the [[identity type]] (the "[[J-rule]]"). For more on this see [below](#InHomotopyTypeTheory).

In [[set theory]] with [[power sets]], the [[inference rule]] for the identity of indiscernables is given by 

$$\frac{\Gamma \vdash A \; \mathrm{set}}{\Gamma, x \in A, y \in A \vdash \left(\forall P \in \mathcal{P}(A).P(x) \iff P(y)\right) \implies x =_A y \; \mathrm{true}}$$


## In dependent type theory
 {#InHomotopyTypeTheory}

In [[dependent type theory]], a direct translation of Leibniz's identity of indiscernibles requires a way to quantify over all propositions and predicates. The only way this is possible is if the dependent type theory comes with a [[type of all propositions]] and thus [[power sets]], upon which the identity of indiscenibles for type $A$ is given by the dependent function 

$$\mathrm{indOfIDs}:\prod_{x:A} \prod_{y:A} (x =_A y) \simeq \left(\prod_{P:\mathcal{P}(A)} P(x) \simeq P(y)\right)$$

If one is working in a [[type universe]] $U$ in [[dependent type theory]], then one could use the type of $U$-small propositions $\mathrm{Prop}_U \coloneqq \sum_{A:U} \mathrm{isProp}(A)$, upon which the identity of indiscenibles for universe $U$ and type $A$ is given by the dependent function 

$$\mathrm{indOfIDs}_U:\prod_{x:A} \prod_{y:A} (x =_A y) \simeq \left(\prod_{P:A \to \mathrm{Prop}_U} P(x) \simeq P(y)\right)$$

However, this version of the identity of indiscenibles for universe $U$ is weaker than Leibniz's original identity of indiscenibles, since it is possible that not every proposition in the [[dependent type theory]] is $U$-small. 

In [[dependent type theories]] with [[identity types]], identity of indiscernibles holds trivially because of [[haecceity|haecceities]].

In addition, extensionality principles like [[function extensionality]], [[propositional extensionality]], and [[univalence]] ("typal extensionality") are naturally regarded as a stronger form of identity of indiscernibles.
In particular, the [[consistency]] of [[univalence]] means that in [[Martin-Löf type theory]] without univalence, one cannot define any [[predicate]] that provably distinguishes [[equivalence in homotopy type theory|equivalent]] [[types]]; thus equivalent types are "externally indiscernible", and univalence incarnates that principle internally by making them identical.


"There are several ways to think about the axiom of [[univalence]]. One can see it as a sophisticated updating of Leibniz's principle of the identity of indiscernibles." --[[John Baez]] [nCaf&#233;](http://golem.ph.utexas.edu/category/2013/11/categories_for_the_working_phi.html)

On the other hand, the converse substitution/substitutivity principle of "indiscernibility of identicals" is expressd by *[[transport]]* in [[homotopy type theory]].

## In point-set topology
 {#InPointSetTopology}

A [[topology|topological]] or geometrical version of the idea of identity of indiscernibles is [[separation axioms|separation]]: if two points are distinct, then they are separated in some sense. This means in turn that if two points in a space subject to a given separation axiom can not be separated by any admissible separation condition then they are identical.

{#InTopologicalSpacesMoreInDetail} More in detail: 

Given a [[topological space]] one might declare that "topological observations" about the space are questions of the form: "Which points are contained in a given open subset?", and hence that two points are "discernible", namely "topologically distinct", if there exists an [[open subset]] that contains one but not the other. 
With this convention, the condition that "indiscernibles be identical" is equivalently the condition that the topological space
satisfies the $T_0$-[[separation axiom]], hence that it is a [[Kolmogorov space]]. Generally, one could regard the [$T_0$-reflection](Kolmogorov+topological+space#KolmogorovQuotient) as the [[modality]] under which identity becomes indiscernibility, in this sense.

In [[dependent type theory]], given a [[dominance]] $\Sigma \subseteq \Omega$, let $\mathcal{O}(A)$ denote the type of $\Sigma$-[[open sets]] of the type $A$, the type of functions $A \to \Sigma$. The $T_0$-[[separation axiom]] for type $A$ is given by the dependent function

$$T_0:\prod_{x:A} \prod_{y:A} (x =_A y) \simeq \left(\prod_{P:\mathcal{O}(A)} P(x) \simeq P(y)\right)$$

The identity of indiscernibles is simply the $T_0$-separation axiom where the [[type of all propositions]] $\Omega$ is the dominance and where the [[predicates]]/[[subsets]] are the $\Omega$-[[open sets]]. 

## Related entries

* [[first law of thought]]

* [[transport]]

## References

Leibniz's original paragraph (from an unpublished manuscript probably written after 1683) is reproduced in the Latin Original in

* {#Gerhard1890} K. Gerhard (ed.), Section XIX, [p. 228](https://archive.org/details/diephilosophisc00gerhgoog/page/228/mode/2up) in: *Die philosophischen Schriften von Gottfried Wilhelm Leibniz*, Siebenter Band, Weidmannsche Buchhandlung (1890) &lbrack;[archive.org](https://archive.org/details/diephilosophisc00gerhgoog/page/n7/mode/2up)&rbrack;

and in English translation in:

* {#Lewis18} [[Clarence I. Lewis]], Appendix (p. 373) of: *A Survey of Symbolic Logic*, University of California (1918) &lbrack;[[LewisAppendix-LeibnizIndiscernibles.pdf:file]]&rbrack;

and further discussed in:

* {#Cartwright71} [[Richard Cartwright]], *Identity and Substitutivity*, p. 119-133 of: Milton Munitz (ed.) *Identity and Individuation*, New York University Press (1971) &lbrack;[[Cartwright-IdentityAndSubstitutivity.pdf:file]]&rbrack;

* {#GriesSchneider98} David Gries, Fred Schneider, *Formalizations Of Substitution Of Equals For Equals* (1998) &lbrack;[pdf](https://ecommons.cornell.edu/bitstream/handle/1813/7340/98-1686.pdf?sequence=1&isAllowed=y), [ecommons:1813/7340](https://ecommons.cornell.edu/handle/1813/7340)

Leibniz's original terminology "salva veritate" for the substitution principle is prominently used in:

* [[W. V. O. Quine]], §3 of *Two Dogmas of Empiricism* and *Three grades of modal involvement*, as reprinted in: Roger F. Gibson (ed.) *Quintessence -- Basic readings from the philosophy of W. V. Quine*, The Belknap Press of Harvard University Press (2004) &lbrack;[ISBN:9780674027558](https://www.hup.harvard.edu/catalog.php?isbn=9780674027558)&rbrack;


See also:

* Wikipedia, *[Identity of indiscernibles](http://en.wikipedia.org/wiki/Identity_of_indiscernibles)*

* Wikipedia, *[Salva veritate](https://en.wikipedia.org/wiki/Salva_veritate)*

* Standord Encyclopedia of Philosophy, *[The Identity of Indiscernibles](http://plato.stanford.edu/entries/identity-indiscernible/)*

Formalization in [[homotopy type theory]] is in 

* [[Univalent Foundations Project]], section 1.12 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_ (2013)

* {#Favonia17} [[Favonia]], appendix B of _Higher-Dimensional Types in the Mechanization of Homotopy Theory_, PhD thesis 2017, ([pdf](https://www.cs.cmu.edu/~kuenbanh/files/thesis.pdf))

The understanding of "indiscernibility of identicals" as *[[transport]]* in [[homotopy type theory]] is made explicit in:

* {#LadymanPresnell15} [[James Ladyman]], [[Stuart Presnell]], §6.3 of: *Identity in Homotopy Type Theory, Part I: The Justification of Path Induction*, Philosophia Mathematica **23** 3 (2015) 386–406 &lbrack;[doi:10.1093/philmat/nkv014](https://doi.org/10.1093/philmat/nkv014), [pdf](http://philsci-archive.pitt.edu/11079/1/Identity_in_HTT_public.pdf)&rbrack;


* [[Benedikt Ahrens]], [[Paige Randall North]], §3.1 in: *Univalent foundations and the equivalence principle*, in: *Reflections on the Foundations of Mathematics*, Synthese Library **407** Springer (2019)  &lbrack;[arXiv:2202.01892](https://arxiv.org/abs/2202.01892), [doi:10.1007/978-3-030-15655-8](https://doi.org/10.1007/978-3-030-15655-8)&rbrack;

See also:

* [Ladyman & Presnell (2016)](https://academic.oup.com/philmat/article/doi/10.1093/philmat/nkw023/2593919/Identity-in-Homotopy-Type-Theory-Part-II-The) 

[[!redirects identity of indiscernibles]]

[[!redirects Leibniz's Law]]
[[!redirects Leibniz's law]]

[[!redirects salva veritate]]
