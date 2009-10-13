
## Description ##

The Whitehead tower of a pointed space $(X,x)$ is a sequence of fibrations 
$$
\ldots \to X\langle n\rangle \to \ldots \to X\langle 1 \rangle \to X\langle 0 \rangle \to X
$$
where each $X\langle n\rangle \to X\langle n-1 \rangle$ induces isomorphisms on $pi_i$ for $i\gt n$ and such that $X\langle n\rangle$ is $n$-connected. For $n=0$ we require that $X\langle 0 \rangle \to X$ is the inclusion of the path-component of $x$. Really this is defined up to homotopy, but we have a canonical model. If $X$ is locally connected and semilocally path-connected, then $X\langle 1\rangle$ can be chosen as the [[universal covering space]]. 

In traditional models this construction is highly non-functorial, except for nice spaces in low dimensions as remarked above. 

## Construction ##

Killing homotopy groups, path fibration etc.

## Non-traditional approaches ##

**The following is some semblance of current research, except the stuff about the string 2-group. All errors and stupid ideas are mine - David Roberts**

For locally nice spaces (say locally contractible), it is desirable to have a functorial construction of the Whitehead tower. A shadow of a low-dimensional case of this can be seen in the constuction of the [[string 2-group]] given by Baez-Crans-Schreiber-Stevenson. Since finite-dimensional Lie groups have non-trivial third homotopy group, it is not possible to form the 3-connected cover in the category $fin.dim.LieGrp$, like it is possible to take the 0-, and 1-connected covers. While most people give up the smoothness and make do with the topological group $String_G$, The BCSS construction leaps out of that category into that of strict (Frechet) Lie 2-groups. The construction is also functorial.

As an aside, I know of two classes of spaces with explicitly  constructed (i.e. not via killing homotopy groups) 2-connected covers: the 2-sphere and its quotients by $\mathbf{Z}/n$ (lens spaces), and the loop group $\Omega G$ of a compact, simple, simply-connected Lie group $G$ (the latter is the level-1 central extension by $U(1)$, the first needs no introduction).

However, without one could demand a conceptually similar approach to the $n$-connected cover of a general (locally nice) space or smooth manifold. For $n=2$, and taking only topological spaces for consideration, this is contained in [[David Roberts|my]] thesis work.
The rough result is that one gets a 2-connected topological groupoid $X^{(2)}$ equipped with a map to $X$ that factors through the universal covering space $X^{(1)}$. This is functorial, and generalises to higher connected covers (at least heuristically - I don't have $n$-categorical superpowers).

But the general idea is that one would get an $(n-1)$-groupoid $X^{(n)}$ over $X$ which is $n$-connected and such that the map to $X$ factors through the $(n-2)$-groupoid $X^{(n-1)}$. The map to $X$ should induce isomorphisms on homotopy groups $\pi_i$ for $i\gt n$, as in the usual Whitehead tower.

---
&lt;http://mathoverflow.net/questions/5268/functorial-whitehead-tower>

nLab page on [[nlab:Whitehead tower]]
