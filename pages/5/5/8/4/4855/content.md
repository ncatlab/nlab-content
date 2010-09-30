[[!redirects fundamental (∞,1)-category]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--

* [[fundamental groupoid]], [[fundamental ∞-groupoid]]

* [[fundamental category]], **fundamental $(\infty,1)$-category**

***

#Contents#
* table of contents
{:toc}

## Idea

In analogy to how a [[topological space]] has a [[fundamental ∞-groupoid]], a [[directed space]] has a fundamental [[(∞,1)-category]]

## Definition


+-- {: .un_defn}
###### Definition

By a **[[directed space|directed topological space]]** we here mean specifically a pair $(X,D)$ consisting of 

* a [[topological space]] $X$;

* a subset $D \subset X^{[0,1]}$ of [[continuous map]]s $\gamma : [0,1] \to X$ that are are labeled as being _directed_ , 

* such that 

  * for every orientation preserving [[homeomorphism]] $\phi : [0,1] \to [0,1]$ and every directed map $\gamma$ also $\gamma \circ \phi$ is directed;

  *  for any two directed paths $\gamma_1, \gamma_2$ with $\gamma_1(1) = \gamma_2(0)$ also the concatenation

     $$
       [0,1] \stackrel{\times 2}{\to} [0,2]
       \simeq [0,1] \coprod_{*} [0,1]
       \stackrel{(\gamma_1, \gamma_2)}{\to} 
       X
     $$ 
 
     is a directed path.

A morphism $(X_1,D_1) \to (X_2, D_2)$ of directed space is a continuous map $X_1 \to X_2$ that takes elements in $D_1$ to elements in $D_2$.

This defines the [[category]] $DTop$ of directed topological spaces.

=--

+-- {: .un_example}
###### Example

For $X$ a topological space equipped with the structure of a [[poset]] on its underlying set, say that $\gamma : [0,1] \to X$ is directed if for all $x \leq y$ in $[0,1]$ we have $\gamma(0) \leq \gamma(1)$ in $X$. 

=--

+-- {: .un_example}
###### Example

For $\Delta^k_{Top}$ the standard topological $k$-[[simplex]] its _standard directed paths_ are the maps $[0,1] \to \Delta^k$ into the [[spine]] that preserve the natural order on the spine. 

=--

+-- {: .un_def}
###### Definition

The **fundamental $(\infty,1)$-category** of a directed topological space $(X,D)$ is given by the [[quasi-category]] $\Pi(X,D)$ whose [[k-morphism]]s are those continuous maps

$$
  \sigma : \Delta^k_{Top} \to X
$$

that are morphisms of directed spaces with respect to the standard spine-paths in $\Delta^k$, as in the above example: maps such that the [[spine]] of $\Delta^k$ is mapped under $\sigma$ to a directed path in $X$.

$$
  \Pi(X,D)_k := Hom_{DTop}(\Delta^k_{Top}, (X,D))
 \,.
$$

=--

+-- {: .un_lemma}
###### Lemma

This does indeed define a quasi-category

=--

+-- {: .proof}
###### Proof

Use the standard [[retract]]s $\Delta^k_{Top} \to \Lambda^k_i$ of the topological [[horn]] inclusions $\Lambda^k_i \hookrightarrow \Delta^k$ to fill horns in $\Pi(X,D)$.

For $k \geq 3$ these retracts are the identity on 1-faces, hence trivially preserve the directed paths. For $k = 2$ it is precisely the retract of the _inner_ horn $\Lambda^2_1$ that preserves the directed paths. This is sufficient to satisfy the inner horn filler condition of quasi-categories.


=--

## Properties

+-- {: .un_lemma}
###### Observation


If $X$ is undirected in that _all_ paths are labeled as directed -- $D = X^{[0,1]}$ -- then $\Pi(X,D)$ coincides with the [[fundamental ∞-groupoid]] $\Pi(X)$ of $X$.

=--
## References ##
Related constructions can be found in the following:
* Marco Grandis, _Directed homotopy theory, I. The fundamental category_ ([arXiv](http://arxiv.org/abs/math.AT/0111048))
* Tim Porter: _Enriched categories and models for spaces of evolving states_, Theoretical Computer Science, 405, (2008), pp. 88--100.
* Tim Porter, _Enriched categories and models for spaces of
dipaths. A discussion document and overview of some techniques_ ([pdf](http://drops.dagstuhl.de/opus/volltexte/2007/898/pdf/06341.PorterTimothy.Paper.898.pdf))