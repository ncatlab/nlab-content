<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea

The notion of _Weil algebra_ is ordinarily defined for a [[Lie algebra]] $\mathfrak{g}$. It may be understood as the [[Chevalley-Eilenberg algebra]] of the tangent [[Lie 2-algebra]] $T \mathfrak{g}$ of $\mathfrak{g}$, generalizing the notion of [[tangent Lie algebroid]] $T X$ from a 0-[[truncated]] Lie algebroid $X$ (a [[smooth manifold]]) to the one-obeject [[Lie algebroid]] $\mathfrak{g}$.

Generally, for every [[Lie-∞-algebroid]] $\mathfrak{a}$ one may define the corresponding tangent Lie-$\infty$-algebroid $T \mathfrak{a}$ , whose Chevalley-Eilenberg algebra may be called the Weil algebra of $\mathfrak{a}$:

$$
  W(\mathfrak{a})
  =
  CE(T \mathfrak{a})
  \,.
$$



### Weil algebra of a Lie algebra 

Let $\mathfrak{g}$ be a finite-dimensional [[Lie algebra]]. The **Weil algebra** $W(\mathfrak{g})$ of $\mathfrak{g}$ is

* the graded [[Grassmann algebra]] generated from the dual [[vector space]] $\mathfrak{g}^*$ together with another copy of $\mathfrak{g}^*$ shifted in degree

  $$
    W(\mathfrak{g}) := \wedge^\bullet 
   (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])
  $$

* equipped with a [[derivation]] $d : W(\mathfrak{g}) \to W(\mathfrak{g})$ that makes this a [[dg-algebra]], defined by the fact that on $\mathfrak{g}^*$ it acts as the differential of the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ plus the degree shift morphism $\mathfrak{g}^* \to \mathfrak{g}^*$.

This Weil algebra has trivial [[chain homology and cohomology|cohomology]] and sits in a sequence

$$
  CE(\mathfrak{g}) \leftarrow W(\mathfrak{g})
  \leftarrow inv(\mathfrak{g})
$$

with the [[Chevalley-Eilenberg algebra]] of $\mathfrak{g}$ and its algebra of [[invariant polynomial]]s on $\mathfrak{g}$. This may be understood as a model for the sequence of algebras of differential forms on the [[generalized universal bundle|universal G-bundle]]

$$
  G \to \mathcal{E}G \to \mathcal{B}G
  \,.
$$

As such, the Weil algebra plays a crucial role in the study of the [[Lie algebra cohomology]] of $\mathfrak{g}$.


## Definition

Let $\mathfrak{a}$ be a [[Lie-∞-algebroid]], identified with its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a}) = \wedge^\bullet_{C^\infty(\mathfrak{a}_0)} \mathfrak{a}_{\geq 1}^* $. 

The corresponding **Weil algebra** is

$$
  \mathrm{W}(\mathfrak{a})
  := CE(T \mathfrak{a})
  :=
  \left(
    \wedge^\bullet_{C^\infty(\mathfrak{a}_0)}
    (
      \mathfrak{a}_{\geq 1}^* \oplus \Gamma(T^* \mathfrak{a}_0) 
      \oplus \mathfrak{a}_{\geq 1}^*[1]
    )
    , d_{\mathrm{W}(\mathfrak{a})}
  \right)
$$

where the differential acts as the de Rham differential on $\wedge^\bullet \Gamma(T^* \mathfrak{a}_0)$ and is defined on generators in $\mathfrak{a}^* \oplus \mathfrak{a}^*[1]$ by 

$$
  d_{\mathrm{W}(\mathfrak{a})}
  =
  \left(
    \array{
       d_{\mathrm{CE}(\mathfrak{a})}
       &
       0
       \\
       \sigma
       &
       - \sigma \circ d_{\mathrm{CE}(\mathfrak{a})}
       \circ \sigma^{-1}
    }
    \,,
  \right)
$$

where $\sigma|_{\mathfrak{a}^*} : \mathfrak{a}^* \to \mathfrak{a}^*[1]$ is the canonical degree-shifting isomorphism.

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

### Weil algebra of a 0-truncated Lie algebroid

A 0-[[truncated]] Lie algebroid is just a [[smooth manifold]] $X$.
Its Weil algebra is the Chevalley-Eilenberg algebra of the
[[tangent Lie algebroid]] $T X$ of $X$, which is the [[de Rham algebra]]
$\Omega^\bullet(X)$ of $X$:

$$
  W(X) = CE(T X) = (\Omega^\bullet(X), d_{dR})
  \,.
$$


## References

The use of the Weil algebra in the calculation of the equivariant [[de Rham cohomology]] of manifolds acted on by a compact group goes at least back to two papers by H. Cartan from 1950. These papers are reprinted, explained and put in a modern context in the book

* Victor Guillemin, Shlomo Sternberg, _Supersymmetry and Equivariant de Rham Theory_, Springer, 1999.


For the role played by the Weil algebra in the general context of higher [[Lie theory]] see

* Hisham Sati, Urs Schreiber, Jim Stasheff, _$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport_ ([arXiv](http://arxiv.org/abs/0801.3480))