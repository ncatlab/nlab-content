
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
  \sigma\;\colon\; Gal \longrightarrow GL_n(\mathbb{C})
$$

of the [[Galois group]]: it is the product ("[[Euler product]]") over all [[prime ideals]] $\mathfrak{p}$ in the [[ring of integers]] of $K$, of,  essentially, the [[characteristic polynomials]] of the [[Frobenius homomorphism]] $Frob_p$ regarded (see [here](Frobenius+morphism#AsElementsOfGaloisGroup)) as elements of [[Galois group]] 

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

For $n = 1$ then for each 1-dimensional [[Galois representation]] $\sigma$ there is a _[[Dirichlet character]]_ $\chi$ such that the Artin L-function $L_\sigma$ is equal to the [[Dirichlet L-function]] $L_\chi$ -- this relation is part of _[[Artin reciprocity]]_.

More generally, for $n \geq 1$ the [[conjecture]] of _[[Langlands correspondence]]_ is that for each $n$-dimensional [[Galois representation]] $\sigma$ there is an [[automorphic representation]] $\pi$ such that the Artin L-function $L_\sigma$ equals the [[automorphic L-function]] $L_\pi$ (e.g [Gelbhart 84, pages 5-6](#Gelbhart84)).



## Related concepts

* The definition of the Artin L-function has some similarity to that of the [[Alexander polynomial]]...

## References

The original article is

* {#Artin23} [[Emil Artin]],  _&#220;ber eine neue Art von L Reihen_. Hamb. Math. Abh. 3. (1923) Reprinted in his collected works, ISBN 0-387-90686-X. English translation in ([Snyder 02, section A](#Snyder02))

Reviews include

* Wikipedia, _[Artin L-function](http://en.wikipedia.org/wiki/Artin_L-function)_

* {#Snyder02} [[Noah Snyder]], _Artin L-Functions: A Historical Approach_, 2002 ([pdf](http://www.math.columbia.edu/~nsnyder/thesismain.pdf))

and in the context of the [[Langlands program]]

* {#Gelbhart84} [[Stephen Gelbart]], _An elementary introduction to the Langlands program_,  Bull. Amer. Math. Soc. (N.S.) 10 (1984), no. 2, 177&#8211;219 ([web](http://www.ams.org/journals/bull/1984-10-02/S0273-0979-1984-15237-6/))

The analogies between Alexander polynomial and L-functions and touched upon in 

* Ken-ichi Sugiyama, _The properties of an L-function from a geometric point of view_, 2007 [pdf](http://geoquant2007.mi.ras.ru/sugiyama.pdf); _A topological $\mathrm{L}$ -function for a threefold_, 2004 [pdf](http://www.kurims.kyoto-u.ac.jp/~kyodo/kokyuroku/contents/pdf/1376-12.pdf)

[[!redirects Artin L-functions]]
