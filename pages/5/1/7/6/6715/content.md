
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _Bockstein homomorphism_ is a [[connecting homomorphism]] induced from a [[short exact sequence]] whose injective map is given by multiplication with an [[integer]].

The archetypical examples are the Bockstein homomorphisms induced this way from the short exact sequence

$$
  \mathbb{Z} 
    \stackrel{\cdot 2}{\to} 
  \mathbb{Z}
    \stackrel{}{\to}
  \mathbb{Z}/2\mathbb{Z}
  \,.
$$

These relate notably degree-$n$ [[cohomology]]  with [[coefficients]] in $\mathbb{Z}_2$ (such as [[Stiefel-Whitney classes]]) to cohomology with integral coefficients in degree $n+1$ (such as [[integral Stiefel-Whitney classes]]).

## Definition

Let $A$ be an [[abelian group]] and $m$ be an [[integer]]. Then multiplication by $m$

$$
  A \stackrel{m\cdot}{\to} A
$$

induces a [[short exact sequence]] of abelian groups

$$
  0\to A/A_{m-tors} \stackrel{m\cdot}{\to} A \to A/m A\to 0,
$$

where $A_{m-tors}$ is the subgroup of $m$-torsion elements of $A$,
and so a long [[fiber sequence]]

$$
\cdots \mathbf{B}^n (A/A_{m-tors}) \to \mathbf{B}^n A \to \mathbf B^n(A/ m A) \to \mathbf{B}^{n+1} (A/A_{m-tors}) \to \cdots
$$

of [[∞-groupoid]]s, where $\mathbf{B}^n(-)$ denotes the $n$-fold [[delooping]] (hence $\mathbf{B}^n A$ is the [[Eilenberg-MacLane object]] on $A$ in degree $n$).

This induces, in turn, for any object $X \in \mathbf{H}$ (for $\mathbf{H}$ the ambient [[(∞,1)-topos]], such as [[Top]] $\simeq$ [[∞Grpd]]) , a long [[fiber sequence]]

$$
\cdots \mathbf{H}(X,\mathbf{B}^n (A/A_{m-tors})) \to \mathbf{H}(X,\mathbf{B}^n A) \to \mathbf{H}(X,\mathbf B^n(A/ m A)) \stackrel{\beta_m}{\to} \mathbf{H}(X,\mathbf{B}^{n+1} (A/A_{m-tors})) \to \cdots
$$

of [[cocycle]] [[∞-groupoids]].

Here the [[connecting homomorphisms]] $\beta_m$ are called the **Bockstein homomorphisms**. 

Notice that often this term is used to refer only to the image of the above in [[cohomology]], hence to the image of $\beta_m$ under [[0-truncated|0-truncation]]/[[homotopy group|0th homotopy group]] $\pi_0$:

$$
 \beta_m : H^n(X,A/ m A) \to H^{n+1}(X,(A/A_{m-tors}))
  \,.
$$

## Examples

* When $A=\mathbb{Z}$, the equivalence $\vert \mathbf{B}^{n+1}\mathbb{Z} \vert \cong \vert \mathbf{B}^n U(1)\vert$ (which holds in ambient contexts such as $\mathbf{H} = $ [[ETop∞Grpd]] or [[Smooth∞Grpd]] under [[geometric realization]] $\vert - \vert : ETop \infty Grpd \stackrel{\Pi}{\to} \infty Grpd \stackrel{\simeq}{\to} Top$) identifies the morphisms $\mathbf{B}^n(\mathbb{Z}_m)\to \mathbf{B}^{n+1}\mathbb{Z}$ with the morphisms $\mathbf{B}^n(\mathbb{Z}_m)\to \mathbf{B}^{n} U(1)$ induced by the inclusion of the subgroup of $m$-th roots of unity into $U(1)$. This identifies the Bockstein homomorphism $\beta_m: H^n(X;\mathbb{Z}_m)\to H^{n+1}(X;\mathbb{Z})$ with the natural homomorphism 
$H^n(X;\mathbb{Z}_m)\to H^{n}(X;U(1))$.

* The Bockstein homomorphism $\beta$ for the sequence $\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z} \stackrel{}{\to} \mathbb{Z}_2$ serves to defined [[integral Stiefel-Whitney class]]es $W_{n+1} := \beta w_n$ in degree $n+1$ from $\mathbb{Z}_2$-valued [[Stiefel-Whitney class]]es in degree $n$.

* For $p$ any [[prime number]] the multiplication by $p$ on $\mathbb{Z}_{p^2}$ induces the short exact sequence $\mathbb{Z}_p \to \mathbb{Z}_{p^2} \to \mathbb{Z}_p$. The corresponding Bockstein homomorphism $\beta_p$ appears as one of the generators of the [[Steenrod algebra]].

## Related concepts

* [[Steenrod squares]], [[cohomology operation]]

* [[Bockstein spectral sequence]]

## References

Original references include

* M. Bockstein,  

  _Universal systems of $\nabla$-homology rings_, C. R. (Doklady) Acad. Sci. URSS (N.S.) 37 (1942), ": 243&#8211;245, MR0008701

  _A complete system of fields of coefficients for the $\nabla$-homological dimension_ ,  C. R. (Doklady) Acad. Sci. URSS (N.S.) (1943),  38: 187&#8211;189, MR0009115

* Bockstein, Meyer _Sur la formule des coefficients universels pour les groupes d'homologie_ ,  Comptes Rendus de l'acad&#233;mie des Sciences. S&#233;rie I. Math&#233;matique (1958),  247: 396&#8211;398, MR0103918

[[!redirects Bockstein homomorphisms]]
[[!redirects Bockstein morphism]]
[[!redirects Bockstein morphisms]]
[[!redirects Bockstein operation]]
[[!redirects Bockstein operations]]