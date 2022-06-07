## Idea ##
There is a canonical way to turn any [[category]] into a [[weak equivalence|weakly equivalent]] [[univalent category]]. This can be thought of as an analogue of [[univalence]] but for [[isomorphisms]] instead of [[equivalence]].

## Construction ##
These results are from the HoTT book. Note: the HoTT book calls a [[category]] a "precategory" and a [[univalent category]] a "category", but here we shall refer to the standard terminology of "category" and "univalent category" respectively. 

### Theorem 9.9.5 ###
For any [[category]] $A$, there is a [[univalent category]] $\hat{A}$ and a [[weak equivalence]] $A\to \hat{A}$.

**Proof.**
Let $\hat{A}_0$ be the type of [[representable]] objects of $\mathit{Set}^{A^{\mathrm{op}}}$, with hom-sets inherited from $\mathit{Set}^{A^{\mathrm{op}}}$. Then the inclusion $\hat{A} \to \mathit{Set}^{A^{\mathrm{op}}}$ is [[fully faithful]] and an [[embedding]] on [[objects]]. Since $\mathit{Set}^{A^{\mathrm{op}}}$ is a category by Theorem 9.2.5 (see [[functor category]]), $\hat{A}$ is also a category. Let $A \to \hat{A}$ be the [[Yoneda embedding]]. This is [[fully faithful]] by corollary 9.5.6 (See [[Yoneda embedding]]), and [[essentially surjective]] by definition of $\hat{A}_0$. Thus it is a [[weak equivalence]]. $\square$ 

* $\hat{A}_0\equiv \sum_{(F : \mathit{Set}^{A^{\mathrm{op}}})} \sum_{(a:A)} \mathbf{y} a \cong F$

This has the unfortunate side affect of raising the [[universe]] level. If $A$ is a [[univalent category]] in a universe $\mathcal{U}$, then in this proof $\mathit{Set}$ must at least be as large as $\mathit{Set}_{\mathcal{U}}$. Hence the univalent category $\mathit{Set}_{\mathcal{U}}$ is in a higher universe than $\mathcal{U}$ hence $\mathit{Set}^{A^{\mathrm{op}}}$ must also be in a higher universe and finally $\hat{A}$ is also in a higher universe than $\mathcal{U}$.

Now this can all be avoided by constructing a [[higher inductive type]] $\hat{A}$ with constructors:

* A function $i : A_0 \to \hat{A}_0$.
* For each $a,b:A$ and $e: a \iso b$, an equality $j e : i a = i b$
* For each $a : A$, an equality $j(1_a)=refl_{i a}$.
* For each $a,b,c:A$, $f : a \cong b$, and $g : b \cong c$, an equality $j(g \circ f)=j(f) \cdot j(g).$
* 1-truncation: for all $x,y:\hat{A}_0$ and $p,q: x = y$ and $r,s : p = q$, an equality $r=s$.

If we ignore the last constructor we could also write the above as $\| \hat{A}_0 \|_1$.

We now go on to build a univalent category $\hat{A}$ with a [[weak equivalence]] $A \to \hat{A}$ by taking the type of objects as $\hat{A}_0$ and defining hom-sets by double [[induction]]. The advantage of this approach is that it preserves [[universe]] levels, there are a lot of things to check but it is an easy proof. The kind of proof that is well suited to a proof assistant. For the complete proof see Theorem 9.9.5 of the [[HoTT book]].

## See also ##
[[category theory]]
[[Yoneda lemma]]
[[weak equivalence]]
[[higher inductive type]]

## References ##
[[HoTT book]]

_Univalent categories and the Rezk completion_. [[Benedikt Ahrens]], [[Chris Kapulkin]], [[Michael Shulman]], Math. Structures Comput. Sci. 25 (2015), no. 5, 1010?1039. 

category: category theory