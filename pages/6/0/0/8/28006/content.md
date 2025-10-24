
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
=--
=--



\tableofcontents

## Idea

The *orbit-stabilizer theorem* says that a [[transitive action]] of a [[group]] $G$ on some $X$ is equivalent to the canonical action of $G$ on the [[cosets]] $G/Stab_G$ by the [[stabilizer subgroup]] $G_x \coloneqq Stab_g(x)$ of any [[element]] $x \in X$, identifying $X$ with the $G$-[[orbit]] of $x$;

$$
  X 
  \simeq
  Orbit_G(x)
  \simeq
  G/Stab_G(x)
  \mathrlap{\,.}
$$

## For smooth actions

In [[differential geometry]]:

\begin{proposition}

For 

* $G$ a [[Lie group]],

* $G \curvearrowright X$ a [[homogeneous space|homogeneous]] [[smooth manifold|smooth]] [[G-manifold|$G$-manifold]], hence with a [[transitive action|transitive]] [[smooth function|smooth]] [[group action|$G$-action]],

* $x \colon \ast \to X$ a point,

then 

1. the [[stabilizer group]] of $x$ under $G$ is a [[closed subgroup]] $G_x \subset G$,

1. the map $G/G_x \longrightarrow X \;\colon\; g \cdot G_x \mapsto g \cdot x$ is an [[equivariant function|equivariant]] [[diffeomorphism]].

\end{proposition}

(cf. [Warner 1983 Thm. 3.62](Warner83), [Lee 2012, Thm. 21.18](#Lee12))

## References

For [[finite groups]] acting on [[sets]]:

* *The Orbit-Stabilizer Theorem* &lbrack;[pdf](https://maths.nuigalway.ie/~rquinlan/groups/section3-2.pdf)&rbrack;

See also: 

* Wikipedia: *[Orbit-stabilizer theorem](https://en.wikipedia.org/wiki/Group_action#Orbit%E2%80%93stabilizer_theorem)*

For [[Lie group]] actions on [[smooth manifolds]]:

* {#Warner83} [[Frank W. Warner]], thm. 3.62 in: *Foundations of Differentiable Manifolds and Lie Groups*,  Graduate Texts in Mathematics **94** (1983) &lbrack;[doi:10.1007/978-1-4757-1799-0](https://doi.org/10.1007/978-1-4757-1799-0)&rbrack; 

* {#Lee12} [[John Lee]], Thm. 21.18 in: *Introduction to Smooth Manifolds*, Springer (2012) &lbrack;[doi:10.1007/978-1-4419-9982-5](https://doi.org/10.1007/978-1-4419-9982-5), [book webpage](https://sites.math.washington.edu/~lee/Books/ISM/), [pdf](https://math.berkeley.edu/~jchaidez/materials/reu/lee_smooth_manifolds.pdf)&rbrack;

[[!redirects orbit-stabilizer theorems]]






