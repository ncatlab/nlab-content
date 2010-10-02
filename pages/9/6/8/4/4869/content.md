+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Contents### {: .clickToReveal}
###Contents### {: .clickToHide tabindex="0"}
+--{: .hide}
[[!include knot theory - contents]]
=--
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--

# Bridge number
* table of contents
{: toc}

## Definitions

A __bridge__ in a [[knot diagram]] is an arc that is the overpass in at least one crossing.

The __bridge number__, $b(K)$ of a [[knot]] $K$ is the minimum number of bridges occuring in a diagram of the knot.

By convention the [[unknot]] has bridge number equal to $1$.

+-- {: .query}
Why not $0$?  (I don\'t see any bridges in the obvious diagram.)  Are there numerical operations on bridge numbers that only work for the unknot if its bridge number is $1$?  Can we motivate the existence of a bridge in the unknot by proper application of [[negative thinking]]?
=--


## Example

The usual picture of the trefoil knot, which we will write as $T_{2,3}$,
has three bridges, but the trefoil knot actually has bridge number 2, as shown:

<svg width="473" height="436" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="10729">
 <g>
  <title>Layer 1</title>
  <path transform="rotate(-120, 259.402, 127.805)" id="svg_10729_17" d="m113.11998,8.914688c6.583008,0.083008 127.167007,1.166992 133.750015,1.25c6.583008,0.083008 30.578491,-0.904808 72.75,1.25c42.171509,2.154816 81.237549,34.19458 85.766724,77.116028c4.529175,42.921463 -44.09137,117.568939 -75.142334,142.410263c-31.050964,24.841339 -96.234955,21.666977 -116.87439,-19.276291c-20.639435,-40.943283 -8.833008,-16.833023 -32.25,-59.75" stroke-width="6" stroke="#bf0000" fill="none"/>
  <path id="svg_10729_19" d="m177.119568,194.914703c6.583008,0.083008 127.166992,1.167007 133.75,1.25c6.583008,0.083008 30.578979,-0.904785 72.75,1.25c42.171997,2.154816 81.237976,34.194611 85.767029,77.115997c4.528931,42.921509 -44.091064,117.568604 -75.142029,142.410614c-31.050995,24.841003 -96.235016,21.666992 -116.875,-19.277008c-20.639008,-40.942902 -8.833008,-16.833008 -32.25,-59.749603" stroke-width="6" stroke="#bf0000" fill="none"/>
  <path id="svg_10729_20" transform="rotate(120, 128.403, 274.805)" d="m-17.880432,155.914703c6.582993,0.083008 127.166992,1.167007 133.75,1.25c6.583008,0.083008 30.578979,-0.904785 72.75,1.25c42.171997,2.154816 81.238007,34.194611 85.767029,77.116013c4.528931,42.921494 -44.091034,117.568588 -75.142029,142.410599c-31.050995,24.841003 -96.235016,21.666992 -116.875,-19.277008c-20.639008,-40.942902 -8.833008,-16.833008 -32.25,-59.749603" stroke-width="6" stroke="#bf0000" fill="none"/>
 </g>
</svg>

<svg width="348" height="311" xmlns="http://www.w3.org/2000/svg" xmlns:se="http://svg-edit.googlecode.com" se:nonce="55496">
 <g>
  <title>Layer 1</title>
  <path id="svg_55496_1" d="m190.78125,51.75c25.416656,-34.25 30.833344,-48.5 72.25,-48.75c41.416656,-0.25 80.833313,64.5 82.25,156.25c1.416687,91.75 -28.166656,145.5 -82.75,148.25c-54.583344,2.75 -117.083313,-42.5 -124.375,-97.375c-7.291687,-54.875 41.416687,-88.75 73.625,-57.375" stroke-width="6" stroke="#00bfbf" fill="none"/>
  <path id="svg_55496_3" d="m158.78125,168.75c22.583313,34.083328 56.166687,9.166672 69.75,-34.75c13.583313,-43.916672 -76.833344,-120.833313 -133.25,-119.75c-56.416656,1.083313 -93.541672,70.208344 -92.25,138.25c1.291672,68.041656 35.083313,152.083344 77.875,153.125c42.791687,1.041656 52.583344,-12.916687 74.875,-32.875" stroke-width="6" stroke="#00bfbf" fill="none"/>
  <path id="svg_55496_4" d="m181.78125,65.75c-14.666656,25.333336 -61.333344,53.666672 -38,84" stroke-width="6" stroke="#00bfbf" fill="none"/>
  <path id="svg_55496_5" d="m225.78125,165.75c38.333344,33.333328 -37.333344,63.666672 -55,93" stroke-width="6" stroke="#00bfbf" fill="none"/>
 </g>
</svg>

The first drawing corresponds to the picture as a (2,3)-[[torus knot]]. The knot thus can be represented on the surface of a solid torus $S^1\times D^2$ in $S^3$. The 3-sphere can be represented as the union of two solid tori with, in this case, the second one being $D^2\times S^1$, where the boundary of the $D^2$ in each case is the corresponding $S^1$ of the other case. Thinking of the trefoil on this other solid torus it is a $(3,2)$-torus knot .... (the second picture) and this has just two bridges, so $b(T_{2,3})\leq 2$.

How does one know that the trefoil does not have $b(K) = 1$.  For that we use
+-- {: .un_proposition}
###### Proposition

A knot $K$ has $b(K) = 1$ if and only if $K$ is the unknot.
=--

To complete the proof one needs to show or know that the trefoil is a non-trivial knot. That is most simply done using some invariant such as 3-[[n-colorability|colorability]].

+-- {: .un_proposition}
###### Proposition

The bridge number is a [[knot invariant]].
=--
This is more or less 'by default' as $b(K)$ is defined as a minimum over all [[knot diagram|knot diagrams]].

#####Remark:

Why is there the convention  that $b(unknot)= 1$? There is a neat result that means that if you know bridge number for [[prime knot|prime knots]] then you can (theoretically) calcuate t for all composite knots. This states the following:
+-- {: .un_proposition}
###### Proposition

Let $K$ and $L$ be two (oriented) knots, and let $K+L$ be their oriented [[knot sum|sum]], then 
$$b(K+L) = b(K) + b(L) -1.$$
=--
The proof is not hard. As '$K$ + unknot = $K$', the formula would be false if either knot was the unknot, if, that is, we had the other possible convention, (i.e. that the bridge number of the unknot should be 0). (There are other deeper reasons for the convention, but this is a neat one.)

(The pictures of the trefoil on this page are based on [[two-trefoils.pdf|this picture of two trefoils:file]] from the [Maths and Knots Exhibition website](http://www.popmath.org.uk/exhib/knotexhib.html), of the Centre for the Popularisation of Mathematics. Their assistance is gratefully acknowledged.)
[[!redirects bridge number]]
[[!redirects bridge numbers]]
