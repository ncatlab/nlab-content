
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea

In [[dependent type theory]], what is known as the *variable rule* (or *projection rule*) is the [[structural rule|structural]] [[inference rule]] which, informally speaking, asserts for any [[dependent type]] $A$ the apparent [[tautology]] that "given a variable $a \colon A$" (as a [[hypothesis]]/[[antecedent]]) "then we have that variable $a \colon A$" (as a [[succedent]]).

$$
  VAR
  \frac{
    \Gamma
    \;\;\;\;
    \vdash
    \;\;\;\;
    A \colon Type
  }{
    \Gamma
    ,\;
    a \colon A
    \;\;\;\;
    \vdash
    \;\;\;\;
    a \colon A
  }
$$

As usual in [[dependent type theory]], the meaning of this rule is a little less trivial than it may superficially seem by the generic [[dependent type|type dependency]] involved: In the [[antecedent]] the variable may be picked out of a [[context]] [[type telescope|telescope]], and in the [[succedent]] it is implicitly [[weakening rule|weakened]] to depend on that full context, -- which includes $a \colon A$ itself! 

Accordingly, the [[categorical semantics]] [[categorical semantics of dependent types|as dependent types]] of the variable rule is given by the [[diagonal]] morphism on the [[object]] interpreting $A$, regarded as a [[section]] of the [[pullback bundle|pullback]] of the [[bundle]]/[[display map]] $A \to \Gamma$ to its own total space:

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>

## Related concepts

* [[variable]]

* [[structural rule]]

  [[weakening rule]]

  [[substitution rule]]

## References

* {#UFP13} [[Univalent Foundations Project]], p. 422 in: *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], p. 4 of: *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])






