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

[[continuous functions]] defined pointwise. 

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

### In metric spaces ###
Let $(S, \rho)$ be a [[metric space]] and let 

$$\mathbb{R}_{+} \coloneqq \{a \in \mathbb{R} \vert 0 \lt a\}$$

be the positive elements in $\mathbb{R}$. A function $f:S \to S$ is __continuous at a point__ $c \in S$ if 

$$isContinuousAt(f, c) \coloneqq \forall \epsilon \in \mathbb{R}_{+}. \forall x \in S. \exists \delta \in \mathbb{R}_{+}. (\rho(x, c) \lt \delta) \to (\rho(f(x), f(c)) \lt \epsilon)$$

$f$ is __pointwise continuous__ in $S$ if it is continuous at all points $c$:
$$isPointwiseContinuous(f) \coloneqq \forall c \in S. isContinuousAt(f, c)$$

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
