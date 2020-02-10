
$$
  \begin{aligned}
    &
    (\sigma_1,\sigma_2)
    \mapsto 
    exp(-t d(\sigma_1,\sigma_2))
    \;\;
    \text{is conditionally positive kernel}
    \\
    \\
    \overset{??}{\Leftrightarrow}
    \;\;\;\;
     &
    \frac{1}{n!} 
    \sum_{\sigma \in Sym(n)} 
    exp\big(
      t \cdot cycles(\sigma)
    \big)
    \;\le\; 
    \left(1+\frac{1}{n!}\right) e^{t n}
  \end{aligned}
$$


$\ldots$

Let $n \in \mathbb{N}$, $n \geq 2$.
On the complex linear span $\mathbb{C}[Sym(n)]$ of the set of permutations on $n$ elements, consider the sesqui-linear form

\[
 \label{SesquilinearForm}
  \array{
    \mathbb{C}[Sym(n)]
    \times
    \mathbb{C}[Sym(n)]
    &
    \overset{
      \langle
        -,-
      \rangle 
    }{\longrightarrow}
    &
    \mathbb{C}
    \\
    (
    a_1 \cdot \sigma_1
    ,\;
    a_2 \cdot \sigma_2
    )
    &\mapsto&
    a_1 a_2^\ast
    \, 
    2^{ (\#\!cycles(\sigma_1 \circ \sigma_2^{-1})) }
  }
\]

\linebreak

**Question:** _Is (eq:SesquilinearForm) positive semi-definite?_


\linebreak

**Non-Answer:** This here is not a counter-example:

Consider

* $\sigma_3$ the cyclic shift by 1

* $\sigma_1$ the cyclic shift by 2

* $\sigma_2$ the cyclic shift by -2 (i.e. in the other direction)

Then if $n = 3 \cdot 4 \cdot k$ is divisible by 12, we have

* $\#\!cycles (\sigma_1 \circ \sigma_3^{-1}) = \#\!cycles(\text{cyclic shift by 1}) = 1$ 

* $\#\!cycles (\sigma_1 \circ \sigma_2^{-1}) = \#\!cycles(\text{cyclic shift by 4}) = 4$ 

* $\#\!cycles (\sigma_2 \circ \sigma_3^{-1}) = \#\!cycles(\text{cyclic shift by 3}) = 3$ 

and hence

$$
  \begin{aligned}
    & \left\vert \sigma_1 - \sigma_2 + \sigma_3 \right\vert^2
    \\
    & = 
    \left\vert \sigma_1 \right\vert^2
    +
    \left\vert \sigma_2 \right\vert^2
    +
    \left\vert \sigma_3 \right\vert^2
    - 
    2 \langle \sigma_1, \sigma_2\rangle
    - 
    2 \langle \sigma_2, \sigma_3\rangle
    + 
    2 \langle \sigma_1, \sigma_3\rangle
    \\
    & = 
    3 \cdot 2^n
    -2 \cdot 2^{4}
    - 2 \cdot 2^{3}
    + 2 \cdot 2^1
  \end{aligned}
$$



