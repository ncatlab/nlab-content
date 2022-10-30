

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

__Berkovich analytic spaces__ are a version of [[analytic space]]s over [[nonarchimedean fields]]. Unlike the _rigid analytic spaces_ (see [[rigid analytic geometry]]) of Tate, which are locally defined via [[maximal spectra]] of Tate algebras flued via rigidified Grothendieck topology, the Berkovich analytic spaces are defined with respect to the [[analytic spectrum]], due to [[Vladimir Berkovich]]; this spectrum can be viewed consisting of the data of prime ideal plus the extension of the norm to the residue field; thus the Berkovich spectrum has far more points (though less than, say, Huber's [[adic space]]s which may also contain valuations of higher order). 

For more background see _[[analytic geometry]]_.

## Definition of Berkovich analytic spaces

Let $k$ be a [[non-archimedean field]].

+-- {: .num_defn}
###### Definition

Given $n \in \mathbb{N}$  and positive elements $\{r_1, \cdots, r_n \in k\}$, consider the sub-[[power series]] [[associative algebra|algebra]] over $k$ defined by

$$
  \{\frac{1}{r_1} T_1 , \cdots, \frac{1}{r_n}T_n\}
  :=
  \left\{
    \sum_\nu a_\nu T^\nu | \lim_{{\vert \nu\vert} \to 0} {\vert a_\nu \vert} r^\nu = 0
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

such that the norm on $A$ is the quotient norm.

If one can choose here $r_i = 1$ for all $i$ then $A$ is called **strictly $k$-affinoid**.

The [[category]] of **$k$-affinoid spaces** is the [[opposite category]] of the category of $k$-affinoid algebras and bounded [[homomorphisms]] between them.

=--

Via the [[analytic spectrum]] $Spec_{an}$ there is a [[topological space]] associated with any $k$-affinoid space. Often this underlying topological space is referred to as _the analytic space_. 

+-- {: .num_defn}
###### Definition

An **affinoid domain** in an affoinoid space $X = Spec_{an} A$ is a [[closed subset]] $V \subset X$ such that there is a [[homomorphism]] of $k$-affinoid spaces 

$$
  \phi : Spec_{an} A_V \to X
$$

for some $A_V$, whose [[image]] is $V$, and such that every other morphism of $k$-affinoid spaces into $X$ whose image is contained in $V$ uniquely factors through this morphism.

=--
 
+-- {: .num_defn}
###### Definition

A **$k$-analytic space** is a [[topological space]] 
equipped with an [[atlas]] by affinoid domains.

=--

See [Berkovich 98, paragraph 2](#BerkovichReview).

## Properties

### Local contractibility
 {#LocalContractibility}

A [[complex analytic space]] is locally isomorphic to a [[polydisk]] and hence is trivially a [[locally contractible space]]. But over a [[non-archimedean field]] analytic spaces no longer need to be locally isomorphic to polydisks (but $p$-adic polydisks are still contractible ([Berkovich 90](#Berkovich90))). The following result establishes, under mild conditions, that general analytic spaces are nevertheless locally contractible.



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

## References

### Introductions and reviews

Basic notions are listed in 

* M. Temkin, _Non-archimedean analytic spaces_ ([pdf slides](http://www.math.huji.ac.il/~temkin/lectures/Non-Archimedean_Analytic_Spaces.pdf))

A review of basic definitions and facts about affinoid and rigid $k$-analytic spaces can be found in 

* Ga&#235;tan Chenevier, _lecture 5_ ([pdf](http://www.math.polytechnique.fr/~chenevier/coursIHP/chenevier_lecture5.pdf))

See also the references at [[rigid analytic geometry]].

A review of definitions and results on  $k$-analytic spaces is in 

* [[Vladimir Berkovich]], _$p$-Adic analytic spaces_, in Proceedings of the International Congress of Mathematicians, Berlin, August 1998, Doc. Math. J. DMV, Extra Volume ICM II (1998), 141-151 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/ICM98_1998.pdf)) 

A more detailed set of lecture notes along these lines is

* [[Vladimir Berkovich]], _Non-archimedean analytic spaces_, lectures at the _Advanced School on $p$-adic Analysis and Applications_, ICTP, Trieste, 31 August - 11 September 2009 ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Trieste_2009.pdf))

The Berkovich spectrum is discussed around section 2.1.4 in the course notes

* [[Frédéric Paugam]], _Global analytic geometry and the functional equation_ (2010) ([pdf](http://www.math.jussieu.fr/~fpaugam/documents/enseignement/master-global-analytic-geometry.pdf))

A exposition of examples of Berkovits spectra is in 

* [[Scott Carnahan]], _Berkovich spaces I_ ([web](http://sbseminar.wordpress.com/2007/09/18/berkovich-spaces-i/))

### Original articles

* [[Vladimir Berkovich]], _Spectral theory and analytic geometry over non-Archimedean fields_, Mathematical Surveys and Monographs, vol. 33, American Mathematical Society, Providence, RI, (1990) 169 pp.
  {#Berkovich90}

* [[Vladimir Berkovich]], _&#201;tale cohomology for non-Archimedean analytic spaces_, Publ. Math. IHES 78 (1993), 5-161.

Discussion of local contractibility of smooth $k$-analytic spaces is in 

* [[Vladimir Berkovich]], _Smooth $p$-adic analytic spaces are locally contractible_, Invent. Math. 137 1-84 (1999) ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Inven_1999_137_contra.pdf))
 {#BerkovichContractible}

* [[Vladimir Berkovich]], _Smooth p-adic analytic spaces are locally contractible. II_, in Geometric Aspects of Dwork Theory, Walter de Gruyter & Co., Berlin, (2004), 293-370. ([pdf](http://www.wisdom.weizmann.ac.il/~vova/Dworkvol_2004_contraII.pdf))
 {#BerkovichContractibleII}

### Relation to other topics

On the relation to [[buildings]]:

* Annette Werner, _Buildings and Berkovich Spaces_ ([pdf](http://www.uni-frankfurt.de/fb/fb12/mathematik/ag/personen/werner/talks/dmvmuench10.pdf))

Relation to [[integration]] theory

* [[Vladimir Berkovich]], _Integration of 1-forms on $p$-adic analytic spaces_, Princeton University Press, 

Aspects of the [[homotopy theory]]/[[étale homotopy]] of analytic spaces are discussed in 

* [[Aise Johan de Jong]], _&#201;tale fundamental groups of non-archimedean analytic spaces_, Mathematica, 97 no. 1-2 (1995), p. 89-118  ([numdam](http://www.numdam.org/item?id=CM_1995__97_1-2_89_0))
[[!redirects Berkovich analytic space]]
[[!redirects Berkovich analytic spaces]]
[[!redirects Berkovich spaces]]
[[!redirects p-adic analytic space]]
[[!redirects p-adic analytic spaces]]
