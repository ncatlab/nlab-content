An _implication_ may be either an _entailment_ or a _conditional_ statement; these are closely related but not quite the same thing.

__Entailment__ is a [[preorder]] on statements within a given [[context]] (including which [[logic]] is being used).  We say that $p$ entails $q$ _semantically_, written $p \vdash q$, if $q$ can be proved from the assumption $p$.  We say that $p$ entails $q$ _syntactically_, written $p \vDash q$, if $q$ holds in every model in which $p$ holds.  (These relations are often equivalent, by various soundness and completeness theorems.)  Notice that while $p$ and $q$ are statements in some _object language_ (the language that we are talking about), $p \vdash q$ and $p \vDash q$ are statements in the _metalanguage_ (the language that we are using to talk about the object language).

A __conditional__ statement is an operation on statements within a given context.  If $p$ and $q$ are statements in some logic, then so is the conditional statement $p \to q$ (at least if that logic has a notion of conditional).  Notice that $p$, $q$, and $p \to q$ are all statements in the _object_ language.


## Relation of these

Depending on what logic one is using, $p \to q$ might be anything, but it\'s probably not fair to consider it a conditional statement unless it is related to entailment as follows:
+-- {: .standout}
If, in some context, $p$ entails $q$ (either semantically or syntactically), then $p \to q$ is a theorem (semantically) or a tautology (syntactically) in that context, and conversely.
=--

You can think of entailment as being an [[external hom]] and the conditional as being an [[internal hom]].  In particular, we expect these to be related as in a [[closed category]]:

*  $ q \to r \vdash (p \to q) \to (q \to r) $,
*  $ p \equiv \top \to p $,
*  $ \top \vdash p \to p $,

where $\top$ is an appropriate constant statement (not necessarily satisfying $p \vdash \top$; compare [[linear logic]] with $\lolli$ for $\to$ and $1$ for $\top$).

Most kinds of logic have a notion of entailment from a [[list]] of multiple premises; then we expect entailment and the conditional to be related as in a closed [[multicategory]].

Just as we may identify the internal and external hom in [[Set]], so we may identify the entailment and conditional of [[truth value]]s.  In the $n$-Lab, we tend to write this as $\Rightarrow$, a symbol that is variously used by other authors in place of $\vdash$, $\vDash$, and $\rightarrow$.


## Heyting algebras

Although [[Heyting algebras]] were first developed as a way to discuss [[intuitionistic logic]], they appear in other contexts; but their characterstic feature is that they have a notion of implication.  So if you replace $\vdash$ above with the Heyting algebra\'s partial order $\leq$, then everything above applies.


[[!redirects Heyting implication]]
[[!redirects entailment]]
[[!redirects conditional]]
[[!redirects conditionals]]
[[!redirects conditional statement]]