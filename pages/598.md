#Definition#
 A **simplicial group**, $G$, is a [[simplicial object]] in the category of groups.

#Notation# 
The category of simplicial groups is the category of functors from $\Delta^{op}$ to $Grp$.  It will be denoted $SimpGrp$

#Discussion#
* Clearly, as any group has an underlying set, a simplicial group has an underlying [[simplicial set]]. The underlying simplicial set of a simplicial group is a [[Kan complex]]. In fact, it is better than a Kan complex as there is an algorithm that gives the fillers for a given [[horn]]:


*  Let $(y_0,\ldots, y_{k-1}, -,y_{k+1}, \ldots, y_n)$ give a horn in $G_{n-1}$, so the $y_i$s are $(n-1)$ simplices that fit together as if they were all but one, the $k^{th}$ one,  of the faces of an $n$-simplex. There are three cases: 

     1. if $k = 0$: Let  $w_n = s_{n-1}y_n$ and then $w_i = w_{i+1}(s_{i-1}d_i w_{i+1})^{-1}s_{i-1}y_i$ for  $i = n, \ldots, 1$, then  $w_1 $ satisfies $d_i w_1 = y_i$, $i\neq  0$;

     2. if $0\lt k \lt n$: Let $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, k-1$, then take $w_n = w_{k-1}(s_{n-1}d_nw_{k-1})^{-1}s_{n-1}y_n$, and finally a downwards induction given by $w_i = w_{i+1}(s_{i-1}d_iw_{i+1})^{-1}s_{i-1}y_i$, for $i = n, \ldots, k+1$, then $w_{k+1}$ gives $d_iw_{k+1} = y_i$ for $i \neq k$;


     3.  if $k=n$ use $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, n-1$, then $w_{n-1}$ satisfies $d_iw_{n-1} = y_i$, $i\neq n$.

One point to note is that the filler for any horn can be chosen to be a _product of degenerate elements_.

* The homotopy groups of a simplicial group, $G$, can be calculated as the homology groups of the [[Moore complex]] of $G$.  This is, in general,  a non-Abelian chain complex.

* A simplicial group can be considered as a [[simplicially enriched category|simplicial groupoid]] having exactly one object. If $G$ is a simplicial group, the suggested notation for the corresponding simplicially enriched groupoid would be $\mathbf{B}G$ according to notational conventions suggested elsewhere in the nLab.

* There is a functor due to Dwyer and Kan, called the [[Dwyer-Kan loop groupoid]] that takes a  simplicial set to a simplcial groupoid. This has a left adjoint $\overline{W}$ and together they give an equivalence of categories between the homotopy category of simplical sets and that of simplicial groupoids. We thus have that all homotopy types are modelled by simplicial groupoids ... and for connected homotopy types by simplicial groups. One *important fact* to note in this equivalence is that it shifts dimension by 1, so if $G(K)$ is the simplicial group corresponding to the connected simplicial set $K$ then $\pi_k(K)$ is the same as $\pi_{k-1}(G(K))$.  This is important when considering algebraic models for a [[homotopy n-type]].