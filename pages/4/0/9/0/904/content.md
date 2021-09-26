
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea 

The _fundamental group_ $\pi_1(X,x)$ of a [[pointed object|pointed]] [[topological space]] $(X,x)$ is the group of based [[homotopy classes]] of [[loops]] at $x$, with multiplication defined by concatenation (following one path by another).  

This is also called _the first [[homotopy group]]_ of $X$.

The notion of _fundamental group_ $\pi_1(X,x)$ generalises in one direction to the [[fundamental groupoid]] $\Pi_1(X)$, or in another direction to the [[homotopy groups]] $\pi_n(X,a)$ for $n \in \mathbb{N}$. Both of this is contained within the [[fundamental ∞-groupoid]] $\Pi(X)$.


## Definition

+-- {: .num_defn}
###### Definition

For $X$ a [[topological space]] and $x : * \to X$ a [[point]]. A [[loop space|loop]] in $X$ based at $x$ is a [[continuous function]]

$$
  \gamma : \Delta^1  \to X
$$

from the topological 1-[[simplex]], such that $\gamma(0) = \gamma(1) = x$.

A _based [[homotopy]]_ between two loops is a [[homotopy]] 

$$
  \array{
    \Delta^1
    \\
    \downarrow^{\mathrlap{(id,\delta_0)}} & \searrow^{\mathrlap{f}}
    \\
    \Delta^1 \times \Delta^1 &\stackrel{\eta}{\to}& X
    \\
    \uparrow^{\mathrlap{(id,\delta_1)}} & \nearrow_{\mathrlap{g}}
    \\
    \Delta^1
  }
$$

such that $\eta(0,-) = \eta(1,-) = x$.

=--

+-- {: .num_prop}
###### Proposition

This notion of based homotopy is an [[equivalence relation]].

=--

+-- {: .proof}
###### Proof

This is directly checked. It is also a special case of the general discussion at _[[homotopy]]_. 

=--


+-- {: .num_definition #Concatenation}
###### Definition

Given two loops $\gamma_1, \gamma_2 : \Delta^1 \to X$, define their 
**concatenation** to be the loop

$$
  \gamma_2 \cdot \gamma_1 : t \mapsto
  \left\{
    \array{
      \gamma_1(2 t) & ( 0 \leq t \leq 1/2 )
      \\
      \gamma_2(2 (t-1/2)) & (1/2 \leq t \leq 1) 
    }
  \right.
  \,.
$$

=--

+-- {: .num_prop #GroupStructure}
###### Proposition

Concatenation of loops respects based homotopy classes
where it becomes an [[associativity|associative]], [[unital]]
binary pairing with [[inverses]], hence the product in a [[group]].

=--

+-- {: .num_remark}
###### Remark

See also at _[[path groupoid]]_ for similar constructions.

=--

+-- {: .num_defn}
###### Definition

For $X$ a topological space and $x \in X$ a point, the set of based homotopy equivalence classes of based loops in $X$ equipped with the group structure from prop. \ref{GroupStructure} is the **fundamental group** or **first [[homotopy group]]** of $(X,x)$, denoted

$$
  \pi_1(X,x) \in Grp
  \,.
$$

=--

Hence if we write $[\gamma] \in p_1(X,x)$ for the based homotopy class of a loop $p$, then then group operation is

$$
  [\gamma_1] \cdot [\gamma_2] \coloneqq [\gamma_1 \cdot \gamma_2]
  \,.
$$

+-- {: .num_defn #SimplyConnectedSpace}
###### Definition

A [[topological space]] whose fundamental group is trivial is called a 
_[[simply connected topological space]]_. 

=--

+-- {: .num_defn #EMSpace}
###### Definition

Conversely, a topological space whose only non-trivial [[homotopy group]] is the fundamental group is called an [[Eilenberg-MacLane space]] denoted $K(\pi_1(X), 1)$.

=--

## Properties

### Naturality

+-- {: .num_prop}
###### Proposition

If a topological space $X$ is path-[[connected space]], then all of the fundamental groups $\pi_1(X,x)$ are [[isomorphism|isomorphic]], for all choices of base points $x \in X$.

=--

+-- {: .proof}
###### Proof

For $x_0, x_1 \in X$ any two basepoints, there is by assumption a path connecting them, hence a [[continuous function]]

$$
  p : \Delta^1 \to X
$$

such that $p(0) = x_0$ and $p(1) = x_1$. 

Write $\bar p \coloneqq (p(1-(-)))$ for the same path with the orientation reversed. Then for $\gamma_0$ any loop based at $x_0$, the concatenation 
$ [ p \cdot (\gamma_0 \cdot \bar p) ]$, def. \ref{Concatenation} yield a loop based at $x_1$ (obtained from $[\gamma_0]$ by [[conjugation]] with $[p]$).

It is immediate to check that this induces an [[isomorphism]]

$$
  Ad_{[p]} : \pi_1(X,x_0) \to \pi_1(X,x_1)
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

Therefore one sometimes loosely speaks of 'the' fundamental group of a connected space. But beware that the isomorphism in the above construction is not unique. Therefore forming fundamental groups is not a [[functor]] on connected spaces. 
=--

+-- {: .num_prop}
###### Proposition

It is, however, a functor on [[pointed object|pointed topological spaces]]:
$\pi_1(-) :$ [[Top]] ${}^{*/} \to$ [[Grp]].

=--

### Relation to singular homology
 {#RelationToSingularHomology}

The fundamental group is in general non-abelian (i.e. is not an [[abelian group]]), the  [Examples](#Examples) below. For a connected topological space $X$, its _[[abelianization]]_ is equivalent to the first [[singular homology]] group

$$
  \pi_1(X,x)^{ab} \simeq H_1(X)
  \,.
$$

See at _[singular homology -- Relation to homotopy groups](singular%20homology#RelationToHomotopyGroups)_ for more on this.


### Relation to universal covers and Galois groups

There is a relation to [[universal cover|universal covers]]: Under suitable conditions the group of cover automorphisms of a universal cover is isomorphic to the fundamental group of the covered space. This is the topic of the _[[étale fundamental group]]_, also referred to at _[[Chevalley fundamental group]]_, see there for more.

In particular in [[algebraic geometry]] and [[arithmetic geometry]] this essentially identifies the concept of fundamental group with that of _[[Galois groups]]_. For this reason one also speaks of the _[[algebraic fundamental group]]_ in this context. See at _[[Galois theory]]_ for more on this. 

See also at _[[link between Galois theory and fundamental groups]]_. 

In [[Grothendieck's Galois theory]], the role of the basepoint is replaced by considering a 'fibre functor' $F:\mathcal{C}\to Sets$ or to $FinSets$, where $\mathcal{C}$ is the category of coverings of the given space. This theory extends to other situations and the term [[algebraic fundamental group]] is used in particular for the case of [[scheme]]s (of a suitable type); see (SGA1).


## Generalizations

### Non-locally 'nice' spaces and 'generalised' spaces

The definition of fundamental group in terms of homotopy classes of loops at a base point does not work well for the spaces that occur in [[algebraic geometry]], nor for many spaces considered in analysis as there may be very few loops.  For instance, for a [[scheme]] there are in general very few paths, and [[Grothendieck]] gave a definition of a fundamental group in SGA1 which is closely related to the [[Galois group|Galois groups]] of number theory, but in cases where both the path-based group and this [[algebraic fundamental group]] make sense, the algebraic form tends to be related to the [[profinite completion of a group|profinite completion]] of the topological fundamental group; see the example in that entry.

A similar type of construction gives the [[fundamental group of a topos]]. Other related forms include a &#268;ech version of the fundamental group used in shape theory, and linked to &#268;ech homology groups of a compact space.

The notion of fundamental group generalizes to that of [[fundamental groupoid]] in both the loop based theory and in [[Grothendieck's Galois theory]] as described in [[SGA1]]. In this form it has been used to give generalisations for simplicial profinite spaces in work by Quick and to [[pro-spaces]] in work of Isaksen.
  

### Proper fundamental groups

In the context of [[proper homotopy theory]] there are two related fundamental groups for single ended spaces. 

## Examples
 {#Examples}

+-- {: .num_example #EuclideanSpaceFundamentalGroup}
###### Example
**(Euclidean space is [[simply connected topological space|simply connected]])**

For $n \in \mathbb{N}$, let $\mathbb{R}^n$ be the $n$-dimensional
[[Euclidean space]] with its [[metric topology]]. Then for every
point $x \in \mathbb{R}^n$ the fundamental group is trivial:

$$
  \pi_1(\mathbb{R}^n, x) = 1
  \,.
$$

=--

+-- {: .proof}
###### Proof

Let 

$$
  \gamma \;\colon\; [0,1] \longrightarrow \mathbb{R}^n
$$

be [[loop]] at $x$, hence a [[continuous function]] with $\gamma(0) = x$ and $\gamma(1) = x$. Using the [[real vector space]] structure on $\mathbb{R}^n$, we may define the function


$$
  \array{
    [0,1] \times [0,1] &\overset{\eta}{\longrightarrow}& \mathbb{R}^n
    \\
    (t,s) &\mapsto& x + s (\gamma(t) - x)
  }
  \,.
$$

This is a [[continuous function]], since it is the composite of the continuous function $(id_{[0,1]} \times \gamma) \;\colon\; (t,s) \mapsto (\gamma(t),s)$ (which is continuous as the [[product topological space|product]] of two continuous functions) and the function $(v,s) \mapsto x + s ( v - x )$ (which is continuous since [[polynomials are continuous]]).

Moreover, by construction we have

$$
  \eta(-,1) = \gamma(-)
   \phantom{AAAA}
  \eta(-,0) = const_x
  \,.
$$

Therefore this is a [[homotopy]] from $\gamma$ to the constant loop at $x$.


=--

+-- {: .num_example}
###### Example

By definition \ref{SimplyConnectedSpace}, the fundamental group of every [[simply connected topological space]] is trivial.

=--

+-- {: .num_example}
###### Example

The [[fundamental group of the circle is the integers]]: 

$$
  \pi_1(S^1) \simeq \mathbb{Z}
  \,.
$$

=--

+-- {: .num_remark}
###### Remark

An instructive formalization of this basic statement in [[homotopy type theory]] is in ([Shulman](#Shulman)).

=--

+-- {: .num_example}
###### Example

By definition \ref{EMSpace}, the fundamental group of any [[Eilenberg-MacLane space]] $K(G,1)$ is $G$: $\pi_1(K(G,1)) = G$.

=--

## Related concept

* [[fundamental theorem of covering spaces]]

* [[winding number]]

* [[algebraic fundamental group]]

* [[anabelian geometry]]

* [[Chevalley fundamental group]]

* [[etale homotopy]]

* [[Grothendieck's Galois theory]]


## References

Historical origins:

* [[Henri Poincaré]], *[[Analysis Situs]]*, Journal de l'École Polytechnique. (2). 1: 1–123  (1895) (Orig.: [gallica:12148/bpt6k4337198/f7](https://gallica.bnf.fr/ark:/12148/bpt6k4337198/f7), Engl.: [[John Stillwell]]: [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/poincare2009.pdf), [[Stillwell_AnalysisSitus.pdf:file]])

Textbook accounts: 


* {#AGP02} [[Marcelo Aguilar]], [[Samuel Gitler]], [[Carlos Prieto]], Section 2.5 of: _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

Lecture notes:

* [[Jesper Møller]], _The fundamental group and covering spaces_ ([pdf](http://www.math.ku.dk/~moller/f03/algtop/notes/covering.pdf))


Discussion from the point of view of [[Galois theory]] is in 

* [[Luis Javier Hernández-Paricio]], _Fundamental pro-groupoids and covering projections_([pdf](http://matwbn.icm.edu.pl/ksiazki/fm/fm156/fm15611.pdf))

See also:

* [[D. C. Isaksen]], _A model structure on the category of pro-simplicial sets_,  Trans. Amer. Math. Soc., 353, (2001), 2805&#8211;2841

* [[G. Quick]], _Profinite homotopy theory_, Documenta Mathematica, 13, (2008), 585&#8211;612. 
 
Proof in [[homotopy type theory]] that the [[fundamental group of the circle is the integers]]:
 
* [[Daniel Licata]], [[Michael Shulman]], _Calculating the Fundamental Group of the Circle in Homotopy Type Theory_,  ([arXiv:1301.3443](https://arxiv.org/abs/1301.3443))

* [[UF-IAS-2012|Univalent Foundations Project]], section 8.1 of _[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]_

the HoTT-[[Coq]]-code is at

* {#Shulman} [[Mike Shulman]], _[P1S1.v](https://github.com/HoTT/HoTT/blob/master/Coq/HIT/Pi1S1.v)_



[[!redirects fundamental groups]]