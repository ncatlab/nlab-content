
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _projective bundle_ is the generalization of that of _[[projective space]]_ from [[vector spaces]] to [[vector bundles]].

## Definition
  {#Definition}

For $\pi_E \colon E \to X$ a [[topological vector bundle]] over some [[topological field]] $k$, write $E \setminus X \subset E$ for its [[complement]] of the [[zero section]], regarded with its [[subspace topology]]. 


Then its _projective bundle_ is the [[fiber bundle]] $P(\pi_E) \,\colon\, P(E) \to X$ whose total space is the [[quotient topological space]] of $E \setminus X$ by the [[equivalence relation]]

$$
  \left( 
    v_1 \sim v_2
  \right)
   \;\Leftrightarrow\;
  \left(
    (\pi(v_1) = \pi(v_2))
    \,\text{and}\,
    \left(
      \underset{c \in k \setminus \{0\}}{\exists}
      ( v_2 = c v_1)
    \right)
  \right)
$$

hence

$$
  P(E) 
    \coloneqq 
  (E \setminus X)/\sim
  \,,
$$

and whose bundle projection is 

$$
  \array{
    P(E) &\longrightarrow& X
    \\
    [v] &\mapsto& \pi(v)
  }
  \,.
$$

## Properties

### Splitting
 {#Splitting}

The [[pullback bundle]] of a vector bundle $E$ to its own projective bundle 

$$
  \array{
    P( \pi_E )^\ast E
    &\longrightarrow&
    E
    \\
    \big\downarrow
    &{}^{{}_{(pb)}}&
    \big\downarrow {}^{\mathrlap{\pi}}
    \\
    P(E) &\underset{P(\pi)}{\longrightarrow}& X
  }
$$

naturally contains a [[line bundle]], whose [[point-set topology|point-set]] definition is

$$
  \mathcal{L}
  \;\coloneqq\;
  \big\{  
    \left.
    ( \ell, v )
    \,\in\,
    P(E) \times_X E
    \;\right\vert\;
    v \in \ell
  \big\}
  \;\subset\;
  P( \pi_E )^\ast E
  \,.
$$

Hence the pullback splits as the [[direct sum of vector bundles]] of this $\mathcal{L}$ and its [[orthogonal complement]] (for any choice of [[inner product on vector bundles|inner product]]):

$$
  (P(\pi_E))^\ast (E)
  \;\simeq\;
  {
    \color{blue}
    \mathcal{L} 
  }
    \oplus 
  \big(
    P(\pi)^\ast(E)
  \big)/\mathcal{L}
  \,.
$$

This process continues: Pulling back further to the projective bundle of $\mathcal{L}^{\perp}$ yields

$$
  (P(\pi_{\mathcal{L}^\perp}))^\ast (P(\pi_E))^\ast (E)
  \;\simeq\;
  {
    \color{blue}
    \mathcal{L}'
  }
    \oplus
  (P(\pi_{\mathcal{L}^\perp}))^\ast
  \big(
    {\color{blue}
      \mathcal{L} 
    }
  \big)
  \oplus
  \big(
    (P(\pi_{\mathcal{L}^\perp}))^\ast P(\pi)^\ast(E)
  \big)/\big( P(\pi_{\mathcal{L}^\perp}))^\ast \mathcal{L} \oplus \mathcal{L}' \big)
  \,,
$$

for some line bundle $\mathcal{L}'$

This way, eventually one finds a [[pullback bundle]] of $E$ which is entirely a [[direct sum of vector bundles|direct sum]] of [[line bundles]].

(e.g. [Wirthmüller 12, p. 15 (17 of 67)](#Wirthmuller12))

This is one incarnation of the _[[splitting principle]]_. 


## Examples

### Complex-projective bundle of quaternionic tautological line bundle
 {#ComplexProjectiveBundleOfQuaternionicTautologicalLineBundle}

+-- {: .num_prop #ComplexProjectiveBundleOfQuaternTautologicalLineBundleIsComplexProjSpace} 
###### Proposition
**([[complex numbers|complex]] [[projective bundle]] of [[quaternionic vector bundle|quaternionic]] [[tautological line bundle]] is [[complex projective space]])**

For $n \in \mathbb{N}$, the [[projective bundle]] of the [[rank of a vector bundle|rank]]=2 [[complex vector bundle]] underlying the [[quaternionic line bundle|quaternionic]] ([[dual vector bundle|dual]]) [[tautological line bundle]] $\mathcal{L}_{{}_{\mathbb{H}P^n}}$ over [[quaternionic projective space]] $\mathbb{H}P^n$ is the [[complex projective space]] $\mathbb{C}P^{2n+1}$ equipped with the map that sends complex lines to the quaternionic lines that they span:

$$
  \array{
    P_{\mathbb{C}}
    \big(
      \mathcal{L}^\ast_{{}_{\!\!\!\mathbb{H}P^n}} 
    \big)
    && 
      \simeq
    &&
    \mathbb{C}P^{2n+1}
    \\
    & 
    \searrow 
    && 
    \swarrow_{ 
      \mathrlap{
        v \cdot \mathbb{C}^\times 
        \,\mapsto\,
        v \cdot \mathbb{H}^\times 
      } 
    }
    \\
    && \mathbb{H}P^n
  }
$$

=--

+-- {: .proof}
###### Proof

We compute as follows (showing this for the dual tautological bundle just for definiteness of notation):

$$
  \begin{aligned} 
    P_{\mathbb{C}}
    \big(
      \mathcal{L}^\ast_{\!\!\!\mathbb{H}P^n} 
    \big)
    & = \;
    \Big(
      \mathcal{L}_{{}_{\mathbb{H}P^n}}
      \setminus 
      \big(
        \mathbb{H}P^n \times \{0\}
      \big)
    \Big)
    \big/
    \mathbb{C}^\times
    \\
    & = \;
    \Big(
      \big(
        \mathbb{H}^{n+1} \setminus \{0\}
      \big)
      \underset
      {
        \mathbb{H}^\times
      }{
        \times
      }
      \big(
        \mathbb{H} \setminus \{0\}
      \big)
    \Big)
    \big/
    \mathbb{C}^\times
    \\
    & 
    \simeq\;
    \Big(
      \big(
        \mathbb{H}^{n+1} \setminus \{0\}
      \big)
      \times
      \{1\}
    \Big)
    \big/
    \mathbb{C}^\times
    \\
    & \simeq
    \big(
      \mathbb{C}^{2n+2} 
    \big)
    \big/
    \mathbb{C}^\times
    \\
    & \simeq \;
    \mathbb{C}P^{2n+1}
    \,.
  \end{aligned}
$$

Here:

1. The first line is the definition of the complex projective bundle ([here](#Definition));

1. the second line inserts the definition of the tautological quaternionic line bundle ([here](tautological+line+bundle#BareDefinition));

1. the third line observes that, being away from its [[zero section]], we have unique representatives of the elements in its defining [[quotient space]] whose fiber component is the unit $1 \in \mathbb{C} \subset \mathbb{H}$;

1. the fourth line identifies the evident underlying $\mathbb{C}^\times$[[G-space|-space]];

1. the fifth line is the definition of complex projective space.

This shows that the total space is as claimed. 

Moreover, since the projection map is the [[quotient space]] projection from this by the full $\mathbb{H}^\times$-action, the same computation with $(-)/\mathbb{C}^\times$ replaced by $(-)/\mathbb{H}^\times$ shows that the bundle map is as claimed.

=--

## Related entries

* [[Thom space]]

* [[fundamental product theorem in topological K-theory]]

* [[projective unitary group]]

* [[twisted K-theory]], [[twisted equivariant K-theory]]

## References

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 5 of: _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])


[[!redirects projective bundles]]
