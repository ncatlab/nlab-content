
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

1. there exists a [[small set]] $S \hookrightarrow Obj(\mathcal{C})$ of $\lambda$-small [[objects]] that generates $\mathcal{C}$ under $\lambda$-filtered colimits for some regular cardinal $\lambda$.

   (meaning that every object of $\mathcal{C}$ may be written as a colimit over a [[diagram]] with objects in $S$); 

1. every object in $\mathcal{C}$ is a [[small object]] (assuming 3, this is equivalent to the assertion that every object in $S$ is small).

=--

+-- {: .num_remark}
###### Remark

The _locally_ in _locally presentable category_ refers to the fact that it is the _objects_ that are presentable, not the category as such.

For instance, consider the notion of "locally finitely presentable category", def. \ref{LocallyFinitelyPresentable} below, in which the generating set $S$ consists of [[finitely presentable objects]], i.e. $\omega$-small ones. If one dropped the word "locally" then one would get the notion "[[finitely presentable category]]" which means something completely different, namely a [[finitely presentable object|finitely presentable]] ($\omega$-small) object of [[Cat]].

=--


+-- {: .num_remark}
###### Remark

Since a [[small object]] is one which is $\kappa$-[[compact object|compact]] for some $\kappa$, and any $\kappa$-compact object is also $\lambda$-compact for any $\lambda\gt\kappa$, it follows that there exists some $\kappa$ such that every object of the colimit-generating set $S$ is $\kappa$-compact.  

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

This is ([Adamek-Rosicky, corollary 1.52](#AdamekRosicky)).

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

of [[categories of presheaves]] on some category $K$.

=--


This appears as ([Ad&#225;mek-Rosick&#253;, prop 1.46](#AdamekRosicky)).

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

=---


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


### Stability of presentability under various operations

+-- {: .num_lemma }
###### Lemma

A [[slice category]] of a locally presentable category
is again locally presentable.

=--

This appears for instance as [Centazzo-Rosick&#253;-Vitale, remark 3](#CentazzoRosickyVitale).


+-- {: .num_theorem}
###### Theorem

If $A$ is locally presentable and $C$ is a [[small category]], then the [[functor category]] $A^C$ is locally presentable. 

=--

### Well-poweredness and well-copoweredness

* Every [[locally presentable category]] is well-powered, since it is a full reflective subcategory of a presheaf topos, so its subobject lattices are subsets of those of the latter.

* Every locally presentable category is also well-*copowered*.  This is shown in [Adamek-Rosicky, Proposition 1.57 and Theorem 2.49](#AdamekRosicky).


## Examples and applications

### Locally finitely presentable categories

We list examples of locally finitely presentable categories, def. \ref{LocallyFinitelyPresentable}.


+-- {: .num_example }
###### Example

The category [[Set]] of [[sets]] is locally finitely presentable.

For notice that every [[set]] is the [[directed colimit]] over the [[poset]] of all its [[finite set|finite]] [[subsets]].

Moreover, a set $S \in Set$ is a $\kappa$-[[compact object]] precisely if it has cardinality $|S| \lt \kappa$. So all finite sets are [[?]]$_0$-compact. 

Hence a a set of generators that exhibits $Set$ as a locally finitely complete category is given by the set containing one finite set of [[cardinality]] $n \in \mathbb{N}$ for all $n$.

=--

+-- {: .num_example }
###### Example

More generally, for $C$ any [[small category]] the [[category of presheaves]] $Set^C$ is locally finitely presentable if $C$ is small. 

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

+-- {: .num_example }
###### Example

The category of [[coalgebras]] over a [[field]] $k$ is locally finitely presentable; similarly the category of commutative coalgebras over $k$ is locally finitely presentable. 

=--

+-- {: .num_example }
###### Example


A [[poset]], regarded as a category, is locally finitely presentable if it is a complete [[lattice]] which is [[algebraic lattice|algebraic]] (each element is a directed [[join]] of finite elements).

=--

+-- {: .num_example}
###### Counterexamples

* The category [[FinSet]] of _finite_ sets is not locally finitely presentable, as it does not have all countable colimits.

* The category of fields and field homomorphisms is not locally presentable, as it does not have all binary coproducts (for instance, there are none between fields of differing characteristics).

* [[Top]] is not locally finitely presentable.

* The [[opposite category]] of a locally presentable category (in particular, a locally finitely presentable category) is _never_ locally presentable, unless it is a poset.  This is  [Gabriel-Ulmer, Satz 7.13](#GabrielUlmer).

=--


### Locally presentable categories

+-- {: .num_example }
###### Example

A [[poset]], considered as a category, is locally presentable precisely if it is a complete [[lattice]]. 

=--

+-- {: .num_example }
###### Example

The following three examples, being [[presheaf categories]], are locally finitely presentable, thus _a fortiori_ locally presentable. They are important for the general study of [[(∞,1)-categories]]. 

* the category [[sSet]] of [[simplicial sets]];

* the category [[dSet]] of [[dendroidal sets]].

* for $C$ a [[small category]] the [[functor category]] $Funct(C,sSet)$ of [[simplicial presheaves]]. 

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

This appears in ([Adamek-Rosicky, 2.78](#AdamekRosicky)).

+-- {: .query} 
This is actually somewhat subtle and gets into some transfinite combinatorics, from what I can gather. 
=--


### Combinatorial model categories

A [[combinatorial model category]] is a [[model category]] that is in particular a locally presentable category.


### Orthogonal subcategory problem

Given a class of morphisms $\Sigma$ in a locally presentable category, the answer to the [[orthogonal subcategory problem]] for $\Sigma^\perp$ is affirmative if $\Sigma$ is small, and is affirmative for any class $\Sigma$ assuming the large cardinal axiom known as [[Vopenka's principle]]. 

### Functor categories

See at _[Functor category -- Local presentability](http://ncatlab.org/nlab/show/functor+category#LocalPresentability)_.

## Related concepts

* [[PrCat]], [[Pr(∞,1)Cat]], [[Ho(CombModCat)]]

* Another notion of "presentable category" is that of an _[[equationally presentable category]]_.

* Locally presentable categories are a special case of _[[locally bounded category|locally bounded categories]]_.

* [[class-locally presentable category]]

[[!include locally presentable categories - table]]


## References 

The definition is due to

* {#GabrielUlmer} [[Pierre Gabriel]], [[Friedrich Ulmer]], _Lokal pr&#228;sentierbare Kategorien_, Springer LNM 221, 1971


The standard textbook is

* {#AdamekRosicky} [[Jiří Adámek]], [[Jiří Rosický]], _[[Locally presentable and accessible categories]]_, Cambridge University Press, (1994)
 


More details are in 

* {#CentazzoRosickyVitale} C. Centazzo, [[Jiří Rosický]], [[Enrico Vitale]], _A characterization of locally $\mathbb{D}$-presentable categories_ ([pdf](http://perso.uclouvain.be/enrico.vitale/ClaudiaJiri.pdf))


Some further discussion is in 

* {#Borceux} [[Francis Borceux]], _[[Handbook of Categorical Algebra]]: III Categories of Sheaves_ (proposition 3.4.16), page 220. 


See also section A.1.1 of 

* [[Jacob Lurie]], _[[Higher Topos Theory]]_

where locally presentable categories are called just [[presentable category|presentable categories]].


[[!redirects locally presentable]]
[[!redirects locally presentable category]]
[[!redirects locally presentable categories]]
[[!redirects presentable category]]
[[!redirects presentable categories]]
[[!redirects locally representable category]]