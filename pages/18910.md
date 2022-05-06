# Explicit mathematics

* table of contents
{: toc}

## Idea

**Explicit mathematics** is a programme initiated by [[Solomon Feferman]] which is related to [[constructive mathematics]].

It is also a range of foundational logical systems based on the [[logic of partial terms]]. Starting from a first-order logic of partial terms axiomatizing [[combinatory algebra]], a second sort of _classes_ is added. Sometimes, the alternative names _classifications_ or _types_ are used.

The classes of explicit mathematics are not like the classes of [[set theory]], but also not like types of [[type theory]]. They are like the former in that they represent certain collections of the underlying first-order model, but they are like the latter in that they have _names_ that can be operated on to construct new ones.

The systems come in flavors with either intuitionistic or [[classical logic]]. On benefit is that they allow for smooth axiomatization of strong notions of [[universes]], see below.

The primary systems are called $T_0$ (the classical variant) and $T_0^i$ (the intuitionistic variant).

In the 1980s there was a proof assistant and program extraction tool called PX based on a version of $T_0$ relative to the Lisp programming language.

## The basic theory of operations and numbers

The first-order part of the systems treat an applicative universe in the sense of combinatory algebra. It includes constants $\mathrm{k}$ and $\mathrm{s}$ (combinators), $\mathrm{p}$, $\mathrm{p}_0$, and $\mathrm{p}_1$ (pairing and projection), $0$, $\mathrm{s}_N$, and $\mathrm{p}_N$ (zero, successor, and predecessor), and $\mathrm{d}_N$ (definition by cases on the natural numbers), and possibly further applicative constants.

There is one binary function symbol ${\cdot}$ for application (usual just indicated by juxtaposition), one unary relation symbol $\downarrow$ for being defined, one unary relation symbol $\mathrm{N}$ for natural numbers, as well the binary equality relation.

In the logic of partial terms, we use the usual abbreviation $s \simeq t \leftrightarrow ({s\downarrow} \wedge {t\downarrow} \to s=t)$. The basic axioms for the operations and natural numbers are:

1. $\mathrm{k} a b = a$,
1. $\mathrm{s} a b \downarrow \wedge \mathrm{s} a b c \simeq a c(b c)$,
1. $\mathrm{p}_0(a,b)=a \wedge \mathrm{p}_1(a,b) = b$,
1. $0\in N \wedge (\forall x\in N)(\mathrm{s}_N x \in N)$,
1. $(\forall x\in N)(\mathrm{s}_N x \ne 0 \wedge \mathrm{p}_N(\mathrm{s}_N x)=x)$,
1. $(\forall x\in N)(x\ne0 \to \mathrm{s}_N(\mathrm{p}_N x) = x)$,
1. $a\in N \wedge b\in N \wedge a=b \to \mathrm{d}_N u v a b = u$,
1. $a\in N \wedge b\in N \wedge a\ne b \to \mathrm{d}_N u v a b = v$.

From the first two axioms we get lambda-definability and a fixed-point combinator.

To these axioms we add the scheme of induction over the natural numbers to obtain the theory $BON + (\mathrm{L}{-}Ind_N)$. This is proof-theoretically equivalent to first-order Peano arithmetic, $PA$, via interpretations both ways. We can interpret $BON + (\mathrm{L}{-}Ind_N)$ in $PA$ by coding operations as indices for recursive functions using Kleene's $T$ and $U$ predicates.

## Elementary comprehension

When we go from the purely applicative theory to the theories of classes and names, we add a second sort (for classes) as well as several new constants, a binary relation symbol $\in$ (for membership) and a binary relation symbol for names $\Re$, where $\Re(s, U)$ means that $s$ is a name for the class $U$. We use the abbreviation $\Re(s) :\leftrightarrow \exists U \Re(s,U)$, indicating that $s$ is a name.

The basic axioms regarding classes and names state that every class has a name, that there are no homonyms, and that $\Re$ respects extensional equality.

The names of classes corresponding to elementary comprehension are generated from $nat$ (natural numbers) and $id$ (the equality relation) using $co$ (complements), $int$ (intersections), $dom$ (domains), and $inv$ (inverse images). [These are for the classical systems. The intuitionistic systems are slightly different. Todo: look this up]

Using the abbreviation $s\dot\in t :\leftrightarrow \exists U(\Re(t,U) \wedge s\in U)$, the axioms are:

1. $\Re(nat) \wedge \forall x(x \dot\in nat \leftrightarrow N(x))$,
1. $\Re(id) \wedge \forall x(x \dot\in id \leftrightarrow \exists y(x = (y,y)))$,
1. $\Re(a) \to \Re(co(a)) \wedge \forall x(x \dot\in co(a) \leftrightarrow \neg x\dot\in a)$,
1. $\Re(a) \wedge \Re(b) \to \Re(int(a,b)) \wedge \forall x(x \dot\in int(a,b) \leftrightarrow x \dot\in a \wedge x \dot\in b)$,
1. $\Re(a) \to \Re(dom(a)) \wedge \forall x(x \dot\in dom(a) \leftrightarrow \exists y((x,y) \dot\in a))$,
1. $\Re(a) \to \Re(inv(a,f)) \wedge \forall x(x \dot\in inv(a,f) \leftrightarrow f x \dot\in a)$.

Again we add some induction over the natural numbers to obtain theories $EC + (\mathrm{C}{-}Ind_N)$ (induction axiom for classes) and $EC + (\mathrm{L}{-}Ind_N)$ (induction schema for all formulas). These correspond proof-theoretically to the subsystems of second-order arithmetic $ACA_0$ and $ACA$, respectively.

## Join and inductive generation

The _join_ of classes gives disjoint unions of classes, and thus corresponds to the $\Sigma$-types of type theory. The inductive generation operation provides accesible parts of classes coding binary relations.

[todo: the axioms for join and inductive generation.]

The theory $T_0$ has elementary comprehension, join, inductive generation, and full induction over the natural numbers. It has the same proof-theoretic strength as [[CZF]] plus $REA$, the [[regular extension axiom]]. Further equivalences are listed at [[ordinal analysis]].

## Universes in explicit mathematics

[todo]

## References

* [Introduction (draft)](https://math.stanford.edu/~feferman/papers/DraftIntroFEM.pdf)

* Solomon Feferman, [How a Little Bit goes a Long Way: Predicative Foundations of Analysis](http://home.inf.unibe.ch/~ltg/em_bibliography/feferman13.pdf), notes prepared 1977-1981 with a new introduction from 2013.

* [Foundations of explicit mathematics](https://web.archive.org/web/20190108170710/http://www.ltg.unibe.ch/research/Foundations%20of%20Explicit%20Mathematics)

* [Bibliography of explicit mathematics](http://home.inf.unibe.ch/~ltg/em_bibliography/)

* Reinhard Kahle and Anton Setzer, [An extended predicative definition of the Mahlo universe](http://www.cs.swan.ac.uk/~csetzer/articles/kahleSetzerExtendedPredicativeMahloPohlersFestschrift.pdf), In: Ways of Proof Theory, pp. 315–340. Ontos Mathematical Logic, vol. 2, 2010.

* Susumu Hayashi and Hiroshi Nakano, [PX: a computational logic](https://dl.acm.org/citation.cfm?id=62010), MIT Press, 1988.
