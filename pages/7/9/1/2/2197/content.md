
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Functional analysis
+-- {: .hide}
[[!include functional analysis - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Definition

A [[topological vector space]] is __locally convex__ if it has a [[base of its topology]] consisting of [[convex subsets|convex]] [[open subsets]].  Equivalently, it is a vector space equipped with a [[gauge space|gauge]] consisting of [[seminormed vector space|seminorms]].  As with other topological vector spaces, a locally convex space (LCS or LCTVS) is often assumed to be [[Hausdorff space|Hausdorff]].

Locally convex (topological vector) spaces are the standard setup for much of contemporary [[functional analysis]]. 

A natural notion of [[smooth map]] between lctvs is given by [[Michal-Bastiani smooth maps]].


## Properties

### Continuous linear functionals
 {#ContinuousLinearFunctionals}

One reason why locally convex [[topological vector spaces]] are important is that lots of [[continuous linear functionals]] exist on them, at least if one assumes an appropriate choice principle, e.g., [[axiom of choice]] or [[ultrafilter theorem]] (or just [[dependent choice]] for a [[separable space]]). This fact is encapsulated in the [[Hahn-Banach theorem]]; a nice exposition is given in [Tao 09](#Tao09). By way of contrast, a [[topological vector space]] which is _not_ locally convex, such as the [[Lebesgue space]] $L^p([0, 1])$ where $0 \lt p \lt 1$, need not have any (nonzero) [[continuous linear functionals]] at all. 



+-- {: .num_defn #DirectedSystemOfSeminorms}
###### Definition
**(directed system of seminorms)**

A family $\{p_q\}_{q \in Q}$ of [[seminorms]] on some [[real vector space]] $V$ is called _directed_ if


$$
  \underset{q_1, q_2 \in Q}{\forall}
  \left(
    \underset{q \in Q}{\exists}
    \left(
      \underset{C \in (0,\infty)}{\exists}
      \left(
        \underset{v \in V}{\forall}
        \left(
          \,
          C p_q(v) \leq max\{ p_{q_1}(v), p_{q_2}(v) \}
          \,
        \right)
      \right)
    \right)
  \right)
  \,.
$$

=--

(e.g. [Infusino 17](#Infusino17) [def. 4.2.15](http://www.math.uni-konstanz.de/~infusino/TVS-SS17/Lect10.pdf))


+-- {: .num_prop #MaximumEnvelopeOfSeminorms}
###### Proposition
**(maximum envelope of seminorms)

Let $V$ be a [[real vector space]] equipped with a set $\{p_q \colon V \to \mathbb{R}\}_{q \in Q}$ of [[seminorms]]. 

Then the [[maxima]] of [[inhabited|non-empty]] [[finite set|finite]] [[subsets]] $J \subset Q$ of these seminorms 

$$
  v \mapsto \left( \underset{q \in J}{max} p_q(v) \right)
$$

are themselves seminorms, and the set of them 

$$
  \left\{
    \underset{q \subset J}{max} p_q(-)
  \right\}_{ { J \subset Q } \atop {\text{finite, non-empty}} }
$$

generate the same [[topological vector space|topology]] on $V$ as the original $\{p_q\}$ do. Moreover, the system of maximum seminorms evidently form a filtered system according to def. \ref{DirectedSystemOfSeminorms}.

=--

(e.g. [Infusino 17](#Infusino17) [prop.  4.2.13, 4.2.14](http://www.math.uni-konstanz.de/~infusino/TVS-SS17/Lect10.pdf))


+-- {: .num_prop #AlternativeCharacterizationOfContinuityForLinearFunctionals}
###### Proposition
**(characterization of continuity for linear functionals by norm-bounds)

Let $V$ be a [[real vector space]] and $\tau$ a [[topological space|topology]] on $V$ that makes it a locally convex topological vector space, induced from a set of [[seminorms]] $\{p_q \colon V \to \mathbb{R}\}_{q \in Q}$.
Consider a [[linear function]] 

$$
  L \colon V \to \mathbb{R}
$$ 


1. (directed system of seminorms) If the system of seminorms $\{p_q\}_{q \in Q}$ is directed (def. \ref{DirectedSystemOfSeminorms}) then $L$ is a [[continuous function]] with respect to $\tau$, hence is a [[continuous linear functional]], precisely if it is $q$-continuous for some $q \in Q$:

   $$
     \left(
       L \,\text{continuous with respect to}\, \tau
     \right)
     \;\Leftrightarrow\;
     \underset{q \in Q}{\exists}
     \left(
       \underset{C \in (0,\infty)}{\exists}
       \left(
         \underset{v \in V}{\forall}
         \left(
           \,
           {\vert L(v)\vert}
            \leq 
           C p_q(v)
           \,
         \right)
       \right)
     \right)
     \,.
   $$

1. (general system of seminorms) Together with prop. \ref{MaximumEnvelopeOfSeminorms} this means that for $\{p_q\}_{q \in Q}$ any set of seminorms (not necessarily directed), then $L$ is continuous precisely if there exists a [[inhabited set|inhabited]] [[finite set|finite]] [[subset]] of seminorms such that $L$ is bounded with respect to the [[maximum]] over this set:

   $$
     \left(
       L \,\text{continuous with respect to}\, \tau
     \right)
     \;\Leftrightarrow\;
     \underset{q_1, \cdots, q_n \in Q}{\exists}
     \left(
       \underset{C \in (0,\infty)}{\exists}
       \left(
         \underset{v \in V}{\forall}
         \left(
           \,
           {\vert L(v)\vert}
            \leq 
           C \underset{k = 1, \cdots, n}{max} p_{q_n}(v)
           \,
         \right)
       \right)
     \right)
     \,.
   $$

=--

(e.g. [Infusino 17](#Infusino17), [prop. 4.6.1, corollary 4.6.2](http://www.math.uni-konstanz.de/~infusino/Lect12.pdf)), or remark 3-4 4. here: [pdf](https://www.math.ksu.edu/~nagy/func-an-2007-2008/lcvs-5.pdf)


### Co-Probes and curves

The collections of [[continuous linear functionals]] on a LCTVS is used in a way analogous to the collection of [[coordinate]] [[projections]] $pr_i:\mathbb{R}^n\to \mathbb{R}$ out of a [[Cartesian space]]. For example, [[curves]] in a LCTVS over the reals can be composed with functionals to arrive at a collection of functions $\mathbb{R} \to \mathbb{R}$ which are analogous to the 'components' of the curve.

In one respect, a locally convex TVS is a [[nice topological space]] in that there are enough co-probes by maps to the base field.


### Diagram of properties

[[!include diagram of LCTVS properties]]


## Examples

* [[Fréchet spaces]] are locally convex topological vector spaces

## References

* J. L. Taylor, _Notes on locally convex topological vector spaces_ (1995) ([pdf](http://www.math.utah.edu/~taylor/LCS.pdf))

* {#Tao09} [[Terence Tao]], _[Duality and the Hahn-Banach theorem](http://terrytao.wordpress.com/2009/01/26/245b-notes-6-duality-and-the-hahn-banach-theorem/)_, 2009

* {#Infusino17} Maria Infusino, _[Topological vector spaces](www.math.uni-konstanz.de/~infusino/TVS-SS17/teachingSS2017.html)_ 2017

category: analysis

[[!redirects locally convex space]]


[[!redirects locally convex]]
[[!redirects locally convex spaces]]
[[!redirects locally convex vector space]]
[[!redirects locally convex vector spaces]]
[[!redirects locally convex topological vector space]]
[[!redirects locally convex topological vector spaces]]
[[!redirects locally convex TVS]]
[[!redirects locally convex TVSs]]
[[!redirects locally convex TVSes]]
[[!redirects LCS]]
[[!redirects LCSs]]
[[!redirects LCSes]]
[[!redirects LCTVS]]
[[!redirects LCTVSs]]
[[!redirects LCTVSes]]

[[!redirects locally convex Hausdorff space]]
[[!redirects locally convex Hausdorff spaces]]
[[!redirects Hausdorff locally convex space]]
[[!redirects Hausdorff locally convex spaces]]
[[!redirects hausdorff locally convex space]]
