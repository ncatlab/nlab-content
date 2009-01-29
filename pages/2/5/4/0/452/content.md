#Idea#

A _crossed module_ (of groups) is a (nonabelian) chain-complex incarnation of a strict [[2-group]]. Crossed modules can be conceptually understood as [[crossed complex|crossed complexes]] concentrated in degree 1 and 2, as generalisations of normal subgroups, or as [[Moore complex]]es of certain [[simplicial group]]s. Historically they were the first example of [[higher dimensional algebra]] to be studied.

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
#Notation#
We may use the notation $(G_2,G_1,\delta)$, for this if the action is fairly obvious, including an explicit action, $(G_2,G_1,\delta,\alpha)$, if there is a risk of confusion.
 
#Discussion#

* The two diagrams can be translated into equations, which may often be helpful.

   *   If we write the effect of acting with $g_1\in G_1$ on $g_2\in G_2$ as ${}^{g_1}g_2$, then the second diagram translates as the equation:
    $$\delta({}^{g_1}g_2) = g_1\delta(g_2)g_1^{-1}.$$
In other words that $\delta$ is equivariant for the action of $G_1$. 

   *   The first diagram is slightly more subtle.  The group $G_2$ can act on itself in two different ways, (i) by the usual conjugation action, ${}^{g_2}g^\prime_2=g_2g^\prime_2g_2^{-1} $ and (ii) by first mapping $g_2$ down to $G_1$ and then using the action of that group back on $G_2$.  The first diagram says that the two actions coincide. Equationally this gives:
$${}^{\delta(g_2)}g^\prime_2 = g_2g^\prime_2g_2^{-1}.$$

This equation is known as the **Peiffer rule** in the literature.

*  Almost the canonical example of a crossed module is given by a group $G$ and a normal subgroup $N$ of $G$.  We take $G_2 = N$, and $G_1 = G$ with the action given by conjugation, whilst $\delta$ is the inclusion, $inc : N \to G$. This is 'almost canonical', since if we replace the groups by simplicial groups $G_.$ and $N_.$, then $(\pi_0(G_.),\pi_0(N_.),\pi_0(inc))$ is a crossed module, and given any crossed module, $(C,P,\delta)$, there is a simplicial group $G_.$ and a normal subgroup $N_.$, sich that the construction above gives the given crossed module up to isomorphism.