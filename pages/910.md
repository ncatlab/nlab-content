
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

A space $X$ is a __$k$-space__ if any (hence all) of the above conditions hold.  Some authors also say that a $k$-space is __compactly generated__, while others reserve that term for a $k$-space which is also _[[weak Hausdorff space|weak Hausdorff]]_, meaning that the image of any $t\colon C\to X$ is closed (when $C$ is compact Hausdorff).  Some authors (especially the early authors on the subject) go on to require a [[Hausdorff space|Hausdorff]] space, but this seems to be unnecessary.

Sometimes $k$-spaces are called __Kelley spaces__, after [[John Kelley]], who studied them extensively; however, they predate him and the '$k$' does not stand for his name but probably it comes from the German word *kompakt*.


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


## k-Ification

Let $k\Top$ denote the category of $k$-spaces and continuous maps, and $\Top_k$ denote the category of all topological spaces and $k$-continuous maps.  We have inclusions
$$ k\Top \to \Top \to \Top_k $$
of which the first is the inclusion of a [[full subcategory|full]] [[coreflective subcategory]], the second is [[bijective on objects functor|bijective on objects]], and the composite $k\Top \to Top_k$ is an [[equivalence of categories]].

The [[coreflection]] $\Top \to k\Top$ is denoted $k$, and is also called **kaonization** ([Postnikov 1982, p. 34](#Postnikov82)) and sometimes  **$k$-ification** ([May 1999, p. 49](#May99)).  This functor is constructed as follows: we take $k(X)=X$ as a set, but with the topology whose closed sets are those whose intersection with compact Hausdorff subsets of (the original topology on) $X$ is closed (in the original topology on $X$). Then $k(X)$ has all the same closed sets and possibly more, hence all the same open sets and possibly more.

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
cartesian closed]] ([Cagliari-Matovani-Vitale 95](#CagliariMatovaniVitale95))

However, if $K$ is the category of not-necessarily-weak-Hausdorff k-spaces, and $A$ and $B$ are k-spaces that are weak Hausdorff, then the pullback functor $K/B\to K/A$ has a right adjoint. This is what May and Sigurdsson used in their book _Parametrized homotopy theory_.

There is still a lot of work on fibred exponential
laws and their applications. One reason for the success and
difficulties is that it is easy to give a topology on the space of
closed subsets of a space $X$ by regarding this as the space of maps
to the [[Sierpinski space]] (the set $\{0,1\}$ of [[truth value]]s in which $\{1\}$
is closed but not open). From this one can get an [[exponential law for
spaces]] over $B$ if $B$ is $T_0$, so that all fibres of spaces over
$B$ are closed in their total space.  Note that weak Hausdorff implies $T_0$.

### Regularity
 {#Regularity}

The category of compactly generated [[Hausdorff spaces]] is a [[regular category]] ([Cagliari-Matovani-Vitale 95](#CagliariMatovaniVitale95)).

## Related concepts

* [[Euclidean-generated topological spaces]] ([[Delta-generated topological spaces]])

## References 

The idea of compactly generated spaces appears first, assuming the Hausdorff condition, in:

* David Gale, Section 1 of: _Compact Sets of Functions and Function Rings_,
Proc. AMS **1** (1950) pp.303-308. ([pdf](http://www.ams.org/journals/proc/1950-001-03/S0002-9939-1950-0036503-X/S0002-9939-1950-0036503-X.pdf), [doi:10.2307/2032373](https://doi.org/10.2307/2032373), [jstor:2032373](https://www.jstor.org/stable/2032373))

where it is attributed to [[Witold Hurewicz]].

Early textbook accounts assuming the Hausdorff condition:

* {#Kelley55} [[John Kelley]], p. 230 in: _General topology_, D. van Nostrand, New York 1955, reprinted as: Graduate Texts in Mathematics, Springer 1955 ([ISBN:978-0-387-90125-1](https://www.springer.com/gp/book/9780387901251))

* [[James Dugundji]], Section XI.9 of: *Topology*, Allyn and Bacon 1966 ([pdf](https://www.southalabama.edu/mathstat/personal_pages/carter/Dugundji.pdf))

* {#GabrielZisman67} [[Pierre Gabriel]], [[Michel Zisman]], sections I.1.5.3 and III.2 of _[[Calculus of fractions and homotopy theory]]_, Ergebnisse der Mathematik und ihrer Grenzgebiete, Band 35, Springer (1967)  ([pdf](https://people.math.rochester.edu/faculty/doug/otherpapers/GZ.pdf))

Influential emphasis of the usefulness of the notion as providing a [[convenient category of topological spaces]]:

* {#Steenrod} [[Norman Steenrod]], _A convenient category of topological spaces_, Michigan Math. J. 14 (1967) 133--152 ([euclid:mmj/1028999711](http://projecteuclid.org/euclid.mmj/1028999711))

Early discussion in the context of [[geometric realization of simplicial topological spaces]]:

* {#MacLane70} [[Saunders MacLane]], Section 4 of: _The Milgram bar construction as a tensor product of functors_,  In: F.P. Peterson  (eds.) *The Steenrod Algebra and Its Applications: A Conference to Celebrate N.E. Steenrod's Sixtieth Birthday*, Lecture Notes in Mathematics *168*,  Springer 1970 ([doi:10.1007/BFb0058523](https://doi.org/10.1007/BFb0058523), [pdf](https://link.springer.com/content/pdf/10.1007/BFb0058523.pdf))

and briefly in 

* {#May72} [[Peter May]], Section 1 of: *The geometry of iterated loop spaces*, Springer 1972 ([pdf](https://www.math.uchicago.edu/~may/BOOKS/geom_iter.pdf), [doi:10.1007/BFb0067491](https://link.springer.com/book/10.1007/BFb0067491))

More history and early references, with emphasis on [[category theory|category-theoretic]] aspects:

* [[Horst Herrlich]], [[George Strecker]], Section 3.4 of: *Categorical topology -- Its origins as exemplified by the unfolding of the theory of topological reflections and coreflections before 1971* ([pdf](https://link.springer.com/content/pdf/10.1007%2F978-94-017-0468-7_15.pdf)), pages 255-341 in: C. E. Aull, R Lowen (eds.), *Handbook of the History  of General Topology. Vol. 1* , Kluwer 1997 ([doi:10.1007/978-94-017-0468-7](https://link.springer.com/book/10.1007/978-94-017-0468-7))


The idea of generalizing compact generation to weakly Hausdorff spaces appears in:

* [[Michael C. McCord]], Section 2 of: *Classifying Spaces and Infinite Symmetric Products*, Transactions of the American Mathematical Society, Vol. 146 (Dec., 1969), pp. 273-298  ([jstor:1995173](https://www.jstor.org/stable/1995173), [pdf](https://www.ams.org/journals/tran/1969-146-00/S0002-9947-1969-0251719-4/S0002-9947-1969-0251719-4.pdf))

where it is attributed to [[John C. Moore]].

Review in this generality of CG weakly Hausdorff spaces:

* {#Lewis78} [[Gaunce Lewis]], _Compactly generated spaces_ ([pdf](http://www.math.uchicago.edu/~may/MISC/GaunceApp.pdf)), appendix A of _The Stable Category and Generalized Thom Spectra_ PhD thesis Chicago, 1978

* {#May99} [[Peter May]], Chapter 5 of: _[[A concise course in algebraic topology]]_, University of Chicago Press 1999 ([ISBN: 9780226511832](https://www.press.uchicago.edu/ucp/books/book/chicago/C/bo3777031.html), [pdf](http://www.math.uchicago.edu/~may/CONCISE/ConciseRevised.pdf))

* {#Strickland09} [[Neil Strickland]], _The category of CGWH spaces_, 2009 ([pdf](http://neil-strickland.staff.shef.ac.uk/courses/homotopy/cgwh.pdf), [[StricklandCGHWSpaces.pdf:file]])

* [[Charles Rezk]], *Compactly Generated Spaces*, 2018 ([pdf](https://faculty.math.illinois.edu/~rezk/cg-spaces-better.pdf), [[Rezk_CompactlyGeneratedSpaces.pdf:file]])


The terminology "kaonic spaces", or rather the Russian version "каонные пространства" is used in 

* {#Postnikov71} [[M M Postnikov]], *Введение в теорию Морса*, Наука 1971 ([web](http://libgen.is/book/index.php?md5=4BF450585846A0531FF485E34D062C0A))

* {#Postnikov82} [[M M Postnikov]], p. 34 of: *Лекции по алгебраической топологии. Основы теории гомотопий*, Наука 1982 ([web](http://libgen.is/book/index.php?md5=34A8C3C956EB80877F4E3CF5A297F514))

Proof that k-spaces form a [[regular category]]:

* {#CagliariMatovaniVitale95} F. Cagliari, S. Mantovani, [[Enrico Vitale]], *Regularity of the category of Kelley spaces*, Applied Categorical Structures volume 3, pages 357–361 (1995) ([doi:10.1007/BF00872904](https://link.springer.com/article/10.1007/BF00872904), [pdf](http://www.dm.unibo.it/~cagliari/articoli/Regularkelley.pdf))

Review  with focus on compactly generated [[topological G-spaces]] in [[equivariant homotopy theory]] and specifically [[equivariant bundle]]-theory:

* [[Bernardo Uribe]], [[Wolfgang Lück]], Section 16 of: _Equivariant principal bundles and their classifying spaces_, Algebr. Geom. Topol. 14 (2014) 1925-1995 ([arXiv:1304.4862](https://arxiv.org/abs/1304.4862), [doi:10.2140/agt.2014.14.1925](http://dx.doi.org/10.2140/agt.2014.14.1925))



See also:

* [[George W. Whitehead]], Section I.4 of: *Elements of Homotopy Theory*, Springer 1978 ([doi:10.1007/978-1-4612-6318-0](https://link.springer.com/book/10.1007/978-1-4612-6318-0))

* [[Brian Day|Brian J. Day]], _Relationship of Spanier's Quasi-topological Spaces to k-Spaces_  , M. Sc. thesis University of Sydney 1968. ([pdf](http://www.math.mq.edu.au/~street/DayMasters.pdf))

* Peter Booth, Philip R. Heath, Renzo A. Piccinini, *Fibre preserving maps and functional spaces*, Algebraic topology (Proc. Conf., Univ. British Columbia, Vancouver, B.C., 1977), pp. 158--167, Lecture Notes in Math., 673, Springer, Berlin, 1978.

* {#FelixHalperinThomas00} [[Yves Félix]], [[Stephen Halperin]], [[Jean-Claude Thomas]], Section 0 of: _Rational Homotopy Theory_, Graduate Texts in Mathematics, 205, Springer-Verlag, 2000 ([doi:10.1007/978-1-4613-0105-9](https://link.springer.com/book/10.1007/978-1-4613-0105-9))

  > (in a context of [[rational homotopy theory]])

* {#AGP02} Marcelo Aguilar, [[Samuel Gitler]], Carlos Prieto, around note 4.3.22 of _Algebraic topology from a homotopical viewpoint_, Springer (2002) ([toc pdf](http://tocs.ulb.tu-darmstadt.de/106999419.pdf))

* [[Ronnie Brown]], _Topology and groupoids_, Booksurge 2006, section 5.9. 

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

[[!redirects weakly Hausdorff compactly generated topological space]]
[[!redirects weakly Hausdorff compactly generated topological spaces]]


[[!redirects k-space]]
[[!redirects k-spaces]]
[[!redirects kaonization]]
[[!redirects kaonizations]]
[[!redirects kaonisation]]
[[!redirects kaonisations]]
[[!redirects Kelley space]] 
[[!redirects Kelley spaces]]

