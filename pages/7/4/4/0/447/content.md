
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

_Geometric realization_ is the operation that builds from a [[simplicial set]] $X$ a [[topological space]] $|X|$ obtained by interpreting each 
element in $X_n$ -- each abstract $n$-simplex in $X$ -- as one copy of the standard topological $n$-simplex $\Delta^n_{Top}$ and then guing together all these along their boundaries to a big topological space, using the information encoded in the face and degeneracy maps of $X$ on how these simplices are supposed to be stuck together.

This is the special case of the general notion of [[nerve and realization]] that is induced from the standard [[simplicial set|cosimplicial]] [[topological space]] $[n] \mapsto \Delta^n_{Top}$.

In the context of [[homotopy theory]] geometric realization plays a notable role in the [[homotopy hypothesis]], where it is part of the [[Quillen equivalence]] between the [[model structure on topological spaces]] and the standard [[model structure on simplicial sets]].

The construction generalizes naturally to a map from [[simplicial object|simplicial]] [[topological space]]s to plain topological spaces. For more on that see [[geometric realization of simplicial spaces]].

## Definition

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] or the [[simplex category]] or the [[cube category]].

There is an obvious functor

 $ st : S \to $ [[Top]]

which sends the standard _cellular_ shape $[n]$ (the standard cellular [[globe]], [[simplex]] or [[cube]], respectively) to the corresponding standard _topological_ shape (for instance  the standard $n$-simplex $ st([n]) := \{ (x_1, \cdots, x_n) | x_i \leq x_{i+1}  \} \subset \mathbb{R}^{n}$ ) with the obvious induced face and boundary maps.

Using this, in cases where $Top$ can be regarded as [[enriched category|enriched]] over and [[copower|tensored]] over a base category $V$, the **geometric realization** of a [[presheaf]] $K^\bullet : S^{op} \to V$ on $S$ -- e.g., of a [[globular set]], a [[simplicial set]] or a [[cubical set]], respectively  (when $V= Set$) -- is the [[topological space]] given by the [[end|coend]] or [[weighted limit|weighted colimit]]

$$
  |K^\bullet| = \int^{[n] \in S} st([n]) \cdot K^n
  \,.
$$


## Properties ## 

### Realizations are CW complexes ### 

Each $|X|$ is a CW complex (proof to be inserted), and so geometric realization $|(-)|: Set^{\Delta^{op}} \to Top$ takes values in the full subcategory of CW complexes, and therefore in any [[convenient category of topological spaces]], for example in the category $CGHaus$ of compactly generated Hausdorff spaces. Let $Space$ be any convenient category of topological spaces. 

+-- {: .un_prop} 
######Proposition
For any simplicial set $X$, there is a natural isomorphism $i(\int^{n: \Delta} X(n) \cdot \sigma(n)) \cong |X|$, where the coend on the left is computed in $Space$. 
=-- 

This is obvious: more generally, if $F: J \to A$ is a diagram and $i: A \hookrightarrow B$ is a full replete subcategory, and if the colimit in $B$ of $i \circ F$ lands in $A$, then this is also the colimit of $F$ in $A$. 
(The dual statement also holds, with limits instead of colimits.) 

Below, we let $R: Set^{\Delta^{op}} \to Space$ denote the geometric realization that lands in $Space$. 

### Theorem: Geometric realization is left exact ### 

We continue to assume $Space$ is any [[convenient category of topological spaces]]. In this section we prove that geometric realization 

$$R: Set^{\Delta^{op}} \to Space$$ 

is a left [[exact functor]] in that it preserves finite [[limit]]s. 

It is important that we use some such niceness assumption, because for example 

$$|(-)|: Set^{\Delta^{op}} \to Top,$$

valued in general [[topological spaces]], does not preserve products. (To get a correct statement, one usual procedure is to "kelley-fy" products by applying the coreflection $k: Haus \to CGHaus$. This gives the correct isomorphism in the case $Space = CGHaus$, where we have that $|X \times Y| \cong |X| \times_k |Y| \coloneqq k(|X| \times |Y|)$; the product on the right has been "kelleyfied" to the product appropriate for $CGHaus$.) 

+-- {: .un_lem}
######Lemma 
If $i: X \to Y$ is a monomorphism of simplicial sets, then $R(i): R(X) \to R(Y)$ is a closed subspace inclusion. 
=-- 

+-- {: .un_thm} 
######Theorem 
Let $U = \hom(1, -): Space \to Set$ be the underlying-set functor. Then the composite $U R: Set^{\Delta^{op}} \to Set$ is left exact. 
=-- 

+-- {: .proof}
######Proof
As described at the nLab article on triangulation [here](http://ncatlab.org/nlab/show/triangulation#standard_affine_simplex_functor_3), the composite 
$$\Delta \stackrel{\sigma}{\to} Space \stackrel{U}{\to} Set$$ 
can be described as the functor 
$$\Delta \cong FinInt^{op} \hookrightarrow Int^{op} \stackrel{Int(-, I)}{\to} Set$$ 
where $Int$ is the category of intervals (linearly ordered sets with distinct top and bottom). Because every interval, in particular $I$, is a filtered colimit of finite intervals, it follows that $U \sigma: \Delta \to Set$ is a [[flat functor]] (a [[filtered colimit]] of representables). But on general grounds, tensoring with a flat functor is left exact, which in this case means
$$U R = - \otimes_\Delta U \sigma: Set^{\Delta^{op}} \to Set$$
is left exact. 
=-- 

Obviously the preceding proof is not sensitive to whether we use $Space$ or $Top$. 

+-- {: .un_cor}
######Corollary
$R: Set^{\Delta^{op}} \to Space$ preserves equalizers. 
=--

+-- {: .proof} 
######Proof
The equalizer of a pair of maps in $Top$ is computed as the equalizer on the level of underlying sets, equipped with the subspace topology. So if 
$$E \stackrel{i}{\to} X \stackrel{\overset{f}{\to}}{\underset{g}{\to}} Y$$ 
is an equalizer diagram in $Set^{\Delta^{op}}$, then $|i|$ is the equalizer of the pair $|f|$, $|g|$, because the underlying function $U(|i|)$ is the equalizer of $U(|f|)$, $U(|g|)$ on the underlying set level by the preceding theorem, and because $|i|$ is a (closed) subspace inclusion by the lemma. But this $Top$-equalizer $|i|: |E| \to |X|$ lives in the full subcategory $Space$, and therefore $R(i) = |i|$ is the equalizer of the pair $R(f) = |f|$, $R(g) = |g|$. 
=-- 

As the proof indicates, that realization preserves equalizers is not at all sensitive to whether we use $Top$ or a convenient category of spaces $Space$. However, the following result _is_ sensitive to such issues, and in fact uses cartesian closure of $Space$ in an essential way. 

First, a small technical result about simplicial sets. 

+-- {: .un_lem}
######Lemma 
The product of two representables $\Delta(-, m) \times \Delta(-, n)$ is the colimit of a finite diagram of representables, i.e., is the quotient of a finite coproduct of representables. 
=--

+-- {: .un_thm} 
######Theorem 
The functor $R: Set^{\Delta^{op}} \to Space$ preserves products. 
=-- 

+-- {: .proof} 
######Proof
First we prove that the canonical map 
$$|\Delta(-, m) \times \Delta(-, n)| \to |\Delta(-, m)| \times |\Delta(-, n)|$$ 
is a homeomorphism. Indeed, this is continuous, and a bijection at the underlying set level by the theorem above. The codomain is the compact Hausdorff space $\sigma(m) \times \sigma(n)$, and the domain is also compact Hausdorff: by the lemma, and using the fact that realization preserves finite colimits, the left side is the topological quotient of a coproduct of finitely many simplices, hence compact. But a continuous bijection between compact Hausdorff spaces is a homeomorphism. 

More generally, suppose $X$ and $Y$ are simplicial sets. By the [[co-Yoneda lemma]], we have isomorphisms 
$$X \cong \int^m X(m) \cdot \Delta(-, m)  \qquad Y \cong \int^n Y(n) \cdot \Delta(-, n)$$ 
and so we calculate 
$$\array{
R(X \times Y) & \cong & R((\int^m X(m) \cdot \Delta(-, n)) \times (\int^n Y(n) \cdot \Delta(-, n))) \\
 & \cong & R(\int^m \int^n X(m) \cdot Y(n) \cdot (\Delta(-, m) \times \Delta(-, n))) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot R(\Delta(-, m) \times \Delta(-, n)) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot (R(\Delta(-, m)) \times R(\Delta(-, n)) \\
 & \cong & \int^m \int^n X(m) \cdot Y(n) \cdot (\sigma(m) \times \sigma(n)) \\
 & \cong & (\int^m X(m) \cdot \sigma(m)) \times (\int^n Y(n) \cdot \sigma(n)) \\
 & \cong & R(X) \times R(Y)
}$$ 
where in each of the second and penultimate lines, we twice used the fact that $- \times -$ preserves colimits in its separate arguments (i.e., the fact that the nice category $Space$ is cartesian closed), and the remaining lines used the fact that $R$ preserves colimits, and also products of representables by the first paragraph of this proof. 
=--


## Examples 

* For $G$ a [[group]], $\mathbf{B}G$ its one-object [[groupoid]] obtained by [[delooping]], $N(\mathbf{B}G)$ the corresponding simplicial [[nerve]] [[Kan complex]], we have that the geometric realization
  $$
    \mathcal{B}G = |N\mathbf{B}G|
  $$
  is the [[topological space]] that is the [[classifying space]] for $G$-[[principal bundle]]s ([[covering space]]s), as long as we give $G$ the [[discrete topology]].


[[!redirects geometric realisation]]