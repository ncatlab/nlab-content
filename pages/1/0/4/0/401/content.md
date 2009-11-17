# Definitions

In the category of all [[topological spaces]] one distinguishes several closely related notions. Consider topological pairs $(X,A)$; in other words, $X$ is a topological space and $A\subset X$.  Then $A$ is a __deformation retract__ of $X$ if there exist a continuous map $H:X\times I\to X$ such that $H(a,t)=a$ for all $a\in A$, $t\in I=[0,1]$, $H(x,0) = x$ for all $x\in X$ and $H(x,1)\in A$ for all $x\in X$.

A pair $(X,A)$ is an __NDR-pair__ if there are two continuous maps, $u:X\to I,\; H:X\times I\to X$ such that $H(a,t)=a$ for all $a\in A$ and all $t$, $H(x,0)=x$ for all $x\in X$, $u^{-1}(0)=A$ and $H(x,1)\in A$ for all $x$ such that $u(x)\lt 1$. If $(X,A)$ is an NDR-pair, then the inclusion has a left [[homotopy inverse]] iff $A$ is also a [[retract]] of $X$ (in [[Top]], in the standard categorical sense).

The pair $(X,A)$ is a __DR-pair__ if it is a deformation retract and there is a function $u:X\to I$ such that $A=u^{-1}(0)$ (i.e. it gives simultaneously a deformation retract and a NDR-pair). If $(X,A)$ is an NDR-pair then the inclusion $A\hookrightarrow X$ is a homotopy equivalence iff $A$ is a deformation retract of $X$. Any map $f:X\to Y$ is a [[homotopy equivalence]] iff $X$ is the deformation retract of the mapping cylinder of $f$. If $(X,A)$ is an NDR-pair and $A$ is [[contractible space|contractible]], then the quotient map $X\to X/A$ is a homotopy equivalence. 

# References

Literature includes G. Whitehead, _Elements of homotopy theory_, chapter 1. 

There is also the notion of a [[deformation retract of a homotopical category]], which has a similar feel in some ways but is not closely related.  (It should not be confused with the idea of a deformation retract *in* a [[model category]], which is a direct generalization of the notion described above for [[Top]].)
