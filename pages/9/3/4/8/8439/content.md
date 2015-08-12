
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Deduction and Induction
+-- {: .hide}
[[!include deduction and induction - contents]]
=--
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

# Contents
* table of contents
{: toc}

## Idea

A _logical framework_ is a formal [[metalanguage]] for [[deductive systems]], such as [[logic]], [[natural deduction]], [[type theories]], [[sequent calculus]], etc.  Of course, like any formal system, these systems can be described in any sufficiently stong metalanguage.  However, all logical systems of this type share certain distinguishing features, so it is helpful to have a particular metalanguage which is well-adapted to describing systems with those features.

Much of the description below is taken from [(Harper)](#Harper).

## Overview

The sentences of a logical framework are called [[judgments]].  It turns out that in deductive systems, there are two kinds of non-basic forms that arise very commonly, which we may call

* *[[hypothetical judgments]]*: one judgment is a logical consequence of some others.
* *generic judgments*: a judgment that is made generally for all values of some parameters, each ranging over a "domain" or "syntactic category".  (Note that a "syntactic category" in this sense is unrelated to the notion of [[syntactic category]] that is a [[category]] built out of syntax; here we mean "category" in its informal sense of a subgrouping, so that for instance we have one syntactic category of "types" and another of "terms".)

These two forms turn out to have many parallel features, e.g. [[reflexivity]] and [[transitivity]] of hypothetical judgments correspond to [[variable]]-use and [[substitution]] in generic judgments.  Appealing to the [[propositions as types]] principle, therefore, it is convenient to describe a system in which they are actually both instances of the same thing.  That is, we identify the notion of *evidence for a judgment* with the notion of *object of a syntactic category*.

This leads to a notion that we will call an _LF-type_.  Thus we will have types such as

* The _LF-type of evidence for some judgment_.
* The _LF-type of objects of a syntactic category_.

We will also have some general type-forming operations.  Perhaps surprisingly, it turns out that

* _[[dependent product types]]_ 

are all that we need.

There is a potential confusion of terminology, because these *LF-types* in a logical framework (being itself a [[type theory]]) are distinct from the objects that may be called "types" in any particular logic we might be talking about *inside* the logical framework.  Thus, for instance, when formalizing [[Martin-Lof type theory]] in a logical framework, there is an "LF-type" which is the type of objects of the syntactic category of MLTT-types.  This is furthermore distinct from a [[type of types]], which is itself an object of the syntactic category of MLTT-types, i.e. a term belonging to the LF-type of such.

Once we have set up the logical framework as a language, there are then two ways to describe a given logic inside of it.  See ([Harper](#Harper)), and the other [references](#References), for more details.

### Synthetic presentations

In a synthetic presentation, there is an LF-type for every judgment of the [[object theory]].  Thus, if the object theory is a type theory, then in LF we have things like:

* an LF-type $tp$ of object-theory types
* an LF-type $tm$ of object-theory terms
* a dependent LF-type $of : tm \to tp \to Type$, where Type denotes the LF-kind of LF-types.  That is, for each object-theory type $a$ and each object-theory type $A$, we have an LF-type $of(a,A)$ expressing the judgment "$a:A$" that $a$ is of type $A$.

Note that we do not have to explicitly carry around an ambient context, as we sometimes do when presenting type theories in a more explicit style of a [[deductive system]].  This is because the notions of hypothetical and generic judgments are built into the logical framework and handled automatically by *its* contexts.

Synthetic presentations are very flexible, but do not make maximal use of the framework in the case when the object-theory is also a type theory whose judgments are "analytic".

### Analytic presentation

An analytic presentation is only possible for certain kinds of object-theories, generally those which are type theories similar to LF itself.  In this case, we represent object-theory types by LF-types themselves.  Thus instead of the LF-type $tm$ of terms and the dependent LF-type $of$ above, we have

* a dependent LF-type $el : tp \to Type$

which assigns to each object-theory type, the LF-type of its elements.

In an analytic presentation of a logic, in addition to merely giving "axioms" such as $tp$ and $el$, we must give *equations* representing the rules of the object-theory as [[equalities]] in the logical framework.  For instance, we must have a [[beta-reduction]] rule such as

    app A B (lam A B F) M = F M

From a practical point-of-view, rather than extending the logical framework with ad hoc definitional equalities to represent a particular object-theory, often what is actually done is that equality is defined as another type family with explicitly-introduced constructors.  For example, in [[Twelf]], the above equation could be represented by first introducing the type family

    eq : {A:tp} el A -> el A -> type

(Twelf uses braces as notation for the [[dependent product]]), and then postulating a constant

    beta : {A:tp} {B:tp} eq (app A B (lam A B F)) (F M)

in addition to the other axioms of equality.

### Higher-order abstract syntax

In both synthetic and analytic presentations, we use [[higher-order abstract syntax]] (HOAS).  Roughly, this means that *variables* in the object-theory are not terms of some LF-type, but are represented by actual LF-variables.  For instance, when describing a type theory containing [[function types]] synthetically, we would have

* an LF-term $arr : tp \to tp \to tp$, where for object-theory types $A:tp$ and $B:tp$, the term $arr(A,B):tp$ represents their function-type
* an LF-term $app : tm \to tm \to tm$, where $app(f,a)$ represents the function application $f(a)$
* an LF-term $lam : (tm \to tm) \to tm$, representing lambda abstraction.

The point is that the argument of $lam$ (the "body" of the lambda abstraction) is not a "term containing a free variable $x$" but rather an LF-function from object-theory terms to object-theory terms.  This is intended to be the function "substitute" which knows about the body of the lambda-abstraction, and when given an argument it substitutes it for the variable in that body and returns the result.

This approach completely avoids dealing with the problems of variable binding and substitution in the object language, by making use of the binding and substitution in the metalanguage LF.  One might say that the variables in LF are the "universal notion of variable" which is merely reused by all object-theories.

### The power of weak frameworks

It may be tempting to think of the LF-types such as $tp$ and $tm$ as [[inductive type|inductively]] defined by their specified constructors (such as $arr$ for $tp$, and $app$ and $lam$ for $tm$).  However, this is incorrect; LF does not have inductive types.  In fact, this weakness is essential in order to guarantee "adequacy" of the HOAS encoding.

Suppose, for instance, that $tm$ were inductively defined inside of LF.  Then we could define a function $tm\to tm$ by pattern-matching on the structure of $tm$, doing one thing if $tm$ were a lambda-abstraction and another thing if it were a function application.  But such a function is definitely *not* the sort of thing that we want to be able to pass to the LF-function $lam$!  By disallowing such matching, though, we can guarantee that the only functions $tm\to tm$ we can define and pass to $lam$ correspond to "substituting in a fixed term" as we intended.

As an even simpler example, suppose we consider an object-theory containing just one LF-type $nat$ together with constructors $z : nat$ and $s : nat \to nat$.  Although we would like to think of $nat$ as representing the natural numbers, because of the lack of an induction principle, the LF-type $nat \to nat$ certainly cannot be shown to contain all the functions from natural numbers to natural numbers (essentially, we can only construct the constant functions and those incrementing their argument by a fixed constant).  On the other hand, to some extent it is possible to get around this restriction by taking a _relational_ rather than a functional point-of-view.  For example, addition of natural numbers can be defined as a type family

    add : nat -> nat -> nat -> type

together with a pair of constructors

    add/z : {N:nat} add z N N.
    add/s : {M:nat}{N:nat}{P:nat} add M N P -> add (s M) N (s P).

Now, it is still not possible to prove _inside_ LF that $add$ is a total functional relation (i.e., that for all `M:nat` and `N:nat` there exists a unique `P:nat` such that `add M N P`).  However, in this case that is certainly easy to verify by inspection, and the [[Twelf]] proof assistant has facilities for verifying such properties automatically (though in general checking totality is better supported than checking uniqueness).

## Implementations

One of the uses of a logical framework is that as a type theory itself, it can be implemented in a computer.  This provides a convenient system in which one can "program" the rules of any other specific type theory or logic which one wants to study.

For a list of logical framework implementations, see _[Specific logical Frameworks and Implementations](http://www.cs.cmu.edu/~fp/lfs-impl.html)_.

Historically, the first logical framework implementation was [[Automath]].
The goal of the Automath project was to provide a tool for the
formalization of mathematics without [[foundations|foundational]] prejudice.
Many modern logical frameworks carry influences of this.

Then inspired by the development of [[Martin-Löf dependent type theory]] was the [[Edinburgh Logical Framework]] (ELF).  The [[logic]] and [[type theory]]-approaches were later combined in the [[Elf]] language. This gave rise to [[Twelf]].


## References
 {#References}

* [[Frank Pfenning]], _Logical frameworks -- a brief introduction_ ([pdf](http://www.cs.cmu.edu/~fp/papers/mdorf01.pdf))

* [[Frank Pfenning]], _Logical frameworks_ In Alan Robinson and Andrei Voronkov (eds.) _Handbook of Automated Reasoning_, chapter 17, pages 1063&#8211;1147. Elsevier Science Publishers, 1999. ([ps](http://www-2.cs.cmu.edu/twelf/notes/handbook00.ps)).

* [[Frank Pfenning]], _Logical frameworks_ ([web](http://www.cs.cmu.edu/~fp/lfs.html))

* Randy Pollack, _Some recent logical frameworks_ (2010) ([pdf](http://homepages.inf.ed.ac.uk/rpollack/export/canonicalLF_talk.pdf))

* [[UF-IAS-2012]], _[Logical frameworks](http://uf-ias-2012.wikispaces.com/Logical+Frameworks)_.

* [[Bob Harper]], _[Notes on logical frameworks](http://uf-ias-2012.wikispaces.com/file/view/lf.pdf)_
 {#Harper}

[[!redirects logical frameworks]]
