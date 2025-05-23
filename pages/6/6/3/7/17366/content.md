
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The incarnation of  [[internal homs]]/[[mapping spaces]] in the context of [[pointed objects]].


## Definition

+-- {: .num_defn #PointedMappingSpace}
###### Definition

Let $\mathcal{C}$ be a [[closed monoidal category]] with [[finite limits]].

For $X, Y \in \mathcal{C}^{\ast}$ two pointed objects in $\mathcal{C}$, their **pointed mapping space** 

$$
  [X,Y]_*
  \in
  \mathcal{C}^{\ast/}
$$

(the "object of basepoint-preserving maps"), is the [[pullback]]

$$
  \array{ 
    [X,Y]_* & \overset{}{\longrightarrow} & \ast
    \\
    \downarrow &(pb)& \downarrow
    \\
    [X,Y] & \underset{}{\longrightarrow} & [1,Y]
   }
$$

where the morphism $[X,Y]\to [1,Y]$ is induced from the point $\ast\to X$, and the morphism $\ast\to [\ast,Y]$ is the [[adjunct]] to $\ast \otimes \ast \to \ast \to Y$.  

Regard $[X,Y]_*$ as a pointed object with basepoint induced by the map $\ast\to [X,Y]$ whose [[adjunct]] is $\ast \otimes X \to \ast \to Y$.  

=--

## Properties

+-- {: .num_prop #SmashProductLeftAdjointToPointedMappingSpace}
###### Proposition

Let $\mathcal{C}$ be a [[closed monoidal category]] with [[finite limits]] and with [[finite colimits]].

For every pointed object $X \in \mathcal{C}^{\ast}$ the operation of forming the pointed [[mapping space]] out of $X$, and the operation of forming the [[smash product#GeneralSmashProduct|smash product]] with $X$, form a pair of [[adjoint functors]]

$$
  (
  X \wedge (-)
  \;\dashv\;
  [X,-]_\ast
  )
  \;\colon\;
  \mathcal{C}^{\ast/}
  \leftrightarrow
  \mathcal{C}^{\ast/}
  \,.
$$

This makes $\mathcal{C}^{\ast/}$ itself a [[closed monoidal category]], which is [[symmetric monoidal category|symmetric]] if $\mathcal{C}$ is.  The [[tensor unit]] is $I_+$ for $I$ the unit for the monoidal structure on $\mathcal{C}$.  

=--

([Elmendorf-Mandell 07, lemma 4.20](#ElmendorfMandell07))

+-- {: .num_remark}
###### Remark

The case when $\mathcal{C}$ is [[cartesian monoidal category|cartesian]], or at least [[semicartesian monoidal category|semicartesian]], is most common in the literature.

=--

+-- {: .num_remark}
###### Remark

If $\mathcal{C}$ is [[monoidal category|monoidal]] but not [[closed monoidal category|closed]], the same definition of the [[smash product#ForGeneralPointedObjects|smash product]] makes $\mathcal{C}^{\ast/}$ [[monoidal category|monoidal]] as long as the tensor product of $\mathcal{C}$ preserves finite colimits in each variable separately.  

If not, the smash product can fail to be associative. For instance, the smash product on the ordinary category [[Top]] (without any [[nice category of spaces|niceness conditions]] imposed) is not associative.

=--

[[!redirects pointed mapping spaces]]
