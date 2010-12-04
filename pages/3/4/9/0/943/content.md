
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


# Contents
* automatic table of contents goes here
{:toc}


## Idea

The term [[convenient category of topological spaces]] is used for a category of [[topological space]]s nice enough to address many of the needs of working topologists, notably including the condition of being a [[cartesian closed category]]. As such, they are examples of [[nice category of spaces|nice categories of spaces]].

A primary example is the category of [[compactly generated space]]s.


## Definition

While the authors of this article don't know whether there exists in the literature a widely accepted definition of "convenient category of topological spaces", we propose the following definition as reasonable and convenient (see also the discussion [below](#NvC) on the distinction between "nice" and "convenient"): 

+-- {: .un_def}
######Definition
A **convenient category of topological spaces** is a [[full subcategory|full]] [[replete subcategory]] $C$ of the category of all topological spaces [[Top]] such that the following conditions 1-3 hold: 

1. Every [[CW complex]] is an object of $C$; 

1. $C$ is [[cartesian closed]]; 

1. $C$ is [[complete category|complete]] and [[cocomplete category|cocomplete]]. 

=--

Frequently it is also felt desirable to add closure under certain types of subspace inclusions. For instance, in the well-known examples one has 

* $C$ is closed under closed subspace inclusions in [[Top]], i.e., if $X$ belongs to $C$ and $A \subseteq X$ is a closed subspace (in $Top$), then $A$ also belongs to $C$. 

At times one might hope that $C$ is closed under open subspace inclusions as well, but this does not hold for all objects in some of the well-known examples of convenient categories. 

It may be well to note that colimits and limits in $C$ need not agree with the corresponding colimits and limits in $Top$, except under certain conditions.  Some convenient categories are [[reflective subcategory|reflective]] or coreflective in $Top$, in which case they are closed under limits or colimits respectively.  Moreover, because $C$ is a full subcategory of $Top$ which contains all CW complexes, the usual sorts of colimits used to present CW complexes are the same whether interpreted in $Top$ or in $C$.  Also, if $C$ is closed under closed subspaces, then an equalizer of a pair of maps between Hausdorff spaces in $C$ (being a closed subspace) is the same whether computed in $Top$ or in $C$.

On the other hand, products of $C$-objects in $Top$ need not land in $C$, so in that situation the product in $Top$ and the product in $C$ do not agree.  This is in particular the case for compactly generated spaces.  In fact, the "compactly generated product" is sometimes preferable to the $Top$-product for more explicit reasons: for instance, if $X$ and $Y$ are CW complexes, then $X\times Y$ need not be a CW complex in the usual product topology, but it is in the compactly generated topology.


## Examples

* [[compactly generated space]]

* others to be written.

## Counterexamples

A naive approach to the problem of constructing "convenient categories" usually runs into problems. For example, one could try to work with the full subcategory of $Top$ consisting of spaces which are [[exponential object|exponentiable]]; the problem is that even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ may not be: 

* The category of exponentiable spaces is not cartesian closed. (It is of course cartesian: the product of two exponentiable spaces under the usual product topology is exponentiable.) 

To see this, we recall that a [[Hausdorff space]] is exponentiable if and only if it is [[locally compact space|locally compact]], and that an exponential $Y^X$ (provided it exists) is Hausdorff if $Y$ is. Thus, it is enough to exhibit two locally compact Hausdorff spaces $X$, $Y$ whose exponential is not locally compact Hausdorff. 

Take $X = Y = \mathbb{N}$ with the [[discrete topology]]. Then the exponential $\mathbb{N}^\mathbb{N}$ is forced to have the product topology, by the following calculation: 

$$LCH(X \times \mathbb{N}, \mathbb{N}) \cong LCH(\sum_{\mathbb{N}} X, \mathbb{N}) \cong \prod_{\mathbb{N}} LCH(X, \mathbb{N})$$ 

where the last functor in $X$, in order to be representable, would have to be represented by a product $\prod_{\mathbb{N}} \mathbb{N}$. However, there is no such product in the category of locally compact Hausdorff spaces. The topological product is in fact homeomorphic to the space of irrationals between $0$ and $1$ via the regular continued fraction expansion, and this is not locally compact. 

## "Nice" versus "convenient" categories of spaces
{#NvC}

A related entry is [[nice category of spaces]]. Here we explain the difference between "convenient" and "nice" categories of spaces. 

"A convenient category of topological spaces" is the title of a well-known paper by Norman Steenrod, who emphasized particularly function space constructions (i.e., cartesian closure) as a great convenience for working algebraic topologists, on top of (generally less problematic) completeness and cocompleteness assumptions. (See also the historical remarks that follow.) 

It is well-known that $Top$ is not [[cartesian closed category|cartesian closed]].  One can characterize the [[exponential law for spaces|exponentiable spaces]], which include all [[locally compact space|locally compact]] [[Hausdorff space|Hausdorff]] spaces, but as we saw above, the naive idea of simply cutting down to some of these does not give a good cartesian closed category either, since firstly it need not be complete and cocomplete, and secondly even if $X$ and $Y$ are exponentiable, the exponential $Y^X$ need not be.

However, one can cut down to *some* full subcategory of spaces which does admit function spaces.  This typically involves the subtle and delicate interplay between compactness conditions and openness conditions.  It comes at a cost -- that limits and/or colimits in the subcategory might not be computed as they are in $Top$ -- but this is generally considered a very small price to pay in exchange for the great convenience of these assumptions. 

That a convenient category of topological spaces contains all the CW complexes was not explicitly declared by Steenrod, but we feel certain that algebraic topologists want these as part of their convenient category. In practice this is a mild assumption, because the usual examples certainly contain all finite topological products of the interval $I$, and are closed under those $Top$-colimits used to present CW complexes, as built inductively from the basic spaces $I^n \cong D^n$. 

"Nice categories of spaces" should be thought of as a wider and vaguer term; it really means the category of spaces has "nice" categorical properties for some mathematical purpose at hand. Certainly any convenient category of spaces should be considered a nice category of spaces for the general purposes of algebraic topology. On the other hand, there are categories of spaces which are not "convenient" in the technical sense described above, but which may be very nice for certain purposes. 

For example, the category of [[compact Hausdorff space]]s can be considered as being very nice for certain purposes, because it is monadic over $Set$ (!). It is, however, not "convenient", as it very far from being cartesian closed. Another example of a nice category of spaces, as explained by Johnstone (see the references below), is the category of [[sequential space]]s, but this too is not cartesian closed. In a different direction, there is the (complete, cocomplete) cartesian closed category of [[equilogical space]]s, but this is not a full subcategory of $Top$, and the core concerns of mathematicians working with equilogical spaces are somewhat different from those of algebraic topologists. 

It should also be noted that "[[space]]" itself has a wider meaning than the technical notion of "[[topological space]]", even if topological intuitions come into play. For example, in domain theory, one often considers certain types of posets (for example, [[directed-complete partial order|dcpos]]) as certain types of "spaces". In this direction, we have that the category of dcpos and _Scott-continuous_ maps between them forms a complete, cocomplete, cartesian closed category. However, these types of spaces are quite far removed from the traditional concerns of geometry, hence are not "convenient" in the sense given above (despite the manifold relations between Scott continuity and the point-set topology which underlies the classical results on compactly generated spaces). In another direction, the category of [[locales]] is in some respects "nice", but these are not topological spaces either. 

Along with the entry on [[nice category of spaces]], see also [[subsequential space]], [[Johnstone's topological topos]], and Spanier's [[quasitopological space]]s. None of these is convenient in the precise sense above. 

## Historical remarks 

The phrase "convenient category of topological spaces" predates Steenrod's paper by a number of years. Indeed, Ronnie Brown had written the following in the Introduction to his paper "Ten topologies for $X \times Y$": 

* "It may be that the category of Hausdorff k-spaces is adequate and convenient for all purposes of topology."

The requirements for convenience were spelled out in the sequel "Function spaces and product topologiea".

In point of fact, Brown (not Steenrod, as has sometimes been assumed) was the first to prove that Hausdorff k-spaces (with the "kelleyfied" weakening of the compact-open topology on function spaces) formed what is now called a cartesian closed category (see his 1961 thesis). Note that this predates the formal introduction of cartesian closed categories in Lawvere's thesis by a couple of years; in fact there is clear anticipation in Brown's thesis of the notions of monoidal closed and cartesian closed categories, which was to attract much attention throughout the sixties. 

Of course, as has often been emphasized by Lawvere, the need for and convenience of considering function spaces is a very old idea in geometry (going back to the roots of the calculus of variations for example). The constructions of exponentials of topological spaces via the compact-open topology had been known for a long time; see for example Kelley's General Topology (1955). The relevance of what are today called Kelley spaces (or k-spaces[^1]) had also been recognized; for example, Kelley's book indicates the completeness of function spaces (wrt the compact-open topology) when the base is a complete uniform space and the exponent is a k-space. However, the problem of obtaining a class of spaces _closed_ under function spaces wasn't solved prior to Brown's thesis. Brown also observed the relevance of k-spaces to studies of how products interact with quotient spaces. The general appreciation of the connection between cartesian closure and preservation of quotients under products came with the appreciation of the conceptual simplicity of categorical adjunctions, namely the point that the functor $- \times X$ preserves colimits if it has an exponential right adjoint $(-)^X$. 

Appreciation of the role of convenient categories was in full force by the early seventies (for a sample, see May's Geometry of Iterated Loop Spaces, where the category of Hausdorff k-spaces plays a foundational role). The notion of a "convenient category" is recognized elsewhere too (and not just within the categorical community); see for example the book by Kriegl and Michor. 

[^1]: The 'k' may refer to 'kompacte' rather than Kelley's initial. 

## References

* [[Ronnie Brown]], Some problems of algebraic topology: a study of function spaces, function complexes, and FD-complexes, DPhil thesis (part A), Oxford University, 1961 [(link)](http://www.bangor.ac.uk/~mas010/pdffiles/rbthesisptA.pdf)
* [[Ronnie Brown]], Ten topologies for $X\times Y$, Quart. J.Math.
(2) 14 (1963),  303-319.
* [[Ronnie Brown]],  Function spaces and product topologies,  Quart. J. Math. (2) 15  (1964), 238--250.
* [[Norman Steenrod]], A convenient category of topological spaces, Michigan Math. J. 14 (1967) 133--152, [project euclid](http://projecteuclid.org/euclid.mmj/1028999711)
* Booth, P.; Tillotson, J., Monoidal closed, Cartesian closed and convenient categories of topological spaces. Pacific J. Math. 88 (1980), no. 1, 35--53. 
* Peter T. Johnstone, On a topological topos, Proc. London Math. Soc. (3) 38 (1979) 237&#8211;271.
* Edwin Spanier, "Quasi-topologies", Duke Mathematical Journal 30 (1) (1963), 1&#8211;14.
* Kriegl, A.; Michor, P.W., The convenient setting of global analysis, Mathematical Surveys and Monographs, Volume 53.
American Mathematical Society, Providence, RI (1997). 


[[!redirects convenient category of topological spaces]]
[[!redirects convenient categories of topological spaces]]
[[!redirects convenient category of spaces]]
[[!redirects convenient categories of spaces]]
