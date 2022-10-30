
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Let $A$ be an [[abelian group]] and $m$ be an [[integer]] such that the multiplication by $m$

$$
  A \stackrel{m\cdot}{\to} A
$$

is [[monomorphism|injective]]. Then we have a [[short exact sequence]] of abelian groups

$$
  0\to A \stackrel{m\cdot}{\to} A \to A/m A\to 0
$$

and so a long [[fiber sequence]]

$$
\cdots \mathbf{B}^n A \to \mathbf{B}^n A \to \mathbf B^n(A/ m A) \to \mathbf{B}^{n+1} A \to \cdots
$$

of [[∞-groupoid]]s, where $\mathbf{B}^n(-)$ denotes the $n$-fold [[delooping]] (hence $\mathbf{B}^n A$ is the [[Eilenberg-MacLane object]] on $A$ in degree $n$).

This induces, in turn, for any object $X \in \mathbf{H}$ (for $\mathbf{H}$ the ambient [[(∞,1)-topos]], such as [[Top]] $\simeq$ [[∞Grpd]]) , a long [[fiber sequence]]

$$
\cdots \mathbf{H}(X,\mathbf{B}^n A) \to \mathbf{H}(X,\mathbf{B}^n A) \to \mathbf{H}(X,\mathbf B^n(A/ m A)) \stackrel{\beta_m}{\to} \mathbf{H}(X,\mathbf{B}^{n+1} A) \to \cdots
$$

of [[cocycle]] [[∞-groupoids]].

Here the [[connecting homomorphisms]] $\beta_m$ are called the **Bockstein homomorphisms**. 

Notice that often this term is used to refer only to the image of the above in [[cohomology]], hence to the image of $\beta_m$ under [[0-truncated|0-truncation]]/[[homotopy group|0th homotopy group]] $\pi_0$:

$$
 \beta_m : H^n(X,A/ m A) \to H^{n+1}(X,A)
  \,.
$$

## Examples

* The Bockstein homomorphism $\beta$ for the sequence $\mathbb{Z} \stackrel{\cdot 2}{\to} \mathbb{Z} \stackrel{}{\to} \mathbb{Z}_2$ serves to defined [[integral Stiefel-Whitney class]]es $W_{n+1} := \beta w_n$ in degree $n+1$ from $\mathbb{Z}_2$-valued [[Stiefel-Whitney class]]es in degree $n$.

* For $p$ any [[prime number]] the Bockstein homomorphism for the sequence $\mathbb{Z}_p \to \mathbb{Z}_{p^2} \to \mathbb{Z}_p$ appears as one of the generators of the [[Steenrod algebra]].


## References

Original references include

* M. Bockstein,  

  _Universal systems of $\nablka$-homology rings_, C. R. (Doklady) Acad. Sci. URSS (N.S.) 37 (1942), ": 243&#8211;245, MR0008701

  _A complete system of fields of coefficients for the $\nabla$-homological dimension_ ,  C. R. (Doklady) Acad. Sci. URSS (N.S.) (1943),  38: 187&#8211;189, MR0009115

* Bockstein, Meyer _Sur la formule des coefficients universels pour les groupes d'homologie_ ,  Comptes Rendus de l'acad&#233;mie des Sciences. S&#233;rie I. Math&#233;matique (1958),  247: 396&#8211;398, MR0103918

[[!redirects Bockstein homomorphisms]]
[[!redirects Bockstein morphism]]
[[!redirects Bockstein morphisms]]