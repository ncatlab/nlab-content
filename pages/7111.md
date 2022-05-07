

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Analytic geometry
+--{: .hide}
[[!include analytic geometry -- contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

__Berkovich analytic spaces__ are a version of [[analytic space]]s over [[nonarchimedean fields]]. Unlike the _rigid analytic spaces_ (see [[rigid analytic geometry]]) of Tate, which are locally defined via [[maximal spectra]] of Tate algebras glued via the [[Grothendieck topology|Grothendieck]] [[G-topology]], the Berkovich analytic spaces are actual [[topological space]] equipped with a cover by [[affinoid domains]] via the [[analytic spectrum]] construction, due to [[Vladimir Berkovich]]. This spectrum can be viewed as consisting of the data of prime ideal plus the extension of the norm to the residue field; thus the Berkovich spectrum has far more points (though fewer than, say, [[Huber's adic spaces]] which may also contain valuations of higher order). 

For more background see _[[analytic geometry]]_.

## Definition of Berkovich analytic spaces

Let $k$ be a [[non-archimedean field]].

+-- {: .num_defn}
###### Definition

Given $n \in \mathbb{N}$  and positive elements $\{r_1, \cdots, r_n \in k\}$, consider the sub-[[power series]] [[associative algebra|algebra]] over $k$ of those series which [[convergence|converge]] inside the radii $k_i$, i.e. the algebra defined by

$$
  \{\frac{1}{r_1} T_1 , \cdots, \frac{1}{r_n}T_n\}
  :=
  \left\{
    \sum_\nu a_\nu T^\nu | \lim_{{\vert \nu\vert} \to \infty} {\vert a_\nu \vert} r^\nu = 0
  \right\}
  \,.
$$

This is a commutative [[Banach algebra]] over $k$ with [[norm]] ${\Vert f \Vert} = max {\vert a_\nu\vert} r^\nu$.

A **$k$-[[affinoid algebra]]** is a commutative Banach $k$-algebra $A$ for which there exists $n$ and $\{r_i\}$ as above and an [[epimorphism]]

$$
  \{\frac{1}{r_1} T_1 , \cdots, \frac{1}{r_n}T_n\}
  \to 
  A
$$

such that the [[norm]] on $A$ is the [[quotient norm]].

If one can choose here $r_i = 1$ for all $i$ then $A$ is called **strictly $k$-affinoid**.

The [[category]] of **$k$-[[affinoid spaces]]** is the [[opposite category]] of the category of $k$-[[affinoid algebras]] and bounded [[homomorphisms]] between them.

=--

Via the [[analytic spectrum]] $Spec_{an}$ there is a [[topological space]] associated with any $k$-affinoid space. Often this underlying topological space is referred to as _the analytic space_. 

+-- {: .num_defn}
###### Definition

An **[[affinoid domain]]** in an [[affinoid space]] $X = Spec_{an} A$ is a [[closed subset]] $V \subset X$ such that there is a [[homomorphism]] of $k$-affinoid spaces 

$$
  \phi : Spec_{an} A_V \to X
$$

for some $A_V$, whose [[image]] is $V$, and such that every other morphism of $k$-affinoid spaces into $X$ whose image is contained in $V$ uniquely factors through this morphism.

=--
 
+-- {: .num_defn}
###### Definition

A **$k$-analytic space** is a [[locally Hausdorff topological space|locally Hausdorff]] [[topological space]] $X$ equipped with an [[atlas]] by $k$-[[affinoid domains]] and [[affinoid domain embeddings]], such that their underlying [[analytic spectra]] [[topological spaces]] form a [[quasinet|net]] of [[compact subsets]] on $X$. 

=--

([Berkovich 09, def. 3.1.4](#Berkovich09))

## Properties

### Cohomology 
 {#Cohomology}

Under some mild conditions, the algebraic and the analytic [[étale cohomology]] of Berkovich spaces agree. ([Berkovich 95](#Berkovich95))

The underlying [[topological space]] $X^{an}$ given by the [[Berkovich analytic spectrum]] has as [[singular cohomology]] the [[weight filtration|weight 0]]-cohomology of $X$ ([Berkovich 09](#Berkovich09)).

See also MO discussion [here](http://mathoverflow.net/a/171653/381).


### Local contractibility
 {#LocalContractibility}

A [[complex analytic manifold]] and a _smooth_ [[complex analytic space]] is locally isomorphic to a [[polydisk]] and hence is trivially a [[locally contractible space]]. But over a [[non-archimedean field]] analytic spaces no longer need to be locally isomorphic to polydisks (but $p$-adic polydisks are still contractible ([Berkovich 90](#Berkovich90))). The following result establishes, under mild conditions, that general analytic spaces are nevertheless locally contractible.



Assume that the [[valuation]] on the ground field $k$ is nontrivial.

+-- {: .num_defn #LocallyEmbeddableInASmoothSpace}
###### Definition

A $k$-analytic space $X$ is called _locally embeddable in a smooth space_ if each point of $X$ has an [[open neighbourhood]] [[isomorphism|isomorphic]] to a strictly $k$-analytic domain in smooth $k$-analytic space. 

=--

+-- {: .num_theorem}
###### Theorem

Every $k$-analytic space which is locally embeddable in a smooth space, def. \ref{LocallyEmbeddableInASmoothSpace}, is a [[locally contractible space]].

More precisely, every point of a locally smooth $k$-analytic space has an open neighbourhood $U$ which is contractible, and which is a [[union]] $U = \cup_{i = 1}^\infty U_i$ of analytic domains.

=--

The local contractibility is [Berkovich (1999), theorem 9.1](#BerkovichContractible). The refined statment in terms of inductive systems of analytic domains is in [Berkovich (2004)](#BerkovichContractibleII).

## Examples

* [[analytic affine line]]

## Applications

* The proof of the [[local Langlands conjecture]]
for $GL_n$ by Harris&#8211;Taylor uses [[étale cohomology]] on non-archimedean analytic spaces (in the sense of Berkovich) to construct the required Galois representations over local fields.

## Related concepts

* [[non-commutative analytic space]]

* [[p-adic geometry]]

* [[G-topology]]

* [[Huber space]], [[perfectoid space]]

* [[global analytic geometry]]

## References

### Introductions and reviews

A nice survey is in

* {#LeStum12} [[Bernard Le Stum]], _One century of $p$-adic geometry -- From Hensel to Berkovich and beyond_, talk notes, June 2012 ([pdf](http://www-irma.u-strasbg.fr/IMG/pdf/NotesCoursLeStum.pdf))

A good introduction to the general idea is at the beginning of

* {#Payne13} [[Sam Payne]], _Topology of nonarchimedean analytic spaces and relations to complex algebraic geometry_ ([arXiv:1309.4403](http://arxiv.org/abs/1309.4403))



Basic notions are listed in 

* M. Temkin, _Non-archimedean analytic spaces_ ([pdf slides](http://www.math.huji.ac.il/~temkin/lectures/Non-Archimedean_Analytic_Spaces.pdf))

A review of basic definitions and facts about affinoid and rigid $k$-analytic spaces can be found in 

* Ga&#235;tan Chenevier, _lecture 5_ ([pdf](http://www.math.polytechnique.fr/~chenevier/coursIHP/chenevier_lecture5.pdf))

See also the references at [[rigid analytic geometry]].

A review of definitions and results on  $k$-analytic spaces is in 

* {#Berkovich98} [[Vladimir Berkovich]], _$p$-Adic analytic spaces_, in Proceedings of the International Congress of Mathematicians, Berlin, August 1998, Doc. Math. J. DMV, Extra Volume ICM II (1998), 141-151 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/ICM98_1998.pdf)) 

A more detailed set of lecture notes along these lines is

* {#Berkovich09} [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))

Introductory exposition of the Berkovich [[analytic spectrum]] is 

* {#Poineau07} [[Jérôme Poineau]], _Global analytic geometry_, pages 20-23 in EMS newsletter September 2007 ([pdf](http://www.ems-ph.org/journals/newsletter/pdf/2007-09-65.pdf))

* [[Frédéric Paugam]], section 2.1.4 of_Global analytic geometry and the functional equation_ (2010) ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-global-analytic-geometry.pdf))

A exposition of examples of Berkovich spectra is in 

* [[Scott Carnahan]], _Berkovich spaces I_ ([web](http://sbseminar.wordpress.com/2007/09/18/berkovich-spaces-i/))

### Original articles

* [[Vladimir Berkovich]], _Spectral theory and analytic geometry over non-Archimedean fields_, Mathematical Surveys and Monographs, vol. 33, American Mathematical Society, Providence, RI, (1990) 169 pp.
  {#Berkovich90}

* [[Vladimir Berkovich]], _&#201;tale cohomology for non-Archimedean analytic spaces_, Publ. Math. IHES 78 (1993), 5-161.

Discussion of Berkovich09cohomology of Berkovich analytic spaces includes

* {#Berkovich95} [[Vladimir Berkovich]], _On the comparison theorem for &#233;tale cohomology of non-Archimedean analytic spaces._ Israel Journal of Mathematics 92.1-3 (1995): 45-59.

* {#Berkovich09} [[Vladimir Berkovich]], _A non-Archimedean interpretation of the weight zero subspaces of limit mixed Hodge structures_, Algebra, Arithmetic, and Geometry. Birkh&#228;user Boston, 2009. 49-67.


Discussion of local contractibility of smooth $k$-analytic spaces is in 

* {#BerkovichContractible} [[Vladimir Berkovich]], _Smooth $p$-adic analytic spaces are locally contractible_, Invent. Math. 137 1-84 (1999) ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Inven_1999_137_contra.pdf))
 

* {#BerkovichContractibleII} [[Vladimir Berkovich]], _Smooth p-adic analytic spaces are locally contractible. II_, in Geometric Aspects of Dwork Theory, Walter de Gruyter & Co., Berlin, (2004), 293-370. ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Dworkvol_2004_contraII.pdf))
 
and more generally in

* {#HrushovskiLoeser10} [[Ehud Hrushovski]], [[François Loeser]], _Non-archimedean tame topology and stably dominated types_ ([arXiv:1009.0252](http://arxiv.org/abs/1009.0252))

* [[Ehud Hrushovski]], [[François Loeser]], [[Bjorn Poonen]], _Berkovich spaces embed in Euclidean spaces_ ([arXiv:1210.6485](http://arxiv.org/abs/1210.6485)) 

### Relation to other topics

On the relation to [[buildings]]:

* Annette Werner, _Buildings and Berkovich Spaces_ ([pdf](http://www.uni-frankfurt.de/fb/fb12/mathematik/ag/personen/werner/talks/dmvmuench10.pdf))

Relation to [[integration]] theory

* [[Vladimir Berkovich]], _Integration of 1-forms on $p$-adic analytic spaces_, Princeton University Press, 

Aspects of the [[homotopy theory]]/[[étale homotopy]] of analytic spaces are discussed in 

* [[Aise Johan de Jong]], _&#201;tale fundamental groups of non-archimedean analytic spaces_, Mathematica, 97 no. 1-2 (1995), p. 89-118  ([numdam](http://www.numdam.org/item?id=CM_1995__97_1-2_89_0))

Relation to [[formal schemes]]: 

* J&#233;r&#244;me Poineau, [MO comment](http://mathoverflow.net/a/138577/381)


Discussion of Berkovich analytic geometry as [[algebraic geometry]] in the general sense of [[Bertrand Toën]] and [[Gabriele Vezzosi]] is in 

* [[Oren Ben-Bassat]], [[Kobi Kremnizer]], _Non-Archimedean analytic geometry as relative algebraic geometry_ ([arXiv:1312.0338](http://arxiv.org/abs/1312.0338))


[[!redirects Berkovich analytic space]]
[[!redirects Berkovich analytic spaces]]
[[!redirects Berkovich spaces]]
[[!redirects p-adic analytic space]]
[[!redirects p-adic analytic spaces]]