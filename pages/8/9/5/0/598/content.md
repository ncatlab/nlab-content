#Definition#
 A **simplicial group**, $G$, is a [[simplicial object]] in the category of groups.

#Discussion#
Clearly, as any group has an underlying set, a simplicial group has an underlying [[simplicial set]].

*  The underlying simplicial set of a simplicial group is a [[Kan complex]]. In fact, it is better than a Kan complex as there is an algorithm that gives the fillers for a given [[horn]]:


     * Let $(y_0,\ldots, y_{k-1}, -,y_{k+1}, \ldots, y_n)$ give a horn in $G_{n-1}$, so the $y_i$s are $(n-1)$ simplices that fit together as if they were all but one, the $k^{th}$ one,  of the faces of an $n$-simplex. There are three cases: 

    * (i) $k = 0$: Let  $w_n = s_{n-1}y_n$ and then $w_i = w_{i+1}(s_{i-1}d_i w_{i+1})^{-1}s_{i-1}y_i$ for  $i = n, \ldots, 1$, then  $w_1 $ satisfies $d_i w_1 = y_i$, $i\neq  0$;

     *(ii)  $0\lt k \lt n$: Let $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, k-1$, then take $w_n = w_{k-1}(s_{n-1}d_nw_{k-1})^{-1}s_{n-1}y_n$, and finally a downwards induction given by $w_i = w_{i+1}(s_{i-1}d_iw_{i+1})^{-1}s_{i-1}y_i$, for $i = n, \ldots, k+1$, then $w_{k+1}$ gives $d_iw_{k+1} = y_i$ for $i \neq k$;


     *[(iii)]  the third case, $k=n$ uses $w_0 = s_0y_0$ and $w_i = w_{i-1}(s_id_iw_{i-1})^{-1}s_iy_i$ for $i = 0, \ldots, n-1$, then $w_{n-1}$ satisfies $d_iw_{n-1} = y_i$, $i\neq n$.

One point to note is that the filler for any horn can be chosen to be a product of degenerate elements.

* The homotopy groups of a simplicial group, $G$, can be calculated as the homology groups of the [[Moore complex]] of $G$.  This is, in general,  a non-Abelian chain complex.

* A simplicial group can be considered as a [[simplicial groupoid]] having exactly one object. If $G$ is a simplicial group, the suggested notation for the corresponding simplicialy enriched groupoid would be $BG$ according to notational conventis suggested elswhere in the nLab