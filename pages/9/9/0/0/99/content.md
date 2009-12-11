#Contents#
* automatic table of contents goes here
{:toc}

## Idea

In as far as a [[Chevalley-Eilenberg algebra]] of an $L_\infty$-[[Lie infinity-algebroid|algebroid]] is the algebra of functions on an [[NQ-supermanifold]] $\mathbf{X}$, the **Weil algebra** is the algebra of functions on the [[shifted tangent bundle]] $T[1] \mathbf{X}$.

Over a contractible base space the Weil algebra may also be understood as the [[mapping cone]] of the identity on the [[Chevalley-Eilenberg algebra]].

One can also understand this as generalizing the notion of [[superdifferential form]] from ordinary [[supermanifold]]s to [[NQ-supermanifolds]].


## Definition

For $CE(\mathfrak{g}) = \wedge^\bullet_{C^\infty(X_0)} \mathfrak{g}^*$ the Chevalley-Eilenberg algebra of a $L_\infty$-[[Lie infinity-algebroid|algebroid]] $g$ over a [[manifold]] $X_0$, the corresponding **Weil algebra** is

$$
  \mathrm{W}(\mathfrak{g})
  :=
  \left(
    \wedge^\bullet_{C^\infty(X_0)}
    (
      \mathfrak{g}^* \oplus \Gamma(T^* X_0) 
      \otimes \mathfrak{g}^*[1]
    )
    , d_{\mathrm{W}(\mathfrak{g})}
  \right)
$$

where the differential acts as the deRham differential on $\wedge^\bullet \Gamma(T^* X)$ and is defined on generators in $\mathfrak{g}^* \oplus \mathfrak{g}^*[1]$ by 
$$
  d_{\mathrm{W}(\mathfrak{g})}
  =
  \left(
    \array{
       d_{\mathrm{CE}(\mathfrak{g})}
       &
       0
       \\
       \sigma
       &
       - \sigma \circ d_{\mathrm{CE}(\mathfrak{g})}
       \circ \sigma^{-1}
    }
    \,,
  \right)
$$
where $\sigma|_{\mathfrak{g}^*} : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ is the canonical degree-shifting isomorphism.

## Examples

### Weil algebra of a Lie algebra {#WeilofLieAlg}

Let $\mathfrak{g}$ be a finite dimensional [[Lie algebra]]. This Lie algebra regarded as a [[Lie algebroid]] has as base manifold the point, $X_0 = pt$. Its algebra of functions is accordingly the ground field, and the algebra $\wedge^\bullet_{C^\infty(X_0)} \mathfrak{g}^*$ is just a [[Grassmann algebra]].

The [[Chevalley-Eilenberg algebra]] is

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{g}^*, d_{\mathfrak{g}})
  \,,
$$

where the differential acts on the elements of $\mathfrak{g}^*$ in degree 1 by the linear dual of the Lie bracket.

$$
  d \mathfrak{g}|_{\mathfrak{g}^*} = [-,-]^* : \mathfrak{g}^* \to \mathfrak{g}^* \wedge \mathfrak{g}^*
  \,.
$$

The corresponding Weil algebra is obtained by adding another copy of $\mathfrak{g}^*$ in degree 2

$$
  W(\mathfrak{g}) = (\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1]), d_{W(\mathfrak{g})})
$$

where with $\sigma : \mathfrak{g}^* \to \mathfrak{g}^*[1]$ the degree shift isomorphism, the differential acts as

$$
  d_{W(\mathfrak{g})}|_{\mathfrak{g}^*}
  : 
  [-,-]^* + \sigma
$$

$$
  d_{W(\mathfrak{g})}|_{\mathfrak{g}^*[1]}
  : 
  \sigma \circ d_{CE(\mathfrak{g})} \circ \sigma^{-1}
  \,.
$$

For illustration, we spell this out in a basis.

Let $\{t_a\}_a$ be a basis for the underlying vector space of $\mathfrak{g}$ and let $\{C^a{}_{b c}\}$ be the corresponding structure constants of the Lie bracket

$$
  [t_b, t_c] = C^a{}_{b c} t_a 
  \,.
$$

Then the Chevalley-Eilenberg algebra is generated on generators $\{t^a\}$ of degree 1, on which the differential acts as

$$
  d_{CE(\mathfrak{g})} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c
  \,.
$$

The Weil algebra in turn is generated from these generators $\{t^a\}$ in degree 1 and generators $\{r^a\}$ in degree 2, with differential given by

$$
  d_{W(\mathfrak{g})} : t^a \mapsto - \frac{1}{2} C^a{}_{b c} t^b \wedge t^c + r^a
$$

$$
  d_{W(\mathfrak{g})} : r^a \mapsto C^a{}_{b c} t^b \wedge r^c 
  \,.
$$




## References

The use of the Weil algebra in the calculation of the equivariant [[deRham cohomology]] of manifolds acted on by a compact group goes at least back to two papers by H. Cartan from 1950. These papers are reprinted, explained and put in a modern context in the book

* Victor Guillemin, Shlomo Sternberg, _Supersymmetry and Equivariant de Rham Theory_, Springer, 1999.


For the role played by the Weil algebra in the general context of higher [[Lie theory]] see

* Hisham Sati, Urs Schreiber, Jim Stasheff, _$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport_ ([arXiv](http://arxiv.org/abs/0801.3480))