
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

Let $\mathcal{A}$ be an [[abelian category]] and write $Ch_\bullet(\mathcal{A})$ for its [[category of chain complexes]]. Under forming [[chain homology]]

$$
  H_0 : Ch_\bullet(\mathcal{A}) \to \mathcal{A}
$$

in some (any) fixed degree, a [[homotopy fiber sequence]] in $Ch_\bullet(\mathcal{A})$ is sent to a [[long exact sequence]] in $\mathcal{A}$. This is the _homology long exact sequence_. 

Often this is considered specifically for the case that the fiber sequence in $Ch_\bullet(\mathcal{A})$ is that induced from a [[short exact sequence]] in $\mathcal{A}$. In this case the further map (that which makes the sequence "long") is called the [[connecting homomorphism]].

## Statement

(...)

For the moment see still at _[[fiber sequence]]_, for instance the section
_[long exact sequence in cohomology](fiber%20sequence#LongSequCoh)_ there.

## Properties

### Relation to homotopy fiber sequences
 {#RelationToHomotopyFiberSequences}

We discuss the relation of homology long exact sequences to [[homotopy cofiber sequences]] of chain complexes. Technical details corresponding to the following survey are at _[[mapping cone]]_ in the section _[Mapping cone -- Homology exact sequences and fiber sequences](http://ncatlab.org/nlab/show/mapping+cone#HomologyExactSequencesAndFiberSequences)_.

$\,$

While the notion of a [[short exact sequence]] of [[chain complexes]] is very useful for computations, it does not have invariant meaning if one considers chain complexes as objects in (abelian) [[homotopy theory]], where one takes into account [[chain homotopies]] between [[chain maps]] and takes [[equivalence]] of chain complexes not to be given by [[isomorphism]], but by [[quasi-isomorphism]].

For if a [[chain map]] $A_\bullet \to B_\bullet$ is the degreewise [[kernel]] of a chain map $B_\bullet \to C_\bullet$, then if $\hat A_\bullet \stackrel{\simeq}{\to} A_\bullet$ is a [[quasi-isomorphism]] (for instance a [[projective resolution]] of $A_\bullet$) then of course the composite chain map $\hat A_\bullet \to B_\bullet$ is in general far from being the degreewise kernel of $C_\bullet$. Hence the notion of degreewise kernels of chain maps and hence that of short exact sequences is not meaningful in the homotopy theory of chain complexes in $\mathcal{A}$ (for instance: not in the [[derived category]] of $\mathcal{A}$).

That short exact sequences of chain complexes nevertheless play an important role in [[homological algebra]] is due to what might be called a "technical coincidence":

+-- {: .num_prop }
###### Proposition

If $A_\bullet \to B_\bullet \to C_\bullet$ is a 
[[short exact sequence]] of [[chain complexes]], then the [[commuting square]]

$$
  \array{
     A_\bullet &\to& 0
     \\
     \downarrow && \downarrow
     \\
     B_\bullet &\to& C_\bullet
  }
$$

is not only a [[pullback]] square in $Ch_\bullet(\mathcal{A})$, exhibiting $A_\bullet$ as the [[fiber]] of $B_\bullet \to C_\bullet$ over $0 \in C_\bullet$, it is in fact also a _[[homotopy pullback]]_.

=--

This means it is [[universal property|universal]] not just among commuting such squares, but also among such squares which commute possibly only up to a [[chain homotopy]] $\phi$:

$$
  \array{
     Q_\bullet &\to& 0
     \\
     \downarrow &\swArrow_{\phi}& \downarrow
     \\
     B_\bullet &\to& C_\bullet
  }
$$

and with morphisms between such squares being maps $A_\bullet \to A'_\bullet$ correspondingly with further chain homotopies filling all diagrams in sight.

+-- {: .proof}
###### Proof

This follows from using the basic property (see at [exact sequence -- Definition](exact+sequence#Definition)) that in a short exact sequence $A_\bullet \to B_\bullet \to C_\bullet$ the morphism on the right is a degreewise [[surjection]]
together with a basic result in the theory of [[model categories]] or in fact that of [[categories of fibrant objects]] which is discussed in detail at _[[homotopy pullback]]_ and also at _[[factorization lemma]]_:

by the existence of the [[projective model structure on chain complexes]], we may regard every chain complex as a [[fibrant object]] and every degreewise surjection as a [[fibration]]. By the basic theorem discussed at [Homotopy pullback -- Properties -- General](homotopy%20pullback#ConstructionsGeneral) these are sufficient conditions for the ordinary pullback as above to produce a chain complex that represents the homotopy-correct [[homotopy pullback]] (which, beware, is defined up "weak chain homology equivalence" only, hence up to [[zig-zags]] of [[quasi-isomorphism]]).

=--

Equivalently, we have the formally dual result, proved using instead the existence of the [[injective model structure on chain complexes]]:

+-- {: .num_prop }
###### Proposition

If $A_\bullet \to B_\bullet \to C_\bullet$ is a 
[[short exact sequence]] of [[chain complexes]], then the [[commuting square]]

$$
  \array{
     A_\bullet &\to& 0
     \\
     \downarrow && \downarrow
     \\
     B_\bullet &\to& C_\bullet
  }
$$

is not only a [[pushout]] square in $Ch_\bullet(\mathcal{A})$, exhibiting $C_\bullet$ as the [[cofiber]] of $A_\bullet \to B_\bullet$ over $0 \in C_\bullet$, it is in fact also a _[[homotopy pushout]]_.

=--

But a central difference between [[fibers]]/[[cofibers]] on the one hand and [[homotopy fibers]]/[[homotopy cofibers]] on the other is that while the (co)fiber of a (co)fiber is necessarily trivial, the homotopy (co)fiber of a homotopy (co)fiber is in general far from trivial: it is instead the [[looping]] $\Omega(-)$  or [[suspension]] $\Sigma(-)$ of the codomain/domain of the original morphism: by the [[pasting law]] for homotopy pullbacks the [[pasting]] composite of successive [[homotopy cofibers]] of a given morphism $f : A_\bullet \to B_\bullet$ looks like this:

$$
  \array{
     A_\bullet &\stackrel{f}{\to}& B_\bullet &\to& 0
     \\
     \downarrow &\swArrow_{\mathrlap{\phi}}& \downarrow &\swArrow& \downarrow
     \\
     0 &\to& cone(f) &\to& A[1]_{\bullet} &\stackrel{}{\to}& 0
     \\
     && \downarrow &\swArrow& \downarrow^{\mathrlap{f[1]}}  &\swArrow& \downarrow
     \\
     && 0 &\to& B[1] &\to& cone(f)[1]_\bullet &\to& \cdots
     \\
     && && \downarrow && \downarrow &\ddots&
     \\
     && && \vdots && && 
  }
$$ 

here

* $cone(f)$ is a specific representative of the [[homotopy cofiber]] of $f$ called the _[[mapping cone]]_ of $f$, whose construction comes with an explicit [[chain homotopy]] $\phi$ as indicated, hence $cone(f)$ is homology-equivalence to $C_\bullet$ above, but is in general a "bigger" model of the homotopy cofiber;

* $A[1]$ etc. is the [[suspension of a chain complex]] of $A$, hence the same chain complex but pushed up in degree by one.

This is discussed in detail at _[[mapping cone]]_, see the section _[mapping cone - for chain complexes](mapping%20cone#InChainComplexes)_.

In conclusion we get from every morphim of chain complexes a 
long **[[homotopy cofiber sequence]]**

$$
    \cdots 
  \to 
     A_\bullet \stackrel{f}{\to}B_\bullet
  \stackrel{}{\to} 
  cone(f)
   \stackrel{}{\to}
  A[1]_\bullet
   \stackrel{f[1]}{\to}
  B[1]_\bullet
   \stackrel{}{\to}   
  cone(f)[1]_\bullet
   \to 
  \cdots
  \,.
$$

And applying the [[chain homology]] functor to this yields the long exact sequence in chain homology which is traditionally said to be associated to the short exact sequence $A_\bullet \to B_\bullet \to C_\bullet$.

In conclusion this means that it is not really the passage to homology groups which "makes a short exact sequence become long". It's rather that passing to homology groups is a shadow of passing to chain complexes regarded up to quasi-isomorphism, and _this_ is what makes every short exact sequence be realized as but a special presentation of a stage in a long [[homotopy fiber sequence]].

## Related concepts

* [[Gysin sequence]]

* [[Serre long exact sequence]]

* [[long exact sequence of homotopy groups]]

* [[long exact sequence in homology]]

  * [[long exact sequence in generalized homology]]

## References

Lecture notes:

* Robert Ash, _The long exact homology sequence and applications_ ([pdf](http://www.math.uiuc.edu/~r-ash/Algebra/Supplement.pdf))

[[!redirects long exact sequences in chain homology]]

[[!redirects long exact sequence in chain cohomology]]
[[!redirects long exact sequences in chain cohomology]]

