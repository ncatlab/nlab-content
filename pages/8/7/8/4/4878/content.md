
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



# Linking numbers
* table of contents
{: toc}

## Signs of crossings

In an oriented link diagram, we can see there are two types of possible crossing. They are allocated a sign, + or -. 

<svg width="250" height="120" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="2798">
 <g>
  <title>Layer 1</title>
  <line marker-end="url(#se_marker_end_svg_2798_1)" id="svg_2798_1" y2="10" x2="108" y1="110" x1="8" stroke-width="2" stroke="#000000" fill="none"/>
  <rect transform="rotate(45, 49, 51.5)" id="svg_2798_3" height="9" width="54" y="47" x="22" stroke-width="2" fill="#ffffff"/>
  <line marker-end="url(#se_marker_end_svg_2798_2)" id="svg_2798_2" y2="10" x2="8" y1="110" x1="108" stroke-width="2" stroke="#000000" fill="none"/>
  <line marker-end="url(#se_marker_end_svg_2798_4)" id="svg_2798_4" y2="9" x2="241" y1="109" x1="141" stroke-width="2" stroke="#000000" fill="none"/>
  <rect marker-end="url(#se_marker_end_svg_2798_6)" id="svg_2798_5" transform="rotate(45, 194, 61.5)" height="9" width="54" y="57" x="167" stroke-width="2" fill="#ffffff"/>
  <line marker-start="url(#se_marker_start_svg_2798_6)" id="svg_2798_6" y2="9" x2="141" y1="109" x1="241" stroke-width="2" stroke="#000000" fill="none"/>
  <foreignObject height="20" width="48" font-size="16" id="svg_2798_7" y="78" x="169">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo rspace="0em" lspace="verythinmathspace">+</mo>
     </mrow>
     <annotation encoding="application/x-tex">+</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject height="20" width="48" font-size="16" id="svg_2798_8" y="81" x="35">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <mo rspace="0em" lspace="verythinmathspace">&#8722;</mo>
     </mrow>
     <annotation encoding="application/x-tex">-</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_2798_2">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_2798_1">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="leftarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_start_svg_2798_6">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m0,50l100,40l-30,-40l30,-40z"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" se_type="rightarrow" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_2798_4">
   <path stroke-width="10" stroke="#000000" fill="#000000" d="m100,50l-100,40l30,-40l-30,-40z"/>
  </marker>
 </defs>
</svg>

One method of remembering the sign convention is to imagine an approach to the crossing along the *underpass* in the direction of the orientation: 

* if the overpass passes from left to right the crossing is counted as being *positive*;
* if it passes from right to left it counts as *negative*.


## Writhe

The *writhe* of an oriented *knot* or *link* diagram is the sum of the signs of all its crossings.  If $D$ is the diagram, we denote its writhe by $w(D)$.

The writhe is used in the definition of some of the [[knot invariants]].


## Linking number

This is a variant of the writhe that is more adapted for use with links. 

Suppose we have an oriented link diagram $D$ with components $C_1, \ldots, C_m$, the *linking number* of $C_i$ with $C_j$ where $C_i$ and $C_j$ are distinct components of $D$, is to be one half of the sum  of the signs of the crossings of $C_i$ with $C_j$; it will be denoted $lk(C_i,C_j)$.

The linking number of the diagram $D$ us then the sum of the linking numbers of all pairs of components:

$$Lk(D) = \sum_{1\le i\lt j\le m}lk(C_i,C_j).$$


## Examples

The writhe of the standard trefoil is 3, of the Hopf link (both components clockwise oriented) is +2, but that of the Borromean rings is 0 although it is a non-trivial link.


## Invariance?

The writhe is not an isotopy invariant, as it can be changed but twisting a stand of the knot (or link).

+-- {: .un_proposition}
###### Proposition

The writhe is an invariant of regular isotopy.
=--

+-- {: .un_proposition}
###### Proposition
The linking number is a [[link invariant]].
=--

+-- {: .proof}
###### Proof
We use [[Reidemeister moves]] so have to check that they do not change the linking number of a diagram. Any Reidemeister move that involves at least two components of the link (i.e. which must be an R2 or R3) leaves all linking numbers between components unchanged.  An R2 move removes or introduces two crossings of opposite sign, whilst an R3 leaves the number of crossings and their signs unaltered.
=--
We can conclude that the Hopf link is not isotopic to the two component unlink, (which is reassuring) as any assignment of orientations to the Hopf link leads to a non-zero linking number.

##Linking number is an integer

Let $n_{1}$ (resp. $n_{2}$) be the sum of the signs of crossings between a pair of components $L_{1}$ and $L_{2}$ of a link in which the over arc belongs to $L_{1}$ (resp.  $L_{2}$). The linking number is then clearly equal to $\frac{1}{2}(n_{1} + n_{2})$.

Now, take a crossing between $L_{1}$ and $L_{2}$ such that the over arc belongs to $L_{1}$. Suppose that we switch the crossing type, so that now the under arc belongs to $L_{1}$. Then, no matter what the sign of the crossing, it can be verified that the sum $n_{1} - n_{2}$ remains unchanged by this switch. 

We may also obviously make crossing switches to the self-crossings of a component, or to crossings of the two components we are looking at with other components, without affecting the sum $n_{1} - n_{2}$.

In addition, it is straightforward to check that the Reidemeister moves do not change the sum $n_{1} - n_{2}$. 

Now, it is obvious that any pair of components of a link can be unlinked from the link after making appropriate crossing switches. In the case that $L_{1}$ and $L_{2}$ are circles disjoint from each other and the rest of the link, we have that $n_{1} - n_{2} = 0$. 

We deduce that $n_{1} - n_{2} = 0$ in all cases. Hence $n_{1} = n_{2}$, and the linking number is equal to $\frac{1}{2}(2n_{1}) = n_{1} = n_{2}$. 

In particular, the linking number is an integer. 

An immediate consequence of the fact that the sum of the signs of the crossings between $L_{1}$ and $L_{2}$ is even is that there must in fact be an even number of such crossings.

[[!redirects linking number]]
[[!redirects linking numbers]]
