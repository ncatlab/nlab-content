+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Type theory
+--{: .hide}
[[!include type theory - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Idea

In [[dependent type theory]], an **identity system** is a [[correspondence]] on a type $A$

$$a:A, b:A \vdash R(a, b)$$

which behaves like a [[weak identity type]] on $A$. 

Identity systems are very useful in characterizing the [[extensionality]] principle of [[types]] such as [[function types]], [[dependent function types]], and [[Tarski universes]]. 

## Definition

In [[dependent type theory]], an __identity system__ on a [[type]] $A$ is a [[correspondence]] on $A$, $a:A, b:A \vdash R(a, b)$, with a [[dependent function]] 
$$a:A \vdash r_0(a):R(a, a)$$ 
such that for any [[dependent type|family of types]] 
$$a:A, b:A, p:R(a, b) \vdash C(a, b, p)$$
there exists a dependent function 
$$t:\prod_{c:A} C(c, c, r_0(c)), a:A, b:A, p:R(a, b) \vdash J(t, a, b, p):C(a, b, p)$$
and a dependent function
$$t:\prod_{c:A} C(c, c, r_0(c)), a:A \vdash \beta(t, a):J(t, a, a, r_0(a)) =_{C(a, a, r_0(a))} t(a)$$

## Extensionality principles

* [[product extensionality]] states that the correspondence 
$$x:A \times B, y:A \times B \vdash (\pi_1(x) =_A \pi_1(y)) \times (\pi_2(x) =_B \pi_2(y))$$
is an identity system. 

* dependent pair extensionality states that the correspondence 
$$y:\sum_{x:A} B(x), z:\sum_{x:A} B(x) \vdash \sum_{p:\pi_1(y) =_A \pi_1(z)} \pi_2(y) =_{x:A.B(x)}^p \pi_2(z)$$
is an identity system. 

* [[function extensionality]] states that the correspondence 
$$f:A \to B, g:A \to B \vdash \prod_{x:A} \mathrm{ev}(f, x) =_B \mathrm{ev}(g, x)$$
is an identity system. 

* dependent function extensionality states that the correspondence 
$$f:\prod_{x:A} B(x), g:\prod_{x:A} B(x) \vdash \prod_{x:A} \mathrm{ev}(f, x) =_{B(x)} \mathrm{ev}(g, x)$$
is an identity system. 

* [[univalence]] or [[universe extensionality]] states that the correspondence 
$$A:U, B:U \vdash T(A) \simeq T(B)$$
is an identity system. 

## See also ##

* [[identity type]]

* [[fundamental theorem of identity types]]

* [[one-to-one correspondence]]

* [[extensionality]]

## References ##

* [[Univalent Foundations Project]], Def. 5.8.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], Def. 11.2.1 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;