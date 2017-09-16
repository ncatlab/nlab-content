#Definition#

A presheaf on a category $S$ with values in a category $C$ is nothing but a functor 
$$
  S^{op} \to C
$$
from the [[opposite category]] $S^{op}$ to $C$.

#Remarks#

* One usually addresses such functors as presheaves instead of just as functors

  * when one is interested in the [[Yoneda embedding]] of a category $C$ into its presheaf category $[C^{op}, Set]$ for purposes of studying for instance [[limit]]s, [[colimit]]s, [[ind-object]]s, [[pro-object]]s of $C$;

  * or when there is the structure of a [[site]] on $S$, such that it makes sense to ask if a given presheaf is actually a [[sheaf]].

* One generally useful way to think of presheaves is in the sense of [[space and quantity]].

* In the case where $C = Set$ and $S$ is [[small category|small]], an important general principle is that the category of presheaves on $S$ and [[natural transformation|natural transformations]] between them is the [[free cocompletion]] of $S$. 


#Properties of presheaves#


Every presheaf is a [[colimit]] of a [[representable functor]].

An elegant way to express this for any preaheaf $F : C^{op} \to Set$ is as the [[end|coend]] identity
$$
  F(-) = \int^{c \in C} F(c) \times hom_C(-,c)
$$
using [[Yoneda reduction]].

Another way to express the same is as follows: let $Y : C \to [C^{op}, Set]$ be the [[Yoneda embedding]] and let $C_F$ be the corresponding [[comma category]]
$$
  C_F := 
  \left\lbrace
     \array{
        Y(V) &&\stackrel{Y(f)}{\to}&& Y(V')
        \\
        & {}_f\searrow && \swarrow_{f'}
        \\
        && F
     }
  \right\rbrace 
$$
and let $p : C_F \to C$ the canonical functor. Then
$$
   F(-) \simeq colim_{(Y(V) \to F) \in C_F} (Y\circ p)
  \,.
$$
To see this notice that for every $B \in [C^{op}, Set]$
and using the property of the Hom we have
$$
 \begin{aligned}
  Hom_{[C^{op}, Set]}(colim_{(Y(V) \to F) \in C_F} (Y\circ p),B)
  &\simeq
  lim_{(Y(V) \to F) \in C_F} Hom_{[C^{op}, Set]}(Y(V),B)
  \\
  & \simeq
  lim_{(Y(V) \to F) \in C_F} B(V)
 \end{aligned}
$$
by the [[Yoneda lemma]]. But the last term is
seen by inspection to be equivalent to
$$
  \cdots \simeq Hom_{[C^{op}, Set]}(F,G)
  \,.
$$
Since this holds for all $B$, the claim follows, again using [[Yoneda lemma|Yoneda]].
