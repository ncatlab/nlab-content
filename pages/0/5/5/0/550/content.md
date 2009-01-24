A co-span in a category $V$ is a diagram

$$
 \array{
   && S
   \\
   & \nearrow && \nwarrow
   \\
   a &&&& b
 }
$$
in $V$, i.e. a [[span]] in the [[opposite category]] $V^{op}$.

Co-spans in a category $V$ with small co-limits form a [[bicategory]] whose objects are the objects of $V$, whose morphisms are co-spans between two objects, and whose 2-morphisms $\eta$ are commuting diagrams of the form

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

The category of co-spans from $a$ to $b$ is naturally a [[enriched category|category enriched in]] $V$: for

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

formed in analogy to the enriched hom of [[pointed object]]s.

If $V$ has a terminal object, $pt$, then co-spans from $pt$ to itself are [[bi-pointed object]]s in $V$.

#Related concepts#

* [[co-span co-trace]]

* [[multi-cospan]]


#References#

Topological cospans and their role as models for [[cobordism]]s are discussed in

* Marco Grandis, _Collared cospans, cohomotopy and TQFT (Cospans in algebraic topology, II)_ ([pdf](http://www.dima.unige.it/~grandis/wCub2.pdf))