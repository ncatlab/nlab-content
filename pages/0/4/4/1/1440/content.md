
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Higher geometry
+--{: .hide}
[[!include higher geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

A _derived smooth manifold_ is the generalization of a [[smooth manifold]] in [[derived differential geometry]]: the [[derived geometry]] over the [[Lawvere theory]] for [[smooth algebra]]s ($C^\infty$-rings):

it is a [[structured (∞,1)-topos]] whose [[structure sheaf]] of functions is a [[smooth (∞,1)-algebra]].


## Motivation: correction of limits

According to the general logic of [[derived geometry]], passing from [[smooth manifold]]s to _derived smooth manifold_ serves to _correct_ certain [[limit]]s that do exist in [[Diff]] but do not have the correct [[cohomology|cohomological behaviour]]. This concerns notably [[pullback]]s along [[smooth function]]s that are not [[transversal map]]s.


### Pontrjagin-Thom construction

For $X$ a [[compact space|compact]] [[smooth manifold]], by the [[Pontrjagin-Thom construction]] there is a [[smooth function]] $f : S^n \to M O$ from an $n$-sphere to the [[Thom spectrum]] such that if chosen [[transversal map|transversal]] to the zero-[[section]] $B \hookrightarrow M O$ the [[pullback]] $f^* B$

$$
  \array{
     f^* B &\to& B
     \\
     \downarrow && \downarrow
     \\
     S^n &\stackrel{f}{\to}& M O
  }
$$

is a manifold cobordant to $X$, so that $[X] \simeq [f^* B]$ in the [[cobordism ring]] $\Omega$.

By using derived smooth manifolds instead of ordinary smooth manifolds here, the condition that $f$ be transversal to $B$ could be dropped.


### String topology

(...)

### Floer homology

(...)

## Definition

The following definition characterizes the design criterion for derived smooth manifolds as being objects for which homotopy-intersections 

$$
  A \cap_X B := A \times_X^h B
$$

preserve the [[cup product]] in the [[cobordism ring]]

$$
  [A] \smile [B] \simeq [A \cap_X B]
  \,.
$$ 


+-- {: .un_defn}
###### Definition

We say an [[(∞,1)-category]] $C$ supports **derived cup products for cobordisms** if

* it is equipped with a [[full and faithful functor]]

  $$
    i : Diff \hookrightarrow C
  $$

  embedding the category of [[smooth manifold]]s into it;

* for any two submanifolds $A \to X \leftarrow B$ (transversal or not) the [[(∞,1)-pullback]] 

  $$
    A \cap_X B := i(A) \times_{i(X)} i(B)
  $$

  exists in $C$;

* if $A \to X \leftarrow B$ happen to be [[transverse map]]s then

  $$
    i(A \times_X B) \simeq i(A) \times_{i(X)} i(B)
    \,,
  $$

  with the image under $i$ of the ordinary [[pullback]] in [[Diff]] on the left;

* $i$ preserves the [[terminal object]];

* (...nice interaction with underlying topological spaces...)

* for each $X \in Diff$ there is a _derived cobordism ring_
  $\Omega(X)$ such that ...

* for any submanifolds $A \to X \leftarrow B$ we have

  $$
    [A] \smile [B] = [A \cap_X B]  
  $$

  in $\Omega(X)$

  (...)

=--

A central statement about derived smooth manifolds will be

+-- {: .un_theorem}
###### Theorem

The $(\infty,1)$-category of derived smooth manifolds has derived cup products for cobordisms.

=--

This is ([Spivak, theorem 1.8](#Spivak)).

## Related concepts

* [[dg-manifold]]


## References

The definition of derived smooth manifolds is indicated at the very end of 

* [[Jacob Lurie]], _[[Structured Spaces]]_ .

A detailed construction and discjussion in terms of the [[model category]] [[presentable (∞,1)-category|presentation]] by [[homotopy T-algebra]]s is in

* {#Spivak08} {#Spivak} [[David Spivak]], _Derived smooth manifolds_, Duke Math. J. **153** 1 (2010) 22-128 &lbrack;[arXiv:0810.5174](http://arxiv.org/abs/0810.5174), [doi:10.1215/00127094-2010-021](https://doi.org/10.1215/00127094-2010-021)&rbrack;

Something similar (derived [[orbifolds]]):

* [[Dominic Joyce]], _D-orbifolds, Kuranishi spaces, and polyfolds_ talk notes (Jan 2010) &lbrack;[pdf](http://people.maths.ox.ac.uk/joyce/dmtalk.pdf), [[Joyce-DOrbifolds.pdf:file]]&rbrack;

Seminar notes:

* [[Urs Schreiber]], _[[schreiber:Seminar on derived differential geometry]]_ (2010)

Further developments:

* Dennis Borisov, Justin Noel, _Simplicial approach to derived differential manifolds_ ([arXiv:1112.0033](http://arxiv.org/abs/1112.0033))

* {#CarchediSteffens19} [[David Carchedi]], [[Pelle Steffens]], _On the universal property of derived manifolds_ &lbrack;[arXiv:1905.06195](https://arxiv.org/abs/1905.06195)&rbrack; 

  > ([[universal property]] of the [[(infinity,1)-category]] of derived smooth manifolds)

* [[David Carchedi]], *Derived Manifolds as Differential Graded Manifolds* &lbrack;[arXiv:2303.11140](https://arxiv.org/abs/2303.11140)&rbrack;

* [[Gregory Taroyan]], *Equivalent models of derived stacks* &lbrack;[arXiv:2303.12699](https://arxiv.org/abs/2303.12699)&rbrack;


* [[Pelle Steffens]], *Derived $C^\infty$-Geometry I: Foundations* &lbrack;[arXiv:2304.08671](https://arxiv.org/abs/2304.08671)&rbrack;




[[!redirects derived smooth manifolds]]

[[!redirects derived manifold]]
[[!redirects derived manifolds]]

