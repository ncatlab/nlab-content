

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Given a [[curve]] in $n$-[[dimension|dimensional]] [[Euclidean space]] $E^n$, with a $C^{n+1}$-[[differentiable function|differentiable]] parametrization by the [[arc length]] from a given point on the curve 

$$ 
  \array{
    F &\colon& I & \longrightarrow & E^n
    \\
    && s &\mapsto& F(s)
  }
$$

(hence a [[naturally parametrized curve]] of smoothness class $C^{n+1}$), __Frenet-Serret formulas__ express the [[derivatives]] with respect to the [[arc length]] of the Frenet moving frame vectors as a [[linear combination]] of the Frenet moving frame vectors, where the coefficients form an antisymmetric matrix whose nonzero coefficients are (up to sign) the curvature of the curve, its torsion and their higher analogues. 

This works under the assumption that the [[derivatives]]

$$ 
  F^{(k)}(s) 
    \;=\; 
  d^k F/d s^k 
    \;\in\; 
  T^k_{F(s)} E^n
    \;\cong\;
  \mathbf{R}^n,
  \,\,\,\,\,
  k = 1,\ldots,n
$$ 

are [[linear independence|linearly independent]] at each point (using the canonical identification with $\mathbf{R}^n$ with any of its [[tangent spaces]]). 

The [[Gram-Schmidt orthogonalization]] procedure then transforms the [[n-tuple]] $(F^{(1)}(s),\ldots,F^{(n)}(s))$ into an [[orthogonality|orthogonal]] $n$-frame $(V_1(s),\ldots,V_n(s))$ called the __Frenet $n$-frame__. 

Writing down the $n$-tuple of the derivatives with respect to $s$ of the Frenet frame in a $C^0(\mathbf{R})$-basis formed by the Frenet frame reveals an antisymmetric matrix of coefficients over $C^0(\mathbf{R})$. Its nonzero coefficients are, up to a sign, the _curvature_ of the curve, the _torsion_ and their higher analogues. 

In dimension $n=3$, the Frenet frame vectors are called the _tangent_, _normal_ and _binormal_ unit vectors of the curve. In dimension 4 the 4th vector is called the _trinormal_ unit vector. The plane spanned by the tangent and normal unit vectors is called the _osculating plane_ at $F(s)$.

## References

* [[Herman Gluck]], _Higher curvatures of curves in Euclidean space_, The American Mathematical Monthly, 73:7 (1966) 699-704, [doi](https://doi.org/10.1080/00029890.1966.11970818) 

See also:

* en.wikipedia/[Frenet-Serret_formulas](https://en.wikipedia.org/wiki/Frenet%E2%80%93Serret_formulas)


