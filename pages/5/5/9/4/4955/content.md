
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

## Statement

The **chain rule** is the statement that [[differentiation]] $d : Diff \to Diff$  is a [[functor]] on [[Diff]]:

given two [[smooth function]]s between [[smooth manifold]]s $f : X \to Y$ and $g : Y \to Z$ we have

$$
  d(g \circ f) : 
  T X 
  \stackrel{d f}{\to}
  T Y 
  \stackrel{d g}{\to}
  T Z
  \,.
$$

If one thinks of a [[tangent vector]] $v \in T_x X$ to be an equivalence class of a smooth path $\gamma_v : [-1,1] \to X$ with $\gamma(0) = x$, then the chain rule is the [[associativity]] of the composite

$$
  [-1,1] \stackrel{\gamma_v}{\to} X \stackrel{f}{\to} Y \stackrel{g}{\to} Z
  \,.
$$

Bracketed as $(g \circ f)\circ \gamma_v$ this represents $d(g \circ f)(v)$. Bracketed as $g \circ (f \circ \gamma_v)$ is represents $d g (d f (v))$.

Alternatively, in a context of [[synthetic differential geometry]] where with $D$ being the [[infinitesimal space|infinitesimal interval]] we may _identify_ $v$ with $v : D \to X$, the chain rule is the associativity of

$$
  D \stackrel{v}{\to} X \stackrel{f}{\to} Y \stackrel{g}{\to} Z
  \,.
$$


## Examples

Let $X = Y = Z = \mathbb{R}$ the [[real line]]. Then the [[tangent bundle]] $T X$ is canonically identified with $\mathbb{R} \times \mathbb{R}$.

Given two functions, $f, g : \mathbb{R} \to \mathbb{R}$ their derivatives are traditionally regarded again as functions $f', g' : \mathbb{R} \to \mathbb{R}$, though strictly speaking we are to think of them as the maps

$$
  d f, d g : \mathbb{R} \times \mathbb{R} = T \mathbb{R}  \to T \mathbb{R}  = \mathbb{R} \times \mathbb{R}
$$

given by

$$
  d f : (x,v) \mapsto (f(x), v f'(x))
$$

and

$$
  d g : (x,v) \mapsto (g(x), v g'(x))
  \,.
$$

The composite

$$
  f (g \circ f) : \mathbb{R} \times \mathbb{R} = 
  T \mathbb{R} \to T \mathbb{R} = \mathbb{R} \times \mathbb{R}
$$

is therefore the map

$$
  d(g \circ f) : (x,v) \mapsto (f(x), v f'(x)) 
   \mapsto 
     (g(f(x)), v f'(x) g'(f(x)))
  \,.
$$

Therefore we have

$$
  (g \circ f)'(x) = f'(x) g'(f(x))
  \,.
$$

This is the form in which the chain rule is taught to kids. It's just a test to see if they understand what's really going on. One of these tests that are never being graded.

[[!redirects chain law]]