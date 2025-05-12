
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
 {#Idea}

In [[algebra]], the notion of *flat* [[modules]] (due to [GAGA](#GAGA)) is a generalisation of the class of [[torsion-free modules]] over [[rings]] $R$ that are not [[PID]].

An $R$-module $M$ is _flat_ (from the French word “*plat*”) if it has “no torsion” in the sense that the [[Tor]]-functor vanishes for every $R$-module $X$:
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  \underset{X \in R Mod}{\forall}
  \;\;\;
  \mathrm{Tor}_1^R(M, X) \,=\, 0
  \,.
$$


\begin{remark}\label{TerminologyAndRelationToFiberBundles}
**(terminology and relation to fiber bundles)**
\linebreak
[[finitely presented module|Finitely presented]] flat modules are locally free \[\ref{FinitelyPresentedFlatIsProjective}\], hence
under the [[duality between algebra and geometry|dual geometric interpretation]] of [modules as generalized vector bundles](module#RelationToVectorBundlesInIntroduction) over the space on which $R$ is the [[ring of functions]], flatness of a finitely presented module is essentially the _[[local triviality]]_ of this bundle, hence in particular the fact that the [[fibers]] of the bundle do not change, up to isomorphism (cf. *[[fiber bundle]]*).

On the other hand there is **no** relation to "flat" as in [[flat connection]] on such a bundle.
\end{remark}

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

+-- {: .num_defn #FaithfullyFlatModule}
###### Definition

A module as above is _faithfully flat_ if it is flat and tensoring in addition _reflects exactness_, hence if the tensored sequence is exact if and only if the original sequence was. Equivalently, one says a module is faithfully flat is it is flat and a module $M$ is nonzero if and only if the module $M\otimes N$ is nonzero.

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

    because the higher [[derived functor in homological algebra|derived functors]] of an [[exact functor]] vanish;

1. $N$ is flat precisely if $N$ is an [[acyclic object]] with respect to the tensor product functor;

   because the [[Tor]] functor is symmetric in both arguments and an object is called tensor-[[acyclic object]] if all its positive-degree $Tor$-groups vanish.

=--

The condition in def. \ref{FlatModule} also has a number of not so immediate equivalent reformulations. These we discuss in detail below in _[Equivalent characterizations](#EquivalentCharacterizations)_. One of them gives an explicit characterization of flat modules in terms of relations beween their elements.  An exposition of this we give now in _[In terms of identities](#InTermsOfIdentities)_.



### Explicitly in terms of identities
 {#InTermsOfIdentities}

There is a characterisation of flatness that says that a left $A$-module $M$ is flat if and only if "everything (that happens in $M$) happens for a reason (in $A$)". We indicate now what this means. Below in prop. \ref{RelationsFromCharacterizationonIdealInclusion} it is shown how this is equivalent to def. \ref{FlatModule} above.

The meaning of this is akin to the existence of [[basis of a vector space|bases in vector spaces]].  In a [[vector space]], say $V$, if we have an identity of the form $\sum_i \alpha_i v_i = 0$ then we cannot necessarily assume that the $\alpha_i$ are all zero.  However, if we choose a basis then we can write each $v_i$ in terms of the basis elements, say $v_i = \sum_j \beta_{i j} u_j$, and substitute in to get $\sum_{i j} \alpha_i \beta_{i j} u_j = 0$.  Now as $\{u_j\}$ forms a basis, we can deduce from this that for each $j$, $\sum_i \alpha_i \beta_{i j} = 0$.  These last identities happen in the coefficient field, which is standing in place of $A$ in the analogy.

When translating this into the language of modules we cannot use bases so we have to be a little more relaxed.  The following statement is the right one.

Suppose there is some identity in $M$ of the form $\sum_i a_i m_i = 0$ with $m_i \in M$ and $a_i \in A$.  Then there is a family $\{n_j\}$ in $M$ such that every $m_i$ can be written in the form $m_i = \sum_j b_{i j} n_j$ and the coefficients $b_{i j}$ have the property that $\sum_i a_i b_{i j} = 0$.

The module $M$ being flat is equivalent to being able always to do this.

There is an alternative way to phrase this which is less element-centric.  The elements $m_i$ correspond to a [[morphism]] into $M$ from a [[free module]], say $m \colon F \to M$.  The $a_i$ correspond to a morphism $a \colon R \to F$, where 1 maps to the tuple whose $i$th term is $a_i$.  That we have the identity $\sum_i a_i m_i = 0$ says that the composition $m a$ is zero, or that $m \colon F \to M$ factors through the [[coequaliser]] of $a$ and $0$.  

Now we consider the elements $n_j$.  These define another morphism from a free module, say $n \colon E \to M$.  That the $m_i$ can be expressed in terms of the $n_j$ says that the morphism $m$ factors through $n$.  That is, there is a morphism $b \colon F \to E$ such that $m = n b$.  We therefore have two factorisations of $m$: one through $n$ and one through the [[cokernel]] $\coker a$.  The question is as to whether these have any relation to each other.  In particular, does $\coker a \to M$ factor through $n$?  We can represent all of this in the following diagram.

+-- {: style="text-align:center"}
<svg width="222" height="136" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="14804">
 <g>
  <title>Layer 1</title>
  <foreignObject height="24.000001" width="30" font-size="16" id="svg_14804_1" y="56" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>R</mi>
     </mrow>
     <annotation encoding="application/x-tex">R</annotation>
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

By theorem \ref{CharacterizationOnIdealInclusions} $N$ is flat precisely if $I \otimes_R N \to N$ is an injection. This in turn is the case precisely if the only element of the tensor product $I \otimes_R R$ that is 0 in $R \otimes_R N = N$ is already 0 on $I \otimes_R N$.

Now by definition of [[tensor product of modules]] an element of $I \otimes_R N$ is of the form $\sum_i (r_i ,n_i)$ for some $\{n_i \in N\}$. Under the inclusion $I \otimes_R N \to N$ this maps to the actual linear combination $\sum_i r_i n_i$. This map is injective if whenever this linear combination is 0, already $\sum_i (r_i, n_i)$ is 0.

But the latter is the case precisely if this is equal to a combination $\sum_j (\tilde r_j  , \tilde n_j)$ where all the $\tilde r_j$ are 0. This implies the claim.

=--

Taking this a step further, we consider the [[filtered category|filtered family]] of all finite [[subsets]] of $M$.  This generates a filtered family of [[finitely generated module|finitely generated]] [[free modules]] with compatible morphisms to $M$.  So there is a morphism from the [[colimit]] of this family to $M$.  This morphism is [[surjection|surjective]] by construction.  To show that it is [[injection|injective]], we need to show that any element in one of the terms in the family that dies by the time it reaches $M$ has actually died on the way.  This is precisely what the above characterisation of flatness is saying: the element corresponding to $\sum_i a_i m_i$ that dies in $M$ is already dead by the time it reaches $E$.

We have thus arrived at the following result: 

+-- {: .num_theorem #filtfree} 
###### Theorem 
A module is flat if and only if it is a [[filtered colimit]] of finitely generated [[free modules]]. 
=-- 

This observation (Wraith, Blass) can be put into the more general context of modelling [[geometric theory|geometric theories]] by [[geometric morphism|geometric morphisms]] from their [[classifying topos|classifying toposes]], or equivalently, certain [[flat functor|flat functors]] from [[site|sites]] for such topoi.

### For more general rings

Even if the [[ring]] $R$ is not necessarily commutative and not necessarily unital, we can say: 

A left $R$-[[module]] is flat precisely if the [[tensor product of modules|tensoring]] functor

$$
  (-)\otimes_R \colon Mod_R \to Ab
$$

from _right_ $R$ modules to [[abelian groups]] is an [[exact functor]].


##  General properties

### Properties of the category of flat modules

\begin{proposition}
The full subcategory of flat modules over a ring $R$ is stable under
the following categorical constructions :

1. (infinite) sums ;
1. filtered colimits ;
1. retracts;
1. tensor product.

\end{proposition}

+-- {: .num_prop #ProjectiveModulesAreFlat}
###### Corollary

Every [[projective module]] is flat.

=--

+-- {: .proof}
###### Proof

Every projective module is a retract of a free module, which in turn is a sum of copies of the base ring $R$, which is flat over itself.

=--

\begin{corollary}
Let $R$ be a commutative ring and $S \subset R$ be a multiplicative subset.
Then the localisation $R[S^{-1}]$ is a flat $R$-module. 
\end{corollary}

\begin{proof}
Regard the set $S$ as a poset with de divisibility relation. The fact that $S$ be multiplicative means that the poset is directed.
One thus have that $R[S^{-1}] = \underset{\longrightarrow}{\lim}_s \;\frac{1}{s} \; R$ is a filtered colimit of free modules, hence it is flat.
\end{proof}

### Flatness is a local property

\begin{proposition}(Stability under base change)
Let $R \to S$ be a morphism of commutative rings and let $M$ be a flat $R$-module, then the $S$-module $M \otimes_R S$ is also flat.
\end{proposition}

\begin{proof}
Let $X \to Y$ be an injective morphism of $S$-modules, then
the map $(M \otimes_R S) \otimes_S X \to (M \otimes_R S) \otimes_S Y$ is
isomorphic to the map $M \otimes_R X \to M \otimes_R Y$ which is injective because $M$ is flat.
\end{proof}

\begin{proposition}(Flatness is a local property)
Let $R$ be a commutative ring and let $M$ be an $R$-module. Then the following assertions are equivalent :

1. $M$ is flat;
1. $M_\mathfrak{p}$ is a flat $R_\mathfrak{p}$-module, for every prime ideal $\mathfrak{p} \subset R$;
1. $M_\mathfrak{m}$ is a flat $R_\mathfrak{m}$-module, for every maximal ideal $\mathfrak{m} \subset R$.

\end{proposition}

\begin{proof}

$1 \Rightarrow 2$. By base change.

$2 \Rightarrow 3$. Obvious.

$3 \Rightarrow 1$. Let $X \to Y$ be an injective morphism of $R$-modules and let $K$ denote the kernel of the induced map $M \otimes_R X \to M \otimes_R Y$. Since $R_\mathfrak{m}$ is a flat $R$-module it follows that
$X_\mathfrak{m} \to Y_\mathfrak{m}$ is also injective ; and $K_\mathfrak{m}$ is the kernel of $M_\mathfrak{m} \otimes_{R_\mathfrak{m}} X_\mathfrak{m}\to M_\mathfrak{m} \otimes_{R_\mathfrak{m}} Y_\mathfrak{m}$.
By the flatness assumption, we deduce that $K_\mathfrak{m} = 0$ for every maximal ideal $\mathfrak{m} \subset R$, so $K = 0$ and $M$ is flat.
\end{proof}

### Flat modules are torsion-free

\begin{proposition}
For any module $M$ over a ring $R$, one has
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Rightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is torsion-free}
  \,.
$$
\end{proposition}

\begin{proof}
For every regular element $p \in R$, the $p$-torsion submodule of $M$ is isomorphic to $\mathrm{Tor}^R_1(M, R/(p))$.
\end{proof}

The converse holds for semi-hereditary rings.

## Reduction to cyclic modules

\begin{theorem}(Reduction to cyclic modules)
Let $R$ be a commutative ring and let $M$ be an $R$-module.
If
$$
  Tor_1^R(M, R/I) = 0
$$
for every finitely generated ideal $I \subset R$, then $M$ is a flat $R$-module.

Equivalently, if
$$
  I \otimes_R M \to IM
$$
is an isomorphism for every finitely generated ideal $I \subset R$, then
$M$ is flat.
\end{theorem}

\begin{proof}
The proof goes in 3 steps.

1. $Tor_1^R(M, R/I) = 0$ for every ideal $I \subset R$. Indeed, write $I$ as the union of the finitely generated ideals $I_\mathrm{fin} \subset I$, then $R/I = \underset{\longrightarrow}{\lim}_{I_\mathrm{fin} \subset I} R/I_\mathrm{fin}$. Then
because $Tor_1$ commutes with filtered colimits
$$
  Tor_1(M, R/I) = Tor_1(M, \underset{\longrightarrow}{\lim}_{I_fin \subset I} R/I_fin) = \underset{\longrightarrow}{\lim}_{I_fin \subset I} Tor_1(M, R/I_fin) = 0
$$
1. $Tor_1^R(M, X) = 0$ for every finitely generated module $X$. We can show this by induction on the number of generators of the module. The case of $n = 1$ generator is covered by the previous step. Assume that $Tor_1(M, X) = 0$ for every module generated by $n$ elements. Let $X$ be generated by $n+1$ elements $x_0, \dots, x_n$. Let us call $Y$ the submodule of $X$ generated by $x_1, \dots, x_n$, then one has a short exact sequence $0 \to Y \to X \to X/Y \to 0$ leading to the sequence
$$
  0 = Tor_1(M, Y) \to Tor_1(M, X) \to Tor_1(M, X/Y) = 0 
$$
which is exact in the middle, so $Tor_1(M, X) =  0$.
1. For the last step, we use the fact that every module is the union of its finitely generated submodules and that $Tor_1(M,-)$ commutes with filtered colimits.
$$
  Tor_1(M, X) = Tor_1\left(M, \bigcup_{X_fin \subset X} X_fin\right) = \underset{\longrightarrow}{\lim}_{X_fin \subset X} Tor_1(M, X_fin) = 0
$$
for every module $X$.

The equivalence with the second characterisation comes from the fact that
using the exact sequence $0 \to I \to R \to R/I \to 0$ and tensoring it with $M$, one gets the long exact sequence
$$
  0 \to Tor_1(M, R/I) \to I \otimes R \to R \to R/I \to 0
$$
identifying $Tor_1(M, R/I)$ as the kernel of the always surjective map
$I \otimes M \to IM \subset R$. 
\end{proof}

## Finitely generated flat modules

Thanks to the general structure theorem of flat modules, one gets

\begin{corollary}
Given a [[finitely presented]] module $M$, one has
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is projective}
  \,.
$$
\label{FinitelyPresentedFlatIsProjective}
\end{corollary}

\begin{proof}
If $M$ is at the same time finitely presented and a filtered colimit of finitely generated free modules, the identity morphism $M \to M$ must factor as $M \to F \to M$ where $F$ is a finitely generated free module. This implies that $M$ is projective.
\end{proof}

In many cases, “finite presentation” can be replaced with “finite generation”.

\begin{proposition}(When $R$ is local)

Let $M$ be a [[finitely generated module]] over a [[local ring]] $R$.
Then one has
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is free}
  \,.
$$

\end{proposition}

This is [Matsumara, Theorem 7.10](#Matsumara).

Thus we see that finitely generated flat modules are locally free in the weak sense. Let us recall the definition of locally free modules and their relation with projective modules.

+-- {: .num_defn #LocallyFreeModule}
###### Definition

An $R$-module $M$ is called a **locally free module in the weak sense** if for every [[prime ideal]] $\mathfrak{p} \hookrightarrow R$ the localised module $M_\mathfrak{p}$ is a [[free module]] over the [[localization of a ring|localization]] $R_\mathfrak{p}$. 

=--

\begin{proposition}
Let $M$ be a [[finitely generated module]], then the following are equivalent :

1. $M$ is projective ;
1. $M$ is locally free in the weak sense and the rank function $\mathfrak{p} \mapsto \mathrm{r}(\mathfrak{p})$ is locally constant.

\end{proposition}

Then one has the following characterisation of finitely generated flat modules.

\begin{proposition}
Let $M$ be a [[finitely generated module]], then
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is locally free in the weak sense}
  \,.
$$
\end{proposition}

This characterisation can be strengthened in two very large cases

\begin{proposition}(When $R$ is Noetherian)
If $R$ is a [[Noetherian ring]] and $M$ is a [[finitely generated module]], then
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is projective}
  \,.
$$
\end{proposition}

\begin{proof}
Over a Noetherian ring all finitely generated modules are finitely presented.
So this is a simple consequence of Corollary (\ref{FinitelyPresentedFlatIsProjective})
\end{proof}

\begin{proposition}(When $R$ is an integral domain)
If $R$ is an [[integral domain]] and $M$ is a [[finitely generated module]], then
$$ 
  M\;\text{is flat}
  \;\;\;\;\;\;\;\;
  \Leftrightarrow
  \;\;\;\;\;\;\;\;
  M\;\text{is projective}
  \,.
$$
\end{proposition}

\begin{proof}
Given two prime ideals $\mathfrak{p} \subset \mathfrak{q}$, one gets
$\mathrm{r}(\mathfrak{p}) = \mathrm{r}(\mathfrak{q})$.
Since $R$ is an integral domain $(0)$ is a prime ideal and $(0) \subset \mathfrak{p}$ for every prime ideal $\mathfrak{p}$.
The function $\mathfrak{p} \mapsto \mathrm{r}(\mathfrak{p})$ is thus constant.
\end{proof}

\begin{remark}
The proof of the above proposition shows that the same result is true for every ring $R$ with a unique minimal ideal.
\end{remark}

In the general case, it is not true that all finitely generated flat modules are projective.

\begin{example}([[counter-example]])
Let $R = \prod_{i = 0}^\infty k$ be an infinite product of fields.
Let $I = \oplus_{i = 0}^\infty k \subset R$ its ideal.

Then $R/I$ is a finitely generated $R$-module, flat (all $R$-modules are flat), but not projective.
\end{example}

The class of commutative rings $R$ over which all finitely generated flat modules are projective has been determined in the 1970s.

\begin{theorem}
Let $R$ be a commutative ring. The following two are equivalent :

1. Every finitely generated flat $R$-module is projective ;
1. Every sequence $(a_0, a_1, \dots)$ of elements of $R$ such that
$a_{n+1} a_n = a_n$ for every $0 \leq n$, is eventually constant.

\end{theorem}

One can see Gena Puninski; Philipp Rothmaler (2004). _When every finitely generated flat module is projective_. Journal of Algebra, 277(2), 542–558.         doi:10.1016/j.jalgebra.2003.10.027     

## Countably presented flat modules

As we have seen finitely presented flat module are always projective ; their projective dimension is equal to zero.
For countably presented flat modules, the dimension cannot exceed one.

\begin{theorem}
A countably presented flat module has [[projective dimension]] inferior or equal to $1$.
\end{theorem}

\begin{proof}
Let $M$ be a countably generated flat module. Being flat, it can be written as an inductive limit of finitely generated free modules $M = \underset{\longrightarrow}{\lim}_A M_\alpha$. Since $M$ is also countably presented, there exists a countable cofinal filtered subset $H \subset A$, so one can reduce to the case where $A = \mathbb{N}$.

Denoting by $g_n : M_n \to M_{n+1}$ the transition maps, one can build the short exact sequence
$$
  0 \to \oplus M_n \overset{G}{\to} \oplus M_n \to M \to 0
$$
where the map $G$ restricted to $M_n$ is given by $1 - g_n$.
\end{proof}

## Classes of rings, related to flatness

As we have seen, there is not much difference between flat modules and projective modules in the finitely generated case.
The notion of flatness starts becoming really distinct in the case of infinitely generated modules. For example the $\mathbb{Z}$-module $\mathbb{Q}$ is flat (since it is torsion-free) but far from being free.

On the other side, for infinitely generated module, the notion of projectivity is less useful since for example the module $\mathbb{Z}[[X]]$ which is the infinite product of copies of $\mathbb{Z}$ is _not free_ but still flat.
It is common to encounter infinitely generated flat modules and uncommon to encounter infinitely generated projective modules.

To better understand the general notion of flatness from a geometric perspective, very early after the definition of the notion, two questions have been asked

1. A product of torsion-free modules is always torsion-free, is it true for flat modules ?
1. What type of rings $R$ have all their modules flat?
1. For what type of rings $R$ is it true that all torsion-free modules are flat?
1. For what type of rings can flat modules be the filtered union of their finitely generated projective submodules?


### Coherent rings

\begin{proposition}
For a commutative ring $R$, the following propositions are equivalent :

1. $R$ is a [[coherent ring]] ;
1. the product of a family of flat $R$-modules is flat.

\end{proposition}

\begin{proof}

$1 \Rightarrow 2$. Let $\{Q_\alpha\}_{\alpha \in A}$ be a set of flat $R$-modules. By cyclic reduction, we only need to show that the map $I \otimes \prod_\alpha Q_\alpha \to \prod_\alpha Q_\alpha$ is injective for every finitely generated ideal $I \subset R$. Since $R$ is coherent every such ideal $I$ is a [[finitely presented module]] and thus the map $I \otimes \prod_\alpha Q_\alpha \to \prod_\alpha Q_\alpha$ is the product of the maps $I \otimes Q_\alpha \to Q_\alpha$. It is injective since each individual map is injective by flatness of each $Q_\alpha$. 

$2 \Rightarrow 1$. Let $I \subset R$ be a finitely generated ideal.
Using one of the equivalent characterisations of [[finitely presented modules]], we shall show
that the canonical map
$I \otimes R^A \to I^A$ is an isomorphism, for every set $A$.
By assumption, since $R^A$ is a flat module, the map $I \otimes R^A \to R^A$ is injective and since $I$ is finitely generated, its image is $I^A$.
\end{proof}

### Absolutely flat rings

\begin{definition}
We say that a ring $R$ is absolutely flat if every $R$-module is flat.
\end{definition}

\begin{theorem}
The following propositions are equivalent for a commutative ring $R$:

1. $R$ is absolutely flat;
1. every ideal $I \subset R$ is idempotent, i.e. $I^2 = I$;
1. for every $x \in R$ there exists an element $y \in R$ such that $x = x^2 y$ ;
1. $R_\mathfrak{p}$ is a field for every prime ideal $\mathfrak{p} \subset R$;
1. $R_\mathfrak{m}$ is a field for every maximal ideal $\mathfrak{m} \subset R$.

\end{theorem}

\begin{proof}
1 $\Rightarrow$ 2. Let $I \subset R$ be any ideal of $R$, then since $R$ is absolutely flat, the $R$-module $R/I$ must be flat.
One has
$$
  Tor_1(R/I, R/I) \simeq I/{I^2}
$$
the ideal $I$ must thus be idempotent;

2 $\Rightarrow$ 3. For every $x \in R$, the ideal $(x)$ must be idempotent, that is $(x)(x) = (x)$ which means that there must exist $y$ such that $x = x^2y$;

3 $\Rightarrow$ 4. Let $r \in \mathfrak{p}$. Let $u \in R$ such that $r u r = r$. Then $r ( 1 - u r ) = 0$. Since $u r \in \mathfrak{p}$ it follows that the image of $1- u r$ is invertible in $R_\mathfrak{p}$, so the image of $r$ is null in $R_\mathfrak{p}$. Thus the maximal ideal $R_\mathfrak{p}$ is trivial.

4 $\Rightarrow$ 5. Obvious.

5 $\Rightarrow$ 1. Because flatness is a local property.

\end{proof}

### Semi-hereditary rings

\begin{definition}
Recall that a commutative ring $R$ is  [[semi-hereditary]] if every finitely generated ideal is projective.
\end{definition}


\begin{theorem}
For a commutative ring $R$, the following are equivalent :

1. $R$ is [[semi-hereditary]] ;
1. The total ring of fractions $\mathrm{Q}(R)$ of $R$ is absolutely flat and for every maximal ideal $\mathfrak{m}$ of $R$, the local ring $R_\mathfrak{m}$ is a [[valuation ring]] ;
1. Every torsion-free $R$-module is flat.

\end{theorem}

\begin{proof}
First, if $R$ is a local ring, this follows from the equivalent characterisations of [[valuation rings]]. So we only need to take care of the global part of the theorem.

$1 \Rightarrow 2$. Every $R_\mathfrak{m}$ is a localisation of $R$, so it is semi-hereditary and hence a valuation ring.
To show that $\mathrm{Q}(R)$ is absolutely flat, it shall be enough to show that for every $x \in R$, there exists a regular $r$ such that $x^2 = r x$. Let $x \in R$, then $(x)$ is projective. As a consequence the annihilator $Ann(x) \subset R$ is a direct summand, so there exists an idempotent $\pi \in R$ such that $Ann(x) = (\pi)$. Then $r \coloneqq x + \pi$ is a regular element such that $x^2 = r x$.

$2 \Rightarrow 3$. When $\mathrm{Q}(R)$ is absolutely flat, being torsion-free becomes a local property, as it is for flatness.

$3 \Rightarrow 1$. Torsion-free modules are stable under product, so it follows that flat modules are also stable under product which means that $R$ is coherent. Then every finitely generated ideal $I \subset R$ is finitely presented. Since they are also torsion-free, they are flat and thus projective.
\end{proof}
## Examples
 {#Examles}

\begin{example}
Since $\mathbb{Z}$ is a [[PID]], an [[abelian group]] is flat (regarded as a $\mathbb{Z}$-module) precisely if it is [[torsion subgroup|torsion-free]].

In particular, the modules $\mathbb{Q}$ and $\mathbb{Z}[[X]]$ are flat.
\end{example}

\begin{example}
The ring of power series $R[[X]]$ (which as an $R$-module is simply an infinite product of the base ring) is an interesting example.

1. It is always torsion-free;
1. it is a flat $R$-module if and only if $R$ is a [[coherent ring]];
1. it is almost never free. In particular $\mathbb{Z}[[X]]$ is not free.

\end{example}

For the flatness of $R[[X]]$ see [_Direct products of modules_, Theorem 2.1](#Chase).

\begin{example}
Let $R$ be an integral domain, with field of fractions $K$. Then $K$ is a flat $R$-module, as it can be written as the filtered colimit
$$
  K = \underset{\longrightarrow}{\lim}_r \;\frac{1}{r}\;R
$$
of free $R$-modules.
\end{example}

\begin{example}
If $\pi$ is an idempotent element of a commutative ring $R$, then
the cyclic module $R/(\pi)$ is projective, hence flat.
\end{example}

## Related concepts

* [[flat morphism of schemes]]

* [[flat resolution lemma]]

* [[projective object]], [[projective presentation]], [[projective cover]], [[projective resolution]]

* [[injective object]], [[injective presentation]], [[injective envelope]], [[injective resolution]]

  * [[injective module]]

* [[free object]], [[free resolution]]
 
* flat object, [[flat resolution]]

* [[free module]] $\Rightarrow$ [[projective module]] $\Rightarrow$ **flat module** $\Rightarrow$ [[torsion-free module]]






## References

Flat modules (“modules plats” in French) where first defined in [[GAGA]]

* Jean-Pierre Serre, _Géométrie Algébrique et Géométrie Analytique_ ([pdf](http://www.numdam.org/article/AIF_1956__6__1_0.pdf))
{#GAGA}

Original articles include

* Shizuo Endo, _On flat modules over commutative rings_,  J. Math. Soc. Japan Volume 14, Number 3 (1962), 284-291. ([EUCLID](http://projecteuclid.org/euclid.jmsj/1261060583))

* Shizuo Endo, _On semi-hereditary rings_,  J. Math. Soc. Japan Vol. 13, No. 2, 1961

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

* Stephen Chase, _[Direct product of modules](https://www.ams.org/journals/tran/1960-097-03/S0002-9947-1960-0120260-3/S0002-9947-1960-0120260-3.pdf)
{#Chase}

[[!redirects flat modules]]

[[!redirects faithfully flat module]]
[[!redirects faithfully flat modules]]

