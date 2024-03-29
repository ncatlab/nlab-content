
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

##The Knot Group of a Knot##

The **knot group**, $G(K)$, of a [[knot]] $K$ is the [[fundamental group]] of the [[knot complement|complement of the knot]].  Taking this apart, the knot, $K$, is an embedding of $S^1$ into $\mathbb{R}^3$ or $S^3$. We tend to abuse terminology and to think (and to write) of $K$ as  the image of the embedding rather than the embedding itself.  We can therefore write $\mathbb{R}^3 \setminus K$ for the space outside the knot, i.e. its complement.  This is clearly arcwise connected so we do not need to worry about a choice of base point any point will do.  We make the 

+-- {: .un_defn}
###### Definition

$G(K) \coloneqq \pi_1(\mathbb{R}^3 \setminus K)$.

=--

To see that this is an invariant of the knot type, note that if you perform an ambient [[isotopy]] on the knot then it deforms this complement into the complement of the isotopic knot.

This is an unambiguous definition, but does not tell us how to calculate anything about this group for a given knot. Luckily there are two neat algorithms for giving [[group presentation|presentations]] of $G(K)$ for arbitrary knots working from a diagram of that knot, one due to Wirtinger, the other to Dehn.

##The Dehn Presentation##

Start by orienting the knot diagram.  The diagram divides the plane into various faces.  Label these faces with distinct letters. For example, $x_1,\ldots, x_n$. These face labels will be the generators in the presentation.  The relations are given by the crossings in the following diagram.

A typical crossing will have a configuration something like this:

+-- {: style="text-align:center"}
<svg width="214" height="214" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="75641">
 <g>
  <title>Layer 1</title>
  <line fill="none" stroke="#7f0000" stroke-width="4" x1="102" y1="214" x2="102" y2="14" id="svg_75641_1" marker-end="url(#se_marker_end_svg_75641_1)"/>
  <rect fill="#ffffff" stroke="#7f0000" stroke-width="0" x="81" y="106" width="43" height="17" id="svg_75641_3"/>
  <line fill="none" stroke="#7f0000" stroke-width="4" x1="2" y1="114" x2="202" y2="114" id="svg_75641_2" marker-end="url(#se_marker_end_svg_75641_2)"/>
  <foreignObject x="27" y="39" id="svg_75641_4" font-size="20" width="50" height="50">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>i</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_i</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="27" y="164" font-size="20" width="50" height="50" id="svg_75641_5">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>j</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_j</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="127" y="39" font-size="20" width="50" height="50" id="svg_75641_13">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>l</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_l</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="127" y="164" font-size="20" width="50" height="50" id="svg_75641_21">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>k</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_k</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker id="se_marker_end_svg_75641_1" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_75641_6" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#7f0000" stroke="#7f0000" stroke-width="10"/>
  </marker>
  <marker id="se_marker_end_svg_75641_2" markerUnits="strokeWidth" orient="auto" viewBox="0 0 100 100" markerWidth="5" markerHeight="5" refX="50" refY="50">
   <path id="svg_75641_7" d="m100,50l-100,40l30,-40l-30,-40l100,40z" fill="#7f0000" stroke="#7f0000" stroke-width="10"/>
  </marker>
 </defs>
</svg>
=--

Look at the underpass arc that leaves the crossing, and write down the face labels going anticlockwise around the crossing, and alternating in exponent between $+1$ and $-1$.  Here that gives $x_i x_j^{-1}x_k x_l^{-1}$.  After doing this for every crossing, set any _one_ face label to be $1$. (This last relation effectively deletes that generator from the presentation.)

That method gives the following presentation, where $x_m$ is the choice of generator to be set to $1$.

$$\langle x_1, \ldots, x_n\mid \text{relations from crossings}, x_m=1\rangle.$$

This is a presentation of $G(K)$.

The element in the fundamental group corresponding to a particular face is given as follows.  We set the basepoint to a point above the plane and draw a path which goes from the basepoint and through the face.  It then goes under the plane (thus, under the knot) to the face whose label was set to $1$, and through this face back to the basepoint.

##Example of a Dehn presentation##

 We will calculate the Dehn presentation for the cinquefoil knot.  This is the next knot in the family of $(2,k)$-torus knots after the [[trefoil knot]].  It has five lobes when drawn in the following nice symmetric form. We orient the diagram clockwise and label the faces of the diagram with the letters from $a$ up to $g$.  

+-- {: style="text-align:center"}
<svg width="150" height="150" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="75642">
 <g>
  <title>Layer 1</title>
  <g id="svg_75642_1">
   <g id="svg_75642_2">
    <g stroke="rgb(0.0%,0.0%,0.0%)" id="svg_75642_3">
     <g fill="rgb(0.0%,0.0%,0.0%)" id="svg_75642_4">
      <g stroke-width="0.4pt" id="svg_75642_5">
       <g id="svg_75642_6"/>
       <g id="svg_75642_7">
        <g id="svg_75642_8">
         <g id="svg_75642_9">
          <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_10">
           <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_11">
            <g stroke-width="2.0pt" id="svg_75642_12">
             <g id="svg_75642_13">
              <g id="svg_75642_14">
               <g transform="matrix(1, 0, 0, -1, 0, -115.306)" id="svg_75642_15">
                <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_16">
                 <text transform="matrix(1, 0, 0, -1, 84, -242)" text-anchor="middle" font-size="10" id="svg_75642_17" y="-4.0977" x="-9.08893"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g id="svg_75642_18">
         <g id="svg_75642_19">
          <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_20">
           <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_21">
            <g stroke-width="2.0pt" id="svg_75642_22">
             <g id="svg_75642_23">
              <g id="svg_75642_24">
               <g transform="matrix(0.30902, -0.95107, -0.95107, -0.30902, 40.5906, -144.797)" id="svg_75642_25">
                <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_26">
                 <text transform="matrix(1, 0, 0, -1, -204.196, -154.668)" text-anchor="middle" font-size="10" id="svg_75642_27" y="-9.91021" x="1.08848"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g id="svg_75642_28">
         <g id="svg_75642_29">
          <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_30">
           <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_31">
            <g stroke-width="2.0pt" id="svg_75642_32">
             <g id="svg_75642_33">
              <g id="svg_75642_34">
               <g transform="matrix(-0.80902, -0.58778, -0.58778, 0.80902, 25.0861, -192.514)" id="svg_75642_35">
                <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_36">
                 <text transform="matrix(1, 0, 0, -1, -210.201, 146.41)" text-anchor="middle" font-size="10" id="svg_75642_37" y="-2.02719" x="9.76166"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g id="svg_75642_38">
         <g id="svg_75642_39">
          <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_40">
           <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_41">
            <g stroke-width="2.0pt" id="svg_75642_42">
             <g id="svg_75642_43">
              <g id="svg_75642_44">
               <g transform="matrix(-0.80902, 0.58778, 0.58778, 0.80902, -25.0861, -192.514)" id="svg_75642_45">
                <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_46">
                 <text transform="matrix(1, 0, 0, -1, 74.2852, 245.157)" text-anchor="middle" font-size="10" id="svg_75642_47" y="8.65743" x="4.9446"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g id="svg_75642_48">
         <g id="svg_75642_49">
          <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_50">
           <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_51">
            <g stroke-width="2.0pt" id="svg_75642_52">
             <g id="svg_75642_53">
              <g id="svg_75642_54">
               <g transform="matrix(0.30902, 0.95107, 0.95107, -0.30902, -40.5906, -144.797)" id="svg_75642_55">
                <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_56">
                 <text transform="matrix(1, 0, 0, -1, 256.11, 5.1069)" text-anchor="middle" font-size="10" id="svg_75642_57" y="7.37776" x="-6.70566"/>
                </g>
               </g>
              </g>
             </g>
            </g>
           </g>
          </g>
         </g>
        </g>
        <g id="svg_75642_58">
         <g stroke="rgb(100.0%,0.0%,0.0%)" id="svg_75642_59">
          <g fill="rgb(100.0%,0.0%,0.0%)" id="svg_75642_60">
           <g stroke-width="2.0pt" id="svg_75642_61">
            <path d="m74.911072,79.916748m2.207169,44.886215c33.106552,33.106613 61.056396,12.800827 38.38343,-31.697487c-5.668228,-11.124565 -13.551338,-35.385445 -15.016228,-44.634148m17.797394,43.216988c41.717148,-21.255791 31.040665,-54.112576 -18.285698,-46.299858c-12.331566,1.953182 -37.840569,1.953182 -47.089268,0.488281m46.600918,-3.571201c-7.324356,-46.243438 -41.871078,-46.243438 -49.683781,3.08292c-1.953197,12.331573 -9.8363,36.592453 -14.087509,44.935829m11.00457,-45.424076c-46.243429,-7.324471 -56.919909,25.532314 -12.4216,48.205265c11.124573,5.668251 31.762173,20.661942 38.383503,27.283272m-39.800533,-24.502029c-21.255939,41.717072 6.693913,62.022858 42.007633,26.709129c8.82843,-8.82843 29.466042,-23.822121 37.809471,-28.07325" fill="none" id="svg_75642_62"/>
           </g>
          </g>
         </g>
        </g>
       </g>
       <g id="svg_75642_63"/>
      </g>
     </g>
    </g>
   </g>
  </g>
  <foreignObject x="52" y="20.32608" id="svg_75642_64" font-size="16" width="48" height="20">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>a</mi>
     </mrow>
     <annotation encoding="application/x-tex">a</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="99" y="48" font-size="16" width="48" height="20" id="svg_75642_65">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>b</mi>
     </mrow>
     <annotation encoding="application/x-tex">b</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="83" y="108" font-size="16" width="48" height="20" id="svg_75642_71">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>c</mi>
     </mrow>
     <annotation encoding="application/x-tex">c</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="21" y="108" font-size="16" width="48" height="20" id="svg_75642_77">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>d</mi>
     </mrow>
     <annotation encoding="application/x-tex">d</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="5" y="48" font-size="16" width="48" height="20" id="svg_75642_83">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>e</mi>
     </mrow>
     <annotation encoding="application/x-tex">e</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="52" y="69.32608" font-size="16" width="48" height="20" id="svg_75642_89">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>f</mi>
     </mrow>
     <annotation encoding="application/x-tex">f</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject x="5" y="13.32608" font-size="16" width="48" height="20" id="svg_75642_95">
   <math xmlns="http://www.w3.org/1998/Math/MathML" display="inline">
    <semantics>
     <mrow>
      <mi>g</mi>
     </mrow>
     <annotation encoding="application/x-tex">g</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>

</svg>
=--

We start with the crossing in the top left. The underpass is going from left to right and has $a$ to its left as it exits from under the overpass. Reading off the relation for this we get $a g^{-1} e f^{-1}$. We go to the next (clockwise) crossing and similarly get $b g^{-1} a f^{-1}$; continuing we get $c g^{-1} b f^{-1}$, then $d g^{-1}c f^{-1}$, and for the final crossing $e g^{-1}d f^{-1}$.

We will choose to kill off $g$ setting it equal to $1$ (and eliminating it from the presentation). This gives 

$$\langle a,b,c,d,e,f \mid b a f^{-1}=c b f^{-1}= d c f^{-1}=e d f^{-1}=a e f^{-1}=1\rangle.$$


This is 'the' **Dehn presentation** of $G(K)$ for this knot

We can eliminate $f$ as it can be expressed in terms of the other generators.  This gives us

$$\langle a,b,c,d,e\mid b a = c b =d c= e d = a e\rangle.$$

This corresponds to something neat.  The 'geometric' significance of the faces is they represent a path that starts above the 'page' goes down through that face then comes up through the face labelled $g$ (as we set that equal to $1$). The presentation in its current form shows that going down through any of the lobes, coming back up at the outside, then going down through the next one clockwise is the same as going through the middle! It can be useful to keep $f$ in the presentation as we will see.

This group presentation is [[Tietze transformation|Tietze equivalent]] to $\langle f,y\mid f^5 = y^2\rangle$. (Use the substitution $y=e d c b a$.)  Note that the nature of the cinquefoil as a (2,5)-[[torus knot]] can be seen in this presentation.

##The Wirtinger presentation##
To  get the Wirtinger presentation of $G(K)$, you label the arcs of the knot diagram rather than the faces. The arc labels will give the generators in this presentation and the crossings will give the relations.  

Suppose the crossing looks like

+-- {: style="text-align:center"}
<svg width="214" height="214" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="63639">
 <g>
  <title>Layer 1</title>
  <line marker-end="url(#se_marker_end_svg_75641_1)" id="svg_75641_1" y2="12" x2="102" y1="212" x1="102" stroke-width="4" stroke="#7f0000" fill="none"/>
  <rect id="svg_75641_3" height="17" width="43" y="104" x="81" stroke-width="0" stroke="#7f0000" fill="#ffffff"/>
  <line marker-end="url(#se_marker_end_svg_75641_2)" id="svg_75641_2" y2="112" x2="202" y1="112" x1="2" stroke-width="4" stroke="#7f0000" fill="none"/>
  <foreignObject height="50" width="50" font-size="20" id="svg_75641_4" y="80" x="20">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>i</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_i</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_75641_5" height="50" width="50" font-size="20" y="40" x="95">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>j</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_j</annotation>
    </semantics>
   </math>
  </foreignObject>
  <foreignObject id="svg_75641_21" height="50" width="50" font-size="20" y="140" x="95">
   <math display="inline" xmlns="http://www.w3.org/1998/Math/MathML">
    <semantics>
     <mrow>
      <msub>
       <mi>x</mi>
       <mi>k</mi>
      </msub>
     </mrow>
     <annotation encoding="application/x-tex">x_k</annotation>
    </semantics>
   </math>
  </foreignObject>
 </g>
 <defs>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_75641_1">
   <path stroke-width="10" stroke="#7f0000" fill="#7f0000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_63639_1"/>
  </marker>
  <marker refY="50" refX="50" markerHeight="5" markerWidth="5" viewBox="0 0 100 100" orient="auto" markerUnits="strokeWidth" id="se_marker_end_svg_75641_2">
   <path stroke-width="10" stroke="#7f0000" fill="#7f0000" d="m100,50l-100,40l30,-40l-30,-40l100,40z" id="svg_63639_2"/>
  </marker>
 </defs>
</svg>
=--

Pick one of the quadrants and think of a rectanglar path going anti-clockwise about the crossing.  (We will assume we have started this path in the NW quadrant, to the left of the exit.) 
Traverse this rectangular path and write down the $\text{arc label}$ if the arc is entering the crossing and $(\text{arc label})^{-1}$ if it is leaving it.  In the above situation we get $x_i  x_k x_i^{-1} x_j^{-1}$.  This is set equal to $1$. Now repeat for all the other crossings.

The **Wirtinger presentation** is then

$$\langle \text{arc labels} \mid \text{crossing relations}\rangle$$

It is worth noting that any one of the crossing relations is a consequence of the others.

The element in the fundamental group corresponding to a strand is the following.  We fix a basepoint above the plane.  The path comes down from this basepoint, goes under the strand, and then back up again.  The direction in which it goes under the strand is determined by the orientation of the strand: to someone sitting on the strand facing in the direction of the orientation, the path will go down on the left and come up on their right.

**Hint:** If doing an example, do not throw away a crossing relation just because it is redundant.  It is a good idea to keep it and it will act as a check on the final form of the presentation when it has been 'processed' through some Tietze transformations. It is easy, at least to start with, to make a slip in the calculation and often the presentation for nice simple knots can be reduced to a form with two generators and one relation.  The above trick keeps in a duplicate relation for comparison.

##Related entries

The classical treatment of the [[Alexander polynomial]] as found, for instance in the book by [[Crowell]] and [[Ralph Fox|Fox]], uses the Wirtinger presentation and [[Fox derivatives]] to derive an Alexander matrix which is then processed to give the polynomial.

Alexander's original paper uses a method which is more closely related to the Dehn presentation.



category: knot theory