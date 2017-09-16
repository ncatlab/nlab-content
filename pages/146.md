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

Any category of presheaves is [[complete category|complete]] and [[cocomplete category|cocomplete]], with both [[limit|limits]] and [[colimit|colimits]] being computed _pointwise_.  That is, to compute the limit or colimit of a diagram $F : D \to Set^{C^op}$, we think of it as a functor $F: D \times C^{op} \times Set$ and take the limit or colimit in the $D$ variable.

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

#Discussion about 'free cocompletion'#

This section is a slightly new sort of experiment.
Here [[John Baez]] would like to explain this remark to [[Mike Stay]]:

"In the case where $C = Set$ and $S$ is [[small category|small]], an important general principle is that the category of presheaves on $S$ and [[natural transformation|natural transformations]] between them is the [[free cocompletion]] of $S$."

The idea is that I'll write some stuff, then Mike will write some questions, and so on.  Other people are welcome to join but only if they _keep it simple_.  Please: _no showing off!_  In particular, Mike does not yet understand coends or Kan extensions, so part of my job is to explain these, not just use them.

First, let me state the above result precisely.

Given a small category $A$, let $\hat{A}$ be our short name for $Set^{A^{op}}$, the category of presheaves on $A$ and natural transformations between them.

The [[Yoneda lemma]] gives an embedding $Y : A \to \hat{A}$.

The result says: given any [[cocomplete category]] $B$, and any functor $F : A \to B$, there is a [[cocontinuous functor]] $\widehat{F} : \hat{A} \to B$ making this triangle commute up to natural isomorphism:

$$
  \array{
     A &\stackrel{F}{\to}& B
     \\
     F\downarrow & \nearrow_{\widehat{F}}
     \\
     \widehat{A}
  }
  \,,
$$

Moreover, $\widehat{F}$ is unique up to natural isomorphism.

Our job is to understand how to construct this $\widehat{F}$.

[[!redirects presheaves]]