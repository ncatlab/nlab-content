
###An example illustrating some of the ideas of [[shape theory]]###


A space  may have very little separating it from 'manifoldness', yet a 'singularity' can cause havoc! The simple example, here, is known as the __Warsaw Circle__ as it was studied extensively by K. Borsuk and his Polish collaborators, cf. Borsuk's book (referenced below.)

The Warsaw circle $S_W $ is the subset of the plane, $\mathbb{R}^2$, specified by

$$\{(x,\sin(\frac{1}{x}) \mid -\frac{1}{2\pi} \lt x \leq \frac{1}{2\pi}, x \neq 0\}\cup \{(0,y) | -1 \leq y \leq 1\} \cup C,$$ 
where $C$ is an arc in $\mathbb{R}^2$ joining $(\frac{1}{2\pi}, 0)$ and $(-\frac{1}{2\pi}, 0)$, disjoint from the other two subsets specified above except at its endpoints.

It looks something like [[warsaw.pdf|this:file]].

**Note** There is a variant version with no $(x,\sin(\frac{1}{x}))$-bit for the $x\lt 0$ and the curve $C$ joins $(0,0)$ to $(\frac{1}{2\pi}, 0)$.  The discussion adapts very easily to that.

It is a compact metric space, but is not locally connected along the line  corresponding to $\{(0,y) \mid -1 \leq y \leq 1\} $, so is not a manifold, nor for that matter a polyhedron.  It is connected, but not pathwise connected as no path can get out from the 'line'. We note

* $\pi_0(S_W)$ is two points;

* $\pi_1(S_W)$ is trivial at any base point.

There is a simple continuous map from $S^0$, the 0-circle, $\{-1,1\}$, to $S_W$ which is a weak homotopy equivalence. (For instance define $f(-1) = (0,0)$ and $f(1)$ to be any point in the outer $sin(1/x)$ part of the space, it does not matter which one.)  This is not a homotopy equivalence. (In fact it is instructive to look at maps from $S_W$ to $S^0$!  It does not take long.)

 A striking thing about the picture is that it 'clearly' divides the plane into two components, an inside and an outside, and has a definite sense of being 'almost' a circle. It has a line of singularities, but otherwise ... .


If we consider, not just $S_W$ as a compact metric space, but as a subspace of the plane, then we can take small open neighbourhoods of $S_W$, to be definite take 

$$N_{\frac{1}{n}}(S_W) = \{ \underline{x}\in \mathbb{R}^2 | d(\underline{x},S_W) \lt \frac{1}{n}\}.$$  

This looks like an annulus with a thickenning at one small section. It has the homotopy type of a circle. If $N \gt n$, $N_{\frac{1}{N}}(S_W)\subset N_{\frac{1}{n}}(S_W)$, of course, (we will write $i^N_n$ for this map, and this is a homotopy equivalence. The Warsaw circle, $S_W$, is clearly the intersection of all these almost annular neighbourhoods. (Note, also clearly, that the complements  of these neighbourhoods are gradually occupying more and more of the two components of $\mathbb{R}^2- S_W$.)

We have a inverse system ([[pro-object]]) of spaces all of which have the homotopy type of a polyhedron, ... in fact always the same polyhedron, $S^1$.  Note that by our use of a specific [[cofinal]] family of neighbourhoods of $S_W$, indexed by the natural numbers, we have an _inverse sequence_. That was a choice and we could have chosen differently or not at all. The ability to pick a sequence of neighbourhoods is related to the fact that we are considering a **compact metric space**. 

Another point to note is that not only is each of the neighbourhoods homotopic to $S^1$, but the inclusion maps making up the 'bonds' of the inverse sequence, are homotopy equivalence.  This is a particularity of $S_W$ and other examples, such as the [[solenoid]]s need not have this 'stability' property.  The Warsaw circle is an example of what is called a [[stable space]].  

####A (Borsuk) shape map $f: S^1 \to S_W$####


There is a sequence of maps, $\{f_n : S^1 \to N_{\frac{1}{n}}(S_W)\mid n\in \mathbb{N}\}$, so that for each pair, $(n,N)$, with $N\gt n$, there is a homotopy $f_n \sim i^N_n f_N$. This makes a (Borsuk) shape map from the circle to the Warsaw circle.  Each $f_n$ is in fact a homotopy equivalence and we can use a choice of homotopy inverses to get another shape map $g : S_W\to S^1$ and these make up a **shape equivalence**.

(A more detailed description of shape maps and shape equivalences in the Borsuk version of shape theory, is given in the entry [[Borsuk shape theory]]. The version given here skates over some points.  It is, in fact, near the ANR-systems approach to shape.)


####The Warsaw circle from a &#268;ech point of view####
To get $\check{C}(S_W,-)$ &#268;ech nerve complex of $S_W$, (see [[Čech methods]]), we can calculate $\check{C}(S_W,\alpha)$ for an arbitrary open cover $\alpha$ of $S_W$, but we need not do that (in fact that is a silly thing to do!).  We first note that $S_W$ is compact so we need only consider finite open covers, as these form a cofinal subcategory of the category of all open covers. ('Cofinal subcategory' means that its inclusion into the bigger category is a [[cofinal functor]].)

Next we look at any finite open cover and note that it has a refinement in the form of open balls of radius $\frac{1}{n}$, in other words we can restrict to (well chosen) such covers, giving a countable family of open covers that have to be worked with.

For such open covers the nerve will look a bit like [[circle.pdf|this:file]]. There may be fine detail in the rectangle depending on the choice of cover, but that detail will disappear as one passes to finer and finer scales. (New holes may occur, but again going finer those disappear.) Cofinally it looks like  a space obtained by adding in a thin rectangle transverse to a circle at one small segment. For different open coverings, the only difference will be where the region of attachment (marked $*$) will occur and the relative thinness of the rectangle.  The line of singularities given by the interval $[-1,1]$ on the $y$-axis cannot be 'observed', of course.  If one passes to finer and finer covers, most of the curve does not change appreciably. It just gets subdivided,  but the part near $*$ will lengthen, 'spawning' a very large number of new vertices.

There are two important points to note:

* (essentially) each $\check{C}(S_W,\alpha)$ has the homotopy type of a circle

*  the transition maps, $C(S_W,\alpha)\to C(S_W,\beta)$, will be (cofinally) homotopy equivalences.

(With a bit more care in the choice of the covers these can be made exact statements, not just 'essentially' or cofinally true.)


We note that there are obvious maps of pro-objects $\check{C}(S^1,-)\to \check{C}(S_W,-)$, and back again.  These give an isomorphism in $pro-Ho(sSets)$.  This is the &#268;ech homotopy versions of the observations made for Borsuk's shape  above.

## References

* K. Borsuk, _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.


[[!redirects Warsaw circle]]
[[!redirects Warsaw Circle]]
