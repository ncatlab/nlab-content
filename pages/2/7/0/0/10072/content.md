

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Complex geometry
+--{: .hide}
[[!include complex geometry - contents]]
=--
#### Spin geometry
+-- {: .hide}
[[!include higher spin geometry - contents]]
=--
#### Index theory
+-- {: .hide}
[[!include index theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

On a [[Kähler manifold]] $(X,\omega)$ with a choice of [[spin structure]] given by a [[Theta characteristic]] $\sqrt{\Omega^{0,n}}$, the sum of the [[Dolbeault operator]] $\overline{\partial}$ with its adjoint $\overline{\partial}^\ast$ are identified with the corresponding [[Dirac operator]]

$$
  \overline{\partial}
  + 
  \overline{\partial}^\ast
  \;\colon\;
  S_X\simeq \Omega^{0,\bullet}_X \otimes \sqrt{\Omega^{0,n}}
  \to 
  \Omega^{0,\bullet}_X \otimes \sqrt{\Omega^{0,n}}
  \simeq
  S_X
  \,.
$$

Here the action of $\overline{\partial} + \overline{\partial}^\ast$ on $\Omega^{0,\bullet}$ is the canonical one. For the action on $\sqrt{\Omega^{n,0}}$ choose any [[line bundle with connection|connection]] $\nabla$ on this line bundle. Then on a local [[coordinate patch]] the action is given by differentiating along a coordinate vector, multiplying with the corresponding Clifford element and projecting on the antiholomorphic part, then summing this over all coordinate vectors (e.g. [Friedrich 97, p. 79](#Friedrich97)).

## Properties

### Index and genus

The [[index]] is the [[Todd genus]] (see there).

## Related concepts

* [[Kähler-Dirac operator]]

* [[spin^c Dirac operator]]

## References

Textbook accounts include

section 3.4 (specifically around p. 79) of 

* [[Thomas Friedrich]], _Dirac operators in Riemannian geometry_, Graduate studies in mathematics 25, AMS (1997)
 {#Friedrich97}


[[!redirects Dirac-Dolbeault operator]]
