
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Context
* table of contents
{: toc}

## Idea 

De Bruijn indices are used to represent [[terms]] in [[lambda calculus]] and [[type theory]] without naming [[bound variables]]. 

Usually in informal mathematical language, an expression involving a lambda is written out as $\lambda x.\phi(x)$. However, this involves the use of [[bound variables]], which are hard to deal with when formalizing [[substitution]] of variables; in addition, the statements $\lambda x.\phi(x)$ and $\lambda y.\phi(y)$ refer to the same thing. De Bruijn indices involve the use [[natural numbers]] instead of bound variables; both $\lambda x.\phi(x)$ and $\lambda y.\phi(y)$ would be written as $\lambda \phi(\underline{0})$ when using De Bruijn indices, and $\lambda x.\lambda y.\phi(x, y)$ would be written as $\lambda \lambda \phi(\underline{1}, \underline{0})$. A statement like $x \lambda x.\phi(x)$ where $x$ is both a bound variable and a free variable would be written as $\underline{1} \lambda \phi(\underline{0})$ using de Bruijn indices. 

## See also

* [[explicit substitution]]

## References 

de Bruijn indices are discussed in section 9.1 of:

* [[Théo Winterhalter]], *Formalisation and Meta-Theory of Type Theory*, Nantes (2020) &lbrack;[pdf](https://github.com/TheoWinterhalter/phd-thesis/releases/download/v1.2.1/TheoWinterhalter-PhD-v1.2.1.pdf), [github](https://github.com/TheoWinterhalter/phd-thesis)&rbrack;

The notion is due to:

* [[Nicolaas de Bruijn]], *Lambda Calculus Notation with Nameless Dummies, a Tool for Automatic Formula Manipulation, with Application to the Church-Rosser Theorem*, Indagationes Mathematicae (Proceedings) **75** 5 (1972) 381-392 &lbrack;<a href="https://doi.org/10.1016/1385-7258(72)90034-0">doi:10.1016/1385-7258(72)90034-0</a>, [pdf](http://alexandria.tue.nl/repository/freearticles/597619.pdf)&rbrack;

See also:

* Wikipedia, [De Bruijn index](https://en.wikipedia.org/wiki/De_Bruijn_index)

[[!redirects de Bruijn index]]

