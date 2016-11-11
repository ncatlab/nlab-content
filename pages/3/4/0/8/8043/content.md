
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

Typical judgements assert for example that a particular formula $\phi$ has no free variables or that a proposition $\phi$ is derivable, i.e. a [[theorem]] of the deductive system.  One writes
$$\vdash \phi$$
for this latter judgement.


## Examples

### In first-order logic

In [[first-order logic]], a paradigmatic example of a judgement is the judgement that a certain string of symbols is a well-formed [[proposition]].  This is often written as "$P \;prop$", where $P$ is a [[metavariable]] standing for a string of symbols that denotes a proposition.

Another example of a judgement is the judgement that these symbols form a proposition [[proof|proved]] to be [[true]].  This judgment is often written as "$P\;true$".

Neither of these judgements is the same thing as the proposition $P$ itself.  In particular, the proposition is a statement *in* the logic, while the judgement that the proposition is a proposition, or is provably true, is a statement *about* the logic.  However, often people abuse notation and conflate a proposition with the judgment that it is true, writing $P$ instead of than $P\;true$.


## Hypothetical judgments

It may happen that a proposition $\phi$ is only derivable under the assumptions of certain other proposition $\phi_1,\dots, \phi_2$. The judgement that expresses this situation is written
$$ \phi_1,\dots,\phi_n \;\vdash \phi.$$
For instance, in order to conclude the truth of an [[implication]] $\phi\Rightarrow\psi$, we must conclude $\psi$ *assuming* $\phi$; thus the [[introduction rule]] for implication is
$$ \frac{\phi \;\vdash\; \psi}{\vdash\; \phi\Rightarrow\psi}$$
with a hypothetical judgment as its hypothesis.

For more about the precise relationship between the various meanings of $\vdash$ here, see [[natural deduction]] and [[logical framework]].

## Related concepts

* [[infinite judgment]]

## References

Foundational discussion of the notion of _judgement_ in [[formal logic]] is in



* {#Martin-L&#246;f83} [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, leture series in Siena (1983) ([web](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))
 

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
