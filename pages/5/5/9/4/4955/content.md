
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
  d f : (x,v) \mapsto (g(x), v g'(x))
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