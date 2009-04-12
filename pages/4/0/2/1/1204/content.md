The aim of _Homological Perturbation Theory_ is to construct small [[chain complex]]es from large ones. It was originally developed for the calculation of chain models of the total spaces of fibre spaces, but has since developed into a useful general computational tool. 

Let $(X,d), (Y,d)$ be chain complexes over a ring $R$ and let $f: X \to Y, \nabla: Y \to X$ be chain maps, and $\Phi: X \to X$ a [[chain homotopy]] such that 

$$ f \nabla=1, \quad \nabla f= 1 + d\Phi + \phi d, $$ 

 $$ f\Phi = 0, \Phi \nabla=0, \Phi^2=0, \Phi d \Phi= - \Phi. $$

Let $X,Y$ have filtrations $F^*$ bounded below by $0$ and preserved by $\nabla,f, \Phi$ and the differentials on $X,Y$. Suppose $X$ has another differential $d^\tau$ with the property that 

$$ (d^\tau -d)F^p X \subseteq F^{p-1} X $$ 

for all $p \geq 0$. The Homological Perturbation Lemma states that $Y$ can be given a new differential $d^\tau$ such that there is a chain equivalence $(Y, d^\tau) \to (X, d^\tau)$. 

The main point is that there is an explicit formula for the new chain homotopy as 

$$\Phi^\tau= \sum _{r=0}^\infty \Phi (1+ d^\tau \Phi)^r.$$

There is considerable interest in describing the new differential in terms of a [[twisting cochain]]. 

This result derived from earlier work of G. Hirsch, E.H. Brown, Weishu Shih, and has been widely developed into a useful theoretical and computational tool by Guggenheim, Lambe, Stasheff and others.  

#References#

* R. Brown, The twisted Eilenberg-Zilber Theorem,  Simposio di Topologia (Messina, 1964)  pp. 33--37 Edizioni Oderisi, Gubbio

* Barnes, Donald W.(5-SYD-PM); Lambe, Larry A.(5-SYD-PM)
A fixed point approach to homological perturbation theory.
Proc. Amer. Math. Soc. 112 (1991), no. 3, 881--892. 


