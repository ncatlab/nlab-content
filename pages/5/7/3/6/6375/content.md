
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

[[Emil Artin]]'s reciprocity law is a [[reciprocity law]] in [[class field theory]] for [[global fields]]. It states, in consequence, that for each 1-dimensional [[Galois representation]] $\sigma$ there exists a [[Dirichlet character]] $\chi$ such that the [[Artin L-function]] $L_\sigma$ equals the [[Dirichlet L-function]] $L_\chi$. (The generalization of this reciprocal correspondence to higher dimensional Galois representations is the content of the conjectured _[[Langlands correspondence]]_).

For $K$ a [[global field]] there is a canonical map

$$
  \mathbb{I}_K \longrightarrow Gal(K^{ab}/K)
$$

from its [[group of ideles]] to the [[abelianization]] of its [[Galois group]], given by

$$
  (\cdots, a_v, \cdots) \mapsto \prod_v Frob_v^{ord_v(a_v)}
  \,.
$$

For $K$ a [[number field]], _Artin's reciprocity law_ says that this map is surjective, that it factors through the [[idele class group]] $K^\times \backslash \mathbb{I}_K$ and moreover that further quotienting this by the connected component $\mathcal{O}$ of 1 in the idele class group yields an [[isomorphism]]

$$
  K^\times \backslash \mathbb{I}_K / \mathcal{O}
  \stackrel{\simeq}{\longrightarrow}
  Gal(K^{ab}/K)
  \,.
$$

For $K = \mathbb{Q}$ this is also the statement of the [[Kronecker-Weber theorem]], and together this is a starting point of the [[Langlands correspondence]] [[conjecture]], see there for more.

For $K$ a [[function field]] the map is no longer surjective, and is instead a injection with dense image

$$
  K^\times \backslash \mathbb{I}_K
  \hookrightarrow
  Gal(K^{ab}/K)
  \,.
$$

moreover, the cokernel is isomorphic to $\hat{\mathbb{Z}}/\mathbb{Z}$ ([See Cohomology of Number Fields, p. 443](#NSW08))

([e.g. Toth 11, p. 3](#Toth11))

Notice that the double quotients appearing here are by the [[Weil uniformization theorem]] analogous to [[moduli stacks of bundles]] on the [[arithmetic curve]] on which $K$ is the field of [[rational functions]]. Under this [[function field analogy]] the analog of Artin's reciprocity law plays a central role in the [[geometric Langlands correspondence]].

## Properties

### Function field analogy

[[!include function field analogy -- table]]

## Related concepts

* [[Artin L-function]]

## References

* [[Serge Lang]], _Algebraic number theory_, Graduate Texts in Mathematics **110**, Springer (1970, 1986, 1994, 2000) &lbrack;[doi:10.1007/978-1-4612-0853-2](https://doi.org/10.1007/978-1-4612-0853-2)&rbrack;

* {#NSW08} Jürgen Neukirch, Alexander Schmidt, Kay Wingberg: *Cohomology of Number Fields*, 2nd edition, Springer (2008) &lbrack;[doi:10.1007/978-3-540-37889-1](https://doi.org/10.1007/978-3-540-37889-1)&rbrack;

* {#Snyder02} [[Noah Snyder]], section 2.3 of _Artin L-Functions: A Historical Approach_, 2002 ([pdf](https://web.archive.org/web/20120204005924/http://www.math.columbia.edu/~nsnyder/thesismain.pdf))

* Wikipedia: *[Artin reciprocity law](http://en.wikipedia.org/wiki/Artin_reciprocity_law)*, 

* Wikipedia, *[Artinsches_Reziprozitaetsgesetz](http://de.wikipedia.org/wiki/Artinsches_Reziprozit%C3%A4tsgesetz)*

A discussion with an eye towards [[geometric class field theory]]:

* {#Toth11} Peter Toth, _Geometric abelian class field theory_, 2011 ([web](http://dspace.library.uu.nl/handle/1874/206061))

[[!redirects Artin's reciprocity law]]

[[!redirects Artin reciprocity]]

