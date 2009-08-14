An _implication_ may be either an _entailment_ or a _conditional_ statement; these are closely related but not quite the same thing.

__Entailment__ is a [[preorder]] on statements within a given [[context]] (including which [[logic]] is being used).  We say that $p$ entails $q$ _semantically_, written $p \vdash q$, if $q$ can be proved from the assumption $p$.  We say that $p$ entails $q$ _syntactically_, written $p \vDash q$, if $q$ holds in every model in which $p$ holds.  (These relations are often equivalent, by various soundness and completeness theorems.)  Notice that while $p$ and $q$ are statements in some _object language_ (the language that we are talking about), $p \vdash q$ and $p \vDash q$ are statements in the _metalanguage_ (the language that we are using to talk about the object language).

A __conditional__ statement is an operation on statements within a given context.  If $p$ and $q$ are statements in some logic, then so is the conditional statement $p \to q$ (at least if that logic has a notion of conditional).  Notice that $p$, $q$, and $p \to q$ are all statements in the _object_ language.

Depending on what logic one is using, $p \to q$ might be anything, but it\'s probably not fair to consider it a conditional statement unless it is related to entailment as follows:
+-- {: .standout}
If, in some context, $p$ entails $q$ (either semantically or syntactically), then $p \to q$ is a theorem (semantically) or a tautology (syntactically) in that context.
=--