
#Contents#
* automatic table of contents goes here
{:toc}

## Idea

The **Chern character** of a [[generalized (Eilenberg-Steenrod) cohomology]] theory is a canonical morphism from the generalized cohomology to ordinary ([[Eilenberg-MacLane spectrum|Eilenberg Mac-Lane]]) real cohomology. When thought of in the refinement to [[differential cohomology]] and thinking of a cocycle in differential cohomology as a generalization of a [[connection on a bundle]], the Chern-character is the map that sends a generalized connection to its [[curvature]] characteristic classes.


More in detail, for every [[generalized (Eilenberg-Steenrod) cohomology]] theory given by a [[spectrum]] $E$, there is a canonical [[natural isomorphism]] from the rationalized $E$-cohomology to ordinary (Eilenberg-MacLane) cohomology with coefficients in the rationalized [[homotopy group]]s of $E$:

$$
  H(-,E)\otimes \mathbb{R}
  \;\;
  \stackrel{\simeq}{\to}
  \;\;
  H(-,(\pi_* E)\otimes \mathbb{R})
  \,.
$$

So rationally, every generalized (Eilenberg-Steenrod) cohomology is ordinary (Eilenberg-MacLane) cohomology. Hence every generalized (ES-)cohomology theory has a canonical morphism to ordinary real cohomology

$$
  ch
  :
  H(-,E) 
  \;\;
  \to 
  \;\;
  H(-,E)\otimes \mathbb{R} 
  \;\;
  \stackrel{\simeq}{\to} 
  \;\;
  H(-,\pi_* E \otimes \mathbb{R})
  \,.
$$

In the case that $E = KU$ is the [[K-theory]] spectrum, this morphism is classically known as the **Chern character**. Generalizing from this example, the term "Chern character" is sometimes used also for the general case.


## For vector bundles and K-theory {#KTheory}

The classical theory of the Chern character applies to the [[spectrum]] of complex [[K-theory]], $E = KU$.

In that case a cocycle $H^0(X,KU)$ may be represented by a complex [[vector bundle]], and the image of this cocycle under the Chern-character is the class in even-graded real cohomology that is represented (under the [[deRham theorem]] isomorphism of deRham cohomology with real cohomology) by the even graded closed [[differential form]]


$$
 ch(\nabla) := \sum_{j \in \mathbb{N}}
   k_j
   tr( F_\nabla \wedge \cdots \wedge F_\nabla)
  \;\;
  \in \Omega^{2 \bullet}(X)
  \,,
$$

where

* $\nabla$ is any chosen [[connection on a bundle|connection]] on the vector bundle;

* $F = F_\nabla \in \Omega^2(X,End(V))$ is the [[curvature]] of this connection;

* $k_j \in \mathbb{R}$ are normalization constants, $k_j = \frac{1}{j!} \left( \frac{1}{2\pi i}\right)^j$.

## General theory

### The fundamental cocycle

The [[isomorphism]]

$$
  H(-,E)\otimes \mathbb{R}
  \;\;
  \stackrel{\simeq}{\to}
  \;\;
  H(-,(\pi_* E)\otimes \mathbb{R})
$$

that defines the Chern-character map is induced by a canonical cocycle on the [[spectrum]] $E$ that is called the **fundamental cocycle**.

This is described for instance in section [4.8, page 47](http://arxiv.org/PS_cache/math/pdf/0211/0211216v2.pdf#page=47) of

* [[Mike Hopkins]], I. Singer, [[Quadratic Functions in Geometry, Topology,and M-Theory]] ([arXiv](http://arxiv.org/abs/math.AT/0211216))