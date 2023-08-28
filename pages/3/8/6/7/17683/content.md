


+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Computing
+-- {: .hide}
[[!include constructivism - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}


## Idea 

In [[computer science]], under *imperative programming* one understands a [[programming language]]-style in which a program largely consists of 

1. a succession of *commands* (whence "imperative")

1. for (in particular) accessing and modifying the *global state* of the computing environment 

   (such as the [[RAM]] and [[I/O]]-devices).

A typical example of imperative [[pseudocode]] would be of the form

> `n <- Read`

> `n++`

> `Write n`

being the sequence of commands to, in this case:

1. read a (numerical) datum (from some input device) and store it in a global variable `n`

1. increment `n`

1. write the value of `n` (to some output device).

Low-level languages are often imperative, reflecting the actual operation of the underlying computing machine; and medium-level imperative languages may be felt to have a transparent flow logic. 

In its naive form the access and modification of global state variables means that imperative programs are hard to [[software verification|verify]] (since there is no guarantee that the global state is in the assumed form). This is generally in contrast to *pure* [[functional programming languages]], which enforce that every procedure be a *pure function* in that its output and side-effect depends deterministically on its input (instead of also on the value of some global variables).

On the other hand, much of the features of imperative programs with access to a global state can be emulated/encapsulated in pure [[functional programming languages]] via the scheme of [[monad in computer science|monadic data types]] (see there for more). With the [[syntactic sugar]] of [do-notation](monad+in+computer+science#DoNotation) &lbrack;[Launchbury 1993 §3.3](#Launchbury93)&rbrack; this allows purely functional languages to look essentially like imperative code while remaining [[software verification|verifiable]].



## Related concepts

* [[functional programming]]

* [[object-oriented programming]]

* [[monad (in computer science)]]


## References

See also:

* Wikipedia, _[Imperative programming](https://en.wikipedia.org/wiki/Imperative_programming)_

The origin of [do-notation](monad+in+computer+science#DoNotation) for emulating imperative programming in [[functional programming languages]] via [[monad in computer science|monadic data types]]:

* {#Launchbury93} [[John Launchbury]], §3.3 in: *Lazy imperative programming*, Proceedings of *ACM Sigplan Workshop on State in Programming Languages*, Copenhagen (1993) &lbrack;[pdf](https://launchbury.files.wordpress.com/2019/01/lazy-imperative-programming.pdf), [[Launchbury-LazyImperative.pdf:file]]&rbrack;


Conversely, building features of [[functional programming languages]] into imperative languages:

* David R. Cok, *Reasoning about functional programming in Java and C++*, ISSTA '18: Companion Proceedings for the ISSTA/ECOOP 2018 WorkshopsJuly 2018 Pages 37–39 ([doi:10.1145/3236454.3236483](https://doi.org/10.1145/3236454.3236483))

[[!redirects imperative programming language]]
[[!redirects imperative programming languages]]

[[!redirects imperative program]]
[[!redirects imperative programs]]


