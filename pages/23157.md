# Complexity class
* this block creates the table of contents, leave as is
{: toc}

## Idea

In computational [[complexity theory]], many problems have similar behavior, leading to similar [[algorithm|algorithms]] for solving families of problems. Many algorithms use resources proportional to the size of their inputs. A **complexity class** is a collection of problems which all can be executed on a single type of computer with similar resource usage.

A complexity class might be defined for [[decision problem|decision problems]], which only return true-or-false answers, but there are also definitions for [[function problem|function problems]].


## Definition 

### Classical

Fix a [[type theory]] to use as a [[model of computation]]. Traditionally, we use the theory of [[Turing machine|Turing machines]]. The complexity class of this theory is the collection of all problems which can be [[decidability|decided]] by a term of the theory -- a [[program]] of the model of computation.

When the type theory is Turing-complete, then we have the complexity class [[R]]. This class is composed of all problems whose answers form a [[recursive set]].

Let a polynomial time bound on a program be a [[polynomial]] in natural numbers which takes the size of an input and returns the number of [[beta-reduction|reductions]] required to compute the output. The theory of Turing machines with at least two tapes, restricted by polynomial time bounds, is associated with the complexity class [[PTIME]]. Similarly, there are exponential time bounds, and a corresponding complexity class [[EXPTIME]].


### Descriptive

Fix a [[fragment]] of [[higher-order logic]]. A query is a predicate on finite structures which can be expressed in the fragment. The descriptive complexity class of the fragment is the collection of queries, and the size of each input is the size of the corresponding finite structure.

For the fragment of [[first-order logic]] with an added least [[fixed point]] operator, the descriptive complexity class is [[PTIME]]. Similarly, the fragment of [[second-order logic]] with a least fixed point operator gives the complexity class [[EXPTIME]].

Second-order logic with [[existential quantification]] but not [[universal quantification]] yields the complexity class [[NPTIME]].


## Properties

(...)


## Examples

The complexity class [[R]] corresponds to the height of computability according to the [[Church-Turing thesis]].

The classes [[PTIME]] and [[NPTIME]] are clearly related, but the exact details are elusive. The question of [[P vs NP]] is central to computer science.

The complexity class [[BQP]] is relevant to the field of [[quantum computation]].


## Related entries

* [[descriptive complexity theory]]
* [[timed set]]


## References

* Wikipedia, _[Complexity class](https://en.wikipedia.org/wiki/Complexity_class)_, _[P versus NP problem](https://en.wikipedia.org/wiki/P_versus_NP_problem)_
