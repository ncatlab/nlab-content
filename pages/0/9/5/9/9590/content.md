
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--



# Contents
* table of contents
{: toc}

## Idea

A [[continuous map]] between [[topological spaces]] _vanishes at infinity_ if $f(x)$ gets arbitrarily close to [[zero]] as $x$ gets sufficiently close to [[infinity]].

In order to make sense of this for a map $f\colon X \longrightarrow A$, one:

1. assumes that $A$ is [[pointed topological space|pointed]] by an element $0 \in A$, 

   then getting arbitrarily close to $0$ means entering any [[neighbourhood]] of this [[basepoint]].

1. assumes that $X$ is [[locally compact Hausdorff space|locally compact Hausdorff]], 
 
   then getting sufficiently close to infinity means entering the [[exterior]] $Ext(K)$ of some [[compact subspace]] $K \subset X$.  

Finally "getting close" is understood in terms of [[nets]].


## Definition

Consider:

* $X$ a [[locally compact Hausdorff space]],

* $A$ a [[pointed topological space|point]] [[topological spaces]], with basepoint to be denoted $0 \in A$,

* $f \,\colon\, X \longrightarrow A$ a [[continuous map]].


\begin{definition}\label{TheDefinition}

The [[map]] $f\colon X \to A$ *vanishes at infinity* if for every [[neighbourhood]] $N$ of the [[basepoint]] $0 \in A$, there is a [[compact subspace]] $K$ of $X$ such that for all $x \in Ext(K)$ in the [[exterior]] of $K$, we have $f(x) \in N$.

\end{definition}

\begin{remark}
If $A$ is a pointed [[metric space]] (such as a [[Banach space]], in particular the [[real line]]), then Def. \ref{TheDefinition} is equivalent to:

* For every [[positive number|positive]] [[real number]] $\epsilon$, there is a [[compact subspace]] $K$ of $X$ such that ${\|f(x)\|} \lt \epsilon$ whenever $x$ lies in the [[exterior]] of $K$ in $X$.

Here, ${\|{-}\|}$ denotes the [[distance]] from the basepoint in the metric space, such as the [[norm]] in the case of Banach spaces.

\end{remark}


## Properties 

### Relation to one-point compactification

One may neatly understand Def. \ref{TheDefinition} as saying that a function "vanishes at infinity" if it literally sends "$\infty \mapsto 0$", where  "$\infty$" denotes the point adjoined to $X$ when passing to its "[[one-point compactification]]" $X^{cpt}$ (and demanding that $f$ extends to a continuous function on $X^{cpt}$).

This is achieved by the fact that in $X^{cpt}$ --- whose [[underlying set]] is $X \sqcup \{\infty\}$ --- the [[open neighborhoods]] of $\infty$ are subsets of the form $\{\infty\} \cup Ext(K)$ for compact $K \subset X$. 

Precisely:

\begin{proposition}
\label{CharacterizationViaOnePointCompactification}
A [[continuous function]] $f \colon X \to A$ vanishes at infinity according to Def. \ref{TheDefinition} iff it [[extension|extends]] along $X \hookrightarrow X^{cpt}$ to a continuous map $\widehat{f} \,\colon\, X^{cpt} \longrightarrow A$ such that $\widehat{f}(\infty) = 0$.
\end{proposition}

\begin{remark}
For applications of this equivalence to [[physics]] see:

* at _[[one-point compactification]] -- [Relevance for Monopoles and Instantons](one-point+compactification#RelevanceForMonopolesAndInstantons)_

* at _[Yang-Mills instanton -- SU(2)-instantons from the correct maths to the traditional physics story](Yang-Mills+instanton#FromTheMathsToThePhysicsStory)_.

\end{remark}

### The $C^\ast$-algebra of functions vanishing at infinity

In view of the equivalence of Prop. \ref{CharacterizationViaOnePointCompactification}, we may say that for locally compact $X$, the vector space of [[continuous maps]] $X \longrightarrow \mathbb{C}$ that vanish at $\infty$, denoted $C_0(X)$, is isomorphic to the [[kernel]] of the [[evaluation map]]

$$
  ev_\infty
  \,\colon\, 
  [X^{cpt}, \mathbb{C}] \longrightarrow \mathbb{C}
$$ 

from the [[function space]] on $X^{cpt}$, with pointwise defined [[C-star algebra|$C^\ast$-algebra]] [[structure]] and the [[sup-norm]] [[topological space|topology]]. 

\begin{proposition}
\label{FunctionsVanInftyAreCstar}
$C_0(X)$ is a ([[nonunital algebra|nonunital]]) [[C-star algebra|$C^\ast$-algebra]]. 
\end{proposition}
\begin{proof} 
Since the function space is a $C^\ast$-algebra and $C_0(X) \cong \ker(ev_\infty)$ is a [[closed subspace]], and thus a [[Banach space]], and since the $C^\ast$-algebra structure on $[X^{cpt}, \mathbb{C}]$ clearly restricts to a $C^\ast$-algebra structure on the kernel, the result is clear. 
\end{proof} 

\begin{remark}
$C_0(X)$ is [[nonunital algebra|nonunital]] unless $X$ is already compact. Its [[unitalization]] is $C_0(X^{cpt})$.
\end{remark}
(cf. [Warner 2010 Ex 1.15](#Warner10))



## References

The algebra $C_0(X)$ is discussed in most monographs on [[C-star algebra|$C^\ast$-algebras]], for instance:

* {#Warner10} [[Garth Warner]] Ex. 1.15 in: *$C^\ast$-Algebras*, EPrint Collection, University of Washington (2010) &lbrack;[hdl:1773/16302](http://hdl.handle.net/1773/16302), [pdf](https://sites.math.washington.edu//~warner/C-star.pdf), [[Waner-CStarAlgebras.pdf:file]]&rbrack;

* {#Blackadar06} [[Bruce Blackadar]] Ex. II.1.1.3(ii) in: *Operator Algebras -- Theory of $C^\ast$-Algebras and von Neumann Algebras*, Encyclopaedia of Mathematical Sciences **122**, Springer (2006) &lbrack;[doi:10.1007/3-540-28517-2](https://doi.org/10.1007/3-540-28517-2)&rbrack;
  > (which however does not dwell on the definition of "vanishing at infinity")

* [[Ian Putnam]], Ex. 1.2.4 in: *Lecture notes on $C^\ast$-algebras* (2019) &lbrack;[pdf](https://www.math.uvic.ca/faculty/putnam/ln/C*-algebras.pdf), [[Putnam-CStarAlgebras.pdf:file]]&rbrack;


See also:

* Wikipedia: *[Vanish at infinity](https://en.wikipedia.org/wiki/Vanish_at_infinity)* 

* Wikipedia: _[Locally compact space](http://en.wikipedia.org/wiki/Locally_compact_space)_


[[!redirects vanishing at infinity]]
[[!redirects vanish at infinity]]
[[!redirects vanishes at infinity]]
