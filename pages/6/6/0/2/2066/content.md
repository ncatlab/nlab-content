
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea ##

The _Karoubi envelope_ or _idempotent completion_ of a [[category]] is the [[universal construction|universal]] enlargement of the category with the property that every [[idempotent]] is a [[split idempotent]].  This is the [[Set]]-enriched version of the more general notion of _[[Cauchy completion]]_ of an [[enriched category]].

A category in which all idempotents split is called *Karoubi complete* or *Cauchy complete* or *idempotent-complete*.  Thus, the Karoubi envelope is a [[completion]] operation into such categories.


## Definition
 {#Definition}

There  is an

* _[Abstract definition](#AbstractDefinition)_

that characterizes idempotent completions. In particular the idempotent completion always exists and is unique up to [[equivalence of categories]]. Explicit constructions include:

* _[Construction in components](#InComponents)_

* _[Construction via the Yoneda embedding](#UnderTheYonedaEmbedding)_

For more constructions and equivalent characterizations see at _[[Cauchy complete category]]_ in the section _[In ordinary category theory](Cauchy+complete+category#InOrdinaryCategoryTheory)_.

### Abstract definition
 {#AbstractDefinition}

+-- {: .num_defn #IdempotentCompletionAbstractly}
###### Definition

For $\mathcal{C}$ a [[category]], a [[functor]] $\mathcal{C} \to \tilde \mathcal{C}$ exhibits $\tilde \mathcal{C}$ as an **idempotent completion** of $\mathcal{C}$ if

* $\tilde \mathcal{C}$ is an [[idempotent complete category]];

* $\mathcal{C} \to \tilde \mathcal{C}$ is a [[full and faithful functor]];

* every object in $\tilde \mathcal{C}$ is the [[retract]] of an object in $\mathcal{C}$, under this embedding.

=--

See e.g. ([Lurie, def. 5.1.4.1](#Lurie)). 

+-- {: .num_lemma #def2}
###### Lemma  
For a fully faithful embedding $i \colon \mathcal{C} \to \mathcal{D}$ to exhibit an idempotent(-splitting) completion of $\mathcal{C}$, it suffices that 

* $i(p)$ splits in $\mathcal{D}$ for every idempotent $p$ in $\mathcal{C}$, and 

* every object in $\mathcal{D}$ is the retract of an object in $\mathcal{C}$ under $i$. 
=-- 

+-- {: .proof} 
###### Proof 
We must show that these conditions imply that every idempotent $e \colon D \to D$ in $\mathcal{D}$ splits. Write $D$ as a retract of some $i(C)$, say $r: i(C) \to D$ with right inverse $s$ ($r s = 1_D$). Then $p = s e r \colon i(C) \to i(C)$ is idempotent, and we may split $p$, say as $p = \sigma \pi$ with $\pi \sigma = 1_E$ for some $E$. We claim that the pair 

$$\pi s \colon D \to E, \qquad r \sigma \colon E \to D$$ 

provides a splitting of $e$. Certainly we have 

$$(r \sigma)(\pi s) = r s e r s = e,$$ 

and we also have 

$$\sigma(\pi s)(r \sigma) = p s r \sigma = s e r s r \sigma = s e r \sigma = p \sigma = \sigma \pi \sigma = \sigma$$ 

whence

$$(\pi s)(r \sigma) = \pi \sigma (\pi s)(r \sigma) = \pi \sigma = 1_E,$$ 

as desired. 
=-- 


### In components
 {#InComponents}

Let $C$ be a [[category]]. We give an elementary construction of the __Karoubi envelope__ $\bar{C}$ which formally splits [[idempotents]] in $C$. 


The objects of $\bar{C}$ are pairs $(c, e: c \to c)$ where $e$ is an idempotent on an object $c$ of $C$. Morphisms $(c, e) \to (d, f)$ are morphisms $\phi: c \to d$ in $C$ such that $f \circ \phi = \phi = \phi \circ e$ (or equivalently, such that $\phi = f \circ \phi \circ e$). NB: the identity on $(c, e)$ in $\bar{C}$ is the morphism $e: c \to c$. 


There is a functor 

$$E: C \to \bar{C}$$ 

which maps an object $c$ to $(c, 1_c)$. This functor is [[fully faithful functor|full and faithful]]: it fully embeds $C$ in $\bar{C}$. If $e: c \to c$ is an idempotent in $C$, then in $\bar{C}$ there are maps 

$$p: (c, 1_c) \to (c, e), \, j: (c, e) \to (c, 1_c),$$ 

both given by $e: c \to c$. It is clear that $p \circ j$ is the identity $e: (c, e) \to (c, e)$, and that $j \circ p$ is the idempotent $E(e): E(c) \to E(c)$. Thus the pair $(p, j)$ formally splits the idempotent $e: c \to c$. The same argument shows that every idempotent $\phi: (c, e) \to (c, e)$ in $\bar{C}$ splits through $(c,\phi)$. Actually this formal construction does more: it gives a _choice_ of splitting for every idempotent. 


Let $D$ be any category in which every idempotent $h: d \to d$ has a chosen splitting $(p_h: d \to d_h, j_h: d_h \to d)$ (using identities to split identities), and let $F: C \to D$ be a functor. Define an extension 

$$\bar{F}: \bar{C} \to D$$ 

by sending $(c, e: c \to c)$ to the underlying object $F(c)_{F(e)}$ of the splitting of $F(e): F(c) \to F(c)$ in $D$. For morphisms $\phi: (c, e) \to (c', e')$, define $\bar{F}(\phi)$ to be the composite 

$$F(c)_{F(e)} \overset{F(j_{F(e)})}{\to} F(c) \overset{F(\phi)}{\to} F(c') \overset{F(p_{F(e')})}{\to} F(c')_{F(e')}$$ 

Then $\bar{F}$ is the unique extension of $F$ which preserves chosen splittings. Thus the Karoubi envelope is universal among functors from $C$ into categories $D$ in which every idempotent has a chosen splitting. 


If $D$ is a category in which every idempotent splits, then we can choose a splitting for each idempotent using the [[axiom of choice]] (AC); the extension $\bar{F}$ depends on how we do this but is unique up to unique [[natural isomorphism]].  Alternatively, we can define $\bar{F}$ as an [[anafunctor]]; then no AC is needed, and we still have $\bar{F}$ unique up to unique natural isomorphism.  (It is key here that a splitting of an idempotent is unique up to a coherent isomorphism.) 

Essentially the same argument shows that for any $D$ in which idempotents split, the restriction functor $[E, D]: [\bar{C}, D] \to [C, D]$ is an equivalence. The details are spelled out [here](http://ncatlab.org/toddtrimble/published/Karoubi+envelope). 


### Under the Yoneda embedding
 {#UnderTheYonedaEmbedding}

+-- {: .num_prop}
###### Proposition

For $\mathcal{C}$ a [[small category]], write $PSh(\mathcal{C})$ for its [[category of presheaves]] and write $\tilde \mathcal{C} \hookrightarrow PSh(\mathcal{C})$ for the [[full subcategory]] on those presheaves which are [[retracts]] of objects in $\mathcal{C}$, under the [[Yoneda embedding]]. Then the Yoneda embedding

$$
  \mathcal{C} \to \tilde \mathcal{C}
$$

exhibits $\tilde \mathcal{C}$ as [[generalized the|the]] idempotent completion of $\mathcal{C}$.

=--

For instance ([Lurie, proof of prop. 5.1.4.2](#Lurie)).

## Properties

### Finality of the completion
 {#Finality}

+-- {: .num_defn}
###### Definition

A functor $\mathcal{C}\to \tilde \mathcal{C}$ exhibiting an idempotent completion, def. \ref{IdempotentCompletionAbstractly}, is a [[final functor]].

=--

For instance ([Lurie, lemma 5.1.4.6](#Lurie)).

### Monadicity over semicategories

The functor that forms idempotent completion is the [[monad]] induced from the [[adjunction]] between categories and [[semicategories]] given by the [[forgetful functor]] $Cat \to SemiCat$ and its [[right adjoint]]. More details on this are at _[Semicategory - Relation to categories](semicategory#RelationToCategories)_.

## Examples

* [[category of Chow motives]] 

### The category of smooth manifolds 

Let $Man$ be the category of [[smooth manifolds]] and [[smooth maps]], where by a "smooth manifold", we mean a finite-dimensional, second-countable, Hausdorff, $C^\infty$ [[manifold]] without boundary.  Let $i: Open \hookrightarrow Man$ be the [[full subcategory]] whose objects are the [[open subspaces]] of finite-dimensional [[Cartesian spaces]]. 

+-- {: .num_theorem} 
###### Theorem 
The subcategory $i: Open \hookrightarrow Man$ exhibits $Man$ as an idempotent-splitting completion of $Open$. 
=-- 

+-- {: .proof} 
###### Proof 
By lemma \ref{def2}, it suffices to prove that 

* Every smooth manifold is a smooth retract of an open set in Euclidean space; 

* If $p : U \to U$ is a smooth idempotent on an open set $U \subseteq \mathbb{R}^n$, then the subset $Fix(p) \hookrightarrow U$ is an embedded submanifold. 

For the first statement, we use the fact that any manifold $M$ can be realized as a closed submanifold of some $\mathbb{R}^n$, and every closed submanifold has a [[tubular neighborhood theorem|tubular neighborhood]] $U \subseteq \mathbb{R}^n$. In this case $U$ carries a structure of vector bundle over $M$ in such a way that the inclusion $M \hookrightarrow U$ is identified with the zero section, so that the bundle projection $U \to M$ provides a retraction, with right inverse given by the zero section. 

For the second statement, assume that the origin $0$ is a fixed point of $p$, and let $T_0(U) \cong \mathbb{R}^n$ be its tangent space (observe the presence of a _canonical_ isomorphism to $\mathbb{R}^n$). Thus we have idempotent linear maps $d p(0), Id-d p(0): T_0(U) \to T_0(U)$ where the latter factors through the inclusion $\ker \; d p(0) \hookrightarrow T_0(U)$ via a projection map $\pi: T_0(U) \to \ker \; d p(0)$. We have a map $f: U \to \mathbb{R}^n$ that takes $x \in U$ to $x - p(x)$; let $g$ denote the composite 

$$U \stackrel{f}{\to} \mathbb{R}^n \cong T_0(U) \stackrel{\pi}{\to} \ker\; d p(0).$$ 

Now we make some easy observations: 

1. $Fix(p) \subseteq g^{-1}(0)$. 

1. The map $p: U \to U$ restricts to a map $p: g^{-1}(0) \to g^{-1}(0)$, by idempotence of $p$. 

1. The derivative $d g(0): T_0(U) \to T_0(\ker \; d p(0)) \cong \ker \; d p(0)$ is $\pi$ again since $Id - d p(0)$ is idempotent. Thus $d g(0)$ has full rank ($m$ say), and so the restriction of $g$ to some neighborhood $V$ has $0$ as a regular value, and $g^{-1}(0) \cap V$ is a manifold of dimension $m$ by the [[implicit function theorem]]. The tangent space $T_0(g^{-1}(0) \cap V)$ is canonically identified with $im(d p(0))$. 

1. There are smaller neighborhoods $V'' \subseteq V' \subseteq V$ so that $p$ restricts to maps $p_1, p_2$ as in the following diagram ($i, i', i''$ are inclusion maps, all taking a domain element $x$ to itself): 
$$\array{
g^{-1}(0) \cap V'' & \stackrel{i''}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_2} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V' & \stackrel{i'}{\hookrightarrow} & g^{-1}(0) \\ 
 _\mathllap{p_1} \downarrow & & \downarrow _\mathrlap{p} \\ 
g^{-1}(0) \cap V & \stackrel{i}{\hookrightarrow} & g^{-1}(0)
}$$ 
and such that $p_1, p_2$ are diffeomorphisms by the [[implicit function theorem|inverse function theorem]] (noting here that $d p_i(0): im(d p(0)) \to im(d p(0))$ is the identity map, by idempotence of $p$). 

1. Letting $q: g^{-1}(0) \cap V' \to g^{-1}(0) \cap V''$ denote the smooth inverse to $p_2$, we calculate $i' = p \circ i'' \circ q$, and 
$$i p_1 = p i' = p p i''q = p i'' q = i',$$ 
so that $p_1(x) = x$ for every $x \in g^{-1}(0) \cap V'$. Hence $g^{-1}(0) \cap V' \subseteq Fix(p)$. 

From all this it follows that $Fix(p) \cap V' = g^{-1}(0) \cap V'$, meaning $Fix(p)$ is locally diffeomorphic to $\mathbb{R}^m$, and so $Fix(p)$ is an embedded submanifold of $\mathbb{R}^n$. 
=--

+-- {: .num_remark} 
###### Remark 
[Lawvere](#Law) comments on this fact as follows: "For example, if $\mathbf{C}$ is the category of all smooth maps between all open subsets of all Euclidean spaces, then $\widebar{\mathbf{C}}$ $[$the Karoubi envelope$]$ 
is the category of all smooth manifolds. This powerful theorem justifies bypassing the complicated considerations of charts, coordinate transformations, and atlases commonly offered as a "basic" definition of the concept of manifold. For example the 2-sphere, a manifold but not an open set of any Euclidean space, may be fully specified with its smooth structure by considering any open set $A$ in 3-space $E$ which contains it but not its center (taken to be $0$) and the smooth idempotent endomap of $A$ given by $e(x) = x/{|x|}$. All general constructions (i.e., functors into categories which are Cauchy complete) on manifolds now follow easily (without any need to check whether they are compatible with coverings, etc.) provided they are known on the opens of Euclidean spaces: for example, the tangent bundle on the sphere is obtained by splitting the idempotent $e'$ on the tangent bundle $A \times V$ of $A$ ($V$ being the vector space of translations of $E$) which is obtained by differentiating $e$. The same for cohomology groups, etc." 
=-- 

### Projective modules and vector bundles

The category of projective modules over any ring is the Karoubi envelope of its full subcategory of free modules.

The category of (locally trivial, finite dimensional) vector bundles over any fixed paracompact space is the Karoubi envelope of its full subcategory of trivial bundles.

Both examples are related by the [[Serre-Swan theorem]]. In fact both these facts together with the observation that the global sections functor is an equivalence from the category trivial bundles over $X$ to the category of free modules over $C(X)$ prove the Serre-Swan theorem itself.

## Related concepts

* [[Karoubian category]], [[pseudo-abelian category]]

* [[Cauchy completion]]

* [[free coproduct completion]]

* [[free cocompletion]]

* [[idempotent complete (infinity,1)-category]]



## References 
 {#References}

The term "Karoubi envelope" appears to have been introduced in:

* {#Hayashi1985} [[Susumu Hayashi]], Def. 1.2 in: *Adjunction of semifunctors: categorical structures in nonextensional lambda calculus*, Theoretical Computer Science **41** (1985) 95-104 &lbrack;<a href="https://doi.org/10.1016/0304-3975(85)90062-3">doi:10.1016/0304-3975(85)90062-3</a>&rbrack;

and apparently in reference to the [[universal construction]] of [[pseudo-abelian categories]] (now also: "[[Karoubian categories]]") in:

* {#Karoubi78} [[Max Karoubi]], Theorem 6.10 of: *K-Theory -- An introduction*, Grundlehren der mathematischen Wissenschaften **226**, Springer (1978) &lbrack;[pdf](https://webusers.imj-prg.fr/~max.karoubi/K.book/MK.book.pdf), [doi:10.1007%2F978-3-540-79890-3](https://link.springer.com/book/10.1007%2F978-3-540-79890-3)&rbrack;

  > (in the context of [[topological K-theory]]).

A classical account is for instance in

* {#BorceuxDejean} [[Francis Borceux]] and D. Dejean, _Cauchy completion in category theory_  Cahiers Topologie G&#233;om. Diff&#233;rentielle Cat&#233;goriques, 27:133&#8211;146, (1986) ([numdam](http://www.numdam.org/item?id=CTGDC_1986__27_2_133_0))
  

For more classical references see at  _[[Cauchy complete category]]_.


Karoubi envelopes for [[(infinity,1)-category|(∞,1)-categories]] are discussed in section 4.4.5 of

* [[Jacob Lurie]], _[[Higher Topos Theory]]_
 {#Lurie}


Some discussion of the stable version is in section 4.1.2 of

* [[David Ben-Zvi]], John Francis, David Nadler, _Integral Transforms and Drinfeld Centers in Derived Algebraic Geometry_ ([arXiv](http://arxiv.org/abs/0805.0157), [[geometric infinity-function theory|nLab entry]])

and section 2.3 of 

* [[David Ben-Zvi]], David Nadler, _The Character Theory of a Complex Group_ ([arXiv](http://arxiv.org/abs/0904.1247))

In section 3.1.2 of latter are also given
references (to Neeman and Lurie) for an important result of Neeman's about Karoubi closure and compact generators.

The Karoubi envelope for the additive case (see also [[additive envelope]]) is covered at 

* [[Dror Bar-Natan]], [[Scott Morrison]], _The Karoubi envelope and Lee's degeneration of Khovanov homology_ ([arXiv](http://arxiv.org/abs/math/0606542))

Discussion for [[triangulated categories]] is in 

* Paul Balmer, Marco Schlichting, _Idempotent completion of triangulated categories_ ([pdf](http://www.math.ucla.edu/~balmer/research/Pubfile/IdempCompl.pdf)) 

The proof that idempotents split in the category of manifolds was adapted from this MO answer: 

* Zack (http://mathoverflow.net/users/300/zack), Idempotents split in category of smooth manifolds?, URL (version: 2014-04-06): http://mathoverflow.net/q/162556 ([web](http://mathoverflow.net/a/162556/2926)) 

Which provides a solution to exercise 3.21 in

* F. W. Lawvere, _Perugia Notes - Theory of Categories over a Base Topos_ , Ms. Universit&#224; di Perugia 1973.

The accompanying above remark of Lawvere appears on page 267 of 

* [[F. William Lawvere]], _Qualitative distinctions between some toposes of generalized graphs_, Contemporary Mathematics 92 (1989), 261-299. ([pdf](http://www.ams.org/books/conm/092/1003203/conm092-1003203.pdf)) 
 {#Law} 

A comparison of the Karoubi envelope to other completions can be found here:

* [[Marta Bunge]], _Tightly Bounded Completions_ , TAC **28** no. 8 (2013) pp.213-240. ([pdf](http://www.tac.mta.ca/tac/volumes/28/8/28-08.pdf))

Formalization in [[homotopy type theory]]:

* {#Shulman14} [[Mike Shulman]], _[Splitting idempotents](http://homotopytypetheory.org/2014/12/08/splitting-idempotents/)_ 

A generalization of the Karoubi envelope for [[n-categories]] is in 

* [[Davide Gaiotto]], [[Theo Johnson-Freyd]], _Condensations in higher categories_, ([arXiv:1905.09566](https://arxiv.org/abs/1905.09566))

[[!redirects Karoubi envelopes]]

[[!redirects Karoubi completion]]
[[!redirects Karoubi complete category]]
[[!redirects idempotent-complete category]]
[[!redirects idempotent complete category]]

[[!redirects idempotent completion]]
[[!redirects idempotent completions]]

[[!redirects idempotent-splitting completion]]
[[!redirects idempotent-splitting completions]]


[[!redirects pseudo-abelian completion]]
[[!redirects Karoubian envelope]]
[[!redirects Karoubianization]]
[[!redirects Karoubianization functor]]
[[!redirects Karoubinization functor]]


