# Initiality Project - Type Theory

This page is part of the [[Initiality Project]].

* table of contents
{: toc}

## Bidirectionality

All our terms are fully annotated.  For instance, we write $App^{(x:A)B}(M,N)$ rather than just $App(M,N)$.  It is, at best, unclear whether any less than fully annotated syntax can be used in an initiality theorem without "preprocessing" that is tantamount to annotating it.

In particular, this means that given $\Gamma$ and $T$, if $\Gamma \vdash T:A$ can be derived for any value of $A$, then there is a canonical such $A$ that can be deduced syntactically, or *synthesized*, from $\Gamma$ and $T$.  For instance, if $App^{(x:A)B}(M,N)$ has any type, then it must have the type $B[N/x]$.  On the other hand, the conversion rule implies that $App^{(x:A)B}(M,N)$ must also have any type that is judgmentally *equal* to $B[N/x]$.

Type theorists have a standard technique for distinguishing these two situations, known as [[bidirectional typechecking]].  Instead of one judgment $\Gamma\vdash t:A$, we have two typing judgments:

* $\Gamma \vdash T \Rightarrow A$: in context $\Gamma$ the term $T$ *synthesizes* the type $A$.  Here $A$ is, if it exists, uniquely determined by $\Gamma$ and $T$: it is an "output" to their "inputs".
* $\Gamma \vdash T \Leftarrow A$: in context $\Gamma$ the term $T$ *checks against* the type $A$.  Here $\Gamma$, $T$, and $A$ are all "inputs" and the only "output" is the truth value of whether the typecheck is valid.

There are various advantages of bidirectional typechecking, including:

1. In at least some cases, it permits a formulation of type theory in which only normal forms exist.
1. In at least some cases, it allows omission of annotations, e.g. an un-annotated abstraction $\lambda x.M$ cannot synthesize a type, but it can check against a $\Pi$-type $\Pi(x:A). B$.
1. In at least some cases, it makes it easier to incorporate [[η-expansion]] into an equality-checking algorithm.
1. In at least some cases, it makes derivations of judgments unique, or at least canonical.
1. In at least some cases, it isolates the use of judgmental equality during typechecking in one particular "mode-switching" rule (see below).

(Experts, feel free to add more.)  It is unclear at present whether any of these advantages are relevant to categorical semantics, but by using a bidirectional framework we are better placed to take advantage of them if they do become relevant.  More importantly, the natural structure of the semantic interpretation, as suggested by [[Peter Lumsdaine]], matches the syntactic bidirectional picture quite closely, and it may be clarifying to make that analogy more precise.

Since all our terms are fully annotated, all of our formation, introduction, and elimination rules can synthesize their types.  However, their *premises* usually involve *checking* their subterms against appropriate types, so the mode-switching rule gets applied a lot (it is the only way, in our system, to derive a checking judgment).  This might be an issue to want to optimize away in an implementation, but for our semantic purposes it seems irrelevant.

## Contexts

A **raw context** is a finite list of pairs consisting of a variable and a raw term.  Each such pair, written $x:A$, is called a **typing declaration**, with $A$ being a type to which the variable $x$ belongs.

A *valid context* will be a raw context $(x_1:A_1, \dots ,x_n:A_n)$ such that $x_k \neq x_\ell$ for $k\neq \ell$, and each judgment $x_1:A_1,\dots, x_k:A_k \vdash A_{k+1} \, type$ is derivable by the rules below.  In fact this notion is defined by a judgment mutually-inductively with the other rules to ensure that the context in any derivable judgment is valid, although in only a few cases (rules without any other premise) do we need that premise explicitly.

## Judgment forms

Our type theory has six judgment forms.  Here $\Gamma$ is a metavariable ranging over raw contexts, while $S,T,A,B$ are metavariables ranging over raw terms.

1. $\Gamma \, ok$ --- "$\Gamma$ is a valid context"
1. $\Gamma \vdash A\,type$ --- "$A$ is a type in context $\Gamma$"
2. $\Gamma \vdash T \Leftarrow A$ --- "$T$ can be checked to have type $A$ in context $\Gamma$"
3. $\Gamma \vdash T \Rightarrow A$ --- "$T$ synthesizes the type $A$ in context $\Gamma$"
4. $\Gamma \vdash A \equiv B \, type$ --- "$A$ and $B$ are judgmentally equal types in context $\Gamma$"
5. $\Gamma \vdash S \equiv T : A$ --- "$S$ and $T$ are judgmentally equal terms of type $A$ in context $\Gamma$"

### Modes, preconditions, etc.

TODO

## Primitive rules

### Context rules

The empty context is valid, and any valid context can be extended by a new variable belonging to a valid type:

$$ \frac{ }{() \, ok} \qquad \frac{\Gamma \,ok \qquad x\notin \Gamma \qquad \Gamma \vdash A\,type}{(\Gamma,x:A) \, ok}$$

### Structural rules

The main structural rule is the "variable" or "hypothesis" rule, which says that if a variable is declared in a context, then as a term it synthesizes the type that it is declared with:

$$ \frac{\Gamma\, ok \qquad (x:A) \in \Gamma}{\Gamma \vdash x \Rightarrow A}$$

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
