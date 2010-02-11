The orthogonal subcategory problem for a class of morphisms $\Sigma$ in a category $C$ asks whether the full subcategory $\Sigma^\perp$ of objects [[orthogonal object|orthogonal]] to $\Sigma$ is a [[reflective subcategory]]. 

This problem is related to the problem of localization. Suppose $\Sigma^\perp$ is indeed a reflective subcategory; let $r: C \to \Sigma^\perp$ be the reflector (the left adjoint to the inclusion $i: \Sigma^\perp \to C$). 

Lemma: If $f: a \to b$ belongs to $\Sigma$, then $r(f): r(a) \to r(b)$ is an isomorphism in $\Sigma^\perp$. 

Proof: By definition of orthogonality, for every object $X$ in $\Sigma^\perp$, $f$ induces an isomorphism of hom-sets 

$$\hom_C(f, i(X)): \hom_C(B, i(X)) \stackrel{\sim}{\to} \hom_C(A, i(X))$$ 

Since $r \dashv i$, this means that for all $X$ in $\Sigma^\perp$ the map 

$$\hom_{\Sigma^\perp}(r(f), X): \hom_{\Sigma^\perp}(r(B), X) \to \hom_{\Sigma^\perp}(r(A), X)$$ 

is an isomorphism, so that $\hom_{\Sigma^\perp}(r(f), -)$ is a natural isomorphism between representables. By the [[Yoneda lemma]], this means $r(f)$ is an isomorphism. 

This lemma can be sharpened. First, given a category $C$, there is a [[Galois connection]] between classes of morphisms $\Sigma$ and classes of objects $K$, induced by the predicate that $\hom_C(\sigma, k)$ is a bijection for all $\sigma \in \Sigma$ and all $k \in K$. The induced monad on the collection of morphism classes $\Sigma$ (partially ordered by inclusion) may be called "saturation", denoted $sat(\Sigma)$. An easy argument due to Gabriel-Zisman is that if $C$ is finitely cocomplete, then $(C, sat(\Sigma))$ satisfies the axioms for a calculus of fractions, so that the localization $C[(sat(\Sigma))^{-1}]$ can be constructed. An easy argument then establishes the following sharpened lemma: 

* If $\Sigma^\perp \hookrightarrow C$ is reflective, then the reflection $r: C \to \Sigma^\perp$ exhibits a canonical equivalence 
$$C[(sat(\Sigma))^{-1}] \simeq \Sigma^\perp$$ 

+--{.query} 

To be connected with things like [[small object argument]], [[Bousfield localization]], and others... 

=--

## References ## 

Gabriel-Zisman

Peter Freyd and Max Kelly, Categories of continuous functors I, Jour. Pure Appl. Alg. 2 (1972), 169-191. 