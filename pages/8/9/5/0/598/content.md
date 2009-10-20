
#Contents#
* automatic table of contents goes here
{:toc}

#Idea#

Recall that a [[simplicial set]] is a combinatorial [[model structure on simplicial sets|model]] for a [[topological space]]. This relation is most immediate when the simplicial set is in fact a [[Kan complex]] (an [[∞-groupoid]]).

A _simplicial group_ is a simplicial set with the structure of a [[group]] on it. It turns out that this necessarily means that it is also a [[Kan complex]]. Therefore a simplicial group is

* an [[∞-groupoid]] with an extra group structure on it;

* a model for a topological space with a group structure.

Accordingly (as discussed at [[group]]) a simplicial group $G$ gives rise to 

* a one-object $\infty$-groupoid $\mathbf{B} G$ whose explicit standard realization as a [[simplicial set]] is denoted $\bar W G$

* an $\infty$-groupoid $\mathbf{E} G$ whose explicit standatd realization as a [[simplicial set]] (even a simplicial group, again) is denoted $W G$

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


#Definition#
 A **simplicial group**, $G$, is a [[simplicial object]] in the category of groups.

#Notation# 
The category of simplicial groups is the category of functors from $\Delta^{op}$ to [[Grp]].  It will be denoted $\Simp\Grp$.

#Properties#


+-- {: .un_theorem}
###### Theorem (J. C. Moore)

The [[simplicial set]] underlying any simplicial group
(by forgetting the group structure) is a [[Kan complex]].

=--

In fact, not only are the [[horn]] fillers guaranteed to exist, but there is an algorithm that provide explicit fillers.  This implies that constructions on a simplicial group that use fillers of horns can often be adjusted to be functorial by using the algorithmically defined fillers.  An argument that just uses 'existence' of fillers can be refined to give something more 'coherent'.


+-- {: .proof}
###### Proof

Let $G$ be a simplicial group. 

Here is the explicit algorithm that computes the horn fillers:

Let $(y_0,\ldots, y_{k-1}, -,y_{k+1}, \ldots, y_n)$ give a [[horn]] in $G_{n-1}$, so the $y_i$s are $(n-1)$ simplices that fit together as if they were all but one, the $k^{th}$ one,  of the faces of an $n$-simplex. There are three cases: 

1. if $k = 0$: 

   * Let  $w_n = s_{n-1}y_n$ and then $w_i = w_{i+1}(s_{i-1}d_i w_{i+1})^{-1}s_{i-1}y_i$ for  $i = n, \ldots, 1$, then  $w_1 $ satisfies $d_i w_1 = y_i$, $i\neq  0$;

1. if $0\lt k \lt n$: 

   * Let $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, k-1$, then take $w_n = w_{k-1}(s_{n-1}d_nw_{k-1})^{-1}s_{n-1}y_n$, and finally a downwards induction given by $w_i = w_{i+1}(s_{i-1}d_iw_{i+1})^{-1}s_{i-1}y_i$, for $i = n, \ldots, k+1$, then $w_{k+1}$ gives $d_iw_{k+1} = y_i$ for $i \neq k$;


3. if $k=n$: 

   * use $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, n-1$, then $w_{n-1}$ satisfies $d_iw_{n-1} = y_i$, $i\neq n$.



=--

**Remark** 

* The filler for any horn can be chosen to be a _product of degenerate elements_.

* The [[simplicial homotopy groups]] of a simplicial group, $G$, can be calculated as the homology groups of the [[Moore complex]] of $G$.  This is, in general,  a non-Abelian chain complex.

* A simplicial group can be considered as a [[simplicial groupoid]] having exactly one object. If $G$ is a simplicial group, the suggested notation for the corresponding simplicially enriched groupoid would be $\mathbf{B}G$ according to notational conventions suggested elsewhere in the nLab.

* There is a functor due to Dwyer and Kan, called the [[Dwyer-Kan loop groupoid]] that takes a  simplicial set to a simplcial groupoid. This has a left adjoint $\overline{W}$ (see below), called the _classifying space_ functor, and together they give an equivalence of categories between the homotopy category of simplical sets and that of simplicial groupoids. We thus have that all homotopy types are modelled by simplicial groupoids ... and for connected homotopy types by simplicial groups. One *important fact* to note in this equivalence is that it shifts dimension by 1, so if $G(K)$ is the simplicial group corresponding to the connected simplicial set $K$ then $\pi_k(K)$ is the same as $\pi_{k-1}(G(K))$.  This is important when considering algebraic models for a [[homotopy n-type]].

#  The adjunction between simplicial groups and simplicial sets #

+-- {: .un_lemma}
###### Lemma

The [[stuff, structure, property|forgetful functor]]

$$
  F : AbSGrpg \to SSet
$$

from simplicial abelian group to the underlying [[simplicial sets]] has a [[left adjoint]]

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


# Classifying space and universal bundle of a simplicial group. #

Every simplicial group $H$ gives rise to a one-object [[∞-groupoid]] $\mathbf{B} G$ whose explicit realization as a [[Kan complex]] is traditionally denoted $\bar W H$.

We will give this in the more general form needed for a [[simplicial groupoid]].

For a general discussion on [[classifying space|classifying spaces]] go to that entry.

Let $H$ be a simplicial groupoid, then $\overline{W}H$ is the simplicial set  described by

* $(\overline{W}H)_0 = ob(H_0)$, the set of objects of the groupoid of 0-simplices (and hence of the groupoid at each level);

* $(\overline{W}H)_1 = arr(H_0)$, the set of arrows of the groupoid $H_0$:


and for $n \geq 2$,

*  $(\overline{W}H)_n = \{(h_{n-1}, \ldots ,h_0)| h_i \in arr(H_i)$  and $s(h_{i-1}) = t(h_i), 0\lt i\lt n\}$.

Here  $s$ and $t$ are generic symbols for the domain and codomain mappings of all the groupoids involved.  The face and degeneracy mappings between 
$\overline{W}(H)_1$ and $\overline{W}(H)_0$ are the source and target maps and the identity maps of $H_0$, respectively; whilst the face and degeneracy maps at higher levels are given as follows:

The face and degeneracy maps are given by

* $d_0(h_{n-1}, \ldots, h_0) = (h_{n-2}, \ldots, h_0)$;


*  for $0 \lt  i\lt  n$, $d_i(h_{n-1}, \ldots, h_0)  = (d_{i-1}h_{n-1}, d_{i-2}h_{n-2}, \ldots, d_0h_{n-i}h_{n-i-1},h_{n-i-2}, \ldots , h_0)$; 

 and


*  $d_n(h_{n-1}, \ldots, h_0) = (d_{n-1}h_{n-1}, d_{n-2}h_{n-2}, \ldots, d_1h_{1})$;


 whilst

*  $s_0(h_{n-1}, \ldots, h_0) = (id_{dom(h_{n-1})},h_{n-1}, \ldots, h_0) $;

 and,


* for $0\lt i \leq n$, $s_i(h_{n-1}, \ldots, h_0) = (s_{i-1}h_{n-1}, \ldots, s_0h_{n-i}, id_{cod(h_{n-i})},h_{n-i-1}, \ldots,  h_0) $.





# References #

A standard reference for the case of _abelian_ simplicial groups is [chapter 5](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-5.dvi) of

* Gorss-Jardine, _Simplicial homotopy theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))

Section 1.3.3 of

* [[Tim Porter]], [[Tim Porter:crossed menagerie|The Crossed Menagerie]] 

discusses simplicial groups in the context of [[nonabelian algebraic topology]].

The algorithm for finding the horn fillers in a simplicial group is given in the proof of

theorem 17.1, page 67 of

* P. May, _Simplicial Objects in Algebraic Topology_ .

The theorem that every simplicial group is a Kan complex is originally due to

* J. C. Moore, _Algebraic homotopy theory_, lecture notes, Princeton University, 1955--1956

[[Note on Formatting|?]]

[[!redirects simplicial groups]]