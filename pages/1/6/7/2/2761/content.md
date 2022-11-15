
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Yoneda lemma
+--{: .hide}
[[!include Yoneda lemma - contents]]
=--
#### $(\infty,1)$-Category theory
+--{: .hide}
[[!include quasi-category theory contents]]
=--
=--
=--



# Contents#
* table of contents
{: toc}


## Idea

The statement of the [[Yoneda lemma]] generalizes from [[categories]] to [[(∞,1)-categories]].


## Yoneda embedding 
 {#YonedaEmbedding}

\begin{definition}
For $C$ an [[(∞,1)-category]] and $PSh(C)$ its [[(∞,1)-category of (∞,1)-presheaves]], the **$(\infty,1)$-Yoneda embedding** is the [[(∞,1)-functor]]

$$
  y \colon C \to PSh(C)
$$


given by $y(X) \colon U \mapsto C(U,X)$.
\end{definition}

Seen under the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]] this is [Riehl & Verity 2018, Def. 6.2.3](#RiehlVerity18).



## Properties

### Yoneda lemma
 {#YonedaLemma}

\begin{prop}
**$(\infty,1)$-Yoneda embedding**

Let $C$ be an [[(∞,1)-category]] and $PSh(C) \coloneqq Func(C^\op, \infty Grpd)$ be the corresponding [[(∞,1)-category of (∞,1)-presheaves]]. Then the canonical [[(∞,1)-functor]]

$$
  Y \colon C \to PSh(C) 
$$

is a [[full and faithful (∞,1)-functor]].
\end{prop}

For small $\infty$-categories this is [[Higher Topos Theory|HTT, prop. 5.1.3.1]]. For possibly large $\infty$-categories see [Riehl & Verity 2018, Thm. 7.2.22](#RiehlVerity18) (which considers $\infty$-presheaves regarded under the [[(infinity,1)-Grothendieck construction|$\infty$-Grothendieck construction]]) and [[Kerodon]], [Thm. 8.2.5.4](https://kerodon.net/tag/03NJ).



+-- {: .num_prop }
###### Proposition
**$(\infty,1)$-Yoneda theorem**

For $C$ a small $(\infty,1)$-category and $F \colon C^{op} \to \infty Grpd$ an $(\infty,1)$-functor, the composite

$$
  C^{op} 
   \to PSh_{(\infty,1)}(C)^{op} \stackrel{Hom(-,F)}{\to}
  \infty Grpd
$$

is equivalent to $F$.

=--

For small $\infty$-sites this is [[Higher Topos Theory|HTT, Lemma 5.5.2.1]]. For possibly large $\infty$-sites see [[Kerodon]], [Prop. 8.2.1.3](https://kerodon.net/tag/03M5).

+-- {: .proof}
###### Proof

For small $\infty$-sites, the statement may be obtained as a consequence of the [[sSet]]-[[enriched category theory|enriched]] [[Yoneda lemma]] by using the fact that the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ is modeled by the [[enriched functor category]] $[C^{op}, sSet]_{proj}$ with $C$ regarded as a [[simplicially enriched category]] and using the global [[model structure on simplicial presheaves]].

=--


### Naturality
 {#Naturality}

+-- {: .num_prop }

###### Proposition

$PSh$ can be extended to a functor $PSh \colon (\infty,1)Cat \to (\infty,1)\widehat{Cat}$ so that the yoneda embedding $C \to PSh(C)$ is a natural transformation.

Here, $(\infty,1)\widehat{Cat}$ is the (∞,1)-category of large (∞,1)-categories.

=--

This follows from ([[Higher Topos Theory|HTT, prop. 5.3.6.10]]), together with the identification of $PSh(C)$ with the category obtained by freely adjoining small colimits to $C$. This functor is locally left adjoint to the contravariant functor $C \mapsto Func(C^\op, \infty Grpd)$.



### Preservation of limits


+-- {: .num_prop }
###### Proposition

The $(\infty,1)$-Yoneda embedding $y : C \to PSh(C)$ preserves all [[(∞,1)-limit]]s that exist in $C$.

=--

([[Higher Topos Theory|HTT, prop. 5.1.3.2]])


### Local Yoneda embedding 
  {#LocalYonedaEmbedding}


+-- {: .num_prop }
###### Proposition

For $C$ an [[(∞,1)-site]] and $\mathcal{X}$ an [[(∞,1)-topos]], [[(∞,1)-geometric morphism]]s $(f^* \dashv f_*) Sh(C) \stackrel{\overset{f^*}{\leftarrow}}{\underset{f_*}{\to}} \mathcal{X}$ from the [[(∞,1)-sheaf (∞,1)-topos]] $Sh(C)$ to $\mathcal{X}$ correspond to the **local** [[(∞,1)-functor]]s $f^* : C \to \mathcal{X}$, those that 

* are left [[exact (∞,1)-functor]]s;

* send [[covering]] families $\{U_i \to X\}$ in $\mathcal{G}$ to [[effective epimorphism]]

  $$
    \coprod_i f^*(U_i) \to f^*(X)
    \,.
  $$

More preseicely, the [[(∞,1)-functor]]

$$
  Topos(\mathcal{X}, Sh_{(\infty,1)}(\mathcal{G}))
  \stackrel{L}{\to}
  Topos(\mathcal{X}, PSh_{(\infty,1)}(\mathcal{G}))
  \stackrel{y}{\to}
  Func(\mathcal{G}, \mathcal{X})
$$

given by precomposition of [[inverse image]] functors by [[∞-stackification]] and by the [(∞,1)-Yoneda embedding](#YonedaEmbedding)
is a [[full and faithful (∞,1)-functor]] and its essential image is spanned by these local morphisms.

=--

([[Higher Topos Theory|HTT, prop. 6.2.3.20]])

## Related concepts

* [[Brown representability theorem]]

* [[Yoneda Lemma for higher categories]]

## References

* {#LurieHTT} [[Jacob Lurie]], Prop. 5.1.3.1 and Lemma 5.5.2.1 in: _[[Higher Topos Theory]]_ (2009)

* {#RiehlVerity18} [[Emily Riehl]], [[Dominic Verity]], Def. 6.2.3 and Thm. 7.2.22 in: *The comprehension construction*, Higher Structures **2** 1 (2018)  ([arXiv:1706.10023](https://arxiv.org/abs/1706.10023), [hs:39](http://137.111.162.45/index.php/higher_structures/article/view/39))

* MathOverflow, _The Yoneda Lemma for $(\infty,1)$-categories?_ ([MO:9737/381](https://mathoverflow.net/q/9737/381))

* {#Kerodon} [[Kerodon]], Part 2, Chapter 8: *The Yoneda Embedding* $[$[kerodon:03JA](https://kerodon.net/tag/03JA), esp. [Prop. 8.2.1.3](https://kerodon.net/tag/03M5) and [Thm. 8.2.5.4](https://kerodon.net/tag/03NJ)$]$

Discussion in the context of an [[∞-cosmos]]:

* {#RiehlVerity17} [[Emily Riehl]], [[Dominic Verity]], Section 6 of: _Fibrations and Yoneda's lemma in an $\infty$-cosmos_, Journal of Pure and Applied Algebra Volume 221, Issue 3, March 2017, Pages 499-564 ([arXiv:1506.05500](https://arxiv.org/abs/1506.05500), [doi:10.1016/j.jpaa.2016.07.003](https://doi.org/10.1016/j.jpaa.2016.07.003))

Discussion [[category internal to an (infinity,1)-topos|internal to]] any [[(∞,1)-topos]]:

* [[Louis Martini]], *Yoneda's lemma for internal higher categories*, &lbrack;[arXiv:2103.17141](https://arxiv.org/abs/2103.17141)&rbrack;


[[!redirects Yoneda lemma for (∞,1)-categories]]
[[!redirects (infinity,1)-Yoneda lemma]]
[[!redirects (∞,1)-Yoneda lemma]]

[[!redirects Yoneda embedding for (∞,1)-categories]]
[[!redirects (∞,1)-Yoneda embedding]]
[[!redirects (infinity,1)-Yoneda embedding]]

[[!redirects Yoneda lemma for infinity-categories]]

[[!redirects Yoneda lemma for infinity1-categories]]
