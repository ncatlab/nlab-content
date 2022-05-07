
{:principle: .un_remark style="border:solid #0000cc;background: #add8e6;border-width:2px 1px;padding:0 1em;margin:0 1em;"}





***

This page is an introduction to basic [[topological homotopy theory|topological]] [[homotopy theory]].
We introduce the concept of [[homotopy]] between [[continuous functions]] and the induced concept
of [[homotopy equivalence]] of [[topological spaces]].
Homotopy classes of paths form the _[[fundamental groupoid]]_ of a topological space, the 
first step in extracting combinatorial data in homotopy theory. We use this example to introduce
[[groupoids]] and their [[homotopy theory]] in general and mention that this models the homotopy theory
of those topological spaces that are [[homotopy 1-types]]. Then we discuss the concept of [[covering spaces]]
and use groupoids to give a simple proof of the [[fundamental theorem of covering spaces]], which says that these  are equivalent
to permutation representations of the fundamental groupoid.  This is
a simple topological version of the general principle of _[[Galois theory]]_ and has many
applications. As one example application, we use it to prove that the [[fundamental group of the circle is the integers]].


$\,$

main page: _[[Introduction to Topology]]_

previous chapter: _[[Introduction to Topology -- 1|Introduction to Topology 1 -- Point-set topology]]_

this chapter: **Introduction to Topology 2 -- Basic Homotopy Theory**

$\,$

For introduction to more general and abstract _[[homotopy theory]]_ see instead
at _[[Introduction to Homotopy Theory]]_.



***

$\,$

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--


#Basic Homotopy Theory#
* table of contents
{:toc}


$\,$

In order to handle topological spaces, to compute their properties and to distinguish them, it
turns out to be useful to consider not just continuous variation within a topological space, i.e.
[[continuous functions]] between topological spaces, but also continuous deformations of [[continuous functions]] themselves.
This is the concept of _[[homotopy]]_ (def. \ref{LeftHomotopy} below), and its study is called _[[homotopy theory]]_.
If one regards topological spaces with [[homotopy classes]] of continuous functions between them
then their nature changes, and one speaks of _[[homotopy types]]_ (remark \ref{IsomorphismHomotopyEquivalence} below).

Of particular interest are homotopies between [[paths]] in a topological space. If a [[loop]]
in a topological space is homotopic to the constant loop, this means that it does not "wind around a hole"
in the space. Hence the set of homotopy classes of loops in a topological space, which is a [[group]]
under [[concatenation of paths]], detects crucial information about the global structure of the space,
and hence is called the _[[fundamental group]]_ of the space (def. \ref{FundamentalGroupoidAndFundamentalGroup}).

This same information turns out to be encoded in "continuously varying sets" over a topological
space, hence in "[[bundles]] of [[sets]]", called _[[covering spaces]]_ (def. \ref{CoveringSpace} below).
As one moves around a loop, then the parameterized set comes back to itself up to a [[bijection]]
called the _[[monodromy]]_ of the loop. This encodes an _[[action]]_ or _[[permutation representation]]_ of the fundamental group. The
_[[fundamental theorem of covering spaces]]_ (prop. \ref{FundamentalTheoremOfCoveringSpaces} below)
says  that covering spaces are equivalently characterized by their [[monodromy]] [[representation]]
of the fundamental group. This is an incarnation of the general principle of _[[Galois theory]]_
in [[topological homotopy theory]]. Sometimes this allows to compute fundamental groups
from behaviour of covering spaces, for instance it allows to prove that the [[fundamental group of the circle is the integers]]
(prop. \ref{CircleFundamentalGroup} below).

In order to formulate and prove these statements, it turns out convenient to do away
with the arbitrary choice of basepoint that is involved in the definition of fundamental
groups, and instead collect _all_ homotopy classes of paths into a single structure,
called the _[[fundamental groupoid]]_ of a topological space (example \ref{FundamentalGroupoid} below)
an example of a generalization of groups to _[[groupoids]]_ (discussed [below](#Groupoid)).
The fundamental groupoid may be regarded as an [[algebra|algebraic]] incarnation of the
[[homotopy type]] presented by a topological space, _up to level 1_ (the _[[homotopy 1-type]]_).

The algebraic reflection of the full [[homotopy type]] of a topological space involves
higher dimensional analogs fo the [[fundamental group]] called the _higher [[homotopy groups]]_.
We close with an outlook on these [below](#HigherHomotopyGroups).


$\,$


## Homotopy
  {#Homotopy}

It is clear that for $n \geq 1$ the [[Euclidean space]] $\mathbb{R}^n$ or equivalently the [[open ball]] $B_0^\circ(1)$ in $\mathbb{R}^n$
is _not_ [[homeomorphic]] to the [[point space]] $\ast = \mathbb{R}^0$ (simply because there is not even a [[bijection]] between the
underlying [[sets]]). Nevertheless, intuitively the $n$-ball is a "continuous deformation" of the point, obtained as the radius of the $n$-ball tends to zero.

This intuition is made precise by observing that there is a [[continuous function]] out of the [[product topological space]]
([this example](Introduction+to+Topology+--+1#BinaryProductTopologicalSpace)) of the open ball with the [[closed interval]]

$$
  \eta \colon [0,1] \times B_0^\circ(1)  \longrightarrow B_0^\circ(1)
$$

which is given by rescaling:

$$
  (t,x) \mapsto t \cdot x
  \,.
$$

This continuously interpolates between the open ball and the point, in that for $t = 1$ it restricts to the identity, while for $t = 0$ it restricts to the map constant on the origin.


We may summarize this situation by saying that there is a
[[diagram]] of [[continuous functions]] of the form

$$
  \array{
    B_0^\circ(1) \times \{0\} &\overset{\exists !}{\longrightarrow}& \ast
    \\
    \downarrow & & \downarrow^{\mathrlap{const_0}}
    \\
    [0,1] \times B_0^\circ(1)
    &\overset{(t,x) \mapsto t \cdot x}{\longrightarrow}&
    B^\circ_0(1)
    \\
    \uparrow & \nearrow_{\simeq}
    \\
    B_0^\circ(1) \times \{1\}
  }
$$

Such "continuous deformations" are called _[[homotopies]]_:

In the following we use this terminlogy:

+-- {: .num_defn #TopologicalInterval}
###### Definition
**([[topological interval]])

The _[[topological interval]]_ is

1. the [[closed interval]] $[0,1] \subset \mathbb{R}^1$
   regarded as a [[topological space]] in the standard way, as a [[subspace]] of the [[real line]] with its [[Euclidean space|Euclidean]] [[metric topology]],

1. equipped with the [[continuous functions]]

   1. $const_0 \;\colon\; \ast \to [0,1]$

   1. $const_1 \;\colon\; \ast \to [0,1]$

   which include the [[point space]] as the two endpoints, respectively

1. equipped with the (unique) [[continuous function]]

   $$
     [0,1] \overset{}{\longrightarrow} \ast
   $$

   to the [[point space]] (which is the [[terminal object]] in [[Top]])

regarded, in summary, as a factorization

$$
  \nabla_\ast
    \;\colon\;
  \ast \sqcup \ast
    \overset{(const_0,const_1)}{\longrightarrow}
  [0,1]
    \overset{}{\longrightarrow}
  \ast
$$

of the [[codiagonal]] on the point space, namely the unique continuous function $\nabla_\ast$
out of the [[disjoint union space]] $\ast \sqcup \ast \simeq Disc(\{0,1\})$
([[homeomorphism|homeomorphic]] to the [[discrete topological space]] on two elements).

=--



+-- {: .num_defn #LeftHomotopy}
###### Definition
**([[homotopy]])**

Let $X,Y \in $ [[Top]] be two [[topological spaces]] and let

$$
  f,g\colon X \longrightarrow Y
$$

be two [[continuous functions]] between them.

A _[[left homotopy|(left)]] [[homotopy]]_ from $f$ to $g$, to be denoted

$$
  \eta \;\colon\; f \,\Rightarrow\, g
  \,,
$$

is a [[continuous function]]

$$
  \eta \;\colon\; X \times [0,1] \longrightarrow Y
$$

out of the [[product topological space]] ([this example](Introduction+to+Topology+--+1#BinaryProductTopologicalSpace))
of $X$ the [[topological interval]] (def. \ref{TopologicalInterval})
such that this makes the following  [[diagram]] in [[Top]] [[commuting diagram|commute]]:

<div style="float:right;margin:0 10px 10px 0;">
<img src="http://www.ncatlab.org/nlab/files/AHomotopy.jpg" width="400">
</div>


$$
  \array{
     {0} \times X
     \\
     {}^{\mathllap{(id,const_0)}}\downarrow & \searrow^{\mathrlap{f}}
     \\
     X \times [0,1]  &\stackrel{\eta}{\longrightarrow}& Y
     \\
     {}^{\mathllap{(id,const_1)}}\uparrow & \nearrow_{\mathrlap{g}}
     \\
     \{1\} \times X
  }
  \,.
$$

> graphics grabbed from J. Tauber [here](http://jtauber.com/blog/2005/07/01/path_homotopy/)

hence such that

$$
  \eta(-,0) = f
  \phantom{AAA}
  \text{and}
  \phantom{AAA}
  \eta(-,1) = g
  \,.
$$

If there is a homotopy $f \Rightarrow g$ (possibly unspecified)
we say that $f$ is _homotopic_ to $g$, denoted

$$
  f \sim_h g
  \,.
$$

=--


+-- {: .num_prop #EquivRelHomotopy}
###### Proposition
**([[homotopy]] is an [[equivalence relation]])

Let $X,Y \in $ [[Top]] be two [[topological spaces]].
Write $Hom_{Top}(X,Y)$ for the [[set]] of [[continuous functions]]
from $X$ to $Y$.

Then the relating of being [[homotopy|homotopic]] (def. \ref{LeftHomotopy}) is an [[equivalence relation]]
on this set. The correspnding [[quotient set]]

$$
  [X,Y] \; \coloneqq \; Hom_{Top}(X,Y)/\sim_h
$$

is called the set of _[[homotopy classes]]_ of continuous functions.

Moreover, this equivalence relation is compatible with [[composition]] of continuous functions:

For $X,Y,Z \in $ [[Top]] three topological spaces, there is a unique function


$$
  [X,Y] \times [Y,Z] \longrightarrow [X,Z]
$$

such that the following [[commuting diagram|diagram commutes]]:

$$
  \array{
    Hom_{Top}(X,Y) \times Hom_{Top}(Y,Z)
      &\overset{\circ_{X,Y,Z}}{\longrightarrow}&
    Hom_{Top}(X,Z)
    \\
    \downarrow && \downarrow^{\mathrlap{}}
    \\
    [X,Y] \times [Y,Z] &\longrightarrow& [X,Z]
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

To see that the relation is [[reflexive relation|reflexive]]: A homotopy $f \Rightarrow f$ from a function $f$ to itself is given by
the function which is constant on the topological interval:

$$
  X \times [0,1] \overset{pr_1}{\longrightarrow} X
  \,.
$$

This is continuous becaue [[projections]] out of [[product topological spaces]] are continuous, by
the [[universal property]] of the [[Cartesian product]].

To see that the relation is [[symmetric relation|symmetric]]: If $\eta \colon f \Rightarrow g$ is a homotopy then

$$
  \array{
    X \times [0,1] &\overset{id_X \times (1-(-))}{\longrightarrow}& X \times [0,1] &\overset{\eta}{\longrightarrow}& X
    \\
    (x,t) &\mapsto& (x,1-t) &\mapsto&  \eta(x,1-t)
  }
$$

is a homotopy $g \Rightarrow f$. This is continuous because $1-(-)$ is a [[polynomial]] function, and
[[polynomials are continuous]], and because [[Cartesian product]] and [[composition]] of continuous functions
is again continuous.

Finally to see that the relation is [[transitive relation|transitive]]: If $\eta_1 \colon f \Rightarrow g$
and $\eta_2 \colon g \Rightarrow h$ are two composable homotopies, then consider the "$X$-parameterized
[[path concatenation]]"

$$
  \array{
    X \times [0,1] &\overset{\eta_2 \circ \eta_1}{\longrightarrow}& X
    \\
    (x,t) &\mapsto&
    \left\{
      \array{
         \eta_1(x,2t) &\vert& t \leq 1/2
         \\
         \eta_{2}(x,2t-1) &\vert& t \leq 1/2
      }
    \right.
  }
  \,.
$$

To see that this is continuous, observe that $\{ X \times [0,1/2] \subset X, X \times [1/2,1] \subset X \}$
is a [[cover]] of $X \times [0,1]$ by [[closed subsets]] (in the [[product topology]]) and
because $\eta_1(-,2(-))$ and $\eta_2(-,2(-)-1)$ are continuous (being composites of
Cartesian products of continuous functions) and agree on the intersection $X \times \{1/2\}$. Hence
the continuity follows by [this example](Top#ClosedSubspacesGluing).

Finally to see that homotopy respects composition: Let

$$
  \array{
    X
      \overset{f_1}{\longrightarrow}
    Y
      \underoverset
        {\underset{f'_2}{\longrightarrow}}
        {\overset{f_2}{\longrightarrow}}
        {}
    Z
     \overset{f_3}{\longrightarrow}
    W
  }
$$

be continuous functions, and let

$$
  \eta \;\colon\; f_2 \Rightarrow f'_2
$$

be a homotopy. It is sufficient to show that then there is a homotopy of the form

$$
  f_3 \circ f_2 \circ f_1 \Rightarrow   f_3 \circ f'_2 \circ f_1
  \,.
$$

This is exhibited by the following diagram

$$
  \array{
     X &\overset{f_1}{\longrightarrow}& Y
     \\
     {}^{\mathllap{ (id_X, const_0) }}\downarrow
       &&
     {}^{\mathllap{ (id_Y,const_0) }}\downarrow
       &
     \searrow^{\mathrlap{ f_2}}
     \\
     X \times [0,1]
       &\overset{f_1 \times id_{[0,1]} }{\longrightarrow}&
     Y \times [0,1]
       &\stackrel{\eta}{\longrightarrow}&
     Z &\overset{f_3}{\longrightarrow}& W
     \\
     {}^{\mathllap{(id_X,  const_1)}}\uparrow
       &&
     {}^{\mathllap{ (id,const_1) } }\uparrow
       &
     \nearrow_{\mathrlap{ f'_2 }}
     \\
     X &\underset{f_1}{\longrightarrow}& Y
  }
  \,.
$$

=--

+-- {: .num_remark #HomotopyCategory}
###### Remark
**([[homotopy category]])**

Prop. \ref{EquivRelHomotopy} means that [[homotopy classes]] of [[continuous functions]]
are the [[morphisms]] in a [[category]] whose [[objects]] are still the [[topological spaces]].

This category (at least when restricted to spaces that admit the structure of [[CW-complexes]])
is called the _[[classical homotopy category]]_, often denoted

$$
  Ho(Top)
  \,.
$$

Hence for $X,Y$ topological spaces, then

$$
  Hom_{Ho(Top)}(X,Y) = [X,Y]
$$

Moreover, sending a continuous function to its homotopy class is a [[functor]]

$$
  \kappa \;\colon\; Top \longrightarrow Ho(Top)
$$

from the ordinary category [[Top]] of topological spaces with actual continuous functions between them.

=--




+-- {: .num_defn #HomotopyEquivalence}
###### Definition
**([[homotopy equivalence]])**

Let $X,Y \in $ [[Top]] be two [[topological spaces]].

A [[continuous function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

is called a _[[homotopy equivalence]]_ if there exists

1. a continuous function the other way around,

   $$
     g \;\colon\; Y \longrightarrow X
   $$

1. [[homotopies]] (def. \ref{LeftHomotopy}) from the two composites to the respective [[identity function]]:

  $$
    f\circ g \Rightarrow id_Y
  $$

  and

  $$
    g\circ f \Rightarrow id_X
    \,.
  $$

We indicate that a continuous function is a homotopy equivalence by writing

$$
  X \overset{\simeq_h}{\longrightarrow} Y
  \,.
$$

If there exists _some_ (possibly unspecified) homotopy equivalence between topological spaces $X$ and $Y$ we write

$$
  X \simeq_h Y
  \,.
$$

=--

+-- {: .num_remark #IsomorphismHomotopyEquivalence}
###### Remark
**([[homotopy equivalences]] are the [[isomorphisms]] in the [[homotopy category]])**

In view of remark \ref{HomotopyCategory} a continuous function $f$ is
a homotopy equivalence precisely if its image $\kappa(f)$ in the
[[homotopy category]] is an [[isomorphism]].

As an object of the [[homotopy category]], a topoogical space is often referred to
as a ([[strong homotopy type|strong]]) [[homotopy type]]. Homotopy types
have a different nature than the [[topological spaces]] which _present_ them,
in that topological spaces that are far from being [[homeomorphism|homeomorphic]]
may still be equivalent as homotopy types.


=--


+-- {: .num_example #HomotopyEquivalenceHomeomorphism}
###### Example
**([[homeomorphism]] is [[homotopy equivalence]])

Every [[homeomorphism]] is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}).

=--

+-- {: .num_prop}
###### Proposition
**([[homotopy equivalence]] is [[equivalence relation]])

Being [[homotopy equivalence|homotopy equivalent]] is an [[equivalence relation]]
on the [[class]] of [[topological spaces]].

=--

+-- {: .proof}
###### Proof

This is immediate from remark \ref{IsomorphismHomotopyEquivalence} by general
properties of [[categories]] and [[functors]].

But for the record we spell it out. This involves the construction already used in the proof
of prop. \ref{EquivRelHomotopy}:

It is clear that the relation it [[reflexive relation|reflexive]] and [[symmetric relation|symmetric]].
To see that it is [[transitive relation|transitive]] consider continuous functions


$$
  X
    \underoverset
      {\underset{g_1}{\longleftarrow}}
      {\overset{f_1}{\longrightarrow}}
      {}
  Y
   \underoverset
     {\underset{g_2}{\longleftarrow}}
     {\overset{f_2}{\longrightarrow}}
     {}
   Z
$$

and homotopies

$$
  g_1 \circ f_1 \Rightarrow id_X
  \phantom{AAAA}
  f_1 \circ g_1 \Rightarrow id_Y
$$

$$
  g_2 \circ f_2 \Rightarrow id_Y
  \phantom{AAAA}
  f_2 \circ g_2 \Rightarrow id_Z
  \,.
$$

We need to produce homotopies of the form

$$
  (g_1 \circ g_2 ) \circ (f_2 \circ f_1) \Rightarrow id_X
$$

and

$$
  (f_2 \circ f_1)  \circ (g_1 \circ g_2 )  \Rightarrow id_Y
  \,.
$$

Now the diagram

$$
  \array{
     X &\overset{f_1}{\longrightarrow}& Y
     \\
     {}^{\mathllap{ (id_X, const_0) }}\downarrow && {}^{\mathllap{(id_Y,const_0)}}\downarrow & \searrow^{\mathrlap{ g_2 \circ f_2}}
     \\
     X \times [0,1] &\overset{f_1 \times id_{[0,1]} }{\longrightarrow}& Y \times [0,1]  &\stackrel{\eta}{\longrightarrow}& Y &\overset{g_1}{\longrightarrow}& X
     \\
     {}^{\mathllap{(id_X,  const_1)}}\uparrow && {}^{\mathllap{(id,const_1)}}\uparrow & \nearrow_{\mathrlap{ id_Y }}
     \\
     X &\underset{f_1}{\longrightarrow}& Y
  }
  \,,
$$

with $\eta$ one of the given homotopies,
exhibits a homotopy $ (g_1\circ g_2) \circ (f_2 \circ f_1) \Rightarrow g_1 \circ f_1$. Composing this with the
given homotopy $g_1 \circ f_1 \Rightarrow id_X$ gives the first of the two homotopies required above.
The second one follows by the same construction, just with the lables of the functions exchanged.

=--

+-- {: .num_defn #SpaceContractible}
###### Definition
**([[contractible topological space]])**

A [[topological space]] $X$ is called _[[contractible topological space|contractible]]_
if the unique [[continuous function]] to the [[point space]]

$$
  X \overset{\simeq_h}{\longrightarrow} \ast
$$

is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}).

=--

+-- {: .num_remark}
###### Remark
**([[contractible topological spaces]] are the [[terminal objects]] in the [[homotopy category]])**

In view of remark \ref{HomotopyCategory}, a topological space $X$ is [[contractible topological space|contractible]]
(def. \ref{SpaceContractible}) precisely if its image $\kappa(X)$ in the [[classical homotopy category]]
is a [[terminal object]].

=--

+-- {: .num_example #BallIsContractible}
###### Example
**([[closed ball]] and [[Euclidean space]] are [[contractible topological space|contractible]])**

Let $B^n \subset \mathbb{R}^n$ be the unit [[open ball]] or [[closed ball]] in [[Euclidean space]].
This is [[contractible topological space|contractible]] (def. \ref{SpaceContractible}):

$$
  p \;\colon\; B^n \overset{\simeq_h}{\longrightarrow} \ast
  \,.
$$

The homotopy inverse function is necessarily constant on a point, we may just as well choose it
to go pick the origin:

$$
  const_0 \;\colon\; \ast \overset{}{\longrightarrow} B^n
  \,.
$$

For one way of composing these functions we have the [[equality]]

$$
  p \circ const_0 = id_\ast
$$

with the [[identity function]]. This is a homotopy by prop. \ref{EquivRelHomotopy}.

The other composite is

$$
  const_0 \circ p = const_0 \;\colon\; B^n \overset{}{\longrightarrow} B^n
  \,.
$$

Hence we need to produce a homotopy

$$
  const_0 \Rightarrow id_{B^n}
$$

This is given by the function

$$
  \array{
    B^n \times [0,1] &\overset{\eta}{\longrightarrow}& B^n
    \\
    (x,t) &\mapsto& t x
  }
  \,,
$$

where on the right we use the multiplication with respect to the standard [[real vector space]]
structure in $\mathbb{R}^n$.


Since the [[open ball]] is [[homeomorphism|homeomorphic]] to the whole [[Cartesian space]] $\mathbb{R}^n$
([this example](Introduction+to+Topology+--+1#OpenBallsHomeomorphicToRn)) it follows with
example \ref{HomotopyEquivalenceHomeomorphism} and example \ref{EquivRelHomotopy}
that also $\mathbb{R}^n$ is a contractible topological space:

$$
  \mathbb{R}^n \overset{\simeq_h}{\longrightarrow} \ast
  \,.
$$


=--

In direct generalization of the construction in example \ref{BallIsContractible}
one finds further examples as follows:

+-- {: .num_example}
###### Example

The following three [[graphs]]

<img src="https://ncatlab.org/nlab/files/ThreeNonHomeoButHomotopyEquivGraphs.png" width="400">

(i.e. the evident [[topological subspaces]] of the [[plane]] $\mathbb{R}^2$ that these pictures indicate) are not [[homeomorphic]]. But they are [[homotopy equivalence|homotopy equivalent]], in fact they are each homotopy equivalent to the [[disk]] with two points removed, by the homotopies indicated by the following pictures:

<img src="https://ncatlab.org/nlab/files/HomotopyEquivalentsToBiAnnulus.png" width="400">


> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)

=--


$\,$

###  Fundamental group
 {#FundamentalGroups}

+-- {: .num_defn #PathHomotopyRelativeBoundary}
###### Definition
**([[homotopy relative boundary]])**

Let $X$ be a [[topological space]] and let

$$
  \gamma_1, \gamma_2 \;\colon\; [0,1] \longrightarrow X
$$

be two [[paths]] in $X$, i.e. two [[continuous functions]] from the [[closed interval]] to $X$,
such that their endpoints agree:

$$
  \gamma_1(0) = \gamma_2(0)
  \phantom{AAAA}
  \gamma_1(1) = \gamma_2(1)
  \,.
$$

Then a [[homotopy relative boundary]] from $\gamma_1$ to $\gamma_2$ is a [[homotopy]] (def. \ref{LeftHomotopy})

$$
  \eta \;\colon\; \gamma_1 \Rightarrow \gamma_2
$$

such that it does not move the endpoints:

$$
  \eta(0,-) = const_{\gamma_1(0)} = const_{\gamma_2(0)}
  \phantom{AAAAAA}
  \eta(1,-) = const_{\gamma_1(0)} = const_{\gamma_2(1)}
  \,.
$$

=--

+-- {: .num_prop #EquivalenceRelationHomotopyRelativeBoundary}
###### Proposition
**([[homotopy relative boundary]] is [[equivalence relation]] on sets of [[paths]])**

Let $X$ be a [[topological space]] and let $x, y \in X$ be two points. Write

$$
  P_{x,y} X
$$

for the set of [[paths]] $\gamma$ in $X$ with $\gamma(0) = x$ and $\gamma(1) = y$.

Then [[homotopy relative boundary]] (def. \ref{PathHomotopyRelativeBoundary})
is an [[equivalence relation]] on $P_{x,y}X$.

The corresponding set of [[equivalence classes]] is denoted

$$
  Hom_{\Pi_1(X)}(x,y)
  \;\coloneqq\;
  (P_{x,y}X)/\sim
  \,.
$$

=--


Recall the operations on [[paths]]: [[path concatenation]] $\gamma_2 \cdot \gamma_1$, [[path reversion]] $\overline{\gamma}$ and [[constant paths]]

+-- {: .num_prop #ConcatenationOfHomotopyClassesOfPaths}
###### Proposition
**([[path concatenation|concatenation]] of [[homotopy relative boundary]]-classes of [[paths]])**

For $X$ a [[topological space]], then  the operation of [[path concatenation]] descends to [[homotopy relative boundary]]
[[equivalence classes]], so that for all $x,y, z \in X$ there is a function

$$
  \array{
    Hom_{\Pi_1(X)}(x,y)
     \times
    Hom_{\Pi_1(X)}(y,z)
      & \longrightarrow &
    Hom_{\Pi_1(X)}(x,z)
    \\
     ([\gamma_1], [\gamma_2])
    &\mapsto&
    [\gamma_2] \cdot [\gamma_1] \coloneqq  [\gamma_2 \cdot \gamma_1]
  }
  \,.
$$

Moreover,

1. this composition operation is [[associativity|associative]] in that for all $x,y,z,w \in X$
   and $[\gamma_1] \in Hom_{\Pi_1(X)}(x,y)$, $[\gamma_2] \in Hom_{\Pi_1(X)}(y,z)$ and $[\gamma_3] \in Hom_{\Pi_1(X)})(z,w)$
   then

   $$
     [\gamma_3] \cdot ([\gamma_2]\cdot [\gamma_1])
     \;=\;
     ([\gamma_3] \cdot [\gamma_2]) \cdot [\gamma_1]
   $$

1. this composition operation is [[unitality|unital]] with [[neutral elements]] the [[constant paths]] in that for all $x,y \in X$
   and $[\gamma] \in Hom_{\Pi_1(X)}(x,y)$ we have

   $$
     [const_y] \cdot [\gamma] = [\gamma] = [\gamma] \cdot [const_x]
     \,.
   $$

1. this composition operation has [[inverse elements]] given by [[path reversal]] in that for all $x, y \in X$
   and $[\gamma] \in Hom_{\Pi_1(X)}(x,y)$ we have

   $$
     [\overline{\gamma}] \cdot[\gamma] = [const_x]
     \phantom{AAAA}
     [\gamma] \cdot [\overline{\gamma}] = [const_y]
     \,.
   $$

=--


+-- {: .num_defn #FundamentalGroupoidAndFundamentalGroup}
###### Definition
**([[fundamental groupoid]] and [[fundamental groups]])**

Let $X$ be a [[topological space]]. Then set of points of $X$ together with the sets $Hom_{\Pi_1(X)}(x,y)$
of [[homotopy relative boundary]]-classes of [[paths]] (def. \ref{PathHomotopyRelativeBoundary}) for all points of points
and equipped with the concatenation operation from prop. \ref{ConcatenationOfHomotopyClassesOfPaths}
is called the _[[fundamental groupoid]]_ of $X$, denoted

$$
  \Pi_1(X)
  \,.
$$

Given a choice of point $x \in X$, then one writes

$$
  \pi_1(X,x)
  \;\coloneqq\;
  Hom_{\Pi_1(X)}(x,x)
  \,.
$$

Prop. \ref{ConcatenationOfHomotopyClassesOfPaths} says that under concatenation of paths, this
set is a [[group]]. As such it is called the _[[fundamental group]]_ of $X$ at $x$.

=--




The following picture indicates the four non-equivalent non-trivial generators of the [[fundamental group]] of the
oriented [[surface]] of [[genus of a surface|genus]] 2:

<img src="https://ncatlab.org/nlab/files/FundamentalGroupOfGenus2Surface.png" width="500">

> graphics grabbed from [Lawson 03](#Lawson03)

+-- {: .num_example #FundamentalGroupOfEuclideanSpace}
###### Example
**([[fundamental group]] of [[Euclidean space]])**

For $n \in \mathbb{N}$ and $x \in \mathbb{R}^n$ any point in the
$n$-dimensional [[Euclidean space]] (regarded with its [[metric topology]])
we have that the [[fundamental group]] (def. \ref{FundamentalGroupoidAndFundamentalGroup})
at that point is trivial:

$$
  \pi_1(\mathbb{R}^n, x) = \ast
  \,.
$$

=--

+-- {: .num_remark #PointedTopologicalSpaces}
###### Remark
**(basepoints)**

Definition \ref{FundamentalGroupoidAndFundamentalGroup} intentionally offers two variants of the
definition.

The first, the _[[fundamental groupoid]]_ is canonically given, without choosing a basepoint. As a result, it is a structure that is not quite a [[group]] but, slightly more generally, a "[[groupoid]]"
(a "group with many objects"). We discuss the concept of [[groupoids]] [below](#Groupoid).

The second, the [[fundamental group]], is a genuine group, but its definition requires picking a base point $x \in X$.

In this context it is useful to say that

1. a _[[pointed topological space]]_ $(X,x)$ is

   1. a [[topological space]] $X$;

   1. a $x \in X$ in the underlying set.

1. a [[homomorphism]] of pointed topological spaces $f \;\colon\; (X,x) \longrightarrow (Y,y)$
   is a base-point preserving continuous function, namely

   1. a [[continuous function]] $f \;\colon\; X \longrightarrow Y$

   1. such that $f(x) = y$.

Hence there is a [[category]], to be denoted, $Top^{\ast/}$, whose [[objects]] are the
[[pointed topological spaces]], and whose [[morphisms]] are tbe base-point preserving continuous functions.

Similarly, a [[homotopy]] between morphisms $f, f' \colon (X,x) \to (Y,y)$ in $Top^{\ast/}$ is a [[homotopy]]
$\eta \colon f \Rightarrow f'$ of underlying
[[continuous functions]], as in def. \ref{LeftHomotopy}, such that the corresponding function

$$
  \eta \;\colon\; X \times [0,1] \longrightarrow Y
$$

preserves the basepoints in that

$$
  \underset{t \in [0,1]}{\forall} \eta(x,t) = y
  \,.
$$

These pointed homotopies still form an [[equivalence relation]] as in prop. \ref{EquivRelHomotopy}
and hence quotienting these out yields the pointed analogue of the [[homotopy category]]
from def. \ref{HomotopyCategory}, now denoted

$$
  \kappa \;\colon\; Top^{\ast/} \longrightarrow Ho(Top^{\ast/})
  \,.
$$

=--



In general it is hard to explicitly compute the fundamental group of a topological
space. But often it is already useful to know if two spaces have the same fundamental group or not:

+-- {: .num_defn #PushElementsFundamentalGroup}
###### Definition
**(pushforward of elements of [[fundamental groups]])**

Let $(X,x)$ and $(Y,y)$ be [[pointed topological space]] (remark \ref{PointedTopologicalSpaces}) and let

$$
  f \;\colon\; X \longrightarrow Y
$$

be a [[continuous function]] which respects the chosen points, in that $f(x) = y$.

Then there is an induced [[homomorphism]] of [[fundamental groups]] (def. \ref{FundamentalGroupoidAndFundamentalGroup})

$$
  \array{
    \pi_1(X,x) &\overset{f_\ast}{\longrightarrow}& \pi_1(Y,y)
    \\
    [\gamma] &\mapsto& [f \circ \gamma]
  }
$$

given by sending a closed [[path]] $\gamma \colon [0,1] \to X$  to the composite

$$
  f \circ \gamma
  \;\colon\;
  [0,1]
    \overset{\gamma}{\longrightarrow}
  X
    \overset{f}{\longrightarrow}
  Y
  \,.
$$

=--


+-- {: .num_remark #FundamentalGroupFunctor}
###### Remark
**([[fundamental group]] is [[functor]] on [[pointed topological spaces]])**

The pushforward operation in def. \ref{PushElementsFundamentalGroup} is [[functor|functorial]], now on the [[category]] $Top^{\ast/}$
of [[pointed topological spaces]] (remark \ref{PointedTopologicalSpaces})

$$
  \pi_1 \;\colon\; Top^{\ast/} \longrightarrow Grp
  \,.
$$

=--

+-- {: .num_prop #DependenceOnHomotopyClassesFundamentalGroup}
###### Proposition
**([[fundamental group]] depends only on [[homotopy classes]])**

Let $X,Y \in Top^{\ast/}$ be [[pointed topological space]] and let $f_1, f_2 \;\colon\; X \longrightarrow Y$
be two base-point preserving continuous functions. If there is a pointed [[homotopy]] (def. \ref{LeftHomotopy}, remark \ref{PointedTopologicalSpaces})

$$
  \eta \;\colon\; f_1 \Rightarrow f_2
$$

then the induced [[homomorphisms]] on fundamental groups (def. \ref{PushElementsFundamentalGroup}) agree

$$
  (f_1)_\ast = (f_2)_\ast \;\colon\; \pi_1(X,x) \to \pi_1(Y,y)
  \,.
$$

In particular if $f \;\colon; X \longrightarrow Y$ is a [[homotopy equivalence]] (def. \ref{HomotopyEquivalence}) then
$f_\ast \;\colon\; \pi_1(X,x) \to \pi_1(Y,y)$ is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

This follows by the fact that homotopy respects composition (prop. \ref{EquivRelHomotopy}):

If $\gamma \;\colon\; [0,1] \longrightarrow X$ is a closed path representing a given element of
$\pi_1(X,x)$, then the homotopy $f_1 \Rightarrow f_2$ induces a homotopy

$$
  f_1 \circ \gamma \Rightarrow f_2 \circ \gamma
$$

and therefore these represent the same elements in $\pi_1(Y,y)$.

If follows that if $f$ is a homotopy equivalence with homotopy inverse $g$, then
$g_\ast \colon \pi_1(Y,y) \to \pi_1(X,x)$ is an [[inverse morphism]] to  $f_\ast \colon \pi_1(X,x) \to \pi_1(Y,y)$
and hence $f_\ast$ is an [[isomorphism]].

=--

+-- {: .num_remark}
###### Remark

Prop. \ref{DependenceOnHomotopyClassesFundamentalGroup} says that the
fundamental group functor from def. \ref{PushElementsFundamentalGroup} and remark \ref{FundamentalGroupFunctor}
factors through the [[classical pointed homotopy category]] from remark \ref{PointedTopologicalSpaces}:

$$
  \array{
    Top^{\ast/} &\overset{\pi_1}{\longrightarrow}& Grp
    \\
    {}^{\mathllap{\kappa}}\downarrow & \nearrow
    \\
    Ho(Top^{\ast/})
  }
  \,.
$$


=--

+-- {: .num_defn #SimplyConnected}
###### Definition
**([[simply connected topological space]])**

A topological space $X$ for which

1. $\pi_0(X) \simeq \ast$ ([[path-connected topological space|path connected]])

1. $\pi_1(X,x) \simeq 1$ (the [[fundamental group]] is [[trivial group|trivial]], def. \ref{FundamentalGroupoidAndFundamentalGroup}),

is called _[[simply connected topological space|simply connected]]_.

=--

We will need also the following local version:

+-- {: .num_defn #SemiLocallySimplyConnected}
###### Definition
**([[semi-locally simply connected topological space]])**

A [[topological space]] $X$ is called  _[[semi-locally simply connected topological space|semi-locally simply connected]]_ if every point $x \in X$ has a [[neighbourhood]] $U_x \subset X$ such that every loop in $U_x$ is contractible as a loop in $X$,
hence such that the induced morphism of [[fundamental groups]] (def. \ref{PushElementsFundamentalGroup})

$$
  \pi_1(U_x,x) \to \pi_1(X,x)
$$

is trivial (i.e. sends everything to the [[neutral element]]).

If every $x$ has a neighbourhood $U_x$ which is itself simyply connected, then $X$ is called a
_[[locally simply connected topological space]]_. This implies semi-local simply-connectedness.

=--


+-- {: .num_example #SimplyConnectedEuclideanSpace}
###### Example
**([[Euclidean space]] is [[simply connected topological space|simply connected]])**

For $n \in \mathbb{N}$, then the [[Euclidean space]] $\mathbb{R}^n$
is a [[simply connected topological space]] (def. \ref{SimplyConnected}).

=--




### Groupoids
 {#Groupoid}

In def. \ref{FundamentalGroupoidAndFundamentalGroup} we extracted the [[fundamental group]]
at some point $x \in X$ from a larger algebraic structure, that incorporates all the basepoints,
to be called the _[[fundamental groupoid]]_. This larger algebraic structure of _[[groupoids]]_ is usefully made
explicit for the formulation and proof of the [[fundamental theorem of covering spaces]] (theorem \ref{FundamentalTheoremOfCoveringSpaces} below)
and the development of [[homotopy theory]] in general.

Where a _[[group]]_ may be thought of as a _group of symmetry transformations_ that [[isomorphism|isomorphically]] relates one [[object]] to itself (the _[[symmetries]]_ of one object, such as the [[isometries]] of a [[polyhedron]]) a _groupoid_ is a collection of symmetry transformations acting between possibly more than one object.

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/AssociativityDiagram.png" width="400">
</div>


Hence a groupoid consists of a [[set]] of objects $x, y, z, \cdots$ and for each [[pair]] of objects $(x,y)$ there is a set of transformations, usually denoted by arrows

$$
  x \overset{f}{\longrightarrow} y
$$

which may be composed if they are composable (i.e. if the first ends where the second starts)

$$
  \array{
    && y
    \\
    & {}^{\mathllap{f}}\nearrow && \searrow^{\mathrlap{g}}
    \\
    x && \underset{g \circ f}{\longrightarrow}  && z
  }
$$

such that this composition is [[associativity|associative]] and such that for each object $x$ there is identity transformation $x \overset{id_X}{\longrightarrow} x$ in that this is a [[neutral element]] for the composition of transformations, whenever defined.

So far this structure is what is called a _[[small category]]_. What makes this a _([[small groupoid|small]]) groupoid_ is that all these transformations are to be "symmetries" in that they are [[invertible morphisms]] meaning that for each transformation $x \overset{f}{\longrightarrow} y$ there is a transformation the other way around $y \overset{f^{-1}}{\longrightarrow} x$ such that

$$
  f^{-1} \circ f  = id_x
  \phantom{AAAA}
  f \circ f^{-1} = id_y
  \,.
$$

If there is only a single object $x$, then this definition reduces to that of a [[group]], and in this sense groupoids are "groups with many objects". Conversely, given any groupoid $\mathcal{G}$ and a choice of one of its objects $x$, then the subcollection of transformations from and to $x$ is a group, sometimes called the [[automorphism group]] $Aut_{\mathcal{G}}(x)$ of $x$ in $\mathcal{G}$.

Just as for groups, the "transformations" above need not necessarily be given by concrete transformations (say by [[bijections]] between [[objects]] which are [[sets]]). Just as for groups, such a concrete realization is always possible, but is an extra choice (called a [[representation]] of the groupoid). Generally one calls these "transformations" _[[morphisms]]_: $x \overset{f}{\longrightarrow} y$ is a morphism with "[[source]]" $x$ and "[[domain]]" $y$.

An archetypical example of a groupoid is the [[fundamental groupoid]] $\Pi_1(X)$ of a [[topological space]]
(def. \ref{FundamentalGroupoid} below, for introduction see [here](Introduction+to+Topology+--+2#Homotopy)): For $X$ a topological space, this is the groupoid whose

* [[objects]] are the points $x \in X$;

* [[morphisms]] $x \overset{[\gamma]}{\longrightarrow} y$ are the [[homotopy relative boundary]]-[[equivalence classes]] $[\gamma]$ of [[paths]] $\gamma \colon [0,1] \to X$ in $X$, with $\gamma(0) = x$ and $\gamma(1) = y$;

and [[composition]] is given, on representatives, by [[concatenation]] of paths. Here the class of the [[reverse path]] $\bar\gamma \;\colon\; t \mapsto \gamma(1-t)$ constitutes the inverse morphism, making this a groupoid.

If one _chooses_ a point $x \in X$, then the corresponding group at that point is the _[[fundamental group]]_ $\pi_1(X,x) \coloneqq Aut_{\Pi_1(X)}(x)$ of $X$ at that point.

This highlights one of the reasons for being interested in groupoids over groups: Sometimes this allows to avoid unnatural ad-hoc choices and it serves to streamline and simplify the theory.

A [[homomorphism]] between groupoids is the obvious: a [[function]] between their underlying [[objects]] together with a function between their morphisms which respects [[source]] and [[target]] objects as well as [[composition]] and [[identity morphisms]]. If one thinks of the groupoid as a special case of a [[category]], then this is a _[[functor]]_. Between groupoids with only a single object this is the same as a [[group homomorphism]].

For example if $f \;\colon\; X \to Y$ is a [[continuous function]] between topological spaces, then postcomposition of [[paths]] with this function induces a groupoid homomorphism $f_\ast \;\colon\; \Pi_1(X) \longrightarrow \Pi_1(Y)$ between the [[fundamental groupoids]] from above.

Groupoids with groupoid homomorphisms ([[functors]]) between them form a [[category]] [[Grpd]] (def. \ref{1CategoryOfGroupoids} below) which includes the categeory [[Grp]] of [[groups]] as the [[full subcategory]] of the groupoids with a single object. This makes precise how groupoid theory is a generalization of [[group theory]].

However, for groupoids more than for groups one is typically interested in "[[conjugation actions]]" on homomorphisms. These are richer for groupoids than for groups, because one may conjugate with a different morphism at each object. If we think of groupoids as special cases of [[categories]], then these "conjugation actions on homomorphisms" are _[[natural transformations]]_ between [[functors]].

For examples if $f,g \;\colon\; X \longrightarrow Y$ are two [[continuous functions]] between [[topological spaces]], and if $\eta \;\colon\; f \Rightarrow g$ is a [[homotopy]] from $f$ to $g$, then the [[homotopy relative boundary]] classes of the [[paths]] $\eta(x,-) \;\colon\; [0,1] \to Y$ constitute a natural transformation between $f_*, g_\ast \;\colon\; \Pi_1(X) \to \Pi_y(Y) $ in that for all paths $x_1 \overset{[\gamma]}{\longrightarrow} x_2$ in $X$ we have the "conjugation relation"

$$
  [\eta(x_1,-)] \cdot [f\circ\gamma]
  =
  [g \circ \gamma] \cdot [\eta(x_2,-)]
  \phantom{AAAA}
  \text{i.e.}
  \phantom{AAAA}
  \array{
    f(x_1) &\overset{[\eta(x_1,-)]}{\longrightarrow}& g(x_1)
    \\
    {}^{\mathllap{[f \circ \gamma]}}\downarrow && \downarrow^{\mathrlap{[f \circ \gamma]}}
    \\
    f(x_2) &\underset{[\eta(x_2,-)]}{\longrightarrow}& g(x_2)
  }
  \,.
$$


+-- {: .num_defn #GroupoidDependentlyTypes}
###### Definition
**([[groupoid]])

A _[[small groupoid]]_ $\mathcal{G}$ is

1. a [[set]] $X$, to be called the _set of [[objects]]_;

1. for all [[pairs]] of objects $(x,y) \in X \times X$ a
   [[set]] $Hom(x,y)$,  to be called the _set of [[morphisms]] with [[domain]] or [[source]] $x$ and [[codomain]] or [[target]] $y$_;

1. for all [[triples]] of objects $(x,y,z) \in X \times X \times X$ a [[function]]

   $$
     \circ_{x,y,z} \;\colon\; Hom(y,z) \times Hom(x,y) \longrightarrow Hom(x,z)
   $$

   to be called _[[composition]]_

1. for all objects $x \in X$ an element

   $$
     id_x \in Hom(x,x)
   $$

   to be called the _[[identity morphism]]_ on $x$;

1. for all pairs $x,y \in Hom(x,y)$ of obects a function

   $$
     (-)^{-1} \;\colon\; Hom(x,y) \longrightarrow Hom(y,x)
   $$

   to be called the _[[inverse morphism|inverse-assigning]] function_


such that

1. ([[associativity]]) for all [[quadruples]] of objects $x_1, x_2, x_3, x_4 \in X$ and all [[triples]] of morphisms $f \in Hom(x_1,x_2)$, $g \in Hom(x_2,x_3)$ and $h \in Hom(x_3,x_4)$ an [[equality]]

   $$
     h \circ (g \circ f) \;=\; (h \circ g) \circ f
   $$

1. ([[unitality]]) for all [[pairs]] of objects $x,y \in X$ and all moprhisms $f \in Hom(x,y)$ [[equalities]]

    $$
      id_y \circ f = f
      \phantom{AAAA}
      f \circ id_x = f
    $$

1. ([[inverse morphism|invertibility]]) for all pairs of objects $x,y \in X$ and every morphism $f \in Hom(x,y)$ [[equalities]]

   $$
     f^{-1}\circ f = id_{x}
     \phantom{AAAA}
     f \circ f^{-1} = id_y
     \,.
   $$

If $\mathcal{G}_1, \mathcal{G}_2$ are two [[groupoids]], then a _[[homomorphism]]_ or _[[functor]]_ between them, denoted

$$
  F \;\colon\; \mathcal{G}_1 \longrightarrow  \mathcal{G}_2
$$

is

1. a [[function]] $F_0 \;\colon\; X_1 \longrightarrow X_2$ between the respective sets of objects;

1. for each pair $x,y \in X_1$ of objects a function

   $$
    F_{x,y} \;\colon\; Hom_{\mathcal{G}_1}(x,y) \longrightarrow Hom_{\mathcal{G}_2}(F_0(x), F_0(y))
   $$

   between sets of morphisms

such that

1. (respect for composition) for all triples $x,y,z \in X_1$ and all $f \in Hom(x,y)$ and $g \in Hom(y,z)$ an [[equality]]

   $$
    F_{y,z}(g) \circ_2 F_{x,y}(f)  \;=\; F_{x,z}(g\circ_1 f)
   $$

1. (respect for identities) for all $x \in X$ an equality

   $$
     F_{x,x}(id_x) = id_{F_0(x)}
     \,.
   $$

For $\mathcal{G}_1, \mathcal{G}_2$ two groupoids, and for $F,G \;\colon\; \mathcal{G}_1 \to \mathcal{G}_2$ two groupoid homomorphisms/functors, then a _conjugation_ or _[[homotopy]]_ or _[[natural transformation]]_ (necessarily a [[natural isomorphism]])

$$
  \eta \;\colon\; F \Rightarrow G
$$

is

* for each object $x \in X_1$ of $\mathcal{G}_1$ a morphism $\eta_{x} \in Hom_{\mathcal{G}_2}(F(x), G(y))$

such that

* for all $x,y \in X_1$ and $f \in Hom_{\mathcal{G}_1}(x,y)$ an [[equality]]

  $$
    \eta_y \circ_2 F(f)
     =
     G(f) \circ \eta_x
     \phantom{AAAAAA}
     \array{
       F(x) &\overset{\eta_x}{\longrightarrow}& G(x)
       \\
       {}^{\mathllap{F(f)}}\downarrow && \downarrow^{\mathrlap{G(f)}}
       \\
       F(y) &\underset{\eta_y}{\longrightarrow}& G(y)
     }
  $$


For $\mathcal{G}_1, \mathcal{G}_2$  two groupoids and $F, G, H \colon \mathcal{G}_1  \longrightarrow \mathcal{G}_2$
three functors between them and $\eta_1 \;\colon\; F \Rightarrow G$ and $\eta_2 \;\colon\; G \Rightarrow H$
conjugation actions/natural isomorphisms between these, there is the composite

$$
  \eta_2 \colon \eta_1  \;\colon\; F \Rightarrow H
$$

with components the composite of the components

$$
  (\eta_2 \circ \eta_1)(x) \coloneqq \eta_2(x) \circ \eta_1(x)
  \,.
$$

This yields for any two groupoid a _[[hom-groupoid]]_

$$
  Hom_{Grpd}(\mathcal{G}_1, \mathcal{G}_2)
$$

whose objects are the groupoid homomorphisms / functors, and whose morphisms are the conjugation actions / natural transformations.


=--

The archetypical example of a groupoid we already encountered above:

+-- {: .num_example #FundamentalGroupoid}
###### Example
**([[fundamental groupoid]])

For $X$ a [[topological space]], then its _[[fundamental groupoid]]_
(as in def. \ref{FundamentalGroupoidAndFundamentalGroup})
has as set of objects the underlying set of $X$, and for $x,y \in X$
two points, the set of homomorphisms is the set of [[paths]] from
$x$ to $y$ modulo [[homotopy relative boundary]]:

$$
  Hom_{\Pi_1(X)}(x,y) (P_{x,y})/\sim_h
$$

and [[composition]] is given by [[concatenation of paths]].

=--

+-- {: .num_remark}
###### Remark
**([[groupoids]] are special cases of [[categories]])**

A [[small groupoid]] (def. \ref{GroupoidDependentlyTypes}) is equivalently a [[small category]] in which all [[morphisms]] are [[isomorphism|isomorphisms]].

While therefore groupoid theory may be regarded as a special case of [[category theory]], it
is noteworthy that the two theories are quite different in character. For example [[higher groupoid]]
theory is _[[homotopy theory]]_ which is rich but quite tractable, for instance via tools
such as [[simplicial homotopy theory]] or [[homotopy type theory]], while [[higher category theory]]
is intricate and becomes tractable mostly by making recourse to higher groupoid theory in the guise of
[[(infinity,1)-category theory]] and [[(infinity,n)-categories]].

=--

+-- {: .num_example #CoreGroupoid}
###### Example
**(groupoid [[core]] of a [[category]])**

For $\mathcal{C}$ any ([[small category|small]]) [[category]], then there is a maximal groupoid inside

$$
  Core(\mathcal{C}) \hookrightarrow \mathcal{C}
$$

sometimes called the _[[core]]_ of $\mathcal{C}$. This is obtained from $\mathcal{C}$
simply by discarding all those [[morphisms]] that are not [[isomorphisms]].

For instance

* For $\mathcal{C} = $ [[Set]] then $Core(Set)$ is the goupoid of [[sets]] and [[bijections]] between them.

  For $\mathcal{C}  $ [[FinSet]] then the [[skeleton]] of this groupoid (prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}) is the disjoint union of deloopings (example \ref{DeloopingGroupoidDisjointUnion}) of all the [[symmetric groups]]:

  $$
    Core(FinSet) \simeq \underset{n \in \mathbb{N}}{\sqcup} \Sigma(n)
  $$

* For $\mathcal{C} = $ [[Vect]] then $Core(Vect)$ is the groupoid of [[vector spaces]] and [[linear map|linear]] [[bijections]] between them.

  For $\mathcal{C} = $ [[FinVect]] then the [[skeleton]] of this groupoid is the disjoint union of delooping of all the
  [[general linear groups]]

  $$
    Core(FinVect) \simeq \underset{n \in \mathbb{N}}{\sqcup} GL(n)
    \,.
  $$


=--




+-- {: .num_example #DiscreteGroupoid}
###### Example
**([[discrete groupoid]])**

For $X$ any set, there is the _[[discrete groupoid]]_ $Disc(X)$, whose set of objects
is $X$ and whose only morphisms are [[identity morphisms]].

This is also the  [[fundamental groupoid]] (example \ref{FundamentalGroupoid})
of the [[discrete topological space]] on the set $X$.

=--




+-- {: .num_example #GroupoidsCoproduct}
###### Example
**([[disjoint union]]/[[coproduct]] of [[groupoids]])

Let $\{\mathcal{G}_i\}_{i \in I}$ be a [[set]] of [[groupoids]]. Then their [[disjoint union]] ([[coproduct]]) is the groupoid

$$
  \underset{i \in I}{\sqcup} \mathcal{G}_i
$$

whose set of objects is the disjoint union of the sets of objects of the summand groupoids, and whose sets of morphisms between two objects is that of $\mathcal{G}_i$ if both objects are form this groupoid, and is [[empty set|empty]] otherwise.

=--

+-- {: .num_defn #ProductGroupoid}
###### Definition
**([[product category|product]] of [[groupoids]])**

Let $\{\mathcal{G}_i\}_{i \in I}$ be a [[set]] of [[groupoids]]. Their [[product category|product groupoid]]
is the [groupoid]]

$$
  \underset{i \in I}{\prod} \mathcal{G}_i
$$

whose set of objects is the [[Cartesian product]] of the sets of objects of the factor groupoids

$$
 \left(
   \underset{i \in I}{\prod} \mathcal{G}_i
 \right)_0
   \;\coloneqq\;
 \underset{i \in I}{\prod} (\mathcal{G}_i)_0
$$

and whose set of [[morphisms]] between [[tuples]] $(x_i)_{i \in I}$ and $(y_i)_{i \in I}$
is the corresponding Cartesian product of morphisms, with elements denoted

$$
  (x_i)_{i \in I} \overset{(f_i)_{i \in I}}{\longrightarrow} (y_i)_{i \in I}
  \,.
$$

For instance if each of the groupoids is the [[delooping]] $\mathcal{G}_i = B G_i$
of a [[group]] $G_i$ (example \ref{GroupoidFromDelooping}) then the product groupoid is the [[delooping groupoid]] of the [[direct product group]]:

$$
  \underset{i \in I}{\prod} B G_i
   \simeq
  B \underset{i \in I}{\prod} G_i
  \,.
$$

As another example, if $\underset{i \in I}{\sqcup} \mathcal{G}_i$ is the [[coproduct]] groupoid from
example \ref{GroupoidsCoproduct}, and if $\mathcal{G}$ is any groupoid, then a groupoid homomorphism
of the form

$$
  \underset{i \in I}{\sqcup} \mathcal{G}_i
    \longrightarrow
  \mathcal{G}
$$

is equivalently a [[tuple]] $(f_i)_{i \in I}$ of groupoid homomorphisms

$$
  \mathcal{G}_1 \overset{f_i}{\longrightarrow} \mathcal{G}
  \,.
$$

The analogous statement holds for homotopies between groupoid homomorphisms, and so one find that the
[[hom-groupoid]] out of a coproduct of groupoids is the product groupoid of the separate hom-groupoids:

$$
  Hom_{Grpd}\left(
    \underset{i \in I}{\sqcup} \mathcal{G}_i
    \;,\;
    \mathcal{G}
  \right)
  \;\simeq\;
  \underset{i \in I}{\prod}
  Hom_{Grpd}( \mathcal{G}_1, \mathcal{G} )
  \,.
$$

=--






+-- {: .num_prop #1CategoryOfGroupoids}
###### Remark
**([[1-category]] of [[groupoids]])**

From def. \ref{GroupoidDependentlyTypes} we see that there
is a [[category]] whose

* [[objects]] are the small groupoids;

* [[morphisms]] are the groupoid homomorphisms ([[functors]]).

=--

But since this [[1-category]] does not reflect the existence of [[homotopies]]/[[natural isomorphisms]]
between homomorphsims/[[functors]] of groupoids (def. \ref{GroupoidDependentlyTypes})
this [[1-category]] is not what one is interested in when considering [[homotopy theory]]/[[higher category theory]].

In order to obtain the right notion of category of groupoids
that does reflect homotopies, we first consider now the _horizontal_ composition of homotopies/natural transformations.

+-- {: .num_lemma #HmotopiesWithMorphismsHorizontaComposition}
###### Lemma
**([[horizontal composition]] of [[homotopies]] with [[morphisms]])**

Let $\mathcal{G}_1$, $\mathcal{G}_2$, $\mathcal{G}_3$, $\mathcal{G}_4$ be groupoid and let

$$
  \mathcal{G}_1
    \overset{F_1}{\longrightarrow}
  \mathcal{G}_2
    \underoverset
      {\underset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
      {\Downarrow{\mathrlap{\eta}}}
  \mathcal{G}_3
    \overset{F_3}{\longrightarrow}
  \mathcal{G}_3
$$

be morphisms and a homotopy $\eta$. Then there is a homotopy

$$
  \mathcal{G}_1
  \phantom{AAAA}
    \underoverset
      {\underset{F_3 \circ F'_2\circ F_1}{\longrightarrow}}
      {\overset{F_3 \circ F'_2\circ F_1}{\longrightarrow}}
      {\Downarrow{\mathrlap{ F_2 \cdot \eta_ \cdot F_1 }}}
  \phantom{AAAA}\mathcal{G}_2
$$

between the respective composites, with components given by

$$
  (F_2 \cdot \eta \cdot F_1)(x)
    \;\coloneqq\;
  F_2(\eta(F_1(x)))
  \,.
$$

This operation constitutes a groupoid homomorphism/functor

$$
  F_3\cdot (-)\cdot F_1
    \;\colon\;
  Hom_{Grpd}(\mathcal{G}_2, \mathcal{G}_3)
    \longrightarrow
  Hom_{Grp}(\mathcal{G}_1, \mathcal{G}_4)
  \,.
$$

=--

+-- {: .proof}
###### Proof

The respect for identities is clear. To see the respect for composition, let

$$
  \mathcal{G}_2
  \array{
     \overset{F}{\longrightarrow}
     \\
     \Downarrow \eta_1
     \\
     \overset{G}{\longrightarrow}
     \\
     \Downarrow \eta_2
     \\
     \underset{H}{\longrightarrow}
  }
  \mathcal{G}_3
$$

be two composable homotopies. We need to show that

$$
  F_3 \cdot (\eta_2 \circ \eta_1) \cdot F_1
  =
  ( F_3 \cdot \eta_2 \cdot F_1 ) \circ ( F_3 \cdot \eta_1 \cdot F_1 )
  \,.
$$

Now for $x$ any object of $\mathcal{G}_1$ we find

$$
  \begin{aligned}
    (F_3 \cdot (\eta_2 \circ \eta_1) \cdot F_1)(x)
      & \coloneqq
    F_2((\eta_2 \circ \eta_1)(F_1(X)))
      \\
      & \coloneqq
   F_3( \eta_2(F_1(x)) \circ \eta_1 (F_1(x)))
     \\
     &=
    F_3( \eta_2(F_1(x)) ) \circ F_3( \eta_1(F_1(X)) )
      \\
     & =
    (( F_3 \cdot \eta_2 \cdot F_1 ) \circ ( F_3 \cdot \eta_1 \cdot F_1 ))(x)
  \end{aligned}
  \,.
$$

Here all steps are unwinding of the definition of horizontal and of ordinary (vbertical)
composition of homotopies, except the third equality, which is the functoriality of $F_2$.

=--

+-- {: .num_lemma #GroupoidHomotopyHorizontalComposition}
###### Lemma
**([[horizontal composition]] of [[homotopies]])

Consider a [[diagram]] of [[groupoids]], groupoid homomorphsims (functors) and homotopies (natural transformations) as follows:

$$
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
$$

The _[[horizontal composition]]_ of the homotopies to a single homotopy of the form

$$
  \mathcal{G}_1
     \underoverset
       {\underset{F'_2 \circ F'_1}{\longrightarrow}}
       {\overset{F_2\circ F_1}{\longrightarrow}}
       {\Downarrow \eta_2 \cdot \eta_1}
  \mathcal{G}_3
$$

may be defined in temrs of the horizontal composition of homotopies with morphisms (lemma \ref{HmotopiesWithMorphismsHorizontaComposition}) and the ("vertical") composition of homotopies with themselves, in two different ways, namely by decomposing the above diagram as


$$
  \array{
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {}
  \mathcal{G}_3
  \\
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {}
       {}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
  }
$$

or as

$$
  \array{
  \mathcal{G}_1
    \underoverset
       {}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_2\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_2}}
  \mathcal{G}_3
  \\
  \mathcal{G}_1
    \underoverset
       {\underset{\phantom{AA}F'_1\phantom{AA}}{\longrightarrow}}
       {\overset{\phantom{AA}F_1\phantom{AA}}{\longrightarrow}}
       {\Downarrow {\eta_1}}
  \mathcal{G}_2
    \underoverset
       {\underset{\phantom{AA}F'_2\phantom{AA}}{\longrightarrow}}
       {}
       {}
  \mathcal{G}_3
  }
$$

In the first case we get

$$
  \eta_2 \cdot \eta_1
  \;\coloneqq\;
  (\eta_2 \cdot F'_1) \circ (F_2 \cdot \eta_1)
$$

while in the second case we get

$$
  \eta_2 \cdot \eta_1
   \;\coloneqq\;
   ( F'_2 \cdot \eta_1 ) \circ (\eta_2 \cdot F_1)
  \,.
$$

These two definitions coincide.

=--

+-- {: .proof}
###### Proof

For $x$ an object of $\mathcal{G}_1$, then we need that the following square [[diagram]] [[commuting diagram|commutes]] in $\mathcal{G}_3$

$$
  \array{
    F_2(F_1(x))
      &\overset{ (F_2\cdot \eta_1)(x) }{\longrightarrow}& F_2(F'_1(x))
    \\
    {}^{\mathllap{ (\eta_2 \cdot F_1)(x) }}\downarrow
      &&
    \downarrow^{\mathrlap{ (\eta_2\cdot F'_1)(x) }}
    \\
    F'_2(F_1(x))
      & \underset{ (F'_2 \cdot \eta_1)(x) }{\longrightarrow} &
    F'_2(F'_1(y))
  }
   \phantom{AAAA} = \phantom{AAAA}
  \array{
    F_2(F_1(x)) &\overset{F_2(\eta_1(x))}{\longrightarrow}& F_2(F'_1(x))
    \\
    { }^{\mathllap{\eta_2(F_1(x))}}\downarrow
      &&
    \downarrow^{\mathrlap{ \eta_2(F'_1(x)) }}
    \\
    F'_2(F_1(x))
      & \underset{F'_2(\eta_1(x))}{\longrightarrow} &
    F'_2(F'_1(y))
  }
  \,.
$$

But the ommutativity of the square on the right is the defining compatibility condition on the components of $\eta_2$ applied to the morphism $\eta_1(x)$ in $\mathcal{G}_2$.

=--


+-- {: .num_prop #HorizontalCompositionWithHomotopyIsNaturalTransformation}
###### Proposition
**([[horizontal composition]] with [[homotopy]] is [[natural transformation]])**

Consider groupoids, homomorphisms and homotopies of the form

$$
  \mathcal{G}_1
    \underoverset
       {\underset{F'_1}{\longrightarrow}}
       {\overset{F_1}{\longrightarrow}}
       {\Downarrow \eta_1}
  \mathcal{G}_2
  \phantom{AAAAAAA}
  \mathcal{G}_3
    \underoverset
       {\underset{F'_3}{\longrightarrow}}
       {\overset{F_3}{\longrightarrow}}
       {\Downarrow \eta_3}
  \mathcal{G}_4
  \,.
$$

Then horizontal composition with the homotopies (lemma \ref{GroupoidHomotopyHorizontalComposition})
constitutes a [[natural transformation]] between the functors of horizontal composition with morphisms (lemma \ref{HmotopiesWithMorphismsHorizontaComposition})

$$
  ( \eta_3\cdot (-)\cdot \eta_1 )
    \;\colon\;
  ( F_3 \cdot (-)\cdot F_1 )
    \;\Rightarrow\;
  (  F^\prime_3 \cdot (-) \cdot  F^\prime_1 )
  \;\colon\;
    Hom_{Grpd}(\mathcal{G}_2,\mathcal{G}_3)
      \longrightarrow
    Hom_{Grpd}(\mathcal{G}_1, \mathcal{G}_4)
  \,.
$$

=--

+-- {: .proof}
###### Proof

By lemma \ref{GroupoidHomotopyHorizontalComposition}.

=--

It first of all follows that the following makes sense

+-- {: .num_defn #HomotopyCategoryOfGroupoids}
###### Definition
**([[homotopy category]] of groupoids)**

There is also the [[homotopy category]] $Ho(Grpd)$ whose

* [[objects]] are small groupoids;

* [[morphisms]] are [[equivalence classes]] of groupoid homomorphisms modulo homotopy (i.e. [[functors]] modulo [[natural transformations]]).

This is usually denoted $Ho(Grpd)$.

=--

Of course what the above really means is that, without quotienting out homotopies,
groupoids form a [[2-category]], in fact a [[(2,1)-category]], in fact an [[enriched category]]
which is enriched over the naive 1-category of groupoids from remark \ref{1CategoryOfGroupoids},
hece a [[strict 2-category]] with [[hom-groupoids]].

+-- {: .num_defn #EquivalenceOfGroupoids}
###### Definition
**([[equivalence of groupoids]])**

Given two groupoids $\mathcal{G}_1$ and $\mathcal{G}_2$, then a homomorphism

$$
  F\;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2
$$

is an _[[equivalence of groupoids|equivalence]]_ if it is an [[isomorphism]]
in the [[homotopy category]] $Ho(Grpd)$ (def. \ref{HomotopyCategoryOfGroupoids}), hence if there exists a homomorphism the
other way around

$$
  G \;\colon\; \mathcal{G}_2 \longrightarrow \mathcal{G}_1
$$

and a homotopy/natural transformations of the form

$$
  G \circ F \simeq id_{\mathcal{G}_1}
  \phantom{AAAA}
  F \circ G \simeq id_{\mathcal{G}_2}
  \,.
$$

=--




+-- {: .num_example #FundamentalGroupoid2Functor}
###### Example
**([[(2,1)-functor|(2,1)-functoriality]] of [[fundamental groupoid]])

If $X$ and $Y$ are [[topological spaces]] and $f \;\colon\; X \longrightarrow Y$
is a [[continuous function]] between them, then this induces a groupoid homomorphism (functor)
between the respective [[fundamental groupoids]] (def. \ref{FundamentalGroupoid})

$$
  F_f \;\colon\; \Pi_1(X) \longrightarrow \Pi_1(Y)
$$

given on objects by the underlying function of $f$

$$
  (F_f)_0 \coloneqq f
$$

and given on the class of a [[path]] by the evident postcomposition with $f$

$$
  (F_f)_{x,y}
    \;\colon\;
  (x \overset{[\gamma]}{\longrightarrow} y)
    \;\mapsto\;
  (f(x) \overset{[f \circ \gamma]}{\longrightarrow} f(y) )
  \,.
$$

This construction clearly respects [[identity morphisms]] and [[composition]] and hence is
itself a [[functor]] of the form

$$
  \Pi_1 \;\colon\; Top \longrightarrow Grpd_1
$$

from the [[category]] [[Top]] of [[topological  space]] to the [[1-category]] [[Grpd]] of groupoids.

But more is true: If $f,g \;\colon\; X \longrightarrow Y$ are two [[continuous function]] and

$$
  \eta \;\colon\; f \Rightarrow g
$$

is a [[left homotopy]] between them, hence a continuous function

$$
  \eta \;\colon\; X \times [0,1] \longrightarrow Y
$$

such that $\eta(-,0) = f$ and $\eta(-,1) = g$, then this induces a homotopy between the above groupoid homomorphisms
(a natural transformation of functors).

This shows that the fundamental groupoid functor in fact descends to [[homotopy categories]]

$$
  \Pi_1 \;\colon\; Ho(Top) \longrightarrow Ho(Grpd)
  \,.
$$

(In fact this means it even extends to a [[(2,1)-functor]] from the [[(2,1)-category]]
of topological spaces, continuous functions, and [[higher homotopy]]-classes of left homotopues,
to that of groupoids.)

As a direct consequence it follows that if there is a [[homotopy equivalence]]

$$
  X \simeq_h Y
$$

between [[topological spaces]], then there is an induced [[equivalence of groupoids]]
betwee their [[fundamental groupoids]]

$$
  \Pi_1(X) \simeq \Pi_1(Y)
  \,.
$$

Hence the [[fundamental groupoid]] is a _[[homotopy invariant]]_ of topological spaces.
Of course by prop. \ref{DeloopingGroupoidEquivalence} the fundamental groupoid is
equivalent, as a groupoid, to the disjoint union of the [[deloopings]] of
all the [[fundamental groups]] of the given topological spaces, one for each [[connected component]],
and hence this is equivalently the statement that the set of connected components
and the fundamental groups of a topological space are homotopy invariants.

=--








+-- {: .num_example #GroupoidFromDelooping}
###### Example
**([[delooping]] of a  [[group]])**

Let $G$ be a [[group]]. Then there is a groupoid, denoted $B G$, with a single object $p$, with morphisms

$$
  Hom_{B G}(p,p) \coloneqq G
$$

the elements of $G$, with composition the multiplication in $G$, with identity morphism the [[neutral element]] in $G$ and with inverse morphisms the inverse elements in $G$.

This is also called the _[[delooping]]_ of $G$ (because the [[loop space object]] of $B G$ at the unique point is the given group:
$\Omega B G \simeq G$).

For $G_1, G_2$ two groups, then there is a [[natural bijection]] between [[group homomorphisms]]
$\phi \colon G_1 \to G_2$ and groupoid homomorphisms $B G_1 \to B G_2$: the latter are all of the form
$B \phi$, with $(B \phi)_0$ uniquely fixed and $(B \phi)_{p,p} = \phi$.

This means that the construction $B(-)$ is a  [[fully faithful functor]]

$$
  B(-) \;\colon\; Grp \hookrightarrow Grpd_1
$$

into from the category [[Grp]] of groups to the [[1-category]] of [[groupoids]].

But beware that this functor is not fully faithful when homotopies of groupoids are taken into acount,
because there are in general non-trivial homotopies between morphims of the form

$$
  B \phi_1, B \phi_2
  \;\colon\;
  B G \longrightarrow B H
$$

By definition, such a homotopy (natural transformation) $\eta \;\colon\; B \phi_1 \Rightarrow B \phi_2$
is a choice of a single elemet $\eta_p \in H$ such that for all $g \in G$
we have

$$
  \phi_2(g) = h \cdot \phi_1(g) \cdot h^{-1}
  \phantom{AAAAAAAAA}
  \array{
    p &\overset{h}{\longrightarrow}& p
    \\
    {}^{\mathllap{\phi_1(g)}}\downarrow && \downarrow^{\mathrlap{\phi_2(g)}}
    \\
    p &\underset{h}{\longrightarrow}& p
  }
$$

hence such that

$$
  \phi_2 = Ad_h \circ \phi_1
  \,.
$$

Therefore notably the induced functor

$$
  B(-) \;\colon\; Grp \longrightarrow Ho(Grp)
$$

to the [[homotopy category]] of groupoids is not fully faithful.

But since $B G$ is canonically a [[pointed object]] in groupoids, we may also regard [[delooping]]
as a functor

$$
  B(-) \;\colon\; Grp \longrightarrow Grpd^{\ast/}
$$

to the [[category of pointed objects]] of [[Grpd]]. Since groupoid homomorphisms $B G_1 \to B G_2$
necessarily preserve the basepoint, this makes no difference at this point. But as we now
pass to the [[homotopy category]]

$$
  B(-) \;\colon\; Grp \hookrightarrow Ho(Grpd^{\ast/})
$$

then also the homotopies are required to preserve the absepoint, and for
homotopies between homomorphisms between delooped groups this means, since there only
is a single point, that these homotopies are all trivial. Hence regarded this way
the functor is a [[fully faithful functor]] again, hence an [[equivalence of categories]]
onto its [[essential image]]. By prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings} below
this essential image consists precisely of the (pointed) [[connected object|connected]] groupoids:

_Groups are equivalently pointed connected groupoids_.

=--


+-- {: .num_example #DeloopingGroupoidDisjointUnion}
###### Example
**([[disjoint union]] of [[delooping groupoids]])

Let $\{G_i\}_{i \in I}$ be a [[set]] of [[groups]]. Then there is a groupoid
$\underset{i \in I}{\sqcup} B G_i$ which is the disjoint union groupoid (example \ref{GroupoidsCoproduct}) of the [[delooping]] groupoids $B G_i$ (example \ref{GroupoidFromDelooping}).

Its set of objects is the index set $I$, and

$$
  Hom(i,j)
   =
  \left\{
    \array{
      G_i &\vert& i = j
      \\
      \emptyset &\vert& \text{otherwise}
    }
  \right.
$$

=--














+-- {: .num_defn #GroupoidConnectedComponents}
###### Definition
**([[connected components]] of a groupoid)**

Given a [[groupoid]] $\mathcal{G}$ with set of objects $X$, then the [[relation]] "there exists a morphism from $x$ to $y$", i.e.

$$
  (x\sim y)
  \;\coloneqq\;
  \left( Hom(x,y) \neq \emptyset \right)
$$

is clearly an [[equivalence relation]] on $X$. The corresponding set of [[equivalence classes]] is denoted

$$
  \pi_0(\mathcal{G})
$$

and called the set of _[[connected components]]_ of $\mathcal{G}$.

=--


+-- {: .num_defn #InGrupoidAutomorphismGroup}
###### Definition
**([[automorphism groups]])

Given a [[groupoid]] $\mathcal{G}$ and an object $x$, then under composition the set $Hom_{\mathcal{G}}(x,x)$ forms a [[group]]. This is called the _[[automorphism group]]_ $Aut_{\mathcal{G}}(x)$ or _vertex group_ or _isotropy group_ of $x$ in $\mathcal{G}$.

For each object $x$ in a groupoid $\mathcal{G}$, there is a canonical groupoid homomorphism

$$
  B Aut_{\mathcal{G}}(x) \hookrightarrow \mathcal{G}
$$

from the [[delooping groupoid]] (def. \ref{GroupoidFromDelooping}) of the automorphism group. This takes the
unique object of $B Aut_{\mathcal{G}}(x)$ to $x$ and takes every automorphism of $x$ "to itself",
regarded now again as a morphism in $\mathcal{G}$.

=--


+-- {: .num_prop #GroupoidWeakHomotopyEquivalence}
###### Definition
**([[weak homotopy equivalence]] of [[groupoids]])

Let $\mathcal{G}_1$ and $\mathcal{G}_2$ be groupoids. Then a morphism (functor)

$$
  F \;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2
$$

is called a _[[weak homotopy equivalence]]_ if

   1. it induces a [[bijection]] on [[connected components]] (def. \ref{GroupoidConnectedComponents}):

      $$
        \pi_0(F) \;\colon\; \pi_0(\mathcal{G}_1) \overset{\simeq}{\longrightarrow} \pi_0(\mathcal{G}_2)
      $$

   1. for each object $x$ of $\mathcal{G}_1$ the morphism

      $$
        F_{x,x} \;\colon\; Aut_{\mathcal{G}_1}(x) \overset{\simeq}{\longrightarrow} Aut_{\mathcal{G}_2}(F_0(X))
      $$

      is an [[isomorphism]] of [[automorphism groups]] (def. \ref{InGrupoidAutomorphismGroup})

=--




+-- {: .num_lemma #AutomorphismGroupDependsOnlyOnConnectedComponent}
###### Lemma
**([[automorphism group]] depends on basepoint only up to [[conjugation]])**

For $\mathcal{G}$ a groupoid, let $x$ and $y$ be two [[objects]] in the
same [[connected component]] (def. \ref{GroupoidConnectedComponents}). Then there is a group [[isomorphism]]

$$
  Aut_{\mathcal{G}}(x) \simeq Aut_{\mathcal{G}}(y)
$$

between their [[automorphism groups]] (def. \ref{InGrupoidAutomorphismGroup}).

=--

+-- {: .proof}
###### Proof

By assumption, there exists some morphism from $x$ to $y$

$$
  x \overset{f}{\longrightarrow} y
  \,.
$$

The operation of [[conjugation]] with this morphism

$$
  \array{
     Aut_{\mathcal{G}}(x)
       &\overset{Ad_{f}}{\longrightarrow}&
     Aut_{\mathcal{G}}(y)
     \\
     g &\mapsto& f^{-1} \circ g \circ f
  }
$$

is clearly a group isomorphism as required.

=--

+-- {: .num_lemma #DeloopingGroupoidEquivalence}
###### Lemma
**([[equivalence of groupoids|equivalences]] between [[coproducts|disjoint unions]] of [[delooping groupoids]])**

Let $\{G_i\}_{i \in I}$ and $\{H_j\}_{j \in J}$ be sets of [[groups]] and consider a homomorphism ([[functor]])

$$
  F
    \;\colon\;
  \underset{i \in I}{\sqcup} B G_i
    \longrightarrow
  \underset{j \in J}{\sqcup} B H_j
$$

between the corresponding disjoint unions of [[delooping groupoids]] (example \ref{GroupoidFromDelooping}).

Then the following are equivalent:

1. $F$ is an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids});

1. $F$ is a [[weak homotopy equivalence]] (def. \ref{GroupoidWeakHomotopyEquivalence}).

=--

+-- {: .proof}
###### Proof


The implication 2) $\Rightarrow 1)$ is immediate.

In the other direction, assume that $F$ is an equivalence of groupoids, and let $G$ be an inverse up to natural isomorphism.
It is clear that both induces bijections on connected components. To see that both are isomorphisms
of automorphisms groups, observe that the conditions for the natural isomorphisms

$$
  \alpha \;\colon\; G \circ F \Rightarrow id
  \phantom{AAAA}
  \beta \;\colon\; F \circ G \Rightarrow id
$$

are in each separate [[delooping groupoid]] $B G_i$ (resp. $B H_j$) of the form

$$
  \array{
    \ast &\overset{\alpha}{\longrightarrow}& \ast
    \\
    {}^{\mathllap{G_{F_0(i),F_0(i)}(F_{i,i}(f))}}\downarrow && \downarrow^{\mathrm{id}}
    \\
    \ast &\underset{\alpha}{\longrightarrow}& \ast
  }
  \phantom{AAAAAAAAAAAAAAAAAAAAA}
  \array{
    \ast &\overset{\beta}{\longrightarrow}& \ast
    \\
    {}^{\mathllap{F_{G_0(j),G_0(j)}(G_{j,j}(f))}}\downarrow && \downarrow^{\mathrm{id}}
    \\
    \ast &\underset{\beta}{\longrightarrow}& \ast
  }
$$

since there is only a single object. But this means $F_{i,i}$ and $G_{j,j}$ are group isomorphisms.

=--

+-- {: .num_prop #EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}
###### Proposition
**(every [[groupoid]] is [[equivalence of groupoids|equivalent]] to a [[disjoint union]] of [[group]] [[deloopings]])

Assuming the [[axiom of choice]], then:

For $\mathcal{G}$ any [[groupoid]], then there exists a [[set]] $\{G_i\}_{i \in I}$ of groups and an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids})

$$
  \mathcal{G} \simeq \underset{i \in I}{\sqcup} B G_i
$$

between $\mathcal{G}$ and a [[disjoint union]] of [[delooping groupoids]] (example \ref{DeloopingGroupoidDisjointUnion}).
This is called a _[[skeleton]]_ of $\mathcal{G}$.

Concretely, this exists for $I = \pi_0(\mathcal{G})$ the set of [[connected components]] of $\mathcal{G}$ (def. \ref{GroupoidConnectedComponents}) and for $G_i \coloneqq Aut_{\mathcal{G}}(x)$ the [[automorphism group]] (def. \ref{InGrupoidAutomorphismGroup}) of any object $x$ in the given connected component.

=--

+-- {: .proof}
###### Proof


Using the [[axiom of choice]] we may find a set $\{x_i\}_{i \in \pi_0(\mathcal{G})}$ of objects of $\mathcal{G}$, with $x_i$ being in the [[connected component]] $i \in \pi_0(\mathcal{G})$.

This choice induces a functor

$$
  inc
   \;\colon\;
  \underset{i \in \pi_0(\mathcal{G})}{\sqcup} Aut_{\mathcal{G}}(x_i)
    \longrightarrow
  \mathcal{G}
$$

which takes each object and morphism "to itself".

Now using the [[axiom of choice]] once more, we choose in each connected component $i \in \pi_0(\mathcal{G})$
and for each object $y$ in that connected component a morphism

$$
  x_i \overset{f_{x_i,y}}{\longrightarrow} y
  \,.
$$

Using this we obtain a functor the other way around

$$
  p \;\colon\; \mathcal{G} \longrightarrow \underset{i \in \pi_0(\mathcal{G})}{\sqcup} Aut_{\mathcal{G}}(x_i)
$$

which sends each object to its connected component, and
which for pairs of objects $y$, $z$ of $\mathcal{G}$ is given by conjugation with the
morphisms choosen above:

$$
  \array{
    Hom_{\mathcal{G}}(y,z) &\overset{p_{y,z}}{\longrightarrow}& & Aut_{\mathcal{G}}(x_i) &
    \\
    \\
    y                 &&                     y & \overset{f_{x_i,y}}{\longleftarrow}& x_i
    \\
    {}^{\mathllap{f}} \downarrow &\mapsto&     {}^{\mathllap{f}}\downarrow
    \\
    z                 &&                     z & \underset{f_{x_i,z}^{-1}}{\longrightarrow} & x_i
  }
  \,.
$$

It is now sufficient to show that there are conjugations/natural isomorphisms

$$
  p \circ inc \simeq id
  \phantom{AAAA}
  inc \circ p \simeq id
  \,.
$$

For the first this is immediate, since we even have equality

$$
  p \circ inc \;=\; id
  \,.
$$

For the second we observe that choosing

$$
  \eta(y) \coloneqq f_{x_i,y}
$$

yields a naturality square by the above construction:

$$
  \array{
    x_i &\overset{f_{x_i,y}}{\longrightarrow}& y
    \\
    {}^{ \mathllap{ f_{x_i,z} \circ f \circ f_{x_i,y}^{-1} } }\downarrow && \downarrow^{\mathrlap{f}}
    \\
    x_i &\underset{f_{x_i,z}}{\longrightarrow}& z
  }
  \,.
$$

=--


+-- {: .num_prop #EquivalenceOfGroupoidsFromWeakHomotopyEquivalence}
###### Proposition
**([[weak homotopy equivalence]] is [[equivalence of groupoids]])

Let $F \;\colon\; \mathcal{G}_1 \longrightarrow \mathcal{G}_2$
be a homomorphism of [[groupoids]].

Assuming the [[axiom of choice]] then the following are equivalent:

1. $F$ is an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids});

1. $F$ is a [[weak homotopy equivalence]] (def. \ref{GroupoidWeakHomotopyEquivalence}).

=--

+-- {: .proof}
###### Proof


In one direction, if $F$ has an inverse up to natural isomorphism, then this induces by definition a bijection
on connected components, and it induces isomorphism on homotopy groups by lemma \ref{AutomorphismGroupDependsOnlyOnConnectedComponent}.

In the other direction, choose equivalences to [[skeleta]] as in prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}
to get a [[commuting diagram]] in the [[1-category]] of groupoids as follows:

$$
  \array{
    \mathcal{G}_1 &\underoverset{\simeq}{inc_1}{\longleftarrow}& \underset{i \in \pi_0(\mathcal{G}_1)}{\sqcup} Aut_{\mathcal{G}_1}(x_i)
    \\
    {}^{\mathllap{F}}\downarrow && \downarrow^{\mathrlap{\tilde F }}
    \\
    \mathcal{G}_2 &\underoverset{inc_2}{\simeq}{\longleftarrow}& \underset{i \in \pi_0(\mathcal{G}_1)}{\sqcup} Aut_{\mathcal{G}_2}(F_0(x_i))
  }
  \,.
$$

Here $inc_1$ and $inc_2$ are equivalences of groupoids by prop. \ref{EveryGroupoidIsEquivalentToDisjointUnionOfGroupDeloopings}.
Moreover, by assumption that $F$ is a weak homotopy equivalence $\tilde F$ is the union of of deloopings of
isomorphisms of groups, and hence has a strict inverse, in particular a homotopy inverse, hence is in particular
an euivalence of groupoids.

In conclusion, when regarded as a diagram in the [[homotopy category]] $Ho(Grpd)$ (def. \ref{HomotopyCategoryOfGroupoids}),
the top, bottom and right moprhism of the above diagram are isomorphisms. It follows that also
$f$ is an isomorphism in $Ho(Grpd)$. But this means exactly that it is a homotopy equivalence of groupoids, by
def. \ref{EquivalenceOfGroupoids}.


=--




## Covering spaces
 {#CoveringSpaces}

A _covering space_ (def. \ref{CoveringSpace} below) is
a "continuous [[fiber bundle]] of sets" over a topological space, in just the same way as
a [[topological vector bundle]] is a "continuous [[fiber bundle]] of vector spaces".

$\,$

+-- {: .num_defn #CoveringSpace}
###### Definition
**([[covering space]])**

Let $X$ be a [[topological space]].
A _[[covering space]]_ over $X$ is a [[continuous function]]

$$
  p \colon E \longrightarrow X
$$

that is [[local trivialization|locally trivial]] in that there exists:

1. an [[open cover]] $\underset{i \in I}{\sqcup}U_i \to X$,

1. for each $i \in I$ a set $F_i$ and a [[homeomorphism]] over $U_i$

$$
  \array{
     U_i \times Disc(F_i) && \overset{\simeq}{\longrightarrow} && \p^{-1}(U_i)
    \\
    & {}_{\mathllap{pr_1}}\searrow && \swarrow_{\mathrlap{p|_{U_i}}}
    \\
    && U_i
  }
$$

   from the [[product topological space]] ([this example](Introduction+to+Topology+--+1#BinaryProductTopologicalSpace)) of $U_i$
with the [[discrete topological space]] ([this example](Introduction+to+Topology+--+1#CoDiscreteTopology)) on $F_i$ to $p|_{U_i}$.


In other words $p \colon E \to X$ is a covering space if there exists a [[pullback|pullback diagram]] in [[Top]] of the form

$$
  \array{
    \underset{i}{\sqcup} U_i \times Disc(F_i) &\longrightarrow&  E
    \\
    \downarrow &(pb)& \downarrow^{\mathrlap{p}}
    \\
    \underset{i \in I}{\sqcup} U_i &\underset{}{\longrightarrow}& X
  }
  \,.
$$

For $x \in U_i \subset X$ a point, the elements in $F_x  = F_i$ are called the _[[leaves]]_ of the covering at $x$.

Given two covering spaces $p_i \colon E_i \to X$ , then a [[homomorphism]] between them is
a [[continuous function]] $f \colon E_1 \to E_2$ between the total covering spaces, which respects
the [[fibers]] in that the following [[commuting diagram|diagram commutes]]

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
  \,.
$$

This defines a [[category]] $Cov(X)$, the _[[category of covering spaces]]_ over $X$, whose

* [[objects]] are the covering spaces over $X$;

* [[morphisms]] are the homomorphisms between these.

=--

+-- {: .num_example #TrivialCoveringSpace}
###### Example
**(trivial covering space)**

For $X$ a [[topological space]] and $S$ a [[set]] with $Disc(S)$ the [[discrete topological space]]
on that set, then the [[projection]] out of the [[product topological space]]

$$
  pr_1 \;\colon\; X \times Disc(S) \longrightarrow X
$$

is a [[covering space]], called the _trivial covering space_ over $X$ with [[fiber]] $Disc(S)$.

If $E \overset{p}{\longrightarrow} X$ is any covering space, then an [[isomorphism]] of covering spaces
of the form

$$
  \array{
    E && \overset{\simeq}{\longrightarrow} && X \times Disc(S)
    \\
    & {}_{\mathllap{p}}\searrow && \swarrow_{\mathrlap{pr_2}}
    \\
    && X
  }
$$

is called a _trivialization_ of $E \overset{p}{\to} X$.

It is in this sense that evry covering space $E$ is, by definition, locally trvializable.

=--


+-- {: .num_example #kForlCovringOfCircle}
###### Example
**(covering of circle by circle)**

<div style="float:left;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/pFoldCoveringOfCircleB.png" width="180">
</div>

Regard the [[circle]] $S^1 = \{ z \in \mathbb{C}  \;\vert\; {\vert z\vert} = 1 \}$ as the [[topological subspace]]
of elements of unit [[absolute value]] in the [[complex plane]].
For $k \in \mathbb{N}^{+}$, consider the continuous function

$$
  p \coloneqq (-)^k \;\colon\; S^1 \longrightarrow S^1
$$

given by taking a complex number to its $k$-th power. This may be thought of as the
result of "winding the circle $k$ times around itself".
Precisely, this is a [[covering space]]
(def. \ref{CoveringSpace}) with $k$ leaves at each point.

> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)


=--


$\,$

$\,$


+-- {: .num_example #CoveringOfCircleByRealLine}
###### Example
**(covering of circle by real line)**

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UniversalCoveringOfCircle.png" width="150">
</div>

Consider the [[continuous function]]

$$
  \exp(2 \pi i(-)) \;\colon\; \mathbb{R}^1 \longrightarrow S^1
$$

from the [[real line]] to the [[circle]],
which,

1. with the circle regarded as the unit circle in the [[complex plane]] $\mathbb{C}$, is given by

   $$
     t \mapsto \exp(2\pi i t)
   $$

1. with the circle regarded as the unit circle in $\mathbb{R}^2$, is given by

   $$
     t \mapsto ( cos(2\pi t), sin(2\pi t) )
     \,.
   $$

We may think of this as the result of "winding the line around the circle ad infinitum".
Precisely, this is a [[covering space]] (def. \ref{CoveringSpace}) with the [[leaves]] at each point forming the
set $\mathbb{Z}$ of [[integers]].

Below in example \ref{UniversalCoveringRealLineOfCircle} we see that this is the _[[universal covering space]]_
&#243;f the circle.

=--


$\,$

Here are some basic properties of covering spaces:



+-- {: .num_prop #CoveringProjectionsAreOpenMaps}
###### Proposition
**(covering projections are [[open maps]])**

If $p \colon E \to X$ is a covering space projection, then $p$ is an [[open map]].


=--

+-- {: .proof}
###### Proof

By definition of covering space there exists an [[open cover]] $\{U_i \subset X\}_{i \in I}$ and [[homeomorphisms]] $p^{-1}(U_i) \simeq U_i \times Disc(F_i)$ for all $i \in I$. Since the [[projections]] out of a [[product topological space]] are [[open maps]] ([this prop.](Introduction+to+Topology+--+1#ProjectionsAreOpenContinuousFunctions)), it follows that $p$ is an open map when restricted to any of the $p^{-1}(U_i)$. But a general open subset $W \subset E$ is the union of its restrictions to these subspaces:

$$
  W = \underset{i \in I}{\cup} (W \cap p^{-1}(U_i))
  \,.
$$

Since images preserve unions ([this prop.](interactions+of+images+and+pre-images+with+unions+and+intersections#PreservationOfUnionsAndIntersectionsOfSets)) it follows that

$$
  p(W) = \underset{i \in I}{\cup} p(W \cap p^{-1}(U_i))
$$

is a union of open sets, and hence itself open.

=--

+-- {: .num_lemma #CoveringSpaceFiberwiseDiagonalOpenAndClosed}
###### Lemma
**([[fiber product|fiber-wise]] [[diagonal]] of covering space is [[open subset|open]] and [[closed subset|closed]])**

Let $E \overset{p}{\to} X$ be a covering space. Consider the [[fiber product]]

$$
  E \times_X E \coloneqq \{ (e_1, e_2) \in E \times E \;\vert\; p(e_1) = p(e_2) \}
$$

hence (by the discussion at [Top - Universal constructions](Top#UniversalConstructions)) the [[topological subspace]] of the [[product space]] $E \times E$, as shown on the right. By the [[universal property]] of the [[fiber product]], there is the [[diagonal]] [[continuous function]]

$$
  \array{
    E &\longrightarrow& E \times_X E
    \\
    e &\mapsto& (e,e)
  }
  \,.
$$

Then the [[image]] of $E$ under this function is an [[open subset]] and a [[closed subset]]:

$$
  \Delta(E) \subset E \times_X E
  \;\;\;
  \text{is open and closed}
  \,.
$$

=--

+-- {: .proof}
###### Proof

First to see that it is an open subset. It is sufficient to show that for any $e \in E$ there exists an open neighbourhood of $(e,e) \in E \times_X E$.

Now by definition of covering spaces, there exists an open neighbourhood $U_{p(e)} \subset X$ of $p(e) \in X$ such that

$$
  \array{
    U_{p(e)} \times Disc(p^{-1}(p(e)))
      && \overset{\simeq}{\longrightarrow} && E\vert_{U_{p(e)}}
    \\
    & {}_{\mathllap{pr_1}}\searrow && \swarrow_{\mathrlap{p}}
    \\
    && U_{p(e)}
  }
  \,.
$$

It follows that $U_{p(e)} \times \{e\} \subset E$ is an open neighbourhood. Hence by the nature of the [[product topology]], $U_{p(e)} \times U_{p(e)} \subset E \times E$ is an open neighbourhood of $(e,e)$ in $E \times E$ and hence by the nature of the [[subspace topology]] the restriction

$$
  (E \times_X E) \cap (U_{p(e)} \times U_{p(e)}) \subset E \times_X E
$$

is an open neighbourhood of $(e,e)$ in $E \times_X E$.

Now to see that the diagonal is closed, hence that the complement $(E \times_X E) \setminus \Delta(E)$ is an open subset, it is sufficient to show that every point $(e_1, e_2)$ with $e_1 \neq e_2$ but $p(e_1) = p(e_2)$ has an open neighbourhood in this complement.

As before, there is an open neighbourhood $U \subset X$ of $p(e_1) = p(e_2)$ over which the cover trivializes, and hence $U \times \{e_1\}, U \times \{e_2\} \subset E$ are open neighbourhoods of $e_1$ and $e_2$, respectively. These are disjoint by the assumption that $e_1 \neq e_2$. As above, this means that the intersection

$$
  (E \times_X E) \cap ( (U \times \{e_1\}) \times (U \times \{e_2\}) )
  \subset
  (E \times_X E) \setminus \Delta(E)
$$

is an open subset of the complement of the diagonal in the fiber product.


=--


$\,$

### Lifting properties

If $E \overset{p}{\longrightarrow} X$ is any [[continuous function]]
(possibly a [[covering space]] or a [[topological vector bundle]]) then a _[[section]]_ is
a continuous function $\sigma \colon  X \to E$ which sends each point in the base
to a point in the [[fiber]] above it, hence which makes this [[commuting diagram|diagram commute]]:

$$
  \array{
    && E
    \\
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    X &=& X
  }
  \,.
$$

We may think of this as "lifting" each point in the base to point in the fibers "through" the
projection map $p$. More generally if $Y \hookrightarrow X$ is a subspace,
we may consider such lifts only over $Y$

$$
  \array{
    && E
    \\
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &\hookrightarrow& X
  }
$$

sometimes called a "local section". But this suggests that for $Y \overset{f}{\longrightarrow} X$
any continuous function, we consider "lifting its image through $p$"

$$
  \array{
    && E
    \\
    &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    Y &\underset{f}{\longrightarrow}& X
  }
  \,.
$$

For example if $Y = [0,1]$ is the [[topological interval]], then $f \colon [0,1] \to X$
is a [[path]] in the base space $X$, and a lift through $p$ of this is a path in the total
space which "runs above" the given path. Such lifts of paths through covering projections
is the topic of _[[monodromy]]_ [below](#Monodromy).

Here it is of interest to consider the lifting problem subject to some constraint.
For instance we will want to consider lifts of paths $\gamma \colon [0,1] \to X$
through a covering projection, subject to the condition that the
starting point $\gamma(0)$ is lifted to a prescribed point $p \in E$.

Since such a point is equivalently a continuous function $const_p \colon \ast \to X$
out of the [[point space]],
this is the same as asking for a continuous function $\sigma$ that makes both triangles in the
following [[diagram]] [[commuting diagram|commute]]:

$$
  \array{
    \ast &\overset{const_p}{\longrightarrow}& E
    \\
    {}^{\mathllap{const_0}}\downarrow &{}^{\mathllap{\sigma}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
  \,.
$$

This is an example of a general situation which plays a central role in
[[homotopy theory]]: We say that a square [[commuting diagram]]

$$
  \array{
    A &\longrightarrow& E
    \\
    {}^{\mathllap{i}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    B &\longrightarrow& X
  }
$$

is a _[[lifting problem]]_ and that a diagonal morphism

$$
  \array{
    A &\longrightarrow& E
    \\
    {}^{\mathllap{i}}\downarrow &\nearrow& \downarrow^{\mathrlap{p}}
    \\
    B &\longrightarrow& X
  }
$$

such that both resulting triangles commute is a _[[lift]]_. If such a lift exists for
for the given $p$ and for each $i$ taken from some [[class]] of morphisms, then one says that $p$ has the _[[right lifting property]]_
against this class.


We now discuss some [[right lifting properties]] satisfied by covering spaces:

1. [homotopy-lifting propery](#HomotopyLiftingPropertyOfCoveringSpaces),

1. the [lifting theorem](#TheTheoremLifting).

A first application of the lifting theorem is that it gives the concept of the _[[universal covering space]]_
(def. \ref{UniversalCoveringSpace}, prop. \ref{UniversalCoveringSpaceUniqueUpToIsomorphism} below)
which is central to the theory of coverign spaces.

These lifting properties will be used in [below](#Examples) for the computation of [[fundamental groups]]
and higher [[homotopy groups]] of some topological spaces.


$\,$



+-- {: .num_lemma #LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}
###### Lemma
**([[lifts]] out of [[connected topological space|connected space]] into [[covering spaces]] are unique relative to any point)**

Let

1. $E \overset{p}{\to} X $ be a covering space,

1. $Y$ a [[connected topological space]]

1. $f \;\colon\; Y \longrightarrow X$ a [[continuous function]].

1. $\hat f_1, \hat f_2 \;\colon\; Y \longrightarrow E$ two [[lifts]] of $f$, in that the following [[commuting diagram|diagram commutes]]:

   $$
     \array{
       && E
       \\
       & {}^{\mathllap{\hat f_i}}\nearrow & \downarrow^{\mathrlap{p}}
       \\
       Y &\underset{f}{\longrightarrow}& X
     }
   $$

   for $i \in \{1,2\}$.

If there exists $y \in Y$ such that $\hat f_1(y) = \hat f_2(y)$ then the two lifts already agree everywhere: $\hat f_1 = \hat f_2$.

=--

+-- {: .proof}
###### Proof

By the [[universal property]] of the [[fiber product]]

$$
  E \times_X E \coloneqq \left\{ (e_1, e_2) \in E \times E \;\vert\; p(e_1) = p(e_2) \right\} \subset E \times E
$$

the two lifts determine a single continuous function of the form

$$
  (\hat f_1, \hat f_2)
    \;\colon\;
  Y \longrightarrow E \times_X E
  \,.
$$

Write

$$
  \Delta(E)  \coloneqq \left\{ (e,e) \in E \times_X E \;\vert\; e \in E  \right\}
$$

for the [[diagonal]] on $E$ in the fiber product. By lemma \ref{CoveringSpaceFiberwiseDiagonalOpenAndClosed} this is an open subset and a closed subset of the fiber product space. Hence by continuity of $(\hat f_1, \hat f_2)$ also its pre-image

$$
  (\hat f_1, \hat f_2)^{-1}(\Delta(E)) \subset Y
$$

is both closed and open, hence also its [[complement]] is open in $Y$.

Moreover, the assumption that the functions $\hat f_1$ and $\hat f_2$ agree in at least one point means that the above pre-image is [[inhabited set|non-empty]]. Therefore the assumption that $Y$ is [[connected topological space|connected]] implies that this pre-image coincides with all of $Y$. This is the statement to be proven.

=--



+-- {: .num_lemma #CoveringSpacePathLifting}
###### Lemma
**(path lifting property)**

Let $p \colon E \to X$ be any [[covering space]].  Given

1. $\gamma \colon [0,1] \to X$ a [[path]] in $X$,

1. $\hat x_0 \in E$ be a lift of its starting point, hence such that $p(\hat x_0) = \gamma(0)$

then there exists a unique path $\hat \gamma \colon [0,1] \to E$ such that

1. it is a lift of the original path: $p \circ \hat \gamma = \gamma$;

1. it starts at the given lifted point: $\hat \gamma(0) = \hat x_0$.

In other words, every [[commuting diagram]] in [[Top]] of the form

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow && \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
$$

has a unique [[lift]]:

$$
  \array{
    \{0\} &\overset{\hat x_0}{\longrightarrow}& E
    \\
    \downarrow
      &{}^{\mathllap{\hat \gamma}}\nearrow&
    \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{\gamma}{\longrightarrow}& X
  }
  \,.
$$

=--

+-- {: .proof}
###### Proof


First consider the case that the covering space is trival, hence of the [[Cartesian product]] form

$$
  pr_1 \;\colon\;  X \times Disc(S) \longrightarrow X
  \,.
$$

By the [[universal property]] of the [[product topological spaces]]
in this case a lift $\hat \gamma \colon [0,1] \to X \times Disc(S)$ is equivalently a [[pair]] of continuous functions

$$
  pr_1(\hat \gamma) \colon [0,1] \to X  \phantom{AAAA} pr_2(\hat \gamma) \colon [0,1] \to Disc(S)
  \,,
$$

Now the lifting condition explicitly fixes $pr_1(\hat \gamma) = \gamma$. Moreover, a continuous function into a [[discrete topological space]] $Disc(S)$ is [[locally constant function|locally constant]], and since $[0,1]$ is a [[connected topological space]] this means that $pr_2(\hat \gamma)$ is in fact a [[constant function]] ([this example](connected+space#LocallyConstantFunctionsOnConnectedSpaces)), hence uniquely fixed to be $pr_2(\hat \gamma) = \hat x_0$.

This shows the statement for the case of trivial covering spaces.

Now consider any covering space $p \colon E \to X$. By definition of covering spaces, there exists for every point $x \in X$ a [[open neighbourhood]] $U_x \subset X$ such that the restriction of $E$ to $U_x$ becomes a trivial covering space:

$$
  p^{-1}(U_x) \simeq U_x \times Disc(p^{-1}(x))
  \,.
$$

Consider such a choice

$$
  \{U_x \subset X\}_{x \in X}
  \,.
$$

This is an [[open cover]] of $X$. Accordingly, the [[pre-images]]

$$
  \left\{
    \gamma^{-1}(U_x)
    \subset
    [0,1]
  \right\}_{x \in X}
$$

constitute an open cover of the [[topological interval]] $[0,1]$.

Now the [[closed interval]] is a [[compact topological space]], so that this cover has a finite open subcover. By the [[Euclidean space|Euclidean]] [[metric topology]], each element in this finite subcover is a disjoint union of open intervals. The collection of all these open intervals is an open refinement of the original cover, and by compactness it once more has a finite subcover, now such that each element of the subcover is guaranteed to be a single open interval.

This means that we find a [[finite number]] of points

$$
  t_0 \lt t_1 \lt \cdots \lt_{n+1} \in [0,1]
$$

with $t_0 = 0$ and $t_{n+1} = 1$ such that for all $0 \lt j \leq n$ there is $x_j \in X$ such that the corresponding path segment

$$
  \gamma([t_j, t_{j+1}]) \subset X
$$

is contained in $U_{x_j}$ from above.

Now assume that $\hat \gamma\vert_{[0,t_j]}$ has been found. Then by the triviality of the covering space over $U_{x_j}$ and the first argument above, there is a unique lift of $\gamma\vert_{[t_j, t_{j+1}]}$ to a continuous function $\hat \gamma|_{[t_j,t_{j+1}]}$ with starting point $\hat \gamma(t_j)$. Since $[0,t_{j+1}]$ is the [[pushout]] $[0,t_j] \underset{\{t_j\}}{\sqcup} [t_j,t_{j+1}]$ ([this example](Top#TopologicalnSphereIsPushoutOfBoundaryOfnBallInclusionAlongItself)), it follows that $\hat \gamma|_{[0,t_j]}$ and $\hat \gamma\vert_{[t_j,t_{j+1}]}$ uniquely glue to a continuous function $\hat \gamma\vert_{[0,t_{j+1}]}$ which lifts $\gamma\vert_{[0,t_{j+1}]}$.

By [[induction]] over $j$, this yields the required lift $\hat \gamma$.

Conversely, given any lift, $\hat \gamma$, then its restrictions $\hat \gamma\vert_{[t_j, t_{j+1}]}$ are uniquely fixed by the above inductive argument. Therefore also the total lift is unique. Altrnatively, uniqueness of the lifts is a special case of lemma \ref{LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}.

=--

+-- {: .num_prop #HomotopyLiftingPropertyOfCoveringSpaces}
###### Proposition
**([[homotopy lifting property]] of [[covering spaces]])**

Let

1. $E \overset{p}{\to} X$ be a covering space;

1. $Y$ a [[topological space]].

Then every [[lifting problem]] of the form

$$
  \array{
    Y &\overset{\hat f}{\longrightarrow}& E
    \\
    {}^{\mathllap{ (id_y, const_0)}}\downarrow && \downarrow^{\mathrlap{p}}
    \\
    Y \times [0,1] &\underset{\eta}{\longrightarrow}& X
  }
$$

has a unique [[lift]]

$$
  \array{
    Y &\overset{\hat f}{\longrightarrow}& E
    \\
    {}^{\mathllap{ (id_y, const_0)}}\downarrow
     &{}^{\mathllap{\hat \eta}}\nearrow&
    \downarrow^{\mathrlap{p}}
    \\
    Y \times [0,1] &\underset{\eta}{\longrightarrow}& X
  }
  \,.
$$


=--

+-- {: .proof}
###### Proof

It is clear what the lift must be:
For every point $y \in Y$ the situation restricts to that of path lifting

$$
  \array{
    \ast &\overset{const_y}{\longrightarrow}& Y &\overset{f}{\longrightarrow}& E
    \\
    {}^{\mathllap{const_0}}\downarrow
    &&
    {}^{\mathllap{ (id_y, const_0)}}\downarrow
     &{}^{\mathllap{\hat \eta}}\nearrow&
    \downarrow^{\mathrlap{p}}
    \\
    [0,1] &\underset{(const_y,id)}{\longrightarrow}& Y \times [0,1] &\underset{\eta}{\longrightarrow}& X
  }
  \,.
$$

And so at each point $y \in Y$ the lift of $\eta(x,-)$ must be the unique path that lifts this
with starting point $\hat \hat f(y)$. We just need to see that this lift is a continuous function.

To that end we generalize he proof of the path lifting to connected open neighbourhoods
of points in $Y$:

Let $\{U_i \subset X\}_{i \in I}$ be an open cover over which the covering space trivializes. Then the pre-images $\{\eta^{-1}(U_i) \subset Y \times [0,1]\}_{i \in I}$ is an open cover of the product space. By nature of the [[product space|product space topology]] and the [[Euclidean topology]] on $[0,1]$, each of the $\eta^{-1}(U_i)$ is a union of Cartesian products $V_j \times I_j$ with $V_i \subset Y$ an open subset of $Y$ and $I_i \subset [0,1]$ an interval. Hence there is an open cover of the form

$$
  \{
    V_j \times I_j \subset Y \times [0,1]
  \}_{j \in J}
$$

with the property that for each $j$ there exists $i \in I$ with $\eta(V_j \times I_j) \subset U_i$.

Now by the fact that $[0,1]$ is a [[compact topological space]], for each $y \in Y$ there exists a finite set $K_y \subset J$ such that

$$
  \{ V_k \times I_k \}_{k \in K_y \subset K}
$$

still restricts to a cover of $\{y\} \times [I]$. Since $K$ is finite, the intersection

$$
  V_y \;\coloneqq\; \underset{k \in K_y}{\cap}
$$

is still open, and so also

$$
  \{ V_y \times I_k \}_{k \in K_y}
$$

still restricts to a cover of $\{y\} \times [0,1]$.

This means that the same argument as for the path lifting in lemma \ref{CoveringSpacePathLifting}
provides a unique lift $\widehat{\eta\vert_{V_y \times [0,1]}}$ for each $y \in Y$.

Moreover, for $y_1, y_2 \in Y$ two points, these lifts clearly have to agree on $V_{y_1} \cap V_{y_2}$.

Since $\{V_y \times [0,1] \subset Y \times [0,1]\}_{y \in Y}$ is an open cover, means that there is a unique function $\hat \eta$ that restricts to all these local lifts ([this prop](Top#ClosedSubspacesGluing)). This is the required lift.


=--



+-- {: .num_remark #CoveringSpacesAreSerreFibrationsButNotInGeneralHurewiczFibrations}
###### Remark
**([[covering spaces]] are [[Hurewicz fibrations]])**

Continuous functions that satisfy the [[homotopy lifting property]], hence that
have the [[right lifting property]] against continuous functions of the form
$Y \overset{(id, const_0)}{\longrightarrow} Y \times [0,1]$
are called _[[Hurewicz fibrations]]_. Hence prop. \ref{HomotopyLiftingPropertyOfCoveringSpaces}
says that covering projections are in particular Hurewicz fibrations.

=--



+-- {: .num_example #CoveringSpacesHomotopyLifting}
###### Example
**([[homotopy  lifting property]] for given lifts of paths relative starting point)**

Let $p \colon E \to X$ be a [[covering space]]. Then given a [[homotopy]] relative the starting point between two [[paths]] in $X$,

$$
  \eta \;\colon\; \gamma_1 \Rightarrow \gamma_2
$$

there is for every lift $\hat \gamma_1, \hat \gamma_2$ of these two paths to paths in $E$ with the same starting point a unique homotopy

$$
  \hat \eta \;\colon\; \hat \gamma_1 \Rightarrow \hat \gamma_2
$$

between the lifted paths that lifts the given homotopy:

For [[commuting squares]] of the form

$$
  \array{
    ([0,1] \times \{0\}) \cup (\{0,1\} \times [0,1])
      &\overset{(\gamma_1, \gamma_2)}{\longrightarrow}&
    E
    \\
    {}^{\mathllap{}}\downarrow
      &{}^{\mathllap{\hat \eta}}\nearrow&
    \downarrow^{\mathrlap{p}}
    \\
    [0,1] \times [0,1] &\underset{\eta}{\longrightarrow}& X
  }
$$

there is a unique diagonal [[lift]] in the lower diagram, as shown.

Moreover if the homotopy $\eta$ also fixes the endpoint, then so does the lifted homotopy $\hat \eta$.


=--

+-- {: .proof}
###### Proof

There are horizontal [[homeomorphisms]] such that the following diagram commutes

$$
  \array{
     [0,1]
       &\overset{\simeq}{\longrightarrow}&
     ([0,1] \times \{0\}) \cap ( \{0,1\} \times [0,1] )
     \\
     \downarrow
     &&
     \downarrow
     \\
     [0,1] \times [0,1] &\underset{\simeq}{\longrightarrow}& [0,1] \times [0,1]
  }
  \,.
$$

With this the statement follows from \ref{HomotopyLiftingPropertyOfCoveringSpaces}.

=--

+-- {: .num_example #IfFundamentalGroupsIncludeThenfLoopsLiftToLoops}
###### Example


Let $(E,e) \overset{p}{\longrightarrow} (X,x)$ be a [[pointed topological space|pointed]] [[covering space]]
and let $f \colon (Y,y) \longrightarrow (X,x)$ be a point-preserving [[continuous function]] such that the image of the [[fundamental group]] of $(Y,y)$ is contained within the image of the fundamental group of $(E,e)$ in that of $(X,x)$:

$$
  f_\ast(\pi_1(Y,y)) \subset p_\ast(\pi_1(E,e))
  \phantom{AA}
  \subset
  \pi_1(X,x)
  \,.
$$

Then for $\ell_Y$ a [[path]] in $(Y,y)$ that happens to be a [[loop]], every lift of its image path $f \circ \ell$ in $(X,x)$ to a path $\widehat{f\circ \ell_Y}$ in $(E,e)$ is also a loop there.

=--

+-- {: .proof}
###### Proof

By assumption, there is a loop $\ell_E$ in $(E,e)$ and a homotopy fixing the endpoints of the form

$$
  \eta_{X} \;\colon\; p \circ \ell_E \Rightarrow f\circ \ell_Y
  \,.
$$

Then by the homotopy lifting property as in example \ref{CoveringSpacesHomotopyLifting}, there is a homotopy in $(E,e)$ relative
to the basepoint

$$
  \eta_{E} \;\colon\; \ell_E \Rightarrow \widehat{f \circ \ell_Y}
$$

and lifting the homotopy $\eta_X$. Therefore $\eta_E$ is in fact a homotopy between loops, and so $\widehat{f \circ \ell_Y}$ is indeed a loop.

=--

+-- {: .num_prop #TheTheoremLifting}
###### Proposition
**(lifting theorem)**

Let

1. $p \colon E \to X$ be a [[covering space]];

1. $e \in E$ a point, with $x \coloneqq p(e)$ denoting its image,

1. $Y$ be a [[connected topological space|connected]] and [[locally path-connected topological space|locally path-connected]] [[topological space]];

1. $y \in Y$ a point

1. $f \colon (Y,y) \longrightarrow (X,x)$ a [[continuous function]] such that $f(y) = x$.

Then the following are equivalent:

1. There exists a unique lift $\hat f$ in the diagram

   $$
     \array{
       && (E,e)
       \\
       & {}^{\mathllap{\hat f}}\nearrow & \downarrow^{\mathrlap{p}}
       \\
       (Y,y) &\underset{f}{\longrightarrow}& (X,x)
     }
   $$

   of [[pointed topological spaces]].

1. The [[image]] of the [[fundamental group]] of $Y$ under $f$ in that of $X$ is contained in the image of the fundamental group of $E$ under $p$:

   $$
     f_\ast(\pi_1(Y,y)) \subset p_\ast( \pi_1(E,e) )
     \,
   $$

Moreover, if $Y$ is path-connected, then the lift in the first item is unique.


=--

+-- {: .proof}
###### Proof

The implication $1) \Rightarrow 2)$ is immediate. We need to show that the second statement already implies the first.

So assume that $f_\ast(\pi_1(Y,y)) \subet p_\ast(\pi_1(E,e))$.
If a lift exists, then its uniqueness is given by lemma \ref{LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}.
Hence we need to exhibit a lift.

Since $Y$ is connected and locally path-connected, it is also a [[path-connected topological space]] ([this prop.](locally+path-connected+space#ForLocallyPathConnectedTheConnectedComponentsCoincideWithThePathConnectedComponents)). Hence for every point $y' \in Y$ there exists a [[path]] $\gamma$ connecting $y$ with $y'$ and hence a path $f \circ \gamma$ connecting $x$ with $f(y')$.  By the path-lifting property (lemma \ref{CoveringSpacePathLifting}) this has a unique lift

$$
  \array{
    \{0\} &\overset{e}{\longrightarrow}& E
    \\
    \downarrow &{}^{\mathllap{\widehat{f \circ \gamma}}}\nearrow& \downarrow^{\mathrlap{p}}
    \\
    [0,1]
     &\underset{f \circ \gamma}{\longrightarrow}&
    X
  }
  \,.
$$

Therefore

$$
  \hat f(y') \coloneqq \widehat{f \circ \gamma}(1)
$$

is a lift of $f(y')$.

We claim now that this pointwise construction is independent of the choice $\gamma$, and that as a function of $y'$ it is indeed continuous. This will prove the claim.

First, by the path lifting lemma \ref{CoveringSpacePathLifting} the lift $\widehat{\f \circ \gamma}$ is unique given $f \circ \gamma$, and hence $\hat f(y')$ depends at most on the choice of $\gamma$.

Hence let $\gamma' \colon [0,1] \to Y$ be another path in $Y$ that connects $y$ with $y'$. We need to show that then $\widehat{f \circ \gamma'} = \widehat{f \circ \gamma}$.

First observe that if $\gamma'$ is related to $\gamma$ by a [[homotopy]], so that then also $f \circ \gamma'$ is related to $f \circ \gamma$ by a homotopy, then this is the statement of the homotopy lifting property in the form of example \ref{CoveringSpacesHomotopyLifting}.

Next write $\bar\gamma'\cdot \gamma$ for the [[path concatenation]] of the path $\gamma$ with the [[reverse path]] of the path $\gamma'$.
This is hence a loop in $Y$, and so $f \circ (\bar\gamma'\cdot \gamma)$ is a loop in $X$. The assumption that $f_\ast(\pi_1(Y,y)) \subset p_\ast(\pi_1(E,e))$ implies, via example \ref{IfFundamentalGroupsIncludeThenfLoopsLiftToLoops}, that the path $\widehat{f \circ (\bar \gamma' \cdot \gamma)}$ which lifts this loop to $E$ is itself a loop in $E$.

By uniqueness of path lifting, this means that the lift of

$$
  f \circ ( \gamma' \cdot (\bar\gamma' \cdot \gamma) )
  =
  (f \circ \gamma') \cdot (f \circ (\bar \gamma' \cdot \gamma) )
$$

coincides
at $1 \in [0,1]$ with that of $f \circ \gamma'$ at 1. But $\gamma' \cdot (\bar \gamma' \cdot \gamma)$ is homotopic (via reparameterization) to just $\gamma$. Hence it follows now with the first statement that the lift of $f \circ \gamma'$ indeed coincides with that of $f \circ \gamma$.

This shows that the above prescription for $\hat f$ is well defined.

It only remains to show that the function $\hat f$ obtained this way is continuous.

Let $y' \in Y$ be a point and $W_{\hat f(y')} \subset E$ an open neighbourhood of its image in $E$. It is sufficient to see that there is an open neighbourhood $V_{y'} \subset Y$ such that $\hat f(V_y) \subset W_{\hat f(y')}$.

Let $U_{f(y')} \subset X$ be an open neighbourhood over which $p$ trivializes. Then the restriction

$$
  p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
    \;\subset\;
  U_{f(y')} \times Disc(p^{-1}(f(y')))
$$

is an open subset of the product space. Consider its further restriction

$$
  \left( U_{f(y')} \times \{\hat f(y')\} \right)
    \cap
  \left(
    p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
  \right)
$$

to the [[leaf]]

$$
  U_{f(y')} \times \{\hat f(y')\} \;\subset\; U_{f(y')} \times p^{-1}(f(y'))
$$

which is itself an open subset. Since $p$ is an [[open map]] ([this prop.](covering+space#CoveringProjectionsAreOpenMaps)), the subset

$$
  p\left(
    \left(
      U_{f(y')} \times \{\hat f(y')\}
    \right)
      \cap
    \left(
      p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
    \right)
  \right)
  \subset X
$$

is open, hence so is its pre-image

$$
  f^{-1}
  \left(
    p
      \left(
        \left(
          U_{f(y')} \times \{\hat f(y')\}
        \right)
          \cap
        \left(
          p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
        \right)
    \right)
  \right)
    \;\subset\;
  Y
  \,.
$$


Since $Y$ is assumed to be [[locally path-connected topological space|locally path-connected]], there exists a path-connected open neighbourhood

$$
  V_{y'}
    \subset
  f^{-1}\left(p\left(
    \left(U_{f(y')} \times \{\hat f(y')\}\right)
      \cap
    \left(
      p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
    \right)
  \right)
  \right)
  \,.
$$

By the uniqueness of path lifting, the image of that under $\hat f$ is

$$
  \begin{aligned}
    \hat f(V_{y_'})
    & =
    f(V_{y'}) \times \{\hat f(y')\}
    \\
     & \subset
    p\left(
      \left(U_{f(y')} \times \{\hat f(y')\}\right)
        \cap
      \left(
        p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
      \right)
    \right) \times \{\hat f(y')\}
    \\
    & \simeq
      \left( U_{f(y')} \times \{\hat f(y')\} \right)
        \cap
      \left(
        p^{-1}(U_{f(y')}) \cap W_{\hat f(y')}
      \right)
     \\
     & \subset W_{\hat f(y')}
  \end{aligned}
  \,.
$$

This shows that the lifted function is continuous. Finally that this continuous lift is unique is the statement of lemma \ref{LiftsOverConnectedSpaceIntoCoveringSpaceAreUniqueRelativePoint}.

=--


The lifting theorem implies that there are "universal" covering spaces:

+-- {: .num_defn #UniversalCoveringSpace}
###### Definition
**([[universal covering space]])**

A [[covering space]] $E \overset{p}{\to} X$ is called a _[[universal covering space]]_
if the total space $E$ is a [[simply connected topological space]] (def. \ref{SimplyConnected})

=--

It makes sense to speak of _[[generalized the|the]]_ universal covering space, because any two
are isomorphic:

+-- {: .num_prop #UniversalCoveringSpaceUniqueUpToIsomorphism}
###### Proposition
**([[universal covering space]] is unique up to [[isomorphism]])**

For $X$ a [[locally path-connected topological space]], then any two [[universal covering spaces]] over
$X$ (def. \ref{UniversalCoveringSpace}) are isomorphic.

=--

+-- {: .proof}
###### Proof


Since both $E_1$ and $E_2$ are simply connected, the assumption of the lifting theorem for covering spaces is satisfied
(prop. \ref{TheTheoremLifting}). This says that there are horizontal continuous function making the following diagrams commute:

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
  \phantom{AAAAAA}
  \array{
    E_2 && \overset{g}{\longrightarrow} && E_1
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

$$
  \array{
    E_i && \overset{id}{\longrightarrow} && E_i
    \\
    & {}_{\mathllap{p_i}}\searrow && \swarrow_{\mathrlap{p_i}}
    \\
    && X
  }
$$

and that these are _unique_ once we specify the image of a single point, which we may freely do (in the given fiber).

So if we pick any point $x \in X$ and $\hat x_1 \in E_1$ with $p(\hat x) = x$ and $\hat x_2 \in E_2$ with $p(\hat x_2) = x$ and specify that $f(\hat x_1) = \hat x_2$ and $g(\hat x_2) = \hat x_1$ then uniqueness applied to the composites implies $f \circ g = id_{E_{2}}$ and $g \circ f = id_{E_1}$.


=--

+-- {: .num_example #UniversalCoveringRealLineOfCircle}
###### Example
**([[universal covering space]] of the [[circle]])**

The [[real line]], which is simply connected by example \ref{SimplyConnectedEuclideanSpace},
equipped with the projection from example \ref{CoveringOfCircleByRealLine}

$$
  \exp(2 \pi i(-)) \;\colon\; \mathbb{R}^1 \longrightarrow S^1
$$

is [[generalized the|the]] (prop. \ref{UniversalCoveringSpaceUniqueUpToIsomorphism}) [[universal covering space]]
of the [[circle]].
=--




### Monodromy
 {#Monodromy}

Since the lift of a path through a [[covering space]] [[projection]] is unique once the lift of the
starting point is chosen (lemma \ref{CoveringSpacePathLifting}) every path in the base space
determines a [[function]] between the [[fiber]] [[sets]] over its endpoints. By the
[[homotopy lifting property]] of covering spaces as in example \ref{CoveringSpacesHomotopyLifting}
this function only depends on the [[equivalence class]] of the path under [[homotopy relative boundary]].
Therefore this fiber-assignment is in fact an _[[action]]_ of the [[fundamental groupoid]] of the base space on sets,
called a _[[groupoid representation]]_ (def. \ref{GroupoidRepresentation} below).
In particular, associated with any homotopy-class
of a [[loop]], hence of an element in the [[fundamental group]], there is associated a
[[bijection]] of the fiber over the loop's basepoint with itself, hence a [[permutation representation]]
of the [[fundamental group]]. This is called the _[[monodromy]]_ of the covering space.
It is a measure for how the coverign space fails to be globally trivial.

In fact the [[fundamental theorem of covering spaces]] (prop. \ref{FundamentalTheoremOfCoveringSpaces})
below says that the [[monodromy]] representation characterizes the covering spaces completely
and faithfully. This means that covering spaces may be dealt with completely with tools from
[[group theory]] and [[representation theory]], a fact that we make use of in the computation of
examples [below](#Examples).

$\,$

+-- {: .num_defn #GroupoidRepresentation}
###### Definition
**([[groupoid representation]])

Let $\mathcal{G}$ be a [[groupoid]]. Then:

A [[linear representation]] of $\mathcal{G}$ is a groupoid homomorphism ([[functor]])

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Vect)
$$

to the groupoid [[core]] of the category [[Vect]] of [[vector spaces]] (example \ref{CoreGroupoid}). Hence this is

1. For each object $x$ of $\mathcal{G}$ a [[vector space]] $V_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[linear map]] $\rho(f) \;\colon\; V_x \to V_y$

such that

1. (respect for composition) for all composable morphisms $x \overset{f}{\to}y \overset{g}{\to} z$ in the
   groupoid we have an [[equality]]

   $$
     \rho(g) \circ \rho(f) = \rho(g \circ f)
   $$

1. (respect for identities) for each object $x$ of the groupoid we have an equality

   $$
     \rho(id_x) = id_{V_x}
     \,.
   $$

Similarly a _[[permutation representation]]_ of $\mathcal{G}$ is a groupoid homomorphism ([[functor]])

$$
  \rho \;\colon\; \mathcal{G} \longrightarrow Core(Set)
$$

to the groupoid core of [[Set]]. Hence this is

1. For each object $x$ of $\mathcal{G}$ a [[set]] $S_x$;

1. for each morphism $x \overset{f}{\longrightarrow} y$ of $\mathcal{G}$ a
   [[function]] $\rho(f) \;\colon\; S_x \to S_y$

such that composition and identities are respected, as above.

For $\rho_1$ and $\rho_2$ two such representations, then a homomorphism of representations

$$
  \phi \;\colon\; \rho_1 \longrightarrow \rho_2
$$

is a [[natural transformation]] between these functors, hence is

* for each object $x$ of the groupoid a (linear) function

  $$
    (V_1)_x \overset{\phi(x)}{\longrightarrow} (V_2)_x
  $$

* such that for all morphisms $x \overset{f}{\longrightarrow} y$
  we have

  $$
    \phi(y) \circ \rho_1(f) = \rho_2(x) \circ \phi(x)
    \phantom{AAAAAA}
    \array{
      (V_1)_x &\overset{\phi(x)}{\longrightarrow}& (V_2)_x
      \\
      {}^{\mathllap{\rho_1(f)}}\downarrow && \downarrow^{\mathrlap{\phi_2(f)}}
      \\
      (V_1)_y &\underset{\phi(y)}{\longrightarrow}& (V_2)_y
    }
  $$


By def. \ref{GroupoidDependentlyTypes}
the representations of $\mathcal{G}$ in $Core(\mathcal{C})$ and homomorphisms between them constitute a [[groupoid]]
called the _[[representation category|representation groupoid]]_

$$
  Rep(\mathcal{G})
  \;\coloneqq\;
  Hom_{Grpd}(\mathcal{G}, Core(\mathcal{C}))
  \,.
$$


=--

+-- {: .num_example #GroupRepresentationsAsDeloopingRepresentations}
###### Example/Definition
**([[group representations]] are [[groupoid representations]] of [[delooping groupoids]])**

If $\mathcal{G} = B G$ is the [[delooping groupoid]] of a [[group]] $G$ (example \ref{GroupoidFromDelooping}), then
a [[groupoid representation]] of $B G$ is a _[[group representation]]_ of $G$ (def. \ref{GroupoidRepresentation}), and one writes

$$
  Rep(G) \coloneqq Rep(B G)
$$

for the [[representation category|representation groupoid]].

For each object $x \in X$ the canonical inclusion of the [[delooping groupoid]] of the [[automorphism group]]
(from def. \ref{InGrupoidAutomorphismGroup})

$$
  inc_x \;\colon\; B Aut_{\mathcal{G}}(x) \hookrightarrow \mathcal{G}
$$

induces by precomposition a homomorphism of representation groupoids:

$$
  inc_x^*
    \;\colon\;
  Rep(\mathcal{G})
    \longrightarrow
  Rep(B Aut_{\mathcal{G}}(x))
  \,.
$$

We say that a groupoid representation is _faithful_ or _free_ if for all objects $x$
its restriction to a group representation of $Aut_{\mathcal{G}}(x)$ this way is transitive or free, respectively.

Here the representation $\rho$ of a group $G$ on some set $S$

1. _[[transitive action|transitive]]_ if for all pairs of elements $s_1, s_2 \in S$ there is a $g \in G$
   such that $\rho(g)(s_1) = s_2$;

1. _[[free action|free]]_ if whenever $g(s) = s$ holds for all $s \in S$ then $g$ is the [[neutral elements]].

=--

+-- {: .num_prop #GroupoidRepresentationsAreProductsOfGroupRepresentations}
###### Proposition
**([[groupoid representations]] are [[product category|products]] of [[group representations]])

Assuming the [[axiom of choice]] then the following holds:

Let $\mathcal{G}$ be a [[groupoid]]. Then its [[category of representations|groupoid of]]
[[groupoid representations]] $Rep(\mathcal{G})$ (def. \ref{GroupoidRepresentation})
is [[equivalence of groupoids|equivalent]] (def. \ref{EquivalenceOfGroupoids}) to
the [[product category|product groupoid]] (example \ref{ProductGroupoid})
indexed by the set of [[connected components]] $\pi_0(\mathcal{G})$ (def. \ref{GroupoidConnectedComponents}) of [[group representations]]
(example \ref{GroupRepresentationsAsDeloopingRepresentations})
of the [[automorphism group]] $G_i \coloneqq Aut_{\mathcal{G}}(x_i)$ (def. \ref{InGrupoidAutomorphismGroup}) for $x_i$ any object in the $i$th
connected component:

$$
  Rep(\mathcal{G})
   \;\simeq\;
  \underset{i \in \pi_0(\mathcal{G})}{\prod} Rep(G_i)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $\mathcal{C}$ be the category that the representation is on (e.g. $\mathcal{C} = $ [[Set]]
for [[permutation representations]]). Then by definition

$$
  Rep(\mathcal{G}) = Hom_{Grpd}( \mathcal{G} , Core(\mathcal{C})  )
  \,.
$$

Consider the injection functor of the [[skeleton]] from lemma \ref{DeloopingGroupoidEquivalence}

$$
  inc
  \;\colon\;
  \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i
  \overset{}{\longrightarrow}
  \mathcal{G}
  \,.
$$


By lemma \ref{HmotopiesWithMorphismsHorizontaComposition} the pre-composition with this constitutes a functor

$$
  inc^\ast \;\colon\; Hom( \mathcal{G}, \mathcal{C} ) \longrightarrow Hom( \underset{i \in \pi_0(\mathcal{G})}{\sqcup} B G_i, \mathcal{C} )
$$

and by combining lemma \ref{DeloopingGroupoidEquivalence} with lemma \ref{HorizontalCompositionWithHomotopyIsNaturalTransformation}
this is an [[equivalence of groupoids]]. Finally, by example \ref{ProductGroupoid} the
groupoid on the right is the product groupoid as claimed.

=--



+-- {: .num_defn #CoveringSpaceMonodromy}
###### Definition
**([[monodromy]] of a [[covering space]])

Let $X$ be a [[topological space]] and $E \overset{p}{\to} X$ a [[covering space]] (def. \ref{CoveringSpace}). Write $\Pi_1(X)$ for the [[fundamental groupoid]] of $X$ (example \ref{FundamentalGroupoid}).

Define a groupoid homomorphism

$$
  Fib_E
    \;\colon\;
  \Pi_1(X)
    \longrightarrow
  Core(Set)
$$

to the groupoid core of the [[category]] [[Set]] of [[sets]] (example \ref{GroupoidRepresentation}), hence a [[permutation representation|permutation]] [[groupoid representation]] (example \ref{GroupoidRepresentation}), as follows:

1. to a point $x \in X$ assign the [[fiber]] $p^{-1}(\{x\}) \in Set$;

1. to the [[homotopy class]] of a [[path]] $\gamma$ connecting $x \coloneqq \gamma(0)$ with $y \coloneqq \gamma(1)$ in $X$ assign the function $p^{-1}(\{x\}) \longrightarrow p^{-1}(\{y\})$ which takes $\hat x \in p^{-1}(\{x\})$ to the endpoint of a path $\hat \gamma$ in $E$ which lifts $\gamma$ through $p$ with starting point $\hat \gamma(0) = \hat x$

   $$
     \array{
       p^{-1}(x) &\overset{}{\longrightarrow}& p^{-1}(y)
       \\
       (\hat x = \hat \gamma(0)) &\mapsto& \hat \gamma(1)
     }
     \,.
   $$

This construction is well defined for a given representative $\gamma$ due to the unique path-lifting property of covering spaces
(lemma \ref{CoveringSpacePathLifting}) and it is independent of the choice of $\gamma$ in the given homotopy class of paths due
to the [[homotopy lifting property]] (example \ref{CoveringSpacesHomotopyLifting}).
Similarly, these two lifting properties give that this construction respects composition in $\Pi_1(X)$ and hence is indeed
a homomorphism of groupoids (a functor).

=--




+-- {: .num_prop #FunctorialExtractingHomotopy}
###### Proposition
**(extracting [[monodromy]] is [[functor|functorial]])**

Given a [[isomorphism]] between two [[covering spaces]] $E_i \overset{p_i}{\to} X$, hence a [[homeomorphism]] $f \colon E_1 \to E_2$ which respects [[fibers]] in that the [[diagram]]

$$
  \array{
    E_1 && \overset{f}{\longrightarrow} && E_2
    \\
    & {}_{\mathllap{p_1}}\searrow && \swarrow_{\mathrlap{p_2}}
    \\
    && X
  }
$$

[[commuting diagram|commutes]], then the component functions

$$
  f\vert_{\{x\}} \;\colon\; p_1^{-1}(\{x\}) \longrightarrow p_2^{-1}(\{x\})
$$

are compatible with the monodromy $Fib_{E}$ (def. \ref{CoveringSpaceMonodromy}) along any [[path]] $\gamma$ between points $x$ and $y$ from def. \ref{CoveringSpaceMonodromy} in that the following [[diagrams]] of [[sets]] [[commuting diagram|commute]]

$$
  \array{
     p_1^{-1}(x) &\overset{f\vert_{\{x\}}}{\longrightarrow}& p_2^{-1}(x)
     \\
     {}^{\mathllap{Fib_{E_1}([\gamma])}}\downarrow
       &&
     \downarrow^{\mathrlap{ Fib_{E_2}([\gamma]) }}
     \\
     p_1^{-1}(y) &\underset{f\vert_{\{y\}}}{\longrightarrow}& p_2^{-1}(\{y\})
  }
  \,.
$$

This means that $f$ induces a homotopy ([[natural transformation]]) between the monodromy homomorphisms (functors)

$$
  \Pi_1(X)
    \array{
      \overset{Fib_{E_1}}{\longrightarrow}
      \\
        \Downarrow
      \\
      \underset{Fib_{E_2}}{\longrightarrow}
    }
  Core(Set)
$$

of $E_1$ and $E_2$, respectively, and hence that constructing monodromy is itself a homomorphism from the [[groupoid]] of [[covering spaces]] of $X$ to that of [[permutation representations]] of the [[fundamental groupoid]] of $X$:

$$
  Fib
   \;\colon\;
  Cov(X)
    \longrightarrow
  Rep(\Pi_1(X), Set)
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let $e \in p_1^{-1}(x)$ be an element, and $\hat \gamma \colon [0,1] \to E_1$
a lift of $\gamma$ to $E_1$ with $\hat \gamma(0) = e$. This means by definition of monodromy that

$$
  Fib_{E_1}([\gamma]) \;\colon\; e \mapsto \hat \gamma(1)
$$

Since the function $f$ is compatible with the
covering projections, the image $f\circ \hat \gamma$ is a lift of $\gamma$ to $E_2$,
with $(f \circ \hat \gamma)(0) = f(\hat \gamma(0)) = f(e)$.
Therefore

$$
  Fib_{E_2}([\gamma]) \;\colon\; f(e) \mapsto f(\hat \gamma(1))
  \,.
$$

In conclusion, for each element $e \in p_1^{-1}(x)$ we have

$$
  \array{
     \{e\} &\overset{f\vert_{\{x\}}}{\longrightarrow}& f(e)
     \\
     {}^{\mathllap{Fib_{E_1}([\gamma])}}\downarrow
       &&
     \downarrow^{\mathrlap{ Fib_{E_2}([\gamma]) }}
     \\
     \hat \gamma(1) &\underset{f\vert_{\{y\}}}{\longrightarrow}& f(\hat\gamma(1))
  }
  \,.
$$


This means that the square commutes, as claimed.

=--




+-- {: .num_example #CoveringSpaceFundamentalGroupoid}
###### Example
**([[fundamental groupoid]] of covering space)

Let $E \overset{p}{\longrightarrow} X$ be a [[covering space]].

Then the [[fundamental groupoid]] $\Pi_1(E)$ of the total space $E$ is
the groupoid

whose

* [[objects]] are pairs $(x,\hat x)$ consisting of a point $x \in X$ and en element $\hat x \in Fib_E(x)$;

* [[morphisms]] $[\hat \gamma] \colon (x,\hat x) \to (x', \hat x')$ are morphisms $[\gamma] \colon x \to x'$ in $\Pi_1(X)$ such that $Fib_E([\gamma])(\hat x) = \hat x'$.


This is also called the _[[Grothendieck construction]]_
of the [[monodromy]] functor $Fib_E \;\colon\; \Pi_1(X) \to Core(Set)$, and denoted

$$
  \Pi_1(E)
   \;\simeq\;
  \int_{\Pi_1(X)} Fib_E
  \,.
$$

=--


+-- {: .proof}
###### Proof

By the uniqueness of the path-lifting, lemma \ref{CoveringSpacePathLifting} and the very definition of the [[monodromy]] functor.

=--


+-- {: .num_example #CoveringConnectivityViaMonodromy}
###### Example
**([[covering space]] is [[universal covering space|universal]] if [[monodromy]] is [[free action|free]] and [[transitive action|transitive]])

Let $X$ be a [[path-connected topological space]] and let $E \overset{p}{\to} X$ be a [[covering space]]. Then the total space $E$ is

1. [[path-connected topological space|path-connected]] precisely if the [[monodromy]] $Fib_E$ is a [[transitive action]];

1. [[simply connected topological space|simply connected]] (def. \ref{SimplyConnected}) hence [[universal covering space]]
   (def. \ref{UniversalCoveringSpace})
   precisely if the [[monodromy]] $Fib_E$ is a [[transitive action|transitive]] and [[free action]].

=--

+-- {: .proof}
###### Proof

By example \ref{CoveringSpaceFundamentalGroupoid}.

=--


$\,$


+-- {: .num_defn #ElementaryReconstructionCoveringSpace}
###### Definition
**([[reconstruction of covering spaces from monodromy]])**

Let

1. $(X,\tau)$ be a [[locally path-connected topological space|locally path-connected]] [[semi-locally simply connected topological space|semi-locally simply connected]] [[topological space]],

1. $\rho \in Rep(\Pi_1(X),Set)$ a [[permutation representation]] of its [[fundamental groupoid]].

Consider the [[disjoint union]] [[set]] of all the sets appearing in this representation

$$
  E(\rho) \;\coloneqq\;  \underset{x \in X}{\sqcup} \rho(x)
$$

For

1. $U \subset X$ an [[open subset]]

   1. which is [[path-connected topological space|path-connected]]

   1. for which every element of the [[fundamental group]] $\pi_1(U,x)$ becomes trivial under $\pi_1(U,x) \to \pi_1(X,x)$,

1. for $\hat x \in \rho(x)$ with $x \in U$

consider the subset

$$
  V_{U,\hat x}
    \coloneqq
  \left\{
    \rho(\gamma)(\hat x)
    \;\vert\;
    x' \in U
    \,,\phantom{A}
    \gamma \,\text{path from}\, x \,\text{to}\, x'
  \right\}
  \;\subset\;
  E(\rho)
  \,.
$$

The collection of these defines a [[base for a topology]] (prop. \ref{ElementaryReconstructedCoveringSpaceWellDefined} below). Write $\tau_{\rho}$ for the corresponding topology. Then

$$
  (E(\rho), \tau_{\rho})
$$

is a [[topological space]]. It canonically comes with the function

$$
  \array{
    E(\rho) &\overset{p}{\longrightarrow}& X
    \\
    \hat x \in \rho(x) &\mapsto& x
  }
  \,.
$$

Finally, for

$$
  f \;\colon\; \rho_1 \longrightarrow \rho_2
$$

a [[homomorphism]] of permutation representations, there is the evident induced function

$$
  \array{
    E(\rho_1)
     &\overset{Rec(f)}{\longrightarrow}&
    E(\rho_2)
    \\
    (\hat x \in \rho_1(x)) &\mapsto& (f_x(\hat x) \in \rho_2(x))
  }
  \,.
$$

=--

+-- {: .num_prop #ElementaryReconstructedCoveringSpaceWellDefined}
###### Proposition

The construction $\rho \mapsto E(\rho)$ in def. \ref{ElementaryReconstructionCoveringSpace}
is well defined and yields a [[covering space]] of $X$.

Moreover, the construction $f \mapsto Rec(f)$ yields a homomorphism of covering spaces.

=--

+-- {: .proof}
###### Proof

First to see that we indeed have a [[topological space|topology]], we need to check  (by [this prop.](topological+base#Recognition)) that every point is contained in some base element, and that every point in the intersection of two base elements has a base neighbourhood that is still contained in that intersection.

So let $x \in X$ be a point. By the assumption that $X$ is [[semi-locally simply connected topological space|semi-locally simply connected]] there exists an [[open neighbourhood]] $U_x \subset X$ such that every loop in $U_x$ on $x$ is contractible in $X$. By the assumption that $X$ is a [[locally path-connected topological space]], this contains an open neighbourhood $U'_x \subset U_x$ which is [[path-connected topological space|path connected]] and, as every subset of $U_x$, it still has the property that every loop in $U'_x$ based on $x$ is contractible as a loop in $X$. Now let $\hat x \in E$ be any point over $x$, then it is contained in the base open $V_{U'_x,x}$.

The argument for the base open neighbourhoods contained in intersections is similar.


Then we need to see that $p \colon E(\rho) \to X$ is a [[continuous function]]. Since taking pre-images preserves unions ([this prop.](interactions+of+images+and+pre-images+with+unions+and+intersections#PreImagePreservesUnionsAndIntersections)), and since by semi-local simply connectedness and local path connectedness every neighbourhood contains an open neighbourhood $U \subset X$ that labels a base open, it is sufficient to see that $p^{-1}(U)$ is a base open. But by the very assumption on $U$, there is a unique morphism in $\Pi_1(X)$ from any point $x \in U$ to any other point in $U$, so that $\rho$ applied to these paths establishes a bijection of sets

$$
  p^{-1}(U)
    \;\simeq\;
  \underset{\hat x \in \rho(x)}{\sqcup} V_{U,\hat x}
    \;\simeq\;
  U \times \rho(x)
  \,,
$$

thus exhibiting $p^{-1}(U)$ as a union of base opens.

Finally we need to see that this continuous function $p$ is a covering projection, hence that every point $x \in X$ has a neighbourhood $U$ such that $p^{-1}(U) \simeq U \times \rho(x)$. But this is again the case for those $U$ all whose loops are contractible in $X$, by the above identification via $\rho$, and these exist around every point by semi-local simply-connetedness of $X$.

This shows that $p \colon E(\rho) \to X$ is a covering space. It remains to see that $Rec(f) \colon E(\rho_1) \to E(\rho_2)$ is a homomorphism of covering spaces. Now by construction it is immediate that this is a function over $X$, in that this [[commuting diagram|diagram commutes]]:

$$
  \array{
    E(\rho_1) && \overset{Rec(f)}{\longrightarrow}&& E(\rho_2)
    \\
    & \searrow && \swarrow
    \\
    && X
  }
  \,.
$$

So it only remains to see that $Rec(f)$ is a [[continuous function]]. So consider $V_{U, y_2 \in \rho_2(x)}$ a base open of $E(\rho_2)$. By [[natural transformation|naturality]] of $f$

$$
  \array{
    \rho_1(x') &\overset{f_{x'}}{\longrightarrow}& \rho_2(x')
    \\
    {}^{\mathllap{\rho_1(\gamma)}}\uparrow{}^{\mathrlap{\simeq}} && {}^{\mathllap{\simeq}}\uparrow^{\mathrlap{\rho_2(\gamma)}}
    \\
    \rho_1(x) &\underset{f_{x}}{\longrightarrow}& \rho_2(x)
  }
$$

its pre-image under $Rec(f)$ is

$$
  Rec(f)^{-1}(V_{U, y_2 \in \rho_2(x)})
  =
  \underset{y_1 \in f^{-1}(y_2)}{\sqcup} V_{U,y_1 \in \rho_1(x)}
$$

and hence a union of base opens.

=--


+-- {: .num_prop #FundamentalTheoremOfCoveringSpaces}
###### Proposition
**([[fundamental theorem of covering spaces]])**

Let $X$ be a [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply-connected topological space]] (def. \ref{SemiLocallySimplyConnected}). Then the operations on

1. extracting the [[monodromy]] $Fib_{E}$ of a [[covering space]] $E$ over $X$ (def. \ref{CoveringSpaceMonodromy}, prop. \ref{FunctorialExtractingHomotopy})

1. [[reconstructing a covering space from monodromy]] $Rec(\rho)$ (def. \ref{ElementaryReconstructionCoveringSpace}, prop. \ref{ElementaryReconstructedCoveringSpaceWellDefined})

constitute an [[equivalence of groupoids]] (def. \ref{EquivalenceOfGroupoids}

$$
  Core(Cov(X))
    \underoverset
      {\underset{\phantom{AA}Fib\phantom{AA}}{\longrightarrow}}
      {\overset{\phantom{AA}Rec\phantom{AA}}{\longleftarrow}}
      {\simeq}
  Rep(\Pi_1(X), Set)
$$

between the groupoid $Core(Cov(X))$ (example \ref{CoreGroupoid}, def. \ref{CoveringSpace}) whose [[objects]]
are covering spaces over $X$, and whose [[morphisms]] are [[isomorphisms]] between these (def. \ref{CoveringSpace})
and the groupoid $Rep(\Pi_1(X), Set)$ of [[permutation representation|permutation]] [[groupoid representations]]
(def. \ref{GroupoidRepresentation}) of the [[fundamental groupoid]] $\Pi_1(X)$ of $X$ (example \ref{FundamentalGroupoid}).

=--

+-- {: .proof}
###### Proof

First we demonstrate a homotopy ([[natural isomorphism]]) of the form

$$
  id_{Rep(\Pi_1(X), Set)}
    \overset{\simeq}{\longrightarrow}
  Fib \circ Rec
  \,.
$$

To this end, given $\rho \in Rep(\Pi_1(X), Set)$ a [[permutation representation|permutation]] [[groupoid representation]],
we need to exhibit in turn a homotopy ([[natural isomorphism]]) of permutation representations.

$$
  \eta_{\rho}
    \;\colon\;
  \rho \longrightarrow Fib(Rec(\rho))
$$

First consider what the right hand side is like:
By def. \ref{ElementaryReconstructionCoveringSpace} of $Rec$ and def. \ref{CoveringSpaceMonodromy} of $Fib$ we have for every $x \in X$ an actual equality

$$
  Fib(Rec(\rho))(x) = \rho(x)
  \,.
$$

To similarly understand the value of $Fib(Rec(\rho))$ on morphisms $[\gamma] \in \Pi_1(X)$, let $\gamma \colon [0,1] \to X$ be a representing [[path]] in $X$. As in the proof of the path lifting lemma \ref{CoveringSpacePathLifting}
we find a [[finite number]] of paths $\{\gamma_i\}_{i \in \{1,n\}}$ such that

1. regarded as morphisms $[\gamma_i]$ in $\Pi_1(X)$ they [[composition|compose]] to $[\gamma]$:

   $$
     [\gamma] = [\gamma_n] \circ \cdots \circ [\gamma_2] \circ [\gamma_1]
   $$

1. each $\gamma_i$ factors through an open subset $U_i \subset X$ over which $Rec(\rho)$ trivializes.

Hence by [[functor|functoriality]] of $Fib(Rec(\rho))$ it is sufficient to understand its value on these paths $\gamma_i$. But on these we have again by direct unwinding of the definitions that

$$
  Fib(Rec(\rho))([\gamma_i]) = \rho([\gamma_i])
  \,.
$$

This means that if we take

$$
  \eta_\rho(x) \;\colon\; \rho(x) \overset{=}{\longrightarrow} Fib(Rec(\rho))
$$

to be the above identification, then this is a homotopy/[[natural isomorphism]] as required.

It remains to see that these morphism $\eta_\rho$ are themselves natural in $\rho$, hence that for each morphism $\phi \colon \rho \to \rho'$ the diagram


$$
  \array{
    \rho &\overset{\phi}{\longrightarrow}& \rho'
    \\
    {}^{\mathllap{eta_\rho}}\downarrow && \downarrow^{\mathrlap{\eta_{\rho'}}}
    \\
    Fib(Rec(\rho))
    &\underset{Fib(Rec(\phi))}{\longrightarrow}&
    Fib(Rec(\rho'))
  }
$$

commutes as a diagram in $Rep(\Pi_1(X), Set)$. Since these morphisms are themselves groupoid homotopies (natural isomorphisms) this is the case precisely if for all $x \in X$ the corresponding component diagram commutes. But by the above this is


$$
  \array{
    \rho(x) &\overset{\phi(x)}{\longrightarrow}& \rho'(x)
    \\
    {}^{\mathllap{=}}\downarrow && \downarrow^{\mathrlap{=}}
    \\
    Fib(Rec(\rho))(x)
    &\underset{Fib(Rec(\phi))(x) }{\longrightarrow}&
    Fib(Rec(\rho'))(x)
  }
$$

and hence this means that the top and bottom horizontal morphism are in fact equal. Directz unwiinding of the definitions shows that this is indeed the case.

Now we demonstrate a homotopy ([[natural isomorphism]]) of the form

$$
  Rec \circ Fib
    \overset{\simeq}{\longrightarrow}
  id_{Core(Cov(X))}
  \,.
$$

For $E \in Cov(X)$ a covering space, we need to exhibit a natural isomorphism of covering spaces of the form

$$
  \epsilon_E
    \;\colon\;
  Rec(Fib(E)) \longrightarrow E
  \,.
$$

Again by def. \ref{ElementaryReconstructionCoveringSpace} of $Rec$ and def. \ref{CoveringSpaceMonodromy} of $Fib$  the underlying set of $Rec(Fib(E))$ is actually equal to that of $E$, hence it is sufficient to check that this [[identity function]] on underlying sets is a [[homeomorphism]] of [[topological spaces]].

By the assumption that $X$ is [[locally path-connected topological space|locally path-connected]] and [[semi-locally simply connected topological space|semi-locally simply connected]], it is sufficient to check for $U\subset X$ an open path-connected subset and $x \in X$ a point with the property that $\pi_1(U,x) \to \pi_1(X,x)$ lands is constant on the trivial element, that the open subsets of $E$ of the form $U \times \{\hat x\} \subset p^{-1}(U)$ form a basis for the topology of $Rec(Fib(E))$. But this is the case by definition of $Rec$.

This proves the equivalence.

=--



+-- {: .num_example #ReconstructCoveringForFreeAndTransitiveMonodromyRepresentation}
###### Example
**([[universal covering space]] reconstructed from [[free action|free]] and [[transitive action|transitive]] [[fundamental group]] [[representation]])**

Let $X$ be a [[topological space]] which is

* [[path-connected space|path-connected]],

* [[locally path-connected space|locally path-connected]]

* and [[semi-locally simply-connected space|semi-locally simply-connected]]

Then a [[universal covering space]] of $X$ (def. \ref{UniversalCoveringSpace}) exists.

=--

+-- {: .proof}
###### Proof

By example \ref{CoveringConnectivityViaMonodromy} the covering space is connected and simply connected precisely if its [[monodromy]] representation is free and transitive. By the [[fundamental theorem of covering spaces]] (prop. \ref{FundamentalTheoremOfCoveringSpaces}) every [[permutation representation]] of the [[fundamental group]] $\pi_1(X)$ arises as the monodromy of some covering space. Hence it remains to see that a free and transitive representation of $\pi_1(X)$ exists: The action of any group $G$ on itself, by left multiplication,
is free and transitive.

=--


$\,$

## Examples
 {#Examples}

We now use the theorems established above to compute the [[fundamental groups]] of topological spaces
in some basic examples. In particular we prove the archetypical example
saying that the [[fundamental group of the circle is the integers]]  (prop. \ref{CircleFundamentalGroup} below).

$\,$

### Fundamental groups
 {#ExamplesFundamentalGroups}


+-- {: .num_prop #CircleFundamentalGroup}
###### Proposition
**([[fundamental group of the circle is the integers]])**

The [[fundamental group]] $\pi_1$ of the [[circle]] $S^1$ is the additive group of [[integers]]:


$$
  \pi_1(S^1) \overset{\simeq}{\longrightarrow} \mathbb{Z}
$$

and the isomorphism is given by assigning [[winding number]].

=--


+-- {: .proof #ClassicalPointSetProof}
###### Proof

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/UniversalCoveringOfCircle.png" width="150">
</div>

By example \ref{UniversalCoveringRealLineOfCircle},
the [[universal covering space]] $\widehat{S^1}$ of $S^1$ is the [[real line]]

$$
  p \coloneqq (cos(2 \pi(-)), \sin(2 \pi(-)))
   \;\colon\; \mathbb{R}^1 \longrightarrow S^1
  \,.
$$

Since the [[circle]] is [[locally path-connected topological space|locally path-connected]] ([this example](locally+path-connected+space#LocallyPathConnectedCircle)) and [[semi-locally simply connected topological space|semi-locally simply connected]] ([this example](semi-locally+simply+connected+topological+space#LocallySimplyConnectedCircle)) the [[fundamental theorem of covering spaces]] applies and gives that the [[automorphism group]] of $\mathbb{R}^1$ over $S^1$ equals the automorphism group of its [[monodromy]] [[permutation representation]]:

$$
  Aut_{Cov(S^1)}(\mathbb{R}^1)
    \;\simeq\;
  Aut_{\pi_1(S^1) Set}(Fib_{S^1})
  \,.
$$

Moreover, as a corollary of the [[fundamental theorem of covering spaces]] we have that the [[monodromy]] representation of a [[universal covering space]] is given by the [[action]] of the [[fundamental group]] $\pi_1(S)$ on itself ([this prop.](universal+covering+space#ReconstructCoveringForFreeAndTransitiveMonodromyRepresentation)).

But the [[automorphism group]] of any group regarded as an [[action]] on itself by left multiplication is canonically isomorphic to that group itself (by [this example](permutation+representation#AutomorphismsOfGAsGTorsor)), hence we have

$$
  Aut_{{\pi_1(S^1)} Set}(Fib_{S^1})
   \;\simeq\;
  Aut_{{\pi_1(S^1)} Set}( \pi_1(S^1) )
   \;\simeq\;
  \pi_1(S^1)
  \,.
$$

Therefore to conclude the proof it is now sufficient to show that

$$
  \mathrm{Aut}_{Cov(S^1)}(\mathbb{R}^1) \simeq \mathbb{Z}
  \,.
$$

To that end, consider a [[homeomorphism]] of the form

$$
  \array{
    \mathbb{R}^1 && \underoverset{\simeq}{f}{\longrightarrow} && \mathbb{R}^1
    \\
    & {}_{\mathllap{p}}\searrow && \swarrow_{\mathrlap{p}}
    \\
    && S^1
  }
  \,.
$$

Let $s \in S^1$ be any point, and consider the restriction of $f$ to the fibers over the [[complement]]:

$$
  \array{
    p^{-1}(S^1 \setminus \{s\}) && \underoverset{\simeq}{f}{\longrightarrow} && p^{-1}(S^1 \setminus \{s\})
    \\
    & {}_{\mathllap{p}}\searrow && \swarrow_{\mathrlap{p}}
    \\
    && S^1 \setminus \{s\}
  }
  \,.
$$

By the [[covering space]] property we have (via [this example](universal+covering+space#UniversalCoveringOfCircleRealLine)) a [[homeomorphism]]

$$
  p^{-1}(S^1 \setminus \{s\})
   \simeq
  (0,1) \times Disc(\mathbb{Z})
  \,.
$$

Therefore, up to homeomorphism,  the restricted function is of the form

$$
  \array{
    (0,1)\times Disc(\mathbb{Z})
      &&
      \underoverset{\simeq}{f}{\longrightarrow}
      &&
    (0,1) \times Disc(\mathbb{Z})
    \\
    & {}_{pr_1}\searrow && \swarrow_{pr_1}
    \\
    && (0,1)
  }
  \,.
$$

By the [[universal property]] of the [[product topological space]] this means that $f$ is equivalently given by its two components

$$
  (0,1) \times Disc(\mathbb{Z})
    \overset{pr_1 \circ f}{\longrightarrow}
  (0,1)
  \phantom{AAAA}
  (0,1) \times Disc(\mathbb{Z})
    \overset{pr_2 \circ f}{\longrightarrow}
  Disc(\mathbb{Z})
  \,.
$$

By the [[commuting diagram|commutativity]] of the above [[diagram]], the first component is fixed to be $pr_1$. Moreover, by the fact that $Disc(\mathbb{Z})$ is a [[discrete space]] it follows that the second component is a [[locally constant function]] (by [this example](locally+constant+function#LocallyConstantFunctionIntoDiscreteSpace)). Therefore, since the [[product space]] with a [[discrete space]] is a [[disjoint union space]]  (via [this example](product+topological+space#ProductWithDiscreteFiniteTopologicalSpace))

$$
  (0,1) \times Disc(\mathbb{Z}) \simeq \underset{n \in \mathbb{Z}}{\sqcup}(0,1)
$$

and since the disjoint summands $(0,1)$ are [[connected topological spaces]] ([this example](connected+space#ConnectedSubspacesOfRealLineAreTheIntervals)), it follows that the second component is a [[constant function]] on each  of these summands (by [this example](connected+space#LocallyConstantFunctionsOnConnectedSpaces)).

Finally, since every function out of a [[discrete topological space]] is continuous, it follows in conclusion that the restriction of $f$ to the fibers over $S^1 \setminus \{s\}$ is entirely encoded in an [[endofunction]] of the set of [[integers]]

$$
  \phi \;\colon\; \mathbb{Z} \to \mathbb{Z}
$$

by

$$
  \array{
    S^1 \setminus \{s\} \times Disc(\mathbb{Z})
      &\overset{f}{\longrightarrow}&
    S^1 \setminus \{s\} \times Disc(\mathbb{Z})
    \\
    (t,k) &\mapsto& (t, \phi(k))
  }
  \,.
$$


Now let $s' \in S^1$ be another point, distinct from $s$. The same analysis as above applies now to the restriction of $f$ to $S^1 \setminus \{s'\}$ and yields a function

$$
  \phi' \;\colon\; \mathbb{Z} \longrightarrow \mathbb{Z}
  \,.
$$


Since

$$
  \left\{
    p^{-1}(S^1 \setminus \{s\})
    \subset \mathbb{R}^1
     \,,\,
    p^{-1}(S^1 \setminus \{s'\})
    \subset \mathbb{R}^1
  \right\}
$$

is an [[open cover]] of $\mathbb{R}^1$, it follows that $f$ is unqiuely fixed by its restrictions to these two subsets.

Now unwinding the definition of $p$ shows that the condition that the two restrictions coincide on the intersection $S^1 \setminus \{s,s'\}$ implies that there is $n \in \mathbb{Z}$ such that $\phi(k) = k+ n$ and $\phi'(k) = k+n$.

This shows that $Aut_{Cov(S^1)}(\mathbb{R}^1) \simeq \mathbb{Z}$.

=--


+-- {: .num_example #CoveringOfCircleAndConjugacyClassesOfSymmetricGroup}
###### Example
**([[isomorphism classes]] of [[covering spaces|coverings]] of the circle are [[conjugacy classes]] in the [[symmetric group]])**

The [[monodromy]] construction assigns to an [[isomorphism class]] of covering spaces
over the [[circle]] $S^1$
with [[fibers]] consisting of $n$ elements [[conjugacy classes]]
of elements the [[symmetric group]] $\Sigma(n)$:

$$
  \left \{
    \array{
      \text{isomorphism classes of}
      \\
      \text{finite covering spaces }
      \\
      \text{over the circle}
    }
  \right\}
   \;\simeq\;
  \left\{
    \array{
      \text{conjugacy classes of}
      \\
      \text{elements of a symmetric group}
    }
  \right\}
$$

To see this we may without restriction choose a basepoint $x \in S^1$ so that
a monodromy representation is equivalently a groupoid morphism of the form (prop. \ref{GroupoidRepresentationsAreProductsOfGroupRepresentations})

$$
  \rho
    \;\colon\;
  B \mathbb{Z}
    \overset{\simeq}{\longrightarrow}
  B \pi_1(S^1,x)
    \overset{\rho}{\longrightarrow}
  Core(Set)
  \,.
$$

Since $\mathbb{Z}$ is the [[free abelian group]] on a single generator, such as morphism
is uniquely determined by the image of $1 \in \mathbb{Z}$. This is taken to some
isomorphism of the set $p^{-1}(x)$. If we choose any identification $\phi \colon p^{-1}(x) \overset{\simeq}{\to} \{1, \cdots, n\}$,
then this defines an element $\sigma \in \Sigma(n)$ in the [[symmetric group]]:

$$
  \array{
    x &\mapsto&  p^{-1}(x) &\underoverset{\simeq}{\phi}{\longrightarrow}& \{1, \cdots, n\}
    \\
    {}^{\mathllap{1}}\downarrow && {}^{\mathllap{\rho(1)}}\downarrow && \downarrow^{\sigma}
    \\
    x &\mapsto& p^{-1}(x) &\underoverset{\phi}{\simeq}{\longrightarrow}& \{1, \cdots, n\}
  }
  \,.
$$

Now if

$$
  f \;\colon\; E_1 \overset{\simeq}{\longrightarrow} E_2
$$

is an isomorphism of covering spaces,
then by the [[fundamental theorem of covering spaces]] (prop.  \ref{FundamentalTheoremOfCoveringSpaces})
this corresponds bijectively to a homomorphism of representations

$$
  Fib(f) \;\colon\; Fib_{E_1} \overset{\simeq}{\longrightarrow} Fib_{E_2}
$$

which in turn is by definition a homotopy (natural isomorphism) between the monodromy functors
$Fib_{E_i} \;\colon\; B \mathbb{Z} \to Core(Set)$.

The combination of the naturality square of this natural isomorphism with the above identification
yields the following diagram

$$
  \array{
    \{1,\cdots, n\}
      &\overset{\phi_1^{-1}}{\longrightarrow}&
    p_1^{-1}(x)
      &\overset{f\vert_{\{x\}}}{\longrightarrow}&
    p_2^{-1}(x)
      &\overset{\phi_2}{\longrightarrow}&
    \{1, \cdots, n\}
    \\
    {}^{\mathllap{\sigma_1}}
    \downarrow
      &&
    {}^{\mathllap{ Fib_{E_1}(1) }}\downarrow
      &&
    \downarrow^{\mathrlap{ Fib_{E_2}(1) }}
      &&
    \downarrow^{\mathrlap{ \sigma_2 }}
    \\
    \{1,\cdots, n\}
      &\underset{\phi_1^{-1}}{\longrightarrow}&
    p_1^{-1}(x)
      &\underset{f\vert_{\{x\}}}{\longrightarrow}&
    p_2^{-1}(x)
      &\underset{\phi_2}{\longrightarrow}&
    \{1, \cdots, n\}
  }
  \,.
$$

The commutativity of the total rectangle says that the permutations $\sigma_1$ and $\sigma_2$ are related by conjugation
with the element $\phi_2 \circ f\vert_{\{x\}} \circ \phi_1^{-1}$.

=--


+-- {: .num_example }
###### Example
**(three-sheeted covers of the circle)**

Consider the three-sheeted [[covering spaces]] of the [[circle]].

By example \ref{CoveringOfCircleAndConjugacyClassesOfSymmetricGroup}
these are, up to isomorphism, given by the [[conjugacy classes]] of the elements
of the [[symmetric group]] $\Sigma(3)$ on three elements. These in turn are labeled by the
[[cycle]] structure of the elements ([this prop.](symmetric+group#ConjugacycClassesOfSymmetricGroupCorrespondToCycleSet)).

<div style="float:right;margin:0 10px 10px 0;">
<img src="https://ncatlab.org/nlab/files/The3SheetedCoveringsOfTheCircle.png" width="150">
</div>

For the symmetric group on
three elements there are three such classes

$$
  \array{
    (1\; 2\; 3)
    \\
    (1 \; 2) (3)
    \\
    (1) (2) (3)

  }
$$

The corresponding covering spaces of the circle are shown in the graphics.

> graphics grabbed from [Hatcher](homotopy+equivalence#Hatcher)

=--



### Higher homotopy groups
 {#HigherHomotopyGroups}


(...)

$\,$


***

This concludes the introduction to basic homotopy theory.

For introduction to more general and abstract homotopy theory see at _[[Introduction to Homotopy Theory]]_.

An incarnation of [[homotopy theory]] in [[linear algebra]] is _[[homological algebra]]_. For
introduction to that see at _[[schreiber:Introduction to Homological Algebra]]_.

***

$\,$

## References

A textbook account:

* {#tomDieck06} [[Tammo tom Dieck]], sections 2 and 3 of _Algebraic Topology_, EMS 2006 ([pdf](http://www.maths.ed.ac.uk/~aar/papers/diecktop.pdf), [doi:10.4171/048](https://www.ems-ph.org/books/book.php?proj_nr=86))

Lecture notes:

* {#Moller11} [[Jesper Møller]], _The fundamental group and covering spaces_ (2011) ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))

Further reading:

* *[[geometry of physics -- categories and toposes]] -- Sec. 7: [∞-Groupoids I: Topological homotopy theory](geometry+of+physics+--+categories+and+toposes#TopologicalHomotopyTheory)*


$\,$

$\,$