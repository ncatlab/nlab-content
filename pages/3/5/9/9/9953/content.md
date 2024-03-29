
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Group Theory
+-- {: .hide}
[[!include group theory - contents]]
=--
#### Topology
+--{: .hide}
[[!include topology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Definition

For each $n \in \mathbb{N}$ there is an inclusion

$$
  O(n) \hookrightarrow O(n+1)
$$

of the [[orthogonal group]] in dimension $n$ into that in dimension $n+1$. The _stable orthogonal group_ is the [[direct limit]] (as [[topological groups]] of this sequence of inclusions.

$$
  O \coloneqq {\underset{\to}{\lim}}_n O(n)
  \,.
$$

## Properties

### Homotopy groups

By the discussion at _[orthogonal group -- homotopy groups](orthogonal%20group#HomotopyGroups)_ we have that the [[homotopy groups]] of the stable orthogonal group are 

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| $\pi_n(O)$ | $\mathbb{Z}_2$ | $\mathbb{Z}_2$ |0 | $\mathbb{Z}$ | 0 | 0 | 0 | $\mathbb{Z}$ |

or if we instead write down the [[order of a group|order]]:

| $n\;mod\; 8$ | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 |
|-----|---|---|---|---|---|---|---|---|
| ${\vert\pi_n(O)\vert}$ | 2 | 2 | 1 | $\infty$ | 1 | 1 | 1 | $\infty$ |

Via the [[J-homomorphism]] this is related to the [[stable homotopy groups of spheres]]:

[[!include image of J -- table]]


## Related concepts

* [[stable unitary group]]

* [[BO(n)]]

* [[J-homomorphism]]

* [[KO-theory]]


[[!redirects stable orthogonal groups]]

[[!redirects stabe orthogonal group]]
