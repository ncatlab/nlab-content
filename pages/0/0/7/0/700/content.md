+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
### Context
#### Category theory
+-- {: .hide}
[[!include category theory - contents]]
=--
#### Idempotents
+-- {: .hide}
[[!include idempotents - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}

## Definition

An [[object]] $A$ in a [[category]] is called a **retract** of an object $B$ if there are [[morphisms]] $i\colon A\to B$ and $r \colon B\to A$ such that $r \circ i = id_A$. In this case $r$ is called a **retraction** of $B$ onto $A$.

$$
  id 
    \;\colon\; 
  A \underoverset{section}{i}{\to} B \underoverset{retraction}{r}{\to} A
  \,.
$$

Here $i$ may also be called a _[[section]]_ of $r$. (In particular if $r$ is thought of as exhibiting a [[bundle]]; the terminology originates from [[topology]].)
 
Hence a **retraction** of a [[morphism]] $i  \;\colon\;  A \to B$ is a _left-[[inverse]]_.

In this situation, $r$ is a [[split epimorphism]] and $i$ is a [[split monomorphism]]. The entire situation is said to be a _splitting of  the [[idempotent]]_

$$
  B \stackrel{r}{\longrightarrow} A \stackrel{i}{\longrightarrow} B
  \,.
$$

Accordingly, a **[[split monomorphism]]** is a morphism that *has* a retraction; a **[[split epimorphism]]** is a morphism that *is* a retraction.



## Properties

+-- {: .num_lemma #LeftInverseWithLeftInverseIsLeftInverse}
###### Lemma
**([[left inverse]] with [[left inverse]] is [[inverse]])**

Let $\mathcal{C}$ be a [[category]], and let $f$ and $g$ be [[morphisms]] in $\mathcal{C}$, such that $g$ is a [[left inverse]] to $f$:

$$
  g \circ f = id
  \,.
$$

If $g$ itself has a left inverse $h$

$$
  h \circ g = id
$$

then $h = f$ and $g = f^{-1}$ is an actual (two-sided) [[inverse morphism]] to $f$.

=--


+-- {: .proof}
###### Proof

Since [[inverse morphisms]] are unique if they exists, it is sufficient to show that

$$
  f \circ g = id
  \,.
$$

Compute as follows:

$$
  \begin{aligned}
    f \circ g
    & =  \underset{ = id}{\underbrace{h \circ g}} \circ f \circ g
    \\
    & =
    h \circ \underset{= id}{\underbrace{g \circ f}} \circ g
    \\
    & = h \circ g
    \\
    & = id
  \end{aligned}
$$


=--


+-- {: .num_remark #RetractsPreservedByFunctor}
###### Remark

Retracts are clearly preserved by any [[functor]]. 

=--


+-- {: .num_remark #SplitEpisAndMonos}
###### Remark

A [[split epimorphism]] $r; B \to A$ is the strongest of various notions of [[epimorphism]] (e.g., it is a [[regular epimorphism]], in fact an [[abolute limit|absolute]] [[coequalizer]], being the coequalizer of a pair $(e, 1_B)$ where $e = i \circ r: B \to B$ is idempotent). Dually, a [[split monomorphism]] is the strongest of various notions of monomorphism. 

=--

+-- {: .num_prop #RetractOfObjectWithLLP}
###### Proposition

If an object $B$ has the [[left lifting property]] against a morphism $X \to Y$, then so does every of its retracts $A \to B$:

$$
  \left(
  \array{
     && X
     \\
     & {}^{\mathllap{\exists}}\nearrow& \downarrow
     \\
     A &\to& Y
  }
  \right)
  \;\;\;\;
  :=
  \;\;\;\;
  \left(    
  \array{
     && && &&  X
     \\
     &&& {}^{\mathllap{\exists}}\nearrow& && \downarrow
     \\
     A &\to& B &\to& A &\to& Y
  }
  \right)
$$

=--


+-- {: .num_prop #RetractOfRepresentable}
###### Proposition

Let $C$ be a [[category]] with [[split idempotent]]s and write $PSh(C) = [C^{op}, Set]$ for its [[presheaf category]]. Then a retract of a [[representable functor]] $F = PSh(C)$ is itself representable.

=--

This appears as ([Borceux, lemma 6.5.6](#Borceux))



## Examples

### To the point

* In a category with [[terminal object]] $*$ every morphism of the form $* \to X$ is a section, and the unique morphism $X \to *$ is the corresponding retraction.

### Of simplices

The inclusion of standard topological [[horn]]s into the topological [[simplex]] $\Lambda^n_k \hookrightarrow \Delta^n$ is a retract in [[Top]]. 

### In arrow categories

Let $\Delta[1] = \{0 \to 1\}$ be the [[interval category]]. For every category $C$ the [[functor category]] $[\Delta[1], C]$ is the [[arrow category]] of $C$.

In the theory of [[weak factorization systems]] and [[model categories]], an important role is played by retracts in $C^{\Delta[1]}$, the [[arrow category]] of $C$.  Explicitly spelled out in terms of the original category $C$, a morphism $f:X\to Y$ is a retract of a morphism $g:Z\to W$ if we have commutative squares

$$
  \array{
     id_X \colon & X & \to & Z & \to & X
     \\
     & f \downarrow  & & g \downarrow & & \downarrow f
     \\
     id_Y \colon & Y & \to & W & \to & Y
  }
$$

such that the top and bottom rows compose to identities.



+-- {: .num_prop #RetractsOfMorphismWithLiftingProperty}
###### Proposition

Classes of morphisms in a category $C$ that are given by a left or right [[lifting property]] are preserved under retracts in the [[arrow category]] $[\Delta[1],C]$. In particular the defining classes of a [[model category]] are closed under retracts.

=--

This is fairly immediate, a proof is made explicit [here](ClosurePropertiesOfInjectiveAndProjectiveMorphisms).

This implies:

+-- {: .num_prop #RetractOfIso}
###### Proposition

In every category $C$ the class of [[isomorphisms]] is preserved under retracts in the [[arrow category]] $[\Delta[1], C]$

=--

+-- {: .proof}
###### Proof

This is also checked directly: for 

$$
  \array{
    id \colon & a_1 &\to& a_2 &\to& a_1
    \\
    & \downarrow && \downarrow && \downarrow
    \\
    id \colon & b_1 &\to& b_2 &\to& b_1    
  }
$$

a retract diagram and $a_2 \to b_2$ an isomorphism, the inverse to $a_1 \to b_1$ is given by the composite

$$
  \array{
    &  & & a_2 &\to& a_1
    \\
    & && \uparrow && 
    \\
    & b_1 &\to& b_2 &&     
  }
  \,,
$$

where $b_2 \to a_2$ is the inverse of the middle morphism.

=--


### Retracts of diagrams
 {#RetractsOfDiagrams}

For the following, let $C$ and $J$ be categories and write $J^{\triangleleft}$ for the [[join of quasi-categories|join]] of $J$ with a single [[initial object]], so that [[functor]]s $J^{\triangleleft} \to C$ are precisely [[cone]]s over functors $J \to C$. Write

$$
  i : J \to J^{\triangleleft}
$$

for the canonical inclusion and hence $i^* F$ for the underlying diagram of a cone $F : J^{\triangleleft} \to C$. Finally, write $[J^{\triangleleft}, C]$ for the [[functor category]].

+-- {: .num_prop #RetractsOfLimits}
###### Proposition

If $Id: F_1 \hookrightarrow F_2 \to F_1$ is a [[retract]] in the category $[J^{\triangleleft}, C]$ and $F_2 : J^{\triangleleft} \to C$ is a [[limit]] [[cone]] over the [[diagram]] $i^* F_2 : J \to C$, then also $F_1$ is a limit cone over $i^* F_1$.

=--

+-- {: .proof}
###### Proof

We give a direct and a more abstract argument.

**Direct argument**. We can directly check the [[universal property]] of the limit: for $G$ any other [[cone]] over $i^* F_1$, the composite $i^* G = i^* F_1 \to i^* F_2$ exhibits $G$ also as a cone over $i^* F_2$. By the pullback property of $F_2$ this extends to a morphism of cones $G \to F_2$. Postcomposition with $F_2 \to F_1$ makes this a morphism of cones $G \to F_1$. By the injectivity of $F_1 \to F_2$ and the universality of $F_2$, any two such cone morphisms are equals.

**More abstract argument**. The limiting cone over a diagram $D : J \to C$ may be regarded as the right [[Kan extension]] $i_* D := Ran_i D$ along $i$

$$
  \array{   
    J &\stackrel{D}{\to}& C
    \\
    {}^{\mathllap{i}}\downarrow & \nearrow_{i_* D}
    \\
    J^{\triangleleft}
  }
  \,.
$$

Therefore a cone $F : J^{\triangleleft} \to C$ is limiting precisely if the $(i^* \dashv i_*)$-[[unit of an adjunction|unit]]

$$
  F \stackrel{}{\to} i_* i^* F
$$

is an [[isomorphism]]. Since this unit is a [[natural transformation]] it follows that applied to the retract diagram

$$
  Id : F_1 \hookrightarrow F_2 \to F_1
$$

it yields the retract diagram

$$
  \array{
    Id : & F_1 &\to& F_2 &\to& F_1
    \\ 
    & \downarrow && \downarrow && \downarrow
    \\
    Id : & i_* i^* F_1 &\to& i_* i^* F_2 &\to& i_* i^* F_1
  }
$$

in $[\Delta[1], [J^{\triangleleft}, C]]$. Here by assumption the middle morphism is an isomorphism. Since isomorphisms are stable under retract, by prop. \ref{RetractOfIso}, also the left and right vertical morphism is an isomorphism, hence also $F_1$ is a limiting cone. 

=--

This argument generalizes form limits to [[homotopy limit]]s.

For that, let now $C$ be a [[category with weak equivalences]] and write $Ho(C) : Diagram^{op} \to Cat$ for the corresponding [[derivator]]: $Ho(C)(J) := [J,C](W^J)^{-1}$ is the [[homotopy category]] of $J$-diagrams in $C$, with respect to the degreewise weak equivalences in $C$.

+-- {: .num_cor #RetractOfHomotopyLimits}
###### Corollary

Let 

$$
  Id : F_1 \to F_2 \to F_1
$$

be a retract in $Ho(C)(J^{\triangleleft})$. If $F_2$ is a [[homotopy limit]] cone over $i^* F_2$, then also $F_1$ is a homotopy limit cone over $i^* F_1$.

=--

+-- {: .proof}
###### Proof

By the discussion at [[derivator]] we have that 

1. $i_* : Ho(C)(J) \to Ho(C)(J^{\triangleleft})$ forms [[homotopy limit]] cones;

1. $F \to i_* i^* F$ is an isomorphism precisely if $F$ is a homotopy limit cone.

With this the claim follows as in prop. \ref{RetractsOfLimits}.

=--


## Related concepts

* [[retractive space]]

* [[deformation retract]], [[neighbourhood retract]]

* [[absolute retract]]

* [[dominant functor]]

## References

* [[Karol Borsuk]], _Theory of retracts_

* [[Sibe Mardešić]], _Absolute Neighborhood  Retracts and Shape  Theory_ ([pdf](https://www.maths.ed.ac.uk/~v1ranick/papers/mardesic.pdf))

* {#Borceux} [[Francis Borceux]], Def. 1.7.3 and Sec. 6.5 of: _[[Handbook of Categorical Algebra]] I_
 
See also

* Wikipedia, _[Retract](https://en.wikipedia.org/wiki/Retract)_

[[!redirects retracts]]

[[!redirects retraction]]
[[!redirects retractions]]

[[!redirects left inverse]]
[[!redirects left inverses]]
[[!redirects left-inverse]]
[[!redirects left-inverses]]

