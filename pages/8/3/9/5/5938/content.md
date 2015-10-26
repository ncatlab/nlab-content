
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[functor]] $F: C\to D$ we say that $F$ __admits a proadjoint__ if the canonical extension $pro(F): pro(C)\to pro(D)$ of $F$ to the categories of [[pro-object]]s
has a [[left adjoint]] $G$. In other words, there is a functor $G: pro(D)\to pro(C)$ and a [[bijection]]

$$
pro(C)(GY',X) \cong pro(D)(Y',y(F)X)
$$

[[natural isomorphism|natural]] in $X$ and $Y'$, where $y:{C^{op}}\hookrightarrow pro(C)$ is the [[Yoneda embedding]] into the category of proobjects $pro(C)\subset (Set^{C})^{op}$. Equivalently, for every [[prorepresentable functor]] $X:D\to Set$, the functor $X\mapsto X\circ F$ is also prorepresentable.

## Examples

### Shape theory, &#233;tale homotopy and Galois theory
 {#EtaleHomotopy}

If an [[(∞,1)-topos]] $\mathbf{H}$ has a genuine [[left adjoint|left]] [[adjoint (∞,1)-functor]] $\Pi$ to its [[constant ∞-stack]] functor $\Delta$, then that may be interpreted as sending each object to its [[fundamental ∞-groupoid]], see at _[[fundamental ∞-groupoid of a locally ∞-connected (∞,1)-topos]]_.

In general such a left adjoint $\Pi$ does not exist, but the [[pro-left adjoint]] $\Pi_{pro}$ to $\Delta$ always exists. This hence produces a pro-version of the [[fundamental ∞-groupoid]]-construction known generally as the [[étale homotopy type]]. In [[algebraic geometry]] and [[arithmetic geometry]] this reproduces the content of [[Galois theory]] (the pro-etale fundamental group is the [[Galois group]]/[[algebraic fundamental group]])  while in [[topology]] this reproduces the concept of [[shape]]. (Whence the term _[[shape modality]]_ for $\Pi$).

## Related concepts

* [[pro-homotopy theory]]

## References

* [[J.-M. Cordier]], [[T. Porter]], _Shape theory : Categorical Methods of Approximation_, (sec. 2.3), Mathematics and its Applications, Ellis Horwood Ltd., March 1989, 207 pages.Dover addition (2008)  (Link to publishers [here](http://store.doverpublications.com/048646623x.html))

* {#Hoyois13} [[Marc Hoyois]], _A note on &#201;tale homotopy_, 2013 ([pdf](http://math.northwestern.edu/~hoyois/papers/etalehomotopy.pdf))

[[!redirects proadjonts]]

[[!redirects pro-adjoint]]
[[!redirects pro-adjoints]]
