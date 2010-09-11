
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

* [[∞-Lie algebra cohomology]]

* [[Chevalley-Eilenberg algebra]]

* [[Weil algebra]]

* **invariant polynomial**

***



#Contents#
* automatic table of contents goes here
{:toc}


## Idea


For every [[Lie algebra]] or [[∞-Lie algebra]] or [[∞-Lie algebroid]] $\mathfrak{a}$ there is its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})$ and its [[Weil algebra]] $W(\mathfrak{a})$ and a canonical [[dg-algebra]] morphism

$$
  CE(\mathfrak{a}) \leftarrow W(\mathfrak{a})
  \,.
$$ 

Recall that a [[∞-Lie algebra cohomology|cocycle]] on $\mathfrak{a}$ is a closed element in $CE(\mathfrak{a})$. An invariant polynomial is a closed elements in $W(\mathfrak{a})$ that sits in the shifted copy $\wedge^\bullet (\mathfrak{a}^*[1])$.

This means that for $X \in \mathfrak{a}$, for $\iota_X : W(\mathfrak{a}) \to W(\mathfrak{a})$ the contraction derivation and $ad_X := [d_W, \iota_X]$ the corresponding [[Lie derivative]], we have in particular that an invariant polynomial $\langle -\rangle \in W(\mathfrak{a})$ is invariant in the sense that 

$$
  ad_X \langle -\rangle = 0
  \,.
$$

For $\mathfrak{a} = \mathfrak{g}$ an ordinary [[Lie algebra]], an invariant polynomial on $\mathfrak{g}$ is precisely a symmetric multilinear map on $\mathfrak{g}$ which is $ad$-invariant in the ordinary sense.


## Definition

+-- {: .un_defn}
###### Definition

For $\mathfrak{a}$ an [[∞-Lie algebroid]] (of finite type, i.e. degreewise of finite rank) with [[Chevalley-Eilenberg algebra]] 

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{a}^*, d_{CE(\mathfrak{a}}))
$$ 

and [[Weil algebra]] 

$$
  W(\mathfrak{a}) = (\wedge^\bullet (\mathfrak{a}^* \oplus \mathfrak{a}^*[1]), d_{W(\mathfrak{a})})
$$

an **invariant polynomial** on $\mathfrak{a}$ is an elements $\langle - \rangle \in W(\mathfrak{a})$ with the property that

* $\langle - \rangle$ is a wedge product of generators in the shifted copy of 
  $\mathfrak{a}^*$ $W(\mathfrak{a})$, i.e.

  $$
    \langle - \rangle \in \wedge^\bullet \mathfrak{a}^*[1]
  $$

  or equivalently: for all $x \in \mathfrak{a}$ and $\iota_X : W(\mathfrak{a}) \to W(\mathfrak{a})$ the contraction [[derivation]], we have

  $$
    \iota_x \langle -\rangle = 0
    \,;
  $$

* it is closed in $W(\mathfrak{a})$ in that $d_{W(\mathfrak{a})} \langle - \rangle = 0$.

=--


+-- {: .un_remark}
###### Remark


This implies that for 

$$
  ad_x := [d_{W(\mathfrak{a})}, \iota_X]
$$

the [[Lie derivative]] in $W(\mathfrak{a})$ along $x \in \mathfrak{a}$, which encodes the coadjoint action of $\mathfrak{a}$ on $W(\mathfrak{a})$, we have

$$
  ad_x \langle - \rangle = 0
$$

for all $x$. But the condition for an invariant polynomial is stronger than these ad-invariances. For instance there are  [[∞-Lie algebra cohomology|∞-Lie algebra cocycles]] $\mu \in CE(\mathfrak{g})$ which when regarded as elements in $W(\mathfrak{g})$ are ad-invariant. But being entirely in the un-shifted copy, $\mu \in \wedge^\bullet \mathfrak{g}^*$, these are not invariant polynomials.

=--

## Role in $\infty$-Chern-Weil theory

In ($\infty$-)[[Chern-Weil theory]] the crucial role played by the invariant polynomials is their relation to [[∞-Lie algebra cocycle]]s. One may understand invariant invariant polynomials as extending under [[Lie integration]] $\infty$-Lie algebra cocycles from [[cohomology]] to [[differential cohomology]].


### Transgression cocycles and Chern-Simons elements {#TransgressionCocycles}


+-- {: .un_defn}
###### Definition
**(Chern-Simons elements and transgression cocycles)**

Let $\mathfrak{a} = \mathfrak{g}$ be an [[∞-Lie algebra]]. Since the [[cochain cohomology]] of the [[Weil algebra]] $W(\mathfrak{g})$ is trivial, for every invariant polynomial $\langle -\rangle \in W(\mathfrak{g})$ there is necessarily an element $cs \in W(\mathfrak{g})$ with

$$
  d_{W(\mathfrak{g})} cs = \langle -\rangle
  \,.
$$

This we call a [[Chern-Simons form|Chern-Simons element]] for $\langle -\rangle$.

This element $cs$ will in general not sit entirely in the shifted copy. Its restriction

$$
  \mu := cs|_{\wedge^\bullet \mathfrak{g}^*} \in CE(\mathfrak{g})
$$

is a [[∞-Lie algebra cohomology|∞-Lie algebra cocycle]]. We say this is _in transgression_ with $\langle -\rangle$.

In total this construction yields a commuting diagram

$$
  \array{
     CE(\mathfrak{g}) &\stackrel{\mu}{\leftarrow}& CE(b^{n-1}\mathbb{R})
     &&& cocycle
     \\
     \uparrow && \uparrow
     \\
     W(\mathfrak{g}) &\stackrel{(cs,\langle -\rangle)}{\leftarrow}&
     W(b^{n-1} \mathbb{R})
     &&&
     Chern-Simons-element
     \\
     \uparrow && \uparrow
     \\
     inv(\mathfrak{g}) &\stackrel{\langle -\rangle}{\leftarrow}&
     CE(b^n \mathbb{R})
     &&&
     invariant\; polynomial
  }
  \,,
$$

where $b^{n-1}\mathbb{R}$ denotes the [[∞-Lie algebra]] whose CE-algebra has a single generator in degree $n$ and vanishing differential, and where $CE(b^n \mathbb{R}) = inv(b^{n-1}\mathbb{R})$ is the algebra of invariant polynomials of $b^{n-1} \mathbb{R}$.

=--

+-- {: .un_prop}
###### Proposition

The element $\mu \in CE(\mathfrak{g})$ associated to an invariant polynomial $\langle -\rangle$ by the above procedure is indeed a cocycle, and its cohomology class is independent of the choice of the element $cs$ involved.

=--

+-- {: .proof}
###### Proof

The procedure tahat assigns $\mu$ to $\langle- \rangle$ is illustarted by the following diagram

$$
  \array{
    0 && \langle-\rangle &\leftarrow & \langle-\rangle
    \\
    \;\;\uparrow^{\mathrlap{d_{CE(\mathfrak{g})}}}
    &&
    \;\;\uparrow^{\mathrlap{d_{W(\mathfrak{g})}}}
    \\
    \mu &\leftarrow& cs
    \\
    \\
    \\
    \\
    CE(\mathfrak{a})
    &\leftarrow&
    W(\mathfrak{a})
    &\leftarrow&
    inv(\mathfrak{a})    
  }
$$

From the fact that all morphisms involved respect the differential and from the fact that the image of $\langle-\rangle$ in $CE(\mathfrak{g})$ vanishes it follows that 

* the element $\mu$ satisfies $d_{CE(\mathfrak{a})} \mu = 0$, hence that it is an [[∞-Lie algebra cohomology|∞-Lie algebra cocycle]];

* any two different choices of $cs$ lead to cocylces $\mu$ that are cohomologous.

=--


This construction exhibits effectively the preimage of the [[connecting homomorphism]] in the [[cochain cohomology]] sequence induced by $W(\mathfrak{g}) \to CE(\mathfrak{g})$:

The [[dg-algebra]] of invariant polynomials is a sub-dg-algebra of the kernel of the morphism $i^* : W(\mathfrak{a}) \to CE(\mathfrak{a})$ from the [[Weil algebra]] to the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$

$$
  inv(\mathfrak{a}) \subset CE(\Sigma \mathfrak{a}) = ker(W(\mathfrak{a}) \to CE(\mathfrak{a}))
  \,.
$$

From the short [[nLab:exact sequence]]

$$
  CE(\Sigma \mathfrak{a}) \to W(\mathfrak{a}) \to 
  CE(\mathfrak{a})
$$

we obtain the long exact sequence in [[chain homology and cohomology|cohomology]]

$$
  \cdots 
  \to 
  H^{n+1}(CE(\mathfrak{a}))
  \stackrel{\delta}{\to} H^{n+2}(CE(\Sigma \mathfrak{a}))
  \to \cdots 
  \,.
$$

We say that $\mu \in CE(\mathfrak{a})$ is in transgression with $\omega \in inv(\mathfrak{a}) \subset CE(\Sigma \mathfrak{a})$ if their classes map to each other under the [[connecting homomorphism]] $\delta$:

$$
  \delta : [\mu] \mapsto [\omega]
  \,.
$$


**Example.** In the case where $\mathfrak{g}$ is an ordinary semisimple [[Lie algebra]], this reduces to the ordinary study of ordinary Chern-Simons 3-forms associated with $\mathfrak{g}$-valued 1-forms. This is described in the section [On semisimple Lie algebras](#SemisimpLie).

### Chern-Simons and curvature characteristic forms

For $\mathfrak{g}$ a [[∞-Lie algebra|Lie n-alghebra]], let $\mathbf{B}G := \mathbf{cosk}_{n+1} \exp(\mathfrak{g})$ be the [[∞-Lie group]] obtained by [[Lie integration]] from it.

For $X$ a [[paracompact space|paracompact]] [[smooth manifold]] with [[good open cover]] $\{U_i \to X\}$ whose [[Cech nerve]] we write $C(U)$, a [[cocycle]] for a $G$-[[principal ∞-bundle]] on $X$ is cocycle with coefficients in the simplicial sheaf

$$
  \mathbf{B}G = 
  \mathbf{cosk}_{n+1}((U,[k]) \mapsto \{ 
     C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
     \leftarrow
     CE(\mathfrak{g})
  \})
  \,.
$$


We say an $\infty$-connection on this is an extension to a cocycle with coefficients in the simplicial sheaf

$$
  \mathbf{B}G_{diff} = 
  \mathbf{cosk}_{n+1}((U,[k]) \mapsto \left\{ 
    \array{
       C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
       &\leftarrow&
       CE(\mathfrak{g})
       &&& underlying \; cocycle
       \\
       \uparrow && \uparrow
       \\
       \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^k)
       &\stackrel{}{\leftarrow}&
       W(\mathfrak{g})
       &&&
       connection
     }
  \right\}
  \,.
$$

The diagrams on the left encode those $\mathfrak{g}$-valued forms on $U \times \Delta^k$ whose [[curvature]] vanishes on $\Delta^k$. One can show that one can always find a _genuine_ $\infty$-connection: one for which the curvatures have no leg along $\Delta^k$, in that they land in $\Omega^\bullet(U) \otimes C^\infty(\Delta^k)$. For tose the above diagram extends to

$$
  \array{
     C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
     &\leftarrow&
     CE(\mathfrak{g})
     &&& underlying \; cocycle
     \\
     \uparrow && \uparrow
     \\
     \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^k)
     &\stackrel{}{\leftarrow}&
     W(\mathfrak{g})
     &&&
     connection
     \\
     \uparrow && \uparrow
     \\
     \Omega^\bullet(U) \otimes C^\infty(\Delta^k)
     &\leftarrow&
     inv(\mathfrak{g})
     &&&
     curvature
   }
$$ 

By [[pasting]]-postcomposition with the above diagrams for an invariant polynomial we obtain connections with values in $b^n \mathbb{R}$

$$
  \array{
     C^\infty(U)\otimes \Omega^\bullet(\Delta^k)
     &\leftarrow&
     CE(\mathfrak{g})
     &\stackrel{\mu}{\leftarrow}&
     CE(b^{n-1}\mathbb{R})
     &&& underlying \; cocycle
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U)\otimes \Omega^\bullet(\Delta^k)
     &\stackrel{}{\leftarrow}&
     W(\mathfrak{g})
     &\stackrel{(cs,\langle- \rangle)}{\leftarrow}&
     W(b^{n-1}\mathbb{R})
     &&&
     Chern-Simons forms
     \\
     \uparrow && \uparrow && \uparrow
     \\
     \Omega^\bullet(U) \otimes C^\infty(\Delta^k)
     &\leftarrow&
     inv(\mathfrak{g})
     &\stackrel{\langle -\rangle}{\leftarrow}&
     CE(b^n \mathbb{R})
     &&&
     curvature\;characteristic\;form
   }
  \,,
$$ 

where in the bottom row we have the [[curvature characteristic forms]] $\langle F_\nabla\rangle$ coresponding to the connection, and in the middle the corresponding [[Chern-Simons forms]].

More details for the moment at [[schreiber:differential cohomology in an (∞,1)-topos -- examples]].


## Examples

### On Lie algebras 

For $\mathfrak{a} = \mathfrak{g}$ an ordinary [[Lie algebra]], the above reproduces the ordinary definition of invariant polynomials on Lie algebras.

For instance for $\mathfrak{g}$ a semisimple Lie algebra with Killing form $P = \langle -,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$, this form regarded as a element (of degree 4) in $\mathfrak{g}[1]^* \wedge \mathfrak{g}[1]^*$ is an invariant polynomial:

* the fact that it is an element in $\wedge^2 \mathfrak{g}[1]^*$ is precisely the fact that $\langle -,-\rangle$ is bilinear and symmetric;

* the fact that it is closed under $d_{W(\mathfrak{g})}$ is precisely the statement that it is invariant.

### On semisimple Lie algebras {#SemisimpLie}

See [[Killing form]].

### On tangent Lie algebroids

For $X$ a [[smooth manifold]], and invariant polynomial on the [[tangent Lie algebroid]] $\mathfrak{a} = T X$ is precisely a closed [[differential form]] on $X$.





[[!redirects algebra of invariant polynomials]]
[[!redirects dg-algebra of invariant polynomials]]