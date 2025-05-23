
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea 

The _homotopy hypothesis_ is the [[hypothesis]] or [[assertion]] that

* [[∞-groupoids]] are [[equivalence of (infinity,1)-categories|equivalent]] to the [[simplicial localization]] of [[topological spaces]] at their [[weak homotopy equivalences]],

or rather the stronger statement that

* [[n-groupoids]] are equivalent to this localization of those topological spaces which are [[homotopy n-types]] for all [[extended natural numbers]] $n \in \bar{\mathbb{N}}$

and moreover

* this equivalence is induced by the [[fundamental ∞-groupoid]] construction.

What this actually means in detail depends on which definition of [[∞Grpd]] is being used and to which precise incarnation of [[Top]] it is being compared to. 

There are some definitions of [[∞-groupoids]] for which the homotopy hypothesis is a proven _theorem_, notably for the usual definition via [[Kan complexes]] (see at *[[classical model structure on simplicial sets]]*).

Depending on where in the spectrum between [[geometric definitions of higher categories]] and [[algebraic definitions of higher categories]] a given definition of $\infty$-groupoids is located, the statement may be more or less obvious. 

For instance there is some justification for _defining_ an $\infty$-groupoid to _be_ equivalently a topological space considered modulo weak homotopy equivalence (see at *[[classical model structure on topological spaces]]*). For this definition the homotopy hypothesis is of course a tautology.

A definition of $\infty$-groupoid that is still very geometrical but much more combinatorial is that given by [[Kan complexes]]. For these the homotopy hypothesis has a (non-trivial but fairly tractable) proof. The equivalence between Kan complexes and [[CW-complexes]] obtained this way is at the heart of all traditional [[homotopy theory]].

A genuine algebraic definition of $\infty$-groupoids for which the homotopy theory has a (non-trivial but tractable) proof is given by [[algebraic Kan complex]]es. 

However for other algebraic definitions of $\infty$-groupoids not much indication for how to prove the homotopy hypothesis is known. The definition of [[Trimble ∞-category]] stands out as an algebraic definition that has the notion of [[fundamental ∞-groupoid]] built right into it, but also here it seems unclear at the moment how to make progress with proving the homotopy hypothesis.

In fact, generally the homotopy hypothesis is regarded as a _consistency condition_ for definitions in [[higher category theory]]:

* Any definition of [[(n,r)-category]] should be such that there is a [[fundamental infinity-groupoid|fundamental n-groupoid]]-construction with values in the corresponding [[(n,0)-categories]] which makes these equivalent to [[homotopy n-type]]s.

One way to justify this condition is by recourse to the proven cases of the homotopy hypothesis: experience shows that the collections of all three models --  topological spaces, Kan complexes, algebraic Kan complexes -- provide a model for [[∞Grpd]] that supports the general abstract [[higher category theory]] -- specifically [[(∞,1)-category theory]] -- that one expects in analogy to how [[Set]] supports ordinary [[category]] theory.  Any other definition of $\infty$-groupoids is hoped/required to reproduce this, and hence is hoped/required to satisfy the homotopy hypothesis.

Apart from having different models of $\infty$-groupoids that lend themselves more or less to a comparison with topological spaces, there is also the issue as to how to conceive of the notion of _equivalence_ between $\infty$-groupoids.

The usual, unstated, implication is that the notion of _equivalence_ of [[n-groupoid]]s used to model [[homotopy n-type]]s is the appropriate *[[n-category]]-theoretic* notion of [[equivalence of categories|equivalence]].  It is in this way that, for instance, it is known that 1-[[groupoid]]s model homotopy 1-types (see below).

The reason this is important to specify is that there are other notions of equivalence on categorical structures which model homotopy types in other ways.  For example, if we declare a functor between categories to be a weak equivalence iff its [[nerve]] is a weak equivalence of [[simplicial set]]s, then _all_ homotopy types can be modeled by 1-categories in this way; see the [[Thomason model structure]] for 1-categories.

Finally, in analogy to the homotopy hypothesis, there are also attempts to relate general [[(∞,n)-categories]] (not necessarily groupoidal) to [[directed topological space]]s by a [[fundamental (∞,1)-category|fundamental (∞,n)-category]]-construction. There have been claims that a _directed homotopy hypothesis_ can be proven, but at the moment there does not seem to be a published statement.

## Abstract statement {#AbstractStatement}


The following general abstract statement of the homotopy hypothesis is often useful to make explicit.

+-- {: .num_theorem}
###### Theorem

There is an [[equivalence of (∞,1)-categories]]

$(\Pi \dashv |-|) : $ [[Top]]$[W^{-1}]$ $\simeq$ [[∞Grpd]]

where $W$ denotes the weak homotopy equivalences, and $[W^{-1}]$ denotes the $(\infty,1)$-categorical localization.

=--


This statement can be formulated, holds true and is proven  below at least for the standard definitions of these two [[(∞,1)-categories]] (see [section on Kan complexes](#ForKanComplexes), [section on algebraic Kan complexes](#ForAlgebraicKanComplexes)).


## Realizations

We discuss various different definitions of [[n-groupoid]]s and [[∞-groupoid]]s and the formulation and proof of the homotopy hypothesis for them, to the extent that it is available.


### For groupoids

+-- {: .num_prop}
###### Proposition


The [[2-category]] [[Grpd]] of [[groupoid]]s, [[functor]]s, and [[natural transformation]]s is equivalent to the 2-category of [[homotopy n-type|homotopy 1-types]], [[continuous map]]s, and [[homotopy]] classes of homotopies.

=--

See [[homotopy hypothesis for 1-types]] for more.

### For 2-groupoids
 {#For2Groupoids}

(...) [[2-groupoid]]s model all [[homotopy n-type|homotopy 2-type]]s (...)

[[strict 2-groupoid]]s suffice (...) (but note that strict 2-functors are not sufficient to model all maps between 2-types)

### For Gray-groupoids

It is known that not all homotopy 3-types can be modeled by strict 3-groupoids, but that [[Gray-groupoid]]s ([[semi-strict infinity-category|semi-strict 3-groupoids]]) suffice; the obstruction is the [[Whitehead product]] which arises from a nontrivial [[interchanger]]. 

###  For Grothendieck &infin;-groupoids

For a review of progress on proving the homotopy hypothesis for Grothendieck's original conception of &infin;-groupoid in _Pursuing Stacks_, as later developed by [[Georges Maltsiniotis]], see [Henry and Lanari](#HenryLanari)'s 2019 paper.

### For Kan complexes {#ForKanComplexes}

We write $sSet_{Quillen}$ for [[sSet]] equipped with the [[classical model structure on simplicial sets]]. The cofibrant-fibrant objects in $sSet_{Quillen}$ are precisely the [[Kan complexes]].

Also we write $Top_{Quillen}$ for [[Top]] equipped with the [[classical model structure on topological spaces]].

+-- {: .num_theorem}
###### Theorem

There is a [[Quillen equivalence]]

$$
  (|-| \dashv Sing) : Top \stackrel{\overset{|-|}{\leftarrow}}{\underset{Sing}{\to}} sSet_{Quillen} 
  \,,
$$

where the [[left adjoint]] $|-|$ is [[geometric realization]] and the [[right adjoint]] $Sing(-)$ is forming the [[singular simplicial complex]] $Sing(-)$.

This induces an [[equivalence of (∞,1)-categories]] of the corresponding [[presentable (infinity,1)-category|presented]] [[(∞,1)-categories]] 

* [[Top]] $\simeq$ [[∞Grpd]]

=--

([Quillen 67](#Quillen67)), see e.g. ([Goerss-Jardine 96, section I.11](#GoerssJardine96), [Joyal-Tierney 05, chapter I](#JoyalTierney05))

### For algebraic Kan complexes {#ForAlgebraicKanComplexes}

An [[algebraic Kan complex]] is an [[algebraic definition of higher categories|algebraic definition of higher groupoids]] obtained by taking the ordinary definition of [[Kan complex]] and equipping these with _choices_ of [[horn]]-fillers. These choices encode specified composition operations, specified [[associator]]s for these, specified _pentagonators_ and so on.

Algebraic Kan complexes constitute a genuine algebraic model in that they are precisely the [[algebras over a monad]] on [[sSet]].

+-- {: .num_theorem}
###### Theorem

The [[transferred model structure|transferred]] [[model structure on algebraic fibrant objects|model structure on algebraic Kan complexes]] is [[Quillen equivalence|Quillen equivalent]] to the standard [[model structure on simplicial sets]]

$$
  (F \dashv U) : Alg Kan \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}  
   sSet_{Quillen}
  \,.
$$

=--

+-- {: .proof}
###### Proof

The proof is spelled out at [[model structure on algebraic fibrant objects]].

=--

+-- {: .num_remark}
###### Remark


With the above [homotopy hypothesis-theorem for Kan complexes](ForKanComplexes) this gives a zig-zag of Quillen equivalences between $Alg Kan$ and $Top$

$$
  Alg Kan 
    \stackrel{\overset{F}{\leftarrow}}{\underset{U}{\to}}  
   sSet_{Quillen}
     \stackrel{\overset{|-|}{\to}}{\underset{Sing}{\leftarrow}}
    Top
  \,.
$$

This already yields the homotopy hypothesis for algebraic Kan complexes at the level of the corresponding [[presentable (∞,1)-category|presented (∞,1)-categories]] (as discussed there)

$$
  Alg C^\circ \simeq Top^\circ
  \,.
$$

=--

But there is also a direct Quillen equivalence:

+-- {: .num_def}
###### Definition

Write $\Delta^n$ and $\Lambda^n_k$ for the topological $n$-[[simplex]] and its $k$-[[horn]].

Fix any choice of [[retract]]s 


$$
  R(n,k) : \Delta^n \to \Lambda^n_k
$$

for all topological [[horn]] inclusions $\Lambda^n_i \hookrightarrow \Delta^n$. 

For $X$ any [[topological space]] equip the [[singular simplicial complex]] $Sing X$ with the stucture of an [[algebraic Kan complex]] by taking the filler of $\Lambda_k[n] \to Sing X$ to be given by the $(|-| \dashv Sing)$-[[adjunct]] of $\Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k \to X$. Write $\Pi_\infty(X) \in Alg Kan$ for the resulting algebraic Kan complex.

This construction constitutes a functor

$$ 
  \Pi_\infty(-) : Top \to Alg C
  \,,
$$


with $U \Pi_\infty = Sing$.

=--

+-- {: .num_remark}
###### Remark

The choices of fillers in $\Pi_\infty(X)$ may be thought of as explicit choice of reparameterizations of paths in $X$. These choices are arbitrary, but by the general statement at [[model structure on algebraic fibrant objects]], any two chocies yield equivalent objects.

=--

+-- {: .num_def}
###### Definition

Given choices $R(-,-)$ of horn retracts as above, define a functor

$$
  |-|_r : Alg Kan \to Top
$$

called **reduced geometric realization** by taking it on an object $A \in Alg Kan$ to be given by the [[coequalizer]]

$$
  |A|_r := \lim_{\to}(\coprod_{\Lambda[n]_k \to A} \Delta^n \stackrel{\to}{\to} |U A|)
  \,,
$$

where $|U A|$ is the ordinary [[geometric realization]] of the underlying simplicial set of $A$ and where the two maps are

1. the image under $|-|$ of the distinguished fillers $\Delta[n] \to U A$ of $A$;

1. the composite $\Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k \to |U X|$ .


=--

+-- {: .num_prop}
###### Proposition

The functor $|-|_r$ is [[left adjoint]] to $\Pi_\infty$.

$$
  (|-|_r \dashv \Pi_\infty)
  \,.
$$

=--

This is ([Nikolaus, prop. 3.4](#Nikolaus)).

+-- {: .proof}
###### Proof

We check the hom-isomorphism. A morphism $f : |A|_r \to X$ is
by definition of the coequalizer the same as a map $\tilde f : |A| \to X$ such that for each horn $h : \Lambda[n]_k \to A$ with distinguished filler $\hat h : \Delta[n] \to A$ the composites

$$
  \Delta^n \stackrel{R(n,k)}{\to} \Lambda^n_k 
  \stackrel{|h|}{\to} |U A|
  \stackrel{\tilde f}{\to}
  X
$$

and

$$
  \Delta^n \stackrel{|\hat h|}{\to} |U A| \stackrel{\tilde f}{\to} X
$$

are equal. This means equivalently that the $(|-| \dashv Sing)$-[[adjunct]] $\tilde \tilde f : U A \to Sing X$ sends distinguished fillers in $A$ to distinguished fillers in $\Pi_\infty(X)$ and is hence a morphism in $Alg Kan$.

This construction shows that the map $(f : |A|_r \to X) \mapsto (\tilde \tilde f : A \to \Pi_\infty(X))$ thus obtained is a bijection.

=--

+-- {: .num_theorem}
###### Theorem

We have an identity:

$$
  \array{
    && Alg Kan
    \\
    & {}^{\mathllap{U}}\swarrow 
    & \Downarrow^{=}& 
    \nwarrow^{\mathrlap{\Pi_\infty}}
    \\
    sSet &&\underset{Sing}{\leftarrow}&& Top
  }
$$

and a [[natural isomorphism]]

$$
  \array{
    && Alg Kan
    \\
    & {}^{\mathllap{F}}\nearrow 
    & \Downarrow^{\simeq}& 
    \searrow^{\mathrlap{|-|_r}}
    \\
    sSet &&\underset{|-|}{\to}&& Top
  }
  \,.
$$


=--

This is ([Nikolaus, corollary 3.5](#Nikolaus))

+-- {: .proof}
###### Proof

The identity is evident by definition of $\Pi_\infty$. 

Using this, we have that 

$$
  (|-|_r \circ F \dashv U \circ \Pi_\infty = Sing)
  \,.
$$

So $|-|_r \circ F$ is another [[left adjoint]] to $Sing$ and hence naturally isomorphism to $|-|$.

=--


+-- {: .num_corollary}
###### Corollary


The adjunction 

$$
  (|-|_r \dashv \Pi_\infty)
  : 
  Alg C \to Top
$$

constitutes a [[Quillen equivalence]]


=--

This is [Nikolaus, corollary 3.6](#Nilkolaus)

+-- {: .proof}
###### Proof

By the above theorem and the <a href="http://ncatlab.org/nlab/show/Quillen+equivalence#TwoOutOfThree">2-out-of-3-property</a> of Quillen equivalences.

=--

### For cubical sets {#Cubical}

Also [[cubical set]]s may serve as a model for homotopy theory.

There is an evident [[simplicial set]]-valued [[functor]]

$$
  \Box \to sSet
$$

from the [[cube category]] to [[sSet]], which sends the cubical $n$-cube to the simplicial $n$-cube

$$
  \mathbf{1}^n \mapsto (\Delta[1])^{\times n}
  \,.
$$

Similarly there is a canonical [[Top]]-valued functor

$$
  \Box \to Top
$$

$$
  \mathbf{1}^n \mapsto (\Delta^1_{Top})^n
  \,.
$$

The corresponding [[nerve and realization]] [[adjunction]]

$$
  (|-| \dashv Sing_\Box) : Top \stackrel{\overset{|-|}{\leftarrow}}{\underset{Sing_\Box}{\to}} Set^{\Box^{op}}
$$

is the cubical analogue of the simplicial nerve and realization discussed [above](#ForKanComplexes).

+-- {: .num_theorem}
###### Theorem


There is a [[model structure on cubical sets]] $Set^{\Box^{op}}$ whose

* weak equivalences are the morphisms that become weak equivalences under geometric realization $|-|$;

* cofibrations are the [[monomorphism]]s.

=--

This is [Jardine, sections 3.](#Jardine)

+-- {: .num_theorem}
###### Theorem

The [[unit of an adjunction|unit of the adjunction]]

$$
  A \to Sing_\Box(|A|)
$$

is a weak equivalence in $Set^{\Box}$ for every cubical set $A$.

The counit of the adjunction

$$
  |Sing_\Box X| \to X
$$

is a weak equivalence in $Top$ for every topological space $X$.

It follows that we have an [[equivalence of categories]] induced on the [[homotopy categories]]

$$
  Ho(Top) \simeq Ho(Set^{\Box^{op}})
  \,.
$$

=--

This is [Jardine, theorem 29, corollary 30](#Jardine).

### For $cat^n$ groups and $n+1$-fold groupoids

Loday's notion of a [[cat-n-group]] corresponds to the connected version of an $n+1$-fold groupoid.  We will restrict our discussion to that connected case.

+-- {: .num_theorem}
###### Theorem

The [[homotopy category]] of [[cat-n-group]]s is equivalent to that of [[pointed object|pointed]] [[connected]] [[homotopy n-type|homotopy n+1-type]]s.

=--

This is proven in ([Loday](#Loday)). (There are some glitches in his proof and these were fixed by various authors (Steiner, Gilbert, ..) and then detailed proofs were given by Bullejos, Cegarra, Duskin and separately, using the equivalent formulation of crossed n-cubes, by Porter. Detailed references and some more commentary is at [[cat-n-group]].)


### For Segal-groupoids

+-- {: .num_prop}
###### Proposition


There is realization/singular complex [[adjunction]]

$$
  (|-| \dashv sSing) : Top \to SegalGrpd 
$$

for [[Segal groupoid]]s, 


Its unit is an equivalence of [[Segal categories]] and its counit a [[weak homotopy equivalence]] of topological spaces.

=--

+-- {: .proof}
###### Proof

This is lemma 6.3.21 and corollary 6.3.24 in ([Pellissier](#Pellissier))

=--

### For strict $\omega$-categories with weak inverses
 {#ForStrictOmegaCategoriesWithWeakInverses}

While [[strict omega-groupoids]] in the sense of 
[[strict omega-categories]] with _strict_ inverses are far from modelling all homotopy types, strict $\omega$-categories with all _weak_ inverses come closer. In ([Kapranov-Voevodsky](#KapranovVoevodsky)) it was argued that these are in fact sufficient, but a mistake in the argument was found in ([Simpson, Cor. 5.2](#Simpson)) (see also [here](Simpson%27s+conjecture#History)).

The issue however is somewhat subtle, as highlighted by Voevodsky [here](http://ncatlab.org/nlab/show/homotopy+type+theory#VoevodskyIASTalk2014).
For more on this see at _[[Simpson's conjecture]]_.


### For diagrammatic $(\infty, 0)$-categories.{#ForDgmSet}
[[diagrammatic set|Diagrammatic sets]] are a topologically sound alternative to [[computad|polygraphs]]: a diagrammatic set is a presheaf over the [[atom category]], whose objects include many of the [[geometric shape for higher structures]]. 

There, an $(\infty, \infty)$-category is a diagrammatic set in which any suitable assemblage of $n$-cells can be composed, via a $(n + 1)$-cell, into a single $n$-cell. For $0 \le n \le \infty$, an $(\infty, n)$-category is an $(\infty, \infty)$-category in which all cells of dimension $\gt n$ are "weakly invertible". 

\begin{theorem}
There is a model structure on diagrammatic sets whose fibrant objects are exactly the $(\infty, 0)$-categories and which is Quillen equivalent to the standard model structure on simplicial sets. 
\end{theorem}      
\begin{proof}
This is [Corollary 5.8](#ChanavatHadzihasanovic2024Model).
\end{proof}


## Generalizations

### For stratified spaces

For a [[categorified]] version which finds an equivalence for $(\infty, 1)$-categories, see [[stratified homotopy hypothesis]] ([Ayala-Francis-Rozenblyum](#AFR15)).

### For spectra

For a stabilized version which finds an equivalence between stable homotopy types (i.e. [[spectra]]) and symmetric monoidal $\infty$-groupoids, see [[stable homotopy hypothesis]] ([Johnson-Osorno](#JO12), [Gurski-Johnson-Osorno](#GJO17))


## References and a bit of history.
 {#References}

The equivalence between the [[classical model structure on topological spaces|classical homotopy theory of topological spaces]] and the [[classical model structure on simplicial sets|homotopy theory of Kan complexes]] is due to 

* {#Quillen67} [[Daniel Quillen]], _Homotopical Algebra_, LNM 43, Springer, (1967) 

Later in 

* [[Alexander Grothendieck]], _[[Pursuing Stacks]]_, 1983  (including and especially the 'letter to [[Daniel Quillen]]' given  on the first few pages),

it was argued that there were [[algebraic definitions of higher categories|algebraic definitions of higher groupoids]] that could be put forward,  so that the resulting objects ought to have a homotopy theory equivalent to the classical homotopy theory of topological spaces, and, moreover, would provide useful tools in the interpretation of [[non-abelian cohomology]] classes. This extended ideas that Grothendieck had explored in letters to [[Larry Breen]] in the mid 1970s in which he had given a sketch of a theory of $n$-stacks and their relation with the homotopy $n$-type of a space or more generally a topos.

At this stage, (in the  1970s and early 1980s) more _geometric_ or _combinatorial_ definitions of infinity categories were not yet available, or, perhaps more accurately, had been discovered, but were not _recognised_ as having such an infinity categoric interpretation; see [[Tim Porter]]'s Letter to Grothendieck (16 June 1983) and the discussion [[Spaces as infinity-groupoids.pdf|here:file]]  in [[New Spaces for Mathematics and Physics]]. These models included Kan complexes which now are interpreted as being one model for infinity groupoids, and [[quasicategory|weak Kan complex]]es, as put forward by Boardman and Vogt, which give one of the main models for (weak) $(\infty,1)$-categories. From this perspective, Quillen's result can be seen as being a precursor of one form of the Homotopy Hypothesis.

The name "Homotopy Hypothesis" for this statement is due to 

* [[John Baez]], _The Homotopy Hypothesis_, 2007 ([web](http://math.ucr.edu/home/baez/homotopy/), [pdf](http://math.ucr.edu/home/baez/homotopy/homotopy.pdf))

More recently [[Georges Maltsiniotis]] has revived the approach to $\infty$-groupoids that Grothendieck initiated in _Pursuing Stacks_ - see [[Grothendieck ∞-groupoids]] - and work has begun on proving the homotopy hypothesis for Grothendieck ∞-groupoids.  For a review of progress so far, see:

* {#HenryLanari} [[Simon Henry]], [[Edoardo Lanari]], *On the homotopy hypothesis in dimension 3*, Theory and Applications of Categories **39** 26 (2023) 735-768 &lbrack;[arxiv/1905.05625](https://arxiv.org/abs/1905.05625), [tac:39-26](http://www.tac.mta.ca/tac/volumes/39/26/39-26abs.html), [pdf](http://www.tac.mta.ca/tac/volumes/39/26/39-26.pdf)&rbrack;.

These authors have reduced the hypothesis to a conjecture which has so far been proved only up to dimension 3, hence the title of their paper.

Technical reviews of Quillen's proof of a version of the homotopy hypothesis include:

* {#GoerssJardine96} [[Paul Goerss]], [[Rick Jardine]], section I.11 of _[[Simplicial homotopy theory]]_, 1996

* {#JoyalTierney05} [[André Joyal]], [[Myles Tierney]] _An introduction to simplicial homotopy theory_, 2005  ([chapter I](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01), more notes [pdf](http://mat.uab.cat/~kock/crm/hocat/advanced-course/Quadern47.pdf))

The homotopy hypothesis for strict $\omega$-categories with weak inverses is discussed in

* {#KapranovVoevodsky} [[Mikhail Kapranov]], [[Vladimir Voevodsky]], _$\infty$-groupoids and homotopy types_, Cahiers de Topologie et G&#233;om&#233;trie Diff&#233;rentielle Cat&#233;goriques, 32 no. 1 (1991), p. 29-46 
 
but a mistake in the argument was pointed out in Corollary 5.2 of

* {#Simpson} [[Carlos Simpson]], _Homotopy types of strict 3-groupoids_ ([arXiv:math/9810059](http://arxiv.org/abs/math/9810059))
 
The homotopy hypothesis for [[algebraic Kan complexes]] is established and discussed in

* [[Thomas Nikolaus]], _Algebraic models for higher categories_ ([arXiv](http://arxiv.org/abs/1003.1342))
{#Nikolaus}

For progress on 

The homotopy hypothesis for [[Segal groupoids]] is formulated in section 6.3.4 of

* Regis Pellissier, _Weak enriched categories - Categories enrichies faibles_ PhD Thesis (2002) ([arXiv:math/0308246](http://arxiv.org/abs/math/0308246))

Models of homotopy $n$-types by $Cat^n$-groups are discussed in

* [[Jean-Louis Loday]], _Spaces with finitely many non-trivial homotopy groups_, J. Pure Appl. Algebra 24 (1982), 179-202.
{#Loday}

More literature on models of homotopy types by strict higher groupoids is at

* [[Ronnie Brown]], _Computing Homotopy Types Using Crossed $N$-Cubes of Groups_ ([arXiv](http://arxiv.org/abs/math/0109091))

* [[Simona Paoli]], _Internal categorical structures in homotopical algebra_, to appear in _[[johnbaez:Towards Higher Categories]]_, eds. [[John Baez]] and [[Peter May]]  ([pdf](http://www.maths.mq.edu.au/~simonap/paoli_IMA.pdf))

The first paper,  as its title suggests, has an emphasis on using higher groupoids for computation of homotopical invariants, in fact by applying higher homotopy van Kampen Theorems.  These theorems lead to algebraic colimit arguments in algebraic topology, implying  results, often nonabelian,  not obtainable by other methods. It is also remarkable that the precision of these results requires the use of strict structures, whereas the current emphasis in higher category theory is on non strict structures. 

The homotopy theory of [[cubical set]]s is discussed in 

* Jardine, _Model structure on cubical sets_ ([pdf](http://hopf.math.purdue.edu/Jardine/cubical2.pdf))
{#Jardine}

* Maltsiniotis, G. La cat&#233;gorie cubique avec connexions est une cat&#233;gorie
  test stricte. Homology, Homotopy Appl. 11, (2) (2009) 309--326.

Cubical methods are also essential in 

*  R. Brown, P.J. Higgins, R. Sivera,  _Nonabelian algebraic
topology: filtered spaces, crossed complexes, cubical homotopy
groupoids_, EMS Tracts in Mathematics Vol. 15, 703 pages. (August
2011).

Diagrammatic $(\infty, 0)$-category are discussed in

* {#ChanavatHadzihasanovic2024Homotopy} Chanavat, Hadzihasanovic, _Diagrammatic sets as a model of homotopy types_, 2024 ([arXiv:2407.06285](https://arxiv.org/abs/2407.06285v1))

* {#ChanavatHadzihasanovic2024Model} Chanavat, Hadzihasanovic, _Model structures for diagrammatic $(\infty,n)$-categories_, 2024 ([arXiv:2410.19053](https://www.arxiv.org/abs/2410.19053))

A version for [[stratified spaces]] is discussed in

* {#AFR15} [[David Ayala]], [[John Francis]], [[Nick Rozenblyum]], *A stratified homotopy hypothesis*, [arXiv](http://arxiv.org/abs/1502.01713)

A version for [[spectra]] is discussed in

* {#JO12} [[Niles Johnson]] and [[Angelica Osorno]], *Modeling stable one-types*, [tac](http://tac.mta.ca/tac/volumes/26/20/26-20abs.html)

* {#GJO17} [[Nick Gurski]], [[Niles Johnson]], and [[Angelica Osorno]], *The 2-dimensional stable homotopy hypothesis*, [arxiv](https://arxiv.org/abs/1712.07218)
