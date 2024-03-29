[[!redirects tubular neighbourhood]]

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Manifolds and cobordisms
+--{: .hide}
[[!include manifolds and cobordisms - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition


+-- {: .num_defn}
###### Definition

For $i : X \hookrightarrow Y$ an [[embedding]] of [[manifold]]s, a **tubular neighbourhood** of $X$ in $Y$ is

* a real [[vector bundle]] $E \to X$;

* an extension of $i$ to an [[isomorphism]]

  $$
    \hat i : E \to U_{i(X)}
  $$

  with an [[open neighbourhood]] of $X$ in $Y$.

=--

+-- {: .num_remark}
###### Remark

The [[derivative]] of $\hat i$ provides an [[isomorphism]] of $E$ with the [[normal bundle]] $\nu_{X/Y}$ of $X$ in $Y$.

=--

## Properties

### General

+-- {: .num_prop}
###### Proposition
**(tubular neighbourhood theorem)**

Every [[embedding]] does admit a tubular neighbourhood.

=--

For instance ([DaSilva, theorem 3.1](#DaSilva)).

Moreover, tubular neighbourhoods are unique _up to [[homotopy]]_ in a suitable sense:

+-- {: .num_defn}
###### Definition

For an embedding $i : X \to Y$, write $Tub(i)$ for the [[topological space]] whose underlying set is the set of tubular neighbourhoods of $i$ and whose [[topology]] is the [[subspace topology]] of $Hom(N_i X, Y)$ equipped with the [[C-infinity topology]].

=--

+-- {: .num_prop}
###### Proposition

If $X$ and $Y$ are [[compact space|compact]] [[manifold]]s, then $Tub(i)$ is [[contractible]] for all [[embedding]]s $i : X \to Y$.

=--

This appears as ([Godin, prop. 31](#Godin)).

### Pullbacks of tubular neighbourhoods



(...) [[propagating flow]] (...) ([Godin](#Godin)).


## Related concepts

* [[tubular neighbourhood of a mapping space]]

* key application: [[Pontrjagin-Thom collapse map]]

## References

* {#DaSilva} [[Ana Cannas da Silva]], §3 of: _Prerequisites from differential geometry_ &lbrack;[pdf](http://www.math.princeton.edu/~acannas/appendix_dg.pdf)&rbrack;

 
* [[Ana Cannas da Silva]], §6.2 in: *Lectures on Symplectic Geometry*, Lecture Notes in Mathematics **1764**, Springer (2008) &lbrack;[doi:10.1007/978-3-540-45330-7](https://doi.org/10.1007/978-3-540-45330-7), [pdf](https://www.math.tecnico.ulisboa.pt/~acannas/Books/lsg.pdf)&rbrack;


The homotopical uniqueness of tubular neighbourhoods is discussed in

* {#Godin} [[Veronique Godin]], _Higher string topology operations_ (2007)([arXiv:0711.4859](http://arxiv.org/abs/0711.4859))
 

For an analogue in homotopical algebraic geometry see

* [[Marc Levine]], _Motivic tubular neighborhoods_, [pdf](http://www.uni-due.de/~bm0032/publ/TubNbdDocumenta.pdf)

See also

* Wikipedia, _[Tubular neighborhood](http://en.wikipedia.org/wiki/Tubular_neighborhood)_


[[!redirects tubular neighborhoods]]

[[!redirects tubular neighbourhood]]
[[!redirects tubular neighbourhoods]]

[[!redirects tubular neighbourhood theorem]]



[[!redirects tubular neighborhood theorem]]

