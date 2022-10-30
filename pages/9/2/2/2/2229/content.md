+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[subset]] $S$ of a [[group]] $G$, its __normalizer__ $N(S)=N_G(S)$ is the [[subgroup]] of $G$ consisting of all elements $g\in G$ such that $g S = S g$, i.e. for each $s\in S$ there is $s'\in S$ such that $g s=s'g$.  

Notice the similarity but also the difference to the definition of the _[[centralizer subgroup]]_, for which $s' = s$ in the above.

## Properties

### Normalization and Weyl group
 {#NormalizationAndWeylGroup}

If the subset $S$ is in fact a [[subgroup]] of $G$, then it is a [[normal subgroup]] of the normalizer $N_G(S)$; and $N_G(S)$ is the largest subgroup of $G$ such that $S$ is a normal subgroup of it, whence the terminology _normalizer_. Indeed, if $S$ is already a normal subgroup of $G$, then its normalizer coincides with the whole of $G$.

Hence when $S$ is a group then the [[quotient]] 

$$
  W_G S \coloneqq N_G(S)/S
$$ 

is a [[quotient group]]. This is also called the _[[Weyl group]]_ of $S$ in $G$. (This use of terminology is common in [[equivariant stable homotopy theory]] -- see e.g. [May 96, p. 13](#May96) -- but not otherwise.)

## Examples

### Holomorph

Each group $G$ embeds into the [[symmetric group]] $Sym(G)$ on the [[underlying set]] of $G$ by the left [[regular representation]] $g\mapsto l_g$ where $l_g(h) = g h$. The [[image]] is isomorphic to $G$ (that is, the left regular representation of a [[discrete group]] is [[faithful representation|faithful]]). 

The normalizer of the image of $G$ in $Sym(G)$ is called the [[holomorph]]. This solves the elementary problem of embedding a group into a bigger group $K$ in which every [[automorphism]] of $G$ is obtained by restricting (to $G$) an [[inner automorphism]] of $K$ that fixes $G$ as a subset of $K$.

## Generalization

In ([Gray 14](#Gray14)) the concept of the normalizer of a subgroup of a group is generalized to the normalizer of a [[monomorphism]] in any [[pointed category]] in terms of a universal decomposition $U \stackrel{u}{\to} N \stackrel{f}{\to}T$ of a [[monomorphism]] $U \to T$ with $u$ a [[normal monomorphism]].

In ([Bourn-Gray 13](#BournGray13)) the condition that $w$ be a monomorphism is dropped.

## Related concepts

* [[stabilizer subgroup]]

* [[centralizer subgroup]]

## References

* {#Gray14} James Richard Andrew Gray, _Normalizers, centralizers and action representability in semiabelian categories_, Applied Categorical Structures 22(5-6), 981&#8211;1007, 2014.

* {#BournGray13} [[Dominique Bourn]], James Richard Andrew Gray, _Normalizers and split extensions_ ([arXiv:1307.4845](http://arxiv.org/abs/1307.4845))

* {#May96} [[Peter May]], _Equivariant homotopy and cohomology theory_ CBMS Regional Conference Series in Mathematics, vol. 91, Published for the Conference Board of the Mathematical Sciences, Washington, DC, 1996. With contributions by M. Cole, G. Comezana, S. Costenoble, A. D. Elmenddorf, J. P. C. Greenlees, L. G. Lewis, Jr., R. J. Piacenza, G. Triantafillou, and S. Waner. ([pdf](http://www.math.rochester.edu/u/faculty/doug/otherpapers/alaska1.pdf))


[[!redirects normalizers]]

[[!redirects normalizer subgroup]]
[[!redirects normalizer subgroups]]
