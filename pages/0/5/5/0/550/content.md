A co-span in a category $V$ is a [[span]] in the [[opposite category]] $V^{op}$.

#Closed monoidal structures (?)#

Regarding the notion of co-span as a generalization of that of [[pointed object]] leads to some obvious generalizations of the properties of categories of pointed objects.


For $V$ a [[closed monoidal category]] 
with finite limits
the catgeory
of co-spans in $V$ between two fixed objects $a, b \in V$
is naturally enriched over $V$: for

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
  \,.
$$

Thinking of a cospan as defining a (generalised) *bi*-pointed object, this is the direct generalization of the the notion of enriched hom of [[pointed object]]s.


(... to be continued ...)