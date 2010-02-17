
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

<center>
<svg width="430" height="250" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" xmlns:xlink="http://www.w3.org/1999/xlink">
 <!-- Created with SVG-edit - http://svg-edit.googlecode.com/ -->
 <defs>
  <marker refX="8" orient="auto" markerHeight="5" markerWidth="5" markerUnits="strokeWidth" refY="5" id="se_arrow_fw1" viewBox="0 0 10 10">
   <path fill="#000" d="m0,0l10,5l-10,5l5,-5l-5,-5z"/>
  </marker>
 </defs>
 <g>
  <title>Layer 1</title>
  <polyline se:connector="svg_7 svg_10" marker-end="url(#se_arrow_fw1)" stroke-dasharray="2,2" fill="none" stroke-width="2" stroke="#000" points="314.145,163.797 338.297,185.633 362.449,207.469" id="svg_25"/>
  <polyline se:connector="svg_8 svg_9" stroke-dasharray="2,2" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="308.656,46.2645 339.672,70.5106 370.688,94.7567" id="svg_24"/>
  <polyline se:connector="svg_2 svg_9" stroke-dasharray="5,5" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="69.6836,93.271 220.186,97.505 370.688,101.739" id="svg_23"/>
  <polyline se:connector="svg_3 svg_9" marker-end="url(#se_arrow_fw1)" stroke-dasharray="5,5" fill="none" stroke-width="2" stroke="#000" points="127.594,31.0161 249.141,65.2049 370.688,99.3938" id="svg_22"/>
  <polyline se:connector="svg_6 svg_10" stroke-dasharray="5,5" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="228.25,188.818 287.188,200.808 346.125,212.799" id="svg_21"/>
  <polyline se:connector="svg_2 svg_8" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="69.6836,90.9294 182.436,66.6886 295.188,42.4478" id="svg_18"/>
  <polyline se:connector="svg_6 svg_7" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="228.25,184.678 252.438,174.14 276.625,163.601" id="svg_13"/>
  <polyline se:connector="svg_4 svg_6" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="92.4688,205.616 153.883,197.011 215.297,188.407" id="svg_12"/>
  <polyline se:connector="svg_5 svg_6" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="153.969,161.173 184.633,173.079 215.297,184.985" id="svg_11"/>
  <text transform="matrix(0.949804, 0, 0, 1, 3.21882, 0)" xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_2" y="102" x="59.2645">ai</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_3" y="35" x="119">aj</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_4" y="217" x="64">U(ai)</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_5" y="157" x="126">U(aj)</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_6" y="194" x="222">x</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_7" y="160" x="302">U(b)</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_8" y="50" x="302">b</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_9" y="111" x="381">b'</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="24" stroke-width="0" stroke="#000000" fill="#000000" id="svg_10" y="226" x="375">U(b')</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-width="0" stroke="#000" fill="#000000" id="svg_14" y="164" x="182">fj</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-width="0" stroke="#000" fill="#000000" id="svg_15" y="215" x="151">fi</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-width="0" stroke="#000000" fill="#000000" id="svg_16" y="170" x="248">g</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000" id="svg_26" y="219" x="286">g'</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000" id="svg_27" y="69" x="346">h</text>
  <text xml:space="preserve" text-anchor="middle" font-family="serif" font-size="16" stroke-dasharray="2,2" stroke-width="0" stroke="#000000" fill="#000000" id="svg_28" y="184" x="353">U(h)</text>
  <polyline se:connector="svg_3 svg_8" marker-end="url(#se_arrow_fw1)" fill="none" stroke-width="2" stroke="#000" points="127.594,29.1101 211.391,34.8254 295.188,40.5407" id="svg_17"/>
 </g>
</svg>
</center>

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
