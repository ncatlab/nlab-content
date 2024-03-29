
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--



## For paths

+-- {: .num_defn #PathHomotopyRelativeBoundary}
###### Definition

Let $X$ be a [[topological space]] and let

$$
  \gamma_1, \gamma_2 \;\colon\; [0,1] \longrightarrow X
$$

be two [[paths]] in $X$, i.e. two [[continuous functions]] from the [[closed interval]] to $X$,
such that their endpoints agree:

$$
  \gamma_1(0) = \gamma_2(0)
  \phantom{AAAA}
  \gamma_1(1) = \gamma_2(1)
  \,.
$$

Then a [[homotopy relative boundary]] from $\gamma_1$ to $\gamma_2$ is a [[homotopy]] (def. \ref{LeftHomotopy})

$$
  \eta \;\colon\; \gamma_1 \Rightarrow \gamma_2
$$

such that it does not move the endpoints:

$$
  \eta(0,-) = const_{\gamma_1(0)} = const_{\gamma_2(0)}
  \phantom{AAAAAA}
  \eta(1,-) = const_{\gamma_1(1)} = const_{\gamma_2(1)}
  \,.
$$

=--

+-- {: .num_prop}
###### Proposition

Let $X$ be a [[topological space]] and let $x, y \in X$ be two points. Write

$$
  P_{x,y} X
$$

for the set of [[paths]] $\gamma$ in $X$ with $\gamma(0) = x$ and $\gamma(1) = y$.

Then [[homotopy relative boundary]] (def. \ref{PathHomotopyRelativeBoundary})
is an [[equivalence relation]] on $P_{x,y}X$.

The corresponding set of [[equivalence classes]] is denoted

$$
  Hom_{\Pi_1(X)}(x,y)
  \;\coloneqq\;
  (P_{x,y}X)/\sim
  \,.
$$

The operation of [[path concatenation]] descends to these equivalence
classes, so that for all $x,y, z \in X$ there is a function

$$
  Hom_{\Pi_1(X)}(x,y)
   \times
  Hom_{\Pi_1(X)}(y,z)
    \longrightarrow
  Hom_{\Pi_1(X)}(x,z)
  \,.
$$

Moreover, this composition operation is [[associativity|associative]] in the evident sense.

Set of points of $X$ together with the set $Hom_{\Pi_1(X)}(x,y)$ for all points of points
and equipped with this composition operation is called the _[[fundamental groupoid]]_ of $X$, denoted

$$
  \Pi_1(X)
  \,.
$$

If we pick a single point $x \in X$, then one writes

$$
  \pi_1(X,x)
  \;\coloneqq\;
  Hom_{\Pi_1(X)}(x,x)
  \,.
$$

Under the above composition this is a [[group]], and as such is called the _[[fundamental group]]_
of $X$ at $x$.

=--


[[!redirects homotopies relative boundary]]
