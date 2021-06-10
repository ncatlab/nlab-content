
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Model category theory
+--{: .hide}
[[!include model category theory - contents]]
=--
=--
=--



# Contents 
* table of contents
{:toc}

## Idea 

A _combinatorial model category_ is a particularly tractable [[model category]] structure. (Notice however that there is also the, closely related, technical notion of a [[tractable model category]]).

Being combinatorial means that there is very strong control over the cofibrations in these model structures: there is a [[set]] (meaning [[small set]], not a [[proper class]]) of [[cofibrantly generated model category|generating (acyclic) cofibrations]], and all objects, in particular the domains and codomains of these cofibrations, are [[small object]]s.

So as a slogan we have that

+-- {: .standout}

 A combinatorial model structure is one that is generated from _small data_: it is generated from a small set of (acyclic) cofibrations between small objects. 

=--

In fact, the combinatoriality condition is a bit stronger than that, as it requires even that _every_ object is small and is the colimit over a small set of generating objects. 

There exist large classes of model categories that either are combinatorial or, if not, are [[Quillen equivalence|Quillen equivalent]] to ones that are. See the list of examples below.


The relevance of combinatorial model categories is given more abstractly by the result that 

+-- {: .standout}

[[combinatorial simplicial model category|Combinatorial simplicial model categories]] are precisely those model categories that model [[presentable (∞,1)-category|presentable (∞,1)-categories]].


=--

For more see at _[[locally presentable categories - introduction]]_.

There is also a more general class of model structures on locally presentable categories, namely [[accessible model categories]], that share many of the properties of combinatorial ones, and are additionally closed under more constructions such as [[transferred model structures]].  In addition, every combinatorial model category can be enhanced to an [[algebraic model category]].

## Definition 

The following definition originates with [[Jeff Smith]]:

+-- {: .num_defn}
###### Definition 

A [[model category]] $C$ is **combinatorial** if it is

* [[locally presentable category|locally presentable]] as a [[category]]

and

* [[cofibrantly generated model category|cofibrantly generated]] as a model category.

=--

+-- {: .num_remark}
###### Remark

Recall from the discussion at [[cofibrantly generated model category]] that this means that $C$ has a [[set]] (i.e. a [[small set]], not a [[proper class]]) $I$ of generating [[cofibrations]] and a set $J$ of generating trivial cofibrations in that

$$ 
  cof = llp(rlp(I))
$$
  
$$
  fib = rlp(J)
  \,.
$$


Here $fib, cof \subset Mor(C)$ is the collection of fibrations and cofibration, respectively, and $llp(S), rlp(S)$ is the collection of morphisms satisfying the left or right, respectively, [[lifting property]] with respect to a collection of morphisms $S$. 

=--

Jeff Smith's theorem, [below](#SmithTheorem), gives an equivalent characterization that is usually easier to handle.


## Characterization theorems 

There are two powerful theorems that characterize combinatorial model categories in terms of data that is often easier to handle: 

* [[Jeff Smith]]'s theorem characterizes combinatorial model categories just in terms of weak equivalences and generating cofibrations, hence using only two third of the input data explicitly required. This greatly facilitates identifying combinatorial model category structures. For instance it helps to show that the left [[Bousfield localization of model categories|Bousfield localization]] of certain combinatorial model categories is again a combinatorial model category.

* [[Dugger's theorem]] shows that [[combinatorial model category|combinatorial model categories]] are, up to [[Quillen equivalence]], precisely those model categories that have a _presentation_ in that they are [[Bousfield localization of model categories|Bousfield localization]]s of [[model structure on simplicial presheaves|global model structures on simplicial presheaves]]. This was used by [[Jacob Lurie]] to show that simplicial combinatorial model categories are precisely the models for [[presentable (∞,1)-category|locally presentable (∞,1)-categories]].


### Smith's theorem 
 {#SmithTheorem}

A central theorem about combinatorial model categories is **[[Jeff Smith]]'s theorem** which establishes the existence of combinatorial model category structures from a small amount of input data.


+-- {: .num_theorem}
###### Theorem 
**(Jeff Smith's theorem)**

For

* $C$ a [[locally presentable category]];

* $Arr_W(C) \subset Arr(C)$ an accessibly embedded [[accessible category|accessible]] [[full subcategory]] of the [[arrow category]] $Arr(C)$ on a [[class]] $W \subset Mor(C)$;

* $I \subset Mor(C)$ a small [[set]] (not a proper class) of morphisms of $C$ 

such that

* $W$ satisfies [[category with weak equivalences|2-out-of-3]];

* $inj(I) \subset W$

* $cof(I) \cap W$ is closed under [[pushout]] and [[transfinite composition]].

we have that $C$ is a combinatorial model category with

* weak equivalences $W$;

* cofibrations $cof(I)$.

Moreover, every combinatorial model category arises in this way.

=--

Here the notation is as described at [[cofibrantly generated model category]], so: $inj(I) = rlp(I)$ and $cof(I) = llp(rlp(I))$.

This statement was announced by [[Jeff Smith]] in 1998 at a conference in Barcelona and appararently first appeared in print as ([Beke, theorem 1.7](#Beke)).
The above formulation follows ([Barwick, prop 1.7](#Barwick)).
 

+-- {: .proof}
###### Proof

To prove the first part of the statement, that the given data encodes a combinatorial model category, it is sufficient to find a small set $J$ such that

$$
  cof(J) = W \cap cof(I)
  \,.
$$

With that the statement follows using the [[small object argument]] to show the existence of the required factorizations.

To find this small set, we make use of the assumption that the subcategory
$Arr_W(C) \subset Arr(C)$ of weak equivalences and commuting squares in $C$ between them is an [[accessible category|accessible]] subcategory of the [[arrow category]] $Arr(C)$.  This means that there is a small set $W_0 \subset W$ such that every element of $W$
is a $\kappa$-[[directed colimit]] over element in $W_0$ in $Arr_W(C)$, for some large enough [[cardinal number]] $\kappa$, such that all elements of $I$ are $\kappa$-[[compact object|compact]].

Using the [[small object argument]] factor
every morphism $P \to Q$ in $W_0$ as 
$P \stackrel{\in cell(I)}{\to} R \stackrel{\in inj(I)}{\to}Q$.  Note that by [[category with weak equivalences|2-out-of-3]] and $inj(I) \subseteq W$,
the cofibration $P \to R$ is in $W$.
Let $J$ be the set of acyclic cofibratons $P \to R$ so obtained.


By the choice of $W_0$ every morphism

$$
  \array{
    K &\to& M
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\mathrlap{\in W}}
    \\
    L &\to& N
  }
$$

in $Arr(C)$ lifts through one of the components in $W_0$ of $W$  (this mechanism is described in detail at [[small object]]) as

$$
  \array{
    K &\to& P &\to& M
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\mathrlap{\in W_0}} && \downarrow^{\mathrlap{\in W}}
    \\
    L &\to& Q &\to& N
  }
  \,.
$$

We can refine this to a factoring through $J$ as follows:
by construction 
the morphism $P \to Q$ factors as 
$P \stackrel{\in J}{\to} R \stackrel{\in inj(I)}{\to}Q$. Then $L \to Q$ lifts to $L \to R$ and we obtain the factorization 

$$
  \array{
    K &\to& P &\to& M
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\mathrlap{\in J}} && \downarrow^{\mathrlap{\in W}}
    \\
    L &\to& R &\to& N
  }
$$

of the original square from an element in $I$ to an element in $W$  through an element in $J$. 
(In [Beke](http://arxiv.org/abs/math/0102087), following [[Jeff Smith]], this is called the 
**solution set condition**: $J$ is "a solution set for $W$ at $I$").
It readily follows that $inj(J) \cap W \subseteq inj(I)$.


By the [[small object argument]] every morphism $A \stackrel{\in W}{\to} B$ in $W$ may be factored as

$$
  A \stackrel{\in cell(J)}{\to} C \stackrel{\in inj(J)}{\to} B
  \,.
$$

Here by [[category with weak equivalences|2-out-of-3]],
the morphism $C \to B$ is in $W$, and hence in 
$inj(J) \cap W \subseteq inj(I)$.

This we use to show that every morphism $f \in cof(I) \cap W$ is in $cof(J)$:

since $f \in W$ we may factor $f$ as above and since $f \in cof(I)$ we obtain a lift $\sigma$ in

$$
  \array{
    A &\stackrel{\in cell(J)}{\to}& C
    \\
    \downarrow^{f} &{}^\sigma \nearrow&
    \downarrow^{\mathrlap{\in inj(I)}}
    \\
    B &\stackrel{=}{\to}& B
  }
  \,.
$$

Rearranging this it becomes a [[retract]] diagram in $Arr(C)$

$$
  \array{
    A &\stackrel{=}{\to}& A &\stackrel{=}{\to}& A
    \\
    \downarrow^f && \downarrow^{\mathrlap{\in cell(J)}}
    && \downarrow^f
    \\
    B &\stackrel{\sigma}{\to}&
    C
    &
    \stackrel{\in inj(I)}{\to}
    &
    B
  }
$$

which shows that $f$ is a retract of an element in $cell(J) \subset cof(J)$, hence itself in $cof(J)$.

And the converse statement is immediate: by definition $J \subset cof(I) \cap W$ and $cof(J)$ is the saturation of $J$ under the operation of forming retracts of transfinite compositions of pushouts of elements of $J$, under which $cof(I) \cap W$ is assumed to be closed.

In total we have indeed $cof(J) = cof(I) \cap W$ which shows that the $I$ and $W$ given determine a combinatorial model category.

To see the converse, that every combinatorial model structure arises this way, it is sufficient to show that for every combinatorial model category the category $Arr_W(C) \subset Arr(C)$ is an [[accessible category]]. 


=--

For applications of this theorem, the following auxiliary statements are useful.

+-- {: .num_prop}
###### Proposition

For $C$ a combinatorial model category, the full subcategory inclusion

$$
  Mor(C)_W \hookrightarrow Mor(C)
$$ 

of the [[arrow category]] on the weak equivalences is an [[accessible functor|accessible inclusion]] of an [[accessible category]].

=--

This is due to Smith. A proof appears as ([Dugger 01, 7.4](#Dugger01)). See also ([Barwick, prop. 1.10](#Barwick)).

+-- {: .num_prop}
###### Proposition

Let 

$$
  F : Mor(A) \to Mor(B)
$$

be an [[accessible functor]] between [[arrow categories]]. Let $B$ be equipped with [[category with weak equivalences|weak equivalences]] $W$ such that the [[full subcategory]] inclusion 

$$
  Mor(W) \hookrightarrow Mor(B)
$$

on the weak equivalences is an [[accessible functor|accessible embedding]] of an [[accessible category]]. Then so is the full subcategory of $Mor(A)$ on the pre-images $F^{-1}(W)$ in $A$.

=--

([Beke, prop. 1.18](#Beke)).

+-- {: .proof}
###### Proof

By general properties of [[accessible categories]] (see there) the full inverse image along an accessible functor of a full accessible subcategory is again accessible.

=--



### Dugger's theorem 
 {#DuggerTheorem} 

The following theorem is precisely the model-category theory version of the statement that every [[locally presentable (∞,1)-category]] arises as the [[localization of an (∞,1)-category|localization]] of an [[(∞,1)-category of (∞,1)-presheaves]].

+-- {: .num_theorem }
###### Theorem 
**([[Dugger's theorem]])**

Every combinatorial model category $C$ is [[Quillen equivalence|Quillen equivalent]] to a left [[Bousfield localization of model categories|Bousfield localization]] $L_S SPSh(K)_{proj}$ of the global projective [[model structure on simplicial presheaves]] $SPSh(K)_{proj}$ on a [[small category]] $K$

$$
  L_S SPSh(K)_{proj} \stackrel{\simeq_{Quillen}}{\to}
  C
  \,.
$$


=--

This is ([Dugger 01, theorem 1.1](#Dugger01)) building on results in ([DuggerUniversalHomotopy](#DuggerUniversalHomotopy)).


+-- {: .proof}
###### Proof


The proof proceeds (the way Dugger presents it, at least) in roughly three steps:

1. Use that $[C^{op}, sSet_{Quillen}]_{proj}$ is in some precise sense the _homotopy-_ [[free cocompletion]] of $C$. This means that every functor $\gamma : C \to B$ from a plain category $C$ to a model category $B$ factors in an essentially unique way through the [[Yoneda embedding]] $j : C \to [C^{op},sSet]$ by a [[Quillen adjunction]] 

   $$
     (\hat \gamma \dashv R) : 
     B
     \stackrel{\overset{\hat \gamma}{\leftarrow}}
      {\underset{R}{\to}}
     [C^{op}, sSet_{Quillen}]_{proj}  
     \,.
   $$

   The detailed definitions and detailed proof of this are discussed at [[(∞,1)-category of (∞,1)-presheaves]].

1. For a given combinatorial model category $B$, choose $C := B_\lambda^{cof}$ the full [[subcategory]] on a [[small set]] (guaranteed to exist since $B$ is [[locally presentable category|locally presentable]]) of cofibrant $\lambda$-[[compact object]]s, for some [[regular cardinal]] $\lambda$, and show that the induced Quillen adjunction 

   $$
     B \stackrel{\overset{\hat i}{\leftarrow}}{\underset{R}{\hookrightarrow}}
     [(B_\lambda^{cof})^{op}, sSet]_{proj} 
   $$


   induced by the above statement from the inclusion $i : B_\lambda^{cof} \hookrightarrow B$ exhibits $B$ as a homotopy-[[reflective subcategory]] in that the [[derived functor|derived]] counit $ \hat i \circ Q \circ R \stackrel{\simeq}{\to} Id$ ($Q$ some cofibrant replacement functor) is a [[natural transformation|natural]] weak equivalence on fibrant objects (recall from [[adjoint functor]] the characterization of adjoints to full and faithful functors).

1. Define $S$ to be the set of morphisms in $[(C_\lambda^{cof})^{op}, sSet]$ that the left [[derived functor]] $\hat i \circ Q$ of $\hat i$ (here $Q$ is some cofibrant replacement functor) sends to weak equivalences in $B$. Then form the left [[Bousfield localization of model categories|Bousfield localization]] $L_S [(C_\lambda^{cof})^{op},sSet]_{proj}$ with respect to this set of morphisms and prove that this is [[Quillen equivalence|Quillen equivalent]] to $B$.

Carrying this program through requires the following intermediate results.

First recall from the discussion at [[(∞,1)-category of (∞,1)-presheaves]] that to produce the Quilen adjunction $(\hat i \dashv R)$ from $i$, we are to choose a [[cofibrant resolution]] functor

$$
  I : C \to [\Delta,B]
$$

of $i : C= B_\lambda^{cof} \to B$.

The [[adjunct]] of this is a functor $\tilde I : C \times \Delta \to B$. For each object $b \in B$ write $(C \times \Delta \downarrow b)$ for the [[slice category]] induced by this functor. 


**Lemma** (Dugger, prop. 4.2) 

For every fibrant object $b \in B$ we have that the [[homotopy colimit]] $hocolim (C \times \Delta \downarrow b) \to B)$
is weakly equivalent to $\hat i \circ Q\circ R (b)$.

**Corollary** (Dugger, cor. 4.4) The induced Quillen adjunction

$$
  B \stackrel{\leftarrow}{\to}
  [C^{op}, sSet]
$$

is a homotopy-reflective embedding precisely if the canonical morphisms

$$
  hocolim (C \times \Delta \downarrow b) \to b
$$

are weak equivalences for every fibrant object $b \in B$.

...


=--

Notice that the theorem just mentions plain combinatorial model categories, not [[simplicial model category|simplicial model categories]]. But of course by basic facts of [[enriched category theory]] $Funct(C^{op}, SSet)$ is an [[SSet]]-[[enriched category]] and its projective [[global model structure on functors]] $Func(C^{op}, SSet)_{proj}$ is compatibly a [[simplicial model category]], as are all its [[Bousfield localization of model categories|Bousfield localizations]]. (See [[model structure on simplicial presheaves]] for more details.) Therefore an immediate but very useful corollary of the above statement is

+-- {: .num_corollary }
###### Corollary 

Every combinatorial model category is [[Quillen equivalence|Quillen equivalent]] to one which is

* a [[simplicial model category]]

* a left [[proper model category]].

=--



### Tractable combinatorial model categories 

A combinatorial model category is a [[tractable model category]] precisely if the set $I$ of generating cofibrations can be chosen such that all elements have a cofibrant object as domain.

A [[proper model category|left proper]] combinatorial model category precisely if the set $J$ of generating trivial cofibrations can be chosen with cofibrant domain.

This are corollaries 2.7 and 2..8 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).


## Properties 

### Homotopy colimits {#hocolims}

+-- {: .num_prop #CharacterizationOfFilteredHomotopyColimits}
###### Proposition

In a combinatorial model category, for every sufficiently large regular [[cardinal number|cardinal]] $\kappa$ the following holds:

* $\kappa$-[[filtered colimits]] preserve weak equivalences;

* hence $\kappa$-[[filtered colimits]] are already [[homotopy colimit]]s.


=--

See also at _[[filtered homotopy colimit]]_.

+-- {: .proof}
###### Proof

This appears as proposition 7.3 in [Dug00](http://arxiv.org/abs/math/0007068), reproduced for instance as prop. 2.5 in [Bar](http://www.math.harvard.edu/~clarkbar/complete.pdf).


The point is to choose $\kappa$ such that all domains and codomains of the generating cofibrations are $\kappa$-[[compact object]]. This is possible since by assumption that $C$ is a [[locally presentable category]] all its objects are [[small object]]s, hence each a $\lambda$-[[compact object]] for some cardinal $\lambda$. Take $\kappa$ to be the maximum of these.

Let $F, G : J \to C$ be $\kappa$-filtered diagrams in $C$ and $F \to G$ a [[natural transformation]] that is degreewise a weak equivalence. Using the functorial factorization provided by the [[small object argument]] this may be factored as $F \to H \to G$ where the first transformation is objectwise an acyclic cofibration and the second objectwise an acyclic fibration, and by functoriality of the factorization this sits over a factorization

$$
  \lim_\to F \stackrel{\simeq}{\hookrightarrow} \lim_\to H \stackrel{}{\to}\lim_\to G
  \,.
$$

It remains to show that the second morphism is a weak equivalence. But by our factorization and by [[category with weak equivalences|2-out-of-3]] applied to our componentwise weak equivalences, we have that all its components $H(j) \to G(j)$ are acyclic fibrations.

At [[small object]] it is described in detail how $\kappa$-smallness of an object $X$ implies that morphisms from $X$ into a $\kappa$-filtered colimit lift to some component of the colimit

$$
  \array{
    \cdots&\to&H(j-1) &\to& H(j) &\to& H(j+1) &\to& \cdots
    \\
    &&&{}^{\mathllap{\exists \hat f}}\nearrow&\downarrow & \swarrow
    \\
    &&X& \stackrel{\forall f}{\to} &\lim_\to H
  }
  \,.
$$

So given a diagram

$$
  \array{
    X &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow
    \\
    Y &\to& \lim_\to G 
  }
$$

we are guaranteed, by the $\kappa$-[[small object|smallness]] of $X$ and $Y$ that we established above, a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} && \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
$$

into some component at $j \in J$ and hence a lift

$$
  \array{
    X &\to& H(j) &\to& \lim_\to H
    \\
    \downarrow^{\mathrlap{\in I}} &
    \nearrow
    & \downarrow^{\in \mathrlap{\in rlp(I)}}
    &&
    \downarrow
    \\
    Y &\to& G(j) &\to& \lim_\to G
  }
  \,.
$$

Thereby $\lim_\to H \to \lim_\to G$ is in $rlp(I) \subset W$.

=--

### Bousfield localization 

Combinatorial model categories, like [[cellular model category|cellular model categories]] have a good theory of [[Bousfield localization of model categories|Bousfield localizations]], at least if in addition they are left [[proper model category|proper]]. See [[Bousfield localization of model categories]] for more on this.

## Examples 

### Basic examples 

Basic examples are

* [[sSet]] with its standard [[model structure on simplicial sets]];

* [[sSet]] with the Joyal-[[model structure for quasi-categories]];

  notice that this is not directly a [[simplicial model category]], but is enriched over itself. A Quillen equivalent combinatorial simplicial model category is

  * the [[model structure for Cartesian fibrations]] over the point.

* the category of [[dendroidal set]]s with its [[model structure on dendroidal sets]].

* the categories of $(n,r)$-[[Theta space]]s.

### Cisinski model structures

More generally, every _[[Cisinski model structure]]_ is combinatorial.

### Derived examples 

Further classes of examples are obtained from such basic examples by localizing presheaf categories with values in these:

* For $V$ a combinatorial model category and $C$ a [[small category]] the injective and projective [[model structure on functors]] $Funct(C,V)_{inj}$ and $Funct(C,V)_{proj}$ are again combinatorial model categories. See there for details.

* If $V$ is a left or right [[proper model category]] then so is $Funct(C,V)_{inj}$ and $Funct(C,V)_{proj}$ and hence the standard results of the theory of [[Bousfield localization of model categories]] applies, which ensures that all left Bousfield localizations $L_S Funct(C,V)$ are again combinatorial model categories. Such local [[model structure on homotopical presheaves|local model structures on homotopical presheaves]] includes notably the local [[model structure on simplicial presheaves]].


### From cofibrantly generated model categories 

Not every [[cofibrantly generated model category]] is also a combinatorial model category. 

For instance:

+-- {: .num_example}
###### (Counter)example
[[Top]] with the standard [[model structure on topological spaces]] is cofibrantly generated, but not combinatorial. But it is [[Quillen equivalence|Quillen equivalent]] to a combinatorial model structure, namely to the standard [[model structure on simplicial sets]] (see [[homotopy hypothesis]]).
=--

One might therefore ask which cofibrantly generated model categories are Quillen equivalent to combinatorial ones.  It turns out that if one assumes the large-cardinal hypothesis [[Vopenka's principle|Vop&#283;nka's principle]], then *every* cofibrantly generated model category is Quillen equivalent to a combinatorial one.  In fact, if we slightly generalize the notion of "cofibrantly generated," this statement is equivalent to Vop&#283;nka's principle.  For a discussion of this see

* [[Jiří Rosický]], _Are all cofibrantly generated model categories combinatorial?_ ([ps](http://www.math.muni.cz/~rosicky/papers/cof1.ps))

Although Vop&#283;nka's principle cannot be proven from [[ZFC]], and in fact is fairly strong as [[large cardinal]] hypotheses go, this means that looking for cofibrantly generated model categories that are not Quillen equivalent to combinatorial ones is probably a waste of time.  Certainly, all known cofibrantly generated model categories *are* Quillen equivalent to simplicial ones, usually in a fairly natural way.

### Simplicial combinatorial model categories 

Those combinatorial model categories that are at the same time [[simplicial model categories]] are precisely those that present [[presentable (∞,1)-categories]].
See [[combinatorial simplicial model category]].


## Related concepts

* [[Ho(CombModCat)]]

* [[Cisinski model structure]]

[[!include locally presentable categories - table]]

[[!include algebraic model structures - table]]

## References 

Much of the theory of combinatorial model categories goes back to [[Jeff Smith]]. Apparently Smith will eventually present a book on this subject. To date, however, his ideas and results appear reproduced in articles of other authors.

After [[Jeff Smith]] presented his recognition theorem at a conference in Barcelona, its first appearance in a publication is apparently lemma 1.8 in 

* {#Beke} [[Tibor Beke]], _Sheafifiable homotopy model categories_, Math. Proc. Cambr. Phil. Soc. 129 (2000), 447&#8211;475 ([arXiv:math/0102087](http://arxiv.org/abs/math/0102087))
 

The definition of combinatorial model categories appears also for instance as 

* {#Lurie} [[Jacob Lurie]], Def. A.2.6.1 in: _[[Higher Topos Theory]]_;
 
* {#Barwick} [[Clark Barwick]], Def. 1.3 in: _On (enriched) left Bousfield localization of model categories_ ([arXiv:0708.2067](http://arxiv.org/abs/0708.2067))

Smith's theorem appears as ([Lurie, A.2.6.10](#Lurie))  and as ([Barwick, prop. 1.7](#Barwick)).

[[Dugger's theorem]] is due to

* {#Dugger01} [[Daniel Dugger]], _[[Combinatorial model categories have presentations]]_, Adv. Math. 164 (2001), no. 1, 177-201 ([arXiv:math/0007068](http://arxiv.org/abs/math/0007068))
 
based on results in

* {#DuggerUniversalHomotopy} [[Dan Dugger]], _[[Universal homotopy theories]]_

Futher details are discussed in:

* [[Jiří Rosický]], *On combinatorial model categories*, Appl. Cat. Str. 17 (2009), 303-316 ([arXiv:0708.2185](https://arxiv.org/abs/0708.2185))

Review:

* [[George Raptis]], *Notes on combinatorial model categories* 2014/2020 ([pdf](https://graptismath.net/files/notes-comb-model-cat.pdf), [[RaptisCombinatorialModelCategories.pdf:file]])

On the [[localization of a 2-category]][[Ho(CombModCat)]] of combinatorial model categories at the [[Quillen equivalences]] and its equivalence to the [[homotopy 2-category]] of (locally) presentable [[derivators]]:

* {#Renaudin06} [[Olivier Renaudin]], *Plongement de certaines théories homotopiques de Quillen dans les dérivateurs*, Journal of Pure and Applied Algebra Volume 213, Issue 10, October 2009, Pages 1916-1935
([arXiv:math/0603339](https://arxiv.org/abs/math/0603339), [doi:10.1016/j.jpaa.2009.02.014](https://doi.org/10.1016/j.jpaa.2009.02.014))
 
See also 

* {#Low14} [[Zhen Lin Low]], _The heart of a combinatorial model category_, Theory and Applications of Categories, Vol. 31, 2016, No. 2, pp 31-62 ([arXiv:1402.6659](http://arxiv.org/abs/1402.6659))

[[!redirects Smith's theorem]]
[[!redirects Smith theorem]]
[[!redirects Smith's theorem]]
[[!redirects Jeff Smith's theorem]]
[[!redirects Jeff Smith theorem]]
[[!redirects Jeff Smith's theorem]]
[[!redirects Smith recognition theorem]]
[[!redirects Smith's recognition theorem]]

[[!redirects combinatorial model categories]]