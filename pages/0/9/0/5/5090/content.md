
#Contents#
* table of contents
{:toc}

##The Knot Group of  Knot##
The **knot group**, $G(K)$, of a knot $K$ is the [[fundamental group]] of the complement of the knot.  Taking this apart, the knot, $K$, is an embedding of $S^1$ into $\mathbb{R}^3$ or $S^3$. We tend to abuse terminology and to think (and write) of $K$ as  the image of the embedding rather than the embedding itself. (If you perform an ambient [[isotopy]] on the knot then it deforms this complement into the complement of the isotopic knot.) . We can therefore write $\mathbf{R}^3-K$ for the space outside the knot, i.e. its complement.  This is clearly arcwise connected so we do not need to worry about a choice of base point any point will do.  We make the 
+--{: .un_defn}
######Definition######
$G(K) := \pi_1(\mathbf{R}^3-K)$.

=--

This is fine, but does not tell us how to calculate anything about this group for a given knot. Luckily there are two neat algorithms for giving [[group presentation|presentations]] of $G(K)$ for arbitrary knots, one due to Wirtinger, the other to Dehn.

##The Dehn Presentation##
Orient the knot diagram.  that diagram will divide the plane into various faces.  Label these faces with distinct letters. We will use $x_1,\ldots, x_n$. (These face labels will be the generators in the presentation.)  

For the relations, we get one such for each crossing
  A typical crossing will have a configuration something like this:

(DIAGRAM TO GO HERE)

Look at the underpass arc that leaves the crossing, and write down the face labels going anticlockwise around the crossing, and alternating in exponent between +1 and -1.  Here that give $x_i x_j^{-1}x_k x_l^{-1}$.  Finally set any _one_ face label, say, $x_m$, to be 1. (This last relation effectively deletes $x_m$ from the presentation.)

That gives the presentation $\langle x_1, \ldots, x_n\mid relations from crossings, x_m=1\rangle$.  This is a presentation of $G(K)$.