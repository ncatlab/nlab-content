
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea 

The _Barratt-Eccles operad_ $\mathcal{E}$ is a specific realization of an [[E-infinity operad]], a cofibrant [[resolution]] of the [[commutative operad]] (in the [[model structure on operads]]).

As a [[topological operad]] it is given by $\mathcal{E}_n := E \Sigma_n$, the [[universal principal bundle]] for the [[symmetric group]] $\Sigma_n$. As an [[sSet]]-operad it has $\mathcal{E}_n = N(\Sigma_n // \Sigma_n)$, the [[nerve]] of the [[action groupoid]] of $\Sigma_n$ acting on itself.


## Definition

### As a simplicial operad

We give the definition of the Barratt-Eccles operad as an object of the category of multi-colored [[symmetric operad|symmetric]] [[simplicial operads]] ([[sSet]]-[[enriched category|enriched]] [[symmetric multicategories]]). (See [Berger-Fress, section 1.1.5 ](#BerFre01).)

The **Barratt-Eccles operad** $\mathcal{E}$ is the operad defined as follows.

It has a single color.

For $n  \in \mathbb{N}$, its [[simplicial set]] $\mathcal{E}(n)$ of $n$-ary operations is the [[nerve]] $N(\Sigma_n//\Sigma_n)$ of the [[action groupoid]] $\Sigma_n//\Sigma_n$ of the [[symmetric group]] $\Sigma_n$ permuting $n$ elements acting by right multiplication on itself.

$$
  \mathcal{E}(n) := N(\Sigma_n // \Sigma_n)
  \,.
$$

Explicitly, this is the [[simplicial set]] whose $k$-cells are $(k+1)$-tuples of group elements

$$
  \mathcal{E}(n)_k =_{iso} (\Sigma_n)^{\times k+1}
  \,.
$$

Regarded as the nerve of the action groupoid, the face maps on $\mathcal{E}(n)$ are given by multiplication in $\Sigma_n$

$$
  d_i (g_0, g_1, \cdots, g_k)
  =
  g_0, \cdots, g_{i-1}, g_i \cdot g_{i+1}, g_{i+2}, \cdots, g_k
  \;\;\;\;\;
  0 \leq i \leq k
  \,.
$$

But, alternatively, we can parameterize $\mathcal{E}(n)_k$ by the tuples

$$
  (w_0, w_1, \cdots, w_k) :=
  (g_0, g_0 \cdot g_1, g_0 \cdot g_1 \cdot g_2, 
  \cdots, \prod_{i=0}^{k} g_i)
  \,.
$$

In terms of this the $i$th face map is given simply by omitting the $i$th entry

$$
  d_i(w_0, \cdots, w_k) = (w_0, \cdots, \hat w_i, \cdots, w_k)
  \,.
$$

The $i$th degeneracy map is given by repeating the $i$th entry

$$
  s_i (w_0, \cdots, w_n)
  :=
  (w_0, \cdots, w_{i-1}, w_i, w_i, w_{i+1}, \cdots, w_n)
  \;\;\;
  0 \leq i \leq n
  \,.
$$

In terms of this, the $\Sigma_n$-[[action]] on $\mathcal{E}(n)$ (giving the structure of a [[symmetric operad]]) is then the [[diagonal]] action

$$
  \sigma \cdot (w_0, w_1, \cdots, w_k) 
  :=
  (\sigma \cdot w_0, \sigma \cdot w_1, \cdots, \sigma \cdot w_k)
  \,.
$$

The composition operations in the operad

$$
  \mathcal{E}(r) \times (\mathcal{E}(n_1) \times \cdots \times \mathcal{E}(n_r))
  \to 
  \mathcal{E}(n_1 + \cdots + n_r)
$$

are the morphisms of simplicial sets which in degree $k$ are maps on tuples, which in each degree $i$ are given by the natural function

$$
  \Sigma_r \times (\Sigma_{n_1} \times \cdots \times \Sigma_{n_r})
  \to 
  \Sigma_{n_1 + \cdots + n_r}
$$

that composes $r$ permutations with a permutation of $r$ elements to a permutation of $\sum_{i = 0}^r n_r$ elements.

(This function is in fact that which gives the composition in [[Assoc]] when regarded as a [[symmetric operad]], $Assoc := Symm(*)$.)

### As a dg-operad

(...)

See ([Berger-Fresse](#BerFre01)).

## Properties

### As a simplicial operad

Each of the simplicial sets $\mathcal{E}(n)$ for $n \in \mathbb{N}$ is [[contractible]]. One way to see this is to observe that $\Sigma_n // \Sigma_n$ is (the [[nerve]] of) the [[pullback]]

$$
  \array{
     \Sigma_n // \Sigma_n
     &\to&
     *
     \\
     \downarrow && \downarrow
     \\
     (\mathbf{B} \Sigma_n)^I &\to& \mathbf{B}\Sigma_n
  }
  \,,
$$
 
where $\mathbf{B}\Sigma_n$ is one-object groupoid with $\Sigma_n$ as its morphisms, $(\mathbf{B}\Sigma_n)^I$ is its [[arrow category]] and the bottom vertical map is evaluation at the source. Since this is an acyclic fibration, so is the top vertical morphism.

It follows that the canonical morphism of simplicial operads

$$
  \mathcal{E} \to Comm
$$

to the [[commutative operad]] (which has $Comm(n) = *$ for all $n \in \mathbb{N}$) is a weak equivalence (in the [[model structure on operads]]). In fact, it is a cofibrant resolution.

### As a dg-operad

(...)

## Related concepts

* [[E-infinity algebra]]

* [[(2,1)-algebraic theory of E-infinity algebras]]

## References

As a [[simplicial operad]], the Barratt-Eccles operad was introduced in 

* [[M. Barratt]], [[P. Eccles]], _On $\Gamma^+$-structures I. A free group functor for stable homotopy theory_, Topology 13 (1974), 25-45.

Its realization as a [[dg-operad]] is discussed in detail in

* C. Berger, _Combinatorial models for real configuration spaces and $E_n$-operads_, [pdf](http://math.unice.fr/~cberger/config.pdf)
* [[Clemens Berger]], [[Benoit Fresse]] _Combinatorial operad actions on cochains_, Math. Proc. Cambridge Philos. Soc. 137 (2004), 135-174, [arXiv:math.AT/0109158](http://arxiv.org/abs/math/0109158), [doi](http://10.1017/S0305004103007138)
{#BerFre01}

* [[Clemens Berger]], [[Benoit Fresse]], _A prismatic decomposition of the Barratt-Eccles operad_, [math.AT/0204326](http://arxiv.org/abs/math/0204326)

Elmendorf and Mandell show that the Barratt-Eccles operad $E\Sigma_*$ is obtained by applying functor $E$ to certain operad $\Sigma_*$ in 

* A.D. Elmendorf, M.A. Mandell, _Rings, modules, and algebras in infinite loop space theory_, Advances in Mathematics __205__, n.1, 2006, pp 163&#8211;228, [arxiv](http://front.math.ucdavis.edu/0403.5403), [doi](http://dx.doi.org/10.1016/j.aim.2005.07.007)

[[!redirects Barratt-Eccles operads]]
