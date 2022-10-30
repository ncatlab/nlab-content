
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Judgments
* table of contents
{: toc}

## Idea

In [[formal logic]], a __judgment__, or __judgement__, is a "meta-[[proposition]]"; that is, a proposition belonging to the [[meta-language]] (the [[deductive system]] or [[logical framework]]) rather than to the [[object language]].

More specifically, any [[deductive system]] includes, as part of its specification, which strings of symbols are to be regarded as the _judgments_.  Some of these symbols may themselves express a [[proposition]] in the object language, but this is not necessarily the case.

The interest in judgements is typically in how they may arise as _theorems_, or as _consequences_ of other judgements, by way of the [[deduction]] rules in a deductive system.  One writes
$$\vdash J$$
to mean that $J$ is a judgment that is derivable, i.e. a [[theorem]] of the deductive system.


## Examples

### In first-order logic

In [[first-order logic]], a paradigmatic example of a judgement is the judgement that a certain string of symbols is a well-formed [[proposition]].  This is often written as "$P \;prop$", where $P$ is a [[metavariable]] standing for a string of symbols that denotes a proposition.

Another example of a judgement is the judgement that these symbols form a proposition [[proof|proved]] to be [[true]].  This judgment is often written as "$P\;true$".

Neither of these judgements is the same thing as the proposition $P$ itself.  In particular, the proposition is a statement *in* the logic, while the judgement that the proposition is a proposition, or is provably true, is a statement *about* the logic.  However, often people abuse notation and conflate a proposition with the judgment that it is true, writing $P$ instead of $P\;true$.


### In type theory

The distinction between judgements and [[propositions]] is particularly important in [[intensional type theory]].

The paradigmatic example of a judgment in [[type theory]] is a *typing judgment*.  The assertion that a [[term]] $t$ has [[type]] $A$ (written "$t:A$") is not a statement *in* the type theory (that is, not something which one could apply logical operators to in the type-theoretic system) but a statement *about* the type theory.

Often, type theories include only a particular small set of judgments, such as:

* typing judgments (written $t:A$, as above)
* judgments of typehood (usually written $A \;type$)
* judgments of [[equality]] between typed terms (written say $(t=t'):A$)

(In a type theory with a [[type of types]], judgments of typehood can sometimes be incorporated as a special case of typing judgments, writing $A:Type$ instead of $A\;type$.)

These limited sets of judgments are often defined [[inductive definition|inductively]] by giving [[type formation]]/[[term introduction]]/[[term elimination]]- and [[computation rules]] (see [[natural deduction]]) that specify under what hypotheses one is allowed to conclude the given judgment.

These inductive definitions can be formalized by choosing a particular [[type theory]] to be the meta-language; usually a very simple type theory suffices (such as a [[dependent type theory]] with only [[dependent product types]]).  Such a meta-type-theory is often called a [[logical framework]].


## Hypothetical and generic judgments

It may happen that a judgment $J$ is only derivable under the assumptions of certain other judgments $J_1,\dots, J_2$.  In this case one writes
$$ J_1,\dots,J_n \;\vdash J.$$
Often, however, it is convenient to incorporate hypotheticality into judgments themselves, so that $ J_1,\dots,J_n \;\vdash J $ becomes a single _[[hypothetical judgment]]_.  It can then be a consequence of other judgments, or (more importantly) a hypothesis used in concluding other judgments.  For instance, in order to conclude the truth of an [[implication]] $\phi\Rightarrow\psi$, we must conclude $\psi$ *assuming* $\phi$; thus the [[introduction rule]] for implication is
$$ \frac{\phi \;\vdash\; \psi}{\vdash\; \phi\Rightarrow\psi}$$
with a hypothetical judgment as its hypothesis.  See [[natural deduction]] for a more extensive discussion.

In a [[type theory]], we may also consider the case where the hypotheses $J_1$ are typing judgments of the form $x:A$, where $x$ is a [[variable]], and in which the conclusion judgment $J$ involves these variables as [[free variables]].  For instance, $J$ could be $\phi\;prop$, where $\phi$ is a valid (well-formed) proposition only when $x$ has a specific [[type]] $X$.  In this case we have a _[[generic judgement]]_, written
$$ (x \colon X) \;\vdash\; (\phi \; prop). $$
which expresses that _assuming the hypothesis or [[antecedent]] judgement_ that $x$ is of type $X$, as a consequence we have the [[succedent]] judgement that $\phi$ is a proposition. If on the right here we have a typing judgment 

$$
  (x \colon X) \;\vdash\; (t \colon A)
$$

we have a _[[term in context]]_.

For more about the precise relationship between the various meanings of $\vdash$ here, see [[natural deduction]] and [[logical framework]].

While this may seem to be a very basic form of (hypothetical/generic) judgement only, in systems such as [[dependent type theory]] or [[homotopy type theory]], all of [[logic]] and a good bit more is all based on just this.

## Related concepts

* [[infinite judgment]]

## References

Foundational discussion of the notion of _judgement_ in [[formal logic]] is in



* {#Martin-L&#246;f83} [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, lecture series in Siena (1983) ([web](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))
 

* {#MartinLoef90} [[Per Martin-Löf]], _A path from logic to metaphysics_, talk at _Nuovi problemi della logica e della filosofia della scienza_, Jan 1990 ([pdf](https://github.com/michaelt/martin-lof/raw/master/pdfs/A-path-from-logic-to-metaphysics-1991.pdf))


More on this is in in sections 2 and 3 of

* [[Frank Pfenning]], Rowan Davies, _A judgemental reconstruction of modal logic_ (2000) ([pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf))
 {#Pfenning-Davies}

A textbook acccount is in section I.3 of 

* [[Robert Harper]], _[[Practical Foundations for Programming Languages]]_

Something called _judgement_ (Urteil) appears in 

* [[Georg Hegel]], second part, first section, second chapter of _[[Science of Logic]]_.

[[!redirects judgment]]
[[!redirects judgments]]
[[!redirects judgement]]
[[!redirects judgements]]
[[!redirects hypothetical judgment]]
[[!redirects hypothetical judgments]]
[[!redirects hypothetical judgement]]
[[!redirects hypothetical judgements]]
[[!redirects generic judgment]]
[[!redirects generic judgments]]
[[!redirects generic judgement]]
[[!redirects generic judgements]]
