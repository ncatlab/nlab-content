
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



# Contents #
* table of contents 
{: toc}

## Idea 

The simplicial approximation theorem roughly says that if $X$ and $Y$ are [[simplicial complexes]] and $f: {|X|} \to {|Y|}$ is a [[continuous map]] between their [[geometric realizations]], then after further [[subdivisions]] $X'$, $Y'$ there is a simplicial map $g: X' \to Y'$ such that ${|g|}$ is [[homotopy|homotopic]] to $f$. 

## Statement 

Let $X$ be a simplicial complex, with vertex set $X_0$. We recall that the geometric realization of $X$ is a space whose points may be described as functions $\alpha: X_0 \to [0, 1]$ such that $\alpha^{-1}((0, 1])$ is a simplex of $X$ (in particular, finite) and $\sum_{v \in X_0} \alpha(v) = 1$. For a simplex $s$ of $X$, we let ${|s|}$ denote the _closed_ (affine) simplex in the geometric realization ${|X|}$, defined by the formula 

$${|s|} = \{\alpha \in {|X|}: \alpha(v) \gt 0 \; implies \; v \in s\}.$$ 

This may be identified with a standard affine simplex, and we topologize ${|s|}$ so that this identification is a homeomorphism. ${|X|}$ is then given the coherent topology: the largest topology rendering each inclusion ${|s|} \hookrightarrow {|X|}$ is continuous. 

If $X, Y$ are simplicial complexes, then a function $f: X_0 \to {|Y|}$ can be extended linearly to a continuous map $\tilde{f}: {|X|} \to {|Y|}$ by the rule 

$$\tilde{f}(\alpha) = \sum_{v \in X_0} \alpha(v)f(v),$$ 

provided that for every simplex $s$ of $X$, all convex combinations of elements of $f(s)$ lie in ${|Y|}$. Naturally this is the case if $f = j \circ \phi$ where $\phi: X_0 \to Y_0$ is a simplicial map and $j: Y_0 \to {|Y|}$ is the natural inclusion. 

We may then define a general _subdivision_ (not necessarily an iterated barycentric [[subdivision]]) of a simplicial complex $X$ to be a simplicial complex $X'$ such that 

* Vertices of $X'$ are points of ${|X|}$, 

* For every simplex $s'$ of $X'$, there is a simplex of $X$ such that $s' \subseteq {|s|}$, 

* The linear map $\tilde{i}: {|X'|} \to {|X|}$ induced from the inclusion $i: X' \hookrightarrow {|X|}$ is a homeomorphism. 

Often one treats such $\tilde{i}$ as an identity map. 

+-- {: .num_defn} 
###### Definition 
Let $X, Y$ be simplicial complexes, and let $f: {|X|} \to {|Y|}$ be a continuous map. A simplicial map $\phi: X \to Y$ is a **simplicial approximation** to $f$ if $f(\alpha) \in {|s|}$ implies ${|\phi|}(\alpha) \in {|s|}$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
Suppose $\phi: X \to Y$ is a simplicial approximation to a map $f: {|X|} \to {|Y|}$, and suppose $f = {|\phi|}$ on a subset $A \subseteq {|X|}$. Then there is a homotopy ${|\phi|} \simeq f \; rel \; A$. 
=-- 

+-- {: .proof} 
###### Proof 
Define the homotopy $H$ by $H(\alpha, t) = t f(\alpha) + (1-t){|\phi|}(\alpha)$. This makes sense since if $f(\alpha) \in {|s|}$, then ${|\phi|}(\alpha) \in {|s|}$ and ${|s|}$ is closed under convex combinations. Clearly $H(\alpha, t) = f(\alpha)$ for all $t$ on a set where $f$ and ${|\phi|}$ agree. 
=-- 

+-- {: .num_theorem} 
###### Theorem 

Given simplicial pairs $(X, A)$, $(Y, B)$ and a map of pairs $f: ({|X|}, {|A|}) \to ({|Y|}, {|B|})$, there is a subdivision $i: (X', A') \hookrightarrow ({|X|}, {|A|})$ and a simplicial approximation $\phi: (X', A') \to (Y, B)$ to $f \circ \tilde{i}: ({|X'|}, {|A'|}) \to ({|Y|}, {|B|})$. 

Moreover, if $(X, A)$ is a finite simplicial pair, we may choose the subdivision to be an iterated barycentric subdivision $(sd^n X, sd^n A)$ for any sufficiently large $n$ (given $f$). 

=-- 

## Related concepts

* [[cellular approximation theorem]]

## References 

* {#Switzer75} [[Robert Switzer]], Lemma 6.8, p. 76 in: _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975 ([doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6))
