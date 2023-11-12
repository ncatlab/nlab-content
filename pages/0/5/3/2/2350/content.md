\tableofcontents

## Definition

### In set theory

Given a [[set]] $X$, its diagonal function is a [[function]] from $X$ to its [[cartesian product|cartesian square]] $X^2$, often denoted $\Delta_X$, $\check{X}$, or an obvious variation.

Specifically, the __diagonal function__ of $X$ maps an element $a$ of $X$ to the pair $(a,a)$:
$$ \Delta_X = \{ a \mapsto (a,a) \} .$$
Note that this map is an [[injection]], so it defines a [[subset]] of $X^2$, also called the [[diagonal subset|diagonal]] of $X$; this is the origin of the term.

### In category theory

The concept can be generalised to any [[category]] in which the [[product]] $X^2$ exists; see [[diagonal morphism]].

A [[topological space]] $X$ is [[Hausdorff space|Hausdorff]] if and only if its diagonal function is a [[closed map]]; this fact can be generalised to other notions of [[space]].

The [[characteristic function]] of the diagonal function is the [[Kronecker delta]].

### In dependent type theory

In [[dependent type theory]], the **diagonal function** of a type $X$ is the function

$$\Delta_X \equiv \lambda x:X.(x, x, \mathrm{refl}_X(x)):X \to \sum_{x:X} \sum_{y:X} x =_X y$$

where $\sum_{x:X} \sum_{y:X} x =_X y$ is the [[homotopy pullback]] of the [[identity function]] along itself. 

Diagonal functions are used in the [[elimination rules]] and [[computation rules]] for [[identity types]]:

The elimination rules for identity types states that given an element $z:\sum_{x:X} \sum_{y:X} x =_X y \vdash C(z)$, there is a dependent function

$$\mathrm{ind}_{=}^{X, C}:\left(\prod_{x:X} C(\Delta_X(x))\right) \to \prod_{z:\sum_{x:X} \sum_{y:X} x =_X y} C(z)$$

and the computation rules for identity types states that there are homotopies

$$\beta_{=}^{X, C}:\prod_{t:\prod_{x:X} C(\Delta_X(x))} \prod_{x:X} \mathrm{ind}_{=}^{X, C}(t, \Delta_X(x)) =_{C(\Delta_X(x))} t(x)$$

The canonical semantics of the diagonal function is the [[path space object]]. 

## See also

* [[equality]]

* [[diagonal subset]], [[diagonal relation]], [[diagonal morphism]]

* [[path space object]]

* [[identity type]]

[[!include types and logic - table]]

[[!redirects diagonal map]]