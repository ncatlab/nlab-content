
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

_L&#246;b's theorem_ in its original form is a generalization of the [[Gödel incompleteness theorem]] whose formulation lends itself to the tools of [[type theory]] and [[modal logic]].

L&#246;b's theorem states that to prove that a [[proposition]] is [[provability logic|provable]], it is sufficient to prove the proposition under the assumption that it  is  provable.  Since the  [[Curry-Howard isomorphism]] identifies [[formal proofs]] with abstract [[syntax]] trees of [[programs]]; L&#246;b's theorem implies, for total [[languages]] which validate it, that self-interpreters are impossible. ([Gross-Gallagher-Fallenstein 16](#GrossGallagherFallenstein16))

In [[provability logic]] the abstract statement is considered in itself as an [[axiom]] on a [[modal operator]] $\Box$ interpreted as the [[modality]] "is provable". In this form the statement reads formally:

$$
  \Box(\Box P \to P) \to \Box P
$$ 

for any [[proposition]] $P$ ("L&#246;b's axiom").

This reduces to an [[incompleteness theorem]] when taking $P = $ [[false]] and using that 

1. [[negation]] is $\not P = (P \to false)$;

1. [[consistency]] means that $\Box P \to \not \Box \not P$


$$
  \begin{aligned}
    & \Box (\Box false \to false) \to \Box false
    \\
    \Rightarrow \;\; & \Box ( \not \Box false ) \to \Box false
    \\
    \Rightarrow \;\;
    & \Box ( \not \Box false ) \to \not \Box \not false
    \\ 
    \Rightarrow \;\;
    & \Box ( \not \Box false ) \to false
    \\
    \Rightarrow \;\;
    & \not \Box \not \Box false
  \end{aligned}
$$

Where the last line reads in words "It is not provable that false is not provable." 

## Guarded Recursion Variant

A variant of the Löb axiom is used in [[guarded recursion]] and [[synthetic guarded domain theory]], which uses a modality $\blacktriangleright$, usually pronounced "later". Then the Löb induction axiom is for any proposition $P$,

$$(\blacktriangleright P \to P) \to P$$

In a setting with the principle of [[unique choice]], this can be used to prove the existence of all guarded [[fixed points]].

Note that the assumptions about the later modality $\blacktriangleright$ are usually quite different from the provability modality $\Box$. For instance, $\Box$ is usually assumed to have some subset of the properties of a [[comonadic]] [[modality]], but $\blacktriangleright$ typically satisfies $P \to \blacktriangleright P$.


## Related concepts

* [[fixed-point combinator]] 

* [[Lawvere's fixed point theorem]]

* [[guarded recursion]]

* [[synthetic guarded domain theory]]

* [[introspective theory]]



## References

* {#GrossGallagherFallenstein16} [[Jason Gross]], Jack Gallagher, Benya Fallenstein, _L&#246;b's theorem -- A functional pearl of dependently typed quining_, 2016 ([pdf](https://jasongross.github.io/lob-paper/nightly/lob.pdf))

* [[Neelakantan Krishnaswami]], _[L&#246;b's theorem is (almost) the Y-combinator](http://semantic-domain.blogspot.de/2016/05/lobs-theorem-is-almost-y-combinator.html)_, 2016

* [[Jason Gross]], [MO comment](https://mathoverflow.net/a/273951/381) on incompletenss theorems in type theory, 2017

See also 

* Wikipedia, _[L&#246;b's theorem](https://en.wikipedia.org/wiki/L%C3%B6b%27s_theorem)_

Unified account of [[Löb's theorem]]/[[Gödel's second incompleteness theorem]], [[Kripke semantics]] for [[provability logic]], and [[guarded recursion]], via [[essentially algebraic theories]] which "self-internalize":

* [[Sridhar Ramesh]], *Introspective Theories and Geminal Categories*, PhD thesis, Berkeley (2023) &lbrack;[escholarship:3mn0c475](https://escholarship.org/uc/item/3mn0c475), [[Ramesh-IntrospectiveTheories.pdf:file]]&rbrack;



[[!redirects Löb theorem]]

[[!redirects Loeb's theorem]]
[[!redirects Loeb theorem]]

[[!redirects Löb's axiom]]
[[!redirects Löb's axioms]]

[[!redirects Loeb's axiom]]
[[!redirects Loeb's axioms]]

[[!redirects Löb axiom]]
[[!redirects Löb axioms]]

[[!redirects Loeb axiom]]
[[!redirects Loeb axioms]]


[[!redirects Löb induction]]
[[!redirects Löb induction]]
[[!redirects Loeb induction]]
[[!redirects Loeb induction]]
