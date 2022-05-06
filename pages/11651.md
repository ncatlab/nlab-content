
#Contents#
* table of contents
{:toc}

## Idea

In [[algebraic geometry]] a _divisor_ (or _[[Weil divisor]]_ for definiteness) in a given [[variety]] is a [[formal linear combination]] of sub-[[varieties]] of [[codimension]] 1. Accordingly the _divisor group_ is the [[free abelian group]] on the set of subvarieties of codimension 1.

A divisor is called _effective_ if all its [[coefficients]] are [[positive numbers]].

In [[complex analytic geometry]] any [[meromorphic function]] induces a divisor whose summands are irreducible codimension-1 subvarieties weighted by the order of the [[poles]] of the function on that subvariety. Divisors arising this way are called _principal divisors_. More generally in [[algebraic geometry]] this leads to the concept of _[[Cartier divisor]]_.

Two divisors are called _linearly equivalent_ if their difference is a principal divisor.

## Properties

### Relation to line bundles and the Picard group

Under suitable conditions the [[Poincaré duality|Poincaré dual]] of a divisor may hence define the [[first Chern class]] of an [[algebraic line bundle]] and this construction yields group homomorphism from the group of divisors to the [[Picard group]]. After quotienting out linear equivalence of divisors this yields an inclusion and in complex geometry this inclusion exhibits precisely the subgroup of the [[Picard group]] of [[holomorphic line bundle]] which admit at least one global holomorphic section ([e.g. Huybrechts 04, cor. 2.3.20](#Huybrechts04)).

More abstractly in terms of [[abelian sheaf cohomology]]:

A divisor $D = \sum_i n_i D_i$ on $X$ induces a [[short exact sequence]] of [[abelian sheaves]] on $X$ ([Brylinski 94, (1-1)](#Brylinski94)) of the form 

$$
  0
  \to
  \mathcal{O}^\times_X
  \longrightarrow
  \mathcal{O}_X(\ast Y)^\times
  \stackrel{v_Y}{\longrightarrow}
  (v_Y)_\ast \mathbb{Z}_{\tilde Y}
  \to 0
  \,,
$$

where $Y$ is the support of $D$ (i.e. $Y \coloneqq \underset{i | n_i \neq 0}{\cup} D_i$) and $\nu_Y \colon \tilde Y \to Y$ is its normalization in $Y$ (...). The induced [[long exact sequence in homology|long exact sequence]] in [[abelian sheaf cohomology]] has as first [[connecting homomorphism]] a map of the form

$$
  \delta \colon H^0(\tilde Y, \mathbb{Z}) \longrightarrow H^1(X,\mathcal{O}^\times_X)
  \,.
$$

Now the divisor $D = \sum_i n_i D_i$ is incarnated as the locally constant function $n$ on $\tilde Y$ whose value on $\tilde D_i$ is $n_i \in \mathbb{Z}$, hence the divisor is incarnated a class in $H^0(\tilde Y, \mathbb{Z})$. The class $\mathcal{O}(D)$ of the line bundle it induces as the image of this class under the above connecting homomorphims:

$$
  \mathcal{O}(D) \simeq \delta(n)
  \,.
$$

([Brylinski 94, prop. 1.1](#Brylinski94)).

A higher analog of the connecting homomorphism abive may be interpreted as being the [[Beilinson regulator]] from $K_1(X)$ to [[Deligne cohomology]] in degree 3 ([Brylinski 94, section 3](#Brylinski94)).


## Examples

* [[canonical divisor]]

* [[theta divisor]]

## Related concepts

* [[algebraic cycle]]

* [[exceptional divisor]] ([[resolution of singularities]])

## References

* Wikipedia, _[Divisor (algebraic geometry)](http://en.wikipedia.org/wiki/Divisor_(algebraic_geometry)_

* [[The Stacks Project]], _[53 Divisors on Algebraic Spaces](http://stacks.math.columbia.edu/chapter/53)_

In [[complex analytic geometry]]:

* {#Brylinski94} [[Jean-Luc Brylinski]], _Holomorphic gerbes and the Beilinson regulator_, Ast&#233;risque 226 (1994): 145-174 ([[Brylinski94.pdf:file]])

* {#Huybrechts04} [[Daniel Huybrechts]] section 2.3 of _Complex geometry - an introduction_. Springer (2004). Universitext. 309 pages. ([pdf](http://www.math.uh.edu/~shanyuji/2012/Geometry/Huybrechts.pdf))


Relation of [[divisors]] to [[complex cobordism cohomology]]:

* [[Burt Totaro]], _Torsion algebraic cycles and complex cobordism_, J. Amer. Math. Soc. 10 (1997), 467-493 ([doi:10.1090/S0894-0347-97-00232-4](https://doi.org/10.1090/S0894-0347-97-00232-4))

* [MO discussion](https://mathoverflow.net/a/272131/381)





