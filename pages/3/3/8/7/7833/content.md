
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

Let $f \colon R \to S$ be a [[homomorphism]] of [[algebra|algebraic]] objects such as [[rings]]. Let $\cdot_S$ be an [[action]] of $S$ on a [[module]] $M$, then 

$$
  r\cdot_R m \coloneqq f( r )\cdot_S m
$$ 

defines an action of $R$ on $M$. This construction extends to a  [[functor]] 
$$
  f^\ast \colon SMod \longrightarrow RMod
$$
between [[categories of modules]], sending $\cdot_S$ to $\cdot_R$. This is called *restriction of scalars* (along $f$).

This functor has a [[left adjoint functor]] 

$$
  f_! \; \coloneqq\;
  S \otimes_R (-)
  \;\colon\; 
  RMod
   \longrightarrow 
  SMod
$$
 
called *[[extension of scalars]]*, since for an $R$-module $M$ and an $R$-module $S$ we have that $M\otimes_R S$ is a well defined [[tensor product of modules|tensor product]] of $R$ modules which becomes an $S$ module by the operation of $S$ on itself in the second factor of the tensor. We have an [[adjoint functors|adjunction]] $f_! \dashv f^*)$.

Not only is restriction of scalars a right adjoint, it is also a [[monadic functor]].  This can be shown using the [[monadicity theorem]] or by direct computation.

Furthermore, not only is restriction of scalars a right adjoint, it is also a left adjoint.  That is, it has a right adjoint of its own, called [[coextension of scalars]]:

$$
  f_* \; \coloneqq\;
  RMod(S, -)
  \;\colon\; 
  RMod
   \longrightarrow 
  SMod
$$


## Related concepts

* [[extension of scalars]] $\dashv$ **restriction of scalars** $\dashv$ [[coextension of scalars]]

* [[restriction (double category theory)]]

