

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Knot theory
+--{: .hide}
[[!include knot theory - contents]]
=--
=--
=--


# Bridge number
* table of contents
{: toc}

## Definitions

A __bridge__ in a [[knot diagram]] is an arc that is the overpass in at least one crossing.

The __bridge number__, $b(K)$ of a [[knot]] $K$ is the minimum number of bridges occurring in a diagram of the knot.

By convention the [[unknot]] has bridge number equal to $1$.

Almost by default this gives a knot invariant as it takes the minimum over all [[knot diagram|knot diagrams]] that represent the isotopy class of the knot. (There is some work to do, but this is left for the moment!)

## Example

The usual picture of the trefoil knot, which we will write as $T_{2,3}$,
has three bridges, but the trefoil knot actually has bridge number 2, as shown:

<table>
<tr>
<td>
[[!include trefoil knot - SVG]]
</td>
<td>
[[!include trefoil knot (2 bridge) - SVG]]
</td>
</tr>
</table>

The first drawing corresponds to the picture as a (2,3)-[[torus knot]]. The knot thus can be represented on the surface of a solid torus $S^1\times D^2$ in $S^3$. The 3-sphere can be represented as the union of two solid tori with, in this case, the second one being $D^2\times S^1$, where the boundary of the $D^2$ in each case is the corresponding $S^1$ of the other case. Thinking of the trefoil on this other solid torus it is a $(3,2)$-torus knot .... (the second picture) and this has just two bridges, so $b(T_{2,3})\leq 2$.

*How does one know that the trefoil does not have $b(K) = 1$?*  

For that we use
+-- {: .un_proposition}
###### Proposition

A knot $K$ has $b(K) = 1$ if and only if $K$ is the unknot.
=--

To complete the proof that $b(trefoil)= 2$, one needs to show or know that the trefoil is a non-trivial knot. That is most simply done using some invariant such as 3-[[n-colorability|colorability]].

+-- {: .un_proposition}
###### Proposition

The bridge number is a [[knot invariant]].
=--
This is more or less 'by default' as $b(K)$ is defined as a minimum over all [[knot diagram|knot diagrams]].

#####Remark:
Why is there the convention  that $b(unknot)= 1$? There is a neat result that means that if you know bridge number for [[prime knot|prime knots]] then you can (theoretically) calculate it for all composite knots. This states the following:
+-- {: .un_proposition}
###### Proposition

Let $K$ and $L$ be two (oriented) knots, and let $K+L$ be their oriented [[knot sum|sum]], then 
$$b(K+L) = b(K) + b(L) -1.$$
=--
The proof is not hard. As '$K$ + unknot = $K$', the formula would be false if either knot was the unknot, if, that is, we had the other possible convention, (i.e. that the bridge number of the unknot should be 0). (There are other deeper reasons for the convention, but this is a neat one.)

(The pictures of the trefoil on this page are based on [[two-trefoils.pdf|this picture of two trefoils:file]] from the [Maths and Knots Exhibition website](http://www.popmath.org.uk/exhib/knotexhib.html), of the Centre for the Popularisation of Mathematics. Their assistance is gratefully acknowledged.)
[[!redirects bridge number]]
[[!redirects bridge numbers]]
