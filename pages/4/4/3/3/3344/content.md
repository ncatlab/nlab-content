+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The notion of a  _test category_ ([Grothendieck 83](#Grothendieck83))
is meant to axiomatize common features of [[categories]] of [[geometric shapes for higher structures|shapes]] used to model [[homotopy types]] in [[homotopy theory]], such as the categories of [[simplicial sets]], [[cubical sets]] or [[cellular sets]]. 

## Definition

Given any [[small category]] $\mathcal{C}$, one considers $\mathcal{C}$-sets, hence [[presheaves]] on $\mathcal{C}$, hence [[contravariant functors]] from $\mathcal{C}$ to [[Set]]. 

Given an [[object]] $c\in C$, one considers the [[representable functor]] $Hom_{\mathcal{C}}(-,c)=:\Delta^c$. If $X \colon \mathcal{C}^{op} \to Set$ is a $\mathcal{C}$-set, the [[elements]] of $X(c)$ are called the _$c$-cells_. By the [[Yoneda lemma]], they correspond to the [[natural transformations]] $\Delta^c\to X$. 

Let the **cell category** of $X$, denoted $i_{\mathcal{C}} X$, be the [[full subcategory]] of the [[overcategory]] $\mathcal{C}Set/X$ whose [[objects]] are the transformations of the form $\Delta^c\to X$. (This is another name for the [[category of elements]] of $X$.) 

The correspondence $X\mapsto i_{\mathcal{C}}X$ extends to a [[functor]] $i_{\mathcal{C}} \colon\mathcal{C}Set
\to $ [[Cat]], which has a [[right adjoint]] $i_{\mathcal{C}}^* \colon Cat\to\mathcal{C}Set$ whose object part is given by the formula

$$ i_{\mathcal{C}}^*(D)(c)
  \coloneqq
Hom_{Cat}(\mathcal{C}/c,D)
\,.
$$

Denote the [[counit of the adjunction]] $\epsilon : i_{\mathcal{C}}i_{\mathcal{C}}^*\to Id_{Cat}$. 

A [[morphism]] of $\mathcal{C}$-sets $f\colon X\to Y$ is a **weak equivalence** is the induced map $i_{\mathcal{C}}(f)\colon i_{\mathcal{C}} X\to i_{\mathcal{C}} Y$ of their cell categories, i.e., the induced map of [[nerves]] ("[[classifying spaces]]") $B(i_{\mathcal{C}} X)\to B(i_{\mathcal{C}} Y)$ is a [[weak equivalence of simplicial sets]].
Two $\mathcal{C}$-sets $X$ and $Y$ are called **weakly equivalent** if there is a weak equivalence $f \colon X\to Y$. The functor
$$i_{\mathcal{C}}:\mathcal{C}Set\to Cat$$
induces a functor
$$i_{\mathcal{C}*}:Ho(\mathcal{C}Set)\to Ho(Cat)$$
of the [[homotopy categories]].  

+-- {: .num_defn #testcategory}
###### Definition

A $\mathcal{C}$-set $X$ is called **aspherical** if the category $i_{\mathcal{C}}(X)$ is weakly contractible, i.e. the nerve $B(i_{\mathcal{C}}(X))$ is a weakly contractible simplicial set. Note that if $\mathcal{C}$ is a weakly contractible category, then this is equivalent to the condition that the map $X \to 1$ to the terminal presheaf is a weak equivalence of $\mathcal{C}$-sets.

A **weak test category** is a small category $\mathcal{C}$ such that, 
for any category $D$ in $Cat$ which has a [[terminal object]], the $\mathcal{C}$-set $i_{\mathcal{C}}^\ast(D)$ is aspherical.

A **test category** is any small category $\mathcal{A}$ such that 

* ($\mathcal{A}$ is aspherical) its ([[geometric realization]] of the) [[nerve]] ("[[classifying space]]") $\vert \mathcal{A}\vert $ is [[contractible space|contractible]]

* ($\mathcal{A}$ is a "local test category") for every [[object]] $a$ in $\mathcal{A}$ require the [[overcategory]] $\mathcal{A}/a$ to be a weak test category. Thus for each $a \in \mathcal{A}$ and any category $D$ with a terminal object, we require that $B(i_{\mathcal{A}/a}(i_{\mathcal{A}/a}^\ast(D)))$ be a weakly contractible simplicial set.

A **strict test category** is a test category $\mathcal{A}$ such that

* $i_{\mathcal{A}} : \mathcal{A}Set \to Cat$ preserves [[finite products]] up to weak equivalence, 

or equivalently, such that

* the induced functor $i_{\mathcal{A}*}:Ho(\mathcal{A}Set)\to Ho(Cat)$ preserves finite products.

=--

+-- {: .num_remark}
###### Remark

One can show that a small category $\mathcal{C}$ is a weak test category if and only if both the unit $\epsilon : i_{\mathcal{C}}i_{\mathcal{C}}^*\to Id_{Cat}$ and the co-unit $\eta : Id_{\mathcal{C}Set/X}\to i^*_{\mathcal{C}}i_{\mathcal{C}}$ are weak equivalence; see Lemme 1.3.8 and Proposition 1.3.9 in ([Maltsiniotis](#Maltsin05)). In particular, one then has an equivalence of categories
$$Ho(\mathcal{C}Set)\cong Ho(Cat)\, .$$

An example of weak test category which is not a test category is the category $\Delta_+$ (so that a presheaf on $\Delta_+$ is a [[semi-simplicial set]]). This comes from a more general family of examples studied in ([Cisinski, Maltsiniotis](#CisMal11)).

=--

## Properties

### Homotopy category

The [[homotopy category]] of a [[category of presheaves]] over a (weak) test category, as a [[category with weak equivalences]] is equivalent to the standard homotopy category of [[homotopy theory]]: that of the category of [[simplicial sets]]/[[topological spaces]] with weak equivalences being [[weak homotopy equivalences]].

In other words, presheaves over a (weak) test category are models for [[homotopy types]] of [[∞-groupoids]]. There is a relative analogue of this situation for local test categories (see below).

### Model category structure

The [[presheaf category]] over a test category with the above weak equivalences admits a [[model category]] structure: the [[model structure on presheaves over a test category]]. This is due to ([Cisinski](#Cisinski)) with further developments due to ([Jardine](#Jardine)). In fact the possibility of such model structures characterizes **local** test categories:

+-- {: .num_theorem}
###### Theorem

A small category $\mathcal{A}$ is a local test category if and only if the category of presheaves of sets on $\mathcal{A}$ is equipped with a [[model category]] structure whose cofibrations are the monomorphisms with the weak equivalences defined as above. Such a model category structure is always [[proper model category | proper]]. Furthermore, if $\mathcal{A}$ is a local test category, the assignment $X\mapsto (N(i_{\mathcal{A}}(X))\to N(\mathcal{A}))$ is a [[Quillen equivalence]]
$$\mathcal{A}Set\to SSet/N(\mathcal{A})$$
(where $SSet/\mathcal{C}$ is equipped with the sliced [[classical model structure on simplicial sets | Kan-Quillen model structure]]),
and thus induces equivalences of homotopy categories
$$Ho(\mathcal{A}Set)\cong Ho(Cat/\mathcal{A})\cong Ho(SSet/N(\mathcal{A}))\, .$$

=--

+-- {: .proof}
###### Proof
See Th&#233;or&#232;me 1.4.3 and Corollaire 4.2.18 in ([Cisinski](#Cisinski)) for the first and second assertion. The Quillen equivalence is a particular case of Proposition 4.4.28 in loc. cit. The properness of the model structure is a particular case of Th&#233;or&#232;me 4.4.30 in loc. cit.
=--

+-- {: .num_remark}
###### Remark

If $\mathcal{A}$ is a local test category, one can describe the model structure on $\mathcal{A}$-sets independently from the functor $i_\mathcal{A}$ as follows: it is the minimal [[Cisinski model structure]] such that any morphism between representable presheaves is a weak equivalence and such that any presheaf on $\mathcal{A}$ is canonically an homotopy colimit of representable presheaves. This is Proposition 6.4.26 in ([Cisinski](#Cisinski)).

=--

## Examples

Apart from the archetypical example of the [[simplex category]] we have the following

* The [[cube category]] is a test category ([Grothendieck](#Grothendieck), [Cisinski](#Cisinski)), however not a strict one ([Kan](#Kan)). (The corresponding [[model category]] is discussed at [[model structure on cubical sets]].=)

  The category of [[cubes]] equipped with [[connection on a cubical set]] is even a strict test category ([Maltsiniotis, 2008](#Maltsiniotis)).

* The [[Theta category]] and its [[groupoid]]-analog $\tilde \Theta$ are strict test categories ([Cisinski, Maltsiniotis](#CisMal11) and [Ara](#Ara)).

* The [[tree category]] $\Omega$ is a test category. This was proven in an unpublished note of Cisinski, and later appeared as [Ara, Cisinski, Moerdijk, 2019](#AraCisinskiMoerdijk).

* The [[cycle category]] of Connes is a local test category. The corresponding model structure models homotopy types over $K(\mathbb{Z},2)$; see paragraph 8.5.14 and Proposition 8.5.19 in ([Cisinski](#Cisinski)).

* Given a local test category $\mathcal{A}$ and a small category $\mathcal{C}$, the [[product]] $\mathcal{A}\times\mathcal{C}$ is a local test category. It is a test category if both $\mathcal{A}$ and $\mathcal{C}$ have weakly contractible nerves. This is a special case of a more general fact: if $\mathcal{A}$ is a local test category, for any a [[Grothendieck fibration]] $p:\mathcal{X}\to\mathcal{A}$ (with small fibers), the category $\mathcal{X}$ is a local test category. This follows from Corollaire 1.7.15, Exemple 3.2.2 and the dual version of Proposition 3.2.9 in ([Maltsiniotis, 2005](#Maltsin05)). In particular, given any presheaf of groups $G$ on a local test category $\mathcal{A}$, one gets a nice homotopy theory of representations of $G$; see Scholie 7.2.15 in [Cisinski](#Cisinski)).


Any small category $\mathcal{A}$ which is closed under finite products and which contains an interval is a strict test category (where an interval is an object $I$ equipped with two morphisms from the terminal object $d^e:*\to I$, $e=0,1$, such that there is no maps from an object of $\mathcal{A}$ which factors through both $d^0$ and $d^1$); see Corollaire 1.5.7 in ([Maltsiniotis](#Maltsin05)). Particular cases include the following examples.

* The category of non-empty finite sets is a strict test category (hence [[symmetric simplicial sets]] are a model of homotopy types of CW-complexes). 

* The full subcategory of the category of topological spaces, whose objects are closed balls in euclidian spaces, is a strict test category.

* The category of open balls in euclidian spaces, with $C^\infty$-maps as morphisms, is a strict test category.

* The category of contractible [[Stein manifold | Stein manifolds]], with holomorphic maps as morphisms, is a strict test category.

## Related concepts

* [[direct category]]

* [[basic localizer]]

* [[test topos]]

## References


The notion of test category was introduced in 

* {#Grothendieck83} [[Alexandre Grothendieck]], _[[Pursuing Stacks]]_, 1983 ([djvu](http://people.math.jussieu.fr/~maltsin/groth/ps/Pursuing_Stacks.djvu))
 

Various conjectures made there are proven in 

* {#Cisinski} [[Denis-Charles Cisinski]], _Les pr&#233;faisceaux comme mod&#232;les des types d'homotopie_, Asterisque __308__, [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf). 

which moreover develops the main toolset and establishes the [[model structure on presheaves over a test category]].


General surveys include

* {#Maltsin05} [[Georges Maltsiniotis]], _La th&#233;orie de l'homotopie de Grothendieck_, Ast&#233;risque, 301, pp. 1-140, (2005) (see
[html](http://people.math.jussieu.fr/~maltsin/textes.html))


* [[J. F. Jardine]], _Categorical homotopy theory_, Homot. Homol. Appl. __8__ (1), 2006, pp.71&#8211;144, ([HHA](http://www.intlpress.com/HHA/v8/n1/a3/),  [pdf](http://www.intlpress.com/HHA/v8/n1/a3/v8n1a3.pdf))

That the [[cube category]] is a test category is asserted without proof in  ([Grothendieck](#Grothendieck)). A proof is spelled out in ([Cisinski](#Cisinski))


That it is not a strict test category is implicitly already in 

* {#Kan} [[Dan Kan]], _Abstract homotopy. I_ , Proc. Nat. Acad. Sci. U.S.A. 41 (1955), 1092&#8211;1096. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC528202/pdf/pnas00727-0082.pdf))


and led to the preference for [[simplicial sets]] over [[cubical sets]].

That the category of [[cubes]] _equipped with [[connection on a cubical set]]_ forms a _strict_ test category is shown in

* [[Georges Maltsiniotis]], _La cat&#233;gorie cubique avec connexions est une cat&#233;gorie test stricte_ . (French. English summary) Homology, Homotopy Appl. 11 (2009), no. 2, 309&#8211;326. ([web](http://www.intlpress.com/HHA/v11/n2/a15/))
 {#Maltsiniotis}

The test category nature of the groupoidal [[Theta category]] is discussed in 

* {#Ara} [[Dimitri Ara]], _The groupoidal analogue $\tilde \Theta$ to Joyal's category $\Theta$ is a test category_ ([arXiv:1012.4319](http://arxiv.org/abs/1012.4319)) 

and the [[Theta category]] itself is discussed in

* [[Denis-Charles Cisinski]], [[Georges Maltsiniotis]], _La cat&#233;gorie $\Theta$ de Joyal est une cat&#233;gorie test_ , JPAA **215** no.5 (2011) pp.962-982. ([pdf](http://webusers.imj-prg.fr/~georges.maltsiniotis/ps/theta.pdf), in French)
{#CisMal11}

That fact that the [[tree category]] is a test category was proved in 

* {#AraCisinskiMoerdijk} [[Dimitri Ara]], [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _The dendroidal category is a test category_, Mathematical Proceedings of the Cambridge Philosophical Society, 167(1), 107-121, 2019, ([doi:10.1017/S030500411800021X](https://doi.org/10.1017/S030500411800021X), [arXiv:1703.07098](http://arxiv.org/abs/1703.07098)).

A short introduction can be found in

* [[Chris Kapulkin]], _Introduction to Test Categories_ [PDF](http://www.math.uwo.ca/faculty/kapulkin/notes/test_categories.pdf).

[[!redirects test categories]]
[[!redirects strict test category]]
[[!redirects strict test categories]]
[[!redirects weak test category]]
[[!redirects weak test categories]]
[[!redirects Grothendieck homotopy theory]]