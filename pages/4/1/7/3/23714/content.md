#Contents#
* table of contents
{:toc}

## Definition ##

Given a [[Heyting field]] $F$ and a subtype $S \subseteq F$, let us define the subtype $\Delta_{\#}(S) \subseteq S \times S$ of pairs of elements apart from the [[diagonal]] as 

$$\Delta_{\#}(S) \coloneqq \sum_{(x,y):S \times S} x \# y$$ 

### In a field ###

Given a function $f:S \to F$, the __difference quotient__ $q:\Delta_{\#}(S) \to F$ is the partial binary function

$$q(x, y) := \frac{f(x) - f(y)}{x - y}$$

### In a vector space ###

Given a $F$-[[vector space]] $V$ and a function $f:S \to V$, the __difference quotient__ $q:\Delta_{\#}(S) \to V$ is the partial binary function

$$q(x, y) := \frac{1}{x - y} (f(x) - f(y))$$

## See also ##

* [[differentiable function]]

* [[Newton-Leibniz operator]]

* [[rational function]]

* [[reciprocal function]]