
<div class="rightHandSide toc">
[[!include topology - contents]]
</div>

#Contents#
* automatic table of contents goes here
{:toc}

## Idea 

_Geometric_ realization denotes usually the special case of [[nerve and realization]] induced from the standard [[simplicial set|cosimplicial]] topological space that in degree $n$ is the standard topological $n$-simplex $\Delta^n_{Top}$.

In this case geometric realization is the operation that reads in a [[simplicial set]] $X$ and spits out the [[topological space]] that is obtained by interpreting each 
element in $X_n$ -- each abstract $n$-simplex in $X$ -- as one copy of $\Delta^n_{Top}$ and then guing together all these along their boundaries to a big topological space, using the information encoded in the face and degeneracy maps of $X$ on how these simplices are supposed to be stuck together.

See also [[nerve and realization]].

## Details 

Let $S$ be one of the categories of [[geometric shapes for higher structures]], such as the [[globe category]] or the [[simplex category]] or the [[cube category]].

There is an obvious functor

 $ st : S \to $ [[Top]]

which sends the standard _cellular_ shape $[n]$ (the standard cellular [[globe]], [[simplex]] or [[cube]], respectively) to the corresponding standard _topological_ shape (for instance  the standard $n$-simplex $ st([n]) := \{ (x_1, \cdots, x_n) | x_i \leq x_{i+1}  \} \subset \mathbb{R}^{n}$ ) with the obvious induced face and boundary maps.

Using this, in cases where $Top$ can be regarded as [[enriched category|enriched]] over and [[copower|tensored]] over a base category $V$, the **geometric realization** of a [[presheaf]] $K^\bullet : S^{op} \to V$ on $S$ -- e.g., of a [[globular set]], a [[simplicial set]] or a [[cubical set]], respectively  (when $V= Set$) -- is the [[topological space]] given by the [[end|coend]] or [[weighted limit|weighted colimit]]

$$
  |K^\bullet| = \int^{[n] \in S} st([n]) \cdot K^n
  \,.
$$

## Examples 

* For $G$ a [[group]], $\mathbf{B}G$ its one-object [[groupoid]] obtained by [[delooping]], $N(\mathbf{B}G)$ the corresponding simplicial [[nerve]] [[Kan complex]], we have that the geometric realization
  $$
    \mathcal{B}G = |N\mathbf{B}G|
  $$
  is the [[topological space]] that is the [[classifying space]] for $G$-[[principal bundle]]s ([[covering space]]s), as long as we give $G$ the [[discrete topology]].

## Properties ## 

### Realizations are CW complexes ### 

Each $|X|$ is a CW complex (proof to be inserted), and so geometric realization factors $|(-)|: Set^{\Delta^{op}} \to Top$ through the full subcategory of CW complexes, and therefore through the full subcategory $i: CGHaus \to Top$ of compactly generated Hausdorff spaces. 

+-- {: .un_prop} 
######Proposition
For any simplicial set $X$, there is a natural isomorphism $i(\int^{n: \Delta} X(n) \cdot \sigma(n)) \cong |X|$, where the coend on the left is computed in $CGHaus$. 
=-- 

This is obvious: more generally, if $F: J \to A$ is a diagram and $i: A \hookrightarrow B$ is a full replete subcategory, and if the colimit in $B$ of $i \circ F$ lands in $A$, then this is also the colimit of $F$ in $A$. 
(The dual statement also holds, with limits instead of colimits.) 

### Theorem: Geometric realization is left exact ### 

In this section we prove that geometric realization 

$$R: Set^{\Delta^{op}} \to CGHaus$$ 

is left exact. Here $CGHaus$ can be regarded as a placeholder for a [[nice category of spaces]]; the same basic methods apply to other cases as well. 

It is important that we use some such niceness assumption, because for example 

$$|(-)|: Set^{\Delta^{op}} \to Top,$$

valued in general topological spaces, does not preserve products. (To get a correct statement, one has to "kelley-fy" the products by applying the coreflection $k: Haus \to CGHaus$. In other words, we do have that $|X \times Y| \cong |X| \times_k |Y|$ where the product on the right is the kelleyfied product.) 

+-- {: .un_lem}
######Lemma 
If $i: X \to Y$ is a monomorphism of simplicial sets, then $R(i): R(X) \to R(Y)$ is a closed subspace inclusion. 
=-- 

+-- {: .un_thm} 
######Theorem 
Let $U: CGHaus \to Set$ be the underlying-set functor. Then the composite $U R: Set^{\Delta^{op}} \to Set$ is left exact. 
=-- 

+-- {: .proof}
######Proof
As described at the nLab article on triangulation [here](http://ncatlab.org/nlab/show/triangulation#standard_affine_simplex_functor_3), the composite 
$$\Delta \stackrel{\sigma}{\to} CGHaus \stackrel{U}{\to} Set$$ 
can be described as the functor 
$$\Delta \cong FinInt^{op} \hookrightarrow Int^{op} \stackrel{Int(-, I)}{\to} Set$$ 
where $Int$ is the category of intervals (linearly ordered sets with distinct top and bottom). Because every interval, in particular $I$, is a filtered colimit of finite intervals, it follows that $U \sigma: \Delta \to Set$ is a [[flat functor]] (a [[filtered colimit]] of representables). But on general grounds, taking the weighted colimit with a flat functor is a left exact functor, which in this case means
$$U R = - \otimes_\Delta U \sigma: Set^{\Delta^{op}} \to Set$$
is left exact. 
=-- 

Notice that the preceding proof is not sensitive to whether we use $CGHaus$ or $Top$. 

+-- {: .un_cor}
######Corollary
$R: Set^{\Delta^{op}} \to CGHaus$ preserves equalizers. 
=--

+-- {: .proof} 
######Proof
Equalizers in $CGHaus$ are computed as the equalizers on the level of underlying sets, equipped with the subspace topology (the subspace is closed since we are dealing with Hausdorff spaces, and a closed subspace of a compactly generated space is again compactly generated). So if 
$$E \stackrel{i}{\to} X \stackrel{\overset{f}{\to}}{\underset{g}{\to}} Y$$ 
is an equalizer diagram in $Set^{\Delta^{op}}$, then $R(i)$ is the equalizer of the pair $R(f)$, $R(g)$, because $U R(i)$ is the equalizer of $U R(f)$, $U R(g)$ on the underlying set level by the preceding theorem, and because $R(i)$ is a closed subspace inclusion by the lemma. 
=-- 

Again, the proof of this corollary is not sensitive to whether we use $CGHaus$ or $Top$, and so $|(-)|: Set^{\Delta^{op}} \to Top$ also preserves equalizers. 


+-- {: .un_thm} 
######Theorem 
The functor $R: Set^{\Delta^{op}} \to CGHaus$ preserves products. 
=-- 

+-- {: .proof} 
######Proof
First we prove that the canonical map 
$$|\Delta(-, m) \times \Delta(-, n)| \to |\Delta(-, m)| \times |\Delta(-, n)|$$ 
is a homeomorphism. Indeed, this is continuous, and a bijection at the underlying set level by the theorem above. Now products of compact Hausdorff spaces are reflected by the (monadic) underlying functor $U: CH \to Set$. In particular $|\Delta(-, m) \times \Delta(-, n)|$ is compact Hausdorff. Thus the canonical map above is a continuous bijection between compact Hausdorff spaces, hence a homeomorphism. 

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
where in each of the second and penultimate lines, we twice used the fact that $- \times -$ preserves colimits in its separate arguments (i.e., the fact that the nice category $CGHaus$ is cartesian closed), and the remaining lines used the fact that $R$ preserves colimits, and also products of representables by the first paragraph of this proof. 
=--
