{: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}

###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### non-archimedean geometry
+--{: .hide}
[[!include non-archimedean geometry - contents]]
=--
=--

#Contents#
* table of contents
{:toc}

## Overview

p-adic _Hodge theory_ is the study of properties of p-adic (&#233;tale, de Rham, logarithmic cristalline) [[cohomology]] (and [[motives]]) of [[non-archimedean varieties]]. The p-adic Hodge structure of a (proper or semi-stably compactified) p-adic analytic variety is essentially given by a relation between three important invariants of the given variety:

* p-adic de Rham cohomology equipped with the Hodge filtration,

* log-cristalline cohomology (of a potentially semi-stable model) equipped with its Frobenius and monodromy map,

* [[pro-étale cohomology]] of the extension of the given variety to a `chosen` algebraic closure of the base field, together with its natural action of the Galois group.

There is an "evident" isomorphism between p-adic de Rham cohomology and log-cristalline cohomology (both are given by a kind of differential calculus).

The main theorem of p-adic Hodge theory is that the datum of these two cohomologies and their relation
on the one side, and of pro-&#233;tale cohomology on the other side, mutually determine each other (once
equipped with their natural additional structures).

This result has been conjectured first by Grothendieck in the case of p-divisible
groups. He called it the `mysterious functor`. A conjecture generalizing this
statement to other kinds of ---algebraic--- p-adic varieties was formulated by
Jannsen in a particular case, and then grounded on the setting of [[p-adic periods]]
by Fontaine. After these important Breakthrough, the theory was fully developed by a long list of contributors (see `periodes p-adiques`, Ast&#233;risque for a first list). The comparison theorem was proved by many Authors in various particular cases, and then in full generality (for algebraic varieties) by Faltings
using [[almost mathematics]].

During the last few years, there were interesting new developments.

If one works with rational coefficients (no torsion), one may get the isomorphism between both
structures in a geometric way (in an algebraic setting),
using Beilinson's approach, through (derived de Rham cohomology)[[de Rham complex]].

It is also possible to use Scholze's [[perfectoid spaces]]
and Faltings' [[almost mathematics]] to give a very elegant
proof of this theorem for proper (or more generally, semi-stably compactified) p-adic
(strict, i.e., rigid analytic) analytic varieties. The fact that the classical result extends
to the analytic setting is essentially due (up to resolution of singularities difficulties, that are
dealt with using Faltings' methods) to the fact that (proper) rigid analytic varieties always
have an integral model, given by a formal scheme over the ring of integers of the given
non-archimedean field.
The same proof may also extend to the non-strict situation by using a convenient base
extension, but this work has not yet been done.

The very important case of torsion coefficients has also been
addressed by Scholze in his setting, and by Bhatt, who gave a useful refinement
of Beilinson's construction.

Remark that Scholze's method involve the use of Witt vectors (already used in
Fontaine's definition of period rings), that were also
studied by Kedlaya and Liu in this Hodge theoretic context. This Witt vector
approach are interesting, but they seem to have the drawback of being
quite hard to globalize (including the archimedean norm in a context of
[[global Hodge theory]]).

It is quite clear to the experts that a nice way to overcome the difficulties that appear
when one uses Witt vectors would be to combine directly the (analytic) `derived de Rham`
approach of Beilinson and Bhatt to the `perfectoid and almost mathematics` approach of
Faltings and Scholze. Both approach may be extended to the analytic setting using
overconvergent derived analytic spaces (see [[global analytic geometry]]).

Indeed, as explained by Bhatt at the end of his paper, one may use derived de Rham cohomology
over $\Z$ to get a (non-archimedean) period ring isomorphism for an [[arithmetic variety]].

## (Very) short list of references