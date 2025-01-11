
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
=--
=--

\tableofcontents

## Idea

The notion of commutativity of an $n$-ary operation in the sense that the order of the parameters can be permuted without changing the result. For $n = 2$ this results in the notion of a [[commutative magma]]. 

## Definition

An [[n-ary operation|$n$-ary operation]] is a function $f:A^n \to A$ from the [[cartesian power]] $A^n$ to $A$. 

Let $\mathrm{Fin}(n)$ denote the standard [[finite set]] with $n$ elements. Given a set $A$, the [[Cartesian power]] $A^n$ is isomorphic to the [[function set]] $\mathrm{Fin}(n) \to A$. As a result, one can equivalently define an $n$-ary operation as a function $f:(\mathrm{Fin}(n) \to A) \to A$ from the function set $\mathrm{Fin}(n) \to A$ to $A$. The function set $\mathrm{Fin}(n) \to A$ represents the set of possible parameters of the $n$-ary operation, and individual functions $a:\mathrm{Fin}(n) \to A$ represents individual possible parameters. 

Using the function set definition, a permutation of the parameters of the $n$-ary operation is the [[composition]] of the parameters $a:\mathrm{Fin}(n) \to A$ with a [[bijection]] $h:\mathrm{Fin}(n) \simeq \mathrm{Fin}(n)$ on the standard finite set with $n$ elements. 

\begin{definition}
An $n$-ary operation $f:(\mathrm{Fin}(n) \to A) \to A$ is **commutative** if for all functions $a:\mathrm{Fin}(n) \to A$ and bijections $h:\mathrm{Fin}(n) \simeq \mathrm{Fin}(n)$, $f(a) = f(a \circ h)$. 
\end{definition}

## Examples

### Commuative binary operations

When $n = 2$, the standard finite set with two elements $\mathrm{Fin}(2)$ is in [[bijection]] with the [[boolean domain]], which means we can simply use the boolean domain $\mathrm{bool}$ in place of $\mathrm{Fin}(2)$. There are two bijections on the boolean domain $\mathrm{bool}$, the identity function and the swap function which swaps the two elements around. By definition of the [[identity function]], it is always true that $f(a) = f(a \circ \mathrm{id}_{\mathrm{bool}})$. Thus, the only relevant thing left to check is the swap function:

\begin{definition}
A [[binary operation]] $f:(\mathrm{bool} \to A) \to A$ is **commutative** if for all functions $a:\mathrm{bool} \to A$, $f(a) = f(a \circ \mathrm{swap})$. 
\end{definition}

After applying the isomorphism between $\mathrm{bool} \to A$ and the [[cartesian square]] $A^2$ constructed from the [[recursion principle]] of the [[boolean domain]], this definition results in the usual notion of [[commutative magma]]: 

\begin{definition}
A [[binary operation]] $f:A^2 \to A$ is **commutative** if for all functions $a:\mathrm{bool} \to A$, $f(a(0), a(1)) = f(a(1), a(0))$. 
\end{definition}

### Commuative unary and nullary operations

By the above definition, every unary operation ($n = 1$) is commutative because there is only one bijection on the standard finite set with one element, the identity function on $\mathrm{Fin}(1)$, and $f(a) = f(a \circ \mathrm{id}_{\mathrm{Fin}(1)})$. Similarly, every constant, considered as a nullary operation ($n = 0$), is commutative because there is only one bijection on the standard finite set with zero elements, the identity function on $\mathrm{Fin}(0)$, and for the unique function $u:\mathrm{Fin}(0) \to A$ (since $\mathrm{Fin}(0)$ is the [[initial object|initial set]]), $f(u) = f(u \circ \mathrm{id}_{\mathrm{Fin}(0)})$. 

## Infinitary operations

The notion of a commutative operation can be extended from finitary operations to infinitary operations. The idea here is that an infinitary operation on a set $A$ consists of a set $I$ of arities and a function $f:(I \to A) \to A$. The notion of commutativity in the sense of permuting the parameters resulting in an equal element still makes sense for infinitary operations:  

\begin{definition}
An infinitary operation $f:(I \to A) \to A$ is **commutative** if for all functions $a:I \to A$ and bijections $b:I \cong I$, $f(a) = f(a \circ b)$. 
\end{definition}

Examples of commutative infinitary operations include the $I$-indexed joins of a [[complete lattice]] for arbitrary set $I$, and the $\mathbb{N}$-indexed joins of a [[sigma-complete lattice]]. 

## Related concepts

* [[commutative magma]]

[[!redirects commutative operation]]
[[!redirects commutative operations]]
[[!redirects commutative]]
[[!redirects commutativity]]