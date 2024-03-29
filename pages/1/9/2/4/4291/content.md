+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition
 {#Definition}

### In an abelian category
 {#InAbelianCategory}

Let $\mathcal{A}$ be an [[abelian category]].

+-- {: .num_defn #SplitnessInAbelianCategory}
###### Definition

A [[short exact sequence]] $0\to A \stackrel{i}{\to} B \stackrel{p}{\to} C\to 0$ in $\mathcal{A}$  is called **split** if either of the following equivalent conditions hold

1. There exists a [[section]] of $p$, hence a morphism $s \colon C\to B$ such that $p \circ s = id_C$.

1. There exists a [[retract]] of $i$, hence a morphism $r \colon B\to A$ such that $r \circ i = id_A$.

1. There exists an [[isomorphism]] of sequences with the sequence 

   $$
     0\to A\to A\oplus C\to C\to 0
   $$

   given by the [[direct sum]] and its canonical injection/projection morphisms.

=--

+-- {: .num_lemma #SplittingLemma}
###### Lemma
**(splitting lemma)**

The three conditions in def. \ref{SplitnessInAbelianCategory} are indeed [[equivalence|equivalent]].

=--

(e.g. [Hatcher (2002)](#Hatcher02), p. 147)

+-- {: .proof}
###### Proof

It is clear that the third condition implies the first two: take the section/retract to be given by the canonical injection/projection maps that come with a [[direct sum]].

Conversely, suppose we have a retract $r \colon B \to A$ of $i \colon A \to B$. Write $P \colon B \stackrel{r}{\to} A \stackrel{i}{\to} B$ for the corresponding [[idempotent]]. 

Then every element $b \in B$ can be decomposed as $b = (b - P(b)) + P(b)$ hence with $b - P(b) \in ker(r)$ and $P(b) \in im(i)$. Moreover this decomposition is unique since if $b = i(a)$ while at the same time $r(b) = 0$ then $0 = r(i(a)) = a$. This shows that $B \simeq im(i) \oplus ker(r)$ is a [[direct sum]] and that $i \colon A \to B$ is the canonical inclusion of $im(i)$. By exactness it then follows that $ker(r) \simeq im(p)$ and hence that $B \simeq A \oplus C$ with the canonical inclusion and projection.

The implication that the second condition also implies the third is formally dual to this argument. 

=--


### In a semi-abelian category

There is a nonabelian analog of split exact sequences in [[semiabelian categories]]. See there.

## Properties

### Relation to chain homotopy
 {#RelationToChainHomotopy}

+-- {: .num_prop}
###### Proposition

A [[long exact sequence]] $C_\bullet$ is _split exact_ precisely if the [[weak homotopy equivalence]] from the 0-chain complex, namely the [[quasi-isomorphism]] $0 \to C_\bullet$ is actually a [[chain homotopy]] [[homotopy equivalence|equivalence]], in that the [[identity]] on $C_\bullet$ has a [[null homotopy]]. 

=--


### Of free modules and vector spaces
 {#OfVectorSpaces}

Assuming the [[axiom of choice]]:

+-- {: .num_prop}
###### Proposition

Every [[exact sequence]] of [[free abelian groups]] is split.

=--

+-- {: .num_prop}
###### Proposition

Every exact sequence of [[free modules]] which is [[bounded-below chain complex|bounded below]] is split.

=--

Let $k$ be a [[field]] and denote by $\mathcal{A} \coloneqq k$[[Vect]] the [[category]] of [[vector spaces]] over $k$.

+-- {: .num_cor #SESOfVectorSpacesSplits}
###### Corollary

Every [[short exact sequence]] of vector spaces is split.

=--

(Essentially by the [[basis theorem]], for exposition see for instance [here](https://unapologetic.wordpress.com/2008/06/26/exact-sequences-split).)



### Involving injective/projective objects
 {#InvolvingInjectiveObjects}


+-- {: .num_lemma }
###### Lemma

If in a [[short exact sequence]] $0 \to A \to B \to C \to 0$ 
in an [[abelian category]] the first object $A$ is an [[injective object]] or the last object is a [[projective object]] then the sequence  is split  exact.

=--

+-- {: .proof}
###### Proof

Consider the first case. The other is formally dual.

By the properties of a [[short exact sequence]] the morphism $A \to B$ here is a [[monomorphism]].
By definition of [[injective object]], if $A$ is injective then it has the [[right lifting property]] against [[monomorphisms]] and so there is a morphism $q : B \to A$ that makes the following [[diagram]] [[commuting diagram|commute]]:

$$
  \array{
     A &\stackrel{id_A}{\to}& A
     \\
     \downarrow & \nearrow_{q}
     \\
     B
  }
  \,.
$$

Hence $q$ is a [[retract]] as in def. \ref{SplitnessInAbelianCategory}.


=--



## References

For instance 

* [[Charles Weibel]], Section 1.4 of: _[[An Introduction to Homological Algebra]]_ (1994)

* {#Hatcher02} [[Allen Hatcher]], pp. 147 of: *Algebraic Topology*, Cambridge University Press (2002) &lbrack;[ISBN:9780521795401](https://www.cambridge.org/gb/academic/subjects/mathematics/geometry-and-topology/algebraic-topology-1?format=PB&isbn=9780521795401), [webpage](https://pi.math.cornell.edu/~hatcher/AT/ATpage.html)&rbrack;



[[!redirects split sequence]]

[[!redirects split exact sequences]]
[[!redirects split sequences]]

[[!redirects split short exact sequence]]
[[!redirects split short exact sequences]]

[[!redirects splitting lemma]]

