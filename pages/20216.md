
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
#### Differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The Poincaré–Hopf theorem says that for any [[vector field]] $v \in \Gamma(T X)$ with a [[finite set]] of isolated vanishing points $\{x_i\}$ on an [[orientation|orientable]] [[compact topological space|compact]] [[differential manifold]] $X$, the [[sum]] over the $x_i \in X$ of the [[degree of a continuous function|degrees]] of the vector in the vicinity of these points, regarded as [[cohomotopy]] classes 

$$
  v/{\vert v\vert}_{\vert x_i} 
  \;\colon\;
  \partial D_{x_i} \longrightarrow S(T_{x_i} X)
$$

and called the _Poincaré–Hopf [[index]]_ of $f$ at $x_i$

$$
  ind_{x_i}(v)
  \;\coloneqq\;
  deg\big(  v/{\vert v\vert}_{\vert {x_i} } \big)
$$

is given by the [[Euler characteristic]], hence by the value of the [[Euler class]] on the [[tangent bundle]]:

$$
  \chi(X)
  \coloneqq
  \chi[T X]
  \;=\;
  \underset{
    {\text{isolated zero}}
    \atop
    { x_i }
  }{\sum}
  ind_{x_i}(v)
  \,.
$$


\begin{center}
\begin{imagefromfile}
  "file_name": "PHIndices.jpg",
  "width": 570
\end{imagefromfile}
\end{center}


In particular, the existence of a nowhere vanishing [[vector field]] (for which the above [[sum]] is empty) implies that the [[Euler characteristic]] vanishes.

## Related concepts

* [[Hopf degree theorem]]

* [[Gauss-Bonnet theorem]]

* [[twisted cohomotopy]]

## References

Named after [[Henri Poincaré]] and [[Heinz Hopf]].

Textbook accounts:

* {#BottTu82} [[Raoul Bott]], [[Loring Tu]], Chapter 11 of  _[[Differential Forms in Algebraic Topology]]_, Graduate Texts in Mathematics 82, Springer 1982 ([doi:10.1007/BFb0063500](https://doi.org/10.1007/BFb0063500))

* {#DubrovinNovikovFomenko85} B. A. Dubrovin, [[S. P. Novikov]], A. T. Fomenko, section 15.2 of _Modern Geometry — Methods and Applications: Part II: The Geometry and Topology of Manifolds_, Graduate Texts in Mathematics 104, Springer-Verlag New York, 1985 ([doi:10.1007/978-1-4612-1100-6](https://link.springer.com/book/10.1007/978-1-4612-1100-6))

* [[John Milnor]], Chapter 6 of: _Topology from the differential viewpoint_, Princeton University Press, 1997. ([ISBN:9780691048338](https://press.princeton.edu/books/paperback/9780691048338/topology-from-the-differentiable-viewpoint), [pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/milnortop.pdf))

* {#Walschap04} Gerard Walschap, chapter 6.7 of _Metric Structures in Differential Geometry_, Graduate Texts in Mathematics, Springer 2004 

Review:

* Alex Wright, Kael Dixon, _The Poincaré–Hopf theorem_ ([pdf](https://pdfs.semanticscholar.org/cd21/dbffb8cbc3a3636c40a58cb921789b0eaac9.pdf))

* Ariel Hafftka, _Differential topology and the Poincaré–Hopf theorem_ ([pdf](http://www.math.uchicago.edu/~may/VIGRE/VIGRE2009/REUPapers/Hafftka.pdf))

See also:

* Wikipedia, _[Poincaré–Hopf theorem](https://en.wikipedia.org/wiki/Poincar%C3%A9%E2%80%93Hopf_theorem)_


Discussion in a broader perspective of [[K-theory]] and [[index theorems]]:

* Omar Mohsen, _Poincaré–Hopf theorem and groupoids_ ([pdf](https://webusers.imj-prg.fr/uploads//omar.mohsen/Poincare-Hopf.pdf), [[MohsenPHIndex.pdf:file]])


A comment on the version for complex vector fields is in 

* Howard Jacobowitz, _Non-vanishing complex vector fields and the Euler characteristic_ ([arXiv:0901.0893](https://arxiv.org/abs/0901.0893)) 

Generalization to [[orbifolds]]:

* Christopher Seaton, _Two Gauss–Bonnet and Poincaré–Hopf theorems for orbifolds with boundary_, Differential Geometry and its Applications
Volume 26, Issue 1, February 2008, Pages 42-51 ([doi:10.1016/j.difgeo.2007.11.002](https://doi.org/10.1016/j.difgeo.2007.11.002))



[[!redirects Poincaré-Hopf theorem]]
[[!redirects Poincare–Hopf theorem]]
[[!redirects Poincare-Hopf theorem]]

[[!redirects Poincaré–Hopf index theorem]]
[[!redirects Poincaré-Hopf index theorem]]
[[!redirects Poincare–Hopf index theorem]]
[[!redirects Poincare-Hopf index theorem]]
