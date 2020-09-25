
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Rational homotopy theory
+--{: .hide}
[[!include differential graded objects - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

The _PL de Rham theorem_ is the variant of the [[de Rham theorem]] with the smooth [[de Rham complex]] replaced by the [[PL de Rham complex]].

## Statement

+-- {: .num_prop #PLdeRhamTheorem} 
###### Proposition
**([[PL de Rham theorem]])**

Let $k$ be a [[field]] of [[characteristic zero]] (such as the [[rational numbers]], [[real numbers]] or [[complex numbers]]). 

Then the evident operation of [[integration of differential forms]] over [[simplices]] induces a [[quasi-isomorphism]] between the [[PL de Rham complex]] with coefficients in $k$  and [[cochain complex]] for [[singular cohomology]] with [[coefficients]] in $k$

$$
  \Omega^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  C^\bullet(X; k)
$$

and hence an [[isomorphism]] from [[PL de Rham cohomology]] to [[ordinary cohomology]] with [[coefficients]] in $k$ (such as [[rational cohomology]], [[real cohomology]], [[complex cohomology]]):

$$
  H^\bullet_{PLdR}(X)
  \underoverset{}{\simeq}{\longrightarrow}
  H^\bullet(X; k)
$$

(for $X$ any [[topological space]]).

=--

([Bousfield-Gugenheim 76, Theorem 2.2](#BousfieldGugenheim76))


## Related statements

* [[PL de Rham complex of smooth manifold is equivalent to de Rham complex]]

* [[equivariant PL de Rham theorem]]

* [[de Rham theorem]]

## References


* {#BousfieldGugenheim76} [[Aldridge Bousfield]], [[Victor Gugenheim]], _[[On PL deRham theory and rational homotopy type]]_, Memoirs of the AMS, vol. 179 (1976) ([ams:memo-8-179](https://bookstore.ams.org/memo-8-179))


