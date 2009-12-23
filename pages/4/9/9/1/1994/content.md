
#Contents#
* automatic table of contents goes here
{:toc}

## Definition

Given [[crossed modules]] $\mathbb{X}=(\partial_X : X_1\to X_0)$, $\mathbb{Y}=(\partial_Y:Y_1\to Y_0)$ (actions surpressed from the notation), a __crossed profunctor__ 

$$
  \mathbb{X}\to\mathbb{Y}
$$ 

consists of a group $P$ and morphisms $x_1:X_1\to P$, $x_0:P\to X_0$, $y_1:Y_1\to P$, $y_0:P\to Y_0$ 

$$
  \array{
    X_1 &&&& Y_1
    \\
    & \searrow^{\mathrlap{x_1}} & & {}^{\mathllap{y_1}}\swarrow
    \\
    {}^{\mathllap{\partial_X}}\downarrow && P && 
    \downarrow^{\mathrlap{\partial_Y}}
    \\
    & \swarrow_{\mathrlap{x_0}} && {}_{\mathllap{y_0}}\searrow
    \\
    X_0 &&&& Y_0
  }
$$


such that 

* the two triangles commute, $x_0\circ x_1=\partial_X$, $y_0\circ y_1=\partial_Y$, 

* the diagonals compose to identites
  $y_0\circ x_1 = 1$, $x_0\circ y_1 = 1$, 
 
* and

  $$
    x_1 ({}^{x_0(p)}x) = p x_1(x) p^{-1}, 
    \,\,\,\,\,y_1   ({}^{y_0(p)}y = py_1(y)p^{-1}
    \,,
  $$

  where $x\in X_1$, $p\in P$, $y\in Y_1$. 

The complex $Y_1\to P\to X_0$ is called the NE-SW complex, and $X_1\to P\to Y_0$ is called the NW-SE complex.

## Related concepts

If to the above definition added the property that the SE-NW sequence $Y_1\to P\to X_0$ is _exact_ in that it is a (nonabelian in general) [[group extension]], this is called a [[butterfly]]. See there for more details.

## References

This notion appeared in

* M. Jibladze, _Coefficients for cohomology of "large" categories_ , pp. 169--179, in H. Inassaridze (Ed.), K-theory and Homological Algebra (A Seminar held at the Razmadze Mathematical Institute in Tbilisi, Georgia, USSR 1987-88), Lec. Notes in Math. 1437, Springer 1990 (*[[jibladzeCoeffLargeCats.djvu:file]]*).

