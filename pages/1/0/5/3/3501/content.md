
#Contents#
* table of contents
{:toc}

## Idea

To a space (typically with singularities) of a certain kind (there are variants) one associates a category whose objects are called **perverse sheaves**. They are neither perverse nor [[sheaves]]. 

They are related to some sheaf categories and notably generalize [[intersection cohomology]]. Perversity there is a parameter involved in the grading of intersection cohomology groups. Another feature similar to sheaves is that they are somehow determined by the local data; there is a famous gluing due to [[Sasha Beilinson]]. In one of the approaches (see [MacPherson's notes](#MacPherson)) there are even modified [[generalized (Eilenberg-Steenrod) cohomology|Steenrod-Eilenberg axioms]] stated for intersection cohomology. 

##Definitions

In this set of examples, $X$ is a complex [[stratified space]] (i.e. a stratification $S$ of $X$ is a collection of locally complex submanifolds which satisfy some conditions). 

We can alternatively define $X$ as an [[algebraic variety]] (where a stratification $S$ of $X$ is a collection of subvarieties which satisfy some conditions).

1. $Shv(X)$ := sheaves of complex vector spaces on X (assigns to every connected open set a vector space)

1. Look at (bounded) chain complexes in $Shv(X)$ (up to homotopy) =: $K^b(X)$

1. formally invert quasi-isomorphisms in $K^b(X)$, making this a [[derived category]] =: $D^b(X)$

1. $D_s^b(X)$ :=  subcategory of $D^b(X)$, all sheaves are constructible; 

* where $F \in D_s^b(X)$ if for all strata $S$, $i: \hookrightarrow X$; 
* $H^k(i^*F)$ is a finite rank local system on $S$ for all $k$, where $k = \text{dim}_{\mathbb{C}}(S)$.

1. $P_S(X)$ := the category of perverse sheaves, an abelian subcategory of the (non-abelian) derived category of sheaves on $X$, $D_s^b(X)$.

In other words, a [[perverse sheaf]] is an object $C$ of the bounded derived category of sheaves with constructible cohomology on a space (X), satisfying some conditions.

(...)

## Terminology
 {#Terminology}

The terminology "perverse sheaf" has an unfortunate connotation to it, at least in some languages (such as German, where it sounds no better than "idiotic sheaf" or the like). 

Accordingly, for instance [[Grothendieck]] wrote in _[[Récoltes et semailles]]_:

> What an idea to give such a name to a mathematical thing! Or to any other thing or living being, except in sternness towards a person&#8212;for it is evident that of all the 'things' in the universe, we humans are the only ones to whom this term could ever apply.

The origin of the terminology is recalled by one of its inventors on [MO here](http://mathoverflow.net/a/44149/381):

> When MacPherson and I first started thinking about intersection homology, we realized that there was a number that measured the "badness" of a cycle with respect to a stratum. This number had the property that when you (transversally) intersected two cycles, their "badness" would add. The best situation occurs for cocycles, in which case that number was zero, and the intersection of two cocycles was again a cocycle. The worst situation was for ordinary homology, in which case that number could be as large as the codimension of the stratum. In that case, the intersection of two cycles could even fail to be a cycle. After a while it became clear that we needed a name for this number and we tried "degeneracy", "gap", etc., but nothing seemed to fit. It seemed that the bad cycles were being "obstinate", but "obstinateness" did not sound reasonable. Finally we said, "let's just call it the perversity, and we'll find a better word later". We tried again later, with no success. (We did not realize that in some languages the word is obscene.) When we first went to talk with Dennis Sullivan and John Morgan about these ideas, we were calling the resulting groups "perverse homology", but Sullivan suggested the alternative, "intersection homology", which seemed fine with us. This was 1974-75. Later, when it was discovered that, for any perversity, there is an abelian category of sheaves, whose simple objects are the intersection cohomology sheaves (with that perversity) of closures of strata, Deligne coined the term "faisceaux pervers".

## References

* [[Alexander Beilinson]], [[Joseph Bernstein]], [[Pierre Deligne]], *Faisceaux pervers*, Astérisque **100** (1982) &lbrack;[ISBN:978-2-85629-878-7](https://smf.emath.fr/publications/faisceaux-pervers), [pdf](https://publications.ias.edu/sites/default/files/Faisceaux%20pervers.pdf), [MR86g:32015](http://www.ams.org/mathscinet-getitem?mr=751966)&rbrack;

* {#MacPherson} [[Robert MacPherson]], _Intersection Homology and Perverse Sheaves_, [pdf](http://faculty.tcu.edu/gfriedman/notes/ih.pdf)

* Reinhardt Kiehl, Rainer Weissauer, _Weil conjectures, perverse sheaves and l'adic Fourier transform_, Ergebnisse Der Mathematik Und Ihrer Grenzgebiete __42__, Springer 2001. 

* Mark Andrea de Cataldo, Luca Migliorini, _What is a perverse sheaf ?_, [arxiv/1004.2983](http://arxiv.org/abs/1004.2983), Notices of Amer. Math. Soc. May 2010, [pdf](http://www.ams.org/notices/201005/rtx100500632p.pdf)

* Ryan Reich, _Notes on Beilinson's "How to glue perverse sheaves"_, [arxiv/1002.1686](http://arxiv.org/abs/1002.1686)

* Geordie Williamson, _An illustrated guide to perverse sheaves_, ([pdf](http://people.mpim-bonn.mpg.de/geordie/perverse_course/lectures.pdf))

An article aiming at the categorification of perverse sheaves is 

* [[Mikhail Kapranov]], Vadim Schechtman, _Perverse Schobers_, [arxiv/1411.2772](http://arxiv.org/abs/1411.2772)

with a proposed application to physics

* [[Mikhail Kapranov]], [[Yan Soibelman]], Lev Soukhanov. *Perverse schobers and the Algebra of the Infrared* (2020). ([arXiv:2011.00845](https://arxiv.org/abs/2011.00845)).

category: sheaf theory, algebraic geometry
[[!redirects perverse sheaves]]