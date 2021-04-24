
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--

# Contents 
* table of contents
{: toc}

## Idea
 {#Idea}

A _compact Hausdorff space_ or _compactum_, for short, is a [[topological space]] which is both a [[Hausdorff space]] as well as a [[compact space]].
This is precisely the kind of topological space in which every [[limit of a sequence|limit]] of a [[sequence]] or more generally of a [[net]] that should exist does exist ([this prop.](net#CompactSpacesEquivalentlyHaveConvergetSubnets)) and does so uniquely ([this prop](#NetsDetectHausdorff)). 

One may consider the analogous condition for [[convergence spaces]], or for [[locales]] (see also at _[Hausdorff locale](Hausdorff+space#HausdorffLocale)_ and _[[compact locale]]_). Even though these are all different contexts, the resulting notion of compactum is (at least assuming the [[axiom of choice]]) always the same.  Interestingly, there is even an algebraic definition, not one that uses only finitary operations, but one which uses a [[monad]]. 


## Definitions

If you know what a [[compact space]] is and what a [[Hausdorff space]] is, then you know what a compact Hausdorff space is, so let\'s be fancy. (Full justifications will be provided in section on [compacta as algebras](compactum#algebras).) 

Given a [[set]] $S$, let $\beta S$ be the set of [[ultrafilters]] on $S$.  Note that $\beta$ is an [[endofunctor]] on [[Set]]; every [[function]] $f: S \to T$ induces a function $\beta f: \beta S \to \beta T$ using the usual application of functions to [[filters]].  In fact, $\beta$ is a [[monad]]; it comes with a [[natural transformation|natural]] (in $S$) unit $\eta_S: S \to \beta S$, which maps a point $x$ to the [[principal ultrafilter]] that $x$ generates, and multiplication $\mu_S: \beta \beta S \to \beta S$, which maps an ultrafilter $U$ on ultrafilters to the ultrafilter of sets whose principal ultrafilters of ultrafilters belong to $U$.  That is,

*  $ A \in \eta x \;\Leftrightarrow\; x \in A $, so $ \eta x = \{ A \subseteq S \;|\; x \in A \} $;
*  $ A \in \mu U \;\Leftrightarrow\; \{ F \in \beta S \;|\; A \in F \} \in U $.

Then a __compactum__ is simply an [[algebra for a monad|algebra]] for this monad; that is, a set $X$ together with a function $\lim: \beta X \to X$, such that

*  each point $x$ is the limit ($\lim$) of the principal ultrafilter $\eta x$, and
*  given an ultrafilter $U$ on ultrafilters, the limit of $\mu U$ is the limit of $(\beta \lim) U$.

It is then a theorem that this $\lim$ generates a [[convergence space|convergence]] on $S$ that is [[compact space|compact]], [[Hausdorff space|Hausdorff]], and [[topological space|topological]].  The converse, that every compact Hausdorff topological convergence is of this form, is equivalent to the [[ultrafilter principle]].

Every compact Hausdorff space is [[regular space|regular]] and [[sober space|sober]] and so defines a compact regular locale.  Again, the [[axiom of choice]] gives us a converse: every compact regular locale is spatial and so comes from a compactum.
>Probably this is also equivalent to the ultrafilter principle, but I need to check.

Note that every compact Hausdorff space (topological or localic) is not only regular but also [[normal space|normal]]. See _[[compact Hausdorff spaces are normal]]_.


## Compacta as algebras {#algebras} 

Throughout this section, $CH$ will be used to denote the category of compact Hausdorff spaces (compacta). 

### The space of ultrafilters 

Let $Bool$ be the category of [[Boolean algebras]]. The functor $\hom(-, \mathbf{2}): Bool^{op} \to Set$ has a left [[adjoint]] $P: Set \to Bool^{op}$ given by power sets, and we define the **ultrafilter monad** to be the composite $\beta \coloneqq \hom(P -, \mathbf{2})$. 

For a set $S$, [[topology|topologize]] $\beta S$ by declaring a basic [[open set]] to be one of the form 

$$\hat{A} \coloneqq \{F \in \beta S: A \in F\}$$ 

for $A$ a subset of $S$. Notice $\hat{\emptyset}$ is [[empty set|empty]]. Indeed, $\widehat{(-)}$ defines a Boolean algebra map 

$$P(S) \to P(\beta S)$$ 

so that in particular $\widehat{A \cap B} = \hat{A} \cap \hat{B}$, which immediately implies that the $\hat{A}$ form a [[basis]] of a topology. 

+-- {: .num_remark #rem} 
###### Remark 
In fact, $\widehat{(-)}$ is the component at $P(S)$ of the counit of the adjunction $P \dashv \hom(-, \mathbf{2})$, as a morphism in $Bool^{op}$. If $f: S \to T$ is a function, the commutativity of the naturality square 

$$\array{
P(T) & \stackrel{\widehat{(-)}}{\to} & P(\beta T) \\
\mathllap{P(f)} \downarrow & & \downarrow \mathrlap{P(\beta f)} \\ 
P(S) & \overset{\widehat{(-)}}{\to} & P(\beta S)
}$$

implies that if $U = \hat{B} \in P(\beta T)$ is a basic (cl)open, then so is 
$(\beta f)^{-1}(U) = P(\beta f)(\hat{B}) = \widehat{f^{-1}(B)}$. It then follows that $\beta f$ is continuous. 
=-- 

These results show that the monad $\beta: Set \to Set$ lifts through the forgetful functor $U: Top \to Set$. 

The _unit_ of the monad $\beta$ is given componentwise by functions 

$$prin_X: X \to \beta X$$ 

where $prin_X$ takes $x \in X$ to the principal ultrafilter 

$$prin_X(x) = \{A \in P(X): x \in A\}.$$ 

It is evident that $prin_X$ is injective. 

+-- {: .num_prop #dense} 
###### Proposition 
The injection $prin_X: X \to \beta X$ exhibits $X$ as a [[dense subset]] of $\beta X$. 
=-- 

+-- {: .proof} 
###### Proof 
If $\hat{A}$ is a basic open neighborhood containing an ultrafilter $F$, then $A$ is nonempty and hence contains some $x \in X$, which is to say $A \in prin_X(x)$ or that $prin_X(x) \in \hat{A}$. 
=-- 


### Ultrafilters form a compactum 

+-- {: .num_prop} 
###### Proposition 
$\beta S$ is [[Hausdorff space|Hausdorff]]. 
=-- 

+-- {: .proof}
###### Proof 
Let $F, G$ be distinct ultrafilters, so there is $A \subseteq S$ with $A \in F$ and $\neg A \in G$. Then $\hat{A}$ and $\widehat{\neg A}$ are disjoint neighborhoods which contain $F$ and $G$ respectively. 
=-- 

+-- {: .num_prop} 
###### Proposition 
$\beta S$ is [[compact space|compact]]. 
=-- 

+-- {: .proof} 
###### Proof 
It is enough to show that if $\mathcal{O}$ is a collection of opens such that the union of any finite subcollection is a proper subset, then the union of $\mathcal{O}$ is also proper. 

If $\mathcal{O}$ covers $U$, it admits a refinement by basic clopens also covering $U$, and thus we may assume WLOG that $\mathcal{O}$ consists of basic clopens $\hat{A}$. If every finite union of elements of $\mathcal{O}$ is a proper subset of $\beta S$, then every finite intersection $\widehat{\neg A_1} \cap \ldots \cap \widehat{\neg A_n}$ is nonempty, so that the $\neg A$ generate a filter, which is contained in some ultrafilter $F$. This $F$ lies outside the union of all the $\hat{A}$'s. 
=-- 

### Convergence 

+-- {: .num_defn}
###### Definition 
Let $X$ be a topological space, and $F$ an ultrafilter on the underlying set $U X$. We say $F$ _converges_ to a point $x$ (in symbols, $F \rightsquigarrow x$) if the [[neighborhood|neighborhood filter]] $N_x$ of $x$ is contained in $F$. 
=-- 

Convergence defines a [[relation]] $\xi$ from $\beta(U X)$ to $U X$. 

+-- {: .num_prop} 
###### Proposition 
If $X$ is Hausdorff, then the relation $\xi$ is well-defined, or [[functional relation|functional]] (i.e., there is at most one point to which a given ultrafilter $F$ converges). 
=-- 

+-- {: .proof} 
###### Proof 
If $x \neq y$, then there are disjoint neighborhoods $U$, $V$ of $x$ and $y$. We cannot have both $U \in F$ and $V \in F$ (otherwise $\emptyset = U \cap V$ would be an element of $F$), so at most one of the neighborhood filters $N_x, N_y$ can be contained in $F$. 
=-- 

+-- {: .num_prop} 
###### Proposition 
If $X$ is compact, then the relation $\xi$ is [[total relation|total]] (i.e., there exists a point to which a given ultrafilter $F$ converges). 
=-- 

+-- {: .proof} 
###### Proof 
If not, then for each $x \in X$ there is an open neighborhood $U_x$ that does not belong to $F$. Then $\neg U_x \in F$. Some finite number of neighborhoods $U_{x_1}, \ldots, U_{x_n}$ covers $X$. Then $\neg U_{x_1} \cap \ldots \cap \neg U_{x_n} = \emptyset \in F$, which is a contradiction. 
=-- 

+-- {: .num_prop #coun} 
###### Proposition 
If $X$ is compact Hausdorff, then the function $\xi: \beta(U X) \to X$ is continuous. 
=-- 

+-- {: .proof} 
###### Proof 
Let $U$ be an open neighborhood of $x \in X$; we must show that $\xi^{-1}(U)$ contains an open neighborhood of any of its points (i.e., ultrafilters $F$ such that $F \rightsquigarrow x$). Since $X$ is $T_3$ ([[separation axioms|Hausdorff regular]]), we may choose a neighborhood $V \in N_x$ whose closure $\bar{V}$ is contained in $U$. Then $\hat{V}$ is an open neighborhood of $F$ in $\beta(U X)$, and we claim $\hat{V} \subseteq \xi^{-1}(U)$. 

For this, we must check that if $G \in \hat{V}$ and $G \rightsquigarrow y$, then $y \in U$. But if $y \in \neg U \subseteq \neg \bar{V}$, then $\neg \bar{V} \in N_y$, whence $G \rightsquigarrow y$ implies $\neg \bar{V} \in G$. This contradicts $G \in \hat{V}$, i.e., contradicts $V \in G$, since $V \cap \neg \bar{V} = \emptyset$. 
=-- 

### Spaces of ultrafilters are universal 

+-- {: .num_prop #exist} 
###### Proposition 
If $S$ is a set and $X$ is a compact Hausdorff space, then any function $f: S \to X$ can be extended (along $prin_S: S \to \beta S$) to a continuous function $\hat{f}: \beta S \to X$. 
=-- 

+-- {: .proof} 
###### Proof 
We define $\hat{f}$ to be the composite 

$$\beta S \stackrel{\beta(f)}{\to} \beta (U X) \stackrel{\xi}{\to} X$$ 

where $\beta(f)$ is continuous by Remark \ref{rem} and $\xi$ is continuous by Proposition \ref{coun}. It remains to check that the following diagram is commutative: 

$$\array{
S & \stackrel{f}{\to} & U X & & \\
\mathllap{prin_S} \downarrow & & \mathllap{prin_{U X}} \downarrow & \searrow \mathrlap{1_{U X}} & \\
\beta S & \underset{\beta (f)}{\to} & \beta (U X) & \underset{\xi}{\to} & U X.
}$$ 

The square commutes by naturality of $prin$, and commutativity of the triangle simply says that the ultrafilter $prin_{U X}(x)$ converges to $x$, or that $N_x \subseteq prin(x)$, which reduces to the tautology that $x \in V$ for every neighborhood $V \in N_x$. 
=-- 

+-- {: .num_theorem #free} 
###### Theorem 
For any set $S$, the function $prin_S: S \to \beta S$ is [[universal property|universal]] among functions from $S$ to compact Hausdorff spaces. Hence the functor $F: Set \to CH$ that takes $S$ to the compact Hausdorff space $\beta S$ is [[left adjoint]] to the forgetful functor $CH \to Set$. 
=-- 

+-- {: .proof} 
###### Proof 
Proposition \ref{exist} shows that for any function $f: S \to U X$ to a compact Hausdorff space, there exists continuous $g: \beta S \to X$ such that $g \circ prin_S = f$. All that remains is to establish uniqueness of such $g$. But if two maps $g, g': \beta S \to X$ to a Hausdorff space $X$ agree on a dense subspace, in this case the subspace $prin_S : S \hookrightarrow \beta S$ by Proposition \ref{dense}, then they must be equal. Indeed, the pullback of the closed diagonal defines a closed subspace $D$ of $\beta S$,

$$\array{
D & \to & X \\
\downarrow & & \downarrow \mathrlap{\delta_X} \\
\beta S & \underset{\langle g, g' \rangle}{\to} & X \times X,
}$$ 

and $D$ contains a dense subspace $S$, therefore $D = \beta S$; i.e., the equalizer of $g$ and $g'$ is all of $\beta S$, hence these two maps are equal. 
=-- 

### Compact Hausdorff spaces are monadic over sets 

We recall hypotheses of Beck's precise [[monadicity theorem]]: a functor $U: C \to D$ is monadic if and only if 

1. $U$ has a left adjoint, 

1. $U$ reflects isomorphisms: a morphism $f: X \to Y$ of $C$ is an isomorphism if $U f: U X \to U Y$ is an isomorphism in $D$, 

1. $D$ has, and $U$ preserves, coequalizers of parallel pairs that are $U$-split. (We say 
$$X \stackrel{\overset{f}{\to}}{\underset{g}{\to}} Y$$ 
is $U$-**split** if there is a coequalizer 
$$U X \stackrel{\overset{U f}{\to}}{\underset{U g}{\to}} U Y \stackrel{h}{\to} Z$$ 
that is split in $D$: there exists $i: Z \to U Y$ and $j: U Y \to U X$ such that $U h \circ i = 1_Z$, $U g \circ j = i \circ h$, and $U f \circ j = 1_{U Y}$.) 

In the case where $D = Set$, we have the following useful lemma: 

+-- {: .num_lemma #split} 
###### Lemma 
Suppose given a coequalizer in $Set$ 

$$X \stackrel{\overset{f}{\to}}{\underset{g}{\to}} Y \stackrel{h}{\to} Z$$ 

split by $i: Z \to Y$, $j: Y \to X$ (so that $f j = 1_Y$, $h i = 1_Z$, $g j = i h$). Let $R \hookrightarrow Y \times Y$ be the image of $\langle f, g \rangle : X \to Y \times Y$, and let $\langle p_1, p_2 \rangle : E \to Y \times Y$ be the equivalence relation given by the kernel pair $(p_1, p_2)$ of $h$. Then $E = R \cdot R^{op}$, the relational composite given by taking the image of the [[span]] composite $R \times_Y R^{op} \to Y \times Y$. 
=-- 

+-- {: .proof} 
###### Proof 
Clearly $R \subseteq E$ since $h f = h g$, and we have $R^{op} \subseteq E^{op} = E$ and $R \cdot R^{op} \subseteq E \cdot E \subseteq E$ by symmetry and transitivity of $E$. In the other direction, suppose $(y_1, y_3) \in E$, so that $h(y_1) = h(y_3)$. Put $x = j(y_1)$ and $x' = j(y_3)$ (so that $f(x) = y_1$ and $f(x') = y_3$), and put $y_2 = g(x)$. Clearly then $(y_1, y_2) \in R$. Moreover, 

$$y_2 = g(x) = g j(y_1) = i h(y_1) = i h(y_3) =  g j(y_3) = g(x')$$ 

so that $(y_3, y_2) \in R$, or $(y_2, y_3) \in R^{op}$. Hence $(y_1, y_3) \in R \cdot R^{op}$, and we have shown $E \subseteq R \cdot R^{op}$. 
=-- 

+-- {: .num_theorem} 
###### Theorem 
The forgetful functor $U: CH \to Set$ is monadic. 
=-- 

+-- {: .proof} 
###### Proof 
By theorem \ref{free}, $U$ has a [[left adjoint]]. Since [[bijection|bijective]] continuous maps between compact Hausdorff spaces are homeomorphisms, we have that $U$ reflects isomorphisms. Finally, suppose $(f, g)$ is a $U$-split pair of morphisms $X \to Y$ in $CH$; let $h: Y \to Z$ be their coequalizer in $Top$, given by a suitable quotient space. Being a quotient of a compact space, $Z$ is compact. Since $CH$ is a full subcategory of $Top$, the map $h$ is a coequalizer in $CH$ once we prove the following claim:  

* **Claim:** $Z$ is Hausdorff. 

Furthermore, since the forgetful functor $Top \to Set$ has a right adjoint (given by taking indiscrete topologies on sets), the underlying function of $h$ (again denoted $h$) is the coequalizer of $(U f, U g)$ in $Set$, so that $U$ would preserve the claimed coequalizer. 

In other words, to complete the proof, it suffices to verify the claim. Letting $p_0, p_1: E \stackrel{\to}{\to} Y$ be the kernel pair of $h$ in $Top$, to show $Z = Y/E$ is Hausdorff, it suffices to prove that the equivalence relation $\langle p_0, p_1 \rangle : E \to Y \times Y$ in $Top$ is closed. Let $R \hookrightarrow Y \times Y$ be the image of $\langle f, g \rangle: X \to Y \times Y$. By lemma \ref{split}, the subset $E$ of $U Y \times U Y$ coincides with the subset $R \cdot R^{op} \subseteq U Y \times U Y$. Now $R$ is the image of the compact space $X$ under the continuous map $\langle f, g \rangle$, so $R$ is a closed subset of $Y \times Y$. Similarly $R^{op}$ is a closed subset of $Y \times Y$. Under their subspace topologies, their fiber product $R \times_Y R^{op}$ is compact, and so its image $R \cdot R^{op}$ under the (continuous) span composite $R \times_Y R^{op} \to Y \times Y$ is also closed. This completes the proof. 
=-- 


## Weak versions

Every [[Hausdorff space]], hence every compactum, satisfies the [[separation axiom]] $T_0$.  As is usual with separation axioms, we can also look for a non-$T_0$ version.  A priori, this is a compact [[preregular space]]; however, since every such space is [[regular space|regular]], we can speak instead of a __compact regular space__.

In the absence of the axiom of choice, and especially in [[constructive mathematics]], the best definition of compactum seems to be a compact regular locale.  That is, it is the category of compact regular locales that has all of the nice properties, forming a [[nice category of spaces]], and that has the desired examples, such as the [[unit interval]].  (See the discussion at [[Tychonoff theorem]] for an example of how the category of compact Hausdorff topological spaces might fail to be nice; see [Frank Waaldijk's PhD thesis](http://www.fwaaldijk.nl/foundations%20of%20constructive%20mathematics.pdf) (pdf) for a thorough discussion of what is needed to make the unit interval a compact Hausdorff topological space.)

The monadic definition, in particular, falls quite flat without some form of the axiom of choice; even [[excluded middle]] and [[COSHEP]] are powerless here.  In fact, it is quite consistent to assume that every ultrafilter is principal (a strong denial of the ultrafilter principle), in which case $\beta$ is the [[identity monad]].  Then a compactum would be just a set if that were the definition used.

On the other hand, it is the monadic definition that gives an [[algebraic category]] with a nice relationship to [[Set]].  Without the ultrafilter principle, there is no reason to think that the set-of-points functor from compact regular locales to sets is even [[continuous functor|continuous]].


## Properties

### General

* [[compact Hausdorff spaces are normal]]

* [[open subspaces of compact Hausdorff spaces are locally compact]]

* [[closed subspaces of compact Hausdorff spaces are equivalently compact subspaces]]


### Stone--&#268;ech compactification
 {#StoneCechCompactification}

By general nonsense, every $\beta S$, regarded as a free $\beta$-algebra, is a compactum, and the functor 

$$\beta: Set \to Comp$$ 

is [[left adjoint]] to the [[forgetful functor]] $Comp \to Set$.  Assuming the ultrafilter principle, this functor extends to a functor $\beta: Top \to Comp$ (identifying a set with its [[discrete space]]) that is left adjoint to the forgetful functor $Comp \to Top$.  This is the __[[Stone–Čech compactification]]__ functor (N.B.: for many authors, Stone--&#268;ech compactification refers to the restriction of this functor to [[Tychonoff spaces]] $X$, which are precisely those spaces where the unit $X \to \beta X$ is an [[embedding]] so that we have a [[compactification]] in the technical sense).

A classical construction of the Stone--&#268;ech compactification starts with the unit [[interval]] $I =[0, 1]$ and proceeds to the [[codensity monad]] induced from the functor 

$$\hom(-, I) \colon Top^{op} \to Set.$$ 

The monad is given on objects by $X \mapsto I^{\hom(X, I)}$; this lands in compact Hausdorff spaces under the ultrafilter principle. Let $\bar{X}$ be the closure of the [[image]] of the unit $u_X: X \to I^{\hom(X, I)}$; this $\bar{X}$ is compact Hausdorff. 

+-- {: .num_prop} 
###### Proposition 
If $X$ is a [[Tychonoff space]], then the unit $u_X: X \to I^{\hom(X, I)}$ is a subspace embedding, so that $I$ is a [[cogenerator]] in the category of Tychonoff spaces. (In particular, $u_C$ is an embedding if $C$ is compact Hausdorff, so $I$ is also a [[cogenerator]] in the category of compact Hausdorff spaces.)  
=-- 

The proof is essentially [[Urysohn's lemma]]; see also related discussion at [[Tychonoff space]] and at [[uniform space]] (noting that compact Hausdorff spaces are uniform spaces for a unique uniformity). 

+-- {: .num_theorem} 
###### Theorem 
The natural map $i_X: X \to \bar{X}$ is universal among maps from $X$ to compact Hausdorff spaces, thus giving a [[left adjoint]] $Top \to Comp$ to the (fully faithful) forgetful functor $U: Comp \to Top$. 
=-- 

+-- {: .proof} 
###### Proof 
Let $f: X \to C$ be a map, where $C$ is a compact Hausdorff space. Since $I$ is a cogenerator in the category of compact Hausdorff spaces, the unit for the codensity monad $M_I$,

$$u_C: C \to I^{\hom(C, I)},$$ 

is a continuous injection (and hence a closed subspace embedding, since $C$ is compact Hausdorff). Let $\hat{f} = M_I(f)$, and consider the pullback square 

$$\array{
\hat{f}^{-1}(C) & \to & I^{\hom(X, I)} \\
\mathllap{\pi} \downarrow & & \downarrow \mathrlap{\hat{f}} \\ 
C & \underset{u_C}{\to} & I^{\hom(C, I)}.
}$$ 

From an evident naturality square for the unit $u$, we have a map $h: X \to \hat{f}^{-1}(C)$, i.e., the map $u_X: X \to I^{\hom(X, I)}$ factors through the closed subspace $\hat{f}^{-1}(C) \hookrightarrow I^{\hom(X, I)}$. Therefore $h$ factors as 

$$X \stackrel{i_X}{\to} \bar{X} \subseteq \hat{f}^{-1}(C)$$ 

and since $\pi \circ h = f$, we conclude that $f$ factors through $i_X$. And moreover, there is at most one $k: \bar{X} \to C$ such that $k \circ i_X = f$, because $i_X$ maps $X$ onto a dense subspace of $\bar{X}$, and dense subspaces are epic in the category of Hausdorff spaces. This completes the proof. 
=-- 


We have a similar Stone--&#268;ech compactification functor $Loc \to Comp$; we do not need the ultrafilter principle here if $Comp$ is defined in terms of locales.

### Category of compacta 

The category $Comp$ of compact Hausdorff spaces and continuous maps is 

* [[exact category|Barr exact]], since $U: Comp \to Set$ is monadic, 

* an [[extensive category]], and 

* a [[total category]] (by monadicity over $Set$), and 

* a [[total category|cototal category]] (because it is [[complete category|complete]], [[well-powered category|well-powered]], and has a [[cogenerator]] given by the unit interval $I = [0, 1]$). 

From the first two properties, it follows that $Comp$ is a [[pretopos]], meaning that $Comp$ enjoys the same finitary exactness properties that hold in a [[topos]]; in particular, first-order intuitionistic logic may be enacted within $Comp$. 

In ([Marra-Reggio 18](#MarraReggio)), the authors give a characterization of $Comp$ up to equivalence as the unique non-trivial [[pretopos]] which is [[well-pointed category|well-pointed]], [[filtrality|filtral]] and admits all set-indexed [[copowers]] of its [[terminal object]]. They contrast this result with Lawvere’s characterisation of the category of sets in [[ETCS]], noting that the main divergence concerns

> the existence of infinite “discrete” objects. While the third axiom of ETCS postulates the existence of a natural numbers object, we prescribe filtrality which forbids the existence of infinite discrete objects. ([Marra-Reggio 18, p. 2](#MarraReggio))

In the context of [[ultracategories]], $Comp$ is equivalent to $Fun_{RUlt}(\ast, Set)$, the category of right ultrafunctors between the terminal ultracategory and $Set$ ([Lurie, p. 4](#Lurie)). 

The [[infinitary pretopos]] of [[condensed sets]]
is the completion of the [[pretopos]] of [[compact Hausdorff spaces]].

## Related concepts

* [[compact space]], [[locally compact space]].

* [[paracompact Hausdorff space]]

* [[pyknotic set]]

## References

* {#MarraReggio} Vincenzo Marra, Luca Reggio, _A characterisation of the category of compact Hausdorff spaces_, ([arXiv:1808.09738](https://arxiv.org/abs/1808.09738))

* {#Lurie} [[Jacob Lurie]], _Ultracategories_, ([pdf](http://www.math.harvard.edu/~lurie/papers/Conceptual.pdf))


[[!redirects compactum]]
[[!redirects compacta]]
[[!redirects compact Hausdorff space]]
[[!redirects compact Hausdorff spaces]]
[[!redirects compact Hausdorff topological space]]
[[!redirects compact Hausdorff topological spaces]]
[[!redirects compact regular locale]]
[[!redirects compact regular locales]]

[[!redirects compact regular space]]
[[!redirects compact regular spaces]]
[[!redirects compact regular topological space]]
[[!redirects compact regular topological spaces]]
