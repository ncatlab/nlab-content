The **slice category** or **over category** $\mathbf{C}/c$ of a [[category]] $\mathbf{C}$ over an object $c \in \mathbf{C}$ has 
* objects that are all arrows $f \in \mathbf{C}$ such that $cod(f) = c$, and
* morphisms $g: X \to X' \in \mathbf{C}$ from $f:X \to c$ to $f': X' \to c$ such that $f' \circ g = f$.

$$
  C/c
  =
  \left\lbrace
    \array{
       X &&\stackrel{g}{\to}&& X'
       \\
       & {}_f \searrow && \swarrow_{f'}
       \\   
       && c
    }
  \right\rbrace
$$


The slice category is a special case of a [[comma category]].

# Examples #

* If $\mathbf{C} = \mathbf{P}$ is a [[partial order|poset]] and $p \in \mathbf{P}$, then the slice category $\mathbf{P}/p$ is the "principal ideal" $\downarrow (p)$ of elements $q \in \mathbf{P}$ with $q \leq p$. 

* If $1$ is a [[terminal object]] in $\mathbf{C}$, then $\mathbf{C}/1$ is isomorphic to $\mathbf{C}$.

# See also #
* [[over quasi-category]]


[[!redirects slice category]]