
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

In [[type theory]] the _empty type_ is the [[type]] with no [[term]].

In a [[model]] by [[categorical semantics]], this is an [[initial object]]. In [[set theory]], it is an [[empty set]].

## Definition

Like all type constructors in type theory, to characterize the empty type we must specify how to build it, how to construct elements of it, how to use such elements, and the computation rules.

The way to build the empty type is trivial: it exists.

$$\frac{ }{\emptyset\colon Type}$$

### As a positive type

The empty type is most naturally presented as a [[positive type]], so that the constructor rules are primary.  However, since the empty type is supposed to contain no elements, there *are* no constructor rules.

The eliminator rules are derived from the constructor rules in the usual way: to use a term $e\colon \emptyset$, it suffices to specify what should be done for all the (zero) ways that $e$ could have been constructed.  Thus, we don't need any hypotheses:

$$\frac{ }{e\colon \emptyset \vdash abort_C(e)\colon C}$$

That is, given an element of $\emptyset$, we can construct an element of any type $C$.  In [[dependent type theory]], we must generalize the eliminator to allow $C$ to depend on $\emptyset$.

There is no [[beta-reduction]] rule, since there are no constructors to compose with the eliminator.  However, there is an [[eta-conversion]] rule, which says that for any term $e\colon \emptyset\vdash c\colon C$ in a context including a term of type $\emptyset$, we have

$$ abort_C(e) \;\leftrightarrow_\eta\; c.$$

As with the $\eta$-conversion rule for the negative presentation of the [[unit type]], this is ill-defined as a *reduction* (since we cannot determine $c$ from $abort_C(e)$), but makes sense as an *expansion*.

The positive presentation of the empty type can be regarded as a particular sort of [[inductive type]].  In [[Coq]] syntax:

    Inductive empty : Type :=
    .

Coq implements the beta reduction rule, but not the eta (although eta equivalence is provable for the inductively defined [[identity types]], using the dependent eliminator mentioned above).


### As a negative type

As for binary [[sum types]], it is possible to present the empty type as a [[negative type]] as well, but only if we allow [[sequents]] with multiple conclusions.  This is common in [[sequent calculus]] presentations of [[classical logic]], but not as common in type theory and almost unheard of in [[dependent type theory]].

The two definitions are provably equivalent, but only using the [[contraction rule]] and the [[weakening rule]].  Thus, in [[linear logic]] they become distinct; the positive empty type is "zero" $\mathbf{0}$ and the negative one is "bottom" $\bot$.


## Related concepts

[[!include empty objects -- contents]]


* [[nothing]], 

* [[sum type]]
* [[unit type]]



[[!redirects bottom type]]
[[!redirects bottom types]]

[[!redirects empty type]]
[[!redirects empty typpe]]
[[!redirects empty types]]
