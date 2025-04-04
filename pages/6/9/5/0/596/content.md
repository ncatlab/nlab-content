[[!redirects multispans]]
[[!redirects multicospan]]
[[!redirects multicospans]]

#Idea#

* A _multi(co)span_ is supposed to be something that generalizes [[span]] (and [[cospan]]) both horizontally and vertically: it may have a number of legs different from 2, but more importantly it need not be a single roof but can be a more complex diagram.

* A multispan is supposed to be a model for a _hierarchical cell complex_ with
  
  * a single top "cell" $K(\top) \in C$ (an object in some ambient category $C$);

  * for each cell $K(a)$ a collection of morphisms $\{K(b_i) \to K(a)\}_i$ into it, to be thought of as pieces of boundary components of $K(a)$;

    * in the language of [[hyperstructures]] we would say that $K(a)$ is a _bond_ for the $K(b_i)$

  * and so on;

  * such that the entire resulting diagram commutes, expressing the fact how one boundary pieces may be part of different higher order boundary pieces.

Multi-cospans of [[cubical]] shape have been introduced and studied by Marco Grandis in his work on [[Cospans in Algebraic Topology]]. Grandis also formulates the idea that an [[FQFT|extended QFT]] should be a morphism with domain [[extended cobordisms]] modeled as multi-cospans.

#Examples#

Special cases of multispans of the above general kind are

* ordinary [[spans]] and [[cospans]]: these are obtained by restricting the domain poset to be of the form 
$\wedge := a_1 \to \top \leftarrow a_2$.

* the double cospans of the form $\wedge^{\times 2}$ with $\wedge$ as above, described in 

  * Jeffrey Morton, _Double Bicategories and Double Cospans_ ([arXiv](https://arxiv.org/pdf/math/0611930)),

 * Grandis' higher cubical cospans, which generalize the previous example: these are obtained by restricting the domain posets to be the cartesian powers
$\wedge^{\times n}$ (with $\wedge$ as above).

An attempt at a discussion of multispans in greater generality is at [[hyperstructure]].


#Related concepts#

* [[span trace]]

* [[co-span co-trace]]

* [[Cospans in Algebraic Topology]]