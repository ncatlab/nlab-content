
# Exclusive disjunction
* table of contents
{: toc}

## Idea

In [[propositional logic]], the __exclusive disjunction__ (also called __exclusive or__ or simply __xor__) of a family of statements ([[truth values]], [[propositions]], [[predicates]], velc) is a statement that is true if and only if exactly one of the statements in the family is true.  The corresponding operation on [[subsets]] (of a fixed set) or [[pure set|material sets]] is called _exclusive union_, and the binary operation agrees with _[[symmetric difference]]_ (which is generalised to higher arities in a different way).  If we think of [[quantifiers]] as infinitary operators, then exclusive disjunction becomes [[uniqueness quantification]].


## Definitions
 {#Definitions}

The __exclusive disjunction__ of $p$ and $q$, written $p &#8891; q$ (and a host of other ways), may be defined in any of these forms:
1.  $\neg(p \Leftrightarrow q)$,
2.  $(p \vee q) \wedge (\neg p \vee \neg q)$,
3.  $(p \wedge \neg{q}) \vee (\neg{p} \wedge q)$.

These are all equivalent in [[classical logic]].  In [[intuitionistic logic]], (2,3) are equivalent but (1) is weaker; (2,3) give the usual meaning in [[constructive mathematics]].

The [[false]] statement is the [[identity element|identity]] for this operation; it is the exclusive disjunction of no statements.

In classical logic (but not in intuitionistic logic), this operation is associative, but multiple applications don\'t mean what you may think.  Instead, $(p &#8891; q) &#8891; r \equiv p &#8891; (q &#8891; r)$ comes out true if $p, q, r$ are all true; in general,
$$ (p_1 &#8891; (p_2 &#8891; \cdots &#8891; p_n)\cdots) $$
is true if and only if an *odd* number of the statements $p_i$ is true.  But when we write a multiple statement with 'xor', we really mean that *exactly one* of the statements is true.  So by fiat, define the __exclusive disjunction__
$$ p_1 &#8891; p_2 &#8891; \cdots &#8891; p_n $$
(without parentheses) to mean that exactly one of the $p_i$ is true; this definition is also used in intuitionistic logic.

As the indexed version of ordinary [[disjunction]] is [[existential quantification]] $\exists$, so the indexed version of exclusive disjunction is [[uniqueness quantification]] $\exists!$; this requires a primitive notion of [[equality]] to state in [[predicate logic]].

Similarly, the __exclusive union__ of two sets $A$ and $B$, written $A \uplus B$ (and a host of other ways), may be defined using exclusive disjunction:
$$ A \uplus B = \{ x \;|\; x \in A \;&#8891;\; x \in B \} .$$
The __exclusive union__ of a family $(A_i)_{i\colon I}$ of sets may be defined using uniqueness quantification:
$$ \biguplus_i A_i = \{ x \;|\; \exists!{i},\; x \in A_i \} .$$

Note that the [[union]], exclusive union, and (internal, or external up to [[natural isomorphism]]) [[disjoint union]] of a family of (pairwise) [[disjoint sets]] are all the same.  For a family that is not disjoint, however, the union are exclusive union are different, the internal disjoint union does not make sense, and the external disjoint union is not isomorphic to either the union or the exclusive union (at least not naturally, and in some cases not at all).

We also have the __[[symmetric difference]]__ of two sets, which is the same as the exclusive union.  But we see this operation as the addition in a [[Boolean ring]] and so actually interpret it in the usual way as an associative operation.  So the symmetric difference of $n$ sets indeed consists of those points that belong to an odd number of sets, and there is no infinitary symmetric difference.

### In dependent type theory

In [[dependent type theory]], [[exclusive disjunction]] of two [[mere propositions]] $P$ and $Q$ is given by the statement that the [[sum type]] $P + Q$ is a [[contractible type]]:

$$P \underline{\vee} Q \coloneqq \mathrm{isContr}(P + Q)$$

This definition of exclusive disjunction also makes sense for any two [[types]] $P$ and $Q$, and guarantees that exactly one of $P$ and $Q$ is a [[contractible type]] while the other one of $P$ and $Q$ is an [[empty type]] if the exclusive disjunction $P \underline{\vee} Q$ holds. 

Since the definition of exclusive disjunction doesn't require [[propositional truncations]], it can be defined in any [[dependent type theory]] which doesn't come with any [[higher inductive types]]. 

Compare with the [[uniqueness quantifier]], which generalises from the exclusive disjunction of two propositions to the exclusive disjunction of a family of propositions. 

### Excluded middle

The exclusive disjunction can be used for the [[law of excluded middle]], saying that the exclusive disjunction of a proposition $P$ and its [[negation]] always holds:

$$P \underline{\vee} \neg P$$

## As a logic gate
 {#AsALogicGate}

Exclusive disjunction as a [[logic gate]], a [[reversible computation|reversible]] gate ([[CNOT]]) and as a [[quantum logic gate]]: 

\begin{imagefromfile}
    "file_name": "CNOTGates-221026c.jpg",
    "width": "750",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}

## In natural language

It is widely said that 'or' in English can mean either inclusive or exclusive disjunction, while Latin has two terms, respectively 'vel' and 'aut', but this is not really correct.  It\'s more correct that 'or' can sometimes mean *[[union]]* and sometimes *[[disjoint union]]* (with the latter sometimes external and sometimes internal), but never symmetric difference.  Thus, the only meaning of 'or' is for some kind of [[coproduct]], which exclusive disjunction is not.  (Similarly, 'aut' is more about disjoint union than symmetric difference.)  In some cases, exclusive disjunction may be a valid *[implicature](http://en.wikipedia.org/wiki/Implicature)* (in the sense of linguistic philosopher Paul Grice) even if the only valid *inference* (by the literal meaning of the sentence) is taken to be inclusive.

For the literature on this subject, see [the Stanford Encylopedia entry](http://plato.stanford.edu/entries/disjunction/#NatLan) and The Myth of the Exclusive 'Or' (*Mind*, 80 (317), 116--121).

## Related concepts

* [[CNOT]]

* [[logic gate]]

* [[uniqueness quantifier]]

## References

See also

* Wikipedia, *[Exclusive or](https://en.wikipedia.org/wiki/Exclusive_or)*


[[!redirects exclusive disjunction]]
[[!redirects exclusive disjunctions]]
[[!redirects exclusive disjunct]]
[[!redirects exclusive disjuncts]]
[[!redirects exclusive union]]
[[!redirects exclusive unions]]
[[!redirects exclusive or]]
[[!redirects xor]]
[[!redirects XOR]]
