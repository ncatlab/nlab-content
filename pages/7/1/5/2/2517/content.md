
<div class="rightHandSide toc">
[[!include synthetic differential geometry - contents]]
</div>


#Contents#

* automatic table of contents goes here
{:toc}

#Idea# 

The Kock-Lawvere axiom is the crucial axiom for the theory
of [[synthetic differential geometry]].

Imposed on a [[topos]] equipped with an [[internalization|internal]] [[algebra]] 
object $R$ over an internal [[ring]] object $k$, the Kock-Lawvere axiom says essentially that morphisms 
$D \to R$ from the
[[infinitesimal space|infinitesimal interval]] $D \subset R$ into $R$ are necessarily _linear_
maps, in that they always and uniquely extend to linear maps $R \to R$.

This linearity condition is what in [[synthetic differential geometry]]
allows to identify the [[tangent bundle]] 
$T X \to X$ of a space $X$ with its fiberwise linearity
by simply the [[internal hom]] object $X^D \to X$.

Put the other way round, the Kock-Lawvere axiom axiomatizes the 
familiar statement that "to first order every function is linear".

# Details #

## KL-axiom for the infinitesimal interval ##

The plain Kock-Lawevere axiom on a [[ring]] object $R$ in a [[topos]] $T$
is that for $D = \{x \in R| x^2 = 0\}$ the [[infinitesimal space|infinitesimal interval]]
the canonical map

$$
  R \times R \to R^D
$$

given by 

$$
  (x,d) \mapsto  (\epsilon \mapsto x + d \epsilon)
$$

is an [[isomorphism]].

## KL-axiom for spectra of internal Weil algebras ##

We  can consider the [[internalization|internal]] $R$-algebra object
$R \oplus \epsilon R := (R \times R, \cdot, +)$ in $T$, whose underlying object is
$R \times R$, with addition $(x,q)+(x',q'):=(x+x',q+q')$ and multiplication $(x, q ) \cdot (x', q') = (x x',x q ' + q x')$.

For $A$ an algebra object in $T$, write $Spec_R(A) := Hom_{R Alg(T)}(A,R) \subset R^A$
for the object of $R$-algebra homomorphisms from $A$ to $R$.

Then one checks that

$$
  D = Spec(R \oplus \epsilon R)
  \,.
$$

The element $q \in D \subset R$, $q^2 = 0$ corresponds to the algebra homomorphism
$(a,d) \mapsto a + q d$.

Using this, we can rephrase the standard Kock-Lawvere axiom by saying that the
canonical moprhism

$$
  R \oplus \epsilon R \to R^{Spec_R(R \oplus \epsilon R)}
$$

is an [[isomorphism]].

Notice that $(R \oplus \epsilon R)$ is a Weil algebra:

+--{.query}
Zoran: Who calls this Weil algebra ? Why ? Besides, $R$ is just a ring, not a field, hence word finite-dimensional is not appropriate (finite rank is OK). 

[[Urs Schreiber]]: this is what all the synthetic diff geometry literature says. Also  [[Models for Smooth Infinitesimal Analysis|Moerdijk-Reyes]].

I am not sure how general this terminology is. See also the new entry [[smooth topos]].

But you are right certainly about the ring/field thing. I have corrected that now above by saying that $R$ is an algebra over a ring object $k$.

=--


an $R$-algebra
that is finite dimensional and whose underlying [[ring]] is a local ring, i.e.
of the form $W = R \oplus m$, where $m$ is a maximal nilpotent ideal inite dimensional over $R$.

Then the general version of the Kock-Lawvere axiom for all Weil algebras says that

For all Weil algebra objects $W$ in $T$ the canonical morphism

$$
  W \to R^{Spec_R(W)}
$$

is an [[isomorphism]].
