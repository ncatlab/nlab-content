
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Symplectic geometry
+--{: .hide}
[[!include symplectic geometry - contents]]
=--
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

For $(X, \omega)$ a [[symplectic manifold]] a _metaplectic structure_ on $X$ is a [[G-structure]] for $G$ the [[metaplectic group]], hence a [[lift of structure groups]] of the [[tangent bundle]] from the [[symplectic group]] to the [[metaplectic group]] through the [[double cover]] map $Mp(2n, \mathbb{R}) \to Sp(2n, \mathbb{R})$:

$$
  \array{
    && \mathbf{B}Mp(2n, \mathbb{R})
    \\
    & {}^{\mathllap{metaplectic \atop structure}}\nearrow & \downarrow
    \\
    X &\stackrel{T X}{\to}& \mathbf{B} Sp(2n, \mathbb{R})
  }
  \,.
$$

Analogously for the [[Mp^c]]-group one considers _$Mp^c$-structures_.

## Properties

### Relation to metalinear structure

+-- {: .num_theorem}
###### Theorem

Let $(X,\omega)$ be a [[symplectic manifold]] and $L \subset T X$ a subbundle of [[Lagrangian subspaces]] of the [[tangent bundle]]. Then $T X$ admits a metaplectic structure precisely if $L$ admits a [[metalinear structure]]. 

=--

([Bates-Weinstein, theorem 7.16](#BatesWeinstein))

### Existence of $Mp^c$-structures

+-- {: .num_theorem}
###### Theorem

Every [[symplectic group|Sp]]-[[principal bundle]] has a [[lift of structure group|lift]] to an [[Mp^c]]-[[principal bundle]].

=--

([Robinson-Rawnsley 89, theorem (6.2)](#RobinsonRawnsley89))

For more details, see at [metaplectic group -- (Non-)Triviality of Extensions](metaplectic+group#NonTrivialityOfExtensions).

## Related concepts

* [[metaplectic group]]

* [[spin structure]]

* [[metaplectic correction (in geometric quantization)]]

## References

* {#ForgerHess79} [[Michael Forger]], Harald Hess, _Universal metaplectic structures and geometric quantization_, Comm. Math. Phys. Volume 64, Number 3 (1979), 269-278. ([EUCLID](https://projecteuclid.org/euclid.cmp/1103904723))

* R. J. Plymen, _The Weyl bundle_, Journal of Functional Analysis 49, 186-197 (1982) ([journal](http://www.sciencedirect.com/science/article/pii/0022123682900799))

* {#RobinsonRawnsley89} P. L. Robinson, [[John Rawnsley]], _The metaplectic representation, $Mp^c$-structures and geometric quantization_, 1989

* Michel Cahen, [[Simone Gutt]], [[John Rawnsley]], _Symplectic Dirac Operators and $Mp^c$-structures_ ([arXiv:1106.0588](http://arxiv.org/abs/1106.0588))

* {#BatesWeinstein} Sean Bates, [[Alan Weinstein]], _[[Lectures on the geometry of quantization]]_, ([pdf](http://www.math.berkeley.edu/~alanw/GofQ.pdf))
 

[[!redirects metaplectic structures]]

[[!redirects Mp^c structure]]
[[!redirects Mp^c structures]]
[[!redirects Mp^c-structure]]
[[!redirects Mp^c-structures]]
