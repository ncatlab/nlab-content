
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Structural rules
* table of contents
{: toc}

## Idea

### General

The _structural rules_ of a [[logic]] or [[deductive system]] are those rules which make no reference to logical operators but only to the unstructured [[premise]]s of a [[deduction]].

In standard [[intuitionistic logic]] the structural rules notably include the [[weakening rule]] and the [[contraction rule]]. Discarding these rules leads to [[linear logic]]. Generally, logical systems discarding some structural rules are called *[[substructural logics]]*.

### In dependent type theory
 {#InDependentTypeTheory}

In ([[intuitionistic type theory|intuitionistic]]) [[dependent type theory]] the structural rules include (e.g. [Jacobs (1998), p. 122](#Jacobs98), [UFP13, A.2.2](#UFP13), [Rijke (2018), Sec. 1.4](#Rijke18)):

* the [[variable rule]], 

* the [[weakening rule]], 

* the [[substitution rule]]

shown in the following table together with their [[categorical semantics]] [[categorical semantics of dependent types|of dependent types]]:

<center>
<img src="/nlab/files/DependentTermsSyntaxAndSemantics-230326.jpg" width="650">
</center>

<center>
<img src="/nlab/files/StructuralTypeInferenceRules-230326b.jpg" width="650">
</center>




## Examples

* the [[weakening rule]],

* the [[contraction rule]],

* the [[exchange rule]],

* the [[identity rule]],

* the [[cut rule]].


## Related pages

* [[substructural logic]] is logic in which one or more structural rules are omitted.

## References

Discussion in [[dependent type theory]]:


* {#Jacobs98} [[Bart Jacobs]], Chapter 10 in: *Categorical Logic and Type Theory*, Studies in Logic and the Foundations of Mathematics **141**, Elsevier (1998)  &lbrack;[ISBN:978-0-444-50170-7](https://www.sciencedirect.com/bookseries/studies-in-logic-and-the-foundations-of-mathematics/vol/141), [pdf](https://people.mpi-sws.org/~dreyer/courses/catlogic/jacobs.pdf)&rbrack;

  > (emphasis on the [[categorical model of dependent types]])

* {#UFP13} [[Univalent Foundations Project]], §A of *[[Homotopy Type Theory -- Univalent Foundations of Mathematics]]* (2013) &lbrack;[web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf)&rbrack;

  > (in the context of [[homotopy type theory]])


* {#Rijke18} [[Egbert Rijke]], *Dependent type theory* &lbrack;[pdf](https://www.andrew.cmu.edu/user/erijke/hott/dtt.pdf)&rbrack;, Lecture 1 in: *[[Introduction to Homotopy Type Theory]]*, lecture notes, CMU (2018) &lbrack;[pdf](http://www.andrew.cmu.edu/user/erijke/hott/hott_intro.pdf), [[Rijke-IntroductionHoTT-2018.pdf:file]], [webpage](https://www.andrew.cmu.edu/user/erijke/hott/)&rbrack;

  > (in the context of [[homotopy type theory]])


[[!redirects structural rule]]
[[!redirects structural rules]]
