
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### 2-Category theory
+--{: .hide}
[[!include 2-category theory - contents]]
=--
=--
=--

* [[object]]

* [[morphism]]

* **2-morphism**

* [[3-morphism]]

* [[k-morphism]]

***


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

A **2-morphism** in an [[n-category]] is a [[k-morphism]] for $k = 2$: it is a higher morphism between ordinary 1-[[morphism]]s.

So in the hierachty of $n$-categories, the first step where 2-morphisms appear is in a [[2-category]]. This includes cases such as [[bicategory]], [[2-groupoid]] or [[double category]].

## Shapes 

There are different [[geometric shapes for higher structures]]: [[globe]]s, [[simplex|simplices]], [[cube]]s, etc. Accordingly, 2-morphisms may appear in different guises:

A **globular** $2$-morphism looks like this:
$$
a\mathrlap{\begin{matrix}\begin{svg}
<svg width="76" height="37" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="79929">
 <g>
  <title>Layer 1</title>
  <path marker-end="url(#se_marker_end_svg_79929_2)" id="svg_79929_2" d="m2,18.511721c31.272522,-14.782231 42.439789,-16.425501 71.625,-1.25" stroke="#000000" fill="none"/>
  <path id="svg_79929_13" marker-end="url(#se_marker_end_svg_79929_2)" d="m2,24.511721c33.286949,14.464769 40.259941,16.4624 71.500008,1.75" stroke="#000000" fill="none"/>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_79929_2">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_79929_3"/>
  </marker>
 </defs>
</svg>
\end{svg}\includegraphics[width=56]{curvearrows}\end{matrix}}\qquad\Downarrow\qquad b
$$

A **simplicial** $2$-morphism looks like this:

$$
\begin{matrix}
    && b
    \\
    & \nearrow &\Downarrow& \searrow
    \\
    a &&\to&& c
\end{matrix}
$$

A **cubical** $2$-morphism looks like this:

$$
\begin{matrix}
  &          & b \\
  & \nearrow &            & \searrow \\
a &          & \Downarrow &          & d \\
  & \searrow &            & \nearrow \\
  &          & c
\end{matrix}
$$

Of course, using [[identity morphisms]] and [[composition]], we can turn one into the other; which is more fundamental depends on which shapes you prefer.

+--{.query}
[[Eric]]: Are there any consistency requirements for a 2-morphism? For example, in the bigon above, if $f:a\to b$, $g:a\to b$, and $\alpha:f\to g$, are there requirements on $\alpha:f\to g$ regarding $f$ and $g$? For example, should $\alpha$ come with component 1-morphisms $\alpha_a:a\to a$ and $\alpha_b:b\to b$ such that 
$$\alpha_a\circ g = f\circ\alpha_b$$
or maybe
$$\alpha_a\circ g \simeq f\circ\alpha_b$$
? Could there be a 2-morphism without the corresponding 1-morphism components?

[[Urs Schreiber]]: in any given [[2-category]] you have to specify which 2-morphisms exactly there are supposed to be, what $ \alpha $ exactly you allow between $f$ and $g$. When you ask about components, it seems you are thinking of 2-morphisms specifically in the 2-category [[Cat]]. Here, yes, th allowed 2-morphisms are those that are [[natural transformation]]s between their source and target 1-morphisms, which are [[functor]]s.

[[Eric]]: I think the [[exchange law]] might be what I had in mind.

=--


## Examples

* in the [[2-category]] [[Cat]], 2-morphisms are [[natural transformation]]s between functors.

* In a [[path 2-groupoid]] 2-morphisms are certain surfaces or images of surfaces in a space, going between paths in that space.

[[!redirects 2-morphism]]
[[!redirects 2-morphisms]]
[[!redirects 2-cell]]
[[!redirects 2-cells]]