
# Contents
* table of contents
{: toc}

## Idea

A [[map]] $f$ between [[spaces]] (say, a [[continuous map]] between [[topological spaces]]) _vanishes at infinity_ if $f(x)$ gets arbitrarily close to [[zero]] as $x$ gets sufficiently close to infinity.

For a map $f\colon X \to Y$, we need a notion of being close to $0$ in $Y$, so take $Y$ to be a [[pointed space]]; then getting arbitrarily close to $0$ means entering any [[neighbourhood]] of the basepoint.  We also need a notion of being close to infinity in $X$, so take $X$ to be a [[locally compact Hausdorff space]]; then getting sufficiently close to infinity means entering the [[exterior]] of some [[compact subspace]].  (To interpret 'getting', of course, we may use [[nets]].)  It is likely, however, that further generalisations are possible.


## Definitions

Let $X$ and $Y$ be [[topological spaces]], and let $f$ be a [[continuous map]] (or potentially any [[function]]) from $X$ to $Y$.  Let $Y$ be [[pointed space|pointed]], and let $X$ be [[locally compact Hausdorff space|locally compact Hausdorff]].

+-- {: .num_defn}
###### Definition
The map $f\colon X \to Y$ __vanishes at infinity__ if for every [[neighbourhood]] $N$ of the [[basepoint]] in $Y$, there is [[compact subspace]] $K$ of $X$ such that $f(x)$ belongs to $N$ whenever $x$ lies in the [[exterior]] of $K$ in $X$.
=--

In case $Y$ is a pointed [[metric space]] (such as a [[Banach space]], with basepoint $0$; or in particular the [[real line]], with basepoint $0$), then we may equivalently say: 

* For every [[positive number]] $\epsilon$, there is [[compact subspace]] $K$ of $X$ such that ${\|f(x)\|} \lt \epsilon$ whenever $x$ lies in the [[exterior]] of $K$ in $X$.

(Here, ${\|{-}\|}$ is the [[norm]] in a Banach space, or more generally the distance from the basepoint in any pointed metric space.)


## Properties 

### Relation to compactifications

One way of considering this definition is that one can adjoin to $X$ a point "at infinity", denoted $\infty$, by declaring that the [[open neighborhoods]] of $\infty$ are sets of the form $\{\infty\} \cup Ext(K)$ for $K \subset X$ compact. This is called the [[one-point compactification]], denoted $X^{cpt}$. Then a [[continuous function]] $f \colon X \to A$ vanishes at infinity equivalently if it [[extension|extends]] $f$ to a map $X^{cpt} \to A$, continuous at $\infty$ (at least) that sends $\infty$ to $0$ -- thus _literally- "vanishing at $\infty$". 

In view of this equivalence, we may say that for locally compact $X$, the vector space of functions $X \to \mathbb{C}$ that vanish at $\infty$, denoted $C_0(X)$, is isomorphic to the kernel of the evaluation map 

$$ev_\infty: [X^{cpt}, \mathbb{C}] \to \mathbb{C}$$ 

from the [[function space]] on $X^{cpt}$, with pointwise defined $C^\ast$-algebra structure and the sup-norm topology. 

+-- {: .num_prop #FunctionsVanInftyAreCstar}
###### Proposition
$C_0(X)$ is a $C^\ast$-algebra. 
=--

\begin{proof} 
Since the function space is a $C^\ast$-algebra and $C_0(X) \cong \ker(ev_\infty)$ is a closed subspace, and thus a Banach space, and since the $C^\ast$-algebra structure on $[X^{cpt}, \mathbb{C}]$ clearly restricts to a $C^\ast$-algebra structure on the kernel, the result is clear. 
\end{proof} 


For more see 

* at _[[one-point compactification]] -- [Relevance for Monopoles and Instantons](one-point+compactification#RelevanceForMonopolesAndInstantons)_


* at _[Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_.




## References

* Wikipedia, _[Locally compact space](http://en.wikipedia.org/wiki/Locally_compact_space)_


[[!redirects vanishing at infinity]]
[[!redirects vanish at infinity]]
[[!redirects vanishes at infinity]]
