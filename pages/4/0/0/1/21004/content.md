

\tableofcontents

## Idea 

*Fuzzy logic* is an algebraic form of [[logic]] in which the [[truth values]] are [[real numbers]] in the [[closed space|closed]] [[interval]] between 0 and 1. It has been proposed as a way to model vagueness or uncertainty, partial truths, and imprecise information. 

One proposed application is to resolve [[paradoxes]] of Sorites type. For example, the proposition "if $n$ is a very large number, then so is $n-1$" does not stand scrutiny if there is a sharp true-false distinction between "very large" and "not very large". The counter is that "very large" is inherently a fuzzy concept, steadily shading into gray as one descends from $n$ to $n-1$. 

To be properly considered "a logic", fuzzy logic should be developed into a full-fledged [[deductive system]] (with [[rules of inference]] and so on), but historically this has been a source of difficulty. See the [SEP](#SEP) for a description of what has been achieved on this front. 

It may also be questioned whether it makes sense to have degrees of certainty be [[total order|totally ordered]], as $[0, 1]$ is. Goguen for example allows consideration of [[frames]] or [[locales]] $L$ more general than $[0, 1]$, and presumably the same consideration would extend to [[quantale]] structures more general than those supported on $[0, 1]$. For some analysis of Goguen's framework, see [Barr 1986](#Barr86). 

## Examples

### T-norm fuzzy logics

One class of fuzzy logics is the class of **[[t-norm]] fuzzy logics**. In this class, one starts by equipping the interval $[0, 1]$ with a [[t-norm]] structure 

$$\otimes\colon [0, 1] \times [0, 1] \to [0, 1],$$ 

thought of as playing a role analogous to [[logical conjunction]] (but not requiring the condition of [[idempotent|idempotence]]), such that $t \otimes -\colon [0, 1] \to [0, 1]$ is left-[[continuous function|continuous]] for any $t \in [0, 1]$, i.e., such that $\underset{s \to r^-}{\lim}\; t \otimes s = t \otimes r$. 

Left continuity is equivalent to the condition that $t \otimes -$ preserves [[suprema]]. By the [[adjoint functor theorem]] for [[posets]], this implies that $t \otimes -$ has a [[right adjoint]] $(t \Rightarrow -) \,\colon\  [0, 1] \to [0, 1]$, or in other words that 

$$a \otimes b \leq c\;\;\; \Leftrightarrow\;\;\; a \leq b \Rightarrow c.$$ 
By considering the case $a = (b \Rightarrow c)$, one then easily derives the corresponding law of [[modus ponens]], $(b \Rightarrow c) \otimes b \;\leq\; c$. 

The resulting [[binary operation]] $\Rightarrow$ is often referred to in the literature as a *residuum* associated with $\otimes$. In alternative language, this class of "fuzzy logics" is identified with the class of commutative [[quantale]] structures on $[0, 1]$. 

Many examples of fuzzy logics are t-norm fuzzy logics, including [[basic fuzzy logic]], [[monoidal t-norm logic]], [[Gödel logic]], [[Łukasiewicz logic]], and [[product fuzzy logic]]. 

## Related entries

- [[Gödel logic]]

- [[fuzzy set]]

## References

* {#SEP} Stanford Encyclopedia of Philosophy, [Fuzzy Logic](https://plato.stanford.edu/entries/logic-fuzzy/)

* Wikipedia, [Fuzzy logic](https://en.wikipedia.org/wiki/Fuzzy_logic) 


In relation to [[topos theory]]:

* {#Barr86} [[Michael Barr]], *Fuzzy set theory and topos theory*, Canad. Math. Bull. **29** 4 (1986) 501-508 &lbrack;[doi:10.4153/CMB-1986-079-9](https://doi.org/10.4153/CMB-1986-079-9), [pdf](https://www.math.mcgill.ca/barr/papers/fuzzy.pdf), [[Barr-FuzzySetToposTheory.pdf:file]]&rbrack;

In relation to [[linear logic]]:

* [[Michael Barr]], *Fuzzy models of linear logic*, Math. Structures Comp. Sci. **6** 3 (1996) 301–312 &lbrack;[doi:10.1017/S096012950000102X](https://doi.org/10.1017/S096012950000102X), [pdf](https://www.math.mcgill.ca/barr/papers/fzymod.pdf), [[Barr-FuzzyLinearLogic.pdf:file]]&rbrack;


[[!redirects fuzzy logic]]