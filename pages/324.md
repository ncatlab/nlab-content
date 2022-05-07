
# Contents
* automatic table of contents goes here
{: toc}

## Definition

In any [[category]], a **cospan** is a diagram like this:
$$
  \array{
     && a &&&& b
      \\
      & 
      && {}_{f}\searrow
       &
       & \swarrow_g
      && 
     \\     
     &&&&
     c
     &&&&
  }
$$


A cospan in the category $C$ is the same as a [[span]] in the [[opposite category]] $C^{op}$.  So, all general facts about cospans in $C$ are general facts about spans in $C^{op}$, and the reader may turn to the entry on [[span|spans]] to learn more.

A cospan that admits a [[cone]] is called a [[quadrable cospan]].

Cospans in a category $V$ with small colimits form a [[bicategory]] whose objects are the objects of $V$, whose morphisms are cospans between two objects, and whose 2-morphisms $\eta$ are commuting diagrams of the form

$$
  \array{
    && S
    \\
    & {}^{\sigma_{S}}\nearrow && \nwarrow^{\tau_S}
    \\
    a &&\downarrow^\eta&& b
    \\
    & {}_{\sigma_T}\searrow
    && \swarrow_{\tau_T}
    \\
    && T
  }
  \,.
$$

The category of cospans from $a$ to $b$ is naturally a [[enriched category|category enriched in]] $V$: for

$$
  \array{
    && S
    \\
    & {}^{\sigma_{S}}\nearrow && \nwarrow^{\tau_S}
    \\
    a &&&& b
    \\
    & {}_{\sigma_T}\searrow
    && \swarrow_{\tau_T}
    \\
    && T
  }
$$

two parallel cospans in $V$, the $V$-object 
${}_a[S,T]_b$
of morphisms between them is the pullback

$$
  \array{
    {}_a[S,T]_b
     &\to&
     pt
    \\
    \downarrow && \downarrow^{\sigma_T \times \tau_T}
    \\
    [S,T] &\stackrel{\sigma_S^* \times \sigma_T^*}{\to}& 
    [a \sqcup b, T]
  }
$$

formed in analogy to the enriched hom of [[pointed object]]s. The [[initial object]] of $V$ is the [[coproduct]] of $a$ and $b$.

If $V$ has a terminal object, $pt$, then cospans from $pt$ to itself are [[bi-pointed object]]s in $V$.

##Related concepts

* [[cospan cotrace]]
* [[multi-cospan]]
* [[Cospans in Algebraic Topology]]
* [[multispan]]
* the [cograph of a function](http://ncatlab.org/nlab/show/graph+of+a+function#cograph)
* the [[cograph of a functor]]


##References

Topological cospans and their role as models for [[cobordism]]s are discussed in

* Marco Grandis, _Collared cospans, cohomotopy and TQFT (Cospans in algebraic topology, II)_ ([pdf](http://www.dima.unige.it/~grandis/wCub2.pdf))




[[!redirects cospan]]
[[!redirects cospans]]
[[!redirects opspan]]
[[!redirects opspans]]
[[!redirects co-span]]
[[!redirects co-spans]]
