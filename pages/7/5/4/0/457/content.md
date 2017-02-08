
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
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

A [[set]] or [[type]] is **inhabited** if it contains an [[element]] or [[term]].

## Definition

### In set theory

In [[set theory]], an **inhabited set** is a [[set]] that contains an [[element]], i.e. a set $X$ such that $\exists x, x\in X$ is [[true]].

At least assuming [[classical logic]], this is the same thing as a set that is [[negation|not]] [[empty set|empty]]. Usually inhabited sets are simply called 'non-empty', but the positive word 'inhabited' reminds us that inhabitation is the simpler notion, which emptiness is defined as the [[negation]] of.

The term 'inhabited' come from [[constructive mathematics]]. In constructive mathematics (such as the [[internal logic]] of some [[topos]] or generally in [[type theory]]), a set/type that is not empty is not already necessarily inhabited.  This is because [[double negation]] is nontrivial in [[intuitionistic logic]]. All the same, many constructive mathematicians use the old word 'non-empty' with the understanding that it *really* means inhabited, and write $A\neq \emptyset$ to mean that $A$ is inhabited.  The latter we can interpret literally if we regard $\neq$ as a reference to an [[inequality relation]] other than the [[denial inequality]], such as the inequality defined for subsets by $A \neq B \iff \exists x ((x\in A \wedge x\notin B)\vee(x\in B\wedge x\notin A))$.  If we prefer to reserve $\neq$ for the denial inequality, then we can write $\#$ for this stronger inequality of sets, and hence $A\#\emptyset$ to mean that $A$ is inhabited.

### In type theory

In [[type theory]] there are two possible notions of **inhabited type**: a type $X$ whose [[propositional truncation]] $\Vert X \Vert$ has an element (or [[term]]), or a type $X$ that *itself* has an element (or [[term]]).  The former is what corresponds to the above notion of inhabitedness in set theory, since $\Vert X \Vert$ is the [[propositions as types]] interpretation of $\exists x:X$.  The latter is more like the notion of a [[pointed set]].

The assertion $\forall X, (\Vert X \Vert \to X)$ is a mildly nonconstructive logical principle called the [[propositional axiom of choice]].  It follows from [[excluded middle]], but in the internal logics of some toposes, it can fail, so that these two notions of "inhabited type" really are different.

### Inhabited objects

An inhabited set is the special case of an internally [[inhabited object]] in the [[topos]] [[Set]].  The two notions of inhabited type correspond to internally and externally inhabited objects (which are, respectively, those objects $X$ where $X\to 1$ is an [[epimorphism]], and those which admit a [[global element]] $1\to X$).

### Related notions

There is a distinction between 'inhabited' and '[[occupied space|occupied]]' spaces in [[Abstract Stone Duality]] (which probably corresponds to something about [[locales]], should explain that here).


## Related concepts

* [[hProp]]

* [[effective epimorphism]]

* [[inhabited object]]

* [[bracket type]], [[image]]

* [[occupied space]]


[[!redirects inhabited set]]
[[!redirects inhabited sets]]
[[!redirects inhabited subset]]
[[!redirects inhabited subsets]]
[[!redirects inhabited type]]
[[!redirects inhabited types]]
[[!redirects inhabited space]]
[[!redirects inhabited spaces]]

[[!redirects nonempty set]]
[[!redirects non-empty set]]
[[!redirects nonempty sets]]
[[!redirects non-empty sets]]
[[!redirects nonempty subset]]
[[!redirects non-empty subset]]
[[!redirects nonempty subsets]]
[[!redirects non-empty subsets]]

[[!redirects nonempty]]
[[!redirects non-empty]]
