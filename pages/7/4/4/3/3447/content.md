+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### $(\infty,1)$-Topos Theory
+--{: .hide}
[[!include (infinity,1)-topos - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--



#Contents#
* automatic table of contents goes here
{:toc}

## Idea

Recall that a [[locally constant sheaf]] (of sets) is a section of the [[constant stack]] with fiber the [[groupoid]] $Core(FinSet)$, the [[core]] of the [[category]] [[FinSet]].

This extends to a general pattern:

a **locally constant $\infty$-stack** is a section of the [[constant ∞-stack]] that is constant on the [[∞-groupoid]] $Core(\infty FinGrpd)$.

## Definition

For $\mathbf{H}$ an [[(∞,1)-sheaf (∞,1)-topos]] there is the [[terminal object|terminal]] [[(∞,1)-geometric morphism]]

$$
  (LConst \dashv \Gamma) : \mathbf{H} \to \infty Grpd
$$

consisting of the [[global section]] and the [[constant ∞-stack]] [[(∞,1)-functor]].


Write $\mathcal{S} := Fin \infty Grpd \in \infty Grpd$ for the [[∞-groupoid]] of finite $\infty$-groupoids. This is canonically a [[pointed object]] $* \to \mathcal{S}$.

Notice the for $X \in \mathbf{H}$ any [[object]], the [[over-(∞,1)-topos]] $\mathbf{H}/X$ is the [[little topos|little]] $(\infty,1)$-topos of $X$. Objects in here we may regard as $\infty$-stacks on $X$.


+-- {: .un_defn}
###### Definition

For $X \in \mathbf{H}$ an [[object]] a **locally constant $\infty$-stack** on $X$ is an object $P \to X$ in the [[over-(∞,1)-topos]] $\mathbf{H}/X$ that arises as the [[homotopy fiber]] of a morphism $\tilde \nabla : X \to LConst \mathcal{S}$ in $\mathbf{H}$

$$
  \array{
    P &\to& * 
    \\
    \downarrow && \downarrow
    \\
    X &\stackrel{\tilde \nabla}{\to}& LConst \mathcal{S}
  }
  \,.
$$ 

The [[∞-groupoid]] of locally constant $\infty$-stacks on $X$ is 

$$
  LConst(X) := \mathbf{H}(X, LConst \mathcal{S})
  \,.
$$

=--

+-- {: .un_remark}
###### Remark

In other words, a locally constant $\infty$-stack is in $\mathbf{H}$ a $LConst \mathcal{S}$-[[principal ∞-bundle]] over $X$. See there for a discussion of how these are indeed classified by morphisms $X \to LConst \mathcal{S}$.


=--

+-- {: .un_remark}
###### Remark

A locally constant $\infty$-stack is also called a [[local system]]. See there for more details.
 
=--

## Examples {#References}

Here are commented references that establish aspects of the above general abstract situation.


### Locally constant 1-stacks and 2-stacks on topological spaces

A discussion of locally constant 2-stacks over topological spaces is in

* [[Pietro Polesello]] and [[Ingo Waschkies]], _Higher monodromy_ , Homology, Homotopy and Applications, Vol. 7(2005), No. 1, pp. 109-150 ([pdf](http://www.intlpress.com/HHA/v7/n1/a7/pdf)).

We indicate briefly how the results stated in this article fit into the general abstract picture as indicated above:

The authors consider locally constant 1-stacks and 2-stacks on sites of open subsets of [[topological space]]s.

Prop. 1.1.9 gives the [[adjunction]]

$$
  (LConst \dashv \Gamma) : Sh_{(2,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Gamma}{\to}} Grpd
$$

between forming constant stacks and taking global sections.

Then prop 1.2.5, 1.2.6, culminating in 
[theorem 1.2.9, p. 121](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=13) gives (somewhat implicitly) the other adjunction

$$
  (\Pi_1\dashv LConst) : Op(X) \hookrightarrow Sh_{(2,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi_1}{\to}} Grpd
$$

with the [[right adjoint]] to $LConst$ being the [[fundamental groupoid]] functor on representables. (Where we change a bit the perspective on the results as presented there, to amplify the pattern indicated above. For instance where the authors write $\Gamma(X,C_X)$ we think of this here equivalently as $Sh_{(2,1)}(X)(X,LConst(C))$, so that the theorem then gives the adjunction equivalence $\cdots \simeq Grpd(\Pi_1(X),C)$).

Then in essentially verbatim analogy, these results are lifted from stacks to 2-stacks in section 2, where now prop 2.2.2, 2.2.3, culminating in [theorem 2.2.5, p. 132](http://www.intlpress.com/HHA/v7/n1/a7/v7n1a7.pdf#page=24) gives (somewhat implicitly) the adjunction

$$
  (\Pi_2\dashv LConst) : Op(X) \hookrightarrow Sh_{(3,1)}(X) \stackrel{\overset{LConst}{\leftarrow}}{\underset{\Pi_2}{\to}} Grpd
$$

now with the [[path n-groupoid|path 2-groupoid]] operation (locally) left adjoint to forming constant 2-stacks. (Subjct verbatim to a remark as above.)


### Locally constant $\infty$-stacks on topological spaces {#ooStackOnTopSpace}


A discussion of locally constant $\infty$-stacks over [[topological space]]s is in

* [[Bertrand Toen]], _Toward a Galoisian interpretation of homotopy theory_ ([arXiv:0007157](http://arxiv1.library.cornell.edu/abs/math/0007157))

In [theorem 2.13, p. 25](http://arxiv1.library.cornell.edu/PS_cache/math/pdf/0007/0007157v4.pdf#page=25) the author proves an equivalence of [[(∞,1)-categories]] (modeled there as [[Segal category|Segal categories]])

$$
  LConst(X) \simeq Fib(\Pi(X))
$$

of [[locally constant ∞-stack]]s on $X$ and [[Kan fibration]]s over the [[fundamental ∞-groupoid]] $\Pi(X) = Sing(X)$.

But by the right Quillen functor $Id : sSet_{Quillen} \to sSet_{Joyal}$ from the Quillen [[model structure on simplicial sets]] to the [[Joyal model structure on simplicial sets]] every Kan fibration is a categorical fibration and every categorical fibration over a [[Kan complex]] is a [[Cartesian fibration]] (as discussed there) and a coCartesian fibration. Finally, by the [[Grothendieck construction|(∞,1)-Grothendieck construction]], these are equivalent to [[(∞,1)-functor]]s $\Pi(X) \to \infty Grpd$.

In total this means that via the [[Grothendieck construction]] To&#235;n's result does actually produce an equivalence

$$
  LConst(X) \simeq Func(\Pi(X), \infty Grpd)
  \,.
$$

## Pattern

* A [[locally constant function]] is a section of a [[constant sheaf]];

* a [[locally constant sheaf]] is a section of a [[constant stack]];

* a [[locally constant stack]] is a section of (... and so on...)

* a **locally constant $\infty$-stack** is a section of a [[constant ∞-stack]].

A locally constant sheaf / $\infty$-stack is also called a [[local system]].



## References

See the references at [[geometric homotopy groups in an (∞,1)-topos]].


[[!redirects locally constant ∞-stack]]
[[!redirects locally constant (∞,1)-sheaf]]

[[!redirects locally constant ∞-stacks]]
[[!redirects locally constant (∞,1)-sheaves]]


















