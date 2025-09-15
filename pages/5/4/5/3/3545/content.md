
>  This entry is about [[quasi-isomorphism]] to [[cochain cohomology]]. For [[infinitesimal neighbourhood|infinitesimal thickening]] of [[smooth manifolds]] see at _[[formal smooth manifold]]_.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Definition

A [[dg-algebra]] $A$ is a **formal dg-algebra** if it is [[quasiisomorphism|quasi-isomorphic]] (i.e.: [[isomorphism|isomorphic]] in the [[homotopy category]] of the [[model structure on dg-algebras]])

\[
  A 
  \xrightarrow{\;\;\; \simeq \;\;\;}
  H^\bullet(A)
\]

to its [[chain homology and cohomology|chain (co)homology]] regarded as a dg-algebra with trivial differential. 

Since all dg-algebras are [[fibrant object|fibrant]] in the [[model structure on dg-algebras|standard model structure]], this is equivalent to the existence of a [[span]]

\[
  \label{TheSpan}
  A 
    \overset{\;\; \simeq_w \;\;}{\leftarrow} 
  Q A 
    \overset{\;\; \simeq \;\;}{\rightarrow}
  H^\bullet(A)
\]

of [[quasi-isomorphisms]] of dg-algebras.


## Examples

In [[rational homotopy theory]] [[rational topological spaces]] are encoded in their [[Sullivan algebra|Sullivan dg-algebras]] (cf. The [[fundamental theorem of dg-algebraic rational homotopy theory]]). A [[simply connected topological space]] $X$ whose Sullivan dg-algebra $\Omega^\bullet(X)$ is formal is called a **formal topological space**.  (One can also say a __formal rational space__, to distinguish from the unrelated formal spaces in [[formal topology]].)  Such a space represents a **formal homotopy type**.

Examples:

* compact [[Kähler manifolds]] (e.g. smooth projective varieties),

* [[Lie groups]],

* [[classifying spaces]]$\;B G$ of [[Lie groups]] $G$,

* some [[homogeneous spaces]] $G/H$ (see ([Amann 12](#Amann12)) for *non*formal examples),

* the unstable [[Thom spaces]] $M U_n$ and $M S O_n$,

* the [[Eilenberg-MacLane space]] $K(\mathbb{Z},n)$, 

  whose Sullivan minimal model is the dg-algebra on a single degree$=n$ generator with trivial differential.,

* [[the little n-disk operad is formal]].

## Related concepts

* [[H-cohomology]]


## References

Early discussion of formal [[Sullivan model]] dg-algebras in the context of [[rational homotopy theory]]:

* {#Sullivan77} [[Dennis Sullivan]], section 12 of: _Infinitesimal computations in topology_, Publications mathématiques de l’ I.H.É.S **47** (1977) 269-331 &lbrack;[numdam:PMIHES_1977__47__269_0](http://www.numdam.org/item?id=PMIHES_1977__47__269_0), [pdf](http://archive.numdam.org/article/PMIHES_1977__47__269_0.pdf)&rbrack;

* [[Pierre Deligne]], [[Phillip Griffiths]], [[John Morgan]], [[Dennis Sullivan]]: _Real homotopy theory of Kähler manifolds_, Invent Math  **29** (1975) 245-274 &lbrack;[doi:10.1007/BF01389853](https://doi.org/10.1007/BF01389853)&rbrack;

Since [[Sullivan models]] are also [[cofibrant object|cofibrant]], the above authors get away with considering a direct comparison map instead of a span as in (eq:TheSpan). The general definition is reviewed in:

* {#Hess06} [[Kathryn Hess]], Def. 2.1 in: _Rational homotopy theory: a brief introduction_, contribution to _[Summer School on Interactions between Homotopy Theory and Algebra](https://jdc.math.uwo.ca/summerschool/)_, University of Chicago, July 26-August 6, 2004, Chicago &lbrack;[arXiv:math.AT/0604626](http://arxiv.org/abs/math.AT/0604626)&rbrack;, chapter in Luchezar Lavramov, [[Dan Christensen]], [[William Dwyer]], [[Michael Mandell]], [[Brooke Shipley]] (eds.), _Interactions between Homotopy Theory and Algebra_, Contemporary Mathematics **436**, AMS (2007) &lbrack;[doi:10.1090/conm/436](http://dx.doi.org/10.1090/conm/436)&rbrack;

* {#Aambø21} Torgeir Aambø, Def. 1.15 & Theorem A (p.2): *On formal DG-algebras*, MSc thesis, NTNU (2021) &lbrack;[hndl:11250/2778399](https://hdl.handle.net/11250/2778399)&rbrack;

Review with an eye towards the [[dd^c-lemma]] and [[H-cohomology]] is in

* {#Cavalcanti03} [[Gil Cavalcanti]], p. 12 of _New aspects of the $d d^c$-lemma_ ([arXiv:math/0501406](https://arxiv.org/abs/math/0501406))

The case of [[Sullivan algebras]] of [[sphere bundles]]:

* Jiawei Zhou, *Formality of Sphere Bundles* &lbrack;[arXiv:2304.09594](https://arxiv.org/abs/2304.09594)&rbrack;

A construction of nonformal homogeneous spaces:

* {#Amann12} [[Manuel Amann]]. *Non-formal Homogeneous Spaces* (2012). ([arXiv:1206.0786](https://arxiv.org/abs/1206.0786)).


[[!redirects formal dg-algebra]]
[[!redirects formal dg-algebras]]

[[!redirects formal differential graded algebra]]
[[!redirects formal differential graded algebras]]

[[!redirects formal rational space]]
[[!redirects formal rational spaces]]

[[!redirects formal homotopy type]]
[[!redirects formal homotopy types]]

[[!redirects formal rational homotopy type]]
[[!redirects formal rational homotopy types]]

