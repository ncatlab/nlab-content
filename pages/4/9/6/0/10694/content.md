
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A _May spectral sequence_ ([May 64](#May64), [May 74](#May74), [Ravenel 86, 3.2](#Ravenel86)) is a certain type of [[spectral sequence]] that computes the second page of the [[classical Adams spectral sequence]]. More generally, it computes [[Ext]]-groups (or [[Cotor]]-groups, via [this lemma](cotensor+product#ComoduleHomInTermsOfCotensorProduct)) of [[comodules]] over [[commutative Hopf algebras]] (the [[dual Steenrod algebra]] in the classical case). 

The May spectral sequence is the [[spectral sequence of a filtered complex]] induced by filtering the canonical (but intractable) [[bar complex]] model for [[Ext]]/[[Cotor]] by co-powers of the unit co-ideal of the given Hopf algebra (see [Ravenel 86, chapter 3, section 2](#Ravenel86), [Kochman 96, section 5.3](#Kochman96)).

## Construction

Throughout, let $A$ be a [[commutative ring]] and let $\Gamma$ be a graded [[commutative Hopf algebroid|commutative Hopf algebra]] over $A$. We write $(\Gamma,A)$ for this data.


> sketch


lemma. if $A = \mathbb{F}_2$ and $\Gamma$ is an exterior algebra on [[primitive elements]] $\{x_i\}$,  then 

$$
  Ext_\Gamma(A,A) \simeq A[x_1, x_2, \cdots]
$$

(if $A$ is a field of characteristic other than 2, this remains true if all the $x_i$ are odd graded)

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))


lemma. If $(\Gamma,A)$ is filtered and $N_1$ and $N_2$ are compatibly filtered comodules, then there is a spectral sequence

$$
  \mathcal{E}_1
  =
  Ext_{gr \Gamma}(gr N_1, gr N_2)
  \;\Rightarrow\;
  Ext_{\Gamma}(N_1, N_2)
$$

converging to the [[Ext]] over $\Gamma$, with first page the Ext over the [[associated graded]] $gr \Gamma$.

([Ravenel 86, lemma 3.1.9](#Ravenel86), [Kochman 96, prop. 3.7.5](#Kochman96))

Proof: The filtering induces a filtering on the standard bar complex which computes $Ext_\Gamma$. The spectral sequence in question is the corresponding [[spectral sequence of a filtered complex]].

$\,$

Let now $A \coloneqq \mathbb{F}_2$,  $\Gamma \coloneqq \mathcal{A}^\bullet_{\mathbb{F}_2}$ be the mod 2 [[dual Steenrod algebra]]. Recall that as a $\mathbb{F}_2$-algebra this is

$$
  \mathcal{A}^\bullet_{\mathbb{F}_2} 
  = 
  \mathbb{F}_2[\xi_1, \xi_2, \cdots]
  \,.
$$

and the coproduct is given by

$$
  \Psi(\xi_n)
  =
  \underoverset{k = 0}{n}{\sum} \xi_{n-k}^{p^k} \otimes \xi_k
  \,,
$$

where $\xi_0 \coloneqq 1$.


Choose degrees of generators as

$$
  {\vert \xi_i^{2^j} \vert}
  \coloneqq
  2i-1
$$

([Ravenel 86, p.69](#Ravenel86)) and consider the [[filtration]]

$$
  \cdots 
   \subset
  F^p \mathcal{A}^\ast_{\mathbb{F}_2}
   \subset
  F^{p+1} \mathcal{A}^\ast_{\mathbb{F}_2}
    \subset 
  \cdots 
    \subset
  \mathcal{A}^\ast_{\mathbb{F}_2}
$$

which at filtering stage $p$ contains all elements of total degree $\leq p$.

Observe then that

$$
  \begin{aligned}
    \Psi(\xi_n)
    &
   =
   \underset{deg = 2n-1}{\underbrace{\xi_{n} \otimes 1}}
   +
    \underoverset{0 \lt k \lt n}{}{\sum} 
     \underset{deg = 2n-2}{\underbrace{\xi_{n-k}^{p^k} \otimes \xi_k}}
   +
    \underset{deg = 2n-1}{\underbrace{1 \otimes \xi_n}}
  \end{aligned}
  \,.
$$

This means that in the [[associated graded]] $gr_\bullet \mathcal{A}^\ast_{\mathbb{F}_2}$ all the generators $\xi_n$ become [[primitive elements]]:

$$
  \begin{aligned}
    \Psi(\xi_n)
    &
   =
   \underset{deg = 2n-1}{\underbrace{\xi_{n} \otimes 1}}
   +
    \underset{deg = 2n-1}{\underbrace{1 \otimes \xi_n}}
   \;\;\;\;
   \in
   F^{2n-1}\mathcal{A}^\ast_{\mathbb{F}_2}/F^{2n-2}\mathcal{A}^\ast_{\mathbb{F}_2}
  \end{aligned}
  \,.
$$


By Hopf structure theory this means that $gr\mathcal{A}^\ast_{\mathbb{F}_2}$ is an exterior algebra. Hence the above lemma applies and says that

$$
  Ext_{gr \mathcal{A}^\bullet_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  =
  P(\{\xi_n^{2^j}\})  
$$

Finally then the other lemma says that this is the first page of a spectral sequence of the form

$$
  \mathcal{E}_1 
  = 
  P(\{\xi_n^{2^j}\})
  \;\Rightarrow\;
  Ext_{\mathcal{A}^\ast_{\mathbb{F}_2}}(\mathbb{F}_2,\mathbb{F}_2)
  \,.
$$

By that same lemma, the differentials on any $r$-page are the restriction of the differentials of the bar complex to the $r$-almost cycles ([prop.](Introduction+to+Stable+homotopy+theory+--+I#DifferentialsOnAlmostChains)). The differential of the bar complex is the alternating sum of the coproduct on $\Gamma$. Hence on generators 

$$
  d \xi_n^{2^k}
  =
  \underoverset{j = 0}{n}{\sum}  \xi_{n-j}^{2^{k+j}} \otimes \xi_j^{2^k}
  \,.
$$

This is the May spectral sequence.



## Related concepts

* [[Curtis algorithm]]

## References

The origin is in 

* {#May64} [[Peter May]],  _The cohomology of restricted Lie algebras and of Hopf algebras; application to the Steenrod algebra_, (Thesis) Journal of Algebra 3, 123-146 (1966) ([pdf](http://math.uchicago.edu/~may/PAPERS/3.pdf))
 

More on the $E_2$-term is in 

* {#May74} [[Peter May]] _The Steenrod algebra and its associated graded algebra_, University of Chicago preprint, 1974.

A computation of the first 70 differentials for the case of the [[Steenrod algebra]] is in 

* [[Martin Tangora]], _On the cohomology of the Steenrod algebra_, Math. Z. 116 (1970), 18&#8211;64.

Review includes

* {#Ravenel86} [[Doug Ravenel]], chapter 3, section 2 of _[[Complex cobordism and stable homotopy groups of spheres]]_, 1986

* {#Kochman96} [[Stanley Kochman]], section 5.3 of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* Wikipedia, _[May spectral sequence](http://en.wikipedia.org/wiki/May_spectral_sequence)_

[[!redirects May spectral sequences]]