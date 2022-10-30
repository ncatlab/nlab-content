
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

What is called the _Langlands correspondence_ in [[number theory]] ([Langlands 67](#Langlands67)) is first of all a [[conjecture|conjectural]] correspondence (a [[bijection]] subject to various conditions) between 

1. $n$-[[dimensional]] complex [[linear representations]] of the [[Galois group]] $Gal(\bar F/F)$ of a given [[number field]] $F$, and

1. certain [[representations]] -- called _[[automorphic representations]]_ -- of the $n$-dimensional [[general linear group]] $GL_n(\mathbb{A}_F)$ with [[coefficients]] in the [[ring of adeles]] of $F$, arising within the representations given by [[functions]] on the double [[coset space]] $GL_n(F) \backslash GL_n(\mathbb{A}_F)/GL_n(\mathcal{O})$ (where $\mathcal{O} = \prod_v \mathcal{O}_p$ is the [[ring of integers]] of all [[formal completions]] of $F$).

This is motivated from the abelian case ($n=1$), which is fully understood: For $n = 1$ then an $n$-dimensional representation of the [[Galois group]] factors through $GL_1$ and hence through an [[abelian group]]. Therefore, by [[adjunction]], it is equivalently a representation of the [[abelianization]] of the Galois group. The [[Kronecker-Weber theorem]] says that for $F = \mathbb{Q}$, then the abelianized Galois group is the [[idele class group]] $GL_1(\mathbb{Q}) \backslash GL_1(\mathbb{A})$, and hence 1-dimensional representations of the Galois group are equivalently representations of this. Moreover, one finds that for any [[prime number]] $p$, then those representations which are "unramified at $p$" are invariant under the subring of [[p-adic integers]], hence are representations of the double quotient group $GL_1(\mathbb{Q}) \backslash GL_1(\mathbb{A})/GL_1(\mathbb{Z}_p)$. More generally, the [[Artin reciprocity law]] says that for [[number fields]] there is an [[isomorphism]] between $GL_1(K) \backslash GL_1(\mathbb{A}_K)/GL_1(\mathcal{O}_K)$ and the [[abelianization|abelianized]] [[Galois group]].

$\,$

Moreover:

**Conjecture 1** To each such [[automorphic representation]] $\pi$ is associated an [[L-function]] -- the _[[automorphic L-function]]_ $L_\pi$ -- and in generalization of [[Artin reciprocity]] the conjecture of Langlands is that the [[Artin L-function]] $L_\sigma$ associated with the given [[Galois representation]] $\sigma$ is equal to this: $L_\sigma = L_\pi$ ([Gelbhart 84, conjecture 1 (page 27 (204))](#Gelbhart84)).

$\,$

More generally, analogous statements are supposed to hold for general [[reductive algebraic groups]] $G$ other than $GL_n$. Here now an [[L-function]] is assigned to data which in addtion to the [[Galois representation]] consists of a [[linear representation]] ${}^L G \longrightarrow GL_n$ of the [[Langlands dual group]] of $G$. 

First of all:

**Conjecture 2** This more general L-function is conjectured to indeed behave like a decent L-function in that it has meromorphic [[analytic continuation]] to the [[complex plane]] and satisfies the "[[functional equation]]"-invariance under sending its parameter $s$ to $1-s$ ([Gelbhart 84, conjecture 2' (page 29 (205))](#Gelbhart84)).

Second:

{#Conjecture3} **Conjecture 3** This construction is supposed to behave well with respect to an analytic [[homomorphism]] ${}^L G \to {}^L G^{'}$ in that when changing the representation of ${}^L G^{'}$ by precomposition with this homomorphism one may find an accompanying change of Galois representation/automorphic representation from $G$ to $G^{'}$ such that the associated L-function remains invariant under these joint changes. This statement is what [[Robert Langlands]] calls _functoriality_ ([Gelbhart 84, conjecture 3 (page 31 (207))](#Gelbhart84))


In fact this last conjecture implies the previous two ([Gelbhart 84, (page 32 (208))](#Gelbhart84)).

$\,$

Various versions and refinements of this conjecture have since been considered, for some perspective see ([Taylor 02](#Taylor02), [Langlands 14](#Langlands14), [Harris 14](#Harris14)). On the one hand the "localization" of the program to [[local fields]] leads to the conjecture of _[[local Langlands correspondences]]_ ([Gelbhart 84, (page 34 (210))](#Gelbhart84)). On the other hand, the interpretation of the above story dually in [[arithmetic geometry]] in view of the [[function field analogy]] motivates the conjectural _[[geometric Langlands correspondence]]_, based on the following [[analogy]]:


* the [[Galois group]] is essentially the [[fundamental group]] of an [[algebraic curve]];

* hence a [[representation]] of it is a [[principal bundle|principal]]/[[vector bundle]] with [[flat connection]] on this curves;

* while that curious double quotient $GL_n(F) \backslash GL_n(\mathbb{A}_F)/GL_n(\mathcal{O}_F)$ is, in view of the [[Weil uniformization theorem]], analogous to the canonical [[Cech cohomology|Cech]]-realization of the [[moduli stack of bundles]] (see there for details) on that curve.

[[!include Langlands analogies -- table]]

From this [[arithmetic geometry]] point of view the Langlands conjecture seems to speak of a correspondence that sends [[Dirac distributions]] on the [[moduli space of flat connections]] over an [[algebraic curve]] to certain "automorphic" functions on the [[moduli stack of bundles]] on the same curve. This suggests that the Langlands correspondence should be understood as a nonabelian version of a [[Fourier-Mukai transform|Fourier-Mukai]]-type [[integral transform]]. This version of the conjecture is known as the _[[geometric Langlands correspondence]]_. See there for more details.


## References

The original [[conjecture]] is due to 

* {#Langlands67} [[Robert Langlands]], letter to [[Andre Weil]] 1967 ([IAS page](https://publications.ias.edu/rpl/paper/43) including scan and TeXed version, see also [this UBC page](http://sunsite.ubc.ca/DigitalMathArchive/Langlands/functoriality.html#weil1967) for a little more information)

Surveys of the state of the program include


* {#Taylor02} Richard Taylor, _Galois Representations_, Proceedings of the ICM 2002 ([long version pdf](http://www.math.ias.edu/~rtaylor/longicm02.pdf)).


* {#Langlands14} [[Robert Langlands]], _[[Problems in the theory of automorphic forms -- 45 years later]]_, Oxford 2014

* {#Harris14} Michael Harris, _Automorphic Galois representations and Shimura varieties_, Proceedings of the ICM 2014 ([pdf](https://www.imj-prg.fr/~michael.harris/2014.pdf)).


Introductions and expository surveys include

* {#Gelbhart84} [[Stephen Gelbart]], _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219 ([web](http://www.ams.org/journals/bull/1984-10-02/S0273-0979-1984-15237-6/))

* [[Edward Frenkel]], _Commentary on "An elementary introduction to the Langlands Program" by Steven Gelbart_, Bull. Amer. Math. Soc. __48__ (2011), 513-515, ([pdf](http://www.ams.org/journals/bull/2011-48-04/S0273-0979-2011-01347-7/S0273-0979-2011-01347-7.pdf)) 

* Mark Goresky, _Langlands' conjectures for physicists_ ([pdf](http://www.math.ias.edu/~goresky/pdf/Physicists.pdf))

* {#MK14} [[Minhyong Kim]], _A superficial introduction to Langlands functoriality_, 2014 ([pdf](http://people.maths.ox.ac.uk/vonk/automorphic/functoriality.pdf))
 
Discussion with an eye towards [[geometric class field theory]] and [[geometric Langlands duality]] and [[quantum field theory]] is in 

* {#Kapranov95} [[Mikhail Kapranov]], _Analogies between the Langlands Correspondence and Topological Quantum Field Theory_, in _Functional Analysis on the Eve of the 21st Century_ Progress in Mathematics Volume 131/132, 1995, pp 119-151
 
* {#Toth11} Peter Toth, _Geometric abelian class field theory_, 2011 ([web](http://dspace.library.uu.nl/handle/1874/206061))

* {#Frenkel09} [[Edward Frenkel]], _Gauge Theory and Langlands Duality_ ([arXiv:0906.2747](http://arxiv.org/abs/0906.2747))


More resources are at

* the [digital archive](http://sunsite.ubc.ca/DigitalMathArchive/Langlands/intro.html) of [[Robert Langlands]]' articles at sunsite.ubc.ca, not currently being maintained, see:

* [The Work of Robert Langlands](https://publications.ias.edu/rpl) at the Institute of Advanced Study.

[[!redirects Langlands duality]]

[[!redirects Langlands correspondence]]
[[!redirects Langlands correspondences]]

[[!redirects Langlands conjecture]]
[[!redirects Langlands conjectures]]