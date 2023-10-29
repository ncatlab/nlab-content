
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Compact objects
+-- {: .hide}
[[!include compact object - contents]]
=--
=--
=--


# Contents
* table of contents
{:toc}

## Idea

A _locally presentable category_ is a [[category]] which contains a [[small set]] $S$ of [[small objects]] such that every [[object]] is a nice [[colimit]] over objects in this set. 

This says equivalently that a locally presentable category $\mathcal{C}$ is a [[reflective localization]] $\mathcal{C} \hookrightarrow PSh(S)$ of a [[category of presheaves]] over $S$. Since here $PSh(S)$ is the [[free colimit completion]] of $S$ and the localization imposes _relations_, this is a presentation of $\mathcal{C}$ by _[[generators and relations]]_, hence the name _(locally) presentable category_.

See also at _[[locally presentable categories - introduction]]_.

## Definition

There are many equivalent characterizations of _locally presentable categories_.  The following is one of the most intuitive, equivalent characterizations are discussed [below](#EquivalentCharacterizations).


+-- {: .num_defn #PresentableCategory}
###### Definition 
**(locally presentable category)**

A [[category]] $\mathcal{C}$ is called **locally presentable** if

1. it is an [[accessible category]];

1. it has all small [[colimits]]. 

This means

1. $\mathcal{C}$ is a [[locally small category]];

1. $\mathcal{C}$ has all small [[colimits]];

1. there exists a [[small set]] $S \hookrightarrow Obj(\mathcal{C})$ of $\lambda$-[[compact]] objects that generates $\mathcal{C}$ under $\lambda$-[[filtered colimits]] for some [[regular cardinal]] $\lambda$.

=--

+-- {: .num_remark}
###### Remark

If follows that every [[object]] in a locally presentable category is a [[small object]].

=--

\begin{remark}
\label{Terminology}
The _locally_ in _locally presentable category_ refers to the fact that it is the _[[objects]]_ of (in) the category that are presentable, not the category as such (which is itself an [[object]] of [[Cat]]). This permits the distinction between, for instance, locally presentable categories, and [[finitely presentable objects]] of [[Cat]], which could be called "finitely presentable categories". In practice, however, it is common to drop "locally" from "locally presentable category" without modifying the meaning.
\end{remark}


+-- {: .num_remark}
###### Remark

Since a [[small object]] is one which is $\kappa$-[[compact object|compact]] for some $\kappa$, and any $\kappa$-compact object is also $\lambda$-compact for any $\lambda \gt \kappa$, it follows that there exists some $\kappa$ such that every object of the colimit-generating set $S$ is $\kappa$-compact.  

=--

This provides a "stratification" of the class of locally presentable categories, as follows.

+-- {: .num_defn}
###### Definition 
**(locally $\kappa$-presentable category)**

For $\kappa$ a [[regular cardinal]], a **locally $\kappa$-presentable category** is a locally presentable category, def. \ref{PresentableCategory}, such that the colimit-generating set $S$ may be taken to consist of $\kappa$-compact objects.

=--

+-- {: .num_remark}
###### Remark

Thus, a locally presentable category is one which is locally $\kappa$-presentable for _some_ [[regular cardinal]] $\kappa$ (hence also for every $\lambda\gt\kappa$).  In fact, in this case the fourth condition is redundant; once we know that there is a colimit-generating set consisting of $\kappa$-compact objects, it follows automatically that every object is $\lambda$-compact for some $\lambda$ (though there is no uniform upper bound on the required size of $\lambda$).  Moreover, colimit-generation is also stronger than necessary; it suffices to have a [[strong generator]] consisting of small objects.

=--

+-- {: .num_defn #LocallyFinitelyPresentable}
###### Definition 

A locally ${\aleph}_0$-presentable category is called a 
**[[locally finitely presentable category]]**.

=--





## Properties
 {#Properties}

### Equivalent characterizations
 {#EquivalentCharacterizations}

There are various equivalent characterizations of locally presentable categories.

#### As limit-preserving functor categories

+-- {: .num_prop}
###### Proposition 
**(as limit sketches)**

Locally presentable categories are precisely the categories of [[sketch|models of limit-sketches]].

=--

This is [Adámek & Rosický (1994), corollary 1.52](#AdámekRosický94).

Restricted to locally finitely presentable categories this becomes:

+-- {: .num_prop} 
###### Proposition 

Locally finitely presentable categories, def. \ref{LocallyFinitelyPresentable}, are equivalently the categories of 
[[finite limit]] preserving functors $C \to Set$, for small finitely complete categories $C$. 

=--

For the more detailed statement see below at _[Gabriel-Ulmer duality](#GabrielUlmerDuality)_. Equivalently this says that:

+-- {: .num_remark} 
###### Remark

Locally finitely presentable categories 
are equivalently [[models]] of finitary [[essentially algebraic theories]].
 
=--

#### As localizations of presheaf categories
 {#AsLocalizationsOfPresheafCategories}

+-- {: .num_prop #AsLocalizationOfPresheafCategories}
###### Proposition 
**(as accessible reflective subcategories of presheaves)**

Locally presentable categories are precisely the [[accessible functor|accessibly embedded]] full [[reflective subcategories]] 

$$
  (L \dashv i) 
  :
  C \stackrel{\overset{L}{\leftarrow}}{\underset{i}{\hookrightarrow}}
  PSh(K)
$$

of [[categories of presheaves]] on some small category $K$.

=--


This appears as [Adámek & Rosický (1994), prop 1.46](#AdámekRosický94).

+-- {: .num_remark}
###### Remark

Here _accessibly embedded_ means that $C \hookrightarrow Psh(K)$ is an [[accessible functor]],  which in turn means that $C$ is closed in $Psh(K)$ under $\kappa$-[[filtered colimits]] for some [[regular cardinal]] $\kappa$.

=--

See also at _[[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]_.

+-- {: .num_cor}
###### Corollary

Locally presentable categories are [[complete category|complete]].

=--

+-- {: .proof}
###### Proof

A reflective subcategory of a complete category is complete, since [[monadic functor|monadic functors]] reflect limits, and the above proposition shows that any locally presentable category is a reflective subcategory of a presheaf category, which is complete. 

=--


### Finite presentability and Gabriel--Ulmer duality 
 {#GabrielUlmerDuality}

+-- {: .num_defn} 
###### Definition

Write $Lex$ for the [[2-category]] of [[small categories]] with [[finite limits]], with finitely continuous (i.e., finite limit preserving) [[functors]] between them, and [[natural transformations]] between those. 

Write $LFP$ for the [[2-category]] of locally finitely presentable categories, def. \ref{LocallyFinitelyPresentable}, [[right adjoint]] functors which preserve [[filtered colimits]], and natural transformations between them. 

=--

+-- {: .num_prop} 
###### Theorem 
**([[Gabriel-Ulmer duality]])**

There is an [[equivalence of 2-categories]]

$$
  Lex^{op} \stackrel{\simeq}{\to} LFP
$$ 

$$
  C \mapsto Lex(C,Set)
$$

which sends a finitely complete category $C$ to the category of [[models]] of $C$, i.e., the category of [[left exact functors]] $C \to $ [[Set]]. 

=-- 




### Well-poweredness and well-copoweredness

* Every [[locally presentable category]] is well-powered, since it is a full reflective subcategory of a presheaf topos, so its subobject lattices are subsets of those of the latter.

* Every locally presentable category is also well-*copowered*.  This is shown in [Adámek & Rosický (1994), Prop. 1.57 & Thm. 2.49](#AdámekRosický94).


## Examples and applications

### Locally finitely presentable categories

We list examples of locally finitely presentable categories, def. \ref{LocallyFinitelyPresentable}.


+-- {: .num_example }
###### Example

The category [[Set]] of [[sets]] is locally finitely presentable.

For notice that every [[set]] is the [[directed colimit]] over the [[poset]] of all its [[finite set|finite]] [[subsets]].

Moreover, a set $S \in Set$ is a $\kappa$-[[compact object]] precisely if it has cardinality $|S| \lt \kappa$. So all finite sets are [[aleph|$\aleph_0$]]-compact. 

Hence a a set of generators that exhibits $Set$ as a locally finitely complete category is given by the set containing one finite set of [[cardinality]] $n \in \mathbb{N}$ for all $n$.

=--

+-- {: .num_example }
###### Example

More generally, for $C$ any [[small category]] the [[category of presheaves]] $Set^C$ is locally finitely presentable. 

This follows with [[Gabriel-Ulmer duality]]: 
the [[lex completion|finite limit completion]] of $C$, $Lex(C)$, is also small, and $Set^C$ is [[equivalence of categories|equivalent]] to the category of finitely continuous functors $Lex(C) \to Set$. 

=--

+-- {: .num_example }
###### Example

More generally still, if $A$ is locally finitely presentable and $C$ is [[small category|small]], then $A^C$ is locally finitely presentable. 

To see this, embed $A$ as a [[accessible functor|finitely-accessible]] [[reflective subcategory]] of a [[presheaf topos]] $Set^B$, and then note that by [[2-functor|2-functoriality]] of $(-)^C$ we get $A^C$ as a finitely-accessible reflective subcategory of $Set^{B \times C}$.

=--

+-- {: .num_example }
###### Example

The category of [[algebra over a Lawvere theory|algebras of]] a [[Lawvere theory]], for example [[Grp]], is locally finitely presentable. A $T$-algebra $A$ is finitely presented if and only if the [[hom-functor]] $Alg_T(A, -)$ preserves [[filtered colimits]], and any $T$-[[algebra over an algebraic theory|algebra]] can be expressed as a filtered colimit of finitely presented algebras. 

=--

\begin{example}
The category of [[coalgebras]] over a [[field]] $k$ is locally finitely presentable; similarly the category of commutative coalgebras over $k$ is locally finitely presentable. 
\end{example}

\begin{example}
A [[poset]], regarded as a category, is locally finitely presentable if it is a complete [[lattice]] which is [[algebraic lattice|algebraic]] (each element is a directed [[join]] of finite elements).
\end{example}

\begin{remark}
**([[counter-examples]])**

* The category [[FinSet]] of _[[finite set|finite]]_ sets is *not* locally finitely presentable, as it does not have all countable colimits.

* The category of [[fields]] and field [[homomorphisms]] is *not* locally presentable, as it does not have all binary coproducts (for instance, there are none between fields of differing characteristics).

* [[TopologicalSpaces]] is not locally finitely presentable.

* The [[opposite category]] of a locally presentable category (in particular, a locally finitely presentable category) is _never_ locally presentable, unless it is a poset.  This is  [Gabriel-Ulmer, Satz 7.13](#GabrielUlmer).

\end{remark}


### Locally presentable categories

+-- {: .num_example }
###### Example

A [[poset]], considered as a category, is locally presentable precisely if it is a complete [[lattice]]. 

=--

\begin{example}\label{GrothAbCatsAreLocPresntbl}
Every [[Grothendieck abelian category]] is locally presentable &lbrack;[Beke (200), Prop. 3.10](#Beke00), cf. [Krause (2015), Cor. 5.2](#Krause15)&rbrack;.

This implies in particular (by [this example](Grothendieck+category#ChainComplexesInGrothAbCat) at *[[Grothendieck abelian category]]*) that for $R$ a [[commutative ring]] ([[internalization|internal]] to any [[Grothendieck topos]]):

* the category $R$[[Mod]] of $R$-[[modules]] is locally presentable

* the category [[category of chain complexes|$Ch_\bullet(R Mod)$]] of [[chain complexes]] is locally presentable.

\end{example}

+-- {: .num_example }
###### Example

The following three examples, being [[presheaf categories]], are locally finitely presentable, thus _a fortiori_ locally presentable. They are important for the general study of [[(∞,1)-categories]]. 

* the category [[sSet]] of [[simplicial sets]];

* the category [[dSet]] of [[dendroidal sets]].

* for $C$ a [[small category]] the [[functor category]] $Funct(C,sSet)$ of [[simplicial presheaves]]

  (see Prop. \ref{PresheavesWithValuesInLocPresAreLocPres} below). 

=--

More generally, 

+-- {: .num_prop}
###### Proposition

Every [[sheaf topos]] is locally presentable. 

=--

This appears for instance as ([Borceux, prop. 3.4.16, page 220](#Borceux)). It follows directly with prop. \ref{AsLocalizationOfPresheafCategories} and using that every [[sheaf topos]] is an  accessibly embedded [[subtopos]] of a [[presheaf topos]] (see at _[[sheaf toposes are equivalently the left exact reflective subcategories of presheaf toposes]]_)

The main ingredient of a direct proof is:

+-- {: .num_prop}
###### Proposition

For $C$ a [[site]] and $\kappa$ a [[regular cardinal]] strictly larger than the [[cardinality]] of $Mor(C)$, every $\kappa$-[[filtered colimit]] in the [[sheaf topos]] $Sh(C)$ is computed objectwise.

=--

This implies that all [[representable functor|representables]] in a [[sheaf topos]] are $\kappa$-[[compact objects]]. 



+-- {: .num_theorem #AlgebrasOverAnAccessibleMonad}
###### Theorem

If $T$ is an [[accessible monad]] (a [[monad]] whose underlying [[functor]] is an [[accessible functor]]) on a locally presentable category $A$, then the category $A^T$ of [[algebras over a monad|algebras over the monad]] is locally presentable. In particular, if $A$ is locally presentable and $i: B \to A$ is a [[reflective subcategory]], then $B$ is locally presentable if $i$ is accessible.  
=--

This appears in [Adámek & Rosický (1994), 2.78](#AdámekRosický94).

+-- {: .query} 
This is actually somewhat subtle and gets into some transfinite combinatorics, from what I can gather. 
=--


\begin{proposition}
\label{PresheavesWithValuesInLocPresAreLocPres}
Given

* $\mathcal{C}$ a [[small category]],

* $\mathcal{A}$ a locally presentable category

then also the [[functor category]] $Func(\mathcal{C}, \mathcal{A})$ is locally presentable.
\end{proposition}
This is [Adámek & Rosický (1994), Cor. 1.54](#AdámekRosický94)

See at _[Functor category -- Local presentability](http://ncatlab.org/nlab/show/functor+category#LocalPresentability)_ for more.

\begin{proposition}
A [[slice category]] of a locally presentable category
is again locally presentable.

\end{proposition}
This appears for instance as [Centazzo-Rosick&#253;-Vitale, remark 3](#CentazzoRosickyVitale).

\begin{proposition}
\label{LocallyPresentableGrothendieckConstruction}
**(locally presentable Grothendieck constructions)**
\linebreak
Given a [[pseudofunctor]] with values in [[CatAdj|$Cat_{Adj}$]] as
$$
  \array{
    \mathllap{
      \mathbf{C} \,\colon\,
      \;
    }
    Base &\longrightarrow& Cat
    \\
    \mathcal{X} &\mapsto& \mathbf{C}_{\mathcal{X}}
    \\
    \Big\downarrow\mathrlap{{}^{f}}
    &&
    \mathllap{^{f^\ast}}\Big\uparrow
    \Big\downarrow\mathrlap{{}^{f_!}}
    \\
    \mathcal{Y} &\mapsto& \mathbf{C}_{\mathcal{Y}}
  }
$$
such that for some [[regular cardinal]] $\kappa$

1. $Base$ is locally $\kappa$-presentable,

1. each $\mathbf{C}_{\mathcal{X}}$ is locally presentable,

1. $\mathbf{C}_{(-)}$ [[preserved colimit|preserves]] [[filtered colimit|$\kappa$-filtered]] [[2-limits]]

then also the [[Grothendieck construction]] $\int \mathbf{C}$ is locally presentable.
\end{proposition}
This follows, as explained in [MO:a/102083](https://mathoverflow.net/a/102083/381) from the analogous statement for [[accessible category|accessibility]] which appears as 
[Makkai & Paré (1989), Prop. 5.3.1. (4)](accessible+category#MakkaiParé1989).


### Combinatorial model categories

A [[combinatorial model category]] is a [[model category]] that is in particular a locally presentable category.


### Orthogonal subcategory problem

Given a class of morphisms $\Sigma$ in a locally presentable category, the answer to the [[orthogonal subcategory problem]] for $\Sigma^\perp$ is affirmative if $\Sigma$ is small, and is affirmative for any class $\Sigma$ assuming the large cardinal axiom known as [[Vopenka's principle]]. 


## Related concepts

* [[PrCat]], [[Pr(∞,1)Cat]], [[Ho(CombModCat)]]

* Another notion of "presentable category" is that of an _[[equationally presentable category]]_.

* Locally presentable categories are a special case of _[[locally bounded category|locally bounded categories]]_.

* [[class-locally presentable category]]

* [[locally strongly finitely presentable category]]

[[!include locally presentable categories - table]]


## References 

### General

The definition is due to

* {#GabrielUlmer} [[Pierre Gabriel]], [[Friedrich Ulmer]], *Lokal präsentierbare Kategorien*, Springer LNM **221** (1971) &lbrack;[doi:10.1007/BFb0059396](https://doi.org/10.1007/BFb0059396), [MR0327863](http://www.ams.org/mathscinet-getitem?mr=0327863)&rbrack;

Textbook account:

* {#AdámekRosický94} [[Jiří Adámek]], [[Jiří Rosický]], *[[Locally presentable and accessible categories]]*, London Mathematical Society Lecture Note Series **189**, Cambridge University Press (1994) &lbrack;[doi:10.1017/CBO9780511600579](https://doi.org/10.1017/CBO9780511600579)&rbrack;

Review for the case of [[locally finitely presentable categories]]:

* [[Maru Sarazola]], *An introduction to locally finitely presentable categories* (2017) &lbrack;[pdf](https://pi.math.cornell.edu/~maru/documents/locally_finitely_presentable_cats.pdf), [[Sarazola_LocallyPresentableCategories.pdf:file]]&rbrack;


See also:


* {#CentazzoRosickyVitale} C. Centazzo, [[Jiří Rosický]], [[Enrico Vitale]], _A characterization of locally $\mathbb{D}$-presentable categories_ ([pdf](http://perso.uclouvain.be/enrico.vitale/ClaudiaJiri.pdf))


* {#Borceux} [[Francis Borceux]], _[[Handbook of Categorical Algebra]]: III Categories of Sheaves_ (proposition 3.4.16), page 220. 


* {#Lurie} [[Jacob Lurie]], A.1.1 of: _[[Higher Topos Theory]]_

  > (where locally presentable categories are called [[presentable categories]]*)

On the example of [[Grothendieck abelian categories]]:

* {#Beke00} [[Tibor Beke]], *Sheafifiable homotopy model categories*, Math. Proc. Cambridge Philosophical Society **129** 3 (2000) 447-475 &lbrack;[arXiv:math/0102087](https://arxiv.org/abs/math/0102087), [doi:10.1017/S0305004100004722](https://doi.org/10.1017/S0305004100004722)&rbrack;

* {#Bird82} [[Greg Bird]], _Limits in 2-Categories of Locally-Presentable Categories [pdf](http://maths.mq.edu.au/~street/BirdPhD.pdf)&rbrack;

* {#Krause15} [[Henning Krause]], _Deriving Auslander's formula_, Documenta Math. **20** (2015) 669-688 &lbrack;[arXiv:1409.7051](https://arxiv.org/abs/1409.7051)&rbrack;


### In enriched category theory
 {#ReferencesInEnrichedCategoryTheory}

Discussion of local presentability in [[enriched category theory]] (see also [references on enriched accessible categories](accessible+category#ReferencesInEnrichedCategoryTheory)):

* {#Kelly82} [[G. Max Kelly]], *Structures defined by finite limits in the enriched context, I*, Cahiers de topologie et géométrie différentielle **23** 1 (1982)  3-42 &lbrack;[numdam:CTGDC_1982__23_1_3_0](http://archive.numdam.org/item/CTGDC_1982__23_1_3_0)&rbrack;

See also:

* [MO:q/53470](https://mathoverflow.net/q/53470/381): *Enriched locally presentable categories*


[[!redirects locally presentable]]
[[!redirects locally presentable category]]
[[!redirects locally presentable categories]]
[[!redirects presentable category]]
[[!redirects presentable categories]]
[[!redirects locally representable category]]



