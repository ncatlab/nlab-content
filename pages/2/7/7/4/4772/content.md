
#Contents#
* table of contents
{:toc}

## Idea

An _adjoint action_ is an [[action]] by _conjugation_ .

## Definition

### Of a group on itself

The _adjoint action_ of a [[group]] $G$ on itself is the [[action]] $Ad : G \times G \to G$ given by

$$
  Ad : (g,h) \mapsto g^{-1} \cdot h \cdot g
  \,.
$$

### Of a Lie group on its Lie algebra

The adjoint action $ad : G \times \mathfrak{g} \to \mathfrak{g}$ of a [[Lie group]] $G$ on its [[Lie algebra]] $\mathfrak{g}$ is for each $g \in G$ the [[derivative]] $d Ad(g) : T_e G \to T_e G$ of this action in the second argument at the neutral element of $G$

$$
  ad : (g,x) \mapsto Ad(g)_*(x)
  \,.
$$

This is often written as $ad(g)(x) = g^{-1} x g$ even though for a general Lie group the expression on the right is not the product of three factors in any way.  But for a [[matrix Lie group]] $G$ it is: in this case both $g$ as well as $x$ are canonically identified with [[matrices]] and the expression on the right is the product of these matrices.

[[!redirects adjoint actions]]