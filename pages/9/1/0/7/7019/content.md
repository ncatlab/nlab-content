
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Homotopy theory
+--{: .hide}
[[!include homotopy - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

The term **homotopy level** (or **h-level**) -- originating in [[homotopy type theory]] -- is another name for the notion of [[truncated object|truncation]] (particularly in [[(∞,1)-categories]] and their 
[[internal logic|internal language]] of [[homotopy type theory]]) in which the numbering is offset by 2:

a [[homotopy n-type]] is a [[type]] of homotopy level $n+2$.  

This offset in counting enables it to "start" at 0 rather than (-2), which is convenient when defining it by induction over the natural numbers in type theory. 

## Definition ##

A [[type]] $A$ has a __homotopy level__ or __h-level__ of $n$ if the type $hasHLevel(n, A)$ is inhabited, for [[natural numbers|natural number]] $n:\mathbb{N}$.  $hasHLevel(n, A)$ is inductively defined as

$$hasHLevel(0, A) \coloneqq isContr(A)$$
$$hasHLevel(s(n), A) \coloneqq \prod_{a:A} \prod_{b:A} hasHLevel(n, a =_A b)$$

### Rules for hasHLevel

Suppose the dependent type theory has [[identity types]], [[contraction types]], and a [[natural numbers type]], but no [[dependent product types]] or [[dependent sum types]]. Then one could still define the type family $\mathrm{hasHLevel}(n, A)$ for all types $A$ in the context of the natural numbers variable $n:\mathrm{N}$, with the following rules: 

Formation rules for hasHLevel types:
$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, x:A \vdash \mathrm{Contr}_A(x) \; \mathrm{type}}{\Gamma \vdash \mathrm{hasHLevel}(0, A) \; \mathrm{type}}$$

$$\frac{\Gamma \vdash A \; \mathrm{type} \quad \Gamma, n:\mathbb{N}, x:A, y:A \vdash \mathrm{hasHLevel}(n, x =_A y) \; \mathrm{type}}{\Gamma, n:\mathbb{N} \vdash \mathrm{hasHLevel}(s(n), A) \; \mathrm{type}}$$

Introduction rules for hasHLevel types:
$$\frac{\Gamma, x:A \vdash b(x):\mathrm{Contr}_A(x) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:\mathrm{Contr}_A[a/x]}{\Gamma, n:\mathbb{N} \vdash (a, b):\mathrm{hasHLevel}(0, A)}$$

$$\frac{\Gamma, n:\mathbb{N}, x:A, y:A \vdash p(n, x, y):\mathrm{hasHLevel}(n, x =_A y)}{\Gamma, n:\mathbb{N} \vdash \lambda(x).\lambda(y).p(n, x, y):\mathrm{hasHLevel}(s(n), A)}$$

Elimination rules for hasHLevel types:
$$\frac{\Gamma \vdash z:\mathrm{hasHLevel}(0, A)}{\Gamma \vdash \pi_1(z):A} \qquad \frac{\Gamma \vdash z:\mathrm{hasHLevel}(0, A)}{\Gamma \vdash \pi_2(z):\mathrm{Contr}_A(\pi_1(z))}$$

$$\frac{\Gamma, n:\mathbb{N} \vdash p:\mathrm{hasHLevel}(s(n), A) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma, n:\mathbb{N} \vdash p(n, a, b):\mathrm{hasHLevel}(n, a =_A b)}$$

Computation rules for hasHLevel types:
$$\frac{\Gamma, x:A \vdash b(x):\mathrm{Contr}_A(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\mathrm{hasHLevel} 1}^0:\pi_1(a, b) =_A a} \qquad \frac{\Gamma, x:A \vdash b(x):\mathrm{Contr}_A(x) \quad \Gamma \vdash a:A}{\Gamma \vdash \beta_{\mathrm{hasHLevel} 2}^0:\pi_2(a, b) =_{\mathrm{Contr}_A(a)} b}$$

$$\frac{\Gamma, n:\mathrm{N}, x:A, y:A \vdash p(n, x, y):\mathrm{hasHLevel}(n, x =_A y) \quad \Gamma \vdash a:A \quad \Gamma \vdash b:A}{\Gamma, n:\mathrm{N} \vdash \beta_{\mathrm{hasHLevel}}^s:(\lambda(x).\lambda(y).p(n, x, y))(a, b) =_{\mathrm{hasHLevel}(n, a =_A b)} p(n, a, b)}$$

Uniqueness rules for hasHLevel types:
$$\frac{\Gamma \vdash z:\mathrm{hasHLevel}(0, A)}{\Gamma \vdash \eta_{\mathrm{hasHLevel}}^0:z =_{\mathrm{hasHLevel}(0, A)} (\pi_1(z), \pi_2(z))}$$

$$\frac{\Gamma, n:\mathbb{N} \vdash p:\mathrm{hasHLevel}(s(n), A)}{\Gamma, n:\mathbb{N} \vdash \eta_{\mathrm{hasHLevel}}^s:p(n) =_{\mathrm{hasHLevel}(s(n), A)} \lambda(x).\lambda(y).p(n, x, y)}$$

## Examples ##

* Every [[proposition]] has a homotopy level of $1$. 

* Every [[set]] has a homotopy level of $2$. 

The correspondence between the various terminologies is indicated in the following table:

[[!include homotopy n-types - table]]

## Referencees ##

The notion of "homotopy levels" (as a notion in [[type theory]]) originates with:

* {#Voevodsky10} [[Vladimir Voevodsky]], p. 8, 10-11 of: *Univalent Foundations Project* (2010) &lbrack;[pdf](http://www.math.ias.edu/~vladimir/Site3/Univalent_Foundations_files/univalent_foundations_project.pdf), [[Voevodsky-UFP2010.pdf:file]]&rbrack;

Further discussion:

* [[Guillaume Brunerie]], *Truncations and truncated higher inductive types* (2012) &lbrack;[blog post](https://homotopytypetheory.org/2012/09/16/truncations-and-truncated-higher-inductive-types/)&rbrack;

Discussion with [[Agda]]:

* [[1lab]], *[h-Levels](https://1lab.dev/1Lab.HLevel.html)*

Synonymous discussion, but under the name *[[homotopy n-type|$n$-types]]*, is in

* [[Univalent Foundations Project]], §7 of: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* [[Nicolai Kraus]], *Truncation levels in Homotopy Type Theory*, Nottingham (2015) &lbrack;[pdf](https://eprints.nottingham.ac.uk/28986/1/thesis.pdf), [eprints:28986](https://eprints.nottingham.ac.uk/28986)&rbrack;

See also:

* [[Thierry Coquand]], Ayberk Tosun, *Formal Topology in Univalent Foundations*, Ch. 6 in:  *Proof and Computation II -- From Proof Theory and Univalent Mathematics to Program Extraction and Verification*, Wold Scientific (2021) &lbrack;[doi:10.1142/12263](https://doi.org/10.1142/12263)&rbrack;



[[!redirects homotopy level]]
[[!redirects homotopy levels]]
[[!redirects h-level]]
[[!redirects h-levels]]

[[!redirects hlevel]]
[[!redirects hlevels]]

