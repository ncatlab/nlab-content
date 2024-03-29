
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Category theory
+--{: .hide}
[[!include category theory - contents]]
=--
#### Monoidal categories
+--{: .hide}
[[!include monoidal categories - contents]]
=--
=--
=--

#Contents#
* table of contents
{:toc}


## Definition

+-- {: .num_defn}
###### Definition

A **cartesian closed functor** is a [[functor]] $F\colon \mathcal{C}\to \mathcal{D}$ between [[cartesian closed categories]] which preserves both [[products]] and [[exponential objects]]/[[internal homs]] (all the structure of cartesian closed categories).

More precisely, if $F\colon \mathcal{C}\to \mathcal{D}$ preserves products, then the canonical [[morphisms]] $F(A\times B) \to F A \times F B$ (for all [[objects]] $A,B \in \mathcal{C}$) are [[isomorphisms]], and we therefore have canonical induced morphisms $F[A,B] \to [F A, F B]$ --- the [[adjuncts]] of the composites $F[A,B] \times F A \xrightarrow{\cong} F([A,B] \times A) \to F B$.  $F$ is **cartesian closed** if these maps $F[A,B] \to [F A, F B]$ are also isomorphisms.

=--

+-- {: .num_remark}
###### Remark

When cartesian closed categories are identified with [[cartesian monoidal categories]] that are also [[closed monoidal category|closed monoidal]], a cartesian closed functor can be identified with a [[strong monoidal functor]] which is also [[strong closed functor|strong closed]].

=--

## Properties

+-- {: .num_prop #FrobeniusReciprocity}
###### Proposition
**(Frobenius reciprocity)**

Let $R : \mathcal{C} \to \mathcal{D}$ be a [[functor]] between [[cartesian closed categories]] with a [[left adjoint]] $L$. Then $R$ is cartesian closed precisely if the [[natural transformation]]

$$
  (L \pi_1, \epsilon_A L \pi_2)
  : 
  L(B \times R(A))
  \to 
  L(B) \times A
$$

is an [[isomorphism]].

=--

+-- {: .proof}
###### Proof

The above natural transformation is the [[mate]] of the exponential comparison natural transformation $R[A,B] \to [R A, R B]$ under the composite adjunctions
$$
\mathcal{C}
\underoverset{R}{L}{\leftrightarrows}
\mathcal{D}
\underoverset{[R A, -]}{- \times R A}{\leftrightarrows}
\mathcal{D}
$$
and
$$
\mathcal{C}
\underoverset{[A,-]}{A\times -}{\leftrightarrows}
\mathcal{C} 
\underoverset{R}{L}{\leftrightarrows}
\mathcal{D}
$$

=--

This is called the **[[Frobenius reciprocity]]** law.  It is discussed, for instance, as ([Johnstone, lemma 1.5.8](#Johnstone)). More generally for closed monoidal categories (not necessarily cartesian monoidal) it is discussed in "[[Wirthmüller contexts]]" in 

Let still $R$ and $L$ be as above.

+-- {: .num_cor}
###### Corollary

If $R$ is [[full and faithful]] and $L$ preserves binary [[products]], then $R$ is cartesian closed.

=--

For instance ([Johnstone, corollary A1.5.9](#Johnstone)).

## Examples
 {#Examples}

+-- {: .num_prop}
###### Proposition

For $\mathcal{C}$ a [[locally cartesian closed category]] and $f : X_1 \to X_2$ a [[morphism]], the [[base change]]/[[pullback]] functor between the [[slice categories]]

$$
  f^* : \mathcal{C}_{/X_2} \to \mathcal{C}_{/X_1} 
$$
 
is cartesian closed.

In particular the [[inverse image]] functor of an [[étale geometric morphism]] between [[toposes]] is cartesian closed and hence constitutes a cartesian [[Wirthmüller context]].

=--

+-- {: .proof}
###### Proof

The functor $f^*$ has a [[left adjoint]]

$$
  \sum_f : \mathcal{C}_{/X_1} \to \mathcal{C}_{/X_2}
$$

given by postcomposition with $f$ (the [[dependent sum]] along $f$). Therefore by prop. \ref{FrobeniusReciprocity} it is sufficient to show that 
for all $(A \to X_2) \in \mathcal{C}_{/X_2}$ and $(B \stackrel{b}{\to} X_1) \in \mathcal{C}_{/X_1}$ that

$$
  B \times_{X_1} f^* A \simeq B \times_{X_2} A
$$

in $\mathcal{C}$. But this is the [[pasting law]] for pullbacks in $\mathcal{C}$, which says that the two consecutive pullbacks on the left of

$$
  \array{
    B \times_{X_1} f^* A &\to& f^* A &\to& A 
    \\
    \downarrow && \downarrow && \downarrow
    \\
    B &\stackrel{b}{\to}& X_1 &\stackrel{f}{\to}& X_2  
  }  
  \;\;\;
  \simeq
  \;\;\;
  \array{
    (b \circ f)^* A &\to&  &\to& A 
    \\
    \downarrow &&  && \downarrow
    \\
    B &\stackrel{b}{\to}& X_1 &\stackrel{f}{\to}& X_2  
  }  
$$

are isomorphic to the direct pullback along the composite on the right.

=--


## Related concepts

* [[strong functor]]

* [[cartesian closed category]], [[locally cartesian closed category]]

* **cartesian closed functor**, [[locally cartesian closed functor]]

* [[cartesian closed model category]], [[locally cartesian closed model category]]

* [[cartesian closed (∞,1)-category]], [[locally cartesian closed (∞,1)-category]]


## References

For instance section A1.5 of 

* [[Peter Johnstone]], _[[Sketches of an Elephant]]_
 {#Johnstone}

Also

* H. Fausk, P. Hu, [[Peter May]],  _Isomorphisms between left and right adjoints_, Theory and Applications of Categories , Vol. 11, 2003, No. 4, pp 107-131. ([TAC](http://www.tac.mta.ca/tac/volumes/11/4/11-04abs.html), [pdf](http://www.math.uiuc.edu/K-theory/0573/FormalFeb16.pdf))
 {#May05}

[[!redirects cartesian closed functors]]