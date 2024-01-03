
# Streams
* table of contents
{: toc}

## Idea

There are two notions of *stream* in use, as an [[infinite]] [[sequence]] or as a potentially infinite list. 

Accounts which take streams to be...

* infinite sequences: [Rutten05](#Rutten05), [ACS15](#ACS15)

* potentially infinite list: [Jacobs16](#Jacobs16)

## Definitions

### Explicit definitions

Let $A$ be a [[set]]. Then 

* the set of streams of $A$ in the sense of infinite sequences is the set of functions $A^\mathbb{N}$ from the [[natural numbers]] to $A$

* the set of streams of $A$ in the sense of potentially infinite list $A_*$ is 

  * the disjoint union of the set $A^\mathbb{N}$ of infinite sequences in $A$ and the set $A^* \coloneqq \biguplus_{n \in \mathbb{N}} A^n$ of finite lists $A$. 

  * the set of all infinite sequences of the disjoint union $A \uplus \{*\}$ such that $a_{i + 1} = *$ if $a_i = *$ for any natural number $i$. Finite lists are identified with a finite list of elements of $A$ followed by all $*$s, while infinite sequences is identified with a sequence of all elements of $A$. 

$$A_* \coloneqq \{a \in (A \uplus \{*\})^\mathbb{N} \vert \forall i \in \mathbb{N}.(a_i = *) \implies (a_{i + 1} = *)\}$$

In [[constructive mathematics]] only the second definition of potentially infinite list is a valid definition of stream. In [[dependent type theory]], the two definitions of potentially infinite list also make sense

$$A_* \coloneqq \mathbb{N} \to A + \sum_{n:\mathbb{N}} (\mathrm{Fin}(n) \to A)$$

$$A_* \coloneqq \sum_{a:\mathbb{N} \to (A + 1)} \prod_{i:\mathbb{N}} (a(i) = \mathrm{inr}(*)) \to (a(i + 1) = \mathrm{inr}(*))$$

but if the type $A$ is not a set, $A_*$ will not be a [[set]] either. 

### Coalgebraic definitions

Let $A$ be a [[set]] (or [[object]] of any [[category]] $C$ where the following makes sense). Then 

* the set of streams of $A$ in the sense of infinite sequences is the final coalgebra of the endofunctor $X \mapsto A \times X$. 

* the set of streams of $A$ in the sense of potentially infinite sequences is the final coalgebra of the endofunctor $X \mapsto 1 + A \times X$. 

## Examples

* An [[extended natural number]] is an element of $1_*$ (much as a [[natural number]] is an element of $1^*$).  Classically, such an element is either a [[natural number]] or [[infinity]] (the unique element of $1^{\mathbb{N}}$).

## Related concepts

* [[writer monad]]

* [[cofree coalgebra]]

## References

* {#Rutten05} [[Jan Rutten]], *A coinductive calculus of streams*, Mathematical Structures in Computer Science, Mathematical Structures in Computer Science, Volume 15, Issue 1, February 2005, pp. 93-147 ([doi:10.1017/S0960129504004517](https://doi.org/10.1017/S0960129504004517))

* {#ACS15} [[Benedikt Ahrens]], [[Paolo Capriotti]], [[Régis Spadotti]], *Non-wellfounded trees in Homotopy Type Theory*, in 13th International Conference on Typed Lambda Calculi and Applications (TLCA 2015). Leibniz International Proceedings in Informatics (LIPIcs), Volume 38, pp. 17-30, Schloss Dagstuhl - Leibniz-Zentrum für Informatik (2015) ([doi:10.4230/LIPIcs.TLCA.2015.17](https://doi.org/10.4230/LIPIcs.TLCA.2015.17), [arXiv:1504.02949](https://arxiv.org/abs/1504.02949))

* {#Jacobs16} [[Bart Jacobs]], *Introduction to Coalgebra Towards Mathematics of States and Observation*, Cambridge Tracts in Theoretical Computer Science. Cambridge: Cambridge University Press; 2016:i-iv. (ISBN:9781316823187, [doi:10.1017/CBO9781316823187](https://doi.org/10.1017/CBO9781316823187))

[[!redirects stream]]
[[!redirects streams]]
