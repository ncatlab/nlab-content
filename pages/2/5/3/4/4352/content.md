

\tableofcontents

## Idea

A **hypergroup** is a [[algebra|algebraic]] structure similar to a [[group]], but where the composition operation does not just take two elements to a single product element in the group, but to a subset of elements of the group.

It is a [[hypermonoid]] with additional groupal [[stuff, structure, property|structure and property]].



## Definition

A **canonical hypergroup** is a [[set]], $H$, equipped with a commutative binary operation, 

$$
  + : H \times H \to \mathcal{P}(H)\backslash\{\emptyset\}
$$ 

whose value is a [[non-empty subset]] of $H$, and a zero element $0 \in H$, such that

1. $+$ is associative (extended to allow addition of subsets of $H$);
2. $0 + x = {\{x\}} = x + 0, \forall x \in H$;
3. $\forall x \in H, \exists ! y \in H$ such that $0 \in x + y$ (we denote this $y$ as $-x$);
4. $\forall x, y, z \in H, x \in y + z$ implies $z \in x - y$ (where $x - y$ means $x + (-y)$ as usual).

$\mathcal{P}(H)$ is the notation for the [[power set]] of $H$. A related variant is the notion of [[n-valued group]].


## Examples

The additive structure underlying a [[hyperring]] is a canonical hypergroup. See there for more examples.

## Related pages

* [[group]]

* [[hypermagma]]

* [[hypermonoid]]

* [[hyperring]]

* [[hypergraph]]

\begin{remark}\label{Terminology}
Beware that, while [[groups]] are [[looping and delooping|equivalently]] [[pointed object|pointed]] [[groupoids]] with a single [[object]], hypergroups are not *[[hypergroupoids]]* with a single object. For this reason some sources refer to the latter as *Duskin-Glenn hypergroupoids*.
\end{remark}


## References

See also at [[hypermagma]] and [[multivalued group]].

* J. Delsarte, _Hypergroupes et opérateurs de permutation et de transmutation_, La théorie des équations aux dérivées partielles. Nancy, 9-15 avril 1956, pp. 29--45
Colloq. Internat. CNRS, LXXI [International Colloquia of the CNRS] Centre National de la Recherche Scientifique, Paris, 1956 [MR0116151](https://mathscinet.ams.org/mathscinet/relay-station?mr=MR0116151), [Zbl 0075.27503](https://zbmath.org/0075.27503).

* J. Jantosciak, _Transposition hypergroups: Noncommutative join spaces_, J. Algebra **187** (1997) pp.97-119. doi:[10.1006/jabr.1997.6789](https://doi.org/10.1006/jabr.1997.6789)

* {#Lit11}G. L. Litvinov, _Hypergroups and hypergroup algebras_,  J. Math. Sci. **38** (1987) pp. 1734–1761, doi:[10.1007/BF01088201](https://doi.org/10.1007/BF01088201) (Translated from Itogi Nauki i Tekhniki, Sovremennye Problemy Matematiki, Noveishie Dostizheniya, Vol. 26, pp. 57–106, 1985), [arXiv:1109.6596](https://arxiv.org/abs/1109.6596).

* F. Marty,  _Sur une généralization de la notion de groupe_ , IV Congrès des Mathématiciens Scandinaves, Stockholm 1934.

* P.-H. Zieschang, _Hypergroups_, ISBN 978-3-031-39488-1, XV+391 pages, Springer, Cham, 2023. doi:[10.1007/978-3-031-39489-8](https://doi.org/10.1007/978-3-031-39489-8)

category: algebra

[[!redirects canonical hypergroup]]
[[!redirects hypergroups]]
[[!redirects canonical hypergroups]]