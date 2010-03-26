In [[propositional logic]], the __exclusive disjunction__ (also called __exclusive or__ or simply __xor__) of a family of statements ([[truth value]]s, propositions, predicates, velc) is a statement that is true if and only if exactly one of the statements in the family is true.  The corresponding on operation on [[subset]]s (of a fixed set) or [[pure set]]s is called _exclusive union_ or _[[symmetric difference]]_, although the latter term is generalised in a different way.


## Definitions

The __exclusive disjunction__ of $p$ and $q$, written $p &#8891; q$ (and a host of other ways), may be defined in any of these forms:
1.  $\neg(p \Leftrightarrow q)$,
2.  $(p \vee q) \wedge \neg(p \wedge q)$,
3.  $(p \wedge \neg{q}) \vee (\neg{p} \wedge q)$.

These are all equivalent in [[classical logic]].  In [[intuitionistic logic]], (2,3) are equivalent but (1) is weaker; (2,3) give the usual meaning in [[constructive mathematics]].

The false statement is the [[identity element|identity]] for this operation; it is the exclusive disjunction of no statements.

In classical logic (but not in intuitionistic logic), this operation is associative, but multiple applications don\'t mean what you may think.  Instead, $(p &#8891; q) &#8891; \equiv p &#8891; (q &#8891; r)$ comes out true if $p, q, r$ are all true; in general,
$$ (p_1 &#8891; (p_2 &#8891; \cdots &#8891; p_n)\cdots) $$
is true if and only if an *odd* number of the statements $p_i$ is true.  But when we write a multiple statement with 'xor', we really mean that *exactly one* of the statements is true.  So by fiat, define the __exclusive disjunction__
$$ p_1 &#8891; p_2 &#8891; \cdots &#8891; p_n $$
(without parentheses) to mean that exactly one of the $p_i$ is true; this definition is also used in intuitionistic logic.

As the indexed version of ordinary [[disjunction]] is [[existential quantification]] $\exists$, so the indexed version of exclusive disjunction is [[uniqueness quantification]] $\exists!$; this requires a primitive notion of [[equality]] to state in [[predicate logic]].

Similarly, the __exclusive union__ of two sets $A$ and $B$, written $A \uplus B$ (and a host of other ways), may be defined using exclusive disjunction:
$$ A \uplus B = \{ x \;|\; x \in A \;&#8891;\; x \in B \} .$$
The __exclusive union__ of a family $(A_i)_{i: I}$ of sets may be defined using uniqueness quantification:
$$ \biguplus_i A_i = \{ x \;|\; \exists!{i},\; x \in A_i \} .$$

Note that the [[union]], exclusive union, and (internal, or external up to [[natural isomorphism]]) [[disjoint union]] of a family of (pairwise) [[disjoint sets]] are all the same.  For a family that is not disjoint, however, the union are exclusive union are different, the internal disjoint union does not make sense, and the external disjoint union is not isomorphic to either the union or the exclusive union (at least not naturally, and in some cases not at all).

We also have the __[[symmetric difference]]__ of two sets, which is the same as the exclusive union.  But we see this operation as the addition in a [[Boolean ring]] and so actually interpret it in the usual way as an associative operation.  So the symmetric difference of $n$ sets indeed consists of those points that belong to an *odd* number of sets; there is no infinitary symmetric difference.


## In natural language

It is widely said that 'or' in English can mean either inclusive or exclusive disjunction, while Latin has two terms, respectively 'vel' and 'aut'.  It\'s not at all clear that this is correct.  It may be more correct that 'or' can sometimes mean [[union]] and sometimes [[disjoint union]] (with the latter sometimes external and sometimes internal), but never symmetric difference.  Thus, the only meaning of 'or' is for some kind of [[coproduct]], which exclusive disjunction is not.  (Similarly, 'aut' may be more about disjoint union than symmetric difference.)  In some cases, exclusive disjunction may be a valid *[implicature](http://en.wikipedia.org/wiki/Implicature)* (in the sense of linguistic philosopher Paul Grice) even if the only valid *inference* (by the literal meaning of the sentence) is taken to be inclusive.

+-- {: .query}
What about the 'or' of parental threat? Consider the logician parent who says "Come here or I'll smack you" to his child and smacks even after obedience as they believe in the inclusive 'or'. -David

That\'s no different from 'If you don\'t come here, then I\'ll smack you.', which also suggests (but does not state) the converse.  And in fact, no parent, logician or otherwise, is actually making the promise implied by the $\neg(p \wedge q)$ clause; if the child comes to such a parent and then kicks the parent in the shin, then the parent will still smack the child.  Instead, if you *want* to make that promise, then you say 'If you come here, then I won\'t smack you.' explicitly.  This has a very different tenor (unless you say it in a wink-nudge mafia kind of way), as it\'s a promise rather than a threat.  (I know, it\'s *only* a promise, which is still different in tenor than a statement that is *both* promise and threat, as an exclusive disjunction would be.  But I still hold that your statement is *only* a threat.)  Note that a logician child who believes the parent\'s literal expression would still choose to come if avoiding smacking is the highest priority; but the reason is that refusal guarantees a smack, not that obedience necessarily avoids it.  That is why the wise child also throws in a contrite expression and an oral apology, to improve the odds.  ---Toby

I see there's a literature on the [subject](http://plato.stanford.edu/entries/disjunction/#NatLan) including "The Myth of the Exclusive 'Or'" (Mind, 80 (317), 116&#8211;121). ---David

Also:  I argued above that the meaning of 'Come here or I\'ll smack you' must be weaker than exclusive disjunction, since the parent will smack the child anyway under some circumstances.  However, I agree that it is stronger than inclusive disjunction, but that is because we may go beyond the literal meaning of the words and apply a Gricean [implicature](http://plato.stanford.edu/entries/implicature/).  To be specific, if the parent intends to smack the child regardless, then the parent should say 'I\'ll smack you' by the Maxim of Quantity, but the parent in fact said something more wordy.  Thus we conclude that the parent does not intend to smack the child if the child comes, without ruling out the possibility that the parent will still smack the child for some other reason.  ---Toby
=--

I should find the reference that argued this; it certainly did not use this terminology.


[[!redirects exclusive disjunction]]
[[!redirects exclusive union]]
[[!redirects xor]]
[[!redirects XOR]]
