
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents 
{:toc}

## Idea

The _Moore complex_ of a [[simplicial group]] -- better known in its normalized version as the **normalized chains complex** -- is a [[chain complex]] whose [[differential]] is built from the face maps of the simplicial group.

The operation of forming the Moore complex of chains of a [[simplicial group]] is one part of the [[Dold-Kan correspondence]] that relates [[simplicial object|simplicial]] (abelian) [[group]]s and [[chain complex]]es.

Recall that a [[simplicial group]] $G$, being in particular a [[Kan complex]], may be thought of, in the sense of the [[homotopy hypothesis]], as a combinatorial space equipped with a group structure. The

* _Moore complex_ 

or 

* _normalized Moore complex_ 

of $G$ is a [[chain complex]] 

* whose $n$-cells are the "$n$-disks with basepoint on their boundary" in this space, with the basepoint sitting on the identity element of the space;

* the boundary map on which acts literally like a boundary map should: it sends an $n$-disk to its boundary, read as an $(n-1)$-disk whose entire boundary is concentrated at the identity point.

This is entirely analogous to how a [[crossed complex]] is obtained from a [[strict omega-groupoid]].

## Definition


Given a [[simplicial group]] $G$, the **Moore complex** (or normalized chain complex), $(N G,\partial )$,  of $G$ is the non-Abelian chain complex defined as the joint [[kernel]] 
$$
N G_n=\bigcap_{i=1}^{n}Ker\,d_i^n 
$$
with $\partial _n:N G_n\rightarrow N G_{n-1}$ induced from $d_0^n$ by
restriction. 


* **Notice:** there is no assumption that $G$ and hence the $N G_n$ are Abelian. But often in the literature the Moore complex is considered only in the special case of the above where all groups involved are Abelian.


So an element in degree 1 element $g \in N G_1$ is a 1-disk

$$
  1 \stackrel{g}{\to} \partial g
  \,,
$$

an element $h \im N G_2$ is a 2-disk

$$
  \array{
     && 1 
     \\
     & {}^1\nearrow &\Downarrow^h& \searrow^{\partial h}
     \\
     1
     &&\stackrel{1}{\to}&&
     1
  }
  \,,
$$

a degree 2 element in the kernel of the boundary map is such a 2-disk that is closed to a 2-spehere

$$
  \array{
     && 1 
     \\
     & {}^1\nearrow &\Downarrow^h& \searrow^{\partial h = 1}
     \\
     1
     &&\stackrel{1}{\to}&&
     1
  }
  \,,
$$

etc.



+-- {: .un_lemma}
###### Lemma

The Moore complex is a [[normal complex of groups]].

=--


+-- {: .un_remark}
###### Remark


* There is an alternative form of this construction using $\bigcap_{i=0}^{n-1}Ker\,d_i^n$ instead of $\bigcap_{i=1}^{n}Ker\,d_i^n$, and with the differential $\partial$ defined using the last face map $d^n_n$ instead of the first. The theories run parallel but the fact there are two valid forms can be confusing for the formulae for various derived structures. 

*  The notation $N G$ is quite widely used in the literature but can get confused with that sometimes used for the [[nerve]] functor, so care is needed. (We have therefore used $\mathcal{N}$ for the latter.) The $N$ here stands for 'normalised'.

=--


At least for $G$ an _abelian_ simplicial group, there are two other complexes naturally associated with it:

* the **alternating face map complex** of $G$, usually just denoted "$G$" itself: in degree $n$ this exactly the group $G_n$, and the differential is given by
  $$
    \partial = \sum_{i = 0}^n (-1)^i d_i
  $$

* the **complex modulo degeneracies**, sometimes denoted $G/D G$ which is obtained from $G$ by dividing out degeneracies, i.e. cells in the image of a degeneracy map.

All three of these chain complexes are essentially the same:

+-- {: .un_theorem}
###### Theorem

There is 

* an isomorphism of chain complexes
  $$
    N G = G / D G
    \,.
  $$

* a quasi-isomorphism of chain complexes
  $$
    N G \simeq G
    \,.
  $$


=--

This is in section 3 of 

* Goerss--Jardine, _Simplicial homotopy theory_. Theorem 2.4 [here](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi).

This indicates that probably

* $G$ should be called "the Moore complex"

* $N G$ should be called "the normalized Moore complex".

Both describe the same complex, up to quasi-isomorphism, but $G$ is "big" while $N G$ encodes the same information more efficiently.
 

## Properties

### Homology and homotopy groups

If an element $g \in G_n$ is in the Moore complex then all but its zeroth face is trivial. In dimension 1, this means that $g$ is a 1-simplex that 'starts' at the identity element of $G_0$. If this $g$ is in the kernel of the boundary map 
$\partial _1: N G_1\rightarrow N G_{0},$
 then $g$ will be a loop at that identity. If it is $\partial x$ for some $x\in N G_2$, then $x$ intuitively provides a homotopy between $g$ and the identity element.  This motivates the following definition:

+--{.un_defn}
###### Definition

The **n$^{th}$ homotopy group**, $\pi_n$(G), of $G$ is the $n^{th}$ homology of the Moore complex of $G$, i.e.,  
$$
\pi _n({G})  \cong  H_n( {N G},\partial ),   = \big( \bigcap_{i=0}^n Ker\,d_i^n\big)/d_{0}^{n+1}\big(\bigcap_{i=1}^{n+1} Ker\,d_i^{n+1}\big). 
$$

=--

Note that $\partial N G_{n+1}\triangleleft  N G_n$.

### Further structure on the Moore complex 

In the case of simplicial Abelian groups or more generally, simplicial modules over a ring, the Moore complex of such an object is merely a chain complex of the same sort of objects by the [[Dold-Kan correspondence]]. Various non-commutative forms of that result have been proved, for instance,  [[group T-complex]]es are equivalent to [[crossed complex]]es, by a result of Ashley,

* N. Ashley, _Simplicial $T$-Complexes: a non abelian version of a theorem of Dold--Kan_ , Dissertations Math., 165, (1989), 11--58.

In general, for simplicial groups, the Moore complex has a beautiful structure of pairings described by Pilar Carasco, in her thesis and in the resulting paper,

* P. Carrasco and A. M. Cegarra, Group-theoretic Algebraic Models for Homotopy Types , J. Pure Appl. Alg., 75, (1991), 195--235

The resulting structure is that of a [[hypercrossed complex]]. Typically one has pairings 
$$N G_p \times N G_q \to N G_{p+q}.$$
These are well understood in low dimensions, see the entry on [[hypercrossed complex]] for more details. 

* Suppose that $G$ is a simplicial group with Moore complex $N G$, which satisfies $N G_k = 1$ for $k\gt 1$, then $(G_1,G_0,d_1,d_0)$ has the structure of a [[2-group]]. The [[interchange law]] is satisfied since the corresponding equation in $G_1$ is always the image of an element in $N G_2$, and here that must be trivial. If one thinks of the 2-group as being specified by a [[crossed module]] $(C,P,\delta, a)$, then in terms of the original simplicial group, $G$,  $N G_0 = G_0 = P$, $N G_1 \cong C$, $ \partial = \delta$ and the action of $P$ on $C$ translates to an action of $N G_0$ on $N G_1$ using conjugation by $s_0(p)$, i.e., for $p\in G_0$ and $c\in N G_1$, 
$$a(p)(c) = s_0(p)c s_0(p)^{-1}.$$


* Suppose next that $N G_k = 1$ for $k \gt 2$, then the Moore complex is a [[2-crossed module]] in the sense of Conduch&#233;.  Such objects model all [[homotopy 3-type]]s.  They are related to the [[crossed square]]s of Guin-Valery and Loday, in that there is a functor from crossed squares to $2$-crossed modules which preserves homotopy types, but crossed squares have the advantage that there is a homotopically defined functor with values in crossed squares, related to classical homotopy invariants of pairs and triads, and which satisfies a [[higher homotopy van Kampen theorem]], so that some calculations are possible. 

## References

A discussion of the Moore complex with an emphasis of its generalization to the non-abelian situation is in section 1.3.3 of

* [[Tim Porter]], [[Tim Porter:crossed menagerie|The Crossed Menagerie]]

A standard reference for the plain abelian version of the Moore and normalized chain complex is
for instance [chapter III.2](http://www.maths.abdn.ac.uk/~bensondj/papers/g/goerss-jardine/ch-3.dvi) of 

* Goerss, Jardine, _Simplicial Homotopy Theory_ ([web](http://www.maths.abdn.ac.uk/~bensondj/html/archive/goerss-jardine.html))
 
Notice that Goerss--Jardine write "normalized chain complex" for the complex that elsewhere in the literature would be called just "Moore complex", whereas what Goerss--Jardine call "Moore complex" is sometime maybe just called "alternating sum complex".


[[!redirects Moore-complex]]