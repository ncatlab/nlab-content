
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

In (classical) [[logic]], the __negation__ of a statement $p$ is a statement $\neg{p}$ which is true if and only if $p$ is false. Hence, viewed algebraically, the negation corresponds to the complement operator of the corresponding [[Boolean algebra]] which satisfies $a\wedge\neg a=\bot$ as well as $a\vee \neg a=\top$.

More generally, as different logics correspond to different types of lattices, one calls *negation* antitone, or polarity reversing, lattice operators that mimic or approximate the algebraic and proof-theoretic behavior of $\neg$.

## As a logic gate
 {#AsALogicGate}

As a [[logic gate]] on [[bits]] and as a [[quantum logic gate]] on [[qbits]] ($X$-[[Pauli matrix]]):


\begin{imagefromfile}
    "file_name": "NOT_LogicGate-221025.jpg",
    "width": "600",
    "unit": "px",
    "margin": {
        "top": -20,
        "bottom": 20,
        "right": 0, 
        "left": 10
    }
\end{imagefromfile}


## Negation in different logics

In [[classical logic]], we have the [[double negation]] law:
$$
  \neg\neg{p} 
    \;\equiv\;
  p
  \,.
$$

In [[intuitionistic logic]], we only have

$$
  \neg\neg{p} 
    \;\dashv\; p
  \,,
$$

while in [[paraconsistent logic]], we instead have

$$
  \neg\neg{p} 
    \;\vdash\; 
  p
  \,.
$$

One may interpret intuitionistic negation as 'denial' and paraconsistent negation as 'doubt'.  So when one says that one doesn\'t deny $p$, that\'s weaker than actually asserting $p$; while when one says that one doesn\'t doubt $p$, that\'s stronger than merely asserting $p$.  Paraconsistent logic has even been applied to the theory of law: if $p$ is a judgment that normally requires only the preponderance of evidence, then $\neg\neg{p}$ is a judgment of $p$ beyond reasonable doubt.

[[linear logic|Linear logic]] features (at least) three different forms of negation, one for each of the above.  (The default meaning of the term 'negation' in linear logic, $p^\bot$, is the one that satisfies the classical double-negation law.)

Accordingly, negation mediates [[de Morgan duality]] in classical and [[linear logic]] but not in intuitionistic or paraconsistent logic.

### Antithesis interpretation

In the [[antithesis interpretation]] of [[intuitionistic logic]], one considers, instead of single propositions, pairs of [[mutually exclusive propositions]], i.e. propositions $p$ and $q$ such that $\neg (p \wedge q)$. These are generalisations of the intuitionistic denial negation since we have by [[currying]] the statements $p \to \neg q$ and $q \to \neg p$. The intuitionistic negation is simply a special case of the above since we have the true statements $p \to \neg \neg p$ and $\neg p \to \neg p$ from the [[law of non-contradiction]] $\neg (p \wedge \neg p)$. 

There is an [[affine logic|affine]] [[linear logic]] associated with mutually exclusive propositions where the affine negation of mutually exclusive propositions $p$ and $q$ is just $q$ and $p$ respectively. Thus, we can say that $q$ is the **negation** of $p$ and vice versa, for mutually exclusive propositions $p$ and $q$. This is very important for [[constructive mathematics]], where the terms "[[equal]]/[[not equal]]" and related concepts such as "[[rational number]]/[[irrational number]]" and "[[algebraic number]]/[[transcendental number]]" are usually defined using [[equality]]/[[tight apartness relation]] for objects such as the [[real numbers]] and the [[p-adic numbers]]. These terms only makes sense in this context if one is using the affine negation of the mutually exclusive propositions rather than intuitionistic denial negation, the latter which in general is not an [[involution]] on propositions. 

## In type theory syntax

In usual [[type theory]] [[syntax]] negation is obtained as the [[function type]] into the [[empty type]]: $\not a = a \to \varnothing$. 

Equivalently, in [[type theory]] with [[equivalence types]] but without [[function types]], negation is the [[equivalence type]] with the [[empty type]]: $\not a = a \simeq \varnothing$. 

## In categorical semantics

The [[categorical semantics]] of negation is the [[internal hom]] into the [[initial object]]: $\not = [-, \emptyset]$. 

In a [[topos]], the __negation__ of an object $A$ (a [[proposition]] under the [[propositions as types]]-interpretation) is the [[internal hom]] object $0^A$, where $0 = \emptyset$ denotes the [[initial object]]. 

This matches the [[intuitionistic mathematics|intuitionistic]] notion of negation in that there is a [[natural transformation|natural morphism]] $A \to 0^{0^A}$ but not the other way around.

## Negation as implying triviality of rings

There are some mathematicians working in [[ring theory]] and [[algebra]], such as [Lombardi & Quitté 2010](#LombardiQuitté2010), who define negation for a [[proposition]] $P$ about a ring $R$ as $P$ implies that the ring $R$ is trivial $0 =_R 1$. The proposition $P \to (0 =_R 1)$ is the same as the usual negation $\neg P$ for a non-trivial commutative ring, but is always true for the [[trivial ring]]. Hence, this leads to the concepts of a [[possibly trivial integral domain]] and a [[possibly trivial field]], which the authors Lombardi & Quitté call simply an "integral domain" and a "field" respectively. 

One can also extend this notion of negation from rings to other [[bi-pointed sets]] such as [[rigs]], [[lattices]], [[frames]], [[pointed abelian groups]], [[absorption monoids]], [[bounded total orders]], [[closed midpoint algebras]], [[scales]], and [[interval coalgebras]]. 

## Related entries

* [[double negation]]

* [[complement]]

* [[De Morgan duality]]

* [[co-Heyting negation]]

* [[adjoint cylinder]]

* [[strong negation]]


[[!include logic symbols -- table]]


## References

* Y. Gauthier, _A Theory of Local Negation: The Model and some Applications_ , Arch. Math. Logik **25** (1985) pp.127-143. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002045923))

* H. Wansing, _Negation_ , pp.415-436 in Goble (ed.), _The Blackwell Guide to Philosophical Logic_ , Blackwell Oxford 2001.

* {#LombardiQuitté2010} [[Henri Lombardi]], [[Claude Quitté]] (2010): *Commutative algebra: Constructive methods (Finite projective modules)* Translated by Tania K. Roblo, Springer (2015) ([doi:10.1007/978-94-017-9944-7](https://link.springer.com/book/10.1007/978-94-017-9944-7), [pdf](http://hlombardi.free.fr/CACM.pdf))

* {#Shulman2022} [[Michael Shulman]], *Affine logic for constructive mathematics*. Bulletin of Symbolic Logic, Volume 28, Issue 3, September 2022. pp. 327 - 386 ([doi:10.1017/bsl.2022.28](https://doi.org/10.1017/bsl.2022.28), [arXiv:1805.07518](https://arxiv.org/abs/1805.07518))


[[!redirects negation]]
[[!redirects negations]]

[[!redirects logical negation]]
[[!redirects logical negations]]

[[!redirects denial negation]]
[[!redirects denial negations]]

[[!redirects intuitionistic negation]]
[[!redirects intuitionistic negations]]

[[!redirects not]]
[[!redirects NOT]]

[[!redirects linear negation]]
[[!redirects linear negations]]

[[!redirects affine negation]]
[[!redirects affine negations]]

[[!redirects constructive negation]]
[[!redirects constructive negations]]
