
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

In [[formal logic]], a _metalanguage_ is a [[language]] (formal or informal) in which the symbols and rules for manipulating another (formal) language -- the _object language_ -- are themselves formulated.  That is, the metalanguage is the language used when talking *about* the object language.

For instance the symbol $\phi$ may denote a [[proposition]] in a [[deductive system]], but the statement "$\phi$ can be proven" is not itself a proposition in the deductive system, but a statement in the metalanguage, often denoted by a [[sequent]] of the form

$$
  \vdash \phi \, true
$$

and then called a _[[judgement]]_ instead (in [[type theory]] one might also omit the "$true$", see at _[[propositions-as-types]]_ for details on this). Or, more generally, if the truth of $\phi$ depends on the truth of some other proposition $\psi$ then 

$$
  \psi \, true \vdash \phi \, true
$$

is the [[hypothetical judgement]] in the metalanguage that there is a [[proof]] of $\phi$ in the [[context]] in which $\psi$ is assumed.

In contrast, the [[implication]] expression $(\psi \to \phi)$ may denote another [[proposition]] in the object language, a [[conditional statement]]. A [[deduction theorem]] connects the two, in that it says that if the [[judgement]]

$$
  \psi \, true \vdash \phi \, true  

$$

holds in the metalanguage, then the judgement

$$
  \vdash (\psi \to \phi) \, true
$$

may be [[deduction|deduced]]; the converse is the rule of [[modus ponens]].  (Actually, both the deduction theorem and modus ponens are slightly more general, being relativized to an arbitrary [[context]], but we needn\'t get into that here.)


## Examples

* A system of [[natural deduction]] with its [[type formation]]/[[term introduction]]/[[term elimination]] and [[computation rules]] is the metalanguage for [[type theory]].


## References

Detailed discussion of the difference between judgements in the metalanguage and propositions in the object language is in the foundational lectures

* [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, lecture series in Siena (1983) ([web](https://ncatlab.org/nlab/files/MartinLofOnTheMeaning96.pdf))
 {#Martin-L&#246;f83}


[[!redirects object language]]
[[!redirects object languages]]
[[!redirects object theory]]
[[!redirects object theories]]

[[!redirects metalanguage]]
[[!redirects metalanguages]]
[[!redirects meta-language]]
[[!redirects meta-languages]]
