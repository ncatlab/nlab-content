

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

Let $E$ be a [[locally small category]] with all small [[colimits]]. An object $e$ of $E$ is called **tiny** or  **small-[[projective object|projective]]** ([Kelly 1982, &#167;5.5](#Kelly82)) if the [[hom-functor]] $E(e, -) \colon E \to Set$ [[preserved colimit|preserves]] [[small colimits]]. It is called **absolutely presentable** if the functor preserves all colimits.

More generally, for $V$ a [[cosmos]] and $E$ a $V$-[[enriched category]], $e \in E$ is called tiny if $E(e,-) \colon E \to V$ preserves all small colimits.
=--

+-- {: .num_remark}
###### Remark

Since being an [[epimorphism]] is a "colimit-property" (a morphism is epic iff its [[pushout]] with itself consists of identities), if $e$ is tiny then $E(e,-)$ preserves epimorphisms, which is to say that $e$ is [[projective object|projective]] (with respect to epimorphisms).  This is presumably the origin of the term "small-projective", i.e. the corepresentable functor preserves small colimits instead of just a certain type of finite one.

=--


+-- {: .num_defn #Atomic} 
###### Definition

If $E$ is [[cartesian closed category|cartesian closed]] and the 
[[inner hom]] $(-)^e$ has a [[right adjoint]] (and hence preserves all colimits), $e$ is called (internally) **atomic** or [[infinitesimal object|infinitesimal]]. 

=--

(See for instance [Lawvere 97](#Lawvere97).)

+-- {: .num_remark}
###### Remark

The [[right adjoint]] in def. \ref{Atomic} is sometimes called an "[[amazing right adjoint]]", particularly in the context of [[synthetic differential geometry]]. 

=--

+-- {: .num_remark} 
###### Remark 
Various terminological discrepancies in the literature hinge on the distinction between internal notions and external notions. Thus, if $E$ is a [[cartesian closed category]] with small colimits, we may say $e \in Ob(E)$ is *internally* tiny if the functor $(-)^e: E \to E$ preserves small colimits. Relatedly, the word "atomic" has been used in both an external sense where $E(e, -): E \to Set$ has a right adjoint, as in Bunge's thesis, and in an internal sense, as when Lawvere refers to $e$ as an a.t.o.m. ("amazingly tiny object model") if $(-)^e: E \to E$ has a right adjoint. But under certain hypotheses, the two notions coincide; see for instance Proposition \ref{coincide}. 
=-- 

+-- {: .num_prop #InSheafToposTinyImpliesAtomic}
###### Proposition

If $E$ is a [[sheaf topos]], then (externally) tiny objects and externally atomic objects coincide.

=--

+-- {: .proof}
###### Proof

Clearly any externally atomic object is tiny. For the converse, use a dual form of the special [[adjoint functor theorem]] (SAFT): $E$ is [[locally small category|locally small]], [[cocomplete category|cocomplete]], and [[well-powered category|co-well-powered]] (because for any object $X$, equivalence classes of [[epimorphisms]] with domain $X$ are in natural bijection with [[internal equivalence relations]] on $X$, and there is a small set of these because they are contained in a set isomorphic to $\hom(X \times X, \Omega)$), and finally $E$ has a [[generating set]] (namely, the set of associated [[sheaves]] of [[representables]] coming from a small [[site]] presentation for $E$). Under these conditions, the SAFT guarantees that any [[cocontinuous functor]] $E \to C$ has a right adjoint, provided that $C$ is locally small; then apply this to the case $C = Set$. 

=-- 

Clearly the statement and the proof of Proposition \ref{InSheafToposTinyImpliesAtomic} carry over when "external" is replaced by "internal" throughout. 

## Properties

### General

+-- {: .num_prop}
###### Proposition

Any [[retract]] of a tiny object is tiny, since [[split idempotent|splitting of idempotents]] is an [[absolute colimit]] (see also [Kelly, prop. 5.25](#Kelly82)).  

=--



### In categories of modules over rings
 {#InCategoriesOfModulesOverRings}

The notion of tiny object is clearly highly dependent on the base of [[enriched category|enrichment]]. For example, for a [[ring]] $R$, the tiny objects in the category of left $R$-[[category of modules|modules]] $Ab^R$, considered as an [[Ab]]-[[enriched category]], are the [[finitely generated module|finitely generated]] [[projective modules]]. Certainly f.g. projective modules are tiny because $R$ is tiny (the [[forgetful functor]] $\hom(R, -): Ab^R \to Ab$ preserves $Ab$-[[colimits]]) and the closure of $R$ under finite direct sums and retracts, which are absolute $Ab$-[[colimits]], comprise finitely generated projective modules. See also _[[Cauchy completion]]_. 

On the other hand, when the category $Ab^R$ is considered as a [[Set]]-[[enriched category]], there are _no_ tiny objects. In fact this is true for any Set-enriched category with a [[zero object]]: Let $X$ be a tiny object. The morphism $X \to 0$ induces a map $Hom(X,X) \to Hom(X,0)$. This map has empty codomain (since $Hom(X,-)$ preserves the zero object, as an empty colimit). Thus $Hom(X,X) = \emptyset$ in contradiction to $id_X \in Hom(X,X)$.


### In presheaf categories


+-- {: .num_example}
###### Example

In a [[presheaf category]] every [[representable functor|representable]] is a tiny object: 

since colimits of presheaves are computed objectwise (see [[limits and colimits by example]]) and using the [[Yoneda lemma]] we have for $U$ a [[representable]] functor and $F : J \to PSh$ a diagram that

$$
  Hom(U, \lim_\to F) \simeq (\lim_\to F)(U) \simeq \lim_\to F(U)
$$

where now the last [[colimit]] is in [[Set]].

=--

Thus, in a presheaf category, any [[retract]] of a representable functor is tiny. In fact the converse also holds:


+-- {: .num_prop #representables}
###### Proposition

The tiny objects in a [[presheaf category]] are precisely the [[retracts]] of [[representable functor]]s.  

=--

This is for instance ([BorceuxDejean, prop 2](#BorceuxDejean)). For instance, the only tiny object in [[G-set]] is $G$ itself with its regular action.

Thus, if the domain category is [[Cauchy complete category|Cauchy complete]] (has [[split idempotent]]s), then every tiny presheaf is representable; and more generally the Cauchy completion or [[Karoubi envelope]] of a category can be defined to consist of the tiny presheaves on it. See [[Cauchy complete category]] for more on this. 

+-- {: .num_prop #coincide} 
###### Proposition 
For presheaves on a category $C$ with finite products, the notions of externally tiny object and internally tiny object coincide. 
=-- 

+-- {: .proof} 
###### Proof 
Without loss of generality, we may assume $C$ is Cauchy complete (note that the Cauchy completion of a category with finite products again has finite products), so that tiny presheaves coincide with representable functors $C(-, c)$. 

Let $E$ denote the presheaf category. Given that the empty product $1$ is tiny, if $e \in Ob(E)$ is internally tiny, then the composite 

$$E(e, -): E \to Set = \left(E \stackrel{(-)^e}{\to} E \stackrel{E(1,-)}{\to} Set \right)$$ 

is cocontinuous, hence $e$ is externally tiny. 

In the other direction, recall how exponentials $G^F$ in $E = PSh(C)$ are constructed: we have the formula 

$$G^F(c) = E(C(-, c) \times F, G).$$ 

In particular, if $F$ is externally tiny, hence a representable $C(-, c')$, we have 

$$G^F(c) = E(C(-, c) \times C(-, c'), G) \cong E(C(-, c \times c'), G) \cong G(c \times c')$$ 

where the last isomorphism is by the [[Yoneda lemma]]. Since colimits in $PSh(C)$ are computed pointwise, whereby evaluation functors $ev_c: PSh(C) \to Set$ preserve colimits, we see that $(-)^{C(-, c')}: G \mapsto G(- \times c')$ preserves colimits, so that $F = C(-, c')$ is internally tiny. The amazing right adjoint $R$ in this case takes a presheaf $H$ to the presheaf $R H$ that takes an object $d$ to the set $(R H)(d) = E(C(- \times c', d), H)$. 
=-- 

(Compare the result [here](https://ncatlab.org/nlab/show/internally+projective+object#enough).) 



In the context of [[topos theory]] we say, for $C$ [[small category]], that an [[adjoint triple]] of [[functors]] 

$$
  Set \stackrel{\overset{f_!}{\to}}{\stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}}}
  [C,Set]
$$

is an [[essential geometric morphism]] of [[topos]]es $f : Set \to [C,Set]$; or an **[[point of a topos|essential point]]** of $[C,Set]$. 

By the [[adjoint functor theorem]] this is equivalently simply a single functor $f^* : [C, Set] \to Set$ that preserves all small [[limits]] and [[colimits]]. Write

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
  \overline{C} := TinyObjects([C,Set]) \simeq Topos_{ess}(Set, [C,Set])^{op}
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

### In a local topos
 {#AtomsInALocalTopos}

+-- {: .num_prop #SliceOverAtomicObject}
###### Proposition

The [[terminal object]] in any [[local topos]] is atomic.

In particular for $\mathbf{H}$ a [[topos]] and $X \in \mathbf{H}$ an object, the [[slice topos]] $\mathbf{H}_{/X}$ is [[local topos|local]] precisely if $X$ is atomic.

=--

This is discuss at [local geometric morphism -- Local over-toposes](local+geometric+morphism#LocalOverTopoes).


### In a cohesive topos
 {#AtomsInACohesiveTopos}

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]]. Write $(\int \dashv \flat \dashv \sharp)$ for its [[adjoint triple]] of [[shape modality]] $\dashv$ [[flat modality]] $\dashv$ [[sharp modality]].
Consider the following basic notion from _[[cohesive (∞,1)-topos -- structures]]_.

+-- {: .num_defn}
###### Definition

An [[object]] $X \in \mathbf{H}$ is called _geometrically contractible_ if its [[shape modality|shape]] is [[contractible]], in that $\int X \simeq \ast$.

=--

+-- {: .num_prop #InCohesionAtomicObjectIsGeometricallyContractible}
###### Proposition

Over the [[base (∞,1)-topos]] [[∞Grpd]],
every atom in a [[cohesive (∞,1)-topos]] is geometrically contractible.

=--

+-- {: .proof}
###### Proof

By [[reflective sub-(∞,1)-category|reflection]] of the [[discrete objects]] it will be sufficient to show that for all [[discrete objects]] $S \in \infty Grpd \hookrightarrow \mathbf{H}$ we have an [[equivalence]]

$$
  \left[\int X , S\right] \simeq S
  \,.
$$

Now notice that, by the discussion at _[∞-tensoring](limit+in+a+quasi-category#Tensoring)_, every [[discrete object]] here is the [[homotopy colimit]] indexed by itself of the [[(∞,1)-functor]] constant on the [[terminal object]]:

$$
  S \simeq \underset{\rightarrow}{\lim}_S \ast
  \,. 
$$

Using this we have

$$
  \begin{aligned}
    \left[\int X, S\right]
    &\simeq
    \left[
       X, \flat S
    \right]
    \\
    & \simeq 
    \left[
       X, \flat \underset{\rightarrow}{\lim}_S \ast
    \right]
    \\
    & \simeq 
    \left[
       X, \underset{\rightarrow}{\lim}_S \flat  \ast
    \right]
    \\
    & \simeq 
    \underset{\rightarrow}{\lim}_S
    \left[
       X, \flat  \ast
    \right]
    \\
    & \simeq 
    \underset{\rightarrow}{\lim}_S
    \left[
       X, \ast
    \right]
    \\
    & \simeq 
    \underset{\rightarrow}{\lim}_S
    \ast
    \\
    & \simeq 
    S
  \end{aligned}
  \,.
$$

where we applied, in order of appearance: the $(\int \dashv \flat)$-[[adjunction]], the $\infty$-[[tensoring]], the fact that $\flat$ is also [[left adjoint]] (hence the existence of the [[sharp modality]]), the assumption that $X$ is atomic, then again the fact that $\flat$ is right adjoint, that $\ast$ is the terminal object and finally again the $\infty$-tensoring.

=--

+-- {: .num_prop #SliceOfCohesionOverAtomIsCohesive}
###### Proposition

Let $\mathbf{H}$ be a [[cohesive (∞,1)-topos]] over [[∞Grpd]] and let $X \in \mathbf{H}$ be an atomic object. Then the [[slice (∞,1)-topos]] $\mathbf{H}_{/X}$ sits by an [[adjoint quadruple]] over [[∞Grpd]] whose leftmost adjoint preserves the terminal object.

=--

+-- {: .proof}
###### Proof

By the discussion at [[étale geometric morphism]], the [[slice (∞,1)-topos]] comes with an [[adjoint triple]] of the form

$$
  \mathbf{H}_{/X}
   \stackrel{\overset{\sum_X}{\longrightarrow}}{\stackrel{\overset{(-)\times X}{\leftarrow}}{\stackrel{\overset{\prod_X}{\longrightarrow}}{\underset{}{}}}}
  \mathbf{H}
    \stackrel{\overset{\Pi}{\longrightarrow}}{\stackrel{\overset{Disc}{\leftarrow}}{\stackrel{\overset{\Gamma}{\longrightarrow}}{\underset{CoDisc}{\leftarrow}}}}
  \infty Grpd
  \,.
$$

The bottom composite $\Gamma\circ \prod_X$
has an extra right adjoint by prop \ref{SliceOverAtomicObject}. The extra left adjoint $\Pi \circ \sum_X$ preserves the terminal object by prop. \ref{InCohesionAtomicObjectIsGeometricallyContractible}.


=--


## Related concepts


* [[atom]] (in a [[poset]])

* [[atomic category]]


## References

The term _small projective object_ is used in: 

* {#Kelly82} [[Max Kelly]], section 5.5. of: _Basic concepts of enriched category theory_, London Math. Soc. Lec. Note Series __64__, Cambridge Univ. Press (1982), Reprints in Theory and Applications of Categories **10** (2005) 1-136  &lbrack;[ISBN:9780521287029](https://www.cambridge.org/de/academic/subjects/mathematics/logic-categories-and-sets/basic-concepts-enriched-category-theory?format=PB&isbn=9780521287029), [tac:tr10](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html), [pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf)&rbrack;

Tiny objects in presheaf categories ([[Cauchy complete categories|Cauchy completion]]) are discussed in

* {#BorceuxDejean} [[Francis Borceux]] and D. Dejean, _Cauchy completion in category theory_  Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;goriques, 27:133&#8211;146, (1986) &lbrack;[numdam:CTGDC_1986__27_2_133_0](http://www.numdam.org/item?id=CTGDC_1986__27_2_133_0)&rbrack;
  

* [[David Yetter]]: _On right adjoints to exponential functors_, Journal of Pure and Applied Algebra **45** 3 (1987) 287-304 &lbrack;<a href="https://doi.org/10.1016/0022-4049(87)90077-6">doi:10.1016/0022-4049(87)90077-6</a>&rbrack;

The term "atomic object" or rather "a.t.o.m" is suggested in 

* {#Lawvere97} [[William Lawvere]], _[[Toposes of laws of motion]]_ (1997)
 
A [[modal type theory]] for tiny objects:

* [[Mitchell Riley]], *A Type Theory with a Tiny Object* &lbrack;[arXiv:2403.01939](https://arxiv.org/abs/2403.01939)&rbrack;

* [[Mitchell Riley]]: *Tiny Objects in Type Theory*, [talk at](CQTS#RileyTinyApr2024) *[Running HoTT 2024](CQTS#RunningHoTT2024)*, [[CQTS]] @ NYU Abu Dhabi (Apr 2024) &lbrack;slides:[[Riley-TinyTypes-Apr2024.pdf:file]], video: [kt](https://cdnapisec.kaltura.com/html5/html5lib/v2.73.2/mwEmbedFrame.php/p/1674401/uiconf_id/23435151/entry_id/1_31zdfvgi?wid=_1674401&iframeembed=true&playerId=kaltura_player&entry_id=1_31zdfvgi)&rbrack;




[[!redirects tiny objects]]


[[!redirects tiny type]]
[[!redirects tiny types]]


[[!redirects small-projective object]]
[[!redirects small-projective objects]]
[[!redirects small-projective]]

[[!redirects tiny]]

[[!redirects atomic object]]
[[!redirects atomic objects]]

[[!redirects absolutely presentable]]


