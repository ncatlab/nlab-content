
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
* table of contents
{:toc}

## Idea

What is called _Cartan calculus_ are the structures and relations present in an [[inner derivation Lie 2-algebra]].

The classical examples considers for $X$ a [[smooth manifold]] the [[de Rham complex]] $(\Omega^\bullet(X), d_{dR})$ of [[differential forms]] on $X$, a [[cochain complex]] with the structure of a [[dg-algebra]].

(There are of course other differential geometric structures named after Cartan, see also at [[equivariant de Rham cohomology]] the section [The Cartan model](equivariant+de+Rham+cohomology#TheCartanModel).)

Every [[vector field]] $v \in \Gamma(T X)$ of $X$ induces a [[derivation]] on this [[dg-algebra]] of degree $-1$
$$
  \iota_v 
    \,\colon\, 
  \Omega^\bullet(X) \to \Omega^{\bullet-1}(X)
$$
given by [[tensor contraction|contraction]] of forms with $v$.

As every degree -1-map, this induces a [[chain homotopy]] 
$$
  0 
    \stackrel{\iota_v}{\to} 
  [d_{dR},\iota_v]
  \,\colon\,
  \Omega^\bullet(X) \to \Omega^\bullet(X)
  \,.
$$

One finds that:

* $[d_{dR},\iota_v] = \mathcal{L}_v$ is the [[Lie derivative]] on forms along $v$;

* $[d_{dR},\mathcal{L}_v]=0$;

* $[\mathcal{L}_v, \mathcal{L}_w] = \mathcal{L}_{[v,w]}$;

* $[\mathcal{L}_v, \iota_w] = \iota_{[v,w]}$;

* $[\iota_v, \iota_w] = 0$;

* $[d_{dR},d_{dR}]=0$.

These relations are sometimes called **Cartan calculus**. The first one is sometimes called **Cartan's magic formula** or _[[Cartan's homotopy formula]]_.

## In $\infty$-Lie theory

The relations of Cartan calculus are precisely those in an [[inner derivation Lie 2-algebra]].

This allows to generalize Cartan calculus to $\infty$-Lie algebroids, see the section <a href="http://ncatlab.org/nlab/show/Weil+algebra#AsInnerDer">As inner derivations</a> at [[Weil algebra]].

There is also the full [[automorphism ∞-Lie algebra]] of any [[dg-algebra]], which subsumes the inner derivation algebras. This is the context in wich the calculus of [[derived brackets]] lives.

## Related concepts

* [[horizontal differential form]]

* [[basic differential form]]

* [[equivariant de Rham cohomology]]

* [[noncommutative differential calculus]] (in the sense of Tsygan, Tamarkin and Nest)

## References

Named after [[Élie Cartan]].

Expository account: Chapter 2.4 and Table 2.4–1 of

* [[Ralph Abraham]], [[Jerrold E. Marsden]], _Foundations of Mechanics_, Second Edition, Addison-Wesley, 1978.  ISBN: 978-0-8218-4438-0.  Reprinted: AMS Chelsea Publishing 364.  [DOI](https://doi.org/10.1090/chel/364).

Cartan calculus on [[diffeological spaces]] requires a nontrivial condition, which is explored and developed in

* [[Christian Blohmann]], _Elastic diffeological spaces_, [arXiv:2301.02583](https://arxiv.org/abs/2301.02583).

For the closely related Cartan model of [[equivariant de Rham cohomology]] see the references [there](equivariant+de+Rham+cohomology#References).

See also

* [[Planet Math]], _[Cartan calculus](https://planetmath.org/cartancalculus)_


The expression _Cartan calculus_ is also used for [[noncommutative geometry]]-analogues such as for [[quantum groups]], see

* P. Schupp, _Cartan calculus: differential geometry for quantum groups_,  Quantum groups and their applications in physics (Varenna, 1994),  507--524, Proc. Internat. School Phys. Enrico Fermi, 127, IOS, Amsterdam, 1996. 
