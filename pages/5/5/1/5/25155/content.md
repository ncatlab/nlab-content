
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Set theory
+-- {: .hide}
[[!include set theory - contents]]
=--
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
=--
=--

\tableofcontents

## Definition

### In set theory

Let $\mathbb{N}$ be the set of natural numbers, and let $A$ be an arbitrary set. Then **sequence extensionality** states that for every [[sequence]] $a:\mathbb{N} \to A$ and $b:\mathbb{N} \to A$, $a =_{\mathbb{N} \to A} b$ if and only if $a(n) =_A b(n)$ for all natural numbers $n \in \mathbb{N}$. 

### In category theory

Sequence extensionality in an [[arithmetic pretopos]] states that for every morphism $a:\mathbb{N} \to A$ and $b:\mathbb{N} \to A$, $a =_{\mathbb{N} \to A} b$ if and only if $a \circ n =_{\mathbb{1} \to A} b \circ n$ for all morphisms $n:\mathbb{1} \to \mathbb{N}$. 

This definition makes sense in any finitely complete category with a parameterized [[natural numbers object]]. 

### In dependent type theory

In [[dependent type theory]], sequence extensionality states that given two sequences $a:\mathbb{N} \to A$ and $b:\mathbb{N} \to A$ there is an [[equivalence of types]] between the [[identity type]] $a =_{\mathbb{N} \to A} b$ and the [[dependent sequence type]] $(n:\mathbb{N}) \to (a(n) =_{A} b(n))$:
$$\frac{\Gamma \vdash A \; \mathrm{type}}{\Gamma, a:\mathbb{N} \to A, b:\mathbb{N} \to A \vdash \mathrm{seqext}(a, b):(a =_{\mathbb{N} \to A} b) \simeq (n:\mathbb{N}) \to (a(n) =_{A} b(n))}$$

There is also a version of sequence extensionality for [[dependent sequence types]] called dependent sequence extensionality, which states that given two dependent sequences $a:(n:\mathbb{N}) \to A(n)$ and $b:(n:\mathbb{N}) \to A(n)$ there is an [[equivalence of types]] between the [[identity type]] $a =_{(n:\mathbb{N}) \to A(n)} b$ and the [[dependent sequence type]] $(n:\mathbb{N}) \to (a(n) =_{A(n)} b(n))$:
$$\frac{\Gamma, n:\mathbb{N} \vdash A(n) \; \mathrm{type}}{\Gamma,a:(n:\mathbb{N}) \to A(n), b:(n:\mathbb{N}) \to A(n) \vdash \mathrm{dseqext}(a, b):(a =_{(n:\mathbb{N}) \to A(n)} b) \simeq (n:\mathbb{N}) \to (a(n) =_{A(n)} b(n))}$$

## Properties

While [[function extensionality]] implies sequence extensionality, sequence extensionality is weaker than function extensionality. However, sequence extensionality is usually more relevant in [[dependent type theories]] which are [[strongly predicative]], which usually have [[dependent sequence types]] but do not have general [[dependent function types]]. 

## See also

* [[extensionality]]
* [[function extensionality]]

[[!redirects sequence extensionality]]
[[!redirects dependent sequence extensionality]]