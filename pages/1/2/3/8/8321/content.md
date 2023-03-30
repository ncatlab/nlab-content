
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# The weakening rule
* table of contents
{: toc}

## Idea

In [[formal logic]] and [[type theory]], by "weakening rules" one means [[inference rules]] for [[context extension]],
which state that any [[premises]] may be added to the [[hypotheses]] ([[antecedents]]) of a valid [[judgement]].

Along with the [[variable rule]], the [[contraction rule]] and the [[exchange rule]], the weakening rule is one of the most commonly adopted [[structural rules]]. But the weakening rule is not used in all [[logical frameworks]], for instance in [[linear logic]] it is discarded.

Concretely, in [[intuitionistic type theory|intuitionistic]] [[dependent type theory]] the weakening rule is the [[inference rule]]

$$
  W
  \frac{
    \Gamma
    ,\,
    \Delta
    \;
      \vdash
    \;
    j \colon J
    \;\;\;\;\;\;\;\;
    \Gamma
    \;
      \vdash
    \;
    A \colon Type
  }{
    \Gamma
    ,\;
    A 
    ,\,
    \Delta
    \;
    \vdash
    \;
    j \colon J
  }
$$

As usual in [[dependent type theory]], the meaning of this rule is a little less trivial than it may superficially seem, due to the generic [[dependent type|type dependency]] involved: In [[context extension|extending the contents]] in the [[antecedent]] we are implicitly making the [[succedent]] [[dependent type|depend]] on this extended context, albeit trivially.

Accordingly, in the [[categorical semantics]] [[categorical semantics of dependent types|of dependent types]] the weakening rule corresponds to [[pullback]] of [[bundles]]/[[display maps]] to the [[fiber product]] which interprets the extended context:

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>


## Semantics

Weakening rules correspond to having [[semicartesian monoidal category|projections for the monoidal structure]] that corresponds to the logical binary operator at hand.

## Related concepts

* [[structural rules]]

  [[variable rule]]

  [[substitution rule]]

## References

Discussion in [[intuitionistic type theory|intuitionistic]] [[dependent type theory]]:

* {#Jacobs98} [[Bart Jacobs]], p. 122 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], §A of *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])




[[!redirects weakening rule]]
[[!redirects weakening rules]]
