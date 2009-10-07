#Contents#
* automatic table of contents goes here
{:toc}


# Idea #

In every [[lined topos]] $(\mathcal{T}, R)$ there is a canonical notion of standard $n$-[[simplex]] [[internalization|internal]] to $\mathcal{T}$.

A line object $R$ in a [[topos]] $\mathcal{T}$
(i.e. a commutative $k$-algebra object $(R,+,\cdot)$ over a commutative ring object
$(k,+,\cdot)$ in $\mathcal{T}$) naturally gives rise to an [[interval object]] in $\mathcal{T}$, whose "endpoints" are the elements $0_{*}$ and $1_{*}$ in $R$ over
_domain of definition_ the terminal object, i.e. the two morphisms ${*} \stackrel{0}{\to} R \stackrel{1}{\leftarrow} {*}$. 

This construction may be iterated to produce higher dimensional intervals and in particular simplices.

# Definition #

For $(\mathcal{T},R)$ a [[lined topos]] (for instance a [[smooth topos]]) define a [[cosimplicial object]] 

$$
  \Delta_{\mathcal{T}} : \Delta \to \mathcal{T}
$$

iteratively as follows:

* set $\Delta_{\mathcal{T}}^0 := {*}$, the [[terminal object]],

* set $\Delta^1_{\mathcal{T}} := R$, the line object

* let the two face maps of $\Delta^1_{\mathcal{T}}$ be

  $$
    (\Delta^0_{\mathcal{T}} \stackrel{\stackrel{\delta_1}{\to}}{\stackrel{\delta_0}{\to}}
    \Delta^1_{\mathcal{T}})
    :=
    ({*} \stackrel{\stackrel{0_{*}}{\to}}{\stackrel{1_{*}}{\to}}
    R)
  $$

* for $n \geq 2$ define $\Delta^n_{\mathcal{T}}$ iteratively as follows:

  as an object, $\Delta^n$ is the [[pushout]]

  $$
    \array{
     {*} \times \Delta^{n-1} 
      &\stackrel{\delta_0 \times Id}{\to}&
      \Delta^1 \times \Delta^{n-1}
      \\
      \downarrow && \downarrow
     \\
     {*} && \Delta^n
    }
  $$

  this inherits face maps $\delta_i : \Delta^{n-1} \to \Delta_n$ and degeneracy maps $\sigma_i : \Delta^n \to \Delta^{n-1}$ as follows 

+-- {: .query}

[[Urs Schreiber]]: what's the standard reference for the definition of the simplicial structure maps for simplices defined inductively as collapsed cylinders this way?

=--
  

+-- {: .un_remark }
###### Remark
**(collars)**

The above definition yields "colared" simplices in the sense of [[collared cobordism|collared]] [[cobordism]]: as objects in $\mathcal{T}$ each such standard simplex extends beyond the loci where we think of its true boundary is: it has _collars_ at its boundary.

And as for [[collared cobordism]], these _collars_ become _invisible up to equivalence_ as soon as we organize the simplices in a suitable homotopic manner, for instance when forming the [[path infinity-groupoid in a lined topos]].

=--



[[!redirects simplex in a smooth topos]]