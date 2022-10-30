
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


## In type theory syntax

In usual [[type theory]] [[syntax]] negation is obtained as the [[function type]] into the [[empty type]]: $\not a = a \to \varnothing$.


## In categorical semantics

The [[categorical semantics]] of negation is the [[internal hom]] into the [[initial object]]: $\not = [-, \emptyset]$. 

In a [[topos]], the __negation__ of an object $A$ (a [[proposition]] under the [[propositions as types]]-interpretation) is the [[internal hom]] object $0^A$, where $0 = \emptyset$ denotes the [[initial object]]. 

This matches the [[intuitionistic mathematics|intuitionistic]] notion of negation in that there is a [[natural transformation|natural morphism]] $A \to 0^{0^A}$ but not the other way around.


## Related entries

* [[double negation]]

* [[complement]]

* [[De Morgan duality]]

* [[co-Heyting negation]]

* [[adjoint cylinder]]


[[!include logic symbols -- table]]


## References

* Y. Gauthier, _A Theory of Local Negation: The Model and some Applications_ , Arch. Math. Logik **25** (1985) pp.127-143. ([gdz](http://gdz.sub.uni-goettingen.de/dms/load/pdf/?PPN=GDZPPN002045923))

* H. Wansing, _Negation_ , pp.415-436 in Goble (ed.), _The Blackwell Guide to Philosophical Logic_ , Blackwell Oxford 2001.


[[!redirects negation]]
[[!redirects negations]]

[[!redirects not]]
[[!redirects NOT]]

[[!redirects linear negation]]
