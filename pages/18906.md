

+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Relations
+-- {: .hide}
[[!include relations - contents]]
=--
#### Riemannian geometry
+--{: .hide}
[[!include Riemannian geometry - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Definition

+-- {: .num_defn #CausalOrdering}
###### Definition
**(causal order)**

Let $\Sigma$ be a [[spacetime]] (a [[Lorentzian manifold]] equipped with [[time orientation]]).

Consider the [[relation]] on the set $P(\Sigma)$ of [[subsets]] of spacetime
which says a [[subset]] $S_1 \subset \Sigma$ is _not prior_ to a subset $S_2 \subset \Sigma$,
denoted $S_1 {\vee\!\!\!\wedge} S_2$, if $S_1$ does not [[intersection|intersect]] the [[causal past]] of $S_2$,
or equivalently that $S_2$ does not intersect the [[causal future]] of $S_1$:

$$
  \begin{aligned}
    S_1 {\vee\!\!\!\wedge} S_2
    & \;\coloneqq\;
    S_1 \cap \overline{V}^-(S_2) = \emptyset
    \\
    & \Leftrightarrow S_2 \cap \overline{V}^+(S_1) = \emptyset
   \end{aligned}
   \,.
$$

If $S_1 {\vee\!\!\!\wedge} S_2$ and $S_2 {\vee\!\!\!\wedge} S_1$ we say that the two subsets are _[[spacelike]] separated_ and
write

$$
   S_1 {\gt\!\!\!\!\lt} S_2
   \;\;\;\coloneqq\;\;\;
   S_1 {\vee\!\!\!\wedge} S_2
   \;\text{and}\;
   S_2 {\vee\!\!\!\wedge} S_1
   \,.
$$

=--

(e.g. [Epstein-Glaser 73, p. 5 (273)](#EpsteinGlaser73))

## Related concepts


* [[causal structure]]

* [[causality]], [[microcausality]]

* [[causal locality]], [[causal additivity]]

* [[causal complement]], [[causal closure]]

* [[causal perturbation theory]]

* [[time-ordered product]]

* [[S-matrix]]



## References


* {#EpsteinGlaser73} [[Henri Epstein]], [[Vladimir Glaser]], _[[The Role of locality in perturbation theory]]_, Annales Poincar&#233; Phys. Theor. A 19 (1973) 211 ([Numdam](http://www.numdam.org/item?id=AIHPA_1973__19_3_211_0 ))


[[!redirects causal ordering]]

