
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _higher homotopy van Kampen theorem_ is a theorem that asserts that the [[homotopy type]], or certain invariants thereof, of a [[topological space]] can be 'computed', in some sense, by a suitable [[colimit]] or [[homotopy colimit]] over the homotopy types / invariants of its pieces.

These all in some sense generalize the [[van Kampen theorem]], (SvKT), which only deals with the underlying 1-type (the fundamental groupoid). The actual statements of the results depend on the models of the homotopy invariants being considered.

## For topological spaces {#ForTopSpaces} (The homotopy small simplex theorem.)


The general form that this takes is similar to the classical homology small simplex theorem which can be found in many books on homology. This states that given an open cover, $\mathcal{U}$, of a space, $X$, the inclusion of the chain complex of $\mathcal{U}$-small singular simplices into the singular complex of $X$ induces isomorphisms on all homology groups. It is closely related to results on [[excision]] and on the [[Mayer-Vietoris sequence|Mayer-Vietoris theorem]].  Various homotopy analogues of this result have been given with one of the most recent being that given by Luire (see below). He explicitly relates it to the van Kampen theorem, and it is a similar 'local-to-global' result. 

The experience from the uses of the homology small simplex theorem suggests that it may be most useful when used in conjunction with specific invariants of homotopy types. (Note excision fails for homotopy groups and so one has to be more subtle.) The precise relationship to the other forms of generalised van Kampen theorem has yet to be determined.

### General statement (Small simplex theorem aka generalised SvKT)

+-- {: .un_theorem}
###### Theorem

Let $X$ be a [[topological space]], write $Op(X)$ for its [[category of open subsets]] and let

$$
  \chi : C \to Op(X)
$$

be a [[functor]] out of a [[small category]] $C$ such that

* for each point $x\in X$ the [[full subcategory]] $C_x$ of objects $c$ such that $\chi(c)$ contains $x$ has a [[weak homotopy equivalence|weakly]] [[contractible]] [[nerve]].

Then:

the canonical morphism in [[sSet]] out of the [[colimit]]

$$
   {\lim_\to} Sing \circ \chi \to Sing(X)
$$ 

into the [[singular simplicial complex]] of $X$ exhibits $Sing(X)$ as the [[homotopy colimit]]  $hocolim Sing \circ \chi$.


=--

This is theorem A.1.1 in ([Lurie](#Lurie)).

A related theorem is given by ([Dugger-Isaksen 2004](#DuggerIsaksen)) and earlier versions were given by [[G. Segal]], (amongst others).



This form of the general type of result gives a relationship between the homotopy type of the space and the homotopy types of parts of that space, telling one how they fit together.  To get explicit more 'algebraic' calculations out it has so far proved necessary to consider spaces with extra structure, such as a [[filtered topological space|filtration]] (Brown-Higgins). The explicit algebraic models do not, in general, give a complete classifying invariant of the homotopy types concerned, but that allows much more precise and calculable invariants  to be found. In the first 'strict' version, the invariant, namely the  [[fundamental ∞-groupoid]],  is a [[strict ∞-groupoid]] and could be substituted by the corresponding [[crossed complex]] (according to your taste and needs!)



## Filtered space / strict  ∞-groupoid generalisation of the SvKT (Brown-Higgins)


Suppose $X_*$ is a [[filtered space]] and $X$ is the union of the interiors of sets $U^i$, $i \in I$. Let $U^i_*$ be the filtered space given by the intersections $U^i \cap X_n$ for $n \geq 0$. If $d=(i,j) \in I^2$ we write $U^d$ for $U^i \cap U^j$. We then have a coequaliser diagram of filtered spaces 

$$\bigsqcup_{d \in I^2} U^d_* \rightrightarrows ^a_b \bigsqcup _{i \in I} U^i_* \to ^c X_*.$$

+-- {: .un_theorem}
###### Strict ∞-groupoid Higher van Kampen Theorem for filtered spaces.

If the filtered spaces $U^f_*$ are [[connected filtered space]]s for all finite intersections $U^f_*$ of the filtered spaces $U^i_*$, then

1. (Conn) The filtered space $X_*$ is connected; and

1. (Iso) The fundamental [[crossed complex]] functor $\Pi$ takes the above coequaliser diagram of filtered spaces to a coequaliser diagram of crossed complexes.

=--

**Remarks**

* Note that because $\Pi$ uses groupoids, it obviously takes disjoint unions $\bigsqcup$ of filtered spaces into disjoint unions (= coproducts) $\bigsqcup$ of crossed complexes. 

* The proof of the theorem is not direct but goes via the fundamental cubical $\omega$-groupoid with connections of the filtered spaces, as that context allows the notions of _algebraic inverse to subdivision_ and of _commutative cube_. However the proof is a direct generalisation of a proof for the [[van Kampen theorem]] for the [[fundamental groupoid]].  

* Applications of this theorem include many basic facts in algebraic topology, such as the Relative Hurewicz Theorem, the Brouwer degree theorem, and new nonabelian results on 2nd relative homotopy groups, not of course obtainable by the traditional wholly abelian methods. No use is made of _singular homology theory_ or of _simplicial approximation_.

* This result includes the crossed module version of the  generalised SvKT. This was the first extension in this direction. It handles relative homotopy groups. That version is also a special case of the next of this type of result given by the Brown-Loday theory.

##Generalised SvKT for models of $n$-types (Brown-Loday)

After [[Loday]] had proved that [[cat-n-group]]s modelled all connected [[homotopy n-type|homotopy (n+1)-type]]s, Brown and Loday investigated generalised forms of the SvKT, in terms of these new invariants. (to be continued)


## Van Kampen spectral sequence (Artin-Mazur)

Artin and Mazur proved the existence of a spectral sequence determined by the [[Cech complex]] of an open cover. This converges to the homotopy groups of the big space. There does nnot seem to have been any study done of the relationship of their results with the others mentioned above.  Their methods are very similar to those used for the Dugger-Isaksen small simplex theorem, however.


## For objects in a cohesive $(\infty,1)$-topos

In a [[cohesive (∞,1)-topos]] higher van Kampen theorems hold in great generality. 

See the section <a href="http://ncatlab.org/nlab/show/cohesive+(infinity%2C1)-topos#vanKampenTheorem">cohesive (∞,1)-topos -- van Kampen theorem</a>.

In particular for the cohesive $(\infty,1)$-topos [[?TopGrpd]] of [[topological ∞-groupoid]]s this reproduces the [topological higher van Kampen theorem](#ForTopSpaces) discussed above.


## Examples

Here is one application in dimension 2 not easily obtainable by traditional [[algebraic topology]]. 

Let $0 \to P \to Q \to R \to 0$ be an [[exact sequence]] of [[abelian groups]]. Let $X$  be the [[mapping cone]] of the induced map $K(P,1) \to K(Q,1)$ of [[Eilenberg-Mac Lane space]]s. Then a [[crossed module]] representing the [[homotopy 2-type]] of $X$ is $\mu: C \to Q$ where $C$ is abelian and is the direct sum $\oplus_{r \in R} P^r$  of copies of $P$ one for each $r \in R$ and the action of $Q$ is via $R$ and permutes the copies by $(p,r)^s=(p,r+s)$. Similar examples for $P,Q,R$ nonabelian are do-able,   more complicated, and certainly **not** obtainable by traditional methods.





## References
 {#References}

Various versions exist, generalising the classical theorem. 

The homology small simplex theorem is to be found, for instance, in [[Spanier]]'s book on algebraic topology.

The homotopy version for topological spaces and the [[fundamental infinity-groupoid]] functor is discussed in  [Appendix A.1](http://www.math.harvard.edu/~lurie/papers/DAG-VI.pdf#page=134) of

* [[Jacob Lurie]], _[[Ek-Algebras]]_ (now part of _[[Higher Algebra]]_)

A very similar result occurs before as prop. A.5 in

* [[Graeme Segal]], _Classifying spaces related to foliations_, Topology, Vol 17, (1978) 367-382
 {#Segal}

An important  central lemma (the _small simplices theorem_) also appears as corollary 3.5 of 

* [[Daniel Dugger]], [[Daniel Isaksen]], _Topological hypercovers and $\mathbb{A}^1$-realizations_, Mathematische Zeitschrift 246 (2004)
 {#DuggerIsaksen}
where many similar results are discussed.

The version for filtered topological spaces and the strict homotopy $\infty$-groupoid functor was one of the aims of the long research programme of [[Ronnie Brown]] and [[Philip Higgins]]. For the original work see the publication lists of Brown and Higgins.  A complete view of this approach is discussed in

* [[Ronnie Brown]], [[Philip Higgins]], [[Rafael Sivera]], _[[Nonabelian Algebraic Topology]]_


The Brown-Loday results can be found in 

* R. Brown and [[J.-L. Loday]], _Homotopical excision, and Hurewicz theorems for n-cubes of spaces_, Proc. London Math. Soc., (3)54, (1987), 
176 &#8211; 192. 

and 

*  R. Brown and [[J.-L. Loday]], _Van Kampen Theorems for diagrams of 
spaces_, Topology, 26, (1987), 311 &#8211; 337. 

The paper of Artin and Mazur is
 
* [[M. Artin]] and [[B. Mazur]], _On the van Kampen theorem_, [Topology, vol. 5 (1966), pp. 179 - 189](http://www.maths.ed.ac.uk/~aar/topology/Topology%20Vol%2005/Artin_On-the-van-Kampen-theorem_1966.pdf).

[[!redirects Higher Homotopy van Kampen Theorem]]
[[!redirects higher homotopy van Kampen Theorem]]

[[!redirects higher van Kampen theorem]]

[[!redirects higher homotopy van Kampen theorem]]

[[!redirects higher van Kampen theorems]]
[[!redirects Higher van Kampen Theorem]]
[[!redirects Higher van Kampen Theorems]]
[[!redirects higher homotopy van Kampen theorems]]