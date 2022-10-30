
+-- {: .standout}
Every wiki needs a sandbox! Just test *between* the horizontal rules below (`***` in the source) and don\'t worry about messing things up.
=--

***

We discuss aspects of the twisted smooth cohomology involved
over [[D-branes]] in [[type II string theory]].


For each $n$, the [[central extension]] of Lie groups

$$
  U(1) \to U(n) \to PU(n)
$$

that exhibits the [[unitary group]] as a [[circle group]]-extension of the [[projective unitary group]] induces the corresponding morphism of smooth [[moduli stacks]]

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
  \,.
$$

This is part of a [[fiber sequence|long fiber sequence]] which continues to the right by a [[connecting homomorphism]] $\mathbf{dd}_n$

$$
  \mathbf{B} U(1) \to \mathbf{B} U(n) \to \mathbf{B} PU(n)
   \stackrel{\mathbf{dd}_n}{\to}
  \mathbf{B}^2 U(1)
  \,.
$$

A morphism $\phi : X \to \mathbf{B}^2 U(1)$ is a [[circle n-bundle with connection|circle 2-bundle]]. With respect to a 

and a $\phi$-twisted cocycle

$$
  \array{
    X &&\stackrel{}{\to}&& \mathbf{B} PU(n)
    \\
    & {}_{\mathllap{\phi}}\searrow &\swArrow_{\simeq}& \swarrow_{\mathrlap{\mathbf{dd}_n}}
    \\
    &&
    \mathbf{B}^2 U(1)
  }
$$

is a unitary $\phi$-[[twisted bundle]]. 

For each $n \in \mathbb{N}$ there is a canonical inclusion $\mathbf{B} U(n) \to \mathbf{B} U(n+1)$, exhibiting the fact that a rank-$n$ complex vector bundle canonically induces a rank-$(n+1)$-bundle by added a trivial line bundle.

We may form the [[directed colimit]] of smooth moduli stacks

$$
  \mathbf{B}U \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} U(n)
$$

$$
  \mathbf{B} PU \coloneqq \underset{\rightarrow_n}{\lim} \mathbf{B} PU(n)
$$

**Proposition** The stack $\mathbf{B} U$ is a smooth refinement of the [[classifying space]] $B U$ of reduced [[K-theory]]. Also, for $X$ a [[compact topological space|compact]] [[smooth manifold]] smooth $U$-principal bundles and smooth $U$-gauge transformations on $X$ are represented by ordinary $U(n)$-bundles for some finite $n$.

$$
  \mathbf{H}(X, \mathbf{B}U)
  \simeq
  \underset{\rightarrow_n}{\lim} \mathbf{H}(X, \mathbf{B} U(n))
  \,.
$$

Write therefore 

$$
  \array{
    \mathbf{B}U &\to& \mathbf{B} PU
    \\
    \downarrow^{\mathbf{dd}}
    \\
    \mathbf{B}^2 U(1)
  }
$$

for the corresponding universal coefficient bundle.

The corresponding twisted cohomology appears in string theory as [[relative cohomology]] over [[D-branes]]. 

Let therefore $i : Q \hookrightarrow X$ be a compact submanifold.
Assume first that it is equipped with [[spin^c structure]].

Then a cocycle in the corresponding relative cohomology is a diagram of smooth stacks

$$
  \array{
    Q &\stackrel{\phi_{ga}}{\to}& \mathbf{B} PU 
    \\
    {}^{\mathllap{i}}\downarrow 
      &\swArrow& \downarrow^{\mathrlap{\mathbf{dd}}}
    \\
    X &\stackrel{\phi_B}{\to}& \mathbf{B}^3 U(1)
  }
  \,.
$$

This is 

* a [[circle n-bundle with connection|circle 2-bundle]] $\phi_B : X \to \mathbf{B}^2 U(1)$ on [[spacetime]] $X$: the underlying bundle of the [[B-field]];

* a projective unitary bundle $\phi_{ga}$ on $Q$;

* together with an identification of the restriction $\phi_{B}|_Q$ with the [[obstruction]] $\mathbf{dd}(\phi_{ga})$ to lift $\phi_{ga}$ to a genuine unitary bundle.

This is a cocycle in reduced $\phi_{ga}|_{Q}$-[[twisted K-theory]] on $Q$.


More generally, if $Q \to \mathbf{B}SO$ does not admit  
a [[spin^c structure]] the Freed-Witten anomaly cancellation condition demands that 

$$
  [\mathbf{dd}(\phi_{ga})] + [W_3(o_Q)] = [\phi_B|_Q]
  \,.
$$

Formulating this constraint not on cohomology classes but on 
cocycles in [[homotopy type theory]] yields the moduli stack

$$
  \array{
    \{
      \mathbf{dd}(\phi_{ga})  +  W_3(o_Q)  \simeq  \phi_B|_Q
    \}
    &\to&
    [Q, \mathbf{B}^2 U(1)]
    \\
    \downarrow && \downarrow
    \\
    [Q, \mathbf{B} (SO \times PU)]
    &\stackrel{\mathbf{W}_3 - \mathbf{dd}}{\to}&
    [Q, \mathbf{B}^3 U(1)]
  }
  \,.
$$




***

category: meta

[[!redirects Sandbox]]
[[!redirects SandBox]]
[[!redirects Sand Box]]
[[!redirects sandbox]]
[[!redirects Symbol Sandbox]]
[[!redirects sandbox905234]]
[[!redirects testing]]
[[!redirects tester]]
[[!redirects test]]
[[!redirects tested]]
[[!redirects foo]]
[[!redirects baz]]
[[!redirects foobar]]
[[!redirects bink]]
[[!redirects bar]]
[[!redirects nitwit]]
[[!redirects nitwits]]
[[!redirects nitwitta]]
[[!redirects nincompoops]]
[[!redirects שנה טובה]]
