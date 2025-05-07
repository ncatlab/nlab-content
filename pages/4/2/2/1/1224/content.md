+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

A [[functor]] $F \colon C \to D$ is **final**, if restricting [[diagrams]] along $F$ does not change their [[colimit]].  

Dually, a functor is **initial** if pulling back diagrams along it does not change the [[limits]] of these diagrams.

Beware that this property is pretty much unrelated to that of a functor being an [[initial object]] or [[terminal object]] in the [[functor category]] $[C,D]$.  The terminology comes instead from the fact that an object $d\in D$ is initial (resp. terminal) just when the corresponding functor $d \colon 1\to D$ is initial (resp. final).


\begin{remark}\label{WarningOnTerminology}
**(warning on terminology)**
\linebreak
In older references (and also some others like *[[Higher Topos Theory|HTT]]*), final functors are sometimes called *cofinal*, the terminology having been imported from [[order theory]] (cf. *[[cofinality]]*).  However, this is confusing in [[category theory]] because usually the prefix "co-" denotes [[formal dual|dualization]].  In at least one place ([Borceux](#fb)) this non-dualization was treated as a dualization and the word "final" used for the *dual* concept, but in general it seems that the consensus is to use "final" for what used to be called "cofinal", and "initial" for the dual concept (since "co-final" would be ambiguous).  For example, [[Peter Johnstone|Johnstone]] in *[[Sketches of an Elephant]]* says (before Proposition B2.5.12 ):

> Traditionally, final functors were called 'cofinal functors'; but this use of 'co' is potentially misleading as it has nothing to do with dualization — it is derived from the Latin 'cum' rather than 'contra' — and so it is now generally omitted.

See also the warning at *[[final (infinity,1)-functor|final $(\infty,1)$-functor]]* ([here](final+infinity1-functor#CofinalTerminologyWarning)).
\end{remark}

## Definition

+-- {: .num_defn}
###### Definition


A [[functor]] $F : C \to D$ is **final** if for every [[object]] $d \in D$ the [[comma category]] $(d/F)$ is (non-empty and) [[connected category|connected]] (the non-emptiness condition is redundant since connected categories are non-empty by convention).

A [[functor]] $F : C \to D$ is **initial** if the [[opposite category|opposite]] $F^{op} : C^{op} \to D^{op}$ is final, i.e. if for every [[object]] $d \in D$ the [[comma category]] $(F/d)$ is [[connected category|connected]].

=--


## Properties

+-- {: .num_prop}
###### Proposition

Let $F : C \to D$ be a [[functor]]

The following conditions are equivalent.

1. $F$ is final.

1. {#AnItem} For all functors $G : D \to Set$ the natural [[function]] between [[colimits]]

   $$
     \lim_\to G \circ F \to \lim_{\to} G
   $$

   is a [[bijection]].


1. For all categories $E$ and all functors $G : D \to E$ the natural [[morphism]] between [[colimit]]s

   $$
     \lim_\to G \circ F \to \lim_{\to} G
   $$

   is an [[isomorphism]].
   

1. For all functors $G : D^{op} \to Set$ the natural [[function]] between [[limit]]s

   $$
     \lim_\leftarrow G \to \lim_\leftarrow G \circ F^{op}
   $$

   is a [[bijection]].

1. For all categories $E$ and all functors $G : D^{op} \to E$ the natural [[morphism]]

   $$
     \lim_\leftarrow G \to \lim_\leftarrow G \circ F^{op}
   $$

   is an [[isomorphism]].
   
1. For all $d \in D$ 

   $$
     {\lim_\to}_{c \in C} Hom_D(d,F(c)) \simeq *
     \,.
   $$

1. for all functors $G: D \to E$, the canonical map

   $$
     Nat(G,\Delta-)\to Nat(GF,\Delta-) : E \to Set
   $$

   between the functors of [[cocones]] on $G$ and $GF$ is an [[isomorphism]]. (Here, the $\Delta$'s denote the functors sending objects to constant functors, and $Nat$ stands for the set of natural transformations.)

=--

([Kashiwara & Schapira 2006, Prop. 2.5.2](#KashiwaraSchapira06))

+-- {: .num_prop}
###### Proposition

If $F : C \to D$ is final then $C$ is connected precisely if $D$ is.

=--


+-- {: .num_prop #Stability}
###### Proposition

If $F_1$ and $F_2$ are final, then so is their composite $F_1 \circ F_2$.

If $F_2$ and the composite $F_1 \circ F_2$ are final, then so is $F_1$.

Final functors are stable under [[pushout]]. 

The [[coproduct]] of final functors in the [[arrow category]] $\mathbf{Cat}^{\mathbf{2}}$ is a final functor. 

If $F_1$ is a [[full and faithful functor]] and the composite is final, then both functors seperately are final.

=--

The first two statements of Proposition \ref{Stability} in fact follow
from the stability properties of orthogonal factorization systems:

+-- {: .num_prop}
###### Proposition

Final functors and [discrete fibrations](http://ncatlab.org/nlab/show/discrete+fibration) form an [orthogonal factorization system](https://ncatlab.org/nlab/show/orthogonal+factorization+system) called the [[comprehensive factorization system]].

=--

## Generalizations

### Exact squares

The characterization of final functors is a special case of the characterization of [[exact squares]].

### Final enriched functors 
 {#FinalityForWeightedLimits}

Finality for [[enriched functors]] with respect to [[weighted colimits]] (for enrichment in a [[cartesian closed category]]) is discussed in [Kelly 1982 §4.5](#Kelly82): see Theorem 4.67 in particular.

See also discussion of finality specifically for [[coends]] (initiality for [[weighted limits]] and [[ends]]) by:

* [[Tim Campion]]: *Cofinality for Coends* (2020) &lbrack;[MO:q/353876](https://mathoverflow.net/q/353876/381), [MO:a/354097](https://mathoverflow.net/a/354097/381)&rbrack;

### Final $\infty$-functors

The generalization of the notion of final functor from [[category theory]] to [[(∞,1)-category|(∞,1)]]-[[higher category theory]] is described at

* [[final (∞,1)-functor]].




## Examples
 {#Examples}

\begin{example}
  \label{InclusionOfATerminalObjectIsFinal}
**([[subcategory|inclusion]] of a [[terminal object]] is [[final functor]])** \linebreak
If $D$ has a [[terminal object]] then the functor $F : {*} \to D$ that picks that terminal object is final: for every $d \in D$ the [[comma category]] $d/F$ is equivalent to $*$.  The converse is also true: if a functor $*\to D$ is final, then its image is a terminal object.

In this case the statement about preservation of colimits states that the colimit over a category with a terminal object is the value of the diagram at that object. Which is also readily checked directly.

More generally, a functor whose domain is a [[discrete category]] is final if and only if it is a right adjoint.  

\end{example}

\begin{example}\label{FinalFunctorBetweenGroupoids}
  A functor between [[groupoids]] is final iff it is [[essentially surjective functor|essentially surjective]] and [[full functor|full]].
\end{example}
(eg. [Cigoli 2018, Prop. 1.1](#Cigoli18))

+-- {: .num_example }
###### Example

Every [[right adjoint|right]] [[adjoint functor]] is final.

=--

+-- {: .proof}
###### Proof

Let $(L \dashv R) : C \to D$ be a pair of [[adjoint functors]].To see that $R$ is final, we may for instance check that for all $d \in D$ the comma category $d / R$ is non-empty and connected:

It is non-empty because it contains the [[unit of an adjunction|adjunction unit]] $(L(d), d \to R L (d))$. Similarly, for 

$$
  \array{
    && d
    \\
    & {}^{\mathllap{f}}\swarrow && \searrow^{\mathrlap{g}}
    \\
    R(a) &&&& R(b)
  }
$$

two objects, they are connected by a zig-zag going through the unit, by the [[adjoint functor#UniversalArrows|universal factorization property]] of adjunctions

$$
  \array{
    && d
    \\
    & \swarrow &\downarrow& \searrow
    \\
    R(a) &\stackrel{R \bar f}{\leftarrow}& R L (d)& \stackrel{R(\bar g)}{\to} & R(b)
  }
  \,.
$$

=--

+-- {: .num_example}
###### Example

The inclusion $\mathcal{C} \to \tilde \mathcal{C}$ of any category into its [[idempotent completion]] is final. 

=--

See at _[[idempotent completion]]_ in the section on _[Finality](Karoubi+envelope#Finality)_.

+-- {: .num_example #CoconeUnderCospan}
###### Example

The inclusion of the [[cospan]] [[diagram]] into its [[cocone]]

$$
  \left(
    \array{
       a
       \\
       \downarrow
       \\
       c
       \\
       \uparrow
       \\
       b
    }
  \right)
  \hookrightarrow
  \left(
    \array{
       a
       \\
       \downarrow & \searrow
       \\
       c &\longrightarrow & p  
       \\
       \uparrow & \nearrow
       \\
       b
    }
  \right)
$$

is initial.

=--

+-- {: .num_remark #FiberProductsInASliceCategory}
###### Remark

By the characterization ([here](overcategory#LimitsInSliceViaLimitsOfCoconedDiagram)) of limits in a [[slice category]], this implies that [[fiber products]] in a [[slice category]] are computed as fiber products in the underlying category, or in other words that [[dependent sum]] to the point preserves fiber products.

=--

\begin{example}\label{FirstPairOfFaceMapsFinalInOppositeSimplexCategory}
  For $\Delta^{op}$ the [[opposite category|opposite]] of the [[simplex category]], the non-full [[subcategory]] inclusion of the lowest two face maps
  $$
    \big(
      [1]
      \underoverset
        {d_0}
        {d_1}
        {\rightrightarrows}          
      [0]
    \big)
    \;\xrightarrow{\;\;\;\;}\;
    \Delta^{op}
  $$
  is a final functor.

  It follows that the [[colimit]] over a [[simplicial diagram]] is equivalently the [[coequalizer]] of the lowest two face maps.
\end{example}

(e.g. [Riehl 14, Exp. 8.3.8](#Riehl14))


## Related concepts

* [[cofinal diagram]]

* [[homotopy final functor]]

* [[final (∞,1)-functor]]



[[!include properties of functors -- contents]]



## References


* {#KashiwaraSchapira06} [[Masaki Kashiwara]], [[Pierre Schapira]], Section 2.5 of: _[[Categories and Sheaves]]_, Grundlehren der Mathematischen Wissenschaften __332__, Springer (2006) &lbrack;[doi:10.1007/3-540-27950-4](https://link.springer.com/book/10.1007/3-540-27950-4), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/kashiwara2.pdf)&rbrack;


* [[Saunders Mac Lane]], Section IX.3 of: _[[Categories for the Working Mathematician]]_

* {#fb} [[Francis Borceux]], Section 2.11 of: _[[Handbook of Categorical Algebra]] 1, Basic category theory_, Encyclopedia of Mathematics and its Applications **50**, Cambridge University Press (1994)

  > (this says "final functor" for the version under which limits are invariant)

* {#Riehl14} [[Emily Riehl]], Section 8.3 of: _[[Categorical Homotopy Theory]]_, Cambridge University Press, 2014 ([pdf](http://www.math.jhu.edu/~eriehl/cathtpy.pdf), [doi:10.1017/CBO9781107261457](https://doi.org/10.1017/CBO9781107261457))

* [[Paolo Perrone]], [[Walter Tholen]], *Kan extensions are partial colimits*, Applied Categorical Structures, 2022. ([arXiv:2101.04531](https://arxiv.org/abs/2101.04531))

  > (this says "confinal functor" for the version under which colimits are invariant)

In [[enriched category theory]]:

* {#Kelly82} [[Max Kelly]], §4.5 in: _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

In [[internal category]] theory for [[internal functors]] between [[internal groupoids]] in [[exact categories]]:

* {#Cigoli18} [[Alan S. Cigoli]], *A characterization of final functors between internal groupoids in exact categories*, Theory and Applications of Categories **33** 11 (2018) 265-275.  &lbrack;[arXiv:1711.10747](https://arxiv.org/abs/1711.10747), [tac:33-11](http://www.tac.mta.ca/tac/volumes/33/11/33-11abs.html)&rbrack;


[[!redirects cofinal functor]]
[[!redirects cofinal functors]]
[[!redirects final functor]]
[[!redirects final functors]]
[[!redirects initial functor]]
[[!redirects initial functors]]

