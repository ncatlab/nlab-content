
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Modalities
+-- {: .hide}
[[!include modalities - contents]]
=--
=--
=--

> This entry is about [[models]] of [[modal logic]]; for *[[frames]]* in the sense of [[geometric logic]] see instead there.

***

# Contents
* table of contents
{:toc}

## Idea

In [[formal logic]], *Kripke frames*, after [Kripke (1959)](#Kripke59), [(1963)](#Kripke63), serve as the [[context|contextual]] substrate of [[set theory|set-theoretic]] [[semantics]]/[[models]] for [[modal logics]] (called *[[geometric model for modal logics|geometric models]]* as opposed to *[[algebraic model for modal logics|algebraic models]]*).

In itself, a Kripke frame is just 

* an [[inhabited set|inhabited]] [[set]] $W$ 

  often called the set of *[[possible worlds]]* (or the set of *nodes* or whatnot)

* equipped with an [[indexed set]] of ([[reflexive relation|reflexive]]) [[relations]] $R_i \subset W \times W$, one for each [[modal operator]] $\Box_i$ in the given [[modal logic]]

  called the *accessiblity* or *transition* relations between worlds, or similar.

Hence a Kripke frame is a [[concept with an attitude]], namely the attidute to serve as a model for a [[modal logic]] -- the idea is to interpret:

1. the [[elements]] of $W$ as the "[[possible worlds]]" about which the [[propositions]] in the modal logic make statements, 

1. the [[relation]] $R_i(w,w')$ as asserting that it makes sense to reason about world $w'$ at world $w$.

Namely a [[geometric model for modal logics|model]] of the modal logic based on such a Kripke frame will interpret 

* each proposition $P$ of the logic as a $W$-[[dependent type|dependent]] proposition,

* each [[modal operator|modal]] proposition $\Box_i P$ as the [[dependent type|dependent]] proposition which at $w \in W$ asserts that "$P$ holds at all those $w'$ that are in $i$th relation to $W$", hence "$P$ holds in all possible worlds $w'$ that are $i$-accessible from $w$".


**The transparent case of S5 logic.** Specifically, for the case of [[S5 modal logic]] with a single [[comonad|comonadic]] [[modal operator]] $\Box$, a Kripke frame (originally considered in [Kripke 1963](#Kripke63)) is an 

* [[inhabited set]]$\;$ $W$

equipped with a single

* [[equivalence relation]]$\;$ $R$ 

  (hence a relation which is [[reflexive relation|reflexive]], [[transitive relation|transitive]] and [[symmetric relation|symmetric]])

which means that $W$ decomposes as the [[disjoint union]] of its [[equivalence classes]], these being the [[fibers]] of the [[quotient]] [[coprojection]]

\[
  \label{QuotientCoprojectionInCaseOfS5}
  W \xrightarrow{\;\; p_W \;\;} W/R
  \,.
\]


{#NecessityLogic} **The simple case necessity logic.** In the further special case there is just a single such class (hence that "all possible worlds are related", originally considered by [Kripke 1959](#Kripke59)) this becomes

\[
  \label{QuotientCoprojectionInCaseOfGlobalS5}
  W \xrightarrow{\;\; p_W \;\;} \ast
\]

so that in [[geometric model for modal logics|models]] based on such a frame the interpretation of the [[modal operator]] $\Box$ is that of *[[necessity]]*: $\Box P$ now asserts, independently of the world that it is evaluated on, that $P$ holds at *all* $w \in W$, hence that $P$ holds *necessarily* in the sense of: no matter which world.

The general case of Kripke frames is really just this basic idea with some variations added. For instance the general case (eq:QuotientCoprojectionInCaseOfS5) of S5 modal logic is just a $W/R$-indexed [[disjoint union]] of this basic situation.



**Perspective of dependent type theory.**
As discussed in detail at *[Possible worlds via Dependent types](necessity+and+possibility#InFirstOrderLogicAndTypeTheory)*,
the Kripke model for the modal operator $\Box$ in the case (eq:QuotientCoprojectionInCaseOfGlobalS5) of [[S5 modal logic]] with a global accessibility relation is just the [[base change]] [[comonad]] along the projection (eq:QuotientCoprojectionInCaseOfGlobalS5), and the same argument immediately applies to the general S5-case (eq:QuotientCoprojectionInCaseOfS5):

\[
  \label{BaseChange}
\]
\begin{tikzcd}
    W \ar[rr, "{ p_{{}_W} }"] && W/R
    \\
    \mathrm{Prop}_W
    \ar[out=180-42, in=180+42,
      <-,
      looseness=4.5, 
      shorten=0pt,
      shift right=3pt,
      "\scalebox{1.1}{${
          \hspace{1pt}
          \mathclap{
            {
              \Box
            }
          }
          \hspace{4pt}
        }$}"{
          pos=.5, 
          swap
        }
    ]  
    \ar[
      from=rr,
      shift right=7pt,
      "{ (p_{{}_W})^\ast }"{swap}
    ]
    \ar[
      rr,
      shift right=7pt,
      "{ (p_{{}_W})_\ast }"{swap}
    ]
    \ar[
      rr,
      phantom,
      "{ \scalebox{.7}{$\bot$} }"
    ]
    &&
    \mathrm{Prop}_{W/R}
  \end{tikzcd}

**The case of S4 logic.** 
If the [[relation]] $R$ in a Kripke frame is ([[reflexive relation|reflexive]] and) [[transitive relation|transitive]] but not necessarily [[symmetric relation|symmetric]], then it still serves to provide models of [[S4 modal logic]] (cf. [Kripke 1959, §2](#Kripke59)).

In this case the relation no longer defines a [[groupoid]] ("[[setoid]]") as it does for the S5-case, but it defines a [[(0,1)-category]] with [[objects]] the elements of $W$.

As such, to retain the type-theoretic perspective (eq:BaseChange) in this case will require some form of *[[directed type theory]]*.

\linebreak

**General case**

[[!include flavors of modal logics and relations -- table]]


## Related entries


* [[possible worlds]]

* [[necessity and possibility]]

* [[epistemic modal logic]]


## References

The original articles:

* {#Kripke59} [[Saul A. Kripke]], *A Completeness Theorem in Modal Logic*, The Journal of Symbolic Logic **24** 1 (1959) 1-14 &lbrack;[doi:10.2307/2964568](https://doi.org/10.2307/2964568), [jstor:2964568](https://www.jstor.org/stable/2964568), [pdf](https://www.filosoficas.unam.mx/~morado/Cursos/17Modal/Kripke1959.pdf)&rbrack;

* {#Kripke63} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic I. Normal Modal Propositional Calculi*, Mathematical Logic Quaterly **9** 5-6 (1963) 67-96 &lbrack;[doi:10.1002/malq.19630090502](https://doi.org/10.1002/malq.19630090502)&rbrack;

* [[Saul A. Kripke]], *Semantical Considerations on Modal Logic*, Acta Philosophical Fennica **16** (1963) 83-94 &lbrack;[pdf](http://saulkripkecenter.org/wp-content/uploads/2019/03/Semantical-Considerations-on-Modal-Logic-PUBLIC.pdf)&rbrack;

* {#Kripke65} [[Saul A. Kripke]], *Semantical Analysis of Modal Logic II. Non-Normal Modal Propositional Calculi*, in *The Theory of Models* (Proceedings of the 1963 International Symposium at Berkeley) Studies in Logic and the Foundations of Mathematics (1965) 206-220 &lbrack;[doi:10.1016/B978-0-7204-2233-7.50026-5](https://doi.org/10.1016/B978-0-7204-2233-7.50026-5)&rbrack;


Textbook accounts;

* {#BlackburnDeRijkeVenema01} [[Patrick Blackburn]], [[Maarten de Rijke]], [[Yde Venema]], §1.3 in: *Modal Logic*, Cambridge Tracts in Theoretical Computer Science **53**, Cambridge University Press (2001) &lbrack;[doi:10.1017/CBO9781107050884](https://doi.org/10.1017/CBO9781107050884)&rbrack;

* [[Valentin Goranko]], [[Martin Otto]], §1.2 in: *Model Theory of Modal Logic*, in Section 5 in: *Handbook of Modal Logic*, Studies in Logic and Practical Reasoning **3** (2007) 249-329 &lbrack;[pdf](https://www2.mathematik.tu-darmstadt.de/~otto/papers/mlhb.pdf),  [book webpage](https://cgi.csc.liv.ac.uk/~frank/MLHandbook/), [publisher page](https://www.sciencedirect.com/bookseries/studies-in-logic-and-practical-reasoning/vol/3/suppl/C)&rbrack;

* {#GasquetHerzigSaidSchwarzentruber13} Olivier Gasquet, Andreas Herzig, Bilal Said, François Schwarzentruber,  *Kripke's Worlds: An Introduction to Modal Logics via Tableaux*, Studies in Universal Logic, Springer (2014) &lbrack;[doi:10.1007/978-3-7643-8504-0](https://doi.org/10.1007/978-3-7643-8504-0), [ISBN:978-3764385033]()&rbrack;

Generalization of Kripke frames:

* [[Dov Samet]], §6 in: *S5 knowledge without partitions*, Synthese **172** (2010) 145–155 &lbrack;[doi:10.1007/s11229-009-9469-0](https://doi.org/10.1007/s11229-009-9469-0)&rbrack;




[[!redirects Kripke frame]]
[[!redirects Kripke frames]]
[[!redirects frame (Kripke)]]
[[!redirects frames (Kripke)]]
[[!redirects frame (modal logic)]]
[[!redirects frames (modal logic)]]
