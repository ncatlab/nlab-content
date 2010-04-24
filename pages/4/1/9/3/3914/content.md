
<div class="rightHandSide toc">
[[!include cohomology - contents]]
</div>


#Contents#
* automatic table of contents goes here
{:toc}

## Definition

For $H$ a [[multiplicative cohomology theory]], and $V \to X$ a [[vector bundle]] of rank $n$, an $H$-**orientation** of $V$ is an element $u \in H^n(Th(V))$ in the cohomology of the [[Thom space]] of $V$ with the property that its restriction $i^* u$ along $i : S^n \to Th(V)$ to any fiber of $Th(V)$ is 

$$
  i^* u = \epsilon \cdot \gamma_n 
  \,,
$$

where

* $\epsilon \in H^0(S^0)$ is a multiplicatively invertible element;

* $\gamma_n \in H^n(S^n)$ is the image of the multiplicative unit
  under the [[suspension isomorphism]] $H^0(S^0) \stackrel{\simeq}{\to}H^n(S^n)$.   

Multiplication with $u$ induces hence an [[isomorphism]]

$$
  (-)\cdot u : H^\bullet(X) \stackrel{\simeq}{\to} H^{\bullet + n}(Th(V))
  \,.
$$

This is called the [[Thom isomorphism]].

## References

* [[eom]], _[Orientation](http://eom.springer.de/o/o070200.htm)_