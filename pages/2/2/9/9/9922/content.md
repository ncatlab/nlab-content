
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Representation theory
+-- {: .hide}
[[!include representation theory - contents]]
=--
#### Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The [[representation]]/[[action]] of a [[Lie algebra]] $\mathfrak{g}$ on a [[vector space]] $V$.

## Definition

A _Lie algebra representation_ is a Lie algebra [[homomorphism]] $\rho \;\colon\;\mathfrak{g} \to end(V)$ to the [[endomorphism Lie algebra]] of $V$.

This means equivalently that

$$
  \array{
    \mathfrak{g} 
      \otimes 
    V 
    & \overset{\rho}{\longrightarrow} & 
    V
    \\
    (x,v) &\mapsto& \rho_x(v)
  }
$$

is a [[bilinear map]] such that for all $x_i \in \mathfrak{g}$ and $v \in V$ we have the [[Lie action property]]:

\[
  \label{LieActionProperty}
  \rho_{x_1}(\rho_{x_2}(v))
  -
  \rho_{x_2}(\rho_{x_1}(v))
  \;=\;
  \rho_{[x_1,x_2]}(v)
\]

## Properties

### In terms of string diagrams / Jacobi diagrams
 {#InTermsOfStringDiagrams}

In [[string diagram]]-notation for [[Lie algebra objects]] [[internalization|internal]] to [[tensor categories]], the [[Lie action property]] (eq:LieActionProperty) looks as follows:

<center>
<img src="https://ncatlab.org/nlab/files/LieActionPropertyAsSTURelation.jpg" width="500">
</center>

$$
  \begin{aligned}
    \Leftrightarrow
    &
    \;\;\;\;\;
    \rho(f(x,y),z) \;=\; \rho(y,\rho(x,z)) - \rho(x,\rho(y,z))
    \\
    \underset{
      {f = [-,-]}
      \atop
      {Lie\;bracket}
    }{
      \Leftrightarrow
    }
    &
    \;\;\;\;\;
    \underset{
       {Lie\;action\;property}
    }{
    \underbrace{
      \rho([x,y],z) \;=\; \rho(y,\rho(x,z)) - \rho(x,\rho(y,z))
    }
    }
    \\
    \underset{
      {\rho = -[-,-]}
      \atop
      {adjoint\;action}
    }{
      \Leftrightarrow
    }
    &
    \;\;\;\;\;
    \underset{
       {Jacobi\;identity}
    }{
    \underbrace{
      [[x,y],z] \;=\; - [y,[x,z]] + [x,[y,z]]
    }
    }
  \end{aligned}
$$

Here the last line shows the equivalence to the [[Jacobi identity]] on the [[Lie algebra object]] itself in the case that the Lie action is the [[adjoint action]].

In the language of [[Jacobi diagrams]] this is called the _[[STU-relation]]_, and is the reason behind the existence of [[Lie algebra weight systems]] in [[knot theory]].



## Related concepts

* [[embedding tensor]]

* [[Casimir invariant]]

* [[Lie algebra cohomology]]

* [[group action]]

* [[Lie infinity-algebroid representation]]

## References

See also 

* Wikipedia, _[Lie algebra representation](https://en.wikipedia.org/wiki/Lie_algebra_representation)_


[[!redirects Lie algebra representations]]

[[!redirects Lie algebra action]]
[[!redirects Lie algebra actions]]

[[!redirects Lie module]]
[[!redirects Lie modules]]

[[!redirects Lie action]]
[[!redirects Lie actions]]
[[!redirects Lie action property]]
[[!redirects Lie action properties]]

[[!redirects Lie algebra module]]
[[!redirects Lie algebra modules]]

