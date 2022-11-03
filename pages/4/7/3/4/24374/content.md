
#Contents#
* table of contents
{:toc}

## Idea

**Synthetic guarded domain theory**(SGDT), is a field of [[synthetic mathematics]] that provides an alternative to [[synthetic domain theory]], where all [[guarded recursion|guarded recursive]] definitions have [[fixed points]]. 

More generally, the aim of [[synthetic domain theory]] is roughly that computability should be built in the logic. As a result, constructions on domains would be set-theoretic with no extra structure and proofs of continuity are for free. 
However, such a theory would yield an unrestricted fixed-point combinator at all types which would render the theory itself inconsistent when viewed as a logical system. 

SGDT solves this problem by introducing a notion of "time". For a type $A$, $\triangleright A$ is the type of computation available one step from now. 
Categorically, SGDT lives in the category of  [[presheaves]] over $\omega$ and $\triangleright$ (pronounced "later") is an endofunctor in this category defined as $\triangleright A (1) = 1$ and $\triangleright A (n+1) = A(n)$.

The internal language of this category admits a restricted fixed-point operator 
$$(\triangleright A \to A) \to A$$ 
at all types $A$, which is consistent when viewing the types as a logic.

Inspired by terminology used in the metric spaces, every map $A \to A$ in $\text{Set}^{\omega^\text{op}}$ is non-expansive while $\triangleright$-algebras are called a contractive maps. 

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

## Models

The most basic model of SGDT is given by the [[topos of trees]], the [[category of presheaves]] on $\omega$, the first infinite [[ordinal]]. The [[topos of trees]] establishes the relationship between synthetic guarded domain theory and metric domain theory: the category of [[complete space|complete]], bisected, [[metric space|ultrametric spaces]] embeds into the topos of trees as the full subcategory spanned by [[flabby objects]] ([Proposition 5.1](#BMSS2012), there called "total" objects).


## Related pages

* [[synthetic domain theory]]
* [[domain theory]]

## References

* {#BMSS2012} [[Lars Birkedal]], Rasmus Ejlers Møgelberg, Jan Schwinghammer, Kristian Støvring, _First steps in synthetic guarded domain theory: step-indexing in the topos of trees_.  Logical Methods in Computer Science **8** 4 (2012)   &lbrack;<a href="https://doi.org/10.2168/LMCS-8(4:1)2012">doi:10.2168/LMCS-8(4:1)2012</a>&rbrack;

* {#BGCMB2016} Aleš Bizjak, Hans Bugge Grathwohl, Ranald Clouston, Rasmus E. Møgelberg, Lars Birkedal. _Guarded Dependent Type Theory with Coinductive Types_. FoSSaCS 2016 ([doi](https://doi.org/10.1007/978-3-662-49630-5_2))

* {#KMV2022} Magnus Baunsgaard Kristensen, Rasmus Ejlers Møgelberg, Andrea Vezzosi _Greatest HITs: Higher inductive types in coinductive definitions via induction under clocks_. LICS 2022 ([preprint](https://arxiv.org/abs/2102.01969))

* {#PalombiSterling22} Daniela Palombi and [[Jonathan Sterling]], _Classifying topoi in synthetic guarded domain theory: The universal property of multi-clock guarded recursion_. Mathematical Foundations of Program Semantics 2022 ([preprint](https://www.jonmsterling.com/papers/palombi-sterling:2022.pdf))

* Marco Paviotti, _Denotational semantics in Synthetic Guarded Domain Theory_. PhD thesis, IT University of Copenhagen ([pdf](https://mpaviotti.github.io/assets/papers/paviotti-phdthesis.pdf))

* {#guardedcubical} [Guarded Cubical Agda ](https://agda.readthedocs.io/en/latest/language/guarded-cubical.html)

* [[Jonathan Sterling]], [Bibliography of Guarded Domain Theory](https://www.jonmsterling.com/gdt-bibliography.html)