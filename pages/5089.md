
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Factorization systems
+--{: .hide}
[[!include factorization systems - contents]]
=--
=--
=--

# $k$-ary factorisation systems
* table of contents
{: toc}

## Idea

A $k$-ary factorization system is a generalization of (binary) [[orthogonal factorization systems]] and [[ternary factorization systems]] to factorizations into a string of $k$ morphisms.


## Definition

For $k \gt 0$ a [[natural number]] and $C$ a [[category]] (or $\infty$-[[infinity-category|category]]), a __$k$-ary factorisation system__ on $C$ consists of $(k - 1)$ factorisation systems $(E_i, M_i)$ (for $0 \lt i \lt k$) on $C$, such that

*  $M_i \subseteq M_{i + 1}$ whenever this is meaningful (equivalently, $E_i \subseteq E_{i - 1}$).

We can extend this to include two other factorisation systems, one for $i = 0$ and one for $i = k$:

*  $M_0$ consists of only [[isomorphisms]]/[[equivalences]] (equivalently, $E_0$ consists of all morphisms), and
*  $M_k$ consists of all morphisms (equivalently, $E_k$ consists of only isomorphisms/equivalences).

Given a $k$-ary factorisation system, the ([[coimage|co]])[[image]] of $(E_i,M_i)$ is the __$i$-(co)image__ of the entire $k$-ary factorisation system.

Note that every (higher) category has a unique $1$-ary factorisation system, since no structure at all is required.  We also say that a [[groupoid]] (or $\infty$-[[infinity-groupoid|groupoid]]) has a (necessarily unique) $0$-ary factorisation system; this makes sense since we have $M_0 = M_k$ (and $E_0 = E_k$) in that case.  A [[discrete category]] has a (necessarily unique) $(-1)$-ary factorisation system.

A $k$-ary factorisation system may also be called a __$k$-step factorisation system__ or a __$(k+1)$-stage factorisation system__.  You can see why if you count the basic morphisms (steps) and objects (stages) that $k - 1$ overlapping factorisation systems produce from a morphism.


## Infinitary factorisation systems

Here is an incomplete attempt at a general definition:

Fix any [[ordinal number]] (or [[opposite poset|opposite]] thereof, or any [[poset]], really) $\alpha$.  Then an __$\alpha$-stage factorisation system__ (in an ambient $\infty$-category $C$) consists of an $\alpha$-indexed family of factorisation systems $(E_i, M_i)$ in $C$ such that:

*  $M_i \subseteq M_j$ whenever $i \leq j$ (equivalently, $E_i \supseteq E_j$ whenever $i \leq j$),
*  each morphism $f\colon X \to Y$ is both the [[inverse limit]] $\underset{i \to \infty}\lim \im_i f$ in the [[slice category]] $C/Y$ and the [[direct limit]] $\underset{i \to -\infty}\colim \coim_i f$ in the [[coslice category]] $X/C$, and
*  for each $f\colon X \to Y$, $\id_Y$ is $\underset{i \to -\infty}\colim \im_i f$ and $\id_X$ is $\underset{i \to \infty}\lim \coim_i f$.

This seems to be correct whenever $\alpha$ really is either an ordinal or the opposite thereof, as well as some other posets such as $\omega^op + \omega$ (which is the poset of [[integers]]), but it seems to be missing something for (for example) $\omega + \omega^op$.  Notice that, when $\alpha$ is *both* an ordinal and the opposite thereof, we recover the above definition of an $(alpha-1)$-ary factorisation system.

## Examples

* For $k = 3$ one speaks of a _[[ternary factorization system]]_. See there for more examples

* In an [[(∞,1)-topos]] the [[(epi, mono) factorization system]] in a [[topos]] splits up to an $\infty$-ary factorization system consisting of the [[(n-epi, n-mono) factorization systems]] (the [[n-image]]-factorization) for all $n \in \mathbb{N}$. This is called the _[[Postnikov system]]_. 



## References

* [Cafe discussion](http://golem.ph.utexas.edu/category/2010/07/ternary_factorization_systems.html) mainly on the ternary version

* [Forum discussion](https://nforum.ncatlab.org/discussion/1629) including the k-ary case, even when k is infinite


[[!redirects k-ary factorization system]]
[[!redirects k-ary factorization systems]]
[[!redirects k-ary factorisation system]]
[[!redirects k-ary factorisation systems]]
[[!redirects n-ary factorization system]]
[[!redirects n-ary factorization systems]]
[[!redirects n-ary factorisation system]]
[[!redirects n-ary factorisation systems]]
[[!redirects alpha-ary factorization system]]
[[!redirects alpha-ary factorization systems]]
[[!redirects alpha-ary factorisation system]]
[[!redirects alpha-ary factorisation systems]]

[[!redirects k-fold factorization system]]
[[!redirects k-fold factorization systems]]
[[!redirects k-fold factorisation system]]
[[!redirects k-fold factorisation systems]]
[[!redirects n-fold factorization system]]
[[!redirects n-fold factorization systems]]
[[!redirects n-fold factorisation system]]
[[!redirects n-fold factorisation systems]]
[[!redirects alpha-fold factorization system]]
[[!redirects alpha-fold factorization systems]]
[[!redirects alpha-fold factorisation system]]
[[!redirects alpha-fold factorisation systems]]

[[!redirects k-step factorization system]]
[[!redirects k-step factorization systems]]
[[!redirects k-step factorisation system]]
[[!redirects k-step factorisation systems]]
[[!redirects n-step factorization system]]
[[!redirects n-step factorization systems]]
[[!redirects n-step factorisation system]]
[[!redirects n-step factorisation systems]]
[[!redirects alpha-step factorization system]]
[[!redirects alpha-step factorization systems]]
[[!redirects alpha-step factorisation system]]
[[!redirects alpha-step factorisation systems]]

[[!redirects k-stage factorization system]]
[[!redirects k-stage factorization systems]]
[[!redirects k-stage factorisation system]]
[[!redirects k-stage factorisation systems]]
[[!redirects n-stage factorization system]]
[[!redirects n-stage factorization systems]]
[[!redirects n-stage factorisation system]]
[[!redirects n-stage factorisation systems]]
[[!redirects alpha-stage factorization system]]
[[!redirects alpha-stage factorization systems]]
[[!redirects alpha-stage factorisation system]]
[[!redirects alpha-stage factorisation systems]]

[[!redirects infinitary factorization system]]
[[!redirects infinitary factorization systems]]
