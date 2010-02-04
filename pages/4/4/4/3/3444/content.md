
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The [[category]] of all [[representation]]s of some type.

If we think, fully generally, of a representation of $C$ on $D$ as nothing but a [[functor]] $C \to D$, then the representation category is just the [[functor category]] $Rep(C,D) = Func(C,D)$.

Notably when $G$ is a [[group]], an ordinary linear representation is a [[functor]] $\mathbf{B}G \to Vect$ from the [[delooping]] [[groupoid]] of $G$ to [[Vect]], and so the representation category is

$$
  Rep(G) = Func(\mathbf{B}G,Vect)
  \,.
$$

## Properties

### Tannakian reconstruction

Representation categories come with [[forgetful functor]]s that send a representation to the underlying object that carries the representation.

For instance for group representations the canonical inclusion ${*} \to \mathbf{B}G$ induces the functor $Func(\mathbf{B}G,Vect) \to Func(*,Vect)$, hence

$$
  F : Rep(G) \to Vect
$$

that sends a representation to its underlying [[vector space]]. The [[Tannakian reconstruction theorem]] says that the group $G$ may be recovered essentially as the group of [[automorphism]]s of the fiber functor $F$.


[[!redirects representation category]]