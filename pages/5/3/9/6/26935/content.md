
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

\tableofcontents

## Idea

In [[constructive mathematics]], **Brouwer's continuity principle** ([Shulman 2018](#Shulman18)) states that all [[endofunctions]] on the (Dedekind) [[real numbers]] are [[pointwise continuous functions]]. It is inconsistent with [[excluded middle]] because excluded middle implies the [[analytic LPO]], from which one can construct the discontinuous [[floor]] and [[ceiling]] functions on the real numbers, contradicting Brouwer's continuity principle. 

Brouwer's continuity principle holds in Johnstone's [[topological topos]]. It also holds for the cohesive types in [[real-cohesive homotopy type theory]], which has semantics in the [[cohesive infinity-topos]] of [[Euclidean-topological infinity-groupoids]]. 

## Variants

There are a few different continuity principles which are sometimes called Brouwer's continuity principle. 

* One of them states that all functions from the [[Baire space]] $\mathbb{N}^\mathbb{N}$ to the natural numbers are continuous. 

* Another one states that all functions from the [[Cantor space]] $\mathbb{2}^\mathbb{N}$ to the natural numbers are continuous. 

* More generally, one can postulate similar Brouwer's continuity principles for any set $X$ and any notion of continuity (i.e. [[pointwise continuity]], [[uniform continuity]], [[Lipschitz continuity]], etc). 

### Untruncated versions

In the definitions of the different notions of continuous function one sees the phrase "there exist", which is usually represented by the [[existential quantifier]]. In [[dependent type theory]] one can instead use the [[dependent sum type]], resulting in untruncated versions of Brouwer's continuity principles. Due to the [[type theoretic principle of choice]] (i.e. the fact that dependent sum types distribute over dependent product types), this means that each continuous function comes with a choice of modulus of continuity in the untruncated versions of Brouwer's continuity principles. 

* The statement that all functions from the [[Baire space]] $\mathbb{N}^\mathbb{N}$ to the natural numbers have a choice of modulus of pointwise continuity is inconsistent. 

* The statement that all functions from the [[Cantor space]] $\mathbb{2}^\mathbb{N}$ to the natural numbers have a choice of modulus of uniform continuity is equivalent to the statement that functions from the [[Cantor space]] to the natural numbers are uniformly continuous (i.e. the untruncated and truncated versions are equivalent to each other). 

## Related concepts

* [[continuous function]]

* [[analytic LPO]]

* [[Kreisel-Lacombe-Shoenfield-Tseitin theorem]]

## References

* {#EscardoXu15} [[Martin Escardo]], Chuangjie Xu, _The inconsistency of a Brouwerian continuity principle with the Curry--Howard interpretation_, 13th International Conference on Typed Lambda Calculi and Applications (TLCA 2015), Leibniz International Proceedings in Informatics (LIPIcs) *38* (2015) &lbrack;[doi:10.4230/LIPIcs.TLCA.2015.153](https://doi.org/10.4230/LIPIcs.TLCA.2015.153), [pdf](http://www.cs.bham.ac.uk/%7Emhe/papers/escardo-xu-inconsistency-continuity.pdf)&rbrack;

* {#Shulman18} [[Mike Shulman]], *Brouwer’s fixed-point theorem in real-cohesive homotopy type theory*, Mathematical Structures in Computer Science Vol 28 (6) (2018): 856-941 &lbrack;[arXiv:1509.07584](https://arxiv.org/abs/1509.07584), [doi:10.1017/S0960129517000147](https://doi.org/10.1017/S0960129517000147)&rbrack;

* {#Grossack24} [[Chris Grossack]], *Life in Johnstone's Topological Topos 3 -- Bonus Axioms* ([web](https://grossack.site/2024/07/03/topological-topos-3-bonus-axioms))

The [[elementary topos]] which appears in the following paper satisfies Brouwer's continuity principle for the [[Dedekind real numbers]], as indicated in theorem 7.7 of the paper, except that there it is called the "KLST theorem": 

* {#BauerHanson} [[Andrej Bauer]], [[James Hanson]], *The Countable Reals* ([arXiv:2404.01256](https://arxiv.org/abs/2404.01256))

[[!redirects Brouwer's theorem]]

[[!redirects Brouwer's continuity principle]]
[[!redirects Brouwer's continuity axiom]]

[[!redirects continuity principle]]
[[!redirects continuity axiom]]