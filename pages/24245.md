
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The [[syntax]] for [[h-set|sets in]] [[homotopy type theory]] behaves a lot like the [[internal language]] of a [[topos]].

## Internal ##

Chapter 10 in the [[HoTT book]] and [RijkeSpitters](#RijkeSpitters) make this precise. [[Set]] is a [[ΠW-pretopos|$\Pi$W-pretopos]]. Assuming the resizing axiom, [Set]] is actually a [[topos]]. These arguments don't quite work in the absence of [[type universes]], because they use so-called large elimations --- recursively defined functions into a universe. But one can augment [[higher inductive type|(H)]][[inductive type|ITs]] in a universeless theory by special rules for large elims --- in the HIT case, replacing paths in the universe by the equivalences that would correspond to them by univalence -- and then the arguments go through.

## Semantics ##

If all types are sets, we cannot have very many univalent universes. Moreover, not all 1-toposes even contain non-univalent universes (beyond Prop). So we need a version of dependent type theory with a separate judgment "A is a type" that is not identified with "A:U for some universe U". Then we need to assume function extensionality explicitly, since we don't have univalence to derive it from, and we can assume a univalent Prop with resizing. At this point (and without any (H)ITs) we have a theory that's almost just a notational variant of iHOL, hence corresponds very closely to elementary 1-toposes. (In this case the coherence issues are solvable, because the only universe Prop is already strict.) Adding ordinary inductive types corresponds to requiring the topos to have a NNO -- it's known that all inductive types can be constructed from a NNO in a topos.

However, now there is a problem on the other side: not every elementary topos with NNO admits *all* large elims. For instance, with a large elim over nat you can construct [beth-omega](https://en.wikipedia.org/wiki/Beth_number#Beth_omega), which is known not to exist in all toposes (e.g. models of Zermelo set theory). One can  construct large elims "categorically" out of something else by using replacement and separation axioms, however, it's not clear how to express in type theory.

Moreover, with HITs the problem is even worse: even replacement and separation don't suffice. Using HITs we can construct uncountable regular cardinals, whereas (possibly assuming some large cardinal property) there are toposes satisfying replacement and separation (namely, certain models of ZF) in which all uncountable cardinals are singular. (we should check whether this construction requires large elims, but at the least, even without large elims, it's certainly not clear how one might show that every elementary topos admits HITs).

## See also

* [[model of type theory in an (infinity,1)-topos]].

* [[Set]]

### References ###

* {#RijkeSpitters} [[Egbert Rijke]] and [[Bas Spitters]], _Sets in homotopy type theory_ $[$[arXiv:1305.3835](http://arxiv.org/abs/1305.3835)$]$ special issue "From type theory and homotopy theory to univalent foundations" of MSCS.


[[!redirects semantics of Set in homotopy type theory]]

