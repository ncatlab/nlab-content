## Idea

Given a category $E$ with pullbacks, one can consider [[internal functor]]s, which are the morphisms in $Cat(E)$. If $E = Set$ then one can consider not only functors among small categories but also functors of the type $F: C\to Set$ from a small category $C$ to a large category of sets. In that case one can describe $F_0$ as consisting of a $C_0$-indexed family of objects and an action of $C_1$ on the diagram.  

## Definition

Given $C\in Cat(E)$ an __internal diagram__ $F$ on $C$ (or, of type $C$) consists of 

* a morphism $\lambda : F_0\to C_0$ in $E$
* a morphism $e : F_1 = F_0\times_{C_0} C_1\to C_1$

such that action axioms hold as well as the compatibility with "momentum" $\lambda$ i.e. $\lambda e = d_1 pr_2$.

It is clear how to define then the morphisms of internal diagrams. Internal diagrams in $E$ of type $C$ form a category denoted by $E^C$. 

## Characterization

From an internal diagram $(F,C,\lambda,e)$ one can equip $F =(F_0,F_1)$ with a strcuture of an internal category over $C$. In other words, there is a forgetful functor $E^C\to Cat(E)/C$ (where $Cat(E)/C$ is the corresponding [[slice category]]). This functor is fully faithful and its essential image consists precisely of all objects in $Cat(E)/C$ which are [[discrete fibration]]s. 

## References

* [[P. T. Johnstone]], _Topos theory_, 1977, chapter 2 