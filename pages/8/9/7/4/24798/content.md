

# Two-sorted set theory
* table of contents
{: toc}

## Notions of sets and elements

We work in a two-sorted first order theory, where $S$ represents the type of probable sets, and $E$ represents the type of probable elements. Then, 

\begin{definition}
A notion of set and element in a two-sorted first-order theory with sorts $S$ and $E$ consists of:

* A binary predicate in $S$, $(-)=_S(-)$, called *equality of sets*

* A binary predicate in $E$, $(-)=_E(-)$, called *equality of elements*

* A unary predicate in $S$, $\mathrm{set}(-)$, called *being a set*

* A unary predicate in $E$, $\mathrm{element}(-)$, called *being an element*

* A binary predicate in $E$ on the left and $S$ on the right, $(-)\in(-)$, called *membership*

such that 

* $(-)=_E(-)$ is an [[equivalence relation]]

* if $a \in b$, then $a$ is an element and $b$ is a set

$$\forall a:E.\forall b:S.(a \in b) \to \mathrm{element}(a) \wedge \mathrm{set}(b)$$

* weak extensionality for sets and elements: for all $a:S$ and for all $b:S$, if a and b are sets, then $a =_S b$ if and only if, for all $c:E$, if $c$ is an element, then $c \in a$ if and only if $c \in b$

$$\forall a:S.\forall b:S.(\mathrm{set}(a) \wedge \mathrm{set}(b)) \implies ((a =_S b) \iff \forall c:E.(\mathrm{element}(c) \implies ((c \in a) \iff (c \in b))))$$
\end{definition}

## Examples

### Set theories with urelements

A two-sorted set theory is a [[material set theory]] with [[urelements]] if $\mathrm{set}(A)$ and $\mathrm{element}(a)$ are both $\top$ for all $a:S$ and $a:E$, and there is an injection $\mathrm{asElem}:S \hookrightarrow E$ which turns every set into an element. The [[atoms]] or [[urelements]] are the elements which are not contained in the [[image]] of $\mathrm{asElem}$. 

### Pure set theories

A two-sorted material set theory with urelements is a [[pure set]] theory if the injection $\mathrm{asElem}$ is a bijection; i.e. every element is contained in the image of $\mathrm{asElem}$. 

### Categorical set theories

There are also two-sorted categorical set theories such as the presentation of ETCS with one class of sets and one set of functions. 

### Allegorical set theories

## See also

* [[unsorted set theory]]
* [[two-sorted set theory]]
* [[dependently-sorted set theory]]

* [[structural set theory]]
* [[material set theory]]
* [[structurally presented set theory]]