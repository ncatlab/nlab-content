
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

 A striking thing about the picture is that it 'clearly' divides the plane into two components, and inside and an outside, and has a definite sense of being 'almost' a circle. It has a line of singularities, but otherwise ... .


If we consider, not just $S_W$ as a compact metric space, but as a subspace of the plane, then we can take small open neighbourhoods of $S_W$, to be definite take 

$$N_{\frac{1}{n}}(S_W) = \{ \underline{x}\in \mathbb{R}^2 | d(\underline{x},S_W) \lt \frac{1}{n}\}.$$  

This looks like an annulus with a thickenning at one small section. It has the homotopy type of a circle. If $N \gt n$, $N_{\frac{1}{N}}(S_W)\subset N_{\frac{1}{n}}(S_W)$, of course, (we will write $i^N_n$ for this map, and this is a homotopy equivalence. The Warsaw circle, $S_W$, is clearly the intersection of all these almost annular neighbourhoods. (Note, also clearly, that the complements  of these neighbourhoods are gradually occupying more and more of the two components of $\mathbb{R}^2- S_W$.)

We have a inverse system ([[pro-object]]) of spaces all of which have the homotopy type of a polyhedron, ... in fact always the same polyhedron, $S^1$.  Note that by our use of a specific [[cofinal]] family of neighbourhoods of $S_W$, indexed by the natural numbers, we have an _inverse sequence_. That was a choice and we could have chosen differently or not at all. The ability to pick a sequence of neighbourhoods is related to the fact that we are considering a **compact metric space**. 

Another point to note is that not only is each of the neighbourhoods homotopic to $S^1$, but the inclusion maps making up the 'bonds' of the inverse sequence, are homotopy equivalence.  This is a particularity of $S_W$ and other examples, such as the [[solenoid]]s need not have this 'stability' property.  The Warsaw circle is an example of what is called a [[stable space]].  

####A (Borsuk) shape map $f: S^1 \to S_W$####


There is a sequence of maps, $\{f_n : S^1 \to N_{\frac{1}{n}}(S_W)\mid n\in \mathbb{N}\}$, so that for each pair, $(n,N)$, with $N\gt n$, there is a homotopy $f_n \sim i^N_n f_N$. This makes a (Borsuk) shape map from the circle to the Warsaw circle.  Each $f_n$ is in fact a homotopy equivalence and we can use a choice of homotopy inverses to get another shape map $g : S_W\to S^1$ and these make up a **shape equivalence**.

(The detailed description of shape maps and shape equivalences in the Borsuk version of shape theory, is given in the entry [[Borsuk shape theory]].)


####The Warsaw circle from a &#268;ech point of view####



## References

* K. Borsuk, _Theory of Shape_, Monografie Matematyczne Tom 59,Warszawa 1975.
