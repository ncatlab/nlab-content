
# Colourability
* table of contents
{: toc}

## Idea

The colourability of a knot tells one information about its [[knot group]] yet has a simple, and visually attractive aspect that seems almost to avoid all mention of groups, presentations, etc., except at a fairly naive level.

The easiest form of colourability to examine is $3$-colourability. 


## $3$-colourability

+--{: .un_defn}
###### Definition
A [[knot diagram]] is _$3$-colourable_ if we can assign colours to its arcs such that

1. each arc is assigned one  colour;

1.  _exactly_ three colours are used in the assignment;

1. at each crossing, either all the arcs have the same colour, or arcs of all three colours meet in the crossing.
=--

+--{: .un_example}
###### Examples
* The usual diagram for the trefoil knot is $3$-colourable. (Just do it! Each arc is given a separate colour and it works.)

* The figure-$8$ knot diagram

[[!include figure 8 knot - SVG]]

is not $3$-colourable. (Try it!)
=--

+--{: .un_theorem}
######Theorem
$3$-colourability is a knot  invariant.
=--

The proof is amusing to work out oneself. You have to show that if a knot diagram $D$ is $3$-colourable and you perform a [[Reidemeister move]] on it then the result is also $3$-colourable. The thing to note is that any arcs that leave the locality of the move must be coloured the same before and after the move is done. 

+--{: .un_note}
###### Notes
*  We can now use phrases such as 'the trefoil knot is $3$-colourable' as its validity does not depend on what diagram is used to represent it, (by the above and by [[Reidemeister moves|Reidemeister's theorem]].) 

* As the trefoil knot is $3$-colourable and the unknot is not, *non-trivial knots exist*.  Moreover, the trefoil is $3$-colourable and the figure $8$ is not, so these are different. We also get that the [[bridge number]] of the trefoil is $2$, as this provides the missing piece of the argument found in that entry.
=--

 There are two comments to make here.  First what does this all mean at a deeper topological level?  The other is : why stop at $3$? What about $n$-colourability? We will handle the second one first.


[[!redirects colorability]]
[[!redirects colourability]]
