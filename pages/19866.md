There are three operators associated to $\Pi$-types: $\Pi,\lambda,App$.

* $\Pi$ is of sort $ty$, has two arguments of sort $ty$, and one binder that scopes over the second argument.  Thus, if $A$, $B$ are raw types and $x$ is a fresh variable, then $\Pi(x:A).B$ is a raw type, where $x$ is bound in $B$.
* $\lambda$ is of sort $tm$, has two arguments of sort $ty$ and one of sort $tm$, and one binder that scopes over the second and third arguments.  Thus, if $A,B$ are raw types, $M$ is a raw term and $x$ is a fresh variable, then $\lambda(x:A.B). M$ is a raw term, where $x$ is bound in $B$ and $M$.
* $App$ is of sort $tm$, has two arguments of sort $ty$ and two of sort $tm$, and one binder that scopes over the second type argument.  Thus, if $A$, $B$ are raw types, $M,N$ are raw terms and $x$ is a fresh variable, then $App^{x:A.B}(M,N)$ is a raw term, where $x$ is bound in $B$ only.
