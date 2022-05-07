+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Recall that a [[simplicial set]] is a combinatorial [[model structure on simplicial sets|model]] for a [[topological space]]. This relation is most immediate when the simplicial set is in fact a [[Kan complex]] (an [[∞-groupoid]]).

A _simplicial group_ is a simplicial set with the structure of a [[group]] on it. It turns out that this necessarily means that it is also a [[Kan complex]]. Therefore a simplicial group is

* an [[∞-groupoid]] with an extra group structure on it;

* a model for a topological space with a group structure.

Accordingly (as discussed at [[group]]) a simplicial group $G$ gives rise to 

* a one-object $\infty$-groupoid $\mathbf{B} G$ whose explicit standard realization as a [[simplicial set]] is denoted $\bar W G$

* an $\infty$-groupoid $\mathbf{E} G$ whose explicit standard realization as a [[simplicial set]] (even a simplicial group, again) is denoted $W G$

* such that there is a fibration
  $$
    \array{
       \mathbf{E} G
       &:=& W G
       \\
       \downarrow && \downarrow
       \\
       \mathbf{B} G
       &:=&
       \bar W G
    }
  $$
  which is the [[generalized universal bundle|universal G-bundle]].

Simplicial abelian groups are models for [[connective spectrum|connective]] [[module spectrum|modules]] over the [[Eilenberg-Mac Lane spectrum]] $H \mathbf{Z}$; see [[Dold-Kan correspondence]] and [[stable Dold-Kan correspondence]].

## Definition

A **simplicial group**, $G$, is a [[simplicial object]] in the [[category]] [[Grp]] of [[group]]s.


The [[category]] of simplicial groups is the category of functors from $\Delta^{op}$ to [[Grp]].  It will be denoted $\Simp\Grp$.



## Properties

### As Kan complexes
 {#AsKanComplexes}

+-- {: .num_theorem #MooreTheorem}
###### Theorem (J. C. Moore)

The [[simplicial set]] underlying any simplicial group
(by forgetting the group structure) is a [[Kan complex]].

=--

This is due to ([Moore, 1954](#Moore54))

In fact, not only are the [[horn]] fillers guaranteed to exist, but there is an algorithm that provides explicit fillers.  This implies that constructions on a simplicial group that use fillers of horns can often be adjusted to be functorial by using the algorithmically defined fillers.  An argument that just uses 'existence' of fillers can be refined to give something more 'coherent'.


+-- {: .proof}
###### Proof

Let $G$ be a simplicial group. 

Here is the explicit algorithm that computes the horn fillers:

Let $(y_0,\ldots, y_{k-1}, -,y_{k+1}, \ldots, y_n)$ give a [[horn]] in $G_{n-1}$, so the $y_i$s are $(n-1)$ simplices that fit together as if they were all but one, the $k^{th}$ one,  of the faces of an $n$-simplex. There are three cases: 

1. if $k = 0$: 

   * Let  $w_n = s_{n-1}y_n$ and then $w_i = w_{i+1}(s_{i-1}d_i w_{i+1})^{-1}s_{i-1}y_i$ for  $i = n-1, \ldots, 1$, then  $w_1 $ satisfies $d_i w_1 = y_i$, $i\neq  0$;

1. if $0\lt k \lt n$: 

   * Let $w_0 = s_0 y_0$ and $w_i = w_{i-1}(s_i d_i w_{i-1})^{-1}s_i y_i$ for $i = 1, \ldots, k-1$, then take $w_n = w_{k-1}(s_{n-1}d_n w_{k-1})^{-1}s_{n-1}y_n$, and finally a downwards induction given by $w_i = w_{i+1}(s_{i-1}d_{i}w_{i+1})^{-1}s_{i-1}y_i$, for $i = n-1, \ldots, k+1$, then $w_{k+1}$ gives $d_{i}w_{k+1} = y_i$ for $i \neq k$;


3. if $k=n$: 

   * use $w_0 = s_0 y_0$ and $w_i = w_{i-1}(s_i d_i w_{i-1})^{-1}s_i y_i$ for $i = 1, \ldots, n-1$, then $w_{n-1}$ satisfies $d_i w_{n-1} = y_i$, $i\neq n$.



=--

+-- {: .num_remark}
###### Remarks

* The filler for any horn can be chosen to be a _product of degenerate elements_.

* The [[simplicial homotopy groups]] of a simplicial group, $G$, can be calculated as the homology groups of the [[Moore complex]] of $G$.  This is, in general,  a non-Abelian chain complex.

* A simplicial group can be considered as a [[simplicial groupoid]] having exactly one object. If $G$ is a simplicial group, the suggested notation for the corresponding simplicially enriched groupoid would be $\mathbf{B}G$ according to notational conventions suggested elsewhere in the nLab.

* There is a functor due to Dwyer and Kan, called the [[Dwyer-Kan loop groupoid]] that takes a  simplicial set to a simplicial groupoid. This has a left adjoint $\overline{W}$ (see below), called the _classifying space_ functor, and together they give an equivalence of categories between the homotopy category of simplical sets and that of simplicial groupoids. We thus have that all homotopy types are modelled by simplicial groupoids ... and for connected homotopy types by simplicial groups. One *important fact* to note in this equivalence is that it shifts dimension by 1, so if $G(K)$ is the simplicial group corresponding to the connected simplicial set $K$ then $\pi_k(K)$ is the same as $\pi_{k-1}(G(K))$.  This is important when considering algebraic models for a [[homotopy n-type]].

=--

### Fiber sequences
 {#FiberSequences}

+-- {: .num_prop}
###### Proposition

Let $G$ be a simplicial group and $G_0$ its group of 0-cells, regarded as a simplicially constant simplicial group. Write $G/G_0$ for the evident [[quotient]] of simplicial groups.

The evident morphisms

$$
  G_0 \to G \to G/G_0 \simeq \mathbf{B} \Omega G/G_0
$$

form a [[fiber sequence]] in [[sSet]].

=--

+-- {: .proof}
###### Proof

One checks that for $X$ any simplicial set and $G$ a simplicial group acting freely on it, the [[quotient]] map

$$
  X \to X/G
$$

is a [[Kan fibration]]. This is for instance 
([Weibel, exercise 8.2.6](#Weibel)). By the disucssion at [[fiber sequence]] it is therefore sufficient to observe that

$$
  \array{
    G_0 &\to& *
    \\
    \downarrow && \downarrow
    \\
    G &\to& G/G_0
  }
$$

is an ordinary [[pullback]] of simplicial sets. 
This is clear since the action of $G_0$ on $G$ is degreewise free (being the action of a subgroup).

=--

+-- {: .num_example}
###### Example

Let $(G_1 \stackrel{\delta}{\to} G_0)$ be a [[crossed module]] of groups, write 

$$
  [G_1 \stackrel{\delta}{\to} G_0]
  =
  \left(
    G_0 \times G_1 
    \stackrel{\overset{(\delta p_2)\cdot p_1}{\to}}{\underset{p_1}{\to}}
    G_0
  \right)
$$

for [[groupoid]] which is the corresponding [[strict 2-group]] and write $N[G_1 \to G_0]$ for the [[nerve]] being the corresponding simplicial group. Then the above says that

$$
  G_0 \to [G_1 \stackrel{\delta}{\to} G_0]
  \to 
  \mathbf{B}G_1
$$

is a fiber sequence of [[groupoid]]s. 

=--


###  Free simplicial groups

+-- {: .num_lemma}
###### Lemma
 
The [[stuff, structure, property|forgetful functor]]

$$
  U : AbSGrpg \to SSet
$$

from simplicial [[abelian group]]s to the underlying [[simplicial sets]] has a [[left adjoint]]

$$
  \mathbb{Z} : SSet \to AbSimpGrp
$$

from [[simplicial sets]] to abelian simplicial groups, 
the **free simplicial abelian group** functor
that sends the set $X_n$ of $n$-simplices to the free abelian group $(\mathbb{Z}X)_n = \mathbb{Z} X_n$ over it.

This functor $\mathbb{Z}$ has the following properties:

* it preserves weak equivalences 

* $\mathbb{Z} X$ is a cofibrant simplicial group

=--

(...)

### Looping and delooping

Let $sSet_0 \hookrightarrow$ [[sSet]] be the category of _reduced simplicial sets_ (simplicial sets with a single 0-cell).

+-- {: .num_defn}
###### Definition

For $X \in sSet_0$ define $\Omega X \in sGrpd$ by

$$
  \Omega X :  [n] \mapsto  (F X_{n+1})/ s_0 F(X_n)
$$


and

$$
  \Omega X : ([n] \to [k]) \mapsto ...
$$


=--

### As $\infty$-groups
 {#AsInfinityGroups}

Simplicial groups are models for [[∞-group]]s. This is exhibited by the [[model structure on simplicial groups]]. See also
<a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity%2C1)-category#ModelsInInfGrpd">models for group objects in ∞Grpd</a>.

Another equivalent model is that of [[connected]] [[Kan complex]]es. 

At the abstract level of [[(∞,1)-category theory]] this equivalence is induced by forming [[loop space object]]s and [[delooping]]

$$
  \Omega
  :
  \infty Grpd_{con} \stackrel{\leftarrow}{\to}
  \infty Grp
  :
  \mathbf{B}
  \,.
$$

This [[equivalence of quasi-categories|(∞,1)-equivalence]] is modeled by a [[Quillen equivalence]] of [[model categories]] whose [[right adjoint]] Quillen functor is the operation $\overline{W}$ discussed above.

$$
  \mathcal{G} : sSet_0 \stackrel{\stackrel{\simeq_{Quillen}}{\longleftarrow}}{\longrightarrow} sGrp
  : \overline{W}
  \,.
$$

This is for instance in [GoerssJardine, chapter 5](#GoerssJardine).


See also <a href="http://ncatlab.org/nlab/show/groupoid+object+in+an+(infinity%2C1)-category#ModelsInInfGrpd">group object in an (∞,1)-category -- models for groups in ∞Grpd</a>.


### Closed monoidal structure
 {#ClosedMonoidalStructure}

The [[category]] $sAb$ of simplicial abelian groups is naturally a [[monoidal category]], with the tensor product being degreewise that of abelian groups. This is indeed a [[closed monoidal category]]. For $A, B$ The [[internal hom]] $[A,B]$ is the simplicial abelian group whose underlying simplicial set is

$$
  [A,B] : [n] \mapsto Hom_{sAb}(A \otimes \mathbb{Z}[\Delta[n]], B)
  \,,
$$

where $\mathbf{Z}[-] : sSet \to sAb$ is degreewise the [[free construction|free]] abelian group functor.

## Delooping and simplicial principal bundles  {#DeloopingAndBundle}

For $G$ a simplicial group, we describe its [[delooping]] [[Kan complex]] $\mathbf{B}G  \in sSet$ and the corresponding [[generalized universal bundle]] $\mathbf{E}G \to \mathbf{B}G$ such that the ordinary [[pullback]]

$$
  \array{
    P_\bullet &\to& \mathbf{E}G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\stackrel{g}{\to}& \mathbf{B}G
  }
$$  

in [[sSet]] models the [[homotopy pullback]] in $sSet_{Quillen}$ / [[(∞,1)-pullback]] in [[∞Grpd]]

$$
  \array{
    P_\bullet &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    X_\bullet &\to& \mathbf{B}G
  }
  \,.
$$  

in the standard [[model structure on simplicial sets]] and hence produces the [[principal ∞-bundle]] $P_\bullet \to X_\bullet$ classified by $X_\bullet \to \mathbf{B}G$.

For all these constructions exist very explicit combinatorial formulas that go by the symbols

* $\overline{W}G$ for the [[delooping]] $\mathbf{B}G$

* $W G$ for the [[generalized universal bundle]] $\mathbf{E}G$

* $\tau : X_\bullet \to G_\bullet$ (called the _[[twisting function]]_) for the [[cocycle]] $X_\bullet \to \mathbf{B}G$;

* $X_\bullet \times_g W G$ for $P_\bullet$ (called _[[twisted Cartesian product]]_ ).

All of these constructions are functorial and hence lift from the context of [[simplicial set]]s to that of [[simplicial presheaves]] over some [[site]] $C$. There they provide models for strict [[group object in an (infinity,1)-category|group objects]], [[delooping]] and [[principal ∞-bundle]]s in the corresponding [[(∞,1)-topos]]es over $C$. In particular in the projective model structure on $[C^{op}, sSet]$ the pullback of the objectwise $W G \to \overline{W}G$ is still a homotopy pullback and models the corresponding principal $\infty$-bundles.


### Delooping {#Delooping}

A simplicial group $G$ is a [[group object in an (infinity,1)-category|group object]] [[internalization|internal]] to the category of [[Kan complex]]es. Accordingly, there should be a [[Kan complex]] $\mathbf{B}G$ which is the [[delooping]] of $G$, i.e. a Kan complex with an essentially unique object, such that the [[loop space object]] of that Kan complex reproduces $G$.

An explicit construction of $\mathbf{B}G$ from $G$ goes traditionally by the symbol $\bar W G \in KanCplx$. Another one by $d B G$.

#### Delooping modeled by $\bar W G$


It is immediate to deloop the simplicial group $G$ to the [[simplicial groupoid]] that in degree $k$ is the 1-[[groupoid]] with a single object and $G_k$ as its collection of morphisms. 


+-- {: .num_defn}
###### Definition

For $\mathcal{G}$ a [[simplicial groupoid]] that on objects is a constant simplicial set, define a [[simplicial set]] $\bar W \mathcal{G}$ as follows.

* $(\overline{W}\mathcal{G})_0 := ob(\mathcal{G}_0)$, the set of objects of the groupoid of 0-simplices (and hence of the groupoid at each level);

* $(\overline{W}\mathcal{G})_1 = Mor(\mathcal{G}_0)$, the collection of [[morphism]]s of the groupoid $\mathcal{G}_0$:

and for $n \geq 2$,

*  $(\overline{W}\mathcal{G})_n = \{(h_{n-1}, \ldots ,h_0)| h_i \in Mor(\mathcal{G}_i)$  and $s(h_{i-1}) = t(h_i), 0\lt i\lt n\}$.

Here  $s$ and $t$ are generic symbols for the domain and codomain mappings of all the groupoids involved.  The face and degeneracy mappings between 
$\overline{W}(\mathcal{G})_1$ and $\overline{W}(\mathcal{G})_0$ are the source and target maps and the identity maps of $\mathcal{G}_0$, respectively; whilst the face and degeneracy maps at higher levels are given as follows:

The face and degeneracy maps are given by

* $d_0(h_{n-1}, \ldots, h_0) = (h_{n-2}, \ldots, h_0)$;


*  for $0 \lt  i\lt  n$, $d_i(h_{n-1}, \ldots, h_0)  = (d_{i-1}h_{n-1}, d_{i-2}h_{n-2}, \ldots, d_0h_{n-i}h_{n-i-1},h_{n-i-2}, \ldots , h_0)$; 

and

*  $d_n(h_{n-1}, \ldots, h_0) = (d_{n-1}h_{n-1}, d_{n-2}h_{n-2}, \ldots, d_1h_{1})$;


whilst

*  $s_0(h_{n-1}, \ldots, h_0) = (id_{dom(h_{n-1})},h_{n-1}, \ldots, h_0) $;

and,


* for $0\lt i \leq n$, $s_i(h_{n-1}, \ldots, h_0) = (s_{i-1}h_{n-1}, \ldots, s_0h_{n-i}, id_{cod(h_{n-i})},h_{n-i-1}, \ldots,  h_0) $.

=--

+-- {: .num_defn}
###### Definition

For $G$ a simplicial group and $\mathcal{G}$ the corresponding one-object [[simplicial groupoid]], one writes

$$
  \overline{W}G := \overline{W}\mathcal{G}
  \,.
$$

=--


+-- {: .num_remark}
###### Remark

The above construction has a straightforward [[internalization]] to contexts other than [[Set]]. For instance if $G$ is a [[simplicial object]] in [[topological group]]s or in [[Lie group]]s, then $\overline{W}G$ with

$$
  (\overline{W}G)_n :=
  G_{n-1} \times G_{n-2} \times \cdots \times G_0
$$

is a [[simplicial object]] in this context ([[topological spaces]], [[smooth manifold]]s, etc.)

In particular, if $C$ is a [[small category]] and $G : C^{op} \to sSet$ is a [[simplicial presheaf]] that is objectwise a simplicial group, then we have the simplicial presheaf

$$
  \overline{W}G : c \mapsto \overline{W}(G(c))
  \,.
$$


=--

#### Delooping modeled by $d B G$

For $G$ a [[simplicial group]], write $B G$ for the [[bisimplicial set]] obtained by taking degreewise the [[nerve]] of the [[delooping]] [[groupoid]]. Write $d B G \in $ [[sSet]] for its [[delooping]].

+-- {: .num_theorem}
###### Theorem

There is a [[weak homotopy equivalence]]

$$
  \bar W G \simeq d B G
  \,.
$$

=--

This is shown for instance in ([JardineLuo](#JardineLuo)) and in ([CegarraRemedios](#CegarraRemedios)).


#### Examples

If $G$ is an ordinary [[group]], regarded as a simplicially constant simplicial group, then $\overline{W}G$ is the usual bar complex of $G$:

$$
  \overline{W}G =
  \left(
    \cdots G \times G \stackrel{\to}{\stackrel{\to}{\to}} G \stackrel{\to}{\to} *
  \right)
  \,.
$$



### Cocycles {#UniversalBundle}

For $X_\bullet$ a [[simplicial set]] a morphism 

$$
  g : X_\bullet \to \overline{W}G
$$

in [[sSet]] corresponds precisely to what is called a [[twisting function]], a family of maps

$$
  \{\phi(g)_n : X_n \to G_{n-1}\}
$$

satisfying the relations

$$
\array{
  d_0 \phi(x) = \phi(d_1 x)(\phi(d_0 x))^{-1}
  \\
  d_i \phi(x) = \phi(d_{i+1}x), i\gt 0,
  \\
  s_i\phi(x) = \phi(s_{i+1}x), i\geq 0,
  \\
  \phi(s_0 x) = 1_G.
}
$$


### Simplicial Principal bundles {#PrincipalBundles}

Simplicial groups model all [[∞-group]]s in [[∞Grpd]]. Accordingly all [[principal ∞-bundle]]s in [[∞Grpd]] should be modeled by [[simplicial principal bundle]]s.


+-- {: .num_defn}
###### Definition
**(principal action)**

Let $G$ be a simplicial group. For $P$ a [[Kan complex]], an 
[[action]] of $G$ on $E$

$$
  \rho : E \times G \to E
$$

is called **principal** if it is degreewise principal, i.e. if for all $n \in \mathbb{N}$ the only elements $g \in G_n$ that have any fixed point $e \in E_n$ in that $\rho(e,g) = e$ are the neutral elements.

=--

+-- {: .num_example}
###### Example

The canonical action 

$$
  G \times G \to G
$$

of any simplicial group on itself is principal.

=--

+-- {: .num_defn}
###### Definition
**(simplicial principal bundle)**

For $G$ a simplicial group, a morphism $P \to X$ of [[Kan complex]]es equipped with a $G$-[[action]] on $P$ is called a $G$-**simplicial principal bundle** if

* the action is principal;

* the base is isomorphic to the quotient $E/G := \lim_{\to}(E \times G \stackrel{\overset{\rho}{\to}}{\underset{p_1}{\to} E})$ by the action:

  $$
    E/G \simeq X
    \,.
  $$ 

=--


+-- {: .num_prop}
###### Proposition

A simplicial $G$-principal bundle $P \to X$ is necessarly a [[Kan fibration]].

=--

+-- {: .proof}
###### Proof

This appears as Lemma 18.2 in [MaySimpOb](#MaySimplicialObjects).

=--


#### Universal simplicial $G$-principal bundle {#UniversalSimplicialBundle}

+-- {: .num_defn}
###### Definition

For $G$ a simplicial group, define the [[simplicial set]] $W G$ to be the [[decalage]] of $\overline{W}G$

$$
  W G := Dec \overline{W}G
  \,.
$$

=--


By the discussion at [[homotopy pullback]] this means that for $X_\bullet$ any [[Kan complex]], an ordinary [[pullback]] diagram

$$
  \array{
    P_\bullet &\to& W G
    \\
    \downarrow && \downarrow
    \\
    X_\bullet &\stackrel{g}{\to}& \overline{W}G
  }
$$

in [[sSet]] exhibits $P_\bullet$ as the [[homotopy pullback]] in $sSet_{Quillen}$ / [[(∞,1)-pullback]] in [[∞Grpd]]

$$
  \array{
    P_\bullet &\to& *
    \\
    \downarrow &\swArrow& \downarrow
    \\
    X_\bullet &\stackrel{g}{\to}& \overline{W}G
  }
  \,,
$$

i.e. as the [[homotopy fiber]] of the cocycle $g$.

+-- {: .num_defn}
###### Definition

We call $P_\bullet := X_\bullet \times^g W G$ the simplicial $G$-[[principal bundle]] corresponding to $g$.

=--

+-- {: .num_prop}
###### Proposition

Let $\{\phi : X_n \to G_{(n-1)}\}$ be the [[twisting function]] corresponding to $g : X_\bullet \to \overline{W}G$ by the above discussion.

Then the simplicial set  $P_\bullet := X_\bullet \times_{g} W G$ is explicitly given by the formula called the [[twisted Cartesian product]] $X_\bullet \times^\phi G_\bullet$:

its cells are

$$
  P_n  = X_n \times G_n
$$

with face and degeneracy maps

*  $d_i (x,g) = (d_i x , d_i g)$ if $i \gt 0$

* $d_0 (x,g) = (d_0 x, \phi(x) d_0 g)$

* $s_i (x,g) = (s_i x, s_i g)$.

=--

#### References {#SimplicialBundleReferences}

Here are some pointers on where precisely in the literature the above statements can be found.

One useful reference is

* [[Peter May]], _Simplicial Objects in Algebraic Topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu)).

There the abbreviation PCTP ( _principal twisted cartesian product_ ) is used for what above we called just [[twisted Cartesian product]]s.

The fact that every PTCP $X \times_\phi G \to X$ defined by a [[twisting function]] $\phi$ arises as the pullback of $W G \to \overline{W}G$ along a morphjism of simplicial sets $X \to \overline{W}G$ can be found there by combining

1. the last sentence on p. 81 which asserts that pullbacks of PTCPs $X \times_\phi G \to X$ along morphisms of simplicial sets $f : Y \to X$ yield PTCPs corresponding to the composite of $f$ with $\phi$;

1. section 21 which establishes that $W G \to \bar W G$ is the PTCP for some universal twisting function $r(G)$.

1. lemma 21.9 states in the language of composites of twisting functions that every PTCP comes from composing a cocycle $Y \to \bar W G$ with the universal twisting function $r(G)$. In view of the relation to pullbacks in item 1, this yields the statement in the form we stated it above.

An explicit version of the statement that [[twisted Cartesian product]]s are nothing but pullbacks of a [[generalized universal bundle]] is on [page 148](http://ncatlab.org/timporter/files/menagerie10.pdf#page=148) of

* [[Tim Porter]], _[[Tim Porter:crossed menagerie|The Crossed Menagerie]].

On [page 239](http://ncatlab.org/timporter/files/menagerie10.pdf#page=239) there it is mentioned that

$$
  G \to W G \to \overline{W}G
$$

is a model for the [[loop space object]] [[fiber sequence]]

$$
  G \to * \to \mathbf{B}G
  \,.
$$

One place in the literature where the observation that $W G $ is the [[decalage]] of $\overline{W}G$ is mentioned fairly explicitly is page 85 of

* [[John Duskin]], _Simplicial methods and the interpretation of "triple" cohomology_, number  163 in Mem. Amer. Math. Soc., 3, Amer. Math. Soc. (1975)

## Related concepts

* [[simplicial topological group]]

* [[group object in an (∞,1)-category]]

* [[group]]

* [[2-group]], [[crossed module]], [[differential crossed module]]

* [[3-group]], [[2-crossed module]] / [[crossed square]], [[differential 2-crossed module]]

* [[n-group]]

* [[∞-group]], **simplicial group**, [[crossed complex]], [[hypercrossed complex]]

* [[model structure on simplicial groups]]

* [[Borel model structure]]




## References 

A standard reference for the case of _abelian_ simplicial groups is [chapter 5](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi) of

* {#GoerssJardine} [[Paul Goerss]], Jardine, _Simplicial homotopy theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))


Also chapter IV of

* {#MaySimplicialObjects} [[Peter May]], _Simplicial Objects in Algebraic Topology_ ([djvu](http://www.math.uchicago.edu/~may/BOOKS/Simp.djvu)).
  

and chapter 8 of

* {#Weibel} [[Charles Weibel]], _An introduction to homological algebra_ Cambridge (1994)
 

The algorithm for finding the horn fillers in a simplicial group is given in the proof of theorem 17.1, page 67 there. 

This proof that simplicial groups are Kan complexes is originally due to theorem 3.4 in 

* [[John Moore]],  _Semi-Simplicial Complexes And Postnikov Systems_, in _Symposium International De Topologia Algebraica_ , 1956 conference, book published in 1958

which appears in more detail as  theorem 3 on p. 18-04 of

* {#Moore54} [[John Moore]], _Homotopie des complexes monoideaux, I_ , Seminaire Henri Cartan, 1954-55. ([numdam](http://www.numdam.org/item?id=SHC_1954-1955__7_2_A8_0)) 
 
and is often attributed to

* {#Moore} [[John Moore]], _Algebraic homotopy theory_, lecture notes, Princeton University, 1955--1956
 
In fact, it seems that this is the origin of the very notion of [[Kan complex]].

A proof is also on p. 14 of

* {#JoyalTierney05} [[André Joyal]], [[Myles Tierney]] chapter I of _An introduction to simplicial homotopy theory_, 2005  ([web](http://hopf.math.purdue.edu/cgi-bin/generate?/Joyal-Tierney/JT-chap-01))


Section 1.3.3 of

* [[Tim Porter]], _[[Tim Porter:crossed menagerie|The Crossed Menagerie]]_ 

discusses simplicial groups in the context of [[nonabelian algebraic topology]].

Additional useful references include

* [[Rick Jardine]], Luo, _Higher order principal bundles_ ([web](http://www.math.uiuc.edu/K-theory/0681/))
 {#JardineLuo}

* [[Antonio Cegarra]], [[Josué Remedios]], _The relationship between the diagonal and the bar constructions on a bisimplicial set_ ([pdf](http://www.ugr.es/~acegarra/Paperspdfs/TRBDWC.pdf))
 {#CegarraRemedios}

category: simplicial object
[[!redirects simplicial groups]]

[[!redirects simplicial abelian group]]
[[!redirects simplicial abelian groups]]