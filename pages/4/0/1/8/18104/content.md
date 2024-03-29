
# Contents
* table of contents
{: toc}

## Idea

The method called _proof by contradiction_ is a method of [[formal proof]] using the [[principle of excluded middle]].

This principle says that for $P$ any [[proposition]], then it or its [[negation]] is [[true]]. (The 'or' here is meant internally, as a formal disjunction $P \vee \neg P$.) One also speaks of _[[classical logic]]_ if this principle is taken to hold. 

But this principle implies that in order to prove a [[proposition]] $P$ it is sufficient to show that its [[negation]] is [[false]], hence that assuming that $P$ were not true would lead to a "contradiction". This is _proof by contradiction_.

Proof by contradiction is used frequently in [[classical mathematics]].

While this method of proof is classical, it has some peculiar consequences. Notably when $P$ is an [[existential quantification|existential statement]] of the form "there exists an object $X$ with the property $Y$", then a proof of such existence by contradiction alone gives no means to actually construct an example. 

Therefore one also says that proof by contradiction is "non-constructive" and that an alternative proof not invoking the [[principle of excluded middle]] (if it exists) is a "constructive" proof, see at _[[constructive logic]]_ and _[[constructive mathematics]]_. 


## Relation to refutation by contradiction

One should take care to distinguish proof by contradiction from _[[refutation by contradiction]]_ (also called _proof of negation_), which nevertheless involves the derivation of a contradiction: assuming the truth of $P$, a contradiction is found, and one concludes that $\neg P$. This remains [[constructive mathematics|constructively]] valid, since it simply uses the constructive _meaning_ of [[negation]], i.e. the [[introduction rule]] for the connective of [[negation]] (see [Bauer 2010](#bauer)).

Since this distinction is sometimes hard for those who have learned classical logic to the point it becomes hard to unlearn, here is another way of putting it (also mentioned by Bauer): 

* A proof by contradiction is where you argue "suppose $P$ is false; then [argue blah blah blah]..., contradiction. Therefore $P$ is true. 

* A refutation by contradiction is where you argue "suppose $P$ is true; then [blah blah blah]..., contradiction. Therefore $P$ is false. 

For example, the standard proofs of the [[irrational number|irrationality]] of $\sqrt{2}$ are sometimes called proofs by contradiction, but they are actually refutations by contradiction (showing that "$\sqrt{2}$ is rational" is false).  (The usual meaning of 'irrational' in [[constructive analysis]] is actually something stronger than 'not rational', so such refutations by contradiction are not enough as they stand to prove irrationality; however, they usually can be easily strengthened to prove irrationality in the strong sense.)

 
## Related concepts

* [[formal proof]]


## References

* {#bauer} [[Andrej Bauer]], _[Proof of negation and proof by contradiction](http://math.andrej.com/2010/03/29/proof-of-negation-and-proof-by-contradiction/)_ 2010

* Wikipedia, _[Proof by contradiction](https://en.wikipedia.org/wiki/Proof_by_contradiction)_

[[!redirects proof by contradiction]]
[[!redirects proof of negation]]
[[!redirects refutation by contradiction]]