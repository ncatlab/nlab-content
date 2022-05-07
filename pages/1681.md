
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


#Contents#
* table of contents
{:toc}

## Idea

An _Eilenberg--Mac Lane space_ is a connected [[topological space]] with nontrivial [[homotopy groups]] only in a single degree.

## Definition

### Characterization

For $n \in \mathbb{N}$ and $G$ a group, and an [[abelian group]] if $n \geq 2$, then an _Eilenberg-MacLane space_ $K(G,n)$ is a [[topological space]] with the property that all its [[homotopy groups]] are trivial, except that in degree $n$, which is $G$.


### Constructions

#### Via geometric realization of higher groupoids

For $G$ a [[group]], the _Eilenberg--Mac Lane space_ $K(G,1)$ is the image under the [[homotopy hypothesis]] [[Quillen equivalence]] $|-| : \infty Grpd \to Top$ of the one-object groupoid $\mathbf{B}G$ whose [[hom-set]] is $G$:

$$
  K(G,1) = | \mathbf{B} G |
  \,.
$$


The construction of EM-spaces $K(A,n)$ for an [[abelian group]] $A$ may be given by the [[Dold-Kan correspondence]] between [[chain complexes]] and [[simplicial abelian groups]]: let $A[-n]$ be the chain complex which is $A$ in dimension $n$ and zero elsewhere; the geometric realisation of the corresponding simplicial abelian group is then a $K(A,n)$. 


We can include the case $n=1$ when $G$ may be nonabelian, by regarding $C(G,n)$ as a [[crossed complex]]. Its [[classifying space]] $B(C(G,n))$ is then a $K(G,n)$. (This also includes the case $n=0$ when $G$ is just a set!) This method also allows for the construction of $K(M,n;G,1)$ where $G$ is a group, or groupoid,  and $M$ is a $G$-module. This gives a space with $\pi_1 =G$, $\pi_n=M$ all other homotopy trivial, and with the given operation of $\pi_1$ on $\pi_n$. 


For $A$ an abelian group, the Eilenberg--Mac Lane space $K(A,n)$ is the image of the [[∞-groupoid]] $\mathbf{B}^n A$ that is the [[strict ∞-groupoid]] given by the [[crossed complex]] $[\mathbf{B}^n A]$ that is trivial everywhere except in degree $n$, where it is $A$:

$$
  \begin{aligned}
    [\mathbf{B}^n A] &=
     (  \cdots \to [\mathbf{B}^n A]_{n+1} \to [\mathbf{B}^n A]_{n} \to 
     [\mathbf{B}^n A]_{n-1} \cdots \to [\mathbf{B}^n A]_{1} \stackrel{\to}{\to} [\mathbf{B}^n A]_{0})
      \\ &=
    (  \cdots \to {*} \to A \to 
    {*} \cdots \to {*} \stackrel{\to}{\to} {*})
  \end{aligned}
  \,.
$$


So

$$
  K(A,n) = |\mathbf{B}^n A|
  \,.
$$

Therefore Eilenberg--Mac Lane spaces constitute a [[spectrum]]: the [[Eilenberg-Mac Lane spectrum]].

In general, if $A$ is an abelian [[topological group]], then there exist a model for the [[classifying space]] $\mathcal{B}A$ which is an abelian topological group. Iterating this construction, one has a notion of $\mathcal{B}^n A$ and a model for it which is an abelian topological group. If moreover $A$ is discrete, then $\mathcal{B}A=|\mathbf{B}A|=K(A,1)$, and one inductively sees that $\mathcal{B}^n A=|\mathbf{B}^n A|=K(A,n)$. Therefore one has a model for $K(A,n)$ which is an abelian topological group.

See for instance ([May, chapter 16, section 5](#May))

#### Via linearization of spheres

+-- {: .num_defn #ReducedALinearizationOfnSphere}
###### Definition

For $A$ an [[abelian group]] and $n \in \mathbb{N}$, the **reduced $A$-linearization** $A[S^n]_\ast$ of the [[n-sphere]] $S^n$ is the [[topological space]], whose underlying set is the [[quotient]] 

$$
  \underset{k \in \mathbb{N}}{\sqcup}
   A^k \times (S^n)^k
  \longrightarrow
  A[S^n]_\ast
$$

of the [[tensor product]]  with $A$ of the [[free abelian group]] on the underlying set of $S^n$, by the relation that identifies every [[formal linear combination]] of the (any fixed) basepoint of $S^n$ with 0. The [[topological space|topology]] is the induced [[quotient topology]] (of the [[disjoint union]] of [[product topological spaces]], where $A$ is equipped with the [[discrete topology]]).

=--

([Aguilar-Gitler-Prieto 02, def. 6.4.20](#AguilarGitlerPrieto02))


+-- {: .num_prop #ReducedALinearizationOfnSphereIsEMSpace}
###### Proposition

For $A$ a [[countable set|countable]] [[abelian group]], then the reduced $A$-linearization $A[S^n]_\ast$ (def. \ref{ReducedALinearizationOfnSphere}) is an [[Eilenberg-MacLane space]], in that its [[homotopy groups]] are

$$
  \pi_q(A[S^n]_\ast)
   \simeq
   \left\{
     \array{
       A & if \; q = n
       \\
       \ast & otherwise
     }
   \right.
$$

(in particular for $n \geq 1$ then there is a unique connected component and hence we need not specify a basepoint for the homotopy group).


=--

([Aguilar-Gitler-Prieto 02, corollary 6.4.23](#AguilarGitlerPrieto02))


+-- {: .num_remark}
###### Remark

The topological space $A[S^n]_\ast$ in definition \ref{ReducedALinearizationOfnSphere} has a canonical continuous [[action]] of the [[orthogonal group]] $O(n)$, by regarding $S^n \simeq (\mathbb{R}^n)^\ast$ as the [[one-point compactification]] of [[Cartesian space]]. Hence, in view of prop. \ref{ReducedALinearizationOfnSphereIsEMSpace}, these models for EM-spaces lend themselves to the defintiion of [[Eilenberg-MacLane spectra]] as [[orthogonal spectra]]. See [there](Eilenberg-Mac+Lane+spectrum#AsSymmetricSpectra).

=--


## Cohomology 

### With coefficients being EM-spaces

One common use of Eilenberg--Mac Lane spaces is as coefficient objects for "ordinary" [[cohomology]] (see e.g. [May, chapter 22](#May)).

The $n$th "ordinary" [[cohomology]] of a [[topological space]] $X$ with coefficients in $G$ (when $n=1$) or $A$ (generally) is the collection of [[homotopy]] classes of maps from $X$ into $K(G,1)$ or $K(A,n)$, respectively:

$$
  H^1(X,G) = Ho_{Top}(X, K(G,1)) = Ho_{\infty Grpd}(X, \mathbf{B} G)
$$

$$
  H^n(X,A) = Ho_{Top}(X, K(A,n)) = Ho_{\infty Grpd}(X, \mathbf{B}^n A)
  \,.
$$

Here on the right $Ho_{Top}$ and $Ho_{\infty Grpd}$ denotes the [[homotopy category]] of the [[(∞,1)-categories]] of [[topological spaces]] and of [[∞-groupoids]], respectively. 

Not only the set $\pi_0\mathbf{Top}(X, K(A,n))=Ho_{Top}(X, K(A,n))$ is related to the cohomology of $X$ with coefficients in $A$, but also the higher homotopy groups $\pi_i\mathbf{Top}(X, K(A,n))$ are, and in the most obvious way: if $X$ is a connected CW-complex, then
$$
H^{n-i}(X,A)=\pi_i\mathbf{Top}(X, K(A,n))=\pi_i\mathbf{\infty Grpd}(X, \mathbf{B}^n A),
$$
for any choice of base point on the right hand sides. This fact, which appears to have first been remarked by Thom and Federer, is an immediate consequence of the natural homotopy equivalences
$$
\Omega\mathbf{H}(X,Y)\simeq \mathbf{H}(X,\Omega Y)
$$
and
$$
\Omega K(A,n)\simeq K(A,n-1)
$$
one has in every $(\infty,1)$-[[(infinity,1)-topos|topos]], see [[loop space object]]. For $G$ a nonabelian group, Gottlieb proves the following nonabelian analogue of the above result: let $X$ be a finite dimensional connected CW-complex; for a fixed map $f:X\to K(G,1)$, let $C_f$ be the centralizer in $G=\pi_1 K(G,1)$ of $f_*(\pi_1(X))$. Then the connected component of $f$ in $\mathbf{Top}(X,K(G,1))$ is a $K(C_f,1)$.

Notice that for $G$ a nonabelian group, $H^1(X,G)$ is a simple (and the most familiar) example of [[nonabelian cohomology]]. Nonabelian cohomology in higher degrees is obtained by replacing here the coefficient $\infty$-groupoids of the simple form $\mathbf{B}^n A$ with more general $\infty$-groupoids.

### Of EM spaces
 {#CohomologyOfEMSpaces}

On the other hand there is the [[cohomology]] of Eilenberg-MacLane spaces itself. This is in general rich. Classical results by [[Serre]] and [[Henri Cartan]] are reviewed in ([Clement 02, section  2](#Clement02)).

+-- {: .num_prop #RationalCohomologyOfKZn}
###### Proposition

For all even $n \in \mathbb{N}$, the [[ordinary cohomology|ordinary]] [[cohomology ring]] of $K(\mathbb{Z},n)$ with [[coefficients]] in the [[rational numbers]] is the [[polynomial algebra]] on the generator $a \in H^n(K(\mathbb{Z},n),\mathbb{Q}) \simeq \mathbb{Q}$. For all odd $n$ it is the [[exterior algebra]] on this generator:

$$
  H^\bullet(K(\mathbb{Z},n),\mathbb{Q})
  \simeq
  \left\{
    \array{
      \mathbb{Q}[a] & n \; even
      \\
      \mathbb{Q}[a]/(a^2) & n \; odd
    }
  \right.
  \,.
$$

=--

This is reviewed for instance in ([Yin, section 4](#Yin)).

## Generalizations

The notion of [[Eilenberg?Mac Lane object]] makes sense in every $(\infty,1)$-[[(infinity,1)-topos|topos]], not just in $L_{whe}$[[Top]]. See at _[[Eilenberg-MacLane object]]_.

## Related concepts

* [[generalized Eilenberg-MacLane space]]

* [[Kan-Thurston theorem]]

* [[Moore space]]

* [[Peterson space]]

## References

### General

Eilenberg-MacLane spaces originate with:

* {#EilenbergMacLane53I} [[Samuel Eilenberg]], [[Saunders Mac Lane]], _On the Groups $H(\Pi,n)$, I_, Annals of Mathematics Second Series, Vol. 58, No. 1 (Jul., 1953), pp. 55-106 ([jstor:1969820](https://www.jstor.org/stable/1969820)) 

* {#EilenbergMacLane54II} [[Samuel Eilenberg]], [[Saunders Mac Lane]], _On the Groups $H(\Pi,n)$, II: Methods of Computation_, Annals of Mathematics Second Series, Vol. 60, No. 1 (Jul., 1954), pp. 49-139 ([jstor:1969702](https://www.jstor.org/stable/1969702))

* {#EilenbergMacLane54III} [[Samuel Eilenberg]], [[Saunders Mac Lane]], _On the Groups $H(\Pi,n)$, III: Operations and Obstructions_, Annals of Mathematics Second Series, Vol. 60, No. 3 (Nov., 1954), pp. 513-557 ([jstor:1969849](https://www.jstor.org/stable/1969849))

That Eilenberg-MacLane spaces represent [[ordinary cohomology]] is due to:

* [[Samuel Eilenberg]], p. 243 of: _Cohomology and Continuous Mappings_, Annals of Mathematics Second Series, Vol. 41, No. 1 (Jan., 1940), pp. 231-251  ([jstor:1968828](https://www.jstor.org/stable/1968828))

* [Eilenberg-MacLane 54 III, p. 520-521](#EilenbergMacLane54III)

Early review is in

* [[Norman Steenrod]], Section 19 of: _Cohomology operations, and obstructions to extending continuous functions_,  Advances in Math. 8, 371&#8211;416. (1972)  (<a href="https://doi.org/10.1016/0001-8708(72)90004-7">doi:10.1016/0001-8708(72)90004-7</a>, [pdf](http://www.maths.ed.ac.uk/%7Eaar/papers/steen6.pdf))


Textbook accounts:

* {#AguilarGitlerPrieto02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf), [doi:10.1007/b97586](https://link.springer.com/book/10.1007/b97586))

  > (EM-spaces are constructed in section 6, the cohomology theory they represent is discussed in section 7.1, and its equivalence to singular cohomology is Corollary 12.1.20)


* {#May} [[Peter May]], Chapter 22 of: _A concise course in algebraic topology_ ([pdf](http://www.maths.ed.ac.uk/~aar/papers/maybook.pdf))

Lecture notes:

* {#Kobin16} Andrew Kobin, Section 7.6 of: _Algebraic Topology_, 2016 ([[KobinAT2016.pdf:file]])

The construction via reduced linearization of spheres is considered in

* {#Schwede12} [[Stefan Schwede]], Example I.1.14 in _Symmetric spectra_, 2012 ([pdf](http://www.math.uni-bonn.de/~schwede/SymSpec.pdf))


Quick review includes

* {#Yin} Xi Yin, _On Eilenberg-MacLane spaces_ ([pdf](http://www.people.fas.harvard.edu/~xiyin/Site/Notes_files/AT.pdf))


Formalization of Eilenberg-MacLane spaces in [[homotopy type theory]] is discussed in

* {#LicataFinster14} [[Dan Licata]], [[Eric Finster]], _Eilenberg-MacLane spaces in homotopy type theory_, LICS 2014 ([pdf text](http://dlicata.web.wesleyan.edu/pubs/lf14em/lf14em.pdf), [Agda HoTT code](https://github.com/dlicata335/hott-agda/blob/master/homotopy/KGn.agda), [web discussion](http://homotopytypetheory.org/2014/04/15/eilenberg-maclane-spaces-in-hott/))

### Cohomology

The [[ordinary cohomology]] of Eilenberg-MacLane spaces is discussed in 

* {#Clement02} Alain Cl&#233;ment, _Integral Cohomology of Finite Postnikov Towers_, 2002 ([pdf](http://doc.rero.ch/record/482/files/Clement_these.pdf))

The [[topological K-theory]] of EM-spaces is discussed in

* {#AndersonHodgkin68} D.W. Anderson, Luke Hodgkin _The K-theory of Eilenberg-Maclane complexes_, Topology, Volume 7, Issue 3, August 1968, Pages 317-329 ([doi:10.1016/0040-9383(68)90009-8](https://doi.org/10.1016/0040-9383(68)90009-8))


[[!redirects Eilenberg-MacLane space]]
[[!redirects Eilenberg--MacLane space]]
[[!redirects Eilenberg?MacLane space]]
[[!redirects Eilenberg-Mac Lane space]]
[[!redirects Eilenberg - Mac Lane space]]
[[!redirects Eilenberg--Mac Lane space]]
[[!redirects Eilenberg?Mac Lane space]]
[[!redirects Eilenberg-MacLane spaces]]
[[!redirects Eilenberg--MacLane spaces]]
[[!redirects Eilenberg?MacLane spaces]]
[[!redirects Eilenberg-Mac Lane spaces]]
[[!redirects Eilenberg--Mac Lane spaces]]
[[!redirects Eilenberg?Mac Lane spaces]]
[[!redirects Eilenberg–MacLane space]]