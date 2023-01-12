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

## Definition ##

In [[dependent type theory]], an __identity system__ on a [[type]] $A$ is a [[correspondence]] on $A$, $a:A, b:A \vdash R(a, b)$, with a [[dependent function]] 
$$r_0: \prod_{a:A} R(a, a)$$ 
such that for any [[dependent type|family of types]] 
$$a:A, b:B, r:R(a, b) \vdash D(a, b, r)$$
and [[dependent function]] 
$$d:\prod_{a:A} D(a, a, r(a))$$ 
there exists a dependent function 
$$f:\prod_{a:A} \prod_{b:B} \prod_{r:R(a, b)} D(a, b, r)$$
and a dependent function
$$e:\prod_{a:A} f(a, a, r(a)) = d(a)$$

## See also ##

* [[identity type]]

* [[fundamental theorem of identity types]]

* [[one-to-one correspondence]]


## References ##

* [[Univalent Foundations Project]], Def. 5.8.3 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

* {#Rijke22} [[Egbert Rijke]], Def. 11.2.1 in: *[[Introduction to Homotopy Type Theory]]*, Cambridge Studies in Advanced Mathematics, Cambridge University Press (2023) &lbrack;[arXiv:2212.11082](https://arxiv.org/abs/2212.11082)&rbrack;