#Idea#

The usual definition of _vertex operator algebra_ is long and unenlightning. But due to work by Huang and Kong it is known now that vertex operator algebras are nothing but certain [[FQFT]]s:

There is a monoidal [[category]] whose [[morphism]]s are conformal spheres with $n$-punctures marked as incoming and one punccture marked as outgoing (each puncture equipped with a conformally parameterized annular neighbourhood). Composition of such spheres is by gluing along puctures. This can be regarded as a category $2Cob_{conf}^0$ of 2-dimensional genus-0 conformal [[cobordism]]s.

As shown by theorems by Huang and Kong, a vertex operator algebra is precisely a _holomorphic representation_ of this category, i.e. an genus-0 conformal [[FQFT]], hence a monoidal functor

$$
  V : 2Cob_{conf}^0 \to Vect
$$

such that its comonent $V_1$ is a holomorphic function on the moduli space of conformal punctured spheres.

#References#

* Yi-Zhi Huan, _Geometric interpretation of vertex operator algebras_, Proc. Natl. Acad. Sci. USA, Vol 88. (1991) pp. 9964-9968

* Liang Kong, _Open-closed field algebras_ Commun. Math. Physics. 280, 207-261 (2008) ([arXiv](http://arxiv.org/abs/math/0610293)).