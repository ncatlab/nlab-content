

{:bluebox: .un_remark style="border:solid #000000;background: #E6DF13;border-width:2px 1px;padding:0 1em;margin:0 1em;"}

***



$\,$

+-- {: .standout}

<div style="float:left;margin:0 10px 10px 0;"> <img width="200" src="http://ncatlab.org/nlab/files/BonnLogo.png"> </div> 

[V4D2 -- Algebraic Topology II](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=109556&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Stable Homotopy Theory**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

[Lecture](#Introduction) and [Seminar](#ComplexOrientedCohomology)

=--

**Abstract** _We give an introduction to the [[stable homotopy category]] and to its key computational tool, the [[Adams spectral sequence]]. In the accompanying [seminar](#ComplexOrientedCohomology) we work through related classical results in [[cobordism theory]] and [[complex oriented cohomology]] such as to converge in the end to a glimpse of the modern picture of [[chromatic homotopy theory]]._



$\,$

***

This page contains topics, links, literature. 

Eventually lecture notes.

***


#Contents#
* table of contents
{:toc}


<div style="float:right;margin:0 10px 10px 0;"> <img src="https://ncatlab.org/nlab/files/HopfFibration.jpg" width="200" />  </div>

***

> My initial inclination was to call this book [[The Music of the Spheres]], but I was dissuaded from doing so by my diligent publisher, who is ever mindful of the sensibilities of librarians. ([Ravenel 86, preface](#Ravenel86))


## Introduction
 {#Introduction}

We are concerned with the theory of _[[spectra]]_ in the sense of [[algebraic topology]]: the proper generalization of [[abelian groups]] to [[homotopy theory]]. 

### 1) Stable homotopy theory
 {#StableHomotopyTheory}

A [[group]] in homotopy theory is equivalently a [[loop space]] under concatenation of loops ("[[∞-group]]"). A double loop space is a group with some commutativity structure ("[[Eckmann-Hilton argument]]"), a triple loop space has more commutativity structure, and so forth. A _spectrum_ is where this progression of [[looping and delooping]] _stabilizes_ (an "$\infty$-abelian group"). Therefore one speaks of _[[stable homotopy theory]]_:

$$
  Spaces
  \;\;
  \underoverset{(linearization)}{stabilization}{\mapsto}
  \;\;
  Spectra
  \,.
$$

Most of [[linear algebra]] and [[algebraic geometry]] passes along as [[abelian groups]] are generalized to [[spectra]] and turns into something remarkably rich, called _[[brave new algebra]]_, _[[higher algebra]]_ and _[[E-∞ geometry|spectral geometry]]_. In particular the analog of the theory of ([[commutative ring|commutative]]) [[rings]] and their [[modules]] exist, given by ([[commutative ring spectrum|commutative]]) [[ring spectra]] ([[E-∞ rings]], [[A-∞ rings]]) and [[module spectra]] ([[∞-modules]]). 

### 2) Adams spectral sequences
 {#ANSS}

Since spectra are considerably richer than abelian groups, stable homotopy is much concerned with "[[fracture theorem|fracturing]]" stable homotopy types into more tractable components:

To that end, notice that from the point of view of [[arithmetic geometry]], an [[abelian group]] $A$ is equivalently a [[quasicoherent sheaf]] over [[Spec(Z)]]. 

$$
  AbelianGroups \simeq QCoh(Spec(\mathbb{Z}))
  \,.
$$

This point of view generalizes to homotopy theory and turns out to be very fruitful there. The analog of the [[integers]] $\mathbb{Z}$ is the [[sphere spectrum]] $\mathbb{S}$, and this is naturally the [[initial object in an (infinity,1)-category|initial]] [[commutative ring spectrum]] ("[[E-∞ ring]]"), just as $\mathbb{Z}$ is the [[initial object|initial]] [[commutative ring]]. The [[formal dual]]  [[Spec(S)]] of $\mathbb{S}$ is hence the [[terminal object in an (infinity,1)-category|terminal]] [[space]] in [[E-∞ arithmetic geometry]] ("[[spectral geometry]]") and [[spectra]] are equivalently the [[quasicoherent ∞-stacks]] over $Spec(\mathbb{S})$

$$
  Spectra \simeq QCoh(Spec(\mathbb{S}))
  \,.
$$

Therefore the study of spectra "[[fracture theorem|fractures]]" into the various [[localizations]] and [[formal completions]] of $Spec(S)$. Since this is like the white light of $Spec(S)$ decomposing into various wavelengths, one speaks of _[[chromatic homotopy theory]]_. 

In particular, an  [[E-∞ ring]] $E$ is [[formal dual|dually]] a morphism of $E_\infty$-algebraic spaces $Spec(E) \longrightarrow Spec(\mathbb{S})$ and under good conditions the [[1-image]] of this map is the formal dual of the [[Bousfield localization of spectra|localization]] $L_E \mathbb{S}$ at $E$:

$$
  Spec(E) \stackrel{epi_1}{\longrightarrow} Spec(L_E \mathbb{S}) \stackrel{mono_1}{\longrightarrow} Spec(\mathbb{S})
 \,.
$$

This means that $Spec(E) \longrightarrow Spec(L_E \mathbb{S})$ is a [[cover]] and that hence $E$-local spectra are equivalently [[quasicoherent ∞-stacks]] on $Spec(E)$ equipped with [[descent data]]: [[formal dual|dually]] they are [[∞-modules]] over $E$ equipped with [[comodule]] structure over the [[Hopf algebroid]] ([[Sweedler coring]]) $E \otimes_{\mathbb{S}} E$.

The computation of [[homotopy groups]] of spectra that make use of their decomposition this way into $E$-[[∞-modules]] equipped with [[descent]] data is the _$E$-[[Adams spectral sequence]]_, a central tool of the theory.

### S) Complex oriented cohomology

For this reason special importance is carried by those [[E-∞ rings]] such that $Spec(E) \to Spec(\mathbb{S})$ is already a [[covering]], for these the $E$-[[∞-modules]] equipped with descent data give an equivalent, but in general more tractable, incarnation of the stable homotopy theory of spectra.

Curiously, this way a good bit of [[differential topology]] -- [[cobordism theory]] -- arises within stable homotopy theory: the archetypical $Spec(E)$ which covers $Spec(\mathbb{S})$ is $E = $ [[MU]], the [[Thom spectrum]] representing [[complex cobordism cohomology]].

An [[commutative ring spectrum]] $E$ over $MU$, hence a $Spec(E)\to Spec(MU)$ is now a [[multiplicative cohomology theory|multiplicative]] "[[complex oriented cohomology theory]]". 


## **Part 1) Stable homotopy theory**

We set up [[stable homotopy theory]].
 
**Literature.** For a decent quick idea see ([Malkiewich 14](#Malkiewich14)).
The original is still good: ([Adams 74, part III sections 2-7](#Adams74)),
except where it considers the [[stable homotopy category]] in its incarnation
as the [[Adams category]], better to consider the [[homotopy category]] of the
[[Bousfield-Friedlander model structure]]. We go through this [below](#Spectra).

### The classical homotopy category

We are interested in the [[stable homotopy category]] of [[spectra]], to which we turn [below](#Spectra). But since its existence is an adjunct of the plain [[homotopy category]] [[Ho(Top)]] of [[homotopy types]] of [[topological spaces]]/[[simplicial sets]], we here review that first.

+-- {: .num_defn #TopologicalSimplex}
###### Definition

For $n \in \mathbb{N}$, the **[topological n-simplex](simplex#TopologicalSimplex)** is,  up to [[nLab:homeomorphism]], the [[nLab:topological space]] whose underlying set is the subset

$$
  \Delta^n \coloneqq 
  \{
    \vec x \in \mathbb{R}^{n+1}
    |
    \sum_{i = 0 }^n x_i = 1 \; and \;
    \forall i . x_i \geq 0 
  \}
  \subset \mathbb{R}^{n+1}
$$

of the [[nLab:Cartesian space]] $\mathbb{R}^{n+1}$, and whose topology is the  [[nLab:subspace topology]] induces from the canonical topology in $\mathbb{R}^{n+1}$.

=--

+-- {: .num_example}
###### Example

For $n = 0$ this is the [[nLab:point]], $\Delta^0 = *$.

For $n = 1$ this is the standard [[nLab:interval object]] $\Delta^1 = [0,1]$.

For $n = 2$ this is the filled triangle.

For $n = 3$ this is the filled tetrahedron.

=--



+-- {: .num_defn #FaceInclusionInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$, $\n \geq 1$ and $0 \leq k \leq n$, the 
**$k$th $(n-1)$-face (inclusion)**  of the topological $n$-simplex, def. \ref{TopologicalSimplex}, is the subspace inclusion

$$
  \delta_k : \Delta^{n-1} \hookrightarrow \Delta^n
$$

induced under the coordinate presentation of def. \ref{TopologicalSimplex},
by the inclusion 

$$
  \mathbb{R}^n \hookrightarrow \mathbb{R}^{n+1}
$$

which "omits" the $k$th canonical coordinate:

$$
  (x_0, \cdots , x_{n-1}) \mapsto (x_0, \cdots, x_{k-1} , 0 , x_{k}, \cdots, x_n)
  \,.
$$

=--

+-- {: .num_example}
###### Example

The inclusion 

$$
  \delta_0 : \Delta^0 \to \Delta^1
$$ 

is the inclusion

$$
  \{1\} \hookrightarrow [0,1]
$$ 

of the "right" end of the standard interval. The other inclusion 

$$
  \delta_1 : \Delta^0 \to \Delta^1
$$ 

is that of the "left" end $\{0\} \hookrightarrow [0,1]$.

=--

+-- {: .num_defn #DegeneracyProjectionsInBarycentricCoords}
###### Definition

For $n \in \mathbb{N}$ and $0 \leq k \lt n$ the **$k$th degenerate $(n)$-simplex (projection)** is the surjective map

$$
  \sigma_k : \Delta^{n} \to \Delta^{n-1}
$$

induced under the barycentric coordinates of def. \ref{TopologicalSimplex} under the surjection

$$
  \mathbb{R}^{n+1} \to \mathbb{R}^n
$$

which sends

$$
  (x_0, \cdots, x_n) \mapsto (x_0, \cdots, x_{k} + x_{k+1}, \cdots, x_n)
  \,.
$$

=--

+-- {: .num_defn #SingularSimplex}
###### Definition

For $X \in $ [[Top]]  and $n \in \mathbb{N}$, a **singular $n$-simplex** in $X$ is a [[continuous map]]

$$
  \sigma : \Delta^n \to X
$$

from the topological $n$-simplex, def. \ref{TopologicalSimplex}, to $X$.

Write 

$$
  (Sing X)_n \coloneqq Hom_{Top}(\Delta^n , X)
$$ 

for the set of singular $n$-simplices of $X$.

=--

The sets $(Sing X)_\bullet$ here are closely related by an interlocking system of maps that make them form what is called a _[[simplicial set]]_, and as such the collection of these sets of singular simplices is called the _[[singular simplicial complex]]_ of $X$. We discuss the definition of simplicial sets now and then come back to this below in def. \ref{SingularSimplicialComplex}.

Since the topological $n$-simplices $\Delta^n$ from def. \ref{TopologicalSimplex} sit inside each other by the face inclusions of def. \ref{FaceInclusionInBarycentricCoords}

$$
  \delta_k : \Delta^{n-1} \to \Delta^{n}
$$

and project onto each other by the degeneracy maps, def. \ref{DegeneracyProjectionsInBarycentricCoords}

$$
  \sigma_k : \Delta^{n+1} \to \Delta^n
$$

we dually have functions

$$
  d_k \coloneqq Hom_{Top}(\delta_k, X) : (Sing X)_n \to (Sing X)_{n-1}
$$

that send each singular $n$-simplex to its $k$-face and functions

$$
  s_k \coloneqq Hom_{Top}(\sigma_k,X) : (Sing X)_{n} \to (Sing X)_{n+1}
$$

that regard an $n$-simplex as beign a degenerate ("thin") $(n+1)$-simplex.
All these sets of simplices and face and degeneracy maps between them form the following structure. 

+-- {: .num_defn #SimplicialSet}
###### Definition

A **[[nLab:simplicial set]]** $S \in sSet$ is 

* for each $n \in \mathbb{N}$ a [[nLab:set]] $S_n \in Set$ -- the **set of $n$-[[simplices]]**;

* for each [[injective map]] $\delta_i : \overline{n-1} \to \overline{n}$ of [[nLab:totally ordered sets]] $\bar n \coloneqq \{ 0 \lt 1 \lt \cdots \lt n \}$

  a [[function]] $d_i : S_{n} \to S_{n-1}$ -- the $i$th **face map** on $n$-simplices;

* for each [[surjective map]] $\sigma_i : \overline{n+1} \to \bar n$ of [[totally ordered sets]]

  a [[function]] $\sigma_i : S_{n} \to S_{n+1}$ -- the $i$th **degeneracy map** on $n$-simplices;

such that these functions satisfy the _[[nLab:simplicial identities]]_.

=--

+-- {: .num_defn #SimplicialIdentities}
###### Definition

The **simplicial identities** satisfied by face and degeneracy maps as above are (whenever these maps are composable as indicated):

1. $ d_i \circ d_j  = d_{j-1} \circ d_i$ if $i \lt j$,

1. $s_i \circ s_j  = s_j \circ s_{i-1}$ if $i \gt j$.

1. $d_i \circ s_j =  \left\{ \array{ s_{j-1} \circ d_i &  if \;  i \lt j \\ id & if  \;  i = j \; or \; i = j+1 \\ s_j \circ d_{i-1} &  if i \gt j+1 } \right. $

=--

It is straightforward to check by explicit inspection that the evident injection and restriction maps between the sets of [[singular simplices]] make $(Sing X)_\bullet$ into a simplicial set. However for working with this, it is good to streamline a little:

+-- {: .num_defn}
###### Definition

The **[[simplex category]]** $\Delta$ is the [[full subcategory]] of [[Cat]] on the free categories of the form

$$
  \begin{aligned}
    [0] & \coloneqq \{0\}
    \\
    [1] & \coloneqq \{0 \to 1\}
    \\
   [2] & \coloneqq \{0 \to 1 \to 2\}
   \\
   \vdots
   \end{aligned}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

This is called the "simplex category" because we are to think of the object $[n]$ as being the "[[spine]]" of the $n$-[[nLab:simplex]]. For instance for $n = 2$ we think of $0 \to 1 \to 2$ as the "spine" of the triangle. This becomes clear if we don't just draw the morphisms that _generate_ the category $[n]$, but draw also all their composites. For instance for $n = 2$ we have_

$$
  [2]  
  = 
  \left\{
  \array{
     && 1
     \\
     & \nearrow && \searrow
     \\
    0 &&\to&& 2
  }
  \right\}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

A [[functor]] 

$$
  S : \Delta^{op} \to Set
$$

from the [[nLab:opposite category]] of the [[nLab:simplex category]] to the category [[nLab:Set]] of sets is canonically identified with a [[nLab:simplicial set]], def. \ref{SimplicialSet}.

=--

+-- {: .proof}
###### Proof

One checks by inspection that the simplicial identities 
characterize precisely the behaviour of the morphisms in
$\Delta^{op}([n],[n+1])$ and $\Delta^{op}([n],[n-1])$.

=--

This makes the following evident:

+-- {: .num_example #StandardCosimplicialTopologicalSpace}
###### Example

The [[topological simplices]] from def. \ref{TopologicalSimplex} arrange into a _[[cosimplicial object]] in [[Top]]_, namely a [[functor]]

$$
  \Delta^\bullet : \Delta \to Top
  \,.
$$

=--

With this now the structure of a simplicial set on $(Sing X)_\bullet$, def. \ref{SingularSimplex}, is manifest: it is just the _[[nerve]]_ of $X$ with respect to $\Delta^\bullet$, namely:

+-- {: .num_defn #SingularSimplicialComplex}
###### Definition

For $X$ a [[topological space]] its **[[singular simplicial complex|simplicial set of singular simplicies]]**  (often called the **[[singular simplicial complex]]**)

$$
  (Sing X)_\bullet : \Delta^{op} \to Set
$$

is given by composition of the functor from example \ref{StandardCosimplicialTopologicalSpace} with the [[nLab:hom functor]] of [[nLab:Top]]:

$$
  (Sing X) : [n] \mapsto Hom_{Top}( \Delta^n , X )
  \,.
$$

=--

+-- {: .num_remark}
###### Remark 

It turns out -- this is the content of the _[[nLab:homotopy hypothesis]]-theorem_ ([Quillen 67](model+structure+on+simplicial+sets#Quillen67)) -- that [[homotopy type]] of the topological space $X$ is entirely captured by its singular simplicial complex $Sing X$. Moreover, the [[geometric realization]] of $Sing X$ is a model for the same [[homotopy type]] as that of $X$, but with the special property that it is canonically a [[cell complex]] -- a [[CW-complex]]. Better yet, $Sing X$ is itself already good cell complex, namely a [[Kan complex]].

=--


+-- {: .num_defn #Horn}
###### Definition

For each $i$, $0 \leq i \leq n$, the **$(n,i)$-horn** 
is the subsimplicial set 

$$
  \Lambda^i[n]
  \hookrightarrow
  \Delta[n] 
$$

of the simplicial $n$-[[simplex]], which is the [[union]] of all faces _except_ the  $i^{th}$ one.

This is called an **outer horn** if $k = 0$ or $k = n$.  Otherwise it is an **inner horn**.


=--

+-- {: .num_remark }
###### Remark


Since [[sSet]]  is a [[presheaf category]], [[unions]] of [[subobjects]] make sense and they are calculated objectwise, thus in this case dimensionwise.  This way it becomes clear what the structure of a horn as a functor $\Lambda^k[n]: \Delta^{op} \to Set$ must therefore be: it takes $[m]$ to the collection of ordinal maps $f: [m] \to [n]$ which do not have the element $k$ in the image.

=--


+-- {: .num_defn #KanComplexes}
###### Definition

A _[[Kan complex]]_ is a [[simplicial set]] $S$ that satisfies the _Kan condition_, 

* which says that all [[horns]] of the simplicial set have _fillers_/extend to [[simplices]];

* which means equivalently that the unique homomorphism $S \to pt$ from $S$ to the [[point]] (the [[terminal object|terminal]] [[simplicial set]]) is a [[Kan fibration]];

* which means equivalently that for all [[diagrams]] of the form

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow && 
    \\
    \Delta[n] 
  }
  $$

  there exists a diagonal morphism

  $$
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& \downarrow
    \\
    \Delta[n] &\to& pt
  }
  \;\;\;
  \leftrightarrow
  \;\;\;
  \array{
    \Lambda^i[n] &\to& S
    \\
    \downarrow &\nearrow& 
    \\
    \Delta[n] 
  }
  $$

  completing this to a [[commuting diagram]];

* which in turn means equivalently that the map from $n$-simplices to $(n,i)$-horns is an [[epimorphism]]
$$
  [\Delta[n], S]\, \twoheadrightarrow \,[\Lambda^i[n],S]
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

For $X$ a [[topological space]], its [[singular simplicial complex]]
$Sing(X)$, def. \ref{SingularSimplicialComplex}, is a Kan complex, def. \ref{KanComplexes}.

=--

+-- {: .proof}
###### Proof

The inclusions ${{\Lambda^n}_{Top}}_k \hookrightarrow \Delta^n_{Top}$ of topological horns into topological simplices are  [[retracts]], in that there are [[continuous maps]] $\Delta^n_{Top} \to {{\Lambda^n}_{Top}}_k$ given by "squashing" a topological $n$-simplex onto parts of its boundary, such that

$$
  ({{\Lambda^n}_{Top}}_k \to \Delta^n_{Top} \to
  {{\Lambda^n}_{Top}}_k)
  =
  Id
  \,.
$$

Therefore the map
$[\Delta^n, \Pi(X)] \to [\Lambda^n_k,\Pi(X)]$ is an epimorphism, since it is equal to  to $Top(\Delta^n, X) \to Top(\Lambda^n_k, X)$ which has a right inverse $Top(\Lambda^n_k, X) \to Top(\Delta^n, X)$.

=--

+-- {: .num_defn #LeftHomotopyOfSimplicialSets}
###### Definition

For $X$ a [[simplicial set]], def. \ref{SimplicialSet}, its _simplicial [[cylinder object]]_ is the [[Cartesian product]] $X\times \Delta[1]$ (formedin the [[category]] [[sSet]]).

A _[[left homotopy]]_ 

$$
  \eta \;\colon\; f \Rightarrow g
$$

between two morphisms

$$
  f,g\;\colon\; X \longrightarrow Y
$$

of [[simplicial sets]] is a morphism 

$$
  \eta \;\colon\; X \times \Delta[1] \longrightarrow Y
$$

such that the following [[commuting diagram|diagram commutes]]

$$
  \array{
     X 
     \\
     {}^{\mathllap{(id_X,d_1)}}\downarrow & \searrow^{\mathllap{f}}
     \\
     X \times \Delta^1 &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id_x, d_0)}}\uparrow & \nearrow_{\mathllap{g}}
     \\
     X
  }
  \,.
$$

=--

+-- {: .num_prop #LeftHomotopyIsEquivalence}
###### Proposition

For $Y$ a [[Kan complex]], def. \ref{KanComplexes}, and $X$ any [[simplicial set]], then left homotopy, def. \ref{LeftHomotopyOfSimplicialSets},
regarded as a [[relation]]

$$
  (f\sim g) \Leftrightarrow (f \stackrel{\exists}{\Righrarrow} g)
$$

on the [[hom set]] $Hom_{sSet}(X,Y)$, is an [[equivalence relation]].

=--

With this we finally arrive at a presentation of the classical homotopy category. For our purposes the following may be taken to be a definition, otherwise it is part of the theorem of ([Quillen 67](model+structure+on+simplicial+sets#Quillen67)), known sometimes as the _[homotopy hypothesis for Kan complexes](homotopy hypothesis#ForKanComplexes)_.

+-- {: .num_defn}
###### Definition

The classical [[homotopy category]] [[Ho(Top)]] $\simeq$ [[Ho(sSet)]] $\simeq$ [[Ho(∞Grpd)]]
is [[equivalence of categories|equivalently]] the category whose

* [[objects]] are [[Kan complexes]];

* [[morphisms]], are left-[[homotopy classes]], def. \ref{LeftHomotopyIsEquivalence}, of morphisms of simplicial sets.

=--





### The stable homotopy category
 {#Spectra}

We construct the [[stable homotopy category]].

The stable homotopy category is to be the [[stabilization]] of the classical [[homotopy category]] [[Ho(Top)]] $\simeq$ [[Ho(sSet)]] under the operation of forming [[loop space objects]] $\Omega$ and [[reduced suspensions]] $\Sigma$: via forming [[suspension spectra]] $\Sigma^\infty$ every [[pointed object]] in the classical [[homotopy category]] maps to the stable homotopy category, and under this map the [[loop space]]- and [[reduced suspension]]-[[functors]] become inverse [[equivalence of categories|equivalences]] on the stable homotopy category.

$$
  \array{
     Ho(Top)^{\ast/} 
      &
      \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{} 
      &
     Ho(Top)^{\ast/}
     \\
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     &&
     {}^{\mathllap{\Sigma^\infty}}\downarrow \dashv \uparrow^{\mathrlap{\Omega^\infty}}
     \\
     Ho(Spectra) 
     &
     \underoverset{\underset{\Omega}{\longrightarrow}}{\overset{\Sigma}{\longleftarrow}}{\simeq}
     &
     Ho(Spectra)
  }
  \,.
$$


In contrast to the classical [[homotopy category]], the stable homotopy category is a [[triangulated category]] (a shadow of the fact that the [[(∞,1)-category of spectra]] is a [[stable (∞,1)-category]]). As such it may be thought of as a refinement of the [[derived category]] [[category of chain complexes|of chain complexes]] (of [[abelian groups]]): every [[chain complex]] gives rise to a [[spectrum]] and every [[chain map]] to a map between these spectra (the [[stable Dold-Kan correspondence]]), but there are many more spectra and maps between them than arise from chain complexes and chain maps.


* [[pointed object]], [[pointed topological space]]

  [[smash product]]

  [[suspension]], [[loop space object]]

* [[spectrum]]

  [[free infinite loop space]]

  [[Omega-spectrum]]

* [[suspension spectrum]]

* [[stable homotopy category]]

* [[triangulated category]]

  [[homotopy fiber sequence]], [[mapping cone]]

### Examples
 {#Examples}

...[[S]], [[HA]], [[MO]], [[MU]], [[KO]], [[KU]]...


### Ring spectra
 {#RingSpectra}

* [[smash product of spectra]]

* [[symmetric monoidal category]]

* [[monoid object]], [[commutative monoid object]], [[module object]]

* [[ring spectrum]]

* [[module spectrum]]




### Localization
 {#Localization}

[[Bousfield localization of spectra]] and [[fracture theorem]]

+-- {: .num_defn #AcyclicAndLocal}
###### Definition

Let $E \in Spec$ be a [[spectrum]]. 

Say that another spectrum $X \in Spec$ is an **$E$-acyclic spectrum** if the [[smash product of spectra|smash product]] is [[zero object|zero]], $E \wedge X \simeq 0$.

Say that $X$ is an **$E$-local spectrum** if every [[morphism]]
$Y \longrightarrow X$ out of an $E$-acyclic spectrum $Y$ is homotopic to the [[zero morphism]]. 

Say that a morphism $f \colon X \to Y$ is an **$E$-equivalence** if it becomes an [[equivalence]] after [[smash product]] with $E$.

=--

(e.g. [Lurie, Lecture 20, example 4](#Lurie10))

+-- {: .num_prop #LocalizationCofiber}
###### Proposition

For $E$ a [[spectrum]], every spectrum sits in an essentially unique [[homotopy cofiber sequence]]

$$
  G_E(X) \to X \to L_E(X)
  \,,
$$

where $G_E(X)$ is $E$-acyclic, and $L_E(X)$ is $E$-local, def. \ref{AcyclicAndLocal}.

Here $X \to L_E (X)$ is characterized by two properties

1. $L_E(X)$ is $E$-local;

1. $X \to L_E(X)$ is an $E$-equivalence

according to def. \ref{AcyclicAndLocal}.

=--

(e.g. [Lurie, Lecture 20, example 4](#Lurie10))

+-- {: .num_remark #Acyclification}
###### Remark

Hence where $L_E$ is traditionally called "$E$-localization", $G_E$ might be called "$E$-acyclification", though that terminology is not used very commonly. 

=--

+-- {: .num_defn}
###### Definition

Given $E \in Spec$, 
the [[natural transformation|natural morphisms]] $X \longrightarrow L_E X$
in prop. \ref{LocalizationCofiber} exhibit the [[localization of an (infinity,1)-category]] called **Bousfield localization** at $E$.

=--


+-- {: .num_remark #CanonicalMapFromELocalizationToTotalization}
###### Remark

There is a canonical map

$$
  L_E X \stackrel{}{\longrightarrow} \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
$$

from the $E$-[[Bousfield localization of spectra]] of $X$ into the [[totalization]].


=--

We consider now conditions for this morphism to be an [[equivalence]].

+-- {: .num_defn #CoreOfARing}
###### Definition

For $R$ a [[ring]], its _core_ $c R$ is the [[equalizer]] in

$$
  c R 
    \longrightarrow 
  R 
    \stackrel{\longrightarrow}{\longrightarrow}
  R \otimes R
  \,.
$$

=--

+-- {: .num_prop #SufficientConditionsForTotalizationToBeELocalization}
###### Proposition

Let $E$ be a [[connective spectrum|connective]] [[E-∞ ring]] such that the core of $\pi_0(E)$, def. \ref{CoreOfARing}, is either of

* the [[localization of a ring|localization]] of the [[integers]] at a set $J$ of [[primes]], $c \pi_0(E) \simeq \mathbb{Z}[J^{-1}]$;

* $\mathbb{Z}_n$ for $n \geq 2$.

Then the map in remark \ref{CanonicalMapFromELocalizationToTotalization} is an equivalence

$$
  L_E X \stackrel{\simeq}{\longrightarrow} 
  \underset{\leftarrow}{\lim}_n (E^{\wedge^{n+1}_S}\wedge_S X)
  \,.
$$

=--

([Bousfield 79](#Bousfield79)). see also for instance ([Bauer 11, p. 2](#Bauer11))

For more discussion of [[E-infinity geometry|E-infinity]] (derived) [[formal completions]] via totalizations of [[Amitsur complexes]], see ([Carlsson 07](completion+of+a+module#Carlsson07)).



+-- {: .num_prop #SullivanArithmeticFracture}
###### Proposition
**(Sullivan arithmetic square)**

For every [[spectrum]] $X$ the canonical square

$$
  \array{
    && L_{\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{\mathbb{Q}}
    \left(
      \prod_p L_p X
    \right)
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && \prod_p L_p X
  }
$$

is a [[homotopy pushout]] (hence also a [[homotopy pullback]]).

=--

Original statements of this include ([Bousfield 79](#Bousfield79), [Sullivan 05, prop. 3.20](#Sullivan05)). Review includes ([van Koughnett 13, prop. 4.5](#VanKoughnett13), [Bauer 11, lemma 2.1](#Bauer11)). 


So the [[nLab:arithmetic fracture square]] from [[nLab:Weil uniformization theorem|Weil uniformization]] over [[nLab:Spec(S)]] synthesizes spectra from their formal completion and torsion approximation:


$$
  \array{
    &&  {{localization} \atop {away\;from\;p}} && \stackrel{}{\longrightarrow} && {{p-adic} \atop {residual}}
    \\
    & \nearrow & & \searrow & & \nearrow && \searrow
    \\
    { {formal\;completion} \atop {away\; from \;p} }  && &&  &&  && {{{p-torsion} \atop {approximation}} \atop {{of\;p-adic} \atop {residual}}}
    \\
    & \searrow &  & \nearrow & & \searrow && \nearrow
    \\
    && { {formal\;completion} \atop {at\;p} }
    \; && \longrightarrow && {{p-torsion} \atop {approximation}}
  }
  \,,
$$

(and there is further fracturing of the $p$-local part by [[nLab:chromatic homotopy theory]]).

+-- {: .num_prop #ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
###### Proposition

The product of all [[p-completions]] is equivalently the [[Bousfield localization of spectra]] at the [[wedge sum]] $\vee_p S \mathbb{F}_p$ of all [[Moore spectra]]


$$
  \prod_p L_p X
  \simeq
   L_{\vee_p S \mathbb{F}_p} X
  \,.
$$

Moreover there is a  [[Bousfield equivalence]] 

$$
  S (\mathbb{Q}/\mathbb{Z}) \simeq_{Bousf} \vee_p S \mathbb{F}_p
  \,,
$$ 

and therefore also an equivalence

$$
  \prod_p L_p X
  \simeq
   L_{S (\mathbb{Q}/\mathbb{Z})} X
  \,.
$$


=--

The first statement originates around ([Bousfield 79, prop. 2.6](Bousfield+localization+of+spectra#Bousfield79)), review includes ([van Koughnett 13, prop. 4.4](Bousfield+localization+of+spectra#VanKoughnett13), [Bauer 11, below prop. 2.2](#Bauer11)); the second is highlighted in ([Strickland 12, MO comment](http://mathoverflow.net/a/91057/381)).


By prop. \ref{ReformulationOfProdOverPComletionByLocalizationAtCoproduct}
the arithmetic fracture square of prop. \ref{SullivanArithmeticFracture} is equivalently of the form

$$
  \array{

    && L_{H\mathbb{Q}}X
    \\
    & \swarrow && \nwarrow
    \\
    L_{H\mathbb{Q}}
    L_{S \mathbb{Q}/\mathbb{Z}} X
    &&  &&
    X
    \\
     & \nwarrow && \swarrow
    \\
    && L_{S \mathbb{Q}/\mathbb{Z}} X
  }
  \,.
$$

In this form the statement holds much more generally:

+-- {: .num_prop #GeneralFractureSquare}
###### Proposition

Let $E, F, X$ be [[spectra]] such that the $F$-[[Bousfield localization of spectra|localization]] of $X$ is $E$-acyclic, i.e.  $E_\bullet(L_F X) \simeq 0$, then the canonical square [[diagram]]


$$
  \array{
    && L_F X
    \\
    & \swarrow && \nwarrow
    \\
    L_F
    L_E X
    &&  &&
    L_{E\vee F} X
    \\
     & \nwarrow && \swarrow
    \\
    && L_E X
  }
$$

is a [[homotopy pullback]] (and hence by stability also a [[homotopy pushout]]).


=--

e.g. ([Bauer 11, prop. 2.2](#Bauer11))


## **Interlude: Spectral sequences**
 {#SpectralSequences}

In the end, what one wants to compute in stable homotopy 
theory are [[stable homotopy groups]] of [[spectra]] that are built
from other spaces and spectra in some way. Notably one wants to 
know the homotopy groups of [[mapping spectra]] $[X,E]$ ([[generalized cohomology|generalized]] [[cohomology groups]])
and of [[smash products of spectra]] $E \wedge X$ ([[generalized homology|generalized]] [[homology groups]]).

Since spectra in general are very rich structures 
(and that's why we are interested in them) the only conceivable way to 
carry out such computations is by doing them along a decomposition of the given spectrum into a "sequence of stages" of sorts. The concept of _[[spectral sequence]]_ is precisely what formalizes this idea.

(Here the re-occurence of the root "spectr-" it is a historical coincidence, but a lucky one.)

There are roughly two main ways to decompose a spectrum $S$ into a sequence of stages:

1. By a [[filtered object in an (∞,1)-category|(co-)filtration]] 

   $$
     0 \to S_0 \to S_1 \to S_2 \to S_3 \to \cdots \to S
   $$

   this leads to the concept of "[[spectral sequence of a cofiltered spectrum]]" with the special and more famous case of "[[spectral sequence of a filtered complex]]".

1. By a tower of [[homotopy fibers]]

   $$
     \array{
       \vdots
       \\
       {}^{\mathllap{hofib(f_2)}}\downarrow
       \\
       S_2 &\stackrel{}{\longrightarrow}&
       \\
       {}^{\mathllap{hofib(f_1)}}\downarrow
       \\
       S_1 &\stackrel{f_1}{\longrightarrow}&
       \\
       {}^{\mathllap{hofib(f_0)}}\downarrow
       \\
       S &\stackrel{f_0}{\longrightarrow}&
     }
   $$

   Here the [[long exact sequence of homotopy groups]] of each of the  [[homotopy fiber sequences]] combine to what is called an [[exact couple]], and these give the coresponding "[[spectral sequence of an exact couple]]".



### Spectral sequence of a filtered complex


We begin with recalling basics of _[[relative homology]]_ and then seamlessly derive the notion of _[[spectral sequences]]_ from that.


Let $X$ be a [[nLab:topological space]] and $A \hookrightarrow X$ a [[nLab:topological subspace]]. Write $C_\bullet(X)$ for the [[nLab:chain complex]] of [[nLab:singular homology]] on $X$, def. \ref{ComplexOfChainsOnASimplicialSet} and $C_\bullet(A) \hookrightarrow C_\bullet(X)$ for the [[nLab:chain map]] induced by the subspace inclusion according to def. \ref{PushforwardOfChains}.

+-- {: .num_defn #RelativeSingularHomology}
###### Definition

The (degreewise) [[nLab:cokernel]] of this inclusion, hence the [[nLab:quotient]] $C_\bullet(X)/C_\bullet(A)$ of $C_\bullet(X)$ by the [[nLab:image]] of $C_\bullet(A)$ under the inclusion, is the **chain complex of $A$-relative singular chains**. 

* A [[nLab:boundary]] in this quotient is called an **$A$-relative singular boundary**, 

* a [[nLab:cycle]] is called an **$A$-relative singular cycle**.

* The [[nLab:chain homology]] of the quotient is the **$A$-relative singular homology of $X$**

  $$
    H_n(X , A)\coloneqq H_n(C_\bullet(X)/C_\bullet(A))
    \,.
  $$

=--

+-- {: .num_remark}
###### Remark

This means that a singular $(n+1)$-chain $c \in C_{n+1}(X)$ is an $A$-relative cycle precisely if its [[nLab:boundary]] $\partial c \in C_{n}(X)$ is, while not necessarily 0, contained in the $n$-chains of $A$: $\partial c \in C_n(A) \hookrightarrow C_n(X)$. So the boundary vanishes possibly only "up to contributions coming from $A$".

=--

We record two evident but important classes of [[nLab:long exact sequences]] that relative homology groups sit in:

+-- {: .num_prop #RelativeHomologyLongExactSequence}
###### Proposition

Let $A \stackrel{i}{\hookrightarrow} X$ be a [[nLab:topological subspace]] inclusion. The corresponding 
relative singular homology, def. \ref{RelativeSingularHomology}, sits in a [[nLab:long exact sequence]] of the form

$$
  \cdots
  \to 
  H_n(A)
   \stackrel{H_n(i)}{\to}
  H_n(X)
  \to 
  H_n(X, A)
   \stackrel{\delta_{n-1}}{\to}
  H_{n-1}(A)
   \stackrel{H_{n-1}(i)}{\to}
  H_{n-1}(X)
  \to 
  H_{n-1}(X, A)
  \to 
  \cdots
  \,.
$$

The [[nLab:connecting homomorphism]] $\delta_{n} \colon H_{n+1}(X, A) \to H_n(A)$ sends an element $[c] \in H_{n+1}(X, A)$ represented by an $A$-relative cycle $c \in C_{n+1}(X)$, to the class represented by the [[nLab:boundary]] $\partial^X c \in C_n(A) \hookrightarrow C_n(X)$.

=--

+-- {: .proof}
###### Proof

This is the _[[nLab:homology long exact sequence]]_, prop. \ref{HomologyLongExactSequence}, induced by the defining [[nLab:short exact sequence]] $0 \to C_\bullet(A) \stackrel{i}{\hookrightarrow} C_\bullet(X) \to coker(i)  \simeq C_\bullet(X)/C_\bullet(A)  \to 0$ of chain complexes.

=--

+-- {: .num_prop #RelativeTripleHomologyLongExactSequence}
###### Proposition

Let $B \hookrightarrow A \hookrightarrow X$ be a sequence of two [[nLab:topological subspace]] inclusions. Then there is a [[nLab:long exact sequence]] of [[nLab:relative singular homology]] groups of the form

$$
  \cdots \to H_n(A , B) \to H_n(X , B) \to H_n(X , A ) \to H_{n-1}(A , B) \to \cdots
  \,.
$$

=--

+-- {: .proof}
###### Proof

Observe that we have a [[nLab:short exact sequence]] of chain complexes, def. \ref{ShortExactSequenceOfChainComplexes}

$$
  0 \to C_\bullet(A)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(B) \to C_\bullet(X)/C_\bullet(A) \to 0
  \,.
$$

The corresponding [[nLab:homology long exact sequence]], prop. \ref{HomologyLongExactSequence}, is the long exact sequence in question.

=--

We look at some concrete fundamental examples in a moment. But first it is useful to make explicit the following general sub-notion of relative homology.

Let $X$ still be a given [[nLab:topological space]].

+-- {: .num_defn}
###### Definition

The **[[nLab:augmentation]] map** for the [[nLab:singular homology]] of $X$ is the [[nLab:homomorphism]] of [[nLab:abelian groups]]

$$
  \epsilon \colon C_0(X) \to \mathbb{Z}
$$

which adds up all the coefficients of all 0-chains:

$$
  \epsilon \colon \colon \sum_{i} n_i \sigma_i \mapsto \sum_i n_i
  \,.
$$

Since the [[nLab:boundary]] of a 1-chain is in the [[nLab:kernel]] of this map, by example \ref{BasicExamplesOfChainBoundaries}, it constitutes a [[nLab:chain map]]

$$
  \epsilon \colon C_\bullet(X) \to \mathbb{Z}
  \,,
$$

where now $\mathbb{Z}$ is regarded as a chain complex concentrated in degree 0.

=--

+-- {: .num_defn #ReducedSingularChainComplex}
###### Definition

The **reduced singular chain complex** $\tilde C_\bullet(X)$ of $X$ is the [[nLab:kernel]] of the augmentation map, the chain complex sitting in the [[nLab:short exact sequence]]

$$
  0 \to \tilde C_\bullet(C) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z} \to 0
  \,.
$$

The **reduced singular homology** $\tilde H_\bullet(X)$ of $X$ is the [[nLab:chain homology]] of the reduced singular chain complex

$$
  \tilde H_\bullet(X) \coloneqq H_\bullet(\tilde C_\bullet(X))
  \,.
$$

=--

Equivalently:

+-- {: .num_defn}
###### Definition

The **reduced singular homology** of $X$, denoted $\tilde H_\bullet(X)$, is the [[nLab:chain homology]] of the [[nLab:augmentation|augmented]] chain complex

$$
  \cdots \to C_2(X) \stackrel{\partial_1}{\to} C_1(X) \stackrel{\partial_0}{\to} C_0(X) \stackrel{\epsilon}{\to}
  \mathbb{Z} \to 0
  \,.
$$

=--

Let $X$ be a [[nLab:topological space]], $H_\bullet(X)$ its [[nLab:singular homology]] and $\tilde H_\bullet(X)$ its reduced singular homology, def. \ref{ReducedSingularChainComplex}.

+-- {: .num_prop #RelationBetweenReducedSingularAndSingular}
###### Proposition

For $n \in \mathbb{N}$ there is an [[nLab:isomorphism]]

$$
  H_n(X)
  \simeq
  \left\{
    \array{
      \tilde H_n(X) & for \; n \geq 1
      \\
      \tilde H_0(X) \oplus \mathbb{Z} & for\; n = 0
    }
  \right.
$$

=--

+-- {: .proof}
###### Proof

The [[nLab:homology long exact sequence]], prop. \ref{HomologyLongExactSequence}, of the defining short exact sequence $\tilde C_\bullet(C) \to C_\bullet(X) \stackrel{\epsilon}{\to} \mathbb{Z}$ is, since $\mathbb{Z}$ here is concentrated in degree 0, of the form

$$
  \cdots \to \tilde H_n(X) \to H_n(X) \to 0 \to \cdots \to 
  0 \to 
  \cdots \to \tilde H_1(X) \to H_1(X) \to 0 \to 
  \tilde H_0(X) \to H_0(X) \stackrel{\epsilon}{\to}  \mathbb{Z} \to 0 
  \,.
$$

Here [[nLab:exact sequence|exactness]] says that all the morphisms $\tilde H_n(X) \to H_n(X)$ for positive $n$ are [[nLab:isomorphisms]]. Moreover, since $\mathbb{Z}$ is a [[nLab:free abelian group]], hence a [[nLab:projective object]], the remaining [[nLab:short exact sequence]]

$$
  0 \to \tilde H_0(X) \to H_0(X) \to \mathbb{Z} \to 0
$$

is [[nLab:split exact sequence|split]], by prop. \ref{SplittingLemma}, and hence $H_0(X) \simeq \tilde H_0(X) \oplus \mathbb{Z}$.
 
=--

+-- {: .num_prop}
###### Proposition

For $X = *$ the [[nLab:point]], the morphism

$$
  H_0(\epsilon) \colon H_0(X) \to \mathbb{Z}
$$

is an [[nLab:isomorphism]]. Accordingly the reduced homology of the point vanishes in every degree:

$$
  \tilde H_\bullet(*) \simeq 0
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the discussion in section [2)](#SimplicialHomology) we have that 

$$
  H_n(*) \simeq
  \left\{
    \array{
       \mathbb{Z} & for \; n = 0
       \\
       0 & otherwise
    }
  \right.
  \,.
$$

Moreover, it is clear that $\epsilon \colon C_0(*) \to \mathbb{Z}$ is the [[nLab:identity]] map. 

=--

Now we can discuss the relation between reduced homology and relative homology.

+-- {: .num_prop}
###### Proposition

For $X$ an [[nLab:inhabited set|inhabited]] [[nLab:topological space]], its [[nLab:reduced singular homology]], def. \ref{ReducedSingularChainComplex}, coincides with its [[nLab:relative singular homology]] relative to any base point $x \colon * \to X$:

$$
  \tilde H_\bullet(X)
  \simeq
   H_\bullet(X,*)
  \,.
$$


=--

+-- {: .proof}
###### Proof

Consider the sequence of [[nLab:topological subspace]] inclusions

$$
  \emptyset \hookrightarrow * \stackrel{x}{\hookrightarrow} X
  \,.
$$

By prop. \ref{RelativeTripleHomologyLongExactSequence} this induces a [[nLab:long exact sequence]] of the form

$$
  \cdots
  \to
  H_{n+1}(*) \to H_{n+1}(X) \to H_{n+1}(X,*)
  \to
  H_n(*) \to H_n(X) \to H_n(X,*)
  \to 
  \cdots
  \to 
  H_1(X) \to H_1(X,*) \to  H_0(*) \stackrel{H_0(x)}{\to}  H_0(X) \to H_n(X,*)
  \to 0
  \,.
$$

Here in positive degrees we have $H_n(*) \simeq 0$ and therefore [[nLab:exact sequence|exactness]] gives [[nLab:isomorphisms]]

$$
  H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}
$$

and hence with prop. \ref{RelationBetweenReducedSingularAndSingular} isomorphisms

$$
  \tilde H_n(X) \stackrel{\simeq}{\to} H_n(X,*)\;\; \forall_{n \geq 1}  
  \,.
$$

It remains to deal with the case in degree 0. To that end, observe that $H_0(x) \colon H_0(*) \to H_0(X)$ is a [[nLab:monomorphism]]: for this notice that we have a [[nLab:commuting diagram]]

$$
  \array{
     H_0(*) &\stackrel{id}{\to}& H_0(*)
     \\
     {}^{\mathllap{H_0(x)}}\downarrow &{}^{\mathllap{H_0(f)}}\nearrow& \downarrow^{\mathrlap{H_0(\epsilon)}}_\simeq
     \\
     H_0(X) &\stackrel{H_0(\epsilon)}{\to}& \mathbb{Z}
  }
  \,,
$$

where $f \colon X \to *$ is the terminal map. 
That the outer square commutes means that $H_0(\epsilon) \circ H_0(x) = H_0(\epsilon)$ and hence the composite on the left is an [[nLab:isomorphism]]. This implies that $H_0(x)$ is an injection.

Therefore we have a [[nLab:short exact sequence]] as shown in the top of this diagram

$$
  \array{
    0 &\to& H_0(*) &\stackrel{H_0(x)}{\hookrightarrow}&
    H_0(X) &\stackrel{}{\to}& H_0(X,*)
    &\to&
    0
    \\
    && & {}_{\mathllap{\simeq}}\searrow & \downarrow^{\mathrlap{H_0(\epsilon)}} & 
   \\
   && && \mathbb{Z}
  }
  \,.
$$

Using this we finally compute

$$
  \begin{aligned}
    \tilde H_0(X)
    & \coloneqq 
    ker H_0(\epsilon)
    \\
    & \simeq coker( H_0(x) )
    \\
    & \simeq H_0(X,*)
  \end{aligned}
  \,.
$$

=--

With this understanding of homology _relative to a point_ in hand, we can now characterize relative homology more generally.
From its definition in def. \ref{RelativeSingularHomology}, it is plausible that the relative homology group $H_n(X,A)$ provides information about the quotient topological space $X/A$. This is indeed true under mild conditions:

+-- {: .num_defn #GoodPair}
###### Definition

A [[nLab:topological subspace]] inclusion $A \hookrightarrow X$ is called a **good pair** if 

1. $A$ is [[nLab:closed subset|closed]] inside $X$;

1. $A$ has an [[nLab:neighbourhood]] $A \hookrightarrow U \hookrightarrow X$ such that $A \hookrightarrow U$ has a [[nLab:deformation retract]].

=--

+-- {: .num_prop #HomologyOfQuotientSpace}
###### Proposition

If $A \hookrightarrow X$ is a [[nLab:topological subspace]] inclusion which is _good_ in the sense of def. \ref{GoodPair}, then the $A$-relative singular homology of $X$ coincides with the [[nLab:reduced singular homology]], def. \ref{ReducedSingularChainComplex}, of the [[nLab:quotient space]] $X/A$: 

$$
  H_n(X/A)
  \simeq
  \tilde H_n(X , A)
 \,.
$$

=--

The proof of this is spelled out at _[Relative homology -- relation to quotient topological spaces](relative%20homology#RelationToQuotientTopologicalSpaces)_. It needs the proof of the _[Excision property](http://ncatlab.org/nlab/show/relative%20homology#Excision)_ of relative homology. While important, here we will not further dwell on this. The interested reader can find more information behind the above links.

With the general definition of relative homology in hand, we now consider the basic _cells_ such that _[[nLab:cell complexes]]_ built from such cells have tractable relative homology groups. Actually, up to [[nLab:weak homotopy equivalence]], _every_ [[nLab:Hausdorff topological space]] is given by such a [[nLab:cell complex]] and hence its relative homology, then called _[[nLab:cellular homology]]_, is a good tool for computing singular homology rather generally.

+-- {: .num_defn }
###### Definition

For $n \in \mathbb{N}$ write

* $D^n \hookrightarrow \mathbb{R}^n \in $ [[nLab:Top]] for the standard $n$-[[nLab:disk]];

* $S^{n-1} \hookrightarrow \mathbb{R}^{n} \in $ [[nLab:Top]] for the standard $(n-1)$-[[nLab:sphere]];

  (notice that the 0-sphere is the disjoint union of _two points_, $S^0 = * \coprod *$, and by definition the $(-1)$-sphere is the [[nLab:empty set]])


* $S^{-1} \hookrightarrow D^{n}$ for the [[nLab:continuous function]] that includes the $(n-1)$-sphere as the [[nLab:boundary]] of the $n$-disk.

=--


+-- {: .num_example }
###### Example

The [[nLab:reduced singular homology]] of the $n$-[[nLab:sphere]] $S^{n}$  equals the $S^{n-1}$-relative homology of the $n$-[[nLab:disk]] with respect to the canonical [[nLab:boundary]] inclusion $S^{n-1} \hookrightarrow D^n$: for all $n \in \mathbb{N}$

$$
  \tilde H_\bullet(S^n) \simeq H_\bullet(D^n, S^{n-1})
 \,.
$$

=--

+-- {: .proof}
###### Proof

The $n$-[[nLab:sphere]] is [[nLab:homeomorphism|homeomorphic]] to the $n$-[[nLab:disk]] with its entire [[nLab:boundary]] identified with a point:

$$
  S^n \simeq D^n/S^{n-1}
  \,.
$$

Moreover the boundary inclusion is a _good pair_ in the sense of def. \ref{GoodPair}. Therefore the example follows with prop. \ref{HomologyOfQuotientSpace}.

=--


When forming [[nLab:cell complexes]] from disks, then each relative dimension will be a [[nLab:wedge sum]] of disks:


+-- {: .num_defn #WedgeSum}
###### Definition

For $\{x_i \colon * \to X_i\}_i$ a [[set]] of [[pointed topological spaces]], their _[[nLab:wedge sum]]_ $\vee_i X_i$ is the result of identifying all base points in their [[nLab:disjoint union]], hence the quotient

$$
  \left(
   \coprod_i X_i
  \right)/
  \left(
    \coprod_i *
  \right)
  \,.
$$

=--

+-- {: .num_example }
###### Example

The wedge sum of two pointed [[nLab:circles]] is the "figure 8"-topological space.

=--

+-- {: .num_prop #ReducedHomologyRespectsWedgeSum}
###### Proposition

Let $\{* \to X_i\}_i$ be a set of [[pointed topological spaces]]. Write $\vee_i X_i \in Top$ for their [[nLab:wedge sum]] and write
$\iota_i \colon X_i \to \vee_i X_i$ for the canonical inclusion functions.


Then for each $n \in \mathbb{N}$ the homomorphism

$$
  (\tilde H_n(\iota_i))_i \colon \oplus_i \tilde H_n(X_i) \to \tilde H_n(\vee_i X_i)
$$

is an [[nLab:isomorphism]].

=--


+-- {: .proof}
###### Proof

By prop. \ref{HomologyOfQuotientSpace} the reduced homology of the wedge sum is equivalently the relative homology of the disjoint union of spaces relative to their disjoint union of basepoints

$$
  \tilde H_n(\vee_i X_i)
  \simeq
  H_n(\coprod_i X_i, \coprod_i *)
  \,.
$$  

The relative homology preserves these coproducts (sends them to [[nLab:direct sums]]) and so 

$$
  H_n(\coprod_i X_i, \coprod_i *)
  \simeq
  \oplus_i H_n(X_i, *)
  \,.  
$$

=--

The following defines topological spaces which are inductively built by gluing disks to each other.

+-- {: .num_defn #CWComplex} 
###### Definition

A **[[nLab:CW complex]] of [[nLab:dimension]] $(-1)$** is the [[nLab:empty set|empty]] [[nLab:topological space]].

By [[nLab:induction]], for $n \in \mathbb{N}$ a **[[nLab:CW complex]] of [[nLab:dimension]] $n$** is a [[nLab:topological space]] $X_{n}$ obtained from

1. a $CW$-complex $X_{n-1}$ of dimension $n-1$;

1. an index set $Cell(X)_n \in Set$;

1. a set of [[nLab:continuous maps]] (the **attaching maps**) $\{ f_i \colon S^{n-1} \to X_{n-1}\}_{i \in Cell(X)_n}$

as the [[nLab:pushout]] 

$$
  X_n 
   \simeq 
  \left(
    \coprod_{j \in Cell(X)_n} D^n
  \right) 
   \underset{j \in Cell(X)_n S^{n-1}}{\coprod} 
   X_n
$$

in

$$
  \array{
    \coprod_{j \in Cell(X)_{n}} S^{n-1} &\stackrel{(f_j)}{\to}& X_{n-1}
    \\
    \downarrow && \downarrow
    \\
    \coprod_{j \in Cell(X)_{n}} D^{n} &\to& X_{n} 
  }
  \,,
$$ 

hence as the topological space obtained from $X_{n-1}$ by gluing in $n$-disks $D^n$ for each $j \in Cell(X)_n$ along the given boundary inclusion $f_j \colon S^{n-1} \to X_{n-1}$.

By this construction, an $n$-dimensional CW-complex is canonically a _[[nLab:filtered topological space]]_, hence a sequence of [[nLab:topological subspace]] inclusions of the form

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X_{n-1} \hookrightarrow X_n
$$

which are the right vertical morphisms in the above pushout diagrams. 

A general **[[nLab:CW complex]]** $X$ then is a [[nLab:topological space]] which is the limiting space of a possibly infinite such sequence, hence a topological space given as the [[nLab:sequential colimit]] over a [[nLab:tower]] [[nLab:diagram]] each of whose morphisms is such a filter inclusion 

$$
  \emptyset \hookrightarrow X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X
  \,.
$$

=--

The following basic facts about the [[nLab:singular homology]] of [[nLab:CW complexes]] are important.



Now we can state a variant of singular homology adapted to CW complexes which admits a more systematic way of computing its homology groups. First we observe the following.

+-- {: .num_prop #SkeletalRelativeSingularHomologyOfCW}
###### Proposition

The [[nLab:relative singular homology]], def. \ref{RelativeSingularHomology}, of the filtering degrees of a [[nLab:CW complex]] $X$, def. \ref{CWComplex}, is

$$
  H_n(X_k , X_{k-1})
  \simeq
  \left\{
    \array{
       \mathbb{Z}[Cells(X)_n] & if\; k = n
       \\
       0 & otherwise
    }
  \right.
  \,,
$$

where $\mathbb{Z}[Cells(X)_n]$ denotes the [[nLab:free abelian group]] on the set of $n$-cells.


=--

+-- {: .proof}
###### Proof

The inclusion $X_{k-1} \hookrightarrow X_k$ is a _good pair_ in the sense of def. \ref{GoodPair}. The quotient $X_k/X_{k-1}$ is by definition of CW-complexes a [[nLab:wedge sum]], def. \ref{WedgeSum}, of $k$-[[nLab:spheres]], one for each element in $Cell(X)_k$. Therefore by prop. \ref{HomologyOfQuotientSpace} we have an isomorphism $H_n(X_k , X_{k-1}) \simeq \tilde H_n( X_k / X_{k-1})$ with the [[nLab:reduced homology]] of this wedge sum. The statement then follows by the respect of reduced homology for wedge sums, prop. \ref{ReducedHomologyRespectsWedgeSum}.

=--

+-- {: .num_prop #SingularHomologyOfCWComples} 
###### Proposition

For $X$ a [[nLab:CW complex]] with skeletal filtration $\{X_n\}_n$ as above, and with $k,n \in \mathbb{N}$ we have for the [[nLab:singular homology]] of $X$ that

$$
  (k \gt n) \Rightarrow (H_k(X_n) \simeq 0)
  \,.
$$

In particular if $X$ is a CW-complex of finite [[nLab:dimension]] $dim X$ (the maximum degree of cells), then 

$$
  (k \gt dim X) \Rightarrow (H_k(X) \simeq 0).
$$

Moreover, for $k \lt n$ the inclusion

$$
  H_k(X_n) \stackrel{\simeq}{\to} H_k(X)
$$

is an [[nLab:isomorphism]] and for $k = n$ we have an isomorphism

$$
  image(H_n(X_n) \to H_n(X)) \simeq H_n(X)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By the [[nLab:long exact sequence]] in [[nLab:relative homology]], prop. \ref{RelativeHomologyLongExactSequence} we have an [[nLab:exact sequence]] of the form

$$
  H_{k+1}(X_n , X_{n-1})
  \to 
  H_k(X_{n-1})
  \to 
  H_k(X_n)
  \to 
  H_k(X_n, X_{n-1})
  \,.
$$

Now by prop. \ref{SkeletalRelativeSingularHomologyOfCW} the leftmost and rightmost homology groups here vanish when $k \neq n$ and $k \neq n-1$ and hence exactness implies that

$$
  H_k(X_{n-1})
  \stackrel{\simeq}{\to}
  H_k(X_n)
$$

is an [[nLab:isomorphism]] for $k \neq n,n-1$. This implies the first claims by [[nLab:induction]] on $n$.

Finally for the last claim use that the above exact sequence gives

$$
  H_{n-1+1}(X_n , X_{n-1})
  \to 
  H_{n-1}(X_{n-1})
  \to 
  H_{n-1}(X_n)
  \to 
  0
$$

and hence that with the above the map $H_{n-1}(X_{n-1}) \to H_{n-1}(X)$ is surjective.

=--

We can now discuss the _[[nLab:cellular homology]]_ of a [[nLab:CW complex]].

+-- {: .num_defn #CellularChainComplex} 
###### Definition

For $X$ a [[nLab:CW-complex]], def. \ref{CWComplex}, its
**cellular chain complex** $H_\bullet^{CW}(X) \in Ch_\bullet$ is the [[nLab:chain complex]] such that for $n \in \mathbb{N}$

* the [[nLab:abelian group]] of [[nLab:chains]] is the [[nLab:relative singular homology]] group, def. \ref{RelativeSingularHomology}, of $X_n \hookrightarrow X$ relative to $X_{n-1} \hookrightarrow X$:

  $$
    H_n^{CW}(X) \coloneqq H_n(X_n, X_{n-1})
    \,,
  $$

* the [[nLab:differential]] $\partial^{CW}_{n+1} \colon H_{n+1}^{CW}(X) \to H_n^{CW}(X)$ is the [[nLab:composition]]

  $$
    \partial^{CW}_n 
    \colon
    H_{n+1}(X_{n+1}, X_n) 
     \stackrel{\partial_n}{\to} 
    H_n(X_n) 
     \stackrel{i_n}{\to} 
    H_n(X_n, X_{n-1})
    \,,
  $$ 

  where $\partial_n$ is the [[nLab:boundary]] map of the [[nLab:singular chain complex]] and where $i_n$ is the morphism on [[nLab:relative homology]] induced from the canonical inclusion of pairs $(X_n, \emptyset) \to (X_n, X_{n-1})$. 

=--

+-- {: .num_prop} 
###### Proposition 

The composition $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ of two differentials in def. \ref{CellularChainComplex} is indeed zero, hence $H^{CW}_\bullet(X)$ is indeed a [[nLab:chain complex]].

=-- 

+-- {: .proof}
###### Proof

On representative singular [[nLab:chains]] the morphism $i_n$ acts as the identity and hence $\partial^{CW}_{n} \circ \partial^{CW}_{n+1}$ acts as the double singular boundary, $\partial_{n} \circ \partial_{n+1} = 0$.

=--

+-- {: .num_remark} 
###### Remark

This means that

* a **cellular $n$-chain** is a singular $n$-chain required to sit in filtering degree $n$, hence in $X_n \hookrightarrow X$;

* a **cellular $n$-cycle** is a singular $n$-chain whose singular boundary is not necessarily 0, but is contained in filtering degree $(n-2)$, hence in $X_{n-2} \hookrightarrow X$.

* a **cellular $n$-boundary** is a singular $n$-chain which is the boundary of a singular $(n+1)$-chain coming from filtering degree $(n+1)$.

=--

This kind of situation -- chains that are cycles only up to lower filtering degree and boundaries that come from specified higher filtering degree -- has an evident generalization to higher relative filtering degrees. And in this greater generality the concept is of great pracrical relevance. Therefore before discussing cellular homology further now, we consider this more general "higher-order relative homology" that it suggests (namely the formalism of [[nLab:spectral sequences]]). After establishing a few fundamental facts about that we will come back in prop. \ref{SpectralSequenceOfCWComplex} below to analyse the above cellular situation using this conceptual tool.

First we abstract the structure on chain complexes that in the above example was induced by the CW-complex structure on the [[nLab:singular chain complex]].

+-- {: .num_defn #FilteredChainComplex}
###### Definition

The structure of a **[[nLab:filtered chain complex]]** in a [[nLab:chain complex]] $C_\bullet$ is a sequence of [[nLab:chain map]] inclusions

$$
  \cdots
  \hookrightarrow
  F_{p-1}C_\bullet \hookrightarrow F_p C_\bullet \hookrightarrow
  \cdots 
  \hookrightarrow
  C_\bullet
  \,.
$$

The **[[nLab:associated graded]] complex** of a filtered chain complex, denoted $G_\bullet C_\bullet$, is the collection of [[nLab:quotient]] chain complexes

$$
  G_p C_\bullet \coloneqq F_p C_\bullet / F_{p-1} C_\bullet
  \,.
$$

We say that element of $G_p C_\bullet$ are _in filtering degree_ $p$.

=--

+-- {: .num_remark}
###### Remark

In more detail this means that

1. $[\cdots \stackrel{\partial_{n}}{\to} C_n \stackrel{\partial_{n-1}}{\to} C_{n-1} \to \cdots]$ is a [[nLab:chain complex]], hence $\{C_n\}$ are [[nLab:objects]] in $\mathcal{A}$ ($R$-[[nLab:modules]]) and $\{\partial_n\}$ are [[nLab:morphisms]] (module [[nLab:homomorphisms]]) with $\partial_{n+1} \circ \partial_{n} = 0$;

1. For each $n \in \mathbb{Z}$ there is a [[nLab:filtered object|filtering]] $F_\bullet C_n$ on $C_n$ and all these filterings are compatible with the [[nLab:differentials]] in that 

   $$
     \partial(F_p C_n) \subset F_p C_{n-1}
   $$

1. The grading associated to the filtering is such that the $p$-graded elements are those in the [[nLab:quotient]]

   $$
     G_p C_n \coloneqq \frac{F_p C_n}{ F_{p-1} C_n}
     \,.
   $$

   Since the differentials respect the grading we have chain complexes $G_p C_\bullet$ in each filtering degree $p$.

=--

Hence elements in a filtered chain complex are **[[nLab:bigraded object|bi-graded]]**: they carry a degree as elements of $C_\bullet$ as usual, but now they also carry a filtering degree: for $p,q \in \mathbb{Z}$ we therefore also write

$$
  C_{p,q} \coloneqq F_p C_{p+q}
$$

and call this the collection of **$(p,q)$-chains** in the filtered chain complex.

Accordingly we have $(p,q)$-cycles and -boundaries. But for these we may furthermore refine to a notion where also the filtering degree of the boundaries is constrained:


+-- {: .num_defn #AlmostChainsCyclesBoundaries}
###### Definition

Let $F_\bullet C_\bullet$ be a [[nLab:filtered chain complex]].  Its [[nLab:associated graded]] chain complex is the set of chain complexes

$$
  G_p C_\bullet \coloneqq F_p C_\bullet / F_{p-1} C_\bullet
$$

for all $p$. 

Then for $r, p, q \in \mathbb{Z}$ we say that

1. $G_p C_{p+q}$ is the module of ***$(p,q)$-[[nLab:chains]]*** or of ***$(p+q)$-chains in filtering degree $p$***;

1. $\begin{aligned} Z^r_{p,q}  & \coloneqq \left\{ c \in G_p C_{p+q} | \partial c = 0 \, mod F_{p-r} C_{\bullet} \right\} \\ & =  \left\{ c \in F_p C_{p+q} | \partial(c) \in F_{p-r} C_{p+q-1} \right\}/ F_{p-1}C_{p+q} \end{aligned}$

   is the module of ***$r$-almost $(p,q)$-[[nLab:cycles]]*** (the $(p+q)$-chains whose differential vanishes modulo terms of filtering degree $p-r$);


1. $B^{r}_{p,q} \coloneqq \partial(F_{p+r-1} C_{p+q+1}) \,,$

   is the module of **$r$-almost $(p,q)$-[[nLab:boundaries]]**.

=--

Similarly we set

$$
  Z^\infty_{p,q} \coloneqq \{c \in F_p C_{p + q} | \partial c = 0 \}/F_{p-1}C_{p+q}
  = 
  Z(G_p C_{p+q})
$$

$$
  B^\infty_{p,q} \coloneqq \partial( F_p C_{p+q+1} )
  \,.
$$

From this definition we immediately have that the differentials $\partial \colon C_{p+q} \to C_{p+q-1}$ restrict to the $r$-almost cycles as follows:

+-- {: .num_prop #DifferentialsOnAlmostChains}
###### Proposition

The [[nLab:differentials]] of $C_\bullet$ restrict on $r$-almost cycles to homomorphisms of the form

$$
  \partial^r 
   \colon
  Z^r_{p,q}
  \to
  Z^r_{p-r, q+r-1}
  \,.
$$

These are still [[nLab:differentials]]: $\partial^2 = 0$.

=--


+-- {: .proof}
###### Proof

By the very definition of $Z^r_{p,q}$ it consists of elements in filtering degree $p$ on which $\partial$ decreases the filtering degree to $p-r$. Also by definition of differential on a chain complex, $\partial$ decreases the actual degree $p+q$ by one. This explains that $\partial$ restricted to $Z^r_{p,q}$ lands in $Z^\bullet_{p-r,q+r-1}$. 
Now the image constists indeed of actual boundaries, not just $r$-almost boundaries. But since actual boundaries are in particular $r$-almost boundaries, we may take the [[codomain]] to be $Z^r_{p-r,q+r-1}$.

=--

As before, we will in general index these differentials by their [[codomain]] and hence write in more detail

$$
  \partial^r 
   \colon
  Z^r_{p,q}
  \to
  Z^r_{p-r, q+r-1}
  \,.
$$


+-- {: .num_prop }
###### Proposition

We have a sequence of canonical inclusions

$$
  B^0_{p,q}
  \hookrightarrow
  B^1_{p,q}
  \hookrightarrow
  \cdots
  B^\infty_{p,q}
  \hookrightarrow
  Z^\infty_{p,q}
  \hookrightarrow
  \cdots 
  \hookrightarrow
  Z^1_{p,q}
  \hookrightarrow
  Z^0_{p,q}
  \,.
$$

=--

The following observation is elementary, and yet this is what drives the theory of [[nLab:spectral sequences]], as it shows that almost cycles may be computed iteratively by homological means themselves.

+-- {: .num_prop #KernelsInsideAlmostCycles}
###### Proposition

The $(r+1)$-almost cycles are the $\partial^r$-[[nLab:kernel]] inside the $r$-almost cycles:

$$
  Z^{r+1}_{p,q}
  \simeq 
  ker( Z^r_{p,q} \stackrel{\partial^r}{\to} Z^r_{p-r, q+r-1} )
  \,.
$$

=--


+-- {: .proof}
###### Proof

An element $c \in F_p C_{p+q}$ represents 

1. an element in $Z^r_{p,q}$ if $\partial c \in F_{p-r} C_{p+q-1}$

1. an element in $Z^{r+1}_{p,q}$ if even $\partial c \in F_{p-r-1} C_{p+q-1} \hookrightarrow F_{p-r} C_{p+q-1}$.

The second condition is equivalent to $\partial c$ representing the 0-element in the quotient $F_{p-r}C_{p+q-1}/ F_{p-r-1}C_{p+q-1}$. But this is in turn equivalent to $\partial c$ being 0 in $Z^r_{p-r,q+r-1} \subset F_{p-r} C_{p+q-1} / F_{p-r-1} C_{p+q-1}$.

=--

With a definition of almost-cycles and almost-boundaries, of course we are now interested in the corresponding homology groups:

+-- {: .num_defn #ExplicitForm}
###### Definition

For $r, p, q \in \mathbb{Z}$ define the **$r$-almost $(p,q)$-[[nLab:chain homology]]** of the filtered complex to be the [[nLab:quotient]] of the $r$-almost $(p,q)$-cycles by the $r$-almost $(p,q)$-boundaries, def. \ref{AlmostChainsCyclesBoundaries}:

$$
  \begin{aligned}
    E^r_{p,q}
    & \coloneqq
    \frac{Z^r_{p,q}}{B^r_{p,q}}
    \\
    & = 
  \frac{
    \left\{
     x \in F_p C_{p+q} \,|\, \partial x \in F_{p-r} C_{p+q-1}
    \right\}
  }
  {
    \partial( F_{p+r-1} C_{p+q+1} ) \oplus F_{p-1} C_{p+q} 
  }
  \end{aligned}
$$

By prop. \ref{DifferentialsOnAlmostChains} the differentials of $C_\bullet$ restrict on the $r$-almost homology groups to maps

$$
  \partial^r : E^r_{p,q} \to E^r_{p-r, q+r - 1}
  \,.
$$


=--

The central property of these $r$-almost homology groups now is their following iterative homological characterization.


+-- {: .num_prop #ExplicitDefIsIndeedSpectralSequ}
###### Proposition

With definition \ref{ExplicitForm} we have that
$E^{r+1}_{\bullet, \bullet}$ is the $\partial^r$-[[nLab:chain homology]] of $E^r_{\bullet, \bullet}$:

$$
  E^{r+1}_{p,q} 
  = 
 \frac{
    ker(\partial^r : E^r_{p,q} \to E^r_{p-r, q+r-1})
  }{
    im( \partial^r : E^r_{p+r, q-r+1} \to E^r_{p,q} )
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof

By prop. \ref{KernelsInsideAlmostCycles}.

=--

This structure on the collection of $r$-almost cycles of a filtered chain complex thus obtained is called a _[[nLab:spectral sequence]]_:

+-- {: .num_defn #SpectralSequence}
###### Definition

A **spectral sequence** of $R$-[[nLab:modules]] is

1. a set $\{E_{p,q}^r\}_{p,q,r \in \mathbb{Z}}$ of $R$-modules;

1. a set $\{ \partial^r_{p,q} \colon E_{p,q}^{r} \to E^r_{p-r, q+r-1} \}_{r,p,q \in \mathbb{Z}}$ of [[nLab:homomorphisms]]

such that

1. the $\partial^r$s are [[nLab:differentials]]: $\forall_{p,q,r}  (\partial^r_{p-r,q+r-1} \circ \partial^r_{p,q} = 0)$;

1. the modules $E^{r+1}_{p,q}$ are the $\partial^r$-[[nLab:homology]] of the modules in relative degree $r$:

   $$
     \forall_{r,p,q} 
     \left(
       E^{r+1}_{p,q} \simeq \frac{ker(\partial^r_{p-r,q+r-1})}{im(\partial^r_{p, q})}
      \right)
     \,.
   $$ 

One says that $E^r_{\bullet,\bullet}$ is the **$r$-page** of the spectral sequence. 

=--

Since this turns out to be a useful structure to make explicit, as the above motivation should already indicate, one introduces the following terminology and basic facts to talk about spectral sequences.


+-- {: .num_defn #LimitTerm}
###### Definition

Let $\{E^r_{p,q}\}_{r,p,q}$ be a [[nLab:spectral sequence]], def. \ref{SpectralSequence}, such that for each $p,q$ there is $r(p,q)$ such that for all $r \geq r(p,q)$ we have

$$
  E^{r \geq r(p,q)}_{p,q} \simeq E^{r(p,q)}_{p,q}
  \,.
$$

Then one says that

1. the [[nLab:bigraded object]]

   $$
     E^\infty 
      \coloneqq 
     \{E^\infty_{p,q}\}_{p,q} \coloneqq \{ E^{r(p,q)}_{p,q} \}_{p,q}
   $$

   is the **limit term** of the spectral sequence;

*  the spectral sequence **abuts** to $E^\infty$.

=--

+-- {: .num_example #Degeneration}
###### Example

If for a spectral sequence there is $r_s$ such that all [[nLab:differentials]] on pages after $r_s$ vanish, $\partial^{r \geq r_s} = 0$, then $\{E^{r_s}\}_{p,q}$ is a limit term for the spectral sequence. One says in this cases that the spectral sequence **degenerates** at $r_s$.

=--

+-- {: .proof}
###### Proof

By the defining relation

$$
  E^{r+1}_{p,q} \simeq ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q}) = E^r_{pq}
$$

the spectral sequence becomes constant in $r$ from $r_s$ on if all the differentials vanish, so that $ker(\partial^r_{p,q}) = E^r_{p,q}$ for all $p,q$.

=--


+-- {: .num_example #Collaps}
###### Example

If for a [[nLab:spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ there is $r_s \geq 2$ such that the $r_s$th page is concentrated in a single row or a single column, then the spectral sequence degenerates on this pages, example \ref{Degeneration}, hence this page is a limit term, def. \ref{LimitTerm}. One says in this case that the spectral sequence **collapses** on this page.

=--

+-- {: .proof}
###### Proof

For $r \geq 2$ the [[nLab:differentials]] of the spectral sequence

$$
  \partial^r \colon E^r_{p,q} \to E^r_{p-r, q+r-1}
$$ 

have [[nLab:domain]] and [[nLab:codomain]] necessarily in different rows an columns (while for $r = 1$ both are in the same row and for $r = 0$ both coincide). Therefore if all but one row or column vanish, then all these differentials vanish.

=--


+-- {: .num_defn #Convergence}
###### Definition

A [[nLab:spectral sequence]] $\{E^r_{p,q}\}_{r,p,q}$ is said to **converge** to a [[nLab:graded object]] $H_\bullet$ with [[nLab:filtered chain complex|filtering]] $F_\bullet H_\bullet$, traditionally denoted

$$
  E^r_{p,q} \Rightarrow H_\bullet
  \,,
$$

if the [[nLab:associated graded]] complex $\{G_p H_{p+q}\}_{p,q} \coloneqq \{F_p H_{p+q} / F_{p-1} H_{p+q}\}$ of $H$ is the limit term of $E$, def. \ref{LimitTerm}:

$$
  E^\infty_{p,q} \simeq G_p H_{p+q} \;\;\;\;\;\;\; \forall_{p,q}
  \,.
$$

=--

+-- {: .num_remark }
###### Remark

In practice spectral sequences are often referred to via their first non-trivial page, often also the page at which it collapses, def. \ref{Collaps}, often already the second page. Then one tends to use notation such as

$$
  E^2_{p,q} \Rightarrow H_\bullet
$$

to be read as "There is a spectral sequence whose second page is as shown on the left and which converges to a filtered object as shown on the right."

=--

+-- {: .num_defn #BoundedSpectralSequence}
###### Definition

A spectral sequence $\{E^r_{p,q}\}$ is called a **bounded spectral sequence** if for all $n,r \in \mathbb{Z}$ the number of non-vanishing terms of total degree $n$, hence of the form $E^r_{k,n-k}$, is finite.

=--

+-- {: .num_defn #QuadrantSpectralSequence}
###### Example

A [[nLab:spectral sequence]] $\{E^r_{p,q}\}$ is called

* a **first quadrant spectral sequence** if all terms except possibly for $p,q \geq 0$ vanish;

* a **third quadrant spectral sequence** if all terms except possibly for $p,q \leq 0$ vanish.

Such spectral sequences are bounded, def. \ref{BoundedSpectralSequence}.

=--



+-- {: .num_prop #BoundedSpectralSequenceHasLimitTerm}
###### Proposition

A bounded spectral sequence, def. \ref{BoundedSpectralSequence}, has a limit term, def. \ref{LimitTerm}.

=--

+-- {: .proof}
###### Proof

First notice that if a spectral sequence has at most $N$ non-vanishing terms of total degree $n$ on page $r$, then all the following pages have at most at these positions non-vanishing terms, too, since these are the homologies of the previous terms.

Therefore for a bounded spectral sequence for each $n$ there is $L(n) \in \mathbb{Z}$ such that $E^r_{p,n-p} = 0$ for all $p \leq L(n)$ and all $r$. Similarly there is $T(n) \in \mathbb{Z}$ such $E^r_{n-q,q} = 0$ for all $q \leq T(n)$ and all $r$.

We claim then that the limit term of the bounded spectral sequence is in position $(p,q)$ given by the value $E^r_{p,q}$ for 

$$
  r \gt max(  p-L(p+q-1), q + 1 - L(p+q+1) )
  \,.
$$

This is because for such $r$ we have

1. $E^r_{p-r, q+r-1} = 0$ because $p-r \lt L(p+q-1)$, and hence the [[nLab:kernel]] $ker(\partial^r_{p-r,q+r-1}) = 0$ vanishes;

1. $E^r_{p+r, q-r+1} = 0$ because $q-r + 1 \lt T(p+q+1)$, and hence the [[nLab:image]] $im(\partial^r_{p,q}) = 0$ vanishes.

Therefore

$$
  \begin{aligned}
    E^{r+1}_{p,q} 
    &= 
    ker(\partial^r_{p-r,q+r-1})/im(\partial^r_{p,q})
    \\
    & \simeq E^r_{p,q}/0
    \\
    & \simeq E^r_{p,q}
  \end{aligned}
  \,.
$$

=--

The central statement about the notion of the spectral sequence of a filtered chain complex then is the following proposition. It says that the iterative computation of higher order relative homology indeed in the limit computes the genuine homology.

+-- {: .num_defn #FilteringOnHomology}
###### Definition

For $F_\bullet C_\bullet$ a [[nLab:filtered complex]], write for $p \in \mathbb{Z}$

$$
  F_p H_\bullet(C) 
   \coloneqq
  image( H_\bullet(F_p C) \to H_\bullet(C) )
  \,.
$$

This defines a [[nLab:filtered object|filtering]] $F_\bullet H_\bullet(C)$ of the homology, regarded as a graded object.

=--


+-- {: .num_prop #ConvergingToGenuineHomology}
###### Proposition

If the [[nLab:spectral sequence of a filtered complex]] $F_\bullet C_\bullet$ of prop. \ref{ExplicitDefIsIndeedSpectralSequ} has a limit term, def. \ref{LimitTerm} then it converges, def. \ref{Convergence}, to the chain homology of $C_\bullet$

$$
  E^r_{p,q} \Rightarrow H_{p+q}(C_\bullet)
  \,,
$$

i.e. for sufficiently large $r$ we have

$$
  E^r_{p,q} \simeq G_p H_{p+q}(C) 
  \,,
$$

where on the right we have the [[nLab:associated graded object]] of the filtering of def. \ref{FilteringOnHomology}.

=--

+-- {: .proof}
###### Proof

By assumption, there is for each $p,q$ an $r(p,q)$ such that for all $r \geq r(p,q)$ the $r$-almost cycles and $r$-almost boundaries, def. \ref{AlmostChainsCyclesBoundaries}, in $F_p C_{p+q}$ are the ordinary [[nLab:cycles]] and [[nLab:boundaries]]. Therefore for $r \geq r(p,q)$ def. \ref{ExplicitForm} gives $E^r_{p,q} \simeq G_p H_{p+q}(C)$.


=--

This says what these spectral sequences are converging to. For computations it is also important to know how they start out for low $r$. We can generally characterize $E^r_{p,q}$ for very low values of $r$ simply as follows:

+-- {: .num_prop #SpectralSequencePagesForLowr}
###### Proposition

We have

* $E^0_{p,q} = G_p C_{p+q} = F_p C_{p+q} / F_{p-1} C_{p+q}$ 

  is the [[nLab:associated graded|associated p-graded]] piece of $C_{p+q}$;

* $E^1_{p,q} = H_{p+q}(G_p C_\bullet)$

=--

+-- {: .proof}
###### Proof

For $r = 0$ def. \ref{ExplicitForm} restricts to

$$
  E^0_{p,q} = \frac{ F_p C_{p+q}}{F_{p-1} C_{p+q}} = G_p C_{p+q}
$$

because for $c \in F_p C_{p+q}$ we automatically also have $\partial c \in F_p C_{p+q}$ since the differential respects the filtering degree by assumption. 

For $r = 1$ def. \ref{ExplicitForm} gives 

$$
  E^1_{p,q} = \frac{\{c \in G_p C_{p+q} | \partial c = 0 \in G_p C_{p+q}\} }{\partial(F_p C_{p+q})} = H_{p+q} (G_p C_\bullet)
  \,.
$$


=--

+-- {: .num_remark}
###### Remark

There is, in general, a decisive difference between the homology of the associated graded complex $H_{p+q}(G_p C_\bullet)$ and the associated graded piece of the genuine homology $G_p H_{p+q}(C_\bullet)$: in the former the differentials of cycles are required to vanish only up to terms in lower degree, but in the latter they are required to vanish genuinely. The latter expression is instead the value of the spectral sequence for $r \to \infty$, see prop. \ref{ConvergingToGenuineHomology} below.

=--


These general facts now allow us, as a first simple example for the application of [[nLab:spectral sequences]] to see transparently that the [[nLab:cellular homology]] of a CW complex, def. \ref{CellularChainComplex}, coincides with its genuine [[nLab:singular homology]].

First notice that of course the structure of a [[nLab:CW-complex]] on a [[nLab:topological space]] $X$, def. \ref{CWComplex} naturally induces on its [[nLab:singular simplicial complex]] $C_\bullet(X)$ the structure of a [[nLab:filtered chain complex]], def. \ref{FilteredChainComplex}:


+-- {: .num_defn #SpectralSequenceOfSingularChainsInCWComplex} 
###### Definition

For $X_0 \hookrightarrow X_1 \hookrightarrow \cdots \hookrightarrow X$ a 
[[nLab:CW complex]], and $p \in \mathbb{N}$, write

$$
  F_p C_\bullet(X) \coloneqq C_\bullet(X_p)
$$

for the [[nLab:singular chain complex]] of $X_p \hookrightarrow X$. The given  [[nLab:topological subspace]] inclusions $X_p \hookrightarrow X_{p+1}$ induce [[nLab:chain map]] inclusions $F_p C_\bullet(X) \hookrightarrow F_{p+1} C_\bullet(X)$ and these equip the singular chain complex $C_\bullet(X)$ of $X$ with the structure of a bounded [[nLab:filtered chain complex]]

$$
  0 
  \hookrightarrow
  F_0 C_\bullet(X)
  \hookrightarrow
  F_1 C_\bullet(X)
  \hookrightarrow
  F_2 C_\bullet(X)
  \hookrightarrow 
  \cdots
  \hookrightarrow 
  F_\infty C_\bullet(X)
  \coloneqq
  C_\bullet(X)
  \,.
$$

(If $X$ is of finite [[nLab:dimension]] $dim X$ then this is a bounded filtration.)

Write $\{E^r_{p,q}(X)\}$ for the [[nLab:spectral sequence of a filtered complex]] corresponding to this filtering.

=--

+-- {: .num_prop #SpectralSequenceOfCWComplex} 
###### Proposition

The spectral sequence $\{E^r_{p,q}(X)\}$ of singular chains in a [[nLab:CW complex]] $X$, def. \ref{SpectralSequenceOfSingularChainsInCWComplex} converges, def. \ref{Convergence}, to the [[nLab:singular homology]] of $X$:

$$
  E^r_{p,q}(X) \Rightarrow H_\bullet(X)
  \,.
$$ 

=--

+-- {: .proof}
###### Proof

The spectral sequence $\{E^r_{p,q}(X)\}$ is clearly a first-quadrant spectral sequence, def. \ref{QuadrantSpectralSequence}. Therefore it is a bounded spectral sequence, def. \ref{BoundedSpectralSequence} and hence has a limit term, def. \ref{BoundedSpectralSequenceHasLimitTerm}. So the statement follows with prop. \ref{ConvergingToGenuineHomology}.

=--


We now identify the low-degree pages of $\{E^r_{p,q}(X)\}$ with structures in singular homology theory.

+-- {: .num_prop #PagesInTheSpectralSequenceOfTheFilteredSingularComplex} 
###### Proposition

* $r = 0$ -- $E^0_{p,q}(X) \simeq C_{p+q}(X_p)/C_{p+q}(X_{p-1})$ is the group of $X_{p-1}$-[[nLab:relative homology|relative (p+q)-chains]], def. \ref{RelativeSingularHomology}, in $X_p$;

* $r = 1$ -- $E^1_{p,q}(X) \simeq H_{p+q}(X_p, X_{p-1})$ is the $X_{p-1}$-[[nLab:relative singular homology]], def. \ref{RelativeSingularHomology}, of $X_p$;

* $r = 2$ -- $E^2_{p,q}(X) \simeq \left\{ \array{ H_p^{CW}(X) & for\; q = 0 \\ 0 & otherwise }  \right.$

* $r = \infty$ -- $E^\infty_{p,q}(X) \simeq F_p H_{p+q}(X) / F_{p-1} H_{p+q}(X) $.

=--

+-- {: .proof}
###### Proof

By straightforward and immediate analysis of the definitions.

=--

As a result of these general considerations we now obtain the promised isomorphism between the cellular homology and the singular homology of a CW-complex $X$:

+-- {: .num_cor #CelluarEquivalentToSingularFromSpectralSequence} 
###### Corollary

For $X \in $ [[nLab:Top]] a [[nLab:CW complex]], def. \ref{CWComplex}, its [[nLab:cellular homology]], def. \ref{CellularChainComplex} $H^{CW}_\bullet(X)$ coincides with its singular homology $H_\bullet(X)$, def. \ref{SingularHomology}:  

$$ 
  H^{CW}_\bullet(X) \simeq H_\bullet(X)
 \,.
$$

=--

+-- {: .proof}
###### Proof

By the third item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} the $(r = 2)$-page of the spectral sequence $\{E^r_{p,q}(X)\}$ is concentrated in the $(q = 0)$-row and hence it collapses there, def. \ref{Collaps}. Accordingly we have 

$$
  E^\infty_{p,q}(X) \simeq E^2_{p,q}(X)
$$

for all $p,q$. By the third and fourth item of prop. \ref{PagesInTheSpectralSequenceOfTheFilteredSingularComplex} this non-trivial only for $q = 0$ and there it is equivalently

$$
  G_p H_{p}(X) \simeq H^{CW}_p(X)
  \,.
$$

Finally observe that $G_p H_p(X) \simeq H_p(X)$ by the definition of the filtering on the homology, def. \ref{FilteringOnHomology}, and using prop. \ref{SingularHomologyOfCWComples}.


=--

This concludes our discussion of how relative homology theory of cellularly filtered objects allows to efficiently compute the genuine homology of these objects, and how this motivates the general concept  of [[nLab:spectral sequences]] as organizing higher order relative homology groups. 

Next we consider the generalisation of the spectral sequence for computing [[ordinary cohomology]] to that computing [[generalized cohomology]], given by maps into [[spectra]]. 

...[[Atiyah-Hirzebruch spectral sequence]]...






## **Part 2) Adams spectral sequences**

We follow ([Hopkins 99, section 5](#Hopkins99),  [Aramian](#Aramian)).


#### $E$-Adams resolutions

First we consider a concept of $E$-[[injective objects]] in [[Spectra]].

+-- {: .num_defn #ExactSequences}
###### Definition

Say that 

1. a sequence of spectra

   $$
     A_1 \longrightarrow A_2 \longrightarrow \cdots \longrightarrow A_n
   $$

   is 

   1. a (long) _exact sequence_ if the induced sequence of homotopy functors, def. \ref{HomotopyFunctor}, is a [[long exact sequence]] in $[HoSpectra,Ab]$;

   2. (for $n = 2$) a _short exact sequence_ if

      $$
        0 \longrightarrow A_1 \longrightarrow A_2 \longrightarrow A_3 \longrightarrow 0
      $$

      is (long) exact;


1. a morphism $A \longrightarrow B$  is 

   1. a _monomorphism_ if $0 \longrightarrow A \longrightarrow B$ is an exact sequence;

   1. an _epimorphism_ if $A \longrightarrow B \longrightarrow 0$ is an exact sequence.

For $E$ a [[ring spectrum]], then a sequence of spectra is (long/short) _$E$-exact_ and a morphism is epi/mono, respectively, if becomes long/short exact or epi/mono, respectively, after taking [[smash product of spectra|smash product]] with $E$.

=--

+-- {: .num_example}
###### Example

Every [[homotopy cofiber sequence]] of spectra is exact in the sense of def. \ref{ExactSequences}. 

=--

+-- {: .num_remark}
###### Remark/Warning

Consecutive morphisms in an $E$-exact sequence according to def. \ref{ExactSequences} in general need not compose up to homotopy, to the [[zero morphism]]. But this does become true for sequences of $E$-injective objects, defined below in def. \ref{EInjective}.

=--

+-- {: .num_lemma}
###### Lemma

1. If $f \colon B\longrightarrow A$ is a monomorphism in the sense of def. \ref{ExactSequences}, then there exists a morphism $g \colon C \longrrightarrow A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     f \vee g \;\colon\; B \wedge C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

1. If $f \colon A \longrightarrow B$ is an epimorpimsm in the sense of def. \ref{ExactSequences}, then there exists a homotopy [[section]] $s \colon B\to A$, i.e. $f\circ s\simeq Id$, together with a morphism $g \colon C \to A$ such that the [[wedge sum]] morphism is a [[weak homotopy equivalence]]

   $$
     s \vee f \colon B\vee C \stackrel{\simeq}{\longrightarrow} A
     \,.
   $$

=--

+-- {: .num_defn #EInjective}
###### Definition

For $E$ a [[ring spectrum]], say that a spectrum $S$ is _$E$-injective_ if for each morphism $A \longrightarrow S$ and  each $E$-monomorphism $f \colon A \longrightarrow S$ in the sense of def. \ref{ExactSequences}, there is a [[diagram]] in [[HoSpectra]] of the form

$$
  \array{
    A &\longrightarrow & S 
    \\
    \downarrow & \nearrow_{\mathrlap{\exists}}
    \\
    B
  }
  \,.
$$

=--

+-- {: .num_lemma}
###### Lemma

If $S$ is $E$-injective in the sense of def. \ref{EInjective}, then there exists a spectrum $X$ such that $S$ is a [[retract]] in [[HoSpectra]] of $E \wedge X$.

=--


+-- {: .num_defn #EAdamsResolution}
###### Definition

For $E$ a [[ring spectrum]], then an _$E$-Adams resolution_ of an spectrum $S$ is a long exact sequence, in the sense of def. \ref{ExactSequences}, of the form


$$
  0 \longrightarrow S \longrightarrow I_0 \longrightarrow I_1 \longrightarrow I_2 \longrightarrow \cdots
$$

such that each $I_j$ is $E$-injective, def. \ref{EInjective}.

=--

+-- {: .num_lemma}
###### Lemma

Any two consecutive maps in an $E$-Adams resolution compose to the [[zero morphism]].

=--


+-- {: .num_lemma}
###### Lemma

For $X \to X_\bullet$ an $E$-Adams resolution, def. \ref{EAdamsResolution}, and for $X \longrightarrow Y$ any morphism, then there exists an $E$-Adams resolution $Y \to J_\bullet$ and a [[commuting diagram]]

$$
  \array{
     X &\longrightarrow& I_\bullet
     \\
     \downarrow^{\mathrlap{f}} && \downarrow^{\mathrlap{g_\bullet}}
     \\
     Y &\longrightarrow& J_\bullet
  }
  \,.
$$

=--

+-- {: .num_example #StandardEResolution}
###### Example
**(standard resolution)**

Consider the augmented [[cosimplicial object|cosimplicial]] which is the $\mathbb{S} \to E$-[[Amitsur complex]] [[smash product of spectra|smashed]] with $X$:

$$
  X \longrightarrow E \wedge X \stackrel{\longrightarrow}{\longrightarrow} E \wedge E \wedge X \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}
  E \wedge E \wedge E \wedge X
 \stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\stackrel{\longrightarrow}{\longrightarrow}}}
 \cdots
  \,.
$$

Its corresponding [[Moore complex]] (the sequence whose maps are the alternating sum of the above coface maps) is an $E$-Adams resolution, def. \ref{EAdamsResolution}.

=--

+-- {: .num_defn #EAdamsTower}
###### Definition

An _$E$-Adams tower_ of a spectrum $X$ is a [[commuting diagram]] in [[HoSpectra]] of the form

$$
  \array{
    && \vdots
    \\
    && \downarrow^{\mathrlap{p_2}}
    \\
    && X_2 &\stackrel{\kappa_2}{\longrightarrow}& \Omega^2 I_3
    \\
    &\nearrow& \downarrow^{\mathrlap{p_1}}
    \\
    && X_1 &\stackrel{\kappa_1}{\longrightarrow}& \Omega I_2
    \\
    &\nearrow& \downarrow^{\mathrlap{p_0}}
    \\
    X 
    &\underset{}{\longrightarrow}&
    X_0 = I_0
    &\stackrel{\kappa_0}{\longrightarrow}&
    I_1
  }
$$

such that 

1. each hook is a [[homotopy fiber sequence]];

1. the [[composition]] of the $(\Sigma \dashv \Omega)$-[[adjuncts]] of $\Sigma_{p_{n-1}}$ with $\Sigma^n \kappa_n$

   $$
     i_{n+1} \;\colon\; I_n \stackrel{\widetilde {\Sigma p_{n-1}}}{\longrightarrow}
     \Sigma^n X_n \stackrel{\Sigma^{n}\kappa_n}{\longrightarrow} I_{n+1}
   $$

   constitute an $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}:

   $$
     0 \to X \stackrel{i_0}{\to} I_0 \stackrel{i_2}{\to} I_2 \stackrel{}{\to} \cdots
     \,.
   $$

Call this the _associated $E$-Adams resolution_ of the $E$-Adams tower.

The _associated inverse sequence_ is ...

=--

+-- {: .num_remark}
###### Remark

In ([Ravenel 86](#Ravenel86)) it is is the associated inverse sequence that is called an $E$-Adams resolution.

=--
+-- {: .num_example}
###### Example

Every $E$-Adams resolution of $X$, def. \ref{EAdamsResolution}, induces an $E$-Adams tower, def. \ref{EAdamsTower} of which it is the associated $E$-Adams resolution.

=--

#### $E$-Adams spectral sequence

+-- {: .num_defn #EAdamsSpectralSequence}
###### Definition

Given an $E$-Adams tower as in  def. \ref{EAdamsTower}, the associated [[exact couple]] is

$$
  \array{
    \mathcal{D} && \stackrel{p}{\longrightarrow} &&  \mathcal{D}
    \\
    & {}_{\mathllap{\partial}}\nwarrow && \swarrow_{\mathrlap{\kappa}} 
    \\
    && \mathcal{E}    
  }
$$

with 

$$
  \mathcal{D} \coloneqq
  \oplus_{s,t} \mathcal{D}^{s,t}
  \coloneqq
  \oplus_{s,t} \pi_{t-s}(X_s)
$$

$$
  \mathcal{E} \coloneqq 
  \oplus_{s,t} \mathcal{E}^{s+1,t}
  \coloneqq
  \oplus_{s,t} \pi_{t-s}(\Omega^s I_{s+1})
$$

and

$$
  p \colon \pi_{t-s}(X_{s+1})\stackrel{\pi_{t-s}(p_s)}{\longrightarrow}
   X_{t-s}(X_s)
$$

$$
  \kappa \colon \pi_{t-s}(X_s)
  \stackrel{\pi_{t-s}(\kappa_s)}{\longrightarrow} \pi_{t-s}(\Omega^s I_{s+1})
$$

$$
  \partial \colon \pi_{t-s}(\Omega^s I_{s+1})
  \stackrel{\pi_{t-s}(\partial_s)}{\longrightarrow}
  \pi_{t-s}(\Sigma X_{s+1})
  \,.
$$

The $E$-Adams spectral sequence of the $E$-Adams tower is the [spectral sequence induced](exact+couple#SpectralSequencesFromExactCouples) by this exact couple.

=--

+-- {: .num_prop #UniquenessOfEAdamsSpectralSequence}
###### Proposition

Given two $E$-Adams towers, def. \ref{EAdamsTower}, for some $X$, then the corresponding two $E$-Adams spectral sequences, def. \ref{EAdamsSpectralSequence}, are [[isomorphism|isomorphic]] from the $\mathcal{E}_2$-page on

=--

Convergence

... $E$-ANSS [[converges conditionally]] to the [[E-nilpotent completion]]...


...([Ravenel 84](#Ravenel84))...


#### The $\mathcal{E}_1$-term and Hopf algebroid structure

Due to prop. \ref{UniquenessOfEAdamsSpectralSequence}
we may focus attention on the standard $E$-resolution, def. \ref{StandardEResolution}.

For this one gets

$$
  \mathcal{E}_1^{s,\bullet}
  \simeq
  \pi_\bullet(E^{\wedge (s+1)}\wedge X )
  \,.
$$

+-- {: .num_defn #FlatE}
###### Definition

Call the [[ring spectrum]] $E$ _flat_ if

$$
  \eta_L,\eta_R \colon E_\bullet \longrightarrow E_\bullet(E)
$$

is a [[flat morphism]].

=--

+-- {: .num_example}
###### Example

Examples of ring spectra that are flat according to def. \ref{FlatE} include

* $E = H \mathbb{F}_p$ an [[Eilenberg-MacLane spectrum]] with $mod\;p$ [[coefficients]];

* $E = B P$ the [[Brown-Peterson spectrum]];

* $E = MU$ the [[complex cobordism cohomology theory|complex cobordism spectrum]];

Examples of ring spectra that are _not_ flat include

* $E = H \mathbb{Z}$ the [[Eilenberg-MacLane spectrum]] for [[integers|integer]] [[coefficients]];

* $E = M S U$.

=--



+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, then
$(E_\bullet, E_\bullet(E))$ (the dual $E$-[[Steenrod operations]]) is canonically a [[Hopf algebroid]].

=--

([Baker-Lazarev 01, theorem 1.1](#BakerLazarev01))


+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, the canonical map

$$
  E_\bullet(E^{\wedge n}) \otimes_{\pi_\bullet} E_\bullet(X)
  \longrightarrow
  \pi_\bullet(E^{\wedge^{(n+1)}}\wedge X  )
$$

is an [[isomorphism]].

=--

#### The $\mathcal{E}_2$-term and homological algebra of Hopf modules

+-- {: .num_prop}
###### Proposition

For $E$ flat, def. \ref{FlatE}, then the $\mathcal{E}_2$-page
of any $E$-Adams spectral sequence over $X$ is

$$
  \mathcal{E}^{s,t}_\bullet
  \simeq
  Ext^{s,t}_{E_\bullet(E)}(E_\bullet, E_\bullet(X))
  \,,
$$

where $Ext^{s,t}_{\Gamma}(-,-)$ denotes the $t$th graded piece of the $s$-th [[Ext]]-functor in the category of $\Gamma$-[[comodules]].

=--





#### The case $E = H \mathbb{F}_p$ and $X = \mathbb{S}$

classical [[Adams spectral sequence]]...

(... [Hatcher 04](#Hatcher04), [Rognes 12](#Rognes12)... )

#### The case $E = H \mathbb{F}_p$ and $X = M U$

(...) [Adams 74, part II, around section 8 ](#Adams74), [Lurie 10, around lecture 9](Lurie10) (...)



#### Outlook: The case $E = M U$ and $X = \mathbb{S}$

(...) [[Adams-Novikov spectral sequence]] (...)

$\,$

***

$\,$

## Seminar: Complex oriented cohomology
 {#ComplexOrientedCohomology}

$\,$

+-- {: .standout}

<div style="float:left;margin:0 10px 10px 0;"> <img width="200" src="http://ncatlab.org/nlab/files/BonnLogo.png"> </div> 

[S4D2 -- Graduate Seminar on Topology](https://basis.uni-bonn.de/qisserver/rds?state=verpublish&status=init&vmfile=no&publishid=107560&moduleCall=webInfo&publishConfFile=webInfo&publishSubDir=veranstaltung)

$\;\;\;\;\;\;\;\;\;\;\;$ **Complex oriented cohomology**

$\;\;\;\;\;\;\;\;\;\;\;$ Dr. [[Urs Schreiber]]

$\;\;\;\;\;\;\;\;\;\;\;$ 

=---

**Abstract.** _The [[(infinity,1)-category|category]] of [[generalized cohomology theories]] equipped with a universal "[[complex oriented cohomology theory|complex]] [[orientation in generalized cohomology|orientation]]" happens to unify within it the abstract structure theory of [[stable homotopy theory]] with the concrete richness of the [[differential topology]] of [[cobordism theory]] and of the [[arithmetic geometry]] of [[formal group laws]] (of [[higher Jacobians]]), such as [[elliptic curves]]. In the seminar we work through classical results in [[algebraic topology]], organized such as to give in the end a first glimpse of the modern picture of [[chromatic homotopy theory]]._


### **Part S1) Generalized cohomology**

For instance ([Aguilar-Gitler-Prieto 02, chapters 7,8 and 12](#AguilarGitlerPrieto02)) and ([Malkiewich 11](#Malkiewich11)).

#### Generalized homology and cohomology functors
 {#GeneralizedHomologyAndCohomologyFunctors}

The concept that makes [[algebraic topology]] be about methods of [[homological algebra]] applied to [[topology]] is that of [[generalized homology]] [[generalized cohomology]]: [[covariant functors]] or [[contravariant functors]]

$$
  Top \longrightarrow Ab^{\mathbb{Z}}
$$

from (suitably nice) [[topological spaces]], such that some key properties of the [[homotopy types]] of topological spaces is preserved as one passes them to the more tractable [[category]] [[Ab]]${}^{\mathbb{Z}}$  of $\mathbb{Z}$-[[graded abelian groups]].

A [[generalized (Eilenberg-Steenrod) cohomology]] theory is such a contravariant functor which satisfies the key properties exhibited by [[ordinary cohomology]] (as computed for instance by [[singular cohomology]]), _except_ that its value on the point is not required to be concentrated in degree 0.

An important example of a generalised cohomology theory other than ordinary cohomology is [[topological K-theory]].


#### Brown representability theorem


(-- from here on we need the basics of [Part 1), Spectra](#Spectra) --)

Given any functor such as the generalized (co)homology functor [above](GeneralizedHomologyAndCohomologyFunctors), an important question to ask is whether it is a _[[representable functor]]_. Due to the $\mathbb{Z}$-grading and the [[suspension isomorphisms]], if a generalized (co)homology functor is representable at all, it must be represented by a $\mathbb{Z}$-indexed sequence of [[pointed topological spaces]] such that the [[reduced suspension]] of one is comparable to the next one in the list, hence it must be represented by a _[[spectrum]]_.

Whitehead observed that indeed every [[spectrum]] represents a generalized (co)homology theory.  The _[[Brown representability theorem]]_ states that, conversely, every generalized (co)homology theory is represented by a spectrum.

Due to [[phantom maps]], there remains a subtle difference between generalized (co)homology functors and the spectra which represent them: a little bit of information is lost as one passes from the spectrum to its cohomology functor (the [[Yoneda lemma]] does not quite apply here, since a spectrum is more than just one (homotopy type of a) topological space).

In applications and modern theory, it is mostly the spectra that matter, and hence the Brown representability theory is used to transfer extra structure on spectra to extra structure on cohomology theories.

For instance a _[[multiplicative cohomology theory]]_ is one which is represented by a [[ring spectrum]].

#### Atiyah-Hirzebruch spectral sequence

(-- from here on we need the basics of [Part 1) Spectral sequences](#SpectralSequences) --)

Given a [[generalized cohomology theory]] $E$, there is a [[spectral sequence]] known as the _[[Atiyah-Hirzebruch spectral sequence]]_ which serves to compute $E$-cohomology of any space $X$ in terms of [[ordinary cohomology]] with [[coefficients]] in $E_\bullet(\ast)$.

### **Part S2) Cobordism theory**

For instance ([Malkiewich 11](#Malkiewich11)).

As one passes from [[abelian groups]] to [[spectra]], a miracle happens: even though the latter are just the proper embodiment of [[linear algebra]] in the context of [[homotopy theory]] ("[[higher algebra]]") their inspection reveals that spectra natively know about deep phenomena of [[differential topology]], [[index theory]] and in fact [[string theory]] (for instance via a close relation between _[[genera and partition functions - table|genera and partition functions]]_). 

The strongest manifestation of this comes about in [[complex oriented cohomology theory]]/[[chromatic homotopy theory]] that we eventually come to [below](#ComplexOrientedCohomologyTheory), which higher linear algebra over the complex Thom spectrum [[MU]]. 

Here we first concentrate on its real avatar, the [[Thom spectrum]] [[MO]]. The seminal result of [[Thom's theorem]] says that the [[homotopy groups of a spectrum|homotopy groups]] of [[MO]] form the [[cobordism ring]] of [[cobordism]]-[[equivalence classes]] of [[manifolds]]. In the course of discussing this _[[cobordism theory]]_ one encounters various phenomena whose complex version also governs the complex oriented cohomology theory that we are interested in [below](#ComplexOrientedCohomologyTheory).



#### Thom spectra

* [[Thom spectrum]], [[MO]]

  [[Thom space]]

  [[Pontrjagin-Thom collapse map]]

#### Thom's theorem

* [[Thom's theorem]]

  [[cobordism]], [[cobordism ring]]

#### Thom isomorphism
 {#ThomIsomorphism}

* [[Thom isomorphism]] (in [[ordinary cohomology]])

  [[cup product]] 

  [[Leray-Hirsch theorem]]

  [[Thom class]]

  [[fiber integration]]


#### Orientation and Fiber integration
 {#OrientationAndFiberIntegration}


From the way the [[Thom isomorphism]] via a [[Thom class]] works in [[ordinary cohomology]] (as [above](#ThomIsomorphism)), one sees what the general concept of [[orientation in generalized cohomology]] ought to be.

use ([Adams 74, part III, section 10](#Adams74) [Lurie 10, lecture 5](#Lurie10))

[[orientation in generalized cohomology]]

* [[fiber integration in generalized cohomology]]


### **Part S3) Complex oriented cohomology**
 {#ComplexOrientedCohomologyTheory}

Use ([Adams 74, Part I, Part II](#Adams74), [Lurie 10, lectures 1-16](#Lurie10)).


#### Complex oriented cohomology

(-- from here on we need the basics of [Part 1), Ring spectra](#RingSpectra) --)

Given the concept of [[orientation in generalized cohomology]] as [above](#OrientationAndFiberIntegration), it is clearly of interest to consider [[cohomology theories]] $E$ such that there exists an orientation/[[Thom class]] on the [[associated bundle|associated]] [[vector bundle]] over any [[classifying space]] $B G$ (or rather: on its induced [[spherical fibration]]), for then _all_ $G$-associated vector bundles inherit an orientation.

Considering this for $G = U(n)$ the [[unitary groups]], for all $n \in \mathbb{N}$, with their defining $\mathbb{C}$-[[linear representations]] on $\mathbb{C}^n \simeq_{\mathbb{R}} \mathbb{R}^2 n$ yields the concept of _[[complex oriented cohomology theory]]_. 

It turns out that a complex orientation on a generalized cohomology theory $E$ in this sense is already given by demanding that there is a suitable generalization of the [[first Chern class]] of [[complex line bundles]] in $E$-cohomology. This already implies the existence of [[generalized Chern classes]] of all degrees $2n$, and these are the required universal generalized [[Thom classes]] ([Lurie 10, lecture 5, prop. 6](#Lurie10)).

Where the ordinary [[first Chern class]] in [[ordinary cohomology]] is simply additive under [[tensor product]] of [[complex line bundles]], one finds that the composite of generalized first Chern classes is instead governed by more general commutative [[formal group laws]]. This phenomenon governs much of the theory to follow.

* [[complex oriented cohomology theory]]

  * [[splitting principle]]

  * [[generalized Chern classes]]

  * [[formal group laws]]

#### Lazard's theorem
 {#LazardTheorem}

* [[Lazard's theorem]]

  * [[Lazard ring]]

#### Complex cobordism cohomology

(-- from here on we need basics from [Part 1), Examples](#Examples) --)

* [[complex cobordism cohomology]]

  * [[MU]]

* [[universal complex orientation on MU]]

#### Homology of $M U$

* [[homology of MU]]

#### Quillen's theorem on $M U$

* [[Quillen's theorem on MU]]

#### Landweber exact functor theorem

* [[Landweber exact functor theorem]]


### Outlook: Geometry of $Spec(MU)$

Use ([Lurie 10, lectures 12-14](#Lurie10))

(-- from here on we need basics of [Part 1), Localization](#Localization) --)

* [[moduli space of formal groups]]

  * [[height of a formal group]]

  * [[moduli space of elliptic curves]]

* [[Landweber-Novikov theorem]]

* [[Adams-Quillen theorem]]

$\,$

***

$\,$

## References
 {#References}

### Basic

For section **1) Stable homotopy theory** we follow ([Adams 74, part III sections 2-7](#Adams74)) and

* {#Malkiewich14} [[Cary Malkiewich]], _The stable homotopy category_, 2014 ([pdf](http://math.uiuc.edu/~cmalkiew/stable.pdf)).


For **2) Adams spectral sequence** we follow ([Hopkins 99, section 5](#Hopkins99)) as worked out in

* {#Aramian} [[Nersés Aramian]], _The Adams spectral sequence_ ([[AramianANSS.pdf:file]])


For **S1) Generalized cohomology** a neat account is in:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, section 12 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* {#Malkiewich11} [[Cary Malkiewich]], _Unoriented cobordism and $M O$_, 2011 ([pdf](http://math.uiuc.edu/~cmalkiew/cobordism.pdf))
 
For **S2) Complex oriented cohomology** we follow

* {#Adams74} [[Frank Adams]], parts I and II of _[[Stable homotopy and generalized homology]]_, Chicago Lectures in mathematics, 1974

* {#Lurie10} [[Jacob Lurie]], lectures 1-16 of _[[Chromatic Homotopy Theory]]_, 2010

(These overlap. [Lurie 10](#Lurie10) at some point invokes [[A-∞ rings]] where [Adams 74](#Adams74) sticks with [[ring spectra]]. )

### Further reading

For further reading on stable homotopy theory an excellent collection is

* {#James95} [[Ioan Mackenzie James]], _[[Handbook of Algebraic Topology]]_ 1995

The modern chromatic picture originates around

* {#Hopkins99} [[Mike Hopkins]], _[[Complex oriented cohomology theories and the language of stacks]]_, 1999 

a useful survey is in

* {#Wilson13} [[Dylan Wilson]] section 1.2 of _Spectral Sequences from Sequences of Spectra: Towards the Spectrum of the Category of Spectra_ lecture at _[2013 Pre-Talbot Seminar](http://math.harvard.edu/~hirolee/pretalbot2013/)_, March 2013 ([[DylanWilsonOnANSS.pdf:file]])

Further useful lecture notes include

* {#Hatcher04} [[Alan Hatcher]], _[Spectral sequences in algebraic topology](http://www.math.cornell.edu/~hatcher/SSAT/SSATpage.html)_ _II: The Adams spectral sequence_, 2004 ([pdf](http://www.math.cornell.edu/~hatcher/SSAT/SSch2.pdf))

* {#Bauer11} [[Tilman Bauer]], _Bousfield localization and the Hasse square_, 2011  ([pdf](http://math.mit.edu/conferences/talbot/2007/tmfproc/Chapter09/bauer.pdf))

* {#Rognes12} [[John Rognes]], _The Adams spectral sequence_ (following [Bruner](#Bruner)), 2012 ([pdf](http://folk.uio.no/rognes/papers/notes.050612.pdf))

And last not least, there is

* {#Ravenel86} [[Doug Ravenel]], _[[Complex cobordism and stable homotopy groups of spheres]]_, 1987/2003 ([pdf](http://www.math.rochester.edu/people/faculty/doug/mybooks/ravenelA1.pdf))


[[!redirects geometry of physics -- stable homotopy types]]