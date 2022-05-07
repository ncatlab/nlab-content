
#Gromov's homotopy principle or h-principle
* table of contents
{:toc}

## Definition

Let $p \colon X\to B$ be a smooth [[fiber bundle]] and write $X^{(r)}$ for the $r$-[[jets]]  of [[sections]] of $p$; there is an induced [[projection]] $X^{(r)} \to B$ which makes it into a smooth bundle.  

One considers a fixed partial differential relation (see [[differential equation]]) which is a subset $R\subset X^{(r)}$. One is interested in finding [[formal geometry|formal]] sections $s$ of $X^{(r)}\to B$ whose image is in $R$, and which are, in addition, __holonomic sections__, i.e. equal to the $r$-jet $J_f^r$ of a $C^r$-section $f$ of $p:X\to B$. 

One says that $R$ satisfies the __h-principle__ if every formal section of $R$ is [[homotopy|homotopic]] to a holonomic section within the appropriate topological space of formal sections. 

##  Applications and examples

For example, in the case of holomorphic fiber bundles $R$ may be the Cauchy-Riemann relation, thus the question is if there is a deformation of a continuous section into a holomorphic one. In other words, one wants to reduce the problem of existence of maps of certain type to the analogous topological problem. Applications include results on the spaces of immersions, submersions, k-mersions, holomorphic maps, symplectic and isometric embeddings, contact structures and so on. 

[[Mikhail Gromov]] demonstrated the result that if $B$ is an open $n$-manifold, and if $R$ is open as a subspace of $X^{(r)}$ and is $Diff(B)$-invariant, then $R$ satisfies the $h$-principle ([EliasMisha 01, sec 2.1](#EliasMisha01), [Haefliger 71, p. 128](#Haefliger71))

##  General methods

Gromov introduced many techniques of proving the h-principle including the method of microflexible/continuous sheaves, the methods of convex integration and the removal of singularities.  

## Related concepts

* [[microflexible sheaf]]

* [[c-principle]]

* [[Oka principle]]  

* [[formal immersion of smooth manifolds]]

## References

Review:

* Y. Eliashberg, N. Mishachev, _Introduction to the h-principle_, Graduate Studies in Mathematics 48. Amer. Math. Soc. 2002 [gBooks](http://books.google.co.uk/books?isbn=0821832271)

* Andr&#233;s Angel, [[Johannes Ebert]], _Gromov's h-principle and its applications research seminar_, 2010, outline [pdf](http://wwwmath.uni-muenster.de/u/jeber_02/frueherelehre/hprinciple.pdf) (with useful bibliography)


* [[eom]]: [H-principle](http://www.encyclopediaofmath.org/index.php/H-principle), [convex integration](http://www.encyclopediaofmath.org/index.php/Convex_integration); 

Wikipedia: [homotopy principle](https://en.wikipedia.org/wiki/Homotopy_principle)

* MathOverflow: [h-principle-and-pdes](http://mathoverflow.net/questions/88513/h-principle-and-pdes)


Original articles:

* [[Mikhail Gromov]], _Partial differential relations_, Ergebn. Math. Grenzgeb. (3), 9, Springer (1986) ([doi:10.1007/978-3-662-02267-2](https://link.springer.com/book/10.1007/978-3-662-02267-2))

* [[Mikhail Gromov]], _A topological technique for the construction of solutions of differential equations and inequalities_, Proc. Int. Congress Math. Nice 1970, vol. 2, 221-225 ([djvu w OCR](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0221.0226.ocr.djvu), [pdf](http://www.mathunion.org/ICM/ICM1970.2/Main/icm1970.2.0221.0226.ocr.pdf))

* [[Mikhail Gromov]], Papers on h-principle: geometric methods for solving partial differential equations/inequalities and the homotopy structure in the spaces of their solutions, [list](http://www.ihes.fr/~gromov/topics/topic2.html) (with some links)

* {#Haefliger71} [[André Haefliger]], _Lectures on the Theorem of Gromov_, Proceedings of Liverpool Singularities Symposium, II (1969/1970), p. 128-141. Lecture Notes in Math. 209, Springer, Berlin, 1971 ([pdf](https://link.springer.com/content/pdf/10.1007/BFb0068900.pdf)).
* [[John Francis]], _[The h-principle in topology](https://sites.math.northwestern.edu/~jnkf/classes/hprin/)_ (overview [pdf](https://sites.math.northwestern.edu/~jnkf/classes/hprin/1overview.pdf))



See also:

* {#EliasMisha01} Y. Eliashberg, N. Mishachev, _Holonomic approximation and Gromov's h-principle_, [arXiv:math/0101196](https://arxiv.org/abs/math/0101196)



* [London h-principle learning seminar](https://www.mathematik.hu-berlin.de/~wendl/h-principle.html)

* [[Konrad Voelkel]], Helene Sigloch, _Homotopy sheaves and h-principles_, ([pdf](https://www.konradvoelkel.com/wp-content/uploads/homotopy-sheaves.pdf))

* [[Alexander Kupers]], *Three applications of delooping to H-principles*, Geom Dedicata **202** (2019) 103–151  ([arXiv:1701.06788](https://arxiv.org/abs/1701.06788), [doi:10.1007/s10711-018-0405-7](https://doi.org/10.1007/s10711-018-0405-7))


[[!redirects homotopy principle]]