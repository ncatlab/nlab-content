

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn}
###### Definition

Let $E$ be a [[locally small category]] with all small [[colimit]]s. An object $e$ of $E$ is called **tiny** or **small-[[projective object]]** ([Kelly, &#167;5.5](#Kelly)) if the [[hom-functor]] $E(e, -) : E \to Set$ preserves small colimits.

More generally, for $V$ a [[cosmos]] and $E$ a $V$-[[enriched category]], $e \in E$ is called tiny if $E(e,-) : E \to V$ preserves all small colimits.
=--


## Remarks

* Since being an [[epimorphism]] is a "colimit-property" (a morphism is epic iff its pushout with itself consists of identities), if $e$ is tiny then $E(e,-)$ preserves epimorphisms, which is to say that $e$ is [[projective object|projective]] (with respect to epimorphisms).  This is presumably the origin of the term "small-projective", i.e. the corepresentable functor preserves small colimits instead of just a certain type of finite one.

* If $E$ is [[cartesian closed category|cartesian closed]] and the inner hom $(-)^e$ has a [[right adjoint]] (and hence preserves all colimits), $e$ is called [[infinitesimal object|atomic]] or [[infinitesimal object|infinitesimal]]. The right adjoint is sometimes called an [[amazing right adjoint]], particularly in the context of [[synthetic differential geometry]]. If $E$ is a sheaf topos, then tiny objects and infinitesimal objects coincide, by the [[adjoint functor theorem]].


## Properies

### General

+-- {: .num_prop}
###### Observation

Any [[retract]] of a tiny object is tiny, since [[split idempotent|splitting of idempotents]] is an [[absolute colimit]] (see also [Kelly, prop. 5.25](#Kelly)).  

=--

### In presheaf categories


+-- {: .num_prop}
###### Observation

In a [[presheaf category]] every [[representable functor|representable]] is a tiny object: 

since colimits of presheaves are computed objectwise (see [[limits and colimits by example]]) and using the [[Yoneda lemma]] we have for $U$ a [[representable]] functor and $F : J \to PSh$ a diagram that

$$
  Hom(U, \lim_\to F) \simeq (\lim_\to F)(U) \simeq \lim_\to F(U)
$$

where now the last [[colimit]] is in [[Set]].

=--

Thus, in a presheaf category, any [[retract]] of a representable functor is tiny. In fact the converse also holds:


+-- {: .num_prop}
###### Proposition

The tiny objects in a [[presheaf category]] are precisely the [[retract]]s of [[representable functor]]s.  

=--

This is for instance ([BorceuxDejean, prop 2](#BorceuxDejean)).

Thus, if the domain category is [[Cauchy complete category|Cauchy complete]] (has [[split idempotent]]s), then every tiny presheaf is representable; and more generally the Cauchy completion or [[Karoubi envelope]] of a category can be defined to consist of the tiny presheaves on it. See [[Cauchy complete category]] for more on this.


In the context of [[topos theory]] we say, for $C$ [[small category]], that an [[adjoint triple]] of [[functor]]s 

$$
  Set \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  [C,Set]
$$

is an [[essential geometric morphism]] of [[topos]]es $f : Set \to [C,Set]$; or an **[[point of a topos|essential point]]** of $[C,Set]$.

By the [[adjoint functor theorem]] this is equivalently simply a single functor $f^* : [C, Set] \to Set$ that preserves all small [[limit]]s and [[colimit]]s. Write

$$
  Topos_{ess}(Set,[C,Set]) 
   \simeq 
  LRFunc([C,Set], Set)
   \subset 
  Func([C,Set], Set)
$$

for the [[full subcategory]] of the [[functor category]] on functors that have a [[left adjoint]] and a [[right adjoint]].

+-- {: .num_prop}
###### Proposition

For $C$ a [[small category]] there is an [[equivalence of categories]]

$$
  \overline{C} := TinyObjects([C,Set]) \simeq \simeq Topos_{ess}(Set, [C,Set])^{op}
$$

of the tiny objects of $[C,Set]$ with the category of essential points of $[C,Set]$.

=--

+-- {: .proof}
###### Proof

We first exhibit a [[full subcategory|full inclusion]] $Topos_{ess}(Set,[C,Set])^{op} \hookrightarrow \overline{C}$.

So let $Set \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}} [C,Set]$ be an [[essential geometric morphism]]. Then because $f_!$ is [[left adjoint]] and thus preserves all small [[colimits]] and because every [[set]] $S \in Set$ is the colimit over itself of the singleton set we have that

$$
  f_! S \simeq \coprod_{s \in S} f_!(*)
$$

is fixed by a choice of [[copresheaf]]

$$
  F := f_!(*) \in [C, Set]
  \,.
$$

The $(f_! \dashv f^*)$-[[adjunction]] [[isomorphism]] then implies that for all $H \in [C,Set]$ we have

$$
  f^* H \simeq Set(*, f^* H) \simeq [C,Set](f_! *, H)
  \simeq [C,Set](F,H)
  \,.
$$

naturally in $H$, and hence that

$$
  f^*(-) \simeq [C,Set](F,-) : Set \to [C,Set]
  \,.
$$

By assumption this has a further right adjoint $f_!$ and hence preserves all [[colimits]]. By the discussion at [[tiny object]] it follows that $F \in [C,Set]$ is a tiny object. By prop. \ref{CauchyComplIsFullSubcatOnTinyObjects} this means that $F$ belongs to $\overline{C} \subset [C,Set]$.

A morphism $f \Rightarrow g$ between [[geometric morphisms]] $f,g : Set \to [C,Set]$ is a [[geometric transformation]], which is a [[natural transformation]] $f^* \Rightarrow g^*$, hence by the above a natural transformation $[C,Set](F,-) \Rightarrow [C,Set](G,-)$. By the [[Yoneda lemma]] these are in bijection with morphisms $G \to H$ in $[C,Set]$. This gives the full inclusion $Topos_{ess}(Set,[C,Set])^{op} \subset \overline{C}$.

The converse inclusion is now immediate by the same arguments: since the objects in $\overline{C}$ are precisely the [[tiny object]]s $F \in [C,Set]$ each of them corresponds to a functor $[C,Set](F,-) : [C,Set] \to Set$ that has a [[right adjoint]]. Since this generally also has a left adjoint, it is the [[inverse image]] of an essential geometric morphism $f : Set \to [C,Set]$.

=--



## References

The term _small projective object_ is used in  section 5.5. of 

* [[Max Kelly]], _Basic Concepts of Enriched Category Theory_ ([pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))
{#Kelly}

Tiny objects in presheaf categories ([[Cauchy complete categories|Cauchy completion]]) are discussed in

* [[Francis Borceux]] and D. Dejean, _Cauchy completion in category theory_  Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;goriques, 27:133&#8211;146, (1986) ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_133_0))
  {#BorceuxDejean}


[[!redirects small-projective object]]
[[!redirects small-projective objects]]
[[!redirects small-projective]]

[[!redirects tiny objects]]
[[!redirects tiny]]
