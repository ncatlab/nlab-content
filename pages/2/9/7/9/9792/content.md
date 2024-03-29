
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea

Once beyond the realm of [[normed vector spaces]], the various ways of defining [[differentiation]] diverge.  This is particularly evident if one considers the slightly stronger notion of **continuous differentiability** wherein the assignment of the derivative must also be continuous.

One can make a reasonable start by saying that for a function $f \colon E \supseteq U \to F$ to be continuously differentiable then it must at least satisfy the notion of [[Gâteaux differentiability]], and one can throw in the requirement that the assignment of the directional derivative be continuous and linear (this is known as *G&#226;teaux--L&#233;vy differentiability*).  Thus one obtains a map $D f \colon U \to \mathcal{L}(E,F)$.  However, outside the realm of normed vector spaces there is not a unique topology on $\mathcal{L}(E,F)$ and thus one can come up with a variety of meanings for the phrase "$D f$ is continuous".


## Finite Dimensions

Let us remind ourselves of the situation in finite dimensions.

+-- {: .num_defn #ctsd}
###### Definition
A function $f \colon \mathbb{R}^m \supseteq U \to \mathbb{R}^n$, where $U$ is open, is said to be **continuously differentiable**, or of class $C^1$, if there is a continuous map $D f \colon U \to \mathcal{L}(\mathbb{R}^m, \mathbb{R}^n)$ with the property that for each $x \in U$ and $h \in \mathbb{R}^m$ then

$$
\lim_{t \to 0} \frac{f(x + t h) - f(x) - t D f(x)h}{t} = 0
$$
=--

Note that for $x \in U$ and $h \in \mathbb{R}^n$ there is an open interval $(-\epsilon,\epsilon)$ with the property that for $t \in (-\epsilon,\epsilon)$ then $x + t h \in U$ and so the limit makes sense.


## Infinite Dimensions

In infinite dimensions the difficulty with extending the standard definition is that of the topology on continuous linear maps.  This becomes more evident with higher derivatives.  Thus the definition depends on such a choice.  In addition, one needn't use a topology but can make sense of the definition with a [[convergence structure]] on the space of linear maps.

+-- {: .num_defn #ctsdinf}
###### Definition
Let $E$ and $F$ be [[locally convex topological vector spaces]].  Let $U \subseteq E$ be an open set.  Let $\mathcal{L}(E,F)$ be the space of continuous linear maps from $E$ to $F$.  Let $\Lambda$ be a [[convergence structure]] on $\mathcal{L}(E,F)$.  A continuous function $f \colon U \to F$ is said to be **differentiable of class $C^1_\Lambda$** if there exists a continuous mapping $D f \colon U \to \mathcal{L}_\Lambda(E,F)$, called the **derivative** of $f$, such that for every $x,h \in U \times E$ then

$$
\lim_{t \to 0} \frac{f(x + t h) - f(x)}{t} = D f(x) h
$$

We define $C^1_\Lambda(X,F)$ to be the set of functions $f \colon X \to F$ which are of class $C^1_\Lambda$.
=--


## Convergence Structures

There are a variety of convergence structures and topologies on $\mathcal{L}(E,F)$ that can be used.  Some of them with particular properties are gathered in the list below.  For these, the notation is condensed slightly as indicated.

In the following, given [[semi-norms]] $\alpha$ on $E$ and $\beta$ on $F$ we define a semi-norm $\rho_{\beta,\alpha}$ on $\mathcal{L}(E,F)$ by

$$
\rho_{\beta,\alpha}(u) \coloneqq \sup \{\beta(u h) | \alpha(h) \le 1\}
$$

1. $C^1_\Theta$: the translation-invariant convergence structure with filters:

    $\mathcal{F} \to 0$ if there is a semi-norm $\alpha$ on $E$ such that for each semi-norm $\beta$ on $F$ and $\epsilon \gt 0$ there is some $Q \in \mathcal{F}$ with $\sup_{u \in Q} \rho_{\beta,\alpha}(u) \le \epsilon$.

2. $C^1_\Delta$: (Marinescu's convergence structure) the colimit in the category of [[convergence vector spaces]] of the following family of spaces.  Let $\Phi$ denote the family of mappings from the set of continuous semi-norms on $F$ to that on $E$.  For $\phi \in \Phi$ define:

$$
\mathcal{L}_\phi(E,F) \coloneqq \{ u \in \mathcal{L}(E,F) | \rho_{\beta,\phi(\beta)} \lt \infty\; \text{for all}\; \beta\}
$$

3. $C^1_\Pi$: the compatible convergence structure with filters:

    $\mathcal{F} \to 0$ if for each semi-norm $\beta$ on $F$ there is a semi-norm $\alpha$ on $E$ such that for each $\epsilon \gt 0$ there is some $Q \in \mathcal{F}$ with $\sup\{\rho_{\beta,\alpha}(u) | u \in Q\} \le \epsilon$.

4. $C^1_{q b}$: the *quasi-bounded* convergence structure.  This has filters:

    $\mathcal{F} \to 0$ if $\mathcal{F}(\mathcal{B}^n) \to 0$ for every quasi-bounded filter $\mathcal{B}$ on $E$.

    Recall that a filter $\mathcal{B}$ on $E$ is *quasi-bounded* if $\mathcal{V} \cdot \mathcal{B} \to 0$ where $\mathcal{V}$ is the neighbourhood filter of $0$ in $\mathbb{R}$.

5. $C^1_c$: the *continuous convergence structure*.  This is the coarsest convergence structure on $\mathcal{L}(E,F)$ which makes the evaluation map $\mathcal{L}(E,F) \times E \to F$ continuous.

6. $C^1_{\mathcal{S}}$: the topology of uniform convergence on a family $\mathcal{S}$ of [[bounded subsets]] of $E$, in particular:
   1. $C^1_b$: the topology of uniform convergence on [[bounded subsets]] of $E$,
   2. $C^1_{p k}$: the topology of uniform convergence on [[precompact subsets]] of $E$,
   3. $C^1_k$: the topology of uniform convergence on compact subsets of $E$,
   4. $C^1_s$: the topology of uniform convergence on finite subsets of $E$.

The relationships between the various definitions of $C^1_?$ are displayed in the following diagram.

+-- {: style="text-align: center"}
<svg width="286" height="425" xmlns="http://www.w3.org/2000/svg">
 <g>
  <title>Layer 1</title>
  <foreignObject height="25" width="40" font-size="16" id="svg_1" y="0" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#920;</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_\Theta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_4" height="24.999999" width="39" font-size="16" y="0" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#916;</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_\Delta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_13" height="25" width="40" font-size="16" y="80" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#928;</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_\Pi</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_22" height="25" width="40" font-size="16" y="160" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mrow>
        <mi>q</mi>
        <mi>b</mi>
       </mrow>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_{q b}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_31" height="24.999999" width="39" font-size="16" y="240" x="0">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>c</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_c</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_40" height="24.999999" width="39" font-size="16" y="160" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>b</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_b</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_49" height="24.999999" width="39" font-size="16" y="240" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mrow>
        <mi>p</mi>
        <mi>k</mi>
       </mrow>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_{p k}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_58" height="24.999999" width="39" font-size="16" y="320" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>k</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_k</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_67" height="24.999999" width="39" font-size="16" y="400" x="80">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>s</mi>
       <mn>1</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^1_s</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line marker-end="url(#se_marker_end_svg_76)" id="svg_76" y2="70" x2="20" y1="30" x1="20" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_77" marker-end="url(#se_marker_end_svg_77)" y2="150" x2="20" y1="110" x1="20" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_78" marker-end="url(#se_marker_end_svg_78)" y2="230" x2="20" y1="190" x1="20" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_79" marker-end="url(#se_marker_end_svg_79)" y2="230" x2="100" y1="190" x1="100" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_80" marker-end="url(#se_marker_end_svg_80)" y2="310" x2="100" y1="270" x1="100" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_81" marker-end="url(#se_marker_end_svg_81)" y2="390" x2="100" y1="350" x1="100" stroke-width="2" stroke="#000000" fill="none"/>
  <line transform="rotate(-90, 60, 175)" id="svg_82" marker-end="url(#se_marker_end_svg_82)" y2="195" x2="60" y1="155" x1="60" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_84" transform="rotate(-90, 60, 255)" marker-end="url(#se_marker_end_svg_84)" y2="275" x2="60" y1="235" x1="60" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_85)" id="svg_85" y2="75.999999" x2="38.999998" y1="26" x1="90" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_86)" id="svg_86" y2="350" x2="110" y1="390" x1="110" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_87" marker-end="url(#se_marker_end_svg_87)" y2="191" x2="109" y1="231" x1="109" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_88" marker-end="url(#se_marker_end_svg_88)" y2="193" x2="30" y1="233" x1="30" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_89" marker-end="url(#se_marker_end_svg_89)" y2="272" x2="109" y1="312" x1="109" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_90" marker-end="url(#se_marker_end_svg_90)" y2="114" x2="29" y1="154" x1="29" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_91" marker-end="url(#se_marker_end_svg_91)" y2="31" x2="30" y1="71" x1="30" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_92)" id="svg_92" y2="162" x2="41.951248" y1="162" x1="83" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_93)" id="svg_93" y2="241" x2="37.954569" y1="241" x1="82" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_94)" id="svg_94" y2="32.947945" x2="96.052055" y1="81" x1="48" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="2" stroke="#000000" fill="none"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_97" y="378" x="201" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="0" stroke="#000000" fill="#000000">E metrisable and barrelled</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_98" y="301" x="202" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="0" stroke="#000000" fill="#000000">E complete or metrisable</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_100" y="223" x="186" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="5,5" stroke-width="0" stroke="#000000" fill="#000000">E Schwartz</text>
  <path id="svg_101" d="m140,226c-15.333328,20 -66.666664,-31 -102,-8" marker-end="url(#se_marker_end_svg_101)" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_102)" id="svg_102" y2="217" x2="116" y1="217" x1="146" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_103" y="128" x="119" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E metrisable or Schwartz</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_104" y="174" x="198" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E metrisable</text>
  <path marker-end="url(#se_marker_end_svg_105)" id="svg_105" d="m154,159c-17,-21 -67,-26 -79,-3" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <path id="svg_106" d="m148,170c-29,7.333328 -82,30.666672 -83,61" marker-end="url(#se_marker_end_svg_106)" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_107" y="63" x="184" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E or F normable</text>
  <path id="svg_108" d="m124,58c-12.333344,-13.333336 -56.666664,-22.666664 -85,-13" marker-end="url(#se_marker_end_svg_108)" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_109)" id="svg_109" y2="68" x2="74" y1="64" x1="123" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_76">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_77">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_78">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_79">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_80">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_81">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_82">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_84">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_85">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_86">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_87">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_88">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_89">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_90">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_91">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_92">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_93">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_94">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_101">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_102">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_105">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_106">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_108">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_109">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>
=--

Let us extract some particular cases:

1. $E$ normable, $F$ arbitrary:
    1. $C^1_\Theta$, $C^1_\Delta$, $C^1_\Pi$, $C^1_{q b}$, $C^1_b$ are equivalent
    2. $C^1_c$, $C^1_{p k}$, $C^1_k$ are equivalent
2. $E$ Banach space, $F$ arbitrary:
    1. $C^1_\Theta$, $C^1_\Delta$, $C^1_\Pi$, $C^1_{q b}$, $C^1_b$ are equivalent
    2. $C^1_c$, $C^1_{p k}$, $C^1_k$, $C^1_s$ are equivalent
3. $E$ Fr&#233;chet space, $F$ arbitrary:
    1. $C^1_{q b}$, $C^1_b$ are equivalent
    2. $C^1_c$, $C^1_{p k}$, $C^1_k$, $C^1_s$ are equivalent
4. $E$ Fr&#233;chet--Schwartz, $F$ arbitrary: $C^1_\Pi$, $C^1_{q b}$, $C^1_c$, $C^1_b$, $C^1_{p k}$, $C^1_k$, $C^1_s$ are equivalent
5. $E$ finite dimensional and $F$ arbitrary, or $E$ Fr&#233;chet--Schwartz and $F$ normable: All equivalent


## Chain Rule

An important question to ask of the various definitions of continuously differentiable is whether they satisfy the chain rule.  The following result provides the basis for this.

+-- {: .num_lemma #lemchain}
###### Lemma
Let $E$, $F$, $G$ be LCTVS, let $U \subseteq E$ and $V \subseteq F$ be open sets, let $\Lambda$ and $\Lambda'$ be convergence structures on $\mathcal{L}(E,F)$ and $\mathcal{L}(E,G)$ respectively.

Assume that the composition map:

$$
\mathcal{L}_k(F,G) \times \mathcal{L}_\Lambda(E,F) \to \mathcal{L}_{\Lambda'}(E,G)
$$

is continuous.

Let $f \colon U \to F$ and $g \colon V \to G$ be functions with $f(U) \subseteq V$.  Suppose that $f$ is of class $C^1_\Lambda$ and $g$ of class $C^1_k$.  Then $g \circ f$ is of class $C^1_{\Lambda'}$.
=--

+-- {: .num_cor #corchain}
###### Corollary
The chain rule holds for each of $C^1_c$, $C^1_{q b}$, $C^1_\Pi$, $C^1_\Delta$, $C^1_\Theta$.

The following partial chain rules also hold:

1. $C^1_\Pi(F,G) \times C^1_{\mathcal{S}}(E,F) \to C^1_{\mathcal{S}}(E,G)$
1. If $E$ is metrisable, $C^1_k(F,G) \times C^1_s(E,F) \to C^1_s(E,G)$
1. If $E$ is metrisable, $C^1_k(F,G) \times C^1_k(E,F) \to C^1_k(E,G)$
=--


## Higher Derivatives

A minor wriggle enters the story with higher derivatives due to the fact that the higher derivatives are multilinear maps $E^n \to F$ and so not only are there different notions of convergence to put on these spaces, there are also different possible meanings of the statement that these are continuous.  When dealing with one of the topologies (defined by some family of bounded sets), we will end up with derivatives in $\mathcal{H}^n_{\mathcal{S}}(E,F)$ rather than $\mathcal{L}^n_{\mathcal{S}}(E,F)$ in the notation of [[continuous multilinear operator]].

However, we can start with a very weak notion to get the ball rolling.  Let $L^n(E,F)$ be the space of all (not necessarily continuous) $n$-linear maps $E^n \to F$.  We equip it with the topology of simple convergence.

+--{: .num_defn #wdiff}
###### Definition
Let $E$ and $F$ be LCTVS, $U \subseteq E$ an open subset, $p \in \mathbb{N}$.  A function $f \colon U \to F$ is said to be **weakly $p$-times differentiable** if there exist functions $D^k f \colon U \to L^k(E,F)$ for $k = 0, 1, \dots, p$ such that $D^0 f = f$ and for each $x \in U$, $h \in E$, and $k = 0, 1, \dots, p-1$ then

$$
\lim_{t \to 0} \frac{D^k f(x + t h) - D^k f(x)}{t} = D^{k+1} f(x)h.
$$
=--

Note that we don't assume that the $D^k f$ are continuous.  If some are continuous then some nice properties ensue.  For example, if $D^p f$ is continuous then each $D^k f$ for $k \le p$ is totally symmetric.

From the definition of weakly $p$-times differentiable we can define the various classes of continuously $p$-times differentiable.  For the definition of $\mathcal{H}^n_{\mathcal{S}}(E,F)$ see the page on [[continuous multilinear operator]].

+-- {: .num_defn #chdiff}
###### Definition
Let $E$ and $F$ be LCTVS, $U \subseteq E$ an open subset, $p \in \mathbb{N}$.  Let $\mathcal{S}$ be a family of bounded sets in $E$ which covers $E$.  A function $f \colon U \to F$ is said to be **differentiable of class $C^p_{\mathcal{S}}$** if $f$ is weakly $p$-times differentiable and such that for $k = 0,1,\dots, p$ then:

1. $D^k f(U) \subseteq \mathcal{H}^k_{\mathcal{S}}(E,F)$, and
2. $D^k f \colon U \to \mathcal{H}^k_{\mathcal{S}}(E,F)$ is continuous.
=--

Using convergence structures, we have:

+-- {: .num_defn #cvdiff}
###### Definition
Let $E$ and $F$ be LCTVS, $U \subseteq E$ an open subset, $p \in \mathbb{N}$.  Let $\Lambda$ be one of the convergence structures $\Lambda_c$, $\Lambda_{q b}$, $\Pi$, $\Delta$, or $\Theta$ on $\mathcal{L}^p(E,F)$.  A function $f \colon U \to F$ is said to be **differentiable of class $C^p_{\mathcal{S}}$** if $f$ is weakly $p$-times differentiable and such that for $k = 0,1,\dots, p$ then:

1. $D^k f(U) \subseteq \mathcal{L}^k_{\Lambda}(E,F)$, and
2. $D^k f \colon U \to \mathcal{L}^k_{\Lambda}(E,F)$ is continuous.
=--

For fixed $p$, the relationships between the various $C^p_?$ are the same as for $p = 1$.  For varying $p$ we have:

+-- {: .num_lemma #diffp}
###### Lemma
Let $E$ and $F$ be LCTVS, $U \subseteq E$ an open set.  If $f \colon U \to E$ is of class $C^{p+1}_c$ then $f$ is of class $C^p_\Pi$.  Whence we have:

$$
C^{p+1}_c(X,F) \subseteq C^p_\Pi(X,F) \subseteq C^p_{q b}(X,F) \subseteq C^p_b(X,F)
$$

If $E$ is metrisable (resp. Fr&#233;chet) and $f$ is of class $C^{p+1}_k$ (resp. $C^{p+1}_s$) then $f$ is of class $C^p_\Pi$.
=--


## Smooth Functions

We make the obvious definition for a [[smooth function]]:

+--{: .num_defn #smooth}
###### Definition
Let $\Lambda$ be one of the convergence structures $\Lambda_s$, $\Lambda_k$, $\Lambda_{p k}$, $\Lambda_b$, $\Lambda_c$, $\Lambda_{q b}$, $\Pi$, $\Delta$, or $\Theta$.  A function $f \colon U \to F$ is said to be **differentiable of class $C^\infty_\Lambda$** if it is of class $C^p_\Lambda$ for all $p \in \mathbb{N}$.
=--

We have the following table of relationships.

+-- {: style="text-align: center"}
<svg width="238" height="448" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="38025">
 <g>
  <title>Layer 1</title>
  <foreignObject height="30" width="30" font-size="16" id="svg_38025_1" y="0" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#920;</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_\Theta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_3" height="30" width="30" font-size="16" y="0" x="96">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#916;</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_\Delta</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_12" height="28.000001" width="30" font-size="16" y="80" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>&#928;</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_\Pi</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_21" height="28.000001" width="30" font-size="16" y="130" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mrow>
        <mi>q</mi>
        <mi>b</mi>
       </mrow>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_{q b}</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_30" height="28.000001" width="30" font-size="16" y="180" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>c</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_c</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_39" height="28.000001" width="30" font-size="16" y="260" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>b</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_b</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_48" height="28.000001" width="30" font-size="16" y="340" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>k</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_k</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_38025_57" height="28.000001" width="30" font-size="16" y="420" x="16">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msubsup>
       <mi>C</mi>
       <mi>s</mi>
       <mn>∞</mn>
      </msubsup>
     </mrow>
     <annotation encoding="application/x-tex">C^\infty_s</annotation>
    </semantics>
   </math>
  </foreignObject>
  <rect id="svg_38025_66" height="150" width="60" y="70" x="1" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_67)" id="svg_38025_67" y2="65" x2="31" y1="30" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line id="svg_38025_68" marker-end="url(#se_marker_end_svg_38025_68)" y2="255" x2="31" y1="225" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_69)" id="svg_38025_69" y2="65" x2="67" y1="30" x1="98" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_70)" id="svg_38025_70" y2="335" x2="31" y1="290" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_71)" id="svg_38025_71" y2="415" x2="31" y1="370" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_72)" id="svg_38025_72" y2="226" x2="44" y1="260" x1="44" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_73)" id="svg_38025_73" y2="288" x2="44" y1="340" x1="44" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_74)" id="svg_38025_74" y2="365.990197" x2="41" y1="417" x1="41" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_75)" id="svg_38025_75" y2="35" x2="110" y1="76" x1="72" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_38025_76)" id="svg_38025_76" y2="28.986114" x2="41" y1="65" x1="41" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-start="url(#se_marker_start_svg_38025_77)" marker-end="url(#se_marker_end_svg_38025_77)" id="svg_38025_77" y2="130" x2="31" y1="110" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-start="url(#se_marker_start_svg_38025_78)" marker-end="url(#se_marker_end_svg_38025_78)" id="svg_38025_78" y2="180" x2="31" y1="160" x1="31" stroke-linecap="null" stroke-linejoin="null" stroke-width="2" stroke="#000000" fill="none"/>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_38025_80" y="58" x="175" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E or F normable</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_38025_81" y="250" x="108" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E metrisable</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_38025_82" y="315" x="108" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E metrisable</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" id="svg_38025_83" y="397" x="153" stroke-linecap="null" stroke-linejoin="null" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000">E metrisable and barrelled</text>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_67">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_68">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_69">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_70">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_71">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_72">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_73">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_74">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_75">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_76">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_77">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_38025_78">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="leftarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_start_svg_38025_77">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m0,50l100,40l-30,-40l30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="leftarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_start_svg_38025_78">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m0,50l100,40l-30,-40l30,-40z"/>
  </marker>
 </defs>
</svg>
=--

Therefore, for [[Banach spaces]] all the notions of "smooth function" collapse, whilst for [[Fréchet spaces]] all of the notions coarser than $\Pi$ collapse.


## Related concepts

* [[continuous function]], [[differentiable function]], **continuously differentiable function**, [[smooth function]], [[analytic function]]


## References

* Keller, H. H. (1974). _Differential calculus in locally convex spaces_. Lecture Notes in Mathematics, Vol. 417. Berlin: Springer-Verlag. [MR0440592](http://www.ams.org/mathscinet-getitem?mr=440592)


[[!redirects continuous differentiability]]
[[!redirects continuously differentiable]]
[[!redirects continuously differentiable map]]
[[!redirects continuously differentiable maps]]
[[!redirects continuously differentiable function]]
[[!redirects continuously differentiable functions]]
