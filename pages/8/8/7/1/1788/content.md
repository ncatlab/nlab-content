

## Notions of orbifold cohomology

Let 

$$
  \mathcal{X}
  \;\coloneqq\;
  OrbSnglr\big(  X \!\sslash\! G \big)
$$ 

be the global quotient [[orbifold]] supposed to correspond to a [[smooth manifold]] $X$ equipped with the [[action]] of a [[finite group]] $G$ (for definiteness, and to avoid inessential technical fine-print).

Write

* $Snglr(\mathcal{X}) = X/G$ for its naive quotient space, 

  traditionally regarded as [[topological space]] 

  (namely the [[quotient topological space]] of the [[topological G-space]] underlying $X$),

  though this quotient does exist also in [[diffeological spaces]], which would be the more appropriate [[category]] to regard it in ([IKZ 10](#IKZ10));

* $Smth(\mathcal{X}) = X \sslash G$ for its [[homotopy quotient]] space,

  traditionally regarded as a [[topological space]] (namely the [[Borel construction]] on the [[topological G-space]] underlying X),

  though this homotopy quotient does exists also in [[differentiable stacks]]/[[smooth groupoids]], which is the more appropriate [[(2,1)-category]] to regard it in ([MP97](#MoerdijkPronk97)).

Most notions of [[cohomology]] of the orbifold $\mathcal{X}$ considered in existing literature are actually invariants just of $Snglr(\mathcal{X})$ or just of $Smth(\mathcal{X})$, and mostly just of their underlying topological spaces -- the closest to an exception to this rule is Chen-Ruan cohomology, which however is also just the cohomology of a naive quotient, just of a different orbifold (the [[inertia orbifold]]):

| **cohomology of $Snglr(\mathcal{X})$** | 
|-----------------------|
| [Satake 56, Thm 1](#Satake56): $H_{Sa}^\bullet(\mathcal{X}) = H^\bullet\big(Shp \circ Snglr(\mathcal{X}),\mathbb{R}\big)$ | 
|  **cohomology of $Smth(\mathcal{X})$**   |
| [Moerdijk-Pronk 99](#MoerdijkPronk99), [ALR 07  Def. 1.56](#ALR07): $H^\bullet_{MP}\big( \mathcal{X}, \mathcal{A} \big) = H^\bullet\big( Shp\circ Smth(\mathcal{X}), A \big)$ <br/>    |
| **cohomology of $Snglr\big( [\mathcal{B}\mathbb{Z}, \mathcal{X}] \big)$** |
| [Chen-Ruan 00](#ChenRuan00): $H^\bullet_{CR}(\mathcal{X}) \coloneqq H^\bullet\Big( Shp \circ Snglr\big( [\mathcal{B}\mathbb{Z}, \mathcal{X}] \big)  ,\mathbb{K}\Big)$ <br/> (see [Clader 14, p. 4, p.7](#Clader14)) <br/> [Moe 02, p. 18](#Moerdijk02):  $H^\bullet_{CR}(\mathcal{X}) = H^\bullet\big( Shp \circ Snglr(\mathcal{X}), R_{\mathbb{K}}(Isotr(-))  \big)$  <br/> [Honkasalo 88, Thm. 6.4](#Honkasalo88), [Honkasalo 90, Thm. 5.5](#Honkasalu90): $\cdots = H^\bullet_G\big(X, something \big) $ |  



## References

* {#Satake56} [[Ichiro Satake]], _On a generalisation of the notion of manifold_, Proc. Nat. Acad. Sci. U.S.A. 42 (1956), 359&#8211;363 ([doi:10.1073/pnas.42.6.359]( https://doi.org/10.1073/pnas.42.6.359))


* {#Honkasalo88} Honkasalo, _Equivariant Alexander-Spanier cohomology_,  Mathematica Scandinavia,  63, 179-195, 1988 ([doi:10.7146/math.scand.a-12232](https://doi.org/10.7146/math.scand.a-12232))


* {#Honkasalu90} Honkasalo, _Equivariant Alexander-Spanier cohomology for actions of compact Lie groups_, Mathematica Scandinavica Vol. 67, No. 1 (1990), pp. 23-34 ([jstor:24492569](https://www.jstor.org/stable/24492569))

* {#MoerdijkPronk97} [[Ieke Moerdijk]], [[Dorette Pronk]], _Orbifolds, sheaves and groupoids_, K-theory 12 3-21 (1997) ([pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/pronk.pdf), [doi:10.4171/LEM/56-3-4](http://dx.doi.org/10.4171/LEM/56-3-4))

* {#MoerdijkPronk99} [[Ieke Moerdijk]], [[Dorette Pronk]], _Simplicial cohomology of orbifolds_, Indagationes Mathematicae Volume 10, Issue 2, 1999, Pages 269-293 (<a href="https://doi.org/10.1016/S0019-3577(99)80021-4">doi:10.1016/S0019-3577(99)80021-4</a>)

* {#ChenRuan00} [[Weimin Chen]], [[Yongbin Ruan]], _A New Cohomology Theory for Orbifold_, Commun. Math. Phys. 248 (2004) 1-31 ([arXiv:math/0004129](https://arxiv.org/abs/math/0004129))

* {#Moerdijk02} [[Ieke Moerdijk]], _Orbifolds as Groupoids: an Introduction_, [[Alejandro Adem]], [[Jack Morava]], Yongbin Ruan (eds.) _[[Orbifolds in Mathematics and Physics]]_, Contemporary Math 310 , AMS (2002), 205–222 ([arXiv:math.DG/0203100](http://arxiv.org/abs/math.DG/0203100)) 

* {#ALR07} A. Adem, J. Leida, [[Yongbin Ruan]], _Orbifolds and Stringy Topology_, Cambridge Tracts in Mathematics **171** (2007) ([doi:10.1017/CBO9780511543081](https://doi.org/10.1017/CBO9780511543081), [pdf](http://www.math.colostate.edu/~renzo/teaching/Orbifolds/Ruan.pdf))


* {#IKZ10} [[Patrick Iglesias-Zemmour]], [[Yael Karshon]], Moshe Zadka, _Orbifolds as diffeologies_, Transactions of the American Mathematical Society 362 (2010), 2811-2831 ([arXiv:math/0501093](https://arxiv.org/abs/math/0501093)) 

* {#Clader14} Emily Clader, _Orbifolds and orbifold cohomology_, 2014 ([pdf](http://www-personal.umich.edu/~eclader/OctLect1.pdf))

