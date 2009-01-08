#Idea#

A _crossed module_ (of groups) is a (nonabelian) chain-complex incarnation of a strict [[2-group]]. Crossed modules are conceptually best understood as [[crossed complex|crossed complexes]] concentrated in degree 1 and 2.

#Definition#

A _crossed module_ is

* a pair of [[group]]s $G_2, G_1$,

* morphisms of groups
  $$
    G_2 \stackrel{\delta }{\to}{G_1}
  $$ 
  and 
  $$
    G_1 \stackrel{\alpha}{\to} Aut(G_2)
  $$ 
  (which below we will conceive of as a map $\alpha : G_1 \times G_2 \to G_2$ analogous the adjoint action $Ad : G \times G \to G$ of a group on itself)

* such that 
$$
  \array{
    G_2 \times G_2
    &&\stackrel{\delta \times Id}{\to}&&
    G_1 \times G_2
    \\
    & {}_{Ad}\searrow && \swarrow_\alpha
    \\
    &&
    G_2
  }
$$
and
$$
  \array{
    G_1 \times G_2 &\stackrel{\alpha}{\to}& G_2
    \\
    \downarrow^{Id \times \delta} && \downarrow^{\delta}
    \\
    G_1 \times G_1 &\stackrel{Ad}{\to}& G_1    
  }
$$
commute.
