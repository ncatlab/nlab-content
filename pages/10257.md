
#Contents#
* table of contents
{:toc}

## Idea

_Bott periodicity_ is the name of a periodicity phenomenon that appears throughout [[spin geometry]], [[supersymmetry]] and [[K-theory]]. Incarnations of it include the following:

### In topological K-theory

The [[complex numbers|complex]] [[reduced K-theory|reduced]] [[topological K-theory]] groups have a degree-2 periodicity: 

$$
  \tilde K_{\mathbb{C}}^\bullet(X) 
    \simeq 
  \tilde K_{\mathbb{C}}^{\bullet + 2}(X) 
  \,.
$$ 

This isomorphism is induced by [[external tensor product]] with the image of the [[basic line bundle on the 2-sphere]] in [[reduced K-theory]], called the _[[Bott element]]_.

For details see at _[[topological K-theory]]_ the section _[Bott periodicity](topological+K-theory#BottPeriodicity)_.

The periodicity lifts to the [[classifying spaces]] and makes the [[Brown representability theorem|representing]] [[spectrum]] [[KU]] of complex K-theory be an [[even periodic ring spectrum]].

In particular the 2-periodicity in the [[homotopy groups]] of the [[stable unitary group]] $U = \underset{\longrightarrow}{\lim}_n U(n)$ is thus a shadow of Bott periodicity.

$$
  \pi_i(U) = \pi_i(GL_{\mathbb{C}})
  = 
  \left\lbrace 
   \array{ 
     0 &\vert& i\, \text{even}
     \\ 
     \mathbb{Z} &\vert& i \, \text{odd}
   }
   \right.
$$


Similarly the [[real numbers|real]] [[reduced K-theory|reduced]] [[topological K-theory]] groups have an 8-periodicity 

$$
 \tilde K^\bullet_{\mathbb{R}}(X)  
   \simeq 
  \tilde K^{\bullet + 8}_{\mathbb{R}}( X ) 
$$

a shadow of which is the 8-periodicity in the [[homotopy groups]] of the [[stable orthogonal group]]

$$
  \pi_i( O ) 
  = 
  \pi_i(GL_{\mathbb{R}})
  =
  \left\{  
    \array{
       \mathbb{Z}_2 &\vert& i = 0 \, \text{mod}\, 8  
       \\ 
       \mathbb{Z}_2 &\vert& i = 1 \, \text{mod}\, 8
       \\ 
       0 &\vert& i = 2 \, \text{mod}\, 8
       \\ 
       \mathbb{Z} &\vert& i = 3 \, \text{mod}\, 8
       \\  
       0 &\vert& i = 4 \, \text{mod}\, 8
       \\
       0 &\vert& i = 5 \, \text{mod}\, 8
       \\ 
       0 &\vert& i = 6 \, \text{mod}\, 8
       \\ 
       \mathbb{Z} &\vert& i = 7 \, \text{mod}\, 8
     }
   \right.
$$


### In Spin geometry

The complex [[Clifford algebras]] repeat -- up to _[[Morita equivalence]]_ -- with period 2, $Cl_{n}(\mathbb{C}) \simeq_{Morita} Cl_{n+2}(\mathbb{C})$. 

The real Clifford algebras analogously have period 8, $Cl_n(\mathbb{R}) \simeq_{Morita} Cl_{n+8}(\mathbb{R})$.


Accordingly the basic properties of complex [[spinor representations]] are the same for $Spin(d-1,1)$ and $Spin(d+2-1,1)$. Those of the real spinor representations repeat with period 8.


## Related concepts

* [[Hopf fibration]]

* [[periodic cohomology theory]]

* [[supersymmetry and division algebras]].


## References

Proof of Bott periodicity for [[topological K-theory]], including [[equivariant K-theory]]:

* [[Michael Atiyah]], _Bott periodicity and the index of elliptic operators_, The Quarterly Journal of Mathematics, Volume 19, Issue 1, 1968, Pages 113–140 ([doi:10.1093/qmath/19.1.113](https://doi.org/10.1093/qmath/19.1.113))

Review:

* {#Segal68} [[Graeme Segal]], Prop. 3.2 in: _Equivariant K-theory_, Inst. Hautes Etudes Sci. Publ. Math.  No. 34 (1968) p. 129-151 ([numdam:PMIHES_1968__34__129_0](http://www.numdam.org/item/PMIHES_1968__34__129_0))

* {#Karoubi05} [[Max Karoubi]], _Bott Periodicity in Topological, Algebraic and Hermitian K-Theory_,  In: [[Eric Friedlander]], [[Daniel Grayson]] (eds.) _[[Handbook of K-Theory]]_, Springer 2005 ([doi:10.1007/978-3-540-27855-9_4](https://doi.org/10.1007/978-3-540-27855-9_4))

* [[Dai Tamaki]], [[Akira Kono]], Section 4.2 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))

* {#HJJS08} [[Dale Husemöller]], [[Michael Joachim]], [[Branislav Jurčo]], [[Martin  Schottenloher]], Section 15 of: _[[Basic Bundle Theory and K-Cohomology Invariants]]_, Springer Lecture Notes in Physics __726__, 2008, ([pdf](http://www.mathematik.uni-muenchen.de/~schotten/Texte/978-3-540-74955-4_Book_LNP726.pdf), [doi:10.1007/978-3-540-74956-1](https://link.springer.com/book/10.1007/978-3-540-74956-1))


For a list of proofs of Bott periodicity, see

* _Proofs of Bott periodicity_, [MO](https://mathoverflow.net/q/8800/447)

[[!redirects Bott periodicities]]

[[!redirects Bott periodicity theorem]]
[[!redirects Bott periodicity theorem]]
