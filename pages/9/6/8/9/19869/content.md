# Initiality Project - Type Theory

This page is part of the [[Initiality Project]].

* table of contents
{: toc}

## Bidirectionality

All our terms are fully annotated.  For instance, we write $App^{(x:A)B}(M,N)$ rather than just $App(M,N)$.  It is, at best, unclear whether any less than fully annotated syntax can be used in an initiality theorem without "preprocessing" that is tantamount to annotating it.

In particular, this means that given $\Gamma$ and $T$, if $\Gamma \vdash T:A$ can be derived for any value of $A$, then there is a canonical such $A$ that can be deduced syntactically, or *synthesized*, from $\Gamma$ and $T$. For instance, if $App^{(x:A)B}(M,N)$ has any type, then it must have the type $B[N/x]$. On the other hand, the conversion rule implies that $App^{(x:A)B}(M,N)$ must also have any type that is judgmentally *equal* to $B[N/x]$. But in what sense does it have those types, if it doesn't synthesize them?

Since all our terms are fully annotated, all of our formation, introduction, and elimination rules can synthesize their types.  However, the type annotations also tell us what types the subterms need to have, in order for the term to have its canonical type.  These types may not be *syntactically* equal to the types synthesized by the subterms, so we need to *check* subterms against the types we want. The check should succeed if and only if the subterm's synthesized type is *judgmentally* equal to the one we want. So in the $App^{(x:A)B}(M,N)$ example, it *synthesizes* only $B[N/x]$, up to syntactic equality, but it *checks against* any type judgmentally equal to $B[N/x]$

Type theorists have a standard technique for distinguishing these two situations, known as [[bidirectional typechecking]].  Instead of one judgment $\Gamma\vdash t:A$, we have two typing judgments:

* $\Gamma \vdash T \Rightarrow A$: in context $\Gamma$ the term $T$ *synthesizes* the type $A$.  Here $A$ is, if it exists, uniquely determined by $\Gamma$ and $T$: it is an "output" to their "inputs".
* $\Gamma \vdash T \Leftarrow A$: in context $\Gamma$ the term $T$ *checks against* the type $A$.  Here $\Gamma$, $T$, and $A$ are all "inputs" and the only "output" is the truth value of whether the typecheck is valid.

Whereas unidirectional typing rules have the conversion rule, allowing the type to be changed at any point to a judgmentally equal one, with bidirectional typing rules, conversion is only used when switching from a synthesizing premise to a checking conclusion, using the "mode-switching" rule. (See below)

Unlike typical versions of bidirectional typing, in our approach the checking judgment is defined *solely* by the mode-switching rule, and all other typing rules conclude a synthesizing judgment. This variant doesn't help with typechecking algorithms, but it still factors out type conversion cleanly.

So in summary, terms formers are fully annotated, their typing rules *synthesize* a type in the conclusion, and have premises that *check* their subterms against appropriate types, so the mode-switching rule gets applied a lot, because it's the only way, in our system, to derive a checking judgment.

From a syntactic perspective, there are many advantages of bidirectional typechecking, but it is unclear at present whether any of them are relevant to categorical semantics (although by using a bidirectional framework we are better placed to take advantage of them if they do become relevant).  But more importantly, the natural structure of the semantic interpretation, as suggested by [[Peter Lumsdaine]], matches the syntactic bidirectional picture quite closely, and it may be clarifying to make that analogy more precise.

## Contexts

A **raw context** is a finite list of pairs consisting of a variable and a raw term in which the variables occurring are all pairwise distinct.  Each such pair, written $x:A$, is called a **typing declaration**, with $A$ being a type to which the variable $x$ belongs.

A **valid context** is a raw context $(x_1:A_1, \dots ,x_n:A_n)$ such that each judgment $x_1:A_1,\dots, x_k:A_k \vdash A_{k+1} \, type$ is derivable by the rules below.  This notion is defined *a posteriori* after the primitive rules for all the judgments have been given.  In particular, the judgments themselves never refer to context validity.  The intuitive interpretation of a judgment-in-context $\Gamma\vdash \mathcal{J}$ should therefore be "*if* $\Gamma$ is a valid context, then $\mathcal{J}$ holds in that context" (and this is the meaning we will give it semantically).

## Judgment forms

Our type theory has five judgment forms.  Here $\Gamma$ is a metavariable ranging over raw contexts, while $S,T,A,B$ are metavariables ranging over raw terms.

1. $\Gamma \vdash A\,type$ --- "$A$ is a type in context $\Gamma$".
2. $\Gamma \vdash T \Leftarrow A$ --- "$T$ can be checked to have type $A$ in context $\Gamma$"
3. $\Gamma \vdash T \Rightarrow A$ --- "$T$ synthesizes the type $A$ in context $\Gamma$"
4. $\Gamma \vdash A \equiv B \, type$ --- "$A$ and $B$ are judgmentally equal types in context $\Gamma$"
5. $\Gamma \vdash S \equiv T : A$ --- "$S$ and $T$ are judgmentally equal terms of type $A$ in context $\Gamma$"

### Modes, preconditions, etc.

All the metavariables occurring in all of our judgments should be regarded as "inputs", with the sole exception that $A$ in the synthesizing judgment $\Gamma \vdash T \Rightarrow A$ is an output.  In other words, if we regard "searching for a derivation of some judgment" as an "algorithm", with the rules for deriving that judgment as the "cases to try" and their premises as the resulting "recursive calls", then in all but one case the algorithm takes all the arguments of the judgment as inputs and returns only a [[truth value]], while in the exceptional case $\Gamma \vdash T \Rightarrow A$ it takes $\Gamma$ and $T$ as inputs and returns $A$ as output (if it succeeds, otherwise it returns failure).

Note, though, that because our judgmental equality is not bidirectional and need not be even semidecidable, these "algorithms" are not really algorithms, unless we regard the equality judgment as a sort of "oracle" that they can invoke.

Similarly, we regard validity of all the "inputs" of each judgment as something that the "caller" should ensure, while validity of the "output" as something that the function returning it should "promise".  For example, the rules for deriving a judgment such as $\Gamma \vdash T \Leftarrow A$ need only be "correct" under the *assumption* that $\Gamma$ is a valid context and $\Gamma \vdash A\,type$, but in turn these assumptions must ensure that all the analogous "preconditions" of all *premises* of such rules hold.

## Primitive rules

### Structural rules

The main structural rule is the "variable" or "hypothesis" rule, which says that if a variable is declared in a context, then as a term it synthesizes the type that it is declared with:

$$ \frac{(x:A) \in \Gamma}{\Gamma \vdash x \Rightarrow A}$$

The other structural rules of weakening, contraction, and substitution will be admissible.

### Mode-switching rule

The mode-switching rule says that to check that a term has a given type, we first synthesize a type for that term and then check that this type equals the given one.  In our fully annotated system, this is the *only* way to derive the checking judgment $\Gamma \vdash T \Leftarrow B$.

$$ \frac{\Gamma \vdash T \Rightarrow A \qquad \Gamma \vdash A \equiv B \, type}{\Gamma \vdash T \Leftarrow B}$$

This is also the only incarnation of the conversion rule, which in a "unidirectional" system is 

$$ \frac{\Gamma \vdash T : A \qquad \Gamma \vdash A \equiv B \, type}{\Gamma \vdash T : B.}$$

A bidirectional system controls this rule more carefully, enforcing it to be used (when and) only when the mode switches.

### Equality rules

We have primitive rules asserting that equality of terms and types are both reflexive, transitive, and symmetric, and moreover that equality of terms is invariant under equality of types.

TODO.

### Constant rules

TODO.  In fact, specifying the constant rules is part of the "signature".

### Type former rules

Each type former ($\Pi$-types, $\Sigma$-types, etc.) has a collection of rules giving its

* formation rule (when is it a valid type)
* introduction rule (what terms synthesize this type)
* elimination rule (how terms in this type can be used)
* equality rules ([[beta-reduction]] and, sometimes, [[eta-conversion]])
* congruence rules (the type former and its introduction and elimination forms respect judgmental equality)

#### $\Pi$-types

[[!include Initiality Project - Type Theory - Pi-types]]

## Admissible rules

(TODO)
