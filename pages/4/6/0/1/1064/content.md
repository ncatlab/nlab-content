
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Homological algebra
+-- {: .hide}
[[!include homological algebra - contents]]
=--
#### Additive and abelian categories
+-- {: .hide}
[[!include additive and abelian categories - contents]]
=--
=--
=--

* table of contents
{: toc}

## Definitions

There is a sequence of extra [[stuff, structure, property|structure and property]] on a [[category]] that makes this category behave like a general context for [[homological algebra]]. In order of increasing structure and property this is:

1. **[[Ab-enriched category]]**:
  a [[category]] that is [[Ab]]-[[enriched category|enriched]];

2. **[[pre-additive category]]**:
  an $Ab$-enriched category that has a [[terminal object]] or [[initial object]] and therefore a [[zero object]]; Notice however that many authors (e.g. Weibel, Popescu) by preadditive (or pre-additive) simply mean $Ab$-enriched. 

   * [[pseudo-abelian category]]: a pre-additive category such that every [[idempotent]] has a [[kernel]] and [[cokernel]]

3. **[[additive category]]**: a pre-additive category that admits binary [[product]]s or binary [[coproduct]]s and therefore binary [[biproduct]]s (equivalently, an $Ab$-enriched category with all finite products or coproducts);

4. **[[pre-abelian category]]**:
  an additive category that admits [[kernel]]s and  [[cokernel]]s (equivalently, an $Ab$-enriched category with all finite [[limit]]s and [[colimit]]s);

5. **[[abelian category]]**:
  a pre-abelian category such that every [[monomorphism]] is a kernel and every [[epimorphism]] is a cokernel (and many other equivalent definitions).

Pre-abelian and abelian categories are sometimes called (AB1) and (AB2) categories, after the sequence of additional axioms on top of additive categories introduced by Grothendieck in [[Tohoku]].  AB1 and AB2 are self-dual axioms (AB1 is existence of kernels and cokernels, and AB2 requires that, for any $f$, the canonical morphism $\mathrm{Coim}\,f\to \mathrm{Im}\,f$ is an isomorphism). These continue in non-selfdual manner:

* AB3: an abelian category with all coproducts (hence with all [[colimit]]s);

* AB4: an (AB3) category in which coproducts of monomorphisms are monic;

* AB5: an (AB3) category in which [[filtered colimits]] of [[exact sequence]]s exist and are exact;

* AB6: an (AB3) category such that
  * For any object $A$ in the category and any family $(B^j)_{j\in J}$ of increasing directed families of $B^i=(B_i^j)_{i\in I_j}$ of [[subobject]]s $B^j$ of $A$, we have $\bigcap_{j\in J}\left(\sum_{i\in I_j}B_j^i\right)=\sum_{(i_j)\in \prod I_j}\left(\bigcap_{j\in J}B_{i_j}^i\right)$. 
  * Notice that this implies that inf for any family of subobjects exists.

We have a chain of implications AB6$\Rightarrow$AB5$\Rightarrow$AB4, see ([Nicolae Popescu 1973, Sect. 2.8, Corollaries 8.9, 8.13](#Popescu73)).

The concepts (AB3--AB6) also have dual forms (AB3\*--AB6\*).

There are further refinements along these lines. In particular

* [[Grothendieck category]]: an (AB5) category with a [[generator]].

\begin{theorem}
**([Nicolae Popescu 1973, Sect. 2.8, Theorem 8.6](#Popescu73)).**
Let $\mathcal{C}$ be an AB3-category. The following assertions are equivalent:

   1. $\mathcal{C}$ is AB5.

   2. For any direct set $\left\{X_i\right\}_i$ of subobjects of any object $X$, the unique morphism $j: \varinjlim X_i \rightarrow X$ defined such that $j u_i=j_i$, (where $u_i: X_i \rightarrow \varinjlim X_i$ are structural morphisms and $j_i: X_i \rightarrow X$ are canonical inclusions) is an iso-

   3. Let $X$ be any object, $\left\{X_i\right\}_i$ a direct set of subobjects, and $X^{\prime}$ a subobject of $X$. Then:
$$
\sum_i\left(X_i \cap X^{\prime}\right)=\left(\sum_i X_i\right) \cap X^{\prime}
$$

   4. Let $f: Y \rightarrow X$ be a morphism and $\left\{X_i\right\}_i$ a direct set of subobjects of $X$. Then:
$$
f^{-1}\left(\sum_i X_i\right)=\sum_i f^{-1}\left(X_i\right)
$$

   5. Let $\left\{X_i\right\}_{i \in I}$ be a set of objects. For any finite subset $F$ of $I$, we denote by $X_F$ image of canonical morphism $u_F: \coprod_{i^{\prime} \in F} X_{i^{\prime}} \rightarrow \coprod_i X_i$, defined such that $u_F u_{i^{\prime}}{ }^{\prime}=u_{i^{\prime}}$, where $u_{i^{\prime}}{ }^{\prime}$ and $u_{i^{\prime}}$ are respectively structural morphisms. Then for any subobject $X$ of $\coprod_i X_i$ we have:
$$
X=\sum_{F \in T}\left(X \cap X_F\right)
$$
$T$ being the set of all finite subsets of $I$.
\end{theorem}


## Further refinements

Various further axiom structures are considered for additive (sometimes abelian) categories.

* [[suspended category]]

* [[triangulated category]]

* [[Quillen exact category]]

* [[Grothendieck category]]:  an AB5-category with a [[generator]]

* Gabriel's [[property sup]]


## Generalizations 

* Abelian groups are to general [[group]]s as [[abelian category|abelian categories]] are to [[semi-abelian category|semi-abelian categories]].


## Examples

Various generic classes of examples of additive and abelian categories are of relevance:


## Related concepts

* [[delta-functor]]
* [[category of chain complexes]]
* [[derived category]]
* [[stable (infinity,1)-category]]

## References

* {#Popescu73} [[Nicolae Popescu]], _[[Abelian categories with applications to rings and modules]]_, London Mathematical Society Monographs 3*, Academic Press (1973)


[[!redirects additive or abelian categories]]
[[!redirects additive or abelian category]]

[[!redirects AB5-category]]
[[!redirects AB5-categories]]

