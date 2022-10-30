"Yoneda reduction" is a term coined by [[Todd Trimble]] in his (unpublished) thesis. It refers to a technique based on the [[Yoneda lemma]] for performing a number of [[end|end and coend]] calculations which arise in [[coherence theory]] and [[enriched category theory]]. 

## The module perspective on the Yoneda lemma

There are various formulations of the Yoneda lemma. One says that given a [[presheaf]] $F: C^{op} \to Set$, there is a canonical isomorphism 

$$F(c) \cong Nat(\hom_C(-, c), F)$$ 

where "Nat" refers to the set of natural transformations between presheaves $C^{op} \to Set$; in other words, the hom 

$$Set^{C^{op}}(\hom_C(-, c), F)$$ 

appropriate to the presheaf category. 

There is an $V$-enriched category version, whenever $C$ is a category enriched in a [[complete category|complete]], [[cocomplete category|cocomplete]], [[symmetric monoidal closed category]] $V$. Here "Nat" is constructed as an enriched [[end]] (an example of a [[weighted limit]]): 

$$V^{C^{op}}(C(-, c), F) = \int_d F(d)^{C(d, c)}$$ 

and therefore the enriched Yoneda lemma gives an isomorphism 

$$F(c) \cong \int_d F(d)^{C(d, c)} \qquad (1)$$

which is ($V$-)natural in $c$; we may therefore write 

$$F(-) \cong \int_d F(d)^{C(d, -)} \qquad (2)$$ 

and this isomorphism is $V$-natural in $F$. 

We pause to give an instance of the Yoneda lemma which is both familiar and which serves to inform much of the module-theoretic terminology in the discussion below. Let $V = Ab$; let $R$ be a ring (conceived as an $Ab$-enriched category with exactly one object $\bullet$). Then $Ab^{R^{op}}$ is the ($Ab$-enriched) category of right $R$-modules, or equivalently, left $R^{op}$-modules). The presheaf $\hom_R(-, \bullet)$ is just the underlying abelian group of $R$ seen as a right module over the ring $R$, also known as the _regular representation_. 

The first formulation (1) of the Yoneda lemma would simply say that at the level of _abelian groups_, we have for any right $R$-module $M$

$$M(\bullet) \cong RightMod_R(R, M)$$ 

Further taking into account the "naturality" in the argument bullet, the formulation (2) says that actually we have an isomorphism at the level of _right $R$-modules_ 

$$M \cong RightMod_R(R, M)$$ 

where the module structure on the right side arises by considering the argument $R$ now as a _bimodule_ over the (ring) $R$. 

The (enriched) Yoneda lemma is nothing but a far-reaching extrapolation of this basic isomorphism: it says 

$$F \cong RightMod_C(\hom_C, F)$$ 

where the $C$-presheaf or right $C$-module hom on the right is appropriately constructed as an enriched end, and $\hom_C: C^{op} \otimes C \to V$ is a treated as a $V$-enriched "bimodule" over $C$, and plays the role of the "regular representation" of $C$. 

## Calculus of bimodules 

The analogy between presheaves and modules can be pursued considerably further. Again, we start with the perhaps more familiar context of rings and modules. 

In the first place, given a ring $R$, there is a familiar monoidal category of $R$-bimodules (and bimodule morphisms). If $M, N$ are bimodules over $R$, with left $R$-actions denoted by $\lambda$'s and the right actions by $\rho$'s, their tensor product $M \otimes_R N$, defined by the coequalizer 

$$M \otimes R \otimes N \stackrel{\to}{\to} M \otimes N \to M \otimes_R N$$

(where the two parallel arrows are $M \otimes \lambda$, $\rho \times N$) carries an evident $R$-bimodule structure. Each of the functors $M \otimes_R -$ and $- \otimes_R N$ admits a [[adjunction|right adjoint]] expressed by natural isomorphisms of abelian groups 

$$Bimod(N, Left_R(M, Q)) \cong Bimod(M \otimes_R N, Q) \cong Bimod(M, Right_R(N, Q))$$

where $Left_R(M, Q)$ denotes the abelian group of left $R$-module maps $M \to Q$, equipped with its natural $R$-bimodule structure; $Right(N, Q)$ is similar. Thus the monoidal category of $R$-bimodules is biclosed. 

More generally, there is a bicategory whose objects or 0-cells are rings $R, S, \ldots$, and whose morphisms or 1-cells $R \to S$ are left $R$-, right $S$-bimodules. 2-cells are homomorphisms of bimodules. If $M: R \to S$ and $N: S \to T$ are bimodules, then their bimodule composite is $M \otimes_S N: R \to T$. This too is a biclosed bicategory, meaning that 

This generalized module theory can be pursued much further. 

(Lost a bunch of work, due to vagaries of computers. Sigh. Will return later.) 