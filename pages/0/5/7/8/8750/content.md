
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Categories of categories
+--{: .hide}
[[!include categories of categories - contents]]
=--
#### Enriched category theory
+-- {: .hide}
[[!include enriched category theory contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea

For $\mathcal{V}$ a [[closed monoidal category|closed]] and [[complete category|complete]] [[cosmos for enrichment]] there is a [[2-category|$2$-category]] $\mathcal{V} Cat$ whose

* [[objects]] are $V$-[[enriched categories]];

* [[morphisms]] are $V$-[[enriched functors]]; and

* [[2-morphism|$2$-morphisms]] are $V$-[[enriched natural transformations]].

Sometimes one also considers $\mathcal{V} Cat$ as a mere [[category]] by dropping the $2$-morphisms (and using enriched [[strict categories]]).


## Possible Contexts

* $\mathcal{V}$ can be a [[monoidal category]] with underlying category $\mathcal{V}_0$

* $\mathcal{V}$ can be a [[closed category]] with underlying category $\mathcal{V}_0$

* $\mathcal{V}$ can be a [[multicategory]] with underlying category $\mathcal{V}_0$

* $\mathcal{V}$ can be a [[cosmos]] with underlying category $\mathcal{V}_0$


## Examples

* For $\mathcal{V} = ($[[Set]]$, \times)$, $\mathcal{V}Cat \simeq$ [[Cat]], the $2$-category of [[locally small categories]].

* For $\mathcal{V} = ($[[Cat]]$, \times)$, $\mathcal{V}Cat \simeq$ [[2Cat|Str2Cat]], the $2$-category of [[strict 2-categories]].


## Extra structure

### Monoidal structure
 {#MonoidalStructure}

If $\mathcal{V}$ is [[symmetric monoidal category|symmetric monoidal]] then $\mathcal{V}Cat$ becomes itself a ([[very large category|very large]]) [[monoidal category]] with [[tensor product]] given by forming [[enriched product categories]].

If $\mathcal{V}$ is in addition [[closed monoidal category|closed]] and [[complete category|complete]], then $\mathcal{V}Cat$ becomes itself a [[closed monoidal category]] with [[internal hom]] given by forming [[enriched functor categories]].

&lbrack;[Kelly (1982), §2.3](#Kelly82)&rbrack;


### Involutions
 {#Involutions}

* If $\mathcal{V}$ is a category $\mathcal{V}_0$ equipped with a [[monoidal category|monoidal]] structure, then $\mathcal{V}$Cat has a [[unit enriched category|unit object]] $\mathcal{I}$, and a designated lax natural transformation $[\mathcal{I},-]^{op}\stackrel{{}^-_0L}{\Rightarrow}[[\mathcal{I},-],\mathcal{V}_0]\colon\mathcal{V}$Cat$\to$Cat, where the former is a $2$-functor flipping $2$-morphisms, and the latter is a $2$-functor flipping $1$-morphisms (c.f. [[contravariant functor]]). For the sake of simplicity, we note that $[\mathcal{I},-]$ is simply the forgetful $2$-functor from $\mathcal{V}$Cat to Cat, and hence abbreviate it as $(-)_0$. Then the above lax natural transformation is given by the following data:

1. For every object (i.e. $\mathcal{V}$-enriched category) $\mathcal{A}$ of $\mathcal{V}$Cat, we have to give a functor $\mathcal{A}_0^{op}\stackrel{{}^{\mathcal{A}}_0L}{\rightarrow}[\mathcal{A}_0,\mathcal{V}_0]$. By the cartesian closed structure of the $1$-category Cat, we define these to be the hom-functors $\mathcal{A}_0^{op}\times\mathcal{A}\stackrel{\mathcal{A}(-,-)}{\rightarrow}\mathcal{V}_0$ which are defined in terms of the monoidal structure $\mathcal{V}$ and the $\mathcal{V}$-enrichment data of $\mathcal{A}$ by setting $\mathcal{A}(B,C)\stackrel{\mathcal{A}(f,g)}{\rightarrow}\mathcal{A}(A,D)$ to be the composites $\mathcal{A}(B,C)\stackrel{l^{-1}r^{-1}}{\to}I\otimes\mathcal{A}(B,C)\otimes I\stackrel{f\otimes id\otimes g}{\to}\mathcal{A}(C,D)\otimes\mathcal{A}(B,C)\otimes\mathcal{A}(A,B)\stackrel{(\circ^{\mathcal{A}})^2}{\to}\mathcal{A}(A,D)$ in $\mathcal{V}_0$.

2. For every $1$-morphism (i.e. $\mathcal{V}$-enriched functor}) $\mathcal{A}\stackrel{F}{\rightarrow}\mathcal{B}$, we have to give a natural transformation ${}^F_0L$:
$$
\array{
\mathcal{A}_0^{op}&\stackrel{F_0^{op}}{\rightarrow}&\mathcal{B}_0^{op}\\
{}_0^{\mathcal{A}}L\downarrow&\stackrel{{}^F_0L}{\Rightarrow}&\downarrow{}^{\mathcal{B}}L\\
[\mathcal{A}_0,\mathcal{V}_0]&\stackrel{[F_0,\mathcal{V}_0]}{\leftarrow}&[\mathcal{B}_0,\mathcal{V}_0]
}$$
Since we have defined ${}_0^{\mathcal{A}}L$ to be the hom-functor $\mathcal{A}(-,-)$, to give a natural transformation ${}^F_0L$ is to give a natural transformation $\mathcal{A}(-,-)\Rightarrow\mathcal{B}(F_0^{op}-,F_0-)\colon\mathcal{A}_0^{op}\times\mathcal{A}\to\mathcal{V}_0$. We thus define the $ob(\mathcal{A}_0)$-indexed family of morphisms $\mathcal{A}(A,B)\stackrel{{}_0^FL_{A,B}}{\rightarrow}\mathcal{B}(F_0A,F_0B)$ in $\mathcal{V}_0$ to be simply the family of morphisms $\mathcal{A}(A,B)\stackrel{F_{A,B}}{\rightarrow}\mathcal{B}(F_0A,F_0B)$ in $\mathcal{V}_0$ defining the $\mathcal{V}$-enriched functor $\mathcal{A}\stackrel{F}{\rightarrow}\mathcal{B}$.

3. The lax naturality of ${}^-_0L$ says that for every $2$-morphism (i.e. a $\mathcal{V}$-enriched natural transformation) $F\stackrel{\alpha}{\Rightarrow} G\colon\mathcal{A}\to\mathcal{B}$ in $\mathcal{V}$Cat, the natural transformations ${}_0^{\mathcal{A}}L\stackrel{{}^F_0L}{\Rightarrow}[F_0,\mathcal{V}_0]\circ{}_0^{\mathcal{B}}L\circ F_0^{op}$ and ${}_0^{\mathcal{A}}L\stackrel{{}^G_0L}{\Rightarrow}[G_0,\mathcal{V}_0]\circ{}_0^{\mathcal{B}}L\circ G_0$ have to satisfy a compatibility condition with the natural transformations $G_0^{op}\stackrel{\alpha_0^{op}}{\Rightarrow}F_0^{op}$ and $[F_0,\mathcal{V}_0]\stackrel{[\alpha_0,\mathcal{V}_0]}{\Rightarrow}[G_0,\mathcal{V}_0]$. Explicitly, the condition is that the composite natural transformation ${}_0^{\mathcal{A}}L\stackrel{{}^F_0L}{\Rightarrow}[F_0,\mathcal{V}_0]\circ{}^{\mathcal{B}}_0L\circ F_0^{op}\stackrel{[\alpha_0,\mathcal{V}_0].({}^{\mathcal{B}}_0L\circ F_0)}{\Rightarrow}[G_0,V_0]\circ{}^{\mathcal{B}}_0L\circ F_0^{op}\colon\mathcal{A}_0^{op}\to[\mathcal{A}_0,\mathcal{V}_0]$ is the same as the composite natural transformation ${}_0^{\mathcal{A}}L\stackrel{{}^G_0L}{\Rightarrow}[G_0,\mathcal{V}_0]\circ{}^{\mathcal{B}}_0L\circ G_0^{op}\stackrel{([G_0,\mathcal{V}_0]\circ{}^{\mathcal{B}}_0L).\alpha_0^{op}}{\Rightarrow}[G_0,V_0]\circ{}^{\mathcal{B}}_0L\circ F_0^{op}\colon\mathcal{A}_0^{op}\to[\mathcal{A}_0,\mathcal{V}_0]$. Unraveling the condition leaves us with the requirement that for every pair of objects $A,B$ of $\mathcal{A}_0$ the following diagram in $\mathcal{V}_0$ must commute:
$$
\array{
\mathcal{A}(A,B)&\stackrel{F_{A,B}}{\rightarrow}&\mathcal{B}(F_0A,F_0B)\\
G_{A,B}\downarrow&&\downarrow\mathcal{B}(F_0A,(\alpha_0)_{B})\\
\mathcal{B}(G_0A,G_0B)&\stackrel{\mathcal{B}((\alpha_0)_A,G_0B)}{\rightarrow}&\mathcal{B}(F_0A,G_0B)
}$$ 
But a $\mathcal{V}$-enriched natural transformation $\alpha$ is by definition a collection of morphisms $\alpha_0$ in $\mathcal{B}_0$ such that the above diagram commutes.

* Supposing that $\mathcal{V}_0$ was a self-enriched category, i.e. isomorphic to the underlying category $\mathcal{V}^e_0$ of a $\mathcal{V}$-enriched category $\mathcal{V}^e$, then it is natural to require that the above lax natural transformation $[\mathcal{I},-]\stackrel{{}^-_0L}{\Rightarrow}[(-)_0,\mathcal{V}_0]$ is in fact the whiskering of a lax natural transformation $[\mathcal{I},-]\stackrel{{}^-L}{\Rightarrow}[-,\mathcal{V}^e]$ with the forgetful $2$-functor $(-)_0=[\mathcal{I},-]$. Such a lax natural transformation should give us most (if not all) of the closed structure on $\mathcal{V}^e_0\cong\mathcal{V}_0$...

...


## Related concepts

[[!include categories of categories - contents]]

## References

* {#Kelly82} [[Max Kelly]], Chapter 1 in: _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;



category: category

[[!redirects VCat]]
[[!redirects V Cat]]

[[!redirects category of V-enriched categories]]
[[!redirects categories of V-enriched categories]]

[[!redirects category of enriched categories]]
[[!redirects categories of enriched categories]]