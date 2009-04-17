In [[logic]], the __negation__ of a statement $p$ is a statement $\neg{p}$ which is true if and only if $p$ is false.

In [[classical logic]], we have the [[double negation]] law:
$$\neg\neg{p} \equiv p.$$
In [[intuitionistic logic]], we only have
$$\neg\neg{p} \dashv p,$$
while in [[paraconsistent logic]], we instead have
$$\neg\neg{p} \vdash p.$$
You can interpret intuitionistic negation as 'denial' and paraconsistent negation as 'doubt'.  So when one says that one doesn\'t deny $p$, that\'s weaker than actually asserting $p$; while when one says that one doesn\'t doubt $p$, that\'s stronger than merely asserting $p$.  Paraconsistent logic has even been applied to the theory of law: if $p$ is a judgment that normally requires only the preponderance of evidence, then $\neg\neg{p}$ is a judgment of $p$ beyond reasonable doubt.

[[linear logic|Linear logic]] features (at least) three different forms of negation, one for each of the above.  (The default meaning of the term 'negation' in linear logic, $p^\bot$, is the one that satisfies the classical double-negation law.)

Accordingly, negation mediates [[de Morgan duality]] in classical and linear logic but not in intuitionistic or paraconsistent logic.

In a [[topos]], the __negation__ of an object $A$ is the object $0^A$; this matches the intuitionistic notion of negation in that there is a [[natural transformation|natural morphism]] $A \to 0^{0^A}$ but not the other way around.