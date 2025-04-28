
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher category theory
+--{: .hide}
[[!include higher category theory - contents]]
=--
#### Internal $(\infty,1)$-Categories
+--{: .hide}
[[!include internal infinity-categories contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Warning
There are several unrelated generalizations of the concept of a [[Segal space]] which might be thought of as "higher Segal spaces". For example, one might discuss

 - [[n-fold Segal space|$n$-fold Segal spaces]], a model for $(\infty,n)$-categories.

 - [[$n$-uple Segal spaces]], a model for cubical $(\infty,n)$-categories.

 - [[$d$-Segal spaces]] in the sense of Dyckerhoff and Kapranov, a model for something like an $(\infty,1)$-category, but without uniqueness of composites (for $d \geq 2$) and with higher associativity only in dimension $d$ and above.

This article discusses $d$-Segal spaces in the sense of Dyckerhoff and Kapranov.

## Idea

There are several ways to think about $d$-Segal spaces:

### Higher associativity parameterized by polyhedra

A $1$-Segal space $C$ is a [[Segal space]], i.e. a simplicial space satisfying the [[Segal condition]]. We think of the Segal condition in the following way. For every subdivision of an interval $I$ into subintervals $I_1,\dots,I_n$, and for any choice of labelings of the endpoints of these intervals by objects $c_0,\dots,c_n$, and any choice of labelings $\gamma_1 \in C(c_0,c_1),\dots,\gamma_n \in C(c_{n-1},c_n)$ of the intervals $I_1, \dots, I_n$, the Segal condition provides us with a "composite" labeling $\gamma_n \circ \dots \circ \gamma_1$ of the whole interval $I$, in a coherent way. "Coherence" here means that the composition is continuous in the $\gamma_i$'s, but moreover that it is associative: if we compose our labelings in two steps, for example, we get the same result as if we compose our labelings in one step: $\gamma_3 \circ (\gamma_2 \circ \gamma_1) = \gamma_3 \circ \gamma_2 \circ \gamma_1$.

A $2$-Segal space is, like a $1$-Segal space, a simplicial space, but it satisfies only a weakened version of the Segal condition. Instead of stipulating that labelings of triangualtions of 1-dimensional intervals may be coherently composed, we stipulate that labelings of triangulations of 2-dimensional polygons may be coherently composed.

Similarly $d$-Segal spaces are simplicial spaces with higher associativity data parameterized by triangulations of $d$-dimensional polyhedra.

### Categories with multivalued composition

A 2-Segal space is a "category with multivalued composition", or a category enriched in [[Span]]. A composite of two morphisms $a \to b \to c$ need not exist, and if it does it may not be unique. But whatever composites there are satisfy all "higher associativity conditions" one could want.


## Definition

### Dyckerhoff-Kapranov
 {#DyckerhoffKapranov}

In ([DyckerhoffKapranov 12](#DyckerhoffKapranov12)) a 2-Segal space is defined to be a simplicial space with a higher analog of the weak composition operation known from [[Segal spaces]].

Let $X$ be a [[simplicial topological space]] or [[bisimplicial set]] or generally a [[simplicial object]] in a suitable [[simplicial model category]].


For $n \in \mathbb{N}$ let $P_n$ be the $n$-[[polygon]]. For any [[triangulation]] $T$ of $P_n$ let $\Delta^T$ be the corresponding [[simplicial set]]. Regarding $\Delta^n$ as the cellular [[boundary]] of that polygon provides a morphism of simplicial sets $\Delta^T \to \Delta^n$.

Say that $X$ is a **2-Segal object** if for all $n$ and all $T$ as above, the induced [[morphisms]]

$$
  X_n := [\Delta^n, X]
  \to 
  X_T := [\Delta^T,X]
$$

are [[weak equivalences]].

**Warning.** A Dyckerhoff-Kapranov "2-Segal spaces" is not itself a model for an [[(∞,2)-category]]. Instead, it is a model for an [[(∞,1)-operad]] ([Dyckerhoff-Kapranov 12, section 3.6](#DyckerhoffKapranov12)).

Under some conditions DW 2-Segal spaces $X_\bullet$ induce [[Hall algebra]] structures on $X_1$ ([Dyckerhoff-Kapranov 12, section 8](#DyckerhoffKapranov12)).

## Examples

A central motivating example comes from $K$-theory. If $C$ is a [[Quillen-exact category]], then $S_\bullet C$ is a 2-Segal space. Here $S_\bullet$ is the [[Waldhausen S-construction]]. There is one object of $S_\bullet C$, denoted $0$. There is a morphism $0 \to 0$ for each object of $C$. A composite of in $S_\bullet C$ of two objects $c,c' \in C$ is an object $c'' \in C$ equipped with a short exact sequence $0 \to c \to c'' \to c' \to 0$. Thus the composite is generally not unique, but it does satisfy all the higher associativity conditions required of a 2-Segal space.

## References

For more references along these lines do *not* see at _[[n-fold complete Segal space]]_ -- that is a different concept.

The Dyckerhoff-Kapranov "higher Segal spaces" [above](#DyckerhoffKapranov) are discussed in

* [[Tobias Dyckerhoff]], [[Mikhail Kapranov]], _Higher Segal spaces I_, [arxiv:1212.3563](https://arxiv.org/abs/1212.3563); now part of the book T. Dyckerhoff, M. Kapranov, _Higher Segal spaces_, Springer LNM 2244 (2019) [doi](https://doi.org/10.1007/978-3-030-27124-4)
 {#DyckerhoffKapranov12}

* [[Tobias Dyckerhoff]], _Higher Segal spaces_, talk at Steklov Mathematical Institute (2011) ([video](http://www.mathnet.ru/php/presentation.phtml?presentid=3718&option_lang=eng))
 {#Dyckerhoff}

* [[Mikhail Kapranov]], _Higher Segal spaces _, talk at IHES (2012) ([video](http://www.dailymotion.com/video/xpm3at_mikhail-kapranov-a-meeting-on-the-occasion-of-the-75th-birthday-of-yuri-ivanovich-manin_tech))
 {#Kapranov}

* Tashi Walde, _On the theory of higher Segal spaces_, thesis, Brexen 2020 [pdf](https://bonndoc.ulb.uni-bonn.de/xmlui/bitstream/handle/20.500.11811/8705/5938.pdf?sequence=1)

* [[Matthew B. Young]], *Relative 2-Segal spaces*, Algebraic & Geometric Topology **18** (2018) 975-1039 &lbrack;[doi:10.2140/agt.2018.18.975](https://doi.org/10.2140/agt.2018.18.975)&rbrack;

  > We introduce a relative version of the 2–Segal simplicial spaces defined by Dyckerhoff and Kapranov, and Gálvez-Carrillo, Kock and Tonks. Examples of relative 2–Segal spaces include the categorified unoriented cyclic nerve, real pseudoholomorphic polygons in almost complex manifolds and the $\mathcal{R}_\bullet$-construction from Grothendieck–Witt theory. We show that a relative 2–Segal space defines a categorical representation of the Hall algebra associated to the base 2–Segal space. In this way, after decategorification we recover a number of known constructions of Hall algebra representations. We also describe some higher categorical interpretations of relative 2–Segal spaces. 

The notion of unital 2-Segal space is also discovered independently under the name of a __decomposition space__ in

* [[Imma Gálvez-Carrillo]], [[Joachim Kock]], [[Andrew Tonks]], _Decomposition spaces, incidence algebras and Möbius inversion_, [arXiv:1404.3202](https://arxiv.org/abs/1404.3202)

There are many sequels including

* Joachim Kock, David I. Spivak, _Decomposition-space slices are toposes_, [arXiv:1807.06000](https://arxiv.org/abs/1807.06000)
* Louis Carlier, [[Joachim Kock]], _Antipodes of monoidal decomposition spaces_, [arXiv:1807.11858](https://arxiv.org/abs/1807.11858)
* Matthew Feller, [[Richard Garner]], [[Joachim Kock]], May U. Proulx, [[Mark Weber]], _Every 2-Segal space is unital_, [arXiv:1905.09580](https://arxiv.org/abs/1905.09580)
* Nicolas Behr, [[Joachim Kock]], _Tracelet Hopf algebras and decomposition spaces_, [arXiv:2105.06186](https://arxiv.org/abs/2105.06186)
* Philip Hackney, [[Joachim Kock]], _Culf maps and edgewise subdivision_, [arXiv:2210.11191](https://arxiv.org/abs/2210.11191); _Free decomposition spaces_, [arXiv:2210.11192](https://arxiv.org/abs/2210.11192)

See also

* Jonte Gödicke. *An $\infty$-Category of 2-Segal Spaces* (2024). ([arXiv:2407.13357](https://arxiv.org/abs/2407.13357)).

* Walker H. Stern, _Perspectives on the 2-Segal Conditons_, [PDF](https://www.walkerstern.com/assets/pdf/Survey_draft3.pdf).


[[!redirects higher Segal space]]
[[!redirects higher Segal spaces]]

[[!redirects 2-Segal space]]
[[!redirects 2-Segal spaces]]

[[!redirects higher complete Segal space]]

[[!redirects decomposition space]]
[[!redirects decomposition spaces]]
[[!redirects $d$-Segal spaces]]
