
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $\infty$-Lie theory
+--{: .hide}
[[!include infinity-Lie theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

For $\mathfrak{g}=\bigoplus_{i}\mathfrak{g}^i$ a [[differential graded Lie algebra]], let $MC(\mathfrak{g})$ be the set of [[Maurer-Cartan element]]s, i.e.,

$$
MC(\mathfrak{g})=\{x\in \mathfrak{g}^1 \;|\; dx+\frac{1}{2}[x,x]=0\}
$$

One thinks of element in this set as _flat $\mathfrak{g}$-[[connection on a bundle|connection]]s: indeed

$$
x\in MC(\mathfrak{g}) \Leftrightarrow (d+[x,-])^2=0.
$$

The subspace $\mathfrak{g}^0$ of $\mathfrak{g}$ is a [[Lie algebra]]; the group 

$$
  exp(\mathfrak{g}^0)
$$

acts on as a group of [[gauge transformation]]s on the set of $\mathfrak{g}$-connections (by conjugation), and this action preserves the subset of flat connections. Hence we have a _gauge action_ of  $exp(\mathfrak{g}^0)$ on $MC(\mathfrak{g})$:
$$
e^{a}(d+[x,-])e^{-a}=d+[e^a*x,-].
$$
Explicitely,
$$
e^a*x=x+\sum_{n=0}^\infty \frac{([a,-])^n}{(n+1)!}([a,x]-da)
$$

The _Deligne groupoid_ $Del(\mathfrak{g})$ of the dgla $\mathfrak{g}$ is the [[action groupoid]]

$$
  Del(\mathfrak{g})=MC(\mathfrak{g})// exp(\mathfrak{g}^0)
$$


## Examples

For $\mathfrak{g}$ a [[nLab:Lie algebra|Lie algebra]] this is the [[delooping|delooping groupoid]] $\mathbf{B} exp(\mathfrak{g})=*//exp(\mathfrak{g})$.

## Related concepts

* [[Lie integration]], [[deformation theory]]


## References

Some of the ideas of Deligne on deformation theory were transmitted via

* W. M. Goldman, J. J. Millson, _The deformation theory of representations of fundamental groups of compact K&#228;hler manifolds_, Inst. Hautes &#201;tudes Sci. Publ. Math. __67__ (1988), 43&#8211;96, [MR90b:32041](http://www.ams.org/mathscinet-getitem?mr=972343), [numdam](http://www.numdam.org/item?id=PMIHES_1988__67__43_0)

but the later study of the Deligne 2-groupoid is from a letter of Deligne to Breen from 1994 (see [[Ezra Getzler]]'s webpage; the letter page is not to be linked). See related 

* [[E. Getzler]], _A Darboux theorem for Hamiltonian operators in the formal calculus of variations_, Duke Math. J. __111__, n. 3 (2002), 535-560, [MR2003e:32026](http://www.ams.org/mathscinet-getitem?mr=1885831), [doi](http://dx.doi.org/10.1215/S0012-7094-02-11136-3)

Other references
* V. Hinich,  _Descent of Deligne groupoids_, Int. Math. Research Notices,  1997, n. 5, 223-239, [alg-geom/9606010](http://arxiv.org/abs/alg-geom/9606010); _DG coalgebras as formal stacks_, J. Pure Appl. Algebra __162__ (2001), 209-250, [pdf](http://math.haifa.ac.il/hinich/WEB/mypapers/dgc.pdf) 
* Amnon Yekutieli, _MC elements in complete DG Lie algebras_, [arXiv/1103.1035](http://arxiv.org/abs/1103.1035)

A careful analysis extends the assignment of the Deligne groupoid to a Maurer-Cartan pseudofunctor, see part 2 of 

* Alexander I. Efimov, Valery A. Lunts, [[Dmitri Orlov|Dmitri O. Orlov]], _Deformation theory of objects in homotopy and derived categories_ 
   * _I: general theory_ [arXiv:math/0702838](http://arxiv.org/abs/math/0702838);
   * _II: pro-representability of the deformation functor_ [arXiv:math/0702839](http://arxiv.org/abs/math/0702839);
   * _III: abelian categories_ [arXiv:math/0702840](http://arxiv.org/abs/math/0702840)

Parts of the above text is taken from

* [[Domenico Fiorenza]], _[[domenicofiorenza:The periods map of a complex projective manifold. An oo-category perspective]]_



[[!redirects Deligne groupoids]]