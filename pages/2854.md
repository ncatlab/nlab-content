Let $H$ be a Hopf algebra, a right $H$-[[comodule algebra]] $E$ is an __$H$-extension__ of a subalgebra $U\subset E$ if $U=E^{co H}$ is precisely  the subalgebra of $H$-coinvariants. The $H$-extension $U\subset E$ is **cleft** if there exist a __convolution-invertible $H$-comodule map__ $\gamma:H\to E$. 

If $U\hookrightarrow E$ is a cleft $H$-extension, then the cleavage $\gamma$ can always be chosen normalized in the sense that $\gamma(1)=1$; because if it is not normalized we can rescale $\gamma$ to form a normalized cleavage $\gamma'=\gamma^{-1}(1)\gamma$ (indeed, $1$ is [[grouplike element|group-like]], hence $\gamma(1)$ is invertible with inverse $(\gamma(1))^{-1}=\gamma^{-1}(1)$). 

It is easy to show that the rule 

$$h\triangleright u := \sum \gamma(h_{(1)})u\gamma^{-1}(h_{(2)})$$

defines a [[measuring]] $\triangleright:H\otimes U\to U$ i.e. $h\triangleright(uv)=\sum (h_{(1)}\triangleright u)(h_{(2)}\triangleright v)$ and if $\gamma$ is chosen normalized, then $h\triangleright 1 = \epsilon(h) 1$. Define a convolution invertible map $\sigma\in Hom_k(H\otimes H,U)$ by

$$\sigma(h,k) = \sum \gamma(h_{(1)})\gamma(k_{(1)})\gamma^{-1}(h_{(2)}k_{(2)}),\,\,\,\,\,h,k\in H.$$

Then the pair $(\triangleright,\sigma)$ defines the data for the __cocycled [[crossed product algebra]]__ $U\sharp_\sigma H$ which is canonically isomorphic to $B$ as an $H$-extension of $U\cong U\otimes 1\hookrightarrow U\sharp_\sigma H$, and i.e. as a right $H$-comodule algebra with the isomorphism fixing $U$ as given.

Conversely, every cocycled product $U\sharp_\sigma H$ is cleft via $\gamma:
h\mapsto 1\sharp h$ and the cocycle $\sigma$ built out of $\gamma$ is the same one, which helped build the cocycled crossed product.  

Every cleft extension is a particular case of a [[Hopf-Galois extension]].
   
* Y. Doi, [[Mitsuhiro Takeuchi]], _Cleft comodule algebras for a bialgebra_, Comm. Alg. __14__ (1986) 801--818 [doi](https://doi.org/10.1080/00927878608823337)
* S. Majid, _Foundations of quantum group theory_, Cambridge University Press 1995, 2000.

* S. Montgomery, _Hopf algebras and their actions on rings_, CBMS 82, AMS 1993.

There are generalizations for Hopf algebroids:

* [[Gabriella Böhm]], [[Tomasz Brzeziński]], _Cleft extensions of Hopf algebroids_, Appl. Cat. Str. 14 (2006) 431-469; [math.QA/0510253](http://arxiv.org/abs/math.QA/0510253)

There are some globalizations of cleft extensions. For the smash product case of the globalization some details are written in 

* [[Zoran Škoda]], _&#268;ech cocycles for quantum principal bundles_, [arxiv/1111.5316](http://arxiv.org/abs/1111.5316)
* Z. &#352;koda, [[zoranskoda:cleft extension of a space cover]]

[[!redirects cleft extensions]]
[[!redirects cleft comodule algebra]]
[[!redirects cleft Hopf-Galois extension]]