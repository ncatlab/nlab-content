## Definition:## 
 The **d\'{e}calage** of an arbitrary simplicial set, $Y$, is the simplicial set, $Dec\, Y$, defined by shifting every dimension down by one, 'forgetting' the last face and degeneracy  of $Y$ in each dimension. 

 More precisely

* $(Dec \, Y)_n = Y_{n+1}$;
* $d_k^{n,Dec \,Y}  = d^{n+1,Y}_{k}$;
* $s_k^{n,Dec \,Y}  = s^{n+1,Y}_{k}$.




This simplicial set comes with a natural projection, $d_{last} : Dec\, Y \to Y$, given by the 'left over' face map.     Moreover this map gives a homotopy equivalence

$$Dec\,Y \simeq K(Y_0,0),$$

between $Dec\, Y$ and the constant simplicial set on $Y_0$. 

The same construction works in other contexts, as is easily seen. The case of $Dec G$ for $G$ a simplicial group is important in the simplicial theory of algebraic models for homotopy $n$-types.

The map $d_{last} : Dec\, Y \to Y$, is a fibration, and in particular, in the simplicial group case, $d_{last} : Dec\, G \to G$, is an epimorphism.  Taking the kernel of this and then applying $\pi_0$, yields a [[crossed module]] constructed from the [[Moore complex]] of $G$

$$NG_1/d_2(NG_2)\to NG_0,$$

which has kernel $\pi_1(G)$ and cokernel $\pi_0(G)$.