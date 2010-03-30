_Nonabelian algebraic topology_ is a program developed by [Ronnie Brown](http://www.bangor.ac.uk/~mas010/index.html) and his collaborators. The idea is to redo and enhance [[algebraic topology]] by making use of the tool of [[strict omega-groupoid]]s and in particular the [[crossed complex]]es equivalent to them, which generalize the complexes of _abelian_ groups traditionally used in algebraic topology.

#Contents#
* automatic table of contents goes here
{:toc}

## History

I hope it is helpful to relate my ([[Ronnie Brown]]\'s) experiences from the 1960s and later with [[nonabelian cohomology]].

In writing my book on [[topology]] in the 1960s, I got offended by having to make a detour to get the [[fundamental group]] of the circle, and then was attracted by [[Paul Olum]]'s paper referenced below. I extended Olum's work to a [[Mayer-Vietoris sequence|Mayer?Vietoris type sequence]] in the second paper below, 
and this enabled one to compute the fundamental group of, for example,  a [[wedge product|wedge]] of circles.

(I use an MV sequence in _Topology and Groupoids_ in connection with pullbacks of [[covering space]]s.)

So I decided to use this account for the book, thus giving students the advantage, it seemed,  of an introduction to [[cohomology|cohomological]] ideas.

The problem was that the account when written in detail came to 30 pages (or maybe 40) and when looked at  in the cold light of day seemed incredibly boring (a full account is different from Olum's research account).

I was at the time looking for exercises and came across [[Philip Higgins]]' paper on [[presentation]]s of groupoids, which used free products with amalgamation of groupoids. So I decided to give an exercise on the fundamental groupoid of a union. Then I felt I ought to write out a solution. When I had done this, it seemed streets ahead in exposition of all that [[nonabelian cohomology]] stuff  and moreover, when souped up to the _[[fundamental groupoid]] on a set of
base points_, gave results not reachable by the MV sequence; for example you could not with the MV sequence deduce the _precise calculation_ of the fundamental group of a union of two open sets whose intersection had say 150 path components. (This anomaly is also significant, in illustrating  the limitations of exact sequences.) 

So I decided to switch to an exposition of groupoids in
1-dimensional [[homotopy theory]]  (also spurred by a meeting with [[George Mackey]] in 1967 where he told me of his work on ergodic groupoids, which is now seen as a preliminary to [[noncommutative geometry|Noncommutative Geometry]]).

It occurred to me that if one could come to the groupoid idea from two distinct directions, then there was likely to be more in this than met the eye.

At the same time, an examination of the proof of the [[van Kampen theorem]] for groupoids, suggested that the theorem should have an extension to all dimensions, if one could define homotopy gadgets with the right properties. Another stimulus was the proof (used in the book) by [[Frank Adams]] (circulated in handwritten lecture notes) of the
[[cellular approximation theorem]], which had analogies to  parts of the van Kampen proof, but failed to get algebraic results because, apparently, of the lack of an appropriate algebraic gadget in dimension $n \gt 1$.

It took 9 years to find such a gadget  in dimension $2$, and another 3 to get them in all dimensions, in work with Philip Higgins.

It seemed to me  unfortunate that this work aroused the opposition, for reasons never explained to me, of Frank Adams,  who told people the whole programme was "ridiculous". His opinion became the opposite only when I told him (1985?) of the extension to the non simply connected case of the Blakers-Massey description of $\pi_3$ of a triad, using the nonabelian tensor product (work with [[Jean-Louis Loday]]). 

The higher order van Kampen theorems, and the often nonabelian calculations which result,  have not been obtained by cohomological methods, but only by working directly  with structures appropriate to the geometry of higher homotopies, i.e. forms of strict [[n-fold category|multiple]]
groupoids. This confirms the comment of [[Philip Hall]], Philip Higgins' supervisor, that one should not try to force the geometry into a given algebraic mode, but search for the algebra which models the geometry. So it seems to me that algebraic topology has  been mainly restricted to, or not got out of,  the single base point and "group", not "groupoid", mode, nor appreciated the possibilities of
[[colimit]] type theorems in algebraic (and geometric?) topology -- no algebraic or geometric topology text (except mine!) mentions the higher order van Kampen work with Philip Higgins.

You can also see this restriction in the contrast between the unsymmetrical, choice laden,  definition of the second relative homotopy group, with its compositions in one direction (recall the limitations of "Lineland" described in "Flatland") and the definition of the fundamental [[double groupoid]] of a pointed pair of spaces $\rho_2(X,A)$, with its compositions in $2$ directions. 
This contrast gets more significant in higher dimensions.

For all these reasons, my inclination is to look for the
applications of the "appropriate" (whatever that is!) structures rather than cohomology with coefficients in such structures, where lots of detail is likely to get lost. Also, in making calculations it is convenient to work with strict algebraic structures, where the notion of colimit is more comprehensible. Even there, it has been a problem to make say colimit calculations with [[crossed module]]s into a symbolic computer algebra format. See the work by [[Chris Wensley]] listed below. 

These results could not have been obtained without the intuitions on multiple compositions easily allowed by a cubical approach.

One of the key observations for this programme was that one could define a strict homotopy double groupoid for a _pointed pair of spaces_, and that this was closely related to the well known fundamental crossed module of a pair of spaces, first considered by J.H.C. [[Whitehead]]. His paper listed below was a key source of ideas. 

The natural extension of this observation is to construct a [[strict cubical omega-groupoid|strict cubical ∞-groupoid]] $\rho X_*$ of a _[[filtered space]]_ $X_*$, and find its relation to the quite classical homotopically defined fundamental crossed complex functor $\Pi: (filtered spaces) \to (crossed complexes)$. The proofs here are non trivial. By proving using $\rho$ a colimit theorem for $\Pi$ one can shortcut [[singular homology]], and obtain old and new results in algebraic topology, including some explicit calculations of homotopy groups, even  as modules over the fundamental group. This working with filtered space is not unreasonable since they abound. For example, classifying spaces often come with convenient filtrations, as do [[geometric realisation]]s of [[simplicial set|simplicial]] or [[cubical set|cubical]] sets. These ideas generalise of course to [[multifiltered space]]s or $n$-cubes of spaces. It is not so clear that one _must_ work with a kind of bare topological space, and so have little handle on which to construct invariants, except say by first taking a singular complex, or using multipaths. 

The main idea of the [[Higher Homotopy van Kampen Theorem]]s is to model algebraically the gluing of homotopy types, or limited models of such. 

An indication of a beginnings of a &#268;ech type approach to nonabelian cohomology using groupoids and crossed complexes is given in the new book, Chapter 12. This has not been developed in terms of [[sheaf theory]]. 

Another big gap in comparison with traditional algebraic topology is [[intersection theory]] and [[Poincare duality]], although the (quite complicated) machinery of tensor products is available in the crossed complex context. 

An obvious gap is also that of extending [[Grothendieck]]'s work on the fundamental group! 




## Remarks

* Nonabelian algebraic topology in particular provides a context for and makes some use of [[nonabelian cohomology]].

* One of the main motivations for the development of Nonabelian algebraic topology was the observation that the [Seifert-van Kampen theorem](http://en.wikipedia.org/wiki/Seifert%E2%80%93van_Kampen_theorem) is most naturally understood as being not about homotopy groups, but about the [[fundamental groupoid|fundamental ∞-groupoid]] of a space. Since the assignment of fundamental $\infty$-groupoids to spaces is an $\infty$-category-valued co-presheaf, one can understand this in the context of [[nonabelian cosheaf homotopy]]. Remarks on this are in the blog entry [Codescent and the van Kampen theorem](http://ncatlab.org/nlab/show/nonabelian+cosheaf+homotopy).

## References

Ronnie Brown has published a long series of articles over the years developing the ideas of nonabelian algebraic topology. 

* Ronnie Brown, _publication list_ ([web](http://www.bangor.ac.uk/~mas010/publicfull.htm))

Currently a comprehensive **monograph** is in preparation on the subject of the algebraic topology of filtered spaces using [[crossed complex]]es and cubical [[omega-groupoid]]s with connections.  A current  version of this monograph is available on the web at

* &lt;http://www.bangor.ac.uk/r.brown/nonab-a-t.html>

near the bottom of the page.




The use of crossed complexes allows the notion of free crossed resolution, and so clear links with standard homological algebra. The place of strict $n$-fold groupoids in nonabelian  homological algebra needs much further work. One key is that the [[higher homotopy van Kampen theorem]] allows some algebraic information on gluing homotopy types, giving _some colimit information on nonabelian structures_. The traditional invariants, e.g. homotopy groups, $k$-invariants, ..., then have to be extracted from this larger structure.  

## References ##

1. Olum, P., _Non-abelian cohomology and van Kampen's theorem_, Ann. Math. 68 (1958) 658--667.

1.  Brown, R., _On a method of P. Olum_, J. London Math. Soc. 40 (1965) 303--304.

1.  Brown, R.,  _Elements of Modern Topology_, McGraw Hill, Maidenhead, 1968.

1. Brown, R., _Topology and Groupoids_, Booksurge, 2006. 

1.  Higgins, P.J., _Presentations of groupoids, with applications to groups_, Proc. Camb. Phil. Soc., 60 (1964) 7--20.

1. Brown, R. and Higgins, P.J., _On the connection between the second relative homotopy groups of some related spaces_, Proc.   London Math.  Soc.(3) 36 (1978) 193--212.

1.Brown, R. and Higgins, P.J., _Colimit theorems for relative homotopy groups_, J. Pure Appl. Algebra 22 (1981) 11--41.

1. Whitehead, J.H.C., _Combinatorial Homotopy II_, Bull.
Amer. Math. Soc., 55 (1949), 453--496.


1. Brown, R. _Crossed complexes and homotopy groupoids as non commutative tools for higher dimensional local-to-global problems_, in Handbook of Algebra 6, Edited M. Hazewinkel, Elsevier, 2009. 

1. Wensley, C.D. and Alp, M., XMOD, a GAP share package for
computation with crossed modules, _GAP Manual_, (1997), 1355--1420. 


[[!redirects Nonabelian algebraic topology]]