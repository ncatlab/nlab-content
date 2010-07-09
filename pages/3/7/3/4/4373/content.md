
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

An embedding is, generally, a [[morphism]] which in some sense is an [[isomorphism]] onto its [[image]]

For this to make sense in a given [[category]] $C$, we not only need a good notion of image.  Note that it is not enough to have the image of $f\colon X \to Y$ as a [[subobject]] $\im f$ of $Y$; we also need to be able to interpret $f$ as a morphism from $X$ to $\im f$, because it is this morphism that we asking to be an isomorphism.


## In the presence of some finite limits and colimits

### Definition

+-- {: .query}

[[Urs Schreiber]]: here a suggestion:

=--

Let $C$ be a [[category]] with finite [[limit]]s and [[colimit]]s, or at least such that the following  [[pushout]] and [[equalizer]] exist. 

Then we have for a [[morphism]] $f : X \to Y$ in $C$ the definition of its [image as an equalizer](http://ncatlab.org/nlab/show/image#AsEqualizer):

$$
  im f := \lim_\leftarrow ( Y \stackrel{\to}{\to} Y \coprod_X Y) 
$$ 

and in particular a factorization of $f$ as

$$
  f : X \stackrel{\tilde f}{\to} im f \hookrightarrow Y
  \,,
$$

where the morphism on the right is a [[monomorphism]].

We say that $f$ is an **embedding** if $\tilde f$ is an [[isomorphism]]. This implies in particular that $f$ is a [[monomorphism]]. It says equivalently that $f$ is an [[effective monomorphism]].

### Examples

In [[Set]] the embeddings in this sense are precisely the [[monomorphism]]s.

In [[Diff]] not all finite limits exist. But if $f : X \to Y$ is an [[embedding of manifolds]], then the above equalizer exists and $f$ is an embedding in the above sense.


[[!redirects embedding]]
[[!redirects embeddings]]
[[!redirects imbedding]]
[[!redirects imbeddings]]
