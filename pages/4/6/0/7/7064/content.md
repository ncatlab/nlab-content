
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Homotopy theory
+-- {: .hide}
[[!include homotopy - contents]]
=--
#### Stable Homotopy theory
+--{: .hide}
[[!include stable homotopy theory - contents]]
=--
=--
=--

# Homotopy groups of spheres
* table of contents
{: toc}

## Idea

The [[homotopy groups]] of [[spheres]] ...

The stable homotopy groups of the [[sphere spectrum]] ...


## Tables

The first stable homotopy groups of the [[sphere spectrum]] $\mathbb{S}$

| $k =$ | 0 | 1 | 2 | 3 | 4  | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 | $\cdots$ | 
|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|--|
| $\pi_k(\mathbb{S}) = $ | $\mathbb{Z}$  | $\mathbb{Z}_2$  |  $\mathbb{Z}_2$ |  $\mathbb{Z}_{24}$ |  $0$ |  $0$ | $\mathbb{Z}_2$ |   $\mathbb{Z}_{240}$ | $(\mathbb{Z}_2)^2$ |  $(\mathbb{Z}_2)^3$ | $\mathbb{Z}_6$ | $\mathbb{Z}_{504}$ | $0$ | $\mathbb{Z}_3$ | $(\mathbb{Z}_2)^2$ | $\mathbb{Z}_{480} \oplus \mathbb{Z}_2$ | $\cdots$ |


## Characteristic maps

### J-homomorphism and Adams e-invariant

The following characterizes the [[image]] of the [[J-homomorphism]] 

$$
  J \;\colon\; \pi_\bullet(O) \longrightarrow \pi_\bullet(\mathbb{S})
$$

from the [[homotopy groups]] of the [[stable orthogonal group]] to the stable homotopy groups of spheres. This was first conjectured in ([Adams 66](#Adams66)) (since called the _Adams conjecture_) and then proven in ([Quillen 71](#Quillen71)).

+-- {: .num_remark}
###### Remark

By the discussion at _[orthogonal group -- homotopy groups](orthogonal%20group#HomotopyGroups)_ we have that the [[homotopy groups]] of the [[stable orthogonal group]] are 

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| $\pi_n(O)$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ |0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

Because all groups appearing here and in the following are [[cyclic groups]], we instead write down the [[order of a group|order]]

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| ${\vert\pi_n(O)\vert}$ | 2 | 2 | 1 | $\infty$ | 1 | 1 | 1 | $\infty$ |

=--

+-- {: .num_theorem}
###### Theorem

The [[stable homotopy groups of spheres]] $\pi_n(\mathbb{S})$ are the [[direct sum]] of the ([[cyclic group|cyclic]]) [[image]] of the 
[[J-homomorphism]], and the [[kernel]] of the [[Adams e-invariant]].

Moreover,

* for $n = 0 \;mod \;$ and $n = 1 \;mod \; 8$ and $n$ positive the J-homomorphism is [[injection|injective]], hence its image is $\mathbb{Z}_2$, 

* for $n = 3\; mod\; 8$ and $n = 7 \; mod \; 8$ hence for $n = 4 k -1$, the [[order of a group|order]] of the image is equal to the [[denominator]] of $B_{2k}/4k$, where $B_{2k}$ is the [[Bernoulli number]]

* for all other cases the image is necessarily zero.

=--

## Related concepts

* [[Adams–Novikov spectral sequence]]

## References

Introductions and surveys include

* Alex Writght, _Homotopy groups of spheres: A very basic introduction_ ([pdf](http://www.math.uchicago.edu/~amwright/HomotopyGroupsOfSoheres.pdf))

* Doug Ravenal, _Complex cobordism and stable homotopy groups of spheres_ ([web](http://www.math.rochester.edu/people/faculty/doug/mu.html))

Discussion of the [[image]] of the [[J-homomorphism]] is due to

* [[John Adams]], _On the groups $J(X)$ IV_, Topology 5: 21,(1966)  _Correction_, Topology 7 (3): 331 (1968)
 {#Adams66}

* [[Daniel Quillen]], _The Adams conjecture_, Topology. an International Journal of Mathematics 10: 67&#8211;80 (1971)
 {#Quillen71}

For formalization in [[homotopy type theory]] see at

* [[UF-IAS-2012]], _[HomotopyGroupsOfSpheres](http://uf-ias-2012.wikispaces.com/HomotopyGroupsOfSpheres)_


See also

* Wikipedia, _[Homotopy groups of spheres](http://en.wikipedia.org/wiki/Homotopy_groups_of_spheres)_

* MO, _[Computational complexity of computing homotopy groups of spheres](http://mathoverflow.net/questions/31004/computational-complexity-of-computing-homotopy-groups-of-spheres)_





[[!redirects homotopy group of a sphere]]
[[!redirects homotopy groups of a sphere]]
[[!redirects homotopy groups of spheres]]
[[!redirects stable homotopy groups of spheres]]