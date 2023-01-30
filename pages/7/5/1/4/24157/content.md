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

## Definition ##

In [[dependent type theory]], an __identity system__ on a [[type]] $A$ is a [[correspondence]] on $A$, $a:A, b:A \vdash R(a, b)$, with a [[dependent function]] 
$$a:A \vdash r_0(a):R(a, a)$$ 
such that for any [[dependent type|family of types]] 
$$a:A, b:A, p:R(a, b) \vdash C(a, b, p)$$
there exists a dependent function 
$$t:\prod_{c:A} C(c, c, r_0(c)), a:A, b:A, p:R(a, b) \vdash J(t, a, b, p):C(a, b, p)$$
and a dependent function
$$t:\prod_{c:A} C(c, c, r_0(c)), a:A \vdash \beta(t, a):J(t, a, a, r_0(a)) =_{C(a, a, r_0(a))} t(a)$$

## See also ##

* [[identity type]]

* [[fundamental theorem of identity types]]

* [[one-to-one correspondence]]


## References ##

* [[Univalent Foundations Project]], Def. 5.8.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], Def. 11.2.1 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;