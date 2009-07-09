Given a [[bialgebra]] $H$, a __Drinfel'd twist__ is an invertible element $\chi\in H^{\otimes 2}$ satisfying

$$
(1\otimes\chi)(id\otimes\Delta)\chi = (\chi\otimes 1)(\Delta\otimes id)\chi,
$$
satisfying $(\epsilon\otimes id)\chi = (id\otimes\epsilon)\chi = 1$ (in fact it is enough to require one out of these two counitality conditions). In Majid's formalism of [[bialgebra cocycle]]s, this is the same as a counital 2-cocycle in $H$. 

Vladimir Drinfel'd introduced $\chi$ in order to suggest a procedure of twisting [[Hopf algebra]]s. Given a bialgebra, Hopf algebra or quasitriangular Hopf algebra, one gets another such structure twisting it with a Drinfel'd twist. Let $H$ be a quasi-triangular Hopf algebra with with comultiplication $\Delta$, antipode $S$, universal R-element $R$ and let $\chi$ be a Drinfel'd twist. Then the same algebra becomes another quasitriangular Hopf algebra with formulas for comultiplication $\Delta_\chi b = \chi (\Delta b)\chi^{-1}$, universal R-element $R_\chi = \chi_{21} R\chi$ and antipode $S_\chi b = 
\sum \chi^{(1)} S(\chi^{(2)}) (S b)(\sum \chi^{(1)}S(\chi^{(2)}))^{-1}$. The counit is not changed. Here $\chi_{21}=\tau(\chi)$ where $\tau$ is the flip of tensor factors, and $\chi = \sum \chi^{(1)}\otimes\chi^{(2)}$ is a notation similar to Sweedler's convention.