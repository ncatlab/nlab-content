
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Bundles
+-- {: .hide}
[[!include bundles - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The concept of _projective bundle_ is the generalization of that of _[[projective space]]_ from [[vector spaces]] to [[vector bundles]].

## Definition

For $\pi \colon E \to X$ a [[topological vector bundle]] over some [[topological field]] $k$, write $E \setminus X \subset E$ for its [[complement]] of the [[zero section]], regarded with its [[subspace topology]]. 


Then its _projective bundle_ is the [[fiber bundle]] $P(E) \to X$ whose total space the [[quotient topological space]] of $E \setminus X$ by the [[equivalence relation]]

$$
  \left( 
    v_1 \sim v_2
  \right)
   \;\Leftrightarrow\;
  \left(
    (\pi(v_1) = \pi(v)_1)
    \,\text{and}\,
    \left(
      \underset{c \in k \setminus \{0\}}{\exists}
      ( v_2 = c v_1)
    \right)
  \right)
$$

hence

$$
  P(E) \coloneqq (E \setminus )/\sim
  \,,
$$

and whose bundle projection is 

$$
  \array{
    P(E) &\longrightarrow& X
    \\
    [v] &\mapsto& \pi(v)
  }
  \,.
$$

## Related entries

* [[Thom space]]

* [[fundamental product theorem in topological K-theory]]


## References

* {#Wirthmuller12} [[Klaus Wirthmüller]], section 5 of _Vector bundles and K-theory_, 2012 ([pdf](ftp://www.mathematik.uni-kl.de/pub/scripts/wirthm/Top/vbkt_skript.pdf))


[[!redirects projective bundles]]
