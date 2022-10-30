
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

A [[module]] over a [[ring]] $R$ is called _flat_ if its satisfies one of many equivalent conditions, the simplest to state of which is maybe: forming the [[tensor product of modules]] with $N$ preserves [[submodules]].

Under the dual geometric interpretation of [modules as generalized vector bundles](module#RelationToVectorBundlesInIntroduction) over the space on which $R$ is the ring of functions, flatness of a module is essentially the _local triviality_ of these bundles, hence in particular the fact that the [[fibers]] of these bundles do not change, up to isomorphism. See prop. \ref{ForFinitelyGeneratedFlatIsLocallyFree} below for the precise statement. On the other hand there is **no** relation to "flat" as in [[flat connection]] on such a bundle.

## Definition
 {#Definition}

We first state the definition and its equivalent reformulations over a [[commutative ring]] abstractly in _[In terms of exact functors and Tor-functors](#InTermsOfExactFunctorsAndTorFunctors)_. Then we give an explicit element-wise characterization in _[Explicitly in terms of identities](#InTermsOfIdentities)_. 

Much of this discussion also works in the more general case where the ring is not-necessarily taken to be commutative and not necessarily required to be equipped with a unit, this we indicate in _[For more general rings](#spring)_.

### In terms of exact functors and Tor-functors
 {#InTermsOfExactFunctorsAndTorFunctors}

Let $R$ be a [[commutative ring]]. 

+-- {: .num_defn #FlatModule}
###### Definition

An $R$-[[module]] $N$ is __flat__ if [[tensor product of modules|tensoring]] with $N$ over $R$ as a [[functor]] from $R$[[Mod]] to itself
$$
  (-)\otimes_R N : R Mod \to R Mod
$$

is an [[exact functor]] (sends [[short exact sequences]] to short exact sequences).  

=--

+-- {: .num_remark #ImmediateReformulationOfFlatness}
###### Remark

The condition in def. \ref{FlatModule} has the following immediate equivalent reformulations:

1. $N$ is flat precisely if $(-)\otimes_R N$ is a [[left exact functor]],

   because tensoring with any module is generally already a [[right exact functor]];

1. $N$ is flat precisely if $(-)\otimes_R N$ sends [[monomorphisms]] ([[injections]]) to monomorphisms,

   because for a right exact functor to also be left exact the only remaining condition is that it preserves the monomorphisms on the left of a [[short exact sequence]];

1. $N$ is flat precisely if $(-)\otimes_R N$ is a [[flat functor]],

   because [[Mod]] is [[finitely complete category|finitely complete]];

1. $N$ is flat precisely if the degree-1 [[Tor]]-[[functor]] $Tor_1^{R Mod}(-,N)$ is zero,

   because by the general properties of [[derived functors in homological algebra]], $L_1 F$ is the obstruction to a [[right exact functor]] $F$ being left exact;

1. $N$ is flat precisely if all higher [[Tor]] functors $Tor_{\geq 1}(R Mod)(-,N)$ are zero,

    because the higher [[derived functor in homological algebra|derived functors]] of an [[exact functor]] vanish.

=--

The condition in def. \ref{FlatModule} also has a number of not so immediate equivalent reformulations. These we discuss in detail below in _[Equivalent characterizations](#EquivalentCharacterizations)_. One of them gives an explicit characterization of flat modules in terms of relations beween their elements.  An exposition of this we give now in _[In terms of identities](#InTermsOfIdentities)_.



### Explicitly in terms of identities
 {#InTermsOfIdentities}

There is a characterisation of flatness that says that a left $A$-module $M$ is flat if and only if "everything (that happens in $M$) happens for a reason (in $A$)". We indicate now what this means. Below in prop. \ref{RelationsFromCharacterizationonIdealInclusion} it is shown how this is equivalent to def. \ref{FlatModule} above.

The meaning of this is akin to the existence of [[basis of a vector space|bases in vector spaces]].  In a [[vector space]], say $V$, if we have an identity of the form $\sum_i \alpha_i v_i = 0$ then we cannot necessarily assume that the $\alpha_i$ are all zero.  However, if we choose a basis then we can write each $v_i$ in terms of the basis elements, say $v_i = \sum_j \beta_{i j} u_j$, and substitute in to get $\sum_{i j} \alpha_i \beta_{i j} u_j = 0$.  Now as $\{u_j\}$ forms a basis, we can deduce from this that for each $j$, $\sum_i \alpha_i \beta_{i j} = 0$.  These last identities happen in the coefficient field, which is standing in place of $A$ in the analogy.

When translating this into the language of modules we cannot use bases so we have to be a little more relaxed.  The following statement is the right one.

Suppose there is some identity in $M$ of the form $\sum_i a_i m_i = 0$ with $m_i \in M$ and $a_i \in A$.  Then there is a family $\{n_j\}$ in $M$ such that every $m_i$ can be written in the form $m_i = \sum_j b_{i j} n_j$ and the coefficients $b_{i j}$ have the property that $\sum_i a_i b_{i j} = 0$.

The module $M$ being flat is equivalent to being able always to do this.

There is an alternative way to phrase this which is less element-centric.  The elements $m_i$ correspond to a [[morphism]] into $M$ from a [[free module]], say $m \colon F \to M$.  The $a_i$ correspond to a morphism $a \colon F \to F$, multiplying the $i$th term by $a_i$.  That we have the identity $\sum_i a_i m_i = 0$ says that the composition $m a$ is zero, or that $m \colon F \to M$ factors through the [[coequaliser]] of $a$ and $0$.  

Now we consider the elements $n_j$.  These define another morphism from a free module, say $n \colon E \to M$.  That the $m_i$ can be expressed in terms of the $n_j$ says that the morphism $m$ factors through $n$.  That is, there is a morphism $b \colon F \to M$ such that $m = n b$.  We therefore have to factorisations of $m$: one through $n$ and one through the [[cokernel]] $\coker a$.  The question is as to whether these have any relation to each other.  In particular, does $\coker a \to M$ factor through $n$?  We can represent all of this in the following diagram.

+-- {: style="text-align:center"}
<svg width="222" height="136" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="14804">
 <g>
  <title>Layer 1</title>
  <foreignObject height="24.000001" width="30" font-size="16" id="svg_14804_1" y="56" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>F</mi>
     </mrow>
     <annotation encoding="application/x-tex">F</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_2" height="24.000001" width="30" font-size="16" y="56" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>F</mi>
     </mrow>
     <annotation encoding="application/x-tex">F</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_8" height="24.000001" width="30" font-size="16" y="56" x="192">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>M</mi>
     </mrow>
     <annotation encoding="application/x-tex">M</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_14" height="24.000001" width="60" font-size="16" y="112" x="121">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo rspace="thinmathspace" lspace="0em">coker</mo>
      <mi>a</mi>
     </mrow>
     <annotation encoding="application/x-tex">\coker a</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_20" height="24.000001" width="30" font-size="16" y="0" x="136">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>E</mi>
     </mrow>
     <annotation encoding="application/x-tex">E</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_14804_26)" id="svg_14804_26" y2="66" x2="80.009803" y1="66" x1="30" stroke-width="2" stroke="#000000" fill="none"/>
  <line transform="rotate(45, 121.006, 94)" id="svg_14804_27" marker-end="url(#se_marker_end_svg_14804_27)" y2="94" x2="146.009803" y1="94" x1="96" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_14804_29" transform="rotate(-45, 122.006, 39)" marker-end="url(#se_marker_end_svg_14804_29)" y2="39" x2="147.009803" y1="39" x1="97" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_14804_30" transform="rotate(-45, 179.006, 95)" marker-end="url(#se_marker_end_svg_14804_30)" y2="95" x2="204.009803" y1="95" x1="154" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_14804_31" transform="rotate(45, 179.006, 38)" marker-end="url(#se_marker_end_svg_14804_31)" y2="38" x2="204.009803" y1="38" x1="154" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="27.999999" font-size="16" id="svg_14804_32" y="44" x="40.000001">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>a</mi>
     </mrow>
     <annotation encoding="application/x-tex">a</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_33" height="20" width="27.999999" font-size="16" y="20" x="99.000001">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>b</mi>
     </mrow>
     <annotation encoding="application/x-tex">b</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_39" height="20" width="27.999999" font-size="16" y="17" x="177.000001">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>n</mi>
     </mrow>
     <annotation encoding="application/x-tex">n</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_14804_45" height="20" width="27.999999" font-size="16" y="44" x="154.000001">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>m</mi>
     </mrow>
     <annotation encoding="application/x-tex">m</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line id="svg_14804_51" marker-end="url(#se_marker_end_svg_14804_51)" y2="66" x2="190" y1="66" x1="110" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_14804_52)" id="svg_14804_52" y2="25.291191" x2="149" y1="111" x1="149" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_26">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_27">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_29">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_30">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_31">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_51">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_14804_52">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>
=--

Saying that $M$ is flat says that this lift always occurs.

Taking this a step further, we consider the [[filtered category|filtered family]] of all finite [[subsets]] of $M$.  This generates a filtered family of [[finitely generated module|finitely generated]] [[free modules]] with compatible morphisms to $M$.  So there is a morphism from the [[colimit]] of this family to $M$.  This morphism is [[surjection|surjective]] by construction.  To show that it is [[injection|injective]], we need to show that any element in one of the terms in the family that dies by the time it reaches $M$ has actually died on the way.  This is precisely what the above characterisation of flatness is saying: the element corresponding to $\sum_i a_i m_i$ that dies in $M$ is already dead by the time it reaches $E$.

Hence a module is flat if and only if it is a [[filtered colimit]] of [[free modules]]. 

This observation (Wraith, Blass) can be put into the more general context of modelling [[geometric theory|geometric theories]] by [[geometric morphism|geometric morphisms]] from their [[classifying topos|classifying toposes]], or equivalently, certain [[flat functor|flat functors]] from [[site|sites]] for such topoi.

### For more general rings

Even if the [[ring]] $R$ is not necessarily commutative and not necessarily unital, we can say: 

A left $R$-[[module]] is flat precisely if the [[tensor product of modules|tensoring]] functor

$$
  (-)\otimes_R \colon Mod_R \to Ab
$$

from _right_ $R$ modules to [[abelian groups]] is an [[exact functor]].


## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

By def. \ref{FlatModule}, or its immediate consequence, remark \ref{ImmediateReformulationOfFlatness}. $N \in R Mod$ is flat if for every injection $i \colon A \hookrightarrow$ also $i \otimes_R N \colon A \otimes_R N \to B \otimes_R N$ is an injection. The following proposition says that this may already be checked on just a very small subclass of injections.

+-- {: .num_theorem #CharacterizationOnIdealInclusions}
###### Theorem

An $R$-module $N$ is flat already if for all inclusions $I \hookrightarrow R$ of a [[finitely generated module|finitely generated]] [[ideal]] into $R$, regarded as a module over itself, the induced morphism

$$  
  I \otimes_R N \to R \otimes_R N \simeq N
$$

is an injection.

=--

+-- {: .proof}
###### Proof

(...)

=--

+-- {: .num_prop #RelationsFromCharacterizationonIdealInclusion}
###### Proposition

A module $N$ is flat precisely if for every finite linear combination of zero, $\sum_i r_i n_i  = 0\in N$ with $\{r_i \in R\}_i$,  $\{n_i \in N\}$ there are elements $\{\tilde n_j \in N\}_j$ and linear combinations

$$
  n_i = \sum_j b_{i j} \tilde n_j \;\;\in  N
$$

with $\{b_{i j} \in R\}_{i,j}$ such that for all $j$ we have

$$
  \sum_i r_i b_{i j}  = 0\;\;\; \in R
  \,.
$$

=--

+-- {: .proof}
###### Proof

A finite set $\{r_i \in R\}_i$ corresponds to the inclusion of a finitely generated ideal $I \hookrightarrow R$. 

By theorem \ref{CharacterizationOnIdealInclusions} $N$ is flat precisely if $I \otimes_R N \to N$ is an injecton. This in turn is the case precisely if the only element of the tensor product $I \otimes_R R$ that is 0 in $R \otimes_R N = N$ is already 0 on $I \otimes_R N$.

Now by definition of [[tensor product of modules]] an element of $I \otimes_R N$ is of the form $\sum_i (r_i ,n_i)$ for some $\{n_i \in N\}$. Under the inclusion $I \otimes_R N \to N$ this maps to the actual linear combination $\sum_i r_i n_i$. This map is injective if whenever this linear combination is 0, already $\sum_i (r_i, n_i)$ is 0.

But the latter is the case precisely if this is equal to a combination $\sum_j (\tilde r_j  , \tilde n_j)$ where all the $\tilde r_j$ are 0. This implies the claim.

=--



### Relation to projective modules

+-- {: .num_prop}
###### Proposition
**([[Lazard's criterion]])**

A module is flat if and only if it is a [[filtered colimit]] of [[free modules]]. 

=--

This is due to ([Lazard (1964)](#Lazard)).

+-- {: .proof}
###### Proof

(...) For the moment see the above discussion. (...)

=--

### Relation to (locally) free modules

+-- {: .num_defn #LocallyFreeModule}
###### Definition

An $R$-module $N$ over a [[Noetherian ring]] $R$ is called a **locally free module** if there is a [[Zariski topology|cover]] by [[prime ideals]] $I \hookrightarrow R$ such that the [[localization of a module|localization]] $N_I$ is a [[free module]] over the [[localization of a ring|localization]] $R_I$. 

=--

+-- {: .num_prop #ForFinitelyGeneratedFlatIsLocallyFree}
###### Proposition

For $R$ a [[Noetherian ring]] and $N$ a [[finitely generated module]] over $R$, $N$ is flat precisely if it is [[locally free module]], def. \ref{LocallyFreeModule}.

=--

By [Raynaud-Gruson, 3.4.6 (part I)](#RaynaudGruson)


+-- {: .num_prop }
###### Proposition

If 

1. $R$ is a [[local ring]],

1. $N$ is a [[finitely generated module]],

1. $N$ is a flat module

then $N$ is a [[free module]].

=--

This is [Matsumara, Theorem 7.10](#Matsumara)

## Examples
 {#Examles}

+-- {: .num_example}
###### Example

An [[abelian group]] is flat (regarded as a $\mathbb{Z}$-module) precisely if it is [[torsion subgroup|torsion-free]].

=--

+-- {: .proof}
###### Proof

By the general discussion at [[derived functor in homological algebra]], the obstruction to $A \in Ab$ being flat are the first [[Tor]]-groups $Tor_1^{\mathbb{Z}}(-,A)$. By the discussion at  _[Tor -- relation to torsion subgroups](Tor#RelationToTorsionGroups)_ these a [[filtered colimits]] and [[direct sums]] of the [[torsion subgroups]] of $A$. In particular for $Tor_1^\mathbb{Z}(\mathbb{Z}_n,A)$ is the $n$-torsion subgroup of $A$. Hence $Tor_1^\mathbb{Z}(-,A)$ vanishes and hence $A$ is flat precisely if all torsion subgroups of $A$ are trivial.

=--

## Related concepts

* [[flat resolution lemma]]

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
* flat object, [[flat resolution]]

* [[free module]] $\Rightarrow$ [[projective module]] $\Rightarrow$ **flat module** $\Rightarrow$ [[torsion-free module]]






## References

Original articles include

* Shizuo Endo, _On flat modules over commutative rings_,  J. Math. Soc. Japan Volume 14, Number 3 (1962), 284-291. ([EUCLID](http://projecteuclid.org/euclid.jmsj/1261060583))

* Michel Raynaud, Laurent Gruson, _Crit&#232;res de platitude et de projectivit&#233;_, Techniques de "platification" d'un module. Invent. Math. 13 (1971), 1&#8211;89.
 {#RaynaudGruson}

* S. Jondrup, _Flat and projective modules_, Math, Scand. 43 (1978) ([pdf](http://www.mscand.dk/article.php?id=2456))

The characterization of flat modules as filtered colimits of [[projective modules]] is due to 

* [[Daniel Lazard]], _Sur les modules plats_ C. R. Acad. Sci. Paris 258, 6313&#8211;6316 (1964)
 {#Lazard}

For a general account see for instance section 3.2 of 

* [[Charles Weibel]], _[[An Introduction to Homological Algebra]]_

For more details see

* Matsumura's CRT book
 {#Matsumara}

Lecture notes include

* Arthur Ogus, _Flatness -- a brief overview_ ([pdf](http://math.berkeley.edu/~ogus/Math%20_256B--09/Supplements/flat.pdf))

Further resources include

* MO discussion _[flatness and local freeness](http://mathoverflow.net/questions/33522/flatness-and-local-freeness)_

[[!redirects flat modules]]
