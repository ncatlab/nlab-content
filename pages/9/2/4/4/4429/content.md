
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Chern-Weil theory
+--{: .hide}
[[!include infinity-Chern-Weil theory - contents]]
=--
#### Differential cohomology
+--{: .hide}
[[!include differential cohomology - contents]]
=--
=--
=--

#Contents#
* automatic table of contents goes here
{:toc}

## Idea

For $G$ a [[Lie group]] with [[Lie algebra]] $\mathfrak{g}$, a $G$-[[principal bundle]] $P \to X$ on a [[smooth manifold]] $X$ induces a collection of classes in the [[de Rham cohomology]] of $X$: the classes of the [[curvature characteristic form]]s 

$$
  P(F_A) \in \Omega^{2n}_{closed}(X)
$$ 

of the [[curvature]] 2-form $F_A \in \Omega^2(P, \mathfrak{g})$ of any [[connection on a bundle|connection]] on $P$, and for each [[invariant polynomial]] $P$ of arity $n$ on $\mathfrak{g}$.

This is a map from the first [[nonabelian cohomology]] of $X$ with coefficients in $G$ to the [[de Rham cohomology]] of $X$

$$
  char : H^1(X,G) \to \prod_{n_i} H_{dR}^{2 n_i}(X)
$$

where $i$ runs over a set of generators of the invariant polynomials. This is the analogy in [[nonabelian cohomology|nonabelian]] [[differential cohomology]] of the generalized [[Chern character]] map in [[generalized (Eilenberg-Steenrod) cohomology|generalized Eilenberg-Steenrod]]-[[differential cohomology]].


## In terms of $\infty$-Lie algebroids

An [[Ehresmann connection]] on a $G$-[[principal bundle]] $P$ is a differential form $A \in \Omega^1(P,\mathfrak{g})$ that restricts to the canonical flat $\mathfrak{g}$-valued 1-form $A_{vert} \in \Omega^1(P_x, \mathfrak{g})$ on the fibers $\simeq G$ of $P$. nWriten $T P$ for the [[tangent Lie algebroid]] of $P$ and $T_{vert}P$ for the [[vertical tangent Lie algebroid]], and $inn(\mathfrak{g})$ for the [[Lie 2-algebra]] coming from the [[differential crossed module]] $[\mathfrak{g} \stackrel{Id}{\to} \mathfrak{g}]$, this gives a diagram of [[∞-Lie algebroid]]s


$$
  \array{
     T_{vert} P &\stackrel{A_{vert}}{\to}& \mathfrak{g}
     \\
     \downarrow && \downarrow
     \\
     T P &\stackrel{(A,F_A)}{\to}& inn(\mathfrak{g})
  }
  \,.
$$

The [[curvature characteristic form]]s of $A$ on $P$ are in terms of this given by postcomposition with the canonical morphisms

$$
  P_i : inn(\mathfrak{g}) \to b^{2 n_i} \mathfrak{u}(1)
$$

that encode the [[invariant polynomial]]s (dually this are the morphism of [[dg-algebra]]s $W(\mathfrak{g}) \leftarrow CE(b^n \mathfrak{u}(1))$ from the dg-algebra on a single degree $2 n_i$-generator and vanishing differential into the [[Weil algebra]]), i.e. by the composite

$$
  P(F_A) : T P \stackrel{(A,F_A)}{\to}
  inn(\mathfrak{g})
  \stackrel{P_i}{\to}
  b^{2 n_i} \mathfrak{u}(1)
  \,.
$$

The _second_ condition on an [[Ehresmann connection]], which says that $A$ is Ad-equivariant under the $G$-action on $P$, ensures precisely that these forms are _invariant_ under the $G$-action and hence descend to forms down on $X$. This is expressed by the commutativiy of the bottom square in

$$
  \array{
     T_{vert} P &\stackrel{A_{vert}}{\to}& b \mathfrak{g}
     \\
     \downarrow && \downarrow
     \\
     T P &\stackrel{(A,F_A)}{\to}& b inn(\mathfrak{g})
     \\
     \downarrow && \downarrow
     \\
     T X &\stackrel{P_i(F_A)}{\to}& b^{2 n_i} \mathfrak{u}(1)
  }
  \,.
$$

So this kind of diagram may be thought of as inducing the Weil-homomorphism mapping $P$ to $P_i(F_A)$.

(...)

## References

See [[Chern-Weil theory]].


[[!redirects Weil homomorphism]]
