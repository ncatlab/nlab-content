

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

An __antilinear map__ is like a [[linear map]], but instead of commuting with scalar multiplication it "anti-commutes" with scalar multiplication: multiplication by a scalar $c$ is mapped to multiplication by the scalar's conjugate $\overline{c}$, for some appropriate notion of "conjugate".

An alternate term is __conjugate linear__.


## Definition

Begin with a [[commutative ring]] (often a [[field]], or possibly just a [[rig]]) $K$, equipped with an [[involution]] $x \mapsto \overline{x}$, meaning an [[endomorphism]] with $\overline{\overline{x}} = x$ for all $x \in K$.

Then for $K$-[[modules]] (or $K$-[[linear spaces]]) $V, W$, a __$K$-antilinear map__ is a function $T : V \to W$ such that for all $x, y \in V$ and $r \in K$,

$$ T(r x + y) = \overline{r} T(x) + T(y) \quad . $$

This differs from a [[linear map]] in the appearance of $\overline{r}$ on the right-hand side, rather than $r$.


## Examples

### Simple general examples

Every $K$-linear map is also a $K$-antilinear map, with the identity involution on $K$.

Any involution $\overline{(-)} : K \to K$ is itself an antilinear map.


### Complex vector spaces

A motivating class of examples is when $K = \mathbb{C}$ is the [[complex numbers]], and $\overline{(-)}$ is [[complex conjugation]].

In particular, the [[Hermitian adjoint]] is an antilinear map from a space of $\mathbb{C}$-linear operators to itself.


### Further examples

A $*$-[[star-algebra|algebra]] requires by definition its [[anti-involution]] to be antilinear.



## Related concepts

* [[real structure]]

* [[antiunitary operator]]

* [[star-algebra]]


## References

See also

* Wikipedia, *[Antilinear map](https://en.wikipedia.org/wiki/Antilinear_map)*

and see also the references at *[[Wigner's theorem]]*.

[[!redirects antilinear maps]]

[[!redirects anti-linear map]]
[[!redirects anti-linear maps]]

[[!redirects antilinear function]]
[[!redirects antilinear functions]]

[[!redirects conjugate linear map]]
[[!redirects conjugate linear maps]]

[[!redirects conjugate linear function]]
[[!redirects conjugate linear function]]


