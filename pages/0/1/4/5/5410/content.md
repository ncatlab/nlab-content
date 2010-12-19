
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Two-sided fibrations

* table of contents
{:toc}

## Idea

Just as a [[Grothendieck fibration]] $E\to B$ is an alternate way to encode a [[pseudofunctor]] $B^{op}\to $ [[Cat]], a *two-sided fibration* $A \leftarrow E \to B$ is a way to encode a pseudofunctor $A\times B^{op}\to Cat$.

## Definition


+-- {: .un_defn}
###### Definition

A **two-sided discrete fibration** is a [[span]] $q \colon E \to A$, $p \colon E \to B$ of [[categories]] and [[functors]] such that 
1. each $b \to p e$ in $B$ has a unique lift in $E$ that has codomain $e$ and is in the fiber over $q e$
1. each $q e \to a$ in $A$ has a unique lift in $E$ that has domain $e$ and is in the fiber over $p e$
1. for each $f\colon e \to e'$ in $E$, the codomain of the lift of $q f$ equals the domain of the lift of $p f$ and their composite is $f$.

=--

+-- {: .un_defn}
###### Definition


A **two-sided fibration** is a span $q \colon E \to A$, $p \colon E \to B$ such that
1. each $b \to p e$ in $B$ has a [[cartesian morphism|cartesian]] lift in $E$ with codomain $e$ and lying in the fiber over the identity at $q e$
1. each $q e \to a$ in $A$ has an opcartesian lift in $E$ with domain $e$ and lying in the fiber over the identity at $p e$
1. for each $f \colon e \to e'$ in $E$ the canonical arrow between the codomain of any opcartesian lift of $q f$ as in (2) and the domain of the cartesian lift of $pf$ as in (1) is an [[isomorphism]].

=--

## Properties

Write $DFib(A,B)$ for the full [[subcategory]] on the category $Span(A,B)$ of  [[span]]s on the 2-sided discrete fibrations.

+-- {: .un_prop}
###### Proposition

There is an [[equivalence of categories]]

$$
  DFib(A,B) \simeq [B^{op} \times A, Set]
$$

[[pseudo-natural transformation|pseudo-natural]] in $A, B \in Cat$.


=--

This appears as ([Riehl, theorem 2.3.2](#Riehl)).

+-- {: .proof}
###### Proof

Given a 2-sided fibration 

$$
  A \stackrel{q}{\leftarrow} E \stackrel{p}{\to} B
$$

define $F_E : B^{op} \times A \to Set$ by

$$
  F_E : (b,a) \mapsto E_{a,b} 
  \,.
$$

Conversely, given

$$
  F : B^{op} \times A \to Set
$$

let the objects of $E_F$ be triples $(a \in A, b \in B, v \in F(b,a))$ and morphisms $(b,v,a) \to (b', v', a')$ be pairs of arrows $f : a \to a'$ and $g : b' \to b$ such that $F(g,f)(v) = v'$.

One checks that these two constructions are indeed weakly inverse to each other.

=--

Given a profunctor $F : B^{op} \times A \to Set$ let 
$p : K_F \to \Delta[1]$ be its [[collage]]. 

For $S, T$ two [[simplicial set]]s write $S \star T$ for their [[join of simplicial sets]]. Write $[n] \in$ [[sSet]] for the simplicial $n$-[[simplex]].


+-- {: .un_prop}
###### Proposition

The two-sided fibration $E_F$ defined above is the category whose

* objects are morphisms of [[simplicial set]]s $[0] \star [0] \to N(K)$
  such that the first copy of $[0]$ lands in the fiber $p^{-1}(0)$
  and the second copy in the fiber $p^{-1}(1)$.

* morphisms are morphisms of [[simplicial set]]s $[1] \star [1] \to N(K)$
  such that the first copy of $[1]$ lands in the fiber $p^{-1}(0)$
  and the second copy in the fiber $p^{-1}(1)$.

=--

+-- {: .proof}
###### Proof

We have canonical [[isomorphism]]s of simplicial sets

* $[0] \star [0] \simeq \Delta[1]$

* $[1] \star [1] \simeq \Delta[3]$.

From the first one the statement about the objects is evident. For the second one, notice the explicit identification, as exibited by the following diagram:



$$
\begin{gathered}
\begin{matrix}
0\overset{g}{\longrightarrow}1\\
\\
0'\underset{f}{\longrightarrow}1'
\end{matrix}
\overset{\quad g\star f\quad}{\longrightarrow}
\array{\arrayopts{\rowalign{center}} 
\begin{svg}
<svg width="96" height="116" xmlns="http://www.w3.org/2000/svg" se:nonce="91144" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw1" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000"/>
  </marker>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_91144_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g display="inline">
  <title>Layer 1</title>
  <rect fill-opacity="0.25" stroke-width="2" fill="#000000" id="svg_91144_6" height="80.249997" width="80.75" y="19.875" x="6.375"/>
  <path stroke-width="2" fill-opacity="0.15" fill="#000000" id="svg_91144_7" d="m6.625,20.25l80.25,80.027077l-80.25,0.222923"/>
  <ellipse fill-opacity="0.5" ry="7.625" rx="7.375" stroke-width="2" fill="#ffffff" id="svg_91144_12" cy="99.874999" cx="87.125"/>
  <ellipse fill-opacity="0.5" id="svg_91144_11" ry="8.374999" rx="8.3125" stroke-width="2" fill="#ffffff" cy="99.625" cx="9.3125"/>
  <ellipse fill-opacity="0.5" id="svg_91144_10" ry="6.875" rx="6.4375" stroke-width="2" fill="#ffffff" cy="21.75" cx="86.187501"/>
  <ellipse fill-opacity="0.5" ry="6.75" rx="5.5625" stroke-width="2" fill="#ffffff" id="svg_91144_1" cy="21.75" cx="7.0625"/>
  <polyline se:connector="svg_97259_9 svg_97259_2" marker-end="url(#se_arrow_91144_fw)" stroke-dasharray="2,2" fill="none" stroke-width="2" stroke="#000000" points="79.2069,28 47.9784,60.0575 16.75,92.115" id="svg_91144_2"/>
  <polyline se:connector="svg_97259_1 svg_97259_9" id="svg_97259_23" points="12.375,19.75 45.125,19.75 77.875,19.75" stroke="#000" stroke-width="2" fill="none" marker-end="url(#se_arrow_fw1)"/>
  <line marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_91144_4" y2="90" x2="6.375" y1="28.25" x1="6.375"/>
  <line id="svg_91144_5" marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" y2="90" x2="86.875" y1="28.25" x1="86.875"/>
  <line marker-end="url(#se_arrow_91144_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_91144_8" y2="93.999999" x2="80.250002" y1="25.25" x1="11.375"/>
  <foreignObject height="20" width="16" font-size="16" id="svg_91144_13" y="96.25" x="35">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>g</mi>
     </mrow>
     <annotation encoding="application/x-tex">g</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line x1="17.374999" y1="100" x2="78" y2="100" id="svg_91144_14" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_91144_fw)"/>
 </g>
 <g>
  <title>Layer 2</title>
  <foreignObject x="1.875" y="91.75" font-size="16" width="14" height="16" id="svg_97259_2">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">0'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="81.875" y="91.75" font-size="16" width="14" height="16" id="svg_97259_16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">1'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="78" y="12" font-size="16" width="18" height="16" id="svg_97259_9">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="12" id="svg_97259_1" font-size="16" width="12" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="16" font-size="16" id="svg_91144_9" y="0" x="35">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>f</mi>
     </mrow>
     <annotation encoding="application/x-tex">f</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
\end{svg}
}
\cong
\array{\arrayopts{\rowalign{center}} 
\begin{svg}
<svg width="108" height="110" xmlns="http://www.w3.org/2000/svg" se:nonce="22396" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
  <marker viewBox="0 0 10 10" id="se_arrow_22396_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <path d="m3.8125,49.25l33.375,53.125l63.125,-41.625l-62.75,-52.875l-33.75,41.375z" id="svg_4422_11" fill="#000000" stroke-width="2" stroke-dasharray="2,2" fill-opacity="0.25"/>
  <ellipse fill-opacity="0.5" cx="98" cy="63.375001" id="svg_22396_4" fill="#ffffff" stroke-width="2" rx="5.25" ry="11.125"/>
  <path d="m3.875,49.0625l35.25,55.75l0.25,-97.25" id="svg_4422_12" fill="#000000" fill-opacity="0.15" stroke-width="2" stroke-dasharray="2,2"/>
  <ellipse fill-opacity="0.5" cx="38.90625" cy="102.125" id="svg_22396_3" fill="#ffffff" stroke-width="2" rx="10.90625" ry="7.75"/>
  <ellipse fill-opacity="0.5" cx="5.25" cy="51" id="svg_22396_2" fill="#ffffff" stroke-width="2" rx="4.5" ry="7"/>
  <ellipse fill-opacity="0.5" cx="37.250001" cy="9.25" id="svg_22396_1" fill="#ffffff" stroke-width="2" rx="9.749999" ry="8.25"/>
  <line x1="8.375" y1="56.750001" x2="32.062498" y2="93.875" id="svg_22396_6" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="92.75" y1="65.875" x2="48.062501" y2="95.250001" id="svg_22396_8" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="10.000001" y1="51.5" x2="91" y2="61" id="svg_22396_9" stroke="#000000" stroke-width="2" stroke-dasharray="2,2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="39.5" y1="17.625" x2="39.375" y2="92.375" id="svg_22396_5" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="31.5" y1="16.25" x2="8.249999" y2="43.249999" id="svg_22396_10" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
  <line x1="45" y1="14" x2="92.999999" y2="53.999999" id="svg_22396_11" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_22396_fw)"/>
 </g>
 <g>
  <title>Layer 2</title>
  <foreignObject y="0" x="30.75" id="svg_4422_1" font-size="16" width="14" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
     </mrow>
     <annotation encoding="application/x-tex">0</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="92.375" y="52" id="svg_4422_4" font-size="16" width="16" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">1'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="33.25" y="94.375" id="svg_4422_2" font-size="16" width="16" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>0</mn>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">0'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="0" y="41.25" id="svg_4422_3" font-size="16" width="8" height="16">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mn>1</mn>
     </mrow>
     <annotation encoding="application/x-tex">1</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>
\end{svg}
}\\
f\cong g \cong [1] \Rightarrow f\star g \cong \Delta[3]
\end{gathered}
$$

Then recall that the [[collage]] $K$ has $K(b,a) = F(b,a)$, $K(a,a') = p^{-1}(0)(a,a')$ and $K(b',a) = p^{-1}(1)(b',b)$.

So a morphism $[1] \star [1] \to K$ subject to the given constraints is a diagram

$$
  \left(
  \array{
    b' &\stackrel{g}{\to}& b
    \\
    & {}^{v}\swarrow & 
    \\
    a &\stackrel{f}{\to}& a'
  }
  \right)
  =
  \left(
  \array{
    b'
    \\
    & {}_{v'}\searrow & 
    \\
    && a'
  }
  \right)
$$

in $K$. This expresses precisely the equation $F(g,f)(v) = v'$ that entered the above definition of $E_F$.

=--

## Related concepts

* [[Grothendieck fibration]], [[two-sided fibration]],

* [[Cartesian fibration]]

## References

The notion is originally discussed in

* [[Ross Street]], Ross Street. Fibrations and Yoneda's lemma in a 2-category. In Category Seminar (Proc. Sem., Sydney, 1972/1973), pages 104  133. Lecture Notes in Math., Vol. 420. Springer, Berlin, 1974.

* [[Ross Street]], _Fibrations in bicategories_ Cahiers Topologie G&eacute;om. Diff&eacute;rentielle,
21(2):111{160, 1980. (Corrections in 28(1):53{56, 1987)

A useful review is in

* [[Emily Riehl]], _Two-sided discrete fibrations in 2-categories and bicategories_ 2010 ([pdf](http://math.uchicago.edu/~eriehl/fibrations.pdf))
{#Riehl}

[[!redirects two-sided fibrations]]
[[!redirects two-sided discrete fibration]]
[[!redirects two-sided discrete fibrations]]
