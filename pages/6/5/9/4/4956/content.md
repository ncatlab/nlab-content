
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The _differentiation_ of a [[function]] $f : X \to Y$ is the process that assigns to each point $x \in X$ _differences_ $f(y) - f(x)$ between the value $f(x)$ of the function at that point, and its value at all [[infinitesimal space|infinitesimally]] nearby points $y$. This collection of information is called the _[[derivative]]_ $d f$ of the function. 



 

## Definition

_Differentiation_ is the [[functor]] $d : Diff \to Diff$ on the [[category]] [[Diff]] of [[smooth manifold]]s that sends

* a manifold $X$ to its [[tangent bundle]] $T X$;

* a [[smooth function]] $f : X \to Y$ to its differential $d f : T X \to T Y$:

  if $\gamma : [-1,1] \to X$ is a path in $X$ representing a vector $v \in T_x X$, then $(d f)(v) \in T_{f(x)} Y$ is the vector represented by the path
  $[-1,1] \stackrel{\gamma}{\to} X \stackrel{f}{\to} Y$. 

In a context $H$ of [[synthetic differential geometry]] the functor $d$ is simply the [[internal hom]] out of the [[infinitesimal space|infinitesimal interval]] $D$

$$
  d = [D, -] : H \to H
  \,.
$$

## Properties

From the above definition the fact that differentiation is indeed functorial is immediate. This functoriality statement is known in the literature as the [[chain rule]] for differentiation.


## Exposition of differentiation via infintiesimals

We attempt to give an exposition of how to think of differentiation not via taking limits in the sense of [[analysis]], but by working with [[infinitsimal space]]s, as in [[synthetic differential geometry]].

### Setup

For that purpose we regard objects such as the [[real line]] $\mathbb{R}$ and more generally any [[smooth manifold]] as being objects of a [[Models for Smooth Infinitesimal Analysis|well adapted]] [[smooth topos]] of [[smooth space]]s. But in fact much less will do for most of the discussion: for the basic theory it is sufficient to work in the canonical [[site]] of such a topos: the category $SmoothLoc$ of [[smooth loci]]. This in turn is defined to be the [[opposite category]]

$$
  SmoothLoc := SmoothAlg^{op}
$$

of the category of [[smooth algebra]]s.

Apart from the real line $\mathbb{R} \om SmoothLoc$ itself, the main object of interest for discussing basics of differentiation is the first order [[infinitesimal space|infinitesimal line segment]]

$$
  D \subset \mathbb{R} 
  \,.
$$

This is the collection of points in $\mathbb{R}$, that square to zero under the canonical multiplicative structure of $\mathbb{R}$

$$
  D = \{\epsilon \in \mathbb{R} | \epsilon^2 = 0\}
  \,.
$$

Of course when interpreted in the usual context of [[Set]] this is just $\{0\}$, but here we are to interpret it in the ambient [[smooth topos]], or equivalently just in our [[site]] $SmoothLoc$ for it: so this means that $D$ is the [[pullback]]

$$
  \array{
    D &\to& *
    \\
    \downarrow && \downarrow^{\mathrlap{0}}
    \\
    \mathbb{R} &\stackrel{(-)^2}{\to}& \mathbb{R}
  }
$$

in $SmoothLoc$. By definition of $SmoothLoc$ as the [[opposite category]] of [[smooth algebra]]s this is dually the [[pushout]]

$$
  \array{
     C^\infty(D) &\leftarrow& C^\infty(*) \simeq \mathbb{R}
     \\
     \uparrow && \uparrow^{\mathrlap{f \mapsto f(0)}}
     \\
     C^\infty(\mathbb{R}) 
      &\stackrel{x \mapsto x^2}{\leftarrow}& 
     C^\infty(\mathbb{R})
  }
$$

of [[smooth algebra]]s. Here in the bottom and on the right we have the ordinary smoth algebras of [[smooth function]]s on the [[smooth manifold]]s $\mathbb{R}^1 = \mathbb{R}$ and $\mathbb{R}^0 = *$, whereas $C^\infty(D)$ is new notation, suggestive and justified, for whatever the algebra of functions on the object $D$ is, where $D$ is _defined_ by the fact that it has this algebra of functions. The bottom morphism is that which sends a smoth function $f : \mathbb{R} \to \mathbb{R}$ to the function $f((-)^2) : \mathb{R} \to \mathbb{R}$. If we write $x = Id : \mathbb{R} \to \mathbb{R}$ for the canonical [[coordinate]] function, then this sends $x$ to the function $x^2$.  

Notice that the commutativity of the pushout diagram means that the image of the squared coordinate function $x^2 \in C^\infty(\mathbb{R})$ in $C^\infty(D)$ is zero, because the former is the image under the bottom morphism of the coordinate function $x$ and that maps under the right vertical morphism to $0 \in C^\infty(*) \simeq \mathbb{R}$.

In fact one shows that the [[pushout]] $C^\infty(D)$ is _generated_ by the coordinate function $x \in C^\infty(R)$ subject to the relation $x^2 = 0$: it is the [[ring of dual numbers]]

$$
  \begin{aligned}
    C^\infty(D) & \simeq C^\infty(X)/(x^2) 
    \\
    & \simeq \mathbb{R}[x]/(x^2)
  \end{aligned}
  \,.
$$

(Here in the second step we have used [[Hadamard's lemma]].)

This expresses the intuitive idea that $D$ is such a small neighbourhood of $0$ in $\mathbb{R}$ that while the canonical coordinate function of $\mathbb{R}$ restricted to $D$ is non-vanishing (it would vanish only when restricted entirely to the point 0) it is "so small that its square is always 0". Readers who like this intuitive statement should keep it in mind, as it is accurate and useful, whereas readers who don't like it should stick with the above abstract definition.


### Functions and differential 1-forms


[[!redirects derivative]] 