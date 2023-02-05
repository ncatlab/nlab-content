
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

*Specht modules* are [[linear representations]] of the [[symmetric group]] $Sym(n)$ (for any $ \in \mathbb{N}$), hence [[modules]] over the [[group ring]] $k(Sym(n))$, which are indexed by the [[partitions]] of $n$. 

For every partition (in other words [[Young diagram]]) $\lambda \vdash n$, the Specht module associated to $\lambda$ is usually denoted $S^{\lambda}$.

In [[characteristic 0]], they are [[irreducible representations|irreducible]] and exhaust the [[isomorphism classes]] of [[irreps]] (e.g. [Sagan 01, Thm. 2.4.6](#Sagan01)). 

In this case, any finite dimensional representation $M$ of $Sym(n)$ is of the form
$$
M \cong \underset{\lambda \vdash n}{\bigoplus} M^{\lambda}
$$
where $M^{\lambda}$ is the isotypic component of $M$ associated to $\lambda$ which is of the form $M^{\lambda} \cong (S^{\lambda})^{\oplus^{m_{\lambda}}}$, with $m_{\lambda}$ called the multiplicity of $S^{\lambda}$ in $M$. 

Over a field of [[positive characteristic]] $p$, where $p \mid n!$, the Specht modules are not irreducible, but every [[irreducible module]] does appear as the [[cosocle]] of a Specht module.

## Related concepts

* [[representation theory of the symmetric group]]

## References

Textbook accounts:

* {#Sagan01} [[Bruce Sagan]], Section 2.3 in: _The symmetric group_, Springer 2001 ([doi:10.1007/978-1-4757-6804-6](https://link.springer.com/book/10.1007/978-1-4757-6804-6), [pdf](http://math.sfsu.edu/federico/Clase/RepTh/sagan.pdf))

* {#LodayVallette12} [[Jean-Louis Loday]], [[Bruno Vallette]], Annex A in: *Algebraic Operads*, Grundlehren der mathematischen Wissenschaften **346**, Springer 2012 ([ISBN 978-3-642-30362-3](https://www.springer.com/gp/book/9783642303616), [pdf](https://pure.mpg.de/rest/items/item_3121746_1/component/file_3121747/content))

See also 

* Wikipedia, *[Specht module](https://en.wikipedia.org/wiki/Specht_module)*

[[!redirects Specht modules]]