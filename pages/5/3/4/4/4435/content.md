
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

What is called _Cartan calculus_ are the structures and relations present in a [[inner derivation Lie 2-algebra]].

For $X$ a [[smooth manifold]], consider the [[de Rham complex]] $(\Omega^\bullet(X), d_{dR})$ of [[differential form]]s on $X$, a [[cochain complex]] with the structure of a [[dg-algebra]].

Every [[vector field]] $v \in \Gamma(T X)$ of $X$ induces a [[derivation]] on this [[dg-algebra]] of degree $-1$ 

$$
  \iota_v : \Omega^\bullet(X) \to \Omega^{\bullet-1}(X)
$$

given by evaluation of forms on $v$.

As every degree -1-map, this induces a [[chain homotopy]] 

$$
  0 \stackrel{\iota_v}{\to} [d_{dR},\iota_v]
  : 
  \Omega^\bullet(X) \to \Omega^\bullet(X)
  \,.
$$

One finds that

* $[d_{dR},\iota_v,] = \mathcal{L}_v$ is the [[Lie derivative]] on forms along $v$;

* $[\mathcal{L}_v, \mathcal{L}_w] = \mathcal{L}_{[v,w]}$

* $[\mathcal{L}_v, \iota_w] = \iota_{[v,w]}$

* $[\iota_v, \iota_w] = 0$.

These relations are sometimes called **Cartan calculus**. The first one is sometimes called **Cartan's magic formula**.

## In $\infty$-Lie theory

The relations of Cartan calculus are preciselyy those in an [[inner derivation Lie 2-algebra]].

This allows to generalize Cartan calculus to oo-Lie algebroids, see the section <a href="http://ncatlab.org/nlab/show/Weil+algebra#AsInnerDer">As inner derivations</a> at [[Weil algebra]].


## References

Original articles by Cartan are

* [[Henri Cartan]], _La transgression dans un groupe de Lie et dans un espace fibr&eacuteM principal_ ,  Colloque de topologie (espaces fibr&eacute;s), Bruxelles, 1950, pp. 57&#8211;71. Georges Thone, Li&egrave;ge;
Masson et Cie., Paris, (1951).


The closely related Cartan model for [[equivariant cohomology]] is discussed for instance in 

* V. Guillemin, S. Sternberg, _Supersymmetry and equivariant de Rham theory_, Springer, 1999.

The expression _Cartan calculus_ is also used for noncommutative analogues, see e.g.

* P. Schupp, _Cartan calculus: differential geometry for quantum groups_,  Quantum groups and their applications in physics (Varenna, 1994),  507--524, Proc. Internat. School Phys. Enrico Fermi, 127, IOS, Amsterdam, 1996. 

[[!redirects Cartan's magic formula]]
