
> This entry is about the notion in [[computer science]]. For the notion in [[particle physics]]/[[quantum gravity]] see at *[[string theory]]*.

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

In [[computer science]], "$String$" is a traditional name for the [[data type]] of [[lists]] of elements of a given [[alphabet]] $\mathscr{A}$.

From the point of view of [[categorical semantics]], the data type $String$ equipped with its evident [[concatenation]] functionality is the [[free monoid]] on $\mathscr{A}$. 

Moreover, from the point of view of [[monads in computer science|monads]] in [[functional programming]], the writing of consecutive log messages of type $String$ is desribed by the [[writer monad]] $Writer\big((String, conc)\big)$

## Related concepts

* [[stream]]

* [[data type]]

* [[list]], [[free monoid]]


## References

See also:

* Wikipedia, *<a href="https://en.wikipedia.org/wiki/String_(computer_science)">String_(computer_science)</a>*

[[!redirects strings (computer science)]]

[[!redirects string in computer science]]
[[!redirects strings in computer science]]


[[!redirects String (computer science)]]
[[!redirects Strings (computer science)]]
