##Definition##


Given a [[simplicial group]] $G$, the **Moore complex**, $({NG},\partial )$,  of $G$ is the non-Abelian chain complex defined by 
$$
NG_n=\bigcap_{i=1}^{n}Ker\,d_i^n 
$$
with $\partial _n:NG_n\rightarrow NG_{n-1}$ induced from $d_0^n$ by
restriction. 

*Note:* there is no assumption that the $NG_n$ are Abelian.

##Conventional remarks##

* There is an alternative 'dual' form of this with $\bigcap_{i=0}^{n-1}Ker\,d_i^n$ and with the boundary /  differential $\partial$ induced by the last face map $d^n_n$. The theories run parallel but the fact there are two valid forms can be confusing for the formulae for various derived structures. 


*  The notation $NG$ is quite widely used in the literature but can get confused with that sometimes used for the nerve functor, so care is needed.


##Discussion##
If an element $g \in G_n$ is in the Moore complex then all but its zeroth face is trivial. In dimension 1, this means that $g$ is a 1-simplex that 'starts' at the identity element of $G_0$. If this $g$ is in the kernel of the boundary map $\partial _1: NG_1\rightarrow NG_{0}$, then $g$ will be a loop at that identity. If it is $\partial x$ for some $x\in NG_2$, then $x$ intuitively provides a homotopy between $g$ and the identity element.  This motivates the following definition:

###Definition###
The **n$^{th}$ homotopy group**, $\pi _n$(G), of $G$ is the $n^{th}$ homology of the Moore complex of $G$, i.e.,  
$$
\pi _n({G})  \cong  H_n( {NG},\partial ),   = \big( \bigcap_{i=0}^n Ker\,d_i^n\big)/d_{0}^{n+1}\big(\bigcap_{i=1}^{n+1} Ker\,d_i^{n+1}\big). 
$$

Note that $\partial NG_{n+1}\triangleleft  NG_n$.

##Back to the Discussion##
*   In the case of simplicial Abelian groups or more generally, simplicial modules over a ring, the Moore complex of such an object is merely a chain complex of the same sort of object by the [[Dold-Kan correspondence]]. Various non-commutative forms of that result have been proved, for instance,  [[group T - complex|group T - complex]]es are equivalent to [[crossed complex]]es, by a result of Ashley,

     * N. Ashley, _Simplicial T-Complexes: a non abelian version of a theorem of Dold-Kan_ , Dissertations Math., 165, (1989), 11 &#8211; 58.

*  In general, for simplicial groups, the Moore complex has a beautiful structure of pairings described by Pilar Carasco, in her thesis and in the resulting paper,

    * P. Carrasco and A. M. Cegarra, Group-theoretic Algebraic Models for Homotopy Types , J. Pure Appl. Alg., 75, (1991), 195 &#8211; 235

The resulting structure is that of a [[hypercrossed complex]]. Typically one has pairings 
$$NG_p \times NG_q \to NG_{p+q}.$$
These are well understood in low dimensions, see the entry on [[hypercrossed complex]] for more details. 

* Suppose that $G$ is a simplicial group with Moore complex $NG$, which satisfies $NG_k = 1$ for $k\gt 1$, then $(G,1,G_0,d_1,d_0)$ has the structure of a [[2-group]]. The interchange law is satisfied since the corresponding equation in $G_1$ is always the image of an element in $NG_2$, and here that must be trivial. If one thinks of the 2-group as being specified by a [[crossed module]] $(C,P,\delta, a)$, then in terms of the original simplicial group, $G$,  $NG_0 = G_0 = P$, $NG_1 \cong C$, $ \partial = \delta$ and the action of $P$ on $C$ translates to an action of $NG_0$ on $NG_1$ using conjugation by $s_0(p)$, i.e., for $p\in G_0$ and $c\in NG_1$, 
$$a(p)(c) = s_0(p)c s_0(p)^{-1}.$$


* Suppose next that $NG_k = 1$ for $k \gt 2$, then the Moore complex is a [[2-crossed module]] in the sense of Conduch&#233;.  Such objects model all [[homotopy 3-types]].  They are related to the [[crossed squares]] of Guin-Valery and Loday, in that there is a functor $(crossed squares) \to (2-crossed modules)$ which preserves homotopy types, but crossed squares have the advantage that there is a homotopically defined functor with values in crossed squares, related to classical homotopy invariants of pairs and triads, and which satisfies a Higher Homotopy van Kampen theorem, so that some calculations are possible. 

