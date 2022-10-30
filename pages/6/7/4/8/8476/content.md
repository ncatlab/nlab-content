Let $\mathfrak{g}$ and $\mathfrak{h}$ be [[nLab:differential graded Lie algebra]]s and $\boldsymbol i\colon \mathfrak{g}\to \mathfrak{h}[-1]$ be a [[nLab:morphism]] of [[nLab:graded vector spaces]]. Define $\boldsymbol l:\mathfrak{g}\to \mathfrak{h}$ as
$$
\boldsymbol l_{a}= d_{\mathfrak{h}} \boldsymbol i_{a} + \boldsymbol i_{d_{\mathfrak{g}}a}
$$
 for any $a\in \mathfrak{g}$. The [[nLab:morphism]] $\boldsymbol i$ is called a Cartan [[nLab:homotopy]] if it satisfies the two conditions
$$
\boldsymbol i_{[a,b]_{\mathfrak{g}}}= [\boldsymbol i_{a}, \boldsymbol l_{b}]_{\mathfrak{h}}\qquad \text{and} \qquad [\boldsymbol i_{a}, \boldsymbol i_{b}]_{\mathfrak{h}}=0,\qquad \text{for all}\quad a, b \in \mathfrak{g}.
$$
This name has an evident geometric origin: if $\mathcal{T}_{X}$ is the tangent [[nLab:sheaf]] of a [[nLab:smooth manifold]] $X$ and $\Omega ^{*}_{X}$ is the [[nLab:sheaf]] of [[nLab:complexes]] of [[nLab:differential forms]], then the [[nLab:contraction]] of [[nLab:differential forms]] with [[nLab:vector fields]] is a Cartan [[nLab:homotopy]]
$$
\boldsymbol i\colon \mathcal{T}_{X}\to \mathcal{E}nd^{*}(\Omega ^{*}_{X})[-1].
$$
In this case, $\boldsymbol l_{a}$ is the [[nLab:Lie derivative]] along the [[nLab:vector field]] $a$, and the conditions $\boldsymbol i_{[a,b]}= [\boldsymbol i_{a}, \boldsymbol l_{b}]$ and $[\boldsymbol i_{a}, \boldsymbol i_{b}]=0$, together with the defining equation $\boldsymbol l_{a}=[d_{\Omega ^{*}_{X}},\boldsymbol i_{a}]$ and with the equations $\boldsymbol l_{[a,b]}=[\boldsymbol l_{a},\boldsymbol l_{b}]$ and $[d_{\Omega ^{*}_{X}},\boldsymbol l_{a}]=0$ expressing the fact that $\boldsymbol l\colon \mathcal{T}_{X}\to \mathcal{E}nd^{*}(\Omega ^{*}_{X})$ is a [[nLab:differential graded Lie algebra|dgla]] [[nLab:morphism]], are nothing but the well-known Cartan identities involving [[nLab:contractions]] and Lie [[nLab:derivatives]].

 It is a straightforward computation to see that, if $\boldsymbol i$ is a Cartan [[nLab:homotopy]], then the degree [[nLab:zero morphism]] of [[nLab:graded vector spaces]] $\boldsymbol l\colon \mathfrak{g}\to \mathfrak{h}$ is actually a [[nLab:differential graded Lie algebra|dgla]] [[nLab:morphism]].

## References ##

* [[nLab:D. Fiorenza]], M. Manetti. _[[nLab:L-∞ algebras]], Cartan [[nLab:homotopies]] and [[nLab:period maps]]_; [arXiv:math/0605297](http://arxiv.org/abs/math/0605297)

* [[nLab:D. Fiorenza]], M. Manetti. _A [[nLab:period map]] for generalized deformations._ Journal of Noncommutative Geometry, Vol. 3, No. 4 (2009), 579-597; [arXiv:0808.0140](http://arxiv.org/abs/0808.0140). 

* [[nLab:D. Fiorenza]], E. Martinengo. _A short note on ∞-groupoids and the period map for projective manifolds_ Publications of the nLab. Vol. 2 (2012); [arXiv:0911.3845](http://arxiv.org/abs/0911.3845)
