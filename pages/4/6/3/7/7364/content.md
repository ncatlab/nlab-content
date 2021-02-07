
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Elliptic cohomology
+-- {: .hide}
[[!include elliptic cohomology -- contents]]
=--
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

An _elliptic fibration_ is a [[bundle]] of [[elliptic curves]], possibly including some [[singularity|singular]] [[fibers]].

An _elliptic surface_ is an elliptic fibration over an [[algebraic curve]].


## Properties

### Classification by local systems with modular group coefficients

Write $SL_2(\mathbb{Z})$ for the [[special linear group]] in dimension 2 with [[integer]] [[coefficients]] and write $SL_2(\mathbb{Z}) \to PSL_2(\mathbb{Z})$ for the [[projection]] to the corresponding [[projective linear group]]. Regarding this as the [[Möbius group]] it comes with its natural [[action]] on the [[upper half plane]] $\mathfrak{h}$. The [[homotopy quotient]]  $\mathcal{M}_{ell}(\mathbb{C}) = \mathfrak{h}//SL_2(\mathbb{Z})$ is the [[moduli stack of elliptic curves]] over the complex numbers.

Accordingly, to any $SL_2(\mathbb{Z})$-[[principal bundle]] $P \to B$  (necessarily [[flat connection|flat]] since $SL_2(\mathbb{Z})$ is a [[discrete group]], hence a "[[local system]]") is [[associated bundle|associated]] a $\mathfrak{h}$-[[fiber bundle]] such that a [[section]] of it defines a non-[[singularity|singular]] elliptic fibration. 

One may turn this around: Given an elliptic fibration $E \to B$, then away from the points $S\subset B$ over which the fiber is singular, it is given by an $SL_2(\mathbb{Z})$-local system together with a section of the associated upper-half plane bundle on $B-S$. 

With due technical care, this data uniquely characterizes the elliptic fibration (e.g. [Miranda 88, prop. VI.3.3](#Miranda88)).

### Classification of the singular fibers
 {#ClassificationOfSingularFibers}

The remaining [[singularity|singular]] fibers follow an [[ADE classification]] ([Kodaira 64](#Kodaira64), [N&#233;ron 64](#Neron64), [Kodaira 66](#Kodaira66))

## Examples

### Elliptic fibration of K3-surfaces

See at _[[elliptic fibration of a K3-surface]]_.


## Related entries

* [[F-theory]]

  * [[F/M-theory on elliptically fibered Calabi-Yau 4-folds]]

* [[K3]]

## References

Specifically for [[complex surfaces]]:



* {#Miranda88} [[Rick Miranda]], _The basic theory of elliptic surfaces_, lecture notes 1988 ([pdf](http://www.math.colostate.edu/~miranda/BTES-Miranda.pdf))


* {#FriedmanMorgan94} [[Robert Friedman]], [[John Morgan]], _Smooth Four-Manifolds and Complex Surfaces_, Ergebnisse der Mathematik und ihrer Grenzgebiete. 3. Folge / A Series of Modern Surveys in Mathematics (1994) ([doi:10.1007/978-3-662-03028-8](https://www.springer.com/gp/book/9783540570585))


* Fedor Bogomolov, Yuri Tschinkel, _Monodromy of elliptic surfaces_ ([[MonodromyOfEllipticSurfaces.pdf:file]])

* Takahiko Yoshida, _Locally standard torus fibrations_ [pdf](http://www.isc.meiji.ac.jp/~takahiko/papers/sympo.pdf)

See also:

* Wikipedia, _[Elliptic surface](http://en.wikipedia.org/wiki/Elliptic_surface)_


Specifically for [[elliptically fibered K3-surfaces]]:

* Viacheslav Nikulin, _Elliptic fibrations on K3 surfaces_ ([arXiv:1010.3904](http://arxiv.org/abs/1010.3904))


The [[ADE classification]] of the possible singular fibers is due to 

* {#Kodaira64} [[Kunihiko Kodaira]],  (1964). "On the structure of compact complex analytic surfaces. I". Am. J. Math. 86: 751&#8211;798. doi:10.2307/2373157. Zbl 0137.17501.

* {#Kodaira66} [[Kunihiko Kodaira]],  (1966). "On the structure of compact complex analytic surfaces. II". Am. J. Math. 88: 682&#8211;721. doi:10.2307/2373150. Zbl 0193.37701.

and 

* {#Neron64} [[André Néron]],  (1964). "Modeles minimaux des vari&#233;t&#233;s abeliennes sur les corps locaux et globaux". Publications Math&#233;matiques de l'IH&#201;S (in French) 21: 5&#8211;128.

[[!redirects elliptic fibrations]]

[[!redirects elliptic surface]]
[[!redirects elliptic surfaces]]

[[!redirects Kodeira classification]]
[[!redirects Kodeira classifications]]

[[!redirects Kodeira's classification]]
[[!redirects Kodeira's classifications]]


