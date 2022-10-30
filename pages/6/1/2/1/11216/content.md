
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
#### Constructivism, Realizability, Computability
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[computability|computable function]] is often taken to be one that acts on the [[natural numbers]] (a [[partial  recursive function]]) but for purposes of [[analysis]] ([[computable analysis]], [[exact analysis]]) and related fields (notably [[physics]], see at _[[computable physics]]_) one considers [[computation]] on [[real numbers]] to finite but arbitrary precision. This means that in this context of analysis a computable function should be an [[algorithm]] that successively reads in [[natural numbers]] from a possibly infinite list (specifying an input to ever higher accuracy) and accordingly outputs a result as incrementally as an infinite list. 

Mathematically this is captured by [[continuous functions]] on [[quotient spaces]] of [[Baire space (computability)]] and goes by the name _[[Type Two Theory of Effectivity]]_ or similar. In implementations this is essentially what is known as _[[exact real computer arithmetic]]_. 

## Definition

In [[Type Two Theory of Effectivity]] for [[computable analysis]] (see [Weihrauch 00](#Weihrauch00)) one considers the following definition:

A _representation_ of a $T_0$-[[topological space]] $X$ is a presentation of it as a [[quotient space]] of a [[subspace]] $B$ of [[irrational number|Baire space]] (the underlying space of [[Kleene's second algebra]]). See also at _[[effective topological space]]_.

Such a representation is called _admissible_ if the quotient map $B \to X$ has the [[right lifting property]] against [[continuous functions]] out of other subspaces $B'$ of Baire space.

Given representations of $X$ and $X'$ in this way, then a [[function]] $f \colon X \to X'$ is called _continuously realizable_ if there exists a [[continuous function]] $\phi \colon B \to B'$ between the corresponding subspaces of Baire space such that the evident [[commuting diagram|diagram commutes]].

For admissible representations a function $X\to X'$ is continuously realizable precisely if it is already continuous.

Write $AdmRep$ for the [[category]] of admissible representations in this sense, and continuously realizable (and hence continuous) functions between these.

## Properties

### General
 {#GeneralProperties

The category $AmdRep$ is [[cartesian closed category|cartesian closed]] and has all countable [[limits]] and [[colimits]] ([BSS 07 (4.10)](#BSS07))

### Relation to function realizability

The category $AdmRep$ above is a [[reflective subcategory]] of the [[function realizability topos]] $RT(\mathcal{K}_2)$ (see [vanOosten 08](#vanOosten08)).

### Relation to topology
 {#RelationToTopology}

$AdmRep$ is [[equivalence of categories|equivalent]] to the [[full subcategory]] of that of [[topological spaces]] on the $T_0$-[[quotient spaces]] of countably based $T_0$ spaces ([BSS 07](#BSS07)).

## Examples

Under the [above](#RelationToTopology) inclusion, all complete separable [[metric spaces]] are in $AdmRep$.

Some standard classes of examples (with an eye towards applications in [[computable physics]]) are discussed in [Weihrauch-Zhong 02, def. 2.6](#WeihrauchZhong02)


Since the [[Sierpinski space]] is in $AdmRep$, and due to cartesian clossure [above](GeneralProperties), for any $X \in AdmRep$ also its lattice of [[closed subspaces]] is in $AdmRep$.

## Related concepts

[[!include computable mathematics -- table]]


The subcategory on the effectively computable morphisms of the [[function realizability topos]] $RT(\mathcal{K}_2)$ is the [[Kleene-Vesley topos]]. The category of "admissible representations" $AdmRep$ above is a a [[reflective subcategory]] of $RT(\mathcal{K}_2)$ and the restriction of that to $KV$ is $AdmRep_{eff}$

$$
  \array{
     AdmRep_{eff} &\hookrightarrow& KV
     \\
     \downarrow && \downarrow
     \\
     AdmRep &\hookrightarrow& RT(\mathcal{K}_2)
  }
$$

See also

* [[topological domain theory]]


## References

Lecture notes include

* {#Bauer05} [[Andrej Bauer]], section 2 of _Realizability as connection between constructive and computable mathematics_, in T. Grubba, P. Hertling, H. Tsuiki, and [[Klaus Weihrauch]], (eds.) _CCA 2005 - Second International Conference on Computability and Complexity in Analysis_, August 25-29,2005, Kyoto, Japan, ser. Informatik Berichte, , vol. 326-7/2005. FernUniversit&#228;t Hagen, Germany, 2005, pp. 378&#8211;379. ([pdf](http://math.andrej.com/data/c2c.pdf))

A useful review is in section 4 of 

* {#BSS07} [[Ingo Battenfeld]], Matthias Schr&#246;der, [[Alex Simpson]], _A convenient category of domains_, in L. Cardelli, M. Fiore and G. Winskel (eds.), _Computation, Meaning and Logic_, Articles dedicated to Gordon Plotkin  Electronic Notes in Computer Science, 34 pp., to appear, 2007  [[BattenfeldDomains.pdf:file]]

Textbooks include

* {#Weihrauch00} [[Klaus Weihrauch]], _Computable Analysis_. Berlin, Springer, 2000

* {#vanOosten08} [[Jaap van Oosten]], _Realizability: an introduction to its categorical side_, Studies in Logic and the Foundations of Mathematics, vol. 152, Elsevier, 2008 ([preface pdf](http://www.staff.science.uu.nl/~ooste110/boekbegin.pdf))

Concrete examples with an eye towards applications in [[computable physics]] are discussed in section 2 of 

* {#WeihrauchZhong02} [[Klaus Weihrauch]],  Ning Zhong, _Is wave propagation computable or can wave computers beat the Turing machine?_, Proc. of the London Math. Soc. (3) 85 (2002) ([web](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.95.5994))

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

$\,$

[[!redirects computable functions (analysis)]]