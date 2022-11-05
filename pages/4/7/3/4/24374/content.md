
#Contents#
* table of contents
{:toc}

## Idea

**Synthetic guarded domain theory**(SGDT), is a field of [[synthetic mathematics]] that provides an alternative to [[synthetic domain theory]], where all [[guarded recursion|guarded recursive]] definitions have [[fixed points]]. 

More generally, the aim of [[synthetic domain theory]] is roughly that computability should be built in the logic. As a result, constructions on domains would be set-theoretic with no extra structure and proofs of continuity are for free. 
However, such a theory would yield an unrestricted fixed-point combinator at all types which would render the theory itself inconsistent when viewed as a logical system. 

SGDT solves this problem by introducing a notion of "time". For a type $A$, $\triangleright A$ is the type of computations available one step from now. 
The $\triangleright$ modality (pronounced "later") yields a restricted fixed-point operator 
$$\text{fix} : (\triangleright A \to A) \to A$$ 
at all types $A$, which is consistent when viewing this theory as a logical framework. In particular, it corresponds to [[Löb's theorem]].

## A model of SGDT 
Categorically, SGDT lives in the category of  [[presheaves]] over $\omega$, the first infinite [[ordinal]]. The objects of this category, also known as the [[topos of trees]], are contravariant set-valued functors $X : \omega^{\text{op}} \to \text{Set}$ which have  the following shape 
$$X(1) \xleftarrow{r_1} X(2)\xleftarrow{r_2}  \dots \xleftarrow{r_{n-1}} X(n)\xleftarrow{r_{n}} \dots $$
where the maps $r_i$, for $i \in \omega^{\text{op}}$, are the restriction maps induced by the functor $X$. The arrows of this category are natural transformations between two functors (satisfying the naturality condition).

The later modality $\triangleright$ is an endofunctor in this category defined as $\triangleright A (1) = 1$ and $\triangleright A (n+1) = A(n)$, for an object $A$. Furthermore, for every object $X$ there exists an obvious map $\text{next} : X\to \triangleright X$ witnessing the fact that everything that is available now is also available later. 

### Fixed-point construction
A $\triangleright$-algebra $(X, f)$ yields a natural transformation with components $f_1 : 1 \to X(1)$ and $f_i : X(i) \to X(i+1)$ commuting with the restriction maps of the object $X$. 
It can therefore be thought of as an $\omega$-chain as follows 
$$1 \xrightarrow{f_1} X(1) \xrightarrow{f_2} X(2)  \dots \to X(n) \dots $$

The morphism $\text{fix}_f : 1 \to X$ is itself a natural transformation whose components are $f_1 \circ \dots f_{i-1} \circ f_{i} : 1 \to X(i)$, for all $i \in \omega^{\text{op}}$ satisfying 
$$\text{fix}_f = f \circ \text{next} \circ (\text{fix}_f)$$

The idea here is that the recursive call is **guarded** by the $\text{next}$ map. 

### Relation with the metric spaces
The category of [[complete space|complete]], bisected, [[metric space|ultrametric spaces]] is a full subcategory of the topos of trees spanned by [[flabby objects]] ([Proposition 5.1](#BMSS2012), there called "total" objects).

Inspired by terminology used in the metric spaces, every map $A \to A$ in $\text{Set}^{\omega^\text{op}}$ is non-expansive while maps of type $\triangleright A \to A$, or $\triangleright$-algebras, are called a contractive maps. 

## Axiomatics
[Palombi and Sterling](#PalombiSterling22) provide the following simple axiomatization of a model of (single-clock) synthetic guarded domain theory:

1. An [[elementary topos]] $E$ with [[natural numbers object]].

2. with a [[left exact]] [[endofunctor]] $\triangleright$ 

3. with a [[natural transformation]] $\text{next} 
\;\colon\; 1 \to \triangleright$ satisfying $\triangleright\text{next} = \text{next}\triangleright$

4. supporting [[Löb's theorem|Löb-induction]], i.e., $\phi : \Omega|\triangleright \phi \Rightarrow \phi \vdash \phi$ in the [[internal logic]] of $E$.

Then "multi-clock" SGDT is simply a topos $E$ with an object of clocks $K \colon E$ such that the [[slice topos|slice]] $E/K$ is a [[model]] of single-clock SGDT.

## Type Theory

Mathematics in synthetic guarded domain theory can be formalized in the [[internal language]] of SGDT models. Several presentations have been proposed such as:

* *guarded dependent type theory* ([BGCMB2016](#BGCMB2016)) which is an [[extensional type theory]] 

* *clocked cubical type theory* ([KMV2022](#KMV2022)), an [[intensional type theory]] extending [[cubical type theory]]. 

[[Agda]] includes an implementation of some portions of clocked cubical type theory under the name *[Guarded Cubical Agda](#guardedcubical)*.


## Related pages

* [[synthetic domain theory]]
* [[domain theory]]
* [[guarded recursion]]

## References

* {#BMSS2012} [[Lars Birkedal]], Rasmus Ejlers Møgelberg, Jan Schwinghammer, Kristian Støvring, _First steps in synthetic guarded domain theory: step-indexing in the topos of trees_.  Logical Methods in Computer Science **8** 4 (2012)   &lbrack;<a href="https://doi.org/10.2168/LMCS-8(4:1)2012">doi:10.2168/LMCS-8(4:1)2012</a>&rbrack;

* {#BGCMB2016} Aleš Bizjak, Hans Bugge Grathwohl, Ranald Clouston, Rasmus E. Møgelberg, Lars Birkedal. _Guarded Dependent Type Theory with Coinductive Types_. FoSSaCS 2016 ([doi](https://doi.org/10.1007/978-3-662-49630-5_2))

* {#KMV2022} Magnus Baunsgaard Kristensen, Rasmus Ejlers Møgelberg, Andrea Vezzosi _Greatest HITs: Higher inductive types in coinductive definitions via induction under clocks_. LICS 2022 ([preprint](https://arxiv.org/abs/2102.01969))

* {#PalombiSterling22} Daniela Palombi and [[Jonathan Sterling]], _Classifying topoi in synthetic guarded domain theory: The universal property of multi-clock guarded recursion_. Mathematical Foundations of Program Semantics 2022 ([preprint](https://www.jonmsterling.com/papers/palombi-sterling:2022.pdf))

* {#Paviotti16} Marco Paviotti, _Denotational semantics in Synthetic Guarded Domain Theory_. PhD thesis, IT University of Copenhagen ([pdf](https://mpaviotti.github.io/assets/papers/paviotti-phdthesis.pdf))

* {#guardedcubical} [Guarded Cubical Agda ](https://agda.readthedocs.io/en/latest/language/guarded-cubical.html)

* [[Jonathan Sterling]], [Bibliography of Guarded Domain Theory](https://www.jonmsterling.com/gdt-bibliography.html)