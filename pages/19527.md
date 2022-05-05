
##Idea

The Cayley graph, also called the Cayley quiver, of a group, $G$ with a given set of generators, $X$, encodes how the chosen generating elements operate (by multiplication)  on the elements of the group.



##Definition

Given a group, $G$, and a set of generators, $X$, which we assume form a subset of $|G|$, we can form a graph with the elements of $G$ as the vertices. The edges of the graph will be directed and will be labelled (some people say 'coloured')  by the elements of $X$ with an edge joining a vertex, $g$, to the vertex $g x$ labelled by $x$.


This graph is called the _Cayley graph_ of the group, $G$, relative to the set of generators.

##Example 

Consider one of the standard presentations of $S_3$, $ (a,b  :  a^3, b^2, (ab)^2)$. Write $ r = a^3$, $s = b^2$, $t = (ab)^2$.  

The Cayley graph is easy to draw.  There are two triangles corresponding to $1\to a\to a^^2$ and its translate by $b$ flipping the orientation, and three 2-cycles, $1\to b\to 1$, $a\to ab\to a$ and $a^2\to a^2b\to a^2$.

Looking at the presentation it leads to a free group, $F$, on the generators, $a$ and $b$, so $F$ is free of rank 2, but the normal closure of the relations $N(R)$ is a subgroup of $F$, so it must be
free as well, by the [[Nielsen-Schreier theorem]].  Its rank will be 7, given by the [[Nielsen index formula]].

This can also be seen geometrically, as it will be the [[fundamental group]] of the Cayley quiver, also called the  Cayley graph, of the
presentation.  This group is free on generators corresponding to edges outside 
a maximal tree, and , of course, there are 7 of these.

[[!redirects Cayley quiver]]