
# Unintentional type theory
* table of contents
{: toc}

## Idea

In contrast to [[intensional type theory]], which is a [[type theory]] containing an [[identity type]] $x=y$ whose elements are identifications of $x$ and $y$, **unintentional type theory** has a [[identity type|mistaken identity type]] $x \overset{?}{\approx} y$ whose elements are inadvertent conflations of $x$ and $y$.  The mistaken identity type

> greatly increases the expressive power of UTT by internalizing many proofs which previously required metametatheoretic techniques (e.g. user error on a blackboard).  [(Angiuli, p1)](#Angiuli)

## Definition

The formation rule for the mistaken identity type says that any two [[terms]], there is a type of inadvertent conflations of them.

$$\frac{\Gamma\vdash M:A \qquad \Gamma\vdash N:B}{\Gamma \vdash (M:A \overset{?}{\approx} N:B) \,type}$$

Note that the terms being (potentially) conflated do not have to belong to the same type.

The introduction rule says that from any reason to conflate two terms we can obtain an inhabitant of the mistaken identity type.  It is important to note that the original reason for conflation of the terms is *not* remembered by the proof term.

$$\frac{\Gamma\vdash M:A \qquad \Gamma\vdash N:B \qquad \Gamma\vdash\text{FIXME: are these equal?}}{\Gamma\vdash confl(M,N) :(M:A \overset{?}{\approx} N:B)}$$

Finally, the elimination rule says that if we have a mistaken conflation of $M$ and $N$, we may replace $M$ by $N$ anywhere inside another term $P$ whose type depends on $M$.  The precise syntax of this rule is somewhat complicated; see [(Angiuli, p2)](#Angiuli) for details.


## Semantics

* In the [[homotopy type theory|homotopical interpretatation]] of unintentional type theory, every type has a tower of iterated mistaken identity types, representing the compounding nature of errors.  This is captured semantically by Angiuli's [[(∞,1)-topos|(∞,1)-accidentopos]] model, in which [[types]] are interpreted by [[globular sets]] that could be confused with an [[∞-groupoid]].

* One might expect that unintentional type theory also admits a model in the [[effective topos|ineffective topos]].  According to Awodey, the disassemblies are too immodest for this to work, but a related construction may be possible.

* [[philosophy|Philosophically]], the "unintended [[semantics]]" of unintentional type theory is described by the [[meaning explanation|meaningless explanation]].


## Computer implementations

Unintentional type theory has not yet been implemented in computer proof assistants.  However, Bauer has proposed that such implementation would be very useful pedagogically.  This is because UTT can formalize the way children are taught to solve algebraic equations in school, by starting out pretending that two things are equal.  Using a proof assistant with UTT could therefore help ensure that students are not doing anything right.


## References

* [[Carlo Angiuli]], *The $(\infty,1)$-accidentopos model of unintentional type theory*.  [Sigbovik '13](http://sigbovik.org/2013/); April 1, 2013. [PDF](https://carloangiuli.com/papers/unintentional.pdf)
 {#Angiuli}


category: joke

[[!redirects mistaken identity type]]
[[!redirects (∞,1)-accidentopos]]
