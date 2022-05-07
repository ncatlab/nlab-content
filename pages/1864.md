+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

A concordance between [[cocycle]]s in [[cohomology]] is a relation similar to but different from a plain [[coboundary]], it is a "coboundary after [[geometric realization]]".

A concordance is a left [[homotopy]] in an [[(∞,1)-topos]] with respect to a _topological_ [[interval object]], not with respect to the _[[interval category|categorical interval]]_ .

For instance for $S = Diff$ the [[site]] of smooth manifolds, there is

* the "topological interval" $I \in \mathbf{H}_{diff}$ which is the [[smooth ∞-stack]] on $Diff$ [[representable functor|represented by]] the manifold $I = [0,1]$;

* the "categorical interval" $Ex^\infty \Delta^1 \in \mathbf{H}_{Diff}$ is the [[smooth ∞-stack]] that is constant on the free groupoid on a single morphism.


## Definition

For $\mathbf{H}$ and [[(∞,1)-topos]] with a fixed notion of topological [[interval object]] $I$, for $A \in \mathbf{A}$ any coefficient object and $X \in \mathbf{H}$ any other object, a **concordance** between two objects

$$
  c,d \in \mathbf{H}(X,A)
$$

(two cocycles in $A$-[[cohomology]] on $X$)

is an object $\eta \in A(X \times I)$ such that

$$
\begin{matrix}
X&&\\
\downarrow&\searrow^{c}&\\
X \times I&\stackrel{\eta}{\to}& A\\
\uparrow& \nearrow_{d}&\\
X&&
\end{matrix}
\,.
$$

## Examples 

### For topological vector bundles
 {#ForTopologicalVectorBundles}

For [[topological vector bundles]] over [[paracompact Hausdorff spaces]], concordance classes coincide with plain [[isomorphism classes]]:

+-- {: .num_prop #ConcondanceOfTopologicalVectorBundles}
###### Proposition
**([[concordance]] of [[topological vector bundles]])**

Let $X$ be a [[paracompact Hausdorff space]]. If $E \to X \times [0,1]$ is a [[topological vector bundle]] over the [[product space]] of $X$ with the [[closed interval]] (hence a _[[concordance]]_ of topological vector bundles on $X$), then the two endpoint-restrictions

$$
  E|_{X \times \{0\}}
  \phantom{AA}
  \text{and}
  \phantom{AA}
  E|_{X \times \{1\}}
$$

are [[isomorphism|isomorphic]] [[topological vector bundles]] over $X$.

=--

For **proof** see at _[[topological vector bundle]]_ [this Prop.](topological+vector+bundle#ConcondanceOfTopologicalVectorBundles).



### More examples

* For $A = VectrBund(-)$ the difference between concordance of [[vectorial bundles]] and isomorphism of vectorial bundles plays a crucial rule in the construction of [[K-theory]] from this model.

* The notions of coboundary and concordance exist in every [[cohesive (∞,1)-topos]].

## References

Discussion of concordance of topological [[principal bundles]] (in fact for [[simplicial principal bundles]] [[parameterized homotopy theory|parameterized]] over some base space):

* [[David Roberts]], [[Danny Stevenson]], Cor. 15 in: _Simplicial principal bundles in parametrized spaces_, New York Journal of Mathematics Volume 22 (2016) 405-440 ([arXiv:1203.2460](https://arxiv.org/abs/1203.2460), [nyjm:22-19](http://nyjm.albany.edu/j/2016/22-19.html))

Discussion of concordance in terms of the [[shape modality]] in the [[cohesive (∞,1)-topos]] of [[smooth ∞-groupoids]] (see at *[[shape via cohesive path ∞-groupoid]]* for more):

* {#BEBP} [[Daniel Berwick-Evans]], [[Pedro Boavida de Brito]], [[Dmitri Pavlov]], _Classifying spaces of infinity-sheaves_ ([arXiv:1912.10544](https://arxiv.org/abs/1912.10544))

[[!redirects concordances]]
