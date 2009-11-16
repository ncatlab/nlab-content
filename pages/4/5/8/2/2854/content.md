Let $H$ be a Hopf algebra, a right $H$-[[comodule algebra]] $E$ is an __$H$-extension__ of a subalgebra $U\subset E$ is $U=E^{co H}$ is the subalgebra of $H$-coinvariants. The $H$-extension $U\subset E$ is **cleft** if there exist a convolution-invertible $H$-comodule map $\gamma:H\to E$. 

If $U\hookrightarrow E$ is a cleft $H$-extension, then the cleavage $\gamma$ can always be chosen normalized in the sense that $\gamma(1)=1$; because if it is not normalized we can rescale $\gamma$ to form a normalized cleavage $\gamma'=\gamma(1)^{-1}\gamma$ (indeed, $1$ is [[grouplike element|group-like]], hence $\gamma(1)$ is invertible with inverse $(\gamma(1))^{-1}=\gamma^{-1}(1)$). 

It is easy to show that the rule 

$$h\triangleright u := \sum \gamma(h_{(1)})u\gamma^{-1}(h_{(2)})$$

defines a [[measuring]] $\triangleright:H\otimes U\to U$ i.e. $h\triangleright(uv)=\sum (h_{(1)}\triangleright u)(h_{(2)}\triangleright v)$ and if $\gamma$ is chosen normalized, then $h\triangleright 1 = \epsilon(h) 1$. Define an invertible map $\sigma\in Hom_k(H\otimes H,U)$ by

$$\sigma(h,k) = \sum \gamma(h_{(1)})\gamma(k_{(1)})\gamma^{-1}(h_{(2)}k_{(2)}),\,\,\,\,\,h,k\in H.$$

Then the pair $(\triangleright,\sigma)$ defines the data for the __cocycled [[crossed product algebra]]__ $U\sharp_\sigma H$ which is canonically isomorphic to $B$ as an $H$-extension of $U\cong U\otimes 1\hookrightarrow U\sharp_\sigma H$, and i.e. as a right $H$-comodule algebra with the isomorphism fixing $U$ as given.

Every cleft extension is a [[Hopf-Galois extension]].   

* S. Majid, Foundations of quantum group theory, Cambridge University Press 1995, 2000.

* S. Montgomery, Hopf algebras and their actions on rings, CBMS 82, AMS 1993.

There are generalizations for Hopf algebroids:

* Gabriella B&#246;hm, Tomasz Brzezi&#324;ski, _Cleft extensions of Hopf algebroids_, Appl. Cat. Str. 14 (2006) 431-469; [math.QA/0510253](http://arxiv.org/abs/math.QA/0510253)

[[!redirects cleft extensions]]