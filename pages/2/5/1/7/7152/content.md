
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### &#201;tale morphisms
+--{: .hide}
[[!include etale morphisms - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
#### $(\infty,1)$-Topos Theory
+-- {: .hide}
[[!include (infinity,1)-topos - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The notion of _&#233;tale homotopy_ can be understood as a vast generalization of the following classical fact.

The [[nerve theorem]] says that for $X$ a [[paracompact topological space]] and $\{U_i \to X\}$ a [[good cover]] of $X$ by open subsets, then the [[simplicial set]] obtained from the [[Cech nerve]] of the covering by degreewise contracting all connected components to a point, presents the [[homotopy type]] of $X$.

If $X$ here is more generally a [[locally contractible space]] there is in general no notion of "good" enough open cover anymore. Instead, one can consider the above kind of construction for _all_ [[hypercovers]] and take the [[limit]] over the resulting simplicial sets. The classical theorem by [Artin-Mazur](#ArtinMazur) states that this still gives the [[homotopy type]] of $X$.

The construction itself, however, makes sense for arbitrary topological spaces and in fact for arbitrary [[sites]]. 

In the literature, particularly the _[[étale site]]_ is often considered and "&#233;tale homotopy" is often implicitly understood to take place over this site. 

But the concept is much more general. In particular, one can understand the construction of the limit over contractions of [[hypercovers]] as a presentation of naturally defined [[(∞,1)-functors]] in [[(∞,1)-topos theory]]. 

Notably, if the given site is a a [[locally ∞-connected site]], then the &#233;tale homotopy construction computes precisely the [[derived functor]] that presents the [[fundamental ∞-groupoid in a locally ∞-connected (∞,1)-topos]]. Many constructions in the literature can be understood as being explicit realizations of this simple general concept. Detailed discussion of this is at _[[geometric homotopy groups in an (∞,1)-topos]]_.

Even more generally, &#233;tale homotopy give the notion of [[shape of an (∞,1)-topos]]. (...)

## Examples
 {#Examples}

### Chevalley groups and Galois groups

For the special case of [[fundamental groups]], the concept of &#233;tale homotopy groups also goes by the name of _[[Chevalley fundamental groups]]_.

The &#233;tale fundamental group of a [[scheme]] is its [[absolute Galois group]]. See at _[Galois theory -- Statement of the main result](Galois+theory#StatementOfMainTheorem)_.


### &#201;tale contractibility

+-- {: .num_example}
###### Example

For $k$ a [[field]] of [[characteristic]] 0, then the [[affine line]] $\mathbb{A}^1_k$ is &#233;tale [[contractible homotopy type|contractible]]. This is no longer the case in [[positive number|positive]] [[characteristic]].

=--

([HSS 13, section 1](#HSS13))

+-- {: .num_prop}
###### Proposition


Let $k$ be an [[algebraically closed field]] of [[positive number|positive]] [[characteristic]]. Then the only [[smooth variety]] over $k$ which is &#233;tale [[contractible homotopy type|contractible]] is the point $Spec(k)$. In fact this is the only smooth variety which is [[n-connected object of an (infinity,1)-topos|2-connected]].

=--

([HSS 13, theorem 1](#HSS13))


## Related concepts

* [[Čech homology]]

* [[algebraic fundamental group]]

* [[anabelian geometry]]

* [[étale topos]], [[pro-étale topos]]

* [[étale cohomology]]


## References

### General

Original articles include

* [[Michael Artin]], [[Barry Mazur]], _Homotopy of varieties in the etale topology_, Proceedings of a Conference on Local Fields, Driebergen 1966, Springer.

* [[Michael Artin]], [[Barry Mazur]], _&#201;tale Homotopy_, Springer Lecture Notes in Mathematics 100, Berlin (1969)  
  {#ArtinMazur}

* [[Eric Friedlander]], _Fibrations in &#233;tale homotopy theory [(numdam)](http://archive.numdam.org/ARCHIVE/PMIHES/PMIHES_1973__42_/PMIHES_1973__42__5_0/PMIHES_1973__42__5_0.pdf)_, Publ. Math. 
Inst. des Haut. &#201;tudes Scient., 42, (1973), 5 &#8211; 46.

The modern perspective from the point of view of [[model structure on simplicial presheaves|model structures on simplicial presheaves]] is in 

* {#Isaksen01} [[Daniel Isaksen]], _&#201;tale realization of the $\mathbb{A}^1$-homotopy theory of schemes_, 2001 ([K-theory archive](http://www.math.uiuc.edu/K-theory/0495/))

* [[G. Quick]], _Stable &#233;tale realization and &#233;tale cobordism_, Adv. in Math.,
214 (2007), 730&#8211;760.

and fully abstractly from the point of view of  [[(∞,1)-topos]]-theory ([[shape of an (∞,1)-topos]]) in

* {#Hoyois13a} [[Marc Hoyois]], _Higher Galois theory_, ([pdf](http://math.mit.edu/~hoyois/papers/highergalois.pdf))

and ([Hoyois 13b, section 1](#Hoyois13b)).

and in, where a comparison theorem over the complex numbers is also proven:

* {#Carchedi15} [[Dave Carchedi]], _On the &#233;tale homotopy type of higher stacks_ ([arXiv:1511.07830](http://arxiv.org/abs/1511.07830))

An introduction is in

* Tomer Schlank, Alexei Skorobogatov, _A very brief introduction to &#233;tale homotopy_. In: "Torsors, &#233;tale homotopy and applications to rational points". LMS Lecture Note Series 405, Cambridge University Press, 2013. ([pdf](https://www.ma.imperial.ac.uk/~anskor/SCHLANK-SKOROBOGATOV.pdf))

Lecture notes on the &#233;tale fundamental group are in

* [[James Milne]], section 4 of _[[Lectures on Étale Cohomology]]
Generalization to [[simplicial schemes]] is discussed in

* [[Eric Friedlander]], 1982, _&#201;tale homotopy of simplicial schemes_ , volume 104 of Annals of Mathematics Studies , Princeton University Press, Princeton, N.J. 

More on this is in 

* Michael Misamore, _&#201;tale homotopy types and bisimplicial hypercovers_, Homology, Homotopy and Applications, Vol. 15 (2013), No. 1, pp.27-49. ([web](http://www.intlpress.com/HHA/v15/n1/a2/))




### Examples and applications


* {#Hoyois13b} [[Marc Hoyois]], _The &#233;tale-symmetric K&#252;nneth theorem_, 2013 ([pdf](http://math.mit.edu/~hoyois/papers/etalekunneth.pdf))


Discussion in [[positive characteristic]] is in 

* {#HSS13} Armin Holschbach, Johannes Schmidt, [[Jakob Stix]], _&#201;tale contractible varieties in positive characteristic_ ([arXiv:1310.2784](http://arxiv.org/abs/1310.2784))

&#201;tale homotopy type of [[moduli stacks of curves]] is discussed in

* Paola Frediani, Frank Neumann, _&#201;tale homotopy types of moduli stacks of algebraic curves with symmetries_, K-Theory 30: 315-340, 2003 ([arXiv:math/0404387](http://arxiv.org/abs/math/0404387))


[[!redirects étale homotopy theory]]

[[!redirects etale homotopy]]
[[!redirects etale homotopy theory]]


[[!redirects etale homotopy group]]
[[!redirects étale homotopy group]]
[[!redirects etale homotopy groups]]
[[!redirects étale homotopy groups]]

[[!redirects étale fundamental group]]
[[!redirects étale fundamental groups]]
[[!redirects etale fundamental group]]
[[!redirects etale fundamental groups]]



[[!redirects étale homotopy type]]
[[!redirects étale homotopy types]]

[[!redirects etale homotopy type]]
[[!redirects etale homotopy types]]