
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

The term *convenient category of topological spaces* is used (going back to [Steenrod 1967](#Steenrod67)) for a [[category]] of [[topological spaces]] [[nice topological space|nice]] enough to address many of the needs of [[topology|working topologists]], notably including the condition of being a [[cartesian closed category]]. As such, they are examples of [[nice categories of spaces]].

A primary example is the category of [[compactly generated spaces]], another useful examples is the category of [[D-topological spaces]].


## Definition

While the authors of this article don't know whether there exists in the literature a widely accepted definition of "convenient category of topological spaces", we propose the following definition as reasonable and convenient (see also the discussion [below](#NvC) on the distinction between "nice" and "convenient"): 

\begin{definition}
\label{ConvenientCategory}
A **convenient category of topological spaces** is a [[full subcategory|full]] [[replete subcategory]] $C$ of the category of all topological spaces [[Top]] such that the following conditions 1-3 hold: 

1. Every [[CW complex]] is an object of $C$; 

2. $C$ is [[cartesian closed]]; 

3. $C$ is [[complete category|complete]] and [[cocomplete category|cocomplete]]. 

\end{definition}

Frequently it is also felt desirable to add closure under certain types of [[subspaces]]. For instance, in the well-known examples one has 

* $C$ is closed under [[closed subspaces]] in [[Top]], i.e., if $X$ belongs to $C$ and $A \subseteq X$ is a closed subspace (in $Top$), then $A$ also belongs to $C$. 

At times one might hope that $C$ is closed under [[open subspaces]] as well, but this does not hold for all objects in some of the well-known examples of convenient categories. 

It may be well to note that [[colimits]] and [[limits]] in $C$ need not agree with the corresponding colimits and limits in $Top$, except under certain conditions.  Some convenient categories are [[reflective subcategory|reflective]] or [[coreflective subcategory|coreflective]] in $Top$, in which case they are closed under limits or colimits respectively.  Moreover, because $C$ is a full subcategory of $Top$ which contains all CW complexes, the usual sorts of colimits used to present CW complexes are the same whether interpreted in $Top$ or in $C$.  Also, if $C$ is closed under closed subspaces, then an [[equalizer]] of a pair of maps between [[Hausdorff spaces]] in $C$ (being a closed subspace) is the same whether computed in $Top$ or in $C$.

On the other hand, [[products]] of $C$-objects in $Top$ need not land in $C$, so in that situation the product in $Top$ and the product in $C$ do not agree.  This is in particular the case for compactly generated spaces.  In fact, the "compactly generated product" is sometimes preferable to the $Top$-product for more explicit reasons: for instance, if $X$ and $Y$ are CW complexes, then $X \times Y$ need not be a CW complex in the usual product topology, but it is in the compactly generated topology.


## Examples
 {#Examples}


### Categories of colimits of generating spaces
 {#CategoriesOfColimitsOfGeneratingSpaces}

The original example of a convenient category of topological spaces is that of 

* [[compactly generated topological space]]

and another example is that of 

* [[Delta-generated spaces]] ([[Euclidean-generated spaces]]).

Both of these are special cases of the general class of convenient *$GenSp$-generated topological spaces*:

These are those topological spaces $X$ which agree with the [[colimit]] ([in TopSp](Top#UniversalConstructions)) of all continuous images inside them of *generating spaces* in a specified [[full subcategory]] $GenSp \,\subset\, $ [[TopSp]] ([Vogt 1971, Sec. 1](#Vogt71)):

\[
  \label{Gfication}
  G(X)
  \,\coloneqq\,
  \Big(
  \underset{
    \underset{
      { T \in GenSp }
      \atop
      {T \to X}
    }{\longrightarrow}
  }{\lim}
  \,
  T
  \Big)
  \xrightarrow{\;\;\; \simeq \;\;\;}
  X
\]

The [[full subcategories]] of such $GenSp$-generated spaces are [[coreflective subcategory|coreflective]] ([Vogt 1971, Cor. 1.4](#Vogt71))

$$
  TopSp
    \underoverset
      {\underset{G}{\longrightarrow}}
      {\hookleftarrow}
      {\;\;\;\;\bot\;\;\;\;}
  G TopSp
  \,.
$$

If one demands of the category $GenSp \,\hookrightarrow TopSp\,$ of generating spaces, for any pair $G_1, G_2 \,\in\, GenSp$ that ([Vogt 1971, Axiom 2](#Vogt71)):

1. their [[product topological space]] is again in $GenSp$;

1. the [[compact-open topology]] on the set of maps $G_1 \to G_2$ has a [[continuous function|continuous]] [[evaluation map]]

then $G TopSp$ is a [[Cartesian closed category]] ([Vogt 1971, Thm. 3.6](#Vogt71)), with [[internal hom]] given by the image under $G$-fication (eq:Gfication) of the [[compact open topology]].

If one in addition demands that $GenSp$ contains all [[topological simplices]] (or all [[Cartesian spaces]] $\mathbb{R}^n$), then $G(X) \to X$ is a [[weak homotopy equivalence]] ([Vogt 1971, Prop. 1.2 (g)](#Vogt71)).  

As special cases of this general construction, the above examples of

* [[compactly generated topological spaces]]  is obtained by 

  taking $GenSp$ to be given by all [[compact Hausdorff spaces]]

* [[Delta-generated topological spaces]] is obtained by 

  taking $GenSp$ to be given by all [[Cartesian spaces]] (equivalently by all [[topological simplices]]).

See also [Gaucher 2007, Sec. 2](#Gaucher07).

Further developments along these lines are in [Escardo, Lawson & Simpson 2004](#EscardoLawsonSimpson04):

The topological spaces $X$ for which there is an [[exponential law for spaces|exponentiable space]] in [[Top]] (i.e such that $X \times (-)  \;\colon\; Top \to Top$ has a [[right adjoint]])
may be described more concretely as _core-compact_ spaces (spaces whose topology is a [[continuous lattice]]). 
A collection $\mathcal{C}$ of core-compact spaces, with the property that the product of any two spaces in $\mathcal{C}$ is a [[colimit]] in [[Top]] of spaces in $\mathcal{C}$. Such a collection $\mathcal{C}$ is called **productive**. Spaces which are $Top$-colimits of spaces in $\mathcal{C}$ are called $\mathcal{C}$-**generated**. 

\begin{definition}
\label{ProductiveClassOfGenerators}
  Say that a class $\mathcal{C}$ of [[topological spaces]] is *productive* if

1. every $U \in \mathcal{C}$ is [[exponentiable object|exponentiable]],

1. for every [[pair]] $U_1, U_2 \in \mathcal{C}$ their [[product space]] $U_1 \times U_2$ is $\mathcal{C}$-generated.  

\end{definition}

\begin{theorem}
\label{ProductiveClassOfGeneratorsImpliesConvenience}
If $\mathcal{C}$ is a productive class of generating objects (Def. \ref{ProductiveClassOfGenerators}), then the full subcategory of $Top$ whose objects are $\mathcal{C}$-generated is 

1. [[coreflective subcategory|coreflective]] in [[Top]], hence [[complete category|complete]] and [[cocomplete category|cocomplete]], 

2. [[cartesian closed category|cartesian closed]], with the [[internal hom]] given by the coreflection of the usual [[mapping space]] with its [[compact-open topology]].

\end{theorem}
\begin{proof}
 The existence of the internal hom is [Escardo, Lawson & Simpson 2004 Thm. 5.15](#EscardoLawsonSimpson04). To see that this is the coreflection of the compact-open topology:

1. find the notation "$\mathcal{C}(-)$" for the coreflector on on p. 6, 

2. observe that the ordinary mapping space with its [[compact-open topology]] is denoted "$[X \Rightarrow_{\ll_{\mathcal{C}}} Y]$" in Rem. 5.20, 

3. while the internal hom in $\mathcal{C}$-generated spaces is denoted "$[X \Rightarrow_{\mathcal{C}} Y] = \mathcal{C}\big(Map_{\mathcal{C}}[X,Y]\big)$" on bottom of p. 14, 

4. where "$Map_{\mathcal{C}}$" is defined in Lemma 3.8, 

5. and finally the statement $Map_{\mathcal{C}}[X,Y] = [X \Rightarrow_{\ll_{\mathcal{C}}} Y]$ is Prop. 5.21 on p. 21,

which implies the claim.
\end{proof}

The other convenience conditions of Def. \ref{ConvenientCategory} (inclusion of [[CW-complexes]], closure under [[closed subspaces]]) are in practice usually satisfied as well. For example, if closed subspaces of objects of $\mathcal{C}$ are $\mathcal{C}$-generated, then closed subspaces of $\mathcal{C}$-generated spaces are also $\mathcal{C}$-generated. If the unit interval $I$ is $\mathcal{C}$-generated, then so are all CW-complexes. 

Moreover:

\begin{lemma}
  \label{RetractsOfCGeneratedSpacesAreCGenerated}
  The category of $\mathcal{C}$-generated spaces is closed under forming [[retracts]].
\end{lemma}
\begin{proof}
 Let $X$ be $\mathcal{C}$-generated and
\[
  \label{ARetract}
  id 
   \;\colon\;
  A \xrightarrow{i} X \xrightarrow{r} A
\]
a retract, for [[continuous maps]] $i$ and $r$. Consider a [[subset]] $U \subset A$ such that for all $C \in \mathcal{C}$ and all [[continuous maps]] $p \colon C \to A$, the [[preimage]] $p^{-1}(U) \subset C$ is open in $C$. We need to show that then $U$ is already open in $A$.

First note that the [[preimage]] $r^{-1}(U)$ of $U \subset A$ is open in $X$: Namely, for all $C \in \mathcal{C}$ and continuous maps $q \colon C \to X$ we have that $q^{-1}\big(r^{-1}(U)\big) = (r \circ q)^{-1}(U)$ is open in $C$ by assumption on $U$, hence $r^{-1}(U)$ is open in $X$ by the assumption that $X$ is $\mathcal{C}$-generated.

But then the retract property (eq:ARetract) implies that 
$$
  U 
    = 
  id^{-1}(U)
    =
  i^{-1}\big(r^{-1}(U)\big)
$$
is the preimage of the open subset $r^{-1}(U)$ under the continuous map $i$, and hence is open.
\end{proof}


### Subcategories of toposes
 {#ExamplesSubcategoriesOfToposes}

The [above](#CategoriesOfColimitsOfGeneratingSpaces) example of the category of [[Delta-generated topological spaces]] [above](#CategoriesOfColimitsOfGeneratingSpaces) has the remarkable property that it is 

1. a [[full subcategory]] of the [[quasi-topos]] of [[diffeological spaces]] (see [there](diffeological+space#RelationToTopologicalSpaces)), 

1. which is in turn a [[full subcategory]] of the [[cohesive topos]] of [[smooth sets]] (see [there](geometry+of+physics+--+smooth+sets#DiffeologicalSpacesAreTheConcreteSmoothSets));

1. which in turn is a [[full sub-(infinity,1)-category|full sub-$(\infty,1)$-category]] of the [[cohesive (infinity,1)-topos|cohesive $(\infty,1)$-topos]] of [[smooth infinity-groupoids|smooth $\infty$-groupoids]]

such that the canonical [[shape modality]] (the [[shape via cohesive path ∞-groupoid|smooth path ∞-groupoid construction]]) still sees the correct underlying [[homotopy type]] of topological spaces ([[schreiber:Proper Orbifold Cohomology|SS20, Ex. 3.18]], see also at [[model structure on Delta-generated topological spaces]]):

\begin{imagefromfile}
    "file_name": "TopologicalConvenienceBySmoothGroupoids210930.jpg",
    "width": 800,
    "unit": "px",
    "margin": {
        "top": -40,
        "bottom": 20,
        "right": 0, 
        "left": 10
    },
    "caption": "From [SS21](https://ncatlab.org/schreiber/show/Equivariant+principal+infinity-bundles)"
\end{imagefromfile}

## Counterexamples

### The rational numbers are not exponentiable in $\mathrm{Top}$

Here is an example showing that the category $\mathrm{Top}$ of [[topological spaces]] and continuous functions is not Cartesian-closed.

Let $\mathbb{Q}$ denote the [[rational numbers]] with the usual topology, and let $S$ denote the [[Sierpiński space]] whose underlying set is $\{0,1\}$ and whose open sets are $\emptyset$, $\{1\}$, and $\{0,1\}$. Notice that, for every topological space $X$, continuous functions from $X$ to $S$ correspond bijectively to open subsets of $X$. Indeed, every open subset $U$ of $X$ corresponds to its [[characteristic function]] $\chi_U : X \to S$, which is constantly equal to $1$ on $U$ and $0$ elsewhere, and the continuous functions from $X$ to $S$ are precisely those functions of the form $\chi_U$ for some open subset $U$.

Suppose the exponential object $S^\mathbb{Q}$ exists in $\mathrm{Top}$. That is, suppose that there exists a topological space $S^\mathbb{Q}$ and a continuous function $\mathrm{ev} : S^\mathbb{Q} \times \mathbb{Q} \to S$ such that, for every topological space $Z$ and every continuous function $f : Z \times \mathbb{Q} \to S$, there exists a unique continuous function $\hat{f} : Z \to S^\mathbb{Q}$ such that $\mathrm{ev} \circ (\hat{f} \times \mathrm{Id}_\mathbb{Q}) = f$. In other words, there is a bijection $\hat{(-)} : \mathrm{Hom}(Z \times \mathbb{Q}, S) \cong \mathrm{Hom}(Z, S^\mathbb{Q})$ which is natural in $Z$. (The inverse, going from $\mathrm{Hom}(Z, S^\mathbb{Q})$ to $\mathrm{Hom}(Z \times \mathbb{Q}, S)$, is obtained by applying the functor $- \times \mathbb{Q}$ and then composing with $\mathrm{ev}$.) Using the singleton space $1$ in place of $Z$, we see that the underlying set of $S^\mathbb{Q}$ is the set $\mathrm{Hom}(\mathbb{Q},S)$ of continuous functions from $\mathbb{Q}$ to $S$ (that is, the set of open subsets of $\mathbb{Q}$), and that $\mathrm{ev} : S^\mathbb{Q} \times \mathbb{Q} \to S$ is indeed the function evaluation map $(f,q) \mapsto f(q)$. The universal property of $S^\mathbb{Q}$ therefore says that, for all spaces $Z$ and all continuous functions $f : Z \times \mathbb{Q} \to S$, the [[currying|curried]] form $\hat{f}$ of $f$ (which maps each $z \in Z$ to $f(z,-) \in S^\mathbb{Q}$) is a continuous function from $Z$ to $S^\mathbb{Q}$. If we identify maps into $S$ with open subsets, then the universal property says that for all topological spaces $Z$ and all open subsets $W \subseteq Z \times \mathbb{Q}$, the function $\gamma_W : Z \to S^\mathbb{Q}$, taking each $z\in Z$ to the set $\{q \in \mathbb{Q} : (z,q) \in W\}$, is continuous.

The continuity of $\mathrm{ev} : S^\mathbb{Q} \times \mathbb{Q} \to S$ implies that the set $\mathcal{E} \ := \{ (\chi_U,q) \in S^\mathbb{Q} \times \mathbb{Q} : U \in \mathcal{O}(\mathbb{Q}), q \in U\}$ is an open set in $S^\mathbb{Q} \times \mathbb{Q}$. Since $0 \in \mathbb{Q}$, $\mathcal{E}$ is an open neighbourhood of $(\chi_\mathbb{Q}, 0)$. By the definition of the product topology, there exist open sets $V \subseteq S^\mathbb{Q}$ and $P \subseteq \mathbb{Q}$ such that $(\chi_\mathbb{Q}, 0) \in V \times P \subseteq \mathcal{E}$. The inclusion $V \times P \subseteq \mathcal{E}$ means that, for all $p \in P$ and all open $U \subseteq \mathbb{Q}$ such that $\chi_U \in V$, we have $p \in U$. That is, for all open $U \subseteq \mathbb{Q}$ such that $\chi_U \in V$, we have $P \subseteq U$. (Note that the pair $(\chi_\mathbb{Q},0)$ is not special here; any element of $\mathcal{E}$ would have sufficed.)

We will now construct a space $Z$ and an open set $W \subseteq Z \times \mathbb{Q}$ such that $\gamma_W$ is not continuous. Since $P$ is a non-empty open set, there exists a non-empty open interval $(r_1, r_2) \subseteq \mathbb{R}$ such that $(r_1, r_2) \cap \mathbb{Q} \subseteq P$. Let $\alpha$ be an irrational number in $(r_1,r_2)$. For each $t \in [0,\infty)$, let $U_t := \mathbb{Q} \setminus [\alpha - t, \alpha + t]$. Each $U_t$ is open in $\mathbb{Q}$, and $U_0 = \mathbb{Q}$. Furthermore, since $P$ contains (the rational numbers in) an open interval around $\alpha$, none of the $U_t$'s contain $P$ except $U_0$. That is, $P \subseteq U_t$ if and only if $t = 0$. (Note that we could have alternatively chosen $Z = \{0\} \cup \left\{ \frac{1}{n} : n \in \mathbb{N} \right\} \subseteq \mathbb{R}$.)

(Here we see the crucial property of the space $\mathbb{Q}$: for all neighbourhoods $P$ of $0$, there is an open cover of $\mathbb{Q}$ with no finite subcollection that covers $P$. In this case, $\{ U_t : t \gt 0 \}$ is such an open cover.)

Let $W = \bigcup_{t \geq 0} \{t\} \times U_t$. It is helpful to draw a picture to visualise this set; $Z \times \mathbb{Q}$ looks like a half-plane, and $W$ looks like the complement of a cone whose vertex is at $(0,\alpha)$. This should also make it clear (at least visually) that $W$ is open in $Z \times \mathbb{Q}$, since it inherits the subspace topology from $Z \times \mathbb{R}$.

Now, for each $t \in [0,\infty)$, the set $\{q \in \mathbb{Q} : (t,q) \in W\}$ is just $U_t$. That is, $\gamma_W(t) = \chi_W(t,-) \in S^\mathbb{Q}$ is the indicator function of $U_t$. But recall that $V \subseteq S^\mathbb{Q}$ and $P \subseteq \mathbb{Q}$ are open sets such that, for all open sets $U \subseteq \mathbb{Q}$ satisfying $\chi_U \in V$, we have $P \subseteq U$. Therefore, if $t \gt 0$, then $\chi_{U_t} \notin V$, because $P \nsubseteq U_t$. Furthermore, $\chi_{U_0} = \chi_\mathbb{Q} \in V$. It follows that $\gamma_W^{-1}(V) = \{0\}$. But $V$ is open and $\{0\}$ is not; therefore, $\gamma_W$ is not continuous, which contradicts the universal property of $S^\mathbb{Q}$. Therefore no such object $S^\mathbb{Q}$ with the universal property exists.

### The exponentiable spaces in $\mathrm{Top}$ do not form a Cartesian-closed subcategory

A naive approach to the problem of constructing "convenient categories" usually runs into problems. For example, one could try to work with the full subcategory of $Top$ consisting of [[exponentiable spaces]]; the problem is that even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ may not be:

* The category of exponentiable spaces is not cartesian closed. (It is however [[cartesian monoidal category|cartesian]]: the product of two exponentiable spaces under the usual product topology is exponentiable.)

To see this, we recall that a [[Hausdorff space]] is exponentiable if and only if it is [[locally compact space|locally compact]], and that an exponential $Y^X$ (provided it exists) is Hausdorff if $Y$ is. Thus, it is enough to exhibit two locally compact Hausdorff spaces $X$, $Y$ whose exponential is not locally compact.

Take $X = \mathbb{R}$ with its usual topology and $Y = \mathbb{N}$ (the set of [[natural numbers]]) with the [[discrete topology]]. Suppose that an exponential $\mathbb{R}^\mathbb{N}$ exists in the category of locally compact Hausdorff spaces. Then it must be a countable product of copies of $\mathbb{R}$ by the following calculation: 

$$LCH(X \times \mathbb{N}, \mathbb{R}) \cong LCH(\sum_{\mathbb{N}} X, \mathbb{R}) \cong \prod_{\mathbb{N}} LCH(X, \mathbb{R})$$ 

where the last functor in $X$, in order to be [[representable functor|representable]], would have to be represented by a product $\prod_{\mathbb{N}} \mathbb{R}$. Using the universal property of products, one may easily exhibit a scalar multiplication 

$$\mathbb{R} \times \mathbb{R}^{\mathbb{N}} \to \mathbb{R}^{\mathbb{N}}$$ 

rendering $\mathbb{R}^{\mathbb{N}}$ a [[topological vector space]] (a TVS) over the real numbers. But it is well-known that locally compact TVS are finite-dimensional, and we have reached an absurdity. 

Similarly, the topological product $\mathbb{N}^{\mathbb{N}}$ is homeomorphic to [[Baire space of irrational numbers|Baire space]], and this is not locally compact either. 

## "Nice" versus "convenient" categories of spaces
{#NvC}

A related entry is [[nice category of spaces]]. Here we explain the difference between "convenient" and "nice" categories of spaces. 

"A convenient category of topological spaces" is the title of [a well-known paper](#Steenrod) by [[Norman Steenrod]], who emphasized particularly [[function space]] constructions (i.e., cartesian closure) as a great convenience for working algebraic topologists, on top of (generally less problematic) completeness and cocompleteness assumptions. (See also the historical remarks that follow.) 

It is well-known that $Top$ is not [[cartesian closed category|cartesian closed]].  One can characterize the [[exponential law for spaces|exponentiable spaces]], which include all [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] spaces, but as we saw above, the naive idea of simply cutting down to some of these does not give a good cartesian closed category either, since firstly it need not be complete and cocomplete, and secondly even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ need not be.

However, one can cut down to *some* full subcategory of spaces which does admit function spaces.  This typically involves the subtle and delicate interplay between compactness conditions and openness conditions.  It comes at a cost -- that limits and/or colimits in the subcategory might not be computed as they are in $Top$ -- but this is generally considered a very small price to pay in exchange for the great convenience of these assumptions. 

That a convenient category of topological spaces contains all the CW complexes was not explicitly declared by Steenrod, but we feel certain that [[algebraic topology|algebraic topologists]] want these as part of their convenient category. In practice this is a mild assumption, because the usual examples certainly contain all finite topological products of the [[unit interval]] $I$, and are closed under those $Top$-colimits used to present CW complexes, as built inductively from the basic spaces $I^n \cong D^n$. 

"Nice categories of spaces" should be thought of as a wider and vaguer term; it really means the category of spaces has "nice" categorical properties for some mathematical purpose at hand. Certainly any convenient category of spaces should be considered a nice category of spaces for the general purposes of algebraic topology. On the other hand, there are categories of spaces which are not "convenient" in the technical sense described above, but which may be very nice for certain purposes. 

For example, the category of [[compact Hausdorff spaces]] can be considered as being very nice for certain purposes. For instance, it is [[monadic category|monadic]] over $Set$ (!) and a [[pretopos]]. It is, however, not "convenient", as it is very far from being cartesian closed. In a different direction, there is the (complete, cocomplete) cartesian closed category of [[equilogical spaces]], but this is not a full subcategory of $Top$, and the core concerns of mathematicians working with equilogical spaces are somewhat different from those of algebraic topologists.

It should also be noted that "[[space]]" itself has a wider meaning than the technical notion of "[[topological space]]", even if topological intuitions come into play. For example, in [[domain theory]], one often considers certain types of [[posets]] (for example, [[directed-complete partial order|dcpos]]) as certain types of "spaces". In this direction, we have that the category of dcpos and [[Scott-continuous map]]s between them forms a complete, cocomplete, cartesian closed category. However, these types of spaces are quite far removed from the traditional concerns of topology, hence are not "convenient" in the sense given above (despite the manifold relations between Scott continuity and the point-set topology which underlies the classical results on compactly generated spaces). In another direction, the category of [[locales]] is in some respects "nice", but these are not topological spaces either. 

Along with the entry on [[nice category of spaces]] and the examples above, see [[Johnstone's topological topos]] and Spanier's [[quasitopological space]]s ([ref](#Spanier)). None of these is convenient in the precise sense above. However there are advantages in having a category which is not only cartesian closed but also locally cartesian closed. In algebraic topology, this has led to Peter Booth's work on "fibred mapping spaces" ([#Booth 1971](##Booth71), [#Crabb & James 1998](##CrabbJames98)).  

There are possible advantages in homotopy theory of using a "topological topos" ([Johnstone](#Johnstone), [Harasani](#Harasani)). 


## Historical remarks 
 {#HistoricalRemarks}

The phrase "convenient category of topological spaces" predates [Steenrod 1967](#Steenrod67) by a number of years;  [Brown 1963, Introduction](#Brown63) says:

> It may be that the category of Hausdorff $k$-spaces is adequate and convenient for all purposes of topology.

The requirements for convenience were spelled out in [Brown 1964](#Brown64).

In fact, Brown (not Steenrod, as has sometimes been assumed) was the first to prove that Hausdorff [[Kelley space|k-spaces]] (with the "kelleyfied" weakening of the [[compact-open topology|compact--open topology]] on function spaces) formed what is now called a [[cartesian closed category]] (see [Brown 1961](#Brown61)), influenced by [Cohen 1954](#Cohen54).  

Note Brown's work predates the formal introduction of cartesian closed categories in [[Bill Lawvere]]'s thesis by a couple of years; in fact there is clear anticipation in Brown's thesis of the notions of [[closed monoidal category|monoidal closed]] and cartesian closed categories, which was to attract much attention throughout the sixties. Further,  Brown's results  on the topological case are more precise than Steenrod's, since the 1964 paper deals with functions continuous on compact subsets, and for these obtains a homeomorphism without kellyfication. An account of this may be found in the book [Topology and Groupoids](#Brown06).  

Of course, as has often been emphasized by Lawvere, the need for and convenience of considering function spaces is a very old idea in [[geometry]] (going back to the roots of the [[calculus of variations]], for example). The constructions of exponentials of topological spaces via the compact--open topology had been known for a long time; see for example [[John Kelley]]'s _General Topology_ (1955). The relevance of what are today called [[Kelley space]]s (or k-spaces[^1]) had also been recognized; for example, Kelley's book indicates the [[complete space|completeness]] of function spaces (wrt the compact--open topology) when the base is a complete [[uniform space]] and the exponent is a k-space. However, the problem of obtaining a class of spaces _closed_ under function spaces wasn't solved prior to Brown's thesis. Brown also observed the relevance of k-spaces to studies of how products interact with [[quotient space]]s. The general appreciation of the connection between cartesian closure and preservation of quotients under products came with the appreciation of the conceptual simplicity of categorical [[adjunctions]], namely the point that the functor $- \times X$ preserves colimits if it has an exponential right adjoint $(-)^X$. The question also solved in Brown's 1964 paper was to give, in the Hausdorff case,  a left adjoint to  the functor $ (-)^Y $ when the function spaces have the compact-open topology, and so to give a monoidal closed structure on the category of Hausdorff spaces; the generalisation to the non-Hausdorff case is given in the paper of Booth and Tillotson listed below. 

Appreciation of the role of convenient categories was in full force by the early seventies (for a sample, see [[Peter May]]'s _Geometry of Iterated Loop Spaces_, where the category of Hausdorff k-spaces plays a foundational role). The notion of a "convenient category" is recognized elsewhere too (and not just within the categorical and algebraic topology communities); see for example the book by [Kriegl and Michor](#KM). 


[^1]: The '$k$' certainly  refers to 'kompakt' rather than Kelley's initial. 

## Related concepts

* [[compactly generated topological space]]

* [[Delta-generated topological space]], [[D-topological space]]

* [[quasi-topological space]]


## References

The terminology ("convenient category of topological spaces") became widely adopted with

* {#Steenrod67} [[Norman Steenrod]]: _A convenient category of topological spaces_, Michigan Math. J. **14** (1967) 133--152 &lbrack;[doi:10.1307/mmj/1028999711](https://doi.org/10.1307/mmj/1028999711), [euclid:mmj/1028999711](http://projecteuclid.org/euclid.mmj/1028999711)&rbrack;

referring there to the category of *[[compactly generated topological space]]* (see the references [there](compactly+generated+topological+space#Refererences) for more), whose convenient [[cartesian closed category|cartesian closure]] had [previously](#HistoricalRemarks) been highlighted in:

* {#Brown61} [[Ronnie Brown]], _Some problems of algebraic topology: a study of function spaces, function complexes, and FD-complexes_, DPhil thesis, Oxford University (1961) &lbrack;[uuid:3af55800-4be7-462f-b91d-9769a6dac2c4](https://ora.ox.ac.uk/objects/uuid:3af55800-4be7-462f-b91d-9769a6dac2c4)&rbrack;
  > (NB: the Appendix of this thesis was withdrawn from the examination.)  
 
* {#Brown63} [[Ronnie Brown]]: _Ten topologies for $X\times Y$_, Quart. J. Math.  **14** 2 (1963) 303--319 &lbrack;[doi:10.1093/qmath/14.1.303](https://doi.org/10.1093/qmath/14.1.303), [pdf](http://groupoids.org.uk/pdffiles/tentopologies.pdf)&rbrack;

* {#Brown64} [[Ronnie Brown]]: _Function spaces and product topologies_,  Quart. J. Math. **15** (1964) 238--250. &lbrack;[doi:10.1093/qmath/15.1.238](https://doi.org/10.1093/qmath/15.1.238)&rbrack;

influenced, in turn, by:

* {#Cohen54} D. E. Cohen:  _Spaces with weak topology_, Quart. J. Math. **5** 2 (1954) 77--80 &lbrack;[doi:10.1093/qmath/5.1.77](https://doi.org/10.1093/qmath/5.1.77)&rbrack;

Discussion in the generality that subsumes [[compactly generated topological spaces]] and [[Delta-generated topological spaces]] and all cases of subcategory-generated spaces in between:

* {#Vogt71} [[Rainer M. Vogt]]: *Convenient categories of topological spaces for homotopy theory*,  Arch. Math **22** (1971) 545–555  &lbrack;[doi:10.1007/BF01222616](https://doi.org/10.1007/BF01222616)&rbrack;

* {#Wyler73} [[Oswald Wyler]]: *Convenient categories for topology*, General Topology and its Applications **3** 3 (1973) 225-242 &lbrack;<a href="https://doi.org/10.1016/0016-660X(72)90014-1">doi:10.1016/0016-660X(72)90014-1</a>&rbrack;

* {#EscardoLawsonSimpson04} [[Martín Escardó]], [[Jimmie Lawson]], [[Alex Simpson]], Section 3 of: *Comparing Cartesian closed categories of (core) compactly generated spaces*, Topology and its Applications **143** 1–3 (2004) 105-145 &lbrack;[doi:10.1016/j.topol.2004.02.011](https://doi.org/10.1016/j.topol.2004.02.011)&rbrack;

* {#FajstrupRosicky08} [[Lisbeth Fajstrup]], [[Jiří Rosický]], Section 3 of: _A convenient category for directed homotopy_, Theory and Applications of Categories **21** 1 (2008) 7-20 &lbrack;[arXiv:0708.3937](https://arxiv.org/abs/0708.3937), [tac:21-01](http://www.tac.mta.ca/tac/volumes/21/1/21-01abs.html)&rbrack;

* {#Gaucher07} [[Philippe Gaucher]], Section 2 of: *Homotopical interpretation of globular complex by multipointed d-space*, Theory and Applications of Categories **22** 22 (2009) 588-621, &lbrack;[arXiv:0710.3553](https://arxiv.org/abs/0710.3553)&rbrack;

On the abstract construction principle of these examples:

* [[Michael Barr]], *Building closed categories*, [[Cahiers|Cahiers Topologie Géométrie Différentielle]] **19** (1978) 115–129 &lbrack;[numdam:CTGDC_1978__19_2_115_0](http://www.numdam.org/item/?id=CTGDC_1978__19_2_115_0)&rbrack;

   
See also:

* {#Spanier} [[Edwin Spanier]], _Quasi-topologies_, Duke Mathematical Journal 30:1 (1963), 1--14.  [doi](https://doi.org/10.1215/s0012-7094-63-03001-1).
  > (on [[quasi-topological spaces]])

* {#Booth71} [[Peter I. Booth]]:  _The exponential law of maps. II._  Math. Z. **121** 4 (1971) 311–319 &lbrack;[doi:10.1007/bf01109977](https://doi.org/10.1007/bf01109977)&rbrack;

* {#BT} [[Peter I. Booth]],  J. Tillotson: _Monoidal closed, Cartesian closed and convenient categories of topological spaces_. Pacific J. Math. **88** 1 (1980) 35--53.  &lbrack;[doi:10.2140/pjm.1980.88.35](https://doi.org/10.2140/pjm.1980.88.35), [euclid:pjm/1102779712](http://projecteuclid.org/euclid.pjm/1102779712)&rbrack;

* {#CrabbJames98} [[Michael Crabb]], [[Ioan James]]:  _Fibrewise homotopy theory_,  Springer Monographs in Mathematics. Springer (1998) &lbrack;ISBN:1-85233-014-7, [doi:10.1007/978-1-4471-1265-5](https://doi.org/10.1007/978-1-4471-1265-5)&rbrack;

* {#Preuss02} Gerhard Preu&#223;, _Foundations of topology: an approach to convenient topology_, Kluwer (2002) &lbrack;[doi:10.1007/978-94-010-0489-3](https://doi.org/10.1007/978-94-010-0489-3)&rbrack;

survey in: 

* _Convenient topology --  a new branch of topology_ ([web](http://at.yorku.ca/i/a/a/c/54.htm))

* {#Brown06} [[Ronald Brown]]: *Spaces of functions and the compact-open topology*, Section 5.9 of: *Topology and Groupoids*, Booksurge (2006) &lbrack;[webpage](https://groupoids.org.uk/topgpds.html), [pdf](https://groupoids.org.uk/pdffiles/topgrpds-e.pdf), [pdf](https://www.sas.rochester.edu/mth/sites/doug-ravenel/otherpapers/rbrown-topgrpds-e.pdf)&rbrack;

Discussion via [[topos theory]]:

* {#Johnstone} [[Peter Johnstone]], _On a topological topos_, Proc. London Math. Soc. (3) 38:2 (1979) 237--271 &lbrack;[doi:10.1112/plms/s3-38.2.237](https://doi.org/10.1112/plms/s3-38.2.237)&rbrack;

* {#Harasani} Harasani, Hamed A. _Topos theoretic methods in general topology_, PhD Thesis, University of Wales, Bangor, (1988) &lbrack;[pdf](http://groupoids.org.uk/harasani.html)&rbrack;

Analogous considerations for [[diffeological spaces]] (subsuming [[D-topological spaces]])

* {#KM} [[Andreas Kriegl]]; [[Peter Michor]], _[[The Convenient Setting of Global Analysis]]_, Mathematical Surveys and Monographs **53**, American Mathematical Society (1997) &lbrack;[doi:10.1090/surv/053](https://doi.org/10.1090/surv/053)&rbrack;




[[!redirects convenient category of topological spaces]]
[[!redirects convenient categories of topological spaces]]
[[!redirects conventient category of topological spaces]]

[[!redirects convenient category of spaces]]
[[!redirects convenient categories of spaces]]