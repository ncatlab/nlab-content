# Explicit mathematics

* table of contents
{: toc}

## Idea

**Explicit mathematics** is a programme initiated by [[Solomon Feferman]] which is related to [[constructive mathematics]].

It is also a range of foundational logical systems based on the [[logic of partial terms]]. Starting from a first-order logic of partial terms axiomatizing [[combinatory algebra]], a second sort of _classes_ is added. Sometimes, the alternative names _classifications_ or _types_ are used.

The classes of explicit mathematics are not like the classes of [[set theory]], but also not like types of [[type theory]]. They are like the former in that they represent certain collections of the underlying first-order model, but they are like the latter in that they have _names_ that can be operated on to construct new ones.

The systems come in flavors with either intuitionistic or [[classical logic]]. On benefit is that they allow for smooth axiomatization of strong notions of [[universes]], see below.

The primary systems are called $T_0$ (the classical variant) and $T_0^i$ (the intuitionistic variant).
 
## The basic theory of operations and numbers

The first-order part of the systems treat an applicative universe in the sense of combinatory algebra. It includes constants $k$ and $s$ (combinators), $p$, $p_0$, and $p_1$ (pairing and projection), $0$, $s_N$, and $p_N$ (zero, successor, and predecessor), and $d_N$ (definition by cases on the natural numbers), and possibly further applicative constants.

There is one binary function symbol $\cdot$ for application, and one unary relation symbol $\downarrow$ (defined), as well as equality.

[todo: write the axioms for the applicative constants]

## Elementary comprehension

When we go from the purely applicative theory to the theories of classes and names, we add a second sort (for classes) as well as several new constants, a binary relation symbol $\in$ (for membership) and a binary relation symbol for names $\mathfrak R$, where $\mathfrak R(s, U)$ means that $s$ is a name for the class $U$.

[todo: write the axioms of elementary comprehension]

## Join and inductive generation

The _join_ of classes correspond to the $\Sigma$-types of type theory, …

[todo: the axioms for join and inductive generation.]

## Universes in explicit mathematics

[todo]

## References

* [Introduction (draft)](https://math.stanford.edu/~feferman/papers/DraftIntroFEM.pdf)

* Solomon Feferman, [How a Little Bit goes a Long Way: Predicative Foundations of Analysis](http://home.inf.unibe.ch/~ltg/em_bibliography/feferman13.pdf), notes prepared 1977-1981 with a new introduction from 2013.

* [Foundations of explicit mathematics](http://www.ltg.unibe.ch/research/Foundations%20of%20Explicit%20Mathematics)

* [Bibliography of explicit mathematics](http://home.inf.unibe.ch/~ltg/em_bibliography/)

* Reinhard Kahle and Anton Setzer, [An extended predicative definition of the Mahlo universe](http://www.cs.swan.ac.uk/~csetzer/articles/kahleSetzerExtendedPredicativeMahloPohlersFestschrift.pdf), In: Ways of Proof Theory, pp. 315–340. Ontos Mathematical Logic, vol. 2, 2010.
