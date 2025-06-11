
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
#### Category Theory
+--{: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

By __$Topos$__ (or __$Toposes$__) is denoted the [[category]] of [[toposes]]. Usually this means:

* [[objects]] are [[sheaf toposes]];

* [[morphisms]] are [[geometric morphisms]] of toposes.


> (In parts of the literature this is denoted merely "$Top$", but that clashes with the common notation for the [[Top|the category of]] [[topological spaces]].)


This is naturally a [[2-category]], where

* [[2-morphism]] are [[geometric transformations]].

That is, a 2-morphism $f\to g$ is a [[natural transformation]] $f^* \to g^*$ (which is, by [[mate]] calculus, equivalent to a natural transformation $g_* \to f_*$ between [[direct image]]s).  

Thus, $Toposes$ is equivalent to both of

* the (non-full) [[sub-2-category]] of the [[opposite 2-category|1-opposite]] $Cat^{op}$ of [[Cat]] on categories that are sheaf toposes and morphisms that are the [[inverse image]] parts of [[geometric morphisms]], and

* the (non-full) sub-2-category of the [[opposite 2-category|2-opposite]] $Cat^{co}$ of [[Cat]] on categories that are sheaf toposes and morphisms that are the [[direct image]] parts of geometric morphisms.


\begin{remark}\label{ElementaryToposesAndLogicalFunctors}
**(elementary toposes and logical functors)**
We obtain a very different 2-category of toposes if we take objects to be [[elementary toposes]] and morphisms the [[logical functors]]; this 2-category is sometimes denoted $Log$ or $LogTopos$.
\end{remark}



## Properties

### From topological spaces to toposes

The operation of forming [[categories of sheaves]]

$$
  Sh(-) \,\colon\, Top \longrightarrow Topos
$$

embeds [[topological spaces]] into toposes. For $f \colon X \to Y$ a [[continuous map]] we have that $Sh(f)$ is the [[geometric morphism]]

$$
  Sh(f) 
   \,\colon\, 
  Sh(X) 
    \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}
  Sh(Y)
$$

with $f_*$ the [[direct image]] and $f^*$ the [[inverse image]].

Strictly speaking, this functor is not an [[embedding]] if we consider $Top$ as a 1-category and $Toposes$ as a 2-category, since it is then not [[fully faithful]] in the 2-categorical sense---there can be nontrivial 2-cells between geometric morphisms between toposes of sheaves on topological spaces.

However, if we regard $Top$ as a [[(1,2)-category]] where the 2-cells are inequalities in the [[specialization ordering]], then this functor does become a 2-categorically full embedding (i.e. an equivalence on hom-categories) if we restrict to the full subcategory $SobTop$ of [[sober spaces]].  This embedding can also be extended from $SobTop$ to the entire category of [[locales]] (which can be viewed as "Grothendieck 0-toposes").


### From toposes to higher toposes

There are similar full embeddings $Topos \hookrightarrow 2 Topos$ and $Topos \hookrightarrow (n,1)Topos$ of sheaf (1-)toposes into [[2-sheaf]] [[2-toposes]] and sheaf [[(n,1)-toposes]] for $2\le n\le \infty$.  

Note that these embeddings are *not* the identity functor on underlying categories: a 1-topos is not itself an $n$-topos, instead we have to take $n$-sheaves on a suitable generating [[site]] for it.

### From locally presentable categories to toposes
 {#AdjunctionToLocallyPresentable}

There is a canonical [[forgetful functor]] $ U : Topos \to$ [[PrCat|LocPrCat]]${}^{op}$  assigning [[underlying]] [[locally presentable categories]]. 

This [[2-functor]] has a [[2-adjunction|right 2-adjoint]] ([Bunge & Carboni 1995 p 235](#BungeCarboni95)).



### Limits and colimits 
 {#Limits}

The 2-category $Topos$ is not all that well-endowed with [[limits]], but its [[slice categories]] are finitely complete [[2-limit|as 2-categories]], and $ShTopos$ is closed under finite limits in $Topos/Set$.  In particular, the [[terminal object]] in $ShToposes$ is the topos [[Set]] $\simeq Sh(*)$.



#### Colimits
 {#Colimits}

The supply with colimits is better:

+-- {: .num_prop #ColimitsByInverseImageLimits}
###### Proposition

All small (indexed) [[2-colimit]]s in $ShTopos$ exists and are computed as (indexed) [[2-limit]]s in [[Cat]] of the underlying [[inverse image]] functors.

=--

This appears as [Moerdijk, theorem 2.5](#Moerdijk)

+-- {: .num_prop}
###### Proposition

Let 

$$
  \array{
    \mathcal{F} &\stackrel{p_2}{\to}& \mathcal{E}_2
    \\
    {}^{\mathllap{p_1}}\downarrow &\swArrow& \downarrow^{\mathrlap{f_2}}
    \\
    \mathcal{E}_1 &\underset{f_1}{\to}& \mathcal{E}
  }
$$

be a [[2-pullback]] in $Topos$ such that

* $f_1, f_2$ are both [[pseudomonic morphism]]s

* $\mathcal{E}_1 \coprod \mathcal{E}_2 \to \mathcal{E}$ is an [[effective epimorphism]];

then the diagram of [[inverse image]] functors

$$
  \array{
    \mathcal{F} &\stackrel{p_2^*}{\leftarrow}& \mathcal{E}_2
    \\
    {}^{\mathllap{p_1^*}}\uparrow &\swArrow& \uparrow^{\mathrlap{f_2^*}}
    \\
    \mathcal{E}_1 &\underset{f_1^*}{\leftarrow}& \mathcal{E}
  }
$$

is a 2-pullback in [[Cat]] and so by the [above](#ColimitsByInverseImageLimits) the original square is also a 2-pushout.

=--

This appears as theorem 5.1 in ([BungeLack](#BungeLack))

+-- {: .num_prop}
###### Proposition


The 2-category $Topos$ is an [[extensive category]]. Same for toposes bounded over a base.

=--

This is in ([BungeLack, proposition 4.3](#BungeLack)).


#### Products
 {#Products}

\begin{proposition}\label{ProductOfGrothendieckToposes}
The [[Cartesian product]] of [[presheaf toposes]] $PSh(C_i)$ in $Topos$ is the presheaf topos on the [[product category]] of their sites:
\[
  \label{ToposProductOfPresheafToposes}
  PSh(C_1)
  \times_{Topos}
  PSh(C_2)
  \;\simeq\;
  PSh(C_1 \times_{Cat} C_2 )
  \,.
\]
More generally, for $J_i$ a [[Grothendieck topology]] on $C_i$, the product in $Topos$ of the sheaf topos is the sheaf topos over the product site $(C_1 \times C_2, J_1 \times J_2)$, where $J_1 \times J_2$ is the Grothendieck topology on the [[product category]] generated from products of [[covering sieves]] from $J_1$ and $J_2$:
\[
  \label{ToposProductOfSheafToposes}
  Sh(C_1, J_1)
  \times_{Topos}
  PSh(C_2, J_2)
  \;\simeq\;
  PSh(C_1 \times C_2,\,  J_1 \times J_2 )
  \,.
\]
\end{proposition}

(cf. [Pitts 1985 proof of Thm. 2.3](#Pitts85), [Valero 2018 p 98-99](#Valero18))

\begin{proof}\label{ProofOfProductOfGrothendieckToposes}
Since every sheaf topos admits a [[site]] that has all [[finite limits]], we first consider the topos-product of presheaf toposes (eq:ToposProductOfPresheafToposes) under the assumption that the sites $C_i$ have all finite limits. (We refer to these small categories $C_i$ as "sites" already, even though in the presheaf case they are as such equipped with the trivial [[Grothendieck topology]]).

To check the defining [[universal property]] of a [[Cartesian product]], we use that [[geometric morphisms]] 

$$
  f_\ast \,\colon\,
  \mathcal{X} 
    \leftrightarrow 
  \mathcal{Y}
  \,\colon\,
  f^\ast
$$

between [[sheaf toposes]] (generally between [[locally presentable categories]]) correspond bijectively to [[finite limit]]-[[preserved limit|preserving]] [[cocontinuous functors]] 

$$
  \mathcal{X} \overset{f^\ast}{\longleftarrow} \mathcal{Y}
$$

(by the [[adjoint functor theorem]] [for locally presentable categories](adjoint+functor+theorem#StatementForLocPresCategories)).

Then writing

$$
  p_i 
    \,\colon\,
  C_1 \times C_2 
  \longrightarrow
  C_i
$$

for the canonical [[projection]] functors out of the [[product category]] of the given sites, and writing


$$
  p^\ast_i
  \,\colon\,
  PSh(C_i) 
  \longrightarrow
  PSh( C_1 \times C_2 )
$$

for the corresponding pre-[[composition]] functors on presheaves (which presverve all (co)limits since (co)[[limits of presheaves are computed objectwise]]), it is sufficient to show that for  $\mathcal{X} \in Topos$ and

$$
  f^\ast_i
  \,\colon\,
  PSh(C_i) \longrightarrow \mathcal{X}
  \,,
  \;\;\;\;
  i \in \{1,2\}
$$

a [[pair]] of cocontinuous and finitely continuous functors, there is a unique such functor

$$
  (f_1, f_2)^\ast \,\colon\,
  PSh(C_1 \times C_2) \longrightarrow \mathcal{X}
$$

which makes the following [[commuting diagram|diagram commute]]:

\begin{tikzcd}
  & 
  \mathcal{X}  
  \\
  & 
  \mathrm{PSh}(C_1 \times C_2)
  \ar[
    u, 
    dashed,
    "{ (f_1, f_2)^\ast }"{description}
  ]
  \\
  \mathrm{PSh}(C_1)    
  \ar[
    uur,
    "{ f^\ast_1 }"
  ]
  \ar[
    ur,
    "{ p^\ast_1 }"{swap}
  ]
  &&
  \mathrm{PSh}(C_2)  
  \ar[
    uul,
    "{ f^\ast_2 }"{swap}
  ]
  \ar[
    ul,
    "{ p^\ast_2 }"
  ]
\end{tikzcd}

To this end, observe that for a [[representable presheaf]]

$$
  c_i \,\in\, C_i \xhookrightarrow{y} PSh(C_i) 
$$

(with the [[Yoneda embedding]] $y$ on the right)

we evidently have

\[
  \label{PullbackOfRepresentablesAlongProductProjection}
  p^\ast_1\big( y(c_1) \big)
    \,\simeq\, 
  y(c_1, \ast_2)
  \;\;\;\;
  \text{and}
  \;\;\;\;
  p^\ast_2\big( y(c_2) \big)
    \,\simeq\, 
  y(\ast_1,  c_2)
\]

(where "$\ast_i$" denotes the [[terminal object]] of $C_i$). It follows that to be finite-limit preserving, and hence in particular [[finite product]]-preserving, the dashed map must send representables 

$$
  (c_1, c_2) \,\in\, C_1 \times C_2 
  \xhookrightarrow{y} PSh(C_1 \times C_2)
$$

to

$$
  \begin{array}{rcl}
    (f_1, f_2)^\ast
    \big( 
      y(c_1, c_2)
    \big)
    &\simeq&
    (f_1, f_2)^\ast
    \big( 
      y\big( 
        (c_1, \ast_2) 
        \times 
        (\ast_1, c_2)
    \big)
    \\
    &\simeq&
    (f_1, f_2)^\ast
    \big( 
      y(c_1, \ast_2) 
        \times 
      y(\ast_1, c_2))
    \big)
    \\
    &\simeq&
    (f_1, f_2)^\ast
    \big( 
      y(c_1, \ast_2) 
    \big)
    \times
    (f_1, f_2)^\ast
    \big( 
      y(\ast_1, c_2) 
    \big)
    \\
    &\simeq&
    (f_1, f_2)^\ast
    \circ
    p^\ast_1 
    \big(
       y(c_1) 
    \big)
    \;\times\;
    (f_1, f_2)^\ast
    \circ
    p^\ast_2
    \big( 
      y(c_2) 
    \big)
    \\
    &\simeq&
    f^\ast_1\big(y(c_1)\big)
    \times
    f^\ast_2\big(y(c_2)\big)
    \,,
  \end{array}
$$

where we have used, in order of appearance, that:

1. limits in a product category are computed via the limits in the factor categories,

1. the [Yoneda embedding preserves limits](Yoneda+embedding#PreservesLimits),

1. $(f_1, f_2)^\ast$ is assumed to preserve finite limits,

1. the equivalences (eq:PullbackOfRepresentablesAlongProductProjection) hold,

1. the above triangles commute.

So this fixes the values of $(f_1, f_2)^\ast$ on all representables. But thereby it actually fixes its values on all of $PSh(C_1 \times C_2)$, since the latter is the [[free cocompletion]] of $C_1 \times C_2$ (all [presheaves are colimits of representables](presheaf#PresheavesAreColimitsOfRepresentables)) and since $(f_1, f_2)^\ast$ is also required to be cocontinuous and hence must [[preserved colimit|preserve]] these colimits. 

This establishes the claim 

$$
  PSh(C_1) \times_{Topos} PSh(C_2)
  \,\simeq\,
  PSh(C_1 \times C_2)
$$

for the case that the $C_i$ have all finite limits. To conclude, it is now sufficient to observe that this construction descends to sheaf toposes as claimed.

To that end, just to note that for a geometric morphism $f$ between presheaf toposes to descend to sheaves is equivalent to $f^\ast$ sending covering morphisms to [[local isomorphisms]] (cf. at *[[morphism of sites]]*, because, by adjunction, this is equivalently the condition for $f_\ast$ to take sheaves to sheaves, whence as such its left adjoint is $f^\ast$ followed by [[sheafification]]).
\end{proof}


\begin{example}
  A category $sSh(C)$ of [[simplicial sheaves]] is the Topos-product of the corresponding sheaf topos of Set-values sheaves with the topos $sSet$ of [[simplicial sets]], the latter being the [[presheaf topos]] over the [[simplex category]]:

$$
  sSh(C)
  \,\equiv\,
  Sh(C,sSet)
  \;\simeq\;
  Sh(C \times \Delta)
  \;\simeq\;
  Sh(C) \times_{Topos} Sh(\Delta)
  \;\simeq\;
  Sh(C) \times_{Topos} sSet
  \,.
$$


\end{example}


\linebreak


#### Pullbacks
 {#Pullbacks}

+-- {: .num_prop}
###### Proposition

Let 

$$
  \array{
    && \mathcal{X}
    \\
    && \downarrow^{\mathrlap{(g^* \dashv g_*)}}
    \\
    \mathcal{Y}
    &\stackrel{(f^* \dashv f_*)}{\to}&  
    \mathcal{Z}
  }
$$

be a [[diagram]] of [[toposes]]. Then its [[pullback]] in the [[(2,1)-category]] version of $Topos$ is computed, roughly, by the [[pushout]] of their [[sites]] of definition.

More in detail: there exist [[sites]] $\tilde \mathcal{D}$, $\mathcal{D}$, and $\mathcal{C}$ with [[finite limit]]s and [[morphisms of sites]]  

$$
  \array{
    && \mathcal{D}
    \\
    && \uparrow^{\mathrlap{g}}
    \\
    \tilde \mathcal{D}
    &\stackrel{f}{\leftarrow}&  
    \mathcal{C}
  }
$$

such that

$$
  \left(
  \array{
    && \mathcal{X}
    \\
    && 
    ^{\mathllap{(g^* \dashv g_*)}}
    \Big\downarrow
    \\
    \mathcal{Y}
    &\underset{(f^* \dashv f_*)}{\longrightarrow}&  
    \mathcal{Z}
  }
  \right) 
  \,\,\,
   \simeq
  \,\,\,
  \left(
  \array{
    && Sh(\mathcal{D})
    \\
    && 
    ^{\mathllap{(Lan_g \dashv (-)\circ g)}}\Big\downarrow
    \\
    Sh(\tilde \mathcal{D})
    &\underset{(Lan_f \dashv (-)\circ f)}{\longrightarrow}&  
    Sh(\mathcal{C})
  }
  \right) 
  \,.
$$

Let then 

$$
  \array{
    \widetilde{\mathcal{D}} 
      \textstyle{\coprod_{\mathcal{C}}} 
    \mathcal{D} 
      &\overset{f'}{\longleftarrow}& 
    \mathcal{D}
    \\
    \mathllap{{}^{g'}}\big\uparrow 
       &\swArrow_{\simeq}& 
    \big\uparrow\mathrlap{^g}
    \\
    \widetilde{\mathcal{D}}
      &\underset{f}{\longleftarrow}&  
    \mathcal{C}
  }
  \,\,\,\,\,
  \in
  Cat^{lex}
$$

be the [[pushout]] of the underlying [[categories]] in the non-[[full subcategory|full]] [[subcategory]] ${Cat}^{lex} \subset Cat$ of categories with [[finite limits]] and [[preserved limit|limit-preserving]] functors between them (cf. [Lurie, prop. 6.3.4.3](#Lurie)).

Let moreover

$$
  Sh\big(
    \widetilde{\mathcal{D}}
      \textstyle{\coprod_{\mathcal{C}}} 
    \mathcal{D}
  \big)
  \hookrightarrow
  PSh\big(
    \widetilde{\mathcal{D}} 
      \textstyle{\coprod_{\mathcal{C}}}
    \widetilde{\mathcal{D}}
  \big)
$$

be the [[reflective subcategory]] obtained by [[localization]] at the class of morphisms generated by the inverse image $Lan_{f'}(-)$ of the [[covering]]s of $\mathcal{D}$ and the inverse image $Lan_{g'}(-)$ of the coverings of $\tilde \mathcal{D}$.

Then

$$
  \array{
    Sh(\tilde \mathcal{D} \coprod_{\mathcal{C}} \mathcal{D})
    &\to& \mathcal{X}
    \\
    \downarrow && \downarrow^{\mathrlap{(g^* \dashv g_*)}}
    \\
    \mathcal{Y}
    &\stackrel{(f^* \dashv f_*)}{\to}&  
    \mathcal{Z}
  }
$$

is a [[pullback]] square.


=--

This appears as [Lurie, prop. 6.3.4.6](#Lurie).


+-- {: .num_remark}
###### Remark

For [[localic toposes]] this reduces to the statement of [[localic reflection]]: the pullback of toposes is given by the of pullback the underlying [[locales]] which in turn is the [[pushout]] of the corresponding [[frames]].

=--

### Free loop spaces

The [[free loop space object]] of a topos in [[Topos]] is called the [[isotropy group of a topos]].

## Related concepts

* **Topos**

* [[(∞,1)Topos]]


## References

On [[Cartesian products]] and [[base change]] in $Topos$:

* {#Pitts85} [[Andrews Pitts]]: *On product and change of base for toposes*, [[Cahiers]] de topologie et géométrie différentielle catégoriques **26** 1 (1985) 43-61 &lbrack;[numdam:CTGDC_1985__26_1_43_0](https://www.numdam.org/item/?id=CTGDC_1985__26_1_43_0), [pdf](https://www.numdam.org/item/CTGDC_1985__26_1_43_0.pdf)&rbrack;

On the characterization of colimits in $Topos$:

* {#Moerdijk} [[Ieke Moerdijk]], _The classifying topos of a continuous groupoid. I_ Transaction of the American mathematical society **310** 2 (1988) &lbrack;[pdf](http://www.ams.org/journals/tran/1988-310-02/S0002-9947-1988-0973173-9/S0002-9947-1988-0973173-9.pdf)&rbrack;

The fact that $Topos$ is extensive:

* {#BungeLack} [[Marta Bunge]], [[Steve Lack]]: _van Kampen theorem for toposes_ &lbrack;[ps](http://www.maths.usyd.edu.au/u/stevel/papers/vkt.ps.gz)&rbrack;

General limits and colimits of toposes: 

* {#Lurie} [[Jacob Lurie]], 6.3.2-6.3.4 of: _[[Higher Topos Theory]]_ (2009) 
  > (discussed for [[(∞,1)-toposes]], but the statements are verbatim true in the [[(2,1)-category]] category $Topos$)

The adjunction between toposes and locally presentable categories:

* {#BungeCarboni95} [[Marta Bunge]], [[Aurelio Carboni]]: *The symmetric topos*, Journal of Pure and Applied Algebra **105** (1995) 233-249 \[<a href="https://doi.org/10.1016/0022-4049(94)00157-X">doi;10.1016/0022-4049(94)00157-X</a>\]


See also:

* {#Valero18} Juan Sebastian Arias Valero: *Gesture Theory: Topos-Theoretic Perspectives and Philosophical Framework*, PhD thesis (2018) &lbrack;[handle:63339](https://repositorio.unal.edu.co/handle/unal/63339), [pdf](https://repositorio.unal.edu.co/bitstream/handle/unal/63339/Thesisfinal.pdf)&rbrack;


category: category

[[!redirects Topos]]
[[!redirects Topoi]]
[[!redirects Toposes]]
