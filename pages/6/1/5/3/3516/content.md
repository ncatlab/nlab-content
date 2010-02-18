
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

A *solid functor* (also called a *semi-topological functor*) is a [[forgetful functor]] $U\colon A\to X$ for which the structure of an $A$-object can be universally lifted along [[sinks]].  One can also say that $U$ has not just a left adjoint but all possible "relative" left adjoints.

When $U$ is solid, colimits in $A$ can be constructed in a natural way out of colimits in $X$, and $A$ inherits strong cocompleteness properties from $X$.

## Definition

Let $U\colon A\to X$ be a [[faithful functor]].  A **$U$-structured sink** is a [[sink]] in $X$ of the form $(U a_i \overset{f_i}{\to} x)$.  Note that the indexing family $i\in I$ need not be a [[set]], it can be a [[proper class]].  A **semi-final lift** of such a $U$-structured sink consists of a morphism $x\overset{g}{\to} U b$ in $X$ such that

1. Every composite $g \circ f_i\colon U a_i \to U b$ is in the image of $U$, i.e. is of the form $U(\tilde{g})$ for some $\tilde{g}\colon a_i\to b$ (necessarily unique, since $U$ is faithful), and

1. $g$ is [[initial object|initial]] with this property, i.e. for any other morphism $x \overset{g'}{\to} U b'$ such that each $g' \circ f_i$ is in the image of $U$, there exists a unique $h\colon b\to b'$ in $A$ such that $g' = U(h) \circ g$.

Finally, $U$ is called **solid** if every $U$-structured sink has a semi-final lift.

+-- {: #SFlift style="text-align:center"}
<svg width="370" height="250" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker viewBox="0 0 10 10" id="se_arrow_fw" refY="5" markerUnits="strokeWidth" markerWidth="5" markerHeight="5" orient="auto" refX="8">
   <path d="m0,0l10,5l-10,5l5,-5l-5,-5z" fill="#000000"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <foreignObject height="24" width="30" font-size="16" id="svg_1" y="82" x="13">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <msub>
     <mi>a</mi>
     <mi>i</mi>
    </msub>
   </math>
  </foreignObject>
  <foreignObject id="svg_19" x="75" y="17" font-size="16" width="30" height="24">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <msub>
     <mi>a</mi>
     <mi>j</mi>
    </msub>
   </math>
  </foreignObject>
  <foreignObject height="25" width="48" font-size="16" y="136" x="65" id="svg_32">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mi>U</mi>
    <mo stretchy="false">(</mo>
    <msub>
     <mi>a</mi>
     <mi>j</mi>
    </msub>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject x="7" y="199" font-size="16" width="48" height="23" id="svg_37">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mi>U</mi>
    <mo stretchy="false">(</mo>
    <msub>
     <mi>a</mi>
     <mi>i</mi>
    </msub>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject id="svg_45" x="102" y="199" font-size="16" width="24" height="24">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <msub>
     <mi>f</mi>
     <mi>i</mi>
    </msub>
   </math>
  </foreignObject>
  <foreignObject id="svg_50" height="26" width="24" font-size="16" y="146" x="132">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <msub>
     <mi>f</mi>
     <mi>j</mi>
    </msub>
   </math>
  </foreignObject>
  <foreignObject id="svg_55" height="20" width="20" font-size="16" y="29" x="250">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mi>b</mi>
   </math>
  </foreignObject>
  <foreignObject id="svg_60" x="281" y="42" font-size="16" width="20" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mi>h</mi>
   </math>
  </foreignObject>
  <foreignObject id="svg_63" height="24" width="26" font-size="16" y="202" x="231">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mrow>
     <mi>g</mi>
     <mo>&#8242;</mo>
    </mrow>
   </math>
  </foreignObject>
  <foreignObject id="svg_66" x="317" y="86" font-size="16" width="24" height="22">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mrow>
     <mi>b</mi>
     <mo>&#8242;</mo>
    </mrow>
   </math>
  </foreignObject>
  <foreignObject id="svg_71" x="210" y="150" font-size="16" width="20" height="24">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mi>g</mi>
   </math>
  </foreignObject>
  <foreignObject id="svg_74" x="248" y="146" font-size="16" width="44" height="24">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <mi>U</mi>
    <mo stretchy="false">(</mo>
    <mi>b</mi>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject id="svg_82" height="24" width="46" font-size="16" y="207" x="315">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mi>U</mi>
    <mo stretchy="false">(</mo>
    <mrow>
     <mi>b</mi>
     <mo>&#8242;</mo>
    </mrow>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject id="svg_88" height="24" width="44" font-size="16" y="170" x="296">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mi>U</mi>
    <mo stretchy="false">(</mo>
    <mi>h</mi>
    <mo stretchy="false">)</mo>
   </math>
  </foreignObject>
  <foreignObject id="svg_108" height="24" width="20" font-size="16" y="176" x="175">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <mi>X</mi>
   </math>
  </foreignObject>
  <line x1="41" y1="90" x2="251" y2="44" id="svg_98" stroke="#000000" fill="none" marker-end="url(#se_arrow_fw)" stroke-width="2"/>
  <line x1="100" y1="37.000001" x2="315" y2="93" id="svg_99" stroke="#000000" fill="none" stroke-width="2" marker-end="url(#se_arrow_fw)" stroke-dasharray="5,5"/>
  <line x1="99" y1="30" x2="249" y2="37" id="svg_100" stroke="#000000" fill="none" stroke-width="2" marker-end="url(#se_arrow_fw)"/>
  <line x1="265" y1="46" x2="318" y2="85" id="svg_102" stroke="#000000" fill="none" stroke-width="2" marker-end="url(#se_arrow_fw)" stroke-dasharray="2,2"/>
  <line x1="109" y1="156" x2="173" y2="183" id="svg_103" stroke="#000000" fill="none" marker-end="url(#se_arrow_fw)" stroke-width="2"/>
  <line x1="58" y1="207" x2="173" y2="190" id="svg_104" stroke="#000000" fill="none" stroke-width="2" marker-end="url(#se_arrow_fw)"/>
  <line x1="196" y1="191" x2="311" y2="215" id="svg_105" stroke="#000000" fill="none" stroke-width="2" stroke-dasharray="5,5" marker-end="url(#se_arrow_fw)"/>
  <line x1="279" y1="169" x2="320" y2="205" id="svg_106" stroke="#000000" fill="none" marker-end="url(#se_arrow_fw)" stroke-width="2" stroke-dasharray="2,2"/>
  <path fill="none" stroke="#000000" stroke-width="2" marker-end="url(#se_arrow_fw)" d="m40.000011,98l268.999989,5" id="svg_107"/>
  <line x1="197" y1="183" x2="250" y2="160" id="svg_111" stroke="#000000" stroke-width="2" fill="none" marker-end="url(#se_arrow_fw)"/>
 </g>
</svg>
=--

## Examples

* Any [[topological functor]] is solid.  Indeed, a functor $U$ is topological just when it has final lifts for all $U$-structured sinks, where a *final lift* is a semi-final lift for which $g$ is an isomorphism.

* Any [[monadic functor]] into $Set$ is solid.

* If $U\colon A\to X$ is faithful and has a left adjoint, and moreover $A$ is [[cocomplete category|cocomplete]] and [[well-powered category|well-copowered]], then $U$ is solid.


## Properties

### Left adjoint

For any $x\in X$, the empty family of morphisms into $x$ is a $U$-structured sink, and a semi-final lift for this family is a universal arrow $x\to U b$.  Therefore, if $U$ is solid, then it has a [[left adjoint]].


### Lifting of colimits

Suppose that $U\colon A\to X$ is solid and let $F\colon D\to A$ be a diagram such that $U F$ has a [[colimit]] in $X$, consisting of a [[cocone]] $U F d_i \to c$.  Let $c \to U e$ be a semi-final lift of this $U$-structured sink, for which we have induced morphisms $F d_i \to e$ in $A$.  Since $U$ is faithful, these morphisms are a cocone under $F$, and the semi-finality makes it into a colimit in $A$.

Therefore, if $A$ is solid over $X$, then it admits all colimits which $X$ does.  Moreover, if we understand colimits in $X$, and we understand the semi-final lifts, then we understand colimits in $A$.


### Lifting of model structures

The standard *transfer theorem* for [[model category|model structures]] states that if $U\colon A\to X$ is a functor such that

1. $U$ has a left adjoint $F$,
1. $U$ is [[accessible functor|accessible]], i.e. preserves $\kappa$-[[filtered colimits]] for sufficiently large $\kappa$,
1. $X$ has a cofibrantly generated model structure, and
1. [[transfinite composition|Transfinite composites]] of [[pushouts]] of images under $F$ of generating acyclic cofibrations in $X$ become weak equivalences after applying $U$ (the *acyclicity condition*),

then $A$ has a cofibrantly generated model structure in which the weak equivalences and fibrations are created by $U$.  Using an argument of [[Thomas Nikolaus]] we can show:

+-- {: .un_theorem}
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

* Tholen, _Semitopological functors. I_
* and others...

[[!redirects semi-topological functor]]
[[!redirects semitopological functor]]
[[!redirects semi-final lift]]
[[!redirects semifinal lift]]
