#Definition#

Let $C$ be an [[abelian category]] and let
$$
  V^\bullet = ( \cdots  \to V_{n+1} \stackrel{\partial_n}{\to}
  V_n \stackrel{\partial_{n-1}}{\to}
  V_{n-1} \to \cdots
  )
$$
be a [[chain complex]] in $C$. For each interger $n \in \mathbb{N}$ this induces the following diagram

$$
  \array{
    && im \delta_n &&\to&& ker \delta_{n-1}
    \\
    & \nearrow && \searrow && \swarrow
    \\
    V_{n+1}
    &&\stackrel{\partial_n}{\to}&&
    V_n
    &&\stackrel{\partial_{n-1}}{\to}&&
    V_{n-1}
    \\
    & &&
    \swarrow && \searrow && \nearrow
    \\
    && coker \delta_n &&\stackrel{}{\to}&&
    im \delta_{n-1}
  }
$$

the **homology** $H_n(V)$ of $V$ in degree $n$ is the object

$$
  \begin{aligned}
    im(ker \delta_{n-1} \to  V_n \to coker \delta) 
    & \simeq
    coker(im \delta_n \to ker \delta_{n-1})
    \\
    & \simeq
    coker(V_{n+1} \to ker \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to im \delta_{n-1})
    \\
    & \simeq
    ker(coker \delta_n \to V_{\delta_{n-1}})
  \end{aligned}
$$

#Remarks#

* If $H^n(V) \simeq 0$ then one says that the complex $V$ is [[exact]] in degree $n$.