
#Contents#
* automatic table of contents goes here
{:toc}


## In terms of synthetic differential geometry

A perspective on differential equations from the [[nPOV]] of [[synthetic differential geometry]] is given in 

* [[Bill Lawvere]], _Toposes of laws of motion_ , transcript of a talk in Montreal, Sept. 1997 ([pdf](http://www.acsu.buffalo.edu/~wlawvere/ToposMotion.pdf))

  (on the description of [[differential equation]]s in terms of synthetic differential geometry)

See also the appendix of

* _Outline of synthetic differential geometry_ , seminar notes (1998) ([pdf](http://www.acsu.buffalo.edu/~wlawvere/SDG_Outline.pdf))

### First order homogeneous ODEs as extension problems in a smooth topos

In a [[smooth topos]] with $X$ any $A$ any two objects and $D = \{x \in R | x^2 = 0\}$ the abstract tangent vector, a diagram, of the form

$$
  \array{
    {*}&\to& D &\stackrel{v}{\to}& X
    \\
    &{}_{\mathllap{v(f)(x)}}\searrow& {}^{\mathllap{v(f)}}\downarrow & \swarrow_{\mathrlap{f}}
    \\
    && A
  }
$$

may be read as

* $f$ is a smooth function on $X$ with values in $A$;

* whose derivative along the [[tangent vector]] $v \in T_x X \subset T X = X^D$...

* ...is the tangent vector $v(f) \in T_{f(x)} A \subset T A = A^D$.

Accordingly, the diagram 

$$
  \array{
    D &\stackrel{v}{\to}& X
    \\
    {}_{\mathllap{\alpha}}\downarrow    
    \\
    A
  }
$$

may be read as encoding the differential equation $v(f)_x = \alpha$ (at one point) whose solutions $f \in A^X$ are the extensions that complete this diagram.

To get differential equations in the more common sense that they impose a condition on the derivative of $f$ at each single point of $X$ and varying smoothly with $X$, we think of  $f : X \to A$ in terms of the [[exponential object|exponential map]]

$$
  f^X : X^X \to A^X
$$

and consider

$$
  \array{
    &&{*}
    \\
    && \downarrow & \searrow^{\mathrlap{Id_X}}
    \\
    {*}&\to& D &\stackrel{v}{\to}& X^X
    \\
    &{}_{\mathllap{f}}\searrow&{}^{\mathllap{\alpha}}\downarrow & \swarrow_{\mathrlap{f^X}}
    \\
    &&A^X
  }
  \,.
$$

In this diagram now

* $v : D \to X^X$ is the [[adjunct]] of a [[vector field]] $X \to T X = X^D$ on $X$;

  (the commutativity of the top  right triangle ensures that indeed this $X \to T X$ is a [[section]] of the [[tangent bundle]] projection $T X \to X$);

* $\alpha : D \to A^X$ is the [[adjunct]] of a map $X \to T A = A^D$ that sends each point $x \in X$ to a tangent vector in $T_{f(x)} A$ 

  (enforced by the commutativity of the left bottom triangle)

* and the commutativity of the right lower triangle is the **differential equation**

  $$
    v(f) = \alpha
    \,.
  $$

