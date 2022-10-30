Given an $A$-coring (a comonoid in the category of $A$-$A$-bimodules for a $k$-algebra $A$) $(C,\Delta,\epsilon)$ (example: any $k$-algebra) a __semi-grouplike__ element is any $g\in C$ such that $\Delta(g) = g\otimes g$. 
A grouplike (or group-like) element is a semi-grouplike such that $\epsilon(g) = 1$. 

All grouplike elements in a $k$-bialgebra make a group. (Can this fact be categorified ??)

For corings with a (sometimes semi-)grouplike element one can define many useful notions which do not exist for general corings.  For example, given a semi-grouplike element $g$, the tensor algebra $\Omega C = \oplus_i \Omega^i C$ of the coring $C$, where $\Omega^i C = C\otimes_A \ldots \otimes_A C$ ($i$ times) over $A$ can be equipped with a differential $d$ of degree $+1$ in canonical way making it a [[differential graded algebra]]. In degree $0$, one defines $da = ga - ag$ and in higher degree 

$$d(c_1\otimes\ldots\otimes c_n) = g\otimes c_1\otimes\ldots\otimes c_n + (-1)^{n+1}c_1\otimes\ldots\otimes c_n\otimes g + \sum_{i=1}^n c_1\otimes\ldots\otimes c_{i-1}\otimes \Delta(c_i)\otimes c_{i+1}\otimes\ldots \otimes c_n.$$

A special case of this construction is when $g = 1\otimes_R 1$ and $C$ is the [[Sweedler coring]] for a $k$-algebra extension $R\to S$. The dga obtained is the classical Amitsur complex $\Omega(S/R)$ for that extension; for this reason the complex $\Omega C = \Omega(C,g)$ above for any coring $C$ and semi-grouplike $g$ is sometimes said to be an Amitsur complex. 