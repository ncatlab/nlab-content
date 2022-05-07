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

In the 1980-s, [[Grothendieck]] in _Pursuing Stacks_ introduced a notion of [[categories]] he called _test categories_ to make the variants of the [[homotopy theory]] based on the usage of combinatorial models with some kind of cell structure (e.g., [[simplicial set]]s, [[cubical set]]s and cellular sets) independent of a particular combinatorial model.

## Definition

Given any small category $\mathcal{C}$, one considers $\mathcal{C}$-sets, hence [[presheaves]] on $\mathcal{C}$, hence [[contravariant functors]] from $\mathcal{C}$ to $Set$. 

Given an [[object]] $c\in C$, one considers the [[representable functor]] $Hom_{\mathcal{C}}(-,c)=:\Delta^c$. If $X:\mathcal{C}^{op} \to Set$ is a $\mathcal{C}$-set, the elements of $X(c)$ are called the $c$-cells. By the [[Yoneda lemma]], they correspond to the [[natural transformations]] $\Delta^c\to X$. 

Let the **cell category** of $X$, denoted $i_{\mathcal{C}} X$, be the full subcategory of the [[overcategory]] $\mathcal{C}Set/X$ whose objects are the transformations of the form $\Delta^c\to X$. (This is another name for the [[category of elements]] of $X$.) The correspondence $X\mapsto i_{\mathcal{C}}X$ extends to a functor $i_{\mathcal{C}}:\mathcal{C}Set\to Cat$ which has a right adjoint $i_{\mathcal{C}}^*:Cat\to\mathcal{C}Set$ whose object part is given by the formula

$$ i_{\mathcal{C}}^*(D)(c):= Hom_{Cat}(\mathcal{C}/c,D).$$

Denote the counit of the adjunction $\epsilon : i_{\mathcal{C}}i_{\mathcal{C}}^*\to Id_{Cat}$. 

Two $\mathcal{C}$-sets $X$ and $Y$ are **weakly equivalent** if there is a map $f:X\to Y$ inducing an equivalence $f_* : i_{\mathcal{C}} X\to i_{\mathcal{C}} Y$ of their cell categories, i.e., the induced map of [[nerve]]s ("[[classifying spaces]]") $B(i_{\mathcal{C}} X)\to B(i_{\mathcal{C}} Y)$ is a weak equivalence of simplicial sets. The functor $i_{\mathcal{C}}:\mathcal{C}Set\to Cat$ induces a functor $i_{\mathcal{C}*}:Ho(\mathcal{C}Set)\to Ho(Cat)$ of the homotopy categories.  

A $\mathcal{C}$-set $X$ is called **aspherical** if the category $i_{\mathcal{C}}(X)$ is weakly contractible, i.e. the nerve $B(i_{\mathcal{C}}(X))$ is a weakly contractible simplicial set. Note that if $\mathcal{C}$ is a weakly contractible category, then this is equivalent to the condition that the map $X \to 1$ to the terminal presheaf is a weak equivalence of $\mathcal{C}$-sets.

A **weak test category** is a small category $\mathcal{C}$ such that, 
for any category $D$ in $Cat$ which has a terminal object, the $\mathcal{C}$-set $i_{\mathcal{C}}^\ast(D)$ is aspherical.

A **test category** is any small category $\mathcal{A}$ such that 

* ($\mathcal{A}$ is aspherical) its ([[geometric realization]] of the) [[nerve]] ("[[classifying space]]") $\vert \mathcal{A}\vert $ is [[contractible space|contractible]]

* ($\mathcal{A}$ is a "local test category") for every [[object]] $a$ in $\mathcal{A}$ require the [[overcategory]] $\mathcal{A}/a$ to be a weak test category. Thus for each $a \in \mathcal{A}$ and any category $D$ with a terminal object, we require that $B(i_{\mathcal{A}/a}(i_{\mathcal{A}/a}^\ast(D)))$ be a weakly contractible simplicial set.

A **strict test category** is a test category $\mathcal{A}$ such that

* $i_{\mathcal{C}} : \mathcal{C}Set \to Cat$ preserves [[finite products]] up to weak equivalence, 

or equivalently, such that

* the induced functor $i_{\mathcal{C}*}:Ho(\mathcal{C}Set)\to Ho(Cat)$ preserves finite products.

Then one proceeds with $\mathcal{A}$-sets.

If $\mathcal{A}$ is a test category and $\mathcal{C}$ any small category whose classifying space is contractible (which may or may not be a test category itself), then their cartesian [[product]] $\mathcal{A}\times\mathcal{C}$ is a test category. 

## Properties

### Homotopy category

The [[homotopy category]] of a [[category of presheaves]] over a test category, as a [[category with weak equivalences]] is equivalent to the standard homotopy category of [[homotopy theory]]: that of the category of [[simplicial sets]]/[[topological spaces]] with weak equivalences being [[weak homotopy equivalences]].

In other words, presheaves over a test category are models for [[homotopy types]] of [[∞-groupoids]].

### Model category structure

The [[presheaf category]] over a test category with the above weak equivalences admits a [[model category]] structure: the [[model structure on presheaves over a test category]]. This is due to ([Cisinski](#Cisinski)) with further developments due to ([Jardine](#Jardine)).

## Examples

Apart from the archeytpical example of the [[simplex category]] we have the following

* The [[cube category]] is a test category ([Grothendieck](#Grothendieck), [Cisinski](#Cisinski)), however not a strict one ([Kan](#Kan)). (The corresponding [[model category]] is discussed at [[model structure on cubical sets]].=)

  The category of [[cubes]] equipped with [[connection on a cubical set]] is even a strict test category ([Maltsiniotis, 2008](#Maltsiniotis)).

* The [[groupoid]]-analog $\tilde \Theta$ of the [[Theta category]] is a test category ([Ara](#Ara)).

* The [[tree category]] $\Omega$ is a test category. This was proven in an unpublished note of Cisinski, and later appeared as [Ara, Cisinski, Moerdijk, 2019](#AraCisinskiMoerdijk).

## Related concepts

* [[direct category]]

* [[basic localizer]]

* [[test topos]]

## References


The notion of test category was introduced in 

* [[Alexandre Grothendieck]], _[[Pursuing Stacks]]_, [djvu](http://people.math.jussieu.fr/~maltsin/groth/ps/Pursuing_Stacks.djvu)
 {#Grothendieck}

Various conjectures made there are proven in 

* {#Cisinksi} [[Denis-Charles Cisinski]], _Les pr&#233;faisceaux comme mod&#232;les des types d'homotopie_, Asterisque __308__, [pdf](http://www.math.univ-toulouse.fr/~dcisinsk/ast.pdf). 

which moreover develops the main toolset and establishes the [[model structure on presheaves over a test category]].


General surveys include

* [[Georges Maltsiniotis]], _La th&#233;orie de l'homotopie de Grothendieck_, Ast&#233;risque, 301, pp. 1-140, (2005) (see
[html](http://people.math.jussieu.fr/~maltsin/textes.html))


* [[Rick Jardine]], _Categorical homotopy theory_, Homot. Homol. Appl. __8__ (1), 2006, pp.71&#8211;144, ([HHA](http://www.intlpress.com/HHA/v8/n1/a3/),  [pdf](http://www.intlpress.com/HHA/v8/n1/a3/v8n1a3.pdf))

That the [[cube category]] is a test category is asserted without proof in  ([Grothendieck](#Grothendieck)). A proof is spelled out in ([Cisinski](#Cisinski))


That it is not a strict test category is implicitly already in 

* [[Dan Kan]], _Abstract homotopy. I_ , Proc. Nat. Acad. Sci. U.S.A. 41 (1955), 1092&#8211;1096. ([pdf](http://www.ncbi.nlm.nih.gov/pmc/articles/PMC528202/pdf/pnas00727-0082.pdf))
 {#Kan}

and led to the preference for [[simplicial sets]] over [[cubical sets]].

That the category of [[cubes]] _equipped with [[connection on a cubical set]]_ forms a _strict_ test category is shown in

* [[Georges Maltsiniotis]], _La cat&#233;gorie cubique avec connexions est une cat&#233;gorie test stricte_ . (French. English summary) Homology, Homotopy Appl. 11 (2009), no. 2, 309&#8211;326. ([web](http://www.intlpress.com/HHA/v11/n2/a15/))
 {#Maltsiniotis}

The test category nature of the groupoidal [[Theta category]] is discussed in 

* {#Ara} [[Dimitri Ara]], _The groupoidal analogue $\tilde \Theta$ to Joyal's category $\Theta$ is a test category_ ([arXiv:1012.4319](http://arxiv.org/abs/1012.4319)) 

That fact that the [[tree category]] is a test category was proved in 

* {#AraCisinskiMoerdijk} [[Dimitri Ara]], [[Denis-Charles Cisinski]], [[Ieke Moerdijk]], _The dendroidal category is a test category_, Mathematical Proceedings of the Cambridge Philosophical Society, 167(1), 107-121, 2019, ([doi:10.1017/S030500411800021X](https://doi.org/10.1017/S030500411800021X), [arXiv:1703.07098](http://arxiv.org/abs/1703.07098)).

A short introduction can be found in

* Chris Kapulkin, _Introduction to Test Categories_ [PDF](http://www.math.uwo.ca/faculty/kapulkin/notes/test_categories.pdf).

[[!redirects test categories]]
[[!redirects strict test category]]
[[!redirects strict test categories]]
[[!redirects weak test category]]
[[!redirects weak test categories]]
[[!redirects Grothendieck homotopy theory]]