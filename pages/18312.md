
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

For $\pi_E \colon E \to X$ a [[topological vector bundle]] over some [[topological field]] $k$, write $E \setminus X \subset E$ for its [[complement]] of the [[zero section]], regarded with its [[subspace topology]]. 


Then its _projective bundle_ is the [[fiber bundle]] $P(\pi_E) \,\colon\, P(E) \to X$ whose total space the [[quotient topological space]] of $E \setminus X$ by the [[equivalence relation]]

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
  P(E) \coloneqq (E \setminus )/\sim
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

This is one incarnation of the _[[splitting principle]]_. 



## Related entries

* [[Thom space]]

* [[fundamental product theorem in topological K-theory]]


## References

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 5 of: _Vector bundles and K-theory_, 2012 ([[wirthmueller-vector-bundles-and-k-theory.pdf:file]])


[[!redirects projective bundles]]
