A space  may have very little separating it from `manifoldness', yet a `singularity' can cause havoc! The simple example, here, is known as the __Warsaw Circle__ as it was studied extensively by K. Borsuk and his Polish collaborators, cf. Borsuk's book (referenced below.)

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


If we consider, not just $S_W$ as a compact metric space, but as a subspace of the plane then we can take small open neighbourhoods of $S_W$, to be definite take 

$$N_{\frac{1}{n}}(S_W) = \{ \underline{x}\in \mathbb{R}^2 | d(\underline{x},S_W) \lt \frac{1}{n}\}.$$  
