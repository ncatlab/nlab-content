
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Type theory
+-- {: .hide}
[[!include type theory - contents]]
=--
=--
=--



# Looping combinators
* table of contents
{: toc}


## Idea

In [[combinatory logic]], in the [[∞-calculus]], or more generally in [[type theory]], a *looping [[combinator]]* is closely akin to a [[fixed-point combinator]], but rather than producing a true [[fixed point]], it produces a sequence of points each of which is the [[image]] of the next.

## Definition

+-- {: .num_defn}
###### Definition
A term $Y$ is a **looping combinator** if for any [[function type|function]] [[term]] $f$ to which $Y$ can be applied, we have a [[beta reduction]]
$$ Y f \to_\beta f (Y' f) $$
where $Y'$ is a looping combinator.
=--

This is a [[coinductive definition]].  Unraveled explicitly, it means that a looping combinator $Y = Y_0$ comes with a sequence of combinators $Y_n$ for $n\in\mathbb{N}$ and reductions
$$ Y_n f \to_\beta f(Y_{n+1} f).$$

## Implementing general recursion

A looping combinator is essentially just as good as a [[fixed-point combinator]] for implementing general [[recursion]].  See the discussion there for details.

## Existence

[[Per Martin-Löf]]'s original [[dependent type theory]], which had the additional rule $\vdash Type:Type$, was shown to be [[inconsistency|inconsistent]] by [[Girard's paradox]].  In the 1980's, Meyer, Reinhold, and Howe (see references) showed that this paradox could be modified to construct a looping combinator.

## References

In the short paper

* Albert Meyer and Mark Reinhold, "'Type' is not a type", POPL 1986

it was claimed that from Girard's paradox one could actually construct a fixed-point combinator.  The proof turned out to be flawed, but it was sufficient to produce a looping combinator.  Details can be found in

* Mark Reinhold, "Typechecking is Undecidable When 'Type' is a Type", 1989, [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.18.7073)

* Douglas Howe, "The Computational Behaviour of Girard's Paradox", Cornell University Technical Report, 1987, [link](http://hdl.handle.net/1813/6660).

Further analysis is in

* [[Herman Geuvers]], Joep Verkoelen, *On Fixed point and Looping Combinators in Type Theory* (2009) &lbrack;[pdf](http://www.cs.ru.nl/~herman/PUBS/TLCApaper.pdf), [citeseer](http://citeseerx.ist.psu.edu/viewdoc/summary?doi=10.1.1.158.1478)&rbrack;


[[!redirects looping combinators]]
