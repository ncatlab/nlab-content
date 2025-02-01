+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Foundations
+-- {: .hide}
[[!include foundations - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

In usual presentations of categorical set theories such as [[ETCS]], the set theory is usually a theory of [[sets]] and [[functions]] in an abstract [[category]], with [[elements]] being defined as the [[global elements]], the [[morphisms]] out of the [[terminal object]]. However, this approach poses a few conceptual and practical issues, namely that in ordinary mathematical practice, elements are not the same as functions out of the terminal set $\mathbb{1}$, although $A$ is in bijection with the function set $A^\mathbb{1}$, and function evaluation of elements defined as function composition of functions out of the terminal set is an abuse of notation. 

There are other [[structural set theories]], such as [[SEAR]], which explicitly put in the elements of a set as a primitive of the theory. In such a theory involving sets and functions, function evaluation would be a primitive of the theory, rather than derived from function composition of [[global elements]], and the axiom of function extensionality is likewise defined directly on the elements. Such a theory reads more like a traditional presentation of set theory in terms of sets and elements, rather than category theory. However, in contrast to [[SEAR]], this theory is essentially the same structurally as [[ETCS]]: as a theory of sets and functions. 

In this presentation, we will be adapting [[Tom Leinster]]'s presentation of ETCS. 

## Basic primitives ##

Our theory has the following primitives:

* Some things called **sets**;

* For every set $A$, these things called **elements in $A$**, with elements $a$ in $A$ written as $a \in A$;

* For every set $A$ and $B$, these things called **functions from $A$ to $B$**, with functions $f$ from $A$ to $B$ written as $f:A \to B$;

* For every set $A$ and $B$, an operation called **function evaluation** assigning every element $a \in A$ and function $f:A \to B$ an element $f(a) \in B$;

* For every set $A$, a function $id_A:A \to A$ called the **identity function of $A$**;

* For every set $A$, $B$, and $C$, an operation called **function composition** assigning every function $f:A \to B$ and $g:B \to C$ a function $g \circ f:A \to C$;

## Equality of elements and functions ##

For every set $A$ and elements $a \in A$ and $b \in A$, there is a relation $a = b$ called **equality of elements**, such that 

* for every element $a \in A$, $a = a$
* for every element $a \in A$ and $b \in A$, $a = b$ implies that $b = a$
* for every element $a \in A$, $b \in A$, and $c \in A$, $a = b$ and $b = c$ implies that $a = c$. 

For every set $A$ and $B$ and functions $f:A \to B$ and $g:A \to B$, there is a relation $f = g$ called **equality of functions**, such that 

* for every function $f:A \to B$, $f = f$
* for every function $f:A \to B$ and $g:A \to B$, $f = g$ implies that $g = f$
* for every function $f:A \to B$, $g:A \to B$, and $h:A \to B$, $f = g$ and $g = h$ implies that $f = h$. 

## Basic axioms for functions ##

**Axiom of identity functions.** For every set $A$ and for every element $a \in A$, $id_A(a) = a$.

**Axiom of composition/evaluation equivalence.** For every set $A$, $B$, and $C$, and for every element $a \in A$, $(g \circ f)(a) = g(f(a))$.

**Axiom of extensionality.** For every set $A$ and $B$ and for every function $f:A \to B$ and $g:A \to B$, if $f(x) = g(x)$ for all elements $x \colon A$, then $f = g$. 

The associativity and unit laws of function composition follow from the axioms:

* For every set $A$ and $B$, function $f:A \to B$, and element $a \in A$, 
$$(g \circ id_A)(a) = g(id_A(a)) = g(a)$$ 
and extensionality implies that $g \circ id_A = g$. 

* For every set $A$ and $B$, function $f:A \to B$, and element $a \in A$, 
$$(id_B \circ g)(a) = id_B(g(a)) = g(a)$$ 
and extensionality implies that $id_B \circ g = g$. 

* For every set $A$, $B$, $C$, and $D$, function $f:A \to B$, $g:B \to C$, and $h:C \to D$, and element $a \in A$, 
$$(h \circ (g \circ f))(a) = h((g \circ f)(a)) = h(g(f(a)) = (h \circ g)(f(a)) = ((h \circ g) \circ f)(a)$$
and extensionality implies that $h \circ (g \circ f) = (h \circ g) \circ f$.

Thus, these axioms imply that the collection of sets, functions, and elements form a [[category]].

## Other axioms ##

**Axiom of singletons.** There is a set $\mathbb{1}$, called a **singleton**, with a unique element $* \in \mathbb{1}$, called a **point**. 

**Axiom of the empty set.** There exists a set $\emptyset$ with no elements.

**Axiom of Cartesian products.** For every set $A$ and $B$, there is a set $A \times B$, called a **Cartesian product** of $A$ and $B$, with a function $p_A:A \times B \to A$ called the **projection onto $A$** and a function $p_B:A \times B \to B$ called the **projection onto $B$**, such that given two elements $a \in A$ and $b \in B$ there is a unique element $a, b \in A \times B$ such that $p_A(a, b) = a$ and $p_B(a, b) = b$. 

**Axiom of fibers.** For every set $A$ and $B$, element $b \in B$, and function $f:A \to B$, there is a set $f^{-1}(b)$ called the **fiber** of $f$ over $b$ with a function $i:f^{-1}(b) \to A$, such that for every element $a \in f^{-1}(b)$, $f(i(a)) = b$, and for every other set $C$ and function $g:C \to A$ such that for every element $c \in C$, $f(g(c)) = b$, there is a unique function $j:C \to f^{-1}(b)$ such that for every element $c \in C$, $g(c) = i(j(c))$. A fiber of $f$ over $b$ is also called the **solution set** of the equation $f(x) = b$. 

An **injection** is a function $f:A \to B$ such that for every element $a \in A$ and $b \in A$, if $f(a) = f(b)$, then $a = b$. 

**Axiom of truth values.** There is a set $\Omega$ called a **set of truth values** with an element $\top \in \Omega$ called **true** such that for every set $A$ and $B$ and injection $f:A \to B$, there is a unique function $\chi_A:B \to \Omega$ called the **classifying function** of $A$ such that $A$ is the fiber of $\chi_A$ over $\top$. 

**Axiom of function sets.** For every set $A$ and $B$ there is a set $B^A$ called the **function set** with a function $(-)((-)):B^A \times A \to B$ such that for every set $C$ and function $f:C \times A \to B$ there is a unique function $g:C \to B^A$ such that for all elements $c \in C$ and $a \in A$, $g(c)(a) = f(c, a)$. 

**Axiom of natural numbers.** There exists a set $\mathbb{N}$ called a **set of natural numbers** with an element $0 \in \mathbb{N}$ and a function $s:\mathbb{N} \to \mathbb{N}$ such that for every other set $A$ with an element $a \in A$ and a function $g:A \to A$, there is a unique function $f:\mathbb{N} \to A$ such that $f(0) = a$ and $f(s(a)) = g(f(a))$. 

A **surjection** is a function $f:A \to B$ such that for every $b \in B$ the fiber of $f$ at $b$ is inhabited. A **right inverse** of $f$ is a function $g:B \to A$ such that for all elements $a \in A$, $f(g(a)) = a$. A **choice set** is a set $B$ such that all surjections into $B$ have right inverses. 

**Axiom of choice.** Every set is a choice set. 

These axioms imply that the collection of sets, functions, and elements form a model of [[ETCS]].

## See also ##

* [[ETCS]]

* [[Trimble on ETCS I]]

* [[SEAR]]

## References ##

* [[Tom Leinster]], Rethinking set theory, ([arxiv:1212.6543](https://arxiv.org/abs/1212.6543))