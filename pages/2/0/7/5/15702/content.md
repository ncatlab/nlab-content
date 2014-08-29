
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Arithmetic geometry
+--{: .hide}
[[!include arithmetic geometry - contents]]
=--
=--
=--
#Contents#
* table of contents
{:toc}

## Idea

An _Artin L-function_ $L_\sigma$ ([Artin 23](#Artin23)) is an [[L-function]] associated with a [[number field]] $K$ and induced from the choice of an $n$-dimensional [[Galois representation]], hence a [[linear representation]] 

$$
  \sigma\;\colon\; Gal(L/K) \longrightarrow GL_n(\mathbb{C})
$$

of the [[Galois group]] for some finite [[Galois extension]] $L$ of $K$: it is the product ("[[Euler product]]") over all [[prime ideals]] $\mathfrak{p}$ in the [[ring of integers]] of $K$, of,  essentially, the [[characteristic polynomials]] of the [[Frobenius homomorphism]] $Frob_p$ regarded (see [here](Frobenius+morphism#AsElementsOfGaloisGroup)) as elements of [[Galois group]] 

$$
  L_\sigma \colon s
  \mapsto
  \underset{\mathfrak{p}}{\prod}
  det
  \left(   
    id - N \mathfrak{p}^{-1}
    \sigma(Frob_{\mathfrak{p}})
  \right)^{-1}
  \,
$$

([e.g. Gelbhart 84, II.C.2](#Gelbhart84), [Snyder 02, def. 2.1.3](#Snyder02)).

> dicussion of ramified primes needs to be added

For $n = 1$ then for each 1-dimensional [[Galois representation]] $\sigma$ there is a _[[Dirichlet character]]_ $\chi$ such that the Artin L-function $L_\sigma$ is equal to the [[Dirichlet L-function]] $L_\chi$ -- this relation is part of _[[Artin reciprocity]]_.

More generally, for $n \geq 1$ the [[conjecture]] of _[[Langlands correspondence]]_ is that for each $n$-dimensional [[Galois representation]] $\sigma$ there is an [[automorphic representation]] $\pi$ such that the Artin L-function $L_\sigma$ equals the [[automorphic L-function]] $L_\pi$ (e.g [Gelbhart 84, pages 5-6](#Gelbhart84)).

## Properties

### For irreducible representations -- Artin's conjecture

_Artin's conjecture_ is the statement that for a nontrivial _[[irreducible representation]]_ $\sigma$ the Artin L-function $L_\sigma$ is not just a [[meromorphic function]] on the complex plane, but in fact an [[entire holomorphic function]].

e.g. ([Ram Murty 94, p. 3](#RamMurty94))

> or rather with at most a  pole at $s = 1$ [Murty-Murty 12, page 29 in chapter 2](#MurtyMurty12)


### For induced representations and  Relation to Dedekind zeta function
 {#RelationToDedekindZeta}

For $H \hookrightarrow Gal(L/K)$ a [[subgroup]] and $Ind_H^{Gal}\chi$ an [[induced representation]], then

$$
  L_{Ind_H^{Gal}\chi}(K) = L_\chi(L^H)
  \,.
$$

e.g. ([Murty-Murty 12, equation (1) in chapter 2](#MurtyMurty12))

In particular therefore the [[Dedekind zeta function]] is the Artin L-function for a representation [[induced representation|induced]] from the trivial representation (...)


(e.g. [here](http://books.google.co.uk/books?id=uxABH9YX-gsC&pg=PA44#v=onepage&q&f=false))




### Analogy with Selberg zeta-functions and zeta functions of bundle-twisted Laplace operators
 {#AnalogyWithSelbergZeta}

The [[Frobenius morphism]] $Frob_p$ giving an element in the [[Galois group]] means that one may think of it as an element of the [[fundamental group]] of the given [[arithmetic curve]] (see at _[[algebraic fundamental group]]_). In this interpretation a [[Galois connection]] corresponds to a [[flat connection]] ([[local system of coefficients]]) on the arithmetic curves.

Under this interpretation, the definition of that Artin L-function is that of a product of [[characteristic polynomials]] of the [[monodromies]]/[[holonomies]] of that flat connection.

Now given, in [[differential geometry]], a suitable [[hyperbolic manifold]] equipped with an actual [[flat bundle]] over it, then associated with it is the _[[Selberg zeta function]]_. While this was originally defined differently, it turns out that this is also an [[Euler product]] of [[characteristic polynomials]] of [[monodromies]]/[[holonomies]]. See at _[Selberg zeta function -- Analogy with Artin L-function](Selberg+zeta+function#AnalogyWithArtinLFunction)_ for more on this.

(The definition also has some similarity to that of the [[Alexander polynomial]], see at _[[arithmetic topology]]_.)


## Related concepts


[[!include zeta-functions and eta-functions and theta-functions and L-functions -- table]]

## References

The original article is

* {#Artin23} [[Emil Artin]],  _&#220;ber eine neue Art von L Reihen_. Hamb. Math. Abh. 3. (1923) Reprinted in his collected works, ISBN 0-387-90686-X. English translation in ([Snyder 02, section A](#Snyder02))

Reviews include

* Wikipedia, _[Artin L-function](http://en.wikipedia.org/wiki/Artin_L-function)_

* {#MurtyMurty12} M. Ram Murty, V. Kumar Murty, _Non-vanishing of L-functions and applications_, Modern Birkh&#228;user classics 2012 ([chapter 2 pdf](http://www.beck-shop.de/fachbuch/leseprobe/9783034802734_Excerpt_001.pdf))


* {#Snyder02} [[Noah Snyder]], _Artin L-Functions: A Historical Approach_, 2002 ([pdf](http://www.math.columbia.edu/~nsnyder/thesismain.pdf))

and in the context of the [[Langlands program]]

* {#Gelbhart84} [[Stephen Gelbart]], _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219 ([web](http://www.ams.org/journals/bull/1984-10-02/S0273-0979-1984-15237-6/))

Further development includes

* {#RamMurty94} M. Ram Murty, _Selberg's conjectures and Artin -functions_, Bull. Amer. Math. Soc. 31 (1994), 1-14 ([web](http://www.ams.org/journals/bull/1994-31-01/S0273-0979-1994-00479-3/home.html))


The analogies between Alexander polynomial and L-functions and touched upon in 

* Ken-ichi Sugiyama, _The properties of an L-function from a geometric point of view_, 2007 [pdf](http://geoquant2007.mi.ras.ru/sugiyama.pdf); _A topological $\mathrm{L}$ -function for a threefold_, 2004 [pdf](http://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/1376-12.pdf)

[[!redirects Artin L-functions]]

