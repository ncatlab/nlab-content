# Hilbert systems

* table of contents
{: toc}

## Idea

A **Hilbert system** is a kind of [[deductive system]] characterized by the presence of many [[axioms]] and few [[rule of inference|rules]].  Usually the only [[judgment]] form is "$A \; true$" for some proposition $A$, which is usually written simply as "$A$".  Thus, a Hilbert-style deduction is a [[tree]] whose edges are formulas, whose leaves are axioms, and whose nodes are one of a very small number of rules.  The most common rule is [[modus ponens]]:

$$ \array{\arrayopts{\rowlines{solid}} A \qquad A\to B \\ B } $$

and in many Hilbert systems this is the only rule, although sometimes one finds others in use.  Then each [[logical connective]] is described by imposing [[axioms]].

## The role of implication

In many cases, the necessary axioms are obtained fairly straightforwardly from the corresponding rules by replacing derivability and entailment by the [[implication]] connective.  For instance, the rules for [[disjunction]] are
$$ \frac{\Gamma\vdash A}{\Gamma\vdash A\vee B}\qquad
\frac{\Gamma\vdash B}{\Gamma\vdash A\vee B} \qquad
\frac{\Gamma\vdash A\vee B \quad \Gamma,A\vdash C \quad \Gamma,B\vdash C}{\Gamma\vdash C}$$
and the corresponding Hilbert-style axioms are
$$ A\to (A\vee B) \qquad B\to (A\vee B) \qquad (A\vee B) \to (A\to C) \to (B\to C) \to C.$$

Of course, this gives a special role to [[implication]].  Its axioms are

$$ \array{ P \to P \\
  P \to (Q\to P) \\
  (P \to (Q\to R)) \to ((P \to Q) \to (P \to R)).
  }
$$

Note that these are precisely the types of the basic [[combinators]] in [[combinatory logic]].  In fact, under the [[propositions as types]] correspondence, Hilbert systems correspond to combinatory logic in the same way that [[natural deduction]]/[[sequent calculus]] corresponds to [[lambda-calculus]].

## On notation

In a Hilbert system one often writes rules and deductions using a turnstile $\vdash$ instead of a horizontal bar.  Thus, modus ponens would be written

$$ A, A\to B \vdash B$$

This can be somewhat confusing when comparing a Hilbert system to other systems such as [[sequent calculus]] or [[type theory]] in which $\vdash$ appears as part of *each judgment* to specify the context of that judgment.  Often the two meanings of $\vdash$ can be conflated, but not always.  For instance, in [[substructural logic]] such as [[linear logic]] or [[relevance logic]], we may have a rule (not an axiom) such as

$$ \array{\arrayopts{\rowlines{solid}} A \qquad B \\ A\& B } $$

(where $\&$ represents the [[additive conjunction]]), which in a Hilbert system would be written as $A,B\vdash A\& B$.  But the *sequent* $A,B\vdash A\& B$ is not valid in the usual sequent-calculus presentations of such logics, because the comma in the sequent context (on the left) is usually a judgment-level version of the [[multiplicative conjunction]].

## Related pages

* [[deductive system]]
* [[sequent calculus]]
* [[type theory]]
* [[natural deduction]]

[[!redirects Hilbert systems]]
[[!redirects Hilbert calculus]]
[[!redirects Hilbert calculi]]
[[!redirects Hilbert-style system]]
[[!redirects Hilbert-style systems]]
[[!redirects Hilbert-style deductive system]]
[[!redirects Hilbert-style deductive systems]]

