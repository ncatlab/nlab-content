#Idea#

A _crossed module_ (of groups) is a (nonabelian) chain-complex incarnation of a strict [[2-group]]. Crossed modules can be conceptually understood as [[crossed complex|crossed complexes]] concentrated in degree 1 and 2, as generalisations of normal subgroups, or as [[Moore complex]]es of certain [[simplicial group]]s. Historically they were the first example of [[higher dimensional algebra]] to be studied.

#Definition#

A **crossed module** is

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
 
#Definition in terms of equations#

The two diagrams can be translated into equations, which may often be helpful.

*   If we write the effect of acting with $g_1\in G_1$ on $g_2\in G_2$ as ${}^{g_1}g_2$, then the second diagram translates as the equation:
    $$\delta({}^{g_1}g_2) = g_1\delta(g_2)g_1^{-1}.$$
In other words that $\delta$ is equivariant for the action of $G_1$. 

*   The first diagram is slightly more subtle.  The group $G_2$ can act on itself in two different ways, (i) by the usual conjugation action, ${}^{g_2}g^\prime_2=g_2g^\prime_2g_2^{-1} $ and (ii) by first mapping $g_2$ down to $G_1$ and then using the action of that group back on $G_2$.  The first diagram says that the two actions coincide. Equationally this gives:
$${}^{\delta(g_2)}g^\prime_2 = g_2g^\prime_2g_2^{-1}.$$

This equation is known as the **Peiffer rule** in the literature.

#Examples#

* for $H$ any group, its automorphism crossed module is $AUT(H) := (G_2 = H, G_1 = Aut(H), \delta = Ad, \alpha = Id)$; under the equivalence of crossed modules with strict [[2-group]]s this corresponds to the 2-group $Aut_{Grpd}(\mathbf{B}H)$ of automorphisms in the category [[Grpd]] of [[groupoid]]s on the one-object [[groupoid]] $\mathbf{B}H$ corresponding to the group $H$.

*  Almost the canonical example of a crossed module is given by a group $G$ and a normal subgroup $N$ of $G$.  We take $G_2 = N$, and $G_1 = G$ with the action given by conjugation, whilst $\delta$ is the inclusion, $inc : N \to G$. This is 'almost canonical', since if we replace the groups by simplicial groups $G_.$ and $N_.$, then $(\pi_0(G_.),\pi_0(N_.),\pi_0(inc))$ is a crossed module, and given any crossed module, $(C,P,\delta)$, there is a simplicial group $G_.$ and a normal subgroup $N_.$, such that the construction above gives the given crossed module up to isomorphism.

* Suppose $F\stackrel{i}{\to}E\stackrel{p}{\to}B$ is a fibration sequence
  of pointed spaces, thus $p$ is a [[fibration]] in the topological sense (lifting of paths and homotopies of paths will suffice), $F = p^{-1}(b_0)$, where $b_0$
  is the basepoint of $B$.  The fibre $F$ is pointed at $f_0$, say, and $f_0$
  is taken as the basepoint of $E$ as well.

    There is an induced map on fundamental groups

    $$\pi_1(F) \stackrel{\pi_1(i)}{\longrightarrow} \pi_1(E)$$ 

    and if $a$ is a loop in $E$
based at $f_0$, and $b$ a loop in $F$ based at $f_0$, then the composite path
corresponding to $aba^{-1}$ is homotopic to one wholly within $F$.  To see
this, note that $p(aba^{-1})$ is null homotopic.  Pick a homotopy in $B$
between it and the constant map, then lift that homotopy back up to $E$ to one 
starting at $aba^{-1}$.  This homotopy is the required one and its other end
gives a well defined element ${}^a b \in \pi_1(F)$ (abusing notation by confusing paths and 
their homotopy classes).  With this action $(\pi_1(F), \pi(E), \pi_1(i))$ is a 
crossed module.  This will not be proved here, but is not that difficult.  (Of course,  secretly, this example is 'really' the same as the previous one since a fibrtion of simplicial groups is just morphism that is an epimorphism in each degree, and the fibre is thus just a normal simplicial subgroup. What is fun is that this generalises to 'higher dimensions'.)  