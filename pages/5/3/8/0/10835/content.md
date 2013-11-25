
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Algebra
+--{: .hide}
[[!include higher algebra - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Locality and descent
+--{: .hide}
[[!include descent and locality - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

Given a [[commutative ring]] $R$ and an $R$-[[associative algebra]] $A$, hence a [[ring]] [[homomorphism]] $R \longrightarrow A$, the _Amitsur complex_ is the [[Moore complex]] of the dual [[Cech nerve]] of $Spec(A) \to Spec(R)$, hence the [[chain complex]]

$$
  R \to A \to A \otimes_R A \to A \otimes_R A \otimes_R A \to \cdots
  \,.
$$

(See also at _[[Sweedler coring]]_ and at _[[commutative Hopf algebroid]]_ for the same or similar constructions.)

## Properties

### Descent theorem



+-- {: .num_theorem }
###### Theorem
**(descent theorem)**

If $A \to B$ is [[faithfully flat]] then its Amitsur complex is [[exact sequence|exact]].

=--

This is due to ([[Grothendieck]], [[FGA]]1)

The following reproduces the proof in low degree from [Milne, prop. 6.8](#Milne)

+-- {: .proof}
###### Proof 

We show that 

$$
  0 \to A \stackrel{f}{\longrightarrow} B \stackrel{1 \otimes id - id \otimes 1}{\longrightarrow} B \otimes_A B
$$ 

is an [[exact sequence]] if $f \colon A \longrightarrow B$ is [[faithfully flat]].

First observe that the statement follows if $A \to B$ admits a [[section]] $s \colon B \to A$. Because then we can define a map 

$$
  k \colon B \otimes_A B \longrightarrow B
$$

$$
  k \;\colon\; b_1 \otimes b_2 \mapsto b \cdot f(s(b)) - b
  \,.
$$

This is such that applied to a coboundary it yields

$$
  k(1 \otimes b - b \otimes 1) = f(s(b)) - b 
$$

and hence it exhibits every cocycle $b$ as a coboundary $b = f(s(b))$.

So the statement is true for the special morphism 

$$
  B \to B \otimes_A B
$$

$$
  b \mapsto b \otimes 1
$$

because that has a section given by the multiplication map. 

But now observe that the morphism $B \to B \otimes_A B$ is the [[tensor product]] of the morphism $f$ with $B$ over $A$. That $A \to B$ is [[faithfully flat]] by assumption, hence that it exhibits $B$ as a [[faithfully flat module]] over $A$ means by definition that the Amitsur complex for $(A \to B)\otimes_A B$ is exact precisely if that for $A \to B$ is exact.

=--


## References

The Amitsur complex was introduced in 

* [[Shimshon Amitsur]], _Simple algebras and cohomology groups of arbitrary fields_, Transactions of the American Mathematical Society
Vol. 90, No. 1 (Jan., 1959), pp. 73-112 ([JSTOR](http://www.jstor.org/stable/1993268))

His results were simplified in 

* Alex Rosenberg and Daniel Zelinsky, _On Amitsur's complex_,  Transactions of the American Mathematical Society Vol. 97, No. 2 (Nov., 1960), pp. 327-356

The statement of proof the descent theorem for the Amitsur complex is due to 

* [[Alexander Grothendieck]], [[FGA]]1


A review of the proof in low degree is in 

* [[James Milne]], prop. 6.8 of _[[Lectures on Étale Cohomology]]_
 {#Milne}

[[!redirects Amitsur complexes]]

[[!redirects descent theorem]]
[[!redirects descent theorems]]