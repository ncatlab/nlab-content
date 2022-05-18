+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Analysis
+-- {: .hide}
[[!include analysis - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea ##

The concept of [[continuous functions]] familiar from [[epsilontic analysis]].

## Definition ##

### In the real numbers ###
Let $\mathbb{R}$ be the [[real numbers]] and let 

$$\mathbb{R}_{+} \coloneqq \{a \in \mathbb{R} \vert 0 \lt a\}$$

be the positive elements in $\mathbb{R}$. A function $f:\mathbb{R} \to \mathbb{R}$ is __continuous at a point__ $c \in \mathbb{R}$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in \mathbb{R}_{+}. \forall x \in \mathbb{R}. \exists \delta \in \mathbb{R}_{+}. (\vert x - c \vert \lt \delta) \to (\vert f(x) - f(c) \vert \lt \epsilon)$$

$f$ is __pointwise continuous__ in $\mathbb{R}$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in \mathbb{R}. isContinuousAt(f, c)$$

### In Archimedean fields ###
Let $F$ be an [[Archimedean field]] and let 

$$F_{+} \coloneqq \{a \in F \vert 0 \lt a\}$$

be the positive elements in $F$. A function $f:F \to F$ is __continuous at a point__ $c \in F$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in F_{+}. \forall x \in F. \exists \delta \in F_{+}. (\vert x - c \vert \lt \delta) \to (\vert f(x) - f(c) \vert \lt \epsilon)$$

$f$ is __pointwise continuous__ in $F$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in F. isContinuousAt(f, c)$$

### In premetric spaces
 {#EpsilonticDefinition}

We state the definition of pointwise continuity in terms of [[epsilontic analysis]], definition \ref{EpsilonDeltaDefinitionOfPointwiseContinuity} below. 

+-- {: .num_defn #PremetricSpace}
###### Definition

A _[[premetric space]]_ is 

1. a [[set]] $X$ (the "underlying set");

1. a ternary [[relation]] $(-)\sim_{(-)} (-)\colon X \times \mathbb{R}_+ \times X \to \Omega$ (the "premetric") from the [[Cartesian product]] of the set with the positive [[real numbers]] and with itself again to the set of [[truth values]]. 

=--


+-- {: .num_example}
###### Example

Every [[normed vector space]] $(V, {\Vert -\Vert})$
becomes a [[premetric space]] according to def. \ref{PremetricSpace} by setting

$$
  x \sim_\epsilon y \coloneqq {\Vert x-y\Vert \lt \epsilon}
  \,.
$$

=--

+-- {: .num_defn #EpsilonDeltaDefinitionOfPointwiseContinuity}
###### Definition
**(epsilontic definition of pointwise continuity)**

For $(X,\sim^X)$ and $(Y,\sim^Y)$ two [[premetric spaces]] (def. \ref{PremetricSpace}), then a [[function]]

$$
  f \;\colon\; X \longrightarrow Y
$$

is said to be _continuous at a point $x \in X$_ if for every $\epsilon$ there exists $\delta$ such that 

$$
  x \sim_\delta^X y \;\Rightarrow\; f(x) \sim_\epsilon^Y f(y) 
$$

The function $f$ is called _pointwise continuous_ if it is continuous at every point $x \in X$.

=--

### In preconvergence spaces ###
Let $S$ and $T$ be [[preconvergence space]]s. A function $f:S \to T$ is __continuous at a point__ $c \in S$ if 
 
$$isContinuousAt(f, c) \coloneqq \forall I \in DirectedSet_\mathcal{U}. \forall x \in I \to S. isLimit_S(x, c) \to isLimit_T(f \circ x, f(c))$$

$f$ is __pointwise continuous__ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in S. isContinuousAt(f, c)$$

### In function limit spaces ###

Let $T$ be a [[Hausdorff function limit space]], and let $S \subseteq T$ be a [[subset]] of $T$. A function $f:S \to T$ is __continuous at a point__ $c \in S$ if the [[limit of a function|limit of $f$ approaching $c$]] is equal to $f(c)$. 

$$\lim_{x \to c} f(x) = f(c)$$

$f$ is __pointwise continuous__ on $S$ if it is continuous at all points $c \in S$: 

$$isPointwiseContinuous(f) \coloneqq \forall c \in S. \lim_{x \to c} f(x) = f(c)$$

## See also ##

* [[limit of a function]]
* [[differentiable function]]
* [[uniformly continuous function]]

[[!redirects pointwise continuous]]
[[!redirects pointwise continuous functions]]