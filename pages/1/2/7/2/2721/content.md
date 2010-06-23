
> under construction

<div class="rightHandSide toc">
[[!include infinity-Lie theory - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}


## Idea


For every [[Lie algebra]] or [[L-infinity algebra|∞-Lie algebra]] or [[Lie ∞-algebroid|∞-Lie algebroid]] $\mathfrak{a}$ there is its [[Chevalley-Eilenberg algebra]] $CE(\mathfrak{a})$ and its [[Weil algebra]] $W(\mathfrak{a})$ and a [[dg-algebra]] morphism

$$
  CE(\mathfrak{a}) \leftarrow W(\mathfrak{a})
  \,.
$$ 

An invariant polynomial on $\mathfrak{a}$ is a closed element in $W(\mathfrak{a})$ that is invariant under those isomorphisms of the identitys on $W(\mathfrak{g})$ that cover an isomorphism of the identity on $CE(\mathfrak{g})$.

The [[dg-algebra]] $inv(\mathfrak{a})$ of **invariant polynomials** on $\mathfrak{a}$ sits in the [[kernel]] of this map

$$
  CE(\mathfrak{a}) \leftarrow W(\mathfrak{a})
  \leftarrow
  inv(\mathfrak{a})
  \,.
$$ 


## Definition

### Concrete definition

For $\mathfrak{a}$ an [[Lie ∞-algebroid|∞-Lie algebroid]] (of finite type, i.e. degreewise finite dimensional) with [[Chevalley-Eilenberg algebra]] 

$$
  CE(\mathfrak{g}) = (\wedge^\bullet \mathfrak{a}^*, d_{CE(\mathfrak{a}}))
$$ 

and [[Weil algebra]] 

$$
  W(\mathfrak{a}) = (\wedge^\bullet (\mathfrak{a}^* \oplus \mathfrak{a}^*[1]), d_{W(\mathfrak{a})})
$$

an **invariant polynomial** on $\mathfrak{a}$ is an elements $P \in W(\mathfrak{a})$ with the property that

* $P$ is a wedge product of generators in the shifted copy of 
  $\mathfrak{a}^*$ $W(\mathfrak{a})$, i.e.

  $$
    P \in \wedge^\bullet \mathfrak{a}^*[1]
  $$

* it is closed in $W(\mathfrak{a})$ in that $d_{W(\mathfrak{a})} P = 0$.


### Conceptual definition


We give an equivalent but more conceptual [[nPOV]] definition of invariant polynomials.

#### Preliminaries

Write $T \mathfrak{a}$ for the tangent $\infty$-Lie algebroid of $\mathfrak{a}$, characterized by the fact that this is the $\infty$-Lie algebroid whose Chevalley-Eilenbeg algebra is the Weil algebra of $\mathfrak{a}$,

$$
  CE(T \mathfrak{a}) = W(\mathfrak{a})
  \,.
$$

Write $i_{\mathfrak{a}} : \mathfrak{a} \to T \mathfrak{a}$ for the canonical inclusion, which dually corresponds to the projection

$$
  CE(\mathfrak{a}) \leftarrow W(\mathfrak{a}) : i_{\mathfrak{a}}^*
  \,.
$$

For $n \in \mathbb{N}$, write $b^n \mathbb{R} = Lie (\mathbf{B}\mathbb{R})$ for the $\infty$-Lie algebroid whose CE-algebra is given by a single generator $c$ in degree $n$ with vanishing differential

$$
  CE(b^n \mathbb{R}) = (\wedge^\bullet \langle c\rangle, d = 0)
  \,.
$$

Its tangent $\infty$-Lie algebroid $T b^n \mathbb{R}$ is given by the CE-algebra

$$
  CE(T b^n \mathbb{R}) = 
  W(b^n \mathbb{R})
  =
  (\wedge^\bullet \langle c, d c\rangle)
  \,.
$$


#### The invariance condition

A closed differential form on $\mathfrak{a}$ is precisely a commuting diagram

$$
  \array{
    \mathfrak{a} &\to& *
    \\
    \downarrow && \downarrow
    \\
    T \mathfrak{a} &\to& b^n \mathbb{R}
  }
$$

of $\infty$-Lie algebroids, namely a commuting diagram

$$
  \array{
    CE(\mathfrak{a}) &\leftarrow& \mathbb{R}
    \\
    \uparrow^{\mathrlap{i^*}} && \uparrow
    \\
    W(\mathfrak{a}) &\stackrel{P}{\leftarrow}& CE(b^n \mathbb{R})
  }
$$

of [[dg-algebra]]s: this says precisely that $P$ is a closed element of degree $n$ in $W(\mathfrak{a})$ that vanishes under $i^*$.

We claim now that the fact that $P$ not just vanishes under $i^*$ but satisfies the above condition that it sits entirely in the shifted copy of generators is equivalent to the following diagrammatic statement: 

for every diagram

...


## Properties

### Transgression cocycles {#TransgressionCocycles}

We describe how to an [[nLab:∞-Lie algebroid]] invariant polynomial $\omega$ we associate an [[∞-Lie algebroid]] cocycle $\nu$ that is _in transgression with_ $\omega$.

The [[dg-algebra]] of invariant polynomials is a sub-dg-alghebra of the kernel of the morphism $i^* : W(\mathfrak{a}) \to CE(\mathfrak{a})$ from the [[Weil algebra]] to the [[Chevalley-Eilenberg algebra]] of $\mathfrak{a}$

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

We say that $\mu \in CE(\mathfrak{a})$ is in transgression with $\omega \in inv(\mathfrak{a}) \subset CE(\Sigma \mathfrak{a})$ if their classes map to each other under the connecting homomorphism $\delta$:

$$
  \delta : [\mu] \mapsto [\omega]
  \,.
$$


1. We first regard the invariant polynomial $\omega$ as an element of the [[Weil algebra]] $W(\mathfrak{a})$ under the inclusion $inv(\mathfrak{a}) \hookrightarrow W(\mathfrak{a})$, where, by the very definiton of invariant polynomials, it is closed: $d_{W(\mathfrak{a})} \omega = 0$.

1. then we find an element $cs_\omega \in W(\mathfrak{a})$ with the property that $d_{W(\mathfrak{a})} cs_\omega = \omega$. This is guranteed to exist because $W(\mathfrak{a})$ has trivial cohomology.

1. then we send this element $cs_\omega\in W(\mathfrak{a})$ along the restriction map $W(\mathfrak{a}) \to CS(\mathfrak{a})$ to an elemeent we call $\nu$.

The procedure is illustarted by the following diagram

$$
  \array{
    0 && \omega &\leftarrow & \omega
    \\
    \;\;\uparrow^{\mathrlap{d_{CE(\mathfrak{a})}}}
    &&
    \;\;\uparrow^{\mathrlap{d_{W(\mathfrak{a})}}}
    \\
    \nu &\leftarrow& cs(\omega)
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

From the fact that all morphisms involved respect the differential and from the fact that the image of $\omega$ in $CE(\mathfrak{a})$ vanishes it follows that 

* this element $\nu$ satisfies $d_{CE(\mathfrak{a})} \nu = 0$, hence that it is an $\infty$-Lie algebroid cocycle.

* any two different choices of $cs_\omega$ lead to cocylces $\mu$ that are cohomologous.

We say $\nu$ is a cocycle _in transgression with_ $\omega$. 
We may call $cs_{\omega}$ here a _Chern-Simons element_ of $\omega$. Because for $A : T X \to T \mathfrak{a}$ any collection of [[schreiber:∞-Lie algebroid valued differential forms]] coming dually from a dg-morphism $\Omega^\bullet(X) \leftarrow W(\mathfrak{a}) : A$ the image $\omega(A)$ of $\omega$ will be a curvature characteristic form and the image $cs_\omega(A)$ its corresponding Chern-Simons form. 

In the case where $\mathfrak{g}$ is an ordinary semisimple [[Lie algebra]], this reduces to the ordinary study of ordinary Chern-Simons 3-forms associated with $\mathfrak{g}$-valued 1-forms. This is described in the section [On semisimple Lie algebras](#SemisimpLie)



## Examples

### On Lie algebras 

For $\mathfrak{a} = \mathfrak{g}$ an ordinary [[Lie algebra]], the above reproduces the ordinary definition of invariant polynomials on Lie algebras.

For instance for $\mathfrak{g}$ a semisimple Lie algebra with Killing form $P = \langle -,-\rangle : \mathfrak{g} \otimes \mathfrak{g} \to \mathbb{R}$, this form regarded as a element (of degree 4) in $\mathfrak{g}[1]^* \wedge \mathfrak{g}[1]^*$ is an invariant polynomial:

* the fact that it is an element in $\wedge^2 \mathfrak{g}[1]^*$ is precisely the fact that $\langle -,-\rangle$ is bilinear and symmetric;

* the fact that it is closed under $d_{W(\mathfrak{g})}$ is precisely the statement that it is invariant.

### On semisimple Lie algebras {#SemisimpLie}

...

### On tangent Lie algebroids

For $X$ a [[smooth manifold]], and invariant polynomial on the [[tangent Lie algebroid]] $\mathfrak{a} = T X$ is precisely a closed [[differential form]] on $X$.





[[!redirects algebra of invariant polynomials]]
[[!redirects dg-algebra of invariant polynomials]]