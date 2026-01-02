
#Contents#
* table of contents
{:toc}

## Idea


**Synthetic guarded domain theory** (SGDT), is a field of [[synthetic mathematics]] that provides an alternative to [[synthetic domain theory]], where all [[guarded recursion|guarded recursive]] definitions have (guarded) [[fixed points]]. 

More generally, the aim of [[synthetic domain theory]] is roughly that computability should be built in the logic. As a result, constructions on domains would be set-theoretic with no extra structure and proofs of continuity are for free. 
However, such a theory would yield an unrestricted fixed-point combinator at all types which would render the theory itself inconsistent when viewed as a logical system. 

SGDT solves this problem by introducing a notion of "time". For a type $A$, $\triangleright A$ is the type of computations available one step from now. 
The $\triangleright$ modality (pronounced "later") yields a restricted fixed-point operator 

$$\text{fix} : (\triangleright A \to A) \to A$$

at all types $A$, which is consistent when viewing this theory as a logical framework. In particular, it corresponds to [[Löb's theorem]].

## A model of SGDT 

The original model of (single-clock) SGDT is the category of  [[presheaves]] over $\omega$, the first infinite [[ordinal]]. The objects of this category, also known as the [[topos of trees]], here named $\mathcal{S}$, are contravariant set-valued functors $X : \omega^{\text{op}} \to \text{Set}$ which have  the following shape 

$$X(0) \xleftarrow{r_0} X(1)\xleftarrow{r_1}  \dots \xleftarrow{r_{n-1}} X(n)\xleftarrow{r_{n}} \dots $$

where the maps $r_i$, for $i \in \omega^{\text{op}}$, are the restriction maps induced by the functor $X$. The arrows of this category are natural transformations between two functors (satisfying the naturality condition).

The later modality $\triangleright$ is an endofunctor in this category defined as $\triangleright A (0) = 1$ and $\triangleright A (n+1) = A(n)$, for an object $A$. Furthermore, for every object $X$ there exists an obvious map $\text{next} : X\to \triangleright X$ witnessing the fact that everything that is available now is also available later. 

Inspired by terminology used in the metric spaces (see below), every map $X \to X$ in $\text{Set}^{\omega^\text{op}}$ is called *non-expansive* while a map $f : X \to X$ is *contractive* if it factors through the $\text{next}$ map, i.e. there exists a map $g : \triangleright X \to X$ such that $f = g \circ \text{next}$. 

### Fixed-point construction
A $\triangleright$-algebra $(X, f)$ yields a natural transformation with components $f_0 : 1 \to X(0)$ and $f_i : X(i) \to X(i+1)$ commuting with the restriction maps of the object $X$. 
It can therefore be thought of as an $\omega$-chain as follows 

$$1 \xrightarrow{f_0} X(0) \xrightarrow{f_1} X(1)  \dots \to X(n) \dots $$

The morphism $\text{fix}_f : 1 \to X$ is itself a natural transformation whose components are $f_0 \circ f_1 \circ \dots f_{i-1} \circ f_{i} : 1 \to X(i)$, for all $i \in \omega^{\text{op}}$ satisfying 

$$\text{fix}_f = f \circ \text{next} \circ (\text{fix}_f)$$

The idea here is that the recursive call is **guarded** by the $\text{next}$ map. 

### Relation with metric spaces
The category of [[complete space|complete]] bisected [[metric space|ultrametric spaces]] (BiCUlt) is a [[coreflective subcategory]] of the topos of trees ([Proposition 5.1](#BMSS2012)). 

$$
  \text{BiCUlt}
    \underoverset
      {\underset{}{\leftarrow}}{\overset{\iota}{\hookrightarrow}}{\bot }
  \mathcal{S}
$$

Moreover, the inclusion functor restricts to an [[equivalence of categories]] when considering objects in $\mathcal{S}$ whose restriction maps are surjective, which are sometimes called the total objects or [[flabby sheaves]]. 

First, recall that every point in a ball $\mathcal{B}$ of an ultrametric space is at its centre while intersecting balls are contained into each other which  means that closed $2^{-n}$-balls partition a space. 
Thus, we can partition a metric space $(X, d)$ by defining a family of equivalence relation 

$$x =_n y \Leftrightarrow d(x,y) \le 2^{-n}$$

for all $n \in \mathbb{N}$. This family is also known as Complete Ordered Family of Equivalences  (c.o.f.e) [(Di Gianantonio and Miculan, 2003)](#GianantonioM03). 
Intuitively, $x$ and $y$ are equal at $n$ if they belong to the same $2^{-n}$-ball. 

The inclusion functor $\iota: \text{BiCUlt} \hookrightarrow \mathcal{S} $ takes a metric space $(X,d)$ in CBUlt into the presheaf of its space decompositions

$$(X/=_1) \leftarrow (X/=_2) \leftarrow  \dots \leftarrow (X/=_n) \leftarrow \dots $$

where each restriction map $(X/=_{(n+1)}) \to (X/=_{n})$ takes a $2^{-(n+1)}$-ball to the $2^{-n}$-ball that contains it. 

The inclusion functor has a right adjoint $\mathcal{S} \to \text{BiCUlt}$ which maps a presheaf $X$ to the homset $\mathcal{S}(1, X)$ (the global elements of $X$). This is also the limit of $X$ when seen as a diagram in **Set**. 
The metric on $\mathcal{S}(1, X)$ is defined as 

$$d(x,y) =  \bigsqcap \{ 2^{-n} \mid \forall i \lt n . x_j(\star)  = y_j(\star)  \}$$

for natural transformations $x, y : 1 \to X$. Intuitively, this metric is the greatest lower bound on which the elements of $X$ agree.

A summary of these results can be found in Bizjak's Ph.D. thesis ([Bizjak 16, Section 1.2](#Bizjak16)).

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

* {#PalombiSterling22} Daniele Palombi and [[Jonathan Sterling]], _Classifying topoi in synthetic guarded domain theory: The universal property of multi-clock guarded recursion_. Mathematical Foundations of Program Semantics 2022 ([doi](https://doi.org/10.48550/arXiv.2210.04636))

* {#Paviotti16} Marco Paviotti, _Denotational semantics in Synthetic Guarded Domain Theory_. PhD thesis, IT University of Copenhagen ([pdf](https://mpaviotti.github.io/assets/papers/paviotti-phdthesis.pdf))

* {#Bizjak16} Aleš Bizjak, _On Semantics and Applications of Guarded Recursion_. PhD thesis, Aarhus University ([pdf](https://abizjak.github.io/documents/thesis/semantics-applications-gr.pdf))

* {#GianantonioM03} Pietro Di Gianantonio, Marino Miculan, _A Unifying Approach to Recursive and Co-recursive Definitions. In Geuvers, Wiedijk, editors, Proceedings of TYPES’02. LNCS 2646, 2003.

* {#guardedcubical} [Guarded Cubical Agda ](https://agda.readthedocs.io/en/latest/language/guarded-cubical.html)

* [[Jonathan Sterling]], [Bibliography of Guarded Domain Theory](https://www.jonmsterling.com/jms-005S.xml)


[[!redirects guarded domain theory]]