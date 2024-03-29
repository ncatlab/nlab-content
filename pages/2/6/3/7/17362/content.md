
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

##Idea

In [[computer science]] and to some extent also in [[formal logic]], **sugaring** refers to the modification of formal notation ([[syntax]]) into a form which is more readable for humans, thereby "sweetening" it for consumption. Syntactic sugar does not add to the functionality or expressivity of the language.

[[Peter Landin]] first used the expression 'syntactic sugaring' in the context of interpretations of terms in the [[λ-calculus]] ([Landin64](#Landin64)).

The reverse process to expressions in the more formal language is sometimes known as 'desugaring'.



## Examples


+-- {: .num_example}
###### Example

In a [[set theory]] where [[classes]] are not "first-class objects" (for example [[ZFC]], but not [[NBG]]), classes are only syntactic sugar and have no independent existence. For instance, if one defines a class $M \coloneqq \{ X | \varphi(X) \}$ by [[comprehension]], then "$X \in M$" is syntactic sugar for "$\varphi(X)$".

=--

+-- {: .num_example}
###### Example

In [[formal linguistics]], natural language versions of formal expressions are described as 'sugarings' (Ranta 1994). Often there are many ways to sugar a formal expression into natural language. 

Consider the [[type theory|type theoretic]] expression $\sum_{x: man} \sum_{y: donkey} (x\;owns\; y)$. Ranta (1994, p. 68) gives nine natural language sugarings for it by applying three different operations twice:

* there is a man and there is a donkey and he owns it,
* there is a man and he owns a donkey,
* there is a man and there is a donkey that he owns,
* there is a donkey and a man owns it,
* a man owns a donkey,
* there is a donkey that a man owns,
* there is a man such that there is a donkey and he owns it,
* there is a man who owns a donkey,
* there is a man such that there is a donkey that he owns.

=--


## References

* {#Landin64} [[Peter Landin]], _The mechanical evaluation of expressions_ &lbrack;[pdf](http://www.cs.cmu.edu/~crary/819-f09/Landin64.pdf)&rbrack;

* {#Ranta93} [[Aarne Ranta]], _Type theory and the informal language of mathematics_, TYPES '93: Proceedings of the international workshop on Types for proofs and programs, pp. 352–365, ([pdf](/nlab/files/InfLang.pdf))

* {#Ranta94} [[Aarne Ranta]], §1.6, §1.7, §9 in: *Type-theoretical grammar*, Oxford University Press (1994) &lbrack;[ISBN:9780198538578](https://global.oup.com/academic/product/type-theoretical-grammar-9780198538578)&rbrack;


See also:

* Wikipedia, *[Syntactic sugar](https://en.wikipedia.org/wiki/Syntactic_sugar)*

[[!redirects syntactic sugar]]