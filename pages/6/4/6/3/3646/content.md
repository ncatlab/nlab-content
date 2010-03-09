Let $(C,d)$ be a nonnegative [[cochain complex]] of [[vector space]]s over a [[field]] of (total) finite dimension $dim C = \sum_{p=0}^\infty dim C^p \lt \infty$ and $f = (f^p)_{p\geq 0} :(C,d)\to (C,d)$ an endomorphism of cochain complexes. 

The **algebraic Lefschetz formula** is the statement

$$
\sum_{p\geq 0} (-1)^p tr (f^p :C^p\to C^p) = \sum_{p\geq 0} (-1)^p tr (H^p(f):H^p(C)\to H^p(C)).
$$

Its special case for $f = id$ is the **Euler-Poincar&#233; formula**

$$
\sum_{p\geq 0} (-1)^p dim C^p = \sum_{p\geq 0} (-1)^p dim H^p(C).
$$