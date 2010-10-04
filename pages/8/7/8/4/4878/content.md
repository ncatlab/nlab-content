## Signs of crossings

In an oriented diagram, we can see there are two types of possible crossing. They are allocated a sign, + or -. 

(Diagram to go here) 
One method of remembering the sign convention is to imagine an approach to the crossing along the *underpass* in the direction of the orientation: 

* if the overpass passes from left to right the crossing is counted as being *positive*;
* if it passes from right to left it counts as *negative*.

## Writhe
 

The *writhe* of an oriented *knot* or *link* diagram is the sum of the signs of all its crossings.  If $D$ is the diagram, we denote its writhe by $w(D)$.

The writhe is used in the definition of some of the [[knot invariants]].

##Linking number
This is a variant of the writhe that is adapted for use with links. 

Suppose we have an oriented link diagram $D$ with components $C_1, \ldots, C_m$, the *linking number* of $C_i$ with $C_j$ where $C_i$ and $C_j$ are distinct components of $D$, is to be one half of the sum  of the signs of the crossings of $C_i$ with $C_j$; it will be denoted $lk(C_i,C_j)$.

The linking number of the diagram $D$ us then the sum of the linking numbers of all pairs of components:

$$Lk(D) = \sum_{1\le i\lt j\le m}lk(C_i,C_j).$$