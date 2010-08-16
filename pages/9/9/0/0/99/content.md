
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

The notion of _Weil algebra_ is ordinarily defined for a [[Lie algebra]] $\mathfrak{g}$. It may be understood as the [[Chevalley-Eilenberg algebra]] of the tangent [[Lie 2-algebra]] $T \mathfrak{g}$ or $inn(\mathfrak{g})$ of $\mathfrak{g}$, generalizing the notion of [[tangent Lie algebroid]] $T X$ from a 0-[[truncated]] Lie algebroid $X$ (a [[smooth manifold]]) to the one-obeject [[Lie algebroid]] $\mathfrak{g}$.

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

Let $\mathfrak{a}$ be a [[∞-Lie algebroid]], identified with its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a}) = \wedge^\bullet_{C^\infty(\mathfrak{a}_0)} \mathfrak{a}_{\geq 1}^* $. 

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

where $\sigma|_{\mathfrak{a}^*} : \mathfrak{a}^* \to \mathfrak{a}^*[1]$ is the canonical degree-shifting isomorphism, and in $\sigma \circ d_{\mathrm{CE}(\mathfrak{a})} \circ \sigma^{-1}$ its left appearance is its extension as a degree +1 [[derivation]].

## Properties {#Properties}

The main point of the definition is that the differential restricted to the original (unshifted) generators is the original differential plus the shift:

$$
  d_{W(\mathfrak{a})} |_{\mathfrak{a}^*} = d_{CE(\mathfrak{a})} + \sigma
  \,.
$$

By solving the condition $d_{W(\mathfrak{a})} \circ d_{W(\mathfrak{a})} = 0$ and using that $d_{CE(\mathfrak{a})} d_{CE(\mathfrak{a})} = 0$ this already fixes uniquely the differential $d_{W(\mathfrak{a})} \sigma t$ on the shifted generators $\sigma(t) \in \mathfrak{a}^*[1]$. For one computes:

$$
  \begin{aligned}
    0 & =
    d_{W(\mathfrak{a})}(d_{W(\mathfrak{a})} t)
    \\
    & = 
    d_{W(\mathfrak{a})}(d_{CE(\mathfrak{a})}t + \sigma t)
    \\
    & = \sigma d_{CE(\mathfrak{a})} t + d_{W(\mathfrak{a}) } \sigma t
  \end{aligned}
$$

and hence

$$
  d_{W(\mathfrak{a})} \sigma t = - \sigma d_{CE(\mathfrak{a})} \sigma^{-1} (\sigma t)
  \,.
$$

This implies the following [[free functor|free property]]:

+-- {: .un_prop}
###### Proposition

Let $\mathfrak{g}$ be an $L_\infty$-algebra. Morphisms of $dg$-algebras $W(\mathfrak{g}) \to A$ are in natural bijection to morphisms of [[graded vector space]]s $\mathfrak{g}^* \to U(A)$, where $U(A)$ is the graded vector space underlying $A$.

=--

+-- {: .proof}
###### Proof

Let $f : W(\mathfrak{g}) \to A$ be a dg-algebra morphism. By the fact that $\wedge^\bullet (\mathfrak{g}^* \oplus \mathfrak{g}^*[1])$ is a free graded-commutative algebra, this is fixed already by its value on the generators in $\mathfrak{g}^*$ and $\mathfrak{g}^*[1]$ and only further subject to the respect for the differentials.

This respect for the differentials implies that the value $f(\sigma(t))$ of $f$ on the shifted generators $\sigma(t)$ is uniquely fixed by its value on the unshifted generators $t$. From 

$$
  \begin{aligned}
    0 &=
    f(d_{W(\mathfrak{g})} t) - d_A f(t)
    \\
    & =
    f(d_{CE(\mathfrak{g})} t) + f(\sigma(t)) - d_A f(t)
  \end{aligned}
$$

we find that in order to have a dg-algebra homomorphism, it must be true that

$$
  f(\sigma(t)) = d_A f(t) - f(d_{CE(\mathfrak{g})} t)
  \,.
$$ 

So it only remains to check that this assignment does in turn imply that $f$ commutes with the differentials also on the shifted generators, i.e. that also

$$
  0 = f(d_{W(\mathfrak{g})} \sigma t) - d_A f(\sigma t)
$$

for all $t \in \mathfrak{g}^*$. To see this, apply $d_A$ to the above assignment, and use $d_A \circ d_A = 0$ to get

$$
  d_A f(\sigma(t)) = - d_A f( d_{CE(\mathfrak{g})} t)
  \,.
$$

Now observe that on the right we have $d_A \circ f$ applied to an expression entirely in the unshifted generators. On these we already know that the differential commutes with the morphism, so that this is

$$
  \cdots = - f (d_{W(\mathfrak{g})} \circ d_{CE(\mathfrak{g})} t)
  \,.
$$

Using now again the definition of $d_{W(\mathfrak{g})}$ on unshifted generators and the fact that $d_{CE(\mathfrak{g})}^2 = 0$ this is

$$
  \cdots = - f \sigma d_{CE(\mathfrak{g}) }t 
  \,.
$$

Comparing with the above unique solution of the action of $d_{W(\mathfrak{g})}$, we find that indeed this is

$$
  \cdots = f d_{W(\mathfrak{g})} \sigma t
  \,.
$$

=--

**Example**

In particular for $A = \Omega^\bullet(X)$ the [[de Rham complex]] of a [[smooth manifold]] $X$, we have that 

$$
  Hom_{dgAlg}(W(\mathfrak{g}), \Omega^\bullet(X))
  = 
  \Omega^\bullet(X) \otimes \mathfrak{g}
$$

is the collection of [[differential form]]s with values in the $\infty$-Lie algebra $\mathfrak{g}$.

A morphism of 

$$
  (A, F_A) : W(\mathfrak{g}) \to \Omega^\bullet(X)
$$

sends the unshifted generators $t^a$ to differential forms $A^a$ and sends the shifted generators $\sigma t^a$ to their [[curvature]]. The respect for the differential on the shifted generators is the [[Bianchi identity]] on these curvatures.


## Relation to invariant polynomials and Chern-Simons elements

A [[cocycle]] in the [[∞-Lie algebra cohomology]] of the [[∞-Lie algebra]] $\mathfrak{g}$ is a closed element in the [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{g})$.

An [[invariant polynomial]] $\langle -\rangle$ on $\mathfrak{g}$ is a closed element in the Weil algebra $\langle -\rangle \in W(\mathfrak{g})$, subject to the addition condition that it its entirely in the shifted copy of $\mathfrak{g}$, $\langle - \rangle \in \wedge^\bullet (\mathfrak{g}^*[1])$.

Since the cohomology of $W(\mathfrak{g})$ is trivial, there is necessarily for each invariant polynomial an element $cs_{\langle -\rangle}$ such that

$$
  d_{W(\mathfrak{g})} cs_{\langle -\rangle} = 
  \langle -\rangle
  \,.
$$

This is the [[Chern-Simons form|Chern-Simons element]] of the invariant polynomial. Its restriction 

$$
  \mu_{\langle -\rangle} := cs_{\langle - \rangle}|_{\wedge^\bullet \mathfrak{g}^*}
$$

to the unshifted copy, hence to the [[Chevalley-Eilenberg algebra]], is the cocycle that is in transgression with $\langle - \rangle$.







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

* [[eom]]: [Weil algebra of a Lie algebra](http://eom.springer.de/W/w130050.htm)

The use of the Weil algebra in the calculation of the equivariant [[de Rham cohomology]] of manifolds acted on by a compact group goes at least back to two papers by H. Cartan from 1950. These papers are reprinted, explained and put in a modern context in the book

* Victor Guillemin, Shlomo Sternberg, _Supersymmetry and equivariant de Rham theory_, Springer, 1999.

For the role played by the Weil algebra in the general context of [[∞-Lie theory]] see

* Hisham Sati, Urs Schreiber, Jim Stasheff, _$L_{\infty}$ algebra connections and applications to String- and Chern-Simons $n$-transport_ (<a href="http://ncatlab.org/schreiber/show/differential+cohomology+in+an+(%E2%88%9E%2C1)-topos+--+references#SSSI">ref</a>)