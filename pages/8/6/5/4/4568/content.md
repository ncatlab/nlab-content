{:myproof: .proof style="margin-left:2em;"}
{:mynumdef: .num_defn style="border:solid #cccccc;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

# Infinitary Lawvere theories
* table of contents
{: toc}

## Idea

An infinitary Lawvere theory is a generalisation of a [[Lawvere theory]] to allow infinitary operations.  As a motivating example, consider the theory of [[suplattices]], where we have, for every [[cardinal number]] $n$, an operation to take the [[supremum]] of $n$ elements.

Size issues can be tricky for infinitary Lawvere theories.  Na&#239;vely, you would expect an infinitary Lawvere theory of [[complete lattices]] too, but there is none, because a smallness condition fails.  (This is connected to the nonexistence of [[free complete lattices]].)

In accordance with the [[red herring principle]], an infinitary Lawvere theory should not be thought of a special case of a [[Lawvere theory]].  To avoid this, one may call the latter a *finitary* Lawvere theory.

There are also many-sorted infinitary Lawvere theories, as well as $\kappa$-ary Lawvere theories for any [[regular cardinal]] $\kappa$.


## Definitions

A __many-sorted infinitary Lawvere theory__ is a [[locally small category]] $\mathcal{D}$ with all small [[products]] and with a small collection $\mathcal{R}$ of objects (called __sorts__) such that every object is a small product of these sorts.

Given a small [[set]] $S$, an __$S$-sorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with an $S$-indexed family $\mathcal{R}$ of objects (called __sorts__) such that every object is a small product of these sorts.  (Note that an $S$-indexed family of objects is precisely a [[functor]] to $\mathcal{D}$ from the [[discrete category]] on $S$.)

If $(\mathcal{D},\mathcal{R})$ is an $S$-sorted infinitary Lawvere theory, then $\mathcal{D}$ is a many-sorted infinitary Lawvere theory; conversely, any many-sorted infinitary Lawvere theory may be interpreted as an $S$-sorted infinitary Lawvere theory, where $S$ is (the set of isomoprhism classes of) an appropriate family $\mathcal{R}$ and the $S$-indexed family is given by the identity indexing.

An __unsorted infinitary Lawvere theory__ is a locally small category $\mathcal{D}$ with all small products and equipped with an object $R$ (so that $(\mathcal{D},R)$ is a [[pointed category]]) such that every object is [[isomorphic]] to $R^n$ for some small cardinal number $n$.  An __infinitary Lawvere theory__ is by default an unsorted infinitary Lawvere theory, invoking the [[red herring principle]].  Note that an unsorted infinitary Lawvery theory is the same thing as a $1$-sorted infinitary Lawvere theory.

We will give the definitions of further special cases for unsorted infinitary Lawvere theories, but these definitions may also be generalised to the many-sorted case.

Given a [[regular cardinal]] $\kappa$, a __$\kappa$-ary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all $n$-ary products for $n \lt \kappa$ such that every object is isomorphic to $R^n$ for some $n \lt \kappa$.  Every $\kappa$-ary Lawvere theory may be interpreted as an infinitary Lawvere theory by using the free category with all small products on $\mathcal{D}$.  More generally, every $\kappa$-ary Lawvere theory may be interpreted as a $\lambda$-ary Lawvere theory if $\kappa \leq \lambda$.

A __bounded infinitary Lawvere theory__ is an infinitary Lawvere theory which is (under the interpretation above) [[equivalence of categories|equivalent]] to some $\kappa$-ary Lawvere theory.

A __finitary Lawvere theory__ is a locally small pointed category $(\mathcal{D},R)$ with all finitary products such that every object is isomorphic to $R^n$ for some [[natural number]] $n$.  A __[[Lawvere theory]]__ is by default a finitary Lawvere theory, invoking the [[red herring principle]].  Note that a finitary Lawvere theory is the same thing as an $\aleph_0$-ary Lawvere theory.


## Size issues

[Freyd and Street (1995)](http://tac.mta.ca/tac/volumes/1995/n9/1-09abs.html) have shown that a category $\mathcal{D}$ is [[small category|small]] if and only if both $\mathcal{D}$ and the [[functor category]] $[\mathcal{D},Set]$ are locally small.  Analogously, it seems that a category $\mathcal{D}$ with products may be given the structure of a many-sorted infinitary Lawvere theory if and only if both $\mathcal{D}$ and $Prod[\mathcal{D},Set]$ (the category of [[product-preserving functor]]s from $\mathcal{D}$ to $Set$, a [[full subcategory]] of $[\mathcal{D},Set]$) are locally small.  In both cases, the 'only if' part is straightfoward, but we haven't yet proved the 'if' part.

See [the n-Forum](http://www.math.ntnu.no/~stacey/Mathforge/nForum/comments.php?DiscussionID=1673) for more preliminary results.


## Algebraic Categories

+-- {: .un_lemma}
###### Conjecture
A multi-sorted infinitary Lawvere theory $\mathcal{D}$ defines a [[monadic category]] over [[Set]] by taking the [[functor category]] consisting of all **product-preserving** covariant functors from $\mathcal{D}$ in to $Set$.
=--

Let us write this functor category as $Prod[\mathcal{D},Set]$ and start by showing that it is a [[locally small category]].

+-- {: .num_lemma #ProdLocSmall}
###### Lemma
The category $Prod[\mathcal{D},Set]$ of product-preserving functors and natural transformations is locally small.
=--

+-- {: myproof}
###### Proof
Let $V_1, V_2 \colon \mathcal{D} \to Set$ be two product-preserving covariant functors.
From the definition of a multi-sorted infinitary category we see that we may choose a set of sorts, say $S$.
Let $D_s \in \mathcal{D}$ be the image of $s \in S$.

As $S$ is a set, the product
$$
\prod_{s \in S} Set(V_1(D_s), V_2(D_s))
$$
is a set.  We define a function $[V_1,V_2] \to \prod_{s \in S} Set(V_1(D_s), V_2(D_s))$ by sending a natural transformation $\alpha \colon V_1 \to V_2$ to the product of its values at each $D_s$.  That is,
\begin{equation}
\label{natrans}
\alpha \mapsto \big(\alpha_{D_s}\big)_{s \in S}.
\end{equation}

Let $D \in \mathcal{D}$ be an arbitrary object.  From the definition of a multi-sorted infinitary Lawvere theory, there is an isomorphism
$$
d \colon D \cong \prod_{s \in S} D_s^{X_s}
$$
for some sets $X_s$.   For each $s \in S$ and $x \in X_s$, there is a projection $p_{s,x} \colon \prod_{s \in S} D_s^{X_s} \to D_s$.
As $V_1$ and $V_2$ are product-preserving, we have isomorphisms
$$
 \cong  \prod_{s \in S} V_i(D_s)^{X_s}
$$
commuting with the projections.
Thus for each $s \in S$ and $x \in X_s$, we have the following commutative diagram.

<svg width="655" height="229" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="37480">
 <g>
  <title>Layer 1</title>
  <foreignObject height="30" width="110.000001" font-size="16" id="svg_37480_1" y="48" x="175">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>1</mn>
      </msub>
      <mrow>
       <mo>(</mo>
       <msub>
        <mo rspace="thinmathspace" lspace="thinmathspace">&#8719;</mo>
        <mrow>
         <mi>s</mi>
         <mo>&#8712;</mo>
         <mi>S</mi>
        </mrow>
       </msub>
       <msubsup>
        <mi>D</mi>
        <mi>s</mi>
        <mrow>
         <msub>
          <mi>X</mi>
          <mi>s</mi>
         </msub>
        </mrow>
       </msubsup>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">V_1\left( \prod_{s \in S} D_s^{X_s}\right)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_2" height="30" width="110" font-size="16" y="48" x="370">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>2</mn>
      </msub>
      <mrow>
       <mo>(</mo>
       <msub>
        <mo rspace="thinmathspace" lspace="thinmathspace">&#8719;</mo>
        <mrow>
         <mi>s</mi>
         <mo>&#8712;</mo>
         <mi>S</mi>
        </mrow>
       </msub>
       <msubsup>
        <mi>D</mi>
        <mi>s</mi>
        <mrow>
         <msub>
          <mi>X</mi>
          <mi>s</mi>
         </msub>
        </mrow>
       </msubsup>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">V_2\left( \prod_{s \in S} D_s^{X_s}\right)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="30" width="110" font-size="16" id="svg_37480_26" y="198" x="175">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>1</mn>
      </msub>
      <mrow>
       <mo>(</mo>
       <msub>
        <mi>D</mi>
        <mi>s</mi>
       </msub>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">V_1\left(D_s\right)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_27" height="30" width="110" font-size="16" y="199" x="370">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>2</mn>
      </msub>
      <mrow>
       <mo>(</mo>
       <msub>
        <mi>D</mi>
        <mi>s</mi>
       </msub>
       <mo>)</mo>
      </mrow>
     </mrow>
     <annotation encoding="application/x-tex">V_2\left(D_s\right)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_37480_41)" id="svg_37480_41" y2="187" x2="232" y1="81" x1="230" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_37480_42" marker-end="url(#se_marker_end_svg_37480_42)" y2="188" x2="424" y1="82" x1="425" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="29.000001" width="66" font-size="16" id="svg_37480_43" y="129.999998" x="164">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>1</mn>
      </msub>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>p</mi>
       <mrow>
        <mi>s</mi>
        <mo>,</mo>
        <mi>x</mi>
       </mrow>
      </msub>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">V_1(p_{s,x})</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_44" height="29.000001" width="66" font-size="16" y="129" x="425">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>V</mi>
       <mn>2</mn>
      </msub>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>p</mi>
       <mrow>
        <mi>s</mi>
        <mo>,</mo>
        <mi>x</mi>
       </mrow>
      </msub>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">V_2(p_{s,x})</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_37480_60)" id="svg_37480_60" y2="211" x2="392.999996" y1="211" x1="262" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_37480_61" y="187" x="304">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#951;</mi>
       <mrow>
        <msub>
         <mi>D</mi>
         <mi>s</mi>
        </msub>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\eta_{D_s}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_37480_62)" id="svg_37480_62" y2="61" x2="368.000006" y1="61" x1="287.000002" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="38" width="85.000002" font-size="16" id="svg_37480_63" y="30.000002" x="284.999994">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>&#951;</mi>
       <mrow>
        <msub>
         <mo rspace="thinmathspace" lspace="thinmathspace">&#8719;</mo>
         <mrow>
          <mi>s</mi>
          <mo>&#8712;</mo>
          <mi>S</mi>
         </mrow>
        </msub>
        <msubsup>
         <mi>D</mi>
         <mi>s</mi>
         <mrow>
          <msub>
           <mi>X</mi>
           <mi>s</mi>
          </msub>
         </mrow>
        </msubsup>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">\eta_{\prod_{s \in S} D_s^{X_s}}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_64" height="30" width="110.000001" font-size="16" y="48" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mo rspace="thinmathspace" lspace="thinmathspace">&#8719;</mo>
       <mrow>
        <mi>s</mi>
        <mo>&#8712;</mo>
        <mi>S</mi>
       </mrow>
      </msub>
      <msub>
       <mi>V</mi>
       <mn>1</mn>
      </msub>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>D</mi>
       <mi>s</mi>
      </msub>
      <msup>
       <mo stretchy="false">)</mo>
       <mrow>
        <msub>
         <mi>X</mi>
         <mi>s</mi>
        </msub>
       </mrow>
      </msup>
     </mrow>
     <annotation encoding="application/x-tex">\prod_{s \in S} V_1(D_s)^{X_s}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_88" height="30" width="110.000001" font-size="16" y="48" x="545">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mo rspace="thinmathspace" lspace="thinmathspace">&#8719;</mo>
       <mrow>
        <mi>s</mi>
        <mo>&#8712;</mo>
        <mi>S</mi>
       </mrow>
      </msub>
      <msub>
       <mi>V</mi>
       <mn>2</mn>
      </msub>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>D</mi>
       <mi>s</mi>
      </msub>
      <msup>
       <mo stretchy="false">)</mo>
       <mrow>
        <msub>
         <mi>X</mi>
         <mi>s</mi>
        </msub>
       </mrow>
      </msup>
     </mrow>
     <annotation encoding="application/x-tex">\prod_{s \in S} V_2(D_s)^{X_s}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-start="url(#se_marker_start_svg_37480_112)" marker-end="url(#se_marker_end_svg_37480_112)" id="svg_37480_112" y2="61" x2="175" y1="61" x1="113" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-start="url(#se_marker_start_svg_37480_113)" marker-end="url(#se_marker_end_svg_37480_113)" id="svg_37480_113" y2="61" x2="546" y1="61" x1="481" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_37480_114)" id="svg_37480_114" y2="197" x2="458" y1="74" x1="594" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_37480_115)" id="svg_37480_115" y2="201" x2="199" y1="75" x1="60" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_37480_116" y="137" x="92">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>p</mi>
       <mrow>
        <mi>s</mi>
        <mo>,</mo>
        <mi>x</mi>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">p_{s,x}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_117" height="20" width="48" font-size="16" y="137" x="511">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>p</mi>
       <mrow>
        <mi>s</mi>
        <mo>,</mo>
        <mi>x</mi>
       </mrow>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">p_{s,x}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_37480_128" y="41" x="491">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo>&#8773;</mo>
     </mrow>
     <annotation encoding="application/x-tex">\cong</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_37480_129" height="20" width="48" font-size="16" y="40" x="120">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo>&#8773;</mo>
     </mrow>
     <annotation encoding="application/x-tex">\cong</annotation>
    </semantics>
   </math>
  </foreignObject>
  <path marker-end="url(#se_marker_end_svg_37480_135)" id="svg_37480_135" d="m63,45c170.666672,-57.333336 353.333344,-60.666664 533,2" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_41">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_42">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_60">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_62">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_115">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_112">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="leftarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_start_svg_37480_112">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m0,50l100,40l-30,-40l30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_113">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="leftarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_start_svg_37480_113">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m0,50l100,40l-30,-40l30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_114">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_37480_135">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>

Since this holds for all $s \in S$ and $x \in X_s$, by the basic properties of products, there is a unique morphism $\prod_{s \in S} V_1(D_s)^{X_s} \to   \prod_{s \in S} V_2(D_s)^{X_s}$ making the diagram commute.  This morphism is normally written $\prod_{s \in S} \alpha_{D_s}^{X_s}$.  Thus under the isomorphism $d$ above, $\alpha_D$ is taken to $\prod_{s \in S} \alpha_{D_s}^{X_s}$.  As this holds for all $D \in \mathcal{D}$, $\alpha$ is completely determined by the $\alpha_{D_s}$, whence the map in \eqref{natrans} is injective.

Hence $[V_1,V_2]$ is a subset of a set and thus a set.
=--

Now that we have a locally small category, the next step is to show that the forgetful functor has a [[left adjoint]].  Firstly, we need to _define_ this forgetful functor.  As we are in the most general case, the forgetful functor does not go to $Set$ but to $S$-indexed tuples of sets (or an $S$-graded set), where $S$ is a choice of set of sorts for $\mathcal{D}$.  To make things a little simpler, we assume that the _sorting_ functor $S \to \mathcal{D}$ is injective on isomorphism classes so that if $s \ne s'$ in $S$ then $D_s \ncong D_{s'}$ in $\mathcal{D}$.  With this assumption, the forgetful functor $Prod[\mathcal{D},Set] \to Set^S$ is the evaluation functor:
$$
V \mapsto \big(s \mapsto V(D_s)\big), \qquad \alpha \mapsto \big(s \mapsto \alpha_{D_s}\big).
$$

+-- {: .num_lemma #ProdFree}
###### Lemma
The forgetful functor $Prod[\mathcal{D},Set] \to Set^S$ has a left adjoint.  The left adjoint is given on objects by:
$$
\big(s \mapsto X_s\big) \mapsto \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, -\right)
$$
=--

+-- {: myproof}
###### Proof
To ease the notation, let us write $U$ for the forgetful ("underlying set(s)") functor and $F$ for the free functor.

To show the adjunction, we define the unit and counit natural transformations:
$$
\eta \colon I \to U F, \qquad \epsilon \colon F U \to I
$$

Let us consider $\eta$.  To define this, we evaluate it at an $S$-graded set, $X$, to get a morphism of graded sets, $\eta_X$.  Such a morphism is itself a natural transformation so we evaluate again at $s_0 \in S$.  At this point, we have a function (in $Set$)
$$
\eta_{X,s_0} \colon  X_{s_0} \to \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, D_{s_0}\right).
$$
This is simple to describe: it is assignment to $x \in X_{s_0}$ of the projection onto the $x$th $D_{s_0}$-factor:
$$
\prod_{s \in S} D_s^{X_s} \to D_{s_0}^{X_{s_0}} \overset{p_x}{\to} D_{s_0}.
$$

The counit, $\epsilon$, is a little more complicated to describe.  Let $V \colon \mathcal{D} \to Set$ be a covariant product-preserving functor.  Evaluated at $V$, $\epsilon_V$ is a natural transformation
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{V(D_s)}, -\right) \to V
$$
By the [[Yoneda lemma]], such natural transformations are in bijective correspondence with elements of $V\left(\prod_{s \in S} D_s^{V(D_s)}\right)$.  As $V$ is product-preserving, there is a natural isomorphism:
$$
V\left(\prod_{s \in S} D_s^{V(D_s)}\right) \cong \prod_{s \in S} V(D_s)^{V(D_s)}
$$
Now for any set $Z$, there is an obvious element in $Z^Z$: the one that has a $z$ in the $z$th place (which corresponds to the identity function $Z \to Z$).  Taking the product of these gives an element in $\prod_{s \in S} V(D_s)^{V(D_s)}$ which we use to define $\epsilon_V$.

Let us now prove that these provide the desired adjunction.  For one half, we need to consider the composition:
$$
F \overset{F \eta}{\to} F U F \overset{\epsilon F}{\to} F
$$
Let us apply this to a graded set $X = (s \mapsto X_s)$.  Then we are looking at a natural transformation from
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, -\right)
$$
to itself.  By the standard Yoneda argument, it is sufficient to look at the induced function on
$$
\mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, \prod_{s \in S} D_s^{X_s}\right)
$$
and in particular at the image of the identity therein.

The first part comes from $F\eta$ at $F(X)$.  For each $s_0 \in S$, we have a function $\eta_{X,s_0} \colon X_{s_0} \to \mathcal{D}\left(\prod_{s \in S} D_s^{X_s}, D_{s_0}\right)$ and thus a morphism
\begin{equation}
\label{prod}
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}  \to \prod_{s \in S} D_s^{X_s}
\end{equation}
What this does is the following: it sends component corresponding to the $(s,x)$th projection to the $x$th component and all other components are forgotten.
Thus we have a morphism:
$$
\mathcal{D}\left( \prod_{s \in S} D_s^{X_s},  \prod_{s \in S} D_s^{X_s}\right) \to \mathcal{D}\left(
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}, \prod_{s \in S} D_s^{X_s}\right)
$$
Under this, the identity morphism goes to the projection morphism described just above.

Now we apply $\epsilon F$ to get a morphism:
$$
\mathcal{D}\left(
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}, \prod_{s \in S} D_s^{X_s}\right)
\to \mathcal{D}\left( \prod_{s \in S} D_s^{X_s},  \prod_{s \in S} D_s^{X_s}\right)
$$
To find this element, we consider the diagram:
$$
\array{
\mathcal{D}\left(
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)},
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}\right)
&\overset{\epsilon }{\to}&
\mathcal{D}\left( \prod_{s \in S} D_s^{X_s},
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}\right)
& \cong &
\prod_{s \in S} \mathcal{D}\left( \prod_{s'' \in S} D_{s''}^{X_{s''}},
 D_s\right)^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)} \\
\downarrow & & \downarrow & & \downarrow \\
\mathcal{D}\left(
\prod_{s \in S} D_s^{\mathcal{D}\left(\prod_{s' \in S} D_{s'}^{X_{s'}},D_s\right)}, \prod_{s \in S} D_s^{X_s}\right)
&\overset{\epsilon }{\to}&
\mathcal{D}\left( \prod_{s \in S} D_s^{X_s},  \prod_{s \in S} D_s^{X_s}\right)
& \cong &
  \prod_{s \in S}\mathcal{D}\left( \prod_{s'' \in S} D_{s''}^{X_{s''}}, D_s\right)^{X_s}
}
$$
In this diagram, we have left off the subscript on $\epsilon$ for conciseness.  The vertical morphism is that induced by the projection from \eqref{prod}.  Since we want to have this projection itself in the lower-left, an obvious place to start is with the identity in the top-left.  The right-hand square commutes since the vertical maps are projections.  Starting with the identity in the top-left, we get the "Yoneda element" corresponding to $\epsilon$ in the top-right.  That element can be written $(f)_f$.  The vertical map selects the $p_{s,x}$th element of the list and puts it in the $(s,x)$th slot.  As this is the projection $p_{s,x}$, when moving back to the lower-middle, we obtain the identity morphism as required.

Now let us turn to the other half.  We need to consider the composition:
$$
U \overset{\eta U}{\to} U F U \overset{U \epsilon}{\to} U
$$
So we need to start with a covariant product-preserving functor $V \colon \mathcal{D} \to Set$ and apply $U$.  Then we are looking at a morphism of graded sets from
$$
\big(s \mapsto V(D_s)\big)
$$
to itself.  So we pick $s_0 \in S$ and look at the function
$$
V(D_{s_0}) \to \mathcal{D}\left(\prod_{s \in S} D_s^{V(D_s)}, D_{s_0}\right) \to V(D_{s_0}).
$$

We start with the function defined by the unit $\eta$:
$$
V(D_{s_0}) \to \mathcal{D}\left(\prod_{s \in S} D_s^{V(D_s)}, D_{s_0}\right)
$$
which sends $v \in V(D_{s_0})$ to the projection $\prod_{s \in S} D_s^{V(D_s)} \to D_{s_0}$ which corresponds to the $v$th factor of the $s_0$th factor.

Now we apply $\epsilon$.  This gives us a natural transformation
$$
 \mathcal{D}\left(\prod_{s \in S} D_s^{V(D_s)}, - \right) \to V(-)
$$
which we evaluate at $D_{s_0}$ (technically, which we evaluate at $(s \mapsto D_s)$ which we then evaluate at $s_0$).  This natural transformation is determined by an element of $V\left(\prod_{s \in S} D_s^{V(D_s)}\right)$ and the element that we want is the image of that element under the function induced by the projection:
$$
V\left(\prod_{s \in S} D_s^{V(D_s)}\right) \overset{V(p_{s_0,v})}{\to} V(D_{s_0})
$$
As $V$ is product-preserving, we can rearrange this to:
$$
\prod_{s \in S} V(D_s)^{V(D_s)} \overset{p_{s_0,v}}{\to} V(D_{s_0}).
$$
The projection selects the $(s_0,v)$th term of the element in question, and this element is, by definition, $v$.  Hence the induced function on $V(D_{s_0})$ is the identity and the adjunction is shown.
=--