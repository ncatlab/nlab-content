
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A [[function]] $f$ is defined by its association to each input value $x$ (belonging to some allowable [[domain]] of values) of an output value, usually denoted $f(x)$ or $f x$.  The process of passing from $f$ and $x$ to $f(x)$ is called **function application**, and one speaks of **applying** $f$ to $x$ to produce $f(x)$.

The determination of the allowable domain for $x$, given $f$, depends a bit on [[foundations|foundational]] choices.  In [[type theory]] and [[structural set theory]], all [[functions]] have a [[type]] (a [[function type]], naturally) which specifies their domain and codomain.  In [[material set theory]], a function is sometimes defined to be simply a particular sort of set of ordered pairs, with its domain specified implicitly as the set of elements occurring as first components of some such pair.  (However, even in material set theory it is sometimes important for a function to come with a specified domain and/or codomain, in which case it can be defined to be an ordered triple.)

## Syntax versus semantics

In formalized [[logic]] and [[type theory]], $f$, $x$, and $f(x)$ are [[terms]] (or more precisely, [[metavariable|metavariables]] standing for terms), and the process of function application is a rule of term formation.  This is something which belongs to the realm of [[syntax]]. On [[propositions]] ([[(-1)-truncation|(-1)-truncated]] types) this is the [[modus ponens]] [[deduction]] rule.

Under a [[denotational semantics|denotational]] [[semantics]], each of these terms denotes a particular object, and we also refer to the object denoted by $f(x)$ as the result of applying the object denoted by $f$ to the object denoted by $x$.  For instance, in a [[material set theory|material set-theoretic]] semantics, $f$ would denote a set of [[ordered pairs]] such that for any $a$, there is at most one $b$ such that $(a,b)\in f$, and $x$ would denote some $a$ such that there *does* exist such a $b$, and $f(x)$ would denote that uniquely specified $b$.  The distinction between the terms $f$, $x$, and $f(x)$ and what they denote is usually (and harmlessly) blurred in ordinary mathematical practice, but when studying logic and type theory formally it becomes important.

Under an [[operational semantics|operational]] [[semantics]], by contrast, the "meaning" of the term $f(x)$ lies in how it is "evaluated".  Usually this proceeds by [[beta-reduction]] and related rules.  For instance, if $f$ is the [[lambda-calculus|term]] $\lambda x. x*x$ and $x$ is the term $s(s(0))$ (the [[numeral]] [[two]]), then $f(x)$ is $(\lambda x.x*x)(s(s(0)))$ which beta-reduces to $s(s(0))*s(s(0))$.  The definition of $*$ can then be invoked to cause futher beta-reductions resulting in $s(s(s(s(0))))$ (the numeral four).

## Dependent function application

In [[dependent type theory]], there is a notion of a [[dependent function]], which is essentially a function $f:(x:A) \to B(x)$ whose [[target]] is a [[type family]] rather than a single [[type]]. The application of a dependent function at a [[term]] $x:A$ is called **dependent function application**. 

## Related concepts

* [[evaluation map]]

* [[function application to identifications]]

* [[dependent function application to identifications]]

[[!redirects application]]

[[!redirects dependent function application]]