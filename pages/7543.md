
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Idea

The _Segal condition_ is a condition on a [[simplicial object]] $X_\bullet \in \mathcal{C}^{\Delta^{op}}$ which says that each component $X_{n \geq 2} \in \mathcal{C}$ is obtained from $X_1 \stackrel{\overset{\partial_0}{\to}}{\underset{\partial_1}{\to}} X_0$ by the $n$-fold [[fiber product]] of $X_1$ over $X_0$ which "glues" $n$ copies of $X_1$ end-to-end.

Hence if one thinks of $X_0$ as a collection of [[objects]] and of $X_1$ as a collection of [[morphisms]], then $X_\bullet$ satisfies the Segal condition precisely if each $X_{n \geq 2}$ can be interpreted as the collection of sequences of [[composition|composable]] morphisms of length $n$. The precise formulation is below in _[Definition -- For simplicial objects](#ForSimplicialObjects)_.

Accordingly, if $\mathcal{C} = $ [[Set]] is the category of [[sets]], then the Segal condition characterizes precisely those [[simplicial sets]] which are the [[nerve]] of a [[small category]], theorem \ref{NerveTheorem} below. This is the observation due to ([Segal 1968](#Segal)), following [[Grothendieck]], which today gives the Segal condition its name. Sometimes this statement also called the _nerve theorem_ (no relation to what is called _[[nerve theorem]]_ in [[homotopy theory]]).

It is useful to decompose this statement into its constituents as follows: 

A [[small category]] $C$ may be thought of as a [[directed graph]] $U(C)$ equipped with a [[unit law|unital]] [[associativity|associative]] [[composition]] operation. This corresponds to a sequence of inclusions of [[sites]]

$$
  (1 \stackrel{\overset{d_0}{\leftarrow}}{\underset{d_1}{\leftarrow}} 0) \hookrightarrow \Delta_0 \to \Delta
$$

into the [[simplex category]], where $\Delta_0$ is the category of finite non-empty directed linear graphs:

* a [[directed graph]] is equivalently a [[presheaf]] on $(1 \stackrel{\overset{d_0}{\leftarrow}}{\underset{d_1}{\leftarrow}} 0)$;

* a [[presheaf]] on $\Delta$, hence a [[simplicial set]] encodes via its face and degeneracy maps a kind of associative and unital composition -- but not necessarily "of composable morphisms" if $X_{n\geq 2}$ is not given in the above fashion.

In terms of this we can say that equipping a directed graph with the structure of a category is equivalent to asking for its pushforward along $(1 \stackrel{\overset{d_0}{\leftarrow}}{\underset{d_1}{\leftarrow}} 0) \hookrightarrow \Delta_0$ (which encodes all the collections of sequences of composable edges) to be equipped with a lift to a simplicial object through the pullback along $\Delta_0 \to \Delta$. Conversely, the simplicial objects obtained as such lifts are precisely the simplicial objects that satisfy the Segal condition.

Formulated in this way one sees that the Segal condition has a large variety of generalizations to structures with richer kinds of composition operations, such as [[globular operads]]. This is made precise below in _[Definition -- For cellular objects](#ForCellularObjects)_.

## Definition

### For simplicial objects 
 {#ForSimplicialObjects}

Let $\mathcal{C}$ be a [[category]] with [[pullbacks]].

+-- {: .num_defn}
###### Definition

A [[simplicial object]] 

$$
  X : \Delta^{op} \to \mathcal{C}
$$

is said to satisfy the **Segal condition** if it sends the [[colimits]] in the [[simplex category]] to [[limits]], hence if the [[Segal maps]] exhibit [[equivalences]]

$$
  X_n 
   \stackrel{\simeq}{\longrightarrow}
  \underbrace{
    X_1 \times_{X_0} \cdots \times_{X_0} X_1
  }_{n\; factors}
$$

for all $n \in \mathbb{N}$.

=--

More in detail:

+-- {: .num_defn #SegalCones}
###### Definition

For all $n \in \mathbb{N}$, consider $\Delta[n]$ naturally as a [[cocone]] in the [[simplex category]] under the [[diagram]]

$$
  \array{
     \Delta[0] && && \Delta[0] && && \Delta[0] &&& \cdots
      \\
      & {}_{\mathllap{d_1}}\searrow && {}^{\mathllap{d_0}}\swarrow && \searrow^{\mathrlap{d_1}} && {}_{d_0}\swarrow && \cdots
      \\
      && \Delta[1] &&&& \Delta[1] && \cdots 
  }
$$

with $n$ copies of $\Delta[1]$ at the bottom, such that the cocone injection of the $k$th copy is $\Delta[1] \simeq (k-1,k) \hookrightarrow (0,1,2, \cdots, n) \simeq \Delta[n]$.

A [[simplicial object]] $X \colon \Delta^{op} \to \mathcal{C}$ satisfies the **Segal conditions** if it sends these cocones to [[limit]] [[cones]] in $\mathcal{C}$. 


=--




+-- {: .num_remark #InfinitySegalCones}
###### Remark

This definition immediately generalizes to [[(∞,1)-category theory]] where $\mathcal{C}$ is an [[(∞,1)-category]] and $X$ is a [[simplicial object in an (∞,1)-category]]. Then for $X$ to satisfy the Segal conditons means that it sends the cocones of def. \ref{SegalCones} to [[(∞,1)-limit]] cones in $\mathcal{C}$.

Such a simplicial object is also called a **[[pre-category object in an (∞,1)-category]]** in $\mathcal{C}$.

=--


### For cellular objects
 {#ForCellularObjects}

A _[[globular theory]]_ is a [[wide subcategory]] inclusion

$$
  i_A \colon \Theta_0 \to \Theta_A
$$

of the [[globular site]] $\Theta_0$. There is an [[equivalence of categories]]

$$
  \omega Grph \simeq Sh(\Theta_0)
  \,.
$$

of [[∞-graphs]] and sheaves on the [[globular site]]. In particular for $\Theta_A = \Theta$ the [[cell category]] ([[Theta category]]) a [[presheaf]] on $\Theta$ is a [[cellular object]].

The **Segal condition** on a cellular object $X \colon \Theta^{op} \to \mathcal{C}$ is that the restriction $i^* X \colon \Theta_0^{op} \to \Theta^{op} \to \mathcal{C}$ to the [[cellular site]] is a [[sheaf]] there.

The cellular objects that satisfy the Segal condition are precisely the [[∞-category]] objects ([Berger](#Berger)).

The cellular spaces/ cellular simplicial sets/cellular [[∞-groupoids]] that satisfy the Segal condition as a [[weak homotopy equivalence]]/ [[equivalence of ∞-groupoids]] is a _[[Theta_n-space]]_ an [[(∞,n)-category]].



## Properties

### Characterization of nerves of (higher) categories

#### Of simplicial nerves of small categories

The archetypical role of the Segal condition is to make the following statement true.

+-- {: .num_theorem #NerveTheorem}
###### Theorem
**(nerve theorem)**

A [[simplicial set]] is the [[nerve]] of a [[small category]] precisely if it satsfies the Segal conditions.

=--

This is due to ([Segal 1968](#Segal)), following [[Grothendieck]].

+-- {: .num_remark}
###### Remark

There is an entirely unrelated theorem in [[homotopy theory]] also often called "the" _[[nerve theorem]]_. See there for more. Not to be confused with the discussion here.

=--

#### Of complete Segal spaces

By refining the above result from sets to $\infty$-groupoids, one obtains the [[pre-category object in an (infinity,1)-category]]. 

#### Of cellular nerves of strict $\omega$-categories

Similarly, a [[cellular set]] is the cellular nerve of a [[strict omega-category]] precisely if it satisfies the cellular Segal condition. ([Berger](#Berger)).

#### Of cellular models of $(\infty,n)$-categories

See at _[[Theta-space]]_.


### In terms of sheaf conditions
 {#InTermsOfSheafConditions}

We discuss an equivalent formulation of the Segal condition in terms of notions in [[topos theory]]/[[(∞,1)-topos theory]]. This perspective for instance lends itself more to a formulation of Segal conditions in terms of the [[internal language]] of toposes.

#### For simplicial objects and category objects
 {#InTermsOfSheafConditionForSimplicialObjects}

We characterize below in prop. \ref{CatAsPullback} the category of categories as the pullback of the [[topos]] of [[simplicial set]] along the inclusion of the topos of graphs into that of presheaves on finite linear graphs. 

First we state some preliminaries.

+-- {: .num_remark}
###### Remark

The condition in def. \ref{SegalCones} superficially looks like a [[sheaf]] condition for [[coverings]] of $\Delta[n]$ by $n$ subsequent copies of $\Delta[1]$. However, these coverings do _not_ form a [[coverage]] on the [[simplex category]] $\Delta$: the refinement-of-covers-axiom is not satisfied:

For instance for $d_1 \colon \Delta[1] \to \Delta[2]$ the map that sends the single edge of $\Delta[1]$ to the composite edge in $\Delta[2]$ there is no way to "pull back" the cover 

$$
  \{\Delta[1] \coprod \Delta[1] \stackrel{((0,1),(1,2))}{\to} \Delta[2]\}
$$ 

along this morphism, not even in the weak sense of _[[coverage]]_.

However, as this example also makes clear, the problem is precisely only with the morphisms in $\Delta$ that are no injective on generating edges.

=--

Therefore consider instead the following:

+-- {: .num_defn #FiniteLinearGraphsInAllGraphs}
###### Definition

Let 

$$
  j \colon \Delta_0 \hookrightarrow Graph
$$ 

be the [[full subcategory]] of that of [[directed graphs]] on the linear graphs $\{0 \to 1 \to \cdots \to n\}$ for $n \in \mathbb{N}$. 

=--

+-- {: .num_remark}
###### Remark

Morphisms in $\Delta_0$ have to send elementary edges to elementary edges. So there are

* precisely $n$ morphisms $\Delta_0[1] \to \Delta_0[n]$

* precisely $n$ morphisms $\Delta_0[2] \to \Delta_0[n+1]$

* precisely $n$ morphisms $\Delta_0[3] \to \Delta_0[n+2]$

* etc. 

=--


+-- {: .num_defn #ParallelMorphismCategory}
###### Definition

Write  

$$
  i 
    \colon 
  (1 \stackrel{\leftarrow}{\leftarrow} 0) \hookrightarrow \Delta_0
$$ 

for the [[full subcategory]] on the linear graphs with no edge and with one edge. 

=--


+-- {: .num_prop}
###### Proposition

The [[category]] of [[directed graphs]] is [[equivalence of categories|equivalently]] the [[category of presheaves]] over $(1 \stackrel{\leftarrow}{\leftarrow} 0)$, def. \ref{ParallelMorphismCategory}:

$$
  Graph(\mathcal{C}) \simeq PSh((1 \Leftarrow 0), \mathcal{C})
  =
  \mathcal{C}^{(1 \Rightarrow 0)}
  \,.
$$

=--

+-- {: .num_prop #AdjointTripleFromGraphs}
###### Definition

Write

$$
  (i_! \dashv i^* \dashv i_*)
  \colon
  \mathcal{C}^{1 \Rightarrow 0}
  \stackrel{\overset{i_!}{\to}}{\stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\to}}}
  \mathcal{C}^{\Delta_0^{op}}
$$

for the [[adjoint triple]] induced on [[categories of presheaves]] by the inclusion $i$ of def. \ref{ParallelMorphismCategory}: $i^*$ is given by precomposition with $i$, $i_!$ is left and $i_*$ is right [[Kan extension]] along $i$.

=--

+-- {: .num_prop #NerveOfGraph} 
###### Proposition

The functor $i_* \colon Graph(\mathcal{C}) \to \mathcal{C}^{\Delta_0^{op}}$
of def. \ref{AdjointTripleFromGraphs} sends a graph $X_1 \stackrel{\overset{\partial_1}{\to}}{\underset{\partial_0}{\to}} X_0$ to the presheaf $i_*(X)$ which on $n \in \mathbb{N}$ is given by th iterated [[pullback]]

$$
  i_*(X) \colon n \mapsto \underbrace{X_1 \times_{X_0} \times \cdots \times_{X_0} X_1}_{n \; factors}
$$

and which sends an inclusion $\Delta[k] \simeq (j, \cdots, j+k) \hookrightarrow (0,\cdots, n)\simeq \Delta[n] $ to the corresponding [[projection]] map out of the pullback.

We may call $i_*(X)$ the **nerve of the graph** $X$.

=--

+-- {: .proof}
###### Proof

Using the [[Yoneda lemma]] and the defining [[hom functor|hom]]-[[isomorphisms]] of the [[adjunction]] as well as the fact that the [[hom functor]] sends [[colimits]] in the first argument to [[limits]], we have

$$
  \begin{aligned}
    i_*(X)(n) & \simeq Hom(\Delta[n], i_*(X))
    \\
    & \simeq Hom(i^* \Delta[n], X)
    \\
    & \simeq Hom( \underbrace{\Delta[1] \coprod_{\Delta[0]} \cdots \coprod_{\Delta[0]} \Delta[1]}, X )
   \\
   & \simeq 
   \underbrace{
     Hom(\Delta[1], X)   
       \underset{Hom(\Delta[0], X)}{\times}   
       \cdots
       \underset{Hom(\Delta[0], X)}{\times}   
     Hom(\Delta[1], X)       
   }_{n\;factors}
   \\
   & \simeq 
   \underbrace{
     X \times_{X_0} \cdots \times_{X_0} X_1
   }_{n\; factors}
  \end{aligned}
  \,.
$$

=--

+-- {: .num_prop #CoverageOnDelta0}
###### Proposition

For $n \in \mathbb{N}$ declare a unique [[covering]] family of $\Delta[n] \in \Delta_0$ to be

$$
  \left\{ 
    \Delta\left[1\right] \simeq \left(k,k+1\right) 
    \hookrightarrow \Delta\left[n\right] \right\}_{k = 0}^{n-1}
  \,.
$$

Then this is a [[coverage]] on $\Delta_0$. 

=--


+-- {: .num_prop}
###### Proposition

A [[presheaf]] $X \colon \Delta_0^{op} \to \mathcal{C}$ is a [[sheaf]] with respect to the coverage of def. \ref{CoverageOnDelta0} precisely if it is in the [[essential image]] of the graph-nerve functor

$$
  i_*
  \colon
  Graph(\mathcal{C})
   \simeq
  \mathcal{C}^{(1 \stackrel{\to}{\to} 0)} 
    \stackrel{}{\to}
  \mathcal{C}^{\Delta_0^{op}}
$$

of prop. \ref{NerveOfGraph}. This yields an [[equivalence of categories]]

$$
  Graph(\mathcal{C})
  \simeq
  Sh(\Delta_0)
$$

with the [[category of sheaves]] on $\Delta_0$. The graph-nerve functor is a [[full and faithful functor]]

$$
  i_* \colon Graph \simeq Sh(\Delta_0)
  \hookrightarrow
  PSh(\Delta_0)
  \,.
$$

=--

+-- {: .num_defn #AdjointTripleFromSimplicialSets}
###### Definition

Write

$$
  (j_! \dashv j^* \dashv j_*)
  \colon
  \mathcal{C}^{\Delta_0^{op}}
  \stackrel{\overset{j_!}{\to}}{\stackrel{\overset{j^*}{\leftarrow}}{\underset{j_*}{\to}}}
  \mathcal{C}^{\Delta^{op}}
$$

for the [[adjoint triple]] induced on [[categories of presheaves]] by the inclusion $j$ of def. \ref{FiniteLinearGraphsInAllGraphs}: $j^*$ is given by precomposition with $j$, $j_!$ is left and $j_*$ is right [[Kan extension]] along $j$.

=--


In terms of all this the nerve theorem \ref{NerveTheorem} says the following:

We have [[geometric morphisms]] of [[toposes]]

$$
  Grph \simeq Sh(\Delta_0)
  \stackrel{\overset{i_!}{\to}}{
  \stackrel{\overset{i^*}{\leftarrow}}{\underset{i_*}{\hookrightarrow}}}
  PSh(\Delta_0)
   \stackrel{\overset{j_!}{\to}}{\stackrel{\overset{j^*}{\leftarrow}}{\underset{j_*}{\to}}}
  PSh(\Delta)
  \simeq sSet
$$

which capture the Segal condition as follows.

+-- {: .num_prop #CatAsPullback}
###### Proposition

The [[commuting diagram]] of [[1-categories]]

$$
  \array{
    Cat &\stackrel{N}{\hookrightarrow}& PSh(\Delta) \simeq sSet
    \\
    \downarrow^{\mathrlap{U}} && \downarrow^{\mathrlap{j^*}}
    \\
    Graph \simeq Sh(\Delta_0) &\stackrel{i_*}{\hookrightarrow}& PSh(\Delta_0)
  }
  \,,
$$

where

* $N$ forms the [[nerve of a category]];

* $U$ is the [[forgetful functor]] that sends a category to its underlying graph

is a [[pullback]].

=--

+-- {: .num_remark #AdjointsToTheSegalPullbackDiagram}
###### Remark

The morphisms in the commuting diagram of prop. \ref{CatAsPullback} participate in further [[adjunctions]], and in terms of these the Segal condition may further be reformulated as a restriction condition on [[algebras over an operad]]:

First of all the nerve has a [[left adjoint]] $\tau \colon PSh(\Delta) \to Cat$. With this the left adjoint $j_!$ of $j^*$ induces a left adjoint

$$
  F \simeq \tau j_! i_*
$$

of $U$, which is the [[free category]] functor. 

Moreover, with $U$ also $j^*$ is a [[monadic functor]] and the [[monad]] $U F \colon Grph \to Grph$ of which [[Cat]] is the category of [[algebras over a monad|algebras]] is the restriction of the monad $j^* \circ j_!$:

$$
  i_* U F \simeq j^* j_! i_* 
  \,.
$$


(All this is discussed in ([Berger, p. 13](#Berger)), and actually in the further generality of cellular sets that we get to [below](#InTermsOfPullBackOfCatOfSheavesForCellularObjects).)

In summary we have a diagram of adjoint pairs of functors of the form

$$
  \array{
    Cat &\stackrel{\overset{\tau}{\leftarrow}}{\underoverset{N}{\bottom}{\hookrightarrow}}& PSh(\Delta) \simeq sSet
    \\
    {}^{\mathllap{U}}\downarrow \vdash \uparrow^{\mathrlap{F}} && {}^{\mathllap{j^*}}\downarrow \vdash \uparrow^{\mathrlap{j_!}}
    \\
    Graph \simeq Sh(\Delta_0) &\stackrel{\overset{i^*}{\leftarrow}}{\underoverset{i_*}{\bottom}{\hookrightarrow}}& PSh(\Delta_0)
  }
$$

where several (however not all) subdiagrams of functors commute, as discussed above. 
In terms of this the reformulation of the Segal condition as in prop. \ref{CatAsPullback} is now further reformulated as:

_A category is equivalently an algebra over the monad $j^* j_!$ on $PSh(\Delta_0)$ which satisfies the Segal condition in that it is in the essential image of the functor $i_*$ of prop. \ref{NerveOfGraph}._

=--



#### For cellular objects and $\omega$-category objects
 {#InTermsOfPullBackOfCatOfSheavesForCellularObjects}

The immediate generalization of prop. \ref{CatAsPullback} from simplicial objects to [[cellular objects]] is the following.

Let 

$$
  j \colon \Theta_0 \to \Theta
$$

be the defining inclusion of the [[cellular site]] into the [[cell category]].

+-- {: .num_prop }
###### Proposition

The category $Str\omega Cat$ of [[strict ∞-categories]] is the [[pullback]]

$$
  \array{
    Str\omega Cat 
     &\underoverset{\simeq}{N}{\to}& Mod_\Theta &\hookrightarrow&      
PSh(\Theta)
    \\
    \downarrow^{\mathrlap{U}} && \downarrow^{} && \downarrow^{\mathrlap{j^*}}
   \\
   \omega Graph &\stackrel{\simeq}{\to}& Sh(\Theta_0) &\hookrightarrow& PSh(\Theta_0)
  }
  \,.
$$

=--

See at _[[globular theory]]_ for more.


## Related concepts

* [[Segal space]], [[complete Segal space]], [[n-fold complete Segal space]]

## References

The "Segal conditions" are originally due to:

* {#Grothendieck61} [[Alexander Grothendieck]], Prop. 4.1 of: _Techniques de construction et théorèmes d'existence en géométrie algébrique III : préschémas quotients_, Séminaire Bourbaki : années 1960/61, exposés 205-222, Séminaire Bourbaki, no. 6 (1961), Exposé no. 212,   ([numdam:SB_1960-1961__6__99_0](http://www.numdam.org/item/?id=SB_1960-1961__6__99_0), [pdf](http://www.numdam.org/item/SB_1960-1961__6__99_0.pdf))

and named after their mentioning in

* {#Segal} [[Graeme Segal]], Section 2 of: _Classifying spaces and spectral sequences_,  Publications Mathématiques de l'IHÉS, Volume 34  (1968), p. 105-112  ([numdam:PMIHES_1968__34__105_0](http://www.numdam.org/item/PMIHES_1968__34__105_0/)) 
 


The interpretation of the Segal condition as a [[sheaf]] condition is reviewed for instance in section 2 of 

* [[Joachim Kock]], _Polynomial functors and trees_ ([pdf](http://mat.uab.es/~kock/cat/poly-trees.pdf))

and discussed for [[strict infinity-categories]] in 

* [[Clemens Berger]], _A cellular nerve for higher categories_, Advances in Mathematics 169, 118-175 (2002) ([pdf](http://math1.unice.fr/~cberger/nerve.pdf))
 {#Berger}

Based on that, an iterative and homotopy-theoretic formulation of the cellular Segal conditions is in section 5 of 

* {#Rezk} [[Charles Rezk]], _A cartesian presentation of weak $n$-categories_ Geom. Topol. 14 (2010), no. 1, 521&#8211;571 ([arXiv:0901.3602](http://arxiv.org/abs/0901.3602))
 

[[!redirects Segal conditions]]
