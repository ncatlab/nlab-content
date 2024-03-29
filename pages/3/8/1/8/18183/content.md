# Refutation by contradiction
* table of contents
{:toc}

## Idea

*Refutation by contradiction* is the "basic" method of [[formal proof]] for proving a [[negation]]: if assuming $P$ leads to a [[contradiction]], then we conclude $\neg P$.  It is the [[introduction rule]] for the [[connective]] of [[negation]] in [[intuitionistic logic]]; if $\neg P$ is defined as $P\to \bot$ (the [[function type]] from $P$ to [[false]]), then it follows from the introduction rule for [[implication]].

Refutation by contradiction is also called *proof of negation*, but this can be confusing because there may be other "indirect" ways to prove a negation.

Rarely one finds logics that have a basic notion of "refutation of $A$" that is distinct from (though generally closely related to) a "proof of $\neg A$" [(Nelson 1949)](#Nelson49).  In that case, refutation by contradiction is more precisely a method of refuting $A$ by deriving a contradiction from an assumption of $A$, which might be distinguished from other more "direct" ways of refuting $A$ (for example, a refutation of a [[universal quantifier|universally quantified]] statement $\forall x.B(x)$ that exhibits an explicit counterexample, i.e., a term $t$ together with a refutation of $B(t)$).

## Related concepts

* [[proof by contradiction]]

## References

* {#bauer} [[Andrej Bauer]], _[Proof of negation and proof by contradiction](http://math.andrej.com/2010/03/29/proof-of-negation-and-proof-by-contradiction/)_ 2010

* {#Lopez-Escobar72} E. G. K. L&#243;pez-Escobar, _Refutability and Elementary Number Theory_ , Indag. Math. **34** 1972 pp.362-374.

* {#Nelson49} David Nelson, Constructible Falsity, _The Journal of Symbolic Logic_, Vol. 14, No. 1 (Mar., 1949), pp. 16-26. ([jstor](http://www.jstor.org/stable/2268973))

[[!redirects proof of negation]]
