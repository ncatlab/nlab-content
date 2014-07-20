
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Langlands correspondence
+--{: .hide}
[[!include Langlands correspondence -- contents]]
=--
#### Duality
+-- {: .hide}
[[!include duality - contents]]
=--
=--
=--




#Contents#
* table of contents
{:toc}

## Idea

What is called the _Langlands correspondence_ in [[number theory]] ([Langlands 67](#Langlands67)) is a [[conjecture|conjectural]] correspondence (a [[bijection]] subject to various conditions) between 

1. $n$-[[dimensional]] [[representations]] of the [[Galois group]] $Gal(\bar F/F)$ of a given [[number field]] $F$, and

1. certain [[representations]] -- called _[[automorphic representations]]_ -- of the $n$-dimensional [[general linear group]] $GL_n(\mathbb{A}_F)$ with [[coefficients]] in the [[ring of adeles]] of $F$, arising within the representations given by [[functions]] on the double [[coset space]] $GL_n(F) \backslash GL_n(\mathbb{A}_F)/GL_n(\mathcal{O})$ (where $\mathcal{O} = \prod_v \mathcal{O}_p$ is the [[ring of integers]] of all [[formal completions]] of $F$).

This conjecture is motivated from the following special case, which is fully understood:

For $n = 1$ then an $n$-dimensional representation of the [[Galois group]] factors through $GL_1$ and hence through an [[abelian group]]. Therefore, by [[adjunction]], it is equivalently a representation of the [[abelianization]] of the Galois group. The [[Kronecker-Weber theorem]] says that for $F = \mathbb{Q}$, then the abelianized Galois group is $GL_1(\mathbb{Q}) \backslash GL_1(\mathbb{A})$, and hence 1-dimensional representations of the Galois group are equivalently representations of this. Moreover, one finds that for any [[prime number]] $p$, then those representations which are "unramified at $p$" are invariant under the subring of [[p-adic integers]], hence are representations of the double quotient group $GL_1(\mathbb{Q}) \backslash GL_1(\mathbb{A})/GL_1(\mathbb{Z}_p)$. 

Various versions and refinements of this conjecture have since been considered, for some perspective see ([Langlands 14](#Langlands14)).

In particular, interpretation of the above story dually in [[arithmetic geometry]] has led to some developments. Namely under the [[function field analogy]] we have that 

* the [[Galois group]] is essentially the [[fundamental group]] of an [[algebraic curve]];

* hence a [[representation]] of it is a [[principal bundle|principal]]/[[vector bundle]] with [[flat connection]] on this curves;

* while that curious double quotient $GL_n(F) \backslash GL_n(\mathbb{A}_F)/GL_n(\mathcal{O}_F)$ is just the canonical [[Cech cohomology|Cech]]-realization of the [[moduli stack of bundles]] (see there for details) on that curve.

From this [[arithmetic geometry]] point of view the Langlands conjecture seems to speak of a correspondence that sends [[Dirac distributions]] on the [[moduli space of flat connections]] over an [[algebraic curve]] to certain "automorphic" functions on the [[moduli stack of bundles]] on the same curve. This suggests that the Langlands correspondence should be understood as a nonabelian version of a [[Fourier-Mukai transform|Fourier-Mukai]]-type [[integral transform]]. This version of the conjecture is known as the _[[geometric Langlands correspondence]]_. See there for more details.


## References

The original [[conjecture]] is due to 

* {#Langlands67} [[Robert Langlands]], letter to [[Andre Weil]] 1967. [IAS page](https://publications.ias.edu/rpl/paper/43) including scan and TeXed version, see also [this UBC page](http://sunsite.ubc.ca/DigitalMathArchive/Langlands/functoriality.html#weil1967) for a little more information.

Surveys include

* {#Langlands14} [[Robert Langlands]], _[[Problems in the theory of automorphic forms -- 45 years later]]_, Oxford 2014

also

* Mark Goresky, _Langlands' conjectures for physicists_ ([pdf](http://www.math.ias.edu/~goresky/pdf/Physicists.pdf))

(which however, despite the title, has nothing in it that is particularly related to physics)

and

* {#Frenkel09} [[Edward Frenkel]], _Gauge Theory and Langlands Duality_ ([arXiv:0906.2747](http://arxiv.org/abs/0906.2747))

See also


* Stephen Gelbart, _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219; Edward Frenkel, _Commentary on "An elementary introduction to the Langlands Program" by Steven Gelbart_, Bull. Amer. Math. Soc. __48__ (2011), 513-515, [abstract](http://www.ams.org/journals/bull/2011-48-04/S0273-0979-2011-01345-3/home.html), [pdf](http://www.ams.org/journals/bull/2011-48-04/S0273-0979-2011-01347-7/S0273-0979-2011-01347-7.pdf) 
* the [digital archive](http://sunsite.ubc.ca/DigitalMathArchive/Langlands/intro.html) of [[Robert Langlands]]' articles at sunsite.ubc.ca, not currently being maintained, see:
* [The Work of Robert Langlands](https://publications.ias.edu/rpl) at the Institute of Advanced Study.
* Michael Harris, Automorphic Galois representations and Shimura varieties, to appear in Proceedings of the ICM 2014 ([pdf](https://www.imj-prg.fr/~michael.harris/2014.pdf)).
* Richard Taylor, Galois Representations, ICM 2002 ([long version](http://www.math.ias.edu/~rtaylor/longicm02.pdf)).
[[!redirects Langlands duality]]

[[!redirects Langlands correspondence]]
[[!redirects Langlands correspondences]]