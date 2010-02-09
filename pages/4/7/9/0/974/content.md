<div class="rightHandSide toc">
[[!include compact object - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Idea ##

A locally presentable category is one where every [[object]] is a [[colimit]] over a [[set]] of [[small object]]s.

## Definition ##

+-- {: .un_defn}
###### Definition (locally presentable category)

A [[category]] $C$ is called **locally presentable** if

* $C$ is [[locally small category]];

* it has all small [[colimit]]s;

* there exists a [[set]] $S$ (not a proper [[class]]) of [[object]]s that generates $C$ under colimits

  (every object may be written as a colimit over a diagram with objects in $S$)

* every object is a [[small object]].

=--

More specifically


+-- {: .un_defn}
###### Definition ($\kappa$-locally presentable category)

For $\kappa$ a [[cardinal number|regular cardinal]], a **locally $\kappa$-presentable category** is defined like a presentable category, only that every object is required to be a $\kappa$-[[compact object]].

=--

So a locally presentable category is one which is locally $\kappa$-presentable for some regular cardinal $\kappa$.

A locally $(\kappa = \aleph_0)$-presentable category is called a **locally finitely presentable category**.

### Equivalent definitions

There are various equivalent statements of this definition.

+-- {: .un_prop}
###### Proposition (as limit sketches)

Locally presentable categories are precisely the categories of [[sketch|models of limit-sketches]].

=--

+-- {: .proof}
###### Proof

This is theorem _xyz_ in _AdRo_ .

=--

This proposition extrapolates part of the Gabriel--Ulmer duality (see below), which concerns locally finitely presentable categories: 

+-- {: .un_prop} 

###### Proposition (as finite limit sketches) 

Every locally finitely presentable category $A$ is equivalent to the category of finite limit preserving functors $C \to Set$, for some small finitely complete category $C$. 

=--

### Gabriel--Ulmer duality 

Let $Lex$ denote the [[2-category]] of small finitely complete categories, finitely continuous (i.e., finite limit preserving) functors, and [[natural transformation]]s between them. 

Let $LFP$ denote the 2-category of locally presentable categories, [[right adjoint]] functors which preserve [[filtered colimit]]s, and natural transformations between them. 

+-- {: .un_prop} 

###### Theorem (Gabriel--Ulmer duality) 

There is a contravariant biequivalence 

$$Lex^{op} \sim LFP$$ 

which sends a finitely complete category $C$ to the category of models of $C$, i.e., the category of left exact functors $C \to Set$. 

=-- 

+--{.query} 

This deserves much further expansion, as it is a basic starting point for the more general study of locally presentable categories. 

=--

### Variations ###

*  The generalization of the concept to the context of [[(infinity,1)-category|(infinity,1)-categories]] is [[presentable (infinity,1)-category]].



### Terminology ###

The _locally_ in _locally presentable category_ refers to the fact that it is the _objects_ that are presentable, not the category as such:

(For instance, consider the notion of "locally finitely presentable category," in which the generating set $S$ consists of [[finitely presentable object]]s, i.e. $\omega$-small ones. If you drop the word "locally" then you would get "[[finitely presentable category]]" which means something completely different, namely a finitely presentable ($\omega$-small) object of [[Cat]].)

Another notion of "presentable category" is [[algebraic category|equationally presentable category]].


## Examples and applications ##

### Locally finitely presentable categories ###

The locally $\kappa$-presentable categories for $\kappa = \aleph_0$.

* [[Set]] is locally finitely presentable: 

  * as the set of generators take the set containing one finite set of cardinality $n \in \mathbb{N}$ for all $n$.

  * every [[set]] is the [[directed colimit]] over the [[poset]] of all its finite [[subset]]s.

  * a set $S \in Set$ is a $\kappa$-[[compact object]] precisely if it has cardinality $|S| \lt \kappa$. So all finite sets are $\aleph_0$-compact. 

* More generally, by Gabriel--Ulmer duality, $Set^C$ is locally finitely presentable if $C$ is small. For, the finite limit completion of $C$, $Lex(C)$, is also small, and $Set^C$ is equivalent to the category of finitely continuous functors $Lex(C) \to Set$. 

* More generally still, if $A$ is locally finitely presentable and $C$ is small, then $A^C$ is locally finitely presentable. 

+--{.query} 

Citation: paper by Lack and Power. Will follow up on this at some point. 

=--

* The category of algebras of a [[Lawvere theory]], for example [[Grp]], is locally finitely presentable. A $T$-algebra $A$ is finitely presented if and only if the hom-functor $Alg_T(A, -)$ preserves filtered colimits, and any $T$-algebra can be expressed as a filtered colimit of finitely presented algebras. 

+--{.query} 

This deserves to be expanded upon. 

=--

* The category of coalgebras over a field $k$ is locally finitely presentable; similarly the category of commutative coalgebras over $k$ is locally finitely presentable. 

* a [[poset]], regarded as a category, is locally finitely presentable if it is a complete [[lattice]] which is algebraic (each element is a directed [[join]] of finite elements).

+-- {: .un_exmple}
###### Counterexamples

* the category [[FinSet]] of _finite_ sets is not locally finitely presentable, as it does not have all countable colimits.

* [[Top]] is not locally finitely presentable.

* The opposite of a locally presentable category (in particular, a locally finitely presentable category) is _never_ locally presentable, unless it is a poset. 
=--

### Locally presentable categories

* A [[poset]], considered as a category, is locally presentable precisely if it is a complete [[lattice]]. 

The following three examples, being presheaf categories, are locally finitely presentable, thus _a fortiori_ locally presentable. They are important for the general study of $(\infty, 1)$-categories. 

* the category [[SSet]] of [[simplicial set]]s;

* the category $dSet$ of [[dendroidal set]]s.

* for $C$ a [[small category]] the [[functor category]] $Funct(C,SSet)$ of [[simplicial presheaf|simplicial presheaves]]. 

More generally, we have the following stability theorems: 

* If $A$ is locally presentable and $C$ is small, then $A^C$ is locally presentable. 

* If $T$ is an accessible monad (a monad whose underlying functor is an [[accessible category|accessible functor]]) on a locally presentable category $A$, then the category of algebras $A^T$ is locally presentable. In particular, if $A$ is locally presentable and $i: B \to A$ is a reflective subcategory, then $B$ is locally presentable if $i$ is accessible.  

+--{.query} 

This is actually somewhat subtle and gets into some transfinite combinatorics, from what I can gather. 

=--

### Combinatorial model categories ###

A [[combinatorial model category]] is a [[model category]] that is in particular a locally presentable category.



## References ##

The definition is due to

* P. Gabriel and F. Ulmer (1971)

The standard textbook is

* **AdRo** Jiri Adamek, Jiri Rosicky, _Locally presentable and accessible categories_

See also section A.1.1 of 

* [[Jacob Lurie]], [[Higher Topos Theory]]

where locally presentable categories are called just [[presentable category|presentable categories]].


## Discussion ##

A previous version of this entry led to the following discussion.

+-- {: .query}
Do you mean __*locally* presentable__?  Or are you following Lurie now?  Should we change the terminology below?

[[Urs Schreiber]]: oh, sorry, this is a result of bad copy-and-pasting, I had meant to type locally presentable -- but now that we are discussing this, maybe we can sort this out: what's the point of saying "locally" presentable? Which reasons would there be not to follow Lurie on this? 

_Toby_:  The only thing that I can think of offhand is to distinguish from [[algebraic category|equationally presentable category]].  (Actually, what I really mean is that if I Google `"presentable category"`, then I mostly get hits with 'locally' in them, and if I Google `"presentable category" -locally`, then I mostly get hits with 'equationally' in them.)

[[Urs Schreiber]]: I have changed the wording in the first sentence now.

I guess the point remains that "locally presentable category" serves to distinguish from "equationally presentable category".

On the other hand, _locally_ presentable then still seems like a bad choice of terminology, as it indicates nothing about the kind of presentation and in fact it remains a mystery to me what is supposed to be local about the above notion. (It's not the local smallness, or is it?) 

But then it gets a bit worse even when we look at the generalizations. I have firmly followed Lurie with the terminology at [[presentable (infinity,1)-category]] that is supposed to generalize the notion here, and there it turns out to be pretty good terminology, as those $(\infty,1)$-categories are, among a whole list of equivalent characterizations, precisely those that are given by combinatorial simplicial model categories. I have used that nice fact to consistently say "a model category [[presentable (infinity,1)-category|presents]] an $(\infty,1)$-category" with the "presents" linking to _presentable $(\infty,1)$-category_ .

[[Mike Shulman]]: Coming into this discussion late, let me speak up in favor of "locally presentable."  I agree that "locally" is a poor choice (and an overworked word), but I think that merely "presentable" is worse; some adjective must be used and "locally" has the weight of history behind it.  The important point requiring the adjective is that it is the _objects_ of the category which are presentable, rather than the category itself.  For instance, consider the notion of "locally _finitely_ presentable category," in which the generating set $S$ consists of finitely presentable objects, i.e. $\omega$-small ones.  If you drop the word "locally" then you would get "finitely presentable category" which means something completely different, namely an $\omega$-small object of [[Cat]].

I'm guessing that when you say "presentable category" you are thinking of the set $S$ as "presenting" the category in some way, but I think this is wrong.  The notion of "presentable object" has a precise meaning in the very theory we are discussing, so we shouldn't apply it unqualified to the category as well with a different meaning.

_Reid Barton_: I don't find these arguments very convincing.  First, local presentability is not something that can be checked objectwise, even once the category is assumed to be cocomplete.  For example, take the large poset of all sets (or elements of a fixed universe), ordered by inclusion.  This category is cocomplete, and every object is $\kappa$-presentable where $\kappa$ is its cardinality as a set, but it is not locally presentable: it has no terminal object.

Secondly, and less pathologically, the name "locally finitely presentable" makes no sense at all from this point of view.  The category of groups is locally finitely presentable even though most of its objects are not finitely presentable.  It is only the category as a whole which is finitely presentable in the sense of being specified by a finite amount of data (the localization of presheaves on a finite category at finitely many morphisms).

Finally, locally presentable categories should be viewed as a full sub-2-category not of Cat but of cocomplete categories and colimit-preserving functors.  A presentation of a category as the localization of a presheaf category at a set of maps is exactly the data you need to compute Hom out of it in this 2-category.  I have not worked out the details, but it seems that local presentability should be closely related to presentability in this setting.

[[Mike Shulman]]: When I said "the objects are presentable" I didn't mean that as a *definition*, just as a fact which is true about locally presentable categories and may help to get intuition for the choice of terminology.  I agree that "locally" is not the best choice of word, but I think *some* word has to be used, because saying "finitely presentable" to mean "locally finitely presentable" is even worse.  A *finitely presentable category* means a finitely presentable object of Cat, i.e. a category which is a quotient of a finite directed graph by finitely many relations.  That is an important notion, and "finitely presentable category" is the completely natural term for it, in line with all sorts of universal algebra and even with the theory of locally presentable categories.

If the term under discussion was "presentable cocomplete categories," then I would find your arguments more convincing.  A presentable category should mean a presentable object of $Cat$; I think if you want to talk about presentable objects of $CocpltCat$, then the terminology should indicate it.  Not all categories are cocomplete.

But also, I don't think a locally finitely presentable category is necessarily a presentable object of $CocpltCat$ in the categorical sense.  Let $D$ be any small [[directed set]], for any $x\in D$ let $D/x = \{ y\in D | y \le x \}$, and consider the $D$-indexed diagram $x\mapsto [{(D/x)^\op},Set]$ in $CocpltCat$, with transitions induced by the inclusions.  Now its colimit, $E$ say, contains a canonical diagram of shape $D$, where $x$ maps to the image of $x\in D/x \hookrightarrow [{(D/x)^\op},Set] \to E$, and since $E$ is cocomplete this diagram has a colimit $y$.  But $y$ is not in any of the categories $[{(D/x)^\op},Set]$, and therefore (since $Set$ is the free cocomplete category on one generator) there is a cocontinuous functor $Set \to [{(D/x)^\op},Set]$ not factoring through any $[{(D/x)^\op},Set]$.  So $Set$ is not a presentable object of $CocpltCat$.
=--



[[!redirects presentable category]]
[[!redirects locally presentable categories]]
[[!redirects presentable categories]]
