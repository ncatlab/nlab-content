
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Theta functions
+--{: .hide}
[[!include theta functions - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

_$L$-functions_ are certain [[meromorphic functions]] generalizing the 
[[Riemann zeta function]]. They are typically defined on parts of the [[complex plane]] by a [[power series]] expressions -- called the _$L$-series_ --  which [[convergence|converges]] in that region,  and then meromorphically extended to all of the [[complex plane]] by [[analytic continuation]]. 

The most canonically defined class of examples of L-functions are the _[[Artin L-functions]]_ defined for any [[Galois representation]] $\sigma \colon Gal \longrightarrow GL_n(\mathbb{C})$ as the [[Euler products]] of, essentially, the [[characteristic polynomials]] of all the [[Frobenius homomorphisms]] acting via $\sigma$.

Most other kinds of L-functions are such as to reproduces these [[Artin L-functions]] from more "arithmetic" data: 

1. for 1-dimensional [[Galois representations]] $\sigma$ (hence for $n = 1$) [[Artin reciprocity]] produces for each $\sigma$ a [[Dirichlet character]], or more generally a [[Hecke character]] $\chi$, and therefrom is built a _[[Dirichlet L-function]]_ or _[[Hecke L-function]]_ $L_\chi$, respectively, which equals the corresponding [[Artin L-function]] $L_\sigma$;

1. for general $n$-dimensional [[Galois representations]] $\sigma$ the [[conjecture]] of [[Langlands correspondence]] states that there is an [[automorphic representation]] $\pi$ corresponding to $\sigma$ and an _[[automorphic L-function]]_ $L_\pi$ built from that, which equalso the [[Artin L-function]] $L_\sigma$.

L-functions typically satisfy [[analogy|analogs]] of all the special properties enjoyed by the [[Riemann zeta function]], such as satisfying a 
"[[functional equation]]" which asserts invariance under modular transformations of the parameter.

The generalized [[Riemann conjecture]] is concerned with zeros of the _[[Dedekind zeta function]]_ for which the L-series (the [[Dirichlet L-function]]) is complicated from the classical Riemann case by the presence of the additional parameter, the Dirichlet character. 

[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## Examples

* [[Dirichlet L-function]]

* [[Artin L-function]]

* [[Hecke L-function]]

* [[Hasse-Weil L-function]]

## Related entries

* [[special values of L-functions]]

* [[S-duality]], [[automorphic form]], [[Langlands program]], 

* [[automorphic L-function]]

* [[Beilinson conjecture]]

* [[motivic L-function]]

* [[explicit formulae (L-function)]]

## References

* {#Gelbhart84} [[Stephen Gelbart]], section C starting on p. 14 (190) of _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219 ([web](http://www.ams.org/journals/bull/1984-10-02/S0273-0979-1984-15237-6/))


* E. Kowalski, first part of _Automorphic forms, L-functions and number theory (March 12&#8211;16) Three Introductory lectures_ ([pdf](http://www.math.ethz.ch/~kowalski/lectures.pdf))


* {#GoldfeldHundley11} [[Dorian Goldfeld]], [[Joseph Hundley]], chapter 2 of _Automorphic representations and L-functions for the general linear group_, Cambridge Studies in Advanced Mathematics 129, 2011 ([pdf](https://www.maths.nottingham.ac.uk/personal/ibf/text/gl2.pdf))


* wikipedia [L-function](http://en.wikipedia.org/wiki/L-function), [Dirichlet L-function](http://en.wikipedia.org/wiki/Dirichlet_L-function), [special values of L-function](http://en.wikipedia.org/wiki/Special_values_of_L-functions), [generalized Riemann hypothesis](http://en.wikipedia.org/wiki/Generalized_Riemann_hypothesis), [Artin L-function](http://en.wikipedia.org/wiki/Artin_L-function), [equivariant L-function](http://en.wikipedia.org/wiki/Equivariant_L-function), [functional equation](en.wikipedia.org/wiki/Functional_equation_(L-function)), [modularity theorem](http://en.wikipedia.org/wiki/Modularity_theorem)

* [[Terrence Tao]]'s blog: [Distinguished Lecture Series III: Shou-wu Zhang, "Triple L-series and effective Mordell conjecture"](http://terrytao.wordpress.com/2007/05/04/distinguished-lecture-series-iii-shou-wu-zhang-%E2%80%9Ctriple-l-series-and-effective-mordell-conjecture%E2%80%9D/)

Some history is in 

* {#Cogdell12} James W. Cogdell, _L-functions and non-abelian class eld theory, from
Artin to Langlands_, 2012 ([pdf](https://people.math.osu.edu/cogdell.1/Artin-www.pdf))


[[!redirects L-functions]]