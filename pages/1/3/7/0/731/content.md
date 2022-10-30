#Idea#
The Dwyer&#8211;Kan loop groupoid of a [[simplicial set]] $K$ is a [[simplicial groupoid|simplically enriched groupoid]] whose objects are the vertices of $K$ and the simplicial set of paths between two such picks up the composable 'strings' of higher dimensional simplices where the zeroth vertex is thought of as the domain vertex and the first vertex as the codomain.

#Definition#

The **loop groupoid functor of Dwyer and Kan** is a functor 
$$G: \Simp\Set \to \Simp\Set\Groupoid,$$
which takes the simplicial set $K$ to the [[simplicial groupoid]] $GK$, where $(GK)_n$ is the [[free groupoid]] on the directed graph given by a pair of arrows
$$s,t: K_{n+1}\rightarrow K_0,$$
where the two functions, $s$, source, and $t$, target, are $s = (d_1)^{n+1}$ and $t = d_0(d_2)^n$ with relations $s_0x = id$ for $x \in K_n$.  

The face and degeneracy maps are given on generators by 
*   $s_i^{GK}(x) = s_{i+1}^K(x),$
*   $d_i^{GK}(x) = d_{i+1}^K(x)$, for $x \in K_{n+1}$, $1 \lt i \leq n$, and 
*   $d_0^{GK}(x) = (d_0^K(x))^{-1}(d_1^K(x))$. 

#Remarks#
*  This simplicial groupoid is a simplicially enriched groupoid, as the face and degeneracy operators are constant on the objects.

* The loop groupoid functor has a right adjoint, $\overline{W}$, called the (simplicial) [[classifying space]] functor.  This is given in more detail in the entry on [[simplicial group]].

* The original reference is 

W. G. Dwyer and D. M. Kan, _Homotopy theory and simplicial groupoids_, Nederl. Akad. 
Wetensch. Indag. Math., 46, (1984), 379 &#8211; 385,

but beware, there are some typographic errors in key formula, so more recent sources should be compared with it as a check.