[[!redirects Univalent Foundations for Mathematics]]

#Contents#
* table of contents
{:toc}

## Idea 

A _univalent foundations for mathematics_ refers to any [[foundations of mathematics|foundational system]] in which [[universes]] are [[object classifiers]], or, equivalently, satisfy the [[univalence axiom]].


### In higher topos theory 

See at _[[object classifier]]_.

### In homotopy type theory

Voevodsky's univalent foundations ([UFIAS 12](#UFIAS12)) are an extension of [[Martin-Löf's dependent type theory]] obtained by adding:

* the [[univalence axiom]],

* [[propositional truncations]].

Notice that:

* [[function extensionality]] is implied by the [[univalence axiom]], so it is not necessary to assume separately;

* [[propositional resizing]] is sometimes also as an axiom;

* the [[UniMath]] library also uses _type in type_, which leads to an [[inconsistency]] via [[Girard's paradox]].

## Related entries

* [[univalence axiom]]

* [[UniMath project]]

## References

### In higher topos theory

* [[Jacob Lurie]], Section 6.1.6 of: _[[Higher Topos Theory]]_

### In type theory

* {#UFIAS12} [[UF-IAS-2012|Univalent Foundations Project]], _Homotopy Type Theory -- Univalent Foundations of Mathematics_ ([web](http://homotopytypetheory.org/book/), [pdf](http://hottheory.files.wordpress.com/2013/03/hott-online-323-g28e4374.pdf), [[Planet Math|PM]] [wiki version](http://planetmath.org/node/87534))

### Libraries with formalizations

* [UniMath](https://github.com/UniMath/UniMath)

* [Coq HoTT library](https://github.com/HoTT/HoTT)
