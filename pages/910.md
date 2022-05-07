
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Topology
+-- {: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents
* table of contents
{: toc}

## Idea 

A [[topological space]] is _compactly generated_ if (in a certain sense) the continuous images in it of all [[compact Hausdorff space]]s tell you everything about its topology.

Compactly generated spaces form a [[convenient category of topological spaces]].


## Definitions 

A [[function]] $f\colon X \to Y$ between [[topological space]]s is __$k$-continuous__
if for all [[compact Hausdorff space]]s $C$ and [[continuous functions]] $t\colon C \to X$ the composite $f \circ t\colon C \to Y$ is continuous.
 
The following conditions on a space $X$ are equivalent:

1. For all spaces $Y$ and all functions $f\colon X \to Y$, $f$ is
continuous if and only if $f$ is $k$-continuous.
2. There is a [[set]] $S$ of compact Hausdorff spaces such that the previous condition holds for all $C \in S$.
3. $X$ is an [[identification space]] of a [[disjoint union]] of compact Hausdorff spaces.
4. A [[subspace]] $U \subseteq X$ is [[open subspace|open]] if and only if the [[preimage]] $t^{-1}(U)$ is open for any compact Hausdorff space $C$ and continuous $t\colon C \to X$.

A space $X$ is a __$k$-space__ if any (hence all) of the above conditions hold.  Some authors also say that a $k$-space is __compactly generated__, while others reserve that term for a $k$-space which is also _[[weak Hausdorff space|weak Hausdorff]]_, meaning that the image of any $t\colon C\to X$ is closed (when $C$ is compact Hausdorff).  Some authors go on to require a [[Hausdorff space|Hausdorff]] space, but this seems to be unnecessary.

Sometimes $k$-spaces are called __Kelley spaces__, after [[John Kelley]], who studied them extensively; however, they predate him and the '$k$' does not stand for his name.  (Probably it has something to do with 'compact' or 'kompakt'.)


## Examples
 {#Examples}

Examples of compactly generated spaces include

+-- {: .num_example }
###### Example

Every [[compact space]] is compactly generated.

=--

+-- {: .num_example }
###### Example

Every [[locally compact space]] is compactly generated.

=--

+-- {: .num_example }
###### Example

Every [[topological manifold]] is compactly generated

=--

+-- {: .num_example #CWComplexIsCompactlyGenerated}
###### Example

Every [[CW-complex]] is a compactly generated topological space.

=--

+-- {: .proof}
###### Proof

Since a CW-complex $X$ is a [[colimit]] in [[Top]] over attachments of standard [[n-disks]] $D^{n_i}$ (its cells), by the characterization of colimits in $Top$ ([prop.](Top#DescriptionOfLimitsAndColimitsInTop)) a subset of $X$ is open or closed precisely if its restriction to each cell is open or closed, respectively. Since the $n$-disks are compact, this implies one direction: if a subset $A$ of $X$ intersected with all compact subsets is closed, then $A$ is closed. 

For the converse direction, since [[a CW-complex is a Hausdorff space]] and since [[compact subspaces of Hausdorff spaces are closed]], the intersection of a closed subset with a compact subset is closed.

=--

+-- {: .num_example }
###### Example

Every [[first countable space]] is a compactly generated space.

=--

+-- {: .proof}
###### Proof idea

Since the topology is determined by convergent sequences = maps from one-point [[compactification]] $\mathbb{N} \cup \{\infty\}$); these include all Fr&#233;chet spaces.

=-- 


## Kaonization

Let $k\Top$ denote the category of $k$-spaces and continuous maps, and $\Top_k$ denote the category of all topological spaces and $k$-continuous maps.  We have inclusions
$$ k\Top \to \Top \to \Top_k $$
of which the first is the inclusion of a [[full subcategory|full]] [[coreflective subcategory]], the second is [[bijective on objects functor|bijective on objects]], and the composite $k\Top \to Top_k$ is an [[equivalence of categories]].

The [[coreflection]] $\Top \to k\Top$ is denoted $k$, and is sometimes (e.g. by [[M M Postnikov]]) also called **kaonization** and sometimes (e.g. by [[Peter May]]) **$k$-ification**.  This functor is constructed as follows: we take $k(X)=X$ as a set, but with the topology whose closed sets are those whose intersection with compact Hausdorff subsets of (the original topology on) $X$ is closed (in the original topology on $X$). Then $k(X)$ has all the same closed sets and possibly more, hence all the same open sets and possibly more.

In particular, the identity map $id:k(X)\to X$ is continuous, and forms the counit of the coreflection.  Thus this coreflection has a counit which is both [[monic]] and [[epic]], i.e. a "[[bimorphism]]"---such a coreflection is sometimes called a "bicoreflection."

Moreover, the identity $id: X \to k(X)$ is $k$-continuous, so that the counit becomes an isomorphism in $\Top_k$.  This shows that $k\Top \to \Top_k$ is [[essentially surjective functor|essentially surjective]], and it is fully faithful since any $k$-continuous function between $k$-spaces is $k$-continuous; hence it is an equivalence.

Since $k\Top \hookrightarrow \Top$ is coreflective, it follows that $k\Top$ is [[complete category|complete]] and [[cocomplete category|cocomplete]].  Its [[colimits]] are constructed as in $Top$, but its [[limits]] are the $k$-ification of limits in $Top$.  This is nontrivial already for [[products]]: the $k$-space product $X\times Y$ is the $k$-ification of the usual [[product topology]].  The $k$-space product is better behaved in many ways; e.g. it enables [[geometric realization]] to preserve products (and all finite limits), and the product of two [[CW complexes]] to be another CW complex.

If one is interested in $k$-spaces which are also [[weakly Hausdorff space|weak Hausdorff]], then there is a further [[reflector]] which must be applied; see [[weakly Hausdorff space]].


## Properties

### Cartesian closure

The categories $k\Top\simeq \Top_k$ are [[cartesian closed category|cartesian closed]]. (While in [[Top]] only some objects are exponentiable, see [[exponential law for spaces]].)  For arbitrary spaces $X$ and $Y$, define the *test-open* or *compact-open topology* on $\Top_k(X,Y)$ to have the [[subbase]] of sets $M(t,U)$, for a given compact Hausdorff space $C$, a map $t\colon C \to X$, and an open set $U$ in $Y$, where $M(t,U)$ consists of all $k$-continuous functions $f\colon X \to Y$ such that $f(t(C))\subseteq U$.

(This is slightly different from the usual [[compact-open topology]] if $X$ happens to have non-Hausdorff compact subspaces; in that case the usual definition includes such subspaces as tests, while the above definition excludes them.  Of course, if $X$ itself is Hausdorff, then the two become identical.)

With this topology, $\Top_k(X,Y)$ becomes an [[exponential object]] in $Top_k$.  It follows, by [[Yoneda lemma]] arguments ([prop.](closed+monoidal+category#TensorHomIsoInternalizes)), that the bijection
$$k\Top(X \times Y, Z) \to kTop(X,k\Top(Y,Z))$$
is actually an isomorphism in $\Top_k$, which we may call a *$k$-homeomorphism* (e.g. [Strickland 09, prop. 2.12](#Strickland09)).  In fact, it is actually a homeomorphism, i.e. an isomorphism already in $Top$.

It follows that the category $k\Top$ of $k$-spaces and continuous maps is also cartesian closed, since it is equivalent to $\Top_k$.  Its exponential object is the $k$-ification of the one constructed above for $\Top_k$.  Since for $k$-spaces, $k$-continuous implies continuous, the underlying set of this exponential space $k\Top(X,Y)$ is the set of all continuous maps from $X$ to $Y$.  Thus, when $X$ is Hausdorff, we can identify this space with the $k$-ification of the usual [[compact-open topology]] on $Top(X,Y)$.

Finally, this all remains true if we also impose the weak Hausdorff, or Hausdorff, conditions.


### Local cartesian closure 
 {#LocalCartesianClosure}

Unfortunately neither of the above categories is [[locally
cartesian closed category|locally
cartesian closed]].

However, if $K$ is the category of not-necessarily-weak-Hausdorff k-spaces, and $A$ and $B$ are k-spaces that are weak Hausdorff, then the pullback functor $K/B\to K/A$ has a right adjoint. This is what May and Sigurdsson used in their book _Parametrized homotopy theory_.

There is still a lot of work on fibred exponential
laws and their applications. One reason for the success and
difficulties is that it is easy to give a topology on the space of
closed subsets of a space $X$ by regarding this as the space of maps
to the [[Sierpinski space]] (the set $\{0,1\}$ of [[truth value]]s in which $\{1\}$
is closed but not open). From this one can get an [[exponential law for
spaces]] over $B$ if $B$ is $T_0$, so that all fibres of spaces over
$B$ are closed in their total space.  Note that weak Hausdorff implies $T_0$.

## Related concepts

* [[Euclidean-generated topological spaces]] ([[Delta-generated topological spaces]])

## References 

The following article attributes the concept to Hurewicz:

* David Gale, 
_Compact Sets of Functions and Function Rings_ ,
Proc. AMS **1** (1950) pp.303-308. ([pdf](http://www.ams.org/journals/proc/1950-001-03/S0002-9939-1950-0036503-X/S0002-9939-1950-0036503-X.pdf))

Compactly generated spaces are discussed by J. L. Kelley in his book

* [[John Kelley]], _General topology_, D. van Nostrand, New York 1955. 

An early textbook account is in

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], sections I.1.5.3 and III.2 of _[[Calculus of fractions and homotopy theory]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 35, Springer (1967)  ([pdf](https://www.math.rochester.edu/people/faculty/doug/otherpapers/GZ.pdf))

A lectue note careful about the (weakly) Hausdorff assumptions when needed/wanted is in the lecture notes

* {#Strickland09} [[Neil Strickland]], _The category of CGWH spaces_, 2009 ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/homotopy/cgwh.pdf), [[StricklandCGHWSpaces.pdf:file]])

Many properties of compactly generated Hausdorff spaces are used to establish a variant of the theory of fibrations, cofibrations and deformation retracts in 

* {#Steenrod67} [[Norman Steenrod]], _A convenient category of topological spaces_, Michigan Math. J. 14 (1967) 133--152, [project euclid](http://projecteuclid.org/euclid.mmj/1028999711)

Gabriel and Zisman discuss the connection with the exactness of [[geometric realization]] in

* [[Peter Gabriel]], Michel Zisman, _Calculus of Fractions and Homotopy Theory_ , Springer Heidelberg 1967. (ch.III.3-4)

Other and later references include

* {#Lewis78} [[Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978

* [[George Whitehead]], _Elements of homotopy theory_

* [[Brian Day|Brian J. Day]], _Relationship of Spanier's Quasi-topological Spaces to k-Spaces_  , M. Sc. thesis University of Sydney 1968. ([pdf](http://www.math.mq.edu.au/~street/DayMasters.pdf))

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, around note 4.3.22 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* [[Ronnie Brown]], _Topology and groupoids_, Booksurge 2006, section 5.9. 

* Booth, Peter I.; Heath, Philip R.; Piccinini, Renzo A.
Fibre preserving maps and functional spaces. Algebraic topology (Proc. Conf., Univ. British Columbia, Vancouver, B.C., 1977), pp. 158--167, Lecture Notes in Math., 673, Springer, Berlin, 1978.

* [[Peter May]], _[[A concise course in algebraic topology]]_, Chapter 5

* Samuel Smith, _The homotopy theory of function spaces: a survey_ ([arXiv:1009.0804](http://arxiv.org/abs/1009.0804))

* {#Schwede12} [[Stefan Schwede]], section A.2 of _[[Symmetric spectra]]_ (2012)


[[!redirects compactly generated topological space]]
[[!redirects compactly generated topological spaces]]
[[!redirects compactly generated space]]
[[!redirects compactly generated spaces]]
[[!redirects compactly generated weakly Hausdorff topological space]]
[[!redirects compactly generated weakly Hausdorff topological spaces]]
[[!redirects compactly generated weakly Hausdorff space]]
[[!redirects compactly generated weakly Hausdorff spaces]]
[[!redirects k-space]]
[[!redirects k-spaces]]
[[!redirects kaonization]]
[[!redirects kaonizations]]
[[!redirects kaonisation]]
[[!redirects kaonisations]]
[[!redirects Kelley space]] 
[[!redirects Kelley spaces]]