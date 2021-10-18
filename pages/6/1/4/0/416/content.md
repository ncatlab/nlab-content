
> This entry is about the [[formal dual]] to [[tensoring]] in the generality of [[category theory]]. For the different concept of _[[cotensor product]]_ of [[comodules]] see there.

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Enriched category theory
+--{: .hide}
[[!include enriched category theory contents]]
=--
#### Limits and colimits
+--{: .hide}
[[!include infinity-limits - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}

## Idea

In a [[closed monoidal category|closed]] [[symmetric monoidal category]] $V$ the [[internal hom]] $[-,-] : V^{op} \times V \to V$ satisfies the [[natural isomorphism]]

$$
  [v_1,[v_2,v_3]] \simeq [v_2,[v_1,v_3]]
$$

for all [[object]]s $v_i \in V$ ([prop.](closed+monoidal+category#TensorHomIsoInternalizes)). If we regard $V$ as a $V$-[[enriched category]] we write $V(v_1,v_2) := [v_1,v_2]$ and this reads

$$
  V(v_1,V(v_2,v_3)) \simeq V(v_2,V(v_1,v_3))
  \,.
$$

If we now pass more generally to any $V$-[[enriched category]] $C$ then we still have the enriched [[hom object]] functor $C(-,-) : C^{op} \times C \to V$. One says that $C$ is _powered_ over $V$ if it is in addition equipped also with a mixed operation $\pitchfork : V^{op} \times C \to C$ such that $\pitchfork(v,c)$ behaves as if it were a hom of the object $v \in V$ into the object $c \in C$ in that it satisfies the natural isomorphism

$$
  C(c_1,\pitchfork(v,c_2)) \simeq V(v,C(c_1,c_2))
  \,.
$$

## Definition 

+-- {: .un_defn}
###### Definition

Let $V$ be a [[closed monoidal category|closed]] [[monoidal category]].  In a $V$-[[enriched category]] $C$, the **power** of an object $y\in C$ by an object $v\in V$ is an object $\pitchfork(v,y) \in C$ with a [[natural isomorphism]]

$$
  C(x, \pitchfork(v,y)) \cong V(v, C(x,y))
$$

where $C(-,-)$ is the $V$-valued hom of $C$ and $V(-,-)$ is the [[internal hom]] of $V$.


We say that $C$ is **powered** or **cotensored** over $V$ if all such power objects exist.


=--

+-- {: .un_remark}
###### Remark

Powers are frequently called _cotensors_ and a $V$-category having all powers is called _cotensored_, while the word "power" is reserved for the case $V=$ [[Set]].  However, there seems to be no good reason for making this distinction.  Moreover, the word "tensor" is fairly overused, and unfortunate since a tensor (= a [[copower]]) is a [[colimit]], while a cotensor (= power) is a [[limit]].

=--

## Properties

* Powers are a special sort of [[weighted limit]]s.  Conversely, all weighted limits can be constructed from powers together with [[conical limit]]s.  The dual colimit notion of a power is a [[copower]].


## Examples

### In 1-category theory

* $V$ itself is always powered over itself, with $\pitchfork(v_1,v_2) := [v_1,v_2]$.

* Every [[locally small category]] $C$ ($V = (Set,\times)$ ) with all [[product]]s  is powered over [[Set]]: the powering operation

  $$
    \pitchfork(S,c) := \prod_{s\in S} c
  $$

  of an object $c$ by a set $S$ forms the $|S|$-fold [[cartesian product]] of $c$ with itself, where $|S|$ is the [[cardinality]] of $S$. 

  The defining natural isomorphism

  $$
    Hom_C(c_1,\pitchfork(S,c_2))\simeq Hom_{Set}(S,Hom_C(c_1,c_2))
  $$

  is effectively the definition of the product (see [[limit]]).

### In $\infty$-topos theory

We discuss how the powering of [[(infinity,1)-toposes]] is given by forming [[mapping stacks]] out of [[locally constant (infinity,1)-stacks|locally constant $\infty$-stacks]]. All of the following formulas and their proos hold verbatim also for [[Grothendieck toposes]], as they just use general abstract properties.

\linebreak

Let $\mathbf{H}$ be an [[(infinity,1)-topos|$\infty$-topos]] with terminal [[(infinity,1)-geometric morphism|geometric morphism]] denoted


$$
  \mathbf{H}
  \underoverset
    {\underset{\Gamma}{\longrightarrow}}
    {\overset{LConst}{\longleftarrow}}
    {\;\;\;\;\bot\;\;\;\;}
  Grp_\infty
  \,,
$$

where the [[inverse image]] construcs [[locally constant infinity-stacks|locally constant $\infty$-stacks]],

and with its [[internal hom]] ([[mapping stack]]) [[adjoint (infinity,1)-functor|adjunction]] denoted

$$
  \mathbf{H}
    \underoverset
      {\underset{Maps(X,-)}{\longrightarrow}}  
      { \overset{ (-) \times X }{\longleftarrow} }
      {\;\;\;\; \bot \;\;\;\;}
  \mathbf{H}
$$

for $X \,\in\, \mathbf{H}$. Notice that this construction is also [[(infinity,1)-functor|$\infty$-functorial]] in the first argument: 
$Maps\big( X \xrightarrow{f} Y ,\, A \big)$ is the morphism which under the [[(infinity,1)-Yoneda lemma|$\infty$-Yoneda lemma]] over $\mathbf{H}$ (which is large but locally small, so that the lemma does apply)  corresponds to

$$
  \mathbf{H}
  \big(
    (-)
    ,\,
    Maps(X,A)
  \big)
  \;\simeq\;
  \mathbf{H}
  \big(
    (-) \times X
    ,\,
    A
  \big)
  \xrightarrow{
    \mathbf{H}
    \big(
      (-) \times f
      ,\,
      A
    \big)   
  }
  \mathbf{H}
  \big(
    (-) \times Y
    ,\,
    A
  \big)
  \;\simeq\;
  \mathbf{H}
  \big(
    (-)
    ,\,
    Maps(X,A)
  \big)
  \,.
$$

\begin{proposition}
The *powering* of $\mathbf{H}$ over [[Infinity-Grpd|$Grpd_\infty$]] is given by the [[mapping stack]] out of the [[locally constant infinity-stack|locally constant $\infty$-stacks]]:

$$
  \array{
    Grpd_\infty^{op}
    \times
    \mathbf{H}
    &
    \overset{ LConst^{op} \times \mathrm{id} }{\longrightarrow}
    &
    \mathbf{H}^{op}
    \times 
    \mathbf{H}
    &
    \overset{Maps(-,-)}{\longrightarrow}
    &
    \mathbf{H}
  }
$$
in that this operation has the following properties

1. For all $X,\,A \,\in\, \mathbf{H}$ and $S \,\in\, Grpd_\infty$ we have a [[natural equivalence]]

   $$
     \mathbf{H}
     \Big(
       X
       ,\,
       Maps
       \big(
         LConst(S)
         ,\,
         A
       \big)
     \Big)
     \;\;
     \simeq
     \;\;
     Grpd_\infty
     \Big(
       S
       ,\,
       \mathbf{H}
       \big(
         X
         ,\,
         A
       \big)
     \Big)
   $$

1. In its first argument the operation 

   1. sends the [[terminal object]] (the [[point]]) to the identity:

      $$
        Maps
        \big(
          LConst(\ast)
          ,\,
          X
        \big)
        \;\;
        \simeq
        \;\;
         X
      $$

   1. sends [[(infinity,1)-colimits|$\infty$-colimits]] to [[(infinity,1)-limits]]:

      $$
        Maps
        \Big(
          \underset{
            \longrightarrow
          }{\lim}
          \,
          LConst\big(S_\bullet\big)
          ,\,
          X
        \Big)
        \;\;
        \simeq
        \;\;
        \underset{
          \longleftarrow
        }{\lim}
        \,
        Maps
        \Big(
          LConst\big(S_\bullet\big)
          ,\,
          X
        \Big)
      $$

\end{proposition}

(...)

## Related concepts

* [[tensored and cotensored category]]

* [[copower]], [[(∞,1)-copower]]

* [[pullback-power]]


## References

* [[Max Kelly]], section 3.7 of _Basic concepts of enriched category theory_ ([tac](http://www.tac.mta.ca/tac/reprints/articles/10/tr10abs.html) ,[pdf](http://www.tac.mta.ca/tac/reprints/articles/10/tr10.pdf))

* {#Borceux94} [[Francis Borceux]], Vol 2, Section 6.5 of _[[Handbook of Categorical Algebra]]_, Cambridge University Press (1994)


[[!redirects cotensor]]
[[!redirects cotensoring]]

[[!redirects powers]]
[[!redirects cotensors]]
[[!redirects cotensored category]]

[[!redirects powering]]