# Fuzzy logic

* table of contents
{: toc}

## Idea 

Fuzzy logic is a form of [[logic]] in which the [[truth values]] are [[real numbers]] in the [[closed space|closed]] [[interval]] between 0 and 1. It is used to  model vagueness or uncertainty, partial truths, and imprecise information. 

## Examples

### T-norm fuzzy logics

One class of fuzzy logics is the class of **[[t-norm]] fuzzy logics**. In this class, one starts by equipping the interval $[0, 1]$ with a [[t-norm]] structure 

$$\otimes\colon [0, 1] \times [0, 1] \to [0, 1],$$ 

thought of as playing a role analogous to [[logical conjunction]] (but not requiring the condition of idempotence), such that $t \otimes -\colon [0, 1] \to [0, 1]$ is left [[continuous function|continuous]] for any $t \in [0, 1]$. 

Left continuity is equivalent to the condition that $t \otimes -$ preserves [[suprema]]. By the [[adjoint functor theorem]] for posets, this implies that $t \otimes -$ has a [[right adjoint]] $t \Rightarrow -\colon [0, 1] \to [0, 1]$, or in other words that 

$$a \otimes b \leq c\;\;\; \Leftrightarrow\;\;\; a \leq b \Rightarrow c.$$ 
By considering the case $a = (b \Rightarrow c)$, one then easily derives the corresponding law of [[modus ponens]], $(b \Rightarrow c) \otimes b \leq c$. 

The resulting binary operation $\Rightarrow$ is often referred to in the literature as a *residuum* associated with $\otimes$. In alternative language, this class of "fuzzy logics" is identified with the class of commutative [[quantale]] structures on $[0, 1]$. 

Many examples of fuzzy logics are t-norm fuzzy logics, including [[basic fuzzy logic]], [[monoidal t-norm logic]], [[Gödel logic]], [[Łukasiewicz logic]], and [[product fuzzy logic]]. 

## Related entries

- [[Gödel logic]]

## References

* Stanford Encyclopedia of Philosophy, [Fuzzy Logic](https://plato.stanford.edu/entries/logic-fuzzy/)

* Wikipedia, [Fuzzy logic](https://en.wikipedia.org/wiki/Fuzzy_logic) 

* [[Michael Barr]], Fuzzy set theory and topos theory, Canad. Math. Bull. Vol. 29 (4), 1986. [(pdf)](https://www.math.mcgill.ca/barr/papers/fuzzy.pdf)

[[!redirects fuzzy logic]]