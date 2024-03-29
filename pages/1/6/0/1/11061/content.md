
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

# Contents
* table of contents
{: toc}

## Idea

In [[formal logic]], _modus ponens_ is the [[elimination rule]] for the [[logical connective]] $\to$ (forming [[conditional statements]]).

On more general [[types]] in [[type theory]] this is [[function application]].

Even in Hilbert-style logic where there are almost no [[rule of inference|rules of inference]] (besides the many [[axioms]]), there is usually a rule of modus ponens.  (In particular, modus ponens is the *only* non-axiom rule of inference in [[David Hilbert|Hilbert]]\'s version of the [[propositional calculus]].)


## Statements

Modus ponens is the [[rule of inference]] which says that from the [[sequents]]

$$
  \vdash \psi
$$

and

$$
  \vdash \psi \to \phi
$$

asserting (respectively) the [[judgement]] that a [[proposition]] $\psi$ is [[true]] and the [[judgement]] that the [[conditional statement]] $\psi \to \phi$ is also true, the sequent

$$
  \vdash \phi
$$

(asserting the judgement that the proposition $\phi$ is true) may be [[deduction|deduced]].

Depending on what sort of sequents are allowed in the [[sequent calculus]] that one is working with, there may be additional [[context]] on either side of the sequents.  So rather generally, from

$$
  \Gamma \vdash \Delta,\; \psi,\; \Theta
$$

and

$$
  \Gamma \vdash \Delta,\; (\psi \to \phi),\; \Theta
,$$

we may deduce

$$
  \Gamma \vdash \Delta,\; \phi,\; \Theta
;$$

this rule may be summarized as

$$
  \frac{ \Gamma \vdash \Delta,\; \psi,\; \Theta ;\;\;\;
         \Gamma \vdash \Delta,\; (\psi \to \phi),\; \Theta }
       { \Gamma \vdash \Delta,\; \phi,\; \Theta }
.$$

In [[linear logic]], we must distinguish between the additive conditional $\to$, whose elimination rule is as above, and the multiplicative conditional $\multimap$, whose elimination rule is

$$
  \frac{ \Gamma \vdash \Delta,\; \psi,\; (\psi \multimap \phi),\; \Theta }
       { \Gamma \vdash \Delta,\; \phi,\; \Theta }
.$$

In [[noncommutative logic]], we would further distinguish this last version from

$$
  \frac{ \Gamma \vdash \Delta,\; (\psi \multimap^{op} \phi),\; \psi,\; \Theta }
       { \Gamma \vdash \Delta,\; \phi,\; \Theta }
.$$


## Properties

The converse to modus ponens, which is the [[introduction rule]] for conditional statements, is much less commonly admitted directly as a rule of inference, but its validity is typically a theorem, the _[[deduction theorem]]_; see also the discussion at _[[metalanguage]]_.

The [[categorical semantics]] of modus ponens in the form

$$
  \psi,\; (\psi \to \phi) \;\vdash \; \phi
$$

is the [[evaluation map]] of the ambient ([[locally cartesian closed category|locally]]) [[cartesian closed category]].


[[!redirects modus ponens]]
