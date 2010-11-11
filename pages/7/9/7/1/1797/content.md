# Adjoint equivalences
* table of contents
{: toc}

## Idea

An adjoint equivalence is a more "coherent" or "structured" notion of [[equivalence]], in which the isomorphisms relating composites to identities are required to satisfy coherence laws (the triangle identities for an [[adjunction]]).

## Definition

An **adjoint equivalence** between [[categories]] is an [[adjunction]] $f\dashv g$ in which the unit and counit are [[natural isomorphisms]].  It follows that it is an [[equivalence of categories]].  Moreover, the inverses of the unit and the counit form the counit and unit, respectively, of an adjunction $g\dashv f$.

There is an identical definition internal to any [[2-category]], which reproduces the above notion when applied in [[Cat]].

## Properties

Although an adjoint equivalence is a "stronger" notion than a mere equivalence, the property of "being adjoint equivalent" is no stronger a condition than "being equivalent," since every equivalence may be refined to an adjoint equivalence by modifying one of the natural isomorphisms involved.  More specifically:

+--{: .un_theorem}
###### Theorem
If $(f,g,\eta\colon 1 \cong g f,\varepsilon \colon f g \cong 1)$ is an equivalence in a 2-category, then there is a unique 2-isomorphism $\varepsilon'\colon f g \cong 1$ such that $(f,g,\eta,\varepsilon')$ is an adjoint equivalence.
=--
+--{: .proof}
###### Proof
Since $\eta$ is an isomorphism, it is easy to see that the [[triangle identities]], together with the fact that $f$ and $g$ are equivalences, forces uniqueness of $\varepsilon'$ if it exists.  To show it exists, we take the composite
$$
f g
\xrightarrow{f g \varepsilon^{-1}} f g f g
\xrightarrow{f \eta^{-1}} f g
\xrightarrow{\varepsilon} 1
$$
In [[string diagram]] notation, with strings progressing up the page and 1-morphisms progressing from left to right, if we draw $\eta$ as a cup and $\varepsilon$ as a cap, then this $\varepsilon'$ is the following composite:

<svg width="250" height="300" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="18130">
 <g>
  <title>Layer 1</title>
  <path fill-opacity="0" id="svg_18130_1" d="m142,272l0,-113c0.333344,-94 -61.333344,-88 -62,3c-1,79.333344 -66,65.666656 -63,-5c2,-163.333344 185,-171.666656 186,2l1,119" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="#ff0000"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_18130_3" y="275" x="193">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>f</mi>
     </mrow>
     <annotation encoding="application/x-tex">f</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_18130_4" y="273" x="125">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>g</mi>
     </mrow>
     <annotation encoding="application/x-tex">g</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_18130_5" y="219" x="43">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msup>
       <mi>&#949;</mi>
       <mrow>
        <mo rspace="0em" lspace="verythinmathspace">&#8722;</mo>
        <mn>1</mn>
       </mrow>
      </msup>
     </mrow>
     <annotation encoding="application/x-tex">\varepsilon^{-1}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_18130_6" y="69" x="102">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msup>
       <mi>&#951;</mi>
       <mrow>
        <mo rspace="0em" lspace="verythinmathspace">&#8722;</mo>
        <mn>1</mn>
       </mrow>
      </msup>
     </mrow>
     <annotation encoding="application/x-tex">\eta^{-1}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_18130_7" y="9" x="100">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>&#949;</mi>
     </mrow>
     <annotation encoding="application/x-tex">\varepsilon</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
</svg>

Verifying that this definition of $\varepsilon'$ works is also easiest in string diagram notation.
=--

In [[Categories Work]], IV.4, there is a different proof of the weaker fact that if a [[functor]] $f$ is part of an equivalence, then it is part of an adjoint equivalence.  This proof is given in [[Cat]], but can be applied representably to any 2-category.

Since adjoints are unique up to unique isomorphism when they exist, it follows that any adjunction involving one functor which is an equivalence must be an adjoint equivalence.  Therefore, for a fixed morphism $f$, the "category of adjoint equivalence data $(f,g,\eta,\varepsilon)$" is either empty (if $f$ is not an equivalence) or equivalent to the [[terminal category]] (if $f$ is an equivalence).  In other words, it is a [[(-1)-category]].  In this sense "being part of an adjoint equivalence" is a [[property]] of a 1-morphism in a 2-category.

## Remarks

* One instance of the usefulness of adjoint equivalences is that the "[[walking structure|walking]] adjoint equivalence" 2-category is equivalent to the [[point]], and thus can be used as an [[interval object]] in $2Cat$, but this is not true of the "walking non-adjoint equivalence."

## In higher category theory

In [[higher category theory]], one expects to have a similar "fully coherent" notion of "adjoint equivalence" in any [[n-category]] or [[infinity-category]], and one hopes to prove a similar theorem that any [[equivalence]] can be refined to an adjoint equivalence.  This is known to be true at least in the following cases:

* For [[Gray-categories]], the statement and proof is in [[Steve Lack]]'s paper [1001.2366](http://arxiv.org/abs/1001.2366) on the [[model structure for Gray-categories]].  See [[adjoint 2-equivalence]].

* For [[strict omega-categories]], more or less this fact can be found in the study of "generic squares" in the paper [0712.0617](http://arxiv.org/abs/0712.0617) on the [[model structure for strict omega-categories]].

* For [[quasicategories]], the theorem is true, where an "adjoint equivalence" means simply a map out of the [[nerve]] of the [[interval groupoid]]; see [[equivalence in a quasicategory]].

[[!redirects adjoint equivalences]]
