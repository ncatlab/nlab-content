

> under construction

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Physics
+--{: .hide}
[[!include physicscontents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Kaluza-Klein mechanism_ is the observation that pure [[gravity]] on a product [[spacetime]] $X \times F$ with fixed [[metric]] $g_F$ on $F$ looks on $X$ like gravity coupled to [[Yang-Mills theory]] for [[gauge group]] $G$ the [[Lie group]] of [[isometries]] of $(F,g_F)$.

More precisely, the [[Einstein-Hilbert action]] functional

$$
  g_{X \times F}
   \mapsto \int_{X \times F} R(g_{X \times F}) dvol(g_{X \times F})
$$

is equivalently rewritten as

$$
  g_{X \times F}
  =
    \left(
    \array{
      g_F & A
      \\
      A & g_X
    }
  \right)
  \mapsto S_{EH}(g_X) + S_{YM}(A) + S_{mod}(g_F)
  \,,
$$

where the first terms is the EH action of $g_X$ on $X$, the second terms is the action functional of [[Yang-Mills theory]] for the [[connection on a bundle|connection]] $A$.


## References

Section V.3.3., page 1186, volume 2 of

* [[Leonardo Castellani]], [[Riccardo D'Auria]], [[Pietro Fre]], _[[Supergravity and Superstrings - A Geometric Perspective]]_
{#CastellaniDAuriaFre}
