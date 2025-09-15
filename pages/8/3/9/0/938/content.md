
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Equality and Equivalence
+--{: .hide}
[[!include equality and equivalence - contents]]
=--
=--
=--



# Weak homotopy equivalences
* table of contents
{: toc}

## Idea

A _[[weak homotopy equivalence]]_ is a map between [[topological spaces]] or [[simplicial sets]] or similar which induces [[isomorphisms]] on all [[homotopy groups]].  (The analogous concept in [[homological algebra]] is called a _[[quasi-isomorphism]]_.)

The [[localization]] or [[simplicial localization]] of the categories [[Top]] and [[sSet]] at the weak homotopy equivalences used as [[weak equivalences]] yields the standard [[homotopy category]] [[Ho(Top)]] and [[Ho(sSet)]] or the [[(∞,1)-category]] of [[∞-groupoids]]/[[homotopy types]], respectively.

Weak homotopy equivalences are named after _[[homotopy equivalences]]_. They can be identified with homotopy equivalences after replacing the [[domains]] by a [[resolution]]. The corresponding notions in [[homological algebra]] are [[quasi-isomorphisms]] and [[chain homotopy]]-equivalences.

From another perspective,  the notion of _weak homotopy equivalence_ is 'observational', in that a map is a weak homotopy equivalence if when we look at it through the observations that we can make of it using [[homotopy groups]] or even the [[fundamental infinity-groupoid]], it looks like an equivalence.   In contrast, _[[homotopy equivalence]]_ is more 'constructive'; in that $f$ is a homotopy equivalence if there exists an inverse for it (up to homotopy, of course).  Note that both of these notions are weaker than mere [[isomorphism]] of topological spaces (homeomorphism) and so can be considered examples of [[weak equivalence]]s.

There are actually two related concepts here: whether two spaces are weakly homotopy equivalent and whether a map between spaces is a weak homotopy equivalence.  The former is usually defined in terms of the latter.


## Definition (for topological spaces and simplicial sets)

+-- {: .num_defn #WeakHomotopyEquivalence}
###### Definition

For $X, Y \in $ [[Top]] or $\in $ [[sSet]] two [[topological spaces]] or [[simplicial sets]], a [[continuous function]] or [[simplicial set|simplicial map]] $f : X \to Y$ between them is called a **weak homotopy equivalence** if

1. $f$ induces an [[isomorphism]] of [[connected components]] (path components in the case of topological spaces)

   $$
     \Pi_0(f) \colon \Pi_0(X) \stackrel{\simeq}{\to} \Pi_0(Y)
   $$

   in [[Set]];

1. for all [[points]] $x \in X$ and for all $(1 \leq n) \in \mathbb{N}$ $f$ induces an isomorphism on [[homotopy groups]]

   $$
     \pi_n(f,x) \colon \pi_n(X,x) \stackrel{\simeq}{\to} \pi_n(Y,f(x))
   $$

   in [[Grp]].

=--


+-- {: .num_remark }
###### Remark

If $X$ and $Y$ are [[connected space|path-connected]], then (1) is trivial, and it suffices to require (2) for a single (arbitrary) $x$, but in general one must require it for at least one $x$ in each path [[connected component]].

=--

\begin{remark}
It is not enough to require that each pair of homotopy groups are isomorphic. For example, let $Y = S^1 \vee S^2$, and let $X$ be its double cover, which glues two spheres at the north and south poles of a circle. Then there are isomorphisms on the fundamental group $\pi_1(X) \simeq \mathbb{Z} \simeq \pi_1(Y)$, although the map $\pi_1(X) \to \pi_1(Y)$ induced by $f$ is not an isomorphism. And by the properties of covering spaces, all higher homotopy groups are isomorphic. But these two are not weakly homotopy equivalent.
\end{remark}

\begin{remark}
There are many alternative definitions of weak homotopy equivalences.
A simplicial map $f$ is a weak equivalence of simplicial sets
if and only if $Ex^\infty f$ is a simplicial homotopy equivalence
if and only if $Hom(f,A)$ is a simplicial homotopy equivalence for any [[Kan complex]] $A$
if and only if $f$ has a right relative-homotopy-lifting property with respect
to the maps $\partial\Delta^n\to\Delta^n$
if and only if $f$ is a composition of an acyclic cofibration
(i.e., a map with a left lifting property with respect to all maps with a right lifting
property with respect to horn inclusions)
and an acyclic fibration (i.e., a map
with a right lifting property with respect to inclusions $\partial\Delta^n\to\Delta^n)$.
A continuous map $f$ is a weak equivalence of topological spaces
if and only if $|Sing(f)|$ is a homotopy equivalence of topological spaces
if and only if $Hom(A,f)$ is a homotopy equivalence for any [[CW-complex]] $A$
if and only if $f$ has a right relative-homotopy-lifting property with respect
to the maps $S^{n-1}\to D^n$
if and only if $f$ is a composition of an acyclic Serre cofibration
(a retract of a relative CW-complex) and an acyclic [[Serre fibration]].
Both functors $|-|$ and $Sing$ preserve and reflect weak equivalences,
so any of the two classes defines the other.
\end{remark}


+-- {: .num_defn }
###### Definition


The [[homotopy category]] of [[Top]] with respect to weak homotopy equivalences is [[Ho(Top)]]${}_{whe}$.

=--

+-- {: .num_remark }
###### Remark

Accordingly, weak homotopy equivalences are the [[weak equivalences]] in the standard [[Quillen model structure on topological spaces]] and the [[Quillen model structure on simplicial sets]], and also in the [[mixed model structure]].

=--

## Properties

### Equivalent characterizations
 {#EquivalentCharacterizations}

+-- {: .num_prop }
###### Proposition

A continuous map $f : X \to Y$ is a weak homotopy equivalence 
precisely if for all $n \in \mathbb{N}$ and for all [[commuting diagrams]] of continuous maps of the form

$$
  \array{
    S^{n-1} &\to& X
    \\
    \downarrow && \downarrow^{\mathrlap{f}}
    \\
    D^n &\to& Y
  }
  \,,
$$

where the left morphism is the inclusion of the $(n-1)$-[[sphere]] as the [[boundary]] of the $n$-[[ball]], 
there exists a continuous map $\sigma : D^n \to X$
that makes the resulting upper triangle commute and such that the lower triangle commutes up to a [[homotopy]]

$$
  \array{
    S^{n-1} &&\to&& X
    \\
    \\
    \downarrow && \nearrow & \swArrow& \downarrow^{\mathrlap{f}}
    \\\\
    D^n &&\to&& Y
  }
$$

which is constant along $S^{n-1} \hookrightarrow D^n$.

=--

In this form the statement and its proof appears in 
([Jardine](#Jardine)) (where it is also generalized to weak equivalences in a [[model structure on simplicial presheaves]]). 
See also around ([Lurie, prop. 6.5.2.1](#Lurie)). The relevant arguments are spelled out in ([May, section 9.6](#May)). A variant is called the _HELP lemma_ in ([Vogt](#Vogt)).


### Relation to homotopy equivalences
 {#RelationToHomotopyEquivalences}

+-- {: .num_prop }
###### Proposition

Every [[homotopy equivalence]] is a weak homotopy equivalence.  

=--

+-- {: .proof}
###### Proof

It requires a little bit of thought to prove this, because $f$ and its homotopy inverse $g$ need not preserve any chosen basepoint.  But for any $x\in X$ and any $n\ge 1$, we have a [[commuting diagram]]
$$
\array{
  \pi_n(X,x) & & \to & & \pi_n(X,g(f(x)))
  \\
  & 
  \searrow 
  && 
  \nearrow 
  && 
  \searrow
  \\
  && 
  \pi_n(Y,f(x)) 
  && 
  \longrightarrow 
  && 
  \pi_n\big(
    Y,f(g(f(x)))
  \big)
  }
$$
in which the two horizontal morphisms are [[isomorphisms]], because $g f$ and $f g$ are [[homotopy|homotopic]] to [[identity morphism|identities]].  Hence, by the [[two-out-of-six property]] for isomorphisms, the diagonal morphisms are also all isomorphisms.

=--

+-- {: .num_prop }
###### Proposition

Conversely, any weak homotopy equivalence between [[m-cofibrant spaces]] (spaces that are homotopy equivalent to [[CW complexes]]) is a [[homotopy equivalence]].

=--

### Relation to homotopy types
 {#RelationToHomotopyTypes}

We discuss the [[equivalence relation]] generated by weak homotopy equivalence, called _(weak) [[homotopy type]]_. For the "abelianized" analog of this situation see at [[quasi-isomorphism]] the section _[Relation to homology type](quasi-isomorphism#RelationToChainHomologyType)_.

+-- {: .num_prop #ReflexiveAndTransitiveButNotSymmetric}
###### Proposition

The existence of a weak homotopy equivalence from $X$ to $Y$ is a [[reflexive relation|reflexive]] and [[transitive relation]] on [[Top]], but it is not a  [[symmetric relation]].  

=--

+-- {: .proof}
###### Proof

Reflexivity and transitivity are trivially checked. A counterexample to symmetry
is example \ref{CircleAndPseudoCircle} below.

=--

But we can consider the genuine equivalence relation _generated_ by weak homotopy equivalence:

+-- {: .num_defn }
###### Definition

We say two spaces $X$ and $Y$ have the same **(weak) [[homotopy type]]** if they are equivalent under the [[equivalence relation]] _generated_ by weak homotopy equivalence.

=--

+-- {: .num_remark }
###### Remark

Equivalently this means that $X$ and $Y$ have the same (weak) homotopy type
if there exists a [[zigzag]] of weak homotopy equivalences 

$$
  X \leftarrow \to\leftarrow \dots \to Y
  \,.
$$

This in turn is equivalent to saying that $X$ and $Y$ become [[isomorphism|isomorphic]] in the [[homotopy category]] [[Ho(Top)]]/[[Ho(sSet)]] with the weak homotopy equivalences [[localization|inverted]].

=--

+-- {: .num_remark }
###### Remark

Two spaces $X$ and $Y$ may have isomorphic homotopy groups without being weak homotopy equivalence: for this all the isomorphisms must be induced by an actual map $f : X \to Y$, as in the above definition.

However, if, roughly, one remembers,  how all the homotopy groups [[nLab:action|act]] on each other, then this is enough information to exhibit the full homotopy type. This collection of data is called the _[[Postnikov tower]]_ decomposition of a homotopy type.

=--

### Relation to free homotopy sets
 {#RelationToFreeHomotopySets}

For $K, X \,\in\, TopSp$, write $Map(K, X)$ for their [[mapping space]], i.e. not considering or respecting any [[basepoint]]. For example,  $Map(S^1, Y)$ is the [[free loop space]] of $Y$, in contrast to the [[based loop space]] 

$$
  \Omega_x X 
    \xhookrightarrow{\; fib_x(ev_\ast) \;} 
  Map(S^1, X) 
    \overset{\; ev_x \;}{\twoheadrightarrow}
  X
$$

for any base point $x \,\in\, X$.

Moreover, when $K$ is a [[CW complex]], write

\[
  \label{FreeHomotopySets}
  {[K,X]} \,\coloneqq\, \tau_0 \,Map(K,X)\,
\]

for the *free homotopy set* of maps from $K$ to $X$, hence the set of [[homotopy classes]] of map $K \to X$, hence the set of [[connected components]] of the mapping space.


\begin{proposition}
**(weak homotopy equivalences detected on free homotopy sets)**
\label{WeakHomotopyEquivalencesDetectedOnTermsOfFreeHomotopySet}
\linebreak
  For $f \,\colon\, X \to Y$, a [[continuous function]] between [[connected topological spaces]], the following are equivalent:

1. $f$ is a [[weak homotopy equivalence]]
  
   $$
     \underset{n \in \mathbb{N}}{\forall}
     \;
     \;\;
     p_n(X)
     \underoverset
       {\simeq}
       {f_\ast}
       {\longrightarrow}
     \pi_n(Y)
     \,;
   $$

1. $f$ induces an [[isomorphism]] on all free homotopy sets (eq:FreeHomotopySets) out of [[CW-complexes]]:


   $$
     \underset{ K \in CWCplx}{\forall}
     \;\;
     [K, X]
     \underoverset
       {\simeq}
       {f_\ast}
       {\longrightarrow}
     [K, Y]
     \,;
   $$


* $f$ induces 

  1. an [[isomorphism]] on all free homotopy sets (eq:FreeHomotopySets) out of $K = $any [[n-sphere]] of [[positive number|positive]] [[dimension]],

     $$
       \underset{ 
         n \in \mathbb{N}_+
       }{\forall}
       \;\;
       [S^n, X]
       \underoverset
         {\simeq}
         {f_\ast}
         {\longrightarrow}
       [S^n, Y]
       \,.
     $$


  1. a [[surjection]] on the free homotopy set out of the [[wedge sum]] of [[circles]] [[index set|indexed]] by (the set [[underlying]]) the [[fundamental group]] of $Y$:

     $$
        \big[
          \underset{\pi_1(Y)}{\vee} S^1
          ,\,
          X
        \big]
        \overset{\; f_\ast \;}{\twoheadrightarrow}
        \big[
          \underset{\pi_1(Y)}{\vee} S^1
          ,\,
          Y
        \big]
     $$

\end{proposition}
([Matumoto, Minami and Sugawara 1984, Thm. 2](#MatumotoMinamiSugawara84))
\begin{proof}
  The implication $(1) \Rightarrow (2)$ is a standard/classical conclusion in homotopy theory, for example it is a small special case of the fact that  $Map(K,-)$ out of any cell complex $K$ preserves weak homotopy equivalences ([this Prop.](classical+model+structure+on+topological+spaces#HomProductAdjunctionForCofibrantObjectInTopCGIsQuillen)).

The implication $(2) \Rightarrow (3)$ is trivial, as the conditions in (3) are just a special case of the condition in (2).

So the point of the statement is that (3) is already sufficient to recover (1). This is the content of [Matumoto, Minami and Sugawara 1984, Thm. 1 & Lem. 1.3](#MatumotoMinamiSugawara84).
\end{proof}


## For other kinds of spaces


A map of [[simplicial sets]] is called a weak homotopy equivalence equivalently if its [[geometric realization]] is a weak homotopy equivalence of topological spaces, as above.  (Since the geometric realization of any simpicial set is a 
[[CW complex]], in this case its geometric realization is actually a [[homotopy equivalence]].)  

Likewise, a [[functor]] between [[small category|small]] categories is sometimes said to be a weak homotopy equivalence if its [[nerve]] is a weak homotopy equivalence of simplicial sets, hence of topological spaces after [[geometric realization of categories]].  These are the weak equivalences in the 
[[Thomason model structure]] on categories (not the [[canonical model structure]]). The statement of [[Quillen's theorem A]] and [[Quillen's theorem B]] in in this contex.

Similarly, one can define weak homotopy equivalences between any sort of object that has a [[geometric realization]], such as a [[cubical set]], a [[globular set]], an [[n-category]], an [[n-fold category]], and so on.

Note that in some of these cases, such as as simplicial sets, symmetric sets, and probably cubical sets, there is also a notion of "homotopy equivalence" from which this notion needs to be distinguished.  A simplicial homotopy equivalence, for instance, is a simplicial map $f:X\to Y$ with an inverse  $g:Y\to X$ and simplicial homotopies $X\times \Delta^1 \to X$ and $Y\times \Delta^1 \to Y$ relating $f g$ and $g f$ to identities.

A different direction of generalization is the notion of a [[homotopy equivalence of toposes]].

## Examples

### Of non-reversible weak homotopy equivalences
 {#ExamplesOfNonReversibleWHEs}

We discuss examples of weak homotopy equivalences that have no weak homotopy equivalence going the other way, according to prop. \ref{ReflexiveAndTransitiveButNotSymmetric} above.

+-- {: .num_example #CircleAndPseudoCircle}
###### Example

Let $S^1 \in $ [[Top]] denote the ordinary [[circle]] and $\mathbb{S}$ the 
[[pseudocircle]].

There is a [[continuous function]] $S^1 \to \mathbb{S}$ which is a weak homotopy equivalence, hence in particular $\pi_1(\mathbb{S}) \simeq \mathbb{Z}$. But every continuous map the other way round has to induce the trivial map on $\pi_1$.

=--

This is the simplest in a class of counter-examples discussed in ([McCord](#McCord)).

## Related concepts

* [[equality]]

* [[isomorphism]]

* [[equivalence]]

* [[weak equivalence]]

* [[homotopy equivalence]], **weak homotopy equivalence**

  * [[rational homotopy equivalence]]

  * [[n-equivalence]]

  * [[equivariant weak homotopy equivalence]]

  * [[stable weak homotopy equivalence]]

* [[Bousfield equivalence]]

* [[homotopy equivalence of toposes]]

* [[equivalence in an (∞,1)-category]]

* [[equivalence of (∞,1)-categories]]

## References

A general account is for instance in section 9.6 of 

* {#May} [[Peter May]], _[[A Concise Course in Algebraic Topology]]_
 

The characterization of weak homotopy equivalences by lifts up to homotopy seems is in

* {#Jardine} [[J. F. Jardine]], _Simplicial Presheaves_, Journal of Pure and Applied Algebra 47, 1987, no.1, 35-87.
 

* {#Vogt} [[Rainer Vogt]], _The HELP-Lemma and its converse in Quillen model categories_ ([arXiv:1004.5249](http://arxiv.org/abs/1004.5249))
 

For related and general discussion see also section 6.5 of 

* {#Lurie} [[Jacob Lurie]], _[[Higher Topos Theory]]_
 

Examples for the non-symmetry of the weak homotopy equivalence relation are in 

* {#McCord} [[Michael McCord]], _Singular homology groups and homotopy groups of finite topological spaces_, Duke Math. J. Volume 33, Number 3 (1966), 465-474. ([euclid.dmj/1077376525](http://projecteuclid.org/euclid.dmj/1077376525))
 
See also:

* Topospaces-Wiki, _[Weak homotopy equivalence of topological spaces](http://topospaces.subwiki.org/wiki/Weak_homotopy_equivalence_of_topological_spaces)_

Detection in terms of free homotopy sets:

* {#MatumotoMinamiSugawara84} [[Takao Matumoto]], [[Norihiko Minami]], [[Masahiro Sugawara]], *On the set of free homotopy classes and Brown's construction*, Hiroshima Math. J. 14(2): 359-369 (1984) ([doi:10.32917/hmj/1206133043](https://projecteuclid.org/journals/hiroshima-mathematical-journal/volume-14/issue-2/On-the-set-of-free-homotopy-classes-and-Browns-construction/10.32917/hmj/1206133043.full))


[[!redirects weak homotopy equivalences]]