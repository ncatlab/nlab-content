+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--

# Contents
* table of contents
{: toc}

## Idea
{#Idea}

The term **higher-order abstract syntax** has been used to refer to several distinct, but related, concepts. In chronological order, and from least to most generality:

1. A [[logical framework]] proposed by &lbrack;[Pfenning & Elliot (1988)](#PfenningElliot88)&rbrack; based on the [[simply-typed lambda-calculus]] with [[polymorphism]].
2. The [[logical framework]] technique of representing [[abstract syntax]] for [[theories]] with [[variable-binding operators]] using the [[function types]] of another theory viewed as a meta-theory, popularised by [[LF]] and Pfenning–Elliot's logical framework described in (1).
3. [[abstract syntax|Abstract syntax]] for [[theories]] with variable-binding operators, metavariable-binding operators, and so on. The logical framework technique in (2) is a particular representation of such abstract syntax.

Usage (1) does not appear to be in common usage. Usage (2) tends to be the convention in literature on [[logical frameworks]]; while usage (3) is the convention in literature on algebraic type theory, though note that authors often restrict to [[second-order abstract syntax]], which is sufficient for most [[type theories]].

Examples of variable-binding operators are [[lambda-abstraction]] and [[quantifiers]] (e.g. in [[higher-order logic]], whence the name).

## Higher-order abstract syntax in logical frameworks

In logical frameworks, one formalizes [[languages]] supporting forms of [[name binding]] (such as function parameters or [[quantifiers]]) by using the meta-language [[function space]] rather than a more syntactic notion of [[bound variable]].

## Higher-order abstract syntax in algebraic type theory

Traditional approaches to [[abstract syntax]], e.g. for [[algebraic theories]], typically involve [[abstract syntax trees]]. However, it is not possibly directly to capture [[variable-binding operators]] with such structures. Therefore, alternative structures are necessary to capture the syntax of [[theories]] with such operators, e.g. [[type theories]].

One possible approach is via the [[logical framework]] approach described above.

## Related Concepts

* [[abstract syntax tree]]

* HOAS is used extensively in [[logical frameworks]]

* [[synthetic Tait computability]]

## References

* {#PfenningElliot88} [[Frank Pfenning]], Conal Elliot, *Higher-order abstract syntax*, ACM SIGPLAN Notices **23** 7 (1988) 199–208 &lbrack;[doi;10.1145/960116.54010](https://doi.org/10.1145/960116.54010), [pdf](https://www.cs.cmu.edu/~fp/papers/pldi88.pdf)&rbrack;

* [[Martin Hofmann]], _Semantical analysis of higher-order abstract syntax_, LICS 1999 &lbrack;[ieee:782616](https://ieeexplore.ieee.org/document/782616), [doi:10.1109/LICS.1999.782616](https://doi.ieeecomputersociety.org/10.1109/LICS.1999.782616)&rbrack;

* [[Marcelo Fiore]], [[Gordon Plotkin]], [[Daniele Turi]]. _Abstract syntax and variable binding_, Proceedings. 14th Symposium on Logic in Computer Science (Cat. No. PR00158). IEEE (1999) &lbrack;[doi:10.1109/LICS.1999.782615](https://doi.org/10.1109/LICS.1999.782615), [pdf](https://homepages.inf.ed.ac.uk/gdp/publications/Abstract_Syn.pdf), [webpage](https://www.dcs.ed.ac.uk/home/dt/abstractsyn.html)&rbrack;

* [[Marcelo Fiore]], [[Chung-Kil Hur]]. _Second-order equational logic_, International Workshop on Computer Science Logic. Springer, Lecture Notes in Computer Science **6247** (2010) &lbrack;[doi:10.1007/978-3-642-15205-4_26](https://doi.org/10.1007/978-3-642-15205-4_26), [pdf](https://www.cl.cam.ac.uk/~mpf23/papers/Types/soeqlog.pdf)&rbrack;


See also: 

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/Higher-order_abstract_syntax">Higher-order abstract syntax</a>*


[[!redirects HOAS]]