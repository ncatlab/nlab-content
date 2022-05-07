
> This entry is about the notion of _Weil algebra_ as the algebra of functions on an infinitesimally thickened point. For the concept of Weil algebra in Lie theory see [[Weil algebra]].

***

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Formal geometry
+--{: .hide}
[[!include formal geometry -- contents]]
=--
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Compact objects
+--{: .hide}
[[!include compact object - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

### Abstractly

In [[differential cohesion]] an [[object]]/[[type]] $D$ is an _infinitesimally thickened point_ if its corresponding [[reduced object]] is the [[terminal object]],

$$
  \Re(D) \simeq *
  \,,
$$

hence it is an [[anti-reduced object]].

### In the standard type of model

An _infinitesimally thickened point_ is -- under [[Isbell duality]] -- the formal dual of an $R$-[[algebra]] of the form

$$
  A = R \oplus W
  \,,
$$

where $W$ is a [[module]] of finite rank over $R$ and consisting of nilpotent elements in the algebra $A$.

+-- {: .num_remark #WeilAlgebra}
###### Remark
**on terminology** 

In the literature on [[synthetic differential geometry]] an algebra $A$ of this form is also called a **Weil algebra**. Notice that this is unrelated to the notion of Weil algebra in [[Lie theory]]. For more on that, see [[Weil algebra]]. 

Over more general base fields, this is called a **[[local Artin algebra]]**.

=--


## Examples

The smallest nontrivial example is the space dual to the [[ring of dual numbers]]. This is the point with "minimal infinitesimal thickening". 

This is a special case of the following


+-- {: .num_defn #JetAlgebra}
###### Definition

For $n , k \in \mathbb{N}$, the _jet algebra_ $C^\infty(\mathbb{D}^n(k))$ is the [[quotient]]

$$
  C^\infty(\mathbb{D}^n(k))
  =
  C^\infty(\mathbb{R}^n)/ I^{k+1}
  \,,
$$

where $I = (x_1, \cdots, x_n)$.

The [[formal dual]] [[smooth locus]] $\mathbb{D}^n(k)$ is the "order-$k$ infinitesimal $n$-disk".

=--

For $X$ an $n$-dimensional [[smooth manifold]] and $E \overset{p}{\to} X$ a [[bundle]], and $\mathbb{D}^n(k) \hookrightarrow X$ the order-$k$ infinitesimal $n$-disk (def. \ref{JetAlgebra}) in $X$ around a point $x \in X$, then a lift

$$
  \array{
     \mathbb{D}^n(k) && \longrightarrow && E
     \\
     & \searrow && \swarrow_{\mathrlap{p}}
     \\
     && X
  }
$$

is a $k$-[[jet]] of a [[section]] of $E$ at $x$. The collection of all of these constitutes the order-$k$ [[jet bundle]] of $E$.

+-- {: .num_prop}
###### Proposition

Every Weil algebra (remark \ref{WeilAlgebra}) is a [[quotient]] of a jet algebra (def. \ref{JetAlgebra}).

=--

(e.g. [Carchedi-Roytenberg 12, prop. 4.43](#CarchediRoytenberg12))

A class of examples are the spaces $\tilde D(n,r)$ of $r$-tuples of infinitesimal neighbours of the origin of $R^n$, that are each also infinitesimal neighbours of each other. Their Weil algebras of functions are a model for the degree $r$-[[differential forms]]. Details on this are at <a href="http://ncatlab.org/nlab/show/infinitesimal+object#SpacOfInfSimpl">spaces of infinitesimal k-simplices</a>.





## Applications

The [[site]] of definition for the [[Cahiers topos]] is the category of spaces that are products of an $R^n$ with the dual of a  Weil algebra. So these are infinitesimally thickened [[Cartesian space]]s. These are typically sufficient as test spaces for more general spaces.


## Related concepts

* [[superpoint]]

* [[formal disk]]

* [[infinitesimal extension]]

## References

* {#CarchediRoytenberg12} [[David Carchedi]], [[Dmitry Roytenberg]], _On Theories of Superalgebras of Differentiable Functions_ ([arXiv:1211.6134](http://arxiv.org/abs/1211.6134))

[[!include cohesion - table]]

[[!redirects infinitesimally thickened points]]

[[!redirects fat point]]
[[!redirects fat points]]