
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


# Judgements
* table of contents
{: toc}

## Idea

In [[formal logic]], a __judgment__ or __judgement__ is a "meta-[[proposition]]"; that is, a proposition belonging to the [[meta-language]] (the [[logical framework]]) rather than to the [[object language]].

Specifically in systems of [[natural deduction]], _judgements_ are statements concerning the strings of symbols of the system, whereas some of these symbols may themselves express a [[proposition]]. A basic example of a judgement is a _typing judgement_, usually written in the form

$$
  x : X
  \,,
$$

which asserts that a string of symbols $x$ expresses a [[term]] of a given [[type]] $X$. For instance the judgement

$$
  \phi : Prop
$$

(often also written just "$\phi \;\; Prop$") asserts that the string of symbols represented by $\phi$ expresses a formal [[proposition]] (and hence clearly the statement "$\phi$ is a proposition" is on a "meta-level" as compared to $\phi$ itself).

Similarly if $X$ expresses a [[type]] (of [[terms]]) in the system, then there is a judgement written

$$
  x : X
$$

which expresses the statement that the string of symbols given by $x$ describes a [[term]] of [[type]] $X$. Notably, under the [[propositions as types]]-paradigma, we may identify $X$ with a [[proposition]] (namely as the type of all terms that verify that proposition) and in this case the judgement $x : X$ exhibits $x$ as a [[proof]] of that proposition and hence says that "$X$ is [[true]]", which is the judgement often written as

$$
  X \;\; true
  \,,
$$

naturally.

As the colon-notation suggests, indeed all these kinds of judgements are unified if there is a [[type of propositions]] or even a [[type of types]] in the system. In this case the judgement $\phi : Prop$ is itself a typing judgement, it says that $\phi$ is of type $Prop$.

The interest in judgements is typically in how they may arise as _consequences_ of other judgements by [[deduction]] rules. For instance it may happen that "$x$" appears as a [[free variable]] in $\phi$ but that $\phi$ is a valid (well-formed) proposition only if $x$ is of a specific [[type]] $X$. In this case one has a _[[hypothetical judgement]]_ or _[[sequent]]_ written

$$
  x : X \vdash \phi : Prop
$$

which expresses that _assuming the hypothesis or [[antecedent]] judgement_ that $x$ is of type $X$, as a consequence we have the [[succedent]] judgement that $\phi$ is a proposition.

While this may seem to be a very basic form of (hypothetical) judgement only, in systems such as [[dependent type theory]] or [[homotopy type theory]] indeed all of [[logic]] and a good bit more is all based on just this.


## Examples

### In first-order logic

In [[first-order logic]], a paradigmatic example of a judgement is the judgement that a certain string of symbols is a well-formed [[proposition]].  Another example of a judgement is the judgement that these symbols form a proposition [[proof|proved]] to be [[true]].  Neither of these judgements is the same thing as the proposition itself.  In particular, the proposition is a statement *in* the logic, while the judgement that the proposition is a proposition or is provably true is a statement *about* the logic.


### In type theory

The distinction between judgements and [[propositions]] is particularly important in [[intensional type theory]].

The paradigmatic example of a judgment in [[type theory]] is a *typing judgment*.  The assertion that a [[term]] $t$ has [[type]] $A$ (written "$t:A$") is not a statement *in* the type theory (that is, not something which one could apply logical operators to in the type-theoretic system) but a statement *about* the type theory.

Often, type theories include only a particular small set of judgments, such as:

* typing judgments
* judgments of typehood (usually written $A \;type$)
* judgments of [[equality]] between typed terms, written say $(t=t'):A$

These limited sets of judgments are often defined [[inductive definition|inductively]] by giving [[type formation]]/[[term introduction]]/[[term elimination]]- and [[computation rules]] that specify under what hypotheses one is allowed to conclude the given judgment.  These inductive definitions can be formalized by choosing a particular [[type theory]] to be the meta-language; usually a very simple type theory suffices (such as a [[dependent type theory]] with only [[dependent product types]]).  Such a meta-type-theory is often called a [[logical framework]].


## References

Foundational discussion of the notion of _judgement_ is in

* [[Per Martin-Löf]], _On the meaning of logical constants and the justifications of the logical laws_, leture series in Siena (1983) ([web](http://docenti.lett.unisi.it/files/4/1/1/6/martinlof4.pdf))
 {#Martin-L&#246;f83}

More on this is in in sections 2 and 3 of

* [[Frank Pfenning]], Rowan Davies, _A judgemental reconstruction of model logic_ (2000) ([pdf](http://www.cs.cmu.edu/~fp/papers/mscs00.pdf))
 {#Pfenning-Davies}

[[!redirects judgment]]
[[!redirects judgments]]
[[!redirects judgement]]
[[!redirects judgements]]
