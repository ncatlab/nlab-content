
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **orthogonal subcategory problem** for a [[class]] of [[morphism]]s $\Sigma$ in a [[category]] $C$ asks whether the [[full subcategory]] $\Sigma^\perp$ of [[object]]s [[orthogonal]] to $\Sigma$ is a [[reflective subcategory]]. 

Here, an object $X$ is said to be orthogonal to a map $f:A\to B$ if every morphism $A\to X$ factors uniquely through $f$. For example, in a category of presheaves, $X:C^{op}\to Set$ is orthogonal to the canonical map $colim_i C(-,a_i)\to C(-,\colim_i a_i)$ if it preserves the limit $\lim_i a_i$ in $C^{op}$. 

This problem is related to the problem of [[localization]]. Suppose $\Sigma^\perp$ is indeed a [[reflective subcategory]]; let $r: C \to \Sigma^\perp$ be the reflector (the [[left adjoint]] to the inclusion $i: \Sigma^\perp \to C$). 


## Properties

+-- {: .un_lemma}
###### Lemma

If $f: a \to b$ belongs to $\Sigma$, then $r(f): r(a) \to r(b)$ is an [[isomorphism]] in $\Sigma^\perp$. 

=--

+-- {: .proof}
###### Proof

By definition of [[orthogonality]], for every object $X$ in $\Sigma^\perp$, $f$ induces an isomorphism of [[hom-set]]s 

$$\hom_C(f, i(X)): \hom_C(B, i(X)) \stackrel{\sim}{\to} \hom_C(A, i(X))$$ 

Since $r \dashv i$, this means that for all $X$ in $\Sigma^\perp$ the map 

$$\hom_{\Sigma^\perp}(r(f), X): \hom_{\Sigma^\perp}(r(B), X) \to \hom_{\Sigma^\perp}(r(A), X)$$ 

is an [[isomorphism]], so that $\hom_{\Sigma^\perp}(r(f), -)$ is a [[natural isomorphism]] between [[representable functor|representables]]. By the [[Yoneda lemma]], this means $r(f)$ is an isomorphism. 

=--


This lemma can be sharpened. First, given a category $C$, there is a [[Galois connection]] between classes of morphisms $\Sigma$ and classes of objects $K$, induced by the predicate that $\hom_C(\sigma, k)$ is a bijection for all $\sigma \in \Sigma$ and all $k \in K$. The induced monad on the collection of morphism classes $\Sigma$ (partially ordered by inclusion) may be called "saturation", denoted $sat(\Sigma)$. An easy argument due to Gabriel-Zisman is that if $C$ is finitely [[cocomplete category|cocomplete]], then $(C, sat(\Sigma))$ satisfies the axioms for a [[calculus of fractions]], so that the [[localization]] $C[(sat(\Sigma))^{-1}]$ can be constructed. An easy argument then establishes the following sharpened lemma: 

+-- {: .un_lemma}
###### Lemma


If $\Sigma^\perp \hookrightarrow C$ is [[reflective subcategory|reflective]], then the reflection $r: C \to \Sigma^\perp$ exhibits a canonical [[equivalence of categories|equivalence]] 
$$C[(sat(\Sigma))^{-1}] \simeq \Sigma^\perp$$ 

=--


+-- {: .un_lemma}
###### Lemma


If $\Sigma^\perp \hookrightarrow C$ is [[reflective subcategory|reflective]], then the reflection $r: C \to \Sigma^\perp$ exhibits a canonical [[equivalence of categories|equivalence]] 
$$C[(sat(\Sigma))^{-1}] \simeq \Sigma^\perp$$ 

=--

+--{.query} 

To be connected with things like [[small object argument]], [[Bousfield localization]], and others... 

=--

## Theorem in the setting of locally presentable categories

+-- {: .num_theorem}
###### Theorem

If $\Sigma$ is a set of morphisms in a [[locally presentable]] category $\mathcal{A}$ then the orthogonality subcategory $\Sigma^\top$ is reflective in $\mathcal{A}$. 

=--


## References ## 

* [[Gabriel-Zisman]]

* [[Peter Freyd]], [[Max Kelly]], _Categories of continuous functors I_, Jour. Pure Appl. Alg. 2 (1972), 169-191. ([web](http://www.sciencedirect.com/science/article/pii/0022404972900011)) 


* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994). But see the [errata](https://www.tu-braunschweig.de/Medien-DB/iti/cor.pdf).
 