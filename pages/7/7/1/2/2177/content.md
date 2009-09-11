[[!redirects Cactus Language]]

## Idea ##

Consider the [[minimal negation operator]] of arity $k$, written in the form $\nu (x_1, \dots, x_k)$ or $\text{&#10647;}\: x_1 \text{&#65104;} \ldots \text{&#65104;} x_k \:\text{&#10648;}$.

Read as a function, $\text{&#10647;}\: x_1 \text{&#65104;} \ldots \text{&#65104;} x_k \:\text{&#10648;}$ returns a value of $1$ in exactly those cases where exactly one of its arguments is $0$.

Read as an assertion, under the interpretation where $1$ represents logical truth, $\text{&#10647;}\: x_1 \text{&#65104;} \ldots \text{&#65104;} x_k \:\text{&#10648;}$ makes a statement to the effect that exactly one of its arguments is false.

The relation between the function and the assertion is this, that the fiber of $1$ under the function captures precisely the models of the assertion.

For added concreteness, consider the case where $k = 3$.  Letting $\neg x$ be written as $x'$, the minimal negation opus $\text{&#10647;}\: u \text{&#65104;} v \text{&#65104;} w \:\text{&#10648;}$ can be written as a sum of products of positive and negative literals in accord with the following equation:

$$\text{&#10647;}\: u \text{&#65104;} v \text{&#65104;} w \:\text{&#10648;} \quad = \quad u' v w + u v' w + u v w'$$

That should bell a few rings &#8230;

Clearly, negation and differentiation are not the same thing, but a seeming coincidence of that sort does get one to asking whether there might be a deeper analogy between flipping bits and taking derivatives.

## External links ##

This is pretty ugly, but it's the best I have by way of a formal definition at present:

* [Cactus Language](http://mywikibiz.com/Directory:Jon_Awbrey/Papers/Cactus_Language)

I'll be working to make it more elegantine and less elephantine ...
