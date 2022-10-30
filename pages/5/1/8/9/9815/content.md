

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Motivic cohomology
+--{: .hide}
[[!include motivic cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

Where the [[category of pure motives]] has [[smooth variety|smooth]] [[projective varieties]] as its [[objects]], the _category of mixed motives_ is supposed to be constructed from all [[smooth varieties]].  

The category of mixed motives is supposed to be an [[abelian category|abelian]] [[tensor category]] which contains the [[pure motives]] as the [[full subcategory]] of [[semisimple objects]].  

So far there is no realisation of such a category, but there are proposals by [[Vladimir Voevodsky]] and [[Marc Levine]] of [[triangulated categories]] that behave as its [[derived category]] is expected to.

## Voevodsky's mixed motives

Here we construct [[Voevodsky]]'s [[triangulated category]] of mixed motives following [Cisinski-Deglise](#CD).

1.  Let $S$ be a [[regular scheme|regular]] and [[noetherian scheme|noetherian]] base [[scheme]].   Let $Sm_S$ be the category of [[schemes]] [[smooth]] and of [[finite type]] over $S$.  Let $N_S^{tr}$ denote the [[closed symmetric monoidal category]] of [[Nisnevich sheaves with transfer]].  We will write $L_S[X]$ for the [[sheaf]] [[representable|represented]] by $X \in Sm_S$.

2.  Let $G_S$ denote the set of representable sheaves and $H_S$ as the set of [[complexes]] in  $Cpx(N_S^{tr})$ which are the [[cones]] of morphisms $L_S[Y] \to L_S[X]$  induced by [[hypercovers]] $Y\to X$.  The pair $(G_S, H_S)$ then defines a weakly flat [[descent structure]] (in the sense of [Cisinski-Deglise](#CD), see discussion at [[model structure on chain complexes]]) and therefore induces a [[symmetric monoidal model structure]] on $Cpx(N_S^{tr})$ where the [[weak equivalences]] are the [[quasi-isomorphisms]].

3.  Let $\mathcal{T}_S$ denote the set of [[complexes]] $Cone(L_S[A^1_X] \to L_S[X])$ where $A^1_X = A^1_S \times_S X$ is the [[affine line]] over $X$.  Call a [[complex]] $K$ **$A^1$-local** if $Hom_{D(A)}(T, K[n]) = 0$ for all $T \in \mathcal{T}$ and integers $n$.   Equivalently, the [[Nisnevich]] [[hypercohomology sheaves]] are [[homotopy invariant]].  In particular, for $F$ [[fibrant]] with respect to the above [[model structure]], $F$ is $A^1$-local iff the morphism $F(X) \to F(A^1_X)$ induced by the projection is a [[quasi-isomorphism]] for all $X \in Sm_S$.  This is again equivalent to the [[cohomology]] [[presheaves]] of $F$ being [[homotopy invariant]].

4.  Consider the [[left Bousfield localization]] of the above [[model structure]] at the class of morphisms $0 \to T[n]$ for $T \in \mathcal{T}_S$ and $n \in \mathbf{Z}$.  The [[fibrant objects]] are $G_S$-local and $A^1$-local complexes.  One can prove that this [[model structure]] is still [[symmetric monoidal model structure||symmetric monoidal]].

4.  The [[homotopy category]] of this [[model category]] is called the **triangulated category of effective motives** over $S$, denoted $DM^{eff}(S)$.  It is canonically equivalent to the [[full subcategory]] of the [[derived category]] $D(N_S^{tr})$ spanned by Nisnevich fibrant and $A^1$-local complexes.

5.  (introduce symmetric Tate spectra and DM(S))

## Related concepts

* [[motive]]

  * mixed motive,

    * [[mixed Tate motive]]

  * [[pure motive]], 

    * [[Chow motive]], [[numerical motive]]

  * [[Voevodsky motive]]

  * [[noncommutative motive]]

* [[motivic cohomology]]

## References

* [[Marc Levine]], _Mixed Motives_, Handbook of K-theory ([pdf](http://www.uni-due.de/~bm0032/publ/MixMotKHB.pdf))

* [[Denis-Charles Cisinski]], [[Frédéric Déglise]], _Local and stable homological algebra in Grothendieck abelian categories_, [arXiv](http://arxiv.org/abs/0712.3296).
{#CD}

Section 8.3 of 

* [[Alain Connes]], [[Matilde Marcolli]], _[[Noncommutative Geometry, Quantum Fields and Motives]]_  ([pdf](http://www.alainconnes.org/docs/bookwebfinal.pdf))


[[!redirects mixed motives]]