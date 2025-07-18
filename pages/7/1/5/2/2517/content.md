
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Synthetic differential geometry
+--{: .hide}
[[!include synthetic differential geometry - contents]]
=--
#### Topos Theory
+--{: .hide}
[[!include topos theory - contents]]
=--
=--
=--


#Kock--Lawvere axiom#
* table of contents
{:toc}


## Idea

The Kock--Lawvere axiom is the crucial axiom for the theory
of [[synthetic differential geometry]].

Imposed on a [[topos]] equipped with an [[internalization|internal]] [[algebra]] 
object $R$ over an internal [[ring]] object $k$, the Kock--Lawvere axiom says essentially that morphisms 
$D \to R$ from the
[[infinitesimal space|infinitesimal interval]] $D \subset R$ into $R$ are necessarily _linear_
maps, in that they always and uniquely extend to linear maps $R \to R$.

This linearity condition is what in [[synthetic differential geometry]]
allows to identify the [[tangent bundle]] 
$T X \to X$ of a space $X$ with its fiberwise linearity
by simply the [[internal hom]] object $X^D \to X$.

Put the other way round, the Kock--Lawvere axiom axiomatizes the 
familiar statement that "to first order every [[smooth map]] is linear".


## Details

### KL axiom for the infinitesimal interval

The plain Kock--Lawevere axiom on a [[ring]] object $R$ in a [[topos]] $T$
is that for $D = \{x \in R| x^2 = 0\}$ the [[infinitesimal space|infinitesimal interval]]
the canonical map

$$
  R \times R \to R^D
$$

given by 

$$
  (x,d) \mapsto  (\epsilon \mapsto x + \epsilon d)
$$

is an [[isomorphism]] of objects in $T$.


### KL axiom for spectra of internal Weil algebras
 {#ForWeilAlgebras}

We  can consider the [[internalization|internal]] $R$-algebra object
$R \oplus \epsilon R \coloneqq (R \times R, \cdot, +)$ in $T$, whose underlying object is
$R \times R$, with addition $(x,q)+(x',q') \coloneqq (x+x',q+q')$ and multiplication $(x, q ) \cdot (x', q') = (x x',x q ' + q x')$.

For $A$ an algebra object in $T$, write $Spec_R(A) \coloneqq Hom_{R Alg(T)}(A,R) \subset R^A$
for the object of $R$-algebra homomorphisms from $A$ to $R$.

Then one checks that

$$
  D = Spec(R \oplus \epsilon R)
  \,.
$$

The element $q \in D \subset R$, $q^2 = 0$ corresponds to the algebra homomorphism
$(a,d) \mapsto a + q d$.

Using this, we can rephrase the standard Kock--Lawvere axiom by saying that the
canonical morphism

$$
  R \oplus \epsilon R \to R^{Spec_R(R \oplus \epsilon R)}
$$

is an [[isomorphism]].

Notice that $(R \oplus \epsilon R)$ is a
[[infinitesimally thickened point|Weil algebra]]/[[Artin algebra]]:
an $R$-algebra
that is finite dimensional and whose underlying [[ring]] is a local ring, i.e.
of the form $W = R \oplus m$, where $m$ is a maximal nilpotent ideal finite dimensional over $R$.

Then the general version of the Kock--Lawvere axiom for all Weil algebras says that

For all Weil algebra objects $W$ in $T$ the canonical morphism

$$
  W \to R^{Spec_R(W)}
$$

is an [[isomorphism]] of objects in $T$. Note that because the canonical morphism is also a homomorphism of $R$-algebras, and inverses of algebra homomorphisms are algebra homomorphisms, this gives an isomorphism of internal $R$-algebras.

## Related concepts

* [[synthetic quasi-coherence]]

## References

The Kock-Lawvere axiom was introduced in

* {#Kock77} [[Anders Kock]], _A simple axiomatics for differentiation_,  Mathematica Scandinavica Vol. 40, No. 2 (October 24, 1977), pp. 183-193 ([JSTOR](http://www.jstor.org/stable/24491223))

Textbook accounts are in

* [[Anders Kock]], section I.12 of _Synthetic differential geometry_, Cambridge University Press, London Math. Society Lecture Notes Series No. 333 (1981, 2006) ([pdf](http://home.imf.au.dk/kock/sdg99.pdf))

* [[Anders Kock]], section 1.3 of _Synthetic geometry of manifolds_, Cambridge Tracts in Mathematics, 180 (2010) ([pdf](http://home.imf.au.dk/kock/SGM-final.pdf))

[[!redirects Kock-Lawvere axioms]]


[[!redirects Kock--Lawvere axiom]]
[[!redirects Kock–Lawvere axiom]]
[[!redirects Kock Lawvere axiom]]
