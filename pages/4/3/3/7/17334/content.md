##Idea

The intrinsic and extrinsic views of typing correspond to different interpretations of types, also known as the contrast between "types &#224; la Church" and "types &#224; la Curry".

Reynolds claims ([Rey00](#Rey00)),

>There are two very different ways of giving denotational semantics to a programming language (or other formal language) with a nontrivial type system. In an intrinsic semantics, only phrases that satisfy typing judgements have meanings. Indeed, meanings are assigned to the typing judgements, rather than to the phrases themselves, so that a phrase that satisfies several judgements will have several meanings.

>In contrast, in an extrinsic semantics, the meaning of each phrase is the same as it would be in a untyped language, regardless of its typing properties. In this view, a typing judgement is an assertion that the meaning of a phrase possesses some property.

>The terms "intrinsic" and "extrinsic" are recent coinages by the author ([Rey88, Chapter 15](#Rey88)), but the concepts are much older. The intrinsic view is associated with Alonzo Church, and has been called "ontological" by Leivant ([Lev86](#Lev86)). The extrinsic view is associated with Haskell Curry, and has been called "semantical" by Leivant.

According to Melli&#232;s and Zeilberger ([MZ13](#MZ13)),

>One of the difficulties in giving a clear mathematical definition of the "topic" of type theory is that the word "type" is actually used with two very different intuitive meanings and technical purposes in mind:

> 1. Like the syntactician's parts of speech, as a way of defining the grammar of well-formed expressions.
> 1. Like the semanticist's predicates, as a way of identifying subsets of expressions with certain desirable properties.

>These two different views of types are often associated respectively with Alonzo Church and Haskell Curry (hence "types &#224; la Church" and "types &#224; la Curry"), while the late John Reynolds referred to these as the intrinsic and the extrinsic interpretations of types ([Rey00](#Rey00)). In the intrinsic view, all expressions carry a type, and there is no need (or even sense) to consider the meaning of "untyped" expressions; while in the extrinsic view, every expression carries an independent meaning, and typing judgments serve to assert some property
of that meaning.

###Related concepts
* [[coercion]]

###References

* {#Rey88} [[John Reynolds]], _Theories of Programming Languages_. Cambridge University Press, Cambridge, England, 1998.
* {#Lev86} [[Daniel Leivant]], _Typing and computational properties of lambda expressions_, Theoretical Computer Science, 44(1):51&#8211;68, 1986.
* {#Rey00} [[John Reynolds]], _The Meaning of Types: from Intrinsic to Extrinsic Semantics_, BRICS Report RS-00-32, Aarhus University, December 2000. [pdf](http://www.cs.cmu.edu/afs/cs/user/jcr/ftp/typemeaning.pdf)
* {#MZ13} [[Paul-André Melliès]], [[Noam Zeilberger]], _Type refinement and monoidal closed bifibrations_, [ arXiv:1310.0263](http://arxiv.org/abs/1310.0263)

Attempts to bring both views together in a theory of [[type refinement]]:

* [[Frank Pfenning]], _Church and Curry: Combining Intrinsic
and Extrinsic Typing_, [pdf](https://www.cs.cmu.edu/~fp/papers/andrews08.pdf)
* [[Paul-André Melliès]], [[Noam Zeilberger]], _Functors are Type Refinement Systems_, ([pdf](http://noamz.org/papers/funts.pdf))

[[!redirects intrinsic type]]
[[!redirects extrinsic type]]
[[!redirects intrinsic types]]
[[!redirects extrinsic types]]