
+-- {: .rightHandSide}
+-- {: .toc .clickDown tabindex="0"}
###Context###
#### Cohomology
+--{: .hide}
[[!include cohomology - contents]]
=--
#### Algebraic topology
+--{: .hide}
[[!include algebraic topology - contents]]
=--
#### Homological algebra
+--{: .hide}
[[!include homological algebra - contents]]
=--
=--
=--


#Contents#
* table of contents
{:toc}

## Idea

The _Thom-Gysin sequence_ is a type of [[long exact sequence in cohomology]] induced by a [[spherical fibration]] and expressing the [[cohomology groups]] of the total space in terms of those of the base plus correction. The sequence may be obtained as a corollary of the [[Serre spectral sequence]] for the given fibration. It induces, and is induced by, the [[Thom isomorphism]].

## Statement
 {#Statement}


+-- {: .num_prop #ThomGysinSequence}
###### Proposition

Let $R$ be a [[commutative ring]] and let

$$
  \array{
    S^n &\longrightarrow& E
    \\
    && \downarrow^{\mathrlap{\pi}}
    \\
    && B
  }
$$

be a [[Serre fibration]] over a [[simply connected topological space|simply connected]] [[CW-complex]] with typical [[fiber]] ([exmpl.](Introduction+to+Stable+homotopy+theory+--+P#FibersOfSerreFibrations)) the [[n-sphere]].

Then there exists an element $c \in H^{n+1}(E; R)$ (in the [[ordinary cohomology]] of the total space with [[coefficients]] in $R$, called the _[[Euler class]]_ of $\pi$) such that the [[cup product]] operation $c \cup (-)$ sits in a [[long exact sequence]] of [[cohomology groups]] of the form

$$
  \cdots 
   \to 
   H^k(B; R) 
     \stackrel{\pi^\ast}{\longrightarrow}
   H^k(E; R)
    \stackrel{}{\longrightarrow}
   H^{k-n}(B;R)
   \stackrel{c \cup (-)}{\longrightarrow}
   H^{k+1}(B; R)
   \to
   \cdots
  \,.
$$

=--

(e.g. [Switzer 75, section 15.30](#Switzer75), [Kochman 96, corollary 2.2.6](#Kochmann96))

+-- {: .proof #ProofOfThomGysinSequence}
###### Proof

Under the given assumptions there is the corresponding [[Serre spectral sequence]] 

$$
  E_2^{s,t}
    \;=\;
  H^s(B; H^t(S^n;R))
    \;\Rightarrow\;
  H^{s+t}(E; R)
  \,.
$$

Since the [[ordinary cohomology]] of the [[n-sphere]] [[fiber]] is concentrated in just two degees

$$
  H^t(S^n; R)
  =
  \left\{
    \array{
      R & for \; t= 0 \; and \; t = n
      \\
      0 & otherwise
    }
  \right.
$$

the only possibly non-vanishing terms on the $E_2$ page of this spectral sequence, and hence on all the further pages, are in bidegrees $(\bullet,0)$ and $(\bullet,n)$:

$$
  E^{\bullet,0}_2 \simeq H^\bullet(B; R)
  \,,
  \;\;\;\;
  and
  \;\;\;
  E^{\bullet,n}_2 \simeq H^\bullet(B; R)
  \,.
$$

As a consequence, since the differentials $d_r$ on the $r$th page of the Serre spectral sequence have bidegree $(r+1,-r)$, the only possibly non-vanishing differentials are those on the $(n+1)$-page of the form

$$
  \array{
     E_{n+1}^{\bullet,n} & \simeq & H^\bullet(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow
     \\
     E_{n+1}^{\bullet+n+1,0} & \simeq &  H^{\bullet+n+1}(B;R)
  }
  \,.
$$

Now since the [[coefficients]] $R$ is a [[ring]], the [[Serre spectral sequence]] is [[multiplicative spectral sequence|multiplicative]] under [[cup product]] and the [[differential]] is a [[derivation]] (of total degree 1) with respect to this product. (See at _[multiplicative spectral sequence -- Examples -- AHSS for multiplicative cohomology](multiplicative+spectral+sequence#AHSSForMultiplicativeCohomology)_.)

To make use of this, write

$$
  \iota \coloneqq 1 \in H^0(B;R) \stackrel{\simeq}{\longrightarrow} E_{n+1}^{0,n} 
$$

for the unit in the [[cohomology ring]] $H^\bullet(B;R)$, but regarded as an element in bidegree $(0,n)$ on the $(n+1)$-page of the spectral sequence. (In particular $\iota$ does _not_ denote the unit in bidegree $(0,0)$, and hence $d_{n+1}(\iota)$ need not vanish; while by the [[derivation]] property, it does vanish on the actual unit $1 \in H^0(B;R) \simeq E_{n+1}^{0,0}$.)

Write

$$
  c 
    \coloneqq 
  d_{n+1}(\iota) 
   \;\;
  \in E_{n+1}^{n+1,0} 
    \stackrel{\simeq}{\longrightarrow} 
  H^{n+1}(B; R)
$$

for the image of this element under the differential. We will show that this is the Euler class in question.

To that end, notice that every element in $E_{n+1}^{\bullet,n}$ is of the form $\iota \cdot b$ for $b\in E_{n+1}^{\bullet,0} \simeq H^\bullet(B;R)$. 

(Because the [[multiplicative spectral sequence|multiplicative structure]] gives a group homomorphism $\iota \cdot(-) \colon H^\bullet(B;R) \simeq E_{n+1}^{0,0} \to E^{0,n}_{n+1} \simeq H^\bullet(B;R)$, which is an isomorphism because the product in the spectral sequence does come from the [[cup product]] in the [[cohomology ring]], see for instance [Kochman 96, first equation in the proof of prop. 4.2.9](#Kochmann96), and since hence $\iota$ does act like the unit that it is in $H^\bullet(B;R)$). 


Now since $d_{n+1}$ is a graded [[derivation]] and vanishes on $E_{n+1}^{\bullet,0}$ (by the above degree reasoning), it follows that its action on any element is uniquely fixed to be given by the product with $c$:

$$
  \begin{aligned}
    d_{n+1}(\iota \cdot b)
      & =
    d_{n+1}(\iota) \cdot b + (-1)^{n}\, \iota \cdot \underset{= 0}{\underbrace{d_{n+1}(b)}}
    \\
    & = c \cdot b
  \end{aligned}
  \,.
$$

This shows that $d_{n+1}$ is identified with the cup product operation in question:

$$
  \array{
     E_{n+1}^{s,n} & \simeq & H^s(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow && \downarrow^{\mathrlap{c \cup (-)}}
     \\
     E_{n+1}^{s+n+1, 0} & \simeq & H^{s+n+1}(B;R)
  }
  \,.
$$

In summary, the non-vanishing entries of the $E_\infty$-page of the spectral sequence sit in [[exact sequences]] like so

$$
  \array{
     0
     \\
     \downarrow
     \\
     E_\infty^{s,n}
     \\
     {}^{\mathllap{ker(d_{n+1})}}\downarrow
     \\
     E_{n+1}^{s,n} & \simeq & H^s(B;R)
     \\
     {}^{\mathllap{d_{n+1}}}\downarrow && \downarrow^{\mathrlap{c \cup (-)}}
     \\
     E_{n+1}^{s+n+1, 0} & \simeq & H^{s+n+1}(B;R)
     \\
     {}^{\mathllap{coker(d_{n+1})}}\downarrow
     \\
     E_\infty^{s+n+1,0}
     \\
     \downarrow
     \\
     0
  }  
  \,.
$$

Finally observe (lemma \ref{ImplicationsOfSparesnessOfSSSForSphericalFibration}) that due to the sparseness of the $E_\infty$-page, there are also [[short exact sequences]] of the form

$$
  0 \to E_\infty^{s,0} \longrightarrow H^s(E; R) \longrightarrow  E_\infty^{s-n,n} \to 0
  \,.
$$

Concatenating these with the above exact sequences yields the desired [[long exact sequence]].

=--

+-- {: .num_lemma #ImplicationsOfSparesnessOfSSSForSphericalFibration}
###### Lemma

Consider a cohomology [[spectral sequence]] converging to some [[filtered object|filtered]] [[graded abelian group]] $F^\bullet C^\bullet$ such that 

1. $F^0 C^\bullet = C^\bullet$;

1. $F^{s} C^{\lt s} = 0$;

1. $E_\infty^{s,t} = 0$ unless $t = 0$ or $t = n$, 

for some $n \in \mathbb{N}$, $n \geq 1$. Then there are [[short exact sequences]] of the form

$$
  0 \to E_\infty^{s,0} \overset{}{\longrightarrow} C^s \longrightarrow  E_\infty^{s-n,n} \to 0
  \,.
$$

=--

(e.g. [Switzer 75, p. 356](#Switzer75))

+-- {: .proof}
###### Proof

By definition of convergence of a spectral sequence, the $E_{\infty}^{s,t}$ sit in [[short exact sequences]] of the form

$$
  0 \to F^{s+1}C^{s+t} \overset{i}{\longrightarrow} F^s C^{s+t} \longrightarrow E_\infty^{s,t} \to 0
  \,.
$$

So when $E_\infty^{s,t} = 0$ then the morphism $i$ above is an [[isomorphism]].

We may use this to either shift away the filtering degree

* if $t \geq n$ then $F^s C^{s+t} = F^{(s-1)+1}C^{(s-1)+(t+1)} \underoverset{\simeq}{i^{s-1}}{\longrightarrow} F^0 C^{(s-1)+(t+1)} = F^0 C^{s+t} \simeq C^{s+t}$;

or to shift away the offset of the filtering to the total degree:

* if $0 \leq t-1 \leq n-1$ then $F^{s+1}C^{s+t} = F^{s+1}C^{(s+1)+(t-1)} 
  \underoverset{\simeq}{i^{-(t-1)}}{\longrightarrow} F^{s+t}C^{(s+1)+(t-1)} = F^{s+t}C^{s+t}$

Moreover, by the assumption that if $t \lt 0$ then $F^{s}C^{s+t} = 0$, we also get

$$
  F^{s}C^{s} \simeq E_\infty^{s,0}
  \,.
$$

In summary this yields the vertical isomorphisms

$$
  \array{
  0 
    &\to& 
  F^{s+1}C^{s+n} 
    &\longrightarrow& 
  F^{s}C^{s+n} 
    &\longrightarrow& 
  E_\infty^{s,n} 
    &\to& 
  0
  \\
  && 
    {}^{\mathllap{i^{-(n-1)}}}\downarrow^{\mathrlap{\simeq}} 
  &&
    {}^{\mathllap{i^{s-1}}}\downarrow^{\mathrlap{\simeq}}
  &&
    \downarrow^{\mathrlap{=}}
  \\
  0 
    &\to& 
  F^{s+n}C^{s+n}
  \simeq
  E_\infty^{s+n,0} 
    &\longrightarrow& 
  C^{s+n} 
    &\longrightarrow& 
  E_\infty^{s,n}
    &\to& 
  0
  }
$$

and hence with the top sequence here being exact, so is the bottom sequence.

=--


## Related concepts

* [[Gysin map]]

* [[Serre long exact sequence]]

* [[Serre spectral sequence]]

## References

* {#Switzer75} [[Robert Switzer]], section 15.30 of _Algebraic Topology - Homotopy and Homology_, Die  Grundlehren der Mathematischen Wissenschaften in Einzeldarstellungen, Vol. 212, Springer-Verlag, New York, N. Y., 1975 ([doi:10.1007/978-3-642-61923-6](https://link.springer.com/book/10.1007/978-3-642-61923-6))


* [[James Milne]], section 16 of _[[Lectures on Étale Cohomology]]_

See also:

* Wikipedia, _[Gysin sequence](http://en.wikipedia.org/wiki/Gysin_sequence)_


In the generality of [[complex oriented cohomology theory]]:

* {#Kochmann96} [[Stanley Kochmann]], section 2.2. of _[[Bordism, Stable Homotopy and Adams Spectral Sequences]]_, AMS 1996

* [[Dai Tamaki]], [[Akira Kono]], Section 3.8 in: _Generalized Cohomology_, Translations of Mathematical Monographs, American Mathematical Society, 2006 ([ISBN: 978-0-8218-3514-2](https://bookstore.ams.org/mmono-230))


Formalization in [[homotopy type theory]]:

* {#Brunerie16} [[Guillaume Brunerie]], _On the homotopy groups of spheres in homotopy type theory_ ([arXiv:1606.05916](http://arxiv.org/abs/1606.05916))

Applications:

* [[Martin Saralegi]], _A Gysin Sequence for Semifree Actions of $S^3$_, Proceedings of the American Mathematical Society Vol. 118, No. 4 (Aug., 1993), pp. 1335-1345 ([jstor](http://www.jstor.org/stable/2160096))


[[!redirects Thom-Gysin sequences]]

[[!redirects Thom-Gysin exact sequence]]
[[!redirects Thom-Gysin exact sequences]]

[[!redirects Gysin sequence]]
[[!redirects Gysin sequences]]

[[!redirects Gysin exact sequence]]
[[!redirects Gysin exact sequences]]