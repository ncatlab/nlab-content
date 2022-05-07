
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

+-- {: .num_defn }
###### Definition

For $C$ an [[(∞,1)-category]] and $PSh(C)$ its [[(∞,1)-category of (∞,1)-presheaves]], the **$(\infty,1)$-Yoneda embedding** is the [[(∞,1)-functor]]

$$
  y : C \to PSh(C)
$$


given by $y(X) : U \mapsto C(U,X)$.

=--



## Properties

### Yoneda lemma

+-- {: .num_prop }
###### Proposition
**$(\infty,1)$-Yoneda embedding**

Let $C$ be an [[(∞,1)-category]] and $PSh(C) \coloneqq Func(C^\op, \infty Grpd)$ be the corresponding [[(∞,1)-category of (∞,1)-presheaves]]. Then the canonical [[(∞,1)-functor]]

$$
  Y : C \to PSh(C) 
$$

is a [[full and faithful (∞,1)-functor]].

=--

([[Higher Topos Theory|HTT, prop. 5.1.3.1]])



+-- {: .num_prop }
###### Proposition
**$(\infty,1)$-Yoneda theorem**

For $C$ a small $(\infty,1)$-category and $F : C^{op} \to \infty Grpd$ an $(\infty,1)$-functor, the composite

$$
  C^{op} \to PSh_{(\infty,1)}(C)^{op} \stackrel{Hom(-,F)}{\to}
  \infty Grpd
$$

is equivalent to $F$.

=--

([[Higher Topos Theory|HTT, Lemma 5.5.2.1]])

+-- {: .proof}
###### Proof

The statement is a direct consequence of the [[sSet]]-[[enriched category theory|enriched]] [[Yoneda lemma]] by using the fact that the [[(∞,1)-category of (∞,1)-presheaves]] $PSh_{(\infty,1)}(C)$ is modeled by the [[enriched functor category]] $[C^{op}, sSet]_{proj}$ with $C$ regarded as a [[simplicially enriched category]] and using the global [[model structure on simplicial presheaves]].

=--

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

* {#LurieHTT} [[Jacob Lurie]], Prop. 5.1.3.1 and Lemma 5.5.2.1 in: _[[Higher Topos Theory]]_

* MathOverflow, _The Yoneda Lemma for $(\infty,1)$-categories?_ ([MO:9737/381](https://mathoverflow.net/q/9737/381))

Discussion in the context of an [[∞-cosmos]]:

* {#RiehlVerity17} [[Emily Riehl]], [[Dominic Verity]], Section 6 of: _Fibrations and Yoneda's lemma in an $\infty$-cosmos_, Journal of Pure and Applied Algebra Volume 221, Issue 3, March 2017, Pages 499-564 ([arXiv:1506.05500](https://arxiv.org/abs/1506.05500), [doi:10.1016/j.jpaa.2016.07.003](https://doi.org/10.1016/j.jpaa.2016.07.003))



[[!redirects Yoneda lemma for (∞,1)-categories]]
[[!redirects (infinity,1)-Yoneda lemma]]
[[!redirects (∞,1)-Yoneda lemma]]

[[!redirects Yoneda embedding for (∞,1)-categories]]
[[!redirects (∞,1)-Yoneda embedding]]
[[!redirects (infinity,1)-Yoneda embedding]]

[[!redirects Yoneda lemma for infinity-categories]]

