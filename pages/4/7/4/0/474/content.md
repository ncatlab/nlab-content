
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



#Contents#
* table of contents
{:toc}


## Idea

### For directed spaces

In generalization to how a [[topological space]] $X$ has a [[fundamental groupoid]] whose [[morphism]]s are [[homotopy]]-classes of paths in $X$ and whose composition operation is the concatenation of paths, a [[directed space]] has a **fundamental category** whose morphisms are _directed_ paths in $X$.

### For stratified spaces

A [[stratified space]] has a 'fundamental [[(infinity,n)-category with duals|n-category with duals]]', which  generalizes the [[fundamental groupoid|fundamental n-groupoid]] of a plain old space.  When a path crosses a codimension-$1$ stratum, "something interesting happens" &#8211; i.e., a [[catastrophe]].   So, we say such a path gives a noninvertible morphism.   The idea is that going along such a path and then going back is not "the same" as having stayed put. So, going back along such a path is not its inverse, just its [[dualizable object|dual]].

See Caf&#233; [discussion] (http://golem.ph.utexas.edu/category/2006/11/this_weeks_finds_in_mathematic_2.html#c006196) and paper it inspired, [[J. Woolf]] [Transversal homotopy theory](http://arxiv.org/abs/0910.3322).

### For simplicial sets

The [[left adjoint]] of the [[nerve]] functor $N:Cat \to SSet$, which takes a [[simplicial set]] to a category, is sometimes called the *fundamental category* functor.  One notation for it is $\tau_1$.  Explicitly, for a simplicial set $X$, $\tau_1(X)$ is the [[category]] [[free category|freely generated]] by the [[directed graph]] whose [[vertices]] are 0-[[simplices]] of $X$ and whose [[edges]] are 1-[[simplices]] (the source and target are defined by the [[face maps]]), modulo the relations $s^0(x) \sim id_x$ for $x \in X_0$ and $d^1(x) \sim d^0(x) \circ d^2(x)$ for $x \in X_2$.  Here $s^i$ and $d^i$ denote the [[degeneracy map|degeneracy]] and [[face maps]], respectively.

If $X$ is a [[quasicategory]], then its fundamental category is equivalent to its [[homotopy category of an (infinity,1)-category|homotopy category]].

$$
  \array{
     QuasiCat &&\hookrightarrow&& sSet
     \\
     & {}_{\mathllap{Ho}}\searrow && \swarrow_{\mathrlap{\tau_1}}
    \\
     && Cat
  }
  \,.
$$ 

## Related concepts

* [[fundamental groupoid]], [[fundamental ∞-groupoid]]

* **fundamental category**, [[fundamental (∞,1)-category]]

  * [[equivariant fundamental groupoid]]

* [[directed homotopy theory]]


## References

* [[Marco Grandis]], _Directed algebraic topology, categories and higher categories_ ([pdf](http://www.dima.unige.it/~grandis/DAT.Intro.pdf))

* [[Andre Joyal]], [[Myles Tierney]], _Notes on simplicial homotopy theory_, 2008, [citeseerx](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.187.2533)

* [[J. Woolf]], _Transversal homotopy theory_, Theory and applications of categories, Vol 24, Issue 7, pp 148-178, 2010. (arXiv:0910.3322)

* [[J. Woolf]], _The fundamental category of a stratified space_, Journal of Homotopy and Related Structures, Vol 4, Issue 1 pp 359-387, 2009. (arXiv:0811.2580)

[[!redirects fundamental categories]]