
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Higher linear algebra
+-- {: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

On a [[complex]] [[vector space]] $V$ a _sesquilinear map_ is a [[function]] of two arguments 

$$
  \langle -,-\rangle
  \;\colon\; 
  V \times V
  \longrightarrow
  \mathbb{C}
$$

which is a [[linear function]] in one argument (say the second) and complex anti-linear in the other.

\begin{defn}\label{Definity}

A sesquilinear form $\langle -,-\rangle$ is called

$$
  \left.
  \array{
    \text{positive definite} &if& \langle v^\ast,v \rangle \gt 0
    \\
    \text{negative definite} &if& \langle v^\ast,v \rangle \lt 0
    \\
    \text{positive semi-definite} &if& \langle v^\ast,v \rangle \geq 0
    \\
    \text{negative semi-definite} &if& \langle v^\ast,v \rangle \leq 0
  }
  \right\rbrace
  \;\;
  \text{for all}\; v \neq 0
  \,.
$$

Finally, it is called *indefinite* if it is neither positive nor negative semi-definite.
\end{defn}


More generally:

Let $A$ be a [[star algebra]]. Then every left $A$-[[module]] $\rho_l \colon A \otimes V \longrightarrow V$ canonically becomes a right module $\rho_r \colon V \otimes A \longrightarrow A$ by setting

$$
  \rho_r(v,a) \coloneqq a^\ast v
$$

and vice versa. 

With this operation understood to turn a left module $V$ into a right module, then a sesquilinear form on $V$ is simply an element in the [[tensor product of modules]]

$$
  V^\ast \otimes_A V^\ast
$$

of the $A$-linear dual $V^\ast$ of $V$ with itself. 


## Related concepts

* [[bilinear form]], [[quadratic form]]

* [[symplectic form]], [[Kähler form]], [[Hermitian form]]


## References

See also:

* [[Brian Osserman]], _A primer on sesquilinear forms_ ([[OssermanSesquilinearForms.pdf:file]])

* Wikipedia, _[Sesquilinear form](https://en.wikipedia.org/wiki/Sesquilinear_form)_


[[!redirects sesquilinear maps]]
[[!redirects sesquilinear function]]
[[!redirects sesquilinear functions]]

[[!redirects sesquilinear forms]]

[[!redirects sesquilinear map]]

