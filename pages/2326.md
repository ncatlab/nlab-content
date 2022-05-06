
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--

# Contents
* automatic table of contents goes here
{:toc}


## Definition

In intrinsic terms, a [[topos]] is _localic_ if it is generated under [[colimit]]s by the [[subobject]]s of its [[terminal object]] $1$. 

In equivalent but extrinsic terms, a category is a localic topos if it is equivalent to the [[category of sheaves]] on a [[locale]] with respect to the [[coverage|topology]] of jointly epimorphic families (accordingly, every localic topos is a [[Grothendieck topos]]). 

The [[frame]] of [[open set|opens]] specifying the locale may indeed be taken as the [[poset]] of [[subobject]]s of $1$ (i.e., internal [[truth value|truth values]]). From the perspective of logic, localic toposes are those categories which are equivalent to the category of [[partial equivalence relation]]s of the [[tripos]] given by a [[complete Heyting algebra]] (as before, the complete Heyting algebra may be taken as the poset of internal truth values).


## Properties


* A Grothendieck topos $E$ is a localic topos if and only if its unique [[global section]] [[geometric morphism]] to [[Set]] is a [[localic geometric morphism]]. 

  Thus, in general we regard a localic geometric morphism $E \to S$ as exhibiting E as a "localic S-topos".

* Moreover, just as localic topoi can be identified with locales, for any base topos $S$ the [[2-category]] of localic $S$-topoi is equivalent to the 2-category [[Loc]]$(S)$ of [[internalization|internal]] [[locale]]s in $S$.

  $$
    LocTopos(S) \simeq (Topos/S)_{loc} \simeq Loc(S)
    \,.
  $$


  Here $LocTopos(S)$ is the [[2-category]] whose 

  * objects are localic toposes over $S$;

  * morphisms are [[geometric morphism]]s, i.e. [[adjunctions]] in which the left adjoint preserves [[finite limits]], considered as pointing in the direction of their right adjoint; and

  * 2-morphisms are [[mate]]-pairs of [[natural transformation]]s.

  Then the 2-category $LocTopos$ is [[equivalence of categories|equivalent]] to the 2-category $Loc$ of [[locales]] (see C1.4.5 in the [[Elephant]]).  

  The 2-category $Loc$ is actually a [[(1,2)-category]]; its [[2-morphism]] are the pointwise ordering of [[frame]] homomorphisms.  Thus this equivalence implies that $LocTopos$ is also a (1,2)-category, and moreover that it is [[locally small category|locally essentially small]], in the sense that its hom-categories are essentially small.  (The 2-category $Topos$ of all toposes is not locally essentially small.)  Assuming sufficient separation axioms, the hom-posets of $Loc$, and hence $LocTopos$, become discrete.


## Examples

* Obviously, every [[Grothendieck topos]] that is a [[category of sheaves]] on (the [[category of open subsets]] of) a [[topological space]] is localic. 

* Every [[sheaf topos]] over a [[posite]] is localic. (See there for details.)

Many familiar toposes $E$, even when they are not localic, can be covered by a localic [[over topos|slice]] $E/X$ ("covered" means the unique map $X \to 1$ is an epi). For example, if $G$ is a group, then $E = Set^G$ is not itself localic, but it has a localic slice $Set^G/G \simeq Set$ that covers it. Such a topos is called an [[étendue]] (cf. Lawvere's 1975 monograph _Variable Sets Etendu and Variable Structure in Topoi_).[^fine] 

[^fine]: The 'etendu' in the title of Lawvere's monograph might not be a misspelled noun, but an adjective as part of a back translation of a (hypothetical) French expression 'ensembles &#233;tendus'. See this [nForum thread](http://nforum.mathforge.org/discussion/5805/etendue/) for some discussion and speculation on this point. 

A significant result due to Joyal and Tierney is that for any Grothendieck topos $E$, there exists an open surjection $F \to E$ where $F$ is localic. This fact is reproduced in Mac Lane and Moerdijk's text _Sheaves in Geometry and Logic_ (section IX.9), where the localic cover taken is called the _Diaconescu cover_ of $E$. 

Then, using methods of descent theory, Joyal and Tierney deduce that every Grothendieck topos is equivalent to the category $B G$ of continuous discrete representations of a [[localic groupoid]] $G$. (Their result is relativized so as to hold internally over any Grothendieck topos $S$ as base.) This should be regarded as a major extrapolation of Grothendieck's [[Galois theory]] (as in [[SGA]] 1), where it is shown that the [[etale topos]] of a field $k$ is equivalent to the category of continuous discrete representations of the fundamental [[pro-group]] $Gal(\bar{k}/k)$, where $\bar{k}$ denotes the separable closure of $k$. It was a watershed event for the penetration of localic methods in topos theory. 

## The connection with propositional logic

Recall that a [[geometric theory]] $\mathbb{P}$ over a signature with no sort symbols is called [[propositional theory|propositional]]. Such a signature can contain at most 0-ary relation symbols but lacks variables and, accordingly, $\mathbb{P}$ admits only sequents over the empty context consisting of nested conjunctions or (infinitary) disjunctions of such relation symbols - in other words, logic boils down to [[propositional logic]].

Propositional theories have the peculiarity that their classifying toposes always exist regardless of the availability of a [[natural numbers object]] in the base topos (cf. for details&references see at [[classifying topos]]).



+-- {: .num_prop #localicclasifiespropositional}
###### Proposition

Localic toposes correspond exactly to [[classifying topos|classifying toposes]] of propositional theories.
=--

This appears in Johnstone (2002, D3.1.14, p.897f.).

Given a locale $L$, the **theory of completely prime filters** $\mathbb{P}_L$ has a 0-ary relation symbol $F_x$ for each $x\in L$, thought to express the proposition that $x$ is contained in the [[filter]] $F$, and the following sequents:

* $\top\vdash F_1$ ,

* $F_x\wedge F_y\vdash F_{x\wedge y}$ for all pairs $x,y\in L$,

* $F_{\big (\bigvee_{i\in I} y_i\big )}\vdash \bigvee_{i\in I} F_{y_i}$ .

In $Set$ models of $\mathbb{P}_L$ correspond precisely to completely prime filters i.e. the multiplicatively closed subsets of $L$ containing $1$ that are inaccessible by infinite joins ($(\bigvee y_i)\in F$ implies $y_i\in F$ for some $i$). Note in particular, that the properness $0\notin F$ of a completely prime filter $F$ is implicit in the third axiom schema with $I=\emptyset$.

The relation between $L$ and $\mathbb{P}_L$ is that $Sh(L)\simeq Set[\mathbb{P}_L]$.

Conversely, given a propositional theory $\mathbb{P}$, the [[Lindenbaum-Tarski algebra]] of classes of provably equivalent formulas over $\mathbb{P}$ together with the entailment order yields a locale $L_{\mathbb{P}}$ such that $Sh(L_\mathbb{P})$ classifies $\mathbb{P}$.

### The initial and terminal toposes as classifying toposes

For illustration let us consider the _empty theory_ $\mathbb{T}_1$ over the empty signature i.e $\mathbb{T}_1$ has no axioms. This is certainly propositional, its deductive closure consists of all tautologies using $\bot,\top,\wedge,\bigvee$. The Lindenbaum-Tarski algebra is simply $\mathbf{2}\simeq\{[\bot]\leq[\top]\}$ which corresponds to the frame of open sets of the one-point space whence $Set[\mathbb{T}_1]=Sh(\mathbf{2})=Set$. Similarly, $\mathbb{P}_{\mathbf{1}}$, the theory of completely prime filters of the one-point locale $\mathbf{1}$, is classified by $Sh(\emptyset)$ i.e. sheaves on the empty space.

Whereas $\mathbb{P}_{\mathbf{2}}$ has up to isomorphism exactly one model in every topos $\mathcal{E}$ namely the one interpreting $F_1$ as $id_{1_\mathcal{E}}$ and $F_0$ as $0_{\mathcal{E}}\hookrightarrow 1_{\mathcal{E}}$, $\mathbb{P}_{\mathbf{1}}$ has up to isomorphism exactly one model in up to isomorphism exactly one topos i.e. its model is the [[zero object]] of the (necessarily) degenerate topos.

Note that since $Set$ is the terminal Grothendieck topos, the empty theory $\mathbb{T}_1$ over the empty signature is [[Morita equivalence|Morita equivalent]] to any other geometric theory $\mathbb{T}$ over any signature whatsoever provided $\mathbb{T}$ has up to isomorphism exactly one model in every Grothendieck topos $\mathcal{E}$. E.g. a slight modification of the inconsistent theory $\{\top\vdash\bot\}$ over the empty signature, namely adding a sort symbol $O$ and "contextualising" $\mathbb{T}_1'=\{\top\vdash_{x:O}\bot\}$ has models exactly the initial objects but these are unique (and every topos has one) whence $Set[\mathbb{T}_1']\simeq Set$.

Note also the difference in behavior between the inconsistent and the empty theory with respect to enlargening the signature: adding a sort symbol does not change the categories of models of the inconsistent theory up to isomorphism whereas $\mathbb{T}_1'$ has entirely different categories of models from the _empty theory_ over the signature containing a sort symbol $O$ since the latter is the [[theory of objects]] $\mathbb{O}$; but $\mathbb{T}_1'$ is a quotient of $\mathbb{O}$ whence we can think of $\mathbb{T}_1'$ as an axiomatisation of $Set$ as subtopos of $Set[\mathbb{O}]$ (see at [[level]] for further information on the duality between quotient theories and [[subtopos|subtoposes]] of the classifying topos). To sum up "paraphrasing" Tolstoy: there is only one way to be inconsistent but an infinite number of ways of being empty!

## Generalizations

In the context of [[(∞,1)-topos]] [[Higher Topos Theory|theory]] there is a notion of [[n-localic (∞,1)-topos]].

Notice that a [[locale]] is itself a (Grothendieck) [[(0,1)-topos]]. Hence a localic topos is a 1-[[topos]] that behaves essentially like a [[(0,1)-topos]]. In the wider context this would be called a [[n-localic (infinity,1)-topos|1-localic (1,1)-topos]].

## Related concepts

* [[locale]]

* [[localic geometric morphism]]

* [[spatial topos]], [[category of sheaves on a topological space]]

* [[étendue]]

* [[n-localic (∞,1)-topos]]

* [[n-localic 2-topos]]

## References

* {#MacLaneMoerdijk} [[Saunders Mac Lane]], [[Ieke Moerdijk]], _[[Sheaves in Geometry and Logic]]_ , Springer Heidelberg 1994. (chapter IX, p.472ff) 

* [[Peter Johnstone]], _[[Sketches of an Elephant]] 2 vols._ , Oxford UP 2002. (In general around C.1.4.5 p.515f, cp filters at D1.1.7 p.816f, as classifying topos B4.2.12. p.431f, D1.1.14 p.897f.)

[[!redirects Localic topos]]
[[!redirects localic toposes]]
[[!redirects localic topoi]]
