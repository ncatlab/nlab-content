
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A *solid functor* (also called a *semi-topological functor*) is a [[forgetful functor]] $U\colon A\to X$ for which the structure of an $A$-object can be universally lifted along [[sinks]].  One can also say that $U$ has not just a [[left adjoint]] but all possible "relative" left adjoints.

When $U$ is solid, [[colimit]]s in $A$ can be constructed in a natural way out of colimits in $X$, and $A$ inherits strong cocompleteness properties from $X$.

## Definition

Let $U\colon A\to X$ be a [[faithful functor]].  A **$U$-structured sink** is a [[sink]] in $X$ of the form $(U a_i \overset{f_i}{\to} x)$.  Note that the indexing family $i\in I$ need not be a [[set]], it can be a [[proper class]].  A **semi-final lift** of such a $U$-structured sink consists of a morphism $x\overset{g}{\to} U b$ in $X$ such that

1. Every composite $g \circ f_i\colon U a_i \to U b$ is in the image of $U$, i.e. is of the form $U(\tilde{g})$ for some $\tilde{g}\colon a_i\to b$ (necessarily unique, since $U$ is faithful), and

1. $g$ is [[initial object|initial]] with this property, i.e. for any other morphism $x \overset{g'}{\to} U b'$ such that each $g' \circ f_i$ is in the image of $U$, there exists a unique $h\colon b\to b'$ in $A$ such that $g' = U(h) \circ g$.

Finally, $U$ is called **solid** if every $U$-structured sink has a semi-final lift.

+-- {: #SFlift style="text-align:center"}
<svg width="370" height="250" xmlns="http://www.w3.org/2000/svg" se:nonce="83381" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns:se="http://svg-edit.googlecode.com">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_83381_fw" viewBox="0 0 10 10">
   <path fill="#000000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <foreignObject x="13" y="82" id="svg_83381_1" font-size="16" width="30" height="24">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>a</mi>
       <mi>i</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">a_i</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="24" width="30" font-size="16" y="17" x="75" id="svg_83381_19">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>a</mi>
       <mi>j</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">a_j</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_83381_32" x="71" y="136" font-size="16" width="42" height="25">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>U</mi>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>a</mi>
       <mi>j</mi>
      </msub>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">U(a_j)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_83381_37" height="23" width="41" font-size="16" y="199" x="14">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>U</mi>
      <mo stretchy="false">(</mo>
      <msub>
       <mi>a</mi>
       <mi>i</mi>
      </msub>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">U(a_i)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="24" width="24" font-size="16" y="199" x="102" id="svg_83381_45">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>f</mi>
       <mi>i</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">f_i</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="132" y="146" font-size="16" width="24" height="26" id="svg_83381_50">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>f</mi>
       <mi>j</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">f_j</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="250" y="29" font-size="16" width="20" height="20" id="svg_83381_55">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>b</mi>
     </mrow>
     <annotation encoding="application/x-tex">b</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="20" font-size="16" y="42" x="281" id="svg_83381_60">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>h</mi>
     </mrow>
     <annotation encoding="application/x-tex">h</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="231" y="202" font-size="16" width="26" height="24" id="svg_83381_63">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>g</mi>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">g'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="22" width="24" font-size="16" y="86" x="317" id="svg_83381_66">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>b</mi>
      <mo>&#8242;</mo>
     </mrow>
     <annotation encoding="application/x-tex">b'</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="24" width="20" font-size="16" y="150" x="210" id="svg_83381_71">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>g</mi>
     </mrow>
     <annotation encoding="application/x-tex">g</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="24" width="44" font-size="16" y="146" x="248" id="svg_83381_74">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>U</mi>
      <mo stretchy="false">(</mo>
      <mi>b</mi>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">U(b)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="313" y="207" font-size="16" width="41" height="24" id="svg_83381_82">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>U</mi>
      <mo stretchy="false">(</mo>
      <mi>b</mi>
      <mo>&#8242;</mo>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">U(b')</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="296" y="170" font-size="16" width="44" height="24" id="svg_83381_88">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>U</mi>
      <mo stretchy="false">(</mo>
      <mi>h</mi>
      <mo stretchy="false">)</mo>
     </mrow>
     <annotation encoding="application/x-tex">U(h)</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="175" y="176" font-size="16" width="20" height="24" id="svg_83381_108">
   <math display="inline" xmlns:xlink="http://www.w3.org/1999/xlink" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mi>X</mi>
     </mrow>
     <annotation encoding="application/x-tex">X</annotation>
    </semantics>
   </math>
  </foreignObject>
  <line stroke-width="2" marker-end="url(#se_arrow_83381_fw)" fill="none" stroke="#000000" id="svg_83381_98" y2="44" x2="251" y1="90" x1="41"/>
  <line stroke-dasharray="5,5" marker-end="url(#se_arrow_83381_fw)" stroke-width="2" fill="none" stroke="#000000" id="svg_83381_99" y2="93" x2="315" y1="37" x1="100"/>
  <line marker-end="url(#se_arrow_83381_fw)" stroke-width="2" fill="none" stroke="#000000" id="svg_83381_100" y2="37" x2="249" y1="30" x1="99"/>
  <line stroke-dasharray="2,2" marker-end="url(#se_arrow_83381_fw)" stroke-width="2" fill="none" stroke="#000000" id="svg_83381_102" y2="85" x2="318" y1="46" x1="265"/>
  <line stroke-width="2" marker-end="url(#se_arrow_83381_fw)" fill="none" stroke="#000000" id="svg_83381_103" y2="183" x2="173" y1="156" x1="109"/>
  <line marker-end="url(#se_arrow_83381_fw)" stroke-width="2" fill="none" stroke="#000000" id="svg_83381_104" y2="190" x2="173" y1="207" x1="58"/>
  <line marker-end="url(#se_arrow_83381_fw)" stroke-dasharray="5,5" stroke-width="2" fill="none" stroke="#000000" id="svg_83381_105" y2="215" x2="311" y1="191" x1="196"/>
  <line stroke-dasharray="2,2" stroke-width="2" marker-end="url(#se_arrow_83381_fw)" fill="none" stroke="#000000" id="svg_83381_106" y2="205" x2="320" y1="169" x1="279"/>
  <path id="svg_83381_107" d="m40.000011,98l268.999989,5" marker-end="url(#se_arrow_83381_fw)" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_arrow_83381_fw)" fill="none" stroke-width="2" stroke="#000000" id="svg_83381_111" y2="160" x2="250" y1="183" x1="197"/>
 </g>
</svg>
=--

## Examples

* Any [[topological functor]] is solid.  Indeed, a functor $U$ is topological just when it has final lifts for all $U$-structured sinks, where a *final lift* is a semi-final lift for which $g$ is an isomorphism.

* Any [[monadic functor]] into $Set$ is solid.

* If $U\colon A\to X$ is faithful and has a left adjoint, and moreover $A$ is [[cocomplete category|cocomplete]] and [[well-powered category|well-copowered]], then $U$ is solid.

* For $C$ a [[cofibrantly generated model category]] with monic generating cofibrations, the forgetful functor from [[model structure on algebraic fibrant objects|algebraic fibrant objects]] to $C$ is solid. See there for details.

## Properties

### Left adjoint

For any $x\in X$, the empty family of morphisms into $x$ is a $U$-structured sink, and a semi-final lift for this family is a <a href="http://ncatlab.org/nlab/show/adjoint+functor#UniversalArrows">universal arrow</a> $x\to U b$.  Therefore, if $U$ is solid, then it has a [[left adjoint]].


### Lifting of colimits

Suppose that $U\colon A\to X$ is solid and let $F\colon D\to A$ be a [[diagram]] such that $U F$ has a [[colimit]] in $X$, consisting of a [[cocone]] $U F d_i \to c$.  Let $c \to U e$ be a semi-final lift of this $U$-structured sink, for which we have induced morphisms $F d_i \to e$ in $A$.  Since $U$ is faithful, these morphisms are a cocone under $F$, and the semi-finality makes it into a colimit in $A$.

Therefore, if $A$ is solid over $X$, then it admits all colimits which $X$ does.  Moreover, if we understand colimits in $X$, and we understand the semi-final lifts, then we understand colimits in $A$.


### Lifting of model structures

The standard *[[transferred model structure|transfer theorem]]* for [[model category|model structures]] states that if $U\colon A\to X$ is a functor such that

1. $U$ has a left adjoint $F$,
1. $U$ is [[accessible functor|accessible]], i.e. preserves $\kappa$-[[filtered colimits]] for sufficiently large $\kappa$,
1. $X$ has a [[cofibrantly generated model category|cofibrantly generated model structure]], and
1. [[transfinite composition|Transfinite composites]] of [[pushouts]] of images under $F$ of generating acyclic cofibrations in $X$ become weak equivalences after applying $U$ (the *acyclicity condition*),

then $A$ has a cofibrantly generated model structure in which the weak equivalences and fibrations are created by $U$.  Using an argument of ([Nikolaus](#Nikolaus)) we can show:

+-- {: .un_theorem #LiftingTheorem}
###### Theorem

Let $U\colon A\to X$ be an accessible solid functor, and assume that $X$ has a cofibrantly generated model structure and the following acyclicity condition:

* If $F\colon D\to A$ is a [[filtered diagram]] and $U(F(d_i)) \to x$ is a cocone under $U\circ F$, each of whose legs is an acyclic cofibration in $X$, then the semifinal lift $x\to U(b)$ of this $U$-structured sink is also an acyclic cofibration.

Then the transfer theorem applies, so that $A$ has a cofibrantly generated model structure in which the weak equivalences and fibrations are created by $U$.

=--
+-- {: .proof}
###### Proof
We have remarked above that $U$ has a left adjoint, and we assumed it to be accessible, so it remains to show that the given acyclicity condition implies the standard one.

We first show that pushouts in $A$ of images under $F$ of generating acyclic cofibrations become acyclic cofibrations (not just weak equivalences) upon applying $U$.  Let $i\colon x\to y$ be a generating acyclic cofibration, and
$$\array{F(x) & \overset{f}{\to} & a\\
  ^{F (i)}\downarrow \\
  F(y)}$$
a diagram in $A$ of which we would like to take the pushout.  Consider the pushout of the corresponding diagram in $X$:
$$\array{x & \overset{\bar{f}}{\to} & U(a)\\
  ^{i}\downarrow && \downarrow^g\\
  y& \underset{h}{\to} & U(a) \sqcup_{x} y.}$$
Since $X$ is a model category, $g$ is an acyclic cofibration.  Therefore, if $U(a) \sqcup_x y \overset{k}{\to} U(b)$ is a semifinal lift of the singleton sink $\{g\}$, by assumption, $k$ is also an acyclic cofibration and thus so is the composite $U(a)\to U(b)$.  But it is straightforward to verify that in fact, the map $a\to b$ of which this is the image (which exists by assumption) gives a pushout diagram in $A$:
$$\array{F(x) & \overset{f}{\to} & a\\
  ^{F(i)}\downarrow && \downarrow\\
  F(y) & \underset{\bar{h}}{\to} & b.}$$

If $U$ is not just accessible but [[finitary functor|finitary]], then it preserves all transfinite composites, so any transfinite composite of such pushouts in $A$ maps to a transfinite composite in $X$, and we know that transfinite composites of acyclic cofibrations in $X$ are acyclic cofibrations, so the desired acyclicity condition follows.  In general, we can argue as follows: given a transfinite sequence $a_0\to a_1\to\dots$ in $A$ of such pushouts, its colimit (= composition) can be constructed as above by forgetting down to $X$, taking the colimit there, and then taking the semifinal lift.  But since acyclic cofibrations in $X$ are closed under transfinite composites, the legs of the colimiting cocone in $X$ are acyclic cofibrations.  Hence by the assumed acyclicity condition, so is the semifinal lift, and hence (by composition) so are the images in $X$ of the legs of the colimiting cone in $A$.  This completes the proof.
=--


## References

* [[Walter Tholen]], _Semitopological functors. I_

* and others...

The example of algebraic fibrant objects and the argument entering the above [lifting theorem](#LiftingTheorem) appears in 

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

See also [[model structure on algebraic fibrant objects]].


[[!redirects semi-topological functor]]
[[!redirects semitopological functor]]
[[!redirects semi-final lift]]
[[!redirects semifinal lift]]
